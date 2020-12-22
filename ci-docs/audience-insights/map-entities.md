---
title: Esleitu entitateak datuak bateratzeko
description: Esleitu datuak bezeroen profil bateratuak sortzeko.
ms.date: 09/25/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
ms.openlocfilehash: e98c7717f7707d43a9fd1fc6f6b0e9c49e4e7ee0
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404989"
---
# <a name="map-entities-and-attributes"></a><span data-ttu-id="6163e-103">Mapen entitateak eta atributuak</span><span class="sxs-lookup"><span data-stu-id="6163e-103">Map entities and attributes</span></span>

<span data-ttu-id="6163e-104">**Esleipena** hartzaileen xehetasunen datuen bateratze prozesuko lehen etapa da.</span><span class="sxs-lookup"><span data-stu-id="6163e-104">**Map** is the first stage in the data unification process of audience insights.</span></span> <span data-ttu-id="6163e-105">Kartografiak hiru fase ditu:</span><span class="sxs-lookup"><span data-stu-id="6163e-105">Mapping consists of three phases:</span></span>

- <span data-ttu-id="6163e-106">*Erakundeen hautaketa*: Identifikatu datu multzo batera daramaten entitate konbinagarriek zure bezeroei buruzko informazio osoagoa.</span><span class="sxs-lookup"><span data-stu-id="6163e-106">*Entity selection*: Identify the combinable entities that lead to a dataset with more complete information about your customers.</span></span>
- <span data-ttu-id="6163e-107">*Ezaugarri hautaketa*: Entitate bakoitzeko, identifikatu konbinatu eta bateratu nahi dituzun zutabeak *bat-etortze* eta *konbinatu* faseak.</span><span class="sxs-lookup"><span data-stu-id="6163e-107">*Attribute selection*: For each entity, identify the columns you want to combine and reconcile in the *match* and *merge* phases.</span></span> <span data-ttu-id="6163e-108">Zutabe horiei *Atributuak* deitzen zaie.</span><span class="sxs-lookup"><span data-stu-id="6163e-108">These columns are called *Attributes*.</span></span>
- <span data-ttu-id="6163e-109">*Gako nagusia eta mota semantikoa hautatzea*: Entitate bakoitzerako, identifikatu entitate horren gako nagusi gisa definitu nahi duzun atributu bat eta atributu bakoitzerako, identifikatu atributu hori hobekien deskribatzen duen mota semantikoa.</span><span class="sxs-lookup"><span data-stu-id="6163e-109">*Primary key and semantic type selection*: For each entity, identify an attribute you want to define as the primary key for that entity, and for each attribute, identify a semantic type that best describes that attribute.</span></span>

<span data-ttu-id="6163e-110">Informazio gehiago lortzeko datuen bateratzeari buruzko informazio gehiago lortzeko, ikus [bateratzeko](data-unification.md).</span><span class="sxs-lookup"><span data-stu-id="6163e-110">For more information about the general flow of data unification, see [Unify](data-unification.md).</span></span>

## <a name="select-the-first-entities"></a><span data-ttu-id="6163e-111">Hautatu lehenengo entitateak</span><span class="sxs-lookup"><span data-stu-id="6163e-111">Select the first entities</span></span>

1. <span data-ttu-id="6163e-112">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Bat egin** > **Esleitu**.</span><span class="sxs-lookup"><span data-stu-id="6163e-112">In audience insights, go to **Data** > **Unify** > **Map**.</span></span>

2. <span data-ttu-id="6163e-113">Hasi mapa fasea aukeratuz **Erakundeak hautatu**.</span><span class="sxs-lookup"><span data-stu-id="6163e-113">Start the map phase by selecting **Select entities**.</span></span>

3. <span data-ttu-id="6163e-114">Aukeratu erabili nahi dituzun entitateak eta atributuak *partida* eta *batu* faseak.</span><span class="sxs-lookup"><span data-stu-id="6163e-114">Select the entities and attributes you want to use in the *match* and *merge* phases.</span></span> <span data-ttu-id="6163e-115">Beharrezko atributuak banaka hauta ditzakezu entitate batetik edo entitate bateko atributu guztiak sar ditzakezu **Sartu eremu guztiak** kontrol-laukia entitate mailan.</span><span class="sxs-lookup"><span data-stu-id="6163e-115">You can select the required attributes individually from an entity or include all attributes from an entity by selecting the **Include all fields** checkbox on the entity level.</span></span> <span data-ttu-id="6163e-116">Gutxienez bi entitate hautatzea gomendatzen dugu datuak bateratzeko prozesuan etekina ateratzeko.</span><span class="sxs-lookup"><span data-stu-id="6163e-116">We recommend selecting at least two entities to benefit from the data unification process.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="6163e-117">![Gehitu entitateak adibidea](media/data-manager-configure-map-add-entities-example.png "Gehitu entitateak adibidea")</span><span class="sxs-lookup"><span data-stu-id="6163e-117">![Add entities example](media/data-manager-configure-map-add-entities-example.png "Add entities example")</span></span>

   <span data-ttu-id="6163e-118">Adibide honetan, **eCommerceContacts** eta **loyBezeroak** entitateak.</span><span class="sxs-lookup"><span data-stu-id="6163e-118">In this example, we're adding the **eCommerceContacts** and **loyCustomers** entities.</span></span> <span data-ttu-id="6163e-119">Entitate horiek aukeratuta, lineako negozioen bezeroak fidelizazio programako kide diren jakiteko.</span><span class="sxs-lookup"><span data-stu-id="6163e-119">By choosing these entities, you can derive insights on which of the online business customers are loyalty program members.</span></span>
   
   <span data-ttu-id="6163e-120">Atributu eta entitate guztietan gako-hitzak bilatu ditzakezu mapatu nahi dituzun beharrezko atributuak hautatzeko.</span><span class="sxs-lookup"><span data-stu-id="6163e-120">You can search on keywords across all attributes and entities to select the required attributes you want to map.</span></span>
   
     > [!div class="mx-imgBorder"]
   > <span data-ttu-id="6163e-121">![Bilatu eremuen adibidea](media/data-manager-configure-map-search-fields-example.png "Bilatu eremuen adibidea")</span><span class="sxs-lookup"><span data-stu-id="6163e-121">![Search fields example](media/data-manager-configure-map-search-fields-example.png "Search fields example")</span></span>

4. <span data-ttu-id="6163e-122">Aukeratu **Aplikatu** zure hautapenak baieztatzeko.</span><span class="sxs-lookup"><span data-stu-id="6163e-122">Select **Apply** to confirm your selections.</span></span>

## <a name="select-primary-key-and-semantic-type-for-attributes"></a><span data-ttu-id="6163e-123">Aukeratu gako nagusia eta mota semantikoa atributuetarako</span><span class="sxs-lookup"><span data-stu-id="6163e-123">Select primary key and semantic type for attributes</span></span>

<span data-ttu-id="6163e-124">Zure entitateak hautatu ondoren, **Mapa** orrialdeak zure berrikuspenerako hautatutako entitateak zerrendatzen ditu.</span><span class="sxs-lookup"><span data-stu-id="6163e-124">After selecting your entities, the **Map** page lists the selected entities for your review.</span></span> <span data-ttu-id="6163e-125">Definitu entitate baten gako nagusia eta identifikatu entitatean atributu baten mota semantikoa.</span><span class="sxs-lookup"><span data-stu-id="6163e-125">Define the primary key for an entity and identify the semantic type for an attribute in the entity.</span></span>

- <span data-ttu-id="6163e-126">**Lehen mailako gakoa**: Aukeratu ezazu atributu bat entitate bakoitzerako gako nagusi gisa.</span><span class="sxs-lookup"><span data-stu-id="6163e-126">**Primary key**: Select one attribute as a primary key for each of your entities.</span></span> <span data-ttu-id="6163e-127">Atributu bat baliozko gako nagusia izan dadin, ez lituzke balio bikoiztuak, falta diren balioak edo balio baliorik sartu behar.</span><span class="sxs-lookup"><span data-stu-id="6163e-127">For an attribute to be a valid primary key, it shouldn't include duplicate values, missing values, or null values.</span></span> <span data-ttu-id="6163e-128">Katea, osoko zenbakia eta GUID datu motaren atributuak gako nagusi gisa onartzen dira eta aukeratu ahal izateko eremu batean bistaratuko dira.</span><span class="sxs-lookup"><span data-stu-id="6163e-128">String, integer, and GUID data type attributes are supported as primary keys and will be displayed in a field for you to select from.</span></span>

- <span data-ttu-id="6163e-129">**Atributu semantiko mota**: Zure atributuen kategoriak, hala nola helbide elektronikoa edo izena.</span><span class="sxs-lookup"><span data-stu-id="6163e-129">**Attribute semantic type**: Categories of your attributes, such as email address or name.</span></span> <span data-ttu-id="6163e-130">AI ereduak semantika iragarpen adimendunetarako erabiltzeko, denbora aurreztu eta zehaztasuna hobetzeko, ezarri **Kartografia adimenduna** hurrengora **Aktibatu**.</span><span class="sxs-lookup"><span data-stu-id="6163e-130">To use AI models for smart prediction of semantics, save time and improve accuracy, set **Intelligent mapping** to **ON**.</span></span> <span data-ttu-id="6163e-131">Kartografia adimendunak AI-n oinarritutako semantika gomendioa nabarmentzen du **Mota** zelaia.</span><span class="sxs-lookup"><span data-stu-id="6163e-131">Intelligent mapping highlights AI-based semantics recommendation in the **Type** field.</span></span> <span data-ttu-id="6163e-132">Ezartzen baduzu **Itzali**, gure ohiko mapen gomendioak ikusiko dituzu.</span><span class="sxs-lookup"><span data-stu-id="6163e-132">If you set it to **OFF**, you will see our regular mapping recommendations.</span></span> <span data-ttu-id="6163e-133">Edozein mota semantiko hauta dezakezu eskuragarri dauden aukeren zerrendan eta iradokitako hautaketa gainidatzi.</span><span class="sxs-lookup"><span data-stu-id="6163e-133">You can select any semantic type from the available list of options and override the suggested selection.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="6163e-134">![Atributu mota eta iragarpen semantikoa](media/data-manager-configure-map-add-attributes-semantic-prediction.png "Atributu mota eta iragarpen semantikoa")</span><span class="sxs-lookup"><span data-stu-id="6163e-134">![Attribute type and semantic prediction](media/data-manager-configure-map-add-attributes-semantic-prediction.png "Attribute type and semantic prediction")</span></span>

<span data-ttu-id="6163e-135">Semantika pertsonalizatu mota bat gehitzea ere posible da.</span><span class="sxs-lookup"><span data-stu-id="6163e-135">Adding a custom semantic type is also possible.</span></span> <span data-ttu-id="6163e-136">Hautatu atributu horren mota-eremua eta idatzi zure semantika-mota pertsonalizatutako izena.</span><span class="sxs-lookup"><span data-stu-id="6163e-136">Select the type field for an attribute, and type your custom semantic type name.</span></span> <span data-ttu-id="6163e-137">Modu honetan, sistemak auto-identifikatutako auto atributu motak ere alda ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="6163e-137">This way, you can also change the attribute types that were identified by the system.</span></span>

<span data-ttu-id="6163e-138">Mota semantikoa automatikoki identifikatzen den atributu guztiak taldean biltzen dira **Berrikusi mapatutako eremuak** atala.</span><span class="sxs-lookup"><span data-stu-id="6163e-138">All attributes for which a semantic type is automatically identified are grouped in the **Review mapped fields** section.</span></span> <span data-ttu-id="6163e-139">Berrikusi atributu hauek eta horien mota semantikoak, zure erakundeak datuen bateratzearen bateratze-urratsean konbinatzeko erabiliko direlako.</span><span class="sxs-lookup"><span data-stu-id="6163e-139">Review these attributes and their semantic types because they'll be used to combine your entities in the merge step of data unification.</span></span>

<span data-ttu-id="6163e-140">Automatikoki mota semantiko batera mapatzen ez diren atributuak fitxategian biltzen dira **Definitu datuak mapatu gabeko eremuetan** atala.</span><span class="sxs-lookup"><span data-stu-id="6163e-140">Attributes that aren't automatically mapped to a semantic type are grouped in the **Define the data in the unmapped fields** section.</span></span> <span data-ttu-id="6163e-141">Hautatu mapatu gabeko atributuen mota semantikoaren eremua edo idatzi zure atributu mota izen pertsonalizatua.</span><span class="sxs-lookup"><span data-stu-id="6163e-141">Select the semantic type field for the unmapped attributes, or enter your custom attribute-type name.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="6163e-142">![Gako nagusia eta atributu mota](media/data-manager-configure-map-add-attributes.png "Gako nagusia eta atributu mota")</span><span class="sxs-lookup"><span data-stu-id="6163e-142">![Primary key and attribute type](media/data-manager-configure-map-add-attributes.png "Primary key and attribute type")</span></span>

> [!NOTE]
> <span data-ttu-id="6163e-143">Eremu batek Person.FullName mota semantikoarekin mapatu beharko luke bezeroaren izena bezero txartelean betetzeko.</span><span class="sxs-lookup"><span data-stu-id="6163e-143">One field should map to the semantic type Person.FullName to populate the customer name in customer card.</span></span> <span data-ttu-id="6163e-144">Bestela, bezeroen txartelak izenik gabe agertuko dira.</span><span class="sxs-lookup"><span data-stu-id="6163e-144">Otherwise, the customer cards will appear nameless.</span></span> 

## <a name="add-and-remove-attributes-and-entities"></a><span data-ttu-id="6163e-145">Gehitu eta kendu atributuak eta entitateak</span><span class="sxs-lookup"><span data-stu-id="6163e-145">Add and remove attributes and entities</span></span>

1. <span data-ttu-id="6163e-146">Aktibatuta **Bat egin** > **Mapa**, hautatu **Editatu eremuak**.</span><span class="sxs-lookup"><span data-stu-id="6163e-146">On **Unify** > **Map**, select **Edit fields**.</span></span>

2. <span data-ttu-id="6163e-147">**Editatu eremuak** panelean, gehitu edo kendu atributuak eta entitateak.</span><span class="sxs-lookup"><span data-stu-id="6163e-147">In the **Edit fields** pane, add or remove attributes and entities.</span></span> <span data-ttu-id="6163e-148">Erabili bilaketa edo korritua zure atributuak eta intereseko entitateak aurkitzeko eta hautatzeko.</span><span class="sxs-lookup"><span data-stu-id="6163e-148">Use the search or scroll to find and select your attributes and entities of interest.</span></span> <span data-ttu-id="6163e-149">Ezin duzu atributu edo entitate bat kendu dagoeneko parekatuta badaude.</span><span class="sxs-lookup"><span data-stu-id="6163e-149">You can't remove an attribute or an entity if they've already been matched.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="6163e-150">![Gehitu edo kendu atributuak](media/configure-data-map-edit.png "Gehitu edo kendu atributuak")</span><span class="sxs-lookup"><span data-stu-id="6163e-150">![Add or remove attributes](media/configure-data-map-edit.png "Add or remove attributes")</span></span>

3. <span data-ttu-id="6163e-151">Hautatu **Aplikatu**.</span><span class="sxs-lookup"><span data-stu-id="6163e-151">Select **Apply**.</span></span>

## <a name="add-images-to-profiles"></a><span data-ttu-id="6163e-152">Gehitu irudiak profiletan</span><span class="sxs-lookup"><span data-stu-id="6163e-152">Add images to profiles</span></span>

<span data-ttu-id="6163e-153">Entitateak URLak baditu jendaurrean eskuragarri dauden profileko irudiak edo logotipoak bidaltzeko, bezeroaren profil bateratuari gehitu diezaiokezu.</span><span class="sxs-lookup"><span data-stu-id="6163e-153">If an entity contains URLs to publicly available profile images or logos, you can add them to the unified customer profile.</span></span>

<span data-ttu-id="6163e-154">Hautatu entitatea eta aurkitu URLa duen profila irudia duen eremua.</span><span class="sxs-lookup"><span data-stu-id="6163e-154">Select the entity and find the field that contains the URL to the profile image.</span></span> <span data-ttu-id="6163e-155">**Mota** sarrerako eremuan eskuz sartu hurrengo balioa:</span><span class="sxs-lookup"><span data-stu-id="6163e-155">In the **Type** input field, manually enter the following value:</span></span> 
- <span data-ttu-id="6163e-156">Pertsona batentzat: Pertsona.ProfileImage</span><span class="sxs-lookup"><span data-stu-id="6163e-156">For a person: Person.ProfileImage</span></span>
- <span data-ttu-id="6163e-157">Erakunde batentzat: Organization.LogoImage</span><span class="sxs-lookup"><span data-stu-id="6163e-157">For an organization: Organization.LogoImage</span></span>

<span data-ttu-id="6163e-158">Jarraitu bateratze urratsekin eta ziurtatu irudiaren URLa duen atributua gehitzen dela [Batu](merge-entities.md) urratsa.</span><span class="sxs-lookup"><span data-stu-id="6163e-158">Continue with the unification steps and ensure the attribute that contains the image URL is also added in the [Merge](merge-entities.md) step.</span></span>

## <a name="set-attributes-for-organizations"></a><span data-ttu-id="6163e-159">Ezarri erakundeentzako atributuak</span><span class="sxs-lookup"><span data-stu-id="6163e-159">Set attributes for organizations</span></span>

<span data-ttu-id="6163e-160">Erakundeentzako (aurrebista), atributu mota "Organization.Name" kokatu behar da</span><span class="sxs-lookup"><span data-stu-id="6163e-160">For organizations (Preview), the attribute type should be mapped to "Organization.Name"</span></span>
> [!div class="mx-imgBorder"]
> <span data-ttu-id="6163e-161">![Gako nagusia eta atributu mota B2B](media/configure-data-map-edit-b2b.png "Gako nagusia eta atributu mota B2B")</span><span class="sxs-lookup"><span data-stu-id="6163e-161">![Primary key and attribute type B2B](media/configure-data-map-edit-b2b.png "Primary key and attribute type B2B")</span></span>

## <a name="next-step"></a><span data-ttu-id="6163e-162">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="6163e-162">Next step</span></span>

<span data-ttu-id="6163e-163">Datuak bateratzeko prozesuaren baitan, joan **Bat-etortzea** orria.</span><span class="sxs-lookup"><span data-stu-id="6163e-163">As part of the data unification process, go to the **Match** page.</span></span> <span data-ttu-id="6163e-164">Bisitatu [**Bat-etortzea**](match-entities.md) fase honen berri izateko.</span><span class="sxs-lookup"><span data-stu-id="6163e-164">Visit [**Match**](match-entities.md) to learn about this phase.</span></span>

> [!TIP]
> <span data-ttu-id="6163e-165">Ikusi hurrengo bideoa: [Lehen urratsak: Bezeroaren profil bateratua sortzea](https://youtu.be/oBfGEhucAxs).</span><span class="sxs-lookup"><span data-stu-id="6163e-165">Check out the following video: [Getting Started: Creating a Unified Customer Profile](https://youtu.be/oBfGEhucAxs).</span></span>
