---
title: OData adibideak Dynamics 365 Customer Insights APIak
description: Gehien erabiltzen diren Open Data Protocol (OData)-ren adibideak Customer Insights APIak kontsultatzeko datuak berrikusteko.
ms.date: 05/10/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 007278e1330e1a8e64d524ded8496acaf83b874c
ms.sourcegitcommit: a50c5e70d2baf4db41a349162fd1b1f84c3e03b6
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740060"
---
# <a name="odata-query-examples"></a>OData kontsultaren adibideak

Open Data Protocol (OData) datuetara sartzeko protokolo bat da, HTTP bezalako protokolo nagusietan eraikia. Sarean REST bezalako onartutako metodologiak erabiltzen ditu. OData zerbitzuak kontsumitzeko hainbat liburutegi eta tresna mota daude.

Artikulu honek maiz eskatzen diren adibide-kontsulta batzuk zerrendatzen ditu, zure inplementazio propioak eraikitzen laguntzeko [Customer Insights APIak](apis.md).

Kontsulten laginak aldatu behar dituzu xede inguruneetan funtzionatzeko: 

- {serviceRoot}:`https://api.ci.ai.dynamics.com/v1/instances/{instanceId}` non{instanceId} kontsultatu nahi duzun Customer Insights ingurunearen GUID da. The [ListAllInstances eragiketa](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances) aurkitzen uzten dizu{InstanceId} sarbidea duzu.
- {CID}: bezeroen erregistro bateratu baten GUID. Adibidez: `ce759201f786d590bf2134bff576c369`.
- {AlternateKey}: Bezero-erregistro baten lehen gakoaren identifikatzailea datu-iturburu batean. Adibidez: `CNTID_1002`
- {DSname}: Customer Insights-en irensten den datu-iturburu baten entitate-izena duen katea. Adibidez: `Website_contacts`.
- {SegmentName}: Customer Insights-en segmentu baten irteerako entitatearen izena duen katea. Adibidez: `Male_under_40`.

## <a name="customer"></a>bezero hori

Hurrengo taulak lagin-kontsulten multzo bat dauka *Bezeroa* entitate.


|Kontsulta mota |Adibidez  | Oharra  |
|---------|---------|---------|
|Bezeroaren ID bakarra     | `{serviceRoot}/Customer?$filter=CustomerId eq '{CID}'`          |  |
|Ordezko gako    | `{serviceRoot}/Customer?$filter={DSname_EntityName_PrimaryKeyColumnName} eq '{AlternateKey}' `         |  Ordezko gakoek bezeroaren entitate bateratuan jarraitzen dute       |
|Select   | `{serviceRoot}/Customer?$select=CustomerId,FullName&$filter=customerid eq '1'`        |         |
|Denbora hau barru:    | `{serviceRoot}/Customer?$filter=CustomerId in ('{CID1}',’{CID2}’)`        |         |
|Ordezko gako + In   | `Customer?$filter={DSname_EntityName_PrimaryKeyColumnName} in ('{AlternateKey}','{AlternateKey}')`         |         |
|Bilatu?  | `{serviceRoot}/Customer?$top=10&$skip=0&$search="string"`        |   Bilaketa-kate baten lehen 10 emaitza ematen ditu      |
|Segmentuko kidetasuna  | `{serviceRoot}/Customer?select=*&$filter=IsMemberOfSegment('{SegmentName}')&$top=10  `     | Segmentazio-entitatearen errenkada-kopuru aurrez ezarritakoa itzultzen du.      |

## <a name="unified-activity"></a>Jarduera bateratua

Hurrengo taulak lagin-kontsulten multzo bat dauka *Jarduera bateratua* entitate.

|Kontsulta mota |Adibidez  | Oharra  |
|---------|---------|---------|
|CIDren jarduera     | `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq '{CID}'`          | Bezero-profil zehatz bateko jarduerak zerrendatzen ditu |
|Jardueraren denbora tartea    | `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq '{CID}' and ActivityTime gt 2017-01-01T00:00:00.000Z and ActivityTime lt 2020-01-01T00:00:00.000Z`     |  Bezeroaren profilaren jarduerak denbora tarte batean       |
|Jarduera mota    |   `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq '{CID}' and ActivityType eq '{ActivityName}'`        |         |
|Jarduera bistaratzeko izenaren arabera     | `{serviceRoot}/UnifiedActivity$filter=CustomerId eq ‘{CID}’ and ActivityTypeDisplay eq ‘{ActivityDisplayName}’ `        | |
|Jarduerak ordenatzea    | `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq ‘{CID}’ & $orderby=ActivityTime asc`     |  Jarduerak goranzko edo beheranzko ordenatu       |
|Jarduera segmentu-kidetasunetik zabaldu da  |   `{serviceRoot}/Customer?$expand=UnifiedActivity,Customer_Measure&$filter=CustomerId eq '{CID}'`     |         |

## <a name="other-examples"></a>Beste adibide batzuk

Ondorengo taulak beste entitate batzuetarako lagin-kontsulten multzoa dauka.

|Kontsulta mota |Adibidez  | Oharra  |
|---------|---------|---------|
|CIDren neurriak    | `{serviceRoot}/Customer_Measure?$filter=CustomerId eq '{CID}'`          |  |
|CID marka aberastuak    | `{serviceRoot}/BrandShareOfVoiceFromMicrosoft?$filter=CustomerId eq '{CID}'`  |       |
|CIDren interes aberastuak    |   `{serviceRoot}/InterestShareOfVoiceFromMicrosoft?$filter=CustomerId eq '{CID}'`       |         |
|Klausula barne + Zabaldu     | `{serviceRoot}/Customer?$expand=UnifiedActivity,Customer_Measure&$filter=CustomerId in ('{CID}', '{CID}')`         | |
