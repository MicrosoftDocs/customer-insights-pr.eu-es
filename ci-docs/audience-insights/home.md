---
title: Etxeko orria hartzaileen xehetasunetan
description: Hasi aplikazioa arakatzen Etxeko orrian.
ms.date: 01/07/2021
ms.reviewer: nimagen
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 7cc767f5d80b213a4c1bb5b2e8062bd44c15279b
ms.sourcegitcommit: 0260ed244b97c2fd0be5e9a084c4c489358e8d4f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/18/2021
ms.locfileid: "5477026"
---
# <a name="create-a-new-environment"></a>Sortu ingurune bat

## <a name="create-a-trial-environment"></a>Sortu probako ingurunea

Epaiketa batean izena eman dezakezu [proba saioa hasteko orria](https://dynamics.microsoft.com/get-started/free-trial/?appname=customerinsights). 

> [!NOTE]
> Probak 30 egunen buruan iraungitzen dira.

1. Aukeratu **Eman izena doako probarako** aukera eta hautatu **Eman izena orain**.

1. Eman zure laneko edo ikastetxeko helbide elektronikoa, esaiguzu zure buruari buruzko informazio gehiago eta hautatu **Hurrengoa**.

   :::image type="content" source="media/trial-signup-dialog.png" alt-text="Probako instantzian izena emateko elkarrizketa-koadroa":::

1. Eman **Izena** zure ingurune berrirako. 

1. Hautatu proba mota.

1. Aukeratu **Eskualdea** zure ingurunerako.

1. Aukeran, Dynamics 365 erakundeko administratzaileentzat: hautatu **Ezarpen aurreratuak** eta eman zure erakundearen URLa iragarpen bezalako funtzioak bezeroaren txanda bezalakoak erabiltzeko.

1. Hautatu **Sortu**. 

Ingurunea sortu ondoren, ikusiko duzu **Demo** aplikazioa fikziozko datuekin esploratzeko aukera ematen duen ingurunea. Laginaren datuak alda ditzakezu zure industriaren arabera. Aukeratu **Ezarpenak** goiburuko ikonoa eta hautatu **Demo ezarpenak**. Gainera, gai bisuala alda dezakezu. 

Zuk [ingurunera aldatu](#switch-environments) erregistratze prozesuan sortu zenuen zure datuekin lan egiteko.

## <a name="create-a-new-production-or-sandbox-environment"></a>Sortu ekoizpen-ingurune edo sandbox ingurunea

Zure ingurunean, hautatu **Inguruneak** hautatzailea aplikazioaren goiburuan eta hautatu **Berria**.

Jarraitu urratsak zuk bezala [sortu proba-ingurunea](#create-a-trial-environment). Berez, datuak Customer Insights kudeatutako datu-biltegian gordetzen dira. Aukera gehigarri bat lortuko duzu hautatzerakoan **Ezarpen aurreratuak** zure datuak zure Azure Data Lake-n gordetzeko. Eman zure kontuaren izena eta kontu gakoa Azure Data Lake-rekin konexioa ezartzeko. 

> [!IMPORTANT]
> Datuak Azure Data Lake Storage-n gordez gero, onartu egingo duzu datuak Azure biltegiratze-konturako egokia den kokaleku geografikora transferitu eta bertan biltegiratuko direla, eta balitekeela Dynamics 365 Customer Insights-en datuak biltegiratzen diren lekua ez den beste kokaleku bat izatea. Informazio gehiago lortzeko, irakurri. [Argibide gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)

## <a name="explore-the-home-page"></a>Esploratu Orri nagusia

[Atzitu ikusleei buruzko informazioa Dynamics 365 Customer Insights-etik](https://home.ci.ai.dynamics.com/) URL honetan: [https://home.ci.ai.dynamics.com/](https://home.ci.ai.dynamics.com/).
**Etxea** orriak segmentuen, neurrien eta aberasteko datuen ikuspegi orokorra erakusten du (konfiguratuta badago) [mapa](map-entities.md), [bat-etortzea](match-entities.md) eta [konbinatu](merge-entities.md) faseak.

> [!div class="mx-imgBorder"] 
> ![Insights hasierako orrian](media/home-page-insights.png "Insights hasierako orrian")

Azpian **Azken segmentuak**, definitu dituzun atributu demografikoetan, portaeran edo transakzioetan oinarritutako bezero taldeak ikusten dituzu. [Segmentuak sortzea](segments.md) zure bezero-taldea taldekatzen eta zure negozio-jarduerak hobeto bideratzen laguntzen dizu.

**Azken neurriak** erakutsi fitxak honekin [errendimendu-adierazleak (KPI)](measures.md) zuk definitu duzula. Adibidez, bezero baten batez besteko probabilitatea edo bezero bakoitzeko batez besteko lineako gastua.

**Azken aberastasunak** atalean duela gutxi burutu diren aberastze lasterketen emaitzak zerrendatzen dira. [Aberasteek](enrichment-hub.md) zure bezero-baseari buruzko informazioa gehitzen dute. Adibidez, haienganako interesak eta markak ulertuz.

## <a name="switch-environments"></a>Aldatu inguruneak

Hautatu botoia **Ingurumena** kontrol orria orriaren goiko eskuinaldean inguruneak aldatzeko.

> [!div class="mx-imgBorder"] 
> ![Aldatu ingurunea](media/home-page-environment-switcher.png "Aldatu ingurunea")

Administratzaileek sortu eta kudeatu dezakete [ingurune anitz](manage-environments.md). Ingurune bat baino gehiago mantentzea erabilgarria izan daiteke, adibidez, zure erakundeak nazioartean funtzionatzen badu eta datuak eta ikuspegi desberdinak modu desberdinetan bereizi behar badituzu.

## <a name="next-step"></a>Hurrengo urratsa

Hasierako orrialdeak zure ikuspegi propioak ikusteko, lehenengo egin behar duzu [gehitu datu iturriak](data-sources.md) eta [bateratzeko](data-unification.md) zure datuak bezeroen profilak eraikitzeko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]