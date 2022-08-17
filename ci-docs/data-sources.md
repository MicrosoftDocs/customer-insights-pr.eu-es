---
title: Datuen iturburuen ikuspegi orokorra
description: Ikasi hainbat iturritako datuak inportatu edo sartzen.
ms.date: 07/26/2022
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
ms.openlocfilehash: 591353bf1ba2f9ca05ddd137e1cf29dc0b0fba97
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9245634"
---
# <a name="data-sources-overview"></a>Datuen iturburuen ikuspegi orokorra

Dynamics 365 Customer Insights konexioak eskaintzen ditu iturri multzo zabal bateko datuak ekartzeko. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak hartu ondoren, egin dezakezu [bateratu](data-unification.md), sortu ikuspegiak eta aktibatu datuak esperientzia pertsonalizatuak eraikitzeko.

## <a name="add-or-edit-data-sources"></a>Gehitu edo editatu datu-iturriak

Datu-iturriak erantsi edo inporta ditzakezu Customer Insights-era. Beheko esteketan datu-iturriak gehitzeko eta editatzeko argibideak ematen dira.

**Erantsi datu-iturburu bat**

Microsoft-en Azure datu-zerbitzuetako batean datuak prestatuta badituzu, Customer Insights erraz konekta daiteke datu-iturburu-era datuak berriro sartu beharrik gabe. Hautatu aukera hauetariko bat:
- [Azure Data Lake Storage(csv edo parquet fitxategiak Common Data Model karpeta batean)](connect-common-data-model.md)
- [Azure Synapse Analytics(Lakuen datu-baseak)](connect-synapse.md)
- [Microsoft Dataverse datu-lakua](connect-dataverse-managed-lake.md)

**Inportatu eta eraldatu**

Datu iturri lokalak, Microsoft edo hirugarrenen datuak erabiltzen badituzu, inportatu eta eraldatu datuak erabiliz Power Query konektoreak.
- [Power Query konektoreak](connect-power-query.md)

## <a name="review-data-sources"></a>Berrikusi datu-iturriak

Zure ingurunea Customer Insights biltegia erabiltzeko konfiguratuta bazegoen eta tokiko datu-iturriak erabiltzen badituzu, erabiltzen duzu Power Platform datu-fluxuak. Horrekin Power Platform datu-fluxuak, partekatutako datu-iturriak eta besteek kudeatutako datu-iturriak ikus ditzakezu. The **Datu-iturriak** orrialdeak hiru ataletan zerrendatzen ditu datu-iturriak:
- **Partekatua** : Customer Insights administratzaile guztiek kudeatu ditzaketen datu-iturriak. Power Platform datu-fluxuak, zure biltegiratze-kontua eta a Dataverse -kudeatutako data lake partekatutako datu-iturrien adibideak dira.
- **Nik kudeatzen dut** :Power Platform Zuk bakarrik sortu eta kudeatutako datu-fluxuak. Customer Insights-eko beste administratzaileek datu-fluxu hauek soilik ikus ditzakete, baina ez editatu, freskatu edo ezabatu.
- **Beste batzuek kudeatzen dute** :Power Platform beste administratzaile batzuek sortutako datu-fluxuak. Horiek bakarrik ikus ditzakezu. Edozein laguntza lortzeko harremanetan jartzeko datu-fluxuaren jabea zerrendatzen du.
> [!NOTE]
> Entitate guztiak beste erabiltzaileek ikusi eta erabil ditzakete. Datu-iturburuak sortu dituen erabiltzailearenak diren arren, datuak sartzearen ondoriozko entitateak Customer Insights-eko erabiltzaile guztiek erabil ditzakete.

Zure inguruneak erabiltzen ez badu Power Platform datu-fluxuak, **Datu-iturriak** orrialdeak datu-iturburu guztien zerrenda baino ez dauka. Ez dago atalik bistaratzen.

## <a name="manage-existing-data-sources"></a>Kudeatu lehendik dauden datu-iturriak

Joan **Datuak** > **Datu-iturriak** irensten den datu-iturburu bakoitzaren izena, bere egoera eta iturri horren datuak azken aldiz freskatu diren ikusteko. Datu iturrien zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun datu-iturburu aurkitzeko.

Hautatu datu-iturburu bat erabilgarri dauden ekintzak ikusteko.

:::image type="content" source="media/data_sources_showmore.png" alt-text="Gehitutako datu-iturriak.":::

- [**Editatu**](#add-or-edit-data-sources) datu-iturburu bere propietateak aldatzeko.
- [**Freskatu**](#refresh-data-sources) datu-iturburu azken datuak sartzeko.
- [**Aberastu**](data-sources-enrichment.md) datu-iturburu bateratu aurretik.
- **Ezabatu** datu-iturburu. datu-iturburu bat ezabatu daiteke datuak prozesamendu batean erabiltzen ez badira, hala nola bateratzean, ikuspegietan, aktibazioetan edo esportazioetan.

## <a name="refresh-data-sources"></a>Freskatu datu-iturburuak

Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera. [Datu iturri lokalak](connect-power-query.md#add-data-from-on-premises-data-sources) freskatu datuak sartzerakoan konfiguratutako ordutegiak. Erantsitako datu-iturburuetarako, datuak barneratzeak datu-iturburu horren eskura dauden azken datuak kontsumitzen ditu.

Joan **Admin** > **Sistema** > [**Ordutegia**](schedule-refresh.md) sartutako datu-iturburuen sistemak programatutako freskaketak konfiguratzeko.

Eskaeraren arabera datu-iturburu bat freskatzeko:

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu freskatu nahi duzun datu-iturburu eta hautatu **Freskatu**. Datu-iturburua eskuz eguneratzeko aktibatuta dago. datu-iturburu freskatzeak entitatearen eskema eta datuak eguneratuko ditu datu-iturburu-en zehaztutako entitate guztientzat.

1. Hautatu egoera irekitzeko **Aurrerapen xehetasunak** panela eta ikusi aurrerapena. Lana bertan behera uzteko, hautatu **Utzi lana** panelaren behealdean.

[!INCLUDE [footer-include](includes/footer-banner.md)]
