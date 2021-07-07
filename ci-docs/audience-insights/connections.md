---
title: Customer Insights-etik beste zerbitzu batzuetarako konexioak.
description: Partekatu datuak beste zerbitzu batzuekin.
ms.date: 04/09/2021
ms.reviewer: nikeller
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 17e04b243e9b3d4375c86f5a890a18be35956835
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304957"
---
# <a name="connections-preview-overview"></a><span data-ttu-id="8231a-103">Konexioen ikuspegi orokorra (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="8231a-103">Connections (preview) overview</span></span>

<span data-ttu-id="8231a-104">Konexioak dira Customer Insights-etik eta horretatik datuak partekatzea ahalbidetzeko gakoa.</span><span class="sxs-lookup"><span data-stu-id="8231a-104">Connections are the key to enable data sharing to and from Customer Insights.</span></span> <span data-ttu-id="8231a-105">Konexio bakoitzak zerbitzu jakin batekin datuak partekatzea ezartzen du.</span><span class="sxs-lookup"><span data-stu-id="8231a-105">Each connection establishes data sharing with a specific service.</span></span> <span data-ttu-id="8231a-106">Konexioak dira oinarria [konfiguratu hirugarrenen aberastasunak](enrichment-hub.md) eta [esportazioak konfiguratu](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="8231a-106">Connections are the foundation to [configure third-party enrichments](enrichment-hub.md) and [configure exports](export-destinations.md).</span></span> <span data-ttu-id="8231a-107">Konexio bera hainbat aldiz erabil daiteke.</span><span class="sxs-lookup"><span data-stu-id="8231a-107">The same connection can be used multiple times.</span></span> <span data-ttu-id="8231a-108">Adibidez, Dynamics 365 Marketing-erako konexio batek esportazio anitzetarako balio du eta Leadspace konexio bat aberastu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="8231a-108">For example, one connection to Dynamics 365 Marketing works for multiple exports and one Leadspace connection can be used for several enrichments.</span></span>

<span data-ttu-id="8231a-109">Joan **Administratzailea** > **Konexioak** konexioak sortzeko eta ikusteko.</span><span class="sxs-lookup"><span data-stu-id="8231a-109">Go to **Admin** > **Connections** to create and view connections.</span></span>

<span data-ttu-id="8231a-110">**Konexioak** fitxak konexio aktibo guztiak erakusten dizkizu.</span><span class="sxs-lookup"><span data-stu-id="8231a-110">The **Connections** tab shows you all active connections.</span></span> <span data-ttu-id="8231a-111">Zerrendan konexio bakoitzerako errenkada bat agertzen da.</span><span class="sxs-lookup"><span data-stu-id="8231a-111">The list shows a row for each connection.</span></span> 

<span data-ttu-id="8231a-112">Lortu ikuspegi orokorra, deskribapena eta jakin zer egin dezakezun **Ezagutu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="8231a-112">Get a quick overview, description, and find out what you can do with each extensibility option on the **Discover** tab.</span></span>

### <a name="exports"></a><span data-ttu-id="8231a-113">Esportazioak</span><span class="sxs-lookup"><span data-stu-id="8231a-113">Exports</span></span>

<span data-ttu-id="8231a-114">Administratzaileek soilik konfigura ditzakete konexio berriak, baina laguntzaileei sarbidea eman diezaiekete lehendik dauden konexioak erabiltzeko.</span><span class="sxs-lookup"><span data-stu-id="8231a-114">Only administrators can configure new connections but they can grant access to contributors to use existing connections.</span></span> <span data-ttu-id="8231a-115">Administratzaileek datuak nora joan daitezkeen kontrolatzen dute, laguntzaileek beren beharretara egokitzen duten karga eta maiztasuna definitzen dute.</span><span class="sxs-lookup"><span data-stu-id="8231a-115">Administrators control where data can go, contributors define the payload and frequency fitting their needs.</span></span> <span data-ttu-id="8231a-116">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="8231a-116">For more information, see [Allow contributors to use a connection for exports](#allow-contributors-to-use-a-connection-for-exports).</span></span>

### <a name="enrichments"></a><span data-ttu-id="8231a-117">Aberasteak</span><span class="sxs-lookup"><span data-stu-id="8231a-117">Enrichments</span></span>

<span data-ttu-id="8231a-118">Administratzaileek soilik konfigura ditzakete konexio berriak, baina sortutako konexioak beti daude eskuragarri administratzaile zein laguntzaileentzat.</span><span class="sxs-lookup"><span data-stu-id="8231a-118">Only administrators can configure new connections but the created connections are always available to both administrators and contributors.</span></span> <span data-ttu-id="8231a-119">Administratzaileek egiaztagiriak kudeatzen dituzte eta datuen transferentziei baimena ematen diete.</span><span class="sxs-lookup"><span data-stu-id="8231a-119">Administrators manage credentials and give consent to data transfers.</span></span> <span data-ttu-id="8231a-120">Konexioak administratzaileek eta laguntzaileek aberasteko erabil ditzakete.</span><span class="sxs-lookup"><span data-stu-id="8231a-120">The connections can then be used for enrichments by both administrators and contributors.</span></span>

## <a name="add-a-new-connection"></a><span data-ttu-id="8231a-121">Gehitu konexio bat</span><span class="sxs-lookup"><span data-stu-id="8231a-121">Add a new connection</span></span>

<span data-ttu-id="8231a-122">Konexioak gehitzeko, eduki behar duzu [administratzaile baimenak](permissions.md).</span><span class="sxs-lookup"><span data-stu-id="8231a-122">To add connections, you need to have [administrator permissions](permissions.md).</span></span> <span data-ttu-id="8231a-123">Beste Microsoft zerbitzu batzuekin konektatzen bazara, bi zerbitzuak erakunde berean daudela suposatuko dugu.</span><span class="sxs-lookup"><span data-stu-id="8231a-123">If you connect to other Microsoft services, we assume both services are in the same organization.</span></span>

1. <span data-ttu-id="8231a-124">Joan **Administratzailea** > **Konexioak (aurrebista)**.</span><span class="sxs-lookup"><span data-stu-id="8231a-124">Go to **Admin** > **Connections (preview)**.</span></span>

1. <span data-ttu-id="8231a-125">Joan **Konexioak** fitxara.</span><span class="sxs-lookup"><span data-stu-id="8231a-125">Go to the **Connections** tab.</span></span>

1. <span data-ttu-id="8231a-126">Hautatu **Gehitu konexioa** konexio berri bat sortzeko.</span><span class="sxs-lookup"><span data-stu-id="8231a-126">Select **Add connection** to create a new connection.</span></span> <span data-ttu-id="8231a-127">Aukeratu goitibeherako menuan zein konexio mota sortu nahi duzun.</span><span class="sxs-lookup"><span data-stu-id="8231a-127">Choose from the dropdown menu what type of connection you want to create.</span></span>

1. <span data-ttu-id="8231a-128">Hurrengoan **Konfiguratu konexioa** panelean, eman beharrezko xehetasunak.</span><span class="sxs-lookup"><span data-stu-id="8231a-128">In the **Set up connection** pane, provide the required details.</span></span> 
   1. <span data-ttu-id="8231a-129">**Bistaratzeko izena** eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="8231a-129">The **Display name** and the type of the connection describe a connection.</span></span> <span data-ttu-id="8231a-130">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="8231a-130">We recommend choosing a name that explains the purpose and target of this connection.</span></span>
   1. <span data-ttu-id="8231a-131">Eremu zehatzak zein zerbitzuetara konektatzen zaren araberakoak dira.</span><span class="sxs-lookup"><span data-stu-id="8231a-131">The exact fields depend on what service you are connecting to.</span></span> <span data-ttu-id="8231a-132">Konexio mota zehatz baten xehetasunak ezagutu ditzakezu xede zerbitzuaren inguruko artikulua.</span><span class="sxs-lookup"><span data-stu-id="8231a-132">You can learn about details of a specific connection type in the article about the target service.</span></span>

1. <span data-ttu-id="8231a-133">Konexioa sortzeko, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="8231a-133">To create the connection, select **Save**.</span></span>

<span data-ttu-id="8231a-134">Aukeratu ere egin dezakezu **Konfiguratu** teila batean **Ezagutu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="8231a-134">You can also select **Set up** on a tile on the **Discover** tab.</span></span>

### <a name="allow-contributors-to-use-a-connection-for-exports"></a><span data-ttu-id="8231a-135">Baimendu laguntzaileei esportazioetarako konexioa erabiltzea</span><span class="sxs-lookup"><span data-stu-id="8231a-135">Allow contributors to use a connection for exports</span></span>

<span data-ttu-id="8231a-136">Esportazio konexioa konfiguratu edo editatzerakoan, aukeratzen duzu zein erabiltzaile konexio zehatz hau erabili ahal izateko definitzeko [esportazioak](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="8231a-136">When setting up or editing an export connection, you choose which users are allowed to use this specific connection to define [exports](export-destinations.md).</span></span> <span data-ttu-id="8231a-137">Berez, konexioa erabilgarri dago administratzaile funtzioa duten erabiltzaileentzat.</span><span class="sxs-lookup"><span data-stu-id="8231a-137">By default a connection is available to users with an administrator role.</span></span> <span data-ttu-id="8231a-138">Ezarpen hau alda dezakezu **Aukeratu nork erabil dezakeen konexio hau** eta lagundu laguntzaile rolak dituzten erabiltzaileei konexio hau erabiltzeko.</span><span class="sxs-lookup"><span data-stu-id="8231a-138">You can change this setting under **Choose who can use this connection** and allow users with contributor role to use this connection.</span></span>

- <span data-ttu-id="8231a-139">Laguntzaileek ezin izango dute konexioa ikusi edo editatu.</span><span class="sxs-lookup"><span data-stu-id="8231a-139">Contributors won't be able to view or edit the connection.</span></span> <span data-ttu-id="8231a-140">Bistaratzeko izena eta mota esportazio bat sortzerakoan soilik ikusiko dute.</span><span class="sxs-lookup"><span data-stu-id="8231a-140">They will only see the display name and its type when creating an export.</span></span>
- <span data-ttu-id="8231a-141">Konexioa partekatuz gero, laguntzaileei konexioa erabiltzeko baimena ematen diezu.</span><span class="sxs-lookup"><span data-stu-id="8231a-141">By sharing a connection, you allow contributors to use a connection.</span></span> <span data-ttu-id="8231a-142">Laguntzaileek partekatutako konexioak ikusiko dituzte esportazioak konfiguratzen dituztenean.</span><span class="sxs-lookup"><span data-stu-id="8231a-142">Contributors will see shared connections when they set up exports.</span></span> <span data-ttu-id="8231a-143">Konexio zehatz hau erabiltzen duten esportazio guztiak kudea ditzakete.</span><span class="sxs-lookup"><span data-stu-id="8231a-143">They can manage every export that uses this specific connection.</span></span>
- <span data-ttu-id="8231a-144">Ezarpen hau alda dezakezu laguntzaileek definitutako esportazioak mantenduz.</span><span class="sxs-lookup"><span data-stu-id="8231a-144">You can change this setting while keeping the exports that have already been defined by contributors.</span></span>

## <a name="edit-a-connection"></a><span data-ttu-id="8231a-145">Editatu konexio bat</span><span class="sxs-lookup"><span data-stu-id="8231a-145">Edit a connection</span></span>

1. <span data-ttu-id="8231a-146">Joan **Administratzailea** > **Konexioak (aurrebista)**.</span><span class="sxs-lookup"><span data-stu-id="8231a-146">Go to **Admin** > **Connections (preview)**.</span></span>

1. <span data-ttu-id="8231a-147">Joan **Konexioak** fitxara.</span><span class="sxs-lookup"><span data-stu-id="8231a-147">Go to the **Connections** tab.</span></span>

1. <span data-ttu-id="8231a-148">Hautatu elipsi bertikala editatu nahi duzun konexiorako.</span><span class="sxs-lookup"><span data-stu-id="8231a-148">Select the vertical ellipsis for the connection you want to edit.</span></span>

1. <span data-ttu-id="8231a-149">Hautatu **Editatu**.</span><span class="sxs-lookup"><span data-stu-id="8231a-149">Select **Edit**.</span></span>

1. <span data-ttu-id="8231a-150">Aldatu eguneratu nahi dituzun balioak eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="8231a-150">Change the values you want to update and select **Save**.</span></span>

## <a name="remove-a-connection"></a><span data-ttu-id="8231a-151">Konexioa kendu nahi duzu</span><span class="sxs-lookup"><span data-stu-id="8231a-151">Remove a connection</span></span>

<span data-ttu-id="8231a-152">Kentzen ari zaren konexioa aberastasunek edo esportazioek erabiltzen badute, lehenengo deskonektatu edo kendu behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="8231a-152">If the connection you are removing is used by enrichments or exports, you first need to detach or remove them.</span></span> <span data-ttu-id="8231a-153">Kendu elkarrizketa-koadroak aberastasun edo esportazio garrantzitsuetara eramango zaitu.</span><span class="sxs-lookup"><span data-stu-id="8231a-153">The remove dialog will guide you to the relevant enrichments or exports.</span></span> 

<span data-ttu-id="8231a-154">Bereizitako aberastasunak eta esportazioak inaktibo bihurtzen dira.</span><span class="sxs-lookup"><span data-stu-id="8231a-154">Detached enrichments and exports become inactive.</span></span> <span data-ttu-id="8231a-155">Berriro aktibatuko dituzu haiekin beste konexio bat gehituz [Aberastasunak](enrichment-hub.md) edo [Esportazioak](export-destinations.md) orrialdea.</span><span class="sxs-lookup"><span data-stu-id="8231a-155">You reactivate them by adding another connection to them on the [Enrichments](enrichment-hub.md) or [Exports](export-destinations.md) page.</span></span>

1. <span data-ttu-id="8231a-156">Joan **Administratzailea** > **Konexioak (aurrebista)**.</span><span class="sxs-lookup"><span data-stu-id="8231a-156">Go to **Admin** > **Connections (preview)**.</span></span>

1. <span data-ttu-id="8231a-157">Joan **Konexioak** fitxara.</span><span class="sxs-lookup"><span data-stu-id="8231a-157">Go to the **Connections** tab.</span></span>

1. <span data-ttu-id="8231a-158">Hautatu elipsi bertikala kendu nahi duzun konexiorako.</span><span class="sxs-lookup"><span data-stu-id="8231a-158">Select the vertical ellipsis for the connection you want to remove.</span></span>

1. <span data-ttu-id="8231a-159">Hautatu **Kendu** goitibeherako menuan.</span><span class="sxs-lookup"><span data-stu-id="8231a-159">Select **Remove** from the dropdown menu.</span></span> <span data-ttu-id="8231a-160">Berresteko elkarrizketa agertzen da.</span><span class="sxs-lookup"><span data-stu-id="8231a-160">A confirmation dialog appears.</span></span>

   1. <span data-ttu-id="8231a-161">Konexio hau erabiltzen duten aberastasunak edo esportazioak badaude, hautatu botoia konexioa erabiltzen ari dena ikusteko.</span><span class="sxs-lookup"><span data-stu-id="8231a-161">If there are enrichments or exports using this connection, select the button to see what's using the connection.</span></span>
      - <span data-ttu-id="8231a-162">**Esportazioak:** Konexioa kendu ahal izateko esportazioak kentzea edo deskonektatzea aukera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="8231a-162">**Exports:** You can choose to either remove or disconnect the exports to be able to remove the connection.</span></span> <span data-ttu-id="8231a-163">Esportazio bat deskonektatzeko, administratzaileek **Deskonektatu** ekintza.</span><span class="sxs-lookup"><span data-stu-id="8231a-163">To disconnect an export, administrators can use the **Disconnect** action.</span></span> <span data-ttu-id="8231a-164">Ekintza hau eskuragarri dago banakako eta hautatutako esportazio anitzetarako.</span><span class="sxs-lookup"><span data-stu-id="8231a-164">This action is available for individual and multiple selected exports.</span></span> <span data-ttu-id="8231a-165">Deskonektatuta esportazio konfigurazioa mantenduko duzu, baina ez da exekutatuko beste konexio bat gehitu arte.</span><span class="sxs-lookup"><span data-stu-id="8231a-165">By disconnecting you keep the export config, but it won't be run until another connection is added to it.</span></span>
      - <span data-ttu-id="8231a-166">**Aberasteak:** Konexioa kendu ahal izateko aberasteak desaktibatzea edo kentzea aukera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="8231a-166">**Enrichments:** You can choose to either remove or deactivate the enrichments to be able to remove the connection.</span></span> 
   1. <span data-ttu-id="8231a-167">Konexioak mendekotasun gehiago ez duenean, itzuli berriro **Administratzailea** > **Konexioak** eta saiatu berriro konexioa kentzen.</span><span class="sxs-lookup"><span data-stu-id="8231a-167">Once the connection has no more dependencies, go back to **Admin** > **Connections** and try removing the connection again.</span></span>

1. <span data-ttu-id="8231a-168">Ezabapena berresteko hautatu **Kendu**.</span><span class="sxs-lookup"><span data-stu-id="8231a-168">To confirm the deletion, select **Remove**.</span></span>

