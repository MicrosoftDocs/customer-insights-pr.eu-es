---
title: Esportatu segmentuak ActiveCampaign-era
description: Ikasi konexioa nola konfiguratu eta ActiveCampaign-ra esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 178d2df8edf1abcec72664e19d73a88f2b97f12d
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195551"
---
# <a name="export-segments-to-activecampaign-preview"></a>Esportatu segmentuak ActiveCampaign-ra (aurrebista)

Esportatu bezero profil bateratuen segmentuak ActiveCampaign-era eta erabili marketin-jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- An [ActiveCampaign kontua](https://www.activecampaign.com/) eta dagozkion administratzailearen kredentzialak.
- An [ActiveCampaign zerrendaren IDa](https://help.activecampaign.com/hc/articles/360000030559-How-to-create-a-list-in-ActiveCampaign).
- An [ActiveCampaign API gakoa](https://help.activecampaign.com/hc/articles/207317590-Getting-started-with-the-API#how-to-obtain-your-activecampaign-api-url-and-key) eta REST Endpoint Hostname.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero-profil ActiveCampaign-era esportatzeko, eta hori osatzeko 90 minutu behar izan daitezke. ActiveCampaign-era esporta ditzakezun bezeroen profil kopurua ActiveCampaign-ekin duzun kontratuaren menpe dago eta mugatua da.
- Segmentuak soilik.

## <a name="set-up-connection-to-activecampaign"></a>Konfiguratu ActiveCampaign-era konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **ActiveCampaign**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure ActiveCampaign API gakoa eta REST amaiera puntuko ostalari izena. REST Endpoint ostalari izena ostalari izena soilik da, gabe https://.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Urtean **Esportaziorako konexioa** eremuan, aukeratu konexio bat ActiveCampaign atalean. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **ActiveCampaign zerrendaren IDa**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, esportatu **izen**, **·**, eta **Mugikorra** mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
