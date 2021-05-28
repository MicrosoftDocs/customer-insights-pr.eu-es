---
title: Esportatu Customer Insights datuak Snapchat-era
description: Ikasi konexioa konfiguratzen eta esportatzen Snapchat.
ms.date: 03/22/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: d3dae7f0fef1fc3792c90c8ac0d3b037f5c0923d
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760460"
---
# <a name="export-segment-lists-to-snapchat-preview"></a><span data-ttu-id="27a48-103">Esportatu segmentuen zerrendak Snapchat (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="27a48-103">Export segment lists to Snapchat (preview)</span></span>

<span data-ttu-id="27a48-104">Esportatu bezeroen profil bateratuen segmentuak Snapchat eta erabili iragarkietarako.</span><span class="sxs-lookup"><span data-stu-id="27a48-104">Export segments of unified customer profiles to Snapchat and use them for advertising.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="27a48-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="27a48-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="27a48-106">Baduzu [Snapchat mailako kontua](https://business.snapchat.com/), [Snapchat iragarkien kontua](https://ads.snapchat.com/) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="27a48-106">You have a [Snapchat Business account](https://business.snapchat.com/), a [Snapchat Ads account](https://ads.snapchat.com/), and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="27a48-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="27a48-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="27a48-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="27a48-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="27a48-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="27a48-109">Known limitations</span></span>

- <span data-ttu-id="27a48-110">Snapchat esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="27a48-110">Exporting to Snapchat is limited to segments.</span></span>
- <span data-ttu-id="27a48-111">Esportatu gehienez 1 milioi profil Snapchat, 15 minutu behar ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="27a48-111">Exporting up to 1 million profiles to Snapchat can take up to 15 minutes to complete.</span></span> 

## <a name="set-up-connection-to-snapchat"></a><span data-ttu-id="27a48-112">Konfiguratu konexioa Snapchat-era</span><span class="sxs-lookup"><span data-stu-id="27a48-112">Set up connection to Snapchat</span></span>

1. <span data-ttu-id="27a48-113">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="27a48-113">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="27a48-114">Hautatu **Gehitu konexioa** eta aukeratu **Snapchat** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="27a48-114">Select **Add connection** and choose **Snapchat** to configure the connection.</span></span>

1. <span data-ttu-id="27a48-115">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="27a48-115">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="27a48-116">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="27a48-116">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="27a48-117">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="27a48-117">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="27a48-118">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="27a48-118">Choose who can use this connection.</span></span> <span data-ttu-id="27a48-119">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="27a48-119">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="27a48-120">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="27a48-120">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="27a48-121">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="27a48-121">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="27a48-122">Aukeratu **Konektatu** Snapchat konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="27a48-122">Select **Connect** to initialize the connection to Snapchat.</span></span>

1. <span data-ttu-id="27a48-123">Aukeratu **Autenticatu Snapchat-ekin** eta eman zure administratzaile egiaztagiriak Snapchat-erako.</span><span class="sxs-lookup"><span data-stu-id="27a48-123">Select **Authenticate with Snapchat** and provide your admin credentials for Snapchat.</span></span> 

1. <span data-ttu-id="27a48-124">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="27a48-124">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="27a48-125">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="27a48-125">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="27a48-126">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="27a48-126">Configure an export</span></span>

<span data-ttu-id="27a48-127">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="27a48-127">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="27a48-128">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="27a48-128">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="27a48-129">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="27a48-129">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="27a48-130">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="27a48-130">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="27a48-131">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Snapchat sekzioan.</span><span class="sxs-lookup"><span data-stu-id="27a48-131">In the **Connection for export** field, choose a connection from the Snapchat section.</span></span> <span data-ttu-id="27a48-132">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="27a48-132">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="27a48-133">Sartu [**Snapchat Audience IDa**](https://businesshelp.snapchat.com/s/article/custom-audiences).</span><span class="sxs-lookup"><span data-stu-id="27a48-133">Enter the [**Snapchat Audience ID**](https://businesshelp.snapchat.com/s/article/custom-audiences).</span></span>

1. <span data-ttu-id="27a48-134">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="27a48-134">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="27a48-135">Segmentuak esportatu behar dira Snapchat.</span><span class="sxs-lookup"><span data-stu-id="27a48-135">It's required to export segments to Snapchat.</span></span>

1. <span data-ttu-id="27a48-136">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="27a48-136">Select the segments you want to export.</span></span> 

1. <span data-ttu-id="27a48-137">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="27a48-137">Select **Save**.</span></span>

<span data-ttu-id="27a48-138">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="27a48-138">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="27a48-139">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="27a48-139">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="27a48-140">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="27a48-140">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="27a48-141">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="27a48-141">Data privacy and compliance</span></span>

<span data-ttu-id="27a48-142">Gaitzen duzunean Dynamics 365 Customer Insights datuak Snapchat-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="27a48-142">When you enable Dynamics 365 Customer Insights to transmit data to Snapchat, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="27a48-143">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Snapchat-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz.</span><span class="sxs-lookup"><span data-stu-id="27a48-143">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Snapchat meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="27a48-144">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="27a48-144">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="27a48-145">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="27a48-145">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>