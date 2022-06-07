---
title: Esportatu Customer Insights datuak Criteora
description: Ikasi nola konfiguratu konexioa eta nola esportatu Criteora.
ms.date: 05/27/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 854f5f0c53f053fc5d742d69a045db1926fec00c
ms.sourcegitcommit: bf65bc0a54cdab71680e658e1617bee7b2c2bb68
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808784"
---
# <a name="export-segments-to-criteo-preview"></a>Esportatu segmentuak Criteo-ra (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak kanpainak sortzeko, posta elektronikoko marketina eskaintzeko eta bezero talde zehatzak erabiltzeko Criteorekin.

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

-   Bat daukazu [Criteo Dynamics Retargeting kontua](https://www.criteo.com/login/) eta dagozkion administratzaile-kreditazioak.
-   [Konfiguratutako segmentuak](segments.md) dituzu.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero profil Criteora esportatzeko.
- Criteora esportatzea segmentuetara mugatzen da.
- Guztira 1 milioi bezero profil dituzten segmentuak esportatzeak 30 minutu arte iraun dezake. 
- Criteora esporta ditzakezun bezero-profilen kopurua Criteorekin duzun kontratuaren menpe dago eta mugatuta dago.

## <a name="set-up-connection-to-criteo"></a>Konfiguratu Criteo-rekin konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Kriteo** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Hautatu **ados** berresteko **Datuen pribatutasuna eta betetzea** eta hautatu **Konektatu** Criteo-rako konexioa hasieratzeko.

1. Hautatu **Autentifikatu Criteo-rekin** eta eman zure Administratzaile izena eta kredentzialak Criteorako. 

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Criteo atalean. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri. 

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. 

1. Aukeran, esportatu dezakezu **Iragarle ID** eta **Izena**

1. Hautatu esportatu nahi dituzun segmentuak. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights Criteori datuak transmititzeko, datuak betetze-mugatik kanpo transferitzea onartzen duzu Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina zure ardura zara Criteok izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](includes/footer-banner.md)]
