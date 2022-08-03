---
title: Esportatu segmentuak Google Ads-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta Google Ads-era esportatzen.
ms.date: 07/25/2022
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: fd7498ecf17ef8a3a8f22dcc49ae204bef88b47f
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196563"
---
# <a name="export-segments-to-google-ads-preview"></a>Esportatu segmentuak Google Ads-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Google Ads audientzia-zerrenda batera eta erabili Google Bilaketa, Gmail, iragarkiak YouTube, eta Google Display Network.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Google Ads kontua](https://ads.google.com/) eta dagozkion administratzailearen kredentzialak.
- A [Google Ads bezeroaren IDa](https://support.google.com/google-ads/answer/1704344).
- Ren eskakizunak [Bezeroa lotzeko politika](https://support.google.com/adspolicy/answer/6299717) betetzen dira.
- Ren eskakizunak [birmarketing-zerrenden tamainak](https://support.google.com/google-ads/answer/7558048) betetzen dira.
- [Konfiguratutako segmentuak](segments.md).
- Esportatutako segmentuetako bezero-profil bateratuek helbide elektronikoa, telefonoa, mugikorreko iragarlearen IDa, hirugarrenen erabiltzaile IDa edo helbidea adierazten duten eremuak dituzte.

## <a name="known-limitations"></a>Muga ezagunak

- Esportatu Google Ads-era Esportazio bakoitzeko milioi bat bezero-profil, eta hori osatzeko 30 minutu behar izan daitezke hornitzailearen aldetik dauden mugak direla eta.
- Segmentuak soilik.
- Google Ads-en parekatzeak 48 ordu iraun ditzake.

## <a name="set-up-connection-to-google-ads"></a>Konfiguratu konexioa Google Ads-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Google Ads**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure Google Ads bezero ID.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Aukeratu **Egiaztatu Google Ads-ekin** eta eman zure Google Ads kredentzialak.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Google Ads sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Aukeratu lehendik dagoen ikusle bat erabili edo berri bat sortu:
   - Lehendik dagoen Google Ads-eko audientzia eguneratzeko, idatzi zure [Google Ads-en ikusleen IDa](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns).
   - Ikusle berri bat sortzeko, utzi Google Audience ID eremua hutsik. Customer Insights-ek ikusle berri bat sortuko du automatikoki zure Google Ads kontuan eta esportatutako segmentuaren izena erabiliko du.

1. urtean **Datuen parekatzea** atalean, hautatu esportatzeko datu-eremu bat edo gehiago eta hautatu Customer Insights-en dagozkien datu-eremuak adierazten dituen eremua.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
