---
title: Aberastu bezeroen profilak Azure Maps-en kokapen-datuekin (aurrebista)
description: Azure Maps-en lehenengoen aberasteari buruzko informazio orokorra.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: dfadc08f67beac3fded1a97e557ee9e1880664e0
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9052592"
---
# <a name="enrich-customer-profiles-with-location-data-from-azure-maps-preview"></a>Aberastu bezeroen profilak Azure Maps-en kokapen-datuekin (aurrebista)

Azure Maps-ek kokapenean oinarritutako datuak eta zerbitzuak eskaintzen ditu datu geoespazialetan oinarritutako esperientziak eskaintzeko, kokapen adimen integratuta. Azure Maps-en datuak aberasteko zerbitzuek bezeroei buruzko kokalekuaren informazioaren zehaztasuna hobetzen dute. Helbideen normalizazioa edo latitudea eta longitudea ateratzeko gaitasunak ekartzen ditu Dynamics 365 Customer Insights-era.

## <a name="prerequisites"></a>Aurrebaldintzak

- Azure Maps-en harpidetza aktiboa. Harpidetza lortzeko, [eman izena edo lortu doako proba bat](https://azure.microsoft.com/services/azure-maps/).

- Azure Maps bat [konexioa](connections.md) da [konfiguratuta](#configure-the-connection-for-azure-maps) administratzaile batek.

## <a name="configure-the-connection-for-azure-maps"></a>Konfiguratu Azure Maps-en konexioa

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta Azure Maps API gako aktibo bat daukazu.

1. Aberastea konfiguratzean, hautatu **Gehitu konexioa** edo joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** Azure Maps-en lauzan.

   :::image type="content" source="media/enrichment-azure-maps-connection.png" alt-text="Azure Maps konexioaren konfigurazio-orria.":::

1. Sartu konexiorako izen bat eta baliozko Azure Maps API gako bat.

1. Berrikusi eta eman zure baimena [Datuen pribatutasuna eta betetzea](#data-privacy-and-compliance) hautatuz **Ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

### <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Datuak Azure Maps-era transmititzeko aukera gaituz gero Dynamics 365 Customer Insights-en, onartu egingo duzu datuak Dynamics 365 Customer Insights-en arau-gordetze eremutik kanpora transferitzea (kontuzkoak izan daitezkeen datuak barne, hala nola datu pertsonalak). Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina zu zara Azure Maps-ek izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, joan [Microsoft-en pribatutasun adierazpenera](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Kokapena** tik Microsoft Azure Mapak lauza.

   :::image type="content" source="media/azure-maps-tile.png" alt-text="Azure Maps lauza.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu Microsoft-en datuekin aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, eta segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Zehaztu zure profil bateratuetako zein eremu mota erabiliko dituzun parekatzeko: helbidea nagusia eta/edo bigarren mailakoa. Bi helbideen eremuen mapak zehaztu ditzakezu eta bi helbideen profilak bereiz aberastu. Adibidez, etxeko helbidea eta negozioaren helbidea. Hautatu **Hurrengoa**.

1. Mapeatu zure eremuak Azure Maps-eko kokapen-datuekin. **1. kalea** eta **Zip / Posta Kodea** eremuak derrigorrezkoak dira hautatutako lehen eta / edo bigarren mailako helbidean. Bat-etortzeen zehaztasun handiagoa lortzeko, gehitu eremu gehiago.

   :::image type="content" source="media/enrichment-azure-maps-attributes.png" alt-text="Azure Maps atributuen mapak.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Iritzia **Ezarpen aurreratuak** erabilera-kasu aurreratuak kudeatzeko malgutasun handiena eskaintzen dutenak. Hala ere, balio lehenetsi hauek normalean ez dira aldatu behar.

   - **Helbide motak** : Helbideen parekatzerik onena itzultzen da, nahiz eta osatu gabe egon. Helbide osoak soilik lortzeko,&mdash;adibidez, etxearen zenbakia duten helbideak,&mdash;garbitu kontrol-lauki guztiak **Seinalatu helbideak** izan ezik.
   - **Hizkuntza** : Helbideak hizkuntzan itzultzen dira helbide-eskualdearen arabera. Helbideen hizkuntza estandarizatua aplikatzeko, hautatu hizkuntza goitibeherako menutik. Adibidez, hautatzea **ingelesa** itzultzen **Kopenhage, Danimarka** ordez **København, Danimarka**.
   - **Gehienezko emaitza kopurua** : Helbide bakoitzeko emaitza kopurua.

1. Hautatu **Hurrengoa**.

1. Eman a **Izena** aberasteko eta **Irteerako entitatearen izena**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

The **Alorka aberastutako bezero kopurua** aberasturiko eremu bakoitzaren estaldura sakontzen du.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
