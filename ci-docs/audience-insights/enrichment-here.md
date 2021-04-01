---
title: HERE Technologies hirugarrenen aberastearekin aberastea
description: HERE Technologies-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 12/10/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: 8e8d6bfea4e0df54682501f60759c24c893444af
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597726"
---
# <a name="enrichment-of-customer-profiles-with-here-technologies-preview"></a><span data-ttu-id="2aef3-103">Bezeroen profilak aberastea HERE Technologies-ekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="2aef3-103">Enrichment of customer profiles with HERE Technologies (preview)</span></span>

<span data-ttu-id="2aef3-104">HERE Technologies kokapen-plataformako enpresa da, kokapenari buruzko datuak eta zerbitzuak eskaintzen dituena.</span><span class="sxs-lookup"><span data-stu-id="2aef3-104">HERE Technologies is a location platform company that provides location-centric data and services.</span></span> <span data-ttu-id="2aef3-105">HERE Technologies-en datuak aberasteko zerbitzuekin, zure bezeroen kokapen zehatzagoa ulertu ahal izango duzu helbide normalizazioarekin, latitudea eta longitudea erauztearekin eta abarrekin.</span><span class="sxs-lookup"><span data-stu-id="2aef3-105">With HERE Technologies' data enrichment services, you can build a more precise location understanding of your customers with address normalization, latitude and longitude extraction, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2aef3-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="2aef3-106">Prerequisites</span></span>

<span data-ttu-id="2aef3-107">HERE Technologies-en aberastea konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="2aef3-107">To configure HERE Technologies enrichments, the following prerequisites must be met:</span></span>

- <span data-ttu-id="2aef3-108">HERE Technologies-en harpidetza aktiboa duzu.</span><span class="sxs-lookup"><span data-stu-id="2aef3-108">You have an active HERE Technologies subscription.</span></span> <span data-ttu-id="2aef3-109">Harpidetza lortzeko, [erregistratu hemen](https://developer.here.com/sign-up?utm_medium=referral&utm_source=Microsoft-Dynamics-CI&create=Freemium-Basic) edo [jarri harremanetan HERE Technologies-ekin](https://developer.here.com/help?utm_medium=referral&utm_source=Microsoft-Dynamics-CI#how-can-we-help-you) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="2aef3-109">To get a subscription, you can [sign-up here](https://developer.here.com/sign-up?utm_medium=referral&utm_source=Microsoft-Dynamics-CI&create=Freemium-Basic) or [contact HERE Technologies](https://developer.here.com/help?utm_medium=referral&utm_source=Microsoft-Dynamics-CI#how-can-we-help-you) directly.</span></span> [<span data-ttu-id="2aef3-110">Lortu informazio gehiago HERE Technologies-en kokapen-aberasteari buruz.</span><span class="sxs-lookup"><span data-stu-id="2aef3-110">Learn more about HERE Technologies Location Enrichment.</span></span>](https://developer.here.com/location-enrichment?cid=Dev-MicrosoftDynamics-DB-0-Dev-&utm_source=MicrosoftDynamics&utm_medium=referral&utm_campaign=Online_Dev_ReferralMicrosoft)

- <span data-ttu-id="2aef3-111">HERE Technologies-en API gakoa duzu.</span><span class="sxs-lookup"><span data-stu-id="2aef3-111">You have the HERE Technologies API key.</span></span>

- <span data-ttu-id="2aef3-112">[Administratzaile](permissions.md#administrator) baimenak dituzu.</span><span class="sxs-lookup"><span data-stu-id="2aef3-112">You have [Administrator](permissions.md#administrator) permissions.</span></span>

## <a name="configuration"></a><span data-ttu-id="2aef3-113">Konfigurazioa</span><span class="sxs-lookup"><span data-stu-id="2aef3-113">Configuration</span></span>

1. <span data-ttu-id="2aef3-114">Joan **Datuak** > **Aberastua**.</span><span class="sxs-lookup"><span data-stu-id="2aef3-114">Go to **Data** > **Enrichment**.</span></span>

1. <span data-ttu-id="2aef3-115">Hautatu **aberastu datuak** HERE Technologies-en lauzan.</span><span class="sxs-lookup"><span data-stu-id="2aef3-115">Select **Enrich my data** on the HERE Technologies tile.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="2aef3-116">![HERE Technologies-en lauza](media/HERE-tile.png "HERE Technologies-en lauza")</span><span class="sxs-lookup"><span data-stu-id="2aef3-116">![HERE Technologies tile](media/HERE-tile.png "HERE Technologies tile")</span></span>

1. <span data-ttu-id="2aef3-117">Sartu **HERE Technologies API gako** aktibo bat.</span><span class="sxs-lookup"><span data-stu-id="2aef3-117">Enter an active **HERE Technologies API key**.</span></span> <span data-ttu-id="2aef3-118">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="2aef3-118">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span> 

1. <span data-ttu-id="2aef3-119">Berretsi bi sarrerak **Konektatu HERE-ra** hautatuta.</span><span class="sxs-lookup"><span data-stu-id="2aef3-119">Confirm both inputs by selecting **Connect to HERE**.</span></span>

1.  <span data-ttu-id="2aef3-120">Aukeratu **Gehitu datuak** eta aukeratu HERE Technologies-eko enpresako datuekin aberastu nahi duzun **Bezeroaren datu multzoa**.</span><span class="sxs-lookup"><span data-stu-id="2aef3-120">Select **Add data** and choose the **Customer data set** you want to enrich with location data from HERE Technologies.</span></span> <span data-ttu-id="2aef3-121">**Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="2aef3-121">You can select the **Customer** entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

    :::image type="content" source="media/enrichment-HERE-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. <span data-ttu-id="2aef3-123">Aukeratu eremuak lehen eta/edo bigarren helbidera esleitu nahi dituzun.</span><span class="sxs-lookup"><span data-stu-id="2aef3-123">Choose if you want to map fields to the primary and/or secondary address.</span></span> <span data-ttu-id="2aef3-124">Bi helbideen eremuen esleipena zehaztu ditzakezu (adibidez, etxeko eta negozioaren helbidea) eta bi helbideen profilak bereiz aberastu.</span><span class="sxs-lookup"><span data-stu-id="2aef3-124">You can specify a field mapping for both addresses (for example, a home and a business address) and enrich the profiles for both addresses separately.</span></span> <span data-ttu-id="2aef3-125">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="2aef3-125">Select **Next**.</span></span>

1. <span data-ttu-id="2aef3-126">Zehaztu zure profil bateratuetako zein eremu erabili beharko liratekeen HERE Technologies-en bat datozen kokapen datuak bilatzeko.</span><span class="sxs-lookup"><span data-stu-id="2aef3-126">Define which fields from your unified profiles should be used to look for matching location data from HERE Technologies.</span></span> <span data-ttu-id="2aef3-127">**1. kalea** eta **Zip / Posta Kodea** eremuak derrigorrezkoak dira hautatutako lehen eta / edo bigarren mailako helbidean.</span><span class="sxs-lookup"><span data-stu-id="2aef3-127">The **Street 1** and **Zip/Postal Code** fields are required for the selected primary and/or secondary address.</span></span> <span data-ttu-id="2aef3-128">Bat-etortze zehatzagoak lortzeko, eremu gehiago gehitu daitezke.</span><span class="sxs-lookup"><span data-stu-id="2aef3-128">For a higher match accuracy, more fields can be added.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="2aef3-129">![HERE Technologies-en aberastearen konfigurazio orria](media/enrichment-HERE-configuration.png "HERE Technologies-en aberastearen konfigurazio orria")</span><span class="sxs-lookup"><span data-stu-id="2aef3-129">![HERE Technologies enrichment configuration page](media/enrichment-HERE-configuration.png "HERE Technologies enrichment configuration page")</span></span>

1. <span data-ttu-id="2aef3-130">Aukeratu **Aplikatu** eremuen esleipena osatzeko.</span><span class="sxs-lookup"><span data-stu-id="2aef3-130">Select **Apply** to complete the field mapping.</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="2aef3-131">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="2aef3-131">Enrichment results</span></span>

<span data-ttu-id="2aef3-132">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="2aef3-132">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="2aef3-133">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="2aef3-133">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="2aef3-134">Prozesatzeko denbora zure bezeroen datuen tamainaren eta HERE Technologies-en APIaren erantzun denboren araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="2aef3-134">The processing time will depend on the size of your customer data and the API response times from HERE Technologies.</span></span>

<span data-ttu-id="2aef3-135">Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**.</span><span class="sxs-lookup"><span data-stu-id="2aef3-135">After the enrichment process completes, you can review the newly enriched customer profiles data under **My enrichments**.</span></span> <span data-ttu-id="2aef3-136">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="2aef3-136">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="2aef3-137">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="2aef3-137">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2aef3-138">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="2aef3-138">Next steps</span></span>

<span data-ttu-id="2aef3-139">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="2aef3-139">Build on top of your enriched customer data.</span></span> <span data-ttu-id="2aef3-140">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="2aef3-140">Create [segments](segments.md), [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="2aef3-141">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="2aef3-141">Data privacy and compliance</span></span>

<span data-ttu-id="2aef3-142">Dynamics 365 Customer Insights gaitzen duzunean datuak HERE Technologies-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="2aef3-142">When you enable Dynamics 365 Customer Insights to transmit data to HERE Technologies, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="2aef3-143">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da HERE Technologies-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="2aef3-143">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that HERE Technologies meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="2aef3-144">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="2aef3-144">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="2aef3-145">Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="2aef3-145">Your Dynamics 365 Customer Insights Administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]