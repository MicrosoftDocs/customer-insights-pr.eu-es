---
title: Aberastu bezeroen profilak HERE Teknologiekin (aurrebista)
description: HERE Technologies-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: d88085b6be156dd1c895e9e5b38cc9d77acbdb95
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9052036"
---
# <a name="enrich-customer-profiles-with-here-technologies-preview"></a>Aberastu bezeroen profilak HERE Teknologiekin (aurrebista)

HERE Technologies kokapen-plataformako enpresa da, kokapenari buruzko datuak eta zerbitzuak eskaintzen dituena. HERE Technologies-en datuak aberasteko zerbitzuek zure bezeroei buruzko kokapen-informazioaren zehaztasuna hobetzen dute. Helbideen normalizazioa, latitudea eta longitudea ateratzea eta abar eskaintzen ditu.

## <a name="prerequisites"></a>Aurrebaldintzak

- HERE Teknologien harpidetza aktiboa. Harpidetza lortzeko, [eman izena hemen](https://developer.here.com/sign-up?utm_medium=referral&utm_source=Microsoft-Dynamics-CI&create=Freemium-Basic) edo [jarri harremanetan HEMEN Teknologiak](https://developer.here.com/help?utm_medium=referral&utm_source=Microsoft-Dynamics-CI#how-can-we-help-you) zuzenean. [Lortu informazio gehiago HERE Technologies-en kokapen-aberasteari buruz.](https://developer.here.com/location-enrichment?cid=Dev-MicrosoftDynamics-DB-0-Dev-&utm_source=MicrosoftDynamics&utm_medium=referral&utm_campaign=Online_Dev_ReferralMicrosoft)

- A HEMEN [konexioa](connections.md) da [konfiguratuta](#configure-the-connection-for-here-technologies) administratzaile batek.

## <a name="configure-the-connection-for-here-technologies"></a>Konfiguratu konexioa HERE Technologies

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta HERE Technologies API gako aktibo bat daukazu.

1. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean, edo joan hona **Admin** > **Konexioak** eta hautatu **Konfiguratu** HEMEN Teknologiak fitxan.

1. Sartu konexiorako izen bat eta baliozko HERE Technologies API gako bat.

1. Berrikusi eta eman zure baimena [Datuen pribatutasuna eta betetzea](#data-privacy-and-compliance) hautatuz **Ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

   :::image type="content" source="media/enrichment-HERE-connection.png" alt-text="HEMEN teknologien konexioa konfigurazioaren orria.":::

### <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak HERE Technologies-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da HERE Technologies-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Kokapena** HEMEN Teknologiak fitxa.

   :::image type="content" source="media/HERE-tile.png" alt-text="HERE Technologies-en lauza.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa. Jarri harremanetan administratzaile batekin erabilgarri ez badago.

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu HERE Teknologien datuekin aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, eta segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Zehaztu zure profil bateratuetako zein eremu mota erabiliko dituzun parekatzeko: helbidea nagusia eta/edo bigarren mailakoa. Bi helbideen eremuen mapak zehaztu ditzakezu eta bi helbideen profilak bereiz aberastu. Adibidez, etxeko helbidea eta negozioaren helbidea. Hautatu **Hurrengoa**.

1. Mapeatu zure eremuak HERE Technologies-en datuekin. **1. kalea** eta **Zip / Posta Kodea** eremuak derrigorrezkoak dira hautatutako lehen eta / edo bigarren mailako helbidean. Bat-etortzeen zehaztasun handiagoa lortzeko, gehitu eremu gehiago.

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Eman a **Izena** aberasteko eta **Irteerako entitatearen izena**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

The **Alorka aberastutako bezero kopurua** aberasturiko eremu bakoitzaren estaldura sakontzen du.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
