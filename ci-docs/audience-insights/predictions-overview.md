---
title: Onartutako iragarpen agertokiei buruzko ikuspegi orokorra
description: Dynamics 365 Customer Insights aplikazioak lantzen dituen iragarpen agertokiak eta aukerak.
ms.date: 05/18/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: get-started
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: 69ae945b22819521db217508c6fc232876346747
ms.sourcegitcommit: 6b07c9c3102761be162e4842f3c9fbc19f948a9b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "6095681"
---
# <a name="predictions-overview"></a><span data-ttu-id="b7f0e-103">Iragarpenen ikuspegi orokorra</span><span class="sxs-lookup"><span data-stu-id="b7f0e-103">Predictions overview</span></span>

<span data-ttu-id="b7f0e-104">Dynamics 365 Customer Insights adimen artifiziala eta Ikaskuntza automatikoa baliatzeko aukera ugari ditu, datuak iragartzeko.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-104">Dynamics 365 Customer Insights comes with a variety of options that leverage AI and machine learning to predict data.</span></span> 

## <a name="out-of-box-models"></a><span data-ttu-id="b7f0e-105">Erabiltzeko prest dauden ereduak</span><span class="sxs-lookup"><span data-stu-id="b7f0e-105">Out-of-box models</span></span>

<span data-ttu-id="b7f0e-106">Datuak aurreikusten hasteko modurik errazena aurrez zehaztutako ereduak dira, maiz erabiltzeko prest dauden eredu gisa aipatzen direnak.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-106">The easiest way to start with predicting data are predefined models, often referred to as out-of-box models.</span></span> <span data-ttu-id="b7f0e-107">Datu eta egitura jakin batzuk besterik ez dituzte eskatzen estatistikak azkar sortzeko.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-107">They only require certain data and structure to generate insights quickly.</span></span> <span data-ttu-id="b7f0e-108">Gaur egun, eredu hauek daude eskuragarri:</span><span class="sxs-lookup"><span data-stu-id="b7f0e-108">Currently, the following models are available:</span></span> 
- <span data-ttu-id="b7f0e-109">[Bezeroaren bizi-iraupenaren balioa](predict-customer-lifetime-value.md): Bezero batek negozioarekin izandako elkarrekintza osoan zehar izan dezakeen diru sarrera iragartzen du.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-109">[Customer lifetime value](predict-customer-lifetime-value.md): Predicts the potential revenue of a customer throughout the entire interaction with a business.</span></span> 
- <span data-ttu-id="b7f0e-110">[Produktuen gomendioa](predict-product-recommendation.md): Produktu iragarleen gomendio multzoak iradokitzen ditu erosketa portaeran eta antzeko erosketa ereduak dituzten bezeroetan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-110">[Product recommendation](predict-product-recommendation.md): Suggests sets of predictive product recommendations based on purchase behavior and customers with similar purchase patterns.</span></span>
- <span data-ttu-id="b7f0e-111">[Harpidetzen galera-tasa](predict-subscription-churn.md): bezeroak enpresaren harpidetza-produktu eta -zerbitzuak erabiltzeari uzteko arriskua duen iragar dezake.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-111">[Subscription churn](predict-subscription-churn.md): Predicts whether a customer is at risk for no longer using your company’s subscription products or services.</span></span>
- <span data-ttu-id="b7f0e-112">[Transakzioen galera-tasa](predict-transactional-churn.md): Aurreikusi bezero batek zure produktuak edo zerbitzuak denbora tarte jakin batean erosiko ez dituen ala ez.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-112">[Transactional churn](predict-transactional-churn.md): Predict if a customer will no longer purchase your products or services in a certain time frame.</span></span>

## <a name="azure-machine-learning-integration"></a><span data-ttu-id="b7f0e-113">Azure ikaskuntza automatikoaren integrazioa</span><span class="sxs-lookup"><span data-stu-id="b7f0e-113">Azure Machine Learning integration</span></span>

<span data-ttu-id="b7f0e-114">Erakunde batek dagoeneko Azure Ikaskuntza automatikoaren esperientzietan oinarritutako Ikaskuntza automatikoko eszenatokiak erabiltzen baditu, Customer Insights-eko eredu pertsonalizatuen ezaugarriak puntuak konektatzen laguntzen du.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-114">If an organization already uses machine learning scenarios based on Azure Machine Learning experiments, the custom models feature in Customer Insights helps to connect the dots.</span></span> <span data-ttu-id="b7f0e-115">Sortu xehetasunak sortu nahi dituzun datuak aukeratzen lagunduko dizuten lan-fluxuak eta emaitzak zure bezeroen profil bateratuei esleitu.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-115">Create workflows that help you choose the data you want to generate insights from and map the results to your unified customer profiles.</span></span> <span data-ttu-id="b7f0e-116">Informazio gehiago lortzeko, ikus [Ikaskuntza automatiko eredu pertsonalizatuak](custom-models.md).</span><span class="sxs-lookup"><span data-stu-id="b7f0e-116">For more information, see [Custom machine learning models](custom-models.md).</span></span>

## <a name="ai-builder-prediction"></a><span data-ttu-id="b7f0e-117">AI Builder-en iragarpena</span><span class="sxs-lookup"><span data-stu-id="b7f0e-117">AI Builder prediction</span></span>

<span data-ttu-id="b7f0e-118">Batzuetan, datu multzoak osatu gabe daude eta balio batzuk falta dira.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-118">Sometimes, data sets are incomplete and some values are missing.</span></span> <span data-ttu-id="b7f0e-119">Customer Insights-ek Bezeroaren entitate eta segmentuetarako falta diren balioak aurreikusten lagun dezake.</span><span class="sxs-lookup"><span data-stu-id="b7f0e-119">Customer Insights can help to predict missing values for the Customer entity and segments.</span></span> <span data-ttu-id="b7f0e-120">Informazio gehiagorako, ikus [Osatu zure datu partzialak iragarpenekin](predictions.md).</span><span class="sxs-lookup"><span data-stu-id="b7f0e-120">For more information, see [Complete your partial data with predictions](predictions.md).</span></span>
