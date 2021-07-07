---
title: HERE Technologies Aberastea hirugarrenen aberastasunarekin
description: HERE Technologies-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: b3c1da0f541efb85b2ca9d87a2e3b97bbfb6ca7f
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305279"
---
# <a name="enrichment-of-customer-profiles-with-here-technologies-preview"></a><span data-ttu-id="50a34-103">Bezeroen profilak aberastea HERE Technologies-ekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="50a34-103">Enrichment of customer profiles with HERE Technologies (preview)</span></span>

<span data-ttu-id="50a34-104">HERE Technologies kokapen-plataformako enpresa da, kokapenari buruzko datuak eta zerbitzuak eskaintzen dituena.</span><span class="sxs-lookup"><span data-stu-id="50a34-104">HERE Technologies is a location platform company that provides location-centric data and services.</span></span> <span data-ttu-id="50a34-105">HERE Technologies-en datuak aberasteko zerbitzuekin, zure bezeroen kokapen zehatzagoa ulertu ahal izango duzu helbide normalizazioarekin, latitudea eta longitudea erauztearekin eta abarrekin.</span><span class="sxs-lookup"><span data-stu-id="50a34-105">With HERE Technologies' data enrichment services, you can build a more precise location understanding of your customers with address normalization, latitude and longitude extraction, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="50a34-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="50a34-106">Prerequisites</span></span>

<span data-ttu-id="50a34-107">HERE Technologies-en aberastea konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="50a34-107">To configure HERE Technologies enrichments, the following prerequisites must be met:</span></span>

- <span data-ttu-id="50a34-108">HERE Technologies-en harpidetza aktiboa duzu.</span><span class="sxs-lookup"><span data-stu-id="50a34-108">You have an active HERE Technologies subscription.</span></span> <span data-ttu-id="50a34-109">Harpidetza lortzeko, [erregistratu hemen](https://developer.here.com/sign-up?utm_medium=referral&utm_source=Microsoft-Dynamics-CI&create=Freemium-Basic) edo [jarri harremanetan HERE Technologies-ekin](https://developer.here.com/help?utm_medium=referral&utm_source=Microsoft-Dynamics-CI#how-can-we-help-you) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="50a34-109">To get a subscription, you can [sign up here](https://developer.here.com/sign-up?utm_medium=referral&utm_source=Microsoft-Dynamics-CI&create=Freemium-Basic) or [contact HERE Technologies](https://developer.here.com/help?utm_medium=referral&utm_source=Microsoft-Dynamics-CI#how-can-we-help-you) directly.</span></span> [<span data-ttu-id="50a34-110">Lortu informazio gehiago HERE Technologies-en kokapen-aberasteari buruz.</span><span class="sxs-lookup"><span data-stu-id="50a34-110">Learn more about HERE Technologies Location Enrichment.</span></span>](https://developer.here.com/location-enrichment?cid=Dev-MicrosoftDynamics-DB-0-Dev-&utm_source=MicrosoftDynamics&utm_medium=referral&utm_campaign=Online_Dev_ReferralMicrosoft)

- <span data-ttu-id="50a34-111">HERE [konexioa](connections.md) eskuragarri dago *edo* duzu [administratzailea](permissions.md#administrator) baimenak eta HERE Technologies API gakoa.</span><span class="sxs-lookup"><span data-stu-id="50a34-111">A HERE [connection](connections.md) is available *or* you have [administrator](permissions.md#administrator) permissions and the HERE Technologies API key.</span></span>

## <a name="configure-the-enrichment"></a><span data-ttu-id="50a34-112">Konfiguratu aberastea</span><span class="sxs-lookup"><span data-stu-id="50a34-112">Configure the enrichment</span></span>

1. <span data-ttu-id="50a34-113">Joan **Datuak** > **Aberastua**.</span><span class="sxs-lookup"><span data-stu-id="50a34-113">Go to **Data** > **Enrichment**.</span></span> 

1. <span data-ttu-id="50a34-114">Aukeratu **Aberastu nire datuak** HERE Technologies fitxan eta hautatu **Hasi**.</span><span class="sxs-lookup"><span data-stu-id="50a34-114">Select **Enrich my data** on the HERE Technologies tile and select **Get started**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="50a34-115">![HERE Technologies-en lauza](media/HERE-tile.png "HERE Technologies-en lauza")</span><span class="sxs-lookup"><span data-stu-id="50a34-115">![HERE Technologies tile](media/HERE-tile.png "HERE Technologies tile")</span></span>

1. <span data-ttu-id="50a34-116">Hautatu goitibeherako zerrendako [konexio](connections.md) bat.</span><span class="sxs-lookup"><span data-stu-id="50a34-116">Select a [connection](connections.md) from the dropdown list.</span></span> <span data-ttu-id="50a34-117">Jarri harremanetan administratzaile batekin konexiorik ez badago.</span><span class="sxs-lookup"><span data-stu-id="50a34-117">Contact  an administrator if no connection is available.</span></span> <span data-ttu-id="50a34-118">Administratzailea bazara, hautatuz konexioa sor dezakezu **Gehitu konexioa**.</span><span class="sxs-lookup"><span data-stu-id="50a34-118">If you are an administrator, you can create a connection by selecting **Add connection**.</span></span> <span data-ttu-id="50a34-119">Aukeratu **HERE Technologies** goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="50a34-119">Choose **HERE Technologies** from the dropdown list.</span></span> 

1. <span data-ttu-id="50a34-120">Aukeratu **Konektatu HERE Teknologietara** hautapena berresteko.</span><span class="sxs-lookup"><span data-stu-id="50a34-120">Select **Connect to HERE Technologies** to confirm the selection.</span></span>

1.  <span data-ttu-id="50a34-121">Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** HERE Teknologien kokapen datuekin aberastu nahi duzu.</span><span class="sxs-lookup"><span data-stu-id="50a34-121">Select **Next** and choose the **Customer data set** you want to enrich with location data from HERE Technologies.</span></span> <span data-ttu-id="50a34-122">**Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="50a34-122">You can select the **Customer** entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

    :::image type="content" source="media/enrichment-HERE-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. <span data-ttu-id="50a34-124">Aukeratu eremuak lehen eta/edo bigarren helbidera esleitu nahi dituzun.</span><span class="sxs-lookup"><span data-stu-id="50a34-124">Choose if you want to map fields to the primary and/or secondary address.</span></span> <span data-ttu-id="50a34-125">Bi helbideen eremuen mapak zehaztu ditzakezu eta bi helbideen profilak bereiz aberastu.</span><span class="sxs-lookup"><span data-stu-id="50a34-125">You can specify a field mapping for both addresses and enrich the profiles for both addresses separately.</span></span> <span data-ttu-id="50a34-126">Adibidez, etxea eta negozioaren helbidea badaude.</span><span class="sxs-lookup"><span data-stu-id="50a34-126">For example, if there's a home and a business address.</span></span> <span data-ttu-id="50a34-127">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="50a34-127">Select **Next**.</span></span>

1. <span data-ttu-id="50a34-128">Zehaztu zure profil bateratuetako zein eremu erabili beharko liratekeen HERE Technologies-en bat datozen kokapen datuak bilatzeko.</span><span class="sxs-lookup"><span data-stu-id="50a34-128">Define which fields from your unified profiles should be used to look for matching location data from HERE Technologies.</span></span> <span data-ttu-id="50a34-129">**1. kalea** eta **Zip / Posta Kodea** eremuak derrigorrezkoak dira hautatutako lehen eta / edo bigarren mailako helbidean.</span><span class="sxs-lookup"><span data-stu-id="50a34-129">The **Street 1** and **Zip/Postal Code** fields are required for the selected primary and/or secondary address.</span></span> <span data-ttu-id="50a34-130">Bat-etortze zehatzagoak lortzeko, eremu gehiago gehitu daitezke.</span><span class="sxs-lookup"><span data-stu-id="50a34-130">For a higher match accuracy, more fields can be added.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="50a34-131">![HERE Technologies-en aberastearen konfigurazio orria](media/enrichment-HERE-configuration.png "HERE Technologies-en aberastearen konfigurazio orria")</span><span class="sxs-lookup"><span data-stu-id="50a34-131">![HERE Technologies enrichment configuration page](media/enrichment-HERE-configuration.png "HERE Technologies enrichment configuration page")</span></span>

1. <span data-ttu-id="50a34-132">Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.</span><span class="sxs-lookup"><span data-stu-id="50a34-132">Select **Next** to complete the field mapping.</span></span>

1. <span data-ttu-id="50a34-133">Idatzi aberastearen izena.</span><span class="sxs-lookup"><span data-stu-id="50a34-133">Provide a name for the enrichment.</span></span> 

1. <span data-ttu-id="50a34-134">Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.</span><span class="sxs-lookup"><span data-stu-id="50a34-134">Select **Save enrichment** after reviewing your choices.</span></span>

## <a name="configure-the-connection-for-here-technologies"></a><span data-ttu-id="50a34-135">Konfiguratu konexioa HERE Technologies</span><span class="sxs-lookup"><span data-stu-id="50a34-135">Configure the connection for HERE Technologies</span></span> 

<span data-ttu-id="50a34-136">Administratzailea izan behar duzu konexioak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="50a34-136">You need to be an administrator to configure connections.</span></span> <span data-ttu-id="50a34-137">Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** HERE Technologies fitxan.</span><span class="sxs-lookup"><span data-stu-id="50a34-137">Select **Add connection** when configuring an enrichment *or* go to **Admin** > **Connections** and select **Set up** on the HERE Technologies tile.</span></span>

1. <span data-ttu-id="50a34-138">Idatzi konexioaren izena **Bistaratzeko izena** kutxa.</span><span class="sxs-lookup"><span data-stu-id="50a34-138">Enter a name for the connection in the **Display name** box.</span></span>

1. <span data-ttu-id="50a34-139">Eman baliozko HERE Technologies API gakoa.</span><span class="sxs-lookup"><span data-stu-id="50a34-139">Provide a valid HERE Technologies API key.</span></span>

1. <span data-ttu-id="50a34-140">Berrikusi eta eman zure baimena **Datuen pribatutasuna eta betetzea** hautatuz **Ados**.</span><span class="sxs-lookup"><span data-stu-id="50a34-140">Review and provide your consent for **Data privacy and compliance** by selecting **I agree**.</span></span>

1. <span data-ttu-id="50a34-141">Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.</span><span class="sxs-lookup"><span data-stu-id="50a34-141">Select **Verify** to validate the configuration.</span></span>

1. <span data-ttu-id="50a34-142">Egiaztapena amaitu ondoren, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="50a34-142">After completing the verification, select **Save**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="50a34-143">![HEMEN teknologien konexioa konfigurazioaren orria](media/enrichment-HERE-connection.png "HEMEN teknologien konexioa konfigurazioaren orria")</span><span class="sxs-lookup"><span data-stu-id="50a34-143">![HERE Technologies connection configuration page](media/enrichment-HERE-connection.png "HERE Technologies connection configuration page")</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="50a34-144">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="50a34-144">Enrichment results</span></span>

<span data-ttu-id="50a34-145">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="50a34-145">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="50a34-146">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="50a34-146">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="50a34-147">Prozesatzeko denbora zure bezeroen datuen tamainaren eta HERE Technologies-en APIaren erantzun denboren araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="50a34-147">The processing time will depend on the size of your customer data and the API response times from HERE Technologies.</span></span>

<span data-ttu-id="50a34-148">Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**.</span><span class="sxs-lookup"><span data-stu-id="50a34-148">After the enrichment process completes, you can review the newly enriched customer profiles data under **My enrichments**.</span></span> <span data-ttu-id="50a34-149">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="50a34-149">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="50a34-150">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="50a34-150">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="50a34-151">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="50a34-151">Next steps</span></span>

<span data-ttu-id="50a34-152">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="50a34-152">Build on top of your enriched customer data.</span></span> <span data-ttu-id="50a34-153">Sortu [segmentuak](segments.md) eta [neurriak](measures.md), eta are [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="50a34-153">Create [segments](segments.md) and [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="50a34-154">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="50a34-154">Data privacy and compliance</span></span>

<span data-ttu-id="50a34-155">Dynamics 365 Customer Insights gaitzen duzunean datuak HERE Technologies-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="50a34-155">When you enable Dynamics 365 Customer Insights to transmit data to HERE Technologies, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="50a34-156">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da HERE Technologies-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="50a34-156">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that HERE Technologies meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="50a34-157">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="50a34-157">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="50a34-158">Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="50a34-158">Your Dynamics 365 Customer Insights administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
