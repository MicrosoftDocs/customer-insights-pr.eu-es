---
title: Sartu datuak Power Query konektore baten bidez
description: Konektoreak datu-iturburuetarako oinarrituz Power Query-n.
ms.date: 09/29/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.openlocfilehash: b9a1b30e37c3792aa7bdfcfc177da9e8a32c324d
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596898"
---
# <a name="connect-to-a-power-query-data-source"></a><span data-ttu-id="22649-103">Konektatu Power Query datu-iturburu batera</span><span class="sxs-lookup"><span data-stu-id="22649-103">Connect to a Power Query data source</span></span>

<span data-ttu-id="22649-104">Power Query-ek konektore multzo zabala eskaintzen du datuak irensteko.</span><span class="sxs-lookup"><span data-stu-id="22649-104">Power Query offers a broad set of connectors to ingest data.</span></span> <span data-ttu-id="22649-105">Konektore hauetako gehienek onartzen dute Dynamics 365 Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="22649-105">Most of these connectors are supported by Dynamics 365 Customer Insights.</span></span> <span data-ttu-id="22649-106">Power Query konektoreetan oinarritutako datu iturriak gehitzeak hurrengo atalean azaldutako urratsak jarraitzen ditu.</span><span class="sxs-lookup"><span data-stu-id="22649-106">Adding data sources based on Power Query connectors generally follows the steps outlined in the next section.</span></span> <span data-ttu-id="22649-107">Hala ere, erabiltzen duzun konektorearen arabera, informazio desberdina behar da.</span><span class="sxs-lookup"><span data-stu-id="22649-107">However, depending on the connector you use, different information is required.</span></span> <span data-ttu-id="22649-108">Informazio gehiagorako, ikusi banakako konektoreei buruzko dokumentazioa [Power Query konektore erreferentzia](/power-query/connectors/).</span><span class="sxs-lookup"><span data-stu-id="22649-108">For more information, see the documentation about individual connectors in the [Power Query connector reference](/power-query/connectors/).</span></span>

## <a name="create-a-new-data-source"></a><span data-ttu-id="22649-109">Sortu datu-iturburua</span><span class="sxs-lookup"><span data-stu-id="22649-109">Create a new data source</span></span>

1. <span data-ttu-id="22649-110">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="22649-110">In audience insights, go to **Data** > **Data sources**.</span></span>

1. <span data-ttu-id="22649-111">Hautatu **Gehitu datu-iturburua**.</span><span class="sxs-lookup"><span data-stu-id="22649-111">Select **Add data source**.</span></span>

1. <span data-ttu-id="22649-112">Aukeratu **Inportatu datuak** metodoa eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="22649-112">Choose the **Import data** method and select **Next**.</span></span>

1. <span data-ttu-id="22649-113">Eman **Izena** datu-iturburu-erako, eta hautatu **Hurrengoa** datu-iturburu sortzeko.</span><span class="sxs-lookup"><span data-stu-id="22649-113">Provide a **Name** for the data source, and select **Next** to create the data source.</span></span> <span data-ttu-id="22649-114">Jarri izena jarraibideei:</span><span class="sxs-lookup"><span data-stu-id="22649-114">Name guidelines:</span></span> 
   - <span data-ttu-id="22649-115">Hasi letra batekin.</span><span class="sxs-lookup"><span data-stu-id="22649-115">Start with a letter.</span></span>
   - <span data-ttu-id="22649-116">Erabili letrak eta zenbakiak soilik.</span><span class="sxs-lookup"><span data-stu-id="22649-116">Use letters and numbers only.</span></span> <span data-ttu-id="22649-117">Ezin da idatzi karaktere berezirik edo zuriunerik.</span><span class="sxs-lookup"><span data-stu-id="22649-117">Special characters and spaces are not allowed.</span></span>
   - <span data-ttu-id="22649-118">Erabili 3 eta 64 karaktere artean.</span><span class="sxs-lookup"><span data-stu-id="22649-118">Use between 3 and 64 characters.</span></span>

1. <span data-ttu-id="22649-119">Hautatu bat [erabilgarri dauden konektoreetatik](#available-power-query-data-sources).</span><span class="sxs-lookup"><span data-stu-id="22649-119">Choose one of the [available connectors](#available-power-query-data-sources).</span></span> <span data-ttu-id="22649-120">Adibide honetarako, hautatu dugu **Testua/CSV** konektore.</span><span class="sxs-lookup"><span data-stu-id="22649-120">For this example, we select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="22649-121">Idatzi beharrezko datuak **Konexio ezarpenak** hautatutako lokailurako eta hautatu **Hurrengoa** datuen aurrebista ikusteko.</span><span class="sxs-lookup"><span data-stu-id="22649-121">Enter the required details in the **Connection settings** for the selected connector and select **Next** to see a preview of the data.</span></span>

1. <span data-ttu-id="22649-122">Hautatu **Transformatu datuak**.</span><span class="sxs-lookup"><span data-stu-id="22649-122">Select **Transform data**.</span></span> <span data-ttu-id="22649-123">Urrats honetan entitateak gehituko dituzu zure datu-iturburu-era.</span><span class="sxs-lookup"><span data-stu-id="22649-123">In this step, you'll add entities to your data source.</span></span> <span data-ttu-id="22649-124">Entitateak datu multzoak dira.</span><span class="sxs-lookup"><span data-stu-id="22649-124">Entities are datasets.</span></span> <span data-ttu-id="22649-125">Datu-multzo ugari biltzen dituen datu-basea baduzu, datu-multzo bakoitza bere entitatea da.</span><span class="sxs-lookup"><span data-stu-id="22649-125">If you have a database that includes multiple datasets, each dataset is its own entity.</span></span>

1. <span data-ttu-id="22649-126">**Power Query - Editatu kontsultak** Elkarrizketa-koadroak datuak berrikusi eta hobetzeko aukera ematen du.</span><span class="sxs-lookup"><span data-stu-id="22649-126">The **Power Query - Edit queries** dialog lets you review and refine the data.</span></span> <span data-ttu-id="22649-127">Aukeratutako datu-iturburu sistemetan identifikatutako sistemak ezkerreko panelean agertzen dira.</span><span class="sxs-lookup"><span data-stu-id="22649-127">The entities that the systems identified in your selected data source appear in the left pane.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="22649-128">![Editatu eskaera eztabaida](media/data-manager-configure-edit-queries.png "Editatu eskaera eztabaida")</span><span class="sxs-lookup"><span data-stu-id="22649-128">![Edit queries dialog](media/data-manager-configure-edit-queries.png "Edit queries dialog")</span></span>

1. <span data-ttu-id="22649-129">Zure datuak ere eralda ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="22649-129">You can also transform your data.</span></span> <span data-ttu-id="22649-130">Hautatu entitate bat editatzeko edo eraldatzeko.</span><span class="sxs-lookup"><span data-stu-id="22649-130">Select an entity to edit or transform.</span></span> <span data-ttu-id="22649-131">Erabili Power Query leihoan dauden aukerak transformazioak aplikatzeko.</span><span class="sxs-lookup"><span data-stu-id="22649-131">Use the options in the Power Query window to apply transformations.</span></span> <span data-ttu-id="22649-132">Eraldaketa bakoitza azpian agertzen da **Urrats aplikatuak**.</span><span class="sxs-lookup"><span data-stu-id="22649-132">Each transformation gets listed under **Applied steps**.</span></span> <span data-ttu-id="22649-133">Power Query-ek aurrez eraikitako eraldaketa aukera ugari eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="22649-133">Power Query provides numerous pre-built transformation options.</span></span> <span data-ttu-id="22649-134">Informazio gehiagorako, ikusi [Power Query eraldaketak](/power-query/power-query-what-is-power-query#transformations).</span><span class="sxs-lookup"><span data-stu-id="22649-134">For more information, see [Power Query Transformations](/power-query/power-query-what-is-power-query#transformations).</span></span>

1. <span data-ttu-id="22649-135">Entitate osagarriak gehi ditzakezu zure datu-iturburu hautatuta **Lortu datuak** herrian **Editatu zalantzak** elkarrizketa.</span><span class="sxs-lookup"><span data-stu-id="22649-135">You can add additional entities to your data source by selecting **Get data** in the **Edit queries** dialog.</span></span>

   <span data-ttu-id="22649-136">Eraldaketa hauek oso gomendagarriak dira:</span><span class="sxs-lookup"><span data-stu-id="22649-136">These transformations are highly recommended:</span></span>

   - <span data-ttu-id="22649-137">CSV fitxategi bateko datuak irensten badituzu, lehenengo ilaran maiz goiburuak agertzen dira.</span><span class="sxs-lookup"><span data-stu-id="22649-137">If you're ingesting data from a CSV file, the first row often contains headers.</span></span> <span data-ttu-id="22649-138">Joan **Transformatu mahaia** eta hautatu **Erabili goiburuak lehen ilara gisa**.</span><span class="sxs-lookup"><span data-stu-id="22649-138">Go to **Transform table** and select **Use headers as first row**.</span></span>
   - <span data-ttu-id="22649-139">Ziurtatu datu mota behar bezala ezarrita dagoela.</span><span class="sxs-lookup"><span data-stu-id="22649-139">Ensure the data type is set appropriately.</span></span>

1. <span data-ttu-id="22649-140">Hautatu **Gorde** Power Query leihoaren azpian gordetzeko eraldaketak.</span><span class="sxs-lookup"><span data-stu-id="22649-140">Select **Save** at the bottom of the Power Query window to save the transformations.</span></span> <span data-ttu-id="22649-141">Gorde ondoren, zure datu-iturburu aktibatuta aurkituko duzu **Datu-iturburuak** > **Datu iturriak**.</span><span class="sxs-lookup"><span data-stu-id="22649-141">After saving, you'll find your data source on **Data** > **Data sources**.</span></span>

1. <span data-ttu-id="22649-142">Gainean **Datu iturriak** orrialdean, datu-iturburu berria dagoela ohartuko zara **Freskagarria** egoera.</span><span class="sxs-lookup"><span data-stu-id="22649-142">On the **Data sources** page, you'll notice the new data source is in **Refreshing** status.</span></span>

## <a name="available-power-query-data-sources"></a><span data-ttu-id="22649-143">Eskuragarri dauden Power Query datu iturriak</span><span class="sxs-lookup"><span data-stu-id="22649-143">Available Power Query data sources</span></span>

<span data-ttu-id="22649-144">Ikusi [Power Query konektore erreferentzia](/power-query/connectors/) datuak Customer Insights inportatzeko hauta ditzakezun konektoreen zerrenda eguneratua lortzeko.</span><span class="sxs-lookup"><span data-stu-id="22649-144">See the [Power Query connector reference](/power-query/connectors/) for an up-to-date list of connectors that you can select to import data to Customer Insights.</span></span> 

<span data-ttu-id="22649-145">Konektoreak kontrol-markarekin **Customer Insights (datu-fluxuak)** zutabea eskuragarri dago Power Query oinarritutako datu iturri berriak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="22649-145">Connectors with a checkmark in the **Customer Insights (Dataflows)** column are available to create new data sources based on Power Query.</span></span> <span data-ttu-id="22649-146">Berrikusi konektore zehatz baten dokumentazioa, bere aurretiazko baldintzak, mugak eta bestelako xehetasunak ezagutzeko.</span><span class="sxs-lookup"><span data-stu-id="22649-146">Review the documentation of a specific connector to learn more about its prerequisites, limitations, and other details.</span></span>

## <a name="edit-power-query-data-sources"></a><span data-ttu-id="22649-147">Editatu Power Query datu iturriak</span><span class="sxs-lookup"><span data-stu-id="22649-147">Edit Power Query data sources</span></span>

> [!NOTE]
> <span data-ttu-id="22649-148">Agian ez da posible aplikazioaren prozesuetako batean erabiltzen ari diren datu iturrietan aldaketak egitea (*segmentazio*, *bat-etortzea*, edo *konbinatu*, adibidez).</span><span class="sxs-lookup"><span data-stu-id="22649-148">It might not be possible to make changes to data sources that are currently being used in one of the app's processes (*segmentation*, *match*, or *merge*, for example).</span></span> 
>
> <span data-ttu-id="22649-149">. Erabiliz **ezarpenak** orrialdea, prozesu aktibo bakoitzaren bilakaeraren jarraipena egin dezakezu.</span><span class="sxs-lookup"><span data-stu-id="22649-149">Using the **Settings** page, you can track the progress of each of the active processes.</span></span> <span data-ttu-id="22649-150">Prozesua amaitutakoan, gailura itzuli dezakezu **Datu iturriak** orria eta egin zure aldaketak.</span><span class="sxs-lookup"><span data-stu-id="22649-150">When a process completes, you can return to the **Data Sources** page and make your changes.</span></span>

1. <span data-ttu-id="22649-151">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="22649-151">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="22649-152">Hautatu aldatu nahi duzun datu-iturburu ondoko elipsi bertikala **Editatu** goitibeherako menuan.</span><span class="sxs-lookup"><span data-stu-id="22649-152">Select the vertical ellipsis next to the data source you want to change and select **Edit** from the drop-down menu.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="22649-153">![Editatu aukera](media/edit-option-data-sources.png "Editatu aukera")</span><span class="sxs-lookup"><span data-stu-id="22649-153">![Edit option](media/edit-option-data-sources.png "Edit option")</span></span>

3. <span data-ttu-id="22649-154">Aplikatu aldaketak eta eraldaketak **Power Query - Editatu kontsultak** elkarrizketa - koadroan deskribatutako moduan [Sortu datu-iturburu berria](#create-a-new-data-source) atala.</span><span class="sxs-lookup"><span data-stu-id="22649-154">Apply your changes and transformations in the **Power Query - Edit queries** dialog as described in the [Create a new data source](#create-a-new-data-source) section.</span></span>

4. <span data-ttu-id="22649-155">Aukeratu **Gorde** Power Query-en aldaketak gordetzeko aldaketak egin ondoren.</span><span class="sxs-lookup"><span data-stu-id="22649-155">Select **Save** in Power Query after completing your edits to save your changes.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]