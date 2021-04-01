---
title: Esportatu Customer Insights datuak AdRoll-era
description: Ikasi AdRoll-erako konexioa nola konfiguratu.
ms.date: 02/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 6fedd549c2e7de362f36e3fb23d363200bb92a04
ms.sourcegitcommit: d24e52150fe5a4fab45128e12d6a03637771d9b9
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "5697059"
---
# <a name="connector-for-adroll-preview"></a><span data-ttu-id="dc33e-103">AdRoll-eko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="dc33e-103">Connector for AdRoll (preview)</span></span>

<span data-ttu-id="dc33e-104">Esportatu bezeroen profil bateratuen segmentuak AdRoll-era eta erabili iragarkietarako.</span><span class="sxs-lookup"><span data-stu-id="dc33e-104">Export segments of unified customer profiles to AdRoll and use them for advertising.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="dc33e-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="dc33e-105">Prerequisites</span></span>

-   <span data-ttu-id="dc33e-106">Baduzu [AdRoll kontua](https://www.adroll.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="dc33e-106">You have an [AdRoll account](https://www.adroll.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="dc33e-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="dc33e-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="dc33e-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="dc33e-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="connect-to-adroll"></a><span data-ttu-id="dc33e-109">Konektatu AdRoll-era</span><span class="sxs-lookup"><span data-stu-id="dc33e-109">Connect to AdRoll</span></span>

1. <span data-ttu-id="dc33e-110">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="dc33e-110">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="dc33e-111">**AdRoll** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="dc33e-111">Under **AdRoll**, select **Set up**.</span></span>

1. <span data-ttu-id="dc33e-112">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="dc33e-112">Give your export destination a recognizable name in the **Display name** field.</span></span>

   :::image type="content" source="media/AdRoll_config.PNG" alt-text="AdRoll konexioaren konfigurazio panela.":::

1. <span data-ttu-id="dc33e-114">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="dc33e-114">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="dc33e-115">Aukeratu **Konektatu** AdRoll-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="dc33e-115">Select **Connect** to initialize the connection to AdRoll.</span></span>

1. <span data-ttu-id="dc33e-116">Aukeratu **Egiaztatu AdRoll-ekin** eta eman zure administraziorako AdRoll kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="dc33e-116">Select **Authenticate with AdRoll** and provide your admin credentials for AdRoll.</span></span> 

1. <span data-ttu-id="dc33e-117">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="dc33e-117">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="dc33e-118">Sartu zure **AdRoll iragarlearen IDa** [AdRoll iragarkia](https://help.adroll.com/hc/en-us/articles/212011838-Advertiser-Profiles).</span><span class="sxs-lookup"><span data-stu-id="dc33e-118">Enter your **AdRoll Advertiser ID** [AdRoll Advertisable](https://help.adroll.com/hc/en-us/articles/212011838-Advertiser-Profiles).</span></span>

1. <span data-ttu-id="dc33e-119">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="dc33e-119">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="dc33e-120">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="dc33e-120">Configure the connector</span></span>

1. <span data-ttu-id="dc33e-121">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="dc33e-121">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="dc33e-122">Segmentuak AdRoll-era esportatu behar dira.</span><span class="sxs-lookup"><span data-stu-id="dc33e-122">It's required to export segments to AdRoll.</span></span>

1. <span data-ttu-id="dc33e-123">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="dc33e-123">Select the segments you want to export.</span></span> <span data-ttu-id="dc33e-124">Aukeratu gutxienez 100 kide dituen segmentua.</span><span class="sxs-lookup"><span data-stu-id="dc33e-124">Select a segment with a least 100 members.</span></span> <span data-ttu-id="dc33e-125">Ezin dituzu segmentu txikiagoak esportatu.</span><span class="sxs-lookup"><span data-stu-id="dc33e-125">You can't export smaller segments.</span></span> <span data-ttu-id="dc33e-126">Gainera, esportatzeko segmentu baten gehieneko tamaina 250.000 kide da esportazio bakoitzeko.</span><span class="sxs-lookup"><span data-stu-id="dc33e-126">Additionally the maximum size of a segment to export is 250'000 members per export.</span></span> 

1. <span data-ttu-id="dc33e-127">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="dc33e-127">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="dc33e-128">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="dc33e-128">Export the data</span></span>

<span data-ttu-id="dc33e-129">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="dc33e-129">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="dc33e-130">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="dc33e-130">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="dc33e-131">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="dc33e-131">Known limitations</span></span>

- <span data-ttu-id="dc33e-132">Guztira 250.000 bezero-profil esporta ditzakezu AdRoll-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="dc33e-132">You can export up to 250'000 profiles in per export to AdRoll.</span></span>
- <span data-ttu-id="dc33e-133">Ezin dituzu esportatu 100 profil baino gutxiagoko segmentuak AdRoll-era.</span><span class="sxs-lookup"><span data-stu-id="dc33e-133">You can't export segments with fewer than 100 profiles to AdRoll.</span></span> 
- <span data-ttu-id="dc33e-134">AdRoll-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="dc33e-134">Exporting to AdRoll is limited to segments.</span></span>
- <span data-ttu-id="dc33e-135">250.000 profila AdRoll-era esportatzeko 10 minutu behar izan ditzakezu osatzeko.</span><span class="sxs-lookup"><span data-stu-id="dc33e-135">Exporting up to 250'000 profiles to AdRoll can take up to 10 minutes to complete.</span></span> 
- <span data-ttu-id="dc33e-136">AdRoll-era esporta ditzakezun profilen kopurua AdRoll-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="dc33e-136">The number of profiles that you can export to AdRoll is dependent and limited on your contract with AdRoll.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="dc33e-137">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="dc33e-137">Data privacy and compliance</span></span>

<span data-ttu-id="dc33e-138">Dynamics 365 Customer Insights gaitzen duzunean datuak AdRoll-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="dc33e-138">When you enable Dynamics 365 Customer Insights to transmit data to AdRoll, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="dc33e-139">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da AdRoll-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="dc33e-139">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that AdRoll meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="dc33e-140">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="dc33e-140">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="dc33e-141">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="dc33e-141">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
