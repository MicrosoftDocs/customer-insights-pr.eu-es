---
title: Esleitu erabiltzaile-baimenak
description: Lortu baimenei eta erabiltzaile-funtzioei buruzko informazio gehiago.
ms.date: 08/08/2022
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
ms.openlocfilehash: a59a672b6f7e1e67c2162ea14bb9860df0d551aa
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9245404"
---
# <a name="assign-user-permissions"></a>Esleitu erabiltzaile-baimenak

Customer Insights-erako sarbidea administratzaile batek aplikazioan gehitzen dituen zure erakundeko erabiltzaileei mugatuta dago. Administratzaile batek erabiltzaileak gehitu, editatu edo kendu ditzake. Erabiltzaile bat erabiltzaile, talde edo aplikazio bakarra izan daiteke. Erabiltzaile batek hiru rol mota izan ditzake:

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
- Osatu **Datuen bateratzea** eta horrek bezeroen profil bateratu entitatea sortzen du.
- Definitu **Harremanak** eta **jarduerak**.
- Sortu segmentuak **Segmentuak** orria erabiliz.
- Sortu neurriak erabiliz **Neurriak** orria.
- Kudeatu eta konfiguratu bezeroen profilak **aberastea** orria (lehen alderdiko aberasketetarako bakarrik).
- Kudeatu eta sortu esportazioak oinarrituta [laguntzaileekin partekatutako konexioak](connections.md#allow-contributors-to-use-a-connection-for-exports).

## <a name="admin"></a>Admin

- Kolaboratzailearen esku dauden baimen guztiak.
- Aldatu ezarpenak **Sistema** orrialdea, lan-hizkuntza barne, zure sistema-prozesuen freskatze-programazioak eta diagnostiko-erregistroak esportatzea.
- Aldatu ezarpenak **Segurtasuna** orrialdea, erabiltzaileak, API gakoak, esteka pribatuak eta gakoen ganga barne.
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
- [Berrezarri eta ezabatu](manage-environments.md#reset-an-existing-environment-preview) Ingurumena.

## <a name="add-users"></a>Gehitu erabiltzaileak

1. Joan **Admin** > **Segurtasuna** eta hautatu **Erabiltzaileak** fitxa.

1. Aukeratu **Gehitu erabiltzaileak** **Gehitu / Editatu baimenak** panela irekitzeko.

1. Erabili **Bilatu** eremua aurkitzeko Azure Active Directory gehitu nahi duzun erabiltzailea edo taldea. Aukeratu a **Funtzioa** erabiltzaile edo talde horri esleitzeko.

1. Sakatu **Gorde**. Uneko ingurunea automatikoki partekatzen da erabiltzailearekin edo taldeko kideekin. Erabiltzaileek Customer Insights aplikaziora sartu eta beraien zehaztutako eginkizunaren arabera lan egin dezakete.

## <a name="view-current-permissions"></a>Ikusi uneko baimenak

Joan **Admin** > **Segurtasuna** eta hautatu **Erabiltzaileak** fitxa erabiltzaile aktiboen zerrenda eta haien rol-esleipenak ikusteko. Erabiltzaileen zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabil dezakezu erabiltzaile jakin bat aurkitzeko.

## <a name="manage-current-users"></a>Kudeatu egungo erabiltzaileak

Joan **Admin** > **Segurtasuna** eta hautatu **Erabiltzaileak** fitxa. Erabiltzaileen zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun erabiltzailea aurkitzeko.

Hautatu erabiltzaile bat erabilgarri dauden ekintzak ikusteko.

- **Editatu** erabiltzailearen rola editatzeko Customer Insights-en. Hautatu **Gorde** aldaketa berresteko.
- **Kendu** erabiltzaileari Customer Insights-etarako sarbidea kentzeko. Hautatu **Ezabatu** ezabatzea baieztatzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
