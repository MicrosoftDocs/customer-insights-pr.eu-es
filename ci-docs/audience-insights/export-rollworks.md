---
title: Esportatu Customer Insights datuak RollWorks-era
description: Ikasi konexioa konfiguratzen eta esportatzen RollWorks.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 4979f0147dea2270f11342c1bb6b0693f3c24aea
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760463"
---
# <a name="export-segment-lists-to-rollworks-preview"></a>Esportatu segmentuen zerrendak RollWorks (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak RollWorks eta erabili iragarkietarako. 

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [RollWorks kontua](https://www.rollworks.com/) eta dagozkien administratzaile egiaztagiriak.
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio bakoitzeko 250.000 profil esportatu ditzakezu RollWorks-era.
- Ezin dituzu 100 profil baino gutxiagoko segmentuak esportatu RollWorks-era. 
- RollWorks esportatzea segmentuetara mugatzen da.
- Esportatu gehienez 250.000 profil RollWorks, 10 minutu behar ditzake osatzeko. 
- RollWorks-era esporta ditzakezun profilen kopurua RollWorks-rekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="set-up-connection-to-rollworks"></a>Konfiguratu konexioa RollWorks-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **RollWorks** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** RollWorks konexioa hasieratzeko.

1. Aukeratu **Autenticatu RollWorks-ekin** eta eman zure administratzaile egiaztagiriak RollWorks-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa RollWorks sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Sartu zure **RollWorks iragarlearen IDa** [RollWorks Iragarkia](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).

3. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. Segmentuak esportatu behar dira RollWorks.

1. Hautatu esportatu nahi dituzun segmentuak. Aukeratu gutxienez 100 kide dituen segmentua. Ezin dituzu segmentu txikiagoak esportatu. Gainera, esportatzeko segmentu baten gehieneko tamaina 250.000 kide da esportazio bakoitzeko. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak RollWorks-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara RollWorks-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
