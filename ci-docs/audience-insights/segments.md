---
title: Sortu eta kudeatu segmentuak
description: Sortu bezeroen segmentuak, hainbat atributuren arabera taldekatzeko.
ms.date: 10/15/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
ms.reviewer: jimsonc
manager: shellyha
ms.openlocfilehash: a1308f07ac3ba7d4b09931bab3d19b6dfaf479ee
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270341"
---
# <a name="create-and-manage-segments"></a><span data-ttu-id="38e03-103">Sortu eta kudeatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="38e03-103">Create and manage segments</span></span>

<span data-ttu-id="38e03-104">Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="38e03-104">Segments let you group your customers based on demographic, transactional, or behavioral attributes.</span></span> <span data-ttu-id="38e03-105">Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-105">You can use segments to target promotional campaigns, sales activities, and customer support actions to achieve your business goals.</span></span>

<span data-ttu-id="38e03-106">Iragazki konplexuak defini ditzakezu Bezero Profilaren entitatearen inguruan eta horiekin lotutako entitateak.</span><span class="sxs-lookup"><span data-stu-id="38e03-106">You can define complex filters around the Customer Profile entity and its related entities.</span></span> <span data-ttu-id="38e03-107">Segmentu bakoitzak, prozesatu ondoren, bezeroen erregistro multzo bat sortzen du eta esportatu eta neurriak hartu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="38e03-107">Each segment, after processing, creates a set of customer records that you can export and take action on.</span></span> <span data-ttu-id="38e03-108">[Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.</span><span class="sxs-lookup"><span data-stu-id="38e03-108">Some [service limits](service-limits.md) apply.</span></span>

<span data-ttu-id="38e03-109">Besterik adierazi ezean, segmentu guztiak **Segmentu dinamikoak** dira, aldizkako antolaketan berritzen direnak.</span><span class="sxs-lookup"><span data-stu-id="38e03-109">Unless stated otherwise, all segments are **Dynamic segments**, which are refreshed on a recurring schedule.</span></span>

<span data-ttu-id="38e03-110">Hurrengo adibideak segmentazio gaitasunaren erabilera ilustratzen du.</span><span class="sxs-lookup"><span data-stu-id="38e03-110">The following example illustrates the segmentation capability.</span></span> <span data-ttu-id="38e03-111">Azken 90 egunetan gutxienez $500 agindu duten bezeroentzako segmentu bat zehaztu dugu *eta* bezeroarentzako arreta-zerbitzu deitu batean parte hartu zutenak eskalatu egin ziren.</span><span class="sxs-lookup"><span data-stu-id="38e03-111">We've defined a segment for customers who ordered at least $500 of goods in the last 90 days *and* who were involved in a customer service call that got escalated.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="38e03-112">![Hainbat talde](media/segmentation-group1-2.png "Hainbat talde")</span><span class="sxs-lookup"><span data-stu-id="38e03-112">![Multiple groups](media/segmentation-group1-2.png "Multiple groups")</span></span>

## <a name="create-a-new-segment"></a><span data-ttu-id="38e03-113">Sortu segmentu berria</span><span class="sxs-lookup"><span data-stu-id="38e03-113">Create a new segment</span></span>

<span data-ttu-id="38e03-114">Segmentuak **Segmentuak** orrian kudeatzen dira.</span><span class="sxs-lookup"><span data-stu-id="38e03-114">Segments are managed on the **Segments** page.</span></span>

1. <span data-ttu-id="38e03-115">Hartzaileen xehetasunetan, joan **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="38e03-115">In audience insights, go to the **Segments** page.</span></span>

2. <span data-ttu-id="38e03-116">Aukeratu **Berria** > **Segmentu zuria**.</span><span class="sxs-lookup"><span data-stu-id="38e03-116">Select **New** > **Blank segment**.</span></span>

3. <span data-ttu-id="38e03-117">Sarbidean **Segmentu berria** hautatu panela, eta aukeratu segmentu mota bat **izena**.</span><span class="sxs-lookup"><span data-stu-id="38e03-117">In the **New segment** pane, choose a segment type and provide a **Name**.</span></span>

   <span data-ttu-id="38e03-118">Aukeran, eman pantailaren izena eta segmentua identifikatzen lagunduko duen deskribapena.</span><span class="sxs-lookup"><span data-stu-id="38e03-118">Optionally, provide a display name, and a description that helps identifying the segment.</span></span>

4. <span data-ttu-id="38e03-119">Aukeratu **hurrengo** etortzeko **Segmentuen eraikitzailea** taldea non definitzen duzun.</span><span class="sxs-lookup"><span data-stu-id="38e03-119">Select **Next** to get to the **Segment builder** page where you define a group.</span></span> <span data-ttu-id="38e03-120">Talde bat bezero multzo bat da.</span><span class="sxs-lookup"><span data-stu-id="38e03-120">A group is a set of customers.</span></span>

5. <span data-ttu-id="38e03-121">Aukeratu segmentatu nahi duzun atributua barne hartzen duen entitatea.</span><span class="sxs-lookup"><span data-stu-id="38e03-121">Choose the entity that includes the attribute you want to segment by.</span></span>

6. <span data-ttu-id="38e03-122">Aukeratu arabera zatitu beharreko atributua.</span><span class="sxs-lookup"><span data-stu-id="38e03-122">Choose the attribute to segment by.</span></span> <span data-ttu-id="38e03-123">Atributu honek lau balio motetako bat izan dezake: zenbakikoa, katea, data edo boolearra.</span><span class="sxs-lookup"><span data-stu-id="38e03-123">This attribute can have one of four value types: numerical, string, date, or Boolean.</span></span>

7. <span data-ttu-id="38e03-124">Aukeratu operadorea eta balio bat hautatutako atributurako.</span><span class="sxs-lookup"><span data-stu-id="38e03-124">Choose an operator and a value for the selected attribute.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="38e03-125">![Pertsonalizatu taldeko iragazkia](media/customer-group-numbers.png "Bezeroaren taldeko iragazkia")</span><span class="sxs-lookup"><span data-stu-id="38e03-125">![Custom group filter](media/customer-group-numbers.png "Customer group filter")</span></span>

   |<span data-ttu-id="38e03-126">Zenbakia</span><span class="sxs-lookup"><span data-stu-id="38e03-126">Number</span></span> |<span data-ttu-id="38e03-127">Definizioa</span><span class="sxs-lookup"><span data-stu-id="38e03-127">Definition</span></span>  |
   |---------|---------|
   |<span data-ttu-id="38e03-128">1</span><span class="sxs-lookup"><span data-stu-id="38e03-128">1</span></span>     |<span data-ttu-id="38e03-129">Entity</span><span class="sxs-lookup"><span data-stu-id="38e03-129">Entity</span></span>          |
   |<span data-ttu-id="38e03-130">2</span><span class="sxs-lookup"><span data-stu-id="38e03-130">2</span></span>     |<span data-ttu-id="38e03-131">Atributua</span><span class="sxs-lookup"><span data-stu-id="38e03-131">Attribute</span></span>          |
   |<span data-ttu-id="38e03-132">3</span><span class="sxs-lookup"><span data-stu-id="38e03-132">3</span></span>    |<span data-ttu-id="38e03-133">Eragilea</span><span class="sxs-lookup"><span data-stu-id="38e03-133">Operator</span></span>         |
   |<span data-ttu-id="38e03-134">4</span><span class="sxs-lookup"><span data-stu-id="38e03-134">4</span></span>    |<span data-ttu-id="38e03-135">Balioa</span><span class="sxs-lookup"><span data-stu-id="38e03-135">Value</span></span>         |

8. <span data-ttu-id="38e03-136">Erakundea bezero bateratutako entitatearekin konektatuta badago [harremanak](relationships.md), erlazio bidea zehaztu behar duzu baliozko segmentua sortzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-136">If the entity is connected to the unified customer entity through [relationships](relationships.md), you need to define the relationship path to create a valid segment.</span></span> <span data-ttu-id="38e03-137">Gehitu entitateak erlazio-bide honetatik hautatu dezakezu arte **Bezeroa: CustomerInsights** entitatea goitibehera.</span><span class="sxs-lookup"><span data-stu-id="38e03-137">Add the entities from the relationship path until you can select the **Customer:CustomerInsights** entity from the dropdown.</span></span> <span data-ttu-id="38e03-138">Ondoren, aukeratu **Erregistro guztiak** baldintza bakoitzerako.</span><span class="sxs-lookup"><span data-stu-id="38e03-138">Then, choose **All records** for each condition.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="38e03-139">![Harreman bidea segmentuak sortzean](media/segments-multiple-relationships.png "Harreman bidea segmentuak sortzean")</span><span class="sxs-lookup"><span data-stu-id="38e03-139">![Relationship path during segment creation](media/segments-multiple-relationships.png "Relationship path during segment creation")</span></span>

9. <span data-ttu-id="38e03-140">Segmentua gordetzeko, sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="38e03-140">Select **Save** to save your segment.</span></span> <span data-ttu-id="38e03-141">Zure segmentua gordeko da eta prozesatu egingo da baldintza guztiak baliozkotuz gero.</span><span class="sxs-lookup"><span data-stu-id="38e03-141">Your segment will be saved and processed if all requirements are validated.</span></span> <span data-ttu-id="38e03-142">Bestela, zirriborro gisa gordeko da.</span><span class="sxs-lookup"><span data-stu-id="38e03-142">Otherwise, it will be saved as a draft.</span></span>

10. <span data-ttu-id="38e03-143">Aukeratu **Segurtasunetara itzuli** berriro ere **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="38e03-143">Select **Back to segments** to go back to the **Segments** page.</span></span>

## <a name="manage-existing-segments"></a><span data-ttu-id="38e03-144">Kudeatu lehendik dauden segmentuak</span><span class="sxs-lookup"><span data-stu-id="38e03-144">Manage existing segments</span></span>

<span data-ttu-id="38e03-145">Gainean **segmentuak** orrialdean, gordetako segmentu guztiak ikusi eta kudeatu ahal izango dituzu.</span><span class="sxs-lookup"><span data-stu-id="38e03-145">On the **Segments** page, you can view all your saved segments and manage them.</span></span>

<span data-ttu-id="38e03-146">Segmentu bakoitza segmentuari buruzko informazio osagarria biltzen duen errenkada batez irudikatuta dago.</span><span class="sxs-lookup"><span data-stu-id="38e03-146">Each segment is represented by a row that includes additional information about the segment.</span></span>

<span data-ttu-id="38e03-147">Zutabeak segmentu bat ordenatu dezakezu zutabearen goiburua hautatuta.</span><span class="sxs-lookup"><span data-stu-id="38e03-147">You can sort the segments in a column by selecting the column heading.</span></span>

<span data-ttu-id="38e03-148">Erabili **Bilatu** goiko eskuineko izkinan segmentuak iragazteko kutxa.</span><span class="sxs-lookup"><span data-stu-id="38e03-148">Use the **Search** box in the top-right corner to filter the segments.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="38e03-149">![Aukerak lehendik dagoen segmentu bat kudeatzeko](media/segments-selected-segment.png "Aukerak lehendik dagoen segmentu bat kudeatzeko")</span><span class="sxs-lookup"><span data-stu-id="38e03-149">![Options to manage an existing segment](media/segments-selected-segment.png "Options to manage an existing segment")</span></span>

<span data-ttu-id="38e03-150">Segmentu bat hautatzean ekintza hauek erabilgarri daude:</span><span class="sxs-lookup"><span data-stu-id="38e03-150">The following action are available when you select a segment:</span></span>

- <span data-ttu-id="38e03-151">**ikusi** segmentuko xehetasunak, kideen zenbaketa joera segmentuko kideen aurrebista barne.</span><span class="sxs-lookup"><span data-stu-id="38e03-151">**View** the segment details, including member count trend a preview of segment members.</span></span>
- <span data-ttu-id="38e03-152">**Editatu** segmentuak bere propietateak aldatzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-152">**Edit** the segment to change its properties.</span></span>
- <span data-ttu-id="38e03-153">**Freskatu** segmentuak azken datuak sartuko ditu.</span><span class="sxs-lookup"><span data-stu-id="38e03-153">**Refresh** the segment to include the latest data.</span></span>
- <span data-ttu-id="38e03-154">**Aktibatu** edo **Desaktibatu** segmentua.</span><span class="sxs-lookup"><span data-stu-id="38e03-154">**Activate** or **Deactivate** the segment.</span></span> <span data-ttu-id="38e03-155">Segmentuek bi egoera posible dituzte: aktiboak edo inaktiboak.</span><span class="sxs-lookup"><span data-stu-id="38e03-155">Segments have two possible states - active or inactive.</span></span> <span data-ttu-id="38e03-156">Egoera hauek oso ondo etortzen dira segmentu bat editatzerakoan.</span><span class="sxs-lookup"><span data-stu-id="38e03-156">These states come in handy when editing a segment.</span></span> <span data-ttu-id="38e03-157">Segmentu inaktiboetan, segmentuaren definizioa badago, baina oraindik ez du bezeroik.</span><span class="sxs-lookup"><span data-stu-id="38e03-157">For inactive segments, the segment definition exists but it doesn't contain any customers yet.</span></span> <span data-ttu-id="38e03-158">Segmentu bat aktibatzean, egoera "inaktibo" izatetik "aktibo" izatera pasatzen da eta segmentuaren definizioarekin bat datozen bezeroak bilatzen hasiko da.</span><span class="sxs-lookup"><span data-stu-id="38e03-158">When you activate a segment, its state changes from 'inactive' to 'active" and it starts looking for customers that match the segment definition.</span></span> <span data-ttu-id="38e03-159">A bada [freskatze programatua](system.md#schedule-tab) konfiguratuta dago, segmentu inaktiboek dute **Egoera** gisa zerrendatuta **Saltatuta**, freskatzen saiatu ere ez zela egin adieraziz.</span><span class="sxs-lookup"><span data-stu-id="38e03-159">If a [scheduled refresh](system.md#schedule-tab) is configured, inactive segments have the **Status** listed as **Skipped**, indicating that a refresh wasn't even attempted.</span></span> <span data-ttu-id="38e03-160">Segmentu inaktiboa aktibatzen denean, freskatu egingo da eta programatutako freskapenetan sartuko da.</span><span class="sxs-lookup"><span data-stu-id="38e03-160">When an inactive segment is activated, it will refresh and will be included in scheduled refreshes.</span></span>
  <span data-ttu-id="38e03-161">Bestela, erabil dezakezu **Ordutegiak beranduago** funtzionaltasuna **Aktibatu / Desaktibatu** goitibehera, segmentu jakin bat aktibatzeko eta desaktibatzeko etorkizuneko data eta ordua zehazteko.</span><span class="sxs-lookup"><span data-stu-id="38e03-161">Alternatively, you can use the **Schedule later** functionality in the **Activate/Deactivate** dropdown to specify a future date and time for activation and deactivation of a particular segment.</span></span>
- <span data-ttu-id="38e03-162">**Aldatu izena** segmentuari.</span><span class="sxs-lookup"><span data-stu-id="38e03-162">**Rename** the segment.</span></span>
- <span data-ttu-id="38e03-163">**Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.</span><span class="sxs-lookup"><span data-stu-id="38e03-163">**Download** the list of members as a .CSV file.</span></span>
- <span data-ttu-id="38e03-164">**Gehitu** aukerak segmentuan dauden bezeroen IDen zerrenda bidaltzen du beste aplikazio batean prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-164">**Add to** option sends the list of customer IDs in the segment for processing in another application.</span></span>
- <span data-ttu-id="38e03-165">**Ezabatu** segmentua.</span><span class="sxs-lookup"><span data-stu-id="38e03-165">**Delete** the segment.</span></span>

## <a name="refresh-segments"></a><span data-ttu-id="38e03-166">Freskatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="38e03-166">Refresh segments</span></span>

<span data-ttu-id="38e03-167">Segmentu guztiak freskatu ditzakezu aldi berean hautatuta **Freskatu guztiak** gainean **segmentuak** orrialdea edo segmentu bat edo gehiago freskatu ditzakezu hautatzen dituzunean eta aukeratutakoan **Freskatu** aukeren artean.</span><span class="sxs-lookup"><span data-stu-id="38e03-167">You can refresh all segments at once by selecting **Refresh all** on the **Segments** page or you can refresh one or multiple segments when you select them and choose **Refresh** in from the options.</span></span> <span data-ttu-id="38e03-168">Bestela, berriztagarria den aldizka konfigura dezakezu **administratzailea** > **Sistema** > **Ordutegiak**.</span><span class="sxs-lookup"><span data-stu-id="38e03-168">Alternatively, you can configure a recurring refresh on **Admin** > **System** > **Schedule**.</span></span>

> [!TIP]
> <span data-ttu-id="38e03-169">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="38e03-169">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="38e03-170">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="38e03-170">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="38e03-171">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="38e03-171">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="38e03-172">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="38e03-172">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="download-and-export-segments"></a><span data-ttu-id="38e03-173">Deskargatu eta esportatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="38e03-173">Download and export segments</span></span>

<span data-ttu-id="38e03-174">Zure segmentuak CSV fitxategi batera deskarga ditzakezu edo Dynamics 365 Sales-era esportatu.</span><span class="sxs-lookup"><span data-stu-id="38e03-174">You can download your segments to a CSV file or export them to Dynamics 365 Sales.</span></span>

### <a name="download-segments-to-a-csv-file"></a><span data-ttu-id="38e03-175">Deskargatu segmentuak CSV fitxategi batera</span><span class="sxs-lookup"><span data-stu-id="38e03-175">Download segments to a CSV file</span></span>

1. <span data-ttu-id="38e03-176">Hartzaileen xehetasunetan, joan **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="38e03-176">In audience insights, go to the **Segments** page.</span></span>

2. <span data-ttu-id="38e03-177">Hautatu elipsia segmentu jakin bateko fitxan.</span><span class="sxs-lookup"><span data-stu-id="38e03-177">Select the ellipsis in a specific segment's tile.</span></span>

3. <span data-ttu-id="38e03-178">Aukeratu **Deskargatu CSV gisa** ekintzen goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="38e03-178">Select **Download as CSV** from the actions drop-down list.</span></span>

### <a name="export-segments-to-dynamics-365-sales"></a><span data-ttu-id="38e03-179">Esportatu segmentuak Dynamics 365 Sales-era</span><span class="sxs-lookup"><span data-stu-id="38e03-179">Export segments to Dynamics 365 Sales</span></span>

<span data-ttu-id="38e03-180">Dynamics 365 Sales-en segmentuak esportatu aurretik, administratzaile bat behar da [sortu esportazio-helmuga](export-destinations.md) Dynamics 365 Sales-erako.</span><span class="sxs-lookup"><span data-stu-id="38e03-180">Before exporting segments to Dynamics 365 Sales, an admin needs to [create the export destination](export-destinations.md) for Dynamics 365 Sales.</span></span>

1. <span data-ttu-id="38e03-181">Hartzaileen xehetasunetan, joan **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="38e03-181">In audience insights, go to the **Segments** page.</span></span>

2. <span data-ttu-id="38e03-182">Hautatu elipsia segmentu jakin bateko fitxan.</span><span class="sxs-lookup"><span data-stu-id="38e03-182">Select the ellipsis in a specific segment's tile.</span></span>

3. <span data-ttu-id="38e03-183">Aukeratu **Gehitu** ekintzen goitibeherako zerrendatik eta hautatu datuak bidali nahi dituzun esportazio helmuga.</span><span class="sxs-lookup"><span data-stu-id="38e03-183">Select **Add to** from the actions drop-down list and select the export destination you want to send the data to.</span></span>

## <a name="draft-mode-for-segments"></a><span data-ttu-id="38e03-184">Zirriborroen modua segmentuetarako</span><span class="sxs-lookup"><span data-stu-id="38e03-184">Draft mode for segments</span></span>

<span data-ttu-id="38e03-185">Segmentu bat prozesatzeko baldintza guztiak betetzen ez badira, segmentua zirriborro gisa gorde dezakezu eta sar itzazu **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="38e03-185">If not all requirements to process a segment are met, you can save the segment as a draft and access it from the **Segments** page.</span></span>

<span data-ttu-id="38e03-186">Segmentu aktibo gisa gordeko da eta ezin da aktibatu baliozkoa izan arte.</span><span class="sxs-lookup"><span data-stu-id="38e03-186">It will be saved as an inactive segment, and can't be activated it until it's valid.</span></span>

## <a name="add-more-conditions-to-a-group"></a><span data-ttu-id="38e03-187">Gehitu baldintza gehiago taldeari</span><span class="sxs-lookup"><span data-stu-id="38e03-187">Add more conditions to a group</span></span>

<span data-ttu-id="38e03-188">Talde bati baldintza gehiago gehitzeko, bi operadore logiko erabil ditzakezu:</span><span class="sxs-lookup"><span data-stu-id="38e03-188">To add more conditions to a group, you can use two logical operators:</span></span>

- <span data-ttu-id="38e03-189">**ETA** operadorea: Bi baldintza segmentazio prozesuaren baitan bete behar dira.</span><span class="sxs-lookup"><span data-stu-id="38e03-189">**AND** operator: Both conditions must be met as part of the segmentation process.</span></span> <span data-ttu-id="38e03-190">Aukera hau baliagarria da entitate desberdinetan baldintzak definitzen dituzunean.</span><span class="sxs-lookup"><span data-stu-id="38e03-190">This option is most useful when you define conditions across different entities.</span></span>

- <span data-ttu-id="38e03-191">**EDO** operadorea: Baldintzaren bat segmentazio prozesuaren zati gisa bete behar da.</span><span class="sxs-lookup"><span data-stu-id="38e03-191">**OR** operator: Either one of the conditions needs to be met as part of the segmentation process.</span></span> <span data-ttu-id="38e03-192">Aukera hau oso baliagarria da hainbat baldintza definitzen dituzunean entitate berarentzat.</span><span class="sxs-lookup"><span data-stu-id="38e03-192">This option is most useful when you define multiple conditions for the same entity.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="38e03-193">![EDO baldintza bat bete behar den operadorea](media/segmentation-either-condition.png "EDO baldintza bat bete behar den operadorea")</span><span class="sxs-lookup"><span data-stu-id="38e03-193">![OR operator where either condition needs to be met](media/segmentation-either-condition.png "OR operator where either condition needs to be met")</span></span>

<span data-ttu-id="38e03-194">Gaur egun, habia habia egin daiteke **EDO** operadorea **ETA** operadorea, baina ez alderantziz.</span><span class="sxs-lookup"><span data-stu-id="38e03-194">It's currently possible to nest an **OR** operator under an **AND** operator, but not the other way around.</span></span>

## <a name="combine-multiple-groups"></a><span data-ttu-id="38e03-195">Konbinatu hainbat talde</span><span class="sxs-lookup"><span data-stu-id="38e03-195">Combine multiple groups</span></span>

<span data-ttu-id="38e03-196">Talde bakoitzak bezero multzo zehatz bat sortzen du.</span><span class="sxs-lookup"><span data-stu-id="38e03-196">Each group produces a specific set of customers.</span></span> <span data-ttu-id="38e03-197">Talde horiek konbinatu ditzakezu zure negoziorako behar diren bezeroak sartzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-197">You can combine these groups to include the customers required for your business case.</span></span>

1. <span data-ttu-id="38e03-198">Hartzaileen xehetasunetan, joan hona: **Segmentuak** orrira eta hautatu segmentu bat.</span><span class="sxs-lookup"><span data-stu-id="38e03-198">In audience insights, go to the **Segments** page and select a segment.</span></span>

2. <span data-ttu-id="38e03-199">Hautatu **Gehitu taldea**.</span><span class="sxs-lookup"><span data-stu-id="38e03-199">Select **Add Group**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="38e03-200">![Bezeroen taldea gehitzeko taldea](media/customer-group-add-group.png "Bezeroen taldea gehitzeko taldea")</span><span class="sxs-lookup"><span data-stu-id="38e03-200">![Customer group add group](media/customer-group-add-group.png "Customer group add group")</span></span>

3. <span data-ttu-id="38e03-201">Hautatu multzo multzo hauetako eragileetako bat: **Batura**, **Gurutzatu**, edo **Salbu**.</span><span class="sxs-lookup"><span data-stu-id="38e03-201">Select one of the following set operators: **Union**, **Intersect**, or **Except**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="38e03-202">![Bezeroen taldea gehitzeko bateratzea](media/customer-group-union.png "Bezeroen taldea gehitzeko bateratzea")</span><span class="sxs-lookup"><span data-stu-id="38e03-202">![Customer group add union](media/customer-group-union.png "Customer group add union")</span></span>

   <span data-ttu-id="38e03-203">Hautatu multzo operatiboa talde berria definitzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-203">Select a set operator to define a new group.</span></span> <span data-ttu-id="38e03-204">Gorde talde desberdinak, zer datu mantentzen diren zehazteko:</span><span class="sxs-lookup"><span data-stu-id="38e03-204">Save different groups to determine what data gets retained:</span></span>

   - <span data-ttu-id="38e03-205">**Bateratzea** bi taldeak batzen ditu.</span><span class="sxs-lookup"><span data-stu-id="38e03-205">**Union** unites the two groups.</span></span>

   - <span data-ttu-id="38e03-206">**Gurutzatu** bi taldeak gainjartzen ditu.</span><span class="sxs-lookup"><span data-stu-id="38e03-206">**Intersect** overlaps the two groups.</span></span> <span data-ttu-id="38e03-207">Bi taldeetako datu *komunak* soilik mantentzen dira talde bateratuan.</span><span class="sxs-lookup"><span data-stu-id="38e03-207">Only data that *is common* to both groups is retained in the unified group.</span></span>

   - <span data-ttu-id="38e03-208">**Salbuespena** bi taldeak batzen ditu.</span><span class="sxs-lookup"><span data-stu-id="38e03-208">**Except** combines the two groups.</span></span> <span data-ttu-id="38e03-209">A eta B talde bietan *ez dauden* datuak soilik mantentzen dira.</span><span class="sxs-lookup"><span data-stu-id="38e03-209">Only data in group A that *is not common* to data in group B is retained.</span></span>

## <a name="view-processing-history-and-segment-members"></a><span data-ttu-id="38e03-210">Ikusi prozesaketaren historia eta segmentuko kideak</span><span class="sxs-lookup"><span data-stu-id="38e03-210">View processing history and segment members</span></span>

<span data-ttu-id="38e03-211">Segurtasun bati buruzko datu bateratuak ikus ditzakezu haren xehetasunak berrikusiz.</span><span class="sxs-lookup"><span data-stu-id="38e03-211">You can see consolidated data about a segment by reviewing its details.</span></span>

<span data-ttu-id="38e03-212">**Segmentuak** orrian, hautatu berrikusi nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="38e03-212">On the **Segments** page, select the segment you want to review.</span></span>

<span data-ttu-id="38e03-213">Orriaren goiko aldean joera grafikoa dago, kideen zenbateko aldaketak bistaratzen dituena.</span><span class="sxs-lookup"><span data-stu-id="38e03-213">The upper part of the page includes a trend graph that visualizes changes in member count.</span></span> <span data-ttu-id="38e03-214">Pasa datuak gainetik kideak data jakin batean ikusteko.</span><span class="sxs-lookup"><span data-stu-id="38e03-214">Hover over data points to see the member count on a specific date.</span></span>

<span data-ttu-id="38e03-215">Bistaratzeko denbora-markoa eguneratu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="38e03-215">You can update the time frame of the visualization.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="38e03-216">![Segmentuaren denbora-tartea](media/segment-time-range.png "Segmentuaren denbora-tartea")</span><span class="sxs-lookup"><span data-stu-id="38e03-216">![Segment time range](media/segment-time-range.png "Segment time range")</span></span>

<span data-ttu-id="38e03-217">Beheko aldean segmentuko kideen zerrenda dago.</span><span class="sxs-lookup"><span data-stu-id="38e03-217">The lower part contains a list of the segment members.</span></span>

> [!NOTE]
> <span data-ttu-id="38e03-218">Zerrenda honetan agertzen diren eremuak zure segmentuko entitateen atributuetan oinarrituta daude.</span><span class="sxs-lookup"><span data-stu-id="38e03-218">Fields that appear in this list are based on the attributes of your segment's entities.</span></span>
>
><span data-ttu-id="38e03-219">Zerrenda bat datorren segmentuko kideen aurrebista da eta zure segmentuko lehen 100 erregistroak erakusten ditu, behar bezala baloratu eta haren definizioak berrikusteko.</span><span class="sxs-lookup"><span data-stu-id="38e03-219">The list is a preview of the matching segment members and shows the first 100 records of your segment so that you can quickly evaluate it and review its definitions if needed.</span></span> <span data-ttu-id="38e03-220">Bat datozen erregistro guztiak ikusteko, beharrezkoa da [esportatu segmentua](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="38e03-220">To see all matching records, you need to [export the segment](export-destinations.md).</span></span>

## <a name="quick-segments"></a><span data-ttu-id="38e03-221">Segmentu azkarrak</span><span class="sxs-lookup"><span data-stu-id="38e03-221">Quick segments</span></span>

<span data-ttu-id="38e03-222">Segmentu-egileaz gain, segmentuak sortzeko beste bide bat dago.</span><span class="sxs-lookup"><span data-stu-id="38e03-222">In addition to the segment builder, there's another path for creating segments.</span></span> <span data-ttu-id="38e03-223">Segmentu azkarrek segmentu errazak (operadore bakarrarekin) eraiki eta berehala eskaintzen dizute.</span><span class="sxs-lookup"><span data-stu-id="38e03-223">Quick segments let you build simple segments with a single operator quickly and with instant insights.</span></span>

1. <span data-ttu-id="38e03-224">Gainean **segmentuak** orria, hautatu **Berria** > **Sortu azkar**.</span><span class="sxs-lookup"><span data-stu-id="38e03-224">On the **Segments** page, select **New** > **Quickly create from**.</span></span>

   - <span data-ttu-id="38e03-225">Hautatu botoia **profilak** Aukeratutako bezeroaren entitatean oinarritutako segmentu bat eraikitzeko aukera.</span><span class="sxs-lookup"><span data-stu-id="38e03-225">Select the **Profiles** option to build a segment that is based on the unified Customer entity.</span></span>
   - <span data-ttu-id="38e03-226">Hautatu botoia **Neurriak** Aukera hau aurrez sortu dituzun bezeroarentzako atributu mota bakoitzaren inguruan segmentu bat eraikitzeko **Neurriak** orria.</span><span class="sxs-lookup"><span data-stu-id="38e03-226">Select the **Measures** option to build a segment around each of the Customer Attribute type of measures you have previously created on the **Measures** page.</span></span>
   - <span data-ttu-id="38e03-227">Hautatu botoia **Adimen** Aukera hau bai erabiliz sortu duzun irteerako entitateetako baten inguruan eraikitzeko aukera **iragarpenak** edo **Neurrira egindako ereduak** gaitasunak.</span><span class="sxs-lookup"><span data-stu-id="38e03-227">Select the **Intelligence** option to build a segment around one of the output entities you generated using either the **Predictions** or **Custom Models** capabilities.</span></span>

2. <span data-ttu-id="38e03-228">Sarbidean **Segmentu azkar berria** elkarrizketa-koadroan, hautatu atributu bat **eremua** goitibeherako menuko.</span><span class="sxs-lookup"><span data-stu-id="38e03-228">In the **New quick segment** dialog box, select an attribute from the **Field** dropdown.</span></span>

3. <span data-ttu-id="38e03-229">Sistemak ikuspegi osagarriak emango ditu zure bezeroen segmentu hobeak sortzen lagunduko dutenak.</span><span class="sxs-lookup"><span data-stu-id="38e03-229">The system will provide some additional insights that help you create better segments of your customers.</span></span>
   - <span data-ttu-id="38e03-230">Eremu kategorikoetarako, 10 bezero zenbatuko ditugu.</span><span class="sxs-lookup"><span data-stu-id="38e03-230">For categorical fields, we'll show 10 top customer counts.</span></span> <span data-ttu-id="38e03-231">Hautatu **Balio** bat eta hautatu **Berrikusi**.</span><span class="sxs-lookup"><span data-stu-id="38e03-231">Choose a **Value** and select **Review**.</span></span>

   - <span data-ttu-id="38e03-232">Zenbakizko atributu bat lortzeko, sistemak erakutsiko du zer atributu-balioa eroriko den bezero bakoitzaren portzentalaren azpian.</span><span class="sxs-lookup"><span data-stu-id="38e03-232">For a numerical attribute, the system will show what attribute value falls under each customer's percentile.</span></span> <span data-ttu-id="38e03-233">Aukeratu bat **Operadorea** eta **Balioa** eta hautatu **Berrikusi**.</span><span class="sxs-lookup"><span data-stu-id="38e03-233">Choose an **Operator** and a **Value**, then select **Review**.</span></span>

4. <span data-ttu-id="38e03-234">Sistemak zurekin hornituko zaitu **Segurtasunaren neurria**.</span><span class="sxs-lookup"><span data-stu-id="38e03-234">The system will provide you with an **Estimated segment size**.</span></span> <span data-ttu-id="38e03-235">Definitu duzun segmentua sortu edo aukeratu dezakezu edo, bestela, berrikusi beste segmentu baten tamaina lortzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-235">You can choose whether to generate the segment you've defined, or first revisit it to get a different segment size.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="38e03-236">![Izena eta estimazioa segmentu azkar baterako](media/quick-segment-name.png "Izena eta estimazioa segmentu azkar baterako")</span><span class="sxs-lookup"><span data-stu-id="38e03-236">![Name and estimation for a quick segment](media/quick-segment-name.png "Name and estimation for a quick segment")</span></span>

5. <span data-ttu-id="38e03-237">Jarri **izena** zure segmentuari.</span><span class="sxs-lookup"><span data-stu-id="38e03-237">Provide a **Name** for your segment.</span></span> <span data-ttu-id="38e03-238">Nahi baduzu, eman **Bistaratzeko izena**.</span><span class="sxs-lookup"><span data-stu-id="38e03-238">Optionally, provide a **Display name**.</span></span>

6. <span data-ttu-id="38e03-239">Segmentua sortzeko, sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="38e03-239">Select **Save** to create your segment.</span></span>

7. <span data-ttu-id="38e03-240">Segmentua prozesatu ondoren, sortu duzun beste edozein segmentu bezala ikus dezakezu.</span><span class="sxs-lookup"><span data-stu-id="38e03-240">After the segment has finished processing, you can view it like any other segment you've created.</span></span>

<span data-ttu-id="38e03-241">Hurrengo agertokietarako, gomendatzen dugu segmentu eraikitzailea erabiltzea gomendatutako segmentuen gaitasuna baino:</span><span class="sxs-lookup"><span data-stu-id="38e03-241">For the following scenarios, we advise using the segment builder rather than the recommended segments capability:</span></span>

- <span data-ttu-id="38e03-242">Segurtasunak sortzen iragazkiak eremu kategorietan operadorea ez den beste eremuetan **da** operadorea</span><span class="sxs-lookup"><span data-stu-id="38e03-242">Creating segments with filters on categorical fields where the operator is different than the **Is** operator</span></span>
- <span data-ttu-id="38e03-243">Segmentuak sortu iragazkiak zenbaki-eremuetan, operadorea baino desberdinak direnetan **bitarte honetan**, **Baino handiagoa**, eta **Baino gutxiago** operadore</span><span class="sxs-lookup"><span data-stu-id="38e03-243">Creating segments with filters on numerical fields where the operator is different than the **Between**, **Greater than**, and **Less than** operators</span></span>
- <span data-ttu-id="38e03-244">Data-motako eremuetan iragazkiak dituzten segmentuak sortzen</span><span class="sxs-lookup"><span data-stu-id="38e03-244">Creating segments with filters on date type fields</span></span>

## <a name="next-steps"></a><span data-ttu-id="38e03-245">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="38e03-245">Next steps</span></span>

<span data-ttu-id="38e03-246">[Esportatu segmentua](export-destinations.md) eta esploratu [Bezero txartela](customer-card-add-in.md) eta [Konektoreak](export-power-bi.md) bezeroaren mailari buruzko informazioa lortzeko.</span><span class="sxs-lookup"><span data-stu-id="38e03-246">[Export a segment](export-destinations.md) and explore the [Customer Card](customer-card-add-in.md) and [Connectors](export-power-bi.md) to get insights on the customer level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]