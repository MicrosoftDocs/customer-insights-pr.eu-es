---
title: Esportatu segmentuak AdRoll-era (aurrebista)
description: Ikasi konexioa nola konfiguratu eta AdRoll-era esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 81adad4caf2d4c6f792bf920b29fc7c67eef42b0
ms.sourcegitcommit: c3ae7e7e0c9566f9479ba71a26afc5a17fb589c2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/27/2022
ms.locfileid: "9724663"
---
# <a name="export-segments-to-adroll-preview"></a>Esportatu segmentuak AdRoll-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak AdRoll-era eta erabili iragarkietarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- An [AdRoll kontua](https://www.adroll.com/) eta dagozkion administratzailearen kredentzialak.
- An [AdRoll iragarle IDa](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Ez da onartzen Bring your own storage (BYOS) esteka pribatua.
- Gehienez 250.000 bezero-profil AdRoll-era esportatzeko, 10 minutu arte iraun ditzake. AdRoll-era esporta dezakezun bezero-profilen kopurua AdRoll-ekin duzun kontratuaren araberakoa da.
- Segmentuak soilik. Segmentu batek gutxienez 100 bezero-profil izan behar ditu.

## <a name="set-up-connection-to-adroll"></a>Konfiguratu konexioa AdRoll-ra

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **AdRoll**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Egiaztatu AdRoll-ekin** eta eman zure administraziorako AdRoll kredentzialak.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa AdRoll sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **AdRoll iragarlearen IDa**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
