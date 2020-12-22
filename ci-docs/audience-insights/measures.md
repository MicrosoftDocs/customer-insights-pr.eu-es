---
title: Sortu eta editatu neurriak
description: Bezeroekin erlazionatutako neurriak definitzea zenbait negozio-arloren errendimendua aztertzeko eta islatzeko.
ms.date: 10/15/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: wameng
manager: shellyha
ms.openlocfilehash: 0e214a6eb66abd27f7292db3ce2c2a6e16a8ff33
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404995"
---
# <a name="define-and-manage-measures"></a><span data-ttu-id="afa89-103">Neurriak zehaztu eta kudeatu</span><span class="sxs-lookup"><span data-stu-id="afa89-103">Define and manage measures</span></span>

<span data-ttu-id="afa89-104">**Neurriak** negozio-arlo jakin batzuen errendimendua eta osasuna islatzen dituzten funtsezko errendimenduen adierazleak (KPI) adierazten dituzte.</span><span class="sxs-lookup"><span data-stu-id="afa89-104">**Measures** represent key performance indicators (KPIs) that reflect the performance and health of specific business areas.</span></span> <span data-ttu-id="afa89-105">Hartzaileen xehetasunek neurri mota desberdinak eraikitzeko esperientzia intuitiboa eskaintzen dute, neurriak eskuz kodifikatu edo balidatzea eskatzen ez duen kontsulta-sortzailea erabiliz.</span><span class="sxs-lookup"><span data-stu-id="afa89-105">Audience insights provides an intuitive experience for building different types of measures, using a query builder that doesn't require you to code or validate your measures manually.</span></span> <span data-ttu-id="afa89-106">Zure negozio neurriak jarrai ditzakezu **Hasiera** orrialdean, ikus bezero zehatzentzako neurriak hemen **Bezero txartela** eta erabili neurriak bezeroaren segmentuak definitzeko **segmentu** orria.</span><span class="sxs-lookup"><span data-stu-id="afa89-106">You can track your business measures on the **Home** page, see measures for specific customers on the **Customer Card**, and use measures to define customer segments on the **Segments** page.</span></span>

## <a name="create-a-measure"></a><span data-ttu-id="afa89-107">Sortu neurri bat</span><span class="sxs-lookup"><span data-stu-id="afa89-107">Create a measure</span></span>

<span data-ttu-id="afa89-108">Atal honetan neurritik hutsetik ibiltzen zara.</span><span class="sxs-lookup"><span data-stu-id="afa89-108">This section walks you through creating a measure from scratch.</span></span> <span data-ttu-id="afa89-109">Neurri bat eraiki dezakezu Bezeroaren entitatearen bidez konektatutako datu-iturri ugarietatik.</span><span class="sxs-lookup"><span data-stu-id="afa89-109">You can build measures with data from multiple data sources that are connected through the Customer entity.</span></span> <span data-ttu-id="afa89-110">[Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.</span><span class="sxs-lookup"><span data-stu-id="afa89-110">Some [service limits](service-limits.md) apply.</span></span>

1. <span data-ttu-id="afa89-111">Hartzaileei buruzko xehetasunetan, joan hona: **Neurriak**.</span><span class="sxs-lookup"><span data-stu-id="afa89-111">In audience insights, go to **Measures**.</span></span>

2. <span data-ttu-id="afa89-112">Hautatu **Neurri berria**.</span><span class="sxs-lookup"><span data-stu-id="afa89-112">Select **New measure**.</span></span>

3. <span data-ttu-id="afa89-113">Aukeratu neurria **Mota**:</span><span class="sxs-lookup"><span data-stu-id="afa89-113">Choose the measure **Type**:</span></span>

   - <span data-ttu-id="afa89-114">**Bezeroaren atributua**: Bezero bakoitzeko puntu bakarra, puntuazioa, balioa edo egoera islatzen duena.</span><span class="sxs-lookup"><span data-stu-id="afa89-114">**Customer attribute**: A single field per customer that reflects a score, value, or state for the customer.</span></span> <span data-ttu-id="afa89-115">Bezeroaren atributuak sistema sortutako entitate berri batean atributu gisa sortzen dira **Customer_Measure**.</span><span class="sxs-lookup"><span data-stu-id="afa89-115">Customer attributes are created as attributes in a new system-generated entity called **Customer_Measure**.</span></span>

   - <span data-ttu-id="afa89-116">**Bezeroaren neurria**: Aukeratutako neurrien arabera, bezeroen portaerari buruzko ikuspegi orokorrak.</span><span class="sxs-lookup"><span data-stu-id="afa89-116">**Customer measure**: Insights on customer behavior with breakdown by selected dimensions.</span></span> <span data-ttu-id="afa89-117">Entitate berri bat sortzen da neurri bakoitzerako, potentzialki bezero bakoitzeko erregistro anitzekin.</span><span class="sxs-lookup"><span data-stu-id="afa89-117">A new entity is generated for each measure, potentially with multiple records per customer.</span></span>

   - <span data-ttu-id="afa89-118">**Negozio neurria**: Zure negozioaren errendimendua eta osasuna kontrolatzen ditu.</span><span class="sxs-lookup"><span data-stu-id="afa89-118">**Business measure**: Tracks your business performance and health of the business.</span></span> <span data-ttu-id="afa89-119">Enpresa-neurriek bi irteera desberdin izan ditzakete: etan agertzen den zenbakizko irteera **Hasiera** orrialdean edo aurkitzen duzun entitate berri batean **erakundeak** orria.</span><span class="sxs-lookup"><span data-stu-id="afa89-119">Business measures can have two different outputs: a numeric output that shows on the **Home** page or a new entity that you find on the **Entities** page.</span></span>

4. <span data-ttu-id="afa89-120">Eman a **izena** eta aukerakoa **Bistaratu izena** eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="afa89-120">Provide a **Name** and an optional **Display name**, then select **Next**.</span></span>

5. <span data-ttu-id="afa89-121">**Entitatea** atalean, goitibeherako zerrendan, hautatu lehenengo entitatea.</span><span class="sxs-lookup"><span data-stu-id="afa89-121">In the **Entities** section, select the first entity from the drop-down list.</span></span> <span data-ttu-id="afa89-122">Puntu honetan, entitate osagarriak beharrezkoak diren erabaki beharko zenuke neurriaren definizioaren barruan.</span><span class="sxs-lookup"><span data-stu-id="afa89-122">At this point, you should decide whether additional entities are needed as part of your measure definition.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="afa89-123">![Neurketaren definizioa](media/measure-definition.png "Neurketaren definizioa")</span><span class="sxs-lookup"><span data-stu-id="afa89-123">![Measure definition](media/measure-definition.png "Measure definition")</span></span>

   <span data-ttu-id="afa89-124">Entitate gehiago gehitzeko, hautatu **Entitatea gehitu** eta hautatu neurria erabili nahi duzun entitateak.</span><span class="sxs-lookup"><span data-stu-id="afa89-124">To add more entities, select **Add entity** and select entities you want to use for the measure.</span></span>

   > [!NOTE]
   > <span data-ttu-id="afa89-125">Soilik hasten ari zaren zuren entitatearekin harremanak dituzten entitateak aukera ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="afa89-125">You can select only entities that have relationships to your starting entity.</span></span> <span data-ttu-id="afa89-126">Harremanak definitzeari buruz informazio gehiago lortzeko, ikusi [Harremanak](relationships.md).</span><span class="sxs-lookup"><span data-stu-id="afa89-126">For more information about defining relationships, see [Relationships](relationships.md).</span></span>

6. <span data-ttu-id="afa89-127">Aukeran, aldagaiak konfigura ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="afa89-127">Optionally, you can configure variables.</span></span> <span data-ttu-id="afa89-128">**Aldagaiak** atalean, hautatu **Aldagai berria**.</span><span class="sxs-lookup"><span data-stu-id="afa89-128">In the **Variables** section, select **New variable**.</span></span>

   <span data-ttu-id="afa89-129">Aldagaiak zure hautatutako erregistro bakoitzean egiten diren kalkuluak dira.</span><span class="sxs-lookup"><span data-stu-id="afa89-129">Variables are calculations that are made on each of your selected records.</span></span> <span data-ttu-id="afa89-130">Adibidez, zure salmentako puntuen salmenta (POS) eta lineako salmentak zure bezeroen erregistro bakoitzerako.</span><span class="sxs-lookup"><span data-stu-id="afa89-130">For example, summing point-of-sale (POS) and online sales for each of your customers' records.</span></span>

7. <span data-ttu-id="afa89-131">Jarri **izena** aldagaiari.</span><span class="sxs-lookup"><span data-stu-id="afa89-131">Provide a **Name** for the variable.</span></span>

8. <span data-ttu-id="afa89-132">Sarbidean **Adierazpen** aukeratu eremua zure kalkuluarekin hasteko.</span><span class="sxs-lookup"><span data-stu-id="afa89-132">In the **Expression** area, choose a field to begin your calculation with.</span></span>

9. <span data-ttu-id="afa89-133">Idatzi adierazpen bat teklean **Adierazpen** eremua zure kalkuluan sartu beharreko eremu gehiago aukeratzen dituzun bitartean.</span><span class="sxs-lookup"><span data-stu-id="afa89-133">Type an expression in the **Expression** area while choosing more fields to be included in your calculation.</span></span>

   > [!NOTE]
   > <span data-ttu-id="afa89-134">Gaur egun, adierazpen aritmetikoak soilik onartzen dira.</span><span class="sxs-lookup"><span data-stu-id="afa89-134">Currently, only arithmetic expressions are supported.</span></span> <span data-ttu-id="afa89-135">Gainera, aldagaien kalkulua ez da onartzen hainbat entitaterentzat [entitate bideak](relationships.md).</span><span class="sxs-lookup"><span data-stu-id="afa89-135">Additionally, variable calculation isn't supported for entities from different [entity paths](relationships.md).</span></span>

10. <span data-ttu-id="afa89-136">Hautatu **Eginda**.</span><span class="sxs-lookup"><span data-stu-id="afa89-136">Select **Done**.</span></span>

11. <span data-ttu-id="afa89-137">Sarbidean **Neurrien definizioa** atalean, zure entitate aukeratuak eta kalkulatutako aldagaiak neurri-entitate edo atributu berri batean nola agregatzen diren zehaztuko duzu.</span><span class="sxs-lookup"><span data-stu-id="afa89-137">In the **Measure definition** section, you'll define how your chosen entities and calculated variables are aggregated in a new measure entity or attribute.</span></span>

12. <span data-ttu-id="afa89-138">Hautatu **Dimentsio berria**.</span><span class="sxs-lookup"><span data-stu-id="afa89-138">Select **New dimension**.</span></span> <span data-ttu-id="afa89-139">Dimentsio bat bezala pentsa dezakezu *taldeka* funtzioa.</span><span class="sxs-lookup"><span data-stu-id="afa89-139">You can think of a dimension as a *group by* function.</span></span> <span data-ttu-id="afa89-140">Zure Neurri entitatearen edo atributuaren irteera datuak zehaztutako dimentsio guztien arabera taldekatuko dira.</span><span class="sxs-lookup"><span data-stu-id="afa89-140">The data output of your Measure entity or attribute will be grouped by all of your defined dimensions.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="afa89-141">![Aukeratu ziklo agregatua](media/measures-businessreport-measure-definition2.png "Aukeratu ziklo agregatua")</span><span class="sxs-lookup"><span data-stu-id="afa89-141">![Choose aggregate cycle](media/measures-businessreport-measure-definition2.png "Choose aggregate cycle")</span></span>

    <span data-ttu-id="afa89-142">Hautatu edo sartu informazio hau zure dimentsioaren definizioaren zati gisa:</span><span class="sxs-lookup"><span data-stu-id="afa89-142">Select or enter the following information as part of your dimension's definition:</span></span>

    - <span data-ttu-id="afa89-143">**Erakunde**: Neurketa entitate bat definitzen baduzu, gutxienez atributu bat izan beharko luke.</span><span class="sxs-lookup"><span data-stu-id="afa89-143">**Entity**: If you define a Measure entity, it should include at least one attribute.</span></span> <span data-ttu-id="afa89-144">Neurrien atributu bat definitzen baduzu, atributu bakarra sartuko du lehenespenez.</span><span class="sxs-lookup"><span data-stu-id="afa89-144">If you define a Measure attribute, it will include only one attribute by default.</span></span> <span data-ttu-id="afa89-145">Aukeraketa atributu hori biltzen duen entitatea aukeratzeari buruzkoa da.</span><span class="sxs-lookup"><span data-stu-id="afa89-145">This selection is about choosing the entity that includes that attribute.</span></span>
    - <span data-ttu-id="afa89-146">**eremua**: Aukeratu ezazu zure Neurketa entitatean edo atributuan sartu beharreko atributua.</span><span class="sxs-lookup"><span data-stu-id="afa89-146">**Field**: Choose the specific attribute to be included either in your Measure entity or attribute.</span></span>
    - <span data-ttu-id="afa89-147">**Ontzia**: Egunero, hilero edo urtero datuak batu nahi dituzun aukeratu.</span><span class="sxs-lookup"><span data-stu-id="afa89-147">**Bucket**: Choose whether you want to aggregate data on a daily, monthly, or annual basis.</span></span> <span data-ttu-id="afa89-148">Beharrezko hautapena da Data motako atributu bat hautatu baduzu bakarrik.</span><span class="sxs-lookup"><span data-stu-id="afa89-148">It's a required selection only if you've selected a Date type attribute.</span></span>
    - <span data-ttu-id="afa89-149">**Hurrengoa bezala**: Zure eremu berriaren izena definitzen du.</span><span class="sxs-lookup"><span data-stu-id="afa89-149">**As**: Defines the name of your new field.</span></span>
    - <span data-ttu-id="afa89-150">**Bistaratu izena**: Zure eremuaren bistaratzeko izena definitzen du.</span><span class="sxs-lookup"><span data-stu-id="afa89-150">**Display name**: Defines the display name of your field.</span></span>

    > [!NOTE]
    > <span data-ttu-id="afa89-151">Zure negozio neurria zenbaki bakarreko entitate gisa gordeko da eta hemen agertuko da **Hasiera** orrialdea neurriari neurri gehiago gehitzen ez bazaio.</span><span class="sxs-lookup"><span data-stu-id="afa89-151">Your business measure will be saved as a single-number entity and will appear on the **Home** page unless you add more dimensions to your measure.</span></span> <span data-ttu-id="afa89-152">Neurri gehiago gehitu ondoren, neurriak hala egingo du *ez* erakutsi **Hasiera** orria.</span><span class="sxs-lookup"><span data-stu-id="afa89-152">After adding more dimensions, the measure will *not* show up on the **Home** page.</span></span>

13. <span data-ttu-id="afa89-153">Aukeran, gehitu funtzioak.</span><span class="sxs-lookup"><span data-stu-id="afa89-153">Optionally, add aggregation functions.</span></span> <span data-ttu-id="afa89-154">Zure neurrien erakundearen edo atributuaren barruan balio berri bat sortzen da.</span><span class="sxs-lookup"><span data-stu-id="afa89-154">Any aggregation that you create results in a new value within your Measures entity or attribute.</span></span> <span data-ttu-id="afa89-155">Onartutako agregazio funtzioak hauek dira: **Min**, **Max**, **Batez beste**, **mediana**, **batura**, **Kontu bakarra**, **Lehen** (dimentsioaren balio baten lehenengo erregistroa hartzen du), eta **Azken** (azken erregistroa neurri erantsiko balioa hartzen du).</span><span class="sxs-lookup"><span data-stu-id="afa89-155">Supported aggregation functions are: **Min**, **Max**, **Average**, **Median**, **Sum**, **Count Unique**, **First** (takes the first record of a dimension value), and **Last** (takes the last record added to a dimension value).</span></span>

14. <span data-ttu-id="afa89-156">Hautatu **Gorde** zure aldaketak neurriari aplikatzeko.</span><span class="sxs-lookup"><span data-stu-id="afa89-156">Select **Save** to apply your changes to the measure.</span></span>

## <a name="manage-your-measures"></a><span data-ttu-id="afa89-157">Kudeatu neurriak</span><span class="sxs-lookup"><span data-stu-id="afa89-157">Manage your measures</span></span>

<span data-ttu-id="afa89-158">Neurri bat gutxienez sortu ondoren, neurrien zerrenda ikusiko duzu **Neurriak** orrian.</span><span class="sxs-lookup"><span data-stu-id="afa89-158">After creating at least one measure, you'll see a list of measures on the **Measures** page.</span></span>

<span data-ttu-id="afa89-159">Neurri motaren inguruko informazioa aurkituko duzu, sortzailea, sortze data eta ordua, azken edizio data eta ordua, egoera (neurria aktiboa den ala ez, aktiboa ala huts egin) eta azken egunera eta ordua freskatzeko.</span><span class="sxs-lookup"><span data-stu-id="afa89-159">You'll find information about the measure type, the creator, creation date and time, last edit date and time, status (whether the measure is active, inactive, or failed), and last refresh date and time.</span></span> <span data-ttu-id="afa89-160">Zerrendako neurri bat hautatzen duzunean, bere irteeraren aurrebista ikus dezakezu.</span><span class="sxs-lookup"><span data-stu-id="afa89-160">When you select a measure from the list, you can see a preview of its output.</span></span>

<span data-ttu-id="afa89-161">Neurri guztiak aldi berean freskatzeko, hautatu **Freskatu guztiak** neurri zehatz bat aukeratu gabe.</span><span class="sxs-lookup"><span data-stu-id="afa89-161">To refresh all of your measures at the same time, select **Refresh all** without selecting a specific measure.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="afa89-162">![Neurri bakarrak kudeatzeko ekintzak](media/measure-actions.png "Neurri bakarrak kudeatzeko ekintzak")</span><span class="sxs-lookup"><span data-stu-id="afa89-162">![Actions to manage single measures](media/measure-actions.png "Actions to manage single measures")</span></span>

<span data-ttu-id="afa89-163">Bestela, hautatu zerrendako neurri bat eta egin ekintza hauetako bat:</span><span class="sxs-lookup"><span data-stu-id="afa89-163">Alternatively, select a measure from the list and perform one of the following actions:</span></span>

- <span data-ttu-id="afa89-164">Hautatu neurriaren izena, haren xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="afa89-164">Select the measure name to see its details.</span></span>
- <span data-ttu-id="afa89-165">**Editatu** neurriaren konfigurazioa.</span><span class="sxs-lookup"><span data-stu-id="afa89-165">**Edit** the configuration of the measure.</span></span>
- <span data-ttu-id="afa89-166">**Aldatu izena** neurria.</span><span class="sxs-lookup"><span data-stu-id="afa89-166">**Rename** the measure.</span></span>
- <span data-ttu-id="afa89-167">**Ezabatu** neurria.</span><span class="sxs-lookup"><span data-stu-id="afa89-167">**Delete** the measure.</span></span>
- <span data-ttu-id="afa89-168">Hautatu elipsia (...) eta gero **Freskatu** neurriaren freskatze prozesua hasteko.</span><span class="sxs-lookup"><span data-stu-id="afa89-168">Select the ellipsis (...) and then **Refresh** to start the refresh process for the measure.</span></span>
- <span data-ttu-id="afa89-169">Hautatu elipsia (...) eta gero **Deskargatu** neurriaren .CSV fitxategia lortzeko.</span><span class="sxs-lookup"><span data-stu-id="afa89-169">Select the ellipsis (...) and then **Download** to get a .CSV file of the measure.</span></span>

> [!TIP]
> <span data-ttu-id="afa89-170">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="afa89-170">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="afa89-171">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="afa89-171">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="afa89-172">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="afa89-172">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="afa89-173">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="afa89-173">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="next-step"></a><span data-ttu-id="afa89-174">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="afa89-174">Next step</span></span>

<span data-ttu-id="afa89-175">Lehendik dauden neurriak erabiltzen dituzu zure lehenengo bezero segmentua sortzeko **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="afa89-175">You cam use existing measures to create your first customer segment on the **Segments** page.</span></span> <span data-ttu-id="afa89-176">Informazio gehiago lortzeko, [Segmentuak](segments.md).</span><span class="sxs-lookup"><span data-stu-id="afa89-176">For more information, see [Segments](segments.md).</span></span>
