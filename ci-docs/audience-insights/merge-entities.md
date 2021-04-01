---
title: Konbinatu entitateak datuen bateratzean
description: Konbinatu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 04/16/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 737c593353878a5e322488d00de5dc5db5befda9
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597818"
---
# <a name="merge-entities"></a><span data-ttu-id="9b616-103">Konbinatu entitateak</span><span class="sxs-lookup"><span data-stu-id="9b616-103">Merge entities</span></span>

<span data-ttu-id="9b616-104">Konbinaketa fasea azken fasea da datuak bateratzeko prozesuan.</span><span class="sxs-lookup"><span data-stu-id="9b616-104">The merge phase is the last phase in the data unification process.</span></span> <span data-ttu-id="9b616-105">Bere helburua gatazkako datuak bateratzea da.</span><span class="sxs-lookup"><span data-stu-id="9b616-105">Its purpose is reconciling conflicting data.</span></span> <span data-ttu-id="9b616-106">Datu gatazkatsu batzuen adibideetan zure datu multzoetako bi bezeroen izena aurki daiteke, baina bakoitza modu desberdinean agertzen da ("Grant Marshall" versus "Grant Marshal"), edo telefono zenbakia (617-803-091X versus 617803091X ).</span><span class="sxs-lookup"><span data-stu-id="9b616-106">Examples of conflicting data could include a customer name found in two of your datasets but that shows up a little differently in each ("Grant Marshall" versus "Grant Marshal"), or a phone number that differs in format (617-803-091X versus 617803091X).</span></span> <span data-ttu-id="9b616-107">Datu-puntu gatazkatsu horiek batzea atributuak banatzen dira.</span><span class="sxs-lookup"><span data-stu-id="9b616-107">Merging those conflicting data points is done on an attribute-by-attribute basis.</span></span>

<span data-ttu-id="9b616-108">Bete ondoren [partidaren fasea](match-entities.md), batu fasea has dezakezu, hautatuta **konbinatu** lauza **bateratzeko** orria.</span><span class="sxs-lookup"><span data-stu-id="9b616-108">After completing the [match phase](match-entities.md), you start the merge phase by selecting the **Merge** tile on the **Unify** page.</span></span>

## <a name="review-system-recommendations"></a><span data-ttu-id="9b616-109">Aztertu sistemaren gomendioak</span><span class="sxs-lookup"><span data-stu-id="9b616-109">Review system recommendations</span></span>

<span data-ttu-id="9b616-110">Gainean **Konbinatu** orrialdea, zure bezeroaren profil bateratuaren entitatean bateratu beharreko atributuak aukeratu eta baztertu ditzakezu (konfigurazio prozesuaren emaitza).</span><span class="sxs-lookup"><span data-stu-id="9b616-110">On the **Merge** page, you choose and exclude attributes to merge within your unified customer profile entity (the result of the configuration process).</span></span> <span data-ttu-id="9b616-111">Zenbait atributu automatikoki bateratzen dira sistemak.</span><span class="sxs-lookup"><span data-stu-id="9b616-111">Some attributes are automatically merged by the system.</span></span>

### <a name="view-merged-attributes"></a><span data-ttu-id="9b616-112">Ikusi konbinatutako atributuak</span><span class="sxs-lookup"><span data-stu-id="9b616-112">View merged attributes</span></span>

<span data-ttu-id="9b616-113">Zure automatikoki batu diren atributuren batean sartutako atributuak ikusteko, hautatu batu atributu hori.</span><span class="sxs-lookup"><span data-stu-id="9b616-113">To view the attributes that are included in one of your automatically merged attributes, select that merged attribute.</span></span> <span data-ttu-id="9b616-114">Bateratutako atributua osatzen duten bi atributuak bi errenkada berri agertuko dira bateratutako atributuaren azpian.</span><span class="sxs-lookup"><span data-stu-id="9b616-114">The two attributes that compose that merged attribute display in two new rows beneath the merged attribute.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="9b616-115">![Hautatu konbinatutako atributua](media/configure-data-merge-profile-attributes.png "Hautatu konbinatutako atributua")</span><span class="sxs-lookup"><span data-stu-id="9b616-115">![Select merged attribute](media/configure-data-merge-profile-attributes.png "Select merged attribute")</span></span>

### <a name="separate-merged-attributes"></a><span data-ttu-id="9b616-116">Bereizi konbinatutako atributuak</span><span class="sxs-lookup"><span data-stu-id="9b616-116">Separate merged attributes</span></span>

<span data-ttu-id="9b616-117">Automatikoki batutako atributuak bereizteko edo desmerratzeko, bilatu atributua atalean **Profilaren atributuak** mahaia.</span><span class="sxs-lookup"><span data-stu-id="9b616-117">To separate or unmerge any of the automatically merged attributes, find the attribute in the **Profile attributes** table.</span></span>

1. <span data-ttu-id="9b616-118">Hautatu elipsi (...) botoia.</span><span class="sxs-lookup"><span data-stu-id="9b616-118">Select the ellipsis (...) button.</span></span>
  
2. <span data-ttu-id="9b616-119">Hautatu goitibeherako zerrendan **Eremu bereiziak**.</span><span class="sxs-lookup"><span data-stu-id="9b616-119">In the dropdown list, select **Separate fields**.</span></span>

### <a name="remove-merged-attributes"></a><span data-ttu-id="9b616-120">Kendu konbinatutako atributuak</span><span class="sxs-lookup"><span data-stu-id="9b616-120">Remove merged attributes</span></span>

<span data-ttu-id="9b616-121">Atributu bat bezeroaren azken profilaren entitatean baztertzeko, bilatu **Profilaren atributuak** mahaia.</span><span class="sxs-lookup"><span data-stu-id="9b616-121">To exclude an attribute from the final customer profile entity, find it in the **Profile attributes** table.</span></span>

1. <span data-ttu-id="9b616-122">Hautatu elipsi (...) botoia.</span><span class="sxs-lookup"><span data-stu-id="9b616-122">Select the ellipsis (...) button.</span></span>
  
2. <span data-ttu-id="9b616-123">Hautatu goitibeherako zerrendan **Ez konbinatu**.</span><span class="sxs-lookup"><span data-stu-id="9b616-123">In the dropdown list, select **Don't merge**.</span></span>

   <span data-ttu-id="9b616-124">Atributua mugitzen da **Bezeroaren erregistrotik kendu da** atalera.</span><span class="sxs-lookup"><span data-stu-id="9b616-124">The attribute is moved to the **Removed from customer record** section.</span></span>

## <a name="manually-add-a-merged-attribute"></a><span data-ttu-id="9b616-125">Gehitu batutako atributua eskuz</span><span class="sxs-lookup"><span data-stu-id="9b616-125">Manually add a merged attribute</span></span>

<span data-ttu-id="9b616-126">Bateratutako atributu bat gehitzeko, joan " **Konbinatu** orria.</span><span class="sxs-lookup"><span data-stu-id="9b616-126">To add a merged attribute, go to the **Merge** page.</span></span>

1. <span data-ttu-id="9b616-127">Hautatu **Gehitu konbinatutako atributua**.</span><span class="sxs-lookup"><span data-stu-id="9b616-127">Select **Add merged attribute**.</span></span>

2. <span data-ttu-id="9b616-128">Eman a **izena** identifikatzeko **konbinatu** orrialdea gero.</span><span class="sxs-lookup"><span data-stu-id="9b616-128">Provide a **Name** to identify it on the **Merge** page later.</span></span>

3. <span data-ttu-id="9b616-129">Aukeran, eman a **Bistaratu izena** hori bezeroaren profil bateratuko entitatean agertuko da.</span><span class="sxs-lookup"><span data-stu-id="9b616-129">Optionally, provide a **Display name** to appear in the unified Customer Profile entity.</span></span>

4. <span data-ttu-id="9b616-130">Konfiguratu **Hautatu bikoiztutako atributuak** parekatutako entitateetatik batu nahi dituzun atributuak hautatzeko.</span><span class="sxs-lookup"><span data-stu-id="9b616-130">Configure **Select duplicate attributes** to select the attributes that you want to merge from the matched entities.</span></span> <span data-ttu-id="9b616-131">Ezaugarriak bila ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="9b616-131">You can also search for attributes.</span></span>

5. <span data-ttu-id="9b616-132">Ezar ezazu **Sailkatu garrantziaren arabera** atributu bat besteen gainetik lehenestea.</span><span class="sxs-lookup"><span data-stu-id="9b616-132">Set the **Rank by importance** to prioritize one attribute above the others.</span></span> <span data-ttu-id="9b616-133">Adibidez, *WebAccountCSV* entitateak datuari buruzko datu zehatzenak biltzen ditu *Izen Osoak* atributuari lehentasuna eman diezaiokezu erakunde honi *ContactCSV* hautatuta *WebAccountCSV*.</span><span class="sxs-lookup"><span data-stu-id="9b616-133">For example, if the *WebAccountCSV* entity includes the most accurate data about the *Full Names* attribute, you could prioritize this entity over *ContactCSV* by selecting *WebAccountCSV*.</span></span> <span data-ttu-id="9b616-134">Ondorioz, *WebAccountCSV* lehen lehentasunera mugitzen da, berriz *ContactCSV* Balioak ateratzean bigarren lehentasunera pasatzen da *Izen osoa* atributu.</span><span class="sxs-lookup"><span data-stu-id="9b616-134">As a result, *WebAccountCSV* moves to first priority, while *ContactCSV* moves to second priority when pulling values for the *Full Name* attribute.</span></span>

## <a name="run-your-merge"></a><span data-ttu-id="9b616-135">Exekutatu zure bateratzea</span><span class="sxs-lookup"><span data-stu-id="9b616-135">Run your merge</span></span>

<span data-ttu-id="9b616-136">Eskuz batu atributuak edo sistemak batzen dituzun ala ez, beti bat egin dezakezu.</span><span class="sxs-lookup"><span data-stu-id="9b616-136">Whether you manually merge attributes or let the system merge them, you can always run your merge.</span></span> <span data-ttu-id="9b616-137">Hautatu **Exekutatu** **Konbinatu** orrian prozesua hasteko.</span><span class="sxs-lookup"><span data-stu-id="9b616-137">Select **Run** on the **Merge** page to start the process.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="9b616-138">![Datuen batzea Gorde eta Exekutatu](media/configure-data-merge-save-run.png "Datuen batzea Gorde eta Exekutatu")</span><span class="sxs-lookup"><span data-stu-id="9b616-138">![Data merge Save and Run](media/configure-data-merge-save-run.png "Data merge Save and Run")</span></span>

<span data-ttu-id="9b616-139">Aldaketa gehigarriak egiteko eta pausoa berriro egiteko, aurrerapen bateratzea bertan behera utzi dezakezu.</span><span class="sxs-lookup"><span data-stu-id="9b616-139">To make additional changes and rerun the step, you can cancel an in-progress merge.</span></span> <span data-ttu-id="9b616-140">Aukeratu **Freskagarria ...** eta hautatu **Lana bertan behera utzi** agertzen den alboko panelean.</span><span class="sxs-lookup"><span data-stu-id="9b616-140">Select **Refreshing ...** and select **Cancel job**  in the side pane that appears.</span></span>

<span data-ttu-id="9b616-141">Ondoren **Freskagarria ...** testua aldatzen da **Arrakastatsua**, bateratu zure datuak kontradikzioak osatu eta ebatzi ditu zuk zehaztutako gidalerroen arabera.</span><span class="sxs-lookup"><span data-stu-id="9b616-141">After the **Refreshing ...** text changes to **Successful**, merge has completed and resolved contradictions in your data according to the policies you defined.</span></span> <span data-ttu-id="9b616-142">Bat egin eta bateratu gabeko atributuak profil bateratuko entitatean sartzen dira.</span><span class="sxs-lookup"><span data-stu-id="9b616-142">Merged and unmerged attributes are included in the unified profile entity.</span></span> <span data-ttu-id="9b616-143">Alde batera utzitako atributuak ez dira barne hartzen bateratutako entitate-profilean.</span><span class="sxs-lookup"><span data-stu-id="9b616-143">Excluded attributes aren't included in the unified profile entity.</span></span>

<span data-ttu-id="9b616-144">Bateratzea behar bezala egiten ez bazen lehenengo aldia bada, downstream-eko prozesu guztiak automatikoki berriro aberastuko dira, aberastasuna, segmentazioa eta neurriak barne.</span><span class="sxs-lookup"><span data-stu-id="9b616-144">If it wasn't the first time you ran a merge successfully, all downstream processes, including enrichment, segmentation, and measures will rerun automatically.</span></span> <span data-ttu-id="9b616-145">Beheranzko prozesu guztiak berriro egin ondoren, bezeroen profilek egindako aldaketak islatzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="9b616-145">After all downstream processes have been rerun, the customer profiles reflect any changes you made.</span></span>

> [!TIP]
> <span data-ttu-id="9b616-146">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="9b616-146">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="9b616-147">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="9b616-147">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="9b616-148">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="9b616-148">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="9b616-149">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="9b616-149">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="next-step"></a><span data-ttu-id="9b616-150">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="9b616-150">Next Step</span></span>

<span data-ttu-id="9b616-151">Konfiguratu [jarduerak](activities.md), [aberastea](enrichment-microsoft-graph.md), edo [Harremanak](relationships.md) zure bezeroei buruzko ikuspegi gehiago lortzeko.</span><span class="sxs-lookup"><span data-stu-id="9b616-151">Configure [activities](activities.md), [enrichment](enrichment-microsoft-graph.md), or [relationships](relationships.md) to gain more insights about your customers.</span></span>

<span data-ttu-id="9b616-152">Jarduerak, aberastasuna edo harremanak konfiguratu badituzu edo segmentuak definitu badituzu, automatikoki prozesatuko dira bezeroen azken datuak erabiltzeko.</span><span class="sxs-lookup"><span data-stu-id="9b616-152">If you already configured activities, enrichment, or relationships, or if you defined segments, they'll be processed automatically to use the latest customer data.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]