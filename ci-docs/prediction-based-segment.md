---
title: Sortu segmentu bat iragarpen ereduan oinarrituta
description: Sortu segmentuak iragarpen modelo baten irteerako entitatean oinarrituta.
ms.date: 09/19/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: ed9c6247a1f9148628dc9b5217484e98a576224e
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610405"
---
# <a name="create-a-segment-based-on-a-prediction-model-preview"></a>Sortu segmentu bat iragarpen modeloan oinarrituta (aurrebista)

Iragarpenen emaitzak batzuetan zure bezeroen azpimultzo bati soilik aplikatzen zaizkio. Handitu gomendioen pertsonalizazioa iragarpen ereduen emaitzetatik segmentuak sortuz. Adibidez, zerbitzu mota jakin bat nahiago duten bezeroei gomendio zehatzak eman nahi dizkiezu.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.

- Customer Insights-en konfiguratutako produktuaren gomendioa, transakzioaren buelta, harpidetzaren buelta edo bezeroaren bizitza osoko balioaren eredua. Berrikusi eredu desberdinak konfiguratzeko eskakizunak:

  - [Produktuak gomendatzeko eredua](predict-product-recommendation.md)
  - [Harpidetza bertan behera uzteko eredua](predict-subscription-churn.md)
  - [Transakzioa bertan behera uzteko eredua](predict-transactional-churn.md)
  - [Bezeroaren bizi-iraupenaren balioaren eredua](predict-customer-lifetime-value.md)

## <a name="create-a-customer-segment-based-on-predictions"></a>Sortu bezeroen segmentua iragarpenetan oinarrituta

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Hautatu berrikusi nahi duzun eredua eta hautatu **Ikusi**.

1. Emaitzen orrian, hautatu **Sortu segmentua**. Emaitzen orriari buruzko informazio gehiago lortzeko, berrikusi ereduari buruzko artikulua.

   :::image type="content" source="media/prediction-create-segment.png" alt-text="iragarpen emaitzen orriaren pantaila-argazkia Sortu segmentua ekintzan nabarmenduta.":::

1. Sortu segmentu berri bat hautatutako ereduaren irteerako entitatearen atributuak erabiliz. Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).

> [!TIP]
> Iragarpen eredu baterako segmentu bat ere sor dezakezu hemendik **Segmentuak** orrialdea hautatuz **Berria** eta aukeratzea **Sortu hemendik** > **Adimena**. Informazio gehiagorako, ikus [Sortu segmentu berri bat segmentu azkarrekin](segment-quick.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
