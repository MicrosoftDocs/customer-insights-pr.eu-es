---
title: Esportatu segmentuak Braze-ra (aurrebista)
description: Ikasi nola konfiguratu konexioa eta Braze-ra esportatzen.
ms.date: 10/06/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: a3967008ec166cb6f099659b0791f1318126c0da
ms.sourcegitcommit: c3ae7e7e0c9566f9479ba71a26afc5a17fb589c2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725201"
---
# <a name="export-segments-to-braze-preview"></a>Esportatu segmentuak Braze-ra (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Braze-ra eta erabili marketin-jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Braze kontua](https://www.braze.com/) eta dagozkion administratzailearen kredentzialak.
- A [Braze API gakoa](https://www.braze.com/docs/api/basics/)
- Zure [Braze REST amaiera-puntua](https://www.braze.com/docs/api/basics/#api-definitions) 
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezero-profil bateratuek helbide elektroniko bat eta Braze bezero ID bat adierazten duten eremu bat dute.

## <a name="known-limitations"></a>Muga ezagunak

- Ez da onartzen Bring your own storage (BYOS) esteka pribatua.
- Gehienez milioi bat bezero profil Braze-ra, 40 minutu arte iraun dezaketenak osatzeko. Braze-ra esporta dezakezun bezero-profilen kopurua Brazerekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.
- Azure Private Link ez da onartzen Braze esportatzeko.

## <a name="set-up-connection-to-braze"></a>Konfiguratu Braze-rekin konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Braze**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman zure Braze API gakoa saioa hasten jarraitzeko.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Braze ataleko. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Sartu zure REST Endpoint-en **Ostalari izena** eremua formatu honetan:`rest.iad-03.braze.com`.

1. Idatzi esportaziorako izen bat.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. urtean **Bezeroaren IDa** eremuan, hautatu bezeroaren Braze IDa adierazten duen eremua. Braze-ko segmentuak atalean dagoen segmentuaren izen berarekin sortuko dira Dynamics 365 Customer Insights. Datuak lotzeko aukerako eremu gehiago hauta ditzakezu.

1. Hautatu esportatu nahi dituzun entitateak edo segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
