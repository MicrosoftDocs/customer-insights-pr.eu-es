---
title: Esportatu Customer Insights datuak AdRoll-era
description: Ikasi AdRoll-erako konexioa nola konfiguratu.
ms.date: 02/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 6fedd549c2e7de362f36e3fb23d363200bb92a04
ms.sourcegitcommit: d24e52150fe5a4fab45128e12d6a03637771d9b9
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "5697059"
---
# <a name="connector-for-adroll-preview"></a>AdRoll-eko konektorea (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak AdRoll-era eta erabili iragarkietarako. 

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [AdRoll kontua](https://www.adroll.com/) eta dagozkion administratzaile kredentzialak.
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="connect-to-adroll"></a>Konektatu AdRoll-era

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. **AdRoll** atalean hautatu **Konfiguratu**.

1. Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.

   :::image type="content" source="media/AdRoll_config.PNG" alt-text="AdRoll konexioaren konfigurazio panela.":::

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** AdRoll-eko konexioa hasieratzeko.

1. Aukeratu **Egiaztatu AdRoll-ekin** eta eman zure administraziorako AdRoll kredentzialak. 

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Sartu zure **AdRoll iragarlearen IDa** [AdRoll iragarkia](https://help.adroll.com/hc/en-us/articles/212011838-Advertiser-Profiles).

1. Aukeratu **hurrengoa** esportazioa konfiguratzeko.

## <a name="configure-the-connector"></a>Konfiguratu konektorea

1. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. Segmentuak AdRoll-era esportatu behar dira.

1. Hautatu esportatu nahi dituzun segmentuak. Aukeratu gutxienez 100 kide dituen segmentua. Ezin dituzu segmentu txikiagoak esportatu. Gainera, esportatzeko segmentu baten gehieneko tamaina 250.000 kide da esportazio bakoitzeko. 

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).

## <a name="known-limitations"></a>Muga ezagunak

- Guztira 250.000 bezero-profil esporta ditzakezu AdRoll-era esportatzeko.
- Ezin dituzu esportatu 100 profil baino gutxiagoko segmentuak AdRoll-era. 
- AdRoll-era esportatzea segmentuetara mugatuta dago.
- 250.000 profila AdRoll-era esportatzeko 10 minutu behar izan ditzakezu osatzeko. 
- AdRoll-era esporta ditzakezun profilen kopurua AdRoll-rekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak AdRoll-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da AdRoll-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
