---
title: Customer Insights APIetarako OData kontsultaren adibideak
description: Gehien erabiltzen diren Open Data Protocol (OData)-ren adibideak Customer Insights APIak kontsultatzeko datuak berrikusteko.
ms.date: 08/30/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 26e56a3bab01ba55284a52e72efbcbfbaadaad6f
ms.sourcegitcommit: 624b27bb65a0de1970dc1ac436643b493f0a31cf
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387187"
---
# <a name="odata-query-examples-for-customer-insights-apis"></a>Customer Insights APIetarako OData kontsultaren adibideak

Open Data Protocol (OData) datuetara sartzeko protokolo bat da, HTTP bezalako protokolo nagusietan eraikia. Sarerako REST bezalako metodologia onartuak erabiltzen ditu. OData zerbitzuak kontsumitzeko erabil daitezkeen hainbat liburutegi eta tresna mota daude.

Zure inplementazio propioak eraikitzen laguntzeko [Customer Insights APIak](apis.md) , berrikusi maiz eskatzen diren adibide-kontsulta batzuk.

Aldatu kontsulta-laginak xede-inguruneetan funtzionatzeko:

- {serviceRoot}:`https://api.ci.ai.dynamics.com/v1/instances/{instanceId}/data` non{instanceId} kontsultatu nahi duzun Customer Insights ingurunearen GUID da. The [ListAllInstances eragiketa](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances) aurkitzen uzten dizu{InstanceId} sarbidea duzu.
- {CID}: bezeroen erregistro bateratu baten GUID. Adibidez: `ce759201f786d590bf2134bff576c369`.
- {AlternateKey}: datu-iturburu batean bezero-erregistro baten gako nagusiaren identifikatzailea. Adibidez: `CNTID_1002`
- {DSname}: Customer Insights-en irensten den datu-iturburu baten entitate-izena duen katea. Adibidez: `Website_contacts`.
- {SegmentName}: Customer Insights-en segmentu baten irteerako entitatearen izena duen katea. Adibidez: `Male_under_40`.

## <a name="customer"></a>bezero hori

Lagin-kontsultak *Bezeroa* entitate.

|Kontsulta mota |Adibidez  | Oharra  |
|---------|---------|---------|
|Bezeroaren ID bakarra     | `{serviceRoot}/Customer?$filter=CustomerId eq '{CID}'`          |  |
|ordezko gako    | `{serviceRoot}/Customer?$filter={DSname_EntityName_PrimaryKeyColumnName} eq '{AlternateKey}'`         |  Ordezko gakoek bezeroaren entitate bateratuan jarraitzen dute       |
|Select   | `{serviceRoot}/Customer?$select=CustomerId,FullName&$filter=customerid eq '1'`        |         |
|Denbora hau barru:    | `{serviceRoot}/Customer?$filter=CustomerId in ('{CID1}',’{CID2}’)`        |         |
|ordezko gako + In   | `{serviceRoot}/Customer?$filter={DSname_EntityName_PrimaryKeyColumnName} in ('{AlternateKey}','{AlternateKey}')`         |         |
|Bilatu?  | `{serviceRoot}/Customer?$top=10&$skip=0&$search="string"`        |   Bilaketa-kate baten 10 emaitza nagusiak ematen ditu      |
|Segmentuko kidetasuna  | `{serviceRoot}/Customer?select=*&$filter=IsMemberOfSegment('{SegmentName}')&$top=10`     | Segmentazio-entitatearen errenkada-kopuru aurrez ezarritakoa ematen du.      |
|Segmentatu bezero baten kidetasuna | `{serviceRoot}/Customer?$filter=CustomerId eq '{CID}'&IsMemberOfSegment('{SegmentName}')`     | Bezeroaren profila ematen du emandako segmentuko kidea bada     |

## <a name="unified-activity"></a>Jarduera bateratua

Lagin-kontsultak *Jarduera bateratua* entitate.

|Kontsulta mota |Adibidez  | Oharra  |
|---------|---------|---------|
|CIDren jarduera     | `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq '{CID}'`          | Bezero-profil jakin bateko jarduerak zerrendatzen ditu |
|Jardueraren denbora tartea    | `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq '{CID}' and ActivityTime gt 2017-01-01T00:00:00.000Z and ActivityTime lt 2020-01-01T00:00:00.000Z`     |  Bezeroen profilaren jarduerak denbora-tarte batean       |
|Jarduera mota    |   `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq '{CID}' and ActivityType eq '{ActivityName}'`        |         |
|Jarduera bistaratzeko izenaren arabera     | `{serviceRoot}/UnifiedActivity$filter=CustomerId eq ‘{CID}’ and ActivityTypeDisplay eq ‘{ActivityDisplayName}’`        | |
|Jarduerak ordenatzea    | `{serviceRoot}/UnifiedActivity?$filter=CustomerId eq ‘{CID}’ & $orderby=ActivityTime asc`     |  Jarduerak goranzko edo beheranzko ordenatu       |
|Jarduera segmentu-kidetasunetik zabaldu da  |   `{serviceRoot}/Customer?$expand=UnifiedActivity,Customer_Measure&$filter=CustomerId eq '{CID}'`     |         |

## <a name="other-examples"></a>Beste adibide batzuk

Beste entitateentzako kontsulta laginak.

|Kontsulta mota |Adibidez  | Oharra  |
|---------|---------|---------|
|CIDren neurriak    | `{serviceRoot}/Customer_Measure?$filter=CustomerId eq '{CID}'`          |  |
|CID marka aberastuak    | `{serviceRoot}/BrandShareOfVoiceFromMicrosoft?$filter=CustomerId eq '{CID}'`  |       |
|CIDren interes aberastuak    |   `{serviceRoot}/InterestShareOfVoiceFromMicrosoft?$filter=CustomerId eq '{CID}'`       |         |
|Klausula barne + Zabaldu     | `{serviceRoot}/Customer?$expand=UnifiedActivity,Customer_Measure&$filter=CustomerId in ('{CID}', '{CID}')`         | |

## <a name="not-supported-odata-queries"></a>Ez dira onartzen OData kontsultak

Kontsulta hauek ez ditu onartzen Customer Insights-ek:

- `$filter` irensten diren iturburu-entitateetan. Customer Insights-ek sortzen dituen sistema-entitateetan $filter kontsultak bakarrik exekutatu ditzakezu.
- `$expand` batetik`$search` kontsulta. Adibidez: `Customer?$expand=UnifiedActivity$top=10&$skip=0&$search="corey"`
- `$expand` tik`$select` atributu azpimultzo bat bakarrik hautatzen bada. Adibidez: `Customer?$select=CustomerId,FullName&$expand=UnifiedActivity&$filter=CustomerId eq '{CID}'`
- `$expand` bezero jakin baterako marka aberastu edo interes-afintasunak. Adibidez: `Customer?$expand=BrandShareOfVoiceFromMicrosoft&$filter=CustomerId eq '518291faaa12f6d853c417835d40eb10'`
- Kontsultatu iragarpen ereduaren irteerako entitateak ordezko gako bidez. Adibidez: `OOBModelOutputEntity?$filter=HotelCustomerID eq '{AK}'`
