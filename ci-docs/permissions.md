---
title: Kudeatu erabiltzaile-baimenak
description: Lortu baimenei eta erabiltzaile-funtzioei buruzko informazio gehiago.
ms.date: 02/09/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
manager: shellyha
searchScope:
- ci-permissions
- ci-system-security
- customerInsights
ms.openlocfilehash: b80f07dfa734f4dd762bd711151a7045f24bed7d
ms.sourcegitcommit: cf74b8c20d88eb96e1ac86e18cd44fe27aad5ab9
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/28/2022
ms.locfileid: "8653553"
---
# <a name="user-permissions"></a>Erabiltzailearen baimenak

The **Baimenak** orrialdean bertan ezarriko dituzu Customer Insights erabiltzeko rolak eta baimenak.

Orrialdea ikusteko administratzaile baimenak izan behar dituzu. Baimenen orrira sartzeko, joan hona **Admin** > **Segurtasuna** > **Erabiltzaileak**.

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

## <a name="admin"></a>Admin

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
- [Esleitu ingurumenaren jabetza](manage-environments.md#change-the-owner-of-an-environment) beste administratzaile bati.

## <a name="admin-owner"></a>Administratzailea (jabea)

- Administratzailearen eskura dauden baimen guztiak.
- [Berrezarri eta ezabatu](manage-environments.md#reset-an-existing-environment) Ingurumena.

## <a name="assign-roles-and-permissions"></a>Rolak eta baimenak esleitu

1. Joan **Admin** > **Segurtasuna** > **Erabiltzaileak***.

1. Aukeratu **Gehitu erabiltzaileak** **Gehitu / Editatu baimenak** panela irekitzeko.

1. Erabili **Bilaketa** eremua aurkitzeko Azure Active Directory erabiltzaile edo taldea doitu nahi dituzun baimenak. Aukeratu a **Funtzioa** erabiltzaile edo talde horri esleitzeko.

1. Sakatu **Gorde**. Uneko ingurunea automatikoki partekatuko da baimenak aldatu dituzun erabiltzailearekin edo taldeko kideekin. Erabiltzaileek Customer Insights aplikaziora sartu eta beraien zehaztutako eginkizunaren arabera lan egin dezakete.

## <a name="view-current-permissions"></a>Ikusi uneko baimenak

Joan **Admin** > **Segurtasuna** > **Erabiltzaileak** une honetan zein rol-esleipen dauden aktibo ikusteko.

- **Mota** zutabeak erabiltzaile, talde edo aplikazio bakarra zehazten du. Sistemak erabiltzaile eta talde indibidualak onartzen ditu.
- Rolak azpian zehazten dira **Rola** zutabea.
- Hautatu zutabeetako edozein titulu emaitzak emaitzak zutabe horren balioaren arabera ordenatzeko.
- Erabili **Bilatu** eremua orrialdearen goialdean erabiltzaile jakinak kokatzeko.


[!INCLUDE [footer-include](includes/footer-banner.md)]