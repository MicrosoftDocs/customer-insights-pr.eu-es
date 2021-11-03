---
title: Esportatu Customer Insights datuak Facebook iragarki-kudeatzailera
description: Ikasi konexioa konfiguratzen eta esportatzen Facebook Iragarkien kudeatzailea.
ms.date: 04/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: bb74e35799410b92b64e48e065b45efda82490ca
ms.sourcegitcommit: 31985755c7c973fb1eb540c52fd1451731d2bed2
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/22/2021
ms.locfileid: "7672938"
---
# <a name="export-segments-list-to-facebook-ads-manager-preview"></a>Esportatu segmentuen zerrenda Facebook Iragarkien kudeatzailea (aurrebista)

Bezeroen profil bateratuen segmentuak esportatu Facebook Iragarkien kudeatzailea kanpainak sortzeko Facebook eta Instagram.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWO1aN]

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

- [**Facebook iragarkien kontuak**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) dut [**Facebook negozio-kontua**](https://business.facebook.com/).
- Administratzailea izan behar duzu [**Facebook iragarkien kontua**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account).

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 10 milioi bezero profil esportatzeko Facebook Iragarkien kudeatzailea.
- Esportatu Facebook Ads-eko kudeatzailera esportatzea segmentuetara mugatuta dago.
- Sortu edo eguneratu audientzia pertsonalizatuak hemen Facebook motakoa *bezeroen zerrenda* bakarrik.
- Guztira 10 milioi bezero profil dituzten segmentuak esportatzen 90 minutu behar izan ditzakete osatzeko.

## <a name="set-up-connection-to-facebook-ads-manager"></a>Konfiguratu konexioa Facebook iragarkien kudeatzailea

Erabiltzaileek esportazio bat sortu aurretik, administratzaile batek zerbitzurako konexioa konfiguratu behar du eta laguntzaileei konexioa erabiltzeko baimena eman behar die.

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **Facebook Iragarkien kudeatzailea** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Autentifikatu Facebook iragarkiekin: 

   1. Aukeratu **Jarraitu honekin Facebook** zure saioa hasteko Facebook Iragarkien kontua.

   1. Onartu **iragarkien kudeaketa** baimena, Facebook-ekin autentifikatu ondoren.

   1. Hautatu **Facebook iragarki kontua** lan egin nahi duzunarekin.

   1. Aukeratu **Lehendik dagoen publiko pertsonalizatua** goitibeherako zerrendatik edo sortu **Publiko pertsonalizatu berria**. Informazio gehiago lortzeko, ikus [**Ikusleak Facebook Iragarkien kudeatzailea**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).
      > [!NOTE]
      > Ikusle pertsonalizatuak soilik sor ditzakezu edo eguneratu Facebook motakoa *bezeroen zerrenda* esportazio honekin. Zenbait kasutan, goitibeherako zerrendan mota desberdinetako ikusle pertsonalizatuak ikusten dituzu. Ez bezalako mota bat hautatzea *bezeroen zerrenda* esportazioak huts egingo du. 

1. Berrikusi **Datuen pribatutasuna eta betetzea** eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**. 

1. Hurrengoan **Esportaziorako konexioa** Aukeratu konexioa **Facebook Iragarkien kudeatzailea** atala. Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.

1. Sarbidean **Aukeratu zure gako identifikatzaileen eremua** hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** bidali Facebook Iragarkien kudeatzailea. 

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.

1. Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.
   > [!TIP]
   > Aukera onenak hautatuta baldin badaude **Helbide elektronikoa** gako identifikatzaile gisa. Identifikatzaile osagarriak gehitzeak bat egin dezake.

1. Aukeratu **Gehitu atributua** bidali beharreko atributu gehiago mapatzeko Facebook Iragarkien kudeatzailea. Atributuak Facebook Iragarkien kudeatzailea erabiltzaileentzako lagunarteko izen hauek kokatzen dira: **FN** = **izena**, **LN** = **abizena**, **FI** = **Lehen Hasierakoa**, **TELEFONOA** = **Telefonoa**, **GEN** = **Generoa**, **DOB** = **Jaioteguna**, **ST** = **Estatu**, **CT** = **hiria**, **ZIP** = **Posta kodea / zip-kodea**, **HERRIALDEA** = **Herrialdea / Eskualdea**

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). 

Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Facebook-en iragarki-kudeatzailera bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Facebook iragarkiek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
