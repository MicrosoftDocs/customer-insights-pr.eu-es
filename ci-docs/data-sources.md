---
title: Erabili datu-iturburuak datuak sartzeko
description: Ikasi iturri desberdinetako datuak nola inportatu.
ms.date: 05/31/2022
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
ms.openlocfilehash: e22977107565a0b28b74f41576a1c7ccc74f6dc1
ms.sourcegitcommit: 5e26cbb6d2258074471505af2da515818327cf2c
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "9011734"
---
# <a name="data-sources-overview"></a>Datuen iturburuen ikuspegi orokorra

Dynamics 365 Customer Insights konexioak eskaintzen ditu iturri multzo zabal bateko datuak ekartzeko. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak hartu ondoren, egin dezakezu [bateratu](data-unification.md), sortu ikuspegiak eta aktibatu datuak esperientzia pertsonalizatuak eraikitzeko.

## <a name="add-data-sources"></a>Gehitu datu-iturburuak

Datu-iturriak erantsi edo inporta ditzakezu Customer Insights-era. Beheko esteketan datu-iturriak gehitzeko argibideak ematen dira.

**Erantsi datu-iturburu bat**

Microsoft-en Azure datu-zerbitzuetako batean datuak prestatuta badituzu, Customer Insights erraz konekta daiteke datu-iturburu-ra datuak berriro sartu beharrik gabe. Hautatu aukera hauetariko bat:
- [Azure Data Lake Storage(csv edo parquet fitxategiak Common Data Model karpeta batean)](connect-common-data-model.md)
- [Azure Synapse Analytics(Lakuen datu-baseak)](connect-synapse.md)
- [Microsoft Dataverse datu-lakua](connect-dataverse-managed-lake.md)

**Inportatu eta eraldatu**

Datu iturri lokalak, Microsoft edo hirugarrenen datuak erabiltzen badituzu, inportatu eta eraldatu datuak erabiliz Power Query konektoreak.
- [Power Query konektoreak](connect-power-query.md)

## <a name="review-data-sources"></a>Berrikusi datu-iturriak

Zure ingurunea Customer Insights biltegiratzea erabiltzeko konfiguratuta badago eta tokiko datu-iturburuak erabiltzen badituzu, erabiltzen duzu Power Platform datu-fluxuak. Horrekin Power Platform datu-fluxuak, partekatutako datu-iturriak eta besteek kudeatutako datu-iturriak ikus ditzakezu. The **Datu-iturriak** orrialdeak hiru ataletan zerrendatzen ditu datu-iturriak:
- **Partekatua** : Customer Insights administratzaile guztiek kudeatu ditzaketen datu-iturriak. Power Platform datu-fluxuak, zure biltegiratze-kontua eta a Dataverse -kudeatutako data lake partekatutako datu-iturrien adibideak dira.
- **Nik kudeatzen dut** :Power Platform Zuk bakarrik sortu eta kudeatutako datu-fluxuak. Customer Insights-eko beste administratzaileek datu-fluxu hauek soilik ikus ditzakete, baina ez editatu, freskatu edo ezabatu.
- **Beste batzuek kudeatzen dute** :Power Platform beste administratzaileek sortutako datu-fluxuak. Horiek bakarrik ikus ditzakezu. Edozein laguntza lortzeko harremanetan jartzeko datu-fluxuaren jabea zerrendatzen du.
> [!NOTE]
> Entitate guztiak beste erabiltzaileek ikusi eta erabil ditzakete. Datu-iturriak sortu dituen erabiltzailearen jabetzakoak diren arren, datuen ingestetik sortutako entitateak Customer Insights-eko erabiltzaile guztiek erabil ditzakete.

Zure inguruneak erabiltzen ez badu Power Platform datu-fluxuak, **Datu-iturriak** orrialdeak datu-iturburu guztien zerrenda baino ez dauka. Ez dago atalik bistaratzen.

Joan **Datuak** > **Datu iturriak** irensten den datu-iturburu bakoitzaren izena, bere egoera eta iturri horren datuak azken aldiz freskatu diren ikusteko. Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.

:::image type="content" source="media/configure-data-datasource-added.png" alt-text="Gehitutako datu-iturriak.":::

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

Datuak kargatzeak denbora behar dezake. Freskatu ondoren, iradokitako datuak berrikusi daitezke **erakundeak** orria. Informazio gehiago lortzeko, [Entitateak](entities.md).

## <a name="refresh-data-sources"></a>Freskatu datu-iturburuak

Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera. [Datu iturri lokalak](connect-power-query.md#add-data-from-on-premises-data-sources) freskatu datuak sartzerakoan konfiguratutako ordutegiak. Erantsitako datu-iturburuetarako, datuak barneratzeak datu-iturburu horren eskura dauden azken datuak kontsumitzen ditu.

Joan **Admin** > **Sistema** > [**Ordutegia**](system.md#schedule-tab) sartutako datu-iturburuen sistemak programatutako freskaketak konfiguratzeko.

Eskatu ahalako datu-iturburu bat freskatzeko, jarraitu urrats hauek:

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu elipsi bertikala (&vellip;) freskatu eta hautatu nahi duzun datu-iturburu ondoan **Freskatu** goitibeherako zerrendatik. Datu-iturburua eskuz eguneratzeko aktibatuta dago. datu-iturburu freskatzeak entitatearen eskema eta datuak eguneratuko ditu datu-iturburu-en zehaztutako entitate guztientzat.

1. Aukeratu **Freskatzeari utzi** lehendik dagoen freskatzea bertan behera utzi nahi baduzu, eta datu-iturburua bere azken eguneratze-egoerara itzuliko da.

## <a name="delete-a-data-source"></a>Ezabatu datu-iturri bat

datu-iturburu bat ezabatu daiteke datuak prozesamendu batean erabiltzen ez badira, hala nola bateratzean, ikuspegietan, aktibazioetan edo esportazioetan.

1. Joan **Datuak** > **Datu-iturburuak**.

2. Hautatu elipsi bertikala (&vellip;) kendu eta hautatu nahi duzun datu-iturburu ondoan **Ezabatu** goitibeherako menutik.

3. Berretsi ezabatu nahi duzula.


[!INCLUDE [footer-include](includes/footer-banner.md)]
