---
title: Esportatu Customer Insights datuak AdRoll-era
description: Ikasi konexioa nola konfiguratu eta AdRoll-era esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 67bfa23d56b26ae592efa4d7197713664bb02623
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304783"
---
# <a name="export-segments-to-adroll-preview"></a><span data-ttu-id="18d38-103">Esportatu segmentuak AdRoll-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="18d38-103">Export segments to AdRoll (preview)</span></span>

<span data-ttu-id="18d38-104">Esportatu bezeroen profil bateratuen segmentuak AdRoll-era eta erabili iragarkietarako.</span><span class="sxs-lookup"><span data-stu-id="18d38-104">Export segments of unified customer profiles to AdRoll and use them for advertising.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="18d38-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="18d38-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="18d38-106">Baduzu [AdRoll kontua](https://www.adroll.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="18d38-106">You have an [AdRoll account](https://www.adroll.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="18d38-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="18d38-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="18d38-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="18d38-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="18d38-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="18d38-109">Known limitations</span></span>

- <span data-ttu-id="18d38-110">Aldiko 250.000 profil esporta ditzakezu gehienez AdRoll batean.</span><span class="sxs-lookup"><span data-stu-id="18d38-110">You can export up to 250,000 profiles at a time to AdRoll.</span></span>
- <span data-ttu-id="18d38-111">Ezin dituzu esportatu 100 profil baino gutxiagoko segmentuak AdRoll-era.</span><span class="sxs-lookup"><span data-stu-id="18d38-111">You can't export segments with fewer than 100 profiles to AdRoll.</span></span> 
- <span data-ttu-id="18d38-112">AdRoll-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="18d38-112">Exporting to AdRoll is limited to segments.</span></span>
- <span data-ttu-id="18d38-113">250.000 profila AdRoll-era esportatzeko 10 minutu behar izan ditzakezu osatzeko.</span><span class="sxs-lookup"><span data-stu-id="18d38-113">Exporting up to 250,000 profiles to AdRoll can take up to 10 minutes to complete.</span></span> 
- <span data-ttu-id="18d38-114">AdRoll-era esporta ditzakezun profilen kopurua AdRoll-ekin duzun kontratuaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="18d38-114">The number of profiles that you can export to AdRoll is dependent on your contract with AdRoll.</span></span>

## <a name="set-up-connection-to-adroll"></a><span data-ttu-id="18d38-115">Konfiguratu konexioa AdRoll-ra</span><span class="sxs-lookup"><span data-stu-id="18d38-115">Set up connection to AdRoll</span></span>

1. <span data-ttu-id="18d38-116">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="18d38-116">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="18d38-117">Hautatu **Gehitu konexioa** eta aukeratu **AdRoll** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="18d38-117">Select **Add connection** and choose **AdRoll** to configure the connection.</span></span>

1. <span data-ttu-id="18d38-118">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="18d38-118">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="18d38-119">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="18d38-119">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="18d38-120">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="18d38-120">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="18d38-121">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="18d38-121">Choose who can use this connection.</span></span> <span data-ttu-id="18d38-122">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="18d38-122">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="18d38-123">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="18d38-123">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="18d38-124">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="18d38-124">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="18d38-125">Aukeratu **Konektatu** AdRoll-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="18d38-125">Select **Connect** to initialize the connection to AdRoll.</span></span>

1. <span data-ttu-id="18d38-126">Aukeratu **Egiaztatu AdRoll-ekin** eta eman zure administraziorako AdRoll kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="18d38-126">Select **Authenticate with AdRoll** and provide your admin credentials for AdRoll.</span></span> 

1. <span data-ttu-id="18d38-127">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="18d38-127">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="18d38-128">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="18d38-128">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="18d38-129">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="18d38-129">Configure an export</span></span>

<span data-ttu-id="18d38-130">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="18d38-130">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="18d38-131">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="18d38-131">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="18d38-132">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="18d38-132">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="18d38-133">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="18d38-133">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="18d38-134">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa AdRoll sekzioan.</span><span class="sxs-lookup"><span data-stu-id="18d38-134">In the **Connection for export** field, choose a connection from the AdRoll section.</span></span> <span data-ttu-id="18d38-135">Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.</span><span class="sxs-lookup"><span data-stu-id="18d38-135">If you don't see this section name, then no connections of this type are available to you.</span></span>

1. <span data-ttu-id="18d38-136">Sartu zure **AdRoll iragarlearen IDa**.</span><span class="sxs-lookup"><span data-stu-id="18d38-136">Enter your **AdRoll Advertiser ID**.</span></span> <span data-ttu-id="18d38-137">Informazio gehiagorako, ikus [AdRoll iragarkien profilak](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).</span><span class="sxs-lookup"><span data-stu-id="18d38-137">For more information, see [AdRoll Advertiser Profiles](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).</span></span>

3. <span data-ttu-id="18d38-138">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="18d38-138">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="18d38-139">Segmentuak AdRoll-era esportatu behar dira.</span><span class="sxs-lookup"><span data-stu-id="18d38-139">It's required to export segments to AdRoll.</span></span>

1. <span data-ttu-id="18d38-140">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="18d38-140">Select the segments you want to export.</span></span> <span data-ttu-id="18d38-141">Aukeratu gutxienez 100 kide dituen segmentua.</span><span class="sxs-lookup"><span data-stu-id="18d38-141">Select a segment with a least 100 members.</span></span> <span data-ttu-id="18d38-142">Ezin dituzu segmentu txikiagoak esportatu.</span><span class="sxs-lookup"><span data-stu-id="18d38-142">You can't export smaller segments.</span></span> <span data-ttu-id="18d38-143">Gainera, esportatzeko segmentu baten gehieneko tamaina 250.000 kide da esportazio bakoitzeko.</span><span class="sxs-lookup"><span data-stu-id="18d38-143">Additionally the maximum size of a segment to export is 250,000 members per export.</span></span> 

1. <span data-ttu-id="18d38-144">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="18d38-144">Select **Save**.</span></span>

<span data-ttu-id="18d38-145">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="18d38-145">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="18d38-146">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="18d38-146">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> 

<span data-ttu-id="18d38-147">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="18d38-147">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="18d38-148">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="18d38-148">Data privacy and compliance</span></span>

<span data-ttu-id="18d38-149">Dynamics 365 Customer Insights gaitzen duzunean datuak AdRoll-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="18d38-149">When you enable Dynamics 365 Customer Insights to transmit data to AdRoll, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="18d38-150">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da AdRoll-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="18d38-150">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that AdRoll meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="18d38-151">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="18d38-151">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="18d38-152">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="18d38-152">Your Dynamics 365 Customer Insights administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
