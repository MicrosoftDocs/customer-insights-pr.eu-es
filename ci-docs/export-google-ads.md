---
title: Esportatu segmentuak Google Ads-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta Google Ads-era esportatzen.
ms.date: 03/31/2022
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: b7f08936d7d90322cb4e62396a2961fe06273b76
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9082988"
---
# <a name="export-segments-to-google-ads-preview"></a>Esportatu segmentuak Google Ads-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Google Ads audientzia-zerrenda batera eta erabili Google Bilaketa, Gmail, iragarkiak YouTube, eta Google Display Network. 


## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [Google Ads kontua](https://ads.google.com/) eta dagozkion administratzaile kredentzialak.
-   Webgunearen baldintzak betetzen dituzu [Bezeroen arteko lotura politika](https://support.google.com/adspolicy/answer/6299717).
-   Webgunearen baldintzak betetzen dituzu [berriro merkaturatzeko zerrenden tamainak](https://support.google.com/google-ads/answer/7558048).
-   [Konfiguratutako segmentuak](segments.md) dituzu.
-   Esportatutako segmentuetako bezero-profil bateratuek helbide elektronikoa, telefonoa, mugikorreko iragarle IDa, hirugarrenen erabiltzaile IDa edo helbidea adierazten duten eremuak dituzte.

## <a name="known-limitations"></a>Muga ezagunak

- Google Ads-era esportatzea segmentuetara mugatuta dago.
- Guztira 1 milioi bezero profil dituzten segmentuak esportatzeak 30 minutu arte iraun dezake hornitzailearen aldetik mugak daudelako. 
- Google Ads zerbitzuan bat etortzeak 48 ordu iraun dezake.

## <a name="set-up-connection-to-google-ads"></a>Konfiguratu konexioa Google Ads-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Google Ads** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Idatzi **[Google Ads bezeroaren IDa](https://support.google.com/google-ads/answer/1704344)**.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Egiaztatu Google Ads-ekin** eta eman zure Google Ads kredentzialak.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko. 

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Google Ads sekzioan. Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.

1. Ikusle berri bat sortu nahi baduzu, utzi Google Audience ID eremua hutsik. Automatikoki publiko berri bat sortuko dugu zure Google Ads kontuan eta esportatutako segmentuaren izena erabiliko dugu. Lehendik dagoen Google Ads-eko audientzia eguneratu nahi baduzu, idatzi zure [Google Ads-en ikusleen IDa](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.)

1. urtean **Datuen parekatzea** atalean, hautatu esportatzeko datu-eremu bat edo gehiago eta hautatu Customer Insights-en dagozkien datu-eremuak adierazten dituen eremua.

1. Hautatu esportatu nahi dituzun segmentuak. 

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). 

Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Google Ads-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Google Ads-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE [footer-include](includes/footer-banner.md)]
