---
title: Sortu eta kudeatu neurriak
description: Zehaztu zure negozioaren errendimendua aztertzeko eta islatzeko neurriak.
ms.date: 02/02/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: wameng
manager: shellyha
ms.openlocfilehash: 5bcee3b4c51880740715575b18fd7a4dbf87e6d0
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269913"
---
# <a name="define-and-manage-measures"></a>Neurriak zehaztu eta kudeatu

Neurriek bezeroen portaerak eta negozioaren errendimendua hobeto ulertzen lagunduko dizute, balio garrantzitsuak eskuratuta [profil bateratuak](data-unification.md). Adibidez, enpresa batek ikusi nahi du *bezero bakoitzeko guztizko gastua* bezero bakoitzaren erosketa historia ulertzeko. Bestela, neurria *enpresaren guztizko salmentak* negozio osoko diru-sarrera agregatuak ulertzeko.  

Neurriak neurri-sortzailea, datuen kontsulta plataforma bat erabiltzen dute hainbat eragilerekin eta esleitzeko aukera sinpleekin. Datuak iragazteko, taldekatzeko emaitzak, detektatzeko aukera ematen du [entitate harreman bideak](relationships.md), eta irteera aurreikusi.

Erabili neurri-sortzailea negozio-jarduerak planifikatzeko bezeroen datuak kontsultatuz eta estatistikak aterata. Adibidez, neurri bat sortzea *bezero bakoitzeko guztizko gastua* eta *bezeroaren itzulketa osoa* gastu handia baina errentagarritasuna handia duten bezero talde bat identifikatzen laguntzen du. [Segmentu bat sor](segments.md) dezakezu hurrengo ekintza onenak gidatzeko. 

## <a name="create-a-measure"></a>Sortu neurri bat

Atal honek hutsetik neurri berri bat sortzen lagunduko dizu. Neurri bat bezeroaren entitatearekin konektatzeko konfiguratuta dauden datu-entitateetako datu-atributuekin eraiki dezakezu. 

1. Hartzaileei buruzko xehetasunetan, joan hona: **Neurriak**.

1. Hautatu **Berria**.

1. Aukeratu **Editatu izena** eta eman **Izena** neurrian. 
   > [!NOTE]
   > Zure neurri konfigurazio berriak bi eremu besterik ez baditu, adibidez, Bezero IDa eta kalkulu bakarra, irteera zutabe berri gisa gehituko zaio Bezeroaren neurria izeneko sistemak sortutako entitateari. Gainera, neurriaren balioa bezeroaren profil bateratuan ikusi ahal izango duzu. Beste neurri batzuek beren entitateak sortuko dituzte.

1. Konfigurazio eremuan, aukeratu agregazio funtzioa **Aukeratu Funtzioa** goitibeherako menua. Agregazio funtzioek honako hauek dituzte: 
   - **Sum**
   - **Batez bestekoa**
   - **Kontaketa**
   - **Kontaketa bakarra**
   - **Gehienekoa**
   - **Min**
   - **Lehenengoa**: datuen erregistroaren lehen balioa hartzen du
   - **Azkena**: datuen erregistroan gehitu den azken balioa hartzen du

   :::image type="content" source="media/measure-operators.png" alt-text="Neurriak kalkulatzeko operadoreak.":::

1. Aukeratu **Gehitu atributua** neurri hau sortzeko behar dituzun datuak hautatzeko.
   
   1. Hautatu **Atributuak** fitxa. 
   1. Datu-entitatea: aukeratu neurtu nahi duzun atributua biltzen duen entitatea. 
   1. Datuen atributua: aukeratu neurria kalkulatzeko agregazio funtzioan erabili nahi duzun atributua. Aldi berean atributu bat besterik ezin duzu hautatu.
   1. Dagoen neurri batetik datuen atributu bat ere hauta dezakezu **Neurriak** fitxa. Edo entitatearen edo neurketaren izena bila dezakezu. 
   1. Aukeratu **Gehitu** hautatutako atributua neurrira gehitzeko.

   :::image type="content" source="media/measure-attribute-selection.png" alt-text="Aukeratu kalkuluetan erabiltzeko atributu bat.":::

1. Neurri konplexuagoak eraikitzeko, atributu gehiago gehi ditzakezu edo kalkulu-operadoreak erabil ditzakezu neurri funtzioan.

   :::image type="content" source="media/measure-math-operators.png" alt-text="Sortu neurri konplexua kalkulu-eragileekin.":::

1. Iragazkiak gehitzeko, hautatu **Iragazi** konfigurazio-eremuan. 
  
   1. **Gehitu atributua** ataleko **Iragazkiak** panelean, hautatu iragazkiak sortzeko erabili nahi duzun atributua.
   1. Ezarri iragazkien eragileak hautatutako atributu bakoitzaren iragazkia definitzeko.
   1. Aukeratu **Aplikatu** hautatutako atributua neurrira gehitzeko.

1. Dimentsioak gehitzeko, hautatu **Dimentsioa** konfigurazio-eremuan. Dimentsioak irteerako entitateko zutabe gisa agertuko dira.
   1. Aukeratu **Editatu dimentsioak** neurriaren balioak taldekatu nahi dituzun datu atributuak gehitzeko. Adibidez, hiria edo generoa. Lehenespenez, *Bezeroaren IDa* dimentsioa hautatzeko hautatzen da *bezero-mailako neurriak*. Neurri lehenetsia kendu dezakezu sortu nahi baduzu *negozio-mailako neurriak*.
   1. Aukeratu **Eginda** hautatutako atributua neurrira gehitzeko.

1. Esleitutako datu-entitatearen eta Bezero-entitatearen artean bide anitz badaude, identifikatutako bat aukeratu behar duzu [entitate erlazio-bideak](relationships.md). Neurriaren emaitzak hautatutako bidearen arabera alda daitezke.
   1. Aukeratu **Datuen hobespenak** eta aukeratu zure neurria identifikatzeko erabili beharreko entitate bidea.
   1. Aukeratu **Eginda** zure hautaketa aplikatzeko. 

   :::image type="content" source="media/measures-data-preferences.png" alt-text="Hautatu neurriaren entitatearen bide-izena.":::

1. Neurriaren kalkulu gehiago gehitzeko, hautatu **Kalkulu berria**. Entitate bide bereko entitateak soilik erabil ditzakezu kalkulu berrietarako. Kalkulu gehiago irteerako entitateko zutabe berri gisa agertuko dira.

1. Aukeratu **...** kalkuluan balioa **Bikoizteko**, **Izena aldatzeko** edo **Kentzeko** neurri batetik.

1. **Aurrebista** eremuan, neurketaren irteerako entitatearen datu-eskema ikusiko duzu, iragazkiak eta neurriak barne. Aurrebistak dinamikoki erreakzionatzen du konfigurazioko aldaketen aurrean.

1. Aukeratu **Exekutatu** konfiguratutako neurriaren emaitzak kalkulatzeko. Aukeratu **Gorde eta itxi** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu.

1. Joan **Neurriak** atalera sortu berri den neurria zerrendan ikusteko.

## <a name="manage-your-measures"></a>Kudeatu neurriak

[Neurri bat sortu](#create-a-measure) ondoren, neurrien zerrenda ikusiko duzu **Neurriak** orrian.

Neurri motari, sortzaileari, sortze datari, egoerari eta egoerari buruzko informazioa aurkituko duzu. Zerrendako neurri bat hautatzen duzunean, irteera aurreikusi eta .CSV fitxategia deskarga dezakezu.

Neurri guztiak aldi berean freskatzeko, hautatu **Freskatu guztiak** neurri zehatz bat aukeratu gabe.

> [!div class="mx-imgBorder"]
> ![Neurri bakarrak kudeatzeko ekintzak](media/measure-actions.png "Neurri bakarrak kudeatzeko ekintzak")

Aukeratu neurri bat zerrendan aukera hauetarako:

- Hautatu neurriaren izena, haren xehetasunak ikusteko.
- **Editatu** neurriaren konfigurazioa.
- **Freskatu** neurria azken datuetan oinarrituta.
- **Aldatu izena** neurria.
- **Ezabatu** neurria.
- **Aktibatu** edo **Desaktibatu**. Neurri inaktiboak ez dira freskatuko [freskatze programatuan](system.md#schedule-tab).

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="next-step"></a>Hurrengo urratsa

Sortzeko dauden neurriak erabiltzen dituzu [bezero segmentu bat](segments.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]