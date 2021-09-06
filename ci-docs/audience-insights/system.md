---
title: Sistemaren konfigurazioa hartzaileen xehetasunetan
description: Lortu informazio gehiago sistemaren ezarpenei buruz Dynamics 365 Customer Insights-en hartzaileen xehetasunen gaitasunean.
ms.date: 02/12/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 2af8728009b4f1d53ebc2557bab8c79537a0dc5dda54477493ab1ad16f3f9a8a
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7035874"
---
# <a name="system-configuration"></a>Sistemaren konfigurazioa

**Sistema** orriak fitxa hauek ditu:
- [Fasea](#status-tab)
- [Antolaketa](#schedule-tab)
- [API erabilera](#api-usage-tab)
- [Honi buruz](#about-tab)
- [Orokorrak](#general-tab)

> [!div class="mx-imgBorder"]
> ![Sistemaren orria.](media/system-tabs.png "Sistemaren orria")

## <a name="status-tab"></a>Egoera fitxa

**Egoeraren fitxa** datuen horniketa, datuen esportazioaren eta produktu garrantzitsuen beste hainbat prozesuren jarraipena egiteko aukera ematen dizu. Berrikusi fitxa honetako informazioa prozesu aktiboen osotasuna ziurtatzeko.

Fitxa honek hainbat prozesurako egoera eta prozesatzeko informazioa duten taulak biltzen ditu. Taula bakoitzak jarraipena egiten du **izena** zeregina eta dagokion entitatea da **Egoera** bere korrika berriena eta noiz izan zen **Azken eguneraketa**.

Ikusi xehetasunak zereginaren azken hainbat exekutatzea bere izena hautatuz.

### <a name="status-types"></a>Egoera motak

Zereginen sei egoera mota daude. Hurrengo egoera motak ere erakusten dira *Bat egin*, *Konbinatu*, *Datu iturriak*, *segmentu*, *Neurriak*, *aberastea*, *jarduerak*, eta *iragarpenak* orriak:

- **Izapidea:** Ataza martxan dago. Egoera alda daiteke arrakasta edo porrota.
- **Arrakastatsua:** Ataza ondo burutu da.
- **Saltatutakoak:** Ataza saltatu egin zen. Zeregin hau kontrolatzen duen downstream-eko prozesu bat edo gehiago huts egin edo saihestu egiten dira.
- **Porrota:** Zereginaren prozesatzeak huts egin du.
- **Bertan behera:** Erabiltzaileak prozesua bertan behera utzi zuen amaitu aurretik.
- **Ilaran:** prozesua ilaran dago eta goranzko zeregin guztiak amaitutakoan hasiko da. Informazio gehiago lortzeko, irakurri [Freskatu politikak](#refresh-policies).

### <a name="refresh-policies"></a>Eguneratu politikak

Zerrenda honek prozesu nagusietako freskatze-gidalerroak erakusten ditu:

- **Datu iturriak:** - (r) en arabera [konfiguratutako egutegia](#schedule-tab). Ez dago beste prozesurik. Partida prozesu honen arrakastaren araberakoa da.
- **Bat-etortzea:** - (r) en arabera [konfiguratutako egutegia](#schedule-tab). Partiduen definizioan erabilitako datu-iturrien prozesamenduaren araberakoa da. Konbinatu Partida prozesu honen arrakastaren araberakoa da.
- **Konbinatu:** - (r) en arabera [konfiguratutako egutegia](#schedule-tab). Bat-etortzearen prozesuaren osatzearen araberakoa da. Segmentuak, neurriak, aberastea, bilaketa, jarduerak, iragarpenak eta datuen prestaketa prozesu honen arrakastaren araberakoak dira.
- **segmentuak**: Eskuz exekutatzen da (denbora bakarreko freskapena) eta arabera [konfiguratutako egutegia](#schedule-tab). Mergeren araberakoa da. Ikuspegiak prozesatzearen araberakoak dira.
- **Neurriak**: Eskuz exekutatzen da (denbora bakarreko freskapena) eta arabera [konfiguratutako egutegia](#schedule-tab). Mergeren araberakoa da.
- **Jarduerak**: Eskuz exekutatzen da (denbora bakarreko freskapena) eta arabera [konfiguratutako egutegia](#schedule-tab). Mergeren araberakoa da.
- **Aberastea**: Eskuz exekutatzen da (denbora bakarreko freskapena) eta arabera [konfiguratutako egutegia](#schedule-tab). Mergeren araberakoa da.
- **Bilatu**: Eskuz exekutatzen da (denbora bakarreko freskapena) eta arabera [konfiguratutako egutegia](#schedule-tab). Mergeren araberakoa da.
- **Datuen prestaketa**: - (r) en arabera [konfiguratutako egutegia](#schedule-tab). Mergeren araberakoa da.
- **Xehetasunak**: Eskuz exekutatzen da (denbora bakarreko freskapena) eta arabera [konfiguratutako egutegia](#schedule-tab). Segmentuen araberakoa da.

Aukeratu zeregin baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Goiko freskatze politikek a-ri aurre egin dezaketena ulertzen lagun dezakete **saltatu** edo **Ilaran** Zeregin.

## <a name="schedule-tab"></a>Antolaketa fitxa

Erabili **Antolaketa** fitxa [sartutako datu-iturburuen](data-sources.md) freskatze automatikoak antolatzeko. Freskatze automatikoak zure datuen iturrien eguneratzeak zure bezeroen profil bateratuetan islatzen laguntzen du.

1. Hartzaileen xehetasunetan, joan hona: **Administratzailea** > **Sistema** eta hautatu **Antolaketa** fitxa.

2. Aurreikusitako freskagarriaren egoera lehenetsia da **itzalita**. Programatutako freskariak gaitzeko, aldatu pantailaren goiko aldean txandakatzeko aukera **Aktibatu**.

3. Aukeratu artean **Asterokoa** (lehenetsia) eta **Egunekoa** freskatzen. Astean freskagarriak antolatzeko asmoa baduzu, hautatu freskagarria exekutatu nahi duzun egun bat edo gehiago.

4. Ezarri zure **Ordu eremu** eta ondoren erabili **Ordua** goitibeherako zure freskatze-denbora ezartzeko. Bukatu duzunean, hautatu **Ezarri** aukera. Egun bakarrean hainbat freskatze programatu nahi badituzu, hautatu **Gehitu beste denbora**.

5. Aldaketak aplikatzeko, hautatu **Gorde**.

## <a name="about-tab"></a>Fitxari buruz

**Buruz** fitxan zure erakundearenak daude **Bistaratu izena**, aktiboa **Ingurumenaren IDa**, **Eskualdea**, eta zure **Saioaren IDa**. Laneko ingurune bat baino gehiago baduzu, bakoitzari erraz identifikatzeko bistaratzeko izena eman beharko zenioke.

## <a name="general-tab"></a>Fitxa orokorra

Bi aukera daude **Orokorra** fitxa, **Hizkuntza** eta **Herrialdearen/Eskualdearen formatua**.

Aplikazioak [hainbat hizkuntza onartzen ditu](supported-languages.md). Nahiago duzun hizkuntza aldatzeko, aukeratu a **Hizkuntza** goitibehera.

Data, ordua eta zenbakiak nahiago duzun formateatzea aldatzeko, erabili '... **Herrialdearen/Eskualdearen formatua** goitibeherako menuko. Eremu honen azpian formateatze aurrebista bistaratzen da. Sistemak automatikoki hautapen bat proposatuko du hizkuntza berria aukeratzen duzunean.

Hautatu **Gorde** zure aukerak baieztatzeko.

## <a name="api-usage-tab"></a>APIaren erabilera fitxa

Bilatu denbora errealeko APIaren erabilerari buruzko xehetasunak eta ikusi denbora-tarte jakin batean zein gertaera gertatu diren. Denboraren denbora tartea aukeratzen duzu **Aukeratu denbora markoa** goitibeherako menua. 

**APIaren erabilera** hiru atal ditu: 
- **API deiak**: hautatutako epean APIra egindako deien kopuru agregatua bistaratzen duen taula.

- **Datuen transferentzia**: hautatutako denbora tartean APIaren bidez transferitu diren datu kopurua erakusten duen taula.

-  **Eragiketak**: taula bat erabilgarri dauden API eragiketa bakoitzerako errenkadekin eta eragiketen erabilerari buruzko xehetasunak. Joan nahi duzun eragiketaren izena hauta dezakezu [APIaren erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances).

   Erabiltzen dituzten eragiketak [denbora errealeko datuak hornitzea](real-time-data-ingestion.md) eduki binokular sinboloa duen botoia denbora errealeko APIaren erabilera ikusteko. Aukeratu botoia APIaren denbora errealeko uneko inguruneko erabilerari buruzko xehetasunak dituen alboko panela irekitzeko.   
   Erabili **Taldekatu honen arabera** koadroan **APIaren erabilera denbora errealean** panelean denbora errealeko elkarrekintzak nola aurkeztu behar diren aukeratzeko. Datuak API metodoaren, entitatearen izen kualifikatua (irenstutako entitatea), sortutako (gertaeraren iturria), emaitza (arrakasta edo hutsegitea) edo errore kodeak arabera talka ditzakezu. Datuak historia-taula gisa eta taula gisa eskuragarri daude.


[!INCLUDE[footer-include](../includes/footer-banner.md)]