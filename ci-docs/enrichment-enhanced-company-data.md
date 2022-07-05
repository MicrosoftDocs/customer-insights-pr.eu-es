---
title: Aberastu enpresen profilak enpresaren datu hobetuekin
description: Aberastu eta normalizatu enpresaren datuak Microsoft-en ereduekin.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 131ef3d1e123628779609ddec368cfef8f4d607e
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9054233"
---
# <a name="enrich-company-profiles-with-enhanced-company-data"></a>Aberastu enpresen profilak enpresaren datu hobetuekin

Erabili Microsoft-en ereduak eta konpilatutako enpresako datuak zure enpresaren profilak zuzentzeko, osatzeko eta estandarizatzeko. Erabiliko dugu [Common Data Model formatua](/common-data-model/schema/core/applicationcommon/account) zehaztasun eta ikuspegi hobea lortzeko.

Zuk ere egin dezakezu [datu-iturriei buruzko enpresaren datuak hobetzea](data-sources-enrichment.md) datuen bateratze prozesuan partidaren zehaztasuna hobetzeko.

Estatu Batuetako enpresa publikoentzat, diru-sarrerak, akzioen ticker, industria eta abar bezalako informazioa eskuragarri dago.  

## <a name="how-we-enhance-company-data"></a>Nola hobetzen ditugun enpresako datuak

Gure ereduak bi urratseko prozesu bat egiten du enpresaren profila hobetzeko. Lehenik eta behin, enpresaren izena normalizatzen du. Adibidez, *Microsoft Corp* zuzendu eta estandarizatu egingo da *Microsoft Corporation*. Microsoft-ek konpilatutako enpresaren datuetan bat-etortze bat bilatzen saiatzen da. Bat-etortze bat aurkitzen bada, konpainiaren profila aberasten dugu gure konpainiaren datuen informazioarekin, enpresaren izena barne.

### <a name="example"></a>Adibidez

Baliteke zure enpresaren informazioak formatu estandar bat ez jarraitzea eta akats ortografikoak izatea. Eredua arazo horiek konpontzen eta informazio koherentea sortzen saiatzen da.

```Input
Microsft
```

```Output
- AccountName: Microsoft Corporation
- MainPhoneNumber: 8006427676
- Website: https://www.microsoft.com/
- Street1: One Microsoft Way
- City: Redmond
- StateOrProvince: Washington
- County: King
- ZipOrPostalCode: 98052
- CountryOrRegion: United States
```

## <a name="limitations"></a>Murriztapenak

Ereduak ez du:

- Enpresaren identitatea berretsi. Ez dugu egiaztatzen sarrera lehendik dagoen erakunde bat den edo enpresa batek irteera izen estandar gisa erabiltzen duen.
- Estali orokorrean enpresak mundu osoan. Microsoft-ek bildutako konpainiaren datuek estaldura globala dute, baina estaldura gehien Australian, Kanadan, Erresuma Batuan eta Estatu Batuetan eskaintzen du.
- Normalizatu enpresen helbideak mundu osoan. Gaur egun, herrialde edo eskualde hauetan helbideak estandarizatzea onartzen dugu: Australia, Kanada, Frantzia, Alemania, Italia, Japonia, Erresuma Batua eta Estatu Batuak.
- Datuen zehaztasuna edo freskotasuna bermatu. Enpresaren informazioa askotan aldatzen denez, ezin dugu bermatu emandako enpresaren datu hobetuak beti zehatzak edo eguneratuak direnik.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Enpresaren datu hobetuak** teila.

   :::image type="content" source="media/enhanced-company-data-tile.png" alt-text="Aberaste-lauza enpresaren datuetarako aberaste-zentroan.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, eta segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Hautatu zure enpresaren profiletatik zein eremu mota erabili nahi dituzun Microsoft-ek bildutako enpresaren datuekin bat etortzeko. Aukeraketa honek hurrengo urratsean atzitu ditzakezun mapen eremuei eragingo die.

1. Hautatu **Hurrengoa**.

1. Mapeatu zure enpresaren eremuak Microsoft-en enpresaren datuekin. Bat-etortzeen zehaztasun handiagoa lortzeko, gehitu eremu gehiago.

    :::image type="content" source="media/enhanced-company-data-mapping.png" alt-text="Datuen mapak egiteko urratsa enpresa aberaste bat konfiguratzean.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Eman a **Izena** aberasteko eta **Irteerako entitatea**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

### <a name="overview-card"></a>Ikuspegiko txartela

The **Bezeroek ikuspegi orokorra aldatzen dute** fitxak aberastearen estaldurari buruzko xehetasunak erakusten ditu

- **Enpresak prozesatu eta aldatu** : arrakastaz aberastu diren bezero-enpresa-profilen kopurua.
- **Enpresak tramitatu eta aldatu gabe** : aitortu baina aldatu ez diren bezero-enpresa-profilen kopurua. Hau normalean sarrerako datuak baliozkoak direnean eta aberastearekin hobetu ezin direnean gertatzen da.
- **Enpresak ez izapidetu eta ez aldatu** : Aitortu ez diren bezero-enpresa-profilen kopurua. Hau normalean baliogabeak diren edo aberasteak onartzen ez dituen sarrerako datuekin gertatzen da.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
