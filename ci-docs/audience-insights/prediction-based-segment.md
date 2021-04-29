---
title: Iragarpen irteeran oinarritutako segmentuak
description: Sortu segmentuak iragarpen modelo baten irteerako entitatean oinarrituta.
ms.date: 03/24/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: 488db1af865ce600ec012716327d053bee33aff8
ms.sourcegitcommit: a95c82f46c23f625cb34fceba021ccc70d4b1df6
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/30/2021
ms.locfileid: "5741414"
---
# <a name="create-a-segment-based-on-a-prediction-model-preview"></a><span data-ttu-id="5429e-103">Sortu segmentu bat iragarpen modeloan oinarrituta (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="5429e-103">Create a segment based on a prediction model (preview)</span></span>

<span data-ttu-id="5429e-104">Iragarpenen emaitzak batzuetan zure bezeroen azpimultzo bati soilik aplikatzen zaizkio.</span><span class="sxs-lookup"><span data-stu-id="5429e-104">The results of predictions sometimes only apply to a subset of your customers.</span></span> <span data-ttu-id="5429e-105">Handitu gomendioen pertsonalizazioa iragarpen ereduen emaitzetatik segmentuak sortuz.</span><span class="sxs-lookup"><span data-stu-id="5429e-105">Increase the personalization of recommendations by creating segments from results of prediction models.</span></span> <span data-ttu-id="5429e-106">Adibidez, zerbitzu mota jakin bat nahiago duten bezeroei gomendio zehatzak eman nahi dizkiezu.</span><span class="sxs-lookup"><span data-stu-id="5429e-106">For example, you may want to give specific recommendations to customers that prefer a certain type of service.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="5429e-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="5429e-107">Prerequisites</span></span>

- <span data-ttu-id="5429e-108">Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="5429e-108">At least [Contributor permissions](permissions.md) in Customer Insights.</span></span>

- <span data-ttu-id="5429e-109">Customer Insights-en konfiguratutako produktuaren gomendioa, transakzioaren buelta, harpidetzaren buelta edo bezeroaren bizitza osoko balioaren eredua.</span><span class="sxs-lookup"><span data-stu-id="5429e-109">A product recommendation, transactional churn, subscription churn, or customer lifetime value model configured in Customer Insights.</span></span> <span data-ttu-id="5429e-110">Berrikusi eredu desberdinak konfiguratzeko eskakizunak:</span><span class="sxs-lookup"><span data-stu-id="5429e-110">Review the requirements to set up the different models:</span></span>

  - [<span data-ttu-id="5429e-111">Produktuak gomendatzeko eredua</span><span class="sxs-lookup"><span data-stu-id="5429e-111">Product recommendation model</span></span>](predict-product-recommendation.md)
  - [<span data-ttu-id="5429e-112">Harpidetza bertan behera uzteko eredua</span><span class="sxs-lookup"><span data-stu-id="5429e-112">Subscription churn model</span></span>](predict-subscription-churn.md)
  - [<span data-ttu-id="5429e-113">Transakzioa bertan behera uzteko eredua</span><span class="sxs-lookup"><span data-stu-id="5429e-113">Transactional churn model</span></span>](predict-transactional-churn.md)
  - [<span data-ttu-id="5429e-114">Bezeroaren bizi-iraupenaren balioaren eredua</span><span class="sxs-lookup"><span data-stu-id="5429e-114">Customer lifetime value model</span></span>](predict-customer-lifetime-value.md)

## <a name="create-a-customer-segment-based-on-predictions"></a><span data-ttu-id="5429e-115">Sortu bezeroen segmentua iragarpenetan oinarrituta</span><span class="sxs-lookup"><span data-stu-id="5429e-115">Create a customer segment based on predictions</span></span>

1. <span data-ttu-id="5429e-116">Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.</span><span class="sxs-lookup"><span data-stu-id="5429e-116">Go to **Intelligence** > **Predictions** and select the **My predictions** tab.</span></span>

1. <span data-ttu-id="5429e-117">Aukeratu berrikusi nahi duzun ereduaren ondoan elipsi bertikalak eta hautatu **Ikusi**.</span><span class="sxs-lookup"><span data-stu-id="5429e-117">Select the vertical ellipses next to the model you want to review and select **View**.</span></span>

1. <span data-ttu-id="5429e-118">Emaitzen orrian, hautatu **Sortu segmentua**.</span><span class="sxs-lookup"><span data-stu-id="5429e-118">On the results page, select **Create segment**.</span></span> <span data-ttu-id="5429e-119">Emaitzen orriari buruzko informazio gehiago lortzeko, berrikusi ereduari buruzko artikulua.</span><span class="sxs-lookup"><span data-stu-id="5429e-119">For more information about the results page, review the article about the model.</span></span>

   :::image type="content" source="media/prediction-create-segment.png" alt-text="iragarpen emaitzen orriaren pantaila-argazkia Sortu segmentua ekintzan nabarmenduta.":::

1. <span data-ttu-id="5429e-121">Sortu segmentu berria irteerako entitatean oinarrituz hautatutako ereduan.</span><span class="sxs-lookup"><span data-stu-id="5429e-121">Create a new segment based on the output entity of the selected model.</span></span> <span data-ttu-id="5429e-122">Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).</span><span class="sxs-lookup"><span data-stu-id="5429e-122">For more information, see [Create and manage segments](segments.md).</span></span>