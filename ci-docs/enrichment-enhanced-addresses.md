---
title: Helbidea hobetzeko aberastea (bideoa dauka)
description: Aberastu eta normalizatu bezeroen profilen helbideen informazioa Microsoft-en ereduekin.
ms.date: 06/10/2022
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
ms.openlocfilehash: f6279b9bb721d99d66f73e8dc839a92f1ad90140
ms.sourcegitcommit: 27c5473eecd851263e60b2b6c96f6c0a99d68acb
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/13/2022
ms.locfileid: "8953796"
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

Helbide hobetuek sartutako helbide-datuetan lehendik dauden balioekin soilik funtzionatzen dute. Ereduak ez du:

1. Egiaztatu helbidea baliozko helbidea den.
2. Egiaztatu balioetako bat, hala nola, posta-kodeak edo kaleen izenak, baliozkoak diren.
3. Aldatu ezagutzen ez dituen balioak.

Ereduak automatikoki ikasten oinarritutako teknikak erabiltzen ditu helbideak hobetzeko. Ikaskuntza automatikoan oinarritutako edozein modelorekin gertatzen den bezala, ehuneko 100eko zehaztasuna ez dago bermatuta.

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

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Aukeratu **Aberastu nire datuak** **Helbide hobetuak** lauzan.

   :::image type="content" source="media/enhanced-addresses-tile.png" alt-text="Helbide hobetuen fitxaren pantaila-argazkia.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, eta segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Hautatu zein formatu eman datu multzoetako helbideei. Aukeratu **Atributu bakarreko helbidea** zure datuetako helbideek eremu bakarra erabiltzen badute. Aukeratu **Hainbat atributuko helbidea** zure datuetako helbideek eremu bat edo gehiago erabiltzen badituzte.

1. Hautatu **Hurrengoa** eta mapatu zure bezero-entitate bateratuko helbide-eremuak.

    :::image type="content" source="media/enhanced-address-mapping.png" alt-text="Helbide hobetuen eremuak esleitzeko orria.":::

   > [!NOTE]
   > Herrialde / eskualdea derrigorrezkoa da atributu bakarreko eta atributu anitzeko helbideetan. Herrialde edo eskualde balio baliodunak edo onartuak ez dituzten helbideak ez dira aberastuko.

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Eman a **Izena** aberasteko eta **Irteerako entitatea**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="enrichment-results"></a>Aberastearen emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

The **Alorka aberastutako bezero kopurua** aberasturiko eremu bakoitzaren estaldura sakontzen du.

### <a name="overview-card"></a>Ikuspegiko txartela

The **Bezeroek ikuspegi orokorra aldatzen dute** txartelak aberastearen estaldurari buruzko xehetasunak erakusten ditu:

- **Helbideak prozesatu eta aldatu** : arrakastaz aberastu diren helbideak dituzten bezero-profilen kopurua.
- **Helbideak prozesatu eta aldatu gabe** : Aitortu baina aldatu ez diren helbideak dituzten bezero-profilen kopurua. Normalean, sarrerako datuak baliozkoak direnean eta aberastearekin hobetu ezin direnean gertatzen da.
- **Helbideak ez dira prozesatu eta ez dira aldatu** : Ezagutzen ez diren helbideak dituzten profilen kopurua. Normalean baliogabeak diren edo aberastasunak onartzen ez dituen sarrerako datuetarako.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
