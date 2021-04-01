---
title: Sortu eta kudeatu neurriak
description: Zehaztu zure negozioaren errendimendua aztertzeko eta islatzeko neurriak.
ms.date: 02/02/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wameng
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 202ea22d290be04e54ce9676b6b693162354607f
ms.sourcegitcommit: d3eb07dcc72624a2d5cfc95c7ea9faaa2c1b6001
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "5654717"
---
# <a name="define-and-manage-measures"></a><span data-ttu-id="6b975-103">Neurriak zehaztu eta kudeatu</span><span class="sxs-lookup"><span data-stu-id="6b975-103">Define and manage measures</span></span>

<span data-ttu-id="6b975-104">Neurriek bezeroen portaerak eta negozioaren errendimendua hobeto ulertzen lagunduko dizute, balio garrantzitsuak eskuratuta [profil bateratuak](data-unification.md).</span><span class="sxs-lookup"><span data-stu-id="6b975-104">Measures help you to better understand customer behaviors and business performance by retrieving relevant values from [unified profiles](data-unification.md).</span></span> <span data-ttu-id="6b975-105">Adibidez, enpresa batek ikusi nahi du *bezero bakoitzeko guztizko gastua* bezero bakoitzaren erosketa historia ulertzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-105">For example, a business wants to see the *total spend per customer* to understand individual customer’s purchase history.</span></span> <span data-ttu-id="6b975-106">Bestela, neurria *enpresaren guztizko salmentak* negozio osoko diru-sarrera agregatuak ulertzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-106">Or measure *total sales of the company* to understand the aggregate-level revenue in the whole business.</span></span>  

<span data-ttu-id="6b975-107">Neurriak neurri-sortzailea, datuen kontsulta plataforma bat erabiltzen dute hainbat eragilerekin eta esleitzeko aukera sinpleekin.</span><span class="sxs-lookup"><span data-stu-id="6b975-107">Measures are created using the measure builder, a data query platform with various operators and simple mapping options.</span></span> <span data-ttu-id="6b975-108">Datuak iragazteko, taldekatzeko emaitzak, detektatzeko aukera ematen du [entitate harreman bideak](relationships.md), eta irteera aurreikusi.</span><span class="sxs-lookup"><span data-stu-id="6b975-108">It lets you filter the data, group results, detect [entity relationship paths](relationships.md), and preview the output.</span></span>

<span data-ttu-id="6b975-109">Erabili neurri-sortzailea negozio-jarduerak planifikatzeko bezeroen datuak kontsultatuz eta estatistikak aterata.</span><span class="sxs-lookup"><span data-stu-id="6b975-109">Use the measure builder to plan business activities by querying customer data and extract insights.</span></span> <span data-ttu-id="6b975-110">Adibidez, neurri bat sortzea *bezero bakoitzeko guztizko gastua* eta *bezeroaren itzulketa osoa* gastu handia baina errentagarritasuna handia duten bezero talde bat identifikatzen laguntzen du.</span><span class="sxs-lookup"><span data-stu-id="6b975-110">For example, creating a measure of *total spend per customer* and *total return per customer* helps identify a group of customers with high spend yet high return.</span></span> <span data-ttu-id="6b975-111">[Segmentu bat sor](segments.md) dezakezu hurrengo ekintza onenak gidatzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-111">You can [create a segment](segments.md) to drive next best actions.</span></span> 

## <a name="create-a-measure"></a><span data-ttu-id="6b975-112">Sortu neurri bat</span><span class="sxs-lookup"><span data-stu-id="6b975-112">Create a measure</span></span>

<span data-ttu-id="6b975-113">Atal honek hutsetik neurri berri bat sortzen lagunduko dizu.</span><span class="sxs-lookup"><span data-stu-id="6b975-113">This section walks you through creating a new measure from scratch.</span></span> <span data-ttu-id="6b975-114">Neurri bat bezeroaren entitatearekin konektatzeko konfiguratuta dauden datu-entitateetako datu-atributuekin eraiki dezakezu.</span><span class="sxs-lookup"><span data-stu-id="6b975-114">You can build a measure with data attributes from data entities that have a relationship set up to connect with the Customer entity.</span></span> 

1. <span data-ttu-id="6b975-115">Hartzaileei buruzko xehetasunetan, joan hona: **Neurriak**.</span><span class="sxs-lookup"><span data-stu-id="6b975-115">In audience insights, go to **Measures**.</span></span>

1. <span data-ttu-id="6b975-116">Hautatu **Berria**.</span><span class="sxs-lookup"><span data-stu-id="6b975-116">Select **New**.</span></span>

1. <span data-ttu-id="6b975-117">Aukeratu **Editatu izena** eta eman **Izena** neurrian.</span><span class="sxs-lookup"><span data-stu-id="6b975-117">Select **Edit name** and provide a **Name** for the measure.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="6b975-118">Zure neurri konfigurazio berriak bi eremu besterik ez baditu, adibidez, Bezero IDa eta kalkulu bakarra, irteera zutabe berri gisa gehituko zaio Bezeroaren neurria izeneko sistemak sortutako entitateari.</span><span class="sxs-lookup"><span data-stu-id="6b975-118">If your new measure configuration has only two fields, for exmample, CustomerID and one calculation, the output will be added as a new column to the system generated entity called Customer_Measure.</span></span> <span data-ttu-id="6b975-119">Gainera, neurriaren balioa bezeroaren profil bateratuan ikusi ahal izango duzu.</span><span class="sxs-lookup"><span data-stu-id="6b975-119">And you will be able to see the measure’s value in the unified customer profile.</span></span> <span data-ttu-id="6b975-120">Beste neurri batzuek beren entitateak sortuko dituzte.</span><span class="sxs-lookup"><span data-stu-id="6b975-120">Other measures will generate their own entities.</span></span>

1. <span data-ttu-id="6b975-121">Konfigurazio eremuan, aukeratu agregazio funtzioa **Aukeratu Funtzioa** goitibeherako menua.</span><span class="sxs-lookup"><span data-stu-id="6b975-121">In the configuration area, choose the aggregation function from the **Select Function** drop-down menu.</span></span> <span data-ttu-id="6b975-122">Agregazio funtzioek honako hauek dituzte:</span><span class="sxs-lookup"><span data-stu-id="6b975-122">Aggregation functions include:</span></span> 
   - <span data-ttu-id="6b975-123">**Sum**</span><span class="sxs-lookup"><span data-stu-id="6b975-123">**Sum**</span></span>
   - <span data-ttu-id="6b975-124">**Batez bestekoa**</span><span class="sxs-lookup"><span data-stu-id="6b975-124">**Average**</span></span>
   - <span data-ttu-id="6b975-125">**Kontaketa**</span><span class="sxs-lookup"><span data-stu-id="6b975-125">**Count**</span></span>
   - <span data-ttu-id="6b975-126">**Kontaketa bakarra**</span><span class="sxs-lookup"><span data-stu-id="6b975-126">**Count Unique**</span></span>
   - <span data-ttu-id="6b975-127">**Gehienekoa**</span><span class="sxs-lookup"><span data-stu-id="6b975-127">**Max**</span></span>
   - <span data-ttu-id="6b975-128">**Min**</span><span class="sxs-lookup"><span data-stu-id="6b975-128">**Min**</span></span>
   - <span data-ttu-id="6b975-129">**Lehenengoa**: datuen erregistroaren lehen balioa hartzen du</span><span class="sxs-lookup"><span data-stu-id="6b975-129">**First**: takes the first value of the data record</span></span>
   - <span data-ttu-id="6b975-130">**Azkena**: datuen erregistroan gehitu den azken balioa hartzen du</span><span class="sxs-lookup"><span data-stu-id="6b975-130">**Last**: takes the last value that was added to the data record</span></span>

   :::image type="content" source="media/measure-operators.png" alt-text="Neurriak kalkulatzeko operadoreak.":::

1. <span data-ttu-id="6b975-132">Aukeratu **Gehitu atributua** neurri hau sortzeko behar dituzun datuak hautatzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-132">Select **Add attribute** to select the data you need to create this measure.</span></span>
   
   1. <span data-ttu-id="6b975-133">Hautatu **Atributuak** fitxa.</span><span class="sxs-lookup"><span data-stu-id="6b975-133">Select the **Attributes** tab.</span></span> 
   1. <span data-ttu-id="6b975-134">Datu-entitatea: aukeratu neurtu nahi duzun atributua biltzen duen entitatea.</span><span class="sxs-lookup"><span data-stu-id="6b975-134">Data entity: Choose the entity that includes the attribute you want to measure.</span></span> 
   1. <span data-ttu-id="6b975-135">Datuen atributua: aukeratu neurria kalkulatzeko agregazio funtzioan erabili nahi duzun atributua.</span><span class="sxs-lookup"><span data-stu-id="6b975-135">Data attribute: Choose the attribute you want to use in the aggregation function to calculate the measure.</span></span> <span data-ttu-id="6b975-136">Aldi berean atributu bat besterik ezin duzu hautatu.</span><span class="sxs-lookup"><span data-stu-id="6b975-136">You can only select one attribute at a time.</span></span>
   1. <span data-ttu-id="6b975-137">Dagoen neurri batetik datuen atributu bat ere hauta dezakezu **Neurriak** fitxa. Edo entitatearen edo neurketaren izena bila dezakezu.</span><span class="sxs-lookup"><span data-stu-id="6b975-137">You can also select a data attribute from an existing measure by selecting the **Measures** tab. Or, you can search for an entity or measure name.</span></span> 
   1. <span data-ttu-id="6b975-138">Aukeratu **Gehitu** hautatutako atributua neurrira gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-138">Select **Add** to add the selected attribute to the measure.</span></span>

   :::image type="content" source="media/measure-attribute-selection.png" alt-text="Aukeratu kalkuluetan erabiltzeko atributu bat.":::

1. <span data-ttu-id="6b975-140">Neurri konplexuagoak eraikitzeko, atributu gehiago gehi ditzakezu edo kalkulu-operadoreak erabil ditzakezu neurri funtzioan.</span><span class="sxs-lookup"><span data-stu-id="6b975-140">To build more complex measures, you can add more attributes or use math operators on your measure function.</span></span>

   :::image type="content" source="media/measure-math-operators.png" alt-text="Sortu neurri konplexua kalkulu-eragileekin.":::

1. <span data-ttu-id="6b975-142">Iragazkiak gehitzeko, hautatu **Iragazi** konfigurazio-eremuan.</span><span class="sxs-lookup"><span data-stu-id="6b975-142">To add filters, select the **Filter** in the configuration area.</span></span> 
  
   1. <span data-ttu-id="6b975-143">**Gehitu atributua** ataleko **Iragazkiak** panelean, hautatu iragazkiak sortzeko erabili nahi duzun atributua.</span><span class="sxs-lookup"><span data-stu-id="6b975-143">In **Add attribute** section of the **Filters** pane, select the attribute you want to use to create filters.</span></span>
   1. <span data-ttu-id="6b975-144">Ezarri iragazkien eragileak hautatutako atributu bakoitzaren iragazkia definitzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-144">Set the filter operators to define the filter for every selected attribute.</span></span>
   1. <span data-ttu-id="6b975-145">Aukeratu **Aplikatu** hautatutako atributua neurrira gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-145">Select **Apply** to add the filters to the measure.</span></span>

1. <span data-ttu-id="6b975-146">Dimentsioak gehitzeko, hautatu **Dimentsioa** konfigurazio-eremuan.</span><span class="sxs-lookup"><span data-stu-id="6b975-146">To add dimensions, select **Dimension** in the configuration area.</span></span> <span data-ttu-id="6b975-147">Dimentsioak irteerako entitateko zutabe gisa agertuko dira.</span><span class="sxs-lookup"><span data-stu-id="6b975-147">Dimensions will show as columns in the measure output entity.</span></span>
   1. <span data-ttu-id="6b975-148">Aukeratu **Editatu dimentsioak** neurriaren balioak taldekatu nahi dituzun datu atributuak gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-148">Select **Edit dimensions** to add data attributes you want to group the measure values by.</span></span> <span data-ttu-id="6b975-149">Adibidez, hiria edo generoa.</span><span class="sxs-lookup"><span data-stu-id="6b975-149">For example, city or gender.</span></span> <span data-ttu-id="6b975-150">Lehenespenez, *Bezeroaren IDa* dimentsioa hautatzeko hautatzen da *bezero-mailako neurriak*.</span><span class="sxs-lookup"><span data-stu-id="6b975-150">By default, the *CustomerID* dimension is selected to create *customer-level measures*.</span></span> <span data-ttu-id="6b975-151">Neurri lehenetsia kendu dezakezu sortu nahi baduzu *negozio-mailako neurriak*.</span><span class="sxs-lookup"><span data-stu-id="6b975-151">You can remove the default dimension if you want to create *business-level measures*.</span></span>
   1. <span data-ttu-id="6b975-152">Aukeratu **Eginda** hautatutako atributua neurrira gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-152">Select **Done** to add the dimensions to the measure.</span></span>

1. <span data-ttu-id="6b975-153">Esleitutako datu-entitatearen eta *Bezero* entitatearen artean bide anitz badaude, identifikatutako bat aukeratu behar duzu [entitate erlazio-bideak](relationships.md).</span><span class="sxs-lookup"><span data-stu-id="6b975-153">If there are multiple paths between the data entity you mapped and the *Customer* entity, you have to choose one of the identified [entity relationship paths](relationships.md).</span></span> <span data-ttu-id="6b975-154">Neurriaren emaitzak hautatutako bidearen arabera alda daitezke.</span><span class="sxs-lookup"><span data-stu-id="6b975-154">Measure results can vary depending on the selected path.</span></span> 
   1. <span data-ttu-id="6b975-155">Aukeratu **Datuen hobespenak** eta aukeratu zure neurria identifikatzeko erabili beharreko entitate bidea.</span><span class="sxs-lookup"><span data-stu-id="6b975-155">Select **Data preferences** and choose the entity path that should be used to identify your measure.</span></span> <span data-ttu-id="6b975-156">Bide bakarra bada *Bezeroa* entitatea, kontrol hau ez da erakutsiko.</span><span class="sxs-lookup"><span data-stu-id="6b975-156">If there's only a single path to the *Customer* entity, this control won't show.</span></span>
   1. <span data-ttu-id="6b975-157">Aukeratu **Eginda** zure hautaketa aplikatzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-157">Select **Done** to apply your selection.</span></span> 

   :::image type="content" source="media/measures-data-preferences.png" alt-text="Hautatu neurriaren entitatearen bide-izena.":::

1. <span data-ttu-id="6b975-159">Neurriaren kalkulu gehiago gehitzeko, hautatu **Kalkulu berria**.</span><span class="sxs-lookup"><span data-stu-id="6b975-159">To add more calculations for the measure, select **New calculation**.</span></span> <span data-ttu-id="6b975-160">Entitate bide bereko entitateak soilik erabil ditzakezu kalkulu berrietarako.</span><span class="sxs-lookup"><span data-stu-id="6b975-160">You can only use entities on the same entity path for new calculations.</span></span> <span data-ttu-id="6b975-161">Kalkulu gehiago irteerako entitateko zutabe berri gisa agertuko dira.</span><span class="sxs-lookup"><span data-stu-id="6b975-161">More calculations will show as new columns in the measure output entity.</span></span>

1. <span data-ttu-id="6b975-162">Aukeratu **...** kalkuluan balioa **Bikoizteko**, **Izena aldatzeko** edo **Kentzeko** neurri batetik.</span><span class="sxs-lookup"><span data-stu-id="6b975-162">Select **...** on the calculation to **Duplicate**, **Rename**, or **Remove** a calculation from a measure.</span></span>

1. <span data-ttu-id="6b975-163">**Aurrebista** eremuan, neurketaren irteerako entitatearen datu-eskema ikusiko duzu, iragazkiak eta neurriak barne.</span><span class="sxs-lookup"><span data-stu-id="6b975-163">In the **Preview** area, you'll see the data schema of the measure output entity, including filters and dimensions.</span></span> <span data-ttu-id="6b975-164">Aurrebistak dinamikoki erreakzionatzen du konfigurazioko aldaketen aurrean.</span><span class="sxs-lookup"><span data-stu-id="6b975-164">The preview reacts dynamically to changes in the configuration.</span></span>

1. <span data-ttu-id="6b975-165">Aukeratu **Exekutatu** konfiguratutako neurriaren emaitzak kalkulatzeko.</span><span class="sxs-lookup"><span data-stu-id="6b975-165">Select **Run** to calculate results for the configured measure.</span></span> <span data-ttu-id="6b975-166">Aukeratu **Gorde eta itxi** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu.</span><span class="sxs-lookup"><span data-stu-id="6b975-166">Select **Save and close** if you want to keep the current configuration and run the measure later.</span></span>

1. <span data-ttu-id="6b975-167">Joan **Neurriak** atalera sortu berri den neurria zerrendan ikusteko.</span><span class="sxs-lookup"><span data-stu-id="6b975-167">Go to **Measures** to see the newly created measure in the list.</span></span>

## <a name="manage-your-measures"></a><span data-ttu-id="6b975-168">Kudeatu neurriak</span><span class="sxs-lookup"><span data-stu-id="6b975-168">Manage your measures</span></span>

<span data-ttu-id="6b975-169">[Neurri bat sortu](#create-a-measure) ondoren, neurrien zerrenda ikusiko duzu **Neurriak** orrian.</span><span class="sxs-lookup"><span data-stu-id="6b975-169">After [creating a measure](#create-a-measure), you see a list of measures on the **Measures** page.</span></span>

<span data-ttu-id="6b975-170">Neurri motari, sortzaileari, sortze datari, egoerari eta egoerari buruzko informazioa aurkituko duzu.</span><span class="sxs-lookup"><span data-stu-id="6b975-170">You'll find information about the measure type, the creator, creation date, status, and state.</span></span> <span data-ttu-id="6b975-171">Zerrendako neurri bat hautatzen duzunean, irteera aurreikusi eta .CSV fitxategia deskarga dezakezu.</span><span class="sxs-lookup"><span data-stu-id="6b975-171">When you select a measure from the list, you can preview the output and download a .CSV file.</span></span>

<span data-ttu-id="6b975-172">Neurri guztiak aldi berean freskatzeko, hautatu **Freskatu guztiak** neurri zehatz bat aukeratu gabe.</span><span class="sxs-lookup"><span data-stu-id="6b975-172">To refresh all of your measures at the same time, select **Refresh all** without selecting a specific measure.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="6b975-173">![Neurri bakarrak kudeatzeko ekintzak](media/measure-actions.png "Neurri bakarrak kudeatzeko ekintzak")</span><span class="sxs-lookup"><span data-stu-id="6b975-173">![Actions to manage single measures](media/measure-actions.png "Actions to manage single measures")</span></span>

<span data-ttu-id="6b975-174">Aukeratu neurri bat zerrendan aukera hauetarako:</span><span class="sxs-lookup"><span data-stu-id="6b975-174">Select a measure from the list for the following options:</span></span>

- <span data-ttu-id="6b975-175">Hautatu neurriaren izena, haren xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="6b975-175">Select the measure name to see its details.</span></span>
- <span data-ttu-id="6b975-176">**Editatu** neurriaren konfigurazioa.</span><span class="sxs-lookup"><span data-stu-id="6b975-176">**Edit** the configuration of the measure.</span></span>
- <span data-ttu-id="6b975-177">**Freskatu** neurria azken datuetan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="6b975-177">**Refresh** the measure based on the latest data.</span></span>
- <span data-ttu-id="6b975-178">**Aldatu izena** neurria.</span><span class="sxs-lookup"><span data-stu-id="6b975-178">**Rename** the measure.</span></span>
- <span data-ttu-id="6b975-179">**Ezabatu** neurria.</span><span class="sxs-lookup"><span data-stu-id="6b975-179">**Delete** the measure.</span></span>
- <span data-ttu-id="6b975-180">**Aktibatu** edo **Desaktibatu**.</span><span class="sxs-lookup"><span data-stu-id="6b975-180">**Activate** or **Deactivate**.</span></span> <span data-ttu-id="6b975-181">Neurri inaktiboak ez dira freskatuko [freskatze programatuan](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="6b975-181">Inactive measures won't get refreshed during a [scheduled refresh](system.md#schedule-tab).</span></span>

> [!TIP]
> <span data-ttu-id="6b975-182">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="6b975-182">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="6b975-183">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="6b975-183">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="6b975-184">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="6b975-184">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="6b975-185">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="6b975-185">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="next-step"></a><span data-ttu-id="6b975-186">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="6b975-186">Next step</span></span>

<span data-ttu-id="6b975-187">Sortzeko dauden neurriak erabiltzen dituzu [bezero segmentu bat](segments.md).</span><span class="sxs-lookup"><span data-stu-id="6b975-187">You cam use existing measures to create [a customer segment](segments.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]