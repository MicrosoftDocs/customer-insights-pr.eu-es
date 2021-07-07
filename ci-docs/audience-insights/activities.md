---
title: Bezeroen jarduerak
description: Definitu bezeroen jarduerak eta ikusi bezeroaren kronologian.
ms.date: 04/07/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: MichelleDevaney
ms.author: midevane
manager: shellyha
ms.openlocfilehash: 342aeb33f652d5d60cd25e13969766954bf56370
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304911"
---
# <a name="customer-activities"></a><span data-ttu-id="a65cc-103">Bezeroen jarduerak</span><span class="sxs-lookup"><span data-stu-id="a65cc-103">Customer activities</span></span>

<span data-ttu-id="a65cc-104">Konbinatu bezeroaren jarduerak [hainbat datu iturri](data-sources.md) hurrengoan Dynamics 365 Customer Insights jarduerak kronologikoki zerrendatuko dituen kronograma sortzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-104">Combine customer activities from [various data sources](data-sources.md) in Dynamics 365 Customer Insights to create a timeline that lists the activities chronologically.</span></span> <span data-ttu-id="a65cc-105">Sartu kronograma Dynamics 365 aplikazioetan [Bezero txartelaren gehigarria](customer-card-add-in.md) irtenbide batean edo Power BI arbela.</span><span class="sxs-lookup"><span data-stu-id="a65cc-105">Include the timeline in Dynamics 365 apps with the [Customer Card add-in](customer-card-add-in.md) solution, or in a Power BI dashboard.</span></span>

## <a name="define-an-activity"></a><span data-ttu-id="a65cc-106">Definitu jarduera</span><span class="sxs-lookup"><span data-stu-id="a65cc-106">Define an activity</span></span>

<span data-ttu-id="a65cc-107">Zure datu-iturriak datu-iturri ugarietatik transakzio- eta jarduera-datuak izan ditzaketen entitateak dira.</span><span class="sxs-lookup"><span data-stu-id="a65cc-107">Your data sources can include entities with transactional and activity data from multiple data sources.</span></span> <span data-ttu-id="a65cc-108">Identifika itzazu entitate horiek eta hautatu bezeroaren denbora-lerroan ikusi nahi dituzun jarduerak.</span><span class="sxs-lookup"><span data-stu-id="a65cc-108">Identify these entities and select the activities you want to view on the customer's timeline.</span></span> <span data-ttu-id="a65cc-109">Aukeratu zure xede-jarduera edo jarduerak biltzen dituen entitatea.</span><span class="sxs-lookup"><span data-stu-id="a65cc-109">Choose the entity that includes your target activity or activities.</span></span>

> [!NOTE]
> <span data-ttu-id="a65cc-110">Entitate batek gutxienez motako atributu bat izan behar du **Data** bezeroaren denbora-lerroan sartzeko eta ezin dituzu entitateak gehitu gabe **data** eremuak.</span><span class="sxs-lookup"><span data-stu-id="a65cc-110">An entity must have at least one attribute of type **Date** to be included in a customer timeline and you can't add entities without **Date** fields.</span></span> <span data-ttu-id="a65cc-111">The **Gehitu jarduera** kontrola ezgaitzen da horrelako entitate bat aurkitzen ez bada.</span><span class="sxs-lookup"><span data-stu-id="a65cc-111">The **Add activity** control is disabled if no such entity is found.</span></span>

1. <span data-ttu-id="a65cc-112">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.</span><span class="sxs-lookup"><span data-stu-id="a65cc-112">In audience insights, go to **Data** > **Activities**.</span></span>

1. <span data-ttu-id="a65cc-113">Aukeratu **Gehitu jarduera** jarduera konfiguratzeko prozesuaren esperientzia gidatua hasteko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-113">Select **Add activity** to start the guided experience for the activity setup process.</span></span>

1. <span data-ttu-id="a65cc-114">Hurrengoan **Jardueren datuak** urratsa, ezarri eremu hauetako balioak:</span><span class="sxs-lookup"><span data-stu-id="a65cc-114">In the **Activity data** step, set the values for the following fields:</span></span>

   - <span data-ttu-id="a65cc-115">**Jardueraren izena**: Hautatu zure jarduerarako izen bat.</span><span class="sxs-lookup"><span data-stu-id="a65cc-115">**Activity name**: Select a name for your activity.</span></span>
   - <span data-ttu-id="a65cc-116">**Erakunde**: Aukeratu transakzio- edo jarduera-datuak biltzen dituen entitatea.</span><span class="sxs-lookup"><span data-stu-id="a65cc-116">**Entity**: Select an entity that includes transactional or activity data.</span></span>
   - <span data-ttu-id="a65cc-117">**Gako nagusia**: Hautatu erregistroa era esklusiboan identifikatzen duen eremua.</span><span class="sxs-lookup"><span data-stu-id="a65cc-117">**Primary key**: Select the field that uniquely identifies a record.</span></span> <span data-ttu-id="a65cc-118">Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.</span><span class="sxs-lookup"><span data-stu-id="a65cc-118">It shouldn't contain any duplicate values, empty values, or missing values.</span></span>

   :::image type="content" source="media/Activity_Wizard1.PNG" alt-text="Konfiguratu jardueraren datuak izena, entitatea eta gako nagusiarekin.":::

1. <span data-ttu-id="a65cc-120">Aukeratu **Hurrengoa** hurrengo urratsera joateko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-120">Select **Next** to go to the next step.</span></span>

1. <span data-ttu-id="a65cc-121">Hurrengoan **Harremana** Urratsa, konfiguratu xehetasunak zure jarduerak datuak dagokion bezeroarekin konektatzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-121">In the **Relationship** step, configure the details to connect your activity data to its corresponding customer.</span></span> <span data-ttu-id="a65cc-122">Urrats honek entitateen arteko konexioa bistaratzen du.</span><span class="sxs-lookup"><span data-stu-id="a65cc-122">This step visualizes the connection between entities.</span></span>  

   - <span data-ttu-id="a65cc-123">**Lehenengoa**: Zure jarduera entitatean atzerriko eremua, beste entitate batekin harremanak sortzeko erabiliko dena.</span><span class="sxs-lookup"><span data-stu-id="a65cc-123">**First**: Foreign field in your activity entity that will be used to establish a relationship with another entity.</span></span>
   - <span data-ttu-id="a65cc-124">**Bigarrena**: Zure jarduera entitatearekin erlazionatuko duen iturburu bezeroari dagokiona.</span><span class="sxs-lookup"><span data-stu-id="a65cc-124">**Second**: Corresponding source customer entity with which your activity entity will be in relationship.</span></span> <span data-ttu-id="a65cc-125">Datuak bateratzeko prozesuan erabiltzen diren iturburu bezeroen entitateekin bakarrik lotu zaitezke.</span><span class="sxs-lookup"><span data-stu-id="a65cc-125">You can only relate to source customer entities that are used in the data unification process.</span></span>
   - <span data-ttu-id="a65cc-126">**Hirugarrena**: Jarduera entitate honen eta hautatutako iturburu bezero entitatearen arteko erlazioa badago jadanik, harremanaren izena irakurtzeko soilik moduan egongo da.</span><span class="sxs-lookup"><span data-stu-id="a65cc-126">**Third**: If a relationship between this activity entity and the selected source customer entity already exists, the relationship name will be in read-only mode.</span></span> <span data-ttu-id="a65cc-127">Harreman hori existitzen ez bada, harreman berri bat sortuko da koadro honetan ematen duzun izenarekin.</span><span class="sxs-lookup"><span data-stu-id="a65cc-127">If no such relationship exists, a new relationship will be created with the name you provide in this box.</span></span>

   :::image type="content" source="media/Activity_Wizard2.PNG" alt-text="Definitu entitate-harremana.":::

1. <span data-ttu-id="a65cc-129">Aukeratu **Hurrengoa** hurrengo urratsera joateko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-129">Select **Next** to go to the next step.</span></span> 

1. <span data-ttu-id="a65cc-130">Hurrengoan **Jarduera bateratzea** urratsa, aukeratu jarduera gertaera eta zure jardueraren hasiera ordua.</span><span class="sxs-lookup"><span data-stu-id="a65cc-130">In the **Activity unification** step, choose the activity event and the start time of your activity.</span></span> 
   - <span data-ttu-id="a65cc-131">**Beharrezko eremuak**</span><span class="sxs-lookup"><span data-stu-id="a65cc-131">**Required fields**</span></span>
      - <span data-ttu-id="a65cc-132">**Ekitaldi jarduera**: Jarduera honen gertaera den eremua.</span><span class="sxs-lookup"><span data-stu-id="a65cc-132">**Event activity**: Field that is the event for this activity.</span></span>
      - <span data-ttu-id="a65cc-133">**Denbora-marka**: Zure jardueraren hasiera ordua adierazten duen eremua.</span><span class="sxs-lookup"><span data-stu-id="a65cc-133">**Timestamp**: Field that represents the start time of your activity.</span></span>

   - <span data-ttu-id="a65cc-134">**Aukerako eremuak**</span><span class="sxs-lookup"><span data-stu-id="a65cc-134">**Optional fields**</span></span>
      - <span data-ttu-id="a65cc-135">**Xehetasun osagarria**: Jarduera honetarako informazio garrantzitsua duen eremua.</span><span class="sxs-lookup"><span data-stu-id="a65cc-135">**Additional detail**: Field with relevant information for this activity.</span></span>
      - <span data-ttu-id="a65cc-136">**Ikonoa**: Jarduera mota hau ondoen irudikatzen duen ikonoa.</span><span class="sxs-lookup"><span data-stu-id="a65cc-136">**Icon**: Icon that best represents this activity type.</span></span>
      - <span data-ttu-id="a65cc-137">**Web-helbidea**: Jarduera honi buruzko informazioa duen URLa duen eremua.</span><span class="sxs-lookup"><span data-stu-id="a65cc-137">**Web address**: Field containing a URL with information about this activity.</span></span> <span data-ttu-id="a65cc-138">Adibidez, jarduera hau iturri duen transakzio-sistema.</span><span class="sxs-lookup"><span data-stu-id="a65cc-138">For example, the transactional system that sources this activity.</span></span> <span data-ttu-id="a65cc-139">URL hau datu-iturburu-eko edozein eremu izan daiteke edo Power Query eraldaketa erabiliz eremu berri gisa eraiki daiteke.</span><span class="sxs-lookup"><span data-stu-id="a65cc-139">This URL can be any field from the data source, or it can be constructed as a new field using a Power Query transformation.</span></span> <span data-ttu-id="a65cc-140">URL datuak fitxategian gordeko dira *Jarduera bateratua* entitatea, erabilita ibaian behera kontsumitu daitekeena [APIak](apis.md).</span><span class="sxs-lookup"><span data-stu-id="a65cc-140">The URL data will be stored in the *Unified Activity* entity, which can be consumed downstream using [APIs](apis.md).</span></span>
   
   :::image type="content" source="media/Activity_Wizard3.PNG" alt-text="Zehaztu bezeroaren jardueraren datuak Jarduera bateratuko entitate batean.":::

1. <span data-ttu-id="a65cc-142">Hautatu **Hurrengoa** hurrengo urratsera mugitzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-142">Select **Next** to move to the next step.</span></span> <span data-ttu-id="a65cc-143">Aukeratu dezakezu **Amaitu eta berrikusi** aktibitatea orain gordetzeko, jarduera mota gisa ezarrita **Beste batzuk**.</span><span class="sxs-lookup"><span data-stu-id="a65cc-143">You can select **Finish and review** to save the activity now with the activity type set to **Other**.</span></span> 

1. <span data-ttu-id="a65cc-144">Hurrengoan **Jarduera mota** urratsa, aukeratu jarduera mota eta hautatu aukeran Customer Insights beste arlo batzuetan erabiltzeko jarduera mota batzuk semantikoki mapatu nahi dituzun.</span><span class="sxs-lookup"><span data-stu-id="a65cc-144">In the **Activity Type** step, choose the activity type and optionally select if you want to semantically map some of the activity types for use in other areas of Customer Insights.</span></span> <span data-ttu-id="a65cc-145">Gaur egun, *Harpidetza* eta *SalesOrderLine* jarduera motak semantikoki mapatu daitezke eremuak mapatzea adostu ondoren.</span><span class="sxs-lookup"><span data-stu-id="a65cc-145">Currently, *Subscription* and *SalesOrderLine* activity types can be semantically mapped after agreeing to map the fields.</span></span> <span data-ttu-id="a65cc-146">Jarduera mota bat jarduera berrirako garrantzitsua ez bada, hauta dezakezu *Beste batzuk* edo *Sortu berria* jarduera mota pertsonalizatua lortzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-146">If an activity type isn't relevant for the new activity, you can choose *Other* or *Create new* for a custom activity type.</span></span>

1. <span data-ttu-id="a65cc-147">Hautatu **Hurrengoa** hurrengo urratsera mugitzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-147">Select **Next** to move to the next step.</span></span> 

1. <span data-ttu-id="a65cc-148">Hurrengoan **Berrikuspena** urratsa, egiaztatu hautapenak.</span><span class="sxs-lookup"><span data-stu-id="a65cc-148">In the **Review** step, verify your selections.</span></span> <span data-ttu-id="a65cc-149">Itzuli aurreko edozein urratsetara eta eguneratu informazioa beharrezkoa bada.</span><span class="sxs-lookup"><span data-stu-id="a65cc-149">Go back to any of the previous steps and update the information if necessary.</span></span>

   :::image type="content" source="media/Activity_Wizard5.PNG" alt-text="Berrikusi jarduera baterako zehaztutako eremuak.":::
   
1. <span data-ttu-id="a65cc-151">Aukeratu **Gorde jarduera** aldaketak aplikatzeko eta hautatu **Eginda** atzera joateko **Datuak** > **Jarduerak**.</span><span class="sxs-lookup"><span data-stu-id="a65cc-151">Select **Save activity** to apply your changes and select **Done** to go back to **Data** > **Activities**.</span></span> <span data-ttu-id="a65cc-152">Hemen ikus ditzakezu zein jarduera erakutsiko diren kronograman.</span><span class="sxs-lookup"><span data-stu-id="a65cc-152">Here you see which activities are set to show in the timeline.</span></span> 

1. <span data-ttu-id="a65cc-153">Gainean **Jarduerak** orrialdea, hautatu **Korrika egin** jarduera prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-153">On the **Activities** page, select **Run** to process the activity.</span></span> 

> [!TIP]
> <span data-ttu-id="a65cc-154">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="a65cc-154">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="a65cc-155">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="a65cc-155">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="a65cc-156">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-156">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="a65cc-157">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="a65cc-157">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>


## <a name="manage-existing-activities"></a><span data-ttu-id="a65cc-158">Kudeatu lehendik dauden jarduerak</span><span class="sxs-lookup"><span data-stu-id="a65cc-158">Manage existing activities</span></span>

<span data-ttu-id="a65cc-159">Aktibatuta **Datuak** > **Jarduerak**, gordetako jarduera guztiak ikusi eta kudeatu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="a65cc-159">On **Data** > **Activities**, you can view all your saved activities, and manage them.</span></span> <span data-ttu-id="a65cc-160">Jarduera bakoitza iturriari, entitateari eta jarduera motari buruzko xehetasunak ere biltzen dituen errenkada baten bidez irudikatzen da.</span><span class="sxs-lookup"><span data-stu-id="a65cc-160">Each activity is represented by a row that also includes details about the source, the entity, and the activity type.</span></span>

<span data-ttu-id="a65cc-161">Jarduera bat hautatzean ekintza hauek erabilgarri daude.</span><span class="sxs-lookup"><span data-stu-id="a65cc-161">The following actions are available when you select an activity.</span></span> 

- <span data-ttu-id="a65cc-162">**Editatu**: Berrikuspen urratsean jarduera konfigurazioa irekitzen du.</span><span class="sxs-lookup"><span data-stu-id="a65cc-162">**Edit**: Opens the activity setup on the review step.</span></span> <span data-ttu-id="a65cc-163">Urrats honetatik uneko konfigurazioaren zati bat edo guztia alda dezakezu.</span><span class="sxs-lookup"><span data-stu-id="a65cc-163">You can change any or all of the current configuration from this step.</span></span> <span data-ttu-id="a65cc-164">Konfigurazioa aldatu ondoren, hautatu **Gorde jarduera** eta, ondoren, hautatu **Korrika egin** aldaketak prozesatzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-164">After changing the configuration, select **Save activity** and then select **Run** to process the changes.</span></span>

- <span data-ttu-id="a65cc-165">**Aldatu izena**: Elkarrizketa-koadro bat irekitzen du eta bertan hautatutako jardueraren beste izen bat sar dezakezu.</span><span class="sxs-lookup"><span data-stu-id="a65cc-165">**Rename**: Opens a dialog where you can enter a different name for the selected activity.</span></span> <span data-ttu-id="a65cc-166">Aldaketak aplikatzeko, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="a65cc-166">Select **Save** to apply your changes.</span></span>

- <span data-ttu-id="a65cc-167">**Ezabatu**: Elkarrizketa bat irekitzen du hautatutako jardueraren ezabaketa berresteko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-167">**Delete**: Opens a dialog to confirm the deletion of the selected activity.</span></span> <span data-ttu-id="a65cc-168">Jarduera bat baino gehiago aldi berean ezaba ditzakezu jarduerak hautatuta eta gero ezabatzeko ikonoa hautatuta.</span><span class="sxs-lookup"><span data-stu-id="a65cc-168">You can also delete more than one activity at once by selecting the activities and then selecting the delete icon.</span></span> <span data-ttu-id="a65cc-169">Hautatu **Ezabatu** ezabatzea baieztatzeko.</span><span class="sxs-lookup"><span data-stu-id="a65cc-169">Select **Delete** to confirm the deletion.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
