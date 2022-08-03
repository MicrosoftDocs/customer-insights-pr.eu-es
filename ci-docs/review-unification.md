---
title: Berrikusi datuen bateratzea
description: Berrikusi datuak bateratzeko urratsak, sortu bezeroen profil bateratuak eta berrikusi emaitzak
ms.date: 06/02/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: adkuppa
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-match
- ci-merge
- ci-relationships
- customerInsights
ms.openlocfilehash: 20728ffaef9bb705410b3ac22d19868ffd5d1243
ms.sourcegitcommit: 3c5b0b40b2b45e420015bbdd228ce0e610245e6f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/12/2022
ms.locfileid: "9139555"
---
# <a name="review-data-unification"></a>Berrikusi datuen bateratzea

Bateratze-prozesuko azken urrats honek prozesuaren urratsen laburpena erakusten du eta profil bateratua sortu aurretik aldaketak egiteko aukera ematen du.

:::image type="content" source="media/m3_review.png" alt-text="Bezeroen profilak berrikusi eta sortu pantaila-argazkia.":::

## <a name="review-the-data-unification-steps"></a>Berrikusi datuak bateratzeko urratsak

1. Hautatu **Editatu** datuak bateratzeko edozein urratsetan aldaketak berrikusteko eta egiteko.

1. Zure hautapenekin pozik bazaude, hautatu **Sortu bezeroen profilak**. The **Bateratu** orria bistaratzen da bezeroaren profil bateratua sortzen ari den bitartean. Fitxa guztiak izan ezik **Iturburu-eremuak** erakutsi **Ilaran jarrita** edo **Freskagarria** egoera.

   :::image type="content" source="media/m3_unify_refreshing.png" alt-text="Unify orriaren pantaila-argazkia Ilaran edo Freskatzen erakusten duten lauzekin.":::

   [!INCLUDE [progress-details-pane-include](includes/progress-details-pane.md)]

Bateratze algoritmoak denbora pixka bat behar du osatzeko eta ezin duzu konfigurazioa aldatu amaitu arte. Bateratze-prozesua amaitzen denean, bezeroen profil bateratuaren entitateak deitu du *Bezeroa*, atalean ageri da **Entitateak** orrialdean **Profilak** atala. Lehenengo bateratze-exekutatu arrakastatsuak bateratua sortzen du *Bezeroa* entitate. Ondorengo exekuzio guztiek entitate hori zabaltzen dute.

## <a name="review-the-results-of-data-unification"></a>Berrikusi datuak bateratzearen emaitzak

Bateratzearen ondoren, **Datuak** > **Bateratu** orrialdeak bezeroen profil bateratuen kopurua erakusten du. Batasun-prozesuko urrats bakoitzaren emaitzak fitxa bakoitzean bistaratzen dira. Adibidez, **Iturburu-eremuak** mapatutako atributu kopurua (eremuak) erakusten du eta **Erregistro bikoiztuak** aurkitutako erregistro bikoiztuen kopurua erakusten du.

:::image type="content" source="media/m3_unified.png" alt-text="Datuak bateratu ondoren datuak bateratu orriaren pantaila-argazkia.":::

> [!TIP]
> The **Bat datozen baldintzak** lauza entitate bat baino gehiago hautatuta badago soilik bistaratzen da.

Emaitzak berrikustea gomendatzen dizugu, batez ere zure kalitatea [partida arauak](data-unification-update.md#manage-match-rules) eta hobetu behar izanez gero.

Beharrezkoa denean, [egin aldaketak bateratze-ezarpenetan](data-unification-update.md) eta berriro exekutatu profil bateratua.

## <a name="next-step"></a>Hurrengo urratsa

Konfiguratu [jarduerak](activities.md),[aberastea](enrichment-hub.md),[harremanak](relationships.md), edo [neurriak](measures.md) zure bezeroei buruzko informazio gehiago lortzeko.

[!INCLUDE[footer-include](includes/footer-banner.md)]
