---
title: Neurrien ikuspegi orokorra
description: Ikasi neurriek nola laguntzen duten zure negozioaren errendimendua aztertzen eta islatzen.
ms.date: 03/24/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: v-wendysmith
ms.author: wameng
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-measures
- ci-measure-builder
- ci-measure-template
- ci-enrichment-details
- customerInsights
ms.openlocfilehash: 99368a7ab2e8d7b3e53c04fbf25bb23bd2e550a9
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9245358"
---
# <a name="measures-overview"></a>Neurrien ikuspegi orokorra

Neurriek bezeroen portaerak eta negozioaren errendimendua hobeto ulertzen lagunduko dizute. Balio garrantzitsuak aztertzen dituzte [profil bateratuak](data-unification.md). Adibidez, enpresa batek ikusi nahi du *bezero bakoitzeko guztizko gastua* bezero bakoitzaren erosketa historia edo neurria ulertzeko *enpresaren guztizko salmentak* negozio osoko diru-sarrera agregatuak ulertzeko.

Sortu negozio-jarduerak planifikatzeko neurriak bezeroen datuak kontsultatuz eta ikuspegiak ateraz. Adibidez, sortu neurri bat *guztizko gastua bezero bakoitzeko* eta *bezero bakoitzeko etekin osoa* gastu handia baina errentagarritasun handia duten bezero talde bat identifikatzen laguntzeko. Orduan, [segmentu bat sortu](segments.md) neurri horietan oinarrituta hurrengo ekintza onenak bultzatzeko.

## <a name="create-a-measure"></a>Sortu neurri bat

Aukeratu nola sortu neurri bat zure xede-publikoaren arabera.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- Hutsetik neurri-eraikitzailearekin: [Eraiki zeurea](measure-builder.md).
- Gehien erabiltzen diren neurrietatik: [Erabili aurrez zehaztutako txantiloiak](measure-templates.md).

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

Hutsetik neurri-eraikitzailearekin: [Eraiki zeurea](measure-builder.md).

---

## <a name="manage-existing-measures"></a>Dauden neurriak kudeatzea

Joan zaitez **Neurriak** orrialdean sortu dituzun neurriak, haien egoera, neurri mota eta datuak freskatu diren azken aldia ikusteko. Neurrien zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun neurria aurkitzeko.

Hautatu neurri baten ondoan erabilgarri dauden ekintzak ikusteko. Hautatu neurriaren izena irteera aurreikusteko eta CSV fitxategi bat deskargatzeko.

:::image type="content" source="media/measures-actions.png" alt-text="Neurri bakarrak kudeatzeko ekintzak."lightbox="media/measures-actions.png":::

- **Editatu** bere propietateak aldatzeko neurria.
- **Freskatu** azken datuak sartzeko neurria.
- **Aldatu izena** neurria.
- **Aktibatu** edo **Desaktibatu** neurria. Neurri inaktiboak ez dira freskatuko a bitartean [programatutako freskadura](schedule-refresh.md) eta izan **Egoera** gisa zerrendatuta **Saltatu**, freskatze bat ere saiatu ez dela adieraziz.
- **Etiketa** to [kudeatu etiketak](work-with-tags-columns.md#manage-tags) neurrirako.
- **Ezabatu** neurria.
- **Zutabeak** to [pertsonalizatu zutabeak](work-with-tags-columns.md#customize-columns) pantaila hori.
- **Iragazkia** to [iragazkia etiketetan](work-with-tags-columns.md#filter-on-tags).
- **Bilatu izena** neurriaren izenaren arabera bilatzeko.

## <a name="refresh-measures"></a>Freskatzeko neurriak

Neurriak programazio automatiko batean freskatu daitezke edo eskuz freskatu daitezke eskaeraren arabera. Neurri bat edo gehiago eskuz freskatzeko, hautatu eta aukeratu **Freskatu**. To [programatu freskatze automatikoa](schedule-refresh.md), joan **Admin** > **Sistema** > **Ordutegia**.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
