---
title: Iradokitako segmentuak jardueraren arabera (aurrebista)
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
ms.openlocfilehash: df4f5f4b5c9a3ad66d57a6b349e18a0d714aff62
ms.sourcegitcommit: 8a28e9458b857adf8e90e25e43b9bc422ebbb2cd
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/18/2022
ms.locfileid: "9170574"
---
# <a name="suggested-segments-based-on-activity-preview"></a>Iradokitako segmentuak jardueraren arabera (aurrebista)

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
Osasun publikoa ematen baduzu eta zure helburua paziente indibidualentzako gastuak murriztea bada, saia zaitezke behin eta berriz bisitak murrizten, ahalik eta arreta onena eskainiz ahalik eta bisita gutxienetan. Kasu honetan, zure helburua da bisitaren maiztasuna baxua izatea eta pazienteen errepikapeneko kostua minimizatzea. Edo maiz hitzorduak eta errepikatzen diren kostu handiak dituzten gaixoen segmentuak identifikatu eta kasu horiek aztertu ditzakezu norbanakoaren tratamendua hobetzeko.

## <a name="required-data"></a>Beharrezko datuak

Iradokizunak hautatutako sarrerako datuetan oinarrituta sortzen dira.

- Bezeroen profilak: segmentu zehatz bateko bezero guztiak edo kideak.

- Denbora-tartea: azken hilabetea, iazkoa edo edozein denbora pertsonalizatua.

- Jarduera mota: erosketak, txikizkako transakzioak, lineako transakzioak, bezeroari arreta emateko kasuak, harpidetzak, eta beste.  

- Jarduera datuak biltzen dituen Customer Insights-eko entitatea: UnifiedActivity entitatea edo jarduera zehatz baterako entitatea.

- Sartu beharreko neurriak: berritasuna, maiztasuna edo diru dimentsioa, zure negozioaren eskakizunen arabera.

## <a name="generate-suggested-segments"></a>Sortu iradokitako segmentuak

1. Joan **Segmentuak** eta hautatu **Iradokizunak (aurrebista)** fitxa.

1. Aukeratu **Bilatu iradokizun berriak** eta aukeratu **Ikusi edo aurreikusi bezeroen portaera**. Hautatu **Hasi**.

   :::image type="content" source="media/suggested-segments-activity-wizard.png" alt-text="Jardueran oinarritutako iradokitako segmentu baterako konfigurazio morroiaren lehen urratsa.":::

1. Eman beharrezko sarrera-datuak eta hautatu **Hurrengoa**.

   - Aukeratu bezeroak: sartu bezero guztiak edo segmentu zehatz bat.
   - Aukeratu jarduera: hautatu jarduera mota eta jarduera azaltzen duten entitateak.
   - Hobespenak: ezarri kontuan hartu beharreko denbora, iradokizunen faktoreak eta esleitu atributuak.

1. Berrikusi zure sarrera eta hautatu **Exekutatu** eredua martxan jartzeko eta iradokizunak sortzeko.

Bezeroen profil kopuruaren eta hautatutako jardueren arabera, minutu batzuk behar izan ditzake burutzeko.

Iradokizunak sortu ondoren, gehien interesatzen zaizun dimentsioaren edo balioaren arabera iragazi ditzakezu.

## <a name="manage-suggested-segments"></a>Kudeatu iradokitako segmentuak

Joan **Segmentuak** eta hautatu **Iradokizunak (aurrebista)** fitxa. urtean **Jardueran oinarritutako iradokizunak** atalean, hautatu iradokitako segmentu bat erabilgarri dauden ekintzak ikusteko.

- **Ikusi iradokizuna** segmentu horren xehetasunak ikusteko dimentsio bakoitzaren hedadura, xede-taldearekin alderatuta. Segmentuko kide potentzialen kopurua eta bezero guztiei dagokien ehunekoa ere nabarmentzen ditu.
- **Sortu segmentua** iradokitakoa segmentu gisa gordetzeko. Bertan bistaratzen da **Segmentu guztiak** fitxa eta izan daiteke [freskatu edo ezabatu](segments.md). Ezin dituzu segmentuaren xehetasunak editatu. Hala ere, iradokizunetarako irizpideak aldatu eta iradokizun desberdinak sor ditzakezu.
- **Editatu iradokizunak** uneko iradokizunak ordezkatuko dituzten konfiguratutako atributuak aldatzeko.
- **Freskatu iradokizunak** iradokizunak freskatzeko, konfiguratutako atributuak mantenduz.

[!INCLUDE [footer-include](includes/footer-banner.md)]
