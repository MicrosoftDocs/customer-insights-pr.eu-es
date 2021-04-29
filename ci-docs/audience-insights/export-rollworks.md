---
title: Esportatu Customer Insights datuak RollWorks-era
description: Ikasi konexioa konfiguratzen eta esportatzen RollWorks.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 4979f0147dea2270f11342c1bb6b0693f3c24aea
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760463"
---
# <a name="export-segment-lists-to-rollworks-preview"></a><span data-ttu-id="6c6c1-103">Esportatu segmentuen zerrendak RollWorks (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="6c6c1-103">Export segment lists to RollWorks (preview)</span></span>

<span data-ttu-id="6c6c1-104">Esportatu bezeroen profil bateratuen segmentuak RollWorks eta erabili iragarkietarako.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-104">Export segments of unified customer profiles to RollWorks and use them for advertising.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="6c6c1-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="6c6c1-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="6c6c1-106">Baduzu [RollWorks kontua](https://www.rollworks.com/) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-106">You have an [RollWorks account](https://www.rollworks.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="6c6c1-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="6c6c1-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="6c6c1-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="6c6c1-109">Known limitations</span></span>

- <span data-ttu-id="6c6c1-110">Esportazio bakoitzeko 250.000 profil esportatu ditzakezu RollWorks-era.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-110">You can export up to 250'000 profiles in per export to RollWorks.</span></span>
- <span data-ttu-id="6c6c1-111">Ezin dituzu 100 profil baino gutxiagoko segmentuak esportatu RollWorks-era.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-111">You can't export segments with fewer than 100 profiles to RollWorks.</span></span> 
- <span data-ttu-id="6c6c1-112">RollWorks esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-112">Exporting to RollWorks is limited to segments.</span></span>
- <span data-ttu-id="6c6c1-113">Esportatu gehienez 250.000 profil RollWorks, 10 minutu behar ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-113">Exporting up to 250'000 profiles to RollWorks can take up to 10 minutes to complete.</span></span> 
- <span data-ttu-id="6c6c1-114">RollWorks-era esporta ditzakezun profilen kopurua RollWorks-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-114">The number of profiles that you can export to RollWorks is dependent and limited on your contract with RollWorks.</span></span>

## <a name="set-up-connection-to-rollworks"></a><span data-ttu-id="6c6c1-115">Konfiguratu konexioa RollWorks-era</span><span class="sxs-lookup"><span data-stu-id="6c6c1-115">Set up connection to RollWorks</span></span>

1. <span data-ttu-id="6c6c1-116">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-116">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="6c6c1-117">Hautatu **Gehitu konexioa** eta aukeratu **RollWorks** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-117">Select **Add connection** and choose **RollWorks** to configure the connection.</span></span>

1. <span data-ttu-id="6c6c1-118">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-118">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="6c6c1-119">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-119">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="6c6c1-120">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-120">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="6c6c1-121">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-121">Choose who can use this connection.</span></span> <span data-ttu-id="6c6c1-122">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-122">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="6c6c1-123">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="6c6c1-123">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="6c6c1-124">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-124">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="6c6c1-125">Aukeratu **Konektatu** RollWorks konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-125">Select **Connect** to initialize the connection to RollWorks.</span></span>

1. <span data-ttu-id="6c6c1-126">Aukeratu **Autenticatu RollWorks-ekin** eta eman zure administratzaile egiaztagiriak RollWorks-erako.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-126">Select **Authenticate with RollWorks** and provide your admin credentials for RollWorks.</span></span>

1. <span data-ttu-id="6c6c1-127">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-127">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="6c6c1-128">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-128">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="6c6c1-129">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="6c6c1-129">Configure an export</span></span>

<span data-ttu-id="6c6c1-130">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-130">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="6c6c1-131">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="6c6c1-131">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="6c6c1-132">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-132">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="6c6c1-133">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-133">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="6c6c1-134">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa RollWorks sekzioan.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-134">In the **Connection for export** field, choose a connection from the RollWorks section.</span></span> <span data-ttu-id="6c6c1-135">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-135">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="6c6c1-136">Sartu zure **RollWorks iragarlearen IDa** [RollWorks Iragarkia](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).</span><span class="sxs-lookup"><span data-stu-id="6c6c1-136">Enter your **RollWorks Advertiser ID** [RollWorks Advertisable](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).</span></span>

3. <span data-ttu-id="6c6c1-137">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-137">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="6c6c1-138">Segmentuak esportatu behar dira RollWorks.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-138">It's required to export segments to RollWorks.</span></span>

1. <span data-ttu-id="6c6c1-139">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-139">Select the segments you want to export.</span></span> <span data-ttu-id="6c6c1-140">Aukeratu gutxienez 100 kide dituen segmentua.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-140">Select a segment with a least 100 members.</span></span> <span data-ttu-id="6c6c1-141">Ezin dituzu segmentu txikiagoak esportatu.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-141">You can't export smaller segments.</span></span> <span data-ttu-id="6c6c1-142">Gainera, esportatzeko segmentu baten gehieneko tamaina 250.000 kide da esportazio bakoitzeko.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-142">Additionally the maximum size of a segment to export is 250'000 members per export.</span></span> 

1. <span data-ttu-id="6c6c1-143">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-143">Select **Save**.</span></span>

<span data-ttu-id="6c6c1-144">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-144">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="6c6c1-145">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="6c6c1-145">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="6c6c1-146">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="6c6c1-146">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="6c6c1-147">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="6c6c1-147">Data privacy and compliance</span></span>

<span data-ttu-id="6c6c1-148">Gaitzen duzunean Dynamics 365 Customer Insights datuak RollWorks-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-148">When you enable Dynamics 365 Customer Insights to transmit data to RollWorks, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="6c6c1-149">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara RollWorks-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-149">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that RollWorks meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="6c6c1-150">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="6c6c1-150">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="6c6c1-151">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="6c6c1-151">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
