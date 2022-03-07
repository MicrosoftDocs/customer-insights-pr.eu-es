---
title: Erabili audientzia estatistiken segmentuak konpromiso estatistiken txostenak iragazteko
description: Erabili audientzia estatistiken segmentuak bezero baten webgunean konpromiso estatistikek hartutako portaera datuen analisi interaktiboetan.
ms.date: 07/27/2021
ms.topic: conceptual
author: mkisel
ms.author: mkisel
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 9c8c7a1a9216e04ebee100c548afbc745af396ec
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8230471"
---
# <a name="use-audience-insights-segments-to-filter-engagement-insights-reports"></a>Erabili audientzia estatistiken segmentuak konpromiso estatistiken txostenak iragazteko

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Elkarreragin xehetasunekin, erabil ditzakezu audientzia estatistiken segmentuak konpromiso estatistikek hartutako portaera datuen analisi interaktiboetan.

## <a name="prerequisite"></a>Aurrebaldintza

- Segmentuak eta bezeroen profilak sortzen diren audientzia estatistiken ingurunearekin loturiko audientzia estatistikak biltzen dituen konpromisoari buruzko ingurunea. Informazio gehiago: [Sortu esteka bat hartzaile xehetasun eta elkarreragin xehetasunen artean](integrate-audience-insights-engagement-insights.md)

## <a name="create-audience-insights-segments"></a>Sortu ikusleen ikuspegi segmentuak 

> [!IMPORTANT]
> Ikusleen estatistiken segmentuak konpromisoen estatistiketan agertzeko, lehenik eta behin egin behar duzu [exekutatu bateratze eta downstream prozesuak](../audience-insights/merge-entities.md). Downstream prozesuak garrantzitsuak dira, ikusleei buruzko informazio segmentuak prestatzen dituen taula bakarra sortzen dutelako, konpromisoekin partekatzeko. (Sistema freskatzea programatuta badago, automatikoki beheranzko prozesuak sartuko ditu.)

Ikusleen estatistikak segmentuak erabil ditzakezu sortutako kutxaz kanpoko txostenetan edo pertsonalizatutako txostenetan. Informazio gehiagorako, joan hona [Kutxaz kanpoko profilen txostenak](profile-reports.md) eta [Sortu eta editatu txosten pertsonalizatuak](custom-reports.md).

**Erabiltzeko audientzia estatistiken segmentuak konpromiso estatistiken txostenak horretan**

1. Zure **Lan eremua** orrialdea, hautatu **Datuak**, eta, ondoren, hautatu **Segmentuak** fitxa.

    :::image type="content" source="media/integrate-audience-insights-segments1.png" alt-text="Hautatu Segmentuen fitxa":::

   >[!NOTE]
   > Audientzia estatistiken segmentu bat hautatzeak ikusleen estatistiketara eramango zaitu, segmentu hori arau eta logikari dagokionez nola sortu zen jakiteko. Ikusleen estatistiken segmentuei buruzko informazio gehiago lortzeko, joan hona [Ikusi eta sortu segmentuak](../audience-insights/segments.md).

2. Aukeratu kutxaz kanpoko txostena edo [txosten pertsonalizatua sortu](custom-reports.md) eta, ondoren, hautatu **Gehitu baldintza**. (Adibide honetarako, aukeratu dugu **Orrialde ikustaldiak** txostena.)

    :::image type="content" source="media/integrate-audience-insights-segments2.png" alt-text="Gehitu baldintza.":::

3. Aukeratu **Iragazi segmentuaren arabera**, zabaldu **Segmentu mota** eta, ondoren, hautatu **Demografikoa**.

    :::image type="content" source="media/integrate-audience-insights-segments3.png" alt-text="Aukeratu segmentu demografiko mota.":::

4. Zabaldu **Segmentuaren izena** zerrendan eta, ondoren, aukeratu ikusleen ikuspegi segmentua.

    :::image type="content" source="media/integrate-audience-insights-segments4.png" alt-text="Aukeratu segmentu bat.":::

5. Segmentu bat edo gehiago aplika ditzakezu, besteak beste, portaeraren (konpromisoari buruzko estatistikak) eta demografikoen (ikusleen estatistikak) segmentuak barne. 

    :::image type="content" source="media/integrate-audience-insights-segments6.png" alt-text="Orrialde ikustaldiak txostena AEBetako bezeroei eta Orri nagusiko segmentuetara mugatuta dago.":::

Aurreko irudian, **AEBetako bezeroak** eta **Orri nagusia** segmentuak hautatu dira eta horrek mugatzen du **Orrialde ikustaldiak** jakinarazi bi segmentu horiek soilik bistaratzeko. 


>[!NOTE]
> Ikusleen estatistikak segmentuak iragazteko erabil ditzakezu sortutako kutxaz kanpoko txostenetan, pertsonalizatutako txostenetan eta inbutu lana egiten du elkarreragin xehetasunetan. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]