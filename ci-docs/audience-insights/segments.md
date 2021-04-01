---
title: Sortu eta kudeatu segmentuak
description: Sortu bezeroen segmentuak, hainbat atributuren arabera taldekatzeko.
ms.date: 03/02/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 4a6e8a3216a2c0738d60247054afa9fc18412f55
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597036"
---
# <a name="create-and-manage-segments"></a><span data-ttu-id="0624b-103">Sortu eta kudeatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="0624b-103">Create and manage segments</span></span>

<span data-ttu-id="0624b-104">Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="0624b-104">Segments let you group your customers based on demographic, transactional, or behavioral attributes.</span></span> <span data-ttu-id="0624b-105">Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-105">You can use segments to target promotional campaigns, sales activities, and customer support actions to achieve your business goals.</span></span>

<span data-ttu-id="0624b-106">Iragazki konplexuak defini ditzakezu Bezero Profilaren entitatearen inguruan eta horiekin lotutako entitateak.</span><span class="sxs-lookup"><span data-stu-id="0624b-106">You can define complex filters around the Customer Profile entity and its related entities.</span></span> <span data-ttu-id="0624b-107">Segmentu bakoitzak, prozesatu ondoren, bezeroen erregistro multzo bat sortzen du eta esportatu eta neurriak hartu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="0624b-107">Each segment, after processing, creates a set of customer records that you can export and take action on.</span></span> <span data-ttu-id="0624b-108">[Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.</span><span class="sxs-lookup"><span data-stu-id="0624b-108">Some [service limits](service-limits.md) apply.</span></span>

<span data-ttu-id="0624b-109">Besterik adierazi ezean, segmentu guztiak **Segmentu dinamikoak** dira, aldizkako antolaketan berritzen direnak.</span><span class="sxs-lookup"><span data-stu-id="0624b-109">Unless stated otherwise, all segments are **Dynamic segments**, which are refreshed on a recurring schedule.</span></span>

<span data-ttu-id="0624b-110">Hurrengo adibideak segmentazio gaitasunaren erabilera ilustratzen du.</span><span class="sxs-lookup"><span data-stu-id="0624b-110">The following example illustrates the segmentation capability.</span></span> <span data-ttu-id="0624b-111">Azken 90 egunetan gutxienez $500 agindu duten bezeroentzako segmentu bat zehaztu dugu *eta* bezeroarentzako arreta-zerbitzu deitu batean parte hartu zutenak eskalatu egin ziren.</span><span class="sxs-lookup"><span data-stu-id="0624b-111">We've defined a segment for customers who ordered at least $500 of goods in the last 90 days *and* who were involved in a customer service call that got escalated.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0624b-112">![Hainbat talde](media/segmentation-group1-2.png "Hainbat talde")</span><span class="sxs-lookup"><span data-stu-id="0624b-112">![Multiple groups](media/segmentation-group1-2.png "Multiple groups")</span></span>

## <a name="create-a-new-segment"></a><span data-ttu-id="0624b-113">Sortu segmentu berria</span><span class="sxs-lookup"><span data-stu-id="0624b-113">Create a new segment</span></span>

<span data-ttu-id="0624b-114">Segmentuak **Segmentuak** orrian kudeatzen dira.</span><span class="sxs-lookup"><span data-stu-id="0624b-114">Segments are managed on the **Segments** page.</span></span>

1. <span data-ttu-id="0624b-115">Hartzaileen xehetasunetan, joan **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="0624b-115">In audience insights, go to the **Segments** page.</span></span>

1. <span data-ttu-id="0624b-116">Aukeratu **Berria** > **Segmentu zuria**.</span><span class="sxs-lookup"><span data-stu-id="0624b-116">Select **New** > **Blank segment**.</span></span>

1. <span data-ttu-id="0624b-117">Sarbidean **Segmentu berria** hautatu panela, eta aukeratu segmentu mota bat **izena**.</span><span class="sxs-lookup"><span data-stu-id="0624b-117">In the **New segment** pane, choose a segment type and provide a **Name**.</span></span>

   <span data-ttu-id="0624b-118">Aukeran, eman pantailaren izena eta segmentua identifikatzen lagunduko duen deskribapena.</span><span class="sxs-lookup"><span data-stu-id="0624b-118">Optionally, provide a display name, and a description that helps identifying the segment.</span></span>

1. <span data-ttu-id="0624b-119">Aukeratu **hurrengo** etortzeko **Segmentuen eraikitzailea** taldea non definitzen duzun.</span><span class="sxs-lookup"><span data-stu-id="0624b-119">Select **Next** to get to the **Segment builder** page where you define a group.</span></span> <span data-ttu-id="0624b-120">Talde bat bezero multzo bat da.</span><span class="sxs-lookup"><span data-stu-id="0624b-120">A group is a set of customers.</span></span>

1. <span data-ttu-id="0624b-121">Aukeratu segmentatu nahi duzun atributua barne hartzen duen entitatea.</span><span class="sxs-lookup"><span data-stu-id="0624b-121">Choose the entity that includes the attribute you want to segment by.</span></span>

1. <span data-ttu-id="0624b-122">Aukeratu arabera zatitu beharreko atributua.</span><span class="sxs-lookup"><span data-stu-id="0624b-122">Choose the attribute to segment by.</span></span> <span data-ttu-id="0624b-123">Atributu honek lau balio motetako bat izan dezake: zenbakikoa, katea, data edo boolearra.</span><span class="sxs-lookup"><span data-stu-id="0624b-123">This attribute can have one of four value types: numerical, string, date, or Boolean.</span></span>

1. <span data-ttu-id="0624b-124">Aukeratu operadorea eta balio bat hautatutako atributurako.</span><span class="sxs-lookup"><span data-stu-id="0624b-124">Choose an operator and a value for the selected attribute.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="0624b-125">![Pertsonalizatu taldeko iragazkia](media/customer-group-numbers.png "Bezeroaren taldeko iragazkia")</span><span class="sxs-lookup"><span data-stu-id="0624b-125">![Custom group filter](media/customer-group-numbers.png "Customer group filter")</span></span>

   |<span data-ttu-id="0624b-126">Zenbakia</span><span class="sxs-lookup"><span data-stu-id="0624b-126">Number</span></span> |<span data-ttu-id="0624b-127">Definizioa</span><span class="sxs-lookup"><span data-stu-id="0624b-127">Definition</span></span>  |
   |---------|---------|
   |<span data-ttu-id="0624b-128">1</span><span class="sxs-lookup"><span data-stu-id="0624b-128">1</span></span>     |<span data-ttu-id="0624b-129">Entity</span><span class="sxs-lookup"><span data-stu-id="0624b-129">Entity</span></span>          |
   |<span data-ttu-id="0624b-130">2</span><span class="sxs-lookup"><span data-stu-id="0624b-130">2</span></span>     |<span data-ttu-id="0624b-131">Atributua</span><span class="sxs-lookup"><span data-stu-id="0624b-131">Attribute</span></span>          |
   |<span data-ttu-id="0624b-132">3</span><span class="sxs-lookup"><span data-stu-id="0624b-132">3</span></span>    |<span data-ttu-id="0624b-133">Eragilea</span><span class="sxs-lookup"><span data-stu-id="0624b-133">Operator</span></span>         |
   |<span data-ttu-id="0624b-134">4</span><span class="sxs-lookup"><span data-stu-id="0624b-134">4</span></span>    |<span data-ttu-id="0624b-135">Balioa</span><span class="sxs-lookup"><span data-stu-id="0624b-135">Value</span></span>         |

8. <span data-ttu-id="0624b-136">Erakundea bezero bateratutako entitatearekin konektatuta badago [harremanak](relationships.md), erlazio bidea zehaztu behar duzu baliozko segmentua sortzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-136">If the entity is connected to the unified customer entity through [relationships](relationships.md), you need to define the relationship path to create a valid segment.</span></span> <span data-ttu-id="0624b-137">Gehitu entitateak erlazio-bide honetatik hautatu dezakezu arte **Bezeroa: CustomerInsights** entitatea goitibehera.</span><span class="sxs-lookup"><span data-stu-id="0624b-137">Add the entities from the relationship path until you can select the **Customer:CustomerInsights** entity from the dropdown.</span></span> <span data-ttu-id="0624b-138">Ondoren, aukeratu **Erregistro guztiak** baldintza bakoitzerako.</span><span class="sxs-lookup"><span data-stu-id="0624b-138">Then, choose **All records** for each condition.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="0624b-139">![Harreman bidea segmentuak sortzean](media/segments-multiple-relationships.png "Harreman bidea segmentuak sortzean")</span><span class="sxs-lookup"><span data-stu-id="0624b-139">![Relationship path during segment creation](media/segments-multiple-relationships.png "Relationship path during segment creation")</span></span>

1. <span data-ttu-id="0624b-140">Lehenespenez, segmentuek definitutako iragazkiekin bat datozen bezeroen profilen atributu guztiak dituen irteerako entitatea sortzen dute.</span><span class="sxs-lookup"><span data-stu-id="0624b-140">By default, segments generate an output entity that contains all attributes of customer profiles which match the defined filters.</span></span> <span data-ttu-id="0624b-141">Segmentu bat ez den beste entitate batzuetan oinarrituta badago *Bezeroa* entitatea, entitate hauetatik atributu gehiago gehi ditzakezu irteerako entitateari.</span><span class="sxs-lookup"><span data-stu-id="0624b-141">If a segment is based on other entities than the *Customer* entity, you can add more attributes from these entities to the output entity.</span></span> <span data-ttu-id="0624b-142">Aukeratu **Proiektuaren atributuak** irteerako entitateari erantsiko zaizkion atributuak aukeratzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-142">Select **Project attributes** to choose the attributes that will be appended to the output entity.</span></span>  

   
   <span data-ttu-id="0624b-143">Adibidez: segmentu bat bezeroarekin lotutako jarduerak dituen entitate batean oinarritzen da *Bezeroa* entitatea.</span><span class="sxs-lookup"><span data-stu-id="0624b-143">Example: A segment is based on an entity that contains customer activity data which is related to the *Customer* entity.</span></span> <span data-ttu-id="0624b-144">Segmentuak azken 60 egunetan laguntza-mahaira deitu duten bezero guztiak bilatzen ditu.</span><span class="sxs-lookup"><span data-stu-id="0624b-144">The segment looks for all customers that called the help desk in the last 60 days.</span></span> <span data-ttu-id="0624b-145">Irteerako entitatean bat datozen bezeroen erregistro guztiei deiaren iraupena eta dei kopurua eranstea aukera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="0624b-145">You can choose to append the call duration and the number of calls to all matching customer records in the output entity.</span></span> <span data-ttu-id="0624b-146">Informazio hau baliagarria izan daiteke maiz deitzen duten bezeroei lineako laguntza artikuluen eta ohiko galderen esteka lagungarriekin mezu elektronikoak bidaltzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-146">This information might be useful to send an email with helpful links to online help articles and FAQs to customers who called frequently.</span></span>

1. <span data-ttu-id="0624b-147">Segmentua gordetzeko, sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="0624b-147">Select **Save** to save your segment.</span></span> <span data-ttu-id="0624b-148">Zure segmentua gordeko da eta prozesatu egingo da baldintza guztiak baliozkotuz gero.</span><span class="sxs-lookup"><span data-stu-id="0624b-148">Your segment will be saved and processed if all requirements are validated.</span></span> <span data-ttu-id="0624b-149">Bestela, zirriborro gisa gordeko da.</span><span class="sxs-lookup"><span data-stu-id="0624b-149">Otherwise, it will be saved as a draft.</span></span>

1. <span data-ttu-id="0624b-150">Aukeratu **Segurtasunetara itzuli** berriro ere **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="0624b-150">Select **Back to segments** to go back to the **Segments** page.</span></span>

## <a name="manage-existing-segments"></a><span data-ttu-id="0624b-151">Kudeatu lehendik dauden segmentuak</span><span class="sxs-lookup"><span data-stu-id="0624b-151">Manage existing segments</span></span>

<span data-ttu-id="0624b-152">Gainean **segmentuak** orrialdean, gordetako segmentu guztiak ikusi eta kudeatu ahal izango dituzu.</span><span class="sxs-lookup"><span data-stu-id="0624b-152">On the **Segments** page, you can view all your saved segments and manage them.</span></span>

<span data-ttu-id="0624b-153">Segmentu bakoitza segmentuari buruzko informazio osagarria biltzen duen errenkada batez irudikatuta dago.</span><span class="sxs-lookup"><span data-stu-id="0624b-153">Each segment is represented by a row that includes additional information about the segment.</span></span>

<span data-ttu-id="0624b-154">Zutabeak segmentu bat ordenatu dezakezu zutabearen goiburua hautatuta.</span><span class="sxs-lookup"><span data-stu-id="0624b-154">You can sort the segments in a column by selecting the column heading.</span></span>

<span data-ttu-id="0624b-155">Erabili **Bilatu** goiko eskuineko izkinan segmentuak iragazteko kutxa.</span><span class="sxs-lookup"><span data-stu-id="0624b-155">Use the **Search** box in the top-right corner to filter the segments.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0624b-156">![Aukerak lehendik dagoen segmentu bat kudeatzeko](media/segments-selected-segment.png "Aukerak lehendik dagoen segmentu bat kudeatzeko")</span><span class="sxs-lookup"><span data-stu-id="0624b-156">![Options to manage an existing segment](media/segments-selected-segment.png "Options to manage an existing segment")</span></span>

<span data-ttu-id="0624b-157">Segmentu bat hautatzean ekintza hauek erabilgarri daude:</span><span class="sxs-lookup"><span data-stu-id="0624b-157">The following action are available when you select a segment:</span></span>

- <span data-ttu-id="0624b-158">**ikusi** segmentuko xehetasunak, kideen zenbaketa joera segmentuko kideen aurrebista barne.</span><span class="sxs-lookup"><span data-stu-id="0624b-158">**View** the segment details, including member count trend a preview of segment members.</span></span>
- <span data-ttu-id="0624b-159">**Editatu** segmentuak bere propietateak aldatzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-159">**Edit** the segment to change its properties.</span></span>
- <span data-ttu-id="0624b-160">**Sortu bikoiztuak** segmentu baten.</span><span class="sxs-lookup"><span data-stu-id="0624b-160">**Create duplicate** of a segment.</span></span> <span data-ttu-id="0624b-161">Bere propietateak berehala editatzea edo bikoiztua gordetzea aukeratu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="0624b-161">You can choose to edit its properties right away or simply save the duplicate.</span></span>
- <span data-ttu-id="0624b-162">**Freskatu** segmentuak azken datuak sartuko ditu.</span><span class="sxs-lookup"><span data-stu-id="0624b-162">**Refresh** the segment to include the latest data.</span></span>
- <span data-ttu-id="0624b-163">**Aktibatu** edo **Desaktibatu** segmentua.</span><span class="sxs-lookup"><span data-stu-id="0624b-163">**Activate** or **Deactivate** the segment.</span></span> <span data-ttu-id="0624b-164">Segmentuek bi egoera posible dituzte: aktiboak edo inaktiboak.</span><span class="sxs-lookup"><span data-stu-id="0624b-164">Segments have two possible states - active or inactive.</span></span> <span data-ttu-id="0624b-165">Egoera hauek oso ondo etortzen dira segmentu bat editatzerakoan.</span><span class="sxs-lookup"><span data-stu-id="0624b-165">These states come in handy when editing a segment.</span></span> <span data-ttu-id="0624b-166">Segmentu inaktiboetan, segmentuaren definizioa badago, baina oraindik ez du bezeroik.</span><span class="sxs-lookup"><span data-stu-id="0624b-166">For inactive segments, the segment definition exists but it doesn't contain any customers yet.</span></span> <span data-ttu-id="0624b-167">Segmentu bat aktibatzean, egoera "inaktibo" izatetik "aktibo" izatera pasatzen da eta segmentuaren definizioarekin bat datozen bezeroak bilatzen hasiko da.</span><span class="sxs-lookup"><span data-stu-id="0624b-167">When you activate a segment, its state changes from 'inactive' to 'active" and it starts looking for customers that match the segment definition.</span></span> <span data-ttu-id="0624b-168">A bada [freskatze programatua](system.md#schedule-tab) konfiguratuta dago, segmentu inaktiboek dute **Egoera** gisa zerrendatuta **Saltatuta**, freskatzen saiatu ere ez zela egin adieraziz.</span><span class="sxs-lookup"><span data-stu-id="0624b-168">If a [scheduled refresh](system.md#schedule-tab) is configured, inactive segments have the **Status** listed as **Skipped**, indicating that a refresh wasn't even attempted.</span></span> <span data-ttu-id="0624b-169">Segmentu inaktiboa aktibatzen denean, freskatu egingo da eta programatutako freskapenetan sartuko da.</span><span class="sxs-lookup"><span data-stu-id="0624b-169">When an inactive segment is activated, it will refresh and will be included in scheduled refreshes.</span></span>
  <span data-ttu-id="0624b-170">Bestela, erabil dezakezu **Ordutegiak beranduago** funtzionaltasuna **Aktibatu / Desaktibatu** goitibehera, segmentu jakin bat aktibatzeko eta desaktibatzeko etorkizuneko data eta ordua zehazteko.</span><span class="sxs-lookup"><span data-stu-id="0624b-170">Alternatively, you can use the **Schedule later** functionality in the **Activate/Deactivate** dropdown to specify a future date and time for activation and deactivation of a particular segment.</span></span>
- <span data-ttu-id="0624b-171">**Aldatu izena** segmentuari.</span><span class="sxs-lookup"><span data-stu-id="0624b-171">**Rename** the segment.</span></span>
- <span data-ttu-id="0624b-172">**Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.</span><span class="sxs-lookup"><span data-stu-id="0624b-172">**Download** the list of members as a .CSV file.</span></span>
- <span data-ttu-id="0624b-173">**Gehitu** aukerak segmentuan dauden bezeroen IDen zerrenda bidaltzen du beste aplikazio batean prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-173">**Add to** option sends the list of customer IDs in the segment for processing in another application.</span></span>
- <span data-ttu-id="0624b-174">**Ezabatu** segmentua.</span><span class="sxs-lookup"><span data-stu-id="0624b-174">**Delete** the segment.</span></span>

## <a name="refresh-segments"></a><span data-ttu-id="0624b-175">Freskatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="0624b-175">Refresh segments</span></span>

<span data-ttu-id="0624b-176">Segmentu guztiak freskatu ditzakezu aldi berean hautatuta **Freskatu guztiak** gainean **segmentuak** orrialdea edo segmentu bat edo gehiago freskatu ditzakezu hautatzen dituzunean eta aukeratutakoan **Freskatu** aukeren artean.</span><span class="sxs-lookup"><span data-stu-id="0624b-176">You can refresh all segments at once by selecting **Refresh all** on the **Segments** page or you can refresh one or multiple segments when you select them and choose **Refresh** in from the options.</span></span> <span data-ttu-id="0624b-177">Bestela, berriztagarria den aldizka konfigura dezakezu **administratzailea** > **Sistema** > **Ordutegiak**.</span><span class="sxs-lookup"><span data-stu-id="0624b-177">Alternatively, you can configure a recurring refresh on **Admin** > **System** > **Schedule**.</span></span>

> [!TIP]
> <span data-ttu-id="0624b-178">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="0624b-178">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="0624b-179">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="0624b-179">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="0624b-180">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="0624b-180">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="0624b-181">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="0624b-181">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="download-and-export-segments"></a><span data-ttu-id="0624b-182">Deskargatu eta esportatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="0624b-182">Download and export segments</span></span>

<span data-ttu-id="0624b-183">Zure segmentuak CSV fitxategi batera deskarga ditzakezu edo Dynamics 365 Sales-era esportatu.</span><span class="sxs-lookup"><span data-stu-id="0624b-183">You can download your segments to a CSV file or export them to Dynamics 365 Sales.</span></span>

### <a name="download-segments-to-a-csv-file"></a><span data-ttu-id="0624b-184">Deskargatu segmentuak CSV fitxategi batera</span><span class="sxs-lookup"><span data-stu-id="0624b-184">Download segments to a CSV file</span></span>

1. <span data-ttu-id="0624b-185">Hartzaileen xehetasunetan, joan **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="0624b-185">In audience insights, go to the **Segments** page.</span></span>

2. <span data-ttu-id="0624b-186">Hautatu elipsia segmentu jakin bateko fitxan.</span><span class="sxs-lookup"><span data-stu-id="0624b-186">Select the ellipsis in a specific segment's tile.</span></span>

3. <span data-ttu-id="0624b-187">Aukeratu **Deskargatu CSV gisa** ekintzen goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="0624b-187">Select **Download as CSV** from the actions drop-down list.</span></span>

### <a name="export-segments-to-dynamics-365-sales"></a><span data-ttu-id="0624b-188">Esportatu segmentuak Dynamics 365 Sales-era</span><span class="sxs-lookup"><span data-stu-id="0624b-188">Export segments to Dynamics 365 Sales</span></span>

<span data-ttu-id="0624b-189">Dynamics 365 Sales-en segmentuak esportatu aurretik, administratzaile bat behar da [sortu esportazio-helmuga](export-destinations.md) Dynamics 365 Sales-erako.</span><span class="sxs-lookup"><span data-stu-id="0624b-189">Before exporting segments to Dynamics 365 Sales, an admin needs to [create the export destination](export-destinations.md) for Dynamics 365 Sales.</span></span>

1. <span data-ttu-id="0624b-190">Hartzaileen xehetasunetan, joan **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="0624b-190">In audience insights, go to the **Segments** page.</span></span>

2. <span data-ttu-id="0624b-191">Hautatu elipsia segmentu jakin bateko fitxan.</span><span class="sxs-lookup"><span data-stu-id="0624b-191">Select the ellipsis in a specific segment's tile.</span></span>

3. <span data-ttu-id="0624b-192">Aukeratu **Gehitu** ekintzen goitibeherako zerrendatik eta hautatu datuak bidali nahi dituzun esportazio helmuga.</span><span class="sxs-lookup"><span data-stu-id="0624b-192">Select **Add to** from the actions drop-down list and select the export destination you want to send the data to.</span></span>

## <a name="draft-mode-for-segments"></a><span data-ttu-id="0624b-193">Zirriborroen modua segmentuetarako</span><span class="sxs-lookup"><span data-stu-id="0624b-193">Draft mode for segments</span></span>

<span data-ttu-id="0624b-194">Segmentu bat prozesatzeko baldintza guztiak betetzen ez badira, segmentua zirriborro gisa gorde dezakezu eta sar itzazu **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="0624b-194">If not all requirements to process a segment are met, you can save the segment as a draft and access it from the **Segments** page.</span></span>

<span data-ttu-id="0624b-195">Segmentu aktibo gisa gordeko da eta ezin da aktibatu baliozkoa izan arte.</span><span class="sxs-lookup"><span data-stu-id="0624b-195">It will be saved as an inactive segment, and can't be activated it until it's valid.</span></span>

## <a name="add-more-conditions-to-a-group"></a><span data-ttu-id="0624b-196">Gehitu baldintza gehiago taldeari</span><span class="sxs-lookup"><span data-stu-id="0624b-196">Add more conditions to a group</span></span>

<span data-ttu-id="0624b-197">Talde bati baldintza gehiago gehitzeko, bi operadore logiko erabil ditzakezu:</span><span class="sxs-lookup"><span data-stu-id="0624b-197">To add more conditions to a group, you can use two logical operators:</span></span>

- <span data-ttu-id="0624b-198">**ETA** operadorea: Bi baldintza segmentazio prozesuaren baitan bete behar dira.</span><span class="sxs-lookup"><span data-stu-id="0624b-198">**AND** operator: Both conditions must be met as part of the segmentation process.</span></span> <span data-ttu-id="0624b-199">Aukera hau baliagarria da entitate desberdinetan baldintzak definitzen dituzunean.</span><span class="sxs-lookup"><span data-stu-id="0624b-199">This option is most useful when you define conditions across different entities.</span></span>

- <span data-ttu-id="0624b-200">**EDO** operadorea: Baldintzaren bat segmentazio prozesuaren zati gisa bete behar da.</span><span class="sxs-lookup"><span data-stu-id="0624b-200">**OR** operator: Either one of the conditions needs to be met as part of the segmentation process.</span></span> <span data-ttu-id="0624b-201">Aukera hau oso baliagarria da hainbat baldintza definitzen dituzunean entitate berarentzat.</span><span class="sxs-lookup"><span data-stu-id="0624b-201">This option is most useful when you define multiple conditions for the same entity.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="0624b-202">![EDO baldintza bat bete behar den operadorea](media/segmentation-either-condition.png "EDO baldintza bat bete behar den operadorea")</span><span class="sxs-lookup"><span data-stu-id="0624b-202">![OR operator where either condition needs to be met](media/segmentation-either-condition.png "OR operator where either condition needs to be met")</span></span>

<span data-ttu-id="0624b-203">Gaur egun, habia habia egin daiteke **EDO** operadorea **ETA** operadorea, baina ez alderantziz.</span><span class="sxs-lookup"><span data-stu-id="0624b-203">It's currently possible to nest an **OR** operator under an **AND** operator, but not the other way around.</span></span>

## <a name="combine-multiple-groups"></a><span data-ttu-id="0624b-204">Konbinatu hainbat talde</span><span class="sxs-lookup"><span data-stu-id="0624b-204">Combine multiple groups</span></span>

<span data-ttu-id="0624b-205">Talde bakoitzak bezero multzo zehatz bat sortzen du.</span><span class="sxs-lookup"><span data-stu-id="0624b-205">Each group produces a specific set of customers.</span></span> <span data-ttu-id="0624b-206">Talde horiek konbinatu ditzakezu zure negoziorako behar diren bezeroak sartzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-206">You can combine these groups to include the customers required for your business case.</span></span>

1. <span data-ttu-id="0624b-207">Hartzaileen xehetasunetan, joan hona: **Segmentuak** orrira eta hautatu segmentu bat.</span><span class="sxs-lookup"><span data-stu-id="0624b-207">In audience insights, go to the **Segments** page and select a segment.</span></span>

2. <span data-ttu-id="0624b-208">Hautatu **Gehitu taldea**.</span><span class="sxs-lookup"><span data-stu-id="0624b-208">Select **Add Group**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="0624b-209">![Bezeroen taldea gehitzeko taldea](media/customer-group-add-group.png "Bezeroen taldea gehitzeko taldea")</span><span class="sxs-lookup"><span data-stu-id="0624b-209">![Customer group add group](media/customer-group-add-group.png "Customer group add group")</span></span>

3. <span data-ttu-id="0624b-210">Hautatu multzo multzo hauetako eragileetako bat: **Batura**, **Gurutzatu**, edo **Salbu**.</span><span class="sxs-lookup"><span data-stu-id="0624b-210">Select one of the following set operators: **Union**, **Intersect**, or **Except**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="0624b-211">![Bezeroen taldea gehitzeko bateratzea](media/customer-group-union.png "Bezeroen taldea gehitzeko bateratzea")</span><span class="sxs-lookup"><span data-stu-id="0624b-211">![Customer group add union](media/customer-group-union.png "Customer group add union")</span></span>

   <span data-ttu-id="0624b-212">Hautatu multzo operatiboa talde berria definitzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-212">Select a set operator to define a new group.</span></span> <span data-ttu-id="0624b-213">Gorde talde desberdinak, zer datu mantentzen diren zehazteko:</span><span class="sxs-lookup"><span data-stu-id="0624b-213">Save different groups to determine what data gets retained:</span></span>

   - <span data-ttu-id="0624b-214">**Bateratzea** bi taldeak batzen ditu.</span><span class="sxs-lookup"><span data-stu-id="0624b-214">**Union** unites the two groups.</span></span>

   - <span data-ttu-id="0624b-215">**Gurutzatu** bi taldeak gainjartzen ditu.</span><span class="sxs-lookup"><span data-stu-id="0624b-215">**Intersect** overlaps the two groups.</span></span> <span data-ttu-id="0624b-216">Bi taldeetako datu *komunak* soilik mantentzen dira talde bateratuan.</span><span class="sxs-lookup"><span data-stu-id="0624b-216">Only data that *is common* to both groups is retained in the unified group.</span></span>

   - <span data-ttu-id="0624b-217">**Salbuespena** bi taldeak batzen ditu.</span><span class="sxs-lookup"><span data-stu-id="0624b-217">**Except** combines the two groups.</span></span> <span data-ttu-id="0624b-218">A eta B talde bietan *ez dauden* datuak soilik mantentzen dira.</span><span class="sxs-lookup"><span data-stu-id="0624b-218">Only data in group A that *is not common* to data in group B is retained.</span></span>

## <a name="view-processing-history-and-segment-members"></a><span data-ttu-id="0624b-219">Ikusi prozesaketaren historia eta segmentuko kideak</span><span class="sxs-lookup"><span data-stu-id="0624b-219">View processing history and segment members</span></span>

<span data-ttu-id="0624b-220">Segurtasun bati buruzko datu bateratuak ikus ditzakezu haren xehetasunak berrikusiz.</span><span class="sxs-lookup"><span data-stu-id="0624b-220">You can see consolidated data about a segment by reviewing its details.</span></span>

<span data-ttu-id="0624b-221">**Segmentuak** orrian, hautatu berrikusi nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="0624b-221">On the **Segments** page, select the segment you want to review.</span></span>

<span data-ttu-id="0624b-222">Orriaren goiko aldean joera grafikoa dago, kideen zenbateko aldaketak bistaratzen dituena.</span><span class="sxs-lookup"><span data-stu-id="0624b-222">The upper part of the page includes a trend graph that visualizes changes in member count.</span></span> <span data-ttu-id="0624b-223">Pasa datuak gainetik kideak data jakin batean ikusteko.</span><span class="sxs-lookup"><span data-stu-id="0624b-223">Hover over data points to see the member count on a specific date.</span></span>

<span data-ttu-id="0624b-224">Bistaratzeko denbora-markoa eguneratu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="0624b-224">You can update the time frame of the visualization.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="0624b-225">![Segmentuaren denbora-tartea](media/segment-time-range.png "Segmentuaren denbora-tartea")</span><span class="sxs-lookup"><span data-stu-id="0624b-225">![Segment time range](media/segment-time-range.png "Segment time range")</span></span>

<span data-ttu-id="0624b-226">Beheko aldean segmentuko kideen zerrenda dago.</span><span class="sxs-lookup"><span data-stu-id="0624b-226">The lower part contains a list of the segment members.</span></span>

> [!NOTE]
> <span data-ttu-id="0624b-227">Zerrenda honetan agertzen diren eremuak zure segmentuko entitateen atributuetan oinarrituta daude.</span><span class="sxs-lookup"><span data-stu-id="0624b-227">Fields that appear in this list are based on the attributes of your segment's entities.</span></span>
>
><span data-ttu-id="0624b-228">Zerrenda bat datorren segmentuko kideen aurrebista da eta zure segmentuko lehen 100 erregistroak erakusten ditu, behar bezala baloratu eta haren definizioak berrikusteko.</span><span class="sxs-lookup"><span data-stu-id="0624b-228">The list is a preview of the matching segment members and shows the first 100 records of your segment so that you can quickly evaluate it and review its definitions if needed.</span></span> <span data-ttu-id="0624b-229">Bat datozen erregistro guztiak ikusteko, beharrezkoa da [esportatu segmentua](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="0624b-229">To see all matching records, you need to [export the segment](export-destinations.md).</span></span>

## <a name="quick-segments"></a><span data-ttu-id="0624b-230">Segmentu azkarrak</span><span class="sxs-lookup"><span data-stu-id="0624b-230">Quick segments</span></span>

<span data-ttu-id="0624b-231">Segmentu-egileaz gain, segmentuak sortzeko beste bide bat dago.</span><span class="sxs-lookup"><span data-stu-id="0624b-231">In addition to the segment builder, there's another path for creating segments.</span></span> <span data-ttu-id="0624b-232">Segmentu azkarrek segmentu errazak (operadore bakarrarekin) eraiki eta berehala eskaintzen dizute.</span><span class="sxs-lookup"><span data-stu-id="0624b-232">Quick segments let you build simple segments with a single operator quickly and with instant insights.</span></span>

1. <span data-ttu-id="0624b-233">Gainean **segmentuak** orria, hautatu **Berria** > **Sortu azkar**.</span><span class="sxs-lookup"><span data-stu-id="0624b-233">On the **Segments** page, select **New** > **Quickly create from**.</span></span>

   - <span data-ttu-id="0624b-234">Hautatu botoia **profilak** Aukeratutako bezeroaren entitatean oinarritutako segmentu bat eraikitzeko aukera.</span><span class="sxs-lookup"><span data-stu-id="0624b-234">Select the **Profiles** option to build a segment that is based on the unified Customer entity.</span></span>
   - <span data-ttu-id="0624b-235">Hautatu botoia **Neurriak** Aukera hau aurrez sortu dituzun bezeroarentzako atributu mota bakoitzaren inguruan segmentu bat eraikitzeko **Neurriak** orria.</span><span class="sxs-lookup"><span data-stu-id="0624b-235">Select the **Measures** option to build a segment around each of the Customer Attribute type of measures you have previously created on the **Measures** page.</span></span>
   - <span data-ttu-id="0624b-236">Hautatu botoia **Adimen** Aukera hau bai erabiliz sortu duzun irteerako entitateetako baten inguruan eraikitzeko aukera **iragarpenak** edo **Neurrira egindako ereduak** gaitasunak.</span><span class="sxs-lookup"><span data-stu-id="0624b-236">Select the **Intelligence** option to build a segment around one of the output entities you generated using either the **Predictions** or **Custom Models** capabilities.</span></span>

2. <span data-ttu-id="0624b-237">Sarbidean **Segmentu azkar berria** elkarrizketa-koadroan, hautatu atributu bat **eremua** goitibeherako menuko.</span><span class="sxs-lookup"><span data-stu-id="0624b-237">In the **New quick segment** dialog box, select an attribute from the **Field** dropdown.</span></span>

3. <span data-ttu-id="0624b-238">Sistemak ikuspegi osagarriak emango ditu zure bezeroen segmentu hobeak sortzen lagunduko dutenak.</span><span class="sxs-lookup"><span data-stu-id="0624b-238">The system will provide some additional insights that help you create better segments of your customers.</span></span>
   - <span data-ttu-id="0624b-239">Eremu kategorikoetarako, 10 bezero zenbatuko ditugu.</span><span class="sxs-lookup"><span data-stu-id="0624b-239">For categorical fields, we'll show 10 top customer counts.</span></span> <span data-ttu-id="0624b-240">Hautatu **Balio** bat eta hautatu **Berrikusi**.</span><span class="sxs-lookup"><span data-stu-id="0624b-240">Choose a **Value** and select **Review**.</span></span>

   - <span data-ttu-id="0624b-241">Zenbakizko atributu bat lortzeko, sistemak erakutsiko du zer atributu-balioa eroriko den bezero bakoitzaren portzentalaren azpian.</span><span class="sxs-lookup"><span data-stu-id="0624b-241">For a numerical attribute, the system will show what attribute value falls under each customer's percentile.</span></span> <span data-ttu-id="0624b-242">Aukeratu bat **Operadorea** eta **Balioa** eta hautatu **Berrikusi**.</span><span class="sxs-lookup"><span data-stu-id="0624b-242">Choose an **Operator** and a **Value**, then select **Review**.</span></span>

4. <span data-ttu-id="0624b-243">Sistemak zurekin hornituko zaitu **Segurtasunaren neurria**.</span><span class="sxs-lookup"><span data-stu-id="0624b-243">The system will provide you with an **Estimated segment size**.</span></span> <span data-ttu-id="0624b-244">Definitu duzun segmentua sortu edo aukeratu dezakezu edo, bestela, berrikusi beste segmentu baten tamaina lortzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-244">You can choose whether to generate the segment you've defined, or first revisit it to get a different segment size.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="0624b-245">![Izena eta estimazioa segmentu azkar baterako](media/quick-segment-name.png "Izena eta estimazioa segmentu azkar baterako")</span><span class="sxs-lookup"><span data-stu-id="0624b-245">![Name and estimation for a quick segment](media/quick-segment-name.png "Name and estimation for a quick segment")</span></span>

5. <span data-ttu-id="0624b-246">Jarri **izena** zure segmentuari.</span><span class="sxs-lookup"><span data-stu-id="0624b-246">Provide a **Name** for your segment.</span></span> <span data-ttu-id="0624b-247">Nahi baduzu, eman **Bistaratzeko izena**.</span><span class="sxs-lookup"><span data-stu-id="0624b-247">Optionally, provide a **Display name**.</span></span>

6. <span data-ttu-id="0624b-248">Segmentua sortzeko, sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="0624b-248">Select **Save** to create your segment.</span></span>

7. <span data-ttu-id="0624b-249">Segmentua prozesatu ondoren, sortu duzun beste edozein segmentu bezala ikus dezakezu.</span><span class="sxs-lookup"><span data-stu-id="0624b-249">After the segment has finished processing, you can view it like any other segment you've created.</span></span>

<span data-ttu-id="0624b-250">Hurrengo agertokietarako, gomendatzen dugu segmentu eraikitzailea erabiltzea gomendatutako segmentuen gaitasuna baino:</span><span class="sxs-lookup"><span data-stu-id="0624b-250">For the following scenarios, we advise using the segment builder rather than the recommended segments capability:</span></span>

- <span data-ttu-id="0624b-251">Segurtasunak sortzen iragazkiak eremu kategorietan operadorea ez den beste eremuetan **da** operadorea</span><span class="sxs-lookup"><span data-stu-id="0624b-251">Creating segments with filters on categorical fields where the operator is different than the **Is** operator</span></span>
- <span data-ttu-id="0624b-252">Segmentuak sortu iragazkiak zenbaki-eremuetan, operadorea baino desberdinak direnetan **bitarte honetan**, **Baino handiagoa**, eta **Baino gutxiago** operadore</span><span class="sxs-lookup"><span data-stu-id="0624b-252">Creating segments with filters on numerical fields where the operator is different than the **Between**, **Greater than**, and **Less than** operators</span></span>
- <span data-ttu-id="0624b-253">Data-motako eremuetan iragazkiak dituzten segmentuak sortzen</span><span class="sxs-lookup"><span data-stu-id="0624b-253">Creating segments with filters on date type fields</span></span>

## <a name="next-steps"></a><span data-ttu-id="0624b-254">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="0624b-254">Next steps</span></span>

<span data-ttu-id="0624b-255">[Esportatu segmentua](export-destinations.md) eta esploratu [Bezero txartela](customer-card-add-in.md) eta [Konektoreak](export-power-bi.md) bezeroaren mailari buruzko informazioa lortzeko.</span><span class="sxs-lookup"><span data-stu-id="0624b-255">[Export a segment](export-destinations.md) and explore the [Customer Card](customer-card-add-in.md) and [Connectors](export-power-bi.md) to get insights on the customer level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]