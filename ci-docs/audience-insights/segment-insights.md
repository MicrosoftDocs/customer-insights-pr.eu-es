---
title: Lehendik dauden segmentuen xehetasunak
description: Lortu lehendik dauden segmentuei buruzko xehetasunak desberdintasunak eta puntu komunak ikusteko.
ms.date: 06/10/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 2856888d6ac64d5daabcc5a234f13bc6f88bb3df
ms.sourcegitcommit: 0b754d194d765afef70d1008db7b347dd1f0ee40
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306059"
---
# <a name="segment-insights-preview"></a><span data-ttu-id="bcfdd-103">Segmentuaren xehetasunak (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="bcfdd-103">Segment insights (preview)</span></span>

<span data-ttu-id="bcfdd-104">Ezagutu informazio eta ikuspegi gehiago zure lehendik dauden segmentuei buruz.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-104">Discover additional information and insights around your existing segments.</span></span> <span data-ttu-id="bcfdd-105">Aurki itzazu bi segmentu bereizten dituztenak edo komunean zer duten.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-105">Find out what differentiates two segments or what they have in common.</span></span>

## <a name="segment-overlap"></a><span data-ttu-id="bcfdd-106">Segmentuen teilakatzea</span><span class="sxs-lookup"><span data-stu-id="bcfdd-106">Segment overlap</span></span>

<span data-ttu-id="bcfdd-107">Segmentuen gaineko gaineko azterketak erakusten du zenbat bezero eta bi bezero edo bi segmenturen ohikoak diren.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-107">Segment overlap analysis shows how many and which customers are common to two or more segments.</span></span> <span data-ttu-id="bcfdd-108">Adibidez, maiz bezeroen segmentu bat nola gurutzatzen den zure zerbitzuarekin edo produktuarekin pozik dauden bezeroak dituen segmentu batekin.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-108">For example, how a segment of frequent customers overlaps with a segment that contains customers that are satisfied with your service or product.</span></span>
<span data-ttu-id="bcfdd-109">Erabaki aldaketak nola lotzen diren ere atributu zehatzetarako azter daiteke.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-109">You can also analyze how the overlap changes for specific attributes.</span></span>

### <a name="run-an-overlap-analysis"></a><span data-ttu-id="bcfdd-110">Egin gainjarrien azterketa</span><span class="sxs-lookup"><span data-stu-id="bcfdd-110">Run an overlap analysis</span></span>

1. <span data-ttu-id="bcfdd-111">Joan **segmentuak** eta hautatu **Xehetasunak (aurrebista)** fitxa.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-111">Go to **Segments** and select the **Insights (preview)** tab.</span></span>

1. <span data-ttu-id="bcfdd-112">Aukeratu **Berria** eta aukeratu **Teilakatzearen** Aukera aukeran **Aukeratu xehetasun mota** panela.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-112">Select **New** and choose the **Overlap** option in the **Choose Insight Type** pane.</span></span>

1. <span data-ttu-id="bcfdd-113">Aukeratu intereseko segmentuak eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-113">Choose the segments of interest and select **Next**.</span></span>

1. <span data-ttu-id="bcfdd-114">Aukeran, interes-eremu bat edo gehiago aukeratu, gainjakinak aztertu litezkeen eremu posible bakoitzerako eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-114">Optionally, choose one or more fields of interest to analyze overlaps for every possible field value and select **Next**.</span></span>

1. <span data-ttu-id="bcfdd-115">Idatzi bata bestearen gaineko analisia egiteko aukera, aukerako pantailaren izena eta deskribapena.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-115">Provide a name for you overlap analysis, an optional display name, and a description.</span></span>

1. <span data-ttu-id="bcfdd-116">Aukeratu **Gorde** azterketa hasteko.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-116">Select **Save** to start the analysis.</span></span> <span data-ttu-id="bcfdd-117">Gainjarpenen analisia egoera prest dago, Freskapenetik Arrakastara.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-117">The overlap analysis is ready when the status changes from Refreshing to Successful.</span></span>

### <a name="view-and-optimize-an-overlap-analysis"></a><span data-ttu-id="bcfdd-118">Ikusi eta optimizatu gainjarritako azterketa bat</span><span class="sxs-lookup"><span data-stu-id="bcfdd-118">View and optimize an overlap analysis</span></span>

<span data-ttu-id="bcfdd-119">Azterketa amaitu ondoren, aurkitu xehetasun honi buruzko xehetasunak **segmentuak** > **Xehetasunak (aurrebista)**.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-119">After completing the analysis, find details on this insight on **Segments** > **Insights (preview)**.</span></span>

> [!div class="mx-imgBorder"]
> :::image type="content" source="media/segment-overlap.png" alt-text="Segmentuen gaineko ikuspegi xehetasunak":::

<span data-ttu-id="bcfdd-121">Hautatu ikuspegi bat analisiaren emaitzak ikusteko:</span><span class="sxs-lookup"><span data-stu-id="bcfdd-121">Select an insight to see the analysis results:</span></span>

- <span data-ttu-id="bcfdd-122">Analisirako hautatutako segmentuen gainjarri diren kideen kopurua.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-122">The number of members overlapping the segments selected for analysis.</span></span>
- <span data-ttu-id="bcfdd-123">Segmenturen batean sartutako kide kopurua baina ez da gainerako segmentuetan.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-123">The number of members included in one of the segments but not in the rest of the segments.</span></span>
- <span data-ttu-id="bcfdd-124">Gainerako azterketak konfiguratzen ari zaren bitartean eremuak aukeratu badituzu, dagozkien fitxetan aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-124">If you selected fields while configuring the overlap analysis, you'll find them in the corresponding tabs.</span></span> <span data-ttu-id="bcfdd-125">Iragazki goitibeherako edozein atributu interes maila hautatzeko erabil dezakezu eta beheko taulan dagozkion datuak erakutsiko dira.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-125">You can use the filter dropdown to select any attribute level of interest and the table at the bottom will show the corresponding data.</span></span>

## <a name="segment-differentiators"></a><span data-ttu-id="bcfdd-126">Segmentu-bereizleak</span><span class="sxs-lookup"><span data-stu-id="bcfdd-126">Segment differentiators</span></span>

<span data-ttu-id="bcfdd-127">Segmentuen bereizleek segmentu bat gainerako bezeroek edo beste segmentu batek bereizten duen jakiten lagunduko dizu.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-127">Segment differentiators help you find out what differentiates a segment from the rest of your customers or from another segment.</span></span> <span data-ttu-id="bcfdd-128">Segmentu bat aukeratu besterik ez duzu eta sistemak hautatutako segmentua bereizten duten profil atributuak eta neurriak identifikatuko ditu.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-128">You just have to select a segment and the system will identify profile attributes and measures that distinguish the selected segment.</span></span>

### <a name="run-a-differentiator-analysis"></a><span data-ttu-id="bcfdd-129">Egin ezberdintasun azterketa</span><span class="sxs-lookup"><span data-stu-id="bcfdd-129">Run a differentiator analysis</span></span>

1. <span data-ttu-id="bcfdd-130">Joan **segmentuak** eta hautatu **Xehetasunak (aurrebista)** fitxa.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-130">Go to **Segments** and select the **Insights (preview)** tab.</span></span>

1. <span data-ttu-id="bcfdd-131">Aukeratu **Berria** eta aukeratu **Teilakatzearen** Aukera aukeran **Aukeratu xehetasun mota** panela.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-131">Select **New** and choose the **Overlap** option in the **Choose Insight Type** pane.</span></span>

1. <span data-ttu-id="bcfdd-132">Aukeratu aztertu nahi duzun segmentua **Lehen mailako segmentua** eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-132">Choose the segment you want to analyze as **Primary segment** and select **Next**.</span></span>

1. <span data-ttu-id="bcfdd-133">Aukeratu **Bezero guztiak** edo **Bigarren mailako segmentua** zure segmentu nagusia konparatu eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-133">Choose **All customers** or a **Secondary segment** to compare your primary segment with and select **Next**.</span></span>

1. <span data-ttu-id="bcfdd-134">Aukeran, interes-eremu bat edo gehiago aukeratu analisia atributu zehatzetara bideratzeko eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-134">Optionally, choose one or more fields of interest to focus the analysis on specific attributes and select **Next**.</span></span>

1. <span data-ttu-id="bcfdd-135">Idatzi bata bestearen gaineko analisia egiteko aukera, aukerako pantailaren izena eta deskribapena.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-135">Provide a name for you overlap analysis, an optional display name, and a description.</span></span>

1. <span data-ttu-id="bcfdd-136">Aukeratu **Gorde** azterketa hasteko.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-136">Select **Save** to start the analysis.</span></span> <span data-ttu-id="bcfdd-137">Gainjarpenen analisia egoera prest dago, Freskapenetik Arrakastara.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-137">The overlap analysis is ready when the status changes from Refreshing to Successful.</span></span>

### <a name="view-and-optimize-a-differentiators-analysis"></a><span data-ttu-id="bcfdd-138">Ikusi eta optimizatu bereizleen azterketa</span><span class="sxs-lookup"><span data-stu-id="bcfdd-138">View and optimize a differentiators analysis</span></span>

<span data-ttu-id="bcfdd-139">Azterketa amaitu ondoren, aurkitu xehetasun honi buruzko xehetasunak **segmentuak** > **Xehetasunak (aurrebista)**.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-139">After completing the analysis, find details on this insight on **Segments** > **Insights (preview)**.</span></span>

> [!div class="mx-imgBorder"]
> :::image type="content" source="media/segment-differentiators.png" alt-text="Segmentuen desberdintzailea ikuspegi xehetasunak":::

<span data-ttu-id="bcfdd-141">Hautatu ikuspegi bat analisiaren emaitzak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-141">Select an insight to see the analysis results.</span></span> <span data-ttu-id="bcfdd-142">Ezberdintasunen azterketak bi fitxa biltzen ditu.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-142">A differentiator analysis includes two tabs.</span></span> <span data-ttu-id="bcfdd-143">**Atributuak** fitxak bereizle gisa kontsideratutako profil atributuak zerrendatzen ditu.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-143">The **Attributes** tab lists profile attributes considered as differentiators.</span></span> <span data-ttu-id="bcfdd-144">**Neurriak** fitxa bereizleak.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-144">The **Measures** tab lists differentiators.</span></span> <span data-ttu-id="bcfdd-145">Fitxa bakoitzean xehetasun hauek daude:</span><span class="sxs-lookup"><span data-stu-id="bcfdd-145">Each tab includes the following details:</span></span>

- <span data-ttu-id="bcfdd-146">Sailkatutako desberdintzen zerrenda, puntuazioaren arabera sailkatuta.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-146">Ranked list of differentiators, sorted by difference score.</span></span>
- <span data-ttu-id="bcfdd-147">**Diferentzia puntuazioa** bereizle bakoitzerako.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-147">The **Difference score** for each differentiator.</span></span> <span data-ttu-id="bcfdd-148">Alde puntuazioak bi segmentuen arteko atributu baten diferentzia maila adierazten du.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-148">The difference score represents the degree of difference of an attribute between two segments.</span></span> <span data-ttu-id="bcfdd-149">Alde puntuazioa zenbat eta handiagoa izan, orduan eta atributuak desberdinagoak dira bi segmentuen artean.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-149">The higher the difference score, the more the attributes differ between the two segments.</span></span> <span data-ttu-id="bcfdd-150">Aukeratu partitura bat irekitzeko **Diferentzia puntuazioa** panela atributu horren balio banaketekin.</span><span class="sxs-lookup"><span data-stu-id="bcfdd-150">Select a score to open the **Difference score** pane with the distributions of values for that attribute.</span></span>

## <a name="manage-segment-insights"></a><span data-ttu-id="bcfdd-151">Kudeatu segmentuaren xehetasunak</span><span class="sxs-lookup"><span data-stu-id="bcfdd-151">Manage segment insights</span></span>

<span data-ttu-id="bcfdd-152">Komandoen barrutik honako aukera hauek erabil ditzakezu:</span><span class="sxs-lookup"><span data-stu-id="bcfdd-152">You can use the following options on your insights from the command bar:</span></span>

- <span data-ttu-id="bcfdd-153">**Atzera** ikuspegi zerrenda itzultzeko</span><span class="sxs-lookup"><span data-stu-id="bcfdd-153">**Back** to return the list of insights</span></span>
- <span data-ttu-id="bcfdd-154">**Freskatu** azterketa berriro exekutatzeko</span><span class="sxs-lookup"><span data-stu-id="bcfdd-154">**Refresh** to run the analysis again</span></span>
- <span data-ttu-id="bcfdd-155">**Ezabatu** ikuspegi hori kentzeko</span><span class="sxs-lookup"><span data-stu-id="bcfdd-155">**Delete** to remove this insight</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]