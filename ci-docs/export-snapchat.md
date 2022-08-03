---
title: Esportatu segmentuak Snapchat-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Snapchat.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 85443dcb54ebd58182997fbb56a738901f2a051f
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195367"
---
# <a name="export-segments-to-snapchat-preview"></a>Esportatu segmentuak Snapchat-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Snapchat eta erabili iragarkietarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Snapchat Enpresa kontua](https://business.snapchat.com/), a [Snapchat Ads kontua](https://ads.snapchat.com/), eta dagozkion administratzailearen kredentzialak. Gutxienez Erakunde-kontu bateko kide eta Iragarki-kontu zehatz bateko Datu-kudeatzailea izan behar duzu.
- Gutxienez publiko bat SAM (Snap Audience Match) motako Snapchat Audience kudeatzailean.
- The [Snapchat Segmentua/Ikusleen IDa](https://businesshelp.snapchat.com/s/article/custom-audiences). Entzuleen IDa URLan aurki daiteke Snapchat Audience Manager-en audientzia hautatu ondoren.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero-profil, 15 minutu iraun ditzakete osatzeko.
- Segmentuak soilik.

## <a name="set-up-connection-to-snapchat"></a>Konfiguratu konexioa Snapchat-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Snapchat**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Autenticatu Snapchat-ekin** eta eman zure administratzaile egiaztagiriak Snapchat-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Snapchat sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu **Snapchat Segmentua/Ikusleen IDa**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
