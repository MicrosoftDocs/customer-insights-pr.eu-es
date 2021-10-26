---
title: Esportatu Customer Insights datuak Google Ads-era
description: Ikasi konexioa konfiguratzen eta Google Ads-era esportatzen.
ms.date: 09/27/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: ce9579f3d31207e666665237fd8935bb86889f8d
ms.sourcegitcommit: 23c8973a726b15050e368cc6e0aab78b266a89f6
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/08/2021
ms.locfileid: "7617903"
---
# <a name="export-segments-to-google-ads-preview"></a>Esportatu segmentuak Google Ads-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Google Ads audientzia-zerrenda batera eta erabili Google Bilaketa, Gmail, iragarkiak YouTube, eta Google Display Network. 

> [!IMPORTANT]
> Une honetan, konexio berri bat sor dezakezu eta datuak Google Ads-era esporta ditzakezu dagoeneko onartutako Google Ads garatzaile token bat baduzu. Politika aldaketak direla eta, Google Ads esportazioa laster eguneratu eta garatzaile tokenik behar ez duen esportazio aukera emango dugu zure esperientziaren jarraipena ziurtatzeko eta Google Ads-era esportazioa errazteko. Google Ads-ekin konexio gehiago ez konfiguratzea gomendatzen dugu esportazio aukera berrira errazago aldatzeko.

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [Google Ads kontua](https://ads.google.com/) eta dagozkion administratzaile kredentzialak.
-   Baduzu [Google Ads garatzaileen token homologatua](https://developers.google.com/google-ads/api/docs/first-call/dev-token). 
-   Webgunearen baldintzak betetzen dituzu [Bezeroen arteko lotura politika](https://support.google.com/adspolicy/answer/6299717).
-   Webgunearen baldintzak betetzen dituzu [berriro merkaturatzeko zerrenden tamainak](https://support.google.com/google-ads/answer/7558048).
-   Google Ads-en hartzaileak eta dagozkien IDak daude. Informazio gehiagorako, ikus [Google Ads-eko hartzaileak](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.).
-   [Konfiguratutako segmentuak](segments.md) dituzu.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa, izena eta abizena adierazten duen eremuak dituzte.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero-profil Google Ads-era esportatzeko.
- Google Ads-era esportatzea segmentuetara mugatuta dago.
- Guztira 1 milioi bezero profil dituzten segmentuak esportatzeak 5 minutu arte iraun dezake hornitzailearen aldetik mugak daudelako. 
- Google Ads zerbitzuan bat etortzeak 48 ordu iraun dezake.

## <a name="set-up-connection-to-google-ads"></a>Konfiguratu konexioa Google Ads-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Google Ads** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Idatzi **[Google Ads bezeroaren IDa](https://support.google.com/google-ads/answer/1704344)**.

1. Sartu **[Google Ads-ek onartutako garatzaile token-a](https://developers.google.com/google-ads/api/docs/first-call/dev-token)**.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Egiaztatu Google Ads-ekin** eta eman zure Google Ads kredentzialak.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko. 

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Google Ads sekzioan. Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.

1. Sartu zure **[Google Ads hartzaileen IDa](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.)** eta hautatu **Konektatu** Google Ads-eko konexioa hasieratzeko.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Hautatu esportatu nahi dituzun segmentuak. Guztira 1 milioi bezero profil esporta ditzakezu Google Ads-era.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). 

Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Google Ads-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Google Ads-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
