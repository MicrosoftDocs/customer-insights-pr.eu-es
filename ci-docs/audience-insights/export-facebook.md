---
title: Esportatu Customer Insights datuak Facebook iragarki-kudeatzailera
description: Ikasi konexioa konfiguratzen eta esportatzen Facebook Iragarkien kudeatzailea.
ms.date: 04/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: ca32906a98bc734639fb369d6f5a92e8888fd850
ms.sourcegitcommit: 6d5dd572f75ba4c0303ec77c3b74e4318d52705c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906795"
---
# <a name="export-segments-list-to-facebook-ads-manager-preview"></a>Esportatu segmentuen zerrenda Facebook Iragarkien kudeatzailea (aurrebista)

Bezeroen profil bateratuen segmentuak esportatu Facebook Iragarkien kudeatzailea kanpainak sortzeko Facebook eta Instagram.

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

- Izan behar duzu [**Facebook iragazki-kontua**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) barne hartzen duena [**Facebook negozio-kontua**](https://business.facebook.com/).
- [**Facebook Iragarkien kontuaren**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) administratzaile izan behar duzu.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 10 milioi bezeroren profila esportazio bakoitzeko Facebook Ads kudeatzailea.
- Esportatu Facebook Ads-eko kudeatzailera esportatzea segmentuetara mugatuta dago.
- Sortu edo eguneratu audientzia pertsonalizatuak hemen Facebook motakoa *bezeroen zerrenda* bakarrik.
- Guztira 10 milioi profil dituzten segmentuak esportatzen 90 minutu behar izan daitezke.

## <a name="set-up-connection-to-facebook-ads-manager"></a>Konfiguratu konexioa Facebook iragarkien kudeatzailea

Erabiltzaileek esportazio bat sortu aurretik, administratzaile batek zerbitzurako konexioa konfiguratu behar du eta laguntzaileei konexioa erabiltzeko baimena eman behar die.

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **Facebook Iragarkien kudeatzailea** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da **Administratzaileak**. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Autentifikatu Facebook iragarkiekin: 

   1. Aukeratu **Jarraitu aurrera Facebook** saioa hasteko Facebook Iragarkien kontua.

   1. Onartu **iragarkien kudeaketa** baimena, Facebook-ekin autentifikatu ondoren.

   1. Hautatu **Facebook iragarki kontua** lan egin nahi duzunarekin.

   1. Aukeratu bat **Existitzen den audientzia pertsonalizatua** goitibeherako zerrendatik edo sortu bat **Ohiko audientzia berriak**. Informazio gehiago lortzeko, ikus [**Ikusleak Facebook Iragarkien kudeatzailea**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).
      > [!NOTE]
      > Ikusle pertsonalizatuak soilik sor ditzakezu edo eguneratu Facebook motakoa *bezeroen zerrenda* esportazio honekin. Zenbait kasutan, goitibeherako zerrendan mota desberdinetako ikusle pertsonalizatuak ikusten dituzu. Ez bezalako mota bat hautatzea *bezeroen zerrenda* esportazioak huts egingo du. 

1. Berrikusi **Datuen pribatutasuna eta betetzea** eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**. 

1. Hurrengoan **Esportaziorako konexioa** Aukeratu konexioa **Facebook Iragarkien kudeatzailea** atala. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Sarbidean **Aukeratu zure gako identifikatzaileen eremua** hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** bidali Facebook Iragarkien kudeatzailea. 

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.

1. Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.
   > [AHOLKULUA] Partidua lortzeko aukera onenak hautatuta baldin badaude **Emaila** gako identifikatzaile gisa. Identifikatzaile osagarriak gehitzeak bat egin dezake.

1. Aukeratu **Gehitu atributua** bidali beharreko atributu gehiago mapatzeko Facebook Iragarkien kudeatzailea. Atributuak Facebook Iragarkien kudeatzailea erabiltzaileentzako lagunarteko izen hauek kokatzen dira: **FN** = **izena**, **LN** = **abizena**, **FI** = **Lehen Hasierakoa**, **TELEFONOA** = **Telefonoa**, **GEN** = **Generoa**, **DOB** = **Jaioteguna**, **ST** = **Estatu**, **CT** = **hiria**, **ZIP** = **Posta kodea / zip kodea**, **HERRIALDEA** = **Herrialdea / Eskualdea**

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak  Facebook-en iragarki-kudeatzailera bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Facebook iragarkiek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
