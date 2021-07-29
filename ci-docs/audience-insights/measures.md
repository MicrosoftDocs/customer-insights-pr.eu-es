---
title: Sortu eta kudeatu neurriak
description: Zehaztu zure negozioaren errendimendua aztertzeko eta islatzeko neurriak.
ms.date: 04/12/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wameng
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: a83caf2428f3dbd9791b9f746d00d370362a508c
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304774"
---
# <a name="define-and-manage-measures"></a><span data-ttu-id="7286a-103">Neurriak zehaztu eta kudeatu</span><span class="sxs-lookup"><span data-stu-id="7286a-103">Define and manage measures</span></span>

<span data-ttu-id="7286a-104">Neurriek bezeroen portaerak eta negozioaren errendimendua hobeto ulertzen lagunduko dizute.</span><span class="sxs-lookup"><span data-stu-id="7286a-104">Measures help you to better understand customer behaviors and business performance.</span></span> <span data-ttu-id="7286a-105">Balio garrantzitsuak aztertzen dituzte [profil bateratuak](data-unification.md).</span><span class="sxs-lookup"><span data-stu-id="7286a-105">They look at relevant values from [unified profiles](data-unification.md).</span></span> <span data-ttu-id="7286a-106">Adibidez, enpresa batek ikusi nahi du *bezero bakoitzeko guztizko gastua* bezero bakoitzaren erosketa historia edo neurria ulertzeko *enpresaren guztizko salmentak* negozio osoko diru-sarrera agregatuak ulertzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-106">For example, a business wants to see the *total spend per customer* to understand an individual customer’s purchase history or measure *total sales of the company* to understand the aggregate-level revenue in the whole business.</span></span>  

<span data-ttu-id="7286a-107">Neurriak neurri-sortzailea, datuen kontsulta plataforma bat erabiltzen dute hainbat eragilerekin eta esleitzeko aukera sinpleekin.</span><span class="sxs-lookup"><span data-stu-id="7286a-107">Measures are created using the measure builder, a data query platform with various operators and simple mapping options.</span></span> <span data-ttu-id="7286a-108">Datuak iragazteko, taldekatzeko emaitzak, detektatzeko aukera ematen du [entitate harreman bideak](relationships.md), eta irteera aurreikusi.</span><span class="sxs-lookup"><span data-stu-id="7286a-108">It lets you filter the data, group results, detect [entity relationship paths](relationships.md), and preview the output.</span></span>

<span data-ttu-id="7286a-109">Erabili neurri-sortzailea negozio-jarduerak planifikatzeko bezeroen datuak kontsultatuz eta estatistikak aterata.</span><span class="sxs-lookup"><span data-stu-id="7286a-109">Use the measure builder to plan business activities by querying customer data and extract insights.</span></span> <span data-ttu-id="7286a-110">Adibidez, neurri bat sortzea *bezero bakoitzeko guztizko gastua* eta *bezeroaren itzulketa osoa* gastu handia baina errentagarritasuna handia duten bezero talde bat identifikatzen laguntzen du.</span><span class="sxs-lookup"><span data-stu-id="7286a-110">For example, creating a measure of *total spend per customer* and *total return per customer* helps identify a group of customers with high spend yet high return.</span></span> <span data-ttu-id="7286a-111">[Segmentu bat sor](segments.md) dezakezu hurrengo ekintza onenak gidatzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-111">You can [create a segment](segments.md) to drive next best actions.</span></span> 

## <a name="build-your-own-measure-from-scratch"></a><span data-ttu-id="7286a-112">Eraiki zure neurketa hutsetik</span><span class="sxs-lookup"><span data-stu-id="7286a-112">Build your own measure from scratch</span></span>

<span data-ttu-id="7286a-113">Atal honek hutsetik neurri berri bat sortzen lagunduko dizu.</span><span class="sxs-lookup"><span data-stu-id="7286a-113">This section walks you through creating a new measure from scratch.</span></span> <span data-ttu-id="7286a-114">Neurri bat bezeroaren entitatearekin konektatzeko konfiguratuta dauden datu-entitateetako datu-atributuekin eraiki dezakezu.</span><span class="sxs-lookup"><span data-stu-id="7286a-114">You can build a measure with data attributes from data entities that have a relationship set up to connect with the Customer entity.</span></span> 

1. <span data-ttu-id="7286a-115">Hartzaileei buruzko xehetasunetan, joan hona: **Neurriak**.</span><span class="sxs-lookup"><span data-stu-id="7286a-115">In audience insights, go to **Measures**.</span></span>

1. <span data-ttu-id="7286a-116">Aukeratu **Berria** eta aukeratu **Eraiki zeurea**.</span><span class="sxs-lookup"><span data-stu-id="7286a-116">Select **New** and choose **Build your own**.</span></span>

1. <span data-ttu-id="7286a-117">Aukeratu **Editatu izena** eta eman **Izena** neurrian.</span><span class="sxs-lookup"><span data-stu-id="7286a-117">Select **Edit name** and provide a **Name** for the measure.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="7286a-118">Zure neurri konfigurazio berriak bi eremu besterik ez baditu, adibidez, CustomerID eta kalkulu bakarra, irteera zutabe berri gisa gehituko zaio Customer_Measure izeneko sistemak sortutako entitateari.</span><span class="sxs-lookup"><span data-stu-id="7286a-118">If your new measure configuration has only two fields—for example, CustomerID and one calculation—the output will be added as a new column to the system-generated entity called Customer_Measure.</span></span> <span data-ttu-id="7286a-119">Gainera, neurriaren balioa bezeroaren profil bateratuan ikusi ahal izango duzu.</span><span class="sxs-lookup"><span data-stu-id="7286a-119">And you will be able to see the measure’s value in the unified customer profile.</span></span> <span data-ttu-id="7286a-120">Beste neurri batzuek beren entitateak sortuko dituzte.</span><span class="sxs-lookup"><span data-stu-id="7286a-120">Other measures will generate their own entities.</span></span>

1. <span data-ttu-id="7286a-121">Konfigurazio eremuan, aukeratu agregazio funtzioa **Aukeratu Funtzioa** goitibeherako menua.</span><span class="sxs-lookup"><span data-stu-id="7286a-121">In the configuration area, choose the aggregation function from the **Select Function** dropdown menu.</span></span> <span data-ttu-id="7286a-122">Agregazio funtzioek honako hauek dituzte:</span><span class="sxs-lookup"><span data-stu-id="7286a-122">Aggregation functions include:</span></span> 
   - <span data-ttu-id="7286a-123">**Sum**</span><span class="sxs-lookup"><span data-stu-id="7286a-123">**Sum**</span></span>
   - <span data-ttu-id="7286a-124">**Batez bestekoa**</span><span class="sxs-lookup"><span data-stu-id="7286a-124">**Average**</span></span>
   - <span data-ttu-id="7286a-125">**Kontaketa**</span><span class="sxs-lookup"><span data-stu-id="7286a-125">**Count**</span></span>
   - <span data-ttu-id="7286a-126">**Kontaketa bakarra**</span><span class="sxs-lookup"><span data-stu-id="7286a-126">**Count Unique**</span></span>
   - <span data-ttu-id="7286a-127">**Gehienekoa**</span><span class="sxs-lookup"><span data-stu-id="7286a-127">**Max**</span></span>
   - <span data-ttu-id="7286a-128">**Min**</span><span class="sxs-lookup"><span data-stu-id="7286a-128">**Min**</span></span>
   - <span data-ttu-id="7286a-129">**Lehenengoa**: datuen erregistroaren lehen balioa hartzen du</span><span class="sxs-lookup"><span data-stu-id="7286a-129">**First**: takes the first value of the data record</span></span>
   - <span data-ttu-id="7286a-130">**Azkena**: datuen erregistroan gehitu den azken balioa hartzen du</span><span class="sxs-lookup"><span data-stu-id="7286a-130">**Last**: takes the last value that was added to the data record</span></span>

   :::image type="content" source="media/measure-operators.png" alt-text="Neurriak kalkulatzeko operadoreak.":::

1. <span data-ttu-id="7286a-132">Aukeratu **Gehitu atributua** neurri hau sortzeko behar dituzun datuak hautatzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-132">Select **Add attribute** to select the data you need to create this measure.</span></span>
   
   1. <span data-ttu-id="7286a-133">Hautatu **Atributuak** fitxa.</span><span class="sxs-lookup"><span data-stu-id="7286a-133">Select the **Attributes** tab.</span></span> 
   1. <span data-ttu-id="7286a-134">Datu-entitatea: aukeratu neurtu nahi duzun atributua biltzen duen entitatea.</span><span class="sxs-lookup"><span data-stu-id="7286a-134">Data entity: Choose the entity that includes the attribute you want to measure.</span></span> 
   1. <span data-ttu-id="7286a-135">Datuen atributua: aukeratu neurria kalkulatzeko agregazio funtzioan erabili nahi duzun atributua.</span><span class="sxs-lookup"><span data-stu-id="7286a-135">Data attribute: Choose the attribute you want to use in the aggregation function to calculate the measure.</span></span> <span data-ttu-id="7286a-136">Aldi berean atributu bat besterik ezin duzu hautatu.</span><span class="sxs-lookup"><span data-stu-id="7286a-136">You can only select one attribute at a time.</span></span>
   1. <span data-ttu-id="7286a-137">Dagoen neurri batetik datuen atributu bat ere hauta dezakezu **Neurriak** fitxa. Edo entitatearen edo neurketaren izena bila dezakezu.</span><span class="sxs-lookup"><span data-stu-id="7286a-137">You can also select a data attribute from an existing measure by selecting the **Measures** tab. Or, you can search for an entity or measure name.</span></span> 
   1. <span data-ttu-id="7286a-138">Aukeratu **Gehitu** hautatutako atributua neurrira gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-138">Select **Add** to add the selected attribute to the measure.</span></span>

   :::image type="content" source="media/measure-attribute-selection.png" alt-text="Aukeratu kalkuluetan erabiltzeko atributu bat.":::

1. <span data-ttu-id="7286a-140">Neurri konplexuagoak eraikitzeko, atributu gehiago gehi ditzakezu edo kalkulu-operadoreak erabil ditzakezu neurri funtzioan.</span><span class="sxs-lookup"><span data-stu-id="7286a-140">To build more complex measures, you can add more attributes or use math operators on your measure function.</span></span>

   :::image type="content" source="media/measure-math-operators.png" alt-text="Sortu neurri konplexua kalkulu-eragileekin.":::

1. <span data-ttu-id="7286a-142">Iragazkiak gehitzeko, hautatu **Iragazi** konfigurazio-eremuan.</span><span class="sxs-lookup"><span data-stu-id="7286a-142">To add filters, select the **Filter** in the configuration area.</span></span> 
  
   1. <span data-ttu-id="7286a-143">Urtean **Gehitu atributua** ataleko **Iragazkiak** panelean, hautatu iragazkiak sortzeko erabili nahi duzun atributua.</span><span class="sxs-lookup"><span data-stu-id="7286a-143">In the **Add attribute** section of the **Filters** pane, select the attribute you want to use to create filters.</span></span>
   1. <span data-ttu-id="7286a-144">Ezarri iragazkien eragileak hautatutako atributu bakoitzaren iragazkia definitzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-144">Set the filter operators to define the filter for every selected attribute.</span></span>
   1. <span data-ttu-id="7286a-145">Aukeratu **Aplikatu** hautatutako atributua neurrira gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-145">Select **Apply** to add the filters to the measure.</span></span>

1. <span data-ttu-id="7286a-146">Dimentsioak gehitzeko, hautatu **Dimentsioa** konfigurazio-eremuan.</span><span class="sxs-lookup"><span data-stu-id="7286a-146">To add dimensions, select **Dimension** in the configuration area.</span></span> <span data-ttu-id="7286a-147">Dimentsioak irteerako entitateko zutabe gisa agertuko dira.</span><span class="sxs-lookup"><span data-stu-id="7286a-147">Dimensions will show as columns in the measure output entity.</span></span>
 
   1. <span data-ttu-id="7286a-148">Aukeratu **Editatu dimentsioak** neurriaren balioak taldekatu nahi dituzun datu atributuak gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-148">Select **Edit dimensions** to add data attributes you want to group the measure values by.</span></span> <span data-ttu-id="7286a-149">Adibidez, hiria edo generoa.</span><span class="sxs-lookup"><span data-stu-id="7286a-149">For example, city or gender.</span></span> <span data-ttu-id="7286a-150">Lehenespenez, *Bezeroaren IDa* dimentsioa hautatzeko hautatzen da *bezero-mailako neurriak*.</span><span class="sxs-lookup"><span data-stu-id="7286a-150">By default, the *CustomerID* dimension is selected to create *customer-level measures*.</span></span> <span data-ttu-id="7286a-151">Neurri lehenetsia kendu dezakezu sortu nahi baduzu *negozio-mailako neurriak*.</span><span class="sxs-lookup"><span data-stu-id="7286a-151">You can remove the default dimension if you want to create *business-level measures*.</span></span>
   1. <span data-ttu-id="7286a-152">Aukeratu **Eginda** hautatutako atributua neurrira gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-152">Select **Done** to add the dimensions to the measure.</span></span>

1. <span data-ttu-id="7286a-153">Zure datuetan zenbaki oso batekin ordezkatu behar dituzun balioak badaude, adibidez *nulua* hurrengoarekin *0*, hautatu **Arauak**.</span><span class="sxs-lookup"><span data-stu-id="7286a-153">If there are values in your data that you need to replace with an integer—for example, replace *null* with *0*—select **Rules**.</span></span> <span data-ttu-id="7286a-154">Konfiguratu araua eta ziurtatu ordezko gisa zenbaki osoak bakarrik aukeratzen dituzula.</span><span class="sxs-lookup"><span data-stu-id="7286a-154">Configure the rule and make sure that you choose only whole numbers as replacements.</span></span>

1. <span data-ttu-id="7286a-155">Esleitutako datu-entitatearen eta *Bezero* entitatearen artean bide anitz badaude, identifikatutako bat aukeratu behar duzu [entitate erlazio-bideak](relationships.md).</span><span class="sxs-lookup"><span data-stu-id="7286a-155">If there are multiple paths between the data entity you mapped and the *Customer* entity, you have to choose one of the identified [entity relationship paths](relationships.md).</span></span> <span data-ttu-id="7286a-156">Neurriaren emaitzak hautatutako bidearen arabera alda daitezke.</span><span class="sxs-lookup"><span data-stu-id="7286a-156">Measure results can vary depending on the selected path.</span></span> 
   
   1. <span data-ttu-id="7286a-157">Aukeratu **Datuen hobespenak** eta aukeratu zure neurria identifikatzeko erabili beharreko entitate bidea.</span><span class="sxs-lookup"><span data-stu-id="7286a-157">Select **Data preferences** and choose the entity path that should be used to identify your measure.</span></span> <span data-ttu-id="7286a-158">Bide bakarra bada *Bezeroa* entitatea, kontrol hau ez da erakutsiko.</span><span class="sxs-lookup"><span data-stu-id="7286a-158">If there's only a single path to the *Customer* entity, this control won't show.</span></span>
   1. <span data-ttu-id="7286a-159">Aukeratu **Eginda** zure hautaketa aplikatzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-159">Select **Done** to apply your selection.</span></span> 

   :::image type="content" source="media/measures-data-preferences.png" alt-text="Hautatu neurriaren entitatearen bide-izena.":::

1. <span data-ttu-id="7286a-161">Neurriaren kalkulu gehiago gehitzeko, hautatu **Kalkulu berria**.</span><span class="sxs-lookup"><span data-stu-id="7286a-161">To add more calculations for the measure, select **New calculation**.</span></span> <span data-ttu-id="7286a-162">Entitate bide bereko entitateak soilik erabil ditzakezu kalkulu berrietarako.</span><span class="sxs-lookup"><span data-stu-id="7286a-162">You can only use entities on the same entity path for new calculations.</span></span> <span data-ttu-id="7286a-163">Kalkulu gehiago irteerako entitateko zutabe berri gisa agertuko dira.</span><span class="sxs-lookup"><span data-stu-id="7286a-163">More calculations will show as new columns in the measure output entity.</span></span>

1. <span data-ttu-id="7286a-164">Aukeratu **...** kalkuluan balioa **Bikoizteko**, **Izena aldatzeko** edo **Kentzeko** neurri batetik.</span><span class="sxs-lookup"><span data-stu-id="7286a-164">Select **...** on the calculation to **Duplicate**, **Rename**, or **Remove** a calculation from a measure.</span></span>

1. <span data-ttu-id="7286a-165">**Aurrebista** eremuan, neurketaren irteerako entitatearen datu-eskema ikusiko duzu, iragazkiak eta neurriak barne.</span><span class="sxs-lookup"><span data-stu-id="7286a-165">In the **Preview** area, you'll see the data schema of the measure output entity, including filters and dimensions.</span></span> <span data-ttu-id="7286a-166">Aurrebistak dinamikoki erreakzionatzen du konfigurazioko aldaketen aurrean.</span><span class="sxs-lookup"><span data-stu-id="7286a-166">The preview reacts dynamically to changes in the configuration.</span></span>

1. <span data-ttu-id="7286a-167">Aukeratu **Exekutatu** konfiguratutako neurriaren emaitzak kalkulatzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-167">Select **Run** to calculate results for the configured measure.</span></span> <span data-ttu-id="7286a-168">Aukeratu **Gorde eta itxi** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu.</span><span class="sxs-lookup"><span data-stu-id="7286a-168">Select **Save and close** if you want to keep the current configuration and run the measure later.</span></span>

1. <span data-ttu-id="7286a-169">Joan **Neurriak** atalera sortu berri den neurria zerrendan ikusteko.</span><span class="sxs-lookup"><span data-stu-id="7286a-169">Go to **Measures** to see the newly created measure in the list.</span></span>

## <a name="use-a-template-to-build-a-measure"></a><span data-ttu-id="7286a-170">Erabili txantiloia neurri bat eraikitzeko</span><span class="sxs-lookup"><span data-stu-id="7286a-170">Use a template to build a measure</span></span>

<span data-ttu-id="7286a-171">Normalean erabiltzen diren neurrien aurrez definitutako txantiloiak erabil ditzakezu horiek sortzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-171">You can use predefined templates of commonly used measures to create them.</span></span> <span data-ttu-id="7286a-172">Txantiloien deskribapen zehatzak eta esperientzia gidatu batek neurrien sorrera eraginkorra izaten laguntzen dizute.</span><span class="sxs-lookup"><span data-stu-id="7286a-172">Detailed descriptions of the templates and a guided experience help you with efficient measure creation.</span></span> <span data-ttu-id="7286a-173">Txantiloiak mapako datuen gainean eraikitzen dira *Jarduera bateratua* entitatea.</span><span class="sxs-lookup"><span data-stu-id="7286a-173">Templates build on mapped data from the *Unified Activity* entity.</span></span> <span data-ttu-id="7286a-174">Beraz, ziurtatu konfiguratu duzula [bezeroen jarduerak](activities.md) txantiloi batetik neurria sortu aurretik.</span><span class="sxs-lookup"><span data-stu-id="7286a-174">So make sure you have configured [customer activities](activities.md) before you create a measure from a template.</span></span>

<span data-ttu-id="7286a-175">Neurketa txantiloi erabilgarriak:</span><span class="sxs-lookup"><span data-stu-id="7286a-175">Available measure templates:</span></span> 
- <span data-ttu-id="7286a-176">Transakzioen batezbesteko balioa</span><span class="sxs-lookup"><span data-stu-id="7286a-176">Average transaction value (ATV)</span></span>
- <span data-ttu-id="7286a-177">Transakzioaren balioa, guztira</span><span class="sxs-lookup"><span data-stu-id="7286a-177">Total transaction value</span></span>
- <span data-ttu-id="7286a-178">Eguneko batezbesteko diru-sarrerak</span><span class="sxs-lookup"><span data-stu-id="7286a-178">Average daily revenue</span></span>
- <span data-ttu-id="7286a-179">Urteko batezbesteko diru-sarrerak</span><span class="sxs-lookup"><span data-stu-id="7286a-179">Average yearly revenue</span></span>
- <span data-ttu-id="7286a-180">Transakzio kopurua</span><span class="sxs-lookup"><span data-stu-id="7286a-180">Transaction count</span></span>
- <span data-ttu-id="7286a-181">Irabazitako fideltasun-puntuak</span><span class="sxs-lookup"><span data-stu-id="7286a-181">Loyalty points earned</span></span>
- <span data-ttu-id="7286a-182">Erabilitako fideltasun-puntuak</span><span class="sxs-lookup"><span data-stu-id="7286a-182">Loyalty points redeemed</span></span>
- <span data-ttu-id="7286a-183">Fideltasun-puntuen balantzea</span><span class="sxs-lookup"><span data-stu-id="7286a-183">Loyalty points balance</span></span>
- <span data-ttu-id="7286a-184">Bezero aktiboaren bizi-iraupena</span><span class="sxs-lookup"><span data-stu-id="7286a-184">Active customer lifespan</span></span>
- <span data-ttu-id="7286a-185">Fideltasun-kidetzaren iraupena</span><span class="sxs-lookup"><span data-stu-id="7286a-185">Loyalty membership duration</span></span>
- <span data-ttu-id="7286a-186">Azken transakziotik igarotako denbora</span><span class="sxs-lookup"><span data-stu-id="7286a-186">Time since last purchase</span></span>

<span data-ttu-id="7286a-187">Ondorengo prozeduran txantiloia erabiliz neurri berria eraikitzeko urratsak azaltzen dira.</span><span class="sxs-lookup"><span data-stu-id="7286a-187">The following procedure outlines the steps to build a new measure using a template.</span></span>

1. <span data-ttu-id="7286a-188">Hartzaileei buruzko xehetasunetan, joan hona: **Neurriak**.</span><span class="sxs-lookup"><span data-stu-id="7286a-188">In audience insights, go to **Measures**.</span></span>

1. <span data-ttu-id="7286a-189">Hautatu **Berria** eta hautatu **Aukeratu txantiloia**.</span><span class="sxs-lookup"><span data-stu-id="7286a-189">Select **New** and select **Choose a template**.</span></span>

   :::image type="content" source="media/measure-use-template.png" alt-text="Goitibeherako menuaren pantaila-argazkia neurri berri bat sortzean txantiloian nabarmenduta.":::

1. <span data-ttu-id="7286a-191">Aurkitu zure beharretara egokitzen den txantiloia eta hautatu **Aukeratu txantiloia**.</span><span class="sxs-lookup"><span data-stu-id="7286a-191">Find the template that fits your need and select **Choose template**.</span></span>

1. <span data-ttu-id="7286a-192">Berrikusi eskatutako datuak eta hautatu **Hasi** datu guztiak lekuan badituzu.</span><span class="sxs-lookup"><span data-stu-id="7286a-192">Review the required data and select **Get started** if you have all the data in place.</span></span>

1. <span data-ttu-id="7286a-193">Hurrengoan **Editatu izena** panelean, ezarri neurriaren izena eta irteerako entitatea.</span><span class="sxs-lookup"><span data-stu-id="7286a-193">In the **Edit name** pane, set the name for your measure and the output entity.</span></span> 

1. <span data-ttu-id="7286a-194">Hautatu **Eginda**.</span><span class="sxs-lookup"><span data-stu-id="7286a-194">Select **Done**.</span></span>

1. <span data-ttu-id="7286a-195">Hurrengoan **Ezarri denbora tartea** atalean, zehaztu erabili beharreko datuen denbora-tartea.</span><span class="sxs-lookup"><span data-stu-id="7286a-195">In the **Set time period** section, define the time frame of the data to use.</span></span> <span data-ttu-id="7286a-196">Aukeratu neurri berriak datu multzo osoa estaltzea nahi baduzu hautatuz **Denbora guztian**, edo neurria a ardatz izatea nahi baduzu **Denbora-tarte zehatza**.</span><span class="sxs-lookup"><span data-stu-id="7286a-196">Choose if you want the new measure to cover the entire dataset by selecting **All time**, or if you want the measure to focus on a **Specific time period**.</span></span>

   :::image type="content" source="media/measure-set-time-period.png" alt-text="Neurria txantiloi batetik konfiguratzerakoan denbora tartea erakusten duen pantaila-argazkia.":::

1. <span data-ttu-id="7286a-198">Hurrengo atalean, hautatu **Gehitu datuak** jarduerak aukeratzeko eta dagozkion datuak mapatzeko *Jarduera bateratua* entitatea.</span><span class="sxs-lookup"><span data-stu-id="7286a-198">In the next section, select **Add data** to choose the activities and map the corresponding data from your *Unified Activity* entity.</span></span>

    1. <span data-ttu-id="7286a-199">1. urratsa: 2. azpian **Jarduera mota**, aukeratu erabili nahi duzun entitatearen mota.</span><span class="sxs-lookup"><span data-stu-id="7286a-199">Step 1 of 2: Under **Activity type**, choose the type of the entity you want to use.</span></span> <span data-ttu-id="7286a-200">Hurrengorako **Jarduerak**, hautatu mapatu nahi dituzun entitateak.</span><span class="sxs-lookup"><span data-stu-id="7286a-200">For **Activities**, select the entities you want to map.</span></span>
    1. <span data-ttu-id="7286a-201">2. urratsa 2: aukeratu atributua *Jarduera bateratua* formulak eskatzen duen osagaiaren entitatea.</span><span class="sxs-lookup"><span data-stu-id="7286a-201">Step 2 of 2: Choose the attribute from the *Unified Activity* entity for the component required by the formula.</span></span> <span data-ttu-id="7286a-202">Adibidez, Transakzioaren batez besteko balioa, Transakzio balioa adierazten duen atributua da.</span><span class="sxs-lookup"><span data-stu-id="7286a-202">For example, for Average transaction value, it's the attribute representing the Transaction value.</span></span> <span data-ttu-id="7286a-203">Hurrengorako **Jardueren denbora-marka**, aukeratu aktibitatea jardueraren data eta ordua adierazten duen Jarduera bateratuko entitatearen artean.</span><span class="sxs-lookup"><span data-stu-id="7286a-203">For **Activity timestamp**, choose the attribute from the Unified Activity entity that represents the date and time of the activity.</span></span>
   
1. <span data-ttu-id="7286a-204">Datuen mapak arrakasta izan ondoren, egoera honela ikus dezakezu **Osatua** eta mapatutako jardueren eta atributuen izena.</span><span class="sxs-lookup"><span data-stu-id="7286a-204">Once the data mapping is successful, you can see the status as **Complete** and the name of the mapped activities and attributes.</span></span>

   :::image type="content" source="media/measure-template-configured.png" alt-text="Osatutako neurri txantiloien konfigurazioaren pantaila-argazkia.":::

1. <span data-ttu-id="7286a-206">Orain hauta dezakezu **Exekutatu** neurriaren emaitzak kalkulatzeko.</span><span class="sxs-lookup"><span data-stu-id="7286a-206">You can now select **Run** to calculate the results of the measure.</span></span> <span data-ttu-id="7286a-207">Geroago fintzeko, hautatu **Gorde zirriborroa**.</span><span class="sxs-lookup"><span data-stu-id="7286a-207">To refine it later, select **Save draft**.</span></span>

## <a name="manage-your-measures"></a><span data-ttu-id="7286a-208">Kudeatu neurriak</span><span class="sxs-lookup"><span data-stu-id="7286a-208">Manage your measures</span></span>

<span data-ttu-id="7286a-209">Hemen aurkituko dituzu neurrien zerrenda **Neurriak** orrialdea.</span><span class="sxs-lookup"><span data-stu-id="7286a-209">You can find the list of measures on the **Measures** page.</span></span>

<span data-ttu-id="7286a-210">Neurri motari, sortzaileari, sortze datari, egoerari eta egoerari buruzko informazioa aurkituko duzu.</span><span class="sxs-lookup"><span data-stu-id="7286a-210">You'll find information about the measure type, the creator, creation date, status, and state.</span></span> <span data-ttu-id="7286a-211">Zerrendako neurri bat hautatzen duzunean, irteera aurreikusi eta CSV fitxategia deskarga dezakezu.</span><span class="sxs-lookup"><span data-stu-id="7286a-211">When you select a measure from the list, you can preview the output and download a CSV file.</span></span>

<span data-ttu-id="7286a-212">Neurri guztiak aldi berean freskatzeko, hautatu **Freskatu guztiak** neurri zehatz bat aukeratu gabe.</span><span class="sxs-lookup"><span data-stu-id="7286a-212">To refresh all of your measures at the same time, select **Refresh all** without selecting a specific measure.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="7286a-213">![Neurri bakarrak kudeatzeko ekintzak.](media/measure-actions.png "Neurri bakarrak kudeatzeko ekintzak.")</span><span class="sxs-lookup"><span data-stu-id="7286a-213">![Actions to manage single measures.](media/measure-actions.png "Actions to manage single measures.")</span></span>

<span data-ttu-id="7286a-214">Aukeratu neurri bat zerrendan aukera hauetarako:</span><span class="sxs-lookup"><span data-stu-id="7286a-214">Select a measure from the list for the following options:</span></span>

- <span data-ttu-id="7286a-215">Hautatu neurriaren izena, haren xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="7286a-215">Select the measure name to see its details.</span></span>
- <span data-ttu-id="7286a-216">**Editatu** neurriaren konfigurazioa.</span><span class="sxs-lookup"><span data-stu-id="7286a-216">**Edit** the configuration of the measure.</span></span>
- <span data-ttu-id="7286a-217">**Freskatu** neurria azken datuetan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="7286a-217">**Refresh** the measure based on the latest data.</span></span>
- <span data-ttu-id="7286a-218">**Aldatu izena** neurria.</span><span class="sxs-lookup"><span data-stu-id="7286a-218">**Rename** the measure.</span></span>
- <span data-ttu-id="7286a-219">**Ezabatu** neurria.</span><span class="sxs-lookup"><span data-stu-id="7286a-219">**Delete** the measure.</span></span>
- <span data-ttu-id="7286a-220">**Aktibatu** edo **Desaktibatu**.</span><span class="sxs-lookup"><span data-stu-id="7286a-220">**Activate** or **Deactivate**.</span></span> <span data-ttu-id="7286a-221">Neurri inaktiboak ez dira freskatuko [freskatze programatuan](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="7286a-221">Inactive measures won't get refreshed during a [scheduled refresh](system.md#schedule-tab).</span></span>

> [!TIP]
> <span data-ttu-id="7286a-222">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="7286a-222">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="7286a-223">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="7286a-223">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="7286a-224">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="7286a-224">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="7286a-225">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="7286a-225">After selecting **See details** for one of the job's tasks, you'll find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="next-step"></a><span data-ttu-id="7286a-226">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="7286a-226">Next step</span></span>

<span data-ttu-id="7286a-227">Sortzeko dauden neurriak erabil ditzakezu [bezero segmentu bat](segments.md).</span><span class="sxs-lookup"><span data-stu-id="7286a-227">You can use existing measures to create [a customer segment](segments.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]