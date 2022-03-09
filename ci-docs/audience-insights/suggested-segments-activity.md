---
title: Jardueretan oinarritutako iradokitako segmentuak.
description: Utzi Ikaskuntza automatikoek bezeroen jardueran oinarritutako segmentu berri eta interesgarriak aurkitzen laguntzen.
ms.date: 05/11/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
manager: shellyha
searchScope:
- ci-segment-suggestions
- customerInsights
ms.openlocfilehash: 9c10a32b770ea110a1166f20f72116a3a12cb92e
ms.sourcegitcommit: 73cb021760516729e696c9a90731304d92e0e1ef
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/25/2022
ms.locfileid: "8354448"
---
# <a name="suggested-segments-based-on-activity-data-preview"></a>Jardueretan oinarritutako iradokitako segmentuen datuak (aurreargitalpena)

Ezagutu bezeroen segmentu interesgarriak Customer Insights-en kontsumitutako bezeroen jardueren datuetan oinarrituta. Jardueren datuen adibideak transakzioak, laguntza deien iraupena, erosketak edo itzulketak dira. Segmentuak iradokitzeko, jardueren datuak aztertzen dira berritasuna, maiztasuna eta diru balioa (edo iraupena). Bestela, sor dezakezu [iradokitako segmentuak neurri bat hobetzeko edo atributu batek zerk eragiten duen hobeto ulertzeko](suggested-segments.md).

:::image type="content" source="media/suggested-segments-tab.png" alt-text="Iradokitako segmentuen fitxa, jardueran oinarritutako eta atributuetan oinarritutako segmentuen iradokizunak erakusten dituena.":::

## <a name="categorize-customers-by-activity"></a>Sailkatu bezeroak jardueraren arabera

Customer Insights-en eskuragarri dauden [Jardueraren datuekin](activities.md), bezero taldeak ordezkatzen dituzten iradokizunak sor ditzakegu:

- bezero aktibo gehienak 
- erosketa gehien egin dituzten bezeroak 
- diru-sarrera gehien sortu duten bezeroak 
- azkenaldian aktibo egon ez diren bezeroak 
- zure negozioarekin maiz elkarreragiten duten bezeroak  

Txikizkako negozioa baduzu, jakingo zenuke zein bezero sortzen duten diru sarrera gehien eta kupoi batekin saritzen dituzten. Edo noizbehinkako bezeroak identifikatu eta sari programa batean sartzeko eskaintza egin dezakezu zure negozioa maizago bisitatzeko.
Osasun publikoa eskaintzen ari zaren osasun negozioan bazabiltza eta zure helburua gaixo bakoitzarentzako gastuak gutxitzea da. Horretarako modu bat aldizkako bisitak murriztea izan daiteke, ahalik eta bisita gutxienetan arreta onena eskainiz. Kasu honetan, zure helburua da bisitaren maiztasuna baxua izatea eta pazienteen errepikapeneko kostua minimizatzea. Edo maiz hitzorduak eta errepikatzen diren kostu handiak dituzten gaixoen segmentuak identifikatu eta kasu horiek aztertu ditzakezu norbanakoaren tratamendua hobetzeko. 

## <a name="required-data"></a>Beharrezko datuak

Iradokizunak hautatutako sarrerako datuetan oinarrituta sortzen dira. 

- Bezeroen profilak: segmentu zehatz bateko bezero guztiak edo kideak. 

- Denbora-tartea: azken hilabetea, iazkoa edo edozein denbora pertsonalizatua.

- Jarduera mota: erosketak, txikizkako transakzioak, lineako transakzioak, bezeroari arreta emateko kasuak, harpidetzak, eta beste.  

- Jarduera datuak biltzen dituen Customer Insights-eko entitatea: UnifiedActivity entitatea edo jarduera zehatz baterako entitatea. 

- Sartu beharreko neurriak: berritasuna, maiztasuna edo diru dimentsioa, zure negozioaren eskakizunen arabera.

## <a name="generate-suggested-segments"></a>Sortu iradokitako segmentuak

1. Joan hona: **Segmentuak**.

1. Aukeratu **Iradokizunak (aurrebista)** fitxa.

1. Aukeratu **Bilatu iradokizun berriak** eta aukeratu **Ikusi edo aurreikusi bezeroen portaera**. Aukeratu **Hasi** esperientzia gidatua martxan jartzeko.

   :::image type="content" source="media/suggested-segments-activity-wizard.png" alt-text="Jardueran oinarritutako iradokitako segmentu baterako konfigurazio morroiaren lehen urratsa.":::

1. Eman beharrezko sarrerako datuak eta hautatu **Hurrengoa** jarraitu.

   - Aukeratu bezeroak: sartu bezero guztiak edo segmentu zehatz bat.
   - Aukeratu jarduera: hautatu jarduera mota eta jarduera azaltzen duten entitateak.
   - Hobespenak: ezarri kontuan hartu beharreko denbora, iradokizunen faktoreak eta esleitu atributuak.

1. Berrikusi zure sarrera eta hautatu **Exekutatu** eredua martxan jartzeko eta iradokizunak sortzeko.

1. Bezeroen profil kopuruaren eta hautatutako jardueren arabera, minutu batzuk behar izan ditzake burutzeko. 

Iradokizunak sortu ondoren, gehien interesatzen zaizun dimentsioaren edo balioaren arabera iragazi ditzakezu. 

## <a name="view-details-of-a-suggested-segment"></a>Ikusi Iradokitako segmentuaren xehetasunak

Iradokizunak sortu ondoren, hemen zerrendatuta aurkituko dituzu **Segmentuak** > **Iradokizunak (aurrebista)** aukera, **Jardueretan oinarritutako iradokizunak** atalean dagoena.

:::image type="content" source="media/suggested-segments-details.png" alt-text="Iradokitako segmentu baten datu zehatzak erakusten dituen alboko panel zabaldua.":::

Aukeratu **Ikusi iradokizuna** iradokitako segmentu batean segmentu horren xehetasunak ikusteko. Alboko panelak dimentsio bakoitzaren neurria bezalako xehetasunak eskaintzen ditu xede-taldearekin alderatuta. Segmentuko kide potentzialen kopurua eta bezero guztiei dagokien ehunekoa ere nabarmentzen ditu. Iradokizuna segmentu gisa gorde nahi baduzu, hautatu **Sortu segmentua**.    

## <a name="save-a-suggestion-as-a-segment"></a>Gorde segmentu bat iradokizun gisa

1. Joan **Segmentuak** > **Iradokizunak (aurrebista)**.

1. Hautatu gorde nahi duzun segmentua. 

1. Alboko panelean, hautatu **Sortu segmentua**. 

1. Segmentua gorde ondoren, segmentuen zerrendan agertuko da **Segmentu guztiak** fitxa. Orain izan daiteke [freskatu edo ezabatu beste edozein segmentu bezala](segments.md). Ezin dituzu segmentuaren xehetasunak editatu. Hala ere, iradokizunetarako irizpideak aldatu eta iradokizun desberdinak sor ditzakezu.

## <a name="refresh-or-edit-a-set-of-suggestions"></a>Freskatu edo editatu iradokizun multzo bat

1. Joan **Segmentuak** > **Iradokizunak (aurrebista)** eta bilatu segmentua **Jardueretan oinarritutako iradokizunak** atala.

1. Aukeratu **Freskatu iradokizunak** iradokizunak freskatzeko konfiguratutako atributuak mantenduz. Edo hautatu **Editatu iradokizunak** konfiguratutako atributuak aldatzeko. Sistemak prozesua berriro exekutatuko du, segmentu iradokizunak sortuko ditu azken datuetan oinarrituta eta uneko iradokizunak ordezkatuko ditu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
