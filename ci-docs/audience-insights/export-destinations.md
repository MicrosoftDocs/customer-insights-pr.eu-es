---
title: Esportatu datuak Customer Insights-etik
description: Kudeatu esportazioak datuak partekatzeko.
ms.date: 06/14/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 28563e3a76535cb0c92bfcda4ef5037430d00cfa
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305463"
---
# <a name="exports-preview-overview"></a><span data-ttu-id="f0cc7-103">Esportazioak (aurreargitalpena) ikuspegi orokorra</span><span class="sxs-lookup"><span data-stu-id="f0cc7-103">Exports (preview) overview</span></span>

<span data-ttu-id="f0cc7-104">**Esportazioak** orrialdeak konfiguratutako esportazio guztiak erakusten ditu.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-104">The **Exports** page shows you all configured exports.</span></span> <span data-ttu-id="f0cc7-105">Esportazioek datu zehatzak partekatzen dituzte hainbat aplikaziorekin.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-105">Exports share specific data with various applications.</span></span> <span data-ttu-id="f0cc7-106">Bezeroen profilak edo entitateak, eskemak eta mapen xehetasunak sar ditzakete.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-106">They can include customer profiles or entities, schemas, and mapping details.</span></span> <span data-ttu-id="f0cc7-107">Esportazio bakoitzak [konexioa, administratzaile batek konfiguratuta, autentifikazioa eta sarbidea kudeatzeko](connections.md).</span><span class="sxs-lookup"><span data-stu-id="f0cc7-107">Each export requires a [connection, set up by an administrator, to manage authentication and access](connections.md).</span></span>

<span data-ttu-id="f0cc7-108">Joan **Datuak** > **Esportazioak** esportazioen orria ikusteko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-108">Go to **Data** > **Exports** to view the exports page.</span></span> <span data-ttu-id="f0cc7-109">Erabiltzaile rol guztiek konfiguratutako esportazioak ikus ditzakete.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-109">All user roles can view configured exports.</span></span> <span data-ttu-id="f0cc7-110">Erabili komando-barrako bilaketa-eremua esportazioak haien izenaren, konexioaren izenaren edo konexio motaren arabera aurkitzeko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-110">Use the search field in the command bar to find exports by their name, connection name, or connection type.</span></span>

## <a name="set-up-a-new-export"></a><span data-ttu-id="f0cc7-111">Konfiguratu esportazio berria</span><span class="sxs-lookup"><span data-stu-id="f0cc7-111">Set up a new export</span></span>

<span data-ttu-id="f0cc7-112">Esportazioa konfiguratzeko edo editatzeko, konexioak eskuragarri izan behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-112">To set up or edit an export, you need to have connections available to you.</span></span> <span data-ttu-id="f0cc7-113">Konexioak zure araberakoak dira [erabiltzailearen rola](permissions.md):</span><span class="sxs-lookup"><span data-stu-id="f0cc7-113">Connections depend on your [user role](permissions.md):</span></span>
- <span data-ttu-id="f0cc7-114">Administratzaileek konexio guztietarako sarbidea dute.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-114">Administrators have access to all connections.</span></span> <span data-ttu-id="f0cc7-115">Konexio berriak sor ditzakete esportazioa konfiguratzerakoan.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-115">They can also create new connections when setting up an export.</span></span>
- <span data-ttu-id="f0cc7-116">Laguntzaileek konexio zehatzetarako sarbidea izan dezakete.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-116">Contributors can have access to specific connections.</span></span> <span data-ttu-id="f0cc7-117">Konexioak konfiguratzeko eta partekatzeko administratzaileen mende daude.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-117">They depend on administrators to configure and share connections.</span></span> <span data-ttu-id="f0cc7-118">Esportazioen zerrendan agertzen da laguntzaileek esportazio bat editatu edo soilik ikus dezaketen **Zure baimenak** zutabean.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-118">The exports list shows contributors whether they can edit or only view an export in the **Your permissions** column.</span></span> <span data-ttu-id="f0cc7-119">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="f0cc7-119">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>
- <span data-ttu-id="f0cc7-120">Ikusleek lehendik dauden esportazioak soilik ikus ditzakete baina ez dituzte sortu.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-120">Viewers can only view existing exports but not create them.</span></span>

### <a name="define-a-new-export"></a><span data-ttu-id="f0cc7-121">Definitu esportazio berria</span><span class="sxs-lookup"><span data-stu-id="f0cc7-121">Define a new export</span></span>

1. <span data-ttu-id="f0cc7-122">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-122">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="f0cc7-123">Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-123">Select **Add export** to create a new export.</span></span>

1. <span data-ttu-id="f0cc7-124">Hurrengoan **Konfiguratu esportazioa** panelean, hautatu zein konexio erabili.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-124">In the **Set up export** pane, select which connection to use.</span></span> <span data-ttu-id="f0cc7-125">[Konexioak](connections.md) administratzaileek kudeatzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-125">[Connections](connections.md) are managed by administrators.</span></span> 

1. <span data-ttu-id="f0cc7-126">Eman beharrezko xehetasunak eta hautatu **Gorde** esportazioa sortzeko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-126">Provide the required details and select **Save** to create the export.</span></span>

### <a name="define-a-new-export-based-on-an-existing-export"></a><span data-ttu-id="f0cc7-127">Definitu esportazio berri bat lehendik dagoen esportazioan oinarrituta</span><span class="sxs-lookup"><span data-stu-id="f0cc7-127">Define a new export based on an existing export</span></span>

1. <span data-ttu-id="f0cc7-128">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-128">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="f0cc7-129">Esportazioen zerrendan, hautatu bikoiztu nahi duzun esportazioa.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-129">In the list of exports, select the export you want to duplicate.</span></span>

1. <span data-ttu-id="f0cc7-130">Aukeratu **Sortu bikoiztuak** komando barran **Konfiguratu esportazioa** panela irakitzeko, hautatutako esportazioaren xehetasunak dituena.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-130">Select **Create duplicate** in the command bar to open the **Set up export** pane with the details of the selected export.</span></span>

1. <span data-ttu-id="f0cc7-131">Berrikusi eta egokitu esportazioa eta hautatu **Gorde** esportazio berri bat sortzeko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-131">Review and adapt the export and select **Save** to create a new export.</span></span>

### <a name="edit-an-export"></a><span data-ttu-id="f0cc7-132">Editatu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="f0cc7-132">Edit an export</span></span>

1. <span data-ttu-id="f0cc7-133">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-133">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="f0cc7-134">Esportazioen zerrendan, hautatu editatu nahi duzun esportazioa.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-134">In the list of exports, select the export you want to edit.</span></span>

1. <span data-ttu-id="f0cc7-135">Komando-barran, hautatu **Editatu**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-135">Select **Edit** in the command bar.</span></span>

1. <span data-ttu-id="f0cc7-136">Aldatu eguneratu nahi dituzun balioak eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-136">Change the values you want to update and select **Save**.</span></span>

## <a name="view-exports-and-export-details"></a><span data-ttu-id="f0cc7-137">Ikusi esportazioak eta esportazioen xehetasunak</span><span class="sxs-lookup"><span data-stu-id="f0cc7-137">View exports and export details</span></span>

<span data-ttu-id="f0cc7-138">Esportazio helmugak sortu ondoren, hemen agertzen dira **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-138">After creating export destinations, they're listed on **Data** > **Exports**.</span></span> <span data-ttu-id="f0cc7-139">Erabiltzaile guztiek ikus dezakete zein datu partekatzen diren eta horien azken egoera.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-139">All users can see which data is shared and its latest status.</span></span>

1. <span data-ttu-id="f0cc7-140">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-140">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="f0cc7-141">Editatzeko baimenik ez duten erabiltzaileak hautatzen dituzte **Ikusi** ordez **Editatu** esportazio xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-141">Users without edit permissions select **View** instead of **Edit** to see the export details.</span></span>

1. <span data-ttu-id="f0cc7-142">Alboko panelak esportazio baten konfigurazioa erakusten du.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-142">The side pane shows the configuration of an export.</span></span> <span data-ttu-id="f0cc7-143">Editatzeko baimenik gabe ezin dituzu balioak aldatu.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-143">Without edit permissions, you can't change values.</span></span> <span data-ttu-id="f0cc7-144">Aukeratu **Itxi** esportazioen orrira itzultzeko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-144">Select **Close** to return to the exports page.</span></span>

## <a name="schedule-and-run-exports"></a><span data-ttu-id="f0cc7-145">Antolatu eta exekutatu esportazioak</span><span class="sxs-lookup"><span data-stu-id="f0cc7-145">Schedule and run exports</span></span>

<span data-ttu-id="f0cc7-146">Konfiguratzen duzun esportazio bakoitzak freskatze ordutegia du.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-146">Each export you configure has a refresh schedule.</span></span> <span data-ttu-id="f0cc7-147">Freskatze batean, sistemak esportazio batean sartzeko datu berri edo eguneratuak bilatzen ditu.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-147">During a refresh, the system looks for new or updated data to include in an export.</span></span> <span data-ttu-id="f0cc7-148">Berez, esportazioak [programatutako eguneratze sistema](system.md#schedule-tab) guztien zati gisa exekutatzen dira.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-148">By default, exports are run as part of every [scheduled system refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="f0cc7-149">Freskatze ordutegia pertsonaliza dezakezu edo desaktiba dezakezu esportazioak eskuz exekutatzeko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-149">You can customize the refresh schedule or turn it off to run exports manually.</span></span>

<span data-ttu-id="f0cc7-150">Esportazio ordutegiak zure ingurunearen egoeraren araberakoak dira.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-150">Export schedules depend on the state of your environment.</span></span> <span data-ttu-id="f0cc7-151">Eguneratzeak martxan badaude aktibatuta [mendekotasunak](system.md#refresh-policies) programatutako esportazio bat hasi behar denean, sistemak eguneraketak osatuko ditu eta esportazioa exekutatuko du.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-151">If there are updates in progress on [dependencies](system.md#refresh-policies) when a scheduled export should start, the system will first complete the updates and then run the export.</span></span> <span data-ttu-id="f0cc7-152">Zutabean esportazio bat noiz freskatu zen azkeneko aldiz ikus dezakezu **Freskatuta** zutabean.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-152">You can see when an export was last refreshed in column **Refreshed**.</span></span>

### <a name="schedule-exports"></a><span data-ttu-id="f0cc7-153">Antolatu esportazioak</span><span class="sxs-lookup"><span data-stu-id="f0cc7-153">Schedule exports</span></span>

<span data-ttu-id="f0cc7-154">Banakako esportazioetarako edo hainbat esportaziorako freskatze ordutegi pertsonalizatuak defini ditzakezu aldi berean.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-154">You can define custom refresh schedules for individual exports or several exports at once.</span></span> <span data-ttu-id="f0cc7-155">Unean definitutako ordutegia esportazio zerrendako **Antolaketa** zutabean agertzen da.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-155">The currently defined schedule is listed in the **Schedule** column of the export list.</span></span> <span data-ttu-id="f0cc7-156">Ordutegia aldatzeko baimena berdina da [esportazioak editatu eta definitzeko](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="f0cc7-156">The permission to change the schedule is the same as for [editing and defining exports](export-destinations.md#set-up-a-new-export).</span></span> 

1. <span data-ttu-id="f0cc7-157">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-157">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="f0cc7-158">Hautatu antolatu nahi duzun esportazioa.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-158">Select the export you want to schedule.</span></span>

1. <span data-ttu-id="f0cc7-159">Komando-barran, hautatu **Antolatu**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-159">Select **Schedule** in the command bar.</span></span>

1. <span data-ttu-id="f0cc7-160">**Programatu esportazioa** panelean, ezarri **Antolatu exekuzioa** aukera **Aktibatuta** gisa, esportazioa automatikoki exekutatzeko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-160">In the **Schedule export** pane, set the **Schedule run** to **On** to run the export automatically.</span></span> <span data-ttu-id="f0cc7-161">Ezarri **Desaktibatuta** gisa eskuz freskatzeko.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-161">Set it to **Off** to refresh it manually.</span></span>

1. <span data-ttu-id="f0cc7-162">Automatikoki freskatutako esportazioetarako, aukeratu **Errepikatzearen** balioa eta zehaztu horren xehetasunak.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-162">For automatically refreshed exports, choose a **Recurrence** value and specify the details for it.</span></span> <span data-ttu-id="f0cc7-163">Definitutako denbora errepikatze-kasu guztiei aplikatzen zaie.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-163">The time defined applies to all instances of a recurrence.</span></span> <span data-ttu-id="f0cc7-164">Esportazio bat freskatzen hasi behar den unea da.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-164">It's the time when an export should start refreshing.</span></span>

1. <span data-ttu-id="f0cc7-165">Aplikatu eta aktibatu aldaketak **Gorde** hautatuta.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-165">Apply and activate your changes by selecting **Save**.</span></span>

<span data-ttu-id="f0cc7-166">Hainbat esportazioen antolaketa editatzerakoan, aukeraketa bat egin behar duzu **Antolaketak gorde edo gainidatzi** atalean:</span><span class="sxs-lookup"><span data-stu-id="f0cc7-166">When editing the schedule for several exports, you need to make a selection under **Keep or override schedules**:</span></span>
- <span data-ttu-id="f0cc7-167">**Mantendu antolaketa indibidualak**: Aurretik definitutako antolaketari eutsi hautatutako esportazioetarako eta desgaitu edo gaitu bakarrik.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-167">**Keep individual schedules**: Persist the previously defined schedule for the selected exports and only disable or enable them.</span></span>
- <span data-ttu-id="f0cc7-168">**Zehaztu hautatutako esportazio guztientzako antolaketa berria**: Gainidatzi hautatutako esportazioen dauden antolaketak.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-168">**Define new schedule for all selected exports**: Override the existing schedules of the selected exports.</span></span>

### <a name="run-exports-on-demand"></a><span data-ttu-id="f0cc7-169">Exekutatu esportazioak eskatu ahala</span><span class="sxs-lookup"><span data-stu-id="f0cc7-169">Run exports on demand</span></span>

<span data-ttu-id="f0cc7-170">Datuak esportatzeko programatutako freskapenaren zain egon gabe, joan hona: **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-170">To export data without waiting for a scheduled refresh, go to **Data** > **Exports**.</span></span>

- <span data-ttu-id="f0cc7-171">Esportazio guztiak exekutatzeko, hautatu **Exekutatu guztiak** komando barran.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-171">To run all exports, select **Run all** in the command bar.</span></span> <span data-ttu-id="f0cc7-172">Ekintza honek antolaketa aktiboa duten esportazioak soilik exekutatuko ditu.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-172">This action will only run exports that have an active schedule.</span></span>
- <span data-ttu-id="f0cc7-173">Esportazio bakarra exekutatzeko, hautatu zerrendatik eta hautatu **Exekutatu** komando barran.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-173">To run a single export, select it in the list and select **Run** in the command bar.</span></span> <span data-ttu-id="f0cc7-174">Horrela exekutatzen dira antolaketa aktiborik gabeko esportazioak.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-174">That's how you run exports with no active schedule.</span></span> 

## <a name="remove-an-export"></a><span data-ttu-id="f0cc7-175">Ezabatu Esportatu</span><span class="sxs-lookup"><span data-stu-id="f0cc7-175">Remove an Export</span></span>

1. <span data-ttu-id="f0cc7-176">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-176">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="f0cc7-177">Hautatu kendu nahi duzun esportazioa.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-177">Select the export you want to remove.</span></span>

1. <span data-ttu-id="f0cc7-178">Komando-barran, sakatu **Kendu**.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-178">Select **Remove** in the command bar.</span></span>

1. <span data-ttu-id="f0cc7-179">Baieztatu kentzea aukeratuz **Kendu** berrespen-pantailan.</span><span class="sxs-lookup"><span data-stu-id="f0cc7-179">Confirm the removal by selecting **Remove** on the confirmation screen.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
