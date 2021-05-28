---
title: Esportatu datuak Customer Insights-etik
description: Kudeatu esportazioak datuak partekatzeko.
ms.date: 03/25/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: c1078ed0ba259a6e9cde3c7ede3570890ae48e67
ms.sourcegitcommit: 33a8e21b3bf6521bdb8346f81f79fce88091ddfd
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6016599"
---
# <a name="exports-preview-overview"></a><span data-ttu-id="42c9e-103">Esportazioak (aurreargitalpena) ikuspegi orokorra</span><span class="sxs-lookup"><span data-stu-id="42c9e-103">Exports (preview) overview</span></span>

<span data-ttu-id="42c9e-104">**Esportazioak** orrialdeak konfiguratutako esportazio guztiak erakusten ditu.</span><span class="sxs-lookup"><span data-stu-id="42c9e-104">The **Exports** page shows you all configured exports.</span></span> <span data-ttu-id="42c9e-105">Esportazioek datu zehatzak partekatzen dituzte hainbat aplikaziorekin.</span><span class="sxs-lookup"><span data-stu-id="42c9e-105">Exports share specific data with various applications.</span></span> <span data-ttu-id="42c9e-106">Bezeroen profilak edo entitateak, eskemak eta mapen xehetasunak sar ditzakete.</span><span class="sxs-lookup"><span data-stu-id="42c9e-106">They can include customer profiles or entities, schemas, and mapping details.</span></span> <span data-ttu-id="42c9e-107">Esportazio bakoitzak [konexioa, administratzaile batek konfiguratuta, autentifikazioa eta sarbidea kudeatzeko](connections.md).</span><span class="sxs-lookup"><span data-stu-id="42c9e-107">Each export requires a [connection, set up by an administrator, to manage authentication and access](connections.md).</span></span>

<span data-ttu-id="42c9e-108">Joan **Datuak** > **Esportazioak** esportazioen orria ikusteko.</span><span class="sxs-lookup"><span data-stu-id="42c9e-108">Go to **Data** > **Exports** to view the exports page.</span></span> <span data-ttu-id="42c9e-109">Erabiltzaile rol guztiek konfiguratutako esportazioak ikusteko sarbidea dute.</span><span class="sxs-lookup"><span data-stu-id="42c9e-109">All user roles have access to view configured exports.</span></span> <span data-ttu-id="42c9e-110">Komando-barrako bilaketa-eremua erabiltzea esportazioak haien izenaren, konexioaren izenaren edo konexio motaren arabera aurkitzeko.</span><span class="sxs-lookup"><span data-stu-id="42c9e-110">Use of the search field in the command bar to find exports by their name, connection name, or connection type.</span></span>

## <a name="set-up-a-new-export"></a><span data-ttu-id="42c9e-111">Konfiguratu esportazio berria</span><span class="sxs-lookup"><span data-stu-id="42c9e-111">Set up a new export</span></span>

<span data-ttu-id="42c9e-112">Esportazioa konfiguratzeko edo editatzeko, konexioak eskuragarri izan behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="42c9e-112">To set up or edit an export, you need to have connections available to you.</span></span> <span data-ttu-id="42c9e-113">Konexioak zure araberakoak dira [erabiltzailearen rola](permissions.md):</span><span class="sxs-lookup"><span data-stu-id="42c9e-113">Connections depend on your [user role](permissions.md):</span></span>
- <span data-ttu-id="42c9e-114">Administratzaileek konexio guztietarako sarbidea dute.</span><span class="sxs-lookup"><span data-stu-id="42c9e-114">Administrators have access to all connections.</span></span> <span data-ttu-id="42c9e-115">Konexio berriak sor ditzakete esportazioa konfiguratzerakoan.</span><span class="sxs-lookup"><span data-stu-id="42c9e-115">They can also create new connections when setting up an export.</span></span>
- <span data-ttu-id="42c9e-116">Laguntzaileek konexio zehatzetarako sarbidea izan dezakete.</span><span class="sxs-lookup"><span data-stu-id="42c9e-116">Contributors can have access to specific connections.</span></span> <span data-ttu-id="42c9e-117">Konexioak konfiguratzeko eta partekatzeko administratzaileen mende daude.</span><span class="sxs-lookup"><span data-stu-id="42c9e-117">They depend on administrators to configure and share connections.</span></span> <span data-ttu-id="42c9e-118">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="42c9e-118">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>
- <span data-ttu-id="42c9e-119">Ikusleek lehendik dauden esportazioak soilik ikus ditzakete baina ez dituzte sortu.</span><span class="sxs-lookup"><span data-stu-id="42c9e-119">Viewers can only view existing exports but not create them.</span></span>

1. <span data-ttu-id="42c9e-120">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="42c9e-120">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="42c9e-121">Aukeratu **Gehitu esportazioa** esportazio helmuga berria sortzeko.</span><span class="sxs-lookup"><span data-stu-id="42c9e-121">Select **Add export** to create a new export destination.</span></span>

1. <span data-ttu-id="42c9e-122">Hurrengoan **Konfiguratu esportazioa** panelean, hautatu zein konexio erabili.</span><span class="sxs-lookup"><span data-stu-id="42c9e-122">In the **Set up export** pane, select which connection to use.</span></span> <span data-ttu-id="42c9e-123">[Konexioak](connections.md) administratzaileek kudeatzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="42c9e-123">[Connections](connections.md) are managed by administrators.</span></span> 

1. <span data-ttu-id="42c9e-124">Eman beharrezko xehetasunak eta hautatu **Gorde** esportazioa sortzeko.</span><span class="sxs-lookup"><span data-stu-id="42c9e-124">Provide the required details and select **Save** to create the export.</span></span>

### <a name="edit-an-export"></a><span data-ttu-id="42c9e-125">Editatu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="42c9e-125">Edit an export</span></span>

1. <span data-ttu-id="42c9e-126">Hautatu elipsi bertikala editatu nahi duzun Export helmugarako.</span><span class="sxs-lookup"><span data-stu-id="42c9e-126">Select the vertical ellipsis for the export destination you want to edit.</span></span>

1. <span data-ttu-id="42c9e-127">Hautatu **Editatu** goitibeherako menutik.</span><span class="sxs-lookup"><span data-stu-id="42c9e-127">Select **Edit** from the drop-down menu.</span></span>

1. <span data-ttu-id="42c9e-128">Aldatu eguneratu nahi dituzun balioak eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="42c9e-128">Change the values you want to update and select **Save**.</span></span>

## <a name="view-exports-and-export-details"></a><span data-ttu-id="42c9e-129">Ikusi esportazioak eta esportazioen xehetasunak</span><span class="sxs-lookup"><span data-stu-id="42c9e-129">View Exports and export details</span></span>

<span data-ttu-id="42c9e-130">Esportazio helmugak sortu ondoren, hemen agertzen dira **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="42c9e-130">After creating export destinations, they are listed on **Data** > **Exports**.</span></span> <span data-ttu-id="42c9e-131">Erabiltzaile guztiek ikus dezakete zein datu partekatzen diren eta horien azken egoera.</span><span class="sxs-lookup"><span data-stu-id="42c9e-131">All users can see which data is shared and its latest status.</span></span>

1. <span data-ttu-id="42c9e-132">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="42c9e-132">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="42c9e-133">Editatzeko baimenik ez duten erabiltzaileak hautatzen dituzte **Ikusi** ordez **Editatu** ikusi esportazio xehetasunak.</span><span class="sxs-lookup"><span data-stu-id="42c9e-133">Users without edit permissions select **View** instead of **Edit** see the export details.</span></span>

1. <span data-ttu-id="42c9e-134">Alboko panel honek esportazio honen konfigurazioa erakusten du.</span><span class="sxs-lookup"><span data-stu-id="42c9e-134">This side pane shows the set up of this export.</span></span> <span data-ttu-id="42c9e-135">Editatzeko baimenik gabe ezin dituzu balioak aldatu.</span><span class="sxs-lookup"><span data-stu-id="42c9e-135">Without edit permissions, you can't change values.</span></span> <span data-ttu-id="42c9e-136">Aukeratu **Itxi** esportazioen orrira itzultzeko.</span><span class="sxs-lookup"><span data-stu-id="42c9e-136">Select **Close** to return to the exports page.</span></span>

## <a name="run-exports-on-demand"></a><span data-ttu-id="42c9e-137">Exekutatu esportazioak eskatu ahala</span><span class="sxs-lookup"><span data-stu-id="42c9e-137">Run exports on demand</span></span>

<span data-ttu-id="42c9e-138">Esportazio bat konfiguratu ondoren, guztietan exekutatuko da [freskatze programatua](system.md#schedule-tab) betiere lan konexioa badu.</span><span class="sxs-lookup"><span data-stu-id="42c9e-138">After configuring an export, it will run with every [scheduled refresh](system.md#schedule-tab) as long as it has a working connection.</span></span>

<span data-ttu-id="42c9e-139">Datuak esportatzeko programatutako freskapenaren zain egon gabe, joan hona: **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="42c9e-139">To export data without waiting for a scheduled refresh, go to **Data** > **Exports**.</span></span> <span data-ttu-id="42c9e-140">Bi aukera dituzu:</span><span class="sxs-lookup"><span data-stu-id="42c9e-140">You have two options:</span></span>

- <span data-ttu-id="42c9e-141">Esportazio guztiak exekutatzeko, hautatu **Exekutatu guztiak** komando barran.</span><span class="sxs-lookup"><span data-stu-id="42c9e-141">To run all exports, select **Run all** in the command bar.</span></span> 
- <span data-ttu-id="42c9e-142">Esportazio bakarra exekutatzeko, hautatu elipsia (...) zerrendako elementu batean eta ondoren aukeratu **Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="42c9e-142">To run a single export, select the ellipsis (...) on a list item and then choose **Run**.</span></span>

## <a name="remove-an-export"></a><span data-ttu-id="42c9e-143">Ezabatu Esportatu</span><span class="sxs-lookup"><span data-stu-id="42c9e-143">Remove an Export</span></span>

1. <span data-ttu-id="42c9e-144">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="42c9e-144">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="42c9e-145">Hautatu elipsi bertikala kendu nahi duzun Esportaziorako.</span><span class="sxs-lookup"><span data-stu-id="42c9e-145">Select the vertical ellipsis for the Export you want to remove.</span></span>

1. <span data-ttu-id="42c9e-146">Hautatu **Kendu** goitibeherako menuan.</span><span class="sxs-lookup"><span data-stu-id="42c9e-146">Select **Remove** from the dropdown menu.</span></span>

1. <span data-ttu-id="42c9e-147">Baieztatu kentzea aukeratuz **Kendu** berrespen-pantailan.</span><span class="sxs-lookup"><span data-stu-id="42c9e-147">Confirm the removal by selecting **Remove** on the confirmation screen.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
