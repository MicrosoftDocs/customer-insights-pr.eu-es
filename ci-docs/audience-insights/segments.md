---
title: Hartzaileen xehetasunen segmentuak
description: Segmentuen ikuspegi orokorra eta nola sortu eta kudeatu.
ms.date: 05/03/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 6cb7bd62bf0f61e6dc5811b20e5011e4a086c743
ms.sourcegitcommit: 84283d523a891298fca8aaf629d9f9ab2a1bc067
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111372"
---
# <a name="segments-overview"></a><span data-ttu-id="2f894-103">Segmentuen informazio orokorra</span><span class="sxs-lookup"><span data-stu-id="2f894-103">Segments overview</span></span>

<span data-ttu-id="2f894-104">Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="2f894-104">Segments let you group your customers based on demographic, transactional, or behavioral attributes.</span></span> <span data-ttu-id="2f894-105">Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="2f894-105">You can use segments to target promotional campaigns, sales activities, and customer support actions to achieve your business goals.</span></span>

<span data-ttu-id="2f894-106">Segmentuaren definizio baten iragazkiekin bat datozen bezeroen profilak aipatzen dira *kideak* segmentu batena.</span><span class="sxs-lookup"><span data-stu-id="2f894-106">Customer profiles that match the filters of a segment definition are referred as *members* of a segment.</span></span> <span data-ttu-id="2f894-107">[Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.</span><span class="sxs-lookup"><span data-stu-id="2f894-107">Some [service limits](service-limits.md) apply.</span></span>

## <a name="create-a-new-segment"></a><span data-ttu-id="2f894-108">Sortu segmentu berria</span><span class="sxs-lookup"><span data-stu-id="2f894-108">Create a new segment</span></span>

<span data-ttu-id="2f894-109">Segmentu berri bat sortzeko hainbat modu daude:</span><span class="sxs-lookup"><span data-stu-id="2f894-109">There are multiple ways to create a new segment:</span></span> 

- <span data-ttu-id="2f894-110">Segmentu konplexua segmentu eraikitzailearekin: [Segmentu hutsa](segment-builder.md#create-a-new-segment)</span><span class="sxs-lookup"><span data-stu-id="2f894-110">Complex segment with segment builder: [Blank segment](segment-builder.md#create-a-new-segment)</span></span>
- <span data-ttu-id="2f894-111">Operadore bakarreko segmentu sinpleak: [Segmentu azkarra](segment-builder.md#quick-segments)</span><span class="sxs-lookup"><span data-stu-id="2f894-111">Simple segments with one operator: [Quick segment](segment-builder.md#quick-segments)</span></span>
- <span data-ttu-id="2f894-112">AI-ren bidezko bezeroak antzeko bezeroak aurkitzeko modua: [Bezero antzekoak](find-similar-customer-segments.md)</span><span class="sxs-lookup"><span data-stu-id="2f894-112">AI-powered way to find similar customers: [Similar Customers](find-similar-customer-segments.md)</span></span>
- <span data-ttu-id="2f894-113">AI-k oinarritutako iradokizunak neurri edo atributuetan oinarrituta: [Neurriak hobetzeko iradokitako segmentuak](suggested-segments.md)</span><span class="sxs-lookup"><span data-stu-id="2f894-113">AI-powered suggestions based on measures or attributes: [Suggested segments to improve measures](suggested-segments.md)</span></span>
- <span data-ttu-id="2f894-114">Jardueretan oinarritutako iradokizunak: [Iradokitako segmentuak bezeroen jardueran oinarrituta](suggested-segments-activity.md)</span><span class="sxs-lookup"><span data-stu-id="2f894-114">Suggestions based on activities: [Suggested segments based on customer activity](suggested-segments-activity.md)</span></span>

## <a name="manage-existing-segments"></a><span data-ttu-id="2f894-115">Kudeatu lehendik dauden segmentuak</span><span class="sxs-lookup"><span data-stu-id="2f894-115">Manage existing segments</span></span>

<span data-ttu-id="2f894-116">Joan **Segmentuak** orrian, gordetako segmentu guztiak ikusi eta kudeatzeko.</span><span class="sxs-lookup"><span data-stu-id="2f894-116">Go to the **Segments** page, to view all your saved segments and manage them.</span></span>

<span data-ttu-id="2f894-117">Segmentu bakoitza segmentuari buruzko informazio osagarria biltzen duen errenkada batez irudikatuta dago.</span><span class="sxs-lookup"><span data-stu-id="2f894-117">Each segment is represented by a row that includes additional information about the segment.</span></span>

:::image type="content" source="media/segments-selected-segment.png" alt-text="Aukeratutako segmentua aukeren goitibeherako zerrendarekin eta eskuragarri dauden aukerekin.":::

<span data-ttu-id="2f894-119">Segmentu bat hautatzean ekintza hauek erabilgarri daude:</span><span class="sxs-lookup"><span data-stu-id="2f894-119">The following action are available when you select a segment:</span></span>

- <span data-ttu-id="2f894-120">**ikusi** segmentuko xehetasunak, kideen zenbaketa joera segmentuko kideen aurrebista barne.</span><span class="sxs-lookup"><span data-stu-id="2f894-120">**View** the segment details, including member count trend a preview of segment members.</span></span>
- <span data-ttu-id="2f894-121">**Editatu** segmentuak bere propietateak aldatzeko.</span><span class="sxs-lookup"><span data-stu-id="2f894-121">**Edit** the segment to change its properties.</span></span>
- <span data-ttu-id="2f894-122">**Sortu bikoiztuak** segmentu baten.</span><span class="sxs-lookup"><span data-stu-id="2f894-122">**Create duplicate** of a segment.</span></span> <span data-ttu-id="2f894-123">Bere propietateak berehala editatzea edo bikoiztua gordetzea aukeratu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="2f894-123">You can choose to edit its properties right away or simply save the duplicate.</span></span>
- <span data-ttu-id="2f894-124">**Freskatu** segmentuak azken datuak sartuko ditu.</span><span class="sxs-lookup"><span data-stu-id="2f894-124">**Refresh** the segment to include the latest data.</span></span>
- <span data-ttu-id="2f894-125">**Aktibatu** edo **Desaktibatu** segmentua.</span><span class="sxs-lookup"><span data-stu-id="2f894-125">**Activate** or **Deactivate** the segment.</span></span> <span data-ttu-id="2f894-126">Segmentuek bi egoera posible dituzte: aktiboak edo inaktiboak.</span><span class="sxs-lookup"><span data-stu-id="2f894-126">Segments have two possible states - active or inactive.</span></span> <span data-ttu-id="2f894-127">Egoera hauek oso ondo etortzen dira segmentu bat editatzerakoan.</span><span class="sxs-lookup"><span data-stu-id="2f894-127">These states come in handy when editing a segment.</span></span> <span data-ttu-id="2f894-128">Segmentu inaktiboetan, segmentuaren definizioa badago, baina oraindik ez du bezeroik.</span><span class="sxs-lookup"><span data-stu-id="2f894-128">For inactive segments, the segment definition exists but it doesn't contain any customers yet.</span></span> <span data-ttu-id="2f894-129">Segmentu bat aktibatzean, egoera "inaktibo" izatetik "aktibo" izatera pasatzen da eta segmentuaren definizioarekin bat datozen bezeroak bilatzen hasiko da.</span><span class="sxs-lookup"><span data-stu-id="2f894-129">When you activate a segment, its state changes from 'inactive' to 'active" and it starts looking for customers that match the segment definition.</span></span> <span data-ttu-id="2f894-130">A bada [freskatze programatua](system.md#schedule-tab) konfiguratuta dago, segmentu inaktiboek dute **Egoera** gisa zerrendatuta **Saltatuta**, freskatzen saiatu ere ez zela egin adieraziz.</span><span class="sxs-lookup"><span data-stu-id="2f894-130">If a [scheduled refresh](system.md#schedule-tab) is configured, inactive segments have the **Status** listed as **Skipped**, indicating that a refresh wasn't even attempted.</span></span> <span data-ttu-id="2f894-131">Segmentu inaktiboa aktibatzen denean, freskatu egingo da eta programatutako freskapenetan sartuko da.</span><span class="sxs-lookup"><span data-stu-id="2f894-131">When an inactive segment is activated, it will refresh and will be included in scheduled refreshes.</span></span>
  <span data-ttu-id="2f894-132">Bestela, erabil dezakezu **Ordutegiak beranduago** funtzionaltasuna **Aktibatu / Desaktibatu** goitibehera, segmentu jakin bat aktibatzeko eta desaktibatzeko etorkizuneko data eta ordua zehazteko.</span><span class="sxs-lookup"><span data-stu-id="2f894-132">Alternatively, you can use the **Schedule later** functionality in the **Activate/Deactivate** dropdown to specify a future date and time for activation and deactivation of a particular segment.</span></span>
- <span data-ttu-id="2f894-133">**Aldatu izena** segmentuari.</span><span class="sxs-lookup"><span data-stu-id="2f894-133">**Rename** the segment.</span></span>
- <span data-ttu-id="2f894-134">**Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.</span><span class="sxs-lookup"><span data-stu-id="2f894-134">**Download** the list of members as a .CSV file.</span></span>
- <span data-ttu-id="2f894-135">**Kudeatu esportazioak** esportazioekin lotutako segmentua ikusteko eta kudeatzeko.</span><span class="sxs-lookup"><span data-stu-id="2f894-135">**Manage exports** to see exports related segment and manage them.</span></span> [<span data-ttu-id="2f894-136">Lortu esportazioei buruzko informazio gehiago.</span><span class="sxs-lookup"><span data-stu-id="2f894-136">Learn more about exports.</span></span>](export-destinations.md)
- <span data-ttu-id="2f894-137">**Ezabatu** segmentua.</span><span class="sxs-lookup"><span data-stu-id="2f894-137">**Delete** the segment.</span></span>

## <a name="refresh-segments"></a><span data-ttu-id="2f894-138">Freskatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="2f894-138">Refresh segments</span></span>

<span data-ttu-id="2f894-139">Segmentu guztiak freskatu ditzakezu aldi berean hautatuta **Freskatu guztiak** gainean **segmentuak** orrialdea edo segmentu bat edo gehiago freskatu ditzakezu hautatzen dituzunean eta aukeratutakoan **Freskatu** aukeren artean.</span><span class="sxs-lookup"><span data-stu-id="2f894-139">You can refresh all segments at once by selecting **Refresh all** on the **Segments** page or you can refresh one or multiple segments when you select them and choose **Refresh** in from the options.</span></span> <span data-ttu-id="2f894-140">Bestela, berriztagarria den aldizka konfigura dezakezu **administratzailea** > **Sistema** > **Ordutegiak**.</span><span class="sxs-lookup"><span data-stu-id="2f894-140">Alternatively, you can configure a recurring refresh on **Admin** > **System** > **Schedule**.</span></span>

> [!TIP]
> <span data-ttu-id="2f894-141">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="2f894-141">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="2f894-142">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="2f894-142">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="2f894-143">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="2f894-143">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="2f894-144">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="2f894-144">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="export-segments"></a><span data-ttu-id="2f894-145">Esportatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="2f894-145">Export segments</span></span>

<span data-ttu-id="2f894-146">Segmentu bat esportatu dezakezu segmentuen orrialdetik edo [esportazioen orritik](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="2f894-146">You can export a segment from the segments page or the [exports page](export-destinations.md).</span></span> 

1. <span data-ttu-id="2f894-147">Zoaz **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="2f894-147">Go to the **Segments** page.</span></span>

1. <span data-ttu-id="2f894-148">Esportatu nahi duzun segmenturako, hautatu **erakutsi gehiago [...]**.</span><span class="sxs-lookup"><span data-stu-id="2f894-148">Select **Show more [...]** for the segment you want to export.</span></span>

1. <span data-ttu-id="2f894-149">Goitibeherako zerrendatik, hautatu **kudeatu esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="2f894-149">Select **Manage exports** from the actions drop-down list.</span></span>

1. <span data-ttu-id="2f894-150">**Segmentuaren esportazioak (aurrebista)** orria irekitzen da.</span><span class="sxs-lookup"><span data-stu-id="2f894-150">The page **Exports (preview) for segment** opens.</span></span> <span data-ttu-id="2f894-151">Uneko segmentua duten edo ez duten esportazioen arabera taldekatutako konfiguratutako esportazio guztiak ikus ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="2f894-151">You can see all configured exports grouped by by exports that contain the current segment or don't contain it.</span></span>

   1. <span data-ttu-id="2f894-152">Aukeratutako segmentua esportazio batera gehitzeko, hautatu esportazioa zerrendan eta hautatu **Gehitu segmentua**.</span><span class="sxs-lookup"><span data-stu-id="2f894-152">To add the selected segment to an export, select the export in the list and select **Add segment**.</span></span>

   1. <span data-ttu-id="2f894-153">Aukeratutako segmentuarekin esportazio berri bat sortzeko, hautatu **Gehitu esportazioa**.</span><span class="sxs-lookup"><span data-stu-id="2f894-153">To create a new export with the selected segment, select **Add export**.</span></span> <span data-ttu-id="2f894-154">Esportazioak sortzeari buruzko informazio gehiago lortzeko, ikusi [Konfiguratu esportazio berria](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="2f894-154">For more information about creating exports, see [Set up a new export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="2f894-155">Aukeratu **Itzuli** segmentuen orri nagusira itzultzeko.</span><span class="sxs-lookup"><span data-stu-id="2f894-155">Select **Back** to return to the main page for segments.</span></span>

## <a name="view-processing-history-and-segment-members"></a><span data-ttu-id="2f894-156">Ikusi prozesaketaren historia eta segmentuko kideak</span><span class="sxs-lookup"><span data-stu-id="2f894-156">View processing history and segment members</span></span>

<span data-ttu-id="2f894-157">Segurtasun bati buruzko datu bateratuak ikus ditzakezu haren xehetasunak berrikusiz.</span><span class="sxs-lookup"><span data-stu-id="2f894-157">You can see consolidated data about a segment by reviewing its details.</span></span>

<span data-ttu-id="2f894-158">**Segmentuak** orrian, hautatu berrikusi nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="2f894-158">On the **Segments** page, select the segment you want to review.</span></span>

<span data-ttu-id="2f894-159">Orriaren goiko aldean joera grafikoa dago, kideen zenbateko aldaketak bistaratzen dituena.</span><span class="sxs-lookup"><span data-stu-id="2f894-159">The upper part of the page includes a trend graph that visualizes changes in member count.</span></span> <span data-ttu-id="2f894-160">Pasa datuak gainetik kideak data jakin batean ikusteko.</span><span class="sxs-lookup"><span data-stu-id="2f894-160">Hover over data points to see the member count on a specific date.</span></span>

<span data-ttu-id="2f894-161">Bistaratzeko denbora-markoa eguneratu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="2f894-161">You can update the time frame of the visualization.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2f894-162">![Segmentuaren denbora-tartea](media/segment-time-range.png "Segmentuaren denbora-tartea")</span><span class="sxs-lookup"><span data-stu-id="2f894-162">![Segment time range](media/segment-time-range.png "Segment time range")</span></span>

<span data-ttu-id="2f894-163">Beheko aldean segmentuko kideen zerrenda dago.</span><span class="sxs-lookup"><span data-stu-id="2f894-163">The lower part contains a list of the segment members.</span></span>

> [!NOTE]
> <span data-ttu-id="2f894-164">Zerrenda honetan agertzen diren eremuak zure segmentuko entitateen atributuetan oinarrituta daude.</span><span class="sxs-lookup"><span data-stu-id="2f894-164">Fields that appear in this list are based on the attributes of your segment's entities.</span></span>
>
><span data-ttu-id="2f894-165">Zerrenda bat datorren segmentuko kideen aurrebista da eta zure segmentuko lehen 100 erregistroak erakusten ditu, behar bezala baloratu eta haren definizioak berrikusteko.</span><span class="sxs-lookup"><span data-stu-id="2f894-165">The list is a preview of the matching segment members and shows the first 100 records of your segment so that you can quickly evaluate it and review its definitions if needed.</span></span> <span data-ttu-id="2f894-166">Bat datozen erregistro guztiak ikusteko, beharrezkoa da [esportatu segmentua](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="2f894-166">To see all matching records, you need to [export the segment](export-destinations.md).</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)] 
