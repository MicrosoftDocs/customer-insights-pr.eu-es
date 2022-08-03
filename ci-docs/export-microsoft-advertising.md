---
title: Esportatu segmentuak Microsoft Advertising-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Microsoft Advertising-era.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 44217e7823ffbe14d232b3e33de1b4ea6ed69dcf
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196517"
---
# <a name="export-segments-to-microsoft-advertising-preview"></a>Esportatu segmentuak Microsoft Advertising-era (aurrebista)

Esportatu Customer Insights segmentuak Microsoft Advertising-era Customer Match audientziak sortzeko. Erabili hartzaile hauek iragarkien kanpainetarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Microsoft Advertising kontua](https://ads.microsoft.com/) eta dagozkion administratzailearen kredentzialak.
- Microsoft Advertising bezeroaren IDa eta kontuaren IDa. Aurkitu Bezero IDa (`cid`) eta kontuaren IDa (`aid`) URLaren parametroetan Microsoft Advertising-en saioa hasten zarenean.
- Customer Match erabilera-baldintzak onartzen dira.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 500.000 bezero-profil Microsoft Advertising-era esportatzeko, eta horrek 10 minutu iraun dezake.
- Segmentuak soilik.

## <a name="set-up-connection-to-microsoft-advertising"></a>Konfiguratu Microsoft Advertising-ekin konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Microsoft Publizitatea**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Lehenetsia administratzaileak dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Microsoft Advertising bezeroaren IDa**.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Autenticatu CMicrosoft Advertising-ekin** eta eman zure administratzaile egiaztagiriak Microsoft Advertising-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Microsoft Advertising sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Hautatu esportatzeko segmentuak. Microsoft Advertising-eko Customer Match audientziak automatikoki sortzen dira esportatzeko hautatutako segmentuen izenarekin. Segmentu bakoitzak Customer Match audientzia bereizi bat sortuko du.

1. Sartu **Microsoft Advertising Bezeroaren IDa eta Kontuaren IDa**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
