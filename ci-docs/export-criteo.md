---
title: Esportatu segmentuak Criteo-ra (aurrebista)
description: Ikasi nola konfiguratu konexioa eta nola esportatu Criteora.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 811752da943cd5e40608d48644a1744c7971d3c8
ms.sourcegitcommit: 40ae3322ac95913e485607494754dd03814e42bb
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/11/2022
ms.locfileid: "9760011"
---
# <a name="export-segments-to-criteo-preview"></a>Esportatu segmentuak Criteo-ra (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak kanpainak sortzeko, posta elektronikoko marketina eskaintzeko eta bezero talde zehatzak erabiltzeko Criteorekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Criteo Dynamics Retargeting kontua](https://www.criteo.com/login/) eta dagozkion administratzailearen kredentzialak.
- [Konfiguratutako segmentuak](segments.md).
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero profil Criteo-ra esportatzeko, eta hori osatzeko 30 minutu behar izan daitezke. Criteora esporta ditzakezun bezero-profilen kopurua Criteorekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-criteo"></a>Konfiguratu Criteo-rekin konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Kriteo**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados** .

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Hautatu **Autentifikatu Criteo-rekin** eta eman zure Admin erabiltzaile-izena eta kredentzialak Criteorako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa** .

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Criteo atalean. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
