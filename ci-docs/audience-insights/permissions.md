---
title: Kudeatu erabiltzaile-baimenak
description: Lortu baimenei eta erabiltzaile-funtzioei buruzko informazio gehiago.
ms.date: 03/25/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
manager: shellyha
ms.openlocfilehash: 8638489dba908d4504278916d2c28454e3ea9e18
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760358"
---
# <a name="user-permissions"></a>Erabiltzailearen baimenak

**Baimenak** orrialdean hartzaileei buruzko xehetasunak erabiltzeko funtzioak eta baimenak konfiguratuko dituzu.

Orrialdea ikusteko administratzaile baimenak izan behar dituzu. Hartzaileen xehetasunetako baimenen orrira sartzeko, joan hona: **Administratzailea** > **Baimenak**.

Hiru funtzio mota daude:

## <a name="viewer"></a>Ikuslea

- Arakatu xehetasunak eta segmentuak **Etxea** eta **Segmentuak** orrietan.
- Bilatu eta iragazi bezeroen profilak erabiliz **Bezeroak** orria. Eremuak bilatzeko aukera izan behar dute.
- Ikusi eta arakatu **Aberastea** orria.
- Arakatu eta esportatu erakundeak erabiliz **erakundeak** orria.
- Ikusi sistemaren prozesuen egoera **Sistema** orria.
- Ikusi esportazioak hemen **Esportazioak** orrialdea.
- Instalatu eta erabili **Power BI Customer Insights** panela.

## <a name="contributor"></a>Kolaboratzailea

- Ikuslearen esku dauden baimen guztiak.
- Kargatu eta eraldatu datuak **Datu-iturburuak** orria erabiliz.
- Osatu *Datuen bateratzea* atalak (**Esleitu**, **Bat-etorri**, eta **Konbinatu**), zeintzuk bezeroaren profil bateratuaren entitatea ematen baituten.
- Definitu **Harremanak** eta **jarduerak**.
- Sortu segmentuak **Segmentuak** orria erabiliz.
- Sortu neurriak erabiliz **Neurriak** orria.
- Kudeatu eta konfiguratu bezeroen profilak **aberastea** orria (lehen alderdiko aberasketetarako bakarrik).
- Kudeatu eta sortu esportazioak laguntzaileekin partekatutako konexioetan oinarrituta. [Lortu informazio gehiago administratzaileek laguntzaileei nola esportazioetarako konexio bat erabiltzea onartzen duten jakiteko](connections.md#allow-contributors-to-use-a-connection-for-exports).

## <a name="administrator"></a>Administratzailea

- Kolaboratzailearen esku dauden baimen guztiak.
- Aldatu ezarpenak **Sistema** orrian, zure sistemaren prozesuetarako laneko hizkuntza eta freskatze ordutegiak barne.
- Ikusi eta gehitu baimenak **Baimenak** orria erabiliz.
- Ezarri bilaketa eta Bezeroak orriko iragazkien definizioak **Bilaketa- eta iragazki-aurkibidea** orria erabiliz (**Bezeroak** orriaren bidez atzi daiteke).
- Kudeatu konexioak eta onar itzazu beste erabiltzaile rolak **Konexioak** orrialdea.
- Kudeatu eta konfiguratu bezeroen profilak **aberastea** orria (aberasketa guztietarako).
- Kudeatu eta sortu esportazioak **Esportazioak** orrialdea.
- Instalatu eta erabili **Bezeroaren txartelaren osagarria**.
- Gehitu eta erabili **Power Apps konektorea**.
- Gaitu [Customer Insights APIen](apis.md) erabilera.

## <a name="assign-roles-and-permissions"></a>Rolak eta baimenak esleitu

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Baimenak**.

1. Aukeratu **Gehitu erabiltzaileak** **Gehitu / Editatu baimenak** panela irekitzeko.

1. Erabili **Bilaketa** eremua aurkitzeko Azure Active Directory erabiltzaile edo taldea doitu nahi dituzun baimenak. Aukeratu a **Funtzioa** erabiltzaile edo talde horri esleitzeko.

1. Sakatu **Gorde**. Uneko ingurunea automatikoki partekatuko da baimenak aldatu dituzun erabiltzailearekin edo taldeko kideekin. Erabiltzaileek Customer Insights aplikaziora sartu eta beraien zehaztutako eginkizunaren arabera lan egin dezakete.

## <a name="view-current-permissions"></a>Ikusi uneko baimenak

Hartzaileen xehetasunetan, joan **Administratzailea** > **Baimenak** atalera une honetan zein funtzio-esleipen dauden aktibo ikusteko.

- **Mota** zutabeak erabiltzaile, talde edo aplikazio bakarra zehazten du. Sistemak erabiltzaile eta talde indibidualak onartzen ditu.
- Rolak azpian zehazten dira **Rola** zutabea.
- Hautatu zutabeetako edozein titulu emaitzak emaitzak zutabe horren balioaren arabera ordenatzeko.
- Erabili **Bilatu** eremua orrialdearen goialdean erabiltzaile jakinak kokatzeko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
