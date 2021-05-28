---
title: Konbinatu entitateak datuen bateratzean
description: Konbinatu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 05/10/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 2cab702509596dd87c0c9b9769d1af8ba8387f9d
ms.sourcegitcommit: fcc94f55dc2dce84eae188d582801dc47696c9cc
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085561"
---
# <a name="merge-entities"></a><span data-ttu-id="6ca33-103">Konbinatu entitateak</span><span class="sxs-lookup"><span data-stu-id="6ca33-103">Merge entities</span></span>

<span data-ttu-id="6ca33-104">Konbinaketa fasea azken fasea da datuak bateratzeko prozesuan.</span><span class="sxs-lookup"><span data-stu-id="6ca33-104">The merge phase is the last phase in the data unification process.</span></span> <span data-ttu-id="6ca33-105">Bere helburua gatazkako datuak bateratzea da.</span><span class="sxs-lookup"><span data-stu-id="6ca33-105">Its purpose is reconciling conflicting data.</span></span> <span data-ttu-id="6ca33-106">Datu gatazkatsu batzuen adibideetan zure datu multzoetako bi bezeroen izena aurki daiteke, baina bakoitza modu desberdinean agertzen da ("Grant Marshall" versus "Grant Marshal"), edo telefono zenbakia (617-803-091X versus 617803091X ).</span><span class="sxs-lookup"><span data-stu-id="6ca33-106">Examples of conflicting data could include a customer name found in two of your datasets but that shows up a little differently in each ("Grant Marshall" versus "Grant Marshal"), or a phone number that differs in format (617-803-091X versus 617803091X).</span></span> <span data-ttu-id="6ca33-107">Datu-puntu gatazkatsu horiek batzea atributuak banatzen dira.</span><span class="sxs-lookup"><span data-stu-id="6ca33-107">Merging those conflicting data points is done on an attribute-by-attribute basis.</span></span>

:::image type="content" source="media/merge-fields-page.png" alt-text="Batu orria datuak bateratzeko prozesuan bezeroaren profil bateratua definitzen duten eremu bateratuekin taula erakusten duena.":::

<span data-ttu-id="6ca33-109">Bete ondoren [partidaren fasea](match-entities.md), batu fasea has dezakezu, hautatuta **konbinatu** lauza **bateratzeko** orria.</span><span class="sxs-lookup"><span data-stu-id="6ca33-109">After completing the [match phase](match-entities.md), you start the merge phase by selecting the **Merge** tile on the **Unify** page.</span></span>

## <a name="review-system-recommendations"></a><span data-ttu-id="6ca33-110">Aztertu sistemaren gomendioak</span><span class="sxs-lookup"><span data-stu-id="6ca33-110">Review system recommendations</span></span>

<span data-ttu-id="6ca33-111">**Datuak** > **Bat egin** > **Batu** aukeran, atributuak aukeratu eta baztertzen dituzu bezeroaren profileko entitate bateratuan bateratzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-111">On **Data** > **Unify** > **Merge**, you choose and exclude attributes to merge within your unified customer profile entity.</span></span> <span data-ttu-id="6ca33-112">Bezeroen profil bateratua datuak bateratzeko prozesuaren emaitza da.</span><span class="sxs-lookup"><span data-stu-id="6ca33-112">The unified customer profile is the result of the data unification process.</span></span> <span data-ttu-id="6ca33-113">Zenbait atributu automatikoki bateratzen dira sistemak.</span><span class="sxs-lookup"><span data-stu-id="6ca33-113">Some attributes are automatically merged by the system.</span></span>

<span data-ttu-id="6ca33-114">Automatikoki bateratutako atributuetako batean sartutako atributuak ikusteko, hautatu bateratutako atributu hori **Bezeroen eremuak** taularen fitxa.</span><span class="sxs-lookup"><span data-stu-id="6ca33-114">To view the attributes that are included in one of your automatically merged attributes, select that merged attribute in the **Customer fields** tab of the table.</span></span> <span data-ttu-id="6ca33-115">Bateratutako atributua osatzen duten bi atributuak bi errenkada berri bistaratuko dira bateratutako atributuaren azpian.</span><span class="sxs-lookup"><span data-stu-id="6ca33-115">The attributes that compose that merged attribute display in two new rows beneath the merged attribute.</span></span>

## <a name="separate-rename-exclude-and-edit-merged-fields"></a><span data-ttu-id="6ca33-116">Bereiztu, aldatu izena, baztertu eta editatu bateratutako eremuak</span><span class="sxs-lookup"><span data-stu-id="6ca33-116">Separate, rename, exclude, and edit merged fields</span></span>

<span data-ttu-id="6ca33-117">Sistemak bateratutako atributuak nola prozesatzen dituen alda dezakezu bezeroaren profil bateratua sortzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-117">You can change how the system processes merged attributes to generate the unified customer profile.</span></span> <span data-ttu-id="6ca33-118">Aukeratu **Erakutsi gehiago** eta aukeratu zer aldatu nahi duzun.</span><span class="sxs-lookup"><span data-stu-id="6ca33-118">Select **Show more** and choose what you want to change.</span></span>

:::image type="content" source="media/manage-merged-attributes.png" alt-text="Aukerak Erakutsi gehiago goitibeherako menuan bateratutako atributuak kudeatzeko.":::

<span data-ttu-id="6ca33-120">Informazio gehiagorako, ikus ondorengo atalak.</span><span class="sxs-lookup"><span data-stu-id="6ca33-120">For more information, see the following sections.</span></span>

## <a name="separate-merged-fields"></a><span data-ttu-id="6ca33-121">Zatitu konbinatutako eremuak</span><span class="sxs-lookup"><span data-stu-id="6ca33-121">Separate merged fields</span></span>

<span data-ttu-id="6ca33-122">Batutako eremuak bereizteko, bilatu atributua taulan.</span><span class="sxs-lookup"><span data-stu-id="6ca33-122">To separate merged fields, find the attribute in the table.</span></span> <span data-ttu-id="6ca33-123">Bereizitako eremuak bezeroaren profil bateratuan banakako datu gisa agertzen dira.</span><span class="sxs-lookup"><span data-stu-id="6ca33-123">Separated fields show as individual data points on the unified customer profile.</span></span> 

1. <span data-ttu-id="6ca33-124">Hautatu konbinatutako eremua.</span><span class="sxs-lookup"><span data-stu-id="6ca33-124">Select the merged field.</span></span>
  
1. <span data-ttu-id="6ca33-125">Aukeratu **Erakutsi gehiago** eta aukeratu **Eremu bereiziak**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-125">Select **Show more** and choose **Separate fields**.</span></span>
 
1. <span data-ttu-id="6ca33-126">Berretsi zatiketa.</span><span class="sxs-lookup"><span data-stu-id="6ca33-126">Confirm the separation.</span></span>

1. <span data-ttu-id="6ca33-127">Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-127">Select **Save** and **Run** to process the changes.</span></span>

## <a name="rename-merged-fields"></a><span data-ttu-id="6ca33-128">Aldatu bateratutako eremuak</span><span class="sxs-lookup"><span data-stu-id="6ca33-128">Rename merged fields</span></span>

<span data-ttu-id="6ca33-129">Aldatu bateratutako atributuen bistaratzeko izena.</span><span class="sxs-lookup"><span data-stu-id="6ca33-129">Change the display name of merged attributes.</span></span> <span data-ttu-id="6ca33-130">Ezin duzu aldatu irteerako entitatearen izena.</span><span class="sxs-lookup"><span data-stu-id="6ca33-130">You can't change the name of the output entity.</span></span>

1. <span data-ttu-id="6ca33-131">Hautatu konbinatutako eremua.</span><span class="sxs-lookup"><span data-stu-id="6ca33-131">Select the merged field.</span></span>
  
1. <span data-ttu-id="6ca33-132">Aukeratu **Erakutsi gehiago** eta aukeratu **Aldatu izena**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-132">Select **Show more** and choose **Rename**.</span></span>

1. <span data-ttu-id="6ca33-133">Berretsi aldatutako bistaratzeko izena.</span><span class="sxs-lookup"><span data-stu-id="6ca33-133">Confirm the changed display name.</span></span> 

1. <span data-ttu-id="6ca33-134">Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-134">Select **Save** and **Run** to process the changes.</span></span>

## <a name="exclude-merged-fields"></a><span data-ttu-id="6ca33-135">Baztertu konbinatutako eremuak</span><span class="sxs-lookup"><span data-stu-id="6ca33-135">Exclude merged fields</span></span>

<span data-ttu-id="6ca33-136">Baztertu atributu bat konbinatutako bezeroaren profiletik.</span><span class="sxs-lookup"><span data-stu-id="6ca33-136">Exclude an attribute from the unified customer profile.</span></span> <span data-ttu-id="6ca33-137">Eremua beste prozesu batzuetan erabiltzen bada, adibidez segmentu batean, ezabatu prozesu hauetatik bezeroaren profiletik baztertu aurretik.</span><span class="sxs-lookup"><span data-stu-id="6ca33-137">If the field is used in other processes, for example in a segment, remove it from these processes before excluding it from the customer profile.</span></span> 

1. <span data-ttu-id="6ca33-138">Hautatu konbinatutako eremua.</span><span class="sxs-lookup"><span data-stu-id="6ca33-138">Select the merged field.</span></span>
  
1. <span data-ttu-id="6ca33-139">Aukeratu **Erakutsi gehiago** eta aukeratu **Baztertu**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-139">Select **Show more** and choose **Exclude**.</span></span>

1. <span data-ttu-id="6ca33-140">Berretsi bazterketa.</span><span class="sxs-lookup"><span data-stu-id="6ca33-140">Confirm the exclusion.</span></span>

1. <span data-ttu-id="6ca33-141">Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-141">Select **Save** and **Run** to process the changes.</span></span> 

<span data-ttu-id="6ca33-142">**Batu** orrian, hautatu **Baztertutako eremuak** baztertutako eremu guztien zerrenda ikusteko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-142">On the **Merge** page, select **Excluded fields** to see the list of all excluded fields.</span></span> <span data-ttu-id="6ca33-143">Panel honek baztertutako eremuak berriro gehitzeko aukera ematen du.</span><span class="sxs-lookup"><span data-stu-id="6ca33-143">This pane lets you add excluded fields back.</span></span>

## <a name="manually-combine-fields"></a><span data-ttu-id="6ca33-144">Konbinatu eremuak eskuz</span><span class="sxs-lookup"><span data-stu-id="6ca33-144">Manually combine fields</span></span>

<span data-ttu-id="6ca33-145">Zehaztu bateratutako atributu bat eskuz.</span><span class="sxs-lookup"><span data-stu-id="6ca33-145">Specify a merged attribute manually.</span></span> 

1. <span data-ttu-id="6ca33-146">**Batu** orrian, hautatu **Konbinatu eremuak**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-146">On the **Merge** page, select **Combine fields**.</span></span>

1. <span data-ttu-id="6ca33-147">Eman **Izena** bat eta **Irteerako eremuaren izena**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-147">Provide a **Name** and an **Output field name**.</span></span>

1. <span data-ttu-id="6ca33-148">Aukeratu gehituko duzun eremua.</span><span class="sxs-lookup"><span data-stu-id="6ca33-148">Choose a field to add.</span></span> <span data-ttu-id="6ca33-149">Hautatu **Gehitu eremuak** eremu gehiago konbinatzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-149">Select **Add fields** to combine more fields.</span></span>

1. <span data-ttu-id="6ca33-150">Berretsi bazterketa.</span><span class="sxs-lookup"><span data-stu-id="6ca33-150">Confirm the exclusion.</span></span>

1. <span data-ttu-id="6ca33-151">Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-151">Select **Save** and **Run** to process the changes.</span></span> 

## <a name="change-the-order-of-fields"></a><span data-ttu-id="6ca33-152">Aldatu eremuen ordena</span><span class="sxs-lookup"><span data-stu-id="6ca33-152">Change the order of fields</span></span>

<span data-ttu-id="6ca33-153">Entitate batzuek besteek baino xehetasun gehiago dituzte.</span><span class="sxs-lookup"><span data-stu-id="6ca33-153">Some entities contain more details than others.</span></span> <span data-ttu-id="6ca33-154">Entitate batek eremu bati buruzko azken datuak biltzen baditu, baliteke bat egitean lehentasuna eman diezaiokezu beste entitateei.</span><span class="sxs-lookup"><span data-stu-id="6ca33-154">If an entity includes the latest data about a field, you can prioritize it over other entities when merging values.</span></span>

1. <span data-ttu-id="6ca33-155">Hautatu konbinatutako eremua.</span><span class="sxs-lookup"><span data-stu-id="6ca33-155">Select the merged field.</span></span>
  
1. <span data-ttu-id="6ca33-156">Aukeratu **Erakutsi gehiago** eta aukeratu **Editatu**.</span><span class="sxs-lookup"><span data-stu-id="6ca33-156">Select **Show more** and choose **Edit**.</span></span>

1. <span data-ttu-id="6ca33-157">Urtean **Konbinatu eremuak** panela, hautatu **Mugitu gora edo behera** ordena ezartzeko edo arrastatu eta askatu nahi duzun posizioan.</span><span class="sxs-lookup"><span data-stu-id="6ca33-157">In the **Combine fields** pane, select **Move up/down** to set the order or drag and drop them in the desired position.</span></span>

1. <span data-ttu-id="6ca33-158">Berretsi aldaketa.</span><span class="sxs-lookup"><span data-stu-id="6ca33-158">Confirm the change.</span></span>

1. <span data-ttu-id="6ca33-159">Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-159">Select **Save** and **Run** to process the changes.</span></span>

## <a name="run-your-merge"></a><span data-ttu-id="6ca33-160">Exekutatu zure bateratzea</span><span class="sxs-lookup"><span data-stu-id="6ca33-160">Run your merge</span></span>

<span data-ttu-id="6ca33-161">Eskuz batu atributuak edo sistemak batzen dituzun ala ez, beti bat egin dezakezu.</span><span class="sxs-lookup"><span data-stu-id="6ca33-161">Whether you manually merge attributes or let the system merge them, you can always run your merge.</span></span> <span data-ttu-id="6ca33-162">Hautatu **Exekutatu** **Konbinatu** orrian prozesua hasteko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-162">Select **Run** on the **Merge** page to start the process.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="6ca33-163">![Datuen batzea Gorde eta Exekutatu](media/configure-data-merge-save-run.png "Datuen batzea Gorde eta Exekutatu")</span><span class="sxs-lookup"><span data-stu-id="6ca33-163">![Data merge Save and Run](media/configure-data-merge-save-run.png "Data merge Save and Run")</span></span>

<span data-ttu-id="6ca33-164">Aukeratu **Exekutatu soilik Batu** bezero entitate bateratuan islatutako irteera soilik ikusi nahi baduzu.</span><span class="sxs-lookup"><span data-stu-id="6ca33-164">Choose **Run only Merge** if you only want to see the output reflected in the unified customer entity.</span></span> <span data-ttu-id="6ca33-165">Beherantz egindako prozesuak bezala freskatuko dira [freskatze-programan definitzen da](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="6ca33-165">Downstream processes will be refreshed as [defined in the refresh schedule](system.md#schedule-tab).</span></span>

<span data-ttu-id="6ca33-166">Aukeratu **Exekutatu, konbinatu eta erraztu prozesuak** sistema zure aldaketekin freskatzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-166">Choose **Run Merge and downstream processes** to refresh the system with your changes.</span></span> <span data-ttu-id="6ca33-167">Prozesu guztiak, aberastea, segmentuak eta neurriak barne automatikoki berriro abiaraziko dira.</span><span class="sxs-lookup"><span data-stu-id="6ca33-167">All processes, including enrichment, segments, and measures will rerun automatically.</span></span> <span data-ttu-id="6ca33-168">Erraztu prozesu guztiak amaitu ondoren, bezeroen profilek egindako aldaketak islatzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="6ca33-168">After all downstream processes have completed, the customer profiles reflect any changes you made.</span></span>

<span data-ttu-id="6ca33-169">Aldaketa gehiago egiteko eta urratsa berriro exekutatzeko, abian den bateratze bat bertan behera utzi dezakezu.</span><span class="sxs-lookup"><span data-stu-id="6ca33-169">To make more changes and rerun the step, you can cancel an in-progress merge.</span></span> <span data-ttu-id="6ca33-170">Aukeratu **Freskagarria ...** eta hautatu **Lana bertan behera utzi** agertzen den alboko panelean.</span><span class="sxs-lookup"><span data-stu-id="6ca33-170">Select **Refreshing ...** and select **Cancel job**  in the side pane that appears.</span></span>

> [!TIP]
> <span data-ttu-id="6ca33-171">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="6ca33-171">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="6ca33-172">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="6ca33-172">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="6ca33-173">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-173">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="6ca33-174">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="6ca33-174">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="next-step"></a><span data-ttu-id="6ca33-175">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="6ca33-175">Next Step</span></span>

<span data-ttu-id="6ca33-176">Konfiguratu [jarduerak](activities.md), [aberastea](enrichment-hub.md), edo [Harremanak](relationships.md) zure bezeroei buruzko ikuspegi gehiago lortzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-176">Configure [activities](activities.md), [enrichment](enrichment-hub.md), or [relationships](relationships.md) to gain more insights about your customers.</span></span>

<span data-ttu-id="6ca33-177">Aurretik jarduerak, aberastasuna edo segmentuak konfiguratu badituzu, automatikoki prozesatuko dira bezeroen azken datuak erabiltzeko.</span><span class="sxs-lookup"><span data-stu-id="6ca33-177">If you already configured activities, enrichment, or segments, they'll be processed automatically to use the latest customer data.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
