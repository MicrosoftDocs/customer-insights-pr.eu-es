---
title: Aberastu bezeroen profilak Azure Maps-eko kokalekuen datuekin
description: Azure Maps-en lehenengoen aberasteari buruzko informazio orokorra.
ms.date: 08/31/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: 6d43dc2ca82c034fbd396d92637e7aea8179df77
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755339"
---
# <a name="enrichment-of-customer-profiles-with-azure-maps-preview"></a>Bezeroen profilen aberastea Azure Maps-ekin (aurreargitalpena)

Azure Maps-ek kokalekuan oinarritutako datuak eta zerbitzuak eskaintzen dituzte, kokalekuen adimen integratudun datu geoespazialetan oinarritutako esperientziak eskaintzeko. Azure Maps-en datuak aberasteko zerbitzuek bezeroei buruzko kokalekuaren informazioaren zehaztasuna hobetzen dute. Helbideen normalizazioa edo latitudea eta longitudea ateratzeko gaitasunak ekartzen ditu Dynamics 365 Customer Insights-era.

## <a name="prerequisites"></a>Aurrebaldintzak

Azure Maps-en datuen aberastea konfiguratzeko, aurrebaldintza hauek bete behar dira:

- Azure Maps-en harpidetza aktibo bat duzu. Harpidetza bat lortzeko, [erregistratu edo lortu doako probaldia](https://azure.microsoft.com/services/azure-maps/).

- Azure Maps [konexio](connections.md) bat erabilgarri dago, *edo* [administratzaile](permissions.md#admin) baimenak dituzu eta Azure Maps API gako aktibo bat.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastua**. 

1. **Kokalekua** lauzan, hautatu **Aberastu datuak**.

   :::image type="content" source="media/azure-maps-tile.png" alt-text="Azure Maps lauza.":::

1. Hautatu goitibeherako zerrendako [konexio](connections.md) bat. Azure Maps konexiorik erabilgarri ez badago, jarri harremanetan administratzaile batekin. Administratzaile bat bazara, [Azure Maps-en konexioa konfigura dezakezu](#configure-the-connection-for-azure-maps). 

1. Hautaketa berresteko, hautatu **Hurrengoa**.

1. Aukeratu Azure Maps-eko kokaleku-datuekin aberastu nahi duzun **Bezeroaren datu multzoa**. Bezeroaren profil bateratu guztiak aberasteko, **Bezeroaren** entitatea hauta dezakezu edo segmentuaren entitate bat aukeratu segmentuan dauden bezeroaren profilak soilik aberasteko.

    :::image type="content" source="media/enrichment-azure-maps-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Aukeratu eremuak lehenengo edo bigarren mailako helbideari esleitu nahi dizkiozun. Eremu-esleipen bat zehaz dezakezu bi helbideetarako eta bi helbideen profilak banaka aberastu&mdash;, aidbidez, etxeko eta laneko helbidearen kasuan. Hautatu **Hurrengoa**.

1. Definitu profil bateratuko zein eremu erabili nahi dituzun Azure Maps-eko bat datozen kokaleku-datuak bilatzeko. **Street 1** eta **Zip/Postal Code** eremuak beharrezkoak dira hautatutako lehen edo bigarren mailako helbiderako. Bat-etortzeak zehatzagoak izateko, eremu gehiago gehi ditzakezu.

   :::image type="content" source="media/enrichment-azure-maps-configuration.png" alt-text="Azure Maps aberastearen konfigurazio-orria.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Ebaluatu **ezarpen aurreratuak** aldatu nahi dituzun. Ezarpen hauek erabilera-kasu aurreratuak kudeatzeko malgutasun handiena emateko eskaintzen dira, baina balio lehenetsiak egokiak izango dira kasu gehienetan:
   - **Helbide motak**: portaera lehenetsia da aberasteak helbiderik egokiena itzuliko duela, nahiz eta osatuta ez egon. Helbide osoak soilik lortzeko,&mdash;adibidez, etxearen zenbakia duten helbideak,&mdash;garbitu kontrol-lauki guztiak **Seinalatu helbideak** izan ezik. 
   - **Hizkuntza**: lehenespenez, helbideak itzultzen dira helbideari dagokiola adierazi den eskualdearen hizkuntzan. Helbideen hizkuntza estandarizatua aplikatzeko, hautatu hizkuntza goitibeherako menutik. Adibidez, **Ingelesa** hautatuta, **Copenhagen, Denmark** itzuliko ditu **København, Danmark** itzuli ordez.

1. Idatzi aberastearen izena.

1. Berrikusi zure aukeraketak eta, ondoren, sakatu **gorde aberastea**.

## <a name="configure-the-connection-for-azure-maps"></a>Konfiguratu Azure Maps-en konexioa

Customer Insights-en administratzailea izan behar duzu konexioak konfiguratzeko. Aberastea konfiguratzean, hautatu **Gehitu konexioa** edo joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** Azure Maps-en lauzan.

1. **Bistaratzeko izena** koadroan, idatzi konexioaren izena.

1. Eman balio duen Azure Maps-en API gako bat.

1. Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitu ondoren, hautatu **Gorde**.

:::image type="content" source="media/enrichment-azure-maps-connection.png" alt-text="Azure Maps konexioaren konfigurazio-orria.":::

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesamenduaren iraupena bezeroaren datuen tamainaren eta APIaren erantzunaren iraupenaren araberakoa da.

Aberaste-prozesua osatu ondoren, berriki aberastutako bezeroen profilak berrikus ditzakezu **Nire aberasteak** atalean. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Datuak Azure Maps-era transmititzeko aukera gaituz gero Dynamics 365 Customer Insights-en, onartu egingo duzu datuak Dynamics 365 Customer Insights-en arau-gordetze eremutik kanpora transferitzea (kontuzkoak izan daitezkeen datuak barne, hala nola datu pertsonalak). Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina zu zara Azure Maps-ek izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, joan [Microsoft-en pribatutasun adierazpenera](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
