---
title: Enpresako profilak aberastea hirugarrenen Leadspace aberastearekin
description: Leadspace-ren hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 11/24/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-MS
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 41c56aece043c2d7658fd2655713e1e98775edec
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597634"
---
# <a name="enrichment-of-company-profiles-with-leadspace-preview"></a><span data-ttu-id="c7bb6-103">Enpresen profilak aberastea Leadspace-rekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="c7bb6-103">Enrichment of company profiles with Leadspace (preview)</span></span>

<span data-ttu-id="c7bb6-104">Leadspace B2B Bezeroaren Datuen Plataforma eskaintzen duen datuen zientzia enpresa da.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-104">Leadspace is a data science company that provides a B2B Customer Data Platform.</span></span> <span data-ttu-id="c7bb6-105">Enpresentzako bezeroen profil bateratuak dituzten bezeroei beren datuak aberasteko aukera ematen die.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-105">It enables customers with unified customer profiles for companies to enrich their data.</span></span> <span data-ttu-id="c7bb6-106">Aberasteek atributu osagarriak barne hartzen dituzte esaterako, enpresaren tamaina, kokalekua, sektorea, etab.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-106">Enrichments include additional attributes such as company size, location, industry, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7bb6-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="c7bb6-107">Prerequisites</span></span>

<span data-ttu-id="c7bb6-108">Leadspace konfiguratzeko eta konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="c7bb6-108">To configure Leadspace, the following prerequisites must be met:</span></span>

- <span data-ttu-id="c7bb6-109">Leadspace lizentzia aktiboa duzu eta "betiko gakoa" (**Leadspace-ko token** deitzen zaio).</span><span class="sxs-lookup"><span data-stu-id="c7bb6-109">You have an active Leadspace license and the “perpetual key” (referred to as **Leadspace token**).</span></span> <span data-ttu-id="c7bb6-110">Jar zaitez harremanetan zuzenean [Leadspace](https://www.leadspace.com/products/leadspace-on-demand/) beren produktuari buruzko xehetasunak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-110">Contact directly [Leadspace](https://www.leadspace.com/products/leadspace-on-demand/) for details about their product.</span></span>
- <span data-ttu-id="c7bb6-111">[Administratzaile](permissions.md#administrator) baimenak dituzu.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-111">You have [Administrator](permissions.md#administrator) permissions.</span></span>
- <span data-ttu-id="c7bb6-112">Duzu [bezeroen profil bateratuak](customer-profiles.md) enpresentzat.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-112">You have [unified customer profiles](customer-profiles.md) for companies.</span></span>

## <a name="configuration"></a><span data-ttu-id="c7bb6-113">Konfigurazioa</span><span class="sxs-lookup"><span data-stu-id="c7bb6-113">Configuration</span></span>

1. <span data-ttu-id="c7bb6-114">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Aberastea**.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-114">In audience insights, go to **Data** > **Enrichment**.</span></span>

1. <span data-ttu-id="c7bb6-115">Aukeratu **Aberastu nire datuak** Leadspace fitxan.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-115">Select **Enrich my data** on the Leadspace tile.</span></span>

   :::image type="content" source="media/leadspace-tile.png" alt-text="Leadspace lauzaren pantaila-argazkia.":::

1. <span data-ttu-id="c7bb6-117">Aukeratu **Hasi** eta, ondoren, sartu **Leadspace token** aktibo bat (betiko giltza).</span><span class="sxs-lookup"><span data-stu-id="c7bb6-117">Select **Get Started** and then enter an active **Leadspace token** (perpetual key).</span></span> <span data-ttu-id="c7bb6-118">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-118">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span> <span data-ttu-id="c7bb6-119">Berretsi bi sarrerak **Konektatu Leadspace-ra** hautatuta.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-119">Confirm both inputs by selecting **Connect to Leadspace**.</span></span>

1. <span data-ttu-id="c7bb6-120">Aukeratu **Esleitu datuak** eta aukeratu Microsoft Leadspace-ko enpresako datuekin aberastu nahi duzun datu multzoa.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-120">Select **Map data** and choose the data set you want to enrich with company data from Leadspace.</span></span> <span data-ttu-id="c7bb6-121">*Bezeroen* entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-121">You can select the *Customer* entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

   :::image type="content" source="media/enrichment-leadspace-select-segment.png" alt-text="Aukeratu bezeroaren profila eta segmentua aberasteko.":::

1. <span data-ttu-id="c7bb6-123">Sakatu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu erabili beharko liratekeen Leadspace enpresako datuekin bat etortzeko.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-123">Click **Next** and define which fields from your unified profiles should be used to look for matching company data from Leadspace.</span></span> <span data-ttu-id="c7bb6-124">**Enpresaren izena** eremua beharrezkoa da.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-124">The **Name of company** field is required.</span></span> <span data-ttu-id="c7bb6-125">Bat-etortzeen zehaztasun handiagoa lortzeko, beste bi eremu, **Enpresaren webgunea** eta **Enpresaren kokapena**, gehitu daitezke.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-125">For a higher match accuracy, up to two other fields, **Company website** and **Company location**, can be added.</span></span>

   :::image type="content" source="media/enrichment-leadspace-mapping.png" alt-text="Leadspace eremuak esleitzeko panela.":::
   
1. <span data-ttu-id="c7bb6-127">Aukeratu **Aplikatu** eremuen esleipena osatzeko.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-127">Select **Apply** to complete the field mapping.</span></span>

1. <span data-ttu-id="c7bb6-128">Aukeratu **Exekutatu** enpresaren profilak aberasteko.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-128">Select **Run** to enrich the company profiles.</span></span> <span data-ttu-id="c7bb6-129">Aberasteak behar duen denbora bateratutako bezeroen profil kopuruaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-129">How long an enrichment takes depends on the number of unified customer profiles.</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="c7bb6-130">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="c7bb6-130">Enrichment results</span></span>

<span data-ttu-id="c7bb6-131">Aberastea freskatu ondoren, azpian dagoen enpresa aberastutako datuak berrikus ditzakezu [Nire aberastasunak](enrichment-hub.md).</span><span class="sxs-lookup"><span data-stu-id="c7bb6-131">After refreshing the enrichment, you can review the newly enriched company data under [My enrichments](enrichment-hub.md).</span></span> <span data-ttu-id="c7bb6-132">Azken eguneraketaren ordua eta aberastutako profil kopurua aurki ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-132">You can find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="c7bb6-133">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-133">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

<span data-ttu-id="c7bb6-134">Informazio gehiago lortzeko, ikus [Leadspace API](https://support.leadspace.com/hc/en-us/sections/201997649-API).</span><span class="sxs-lookup"><span data-stu-id="c7bb6-134">For more information, see [Leadspace APIs](https://support.leadspace.com/hc/en-us/sections/201997649-API).</span></span>

## <a name="next-steps"></a><span data-ttu-id="c7bb6-135">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="c7bb6-135">Next steps</span></span>

<span data-ttu-id="c7bb6-136">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-136">Build on top of your enriched customer data.</span></span> <span data-ttu-id="c7bb6-137">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-137">Create [segments](segments.md), [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="c7bb6-138">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="c7bb6-138">Data privacy and compliance</span></span>

<span data-ttu-id="c7bb6-139">Dynamics 365 Customer Insights gaitzen duzunean datuak Leadspace-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-139">When you enable Dynamics 365 Customer Insights to transmit data to Leadspace, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="c7bb6-140">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Leadspace-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-140">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Leadspace meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="c7bb6-141">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="c7bb6-141">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="c7bb6-142">Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="c7bb6-142">Your Dynamics 365 Customer Insights Administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]