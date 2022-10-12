---
title: Datuen iturburuen ikuspegi orokorra
description: Ikasi hainbat iturritatik datuak inportatu edo sartzen.
ms.date: 09/29/2022
ms.subservice: audience-insights
ms.topic: overview
author: mukeshpo
ms.author: mukeshpo
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-data-sources
- ci-create-data-source
- customerInsights
ms.openlocfilehash: f89da3cf5b56e367bd673740f80cd82ec0907b28
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610037"
---
# <a name="data-sources-overview"></a>Datuen iturburuen ikuspegi orokorra

Dynamics 365 Customer Insights konexioak eskaintzen ditu iturri multzo zabal bateko datuak ekartzeko. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak hartu ondoren, egin dezakezu [bateratu](data-unification.md), ikuspegiak sortu eta datuak aktibatu esperientzia pertsonalizatuak eraikitzeko.

## <a name="add-or-edit-data-sources"></a>Gehitu edo editatu datu-iturriak

Datu-iturriak erantsi edo inporta ditzakezu Customer Insights-era. Beheko esteketan datu-iturriak gehitzeko eta editatzeko argibideak ematen dira.

**Erantsi datu-iturburu bat**

Microsoft-en Azure datu-zerbitzuetako batean datuak prestatuta badituzu, Customer Insights erraz konekta daiteke datu-iturburu-ra datuak berriro sartu beharrik gabe. Hautatu aukera hauetariko bat:
- [Azure Data Lake Storage(csv edo parquet fitxategiak Common Data Model karpeta batean)](connect-common-data-model.md)
- [Azure Synapse Analytics(Lakuen datu-baseak)](connect-synapse.md)
- [Microsoft Dataverse datu-lakua](connect-dataverse-managed-lake.md)

**Inportatu eta eraldatu**

Datu iturri lokalak, Microsoft edo hirugarrenen datuak erabiltzen badituzu, inportatu eta eraldatu datuak erabiliz Power Query konektoreak.
- [Power Query konektoreak](connect-power-query.md)

## <a name="review-data-sources"></a>Berrikusi datu-iturriak

Zure ingurunea Customer Insights biltegia erabiltzeko konfiguratuta bazegoen eta tokiko datu-iturburuak erabiltzen badituzu, erabiltzen duzu Power Platform datu-fluxuak. Horrekin Power Platform datu-fluxuak, partekatutako datu-iturriak eta besteek kudeatutako datu-iturriak ikus ditzakezu. The **Datu-iturriak** orrialdeak hiru ataletan zerrendatzen ditu datu-iturriak:
- **Partekatua** : Customer Insights administratzaile guztiek kudeatu ditzaketen datu-iturriak. Power Platform datu-fluxuak, zure biltegiratze-kontua eta a Dataverse -kudeatutako data lake partekatutako datu-iturrien adibideak dira.
- **Nik kudeatzen dut** :Power Platform Zuk bakarrik sortu eta kudeatutako datu-fluxuak. Customer Insights-eko beste administratzaileek datu-fluxu hauek soilik ikus ditzakete, baina ez editatu, freskatu edo ezabatu.
- **Beste batzuek kudeatzen dute** :Power Platform beste administratzaile batzuek sortutako datu-fluxuak. Horiek bakarrik ikus ditzakezu. Edozein laguntza lortzeko harremanetan jartzeko datu-fluxuaren jabea zerrendatzen du.
> [!NOTE]
> Entitate guztiak beste erabiltzaileek ikusi eta erabil ditzakete. Datu-iturriak sortu dituen erabiltzailearen jabetzakoak diren arren, datuen ingestetik sortutako entitateak Customer Insights-eko erabiltzaile guztiek erabil ditzakete.

Zure inguruneak erabiltzen ez badu Power Platform datu-fluxuak, **Datu-iturriak** orrialdeak datu-iturburu guztien zerrenda baino ez dauka. Ez dago atalik bistaratzen.

## <a name="manage-existing-data-sources"></a>Kudeatu lehendik dauden datu-iturriak

Joan **Datuak** > **Datu-iturriak** irensten den datu-iturburu bakoitzaren izena, bere egoera eta iturri horren datuak azken aldiz freskatu diren ikusteko. Datu-iturburuen zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun datu-iturburu aurkitzeko.

Hautatu datu-iturburu bat erabilgarri dauden ekintzak ikusteko.

:::image type="content" source="media/data_sources_showmore.png" alt-text="Gehitutako datu-iturriak.":::

- [**Editatu**](#add-or-edit-data-sources) datu-iturburu bere propietateak aldatzeko.
- [**Freskatu**](#refresh-data-sources) datu-iturburu azken datuak sartzeko.
- [**Aberastu**](data-sources-enrichment.md) datu-iturburu bateratu aurretik.
- **Ezabatu** datu-iturburu. datu-iturburu bat ezabatu daiteke datuak prozesamendu batean erabiltzen ez badira, hala nola bateratzean, ikuspegietan, aktibazioetan edo esportazioetan.

## <a name="refresh-data-sources"></a>Freskatu datu-iturburuak

Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera. [Datu iturri lokalak](connect-power-query.md#add-data-from-on-premises-data-sources) freskatu datuak sartzerakoan konfiguratutako ordutegiak. Arazoak konpontzeko aholkuak ikusteko, ikus [Arazoak konpondu PPDF Power Query -oinarritutako datu-iturburu freskatze arazoak](connect-power-query.md#troubleshoot-ppdf-power-query-based-data-source-refresh-issues).

Erantsitako datu-iturburuetarako, datuak barneratzeak datu-iturburu horren eskura dauden azken datuak kontsumitzen ditu.

Joan **Admin** > **Sistema** > [**Ordutegia**](schedule-refresh.md) sartutako datu-iturburuen sistemak programatutako freskaketak konfiguratzeko.

Eskaeraren arabera datu-iturburu bat freskatzeko:

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu freskatu nahi duzun datu-iturburu eta hautatu **Freskatu**. Datu-iturburua eskuz eguneratzeko aktibatuta dago. datu-iturburu freskatzeak entitatearen eskema eta datuak eguneratuko ditu datu-iturburu-en zehaztutako entitate guztientzat.

1. Hautatu egoera irekitzeko **Aurrerapen xehetasunak** panela eta ikusi aurrerapena. Lana bertan behera uzteko, hautatu **Utzi lana** panelaren behealdean.

## <a name="corrupt-data-sources"></a>Datu iturri hondatuak

Irensten ari diren datuek erregistro hondatuak izan ditzakete eta horrek datuak sartzeko prozesua akatsekin edo abisuekin osatzea eragin dezake.

> [!NOTE]
> Datuak sartzea akatsekin amaitzen bada, datu-iturburu hau aprobetxatzen duen ondorengo prozesaketa (adibidez, bateratzea edo jarduera sortzea) saltatu egingo da. Irenstea abisuekin osatzen bada, ondorengo prozesamenduak jarraitzen du, baina baliteke erregistro batzuk ez egotea.

Akats hauek zereginen xehetasunetan ikus daitezke.

:::image type="content" source="media/corrupt-task-error.png" alt-text="Datu hondatuta dagoen errorea erakusten duen zereginaren xehetasunak.":::

Erregistro hondatuak sistemak sortutako entitateetan erakusten dira.

### <a name="fix-corrupt-data"></a>Konpondu datu hondatuak

1. Datu hondatuak ikusteko, joan hona **Datuak** > **Entitateak** eta hondatutako entitateak bilatu **Sistema** atala. Hondatutako entitateen izen-eskema: 'DataSourceName_EntityName_corrupt'.

1. Hautatu hondatutako entitate bat eta gero **Datuak** fitxa.

1. Identifikatu erregistro batean hondatutako eremuak eta arrazoia.

   :::image type="content" source="media/corruption-reason.png" alt-text="Ustelkeria arrazoia." lightbox="media/corruption-reason.png":::

   > [!NOTE]
   > **Datuak** > **Entitateak** hondatutako erregistroen zati bat bakarrik erakutsi. Erregistro hondatu guztiak ikusteko, esportatu fitxategiak biltegiratze-kontuko edukiontzi batera [Customer Insights esportatzeko prozesua](export-destinations.md). Zure biltegiratze-kontua erabili baduzu, biltegiratze-kontuko Customer Insights karpeta ere begiratu dezakezu.

1. Konpondu hondatutako datuak. Adibidez, Azure Data Lake datu-iturburuetarako, [konpondu datuak Data Lake biltegian edo eguneratu manifest/model.json fitxategiko datu motak](connect-common-data-model.md#common-reasons-for-ingestion-errors-or-corrupt-data). Izan ere Power Query datu-iturriak, konpondu datuak iturburu-fitxategian eta [zuzendu datu mota eraldaketa urratsa](connect-power-query.md#data-type-does-not-match-data) gainean **Power Query - Kontsultak editatu** orrialdea.

Datu-iturburuaren hurrengo freskatzearen ondoren, zuzendutako erregistroak Customer Insights-en irensten dira eta beheranzko prozesuetara pasatzen dira.

Adibidez, "urtebetetzea" zutabeak datu mota "data" gisa ezarrita dauka. Bezeroaren erregistroan urtebetetzea '01/01/19777' gisa sartu da. Sistemak erregistro hau hondatuta dagoela adierazten du. Aldatu iturburu-sistemako urtebetetzea '1977'-ra. Datu-iturriak automatikoki freskatu ondoren, eremuak baliozko formatua du eta erregistroa hondatutako entitatetik kentzen da.

[!INCLUDE [footer-include](includes/footer-banner.md)]
