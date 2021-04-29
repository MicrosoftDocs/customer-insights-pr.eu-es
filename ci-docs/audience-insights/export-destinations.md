---
title: Esportatu datuak Customer Insights-etik
description: Kudeatu esportazioak datuak partekatzeko.
ms.date: 03/25/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 354ce9ef30fe918975d06290430996c84f8bd3f7
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5896128"
---
# <a name="exports-preview-overview"></a><span data-ttu-id="24a3f-103">Esportazioak (aurreargitalpena) ikuspegi orokorra</span><span class="sxs-lookup"><span data-stu-id="24a3f-103">Exports (preview) overview</span></span>

<span data-ttu-id="24a3f-104">**Esportazioak** orrialdeak konfiguratutako esportazio guztiak erakusten ditu.</span><span class="sxs-lookup"><span data-stu-id="24a3f-104">The **Exports** page shows you all configured exports.</span></span> <span data-ttu-id="24a3f-105">Esportazioek datu zehatzak partekatzen dituzte hainbat aplikaziorekin.</span><span class="sxs-lookup"><span data-stu-id="24a3f-105">Exports share specific data with various applications.</span></span> <span data-ttu-id="24a3f-106">Bezeroen profilak edo entitateak, eskemak eta mapen xehetasunak sar ditzakete.</span><span class="sxs-lookup"><span data-stu-id="24a3f-106">They can include customer profiles or entities, schemas, and mapping details.</span></span> <span data-ttu-id="24a3f-107">Esportazio bakoitzak [konexioa, administratzaile batek konfiguratuta, autentifikazioa eta sarbidea kudeatzeko](connections.md).</span><span class="sxs-lookup"><span data-stu-id="24a3f-107">Each export requires a [connection, set up by an administrator, to manage authentication and access](connections.md).</span></span>

> [!NOTE]
> <span data-ttu-id="24a3f-108">2021eko martxora arte, esportazioek konexioa sortu zuten dagokion zerbitzura automatikoki.</span><span class="sxs-lookup"><span data-stu-id="24a3f-108">Until March 2021, exports created a connection to the corresponding service automatically.</span></span> <span data-ttu-id="24a3f-109">Esportazioek orain [konexioa, administratzaile batek sortua eta partekatua](connections.md) sortu aurretik.</span><span class="sxs-lookup"><span data-stu-id="24a3f-109">Exports now require a [connection, created and shared by an administrator](connections.md) before you can create them.</span></span>

<span data-ttu-id="24a3f-110">Joan **Datuak** > **Esportazioak** esportazioen orria ikusteko.</span><span class="sxs-lookup"><span data-stu-id="24a3f-110">Go to **Data** > **Exports** to view the exports page.</span></span> <span data-ttu-id="24a3f-111">Erabiltzaile rol guztiek konfiguratutako esportazioak ikusteko sarbidea dute.</span><span class="sxs-lookup"><span data-stu-id="24a3f-111">All user roles have access to view configured exports.</span></span> <span data-ttu-id="24a3f-112">Komando-barrako bilaketa-eremua erabiltzea esportazioak haien izenaren, konexioaren izenaren edo konexio motaren arabera aurkitzeko.</span><span class="sxs-lookup"><span data-stu-id="24a3f-112">Use of the search field in the command bar to find exports by their name, connection name, or connection type.</span></span>

## <a name="set-up-a-new-export"></a><span data-ttu-id="24a3f-113">Konfiguratu esportazio berria</span><span class="sxs-lookup"><span data-stu-id="24a3f-113">Set up a new export</span></span>

<span data-ttu-id="24a3f-114">Esportazioa konfiguratzeko edo editatzeko, konexioak eskuragarri izan behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="24a3f-114">To set up or edit an export, you need to have connections available to you.</span></span> <span data-ttu-id="24a3f-115">Konexioak zure araberakoak dira [erabiltzailearen rola](permissions.md):</span><span class="sxs-lookup"><span data-stu-id="24a3f-115">Connections depend on your [user role](permissions.md):</span></span>
- <span data-ttu-id="24a3f-116">Administratzaileek konexio guztietarako sarbidea dute.</span><span class="sxs-lookup"><span data-stu-id="24a3f-116">Administrators have access to all connections.</span></span> <span data-ttu-id="24a3f-117">Konexio berriak sor ditzakete esportazioa konfiguratzerakoan.</span><span class="sxs-lookup"><span data-stu-id="24a3f-117">They can also create new connections when setting up an export.</span></span>
- <span data-ttu-id="24a3f-118">Laguntzaileek konexio zehatzetarako sarbidea izan dezakete.</span><span class="sxs-lookup"><span data-stu-id="24a3f-118">Contributors can have access to specific connections.</span></span> <span data-ttu-id="24a3f-119">Konexioak konfiguratzeko eta partekatzeko administratzaileen mende daude.</span><span class="sxs-lookup"><span data-stu-id="24a3f-119">They depend on administrators to configure and share connections.</span></span> <span data-ttu-id="24a3f-120">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="24a3f-120">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>
- <span data-ttu-id="24a3f-121">Ikusleek lehendik dauden esportazioak soilik ikus ditzakete baina ez dituzte sortu.</span><span class="sxs-lookup"><span data-stu-id="24a3f-121">Viewers can only view existing exports but not create them.</span></span>

1. <span data-ttu-id="24a3f-122">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="24a3f-122">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="24a3f-123">Aukeratu **Gehitu esportazioa** esportazio helmuga berria sortzeko.</span><span class="sxs-lookup"><span data-stu-id="24a3f-123">Select **Add export** to create a new export destination.</span></span>

1. <span data-ttu-id="24a3f-124">Hurrengoan **Konfiguratu esportazioa** panelean, hautatu zein konexio erabili.</span><span class="sxs-lookup"><span data-stu-id="24a3f-124">In the **Set up export** pane, select which connection to use.</span></span> <span data-ttu-id="24a3f-125">[Konexioak](connections.md) administratzaileek kudeatzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="24a3f-125">[Connections](connections.md) are managed by administrators.</span></span> 

1. <span data-ttu-id="24a3f-126">Eman beharrezko xehetasunak eta hautatu **Gorde** esportazioa sortzeko.</span><span class="sxs-lookup"><span data-stu-id="24a3f-126">Provide the required details and select **Save** to create the export.</span></span>

### <a name="edit-an-export"></a><span data-ttu-id="24a3f-127">Editatu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="24a3f-127">Edit an export</span></span>

1. <span data-ttu-id="24a3f-128">Hautatu elipsi bertikala editatu nahi duzun Export helmugarako.</span><span class="sxs-lookup"><span data-stu-id="24a3f-128">Select the vertical ellipsis for the export destination you want to edit.</span></span>

1. <span data-ttu-id="24a3f-129">Hautatu **Editatu** goitibeherako menutik.</span><span class="sxs-lookup"><span data-stu-id="24a3f-129">Select **Edit** from the drop-down menu.</span></span>

1. <span data-ttu-id="24a3f-130">Aldatu eguneratu nahi dituzun balioak eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="24a3f-130">Change the values you want to update and select **Save**.</span></span>

## <a name="view-exports-and-export-details"></a><span data-ttu-id="24a3f-131">Ikusi esportazioak eta esportazioen xehetasunak</span><span class="sxs-lookup"><span data-stu-id="24a3f-131">View Exports and export details</span></span>

<span data-ttu-id="24a3f-132">Esportazio helmugak sortu ondoren, hemen agertzen dira **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="24a3f-132">After creating export destinations, they are listed on **Data** > **Exports**.</span></span> <span data-ttu-id="24a3f-133">Erabiltzaile guztiek ikus dezakete zein datu partekatzen diren eta horien azken egoera.</span><span class="sxs-lookup"><span data-stu-id="24a3f-133">All users can see which data is shared and its latest status.</span></span>

1. <span data-ttu-id="24a3f-134">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="24a3f-134">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="24a3f-135">Editatzeko baimenik ez duten erabiltzaileak hautatzen dituzte **Ikusi** ordez **Editatu** ikusi esportazio xehetasunak.</span><span class="sxs-lookup"><span data-stu-id="24a3f-135">Users without edit permissions select **View** instead of **Edit** see the export details.</span></span>

1. <span data-ttu-id="24a3f-136">Alboko panel honek esportazio honen konfigurazioa erakusten du.</span><span class="sxs-lookup"><span data-stu-id="24a3f-136">This side pane shows the set up of this export.</span></span> <span data-ttu-id="24a3f-137">Editatzeko baimenik gabe ezin dituzu balioak aldatu.</span><span class="sxs-lookup"><span data-stu-id="24a3f-137">Without edit permissions, you can't change values.</span></span> <span data-ttu-id="24a3f-138">Aukeratu **Itxi** esportazioen orrira itzultzeko.</span><span class="sxs-lookup"><span data-stu-id="24a3f-138">Select **Close** to return to the exports page.</span></span>

## <a name="run-exports-on-demand"></a><span data-ttu-id="24a3f-139">Exekutatu esportazioak eskatu ahala</span><span class="sxs-lookup"><span data-stu-id="24a3f-139">Run exports on demand</span></span>

<span data-ttu-id="24a3f-140">Esportazio bat konfiguratu ondoren, guztietan exekutatuko da [freskatze programatua](system.md#schedule-tab) betiere lan konexioa badu.</span><span class="sxs-lookup"><span data-stu-id="24a3f-140">After configuring an export, it will run with every [scheduled refresh](system.md#schedule-tab) as long as it has a working connection.</span></span>

<span data-ttu-id="24a3f-141">Datuak esportatzeko programatutako freskapenaren zain egon gabe, joan hona: **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="24a3f-141">To export data without waiting for a scheduled refresh, go to **Data** > **Exports**.</span></span> <span data-ttu-id="24a3f-142">Bi aukera dituzu:</span><span class="sxs-lookup"><span data-stu-id="24a3f-142">You have two options:</span></span>

- <span data-ttu-id="24a3f-143">Esportazio guztiak exekutatzeko, hautatu **Exekutatu guztiak** komando barran.</span><span class="sxs-lookup"><span data-stu-id="24a3f-143">To run all exports, select **Run all** in the command bar.</span></span> 
- <span data-ttu-id="24a3f-144">Esportazio bakarra exekutatzeko, hautatu elipsia (...) zerrendako elementu batean eta ondoren aukeratu **Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="24a3f-144">To run a single export, select the ellipsis (...) on a list item and then choose **Run**.</span></span>

## <a name="remove-an-export"></a><span data-ttu-id="24a3f-145">Ezabatu Esportatu</span><span class="sxs-lookup"><span data-stu-id="24a3f-145">Remove an Export</span></span>

1. <span data-ttu-id="24a3f-146">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="24a3f-146">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="24a3f-147">Hautatu elipsi bertikala kendu nahi duzun Esportaziorako.</span><span class="sxs-lookup"><span data-stu-id="24a3f-147">Select the vertical ellipsis for the Export you want to remove.</span></span>

1. <span data-ttu-id="24a3f-148">Hautatu **Kendu** goitibeherako menuan.</span><span class="sxs-lookup"><span data-stu-id="24a3f-148">Select **Remove** from the dropdown menu.</span></span>

1. <span data-ttu-id="24a3f-149">Baieztatu kentzea aukeratuz **Kendu** berrespen-pantailan.</span><span class="sxs-lookup"><span data-stu-id="24a3f-149">Confirm the removal by selecting **Remove** on the confirmation screen.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
