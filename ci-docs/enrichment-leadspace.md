---
title: Aberastu enpresaren profilak Leadspace-rekin (aurrebista)
description: Leadspace-ren hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: b58532a541ee22a5e34d0af1a3334ccbd53627b2
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9082358"
---
# <a name="enrich-company-profiles-with-leadspace-preview"></a>Aberastu enpresaren profilak Leadspace-rekin (aurrebista)

Leadspace datu-zientzietako enpresa bat da, B-to-B Bezeroentzako Datuen Plataforma eskaintzen duena. Kontuetan oinarritutako bezeroen profil bateratuak dituzten inguruneak ahalbidetzen ditu beren datuak aberasteko. Aberastu *Bezeroen profilak* enpresaren tamaina, kokapena edo industria bezalako atributuekin. Aberastu *Harremanetarako profilak* izenburua, pertsona edo posta elektronikoa egiaztatzea bezalako atributuekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- Leadspace lizentzia aktiboa.
- [Bezeroen profil bateratuak](customer-profiles.md) kontuetan oinarrituta.
- Leadspace bat [konexioa](connections.md) da [konfiguratuta](#configure-the-connection-for-leadspace) administratzaile batek. Harremanetarako [Leadspace](https://www.leadspace.com/leadspace-microsoft-dynamics-365/) zuzenean produktuaren inguruko xehetasunak lortzeko.

## <a name="configure-the-connection-for-leadspace"></a>Konfiguratu konexioa Leadspace-rako

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta "betiko giltza" dute (deitzen dena **Leadspace tokena**).

1. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean edo joan **Admin** > **Konexioak** eta hautatu **Konfiguratu** Leadspace fitxan.

   :::image type="content" source="media/enrichment-Leadspace-connection.png" alt-text="Leadspace konexioa konfigurazioaren orria.":::

1. Sartu konexiorako izen bat eta baliozko Leadspace token bat.

1. Berrikusi eta eman zure baimena [Datuen pribatutasuna eta betetzea](#data-privacy-and-compliance) hautatuz **Ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

### <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Leadspace-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Leadspace-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Enpresaren datuak** Leadspace fitxatik.

   :::image type="content" source="media/leadspace-tile.png" alt-text="Leadspace lauzaren pantaila-argazkia.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa. Jarri harremanetan administratzaile batekin erabilgarri ez badago.

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu Leadspace enpresako datuekin aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, eta segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

    :::image type="content" source="media/enrichment-Leadspace-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Zehaztu zure profil bateratuetako zein eremu mota erabiliko dituzun parekatzeko: helbidea nagusia eta/edo bigarren mailakoa. Bi helbideen eremuen mapak zehaztu ditzakezu eta bi helbideen profilak bereiz aberastu. Adibidez, etxeko helbidea eta negozioaren helbidea. Hautatu **Hurrengoa**.

1. Mapeatu zure eremuak Leadspace-ko konpainiaren datuekin. **Enpresaren izena** eremua beharrezkoa da. Bat-etortzeen zehaztasun handiagoa lortzeko, beste bi eremu, **Enpresaren webgunea** eta **Enpresaren kokapena**, gehitu daitezke.

   :::image type="content" source="media/enrichment-leadspace-mapping.png" alt-text="Leadspace eremuak esleitzeko panela.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Hautatu kontrol laukia baduzu *Harremanetarako profilak* aberastu nahiko zenukeela. Customer Insights-ek automatikoki mapatuko ditu beharrezko eremuak.

   :::image type="content" source="media/enrichment-leadspace-contacts.png" alt-text="Leadspace kontaktuak aberastu egiten du.":::

1. Hautatu **Hurrengoa**.

1. Eman a **Izena** aberasteko eta **Irteerako entitatearen izena**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

Informazio gehiago lortzeko, ikus [Leadspace API](https://support.leadspace.com/hc/en-us/sections/201997649-API).

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
