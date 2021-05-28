---
title: Sortu eta kudeatu segmentuak
description: Sortu bezeroen segmentuak, hainbat atributuren arabera taldekatzeko.
ms.date: 05/03/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 550e509a24701fe5fcdeb9d54311872dc954156c
ms.sourcegitcommit: 72603fb39c4d5dbca71128815a2e1692542ea4dc
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/19/2021
ms.locfileid: "6064922"
---
# <a name="create-and-manage-segments"></a><span data-ttu-id="50abf-103">Sortu eta kudeatu segmentuak</span><span class="sxs-lookup"><span data-stu-id="50abf-103">Create and manage segments</span></span>

<span data-ttu-id="50abf-104">Definitu iragazki konplexuak bezero entitate bateratuaren eta hari lotutako entitateen inguruan.</span><span class="sxs-lookup"><span data-stu-id="50abf-104">Define complex filters around the unified customer entity and its related entities.</span></span> <span data-ttu-id="50abf-105">Segmentu bakoitzak, prozesatu ondoren, bezeroen erregistro multzo bat sortzen du eta esportatu eta neurriak hartu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="50abf-105">Each segment, after processing, creates a set of customer records that you can export and take action on.</span></span> <span data-ttu-id="50abf-106">Segmentuak **Segmentuak** orrian kudeatzen dira.</span><span class="sxs-lookup"><span data-stu-id="50abf-106">Segments are managed on the **Segments** page.</span></span> 

<span data-ttu-id="50abf-107">Hurrengo adibideak segmentazio gaitasunaren erabilera ilustratzen du.</span><span class="sxs-lookup"><span data-stu-id="50abf-107">The following example illustrates the segmentation capability.</span></span> <span data-ttu-id="50abf-108">Azken 90 egunetan gutxienez $500 agindu duten bezeroentzako segmentu bat zehaztu dugu *eta* bezeroarentzako arreta-zerbitzu deitu batean parte hartu zutenak eskalatu egin ziren.</span><span class="sxs-lookup"><span data-stu-id="50abf-108">We've defined a segment for customers who ordered at least $500 of goods in the last 90 days *and* who were involved in a customer service call that got escalated.</span></span>

:::image type="content" source="media/segmentation-group1-2.png" alt-text="Segmentu-sortzailearen UIren pantaila-argazkia bezero segmentu bat zehazten duten bi taldeekin.":::

## <a name="create-a-new-segment"></a><span data-ttu-id="50abf-110">Sortu segmentu berria</span><span class="sxs-lookup"><span data-stu-id="50abf-110">Create a new segment</span></span>

<span data-ttu-id="50abf-111">Segmentu berri bat sortzeko hainbat modu daude.</span><span class="sxs-lookup"><span data-stu-id="50abf-111">There are multiple ways to create a new segment.</span></span> <span data-ttu-id="50abf-112">Atal honetan a nola sortu deskribatzen da *segmentu hutsa* hutsetik.</span><span class="sxs-lookup"><span data-stu-id="50abf-112">This section describes how to create a *blank segment* from scratch.</span></span> <span data-ttu-id="50abf-113">A ere sor dezakezu *segmentu azkarra* dauden entitateetan oinarrituta edo lortzeko Ikaskuntza automatiko ereduak *iradokitako segmentuak*.</span><span class="sxs-lookup"><span data-stu-id="50abf-113">You can also create a *quick segment* based on existing entities or make use of machine learning models to get *suggested segments*.</span></span> <span data-ttu-id="50abf-114">Informazio gehiago lortzeko: [Segmentuen informazio orokorra](segments.md).</span><span class="sxs-lookup"><span data-stu-id="50abf-114">More information: [Segments overview](segments.md).</span></span>

<span data-ttu-id="50abf-115">Segmentua sortu bitartean, zirriborroa gorde dezakezu.</span><span class="sxs-lookup"><span data-stu-id="50abf-115">While creating a segment, you can save a draft.</span></span> <span data-ttu-id="50abf-116">Segmentu inaktibo gisa gordeko da eta ezin da aktibatu baliozko konfigurazio batekin amaituta.</span><span class="sxs-lookup"><span data-stu-id="50abf-116">It will be saved as an inactive segment, and can't be activated it finished with a valid configuration.</span></span>

1. <span data-ttu-id="50abf-117">Zoaz **Segmentuak** orrira.</span><span class="sxs-lookup"><span data-stu-id="50abf-117">Go to the **Segments** page.</span></span>

1. <span data-ttu-id="50abf-118">Aukeratu **Berria** > **Segmentu zuria**.</span><span class="sxs-lookup"><span data-stu-id="50abf-118">Select **New** > **Blank segment**.</span></span>

1. <span data-ttu-id="50abf-119">**Segmentu berria** panelean, aukeratu segmentu mota bat:</span><span class="sxs-lookup"><span data-stu-id="50abf-119">In the **New segment** pane, choose a segment type:</span></span>

   - <span data-ttu-id="50abf-120">**Segmentu dinamikoak** [freskatu](segments.md#refresh-segments) aldizkako ordutegian.</span><span class="sxs-lookup"><span data-stu-id="50abf-120">**Dynamic segments** [refresh](segments.md#refresh-segments) on a recurring schedule.</span></span>
   - <span data-ttu-id="50abf-121">**Segmentu estatikoak** exekutatu behin sortzen duzunean.</span><span class="sxs-lookup"><span data-stu-id="50abf-121">**Static segments** run once when you create it.</span></span>

1. <span data-ttu-id="50abf-122">Eman **Irteerako entitatearen izena** segmenturako.</span><span class="sxs-lookup"><span data-stu-id="50abf-122">Provide an **Output entity name** for the segment.</span></span> <span data-ttu-id="50abf-123">Aukeran, eman pantailaren izena eta segmentua identifikatzen lagunduko duen deskribapena.</span><span class="sxs-lookup"><span data-stu-id="50abf-123">Optionally, provide a display name, and a description that helps identifying the segment.</span></span>

1. <span data-ttu-id="50abf-124">Aukeratu **hurrengo** etortzeko **Segmentuen eraikitzailea** taldea non definitzen duzun.</span><span class="sxs-lookup"><span data-stu-id="50abf-124">Select **Next** to get to the **Segment builder** page where you define a group.</span></span> <span data-ttu-id="50abf-125">Talde bat bezero multzo bat da.</span><span class="sxs-lookup"><span data-stu-id="50abf-125">A group is a set of customers.</span></span>

1. <span data-ttu-id="50abf-126">Aukeratu segmentatu nahi duzun atributua barne hartzen duen entitatea.</span><span class="sxs-lookup"><span data-stu-id="50abf-126">Choose the entity that includes the attribute you want to segment by.</span></span>

1. <span data-ttu-id="50abf-127">Aukeratu arabera zatitu beharreko atributua.</span><span class="sxs-lookup"><span data-stu-id="50abf-127">Choose the attribute to segment by.</span></span> <span data-ttu-id="50abf-128">Atributu honek lau balio motetako bat izan dezake: zenbakikoa, katea, data edo boolearra.</span><span class="sxs-lookup"><span data-stu-id="50abf-128">This attribute can have one of four value types: numerical, string, date, or Boolean.</span></span>

1. <span data-ttu-id="50abf-129">Aukeratu operadorea eta balio bat hautatutako atributurako.</span><span class="sxs-lookup"><span data-stu-id="50abf-129">Choose an operator and a value for the selected attribute.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="50abf-130">![Pertsonalizatu taldeko iragazkia](media/customer-group-numbers.png "Bezeroaren taldeko iragazkia")</span><span class="sxs-lookup"><span data-stu-id="50abf-130">![Custom group filter](media/customer-group-numbers.png "Customer group filter")</span></span>

   |<span data-ttu-id="50abf-131">Zenbakia</span><span class="sxs-lookup"><span data-stu-id="50abf-131">Number</span></span> |<span data-ttu-id="50abf-132">Definizioa</span><span class="sxs-lookup"><span data-stu-id="50abf-132">Definition</span></span>  |
   |---------|---------|
   |<span data-ttu-id="50abf-133">1</span><span class="sxs-lookup"><span data-stu-id="50abf-133">1</span></span>     |<span data-ttu-id="50abf-134">Entity</span><span class="sxs-lookup"><span data-stu-id="50abf-134">Entity</span></span>          |
   |<span data-ttu-id="50abf-135">2</span><span class="sxs-lookup"><span data-stu-id="50abf-135">2</span></span>     |<span data-ttu-id="50abf-136">Atributua</span><span class="sxs-lookup"><span data-stu-id="50abf-136">Attribute</span></span>          |
   |<span data-ttu-id="50abf-137">3</span><span class="sxs-lookup"><span data-stu-id="50abf-137">3</span></span>    |<span data-ttu-id="50abf-138">Eragilea</span><span class="sxs-lookup"><span data-stu-id="50abf-138">Operator</span></span>         |
   |<span data-ttu-id="50abf-139">4</span><span class="sxs-lookup"><span data-stu-id="50abf-139">4</span></span>    |<span data-ttu-id="50abf-140">Balioa</span><span class="sxs-lookup"><span data-stu-id="50abf-140">Value</span></span>         |

   1. <span data-ttu-id="50abf-141">Talde bati baldintza gehiago gehitzeko, bi operadore logiko erabil ditzakezu:</span><span class="sxs-lookup"><span data-stu-id="50abf-141">To add more conditions to a group, you can use two logical operators:</span></span>

      - <span data-ttu-id="50abf-142">**ETA** operadorea: Bi baldintza segmentazio prozesuaren baitan bete behar dira.</span><span class="sxs-lookup"><span data-stu-id="50abf-142">**AND** operator: Both conditions must be met as part of the segmentation process.</span></span> <span data-ttu-id="50abf-143">Aukera hau baliagarria da entitate desberdinetan baldintzak definitzen dituzunean.</span><span class="sxs-lookup"><span data-stu-id="50abf-143">This option is most useful when you define conditions across different entities.</span></span>

      - <span data-ttu-id="50abf-144">**EDO** operadorea: Baldintzaren bat segmentazio prozesuaren zati gisa bete behar da.</span><span class="sxs-lookup"><span data-stu-id="50abf-144">**OR** operator: Either one of the conditions needs to be met as part of the segmentation process.</span></span> <span data-ttu-id="50abf-145">Aukera hau oso baliagarria da hainbat baldintza definitzen dituzunean entitate berarentzat.</span><span class="sxs-lookup"><span data-stu-id="50abf-145">This option is most useful when you define multiple conditions for the same entity.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="50abf-146">![EDO baldintza bat bete behar den operadorea](media/segmentation-either-condition.png "EDO baldintza bat bete behar den operadorea")</span><span class="sxs-lookup"><span data-stu-id="50abf-146">![OR operator where either condition needs to be met](media/segmentation-either-condition.png "OR operator where either condition needs to be met")</span></span>

      <span data-ttu-id="50abf-147">Gaur egun, habia habia egin daiteke **EDO** operadorea **ETA** operadorea, baina ez alderantziz.</span><span class="sxs-lookup"><span data-stu-id="50abf-147">It's currently possible to nest an **OR** operator under an **AND** operator, but not the other way around.</span></span>

   1. <span data-ttu-id="50abf-148">Talde bakoitza bezero multzoarekin bat dator.</span><span class="sxs-lookup"><span data-stu-id="50abf-148">Each group matches set of customers.</span></span> <span data-ttu-id="50abf-149">Taldeak konbinatu ditzakezu zure negozio kasurako behar diren bezeroak sartzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-149">You can combine groups to include the customers required for your business case.</span></span>    
   <span data-ttu-id="50abf-150">Hautatu **Gehitu taldea**.</span><span class="sxs-lookup"><span data-stu-id="50abf-150">Select **Add Group**.</span></span>

      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="50abf-151">![Bezeroen taldea gehitzeko taldea](media/customer-group-add-group.png "Bezeroen taldea gehitzeko taldea")</span><span class="sxs-lookup"><span data-stu-id="50abf-151">![Customer group add group](media/customer-group-add-group.png "Customer group add group")</span></span>

   1. <span data-ttu-id="50abf-152">Aukeratu multzo operadoreetako bat: **Batasuna**, **Elkartu**, edo **Izan ezik**.</span><span class="sxs-lookup"><span data-stu-id="50abf-152">Select one of the set operators: **Union**, **Intersect**, or **Except**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="50abf-153">![Bezeroen taldea gehitzeko bateratzea](media/customer-group-union.png "Bezeroen taldea gehitzeko bateratzea")</span><span class="sxs-lookup"><span data-stu-id="50abf-153">![Customer group add union](media/customer-group-union.png "Customer group add union")</span></span>

   - <span data-ttu-id="50abf-154">**Bateratzea** bi taldeak batzen ditu.</span><span class="sxs-lookup"><span data-stu-id="50abf-154">**Union** unites the two groups.</span></span>

   - <span data-ttu-id="50abf-155">**Gurutzatu** bi taldeak gainjartzen ditu.</span><span class="sxs-lookup"><span data-stu-id="50abf-155">**Intersect** overlaps the two groups.</span></span> <span data-ttu-id="50abf-156">Bi taldeetako datu *komunak* soilik mantentzen dira talde bateratuan.</span><span class="sxs-lookup"><span data-stu-id="50abf-156">Only data that *is common* to both groups is retained in the unified group.</span></span>

   - <span data-ttu-id="50abf-157">**Salbuespena** bi taldeak batzen ditu.</span><span class="sxs-lookup"><span data-stu-id="50abf-157">**Except** combines the two groups.</span></span> <span data-ttu-id="50abf-158">A eta B talde bietan *ez dauden* datuak soilik mantentzen dira.</span><span class="sxs-lookup"><span data-stu-id="50abf-158">Only data in group A that *is not common* to data in group B is retained.</span></span>

1. <span data-ttu-id="50abf-159">Erakundea bezero bateratutako entitatearekin konektatuta badago [harremanak](relationships.md), erlazio bidea zehaztu behar duzu baliozko segmentua sortzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-159">If the entity is connected to the unified customer entity through [relationships](relationships.md), you need to define the relationship path to create a valid segment.</span></span> <span data-ttu-id="50abf-160">Gehitu entitateak erlazio-bide honetatik hautatu dezakezu arte **Bezeroa: CustomerInsights** entitatea goitibehera.</span><span class="sxs-lookup"><span data-stu-id="50abf-160">Add the entities from the relationship path until you can select the **Customer:CustomerInsights** entity from the dropdown.</span></span> <span data-ttu-id="50abf-161">Ondoren, aukeratu **Erregistro guztiak** urrats bakoitzerako.</span><span class="sxs-lookup"><span data-stu-id="50abf-161">Then, choose **All records** for each step.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="50abf-162">![Harreman bidea segmentuak sortzean](media/segments-multiple-relationships.png "Harreman bidea segmentuak sortzean")</span><span class="sxs-lookup"><span data-stu-id="50abf-162">![Relationship path during segment creation](media/segments-multiple-relationships.png "Relationship path during segment creation")</span></span>

1. <span data-ttu-id="50abf-163">Lehenespenez, segmentuek definitutako iragazkiekin bat datozen bezeroen profilen atributu guztiak dituen irteerako entitatea sortzen dute.</span><span class="sxs-lookup"><span data-stu-id="50abf-163">By default, segments generate an output entity that contains all attributes of customer profiles which match the defined filters.</span></span> <span data-ttu-id="50abf-164">Segmentu bat ez den beste entitate batzuetan oinarrituta badago *Bezeroa* entitatea, entitate hauetatik atributu gehiago gehi ditzakezu irteerako entitateari.</span><span class="sxs-lookup"><span data-stu-id="50abf-164">If a segment is based on other entities than the *Customer* entity, you can add more attributes from these entities to the output entity.</span></span> <span data-ttu-id="50abf-165">Aukeratu **Proiektuaren atributuak** irteerako entitateari erantsiko zaizkion atributuak aukeratzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-165">Select **Project attributes** to choose the attributes that will be appended to the output entity.</span></span>  
  
   <span data-ttu-id="50abf-166">Adibidez: segmentu bat bezeroarekin lotutako jarduerak dituen entitate batean oinarritzen da *Bezeroa* entitatea.</span><span class="sxs-lookup"><span data-stu-id="50abf-166">Example: A segment is based on an entity that contains customer activity data which is related to the *Customer* entity.</span></span> <span data-ttu-id="50abf-167">Segmentuak azken 60 egunetan laguntza-mahaira deitu duten bezero guztiak bilatzen ditu.</span><span class="sxs-lookup"><span data-stu-id="50abf-167">The segment looks for all customers that called the help desk in the last 60 days.</span></span> <span data-ttu-id="50abf-168">Irteerako entitatean bat datozen bezeroen erregistro guztiei deiaren iraupena eta dei kopurua eranstea aukera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="50abf-168">You can choose to append the call duration and the number of calls to all matching customer records in the output entity.</span></span> <span data-ttu-id="50abf-169">Informazio hau baliagarria izan daiteke maiz deitzen duten bezeroei lineako laguntza artikuluen eta ohiko galderen esteka lagungarriekin mezu elektronikoak bidaltzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-169">This information might be useful to send an email with helpful links to online help articles and FAQs to customers who called frequently.</span></span>

   > [!NOTE]
   > - <span data-ttu-id="50abf-170">Proiektatutako atributuek bezeroaren entitatearekin bat-bateko harremana duten entitateentzat bakarrik funtzionatzen dute.</span><span class="sxs-lookup"><span data-stu-id="50abf-170">Projected attributes only work for entities that have a one-to-many relationship with the customer entity.</span></span> <span data-ttu-id="50abf-171">Adibidez, bezero batek harpidetza ugari izan ditzake.</span><span class="sxs-lookup"><span data-stu-id="50abf-171">For example, one customer can have multiple subscriptions.</span></span>
   > - <span data-ttu-id="50abf-172">Eraikitzen ari zaren segmentu kontsulta talde guztietan erabiltzen den entitate bateko atributuak soilik proiekta ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="50abf-172">You can only project attributes from an entity that is used in every group of segment query you are building.</span></span>
   > - <span data-ttu-id="50abf-173">Multzo operadoreak erabiltzean proiektatutako atributuak kontuan hartzen dira.</span><span class="sxs-lookup"><span data-stu-id="50abf-173">Projected attributes are factored in when using set operators.</span></span>

1. <span data-ttu-id="50abf-174">Segmentua gordetzeko, sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="50abf-174">Select **Save** to save your segment.</span></span> <span data-ttu-id="50abf-175">Zure segmentua gordeko da eta prozesatu egingo da baldintza guztiak baliozkotuz gero.</span><span class="sxs-lookup"><span data-stu-id="50abf-175">Your segment will be saved and processed if all requirements are validated.</span></span> <span data-ttu-id="50abf-176">Bestela, zirriborro gisa gordeko da.</span><span class="sxs-lookup"><span data-stu-id="50abf-176">Otherwise, it will be saved as a draft.</span></span>

1. <span data-ttu-id="50abf-177">Aukeratu **Segurtasunetara itzuli** berriro ere **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="50abf-177">Select **Back to segments** to go back to the **Segments** page.</span></span>



## <a name="quick-segments"></a><span data-ttu-id="50abf-178">Segmentu azkarrak</span><span class="sxs-lookup"><span data-stu-id="50abf-178">Quick segments</span></span>

<span data-ttu-id="50abf-179">Segmentu bizkorrek segmentu sinpleak operadore bakar batekin azkar eraikitzeko aukera ematen dute ikuspegi azkarragoak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-179">Quick segments let you build simple segments with a single operator quickly for faster insights.</span></span>

1. <span data-ttu-id="50abf-180">**Segmentuak** orrian, hautatu **Berria** > **Sortu honetatik**.</span><span class="sxs-lookup"><span data-stu-id="50abf-180">On the **Segments** page, select **New** > **Create from**.</span></span>

   - <span data-ttu-id="50abf-181">Hautatu **Profilak** aukera *bateratutako bezeroaren* entitatean oinarritutako segmentu bat eraikitzeko aukera.</span><span class="sxs-lookup"><span data-stu-id="50abf-181">Select the **Profiles** option to build a segment that is based on the *unified customer* entity.</span></span>
   - <span data-ttu-id="50abf-182">Aukeratu **Neurriak** aukera sortu aurretik sortutako neurrien inguruan segmentu bat eraikitzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-182">Select the **Measures** option to build a segment around  measures you have previously created.</span></span>
   - <span data-ttu-id="50abf-183">Hautatu botoia **Adimen** Aukera hau bai erabiliz sortu duzun irteerako entitateetako baten inguruan eraikitzeko aukera **iragarpenak** edo **Neurrira egindako ereduak** gaitasunak.</span><span class="sxs-lookup"><span data-stu-id="50abf-183">Select the **Intelligence** option to build a segment around one of the output entities you generated using either the **Predictions** or **Custom Models** capabilities.</span></span>

2. <span data-ttu-id="50abf-184">Sarbidean **Segmentu azkar berria** elkarrizketa-koadroan, hautatu atributu bat **eremua** goitibeherako menuko.</span><span class="sxs-lookup"><span data-stu-id="50abf-184">In the **New quick segment** dialog box, select an attribute from the **Field** dropdown.</span></span>

3. <span data-ttu-id="50abf-185">Sistemak ikuspegi osagarriak emango ditu zure bezeroen segmentu hobeak sortzen lagunduko dutenak.</span><span class="sxs-lookup"><span data-stu-id="50abf-185">The system will provide some additional insights that help you create better segments of your customers.</span></span>
   - <span data-ttu-id="50abf-186">Eremu kategorikoetarako, 10 bezero zenbatuko ditugu.</span><span class="sxs-lookup"><span data-stu-id="50abf-186">For categorical fields, we'll show 10 top customer counts.</span></span> <span data-ttu-id="50abf-187">Hautatu **Balio** bat eta hautatu **Berrikusi**.</span><span class="sxs-lookup"><span data-stu-id="50abf-187">Choose a **Value** and select **Review**.</span></span>

   - <span data-ttu-id="50abf-188">Zenbakizko atributu bat lortzeko, sistemak erakutsiko du zer atributu-balioa eroriko den bezero bakoitzaren portzentalaren azpian.</span><span class="sxs-lookup"><span data-stu-id="50abf-188">For a numerical attribute, the system will show what attribute value falls under each customer's percentile.</span></span> <span data-ttu-id="50abf-189">Aukeratu bat **Operadorea** eta **Balioa** eta hautatu **Berrikusi**.</span><span class="sxs-lookup"><span data-stu-id="50abf-189">Choose an **Operator** and a **Value**, then select **Review**.</span></span>

4. <span data-ttu-id="50abf-190">Sistemak zurekin hornituko zaitu **Segurtasunaren neurria**.</span><span class="sxs-lookup"><span data-stu-id="50abf-190">The system will provide you with an **Estimated segment size**.</span></span> <span data-ttu-id="50abf-191">Definitu duzun segmentua sortu edo aukeratu dezakezu edo, bestela, berrikusi beste segmentu baten tamaina lortzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-191">You can choose whether to generate the segment you've defined, or first revisit it to get a different segment size.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="50abf-192">![Izena eta estimazioa segmentu azkar baterako](media/quick-segment-name.png "Izena eta estimazioa segmentu azkar baterako")</span><span class="sxs-lookup"><span data-stu-id="50abf-192">![Name and estimation for a quick segment](media/quick-segment-name.png "Name and estimation for a quick segment")</span></span>

5. <span data-ttu-id="50abf-193">Jarri **izena** zure segmentuari.</span><span class="sxs-lookup"><span data-stu-id="50abf-193">Provide a **Name** for your segment.</span></span> <span data-ttu-id="50abf-194">Nahi baduzu, eman **Bistaratzeko izena**.</span><span class="sxs-lookup"><span data-stu-id="50abf-194">Optionally, provide a **Display name**.</span></span>

6. <span data-ttu-id="50abf-195">Segmentua sortzeko, sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="50abf-195">Select **Save** to create your segment.</span></span>

7. <span data-ttu-id="50abf-196">Segmentua prozesatu ondoren, sortu duzun beste edozein segmentu bezala ikus dezakezu.</span><span class="sxs-lookup"><span data-stu-id="50abf-196">After the segment has finished processing, you can view it like any other segment you've created.</span></span>

## <a name="next-steps"></a><span data-ttu-id="50abf-197">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="50abf-197">Next steps</span></span>

<span data-ttu-id="50abf-198">[Esportatu segmentua](export-destinations.md) eta esploratu [Bezero txartela](customer-card-add-in.md) eta [Konektoreak](export-power-bi.md) bezeroaren mailari buruzko informazioa lortzeko.</span><span class="sxs-lookup"><span data-stu-id="50abf-198">[Export a segment](export-destinations.md) and explore the [Customer Card](customer-card-add-in.md) and [Connectors](export-power-bi.md) to get insights on the customer level.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
