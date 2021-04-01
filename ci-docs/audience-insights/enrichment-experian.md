---
title: Aberastea Experian hirugarrenen aberastearekin
description: Experian-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 12/10/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 4d4723e8f793ee857c4f5204a42be8338c71d4c3
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597772"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a><span data-ttu-id="27457-103">Aberastu bezeroen profilak demografiarekin Experian-etik (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="27457-103">Enrich customer profiles with demographics from Experian (preview)</span></span>

<span data-ttu-id="27457-104">Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta marketin zerbitzuetan.</span><span class="sxs-lookup"><span data-stu-id="27457-104">Experian is a global leader in consumer and business credit reporting and marketing services.</span></span> <span data-ttu-id="27457-105">Batera Experianen datuak aberasteko zerbitzuak, zure bezeroen ulermen sakona sor dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.</span><span class="sxs-lookup"><span data-stu-id="27457-105">With Experian’s data enrichment services, you can build a deeper understanding of your customers by enriching your customer profiles with demographic data such as household size, income, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="27457-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="27457-106">Prerequisites</span></span>

<span data-ttu-id="27457-107">Experian konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="27457-107">To configure Experian, the following prerequisites must be met:</span></span>

- <span data-ttu-id="27457-108">Experian harpidetza aktiboa duzu.</span><span class="sxs-lookup"><span data-stu-id="27457-108">You have an active Experian subscription.</span></span> <span data-ttu-id="27457-109">Harpidetza lortzeko, [jarri harremanetan Experian-ekin](https://www.experian.com/marketing-services/contact) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="27457-109">To get a subscription, [contact Experian](https://www.experian.com/marketing-services/contact) directly.</span></span> <span data-ttu-id="27457-110">[Ikasi gehiago Experian datu-aberasteari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span><span class="sxs-lookup"><span data-stu-id="27457-110">[Learn more about Experian Data Enrichment](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span></span>
- <span data-ttu-id="27457-111">Experian-ek sortu duen SSH gaitutako Garraio Seguru (ST) konturako Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia dituzu.</span><span class="sxs-lookup"><span data-stu-id="27457-111">You have the User ID, Party ID, and Model Number for your SSH-enabled Secure Transport (ST) account that Experian created for you.</span></span>
- <span data-ttu-id="27457-112">Badituzu [Administratzaile](permissions.md#administrator) baimenak hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="27457-112">You have [Administrator](permissions.md#administrator) permissions in audience insights.</span></span>

## <a name="configuration"></a><span data-ttu-id="27457-113">Konfigurazioa</span><span class="sxs-lookup"><span data-stu-id="27457-113">Configuration</span></span>

1. <span data-ttu-id="27457-114">Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="27457-114">Go to **Data** > **Enrichment** and select the **Discover** tab.</span></span>

1. <span data-ttu-id="27457-115">Aukeratu **Aberastu nire datuak** Experian fitxan.</span><span class="sxs-lookup"><span data-stu-id="27457-115">Select **Enrich my data** on the Experian tile.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="27457-116">![Teila Experian](media/experian-tile.png "Teila Experian")</span><span class="sxs-lookup"><span data-stu-id="27457-116">![Experian tile](media/experian-tile.png "Experian tile")</span></span>

1. <span data-ttu-id="27457-117">Aukeratu **Hasi** eta sartu Erabiltzailearen IDa, Alderdiaren IDa eta Modelo zenbakia Experian Secure Transport konturako.</span><span class="sxs-lookup"><span data-stu-id="27457-117">Select **Get started** and enter the User ID, Party ID, and Model Number for your Experian Secure Transport account.</span></span> <span data-ttu-id="27457-118">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="27457-118">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span> <span data-ttu-id="27457-119">Berretsi sarrera guztiak hautatuta **Aplikatu**.</span><span class="sxs-lookup"><span data-stu-id="27457-119">Confirm all inputs by selecting **Apply**.</span></span>

## <a name="map-your-fields"></a><span data-ttu-id="27457-120">Esleitu eremuak</span><span class="sxs-lookup"><span data-stu-id="27457-120">Map your fields</span></span>

1.  <span data-ttu-id="27457-121">Aukeratu **Gehitu datuak** eta aukeratu Experian-eko enpresako datu demografikoekin aberastu nahi duzun **Bezeroaren datu multzoa**.</span><span class="sxs-lookup"><span data-stu-id="27457-121">Select **Add data** and choose the **Customer data set** you want to enrich with demographics data from Experian.</span></span> <span data-ttu-id="27457-122">**Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="27457-122">You can select the **Customer** entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

1. <span data-ttu-id="27457-123">Aukeratu zure gako identifikatzaileak **Izena eta helbidea**, **Helbide elektronikoa**, edo **Mugikorra** identitate-ebazpena Experian-era bidaltzeko.</span><span class="sxs-lookup"><span data-stu-id="27457-123">Select your key identifiers from **Name and Address**, **E-mail**, or **Phone** to send to Experian for identity resolution.</span></span>

   > [!TIP]
   > <span data-ttu-id="27457-124">Litekeena da Experian-era bidalitako gako identifikatzaile atributu gehiagok bat etortze tasa handiagoa lortzea.</span><span class="sxs-lookup"><span data-stu-id="27457-124">More key identifier attributes sent to Experian likely yield a higher match rate.</span></span>

1. <span data-ttu-id="27457-125">Aukeratu **Hurrengoa** eta mapatu dagozkien atributuak zure bezero entitate bateratuarekin hautatutako gako identifikatzailearen eremuetarako.</span><span class="sxs-lookup"><span data-stu-id="27457-125">Select **Next** and map the corresponding attributes from your unified customer entity for the selected key identifier fields.</span></span>

1. <span data-ttu-id="27457-126">Aukeratu **Gehitu atributua** Experian-era bidali nahi dituzun atributu osagarriak mapatzeko.</span><span class="sxs-lookup"><span data-stu-id="27457-126">Select **Add attribute** to map any additional attributes you would like to send to Experian.</span></span>

1.  <span data-ttu-id="27457-127">Aukeratu **Gorde** eremuaren mapa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="27457-127">Select **Save** to complete the field mapping.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="27457-128">![Experian eremuaren esleipena](media/experian-field-mapping.png "Experian eremuaren esleipena")</span><span class="sxs-lookup"><span data-stu-id="27457-128">![Experian field mapping](media/experian-field-mapping.png "Experian field mapping")</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="27457-129">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="27457-129">Enrichment results</span></span>

<span data-ttu-id="27457-130">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="27457-130">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="27457-131">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="27457-131">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="27457-132">Prozesatzeko denbora zure bezeroen datuen tamainaren eta Experian-ek zure konturako aberastutako prozesuen araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="27457-132">The processing time will depend on the size of your customer data and the enrichment processes set up for your account by Experian.</span></span>

<span data-ttu-id="27457-133">Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**.</span><span class="sxs-lookup"><span data-stu-id="27457-133">After the enrichment process completes, you can review the newly enriched customer profiles data under **My enrichments**.</span></span> <span data-ttu-id="27457-134">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="27457-134">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="27457-135">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="27457-135">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="27457-136">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="27457-136">Next steps</span></span>

<span data-ttu-id="27457-137">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="27457-137">Build on top of your enriched customer data.</span></span> <span data-ttu-id="27457-138">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="27457-138">Create [segments](segments.md), [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="27457-139">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="27457-139">Data privacy and compliance</span></span>

<span data-ttu-id="27457-140">Dynamics 365 Customer Insights gaitzen duzunean datuak Experian-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="27457-140">When you enable Dynamics 365 Customer Insights to transmit data to Experian, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="27457-141">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Experian-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="27457-141">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Experian meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="27457-142">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="27457-142">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="27457-143">Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="27457-143">Your Dynamics 365 Customer Insights Administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]