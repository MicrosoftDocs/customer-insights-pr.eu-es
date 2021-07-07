---
title: Aberastea hirugarrenen aberastasunarekin Experian
description: -Ri buruzko informazio orokorra Experian hirugarrenen aberastea.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 7c82fe92b3351a782a4fa6510300d870b742d042
ms.sourcegitcommit: 42b3bce1e20e7cc707d232844dacfeed3d6fc096
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/28/2021
ms.locfileid: "6309805"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a><span data-ttu-id="dc02c-103">Aberastu bezeroen profilak datu demografikoekin Experian (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="dc02c-103">Enrich customer profiles with demographics from Experian (preview)</span></span>

<span data-ttu-id="dc02c-104">Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta merkaturatzeko zerbitzuetan.</span><span class="sxs-lookup"><span data-stu-id="dc02c-104">Experian is a global leader in consumer and business credit reporting and marketing services.</span></span> <span data-ttu-id="dc02c-105">Batera Experian Datuak aberasteko zerbitzuak, zure bezeroen ezagutza sakonagoa eraiki dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.</span><span class="sxs-lookup"><span data-stu-id="dc02c-105">With Experian’s data enrichment services, you can build a deeper understanding of your customers by enriching your customer profiles with demographic data such as household size, income, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dc02c-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="dc02c-106">Prerequisites</span></span>

<span data-ttu-id="dc02c-107">Konfiguratzeko Experian, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="dc02c-107">To configure Experian, the following prerequisites must be met:</span></span>

- <span data-ttu-id="dc02c-108">Experian harpidetza aktiboa izan behar duzu.</span><span class="sxs-lookup"><span data-stu-id="dc02c-108">You have an active Experian subscription.</span></span> <span data-ttu-id="dc02c-109">Harpidetza lortzeko, [harremanetarako Experian](https://www.experian.com/marketing-services/contact) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="dc02c-109">To get a subscription, [contact Experian](https://www.experian.com/marketing-services/contact) directly.</span></span> <span data-ttu-id="dc02c-110">[Lortu informazio gehiago Experian datuen eraginari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span><span class="sxs-lookup"><span data-stu-id="dc02c-110">[Learn more about Experian Data Enrichment](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span></span>

- <span data-ttu-id="dc02c-111">Administratzaile batek Experian konexioa konfiguratu du dagoeneko *edo* duzu [administratzailea](permissions.md#administrator) baimenak.</span><span class="sxs-lookup"><span data-stu-id="dc02c-111">An Experian connection has already been configured by an administrator *or* you have [administrator](permissions.md#administrator) permissions.</span></span> <span data-ttu-id="dc02c-112">Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia ere behar dituzu SSH gaitutako Garraio Seguru (ST) konturako Experian zuretzat sortua.</span><span class="sxs-lookup"><span data-stu-id="dc02c-112">You also need the User ID, Party ID, and Model Number for your SSH-enabled Secure Transport (ST) account that Experian created for you.</span></span>

## <a name="supported-countriesregions"></a><span data-ttu-id="dc02c-113">Lagundutako herrialde / eskualdeak</span><span class="sxs-lookup"><span data-stu-id="dc02c-113">Supported countries/regions</span></span>

<span data-ttu-id="dc02c-114">Gaur egun, Estatu Batuetan bezeroen profil aberasgarriak onartzen ditugu.</span><span class="sxs-lookup"><span data-stu-id="dc02c-114">We currently support enriching customer profiles in the United States only.</span></span>

## <a name="configure-the-enrichment"></a><span data-ttu-id="dc02c-115">Konfiguratu aberastea</span><span class="sxs-lookup"><span data-stu-id="dc02c-115">Configure the enrichment</span></span>

1. <span data-ttu-id="dc02c-116">Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="dc02c-116">Go to **Data** > **Enrichment** and select the **Discover** tab.</span></span>

1. <span data-ttu-id="dc02c-117">Aukeratu **Aberastu nire datuak** gainean Experian teila.</span><span class="sxs-lookup"><span data-stu-id="dc02c-117">Select **Enrich my data** on the Experian tile.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="dc02c-118">![Experian lauza](media/experian-tile.png "Experian lauza")</span><span class="sxs-lookup"><span data-stu-id="dc02c-118">![Experian tile](media/experian-tile.png "Experian tile")</span></span>
   > 

1. <span data-ttu-id="dc02c-119">Hautatu goitibeherako zerrendako [konexio](connections.md) bat.</span><span class="sxs-lookup"><span data-stu-id="dc02c-119">Select a [connection](connections.md) from the dropdown list.</span></span> <span data-ttu-id="dc02c-120">Jarri harremanetan administratzaile batekin konexiorik ez badago.</span><span class="sxs-lookup"><span data-stu-id="dc02c-120">Contact an administrator if no connection is available.</span></span> <span data-ttu-id="dc02c-121">Administratzailea bazara, konexioa sor dezakezu hautatuta **Gehitu konexioa** eta aukeratzea Experian goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="dc02c-121">If you are an administrator, you can create a connection by selecting **Add connection** and choosing Experian from the dropdown list.</span></span> 

1. <span data-ttu-id="dc02c-122">Aukeratu **Konektatu Experian** konexioaren hautapena berresteko.</span><span class="sxs-lookup"><span data-stu-id="dc02c-122">Select **Connect to Experian** to confirm the connection selection.</span></span>

1.  <span data-ttu-id="dc02c-123">Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** datu demografikoekin aberastu nahi duzu Experian-etik.</span><span class="sxs-lookup"><span data-stu-id="dc02c-123">Select **Next** and choose the **Customer data set** you want to enrich with demographics data from Experian.</span></span> <span data-ttu-id="dc02c-124">**Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="dc02c-124">You can select the **Customer** entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

    :::image type="content" source="media/enrichment-Experian-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. <span data-ttu-id="dc02c-126">Aukeratu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu mota erabili behar diren datu demografikoekin bat datozenak bilatzeko Experian.</span><span class="sxs-lookup"><span data-stu-id="dc02c-126">Select **Next** and define which type of fields from your unified profiles should be used to look for matching demographics data from Experian.</span></span> <span data-ttu-id="dc02c-127">Eremuetako bat gutxienez **Izena eta helbidea**, **Mugikorra**, edo **Posta elektronikoa** beharrezkoa da.</span><span class="sxs-lookup"><span data-stu-id="dc02c-127">At least one of the fields **Name and address**, **Phone**, or **Email** is required.</span></span> <span data-ttu-id="dc02c-128">Partiduen zehaztasun handiagoa lortzeko, beste bi eremu gehi daitezke.</span><span class="sxs-lookup"><span data-stu-id="dc02c-128">For a higher match accuracy, up to two other fields can be added.</span></span> <span data-ttu-id="dc02c-129">Aukeraketa honek hurrengo urratsean atzitu ditzakezun mapen eremuei eragingo die.</span><span class="sxs-lookup"><span data-stu-id="dc02c-129">This selection will affect the mapping fields you have access to in the next step.</span></span>

    > [!TIP]
    > <span data-ttu-id="dc02c-130">Gako identifikatzaile atributu gehiago bidali dira Experian litekeena da partida-tasa handiagoa lortzea.</span><span class="sxs-lookup"><span data-stu-id="dc02c-130">More key identifier attributes sent to Experian likely yield a higher match rate.</span></span>

1. <span data-ttu-id="dc02c-131">Hautatu **Hurrengoa** eremuaren jarraipena hasteko.</span><span class="sxs-lookup"><span data-stu-id="dc02c-131">Select **Next** to start the field mapping.</span></span>

1. <span data-ttu-id="dc02c-132">Zehaztu profil bateratuetako zein eremu mota erabili behar diren datu demografikoekin bat datozenak bilatzeko Experian.</span><span class="sxs-lookup"><span data-stu-id="dc02c-132">Define which fields from your unified profiles should be used to look for matching demographics data from Experian.</span></span> <span data-ttu-id="dc02c-133">Eskatutako eremuak markatuta daude.</span><span class="sxs-lookup"><span data-stu-id="dc02c-133">Required fields are marked.</span></span>

1. <span data-ttu-id="dc02c-134">Hornitu aberasturako izena eta irteerako entitatearen izena.</span><span class="sxs-lookup"><span data-stu-id="dc02c-134">Provide a name for the enrichment and a name for the output entity.</span></span>

1. <span data-ttu-id="dc02c-135">Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.</span><span class="sxs-lookup"><span data-stu-id="dc02c-135">Select **Save enrichment** after reviewing your choices.</span></span>

## <a name="configure-the-connection-for-experian"></a><span data-ttu-id="dc02c-136">Konfiguratu konexio-funtzioak Experian-en</span><span class="sxs-lookup"><span data-stu-id="dc02c-136">Configure the connection for Experian</span></span> 

<span data-ttu-id="dc02c-137">Administratzailea izan behar duzu konexioak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="dc02c-137">You need to be an administrator to configure connections.</span></span> <span data-ttu-id="dc02c-138">Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** gainean Experian lauza.</span><span class="sxs-lookup"><span data-stu-id="dc02c-138">Select **Add connection** when configuring an enrichment *or* go to **Admin** > **Connections** and select **Set up** on the Experian tile.</span></span>

1. <span data-ttu-id="dc02c-139">Hautatu **Hasi erabiltzen**.</span><span class="sxs-lookup"><span data-stu-id="dc02c-139">Select **Get Started**.</span></span>

1. <span data-ttu-id="dc02c-140">Idatzi konexioaren izena **Bistaratzeko izena** kutxa.</span><span class="sxs-lookup"><span data-stu-id="dc02c-140">Enter a name for the connection in the **Display name** box.</span></span>

1. <span data-ttu-id="dc02c-141">Idatzi baliozko Erabiltzaile IDa, Alderdiaren IDa eta Modelo Zenbakia Experian Garraio Seguruaren kontua.</span><span class="sxs-lookup"><span data-stu-id="dc02c-141">Enter valid User ID, Party ID, and Model Number for your Experian Secure Transport account.</span></span>

1. <span data-ttu-id="dc02c-142">Berrikusi eta eman zure baimena **Datuen pribatutasuna eta betetzea** hautatuz **Ados**.</span><span class="sxs-lookup"><span data-stu-id="dc02c-142">Review and provide your consent for **Data privacy and compliance** by selecting **I agree**.</span></span>

1. <span data-ttu-id="dc02c-143">Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.</span><span class="sxs-lookup"><span data-stu-id="dc02c-143">Select **Verify** to validate the configuration.</span></span>

1. <span data-ttu-id="dc02c-144">Egiaztapena amaitu ondoren, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="dc02c-144">After completing the verification, select **Save**.</span></span>
   
   :::image type="content" source="media/enrichment-Experian-connection.png" alt-text="Experian konexioaren konfigurazio-panela.":::

## <a name="enrichment-results"></a><span data-ttu-id="dc02c-146">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="dc02c-146">Enrichment results</span></span>

<span data-ttu-id="dc02c-147">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="dc02c-147">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="dc02c-148">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="dc02c-148">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="dc02c-149">Prozesatzeko denbora zure bezeroen datuen tamainaren eta zure konturako aberastutako prozesuen araberakoa izango da Experian.</span><span class="sxs-lookup"><span data-stu-id="dc02c-149">The processing time will depend on the size of your customer data and the enrichment processes set up for your account by Experian.</span></span>

<span data-ttu-id="dc02c-150">Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**.</span><span class="sxs-lookup"><span data-stu-id="dc02c-150">After the enrichment process completes, you can review the newly enriched customer profiles data under **My enrichments**.</span></span> <span data-ttu-id="dc02c-151">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="dc02c-151">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="dc02c-152">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="dc02c-152">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dc02c-153">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="dc02c-153">Next steps</span></span>

<span data-ttu-id="dc02c-154">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="dc02c-154">Build on top of your enriched customer data.</span></span> <span data-ttu-id="dc02c-155">Sortu [segmentuak](segments.md) eta [neurriak](measures.md), eta are [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="dc02c-155">Create [segments](segments.md) and [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="dc02c-156">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="dc02c-156">Data privacy and compliance</span></span>

<span data-ttu-id="dc02c-157">Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko Experian, datuak betetze mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="dc02c-157">When you enable Dynamics 365 Customer Insights to transmit data to Experian, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="dc02c-158">Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz Experian izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu.</span><span class="sxs-lookup"><span data-stu-id="dc02c-158">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Experian meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="dc02c-159">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="dc02c-159">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="dc02c-160">Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="dc02c-160">Your Dynamics 365 Customer Insights administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
