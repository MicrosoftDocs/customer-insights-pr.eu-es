---
title: Esportatu Customer Insights datuak LinkedIn Ads-era
description: Ikasi konexioa konfiguratzen eta LinkedIn Ads-era esportatzen.
ms.date: 05/12/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 2cfaa37fd0ac697f29665792bab27a925d8ea1eede0519d424524a7e5accbfeb
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7034208"
---
# <a name="export-segments-to-linkedin-ads-preview"></a>Esportatu segmentuak LinkedIn Ads-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak LinkedIn Ads-era bat datozen hartzaileak sortzeko. Erabili bat datozen hartzaileak enpresaren bideratzerako eta kontaktuen bideratzerako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Badituzu [LinkedIn Campaign Manager kontua](https://business.linkedin.com/marketing-solutions/ads) eta dagozkien administratzaile egiaztagiriak.
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profilek helbide elektronikoa duen eremu bat dute.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio bakoitzeko 100.000 profil esportatu ditzakezu LinkedIn Ads-era.
- LinkedIn Ads-era esportatzea segmentuetara mugatzen da.
- Esportatu gehienez 100.000 profil LinkedIn Ads-era, 10 minutu behar ditzake osatzeko. 

## <a name="set-up-the-connection-to-linkedin-ads"></a>Konfiguratu konexioa LinkedIn Ads-era

1. Ikusleen ikuspegietan, joan hona **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **LinkedIn Ads** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman zure [LinkedIn Campaign Manager Kontuaren IDa](https://www.linkedin.com/help/lms/answer/a424270).

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** Campaign Monitor konexioa hasieratzeko.

1. Aukeratu **Autentifikatu LinkedIn-ekin** eta eman zure administratzaile egiaztagiriak LinkedIn Campaign Manager-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio bat konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa LinkedIn Ads sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Aukeratu egin nahi dituzun datuak esportatu nahi dituzun ala ez [kontaktuen bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/contact-targeting) edo [enpresen bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/account-targeting) egiteko LinkedIn-en. 

1. **Datuen bat etortzea** atalean, hautatu bezeroaren profil bateratuko bezero baten helbide elektronikoa adierazten duen eremua. Segmentuak esportatu behar dira LinkedIn Ads-era.

1. Hautatu esportatu nahi dituzun segmentuak. LinkedIn Campaign Manager-eko bat datozen hartzaileak automatikoki sortuko dira esportatzeko hautatu dituzun segmentuen izenarekin. Segmentu bakoitzak bat datorren hartzaile bereizi bat sortuko du. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak LinkedIn Ads-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara LinkedIn Ads-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, esportazioaren helburuko kokaleku hori ken dezake Dynamics 365 Customer Insights administratzaileak.
