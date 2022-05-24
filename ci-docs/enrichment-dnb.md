---
title: Enpresa-profilak aberastea Dun & Bradstreet-ekin
description: Dun & Bradstreet hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 04/26/2022
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: c738c2657d4cda213342629156ddc8104366bd8a
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755385"
---
# <a name="enrichment-of-company-profiles-with-dun--bradstreet-preview"></a>Enpresaren profilak aberastea Dun & Bradstreet-ekin (aurrebista)

Dun & Bradstreet-ek negozioentzako datu komertzialak, analitikoak eta ikuspegiak eskaintzen ditu. Enpresentzako bezeroen profil bateratuak dituzten bezeroei beren datuak aberasteko aukera ematen die. Aberasteen artean, DUNS zenbakia, enpresaren tamaina, kokapena, industria eta abar bezalako atributuak daude.

## <a name="prerequisites"></a>Aurrebaldintzak

Dun & Bradstreet aberaste bat konfiguratzeko, aurrebaldintza hauek bete behar dira:

- Aktibo bat duzu [Dun & Bradstreet](https://www.dnb.com/marketing/media/give-your-data-a-boost.html?source=microsoft_audience_insights) lizentzia.
- Duzu [bezeroen profil bateratuak](customer-profiles.md) enpresentzat.
- Dun & Bradstreet bat [konexioa](connections.md) administratzaile batek konfiguratzen du. Badaukazu sor dezakezu [administratzailea](permissions.md#admin) baimenak eta Dun & Bradstreet Connect-en kredentzialak.

## <a name="setting-up-your-dun--bradstreet-project"></a>Zure Dun & Bradstreet proiektua konfiguratzen

Dun & Bradstreet-en lizentziadun erabiltzaile gisa, proiektu bat konfigura dezakezu [Dun & Bradstreet Connect](https://connect.dnb.com?lead_source=microsoft_audienceinsights).


1. Saioa hasi [Dun & Bradstreet Connect](https://connect.dnb.com?lead_source=microsoft_audienceinsights). Kredentzialak berreskuratzeko, [leheneratu pasahitza](https://sso.dnb.com/signin/forgot-password?lead_source=microsoft_audienceinsights).

1. Deskargatu [gure csv txantiloi fitxategia](https://c360devenrichment.blob.core.windows.net/mapping/DnBCIdatamapping.csv) Customer Insights eremuak dagozkien Dun & Bradstreet eremuekin mapatzeko erabiliko dena.

1. Kargatu fitxategia **Kargatu datuak** Dun & Bradstreet proiektuak sortzeko esperientziaren urratsa.

1. Hautatu puntu horizontalak dagokion azpian **iturria** sortu berri den Dun & Bradstreet proiektuan eskuragarri dauden aukerak ikusteko.

   :::image type="content" source="media/enrichment-dnb-dots.png" alt-text="Dun & Bradstreet proiektu bateko puntuen pantaila-argazkia.":::

1. Aukeratu **Lortu S3 xehetasunak**. Gorde informazio hau leku seguru batean. Behar izango duzu [aberasteko konexioa ezarri](#configure-a-connection-for-dun--bradstreet) Bezeroen Insights-en.

   :::image type="content" source="media/enrichment-dnb-s3info.png" alt-text="Dun & Bradstreet proiektu batean s3 informazioa aukeratzeko pantaila-argazkia.":::

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastua**.

1. Hautatu **Aberastu nire datuak** Dun & Bradstreet fitxan eta hautatu **Hasi**.

   :::image type="content" source="media/enrichment-dnb-tile.png" alt-text="Dun & Bradstreet fitxaren pantaila-argazkia.":::

1. Hautatu goitibeherako zerrendako [konexio](connections.md) bat. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, konexio bat sor dezakezu. Hautatu **Gehitu konexioa** eta aukeratu **Dun & Bradstreet**.

1. Hautatu **Konektatu Dun & Bradstreet-era** konexioa berresteko.

1. Hautatu **Hurrengoa** eta aukeratu **Bezeroaren datu multzoa** Dun & Bradstreet enpresaren datuekin aberastu nahi duzu. Hautatu dezakezu **Bezeroa** entitatea zure bezero-profil guztiak aberasteko edo segmentu-entitate bat hautatu segmentu horretan dauden bezero-profil bateratuak soilik aberasteko.

1. Hautatu **Hurrengoa** eta definitu zure profil bateratuetako zein eremu erabiltzen diren Dun & Bradstreet-en konpainiaren bat datozen datuak bilatzeko. Edota **DUNS zenbakia** edo **Enpresaren izena** eta **Herrialdea** eremuak beharrezkoak dira. Herrialdearen eremuak onartzen du [bi edo hiru letrako herrialde-kodeak](https://www.iso.org/iso-3166-country-codes.html), herrialdearen izena ingelesez, herrialdearen izena jatorrizko hizkuntzan eta telefonoaren aurrizkia. Herrialdearen aldaera arrunt batzuk hauek dira:

- AEB: Ameriketako Estatu Batuak, Estatu Batuak, AEB, Amerika.
- CA: Kanada.
- GB: Erresuma Batua, Erresuma Batua, Britainia Handia, GB, Britainia Handiko eta Ipar Irlandako Erresuma Batua, Britainia Handiko Erresuma Batua.
- AU: Australia, Australiako Commonwealth.
- FR: Frantzia, Frantziako Errepublika.
- DE: Alemania, Alemania, Alemania, Alemania, Alemaniako Errepublika Federala, Alemaniako Errepublika.

   :::image type="content" source="media/enrichment-dnb-mapping.png" alt-text="Dun & Bradstreet eremu-mapa-panela.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Eman aberasturako izena eta hautatu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="configure-a-connection-for-dun--bradstreet"></a>Konfiguratu konexio bat Dun & Bradstreet-erako

Administratzailea izan behar duzu konexioak konfiguratzeko. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean *edo* joan **Admin** > **Konexioak** eta hautatu **Konfiguratu** Dun & Bradstreet fitxan.

1. Hautatu **Hasi erabiltzen**.

1. Idatzi konexioaren izena **Bistaratzeko izena** kutxa.

1. Eman baliozko Dun & Bradstreet kredentzialak eta Dun & Bradstreet proiektuaren xehetasunak *Eskualdea, Jaregin karpetaren bidea eta Jaregin karpetaren izena*. Zuk [lortu informazio hau](#setting-up-your-dun--bradstreet-project) Dun & Bradstreet proiektutik.

1. Berrikusi eta eman zure baimena **Datuen pribatutasuna eta betetzea** hautatuz **Ados**.

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitu ondoren, hautatu **Gorde**.

   :::image type="content" source="media/enrichment-dnb-connection.png" alt-text="Dun & Bradstreet konexioaren konfigurazio orria.":::

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberastea freskatu ondoren, azpian dagoen enpresa aberastutako datuak berrikus ditzakezu [Nire aberastasunak](enrichment-hub.md). Azken eguneraketaren ordua eta aberastutako profil kopurua aurki ditzakezu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights Dun & Bradstreet-i datuak transmititzeko, datuak betetze-mugatik kanpo transferitzea onartzen duzu Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina zu zara Dun & Bradstreet-ek izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

[!INCLUDE[footer-include](includes/footer-banner.md)]
