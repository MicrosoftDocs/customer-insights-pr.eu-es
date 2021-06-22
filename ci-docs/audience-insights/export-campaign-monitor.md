---
title: Esportatu Customer Insights datuak Campaign Monitor-era
description: Ikasi konexioa konfiguratzen eta esportatzen Campaign Monitor.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 091a3197dc0c19ff78f0419fb4e88868e0f78359
ms.sourcegitcommit: 831765a55775d358447cb7ffa56f2c3b85459084
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6124166"
---
# <a name="export-segments-to-campaign-monitor-preview"></a><span data-ttu-id="39ed6-103">Esportatu segmentuak Campaign Monitor-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="39ed6-103">Export segments to Campaign Monitor (preview)</span></span>

<span data-ttu-id="39ed6-104">Esportatu bezeroen profil bateratuen segmentuak Campaign Monitor-era eta erabili marketin jardueretarako.</span><span class="sxs-lookup"><span data-stu-id="39ed6-104">Export segments of unified customer profiles to Campaign Monitor and use them for marketing activities.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="39ed6-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="39ed6-105">Prerequisites</span></span>

-   <span data-ttu-id="39ed6-106">Baduzu [Campaign Monitor kontua](https://www.campaignmonitor.com/) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="39ed6-106">You have an [Campaign Monitor account](https://www.campaignmonitor.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="39ed6-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="39ed6-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="39ed6-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="39ed6-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="39ed6-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="39ed6-109">Known limitations</span></span>

- <span data-ttu-id="39ed6-110">Esportazio bakoitzeko milioi bat profil esportatu ditzakezu Campaign Monitor.</span><span class="sxs-lookup"><span data-stu-id="39ed6-110">You can export up to 1 million profiles per export to Campaign Monitor.</span></span>
- <span data-ttu-id="39ed6-111">Campaign Monitor-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="39ed6-111">Exporting to Campaign Monitor is limited to segments.</span></span>
- <span data-ttu-id="39ed6-112">Esportatu gehienez 1 milioi profil Campaign Monitor, 20 minutu behar ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="39ed6-112">Exporting up to 1 million profiles to Campaign Monitor can take up to 20 minutes to complete.</span></span> 
- <span data-ttu-id="39ed6-113">Campaign Monitor-era esporta ditzakezun profilen kopurua Campaign Monitor-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="39ed6-113">The number of profiles that you can export to Campaign Monitor is dependent and limited on your contract with Campaign Monitor.</span></span>

## <a name="set-up-connection-to-campaign-monitor"></a><span data-ttu-id="39ed6-114">Konfiguratu konexioa Campaign Monitor</span><span class="sxs-lookup"><span data-stu-id="39ed6-114">Set up connection to Campaign Monitor</span></span>

1. <span data-ttu-id="39ed6-115">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="39ed6-115">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="39ed6-116">Hautatu **Gehitu konexioa** eta aukeratu **Campaign Monitor** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="39ed6-116">Select **Add connection** and choose **Campaign Monitor** to configure the connection.</span></span>

1. <span data-ttu-id="39ed6-117">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="39ed6-117">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="39ed6-118">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="39ed6-118">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="39ed6-119">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="39ed6-119">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="39ed6-120">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="39ed6-120">Choose who can use this connection.</span></span> <span data-ttu-id="39ed6-121">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="39ed6-121">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="39ed6-122">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="39ed6-122">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="39ed6-123">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="39ed6-123">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="39ed6-124">Aukeratu **Konektatu** Campaign Monitor konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="39ed6-124">Select **Connect** to initialize the connection to Campaign Monitor.</span></span>

1. <span data-ttu-id="39ed6-125">Aukeratu **Autenticatu Campaign Monitor-ekin** eta eman zure administratzaile egiaztagiriak Campaign Monitor-erako.</span><span class="sxs-lookup"><span data-stu-id="39ed6-125">Select **Authenticate with Campaign Monitor** and provide your admin credentials for Campaign Monitor.</span></span>

1. <span data-ttu-id="39ed6-126">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="39ed6-126">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="39ed6-127">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="39ed6-127">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="39ed6-128">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="39ed6-128">Configure an export</span></span>

<span data-ttu-id="39ed6-129">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="39ed6-129">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="39ed6-130">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="39ed6-130">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="39ed6-131">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="39ed6-131">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="39ed6-132">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="39ed6-132">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="39ed6-133">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Campaign Monitor sekzioan.</span><span class="sxs-lookup"><span data-stu-id="39ed6-133">In the **Connection for export** field, choose a connection from the Campaign Monitor section.</span></span> <span data-ttu-id="39ed6-134">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="39ed6-134">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="39ed6-135">Idatzi [**Campaign Monitor zerrendaren IDa**](https://www.campaignmonitor.com/api/getting-started/#your-list-id).</span><span class="sxs-lookup"><span data-stu-id="39ed6-135">Enter your [**Campaign Monitor List ID**](https://www.campaignmonitor.com/api/getting-started/#your-list-id).</span></span>    
   <span data-ttu-id="39ed6-136">[Sortu API gakoa](https://www.campaignmonitor.com/api/getting-started/) hurrengotik **Kontu ezarpenak** Campaign Monitor-en lehenengo API zerrendaren IDa ikusteko.</span><span class="sxs-lookup"><span data-stu-id="39ed6-136">[Generate the API key](https://www.campaignmonitor.com/api/getting-started/) from **Account Settings** in Campaign Monitor first to view the API list ID.</span></span>  

3. <span data-ttu-id="39ed6-137">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="39ed6-137">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="39ed6-138">Segmentuak esportatu behar dira Campaign Monitor.</span><span class="sxs-lookup"><span data-stu-id="39ed6-138">It's required to export segments to Campaign Monitor.</span></span>

1. <span data-ttu-id="39ed6-139">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="39ed6-139">Select **Save**.</span></span>

<span data-ttu-id="39ed6-140">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="39ed6-140">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="39ed6-141">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="39ed6-141">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="39ed6-142">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="39ed6-142">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="39ed6-143">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="39ed6-143">Data privacy and compliance</span></span>

<span data-ttu-id="39ed6-144">Gaitzen duzunean Dynamics 365 Customer Insights datuak Campaign Monitor-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="39ed6-144">When you enable Dynamics 365 Customer Insights to transmit data to Campaign Monitor, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="39ed6-145">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Campaign Monitor-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz.</span><span class="sxs-lookup"><span data-stu-id="39ed6-145">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Campaign Monitor meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="39ed6-146">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="39ed6-146">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="39ed6-147">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="39ed6-147">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
