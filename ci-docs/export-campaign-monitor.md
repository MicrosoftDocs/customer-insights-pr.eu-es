---
title: Esportatu segmentuak Campaign Monitor-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Campaign Monitor.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 82303c7bcb269ee68419c9639ee743e13451f273
ms.sourcegitcommit: c3ae7e7e0c9566f9479ba71a26afc5a17fb589c2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/27/2022
ms.locfileid: "9724533"
---
# <a name="export-segments-to-campaign-monitor-preview"></a>Esportatu segmentuak Campaign Monitor-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Campaign Monitor-era eta erabili marketin jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Campaign Monitor kontua](https://www.campaignmonitor.com/) eta dagozkion administratzailearen kredentzialak.
- A [Campaign Monitor zerrendaren IDa](https://www.campaignmonitor.com/api/getting-started/#your-list-id).
- A [Sortutako API gakoa](https://www.campaignmonitor.com/api/getting-started/) tik **Kontu ezarpenak** Campaign Monitor-en API zerrendaren IDa lortzeko.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Ez da onartzen Bring your own storage (BYOS) esteka pribatua.
- Gehienez milioi bat bezero-profil Esportazio bakoitzeko Campaign Monitor-era, eta hori osatzeko 20 minutu behar izan daitezke. Campaign Monitor-era esporta dezakezun bezero-profilen kopurua Campaign Monitor-ekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-campaign-monitor"></a>Konfiguratu konexioa Campaign Monitor

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Kanpainaren monitorea**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Aukeratu **Konektatu** Campaign Monitor konexioa hasieratzeko.

1. Aukeratu **Autenticatu Campaign Monitor-ekin** eta eman zure administratzaile egiaztagiriak Campaign Monitor-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Campaign Monitor sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **Campaign Monitor zerrendaren IDa**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. Segmentuak esportatu behar dira Campaign Monitor.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
