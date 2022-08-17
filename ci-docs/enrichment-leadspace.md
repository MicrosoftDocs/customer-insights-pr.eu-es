---
title: Aberastu enpresaren profilak Leadspace-rekin (aurrebista)
description: Leadspace-ren hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 08/08/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: f45fabc036775e11fc439f69513678d0607729d0
ms.sourcegitcommit: b1d06fe26934f12f0c5ed13e8ef1d37e52e67cc7
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/08/2022
ms.locfileid: "9237935"
---
# <a name="enrich-company-profiles-with-leadspace-preview"></a>Aberastu enpresaren profilak Leadspace-rekin (aurrebista)

Leadspace datu-zientzietako enpresa bat da, B-to-B Bezeroentzako Datuen Plataforma eskaintzen duena. Kontuetan oinarritutako bezeroen profil bateratuak dituzten inguruneak ahalbidetzen ditu beren datuak aberasteko. Aberastu *Bezeroen profilak* enpresaren tamaina, kokapena edo industria bezalako atributuekin. Aberastu *Harremanetarako profilak* izenburua, pertsona edo posta elektronikoa egiaztatzea bezalako atributuekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- Leadspace lizentzia aktiboa.
- [Bezeroen profil bateratuak](customer-profiles.md) kontuetan oinarrituta.
- Leadspace bat [konexioa](connections.md) da [konfiguratuta](#configure-the-connection-for-leadspace) administratzaile batek. Harremanetarako [Leadspace](https://www.leadspace.com/leadspace-microsoft-dynamics-365/) zuzenean produktuaren inguruko xehetasunak lortzeko.

## <a name="configure-the-connection-for-leadspace"></a>Konfiguratu konexioa Leadspace-rako

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta "betiko giltza" dute (deitzen zaio **Leadspace tokena**).

1. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean edo joan **Admin** > **Konexioak** eta hautatu **Konfiguratu** Leadspace fitxan.

   :::image type="content" source="media/enrichment-Leadspace-connection.png" alt-text="Leadspace konexioa konfigurazioaren orria.":::

1. Sartu konexiorako izen bat eta baliozko Leadspace token bat.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Enpresaren datuak** Leadspace fitxatik.

   :::image type="content" source="media/leadspace-tile.png" alt-text="Leadspace lauzaren pantaila-argazkia.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu Leadspace enpresako datuekin aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

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
