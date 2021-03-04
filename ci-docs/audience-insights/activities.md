---
title: Bezeroen jarduerak
description: Definitu bezeroen jarduerak eta ikusi bezeroaren kronologian.
ms.date: 10/13/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.reviewer: adkuppa
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: dcef8f0547009e1488f1abe91423fa0bf5b061de
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267417"
---
# <a name="customer-activities"></a><span data-ttu-id="28338-103">Bezeroen jarduerak</span><span class="sxs-lookup"><span data-stu-id="28338-103">Customer activities</span></span>

<span data-ttu-id="28338-104">Konbinatu Dynamics 365 Customer Insights-eko [hainbat datu-iturburutako](data-sources.md) bezeroen jarduerak, jarduerak ordena kronologikoan zerrendatuko dituen bezeroen kronologia sortzeko.</span><span class="sxs-lookup"><span data-stu-id="28338-104">Combine customer activities from [various data sources](data-sources.md) in Dynamics 365 Customer Insights to create a customer timeline that lists the activities in chronological order.</span></span> <span data-ttu-id="28338-105">Kronika customer engagement aplikazioetan sar dezakezu Dynamics 365 aplikazioan [Bezero Txartelaren gehigarria](customer-card-add-in.md), edo a Power BI Arbel.</span><span class="sxs-lookup"><span data-stu-id="28338-105">You can include the timeline in customer engagement apps in Dynamics 365 via the [Customer Card add-in](customer-card-add-in.md), or in a Power BI dashboard.</span></span>

## <a name="define-an-activity"></a><span data-ttu-id="28338-106">Definitu jarduera</span><span class="sxs-lookup"><span data-stu-id="28338-106">Define an activity</span></span>

<span data-ttu-id="28338-107">Zure datu-iturriak datu-iturri ugarietatik transakzio- eta jarduera-datuak dituzten entitateak dira.</span><span class="sxs-lookup"><span data-stu-id="28338-107">Your data sources include entities with transactional and activity data from multiple data sources.</span></span> <span data-ttu-id="28338-108">Identifika itzazu entitate horiek eta hautatu bezeroaren denbora-lerroan ikusi nahi dituzun jarduerak.</span><span class="sxs-lookup"><span data-stu-id="28338-108">Identify these entities and select the activities you want to view on the customer's timeline.</span></span> <span data-ttu-id="28338-109">Aukeratu zure xede-jarduera edo jarduerak biltzen dituen entitatea.</span><span class="sxs-lookup"><span data-stu-id="28338-109">Choose the entity that includes your target activity or activities.</span></span>

1. <span data-ttu-id="28338-110">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.</span><span class="sxs-lookup"><span data-stu-id="28338-110">In audience insights, go to **Data** > **Activities**.</span></span>

1. <span data-ttu-id="28338-111">Hautatu **Gehitu jarduera**.</span><span class="sxs-lookup"><span data-stu-id="28338-111">Select **Add activity**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="28338-112">Entitate batek gutxienez motako atributu bat izan behar du **Data** bezeroaren denbora-lerroan sartzeko eta ezin dituzu entitateak gehitu gabe **data** eremuak.</span><span class="sxs-lookup"><span data-stu-id="28338-112">An entity must have at least one attribute of type **Date** to be included in a customer timeline and you can't add entities without **Date** fields.</span></span> <span data-ttu-id="28338-113">The **Gehitu jarduera** kontrola ezgaitzen da horrelako entitate bat aurkitzen ez bada.</span><span class="sxs-lookup"><span data-stu-id="28338-113">The **Add activity** control is disabled if no such entity is found.</span></span>

1. <span data-ttu-id="28338-114">Sarbidean **Gehitu jarduera** panela, ezarri hurrengo eremuetarako balioak:</span><span class="sxs-lookup"><span data-stu-id="28338-114">In the **Add activity** pane, set the values for the following fields:</span></span>

   - <span data-ttu-id="28338-115">**Erakunde**: Aukeratu transakzio- edo jarduera-datuak biltzen dituen entitatea.</span><span class="sxs-lookup"><span data-stu-id="28338-115">**Entity**: Select an entity that includes transactional or activity data.</span></span>
   - <span data-ttu-id="28338-116">**Gako nagusia**: Hautatu erregistroa era esklusiboan identifikatzen duen eremua.</span><span class="sxs-lookup"><span data-stu-id="28338-116">**Primary key**: Select the field that uniquely identifies a record.</span></span> <span data-ttu-id="28338-117">Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.</span><span class="sxs-lookup"><span data-stu-id="28338-117">It shouldn't contain any duplicate values, empty values, or missing values.</span></span>
   - <span data-ttu-id="28338-118">**Denbora-zigilua**: Aukeratu zure jardueraren hasiera ordua adierazten duen eremua.</span><span class="sxs-lookup"><span data-stu-id="28338-118">**Timestamp**: Select the field that represents the start time of your activity.</span></span>
   - <span data-ttu-id="28338-119">**Gertaera**: Aukeratu jardueraren gertaera den eremua.</span><span class="sxs-lookup"><span data-stu-id="28338-119">**Event**: Select the field that is the event for the activity.</span></span>
   - <span data-ttu-id="28338-120">**Web helbidea**: Aukeratu URLa adierazten duen eremua jarduera honi buruzko informazio osagarria eskaintzen duena.</span><span class="sxs-lookup"><span data-stu-id="28338-120">**Web address**: Select the field that represents a URL providing additional information about this activity.</span></span> <span data-ttu-id="28338-121">Adibidez, jarduera hau iturri duen transakzio-sistema.</span><span class="sxs-lookup"><span data-stu-id="28338-121">For example, the transactional system that sources this activity.</span></span> <span data-ttu-id="28338-122">URL hau datu-iturburu-eko edozein eremu izan daiteke edo Power Query eraldaketa erabiliz eremu berri gisa eraiki daiteke.</span><span class="sxs-lookup"><span data-stu-id="28338-122">This URL can be any field from the data source, or it can be constructed as a new field using a Power Query transformation.</span></span> <span data-ttu-id="28338-123">URLko datu hau Jarduera Unibidearen entitatean gordeko da, APIak erabiliz downstream kontsumitu daitekeena.</span><span class="sxs-lookup"><span data-stu-id="28338-123">This URL data will be stored in the Unified Activity entity, which can be consumed downstream using APIs.</span></span>
   - <span data-ttu-id="28338-124">**Xehetasunak**: Aukeran, hautatu gehitzen den eremua xehetasun gehiagorako.</span><span class="sxs-lookup"><span data-stu-id="28338-124">**Details**: Optionally, select the field that is added for additional details.</span></span>
   - <span data-ttu-id="28338-125">**Ikonoa**: Aukeran, hautatu jarduera hau adierazten duen ikonoa.</span><span class="sxs-lookup"><span data-stu-id="28338-125">**Icon**: Optionally, select the icon that represents this activity.</span></span>
   - <span data-ttu-id="28338-126">**Jarduera mota**: Idatzi jarduera motaren definizio semantikoa hobekien deskribatzen duen datu arruntaren ereduari erreferentzia.</span><span class="sxs-lookup"><span data-stu-id="28338-126">**Activity Type**: Define the activity type reference to Common Data Model that best describes the semantic definition of the activity.</span></span>

1. <span data-ttu-id="28338-127">Sarbidean **Ezarri harremana** atala konfiguratu xehetasunak zure jardueraren datuak dagokion bezeroari lotzeko.</span><span class="sxs-lookup"><span data-stu-id="28338-127">In the **Set up relationship** section, configure the details to connect your activity data to its corresponding customer.</span></span>

    - <span data-ttu-id="28338-128">**Jardueraren entitatearen eremua**: Aukeratu beste erakunde batekin harremana ezartzeko erabiliko den eremuko zure entitatearen eremua.</span><span class="sxs-lookup"><span data-stu-id="28338-128">**Activity entity field**: Select the field in your activity entity that will be used to establish a relationship with another entity.</span></span>
    - <span data-ttu-id="28338-129">**Bezero entitatea**: Aukeratu dagokion iturburu bezeroaren entitatea zein harremana izango duen.</span><span class="sxs-lookup"><span data-stu-id="28338-129">**Customer entity**: Select the corresponding source customer entity with which your activity entity will be in relationship.</span></span> <span data-ttu-id="28338-130">Datuak bateratzeko prozesuan erabiltzen diren iturri bezeroak dituzten erakundeekin soilik erlaziona zaitezke.</span><span class="sxs-lookup"><span data-stu-id="28338-130">You can relate to only those source customer entities that are used in the data unification process.</span></span>
    - <span data-ttu-id="28338-131">**Bezeroaren entitatearen eremua**: Eremu honek iturburu bezeroaren entitatearen gako nagusia mapa prozesuan hautatzen den bezala erakusten du.</span><span class="sxs-lookup"><span data-stu-id="28338-131">**Customer entity field**: This field shows the primary key of the source customer entity as selected in the map process.</span></span> <span data-ttu-id="28338-132">Jatorri bezeroaren entitatearen funtsezko eremu hau jarduera-entitatearekin harremana ezartzeko erabiltzen da.</span><span class="sxs-lookup"><span data-stu-id="28338-132">This primary key field in the source customer entity is used to establish a relationship with the activity entity.</span></span>
    - <span data-ttu-id="28338-133">**Izena**: Jarduera-entitate honen eta hautatutako iturri bezeroaren entitatearen arteko harremana badago, erlazioaren izena irakurtzeko moduan egongo da.</span><span class="sxs-lookup"><span data-stu-id="28338-133">**Name**: If a relationship between this activity entity and the selected source customer entity already exists, the relationship name will be in read-only mode.</span></span> <span data-ttu-id="28338-134">Horrelako harremanik ez badago, harreman berria sortuko da hemen emandako izenarekin.</span><span class="sxs-lookup"><span data-stu-id="28338-134">If there no such relationship exists, a new relationship will be created with the name provided here.</span></span>
   
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="28338-135">![Definitu entitate-harremana](media/activities-entities-define.png "Definitu entitate-harremana")</span><span class="sxs-lookup"><span data-stu-id="28338-135">![Define the entity relationship](media/activities-entities-define.png "Define the entity relationship")</span></span>

1. <span data-ttu-id="28338-136">Aldaketak aplikatzeko, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="28338-136">Select **Save** to apply your changes.</span></span>

1. <span data-ttu-id="28338-137">**Jarduerak** orrian, hautatu **Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="28338-137">On the **Activities** page, select **Run**.</span></span>

> [!TIP]
> <span data-ttu-id="28338-138">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="28338-138">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="28338-139">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="28338-139">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="28338-140">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="28338-140">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="28338-141">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="28338-141">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="edit-an-activity"></a><span data-ttu-id="28338-142">Editatu jarduera</span><span class="sxs-lookup"><span data-stu-id="28338-142">Edit an activity</span></span>

1. <span data-ttu-id="28338-143">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.</span><span class="sxs-lookup"><span data-stu-id="28338-143">In audience insights, go to **Data** > **Activities**.</span></span>

2. <span data-ttu-id="28338-144">Hautatu editatu nahi duzun entitate-jarduera eta hautatu **Editatu**.</span><span class="sxs-lookup"><span data-stu-id="28338-144">Select the activity entity you want to edit and select **Edit**.</span></span> <span data-ttu-id="28338-145">Edo, entitate errenkadan pasa dezakezu eta hauta dezakezu **Editatu** ikonoa.</span><span class="sxs-lookup"><span data-stu-id="28338-145">Or, you can hover over the entity row and select the **Edit** icon.</span></span>

3. <span data-ttu-id="28338-146">Egin klik botoian **Editatu** ikonoa.</span><span class="sxs-lookup"><span data-stu-id="28338-146">Click on the **Edit** icon.</span></span>

4. <span data-ttu-id="28338-147">Sarbidean **Editatu jarduera** panela, eguneratu balioak eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="28338-147">In the **Edit activity** pane, update the values and select **Save**.</span></span>

5. <span data-ttu-id="28338-148">**Jarduerak** orrian, hautatu **Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="28338-148">On the **Activities** page, select **Run**.</span></span>

## <a name="delete-an-activity"></a><span data-ttu-id="28338-149">Ezabatu jarduera</span><span class="sxs-lookup"><span data-stu-id="28338-149">Delete an activity</span></span>

1. <span data-ttu-id="28338-150">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.</span><span class="sxs-lookup"><span data-stu-id="28338-150">In audience insights, go to **Data** > **Activities**.</span></span>

2. <span data-ttu-id="28338-151">Hautatu kendu nahi duzun entitate-jarduera eta hautatu **Ezabatu**.</span><span class="sxs-lookup"><span data-stu-id="28338-151">Select the activity entity you want to remove and select **Delete**.</span></span> <span data-ttu-id="28338-152">Edo, entitate errenkadan pasa dezakezu eta hauta dezakezu **Ezabatu** ikonoa.</span><span class="sxs-lookup"><span data-stu-id="28338-152">Or, you can hover over the entity row and select the **Delete** icon.</span></span> <span data-ttu-id="28338-153">Gainera, aldi berean ezabatu beharreko hainbat jarduera-entitate hauta ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="28338-153">Additionally, you can select multiple activity entities to be deleted at once.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="28338-154">![Editatu edo ezabatu entitatearen erlazioak](media/activities-entities-edit-delete.png "Editatu edo ezabatu entitatearen erlazioak")</span><span class="sxs-lookup"><span data-stu-id="28338-154">![Edit or delete the entity relationship](media/activities-entities-edit-delete.png "Edit or delete the entity relationship")</span></span>

3. <span data-ttu-id="28338-155">Hautatu botoian **Ezabatu** ikonoa.</span><span class="sxs-lookup"><span data-stu-id="28338-155">Select on the **Delete** icon.</span></span>

4. <span data-ttu-id="28338-156">Berretsi ezabatu nahi duzula.</span><span class="sxs-lookup"><span data-stu-id="28338-156">Confirm your deletion.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]