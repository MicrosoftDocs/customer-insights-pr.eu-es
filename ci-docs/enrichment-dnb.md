---
title: Enpresa-profilak aberastea Dun & Bradstreet-ekin
description: Dun & Bradstreet hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: b1038970b6aee3bbdd7f79cc457f79aaf1c38222
ms.sourcegitcommit: 27c5473eecd851263e60b2b6c96f6c0a99d68acb
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/13/2022
ms.locfileid: "8953873"
---
# <a name="enrichment-of-company-profiles-with-dun--bradstreet-preview"></a>Enpresaren profilak aberastea Dun & Bradstreet-ekin (aurrebista)

Dun & Bradstreet-ek negozioentzako datu komertzialak, analitikoak eta ikuspegiak eskaintzen ditu. Enpresentzako bezeroen profil bateratuak dituzten bezeroei beren datuak aberasteko aukera ematen die. Aberasteen artean, DUNS zenbakia, enpresaren tamaina, kokapena, industria eta abar bezalako atributuak daude.

## <a name="prerequisites"></a>Aurrebaldintzak

- Aktibo bat [Dun & Bradstreet](https://www.dnb.com/marketing/media/give-your-data-a-boost.html?source=microsoft_audience_insights) lizentzia.
- [Bezeroen profil bateratuak](customer-profiles.md) enpresentzat.
- Dun & Bradstreet bat [proiektua](#set-up-your-dun--bradstreet-project) ezartzen da.
- Dun & Bradstreet bat [konexioa](connections.md) da [konfiguratuta](#configure-a-connection-for-dun--bradstreet) administratzaile batek.

## <a name="set-up-your-dun--bradstreet-project"></a>Konfiguratu zure Dun & Bradstreet proiektua

Dun & Bradstreet-en lizentziadun erabiltzaile gisa, proiektu bat konfigura dezakezu [Dun & Bradstreet Connect](https://connect.dnb.com?lead_source=microsoft_audienceinsights).

1. Saioa hasi [Dun & Bradstreet Connect](https://connect.dnb.com?lead_source=microsoft_audienceinsights). Kredentzialak berreskuratzeko, [leheneratu pasahitza](https://sso.dnb.com/signin/forgot-password?lead_source=microsoft_audienceinsights).

1. Deskargatu [gure csv txantiloi fitxategia](https://c360devenrichment.blob.core.windows.net/mapping/DnBCIdatamapping.csv) Customer Insights eremuak dagozkien Dun & Bradstreet eremuekin mapatzeko erabiliko dena.

1. Kargatu fitxategia **Kargatu datuak** Dun & Bradstreet proiektuak sortzeko esperientziaren urratsa.

1. Hautatu puntu horizontalak dagokion azpian **iturria** sortu berri den Dun & Bradstreet proiektuan eskuragarri dauden aukerak ikusteko.

   :::image type="content" source="media/enrichment-dnb-dots.png" alt-text="Dun & Bradstreet proiektu bateko puntuen pantaila-argazkia.":::

1. Aukeratu **Lortu S3 xehetasunak**. Gorde informazio hau leku seguru batean. Behar izango duzu [aberasteko konexioa ezarri](#configure-a-connection-for-dun--bradstreet) Bezeroen Insights-en.

   :::image type="content" source="media/enrichment-dnb-s3info.png" alt-text="Dun & Bradstreet proiektu batean s3 informazioa aukeratzeko pantaila-argazkia.":::

## <a name="configure-a-connection-for-dun--bradstreet"></a>Konfiguratu konexio bat Dun & Bradstreet-erako

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta Dun & Bradstreet Connect-en kredentzialak izan.

1. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean edo joan **Admin** > **Konexioak** eta hautatu **Konfiguratu** Dun & Bradstreet fitxan.

1. Sartu konexiorako izen bat.

1. Eman baliozko Dun & Bradstreet kredentzialak eta Dun & Bradstreet proiektuaren xehetasunak *Eskualdea, Jaregin karpetaren bidea eta Jaregin karpetaren izena*. Zuk [lortu informazio hau](#set-up-your-dun--bradstreet-project) Dun & Bradstreet proiektutik.

1. Berrikusi eta eman zure baimena [Datuen pribatutasuna eta betetzea](#data-privacy-and-compliance) hautatuz **Ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

   :::image type="content" source="media/enrichment-dnb-connection.png" alt-text="Dun & Bradstreet konexioaren konfigurazio orria.":::

### <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights Dun & Bradstreet-i datuak transmititzeko, datuak betetze-mugatik kanpo transferitzea onartzen duzu Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina zu zara Dun & Bradstreet-ek izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

## <a name="supported-countries-or-regions"></a>Lagundutako herrialdeak edo eskualdeak

Une honetan herrialde/eskualde aukera hauek onartzen ditugu: Kanada (ingelesa) edo Estatu Batuak (ingelesa).

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Enpresaren datuak** Dun & Bradstreet fitxarako.

   :::image type="content" source="media/enrichment-dnb-tile.png" alt-text="Dun & Bradstreet fitxaren pantaila-argazkia.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa eta berretsi. Jarri harremanetan administratzaile batekin erabilgarri ez badago.

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu Dun & Bradstreet enpresaren datuekin aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, eta segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Definitu zure profil bateratuetako zein eremu mota erabili Dun & Bradstreet-en konpainiaren datuak bat etortzeko. Eremuetako bat gutxienez **Izena eta helbidea**, **Mugikorra**, edo **Posta elektronikoa** beharrezkoa da.

1. Hautatu **Hurrengoa**

1. Mapeatu zure eremuak Dun & Bradstreet-en konpainiaren datuekin. Edota **DUNS zenbakia** edo **Enpresaren izena** eta **Herrialdea** eremuak beharrezkoak dira.

      :::image type="content" source="media/enrichment-dnb-mapping.png" alt-text="Dun & Bradstreet eremu-mapa-panela.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Eman a **Izena** aberasteko eta **Irteerako entitatearen izena**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="enrichment-results"></a>Aberastearen emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
