---
title: Helbidea hobetzeko aberastea (bideoa dauka)
description: Aberastu eta normalizatu bezeroen profilen helbideen informazioa Microsoft-en ereduekin.
ms.date: 01/19/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
searchScope:
- ci-data-sources-enrichment
- ci-data-sources-enrichment-details
- ci-enrichments
- ci-enrichment-wizard
- customerInsights
ms.openlocfilehash: b4fef3b5e30e1cac4e5cb4401498f2f0981a409e
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642001"
---
# <a name="enrichment-of-customer-profiles-with-enhanced-addresses"></a>Bezeroen profilak aberastu helbide hobetuekin

Zure datuetako helbideak desegituratuak, osatugabeak edo okerrak izan daitezke. Erabili Microsoft-en ereduak zure helbideak normalizatzeko eta aberasteko [Common Data Model formatua](/common-data-model/schema/core/applicationcommon/address) zehaztasun eta ikuspegi hobeak lortzeko.

Zuk ere egin dezakezu [aberastu helbideak datu-iturrietan](data-sources-enrichment.md) datuen bateratze prozesuan partidaren zehaztasuna hobetzeko. 

## <a name="how-we-enhance-addresses"></a>Helbideak nola hobetzen ditugun

Gure ereduak bi urratseko prozesua egiten du helbide bat hobetzeko. Lehenik eta behin, helbidea analizatzen du bere osagaiak identifikatzeko eta formatu egituratu batean jartzen ditu. Ondoren, AI erabiltzen dugu helbideko balioak zuzentzeko, osatzeko eta estandarizatzeko.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWNewo]

### <a name="example"></a>Adibidez

Baliteke helbideen informazioa formatu estandarra izatea eta akats ortografikoak izatea. Ereduak arazo horiek konpon ditzake eta helbide koherenteak sor ditzake bezeroen profil bateratuetan.

```Input
4567 w main stret californa missouri 54321 us
```

```Output
- Street1: 4567 W Main St
- City: California
- StateOrProvince: MO
- ZipOrPostalCode: 54321
- CountryOrRegion: United States of America

- Address: 4567 W Main St, California, MO, 54321, United States of America
```

### <a name="limitations"></a>Murriztapenak

Helbide hobetuak sartutako helbide datuetan dauden balioekin bakarrik funtzionatzen du. Ereduak ez du: 

1. Egiaztatu helbidea baliozko helbidea den.
2. Egiaztatu balioetako bat, hala nola, posta-kodeak edo kaleen izenak, baliozkoak diren.
3. Aldatu ezagutzen ez dituen balioak.

Ereduak automatikoki ikasten oinarritutako teknikak erabiltzen ditu helbideak hobetzeko. Ereduak sarrerako balioa aldatzen duenerako konfiantza atalase handia aplikatzen dugun bitartean, ikaskuntzan oinarritutako edozein eredurekin gertatzen den moduan, ez da ehuneko 100eko zehaztasuna bermatzen.

## <a name="supported-countries-or-regions"></a>Lagundutako herrialdeak edo eskualdeak

Gaur egun herrialde edo eskualde hauetan helbide aberasgarriak onartzen ditugu: 

- Australia
- Kanada
- Frantzia
- Alemania
- Italia
- Japonia
- Erresuma Batua
- Estatu Batuak

Helbideek herrialde edo eskualde balioa izan behar dute. Ez dugu prozesatzen onartzen ez diren herrialde edo eskualdeen helbiderik eta herrialderik edo eskualderik eman ez duten helbiderik.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastua**.

1. Aukeratu **Aberastu nire datuak** **Helbide hobetuak** lauzan.

   :::image type="content" source="media/enhanced-addresses-tile.png" alt-text="Helbide hobetuen fitxaren pantaila-argazkia.":::

1. Aukeratu **Bezeroen datu multzoa** eta aukeratu aberastu nahi dituzun helbideak dituen entitatea. Aukeratu dezakezu *Bezeroa* entitateak helbideak aberastu ditzan zure bezeroen profil guztietan edo hautatu segmentu bat entitateak helbideak segmentu horretan dauden bezeroen profiletan soilik aberasteko.

1. Hautatu zein formatu eman datu multzoetako helbideei. Aukeratu **Atributu bakarreko helbidea** zure datuetako helbideek eremu bakarra erabiltzen badute. Aukeratu **Hainbat atributuko helbidea** zure datuetako helbideek eremu bat edo gehiago erabiltzen badituzte.

   > [!NOTE]
   > Herrialde / eskualdea derrigorrezkoa da atributu bakarreko eta atributu anitzeko helbideetan. Herrialde edo eskualde balio baliodunak edo onartuak ez dituzten helbideak ez dira aberastuko.

1.  Esleitu helbide eremuak zure bezero entitate bateratuarekin.

    :::image type="content" source="media/enhanced-address-mapping.png" alt-text="Helbide hobetuen eremuak esleitzeko orria.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Hornitu aberastearen izena eta irteerako entitatearen izena.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren araberakoa da.

Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako datuen lagin bat ikus dezakezu **Bezeroen aurrebista aberastua** teila. Hautatu **Gehiago ikusi** eta hautatu **Datuak** fitxa aberastutako profil bakoitzaren ikuspegi zehatzera sartzeko.

### <a name="overview-card"></a>Ikuspegiko txartela

Ikuspegi-txartelak aberastearen estaldurari buruzko xehetasunak erakusten ditu. 

* **Helbideak prozesatu eta aldatu** : arrakastaz aberastu diren helbideak dituzten bezero-profilen kopurua.

* **Helbideak prozesatu eta aldatu gabe** : Aitortu baina aldatu ez diren helbideak dituzten bezero-profilen kopurua. Normalean, sarrerako datuak baliozkoak direnean eta aberastearekin hobetu ezin direnean gertatzen da.

* **Helbideak ez dira prozesatu eta ez dira aldatu** : Aitortu gabeko helbideak dituzten profilen kopurua. Normalean baliogabeak diren edo aberastasunak onartzen ez dituen sarrerako datuetarako.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]