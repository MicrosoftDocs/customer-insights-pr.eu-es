---
title: Jardueretan oinarritutako iradokitako segmentuak.
description: Utzi Ikaskuntza automatikoek bezeroen jardueran oinarritutako segmentu berri eta interesgarriak aurkitzen laguntzen.
ms.date: 05/11/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
manager: shellyha
ms.openlocfilehash: 14d9d4f0df6b5835f21fb63447d05853ee98a757
ms.sourcegitcommit: 8341fa964365c185b65bc4b71fc0c695ea127dc0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/14/2021
ms.locfileid: "6034045"
---
# <a name="suggested-segments-based-on-activity-data-preview"></a><span data-ttu-id="c2cb6-103">Jardueretan oinarritutako iradokitako segmentuen datuak (aurreargitalpena)</span><span class="sxs-lookup"><span data-stu-id="c2cb6-103">Suggested segments based on activity data (preview)</span></span>

<span data-ttu-id="c2cb6-104">Ezagutu bezeroen segmentu interesgarriak Customer Insights-en kontsumitutako bezeroen jardueren datuetan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-104">Discover interesting segments of your customers based on customer activity data that is ingested to Customer Insights.</span></span> <span data-ttu-id="c2cb6-105">Jardueren datuen adibideak transakzioak, laguntza deien iraupena, erosketak edo itzulketak dira.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-105">Examples of activity data are transactions, support call duration, purchases, or returns.</span></span> <span data-ttu-id="c2cb6-106">Segmentuak iradokitzeko, jardueren datuak aztertzen dira berritasuna, maiztasuna eta diru balioa (edo iraupena).</span><span class="sxs-lookup"><span data-stu-id="c2cb6-106">To suggest segments, activity data gets analyzed for recency, frequency, and monetary value (or duration).</span></span> <span data-ttu-id="c2cb6-107">Bestela, sor dezakezu [iradokitako segmentuak neurri bat hobetzeko edo atributu batek zerk eragiten duen hobeto ulertzeko](suggested-segments.md).</span><span class="sxs-lookup"><span data-stu-id="c2cb6-107">Alternatively, you can generate [suggested segments to improve a measure or better understand what influences an attribute](suggested-segments.md).</span></span>

:::image type="content" source="media/suggested-segments-tab.png" alt-text="Iradokitako segmentuen fitxa, jardueran oinarritutako eta atributuetan oinarritutako segmentuen iradokizunak erakusten dituena.":::

## <a name="categorize-customers-by-activity"></a><span data-ttu-id="c2cb6-109">Sailkatu bezeroak jardueraren arabera</span><span class="sxs-lookup"><span data-stu-id="c2cb6-109">Categorize customers by activity</span></span>

<span data-ttu-id="c2cb6-110">Customer Insights-en eskuragarri dauden [Jardueraren datuekin](activities.md), bezero taldeak ordezkatzen dituzten iradokizunak sor ditzakegu:</span><span class="sxs-lookup"><span data-stu-id="c2cb6-110">With [activity data](activities.md) available in Customer Insights, we can generate suggestions that represent customer groups:</span></span>

- <span data-ttu-id="c2cb6-111">bezero aktibo gehienak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-111">most active customers</span></span> 
- <span data-ttu-id="c2cb6-112">erosketa gehien egin dituzten bezeroak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-112">customers that have made the most purchases</span></span> 
- <span data-ttu-id="c2cb6-113">diru-sarrera gehien sortu duten bezeroak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-113">customers that generated the most revenue</span></span> 
- <span data-ttu-id="c2cb6-114">azkenaldian aktibo egon ez diren bezeroak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-114">customers who haven’t been active lately</span></span> 
- <span data-ttu-id="c2cb6-115">zure negozioarekin maiz elkarreragiten duten bezeroak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-115">customers who frequently interact with your business</span></span>  

<span data-ttu-id="c2cb6-116">Txikizkako negozioa baduzu, jakingo zenuke zein bezero sortzen duten diru sarrera gehien eta kupoi batekin saritzen dituzten.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-116">If you have a retail business, you could find out which customers generate the most revenue and reward them with a coupon.</span></span> <span data-ttu-id="c2cb6-117">Edo noizbehinkako bezeroak identifikatu eta sari programa batean sartzeko eskaintza egin dezakezu zure negozioa maizago bisitatzeko.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-117">Or you can identify occasional customers and offer them to join a rewards program so they visit your business more often.</span></span>
<span data-ttu-id="c2cb6-118">Osasun publikoa eskaintzen ari zaren osasun negozioan bazabiltza eta zure helburua gaixo bakoitzarentzako gastuak gutxitzea da.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-118">If you're in the healthcare business providing public healthcare and your goal is to minimize the expenses for individual patients.</span></span> <span data-ttu-id="c2cb6-119">Horretarako modu bat aldizkako bisitak murriztea izan daiteke, ahalik eta bisita gutxienetan arreta onena eskainiz.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-119">A way to do so could be to reduce recurring visits by providing best possible care in as few visits as possible.</span></span> <span data-ttu-id="c2cb6-120">Kasu honetan, zure helburua da bisitaren maiztasuna baxua izatea eta pazienteen errepikapeneko kostua minimizatzea.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-120">In this case, your goal is to keep the visit frequency low and minimize recurring cost for the patients.</span></span> <span data-ttu-id="c2cb6-121">Edo maiz hitzorduak eta errepikatzen diren kostu handiak dituzten gaixoen segmentuak identifikatu eta kasu horiek aztertu ditzakezu norbanakoaren tratamendua hobetzeko.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-121">Or you can identify segments of patients who have frequent appointments and high recurring costs and analyze these cases to improve the treatment of the individual.</span></span> 

## <a name="required-data"></a><span data-ttu-id="c2cb6-122">Beharrezko datuak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-122">Required data</span></span>

<span data-ttu-id="c2cb6-123">Iradokizunak hautatutako sarrerako datuetan oinarrituta sortzen dira.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-123">Suggestions are generated based on the selected input data.</span></span> 

- <span data-ttu-id="c2cb6-124">Bezeroen profilak: segmentu zehatz bateko bezero guztiak edo kideak.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-124">Customer profiles: All customers or members of a specific segment.</span></span> 

- <span data-ttu-id="c2cb6-125">Denbora-tartea: azken hilabetea, iazkoa edo edozein denbora pertsonalizatua.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-125">Time period: Last month, last year, or any custom time frame.</span></span>

- <span data-ttu-id="c2cb6-126">Jarduera mota: erosketak, txikizkako transakzioak, lineako transakzioak, bezeroari arreta emateko kasuak, harpidetzak, eta beste.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-126">Activity type: purchases, retail transactions, online transactions, customer support cases, subscriptions, and so on.</span></span>  

- <span data-ttu-id="c2cb6-127">Jarduera datuak biltzen dituen Customer Insights-eko entitatea: UnifiedActivity entitatea edo jarduera zehatz baterako entitatea.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-127">Entity in Customer Insights that contains the activity data: The UnifiedActivity entity or the entity for a specific activity.</span></span> 

- <span data-ttu-id="c2cb6-128">Sartu beharreko neurriak: berritasuna, maiztasuna edo diru dimentsioa, zure negozioaren eskakizunen arabera.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-128">Dimensions to include: Recency, frequency, or monetary dimension, depending on your business requirements.</span></span>

## <a name="generate-suggested-segments"></a><span data-ttu-id="c2cb6-129">Sortu iradokitako segmentuak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-129">Generate suggested segments</span></span>

1. <span data-ttu-id="c2cb6-130">Joan hona: **Segmentuak**.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-130">Go to **Segments**.</span></span>

1. <span data-ttu-id="c2cb6-131">Aukeratu **Iradokizunak (aurrebista)** fitxa.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-131">Select the **Suggestions (preview)** tab.</span></span>

1. <span data-ttu-id="c2cb6-132">Aukeratu **Bilatu iradokizun berriak** eta aukeratu **Ikusi edo aurreikusi bezeroen portaera**.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-132">Select **Find new suggestions** and choose **See or anticipate customer behavior**.</span></span> <span data-ttu-id="c2cb6-133">Aukeratu **Hasi** esperientzia gidatua martxan jartzeko.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-133">Select **Start** to run the guided experience.</span></span>

   :::image type="content" source="media/suggested-segments-activity-wizard.png" alt-text="Jardueran oinarritutako iradokitako segmentu baterako konfigurazio morroiaren lehen urratsa.":::

1. <span data-ttu-id="c2cb6-135">Eman beharrezko sarrerako datuak eta hautatu **Hurrengoa** jarraitu.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-135">Provide the required input data and select **Next** proceed.</span></span>

   - <span data-ttu-id="c2cb6-136">Aukeratu bezeroak: sartu bezero guztiak edo segmentu zehatz bat.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-136">Choose customers: Include all customers or a specific segment.</span></span>
   - <span data-ttu-id="c2cb6-137">Aukeratu jarduera: hautatu jarduera mota eta jarduera azaltzen duten entitateak.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-137">Choose activity: Select the activity type and the entities that describe the activity.</span></span>
   - <span data-ttu-id="c2cb6-138">Hobespenak: ezarri kontuan hartu beharreko denbora, iradokizunen faktoreak eta esleitu atributuak.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-138">Preferences: Set the time period to consider, the factors for suggestions, and map the attributes.</span></span>

1. <span data-ttu-id="c2cb6-139">Berrikusi zure sarrera eta hautatu **Exekutatu** eredua martxan jartzeko eta iradokizunak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-139">Review your input and select **Run** to run the model and generate suggestions.</span></span>

1. <span data-ttu-id="c2cb6-140">Bezeroen profil kopuruaren eta hautatutako jardueren arabera, minutu batzuk behar izan ditzake burutzeko.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-140">Depending on the number of customer profiles and selected activities, it can take a few minutes to complete.</span></span> 

<span data-ttu-id="c2cb6-141">Iradokizunak sortu ondoren, gehien interesatzen zaizun dimentsioaren edo balioaren arabera iragazi ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-141">After generating the suggestions, you can filter them by the dimension or value you're most interested in.</span></span> 

## <a name="view-details-of-a-suggested-segment"></a><span data-ttu-id="c2cb6-142">Ikusi Iradokitako segmentuaren xehetasunak</span><span class="sxs-lookup"><span data-stu-id="c2cb6-142">View details of a suggested segment</span></span>

<span data-ttu-id="c2cb6-143">Iradokizunak sortu ondoren, hemen zerrendatuta aurkituko dituzu **Segmentuak** > **Iradokizunak (aurrebista)** aukera, **Jardueretan oinarritutako iradokizunak** atalean dagoena.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-143">Once the suggestions are generated, you'll find them listed on **Segments** > **Suggestions (preview)** in the **Activity-based suggestions** section.</span></span>

:::image type="content" source="media/suggested-segments-details.png" alt-text="Iradokitako segmentu baten datu zehatzak erakusten dituen alboko panel zabaldua.":::

<span data-ttu-id="c2cb6-145">Aukeratu **Ikusi iradokizuna** iradokitako segmentu batean segmentu horren xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-145">Select **See suggestion** on a suggested segment to view the details of that segment.</span></span> <span data-ttu-id="c2cb6-146">Alboko panelak dimentsio bakoitzaren neurria bezalako xehetasunak eskaintzen ditu xede-taldearekin alderatuta.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-146">The side pane provides details like the extent of each dimension in comparison to the target group.</span></span> <span data-ttu-id="c2cb6-147">Segmentuko kide potentzialen kopurua eta bezero guztiei dagokien ehunekoa ere nabarmentzen ditu.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-147">It also highlights the number of potential members in the segment and the corresponding percentage of the total customers.</span></span> <span data-ttu-id="c2cb6-148">Iradokizuna segmentu gisa gorde nahi baduzu, hautatu **Sortu segmentua**.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-148">If you want to keep the suggestion as a segment, select **Create segment**.</span></span>    

## <a name="save-a-suggestion-as-a-segment"></a><span data-ttu-id="c2cb6-149">Gorde segmentu bat iradokizun gisa</span><span class="sxs-lookup"><span data-stu-id="c2cb6-149">Save a suggestion as a segment</span></span>

1. <span data-ttu-id="c2cb6-150">Joan **Segmentuak** > **Iradokizunak (aurrebista)**.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-150">Go to **Segments** > **Suggestions (preview)**.</span></span>

1. <span data-ttu-id="c2cb6-151">Hautatu gorde nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-151">Select the segment you want to save.</span></span> 

1. <span data-ttu-id="c2cb6-152">Alboko panelean, hautatu **Sortu segmentua**.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-152">In the side pane, select **Create segment**.</span></span> 

1. <span data-ttu-id="c2cb6-153">Segmentua gorde ondoren, segmentuen zerrendan agertuko da **Segmentu guztiak** fitxa. Orain izan daiteke [freskatu edo ezabatu beste edozein segmentu bezala](segments.md).</span><span class="sxs-lookup"><span data-stu-id="c2cb6-153">After saving the segment, it will show in the list of segments on the **All segments** tab. It can now be [refreshed or deleted like any other segment](segments.md).</span></span> <span data-ttu-id="c2cb6-154">Ezin dituzu segmentuaren xehetasunak editatu.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-154">You can't edit the segment details.</span></span> <span data-ttu-id="c2cb6-155">Hala ere, iradokizunetarako irizpideak aldatu eta iradokizun desberdinak sor ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-155">However, you can change the input criteria for the suggestions and generate different suggestions.</span></span>

## <a name="refresh-or-edit-a-set-of-suggestions"></a><span data-ttu-id="c2cb6-156">Freskatu edo editatu iradokizun multzo bat</span><span class="sxs-lookup"><span data-stu-id="c2cb6-156">Refresh or edit a set of suggestions</span></span>

1. <span data-ttu-id="c2cb6-157">Joan **Segmentuak** > **Iradokizunak (aurrebista)** eta bilatu segmentua **Jardueretan oinarritutako iradokizunak** atala.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-157">Go to **Segments** > **Suggestions (preview)** and look for the segment in the **Activity-based suggestions** section.</span></span>

1. <span data-ttu-id="c2cb6-158">Aukeratu **Freskatu iradokizunak** iradokizunak freskatzeko konfiguratutako atributuak mantenduz.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-158">Select **Refresh suggestions** to refresh the suggestions while keeping configured attributes.</span></span> <span data-ttu-id="c2cb6-159">Edo hautatu **Editatu iradokizunak** konfiguratutako atributuak aldatzeko.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-159">Or select **Edit suggestions** to modify the configured attributes.</span></span> <span data-ttu-id="c2cb6-160">Sistemak prozesua berriro exekutatuko du, segmentu iradokizunak sortuko ditu azken datuetan oinarrituta eta uneko iradokizunak ordezkatuko ditu.</span><span class="sxs-lookup"><span data-stu-id="c2cb6-160">The system will rerun the process, generate segment suggestions based on the latest data, and replace the current suggestions.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
