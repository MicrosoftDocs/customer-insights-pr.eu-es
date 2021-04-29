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
ms.openlocfilehash: e8f4d4ee6b2c6cdec513b700641db568fa16076d
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5895944"
---
# <a name="export-segment-lists-to-adroll-preview"></a><span data-ttu-id="67269-103">Esportatu segmentuen zerrendak AdRoll (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="67269-103">Export segment lists to AdRoll (preview)</span></span>

<span data-ttu-id="67269-104">Esportatu bezeroen profil bateratuen segmentuak AdRoll-era eta erabili iragarkietarako.</span><span class="sxs-lookup"><span data-stu-id="67269-104">Export segments of unified customer profiles to AdRoll and use them for advertising.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="67269-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="67269-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="67269-106">Baduzu [AdRoll kontua](https://www.adroll.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="67269-106">You have an [AdRoll account](https://www.adroll.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="67269-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="67269-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="67269-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="67269-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="67269-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="67269-109">Known limitations</span></span>

- <span data-ttu-id="67269-110">Guztira 250.000 bezero-profil esporta ditzakezu AdRoll-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="67269-110">You can export up to 250'000 profiles in per export to AdRoll.</span></span>
- <span data-ttu-id="67269-111">Ezin dituzu esportatu 100 profil baino gutxiagoko segmentuak AdRoll-era.</span><span class="sxs-lookup"><span data-stu-id="67269-111">You can't export segments with fewer than 100 profiles to AdRoll.</span></span> 
- <span data-ttu-id="67269-112">AdRoll-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="67269-112">Exporting to AdRoll is limited to segments.</span></span>
- <span data-ttu-id="67269-113">250.000 profila AdRoll-era esportatzeko 10 minutu behar izan ditzakezu osatzeko.</span><span class="sxs-lookup"><span data-stu-id="67269-113">Exporting up to 250'000 profiles to AdRoll can take up to 10 minutes to complete.</span></span> 
- <span data-ttu-id="67269-114">AdRoll-era esporta ditzakezun profilen kopurua AdRoll-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="67269-114">The number of profiles that you can export to AdRoll is dependent and limited on your contract with AdRoll.</span></span>

## <a name="set-up-connection-to-adroll"></a><span data-ttu-id="67269-115">Konfiguratu konexioa AdRoll-ra</span><span class="sxs-lookup"><span data-stu-id="67269-115">Set up connection to AdRoll</span></span>

1. <span data-ttu-id="67269-116">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="67269-116">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="67269-117">Hautatu **Gehitu konexioa** eta aukeratu **AdRoll** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="67269-117">Select **Add connection** and choose **AdRoll** to configure the connection.</span></span>

1. <span data-ttu-id="67269-118">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="67269-118">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="67269-119">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="67269-119">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="67269-120">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="67269-120">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="67269-121">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="67269-121">Choose who can use this connection.</span></span> <span data-ttu-id="67269-122">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="67269-122">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="67269-123">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="67269-123">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="67269-124">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="67269-124">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="67269-125">Aukeratu **Konektatu** AdRoll-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="67269-125">Select **Connect** to initialize the connection to AdRoll.</span></span>

1. <span data-ttu-id="67269-126">Aukeratu **Egiaztatu AdRoll-ekin** eta eman zure administraziorako AdRoll kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="67269-126">Select **Authenticate with AdRoll** and provide your admin credentials for AdRoll.</span></span> 

1. <span data-ttu-id="67269-127">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="67269-127">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="67269-128">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="67269-128">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="67269-129">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="67269-129">Configure an export</span></span>

<span data-ttu-id="67269-130">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="67269-130">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="67269-131">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="67269-131">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="67269-132">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="67269-132">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="67269-133">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="67269-133">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="67269-134">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa AdRoll sekzioan.</span><span class="sxs-lookup"><span data-stu-id="67269-134">In the **Connection for export** field, choose a connection from the AdRoll section.</span></span> <span data-ttu-id="67269-135">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="67269-135">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="67269-136">Sartu zure **AdRoll iragarlearen IDa** Informazio gehiagorako, ikus [Iragarkien iragarkien profilak](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).</span><span class="sxs-lookup"><span data-stu-id="67269-136">Enter your **AdRoll Advertiser ID** For more information, see [AdRoll Advertiser Profiles](https://help.adroll.com/hc/articles/212011838-Advertiser-Profiles).</span></span>

3. <span data-ttu-id="67269-137">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="67269-137">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="67269-138">Segmentuak AdRoll-era esportatu behar dira.</span><span class="sxs-lookup"><span data-stu-id="67269-138">It's required to export segments to AdRoll.</span></span>

1. <span data-ttu-id="67269-139">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="67269-139">Select the segments you want to export.</span></span> <span data-ttu-id="67269-140">Aukeratu gutxienez 100 kide dituen segmentua.</span><span class="sxs-lookup"><span data-stu-id="67269-140">Select a segment with a least 100 members.</span></span> <span data-ttu-id="67269-141">Ezin dituzu segmentu txikiagoak esportatu.</span><span class="sxs-lookup"><span data-stu-id="67269-141">You can't export smaller segments.</span></span> <span data-ttu-id="67269-142">Gainera, esportatzeko segmentu baten gehieneko tamaina 250.000 kide da esportazio bakoitzeko.</span><span class="sxs-lookup"><span data-stu-id="67269-142">Additionally the maximum size of a segment to export is 250'000 members per export.</span></span> 

1. <span data-ttu-id="67269-143">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="67269-143">Select **Save**.</span></span>

<span data-ttu-id="67269-144">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="67269-144">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="67269-145">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="67269-145">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="67269-146">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="67269-146">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="67269-147">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="67269-147">Data privacy and compliance</span></span>

<span data-ttu-id="67269-148">Dynamics 365 Customer Insights gaitzen duzunean datuak AdRoll-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="67269-148">When you enable Dynamics 365 Customer Insights to transmit data to AdRoll, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="67269-149">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da AdRoll-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="67269-149">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that AdRoll meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="67269-150">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="67269-150">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="67269-151">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="67269-151">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
