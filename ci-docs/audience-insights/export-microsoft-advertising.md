---
title: Esportatu Customer Insights datuak Microsoft Advertising-era
description: Ikasi konexioa konfiguratzen eta esportatzen Microsoft Advertising-era.
ms.date: 05/12/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: c2ac92de2718cf7f0622b407bf198a7a7e50a37b
ms.sourcegitcommit: 831765a55775d358447cb7ffa56f2c3b85459084
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6124447"
---
# <a name="export-segments-to-microsoft-advertising-preview"></a><span data-ttu-id="3604f-103">Esportatu segmentuak Microsoft Advertising-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="3604f-103">Export segments to Microsoft Advertising (preview)</span></span>

<span data-ttu-id="3604f-104">Esportatu Customer Insights segmentuak Microsoft Advertising-era Customer Match audientziak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="3604f-104">Export Customer Insights segments to Microsoft Advertising to create Customer Match audiences.</span></span> <span data-ttu-id="3604f-105">Erabili hartzaile hauek iragarkien kanpainetarako.</span><span class="sxs-lookup"><span data-stu-id="3604f-105">Use these audiences for your ad campaigns.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3604f-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="3604f-106">Prerequisites</span></span>

-   <span data-ttu-id="3604f-107">[Microsoft Advertising kontua](https://ads.microsoft.com/) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="3604f-107">An [Microsoft Advertising account](https://ads.microsoft.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="3604f-108">Customer Match-en erabilera-baldintzak onartu dituzu.</span><span class="sxs-lookup"><span data-stu-id="3604f-108">You've accepted the Customer Match terms of use.</span></span> 
-   <span data-ttu-id="3604f-109">[Konfiguratutako segmentuak](segments.md) hartzaileen xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="3604f-109">[Configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="3604f-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa duen eremu bat dute.</span><span class="sxs-lookup"><span data-stu-id="3604f-110">Unified customer profiles in the exported segments contain a field with an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="3604f-111">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="3604f-111">Known limitations</span></span>

- <span data-ttu-id="3604f-112">Esportazio bakoitzeko 500.000 bat profil esportatu ditzakezu Microsoft Advertising-era.</span><span class="sxs-lookup"><span data-stu-id="3604f-112">You can export up to 500 K profiles per export to Microsoft Advertising.</span></span>
- <span data-ttu-id="3604f-113">Microsoft Advertising-era esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="3604f-113">Exporting to Microsoft Advertising is limited to segments.</span></span>
- <span data-ttu-id="3604f-114">Gehienez 500.000 profil Microsoft Advertising-era esportatzeak 10 minutu behar ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="3604f-114">Exporting up to 500 K profiles to Microsoft Advertising can take up to 10 minutes to complete.</span></span> 


## <a name="set-up-the-connection-to-microsoft-advertising"></a><span data-ttu-id="3604f-115">Konfiguratu Microsoft Advertising-erako konexioa</span><span class="sxs-lookup"><span data-stu-id="3604f-115">Set up the connection to Microsoft Advertising</span></span>

1. <span data-ttu-id="3604f-116">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="3604f-116">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="3604f-117">Hautatu **Gehitu konexioa** eta aukeratu **Microsoft Advertising** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="3604f-117">Select **Add connection** and choose **Microsoft Advertising** to configure the connection.</span></span>

1. <span data-ttu-id="3604f-118">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="3604f-118">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="3604f-119">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="3604f-119">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="3604f-120">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="3604f-120">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="3604f-121">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="3604f-121">Choose who can use this connection.</span></span> <span data-ttu-id="3604f-122">Lehenetsia administratzaileak dira.</span><span class="sxs-lookup"><span data-stu-id="3604f-122">The default is administrators.</span></span> <span data-ttu-id="3604f-123">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="3604f-123">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="3604f-124">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="3604f-124">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="3604f-125">Aukeratu **Konektatu** Microsoft Advertising-erako konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="3604f-125">Select **Connect** to initialize the connection to Microsoft Advertising.</span></span>

1. <span data-ttu-id="3604f-126">Aukeratu **Autenticatu CMicrosoft Advertising-ekin** eta eman zure administratzaile egiaztagiriak Microsoft Advertising-erako.</span><span class="sxs-lookup"><span data-stu-id="3604f-126">Select **Authenticate with Microsoft Advertising** and provide your admin credentials for Microsoft Advertising.</span></span>

1. <span data-ttu-id="3604f-127">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="3604f-127">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="3604f-128">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="3604f-128">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="3604f-129">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="3604f-129">Configure an export</span></span>

<span data-ttu-id="3604f-130">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="3604f-130">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="3604f-131">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="3604f-131">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="3604f-132">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="3604f-132">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="3604f-133">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="3604f-133">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="3604f-134">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Microsoft Advertising sekzioan.</span><span class="sxs-lookup"><span data-stu-id="3604f-134">In the **Connection for export** field, choose a connection from the Microsoft Advertising section.</span></span> <span data-ttu-id="3604f-135">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="3604f-135">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="3604f-136">Hautatu esportatzeko segmentuak.</span><span class="sxs-lookup"><span data-stu-id="3604f-136">Select the segments to export.</span></span> <span data-ttu-id="3604f-137">Microsoft Advertising-eko Customer Match audientziak automatikoki sortzen dira esportatzeko hautatutako segmentuen izenarekin.</span><span class="sxs-lookup"><span data-stu-id="3604f-137">The Customer Match audiences in Microsoft Advertising are automatically created with the name of the segments selected for export.</span></span> <span data-ttu-id="3604f-138">Segmentu bakoitzak Customer Match audientzia bereizi bat sortuko du.</span><span class="sxs-lookup"><span data-stu-id="3604f-138">Each segment will result in a separate Customer Match audience.</span></span> 

1. <span data-ttu-id="3604f-139">Sartu **Microsoft Advertising Bezeroaren IDa eta Kontuaren IDa**.</span><span class="sxs-lookup"><span data-stu-id="3604f-139">Enter your **Microsoft Advertising Customer ID and Account ID**.</span></span> <span data-ttu-id="3604f-140">Bezeroaren IDa (`cid`) eta Kontuaren IDa (`aid`) URLaren parametroetan aurki ditzakezu Microsoft Advertising-en saioa hasten duzunean.</span><span class="sxs-lookup"><span data-stu-id="3604f-140">You can find the Customer ID (`cid`) and Account ID (`aid`) in the parameters of the URL when you're signed in Microsoft Advertising.</span></span>

1. <span data-ttu-id="3604f-141">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu bezeroaren profil bateratuko eremua bezero baten helbide elektronikoarekin.</span><span class="sxs-lookup"><span data-stu-id="3604f-141">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile with a customer's email address.</span></span> <span data-ttu-id="3604f-142">Segmentuak esportatu behar dira Microsoft Advertising-era.</span><span class="sxs-lookup"><span data-stu-id="3604f-142">It's required to export segments to Microsoft Advertising.</span></span>

1. <span data-ttu-id="3604f-143">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="3604f-143">Select **Save**.</span></span>

<span data-ttu-id="3604f-144">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="3604f-144">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="3604f-145">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="3604f-145">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="3604f-146">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="3604f-146">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="3604f-147">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="3604f-147">Data privacy and compliance</span></span>

<span data-ttu-id="3604f-148">Gaitzen duzunean Dynamics 365 Customer Insights datuak Microsoft Advertising-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="3604f-148">When you enable Dynamics 365 Customer Insights to transmit data to Microsoft Advertising, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="3604f-149">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Microsoft Advertising-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz.</span><span class="sxs-lookup"><span data-stu-id="3604f-149">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Microsoft Advertising meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="3604f-150">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="3604f-150">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="3604f-151">Funtzio hau erabiltzeari uzteko, esportazioaren helburuko kokaleku hori ken dezake Dynamics 365 Customer Insights administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="3604f-151">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to stop use of this functionality.</span></span>
