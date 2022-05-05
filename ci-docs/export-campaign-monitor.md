---
title: Esportatu Customer Insights datuak Campaign Monitor-era
description: Ikasi konexioa konfiguratzen eta esportatzen Campaign Monitor.
ms.date: 10/08/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: b351e491ee830b6360d4efe33d32a726c2e553ba
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642081"
---
# <a name="export-segments-to-campaign-monitor-preview"></a>Esportatu segmentuak Campaign Monitor-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Campaign Monitor-era eta erabili marketin jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [Campaign Monitor kontua](https://www.campaignmonitor.com/) eta dagozkien administratzaile egiaztagiriak.
-   Zuk daukazu [konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio bakoitzeko milioi bat bezero profila esporta ditzakezu Kanpainaren monitorea.
- Campaign Monitor-era esportatzea segmentuetara mugatuta dago.
- Milioi batera arte bezero profil Kanpainaren monitorea dituzten segmentuak esportatzen 20 minutu behar izan ditzakete osatzeko. 
- Kanpainaren monitorea esporta ditzakezun bezeroen profil kopurua Kanpainaren monitorearekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="set-up-connection-to-campaign-monitor"></a>Konfiguratu konexioa Campaign Monitor

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Campaign Monitor** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** Campaign Monitor konexioa hasieratzeko.

1. Aukeratu **Autenticatu Campaign Monitor-ekin** eta eman zure administratzaile egiaztagiriak Campaign Monitor-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Campaign Monitor sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Idatzi [**Campaign Monitor zerrendaren IDa**](https://www.campaignmonitor.com/api/getting-started/#your-list-id).    
   [Sortu API gakoa](https://www.campaignmonitor.com/api/getting-started/) hurrengotik **Kontu ezarpenak** Campaign Monitor-en lehenengo API zerrendaren IDa ikusteko.  

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. Segmentuak esportatu behar dira Campaign Monitor.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak Campaign Monitor-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Campaign Monitor-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
