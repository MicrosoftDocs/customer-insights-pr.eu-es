---
title: Esportatu Customer Insights datuak Facebook iragarki-kudeatzailera
description: Ikusi nola konfiguratu konexioa Facebook Iragarkien kudeatzailea.
ms.date: 06/05/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 3e2b52fe743563e4bf61d870cbf1718e6c752a67
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596656"
---
# <a name="connector-for-facebook-ads-manager-preview"></a>Konektatzailea Facebook Iragarkien kudeatzailea (aurrebista)

Bezeroen profil bateratuen segmentuak esportatu Facebook Iragarkien kudeatzailea kanpainak sortzeko Facebook eta Instagram.

## <a name="prerequisites"></a>Aurrebaldintzak

- [**Facebook Iragarkien kontua**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) eduki behar duzu, zeinak [**Facebook negozio-kontu**](https://business.facebook.com/) bat barne hartzen duen.
- [**Facebook Iragarkien kontuaren**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) administratzaile izan behar duzu.

## <a name="connect-to-facebook-ads-manager"></a>Konektatu Facebook Iragarkien kudeatzailea

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. Azpian **Facebook Iragarkien kudeatzailea** hautatu **Konfiguratu**.

1. Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.

1. Aukeratu **Jarraitu aurrera Facebook** saioa hasteko Facebook Iragarkien kontua.

1. Onartu **iragarkien kudeaketa** baimena, Facebook-ekin autentifikatu ondoren.

1. Hautatu **Facebook iragarki kontua** lan egin nahi duzunarekin.

1. Aukeratu bat **Existitzen den audientzia pertsonalizatua** goitibeherako zerrendatik edo sortu bat **Ohiko audientzia berriak**. Informazio gehiago lortzeko, ikus [**Ikusleak Facebook Iragarkien kudeatzailea**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **hurrengoa** esportazioa konfiguratzeko.

## <a name="configure-the-connector"></a>Konfiguratu konektorea

1. Sarbidean **Aukeratu zure gako identifikatzaileen eremua** hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** bidali Facebook Iragarkien kudeatzailea.

1. Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.
   > [AHOLKULUA] Partidua lortzeko aukera onenak hautatuta baldin badaude **Emaila** gako identifikatzaile gisa. Identifikatzaile osagarriak gehitzeak bat egin dezake.

1. Aukeratu **Gehitu atributua** bidali beharreko atributu osagarriak mapatzeko Facebook Iragarkien kudeatzailea. Atributuak Facebook Iragarkien kudeatzailea erabiltzaileentzako lagunarteko izen hauek kokatzen dira: **FN** = **izena**, **LN** = **abizena**, **FI** = **Lehen Hasierakoa**, **TELEFONOA** = **Telefonoa**, **GEN** = **Generoa**, **DOB** = **Jaioteguna**, **ST** = **Estatu**, **CT** = **hiria**, **ZIP** = **Posta kodea / zip kodea**, **HERRIALDEA** = **Herrialdea / Eskualdea**

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 10 milioi bezeroren profila esportazio bakoitzeko Facebook Ads kudeatzailea 
- Esportatu Facebook Ads-eko kudeatzailera esportatzea segmentuetara mugatuta dago
- Guztira 10 milioi profil dituzten segmentuak esportatzen 90 minutu behar izan daitezke

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak  Facebook-en iragarki-kudeatzailera bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Facebook iragarkiek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]