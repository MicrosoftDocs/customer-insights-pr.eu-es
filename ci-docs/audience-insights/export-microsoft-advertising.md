---
title: Esportatu Customer Insights datuak Microsoft Advertising-era
description: Ikasi konexioa konfiguratzen eta esportatzen Microsoft Advertising-era.
ms.date: 05/12/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 8f8a4cbb9590f9c5311789154319283530e0a10343cccbe9c7aec99765b4fbf2
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7031438"
---
# <a name="export-segments-to-microsoft-advertising-preview"></a>Esportatu segmentuak Microsoft Advertising-era (aurrebista)

Esportatu Customer Insights segmentuak Microsoft Advertising-era Customer Match audientziak sortzeko. Erabili hartzaile hauek iragarkien kanpainetarako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   [Microsoft Advertising kontua](https://ads.microsoft.com/) eta dagozkien administratzaile egiaztagiriak.
-   Customer Match-en erabilera-baldintzak onartu dituzu. 
-   [Konfiguratutako segmentuak](segments.md) hartzaileen xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa duen eremu bat dute.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio bakoitzeko 500.000 bat profil esportatu ditzakezu Microsoft Advertising-era.
- Microsoft Advertising-era esportatzea segmentuetara mugatzen da.
- Gehienez 500.000 profil Microsoft Advertising-era esportatzeak 10 minutu behar ditzake osatzeko. 


## <a name="set-up-the-connection-to-microsoft-advertising"></a>Konfiguratu Microsoft Advertising-erako konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Microsoft Advertising** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Lehenetsia administratzaileak dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** Microsoft Advertising-erako konexioa hasieratzeko.

1. Aukeratu **Autenticatu CMicrosoft Advertising-ekin** eta eman zure administratzaile egiaztagiriak Microsoft Advertising-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Microsoft Advertising sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Hautatu esportatzeko segmentuak. Microsoft Advertising-eko Customer Match audientziak automatikoki sortzen dira esportatzeko hautatutako segmentuen izenarekin. Segmentu bakoitzak Customer Match audientzia bereizi bat sortuko du. 

1. Sartu **Microsoft Advertising Bezeroaren IDa eta Kontuaren IDa**. Bezeroaren IDa (`cid`) eta Kontuaren IDa (`aid`) URLaren parametroetan aurki ditzakezu Microsoft Advertising-en saioa hasten duzunean.

1. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu bezeroaren profil bateratuko eremua bezero baten helbide elektronikoarekin. Segmentuak esportatu behar dira Microsoft Advertising-era.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak Microsoft Advertising-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Microsoft Advertising-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, esportazioaren helburuko kokaleku hori ken dezake Dynamics 365 Customer Insights administratzaileak.
