---
title: Esportatu Customer Insights datuak HubSpot-era
description: Ikasi konexioa konfiguratzen eta HubSpot-era esportatzen.
ms.date: 09/23/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: b34f1d54fa499f6c6b80fa547a8aaf61af3b35a1
ms.sourcegitcommit: c3ae7e7e0c9566f9479ba71a26afc5a17fb589c2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725339"
---
# <a name="export-segments-to-hubspot-preview"></a>Esportatu segmentuak HubSpot-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak HubSpot-era eta erabili posta elektroniko bidezko marketinerako.

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

- A [HubSpot kontua](https://www.hubspot.com/) eta dagozkion administratzailearen kredentzialak.
- [API gakoa](https://knowledge.hubspot.com/Integrations/How-do-I-get-my-HubSpot-API-key) HubSpot-etik.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.

## <a name="known-limitations"></a>Muga ezagunak

- Ez da onartzen Bring your own storage (BYOS) esteka pribatua.
- Gehienez 100.000 bezero-profil HubSpot-era esportatzeko, 15 minutu arte iraun ditzake. HubSpot-era esporta dezakezun bezero-profilen kopurua HubSpot-ekin duzun kontratuaren araberakoa eta mugatua da.
- Segmentuak soilik.

## <a name="set-up-connection-to-hubspot"></a>Konfiguratu HubSpot-erako konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **HubSpot** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Idatzi zure HubSpot-eko kredentzialak eskatzen dionean.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** HubSpot-erako konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat HubSpot atalean. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. Errepikatu urrats berdinak aukerako beste eremuetarako.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
