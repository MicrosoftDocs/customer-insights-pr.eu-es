---
title: Microsoft Teams-eko bot-a
description: Bilatu bezeroen profil bateratuak Microsoft Teams-en bot baten laguntzarekin.
ms.date: 10/08/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: cff696834e3dad00ce5b0f1b5bcb13d86354a4e7
ms.sourcegitcommit: 23c8973a726b15050e368cc6e0aab78b266a89f6
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/08/2021
ms.locfileid: "7617586"
---
# <a name="teams-bot-for-dynamics-365-customer-insights-preview"></a>Teams-en bot-a Dynamics 365 Customer Insights-erako (aurrebista)

Konektatu Microsoft Teams-ekin, bot batek bezeroen profil bateratuak bilatzeko Teams kanaletan.

> [!div class="mx-imgBorder"]
> ![Taldeak bezeroaren erregistroa erakusten duten botak.](media/teams-bot.png "Taldeak bezeroaren erregistroa erakusten duten botak")

## <a name="prerequisites"></a>Aurrebaldintzak

Bot-a konfiguratzeko eta konfiguratzeko, honako baldintza hauek bete behar dira:

- Gutxienez bat dago [datu-iturburu gehitu da](data-sources.md).
- [Bateratze prozesua](data-unification.md) osatu da.
- Eremuak gehitzen dira [bilaketa eta iragazki indizea](search-filter-index.md).
- Customer Insights eta taldeak antolaketa berean daude.
- Zure inguruneak bezero partikularrei ezarri die helburu nagusia. Enpresa kontuak ez dira onartzen.

## <a name="configure-the-bot"></a>Konfiguratu bota

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.
1. Gainean Microsoft Teams fitxa, hautatu **Konfiguratu**.
1. Hara birbideratu zara **Aplikazioak** eremua Taldeetan. Taldeak ere ireki eta hautatu ditzakezu **Aplikazioak** behe-ezkerreko izkinan edo [atera ezazu AppSource](https://go.microsoft.com/fwlink/?linkid=2124104) zuzenean.
1. Bilatu **Customer Insights** eta hautatu aplikazioa.
1. Hautatu **Gehitu**.
1. Customer Insights taldeetan saioa hasi ondoren, ongietorri mezua ikusiko duzu eta hasteko aukera izango duzu.

## <a name="things-you-can-do-with-the-bot"></a>Botarekin egin ditzakezun gauzak

Botak bezeroaren profil bateratuak bilatzeko gaitasunak eskaintzen ditu.

- Sartu **bilatu** ondoren, bilaketa, iragazki indizean gehitzen den bezeroaren profil bateratuaren izen bat, helbide elektronikoa edo beste edozein eremutan.

  Lortutako bezeroen profiletik 15 eremu gehienez 15 txartel jasoko dituzu. Hainbat partiduren bidez, profil bat hauta dezakezu emaitza guztien zerrenda itzultzen da. Bilaketa terminoa komatxo bikoitzetan gehi dezakezu partida zehatza bilatzeko.

- Zure erakundeak Customer Insights ingurune ugari mantentzen baditu erakunde berean, **aldatu instantzia** atalean sar zaitezke bot-a zein ingurunera konektatu nahi duzun aukeratzeko.

- Sartu **laguntza** boterako erabilgarri dauden komandoen zerrenda ikusteko.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]