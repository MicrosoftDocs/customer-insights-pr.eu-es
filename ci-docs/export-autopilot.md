---
title: Esportatu segmentuak Autopilot-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta pilotu automatora esportatzen.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 449d2c5e32697e4a5d2c9dff4a5a1cbdb26aeb4d
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195045"
---
# <a name="export-segments-to-autopilot-preview"></a>Esportatu segmentuak Autopilot-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Autopilot kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko Autopilot-en.

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

- An [Pilotu automatikoaren kontua](https://www.autopilothq.com/) eta dagozkion administratzailearen kredentzialak.
- An [Autopilot API gakoa](https://autopilot.docs.apiary.io/#)
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 100.000 bezero-profil esportazio bakoitzeko Autopilot-era, eta hori osatzeko ordu batzuk behar izan daitezke. Autopilot-era esporta dezakezun bezero-profilen kopurua Autopilot-ekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-autopilot"></a>Konfiguratu konexioa Autopilot-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Pilotu automatikoa**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure Pilotatze automatikoaren API gakoa.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Autopilot sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, esportatu beste eremu batzuk, adibidez **izen** eta **abizen**.

1. Hautatu esportatu nahi dituzun segmentuak ezagutzen diren mugei atxikita.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
