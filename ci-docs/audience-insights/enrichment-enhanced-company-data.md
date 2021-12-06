---
title: Enpresaren datuen hobekuntza
description: Aberastu eta normalizatu enpresaren datuak Microsoft-en ereduekin.
ms.date: 11/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: d11700c87f31cedc40d32b201251d8a9e2e2c312
ms.sourcegitcommit: dfc4843cc78857f1e3ca49d7b938e3ba77969169
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/15/2021
ms.locfileid: "7813905"
---
# <a name="enrichment-of-company-profiles-with-enhanced-company-data"></a>Enpresaren profilak aberastea enpresaren datu hobetuekin

Erabili Microsoft-en ereduak eta konpilatutako enpresako datuak zure enpresaren profilak zuzentzeko, osatzeko eta estandarizatzeko. Erabiliko dugu [Common Data Model formatua](/common-data-model/schema/core/applicationcommon/account) zehaztasun eta ikuspegi hobeak lortzeko.

## <a name="how-we-enhance-company-data"></a>Nola hobetzen ditugun enpresako datuak

Gure ereduak bi urratseko prozesu bat egiten du enpresaren profila hobetzeko. Lehenik eta behin, enpresaren izena normalizatzen du. Adibidez, *Microsoft Corp* zuzendu eta estandarizatu egingo da *Microsoft Corporation*. Microsoft-ek konpilatutako enpresaren datuetan bat-etortze bat bilatzen saiatzen da. Bat-etortze bat aurkitzen bada, konpainiaren profila aberasten dugu gure konpainiaren datuen informazioarekin, enpresaren izena barne.


### <a name="example"></a>Adibidez

Baliteke zure enpresaren informazioak formatu estandar bat ez jarraitzea eta akats ortografikoak izatea. Eredua arazo hauek konpontzen eta informazio koherentea sortzen saiatzen da.

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

Datu hobetuekin muga batzuk daude. Beheko zerrendako elementuak ez ditu ereduak onartzen.

1.  Enpresaren identitatea berretsi. Ez dugu egiaztatzen sarrera lehendik dagoen erakunde bat den edo enpresa batek irteera izen estandar gisa erabiltzen duen.
2.  Estali orokorrean enpresak mundu osoan. Microsoft-ek bildutako konpainiaren datuek estaldura globala dute, baina estaldura gehien Australian, Kanadan, Erresuma Batuan eta Estatu Batuetan eskaintzen du.
3.  Normalizatu enpresen helbideak mundu osoan. Gaur egun, herrialde edo eskualde hauetan helbideak estandarizatzea onartzen dugu: Australia, Kanada, Frantzia, Alemania, Italia, Japonia, Erresuma Batua eta Estatu Batuak.
4.  Datuen zehaztasuna edo freskotasuna bermatu. Enpresaren informazioa askotan aldatzen denez, ezin dugu bermatu emandako enpresaren datu hobetuak beti zehatzak edo eguneratuak direnik.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastua**.

1. Hautatu **Aberastu nire datuak** gainean **Enpresaren datu hobetuak** teila.

   :::image type="content" source="media/enhanced-company-data-tile.png" alt-text="Aberaste-lauza enpresaren datuetarako aberaste-zentroan.":::

1. Aukeratu **Bezeroen datu multzoa** eta aukeratu aberastu nahi dituzun helbideak dituen entitatea. Aukeratu dezakezu *Bezeroa* entitateak helbideak aberastu ditzan zure bezeroen profil guztietan edo hautatu segmentu bat entitateak helbideak segmentu horretan dauden bezeroen profiletan soilik aberasteko.

1. Hautatu zure enpresa-profiletatik zein eremu mota erabili behar diren Microsoft-ek konpilatutako enpresa-datuekin bat etortzeko. Aukeraketa honek hurrengo urratsean atzitu ditzakezun mapen eremuei eragingo die.

1.  Mapeatu zure bezero-entitate bateratuko konpainiaren eremuak. Zenbat eta gako-identifikatzaile eta eremu gehiago mapatu, orduan eta aukera handiagoa izango da bat-etortze-tasa handiagoa izateko.

    :::image type="content" source="media/enhanced-company-data-mapping.png" alt-text="Datuen mapak egiteko urratsa enpresa aberaste bat konfiguratzean.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Hornitu aberastearen izena eta irteerako entitatearen izena.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren araberakoa da.

Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](../includes/next-steps-enrichment.md)]

[!INCLUDE[footer-include](../includes/footer-banner.md)]