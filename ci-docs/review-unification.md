---
title: Berrikusi datuen bateratzea
description: Berrikusi datuak bateratzeko urratsak, sortu bezeroen profil bateratuak eta berrikusi emaitzak
ms.date: 05/04/2022
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
ms.openlocfilehash: 4c709dfb55bf079dd2fe99e41adb4c77c2bece4b
ms.sourcegitcommit: 6a5f4312a2bb808c40830863f26620daf65b921d
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8742925"
---
# <a name="review-data-unification"></a>Berrikusi datuen bateratzea

[!INCLUDE [m3-prod-trial-note](includes/m3-prod-trial-note.md)]

Bateratze-prozesuaren azken urrats honek prozesuaren urratsen laburpena erakusten du eta profil bateratua sortu aurretik aldaketak egiteko aukera ematen du.

:::image type="content" source="media/m3_review.png" alt-text="Bezeroen profilak berrikusi eta sortu pantaila-argazkia.":::

## <a name="review-the-data-unification-steps"></a>Berrikusi datuak bateratzeko urratsak

1. Hautatu **Editatu** datuak bateratzeko edozein urratsetan aldaketak berrikusteko eta egiteko.

1. Zure hautapenekin pozik bazaude, hautatu **Sortu bezeroen profilak**. The **Bateratu** orria bistaratzen da bezeroaren profil bateratua sortzen ari den bitartean. Bateratze algoritmoak denbora pixka bat behar du osatzeko eta ezin duzu konfigurazioa aldatu amaitu arte.

   [!INCLUDE [m3-task-details-include](includes/m3-task-details.md)]

Bateratze-prozesua amaitzen denean, bezeroen profil bateratuaren entitateak deitu du *Bezeroa*, atalean ageri da **Entitateak** orrialdean **Profilak** atala. Lehenengo bateratze-exekutatu arrakastatsuak bateratua sortzen du *Bezeroa* entitate. Ondorengo exekuzio guztiek entitate hori zabaltzen dute.

## <a name="review-the-results-of-data-unification"></a>Berrikusi datuak bateratzearen emaitzak

Bategitearen ostean, **Datuak** > **Bateratu** orrialdeak bezeroen profil bateratuen kopurua erakusten du. Batasun-prozesuko urrats bakoitzaren emaitzak fitxa bakoitzean bistaratzen dira. Adibidez, **Iturburu-eremuak** mapatutako atributu kopurua (eremuak) erakusten du eta **Erregistro bikoiztuak** aurkitutako erregistro bikoiztuen kopurua erakusten du.

:::image type="content" source="media/m3_unified.png" alt-text="Datuak bateratu ondoren datuak bateratu orriaren pantaila-argazkia.":::

> [!TIP]
> The **Bat datozen baldintzak** lauza entitate bat baino gehiago hautatuta badago soilik bistaratzen da.

Emaitzak berrikustea gomendatzen dizugu, batez ere zure kalitatea [partida arauak](data-unification-update.md#manage-match-rules) eta hobetu behar izanez gero.

Beharrezkoa denean, [egin aldaketak bateratze-ezarpenetan](data-unification-update.md) eta berriro exekutatu profil bateratua.

## <a name="next-step"></a>Hurrengo urratsa

Konfiguratu [jarduerak](activities.md),[aberastea](enrichment-hub.md),[harremanak](relationships.md), edo [neurriak](measures.md) zure bezeroei buruzko informazio gehiago lortzeko.

[!INCLUDE[footer-include](includes/footer-banner.md)]
