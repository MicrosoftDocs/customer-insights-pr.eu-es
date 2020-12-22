---
title: Aberastea Experian hirugarrenen aberastearekin
description: Experian-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 09/17/2020
ms.reviewer: kishorem
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 60fc49734e54740e83b47a7028be216a0eb81e49
ms.sourcegitcommit: a9b2cf598f256d07a48bba8617347ee90024a1dd
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/03/2020
ms.locfileid: "4668784"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a><span data-ttu-id="525d4-103">Aberastu bezeroen profilak demografiarekin Experian-etik (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="525d4-103">Enrich customer profiles with demographics from Experian (preview)</span></span>

<span data-ttu-id="525d4-104">Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta marketin zerbitzuetan.</span><span class="sxs-lookup"><span data-stu-id="525d4-104">Experian is a global leader in consumer and business credit reporting and marketing services.</span></span> <span data-ttu-id="525d4-105">Batera Experianen datuak aberasteko zerbitzuak, zure bezeroen ulermen sakona sor dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.</span><span class="sxs-lookup"><span data-stu-id="525d4-105">With Experian’s data enrichment services, you can build a deeper understanding of your customers by enriching your customer profiles with demographic data such as household size, income, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="525d4-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="525d4-106">Prerequisites</span></span>

<span data-ttu-id="525d4-107">Experian konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="525d4-107">To configure Experian, the following prerequisites must be met:</span></span>

- <span data-ttu-id="525d4-108">Experian harpidetza aktiboa duzu.</span><span class="sxs-lookup"><span data-stu-id="525d4-108">You have an active Experian subscription.</span></span> <span data-ttu-id="525d4-109">Harpidetza lortzeko, [jarri harremanetan Experian-ekin](https://www.experian.com/marketing-services/contact) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="525d4-109">To get a subscription, [contact Experian](https://www.experian.com/marketing-services/contact) directly.</span></span> <span data-ttu-id="525d4-110">[Ikasi gehiago Experian datu-aberasteari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span><span class="sxs-lookup"><span data-stu-id="525d4-110">[Learn more about Experian Data Enrichment](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span></span>
- <span data-ttu-id="525d4-111">Experian-ek sortu duen SSH gaitutako Garraio Seguru (ST) konturako Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia dituzu.</span><span class="sxs-lookup"><span data-stu-id="525d4-111">You have the User ID, Party ID, and Model Number for your SSH-enabled Secure Transport (ST) account that Experian created for you.</span></span>
- <span data-ttu-id="525d4-112">Badituzu [Administratzaile](permissions.md#administrator) baimenak hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="525d4-112">You have [Administrator](permissions.md#administrator) permissions in audience insights.</span></span>

## <a name="configuration"></a><span data-ttu-id="525d4-113">Konfigurazioa</span><span class="sxs-lookup"><span data-stu-id="525d4-113">Configuration</span></span>

1. <span data-ttu-id="525d4-114">Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="525d4-114">Go to **Data** > **Enrichment** and select the **Discover** tab.</span></span>

1. <span data-ttu-id="525d4-115">Aukeratu **Aberastu nire datuak** Experian fitxan.</span><span class="sxs-lookup"><span data-stu-id="525d4-115">Select **Enrich my data** on the Experian tile.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="525d4-116">![Teila Experian](media/experian-tile.png "Teila Experian")</span><span class="sxs-lookup"><span data-stu-id="525d4-116">![Experian tile](media/experian-tile.png "Experian tile")</span></span>

1. <span data-ttu-id="525d4-117">Aukeratu **Hasi** eta sartu Erabiltzailearen IDa, Alderdiaren IDa eta Modelo zenbakia Experian Secure Transport konturako.</span><span class="sxs-lookup"><span data-stu-id="525d4-117">Select **Get started** and enter the User ID, Party ID, and Model Number for your Experian Secure Transport account.</span></span> <span data-ttu-id="525d4-118">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="525d4-118">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span> <span data-ttu-id="525d4-119">Berretsi sarrera guztiak hautatuta **Aplikatu**.</span><span class="sxs-lookup"><span data-stu-id="525d4-119">Confirm all inputs by selecting **Apply**.</span></span>

## <a name="map-your-fields"></a><span data-ttu-id="525d4-120">Esleitu eremuak</span><span class="sxs-lookup"><span data-stu-id="525d4-120">Map your fields</span></span>

1. <span data-ttu-id="525d4-121">Aukeratu **Gehitu datuak** eta aukeratu zure gako identifikatzaileak **Izena eta helbidea**, **Posta elektronikoa**, edo **Mugikorra** nortasun ebazpena Experianera bidaltzeko.</span><span class="sxs-lookup"><span data-stu-id="525d4-121">Select **Add data** and choose your key identifiers from **Name and Address**, **E-mail**, or **Phone** to send to Experian for identity resolution.</span></span>

   > [!TIP]
   > <span data-ttu-id="525d4-122">Litekeena da Experian-era bidalitako gako identifikatzaile atributu gehiagok bat etortze tasa handiagoa lortzea.</span><span class="sxs-lookup"><span data-stu-id="525d4-122">More key identifier attributes sent to Experian likely yield a higher match rate.</span></span>

1. <span data-ttu-id="525d4-123">Aukeratu **Hurrengoa** eta mapatu dagozkien atributuak zure bezero entitate bateratuarekin hautatutako gako identifikatzailearen eremuetarako.</span><span class="sxs-lookup"><span data-stu-id="525d4-123">Select **Next** and map the corresponding attributes from your unified customer entity for the selected key identifier fields.</span></span>

1. <span data-ttu-id="525d4-124">Aukeratu **Gehitu atributua** Experian-era bidali nahi dituzun atributu osagarriak mapatzeko.</span><span class="sxs-lookup"><span data-stu-id="525d4-124">Select **Add attribute** to map any additional attributes you would like to send to Experian.</span></span>

1.  <span data-ttu-id="525d4-125">Aukeratu **Gorde** eremuaren mapa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="525d4-125">Select **Save** to complete the field mapping.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="525d4-126">![Experian eremuaren esleipena](media/experian-field-mapping.png "Experian eremuaren esleipena")</span><span class="sxs-lookup"><span data-stu-id="525d4-126">![Experian field mapping](media/experian-field-mapping.png "Experian field mapping")</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="525d4-127">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="525d4-127">Enrichment results</span></span>

<span data-ttu-id="525d4-128">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="525d4-128">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="525d4-129">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="525d4-129">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="525d4-130">Prozesatzeko denbora zure bezeroen datuen tamainaren eta Experian-ek zure konturako aberastutako prozesuen araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="525d4-130">The processing time will depend on the size of your customer data and the enrichment processes set up for your account by Experian.</span></span>

<span data-ttu-id="525d4-131">Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**.</span><span class="sxs-lookup"><span data-stu-id="525d4-131">After the enrichment process completes, you can review the newly enriched customer profiles data under **My enrichments**.</span></span> <span data-ttu-id="525d4-132">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="525d4-132">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="525d4-133">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="525d4-133">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="525d4-134">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="525d4-134">Next steps</span></span>

<span data-ttu-id="525d4-135">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="525d4-135">Build on top of your enriched customer data.</span></span> <span data-ttu-id="525d4-136">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="525d4-136">Create [segments](segments.md), [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="525d4-137">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="525d4-137">Data privacy and compliance</span></span>

<span data-ttu-id="525d4-138">Dynamics 365 Customer Insights gaitzen duzunean datuak Experian-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="525d4-138">When you enable Dynamics 365 Customer Insights to transmit data to Experian, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="525d4-139">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Experian-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="525d4-139">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Experian meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="525d4-140">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="525d4-140">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="525d4-141">Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="525d4-141">Your Dynamics 365 Customer Insights Administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>
