---
title: Esportatu segmentuak MoEngage-ra
description: Ikasi nola konfiguratu konexioa eta MoEngage-ra esportatzen.
ms.date: 07/26/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: ffc591c01a5a9434cde41f2da25fa930a515b8c1
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9199171"
---
# <a name="export-segments-to-moengage-preview"></a>Esportatu segmentuak MoEngage-ra (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak MoEngage-ra eta erabili posta elektroniko bidezko marketinerako MoEngage-n.

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

- [MoEngage kontua](https://www.moengage.com/) eta dagozkion administratzailearen kredentzialak.
- MoEngage API gakoa Ezarpenak > API MoEngage-n.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 100.000 bezero-profil MoEngage-ra esportatzeko, eta horrek 15 minutu iraun dezake. MoEngage-ra esporta ditzakezun bezero-profilen kopurua MoEngage-rekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-moengage"></a>Konfiguratu MoEngage-rekin konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **MoEngage** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure [MoEngage Data API ID eta API gakoa](https://developers.moengage.com/hc/articles/4404674776724-Overview#:~:text=Navigate%20to%20Settings%20%3E%20APIs%20%3E%20DATA,ID%20Password%20%2D%20DATA%20API%20KEY).

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** MoEngage-rako konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat MoEngage ataleko. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. Errepikatu urrats berdinak aukerako beste eremuetarako.

1. Hautatu esportatu nahi dituzun segmentuak. MoEngage-n hautatutako segmentuen izen bereko segmentu bat edo gehiago sortuko ditugu **Segmentuak** > **Segmentu pertsonalizatuak**.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
