---
title: Teams-en bot-a Dynamics 365 Customer Insights-erako (aurrebista)
description: Bilatu bezeroen profil bateratuak Microsoft Teams-en bot baten laguntzarekin.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: d140ae72578b48091a41005c4acafe03bac540da
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195827"
---
# <a name="teams-bot-for-dynamics-365-customer-insights-preview"></a>Teams-en bot-a Dynamics 365 Customer Insights-erako (aurrebista)

Konektatu Microsoft Teams-ekin, bot batek bezeroen profil bateratuak bilatzeko Teams kanaletan.

:::image type="content" source="media/teams-bot.png" alt-text="Taldeak bezeroaren erregistroa erakusten duten botak":::

## <a name="prerequisites"></a>Aurrebaldintzak

- Bat behintzat [datu-iturburu gehitu da](data-sources.md).
- [Bateratze prozesua](data-unification.md) osatu da.
- Eremuak gehitzen zaizkio [bilatu eta iragazi indizea](search-filter-index.md).
- Customer Insights eta taldeak antolaketa berean daude.
- Zure inguruneak bezero partikularrei ezarri die helburu nagusia. Enpresa kontuak ez dira onartzen.


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWRElj]

## <a name="configure-the-bot"></a>Konfiguratu bota

1. Joan **Administratzailea** > **Konexioak**.
1. Gainean Microsoft Teams fitxa, hautatu **Konfiguratu**.
1. Hara birbideratu zara **Aplikazioak** eremua Taldeetan. Taldeak ere ireki eta hautatu ditzakezu **Aplikazioak** behe-ezkerreko izkinan edo [atera ezazu AppSource](https://go.microsoft.com/fwlink/?linkid=2124104) zuzenean.
1. Bilatu **Customer Insights** eta hautatu aplikazioa.
1. Hautatu **Gehitu**.
1. Hasi saioa Customer Insights-en Teams-en. Ongietorri mezu bat agertzen da.

## <a name="things-you-can-do-with-the-bot"></a>Botarekin egin ditzakezun gauzak

Botak bezeroaren profil bateratuak bilatzeko gaitasunak eskaintzen ditu.

- Sartu **bilatu** ondoren, bilaketa eta iragazkien indizean gehitzen den bezero-profil bateratuko beste edozein eremuren izena, helbide elektronikoa edo.

  Lortutako bezeroen profiletik 15 eremu gehienez 15 txartel jasoko dituzu. Hainbat partiduren bidez, profil bat hauta dezakezu emaitza guztien zerrenda itzultzen da. Bat-etortze zehatz bat bilatzeko, gehitu bilaketa-terminoa komatxo bikoitz artean.

- Zure erakundeak Customer Insights ingurune anitz mantentzen baditu erakunde berean, sartu **switchinstantzia** bot-a zein ingurunetara konektatu nahi duzun aukeratzeko.

- Sartu **laguntza** boterako erabilgarri dauden komandoen zerrenda ikusteko.  

[!INCLUDE [footer-include](includes/footer-banner.md)]