---
title: Harpidetzaren galera-tasaren iragarpenaren lagin-gida
description: Erabil ezazu lagin-gida hau harpidetzen galera-tasaren iragarpenaren eredua probatzeko.
ms.date: 11/19/2020
ms.reviewer: digranad
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 3f1019ace424f89320c5a0d5058e928f4cbc7e62
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269821"
---
# <a name="subscription-churn-prediction-preview-sample-guide"></a><span data-ttu-id="f7300-103">Harpidetzaren galera-tasaren iragarpenaren (aurrebista) lagin-gida</span><span class="sxs-lookup"><span data-stu-id="f7300-103">Subscription churn prediction (preview) sample guide</span></span>

<span data-ttu-id="f7300-104">Harpidetzaren galera-tasaren iragarpenaren adibide bat azalduko dizugu, behean emandako lagin datuak erabiliz.</span><span class="sxs-lookup"><span data-stu-id="f7300-104">We'll walk you through an end to end example of subscription churn prediction using the sample data provided below.</span></span> 

## <a name="scenario"></a><span data-ttu-id="f7300-105">Egoera</span><span class="sxs-lookup"><span data-stu-id="f7300-105">Scenario</span></span>

<span data-ttu-id="f7300-106">Contoso kalitate handiko kafea eta kafe-makinak sortzen dituen enpresa bat da. Horiek Contoso Coffee webgunearen bidez saltzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="f7300-106">Contoso is a company that produces high-quality coffee and coffee machines, which they sell through their Contoso Coffee website.</span></span> <span data-ttu-id="f7300-107">Berriki harpidetza negozioa hasi zuten euren bezeroek aldiro kafea hartzeko.</span><span class="sxs-lookup"><span data-stu-id="f7300-107">They recently started a subscription business for their customers to get coffee on a regular basis.</span></span> <span data-ttu-id="f7300-108">Haien helburua da ulertzea harpidetutako bezeroetako zeintzuk utz dezaketen harpidetza bertan behera hurrengo hilabeteetan.</span><span class="sxs-lookup"><span data-stu-id="f7300-108">Their goal is to understand, which subscribed customers might cancel their subscription in the next few months.</span></span> <span data-ttu-id="f7300-109">Zein bezero **galtzeko arriskua** dagoen jakiteak marketinarekin erlazionatutako ahalegina bideratzen lagun diezaioke enpresari, arreta bezero horiengan jarrita.</span><span class="sxs-lookup"><span data-stu-id="f7300-109">Knowing which of their customers is **likely to churn**, can help them save marketing efforts by focusing on keeping them.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7300-110">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="f7300-110">Prerequisites</span></span>

- <span data-ttu-id="f7300-111">Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="f7300-111">At least [Contributor permissions](permissions.md) in Customer Insights.</span></span>
- <span data-ttu-id="f7300-112">Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.</span><span class="sxs-lookup"><span data-stu-id="f7300-112">We recommend that you implement the following steps [in a new environment](manage-environments.md).</span></span>

## <a name="task-1---ingest-data"></a><span data-ttu-id="f7300-113">1. zeregina - Datuen sarrera</span><span class="sxs-lookup"><span data-stu-id="f7300-113">Task 1 - Ingest data</span></span>

<span data-ttu-id="f7300-114">Berrikusi zehazki [datuen sarrerari](data-sources.md) eta [Power Query konektoreak erabiliz datu-iturburuak inportatzeari](connect-power-query.md) buruzko artikuluak.</span><span class="sxs-lookup"><span data-stu-id="f7300-114">Review the articles [about data ingestion](data-sources.md) and [importing data sources using Power Query connectors](connect-power-query.md) specifically.</span></span> <span data-ttu-id="f7300-115">Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.</span><span class="sxs-lookup"><span data-stu-id="f7300-115">The following information assumes you familiarized with ingesting data in general.</span></span> 

### <a name="ingest-customer-data-from-ecommerce-platform"></a><span data-ttu-id="f7300-116">Sartu bezero-datuak merkataritza elektronikoko plataformatik</span><span class="sxs-lookup"><span data-stu-id="f7300-116">Ingest customer data from eCommerce platform</span></span>

1. <span data-ttu-id="f7300-117">Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="f7300-117">Create a data source named **eCommerce**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="f7300-118">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscontacts.</span><span class="sxs-lookup"><span data-stu-id="f7300-118">Enter the URL for eCommerce contacts https://aka.ms/ciadclasscontacts.</span></span>

1. <span data-ttu-id="f7300-119">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="f7300-119">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="f7300-120">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="f7300-120">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="f7300-121">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="f7300-121">**DateOfBirth**: Date</span></span>
   - <span data-ttu-id="f7300-122">**Sorrera-data**: Data/ordua/zona</span><span class="sxs-lookup"><span data-stu-id="f7300-122">**CreatedOn**: Date/Time/Zone</span></span>

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

1. <span data-ttu-id="f7300-124">Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**</span><span class="sxs-lookup"><span data-stu-id="f7300-124">In the **Name** field on the right-hand pane, rename your data source from **Query** to **eCommerceContacts**</span></span>

1. <span data-ttu-id="f7300-125">Gorde datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="f7300-125">Save the data source.</span></span>

### <a name="ingest-customer-data-from-loyalty-schema"></a><span data-ttu-id="f7300-126">Sartu bezero-datuak fideltasun-eskematik</span><span class="sxs-lookup"><span data-stu-id="f7300-126">Ingest customer data from loyalty schema</span></span>

1. <span data-ttu-id="f7300-127">Sortu **LoyaltyScheme** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="f7300-127">Create a data source named **LoyaltyScheme**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="f7300-128">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscustomerloyalty.</span><span class="sxs-lookup"><span data-stu-id="f7300-128">Enter the URL for eCommerce contacts https://aka.ms/ciadclasscustomerloyalty.</span></span>

1. <span data-ttu-id="f7300-129">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="f7300-129">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="f7300-130">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="f7300-130">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="f7300-131">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="f7300-131">**DateOfBirth**: Date</span></span>
   - <span data-ttu-id="f7300-132">**RewardsPoints**: Zenbaki osoa</span><span class="sxs-lookup"><span data-stu-id="f7300-132">**RewardsPoints**: Whole Number</span></span>
   - <span data-ttu-id="f7300-133">**Sorrera-data**: Data/ordua</span><span class="sxs-lookup"><span data-stu-id="f7300-133">**CreatedOn**: Date/Time</span></span>

1. <span data-ttu-id="f7300-134">Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="f7300-134">In the **Name** field on the right-hand pane, rename your data source from **Query** to **loyCustomers**.</span></span>

1. <span data-ttu-id="f7300-135">Gorde datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="f7300-135">Save the data source.</span></span>

### <a name="ingest-subscription-information"></a><span data-ttu-id="f7300-136">Sartu harpidetzari buruzko informazioa</span><span class="sxs-lookup"><span data-stu-id="f7300-136">Ingest subscription information</span></span>

1. <span data-ttu-id="f7300-137">Sortu **Harpidetzaren historia** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua / CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="f7300-137">Create a data source named **SubscriptionHistory**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="f7300-138">Idatzi merkataritza elektronikoko kontaktuen URLa https://aka.ms/ciadchurnsubscriptionhistory.</span><span class="sxs-lookup"><span data-stu-id="f7300-138">Enter the URL for eCommerce contacts https://aka.ms/ciadchurnsubscriptionhistory.</span></span>

1. <span data-ttu-id="f7300-139">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="f7300-139">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="f7300-140">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="f7300-140">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="f7300-141">**Harpidetzaren IDa**: osoko zenbakia</span><span class="sxs-lookup"><span data-stu-id="f7300-141">**SubscriptioID**: Whole Number</span></span>
   - <span data-ttu-id="f7300-142">**Harpidetza kopurua**: Moneta</span><span class="sxs-lookup"><span data-stu-id="f7300-142">**SubscriptionAmount**: Currency</span></span>
   - <span data-ttu-id="f7300-143">**Harpidetzaren amaiera-data**: Data / Ordua</span><span class="sxs-lookup"><span data-stu-id="f7300-143">**SubscriptionEndDate**: Date/Time</span></span>
   - <span data-ttu-id="f7300-144">**Harpidetzaren hasiera-data**: Data / Ordua</span><span class="sxs-lookup"><span data-stu-id="f7300-144">**SubscriptionStartDate**: Date/Time</span></span>
   - <span data-ttu-id="f7300-145">**Transakzioaren data**: Data / Ordua</span><span class="sxs-lookup"><span data-stu-id="f7300-145">**TransactionDate**: Date/Time</span></span>
   - <span data-ttu-id="f7300-146">**Errepikakorra da**: Egia / gezurra</span><span class="sxs-lookup"><span data-stu-id="f7300-146">**IsRecurring**: True/False</span></span>
   - <span data-ttu-id="f7300-147">**Automatikoki berritzen da**: Egia / gezurra</span><span class="sxs-lookup"><span data-stu-id="f7300-147">**Is_auto_renew**: True/False</span></span>
   - <span data-ttu-id="f7300-148">**Errepikapen-maiztasuna, hilabetetan**: osoko zenbakia</span><span class="sxs-lookup"><span data-stu-id="f7300-148">**RecurringFrequencyInMonths**: Whole Number</span></span>

1. <span data-ttu-id="f7300-149">Eskuineko paneleko **Izena** eremuan, aldatu **Kontsulta** izena datu-iturburuari eta idatzi **SubscriptionHistory**.</span><span class="sxs-lookup"><span data-stu-id="f7300-149">In the **Name** field on the right-hand pane, rename your data source from **Query** to **SubscriptionHistory**.</span></span>

1. <span data-ttu-id="f7300-150">Gorde datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="f7300-150">Save the data source.</span></span>

### <a name="ingest-customer-data-from-website-reviews"></a><span data-ttu-id="f7300-151">Sartu bezeroaren datuak webguneen berrikuspenetatik</span><span class="sxs-lookup"><span data-stu-id="f7300-151">Ingest customer data from website reviews</span></span>

1. <span data-ttu-id="f7300-152">Sortu **Webgunea** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua / CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="f7300-152">Create a data source named **Website**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="f7300-153">Idatzi merkataritza elektronikoko kontaktuen URLa https://aka.ms/ciadclasswebsite.</span><span class="sxs-lookup"><span data-stu-id="f7300-153">Enter the URL for eCommerce contacts https://aka.ms/ciadclasswebsite.</span></span>

1. <span data-ttu-id="f7300-154">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="f7300-154">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="f7300-155">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="f7300-155">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="f7300-156">**Iritziaren batez besteko balorazioa**: osoko zenbakia</span><span class="sxs-lookup"><span data-stu-id="f7300-156">**ReviewRating**: Whole Number</span></span>
   - <span data-ttu-id="f7300-157">**Iritziaren data**: Data</span><span class="sxs-lookup"><span data-stu-id="f7300-157">**ReviewDate**: Date</span></span>

1. <span data-ttu-id="f7300-158">Eskuineko paneleko 'Izena' eremuan, aldatu **Kontsulta** izena datu-iturburuari eta ipini **web-eko iritziak**.</span><span class="sxs-lookup"><span data-stu-id="f7300-158">In the 'Name' field on the right-hand pane, rename your data source from **Query** to **webReviews**.</span></span>

## <a name="task-2---data-unification"></a><span data-ttu-id="f7300-159">2. zeregina - Datuen bateratzea</span><span class="sxs-lookup"><span data-stu-id="f7300-159">Task 2 - Data unification</span></span>

<span data-ttu-id="f7300-160">Behin datuak sartuta, **Esleitu, bat etorri, konbinatu** prozesuarekin hasiko gara, bezeroaren profil bateratu bat sortzeko.</span><span class="sxs-lookup"><span data-stu-id="f7300-160">After ingesting the data we now begin the **Map, Match, Merge** process to create a unified customer profile.</span></span> <span data-ttu-id="f7300-161">Informazio gehiago lortzeko, ikusi [Datuen bateratzea](data-unification.md).</span><span class="sxs-lookup"><span data-stu-id="f7300-161">For more information, see [Data unification](data-unification.md).</span></span>

### <a name="map"></a><span data-ttu-id="f7300-162">Esleitu</span><span class="sxs-lookup"><span data-stu-id="f7300-162">Map</span></span>

1. <span data-ttu-id="f7300-163">Behin datuak sartuta, esleitu merkataritza elektronikoko eta fideltasun-datuetako kontaktuak ohiko datu motei.</span><span class="sxs-lookup"><span data-stu-id="f7300-163">After ingesting the data, map contacts from eCommerce and Loyalty data to common data types.</span></span> <span data-ttu-id="f7300-164">Joan hona: **Datuak** > **Bateratu** > **Esleitu**.</span><span class="sxs-lookup"><span data-stu-id="f7300-164">Go to **Data** > **Unify** > **Map**.</span></span>

1. <span data-ttu-id="f7300-165">Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="f7300-165">Select the entities that represent the customer profile – **eCommerceContacts** and **loyCustomers**.</span></span> 

   :::image type="content" source="media/unify-ecommerce-loyalty.PNG" alt-text="bateratu ecommerce eta loyalty datu-iturburuak.":::

1. <span data-ttu-id="f7300-167">Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.</span><span class="sxs-lookup"><span data-stu-id="f7300-167">Select **ContactId** as the primary key for **eCommerceContacts** and **LoyaltyID** as the primary key for **loyCustomers**.</span></span>

   :::image type="content" source="media/unify-loyaltyid.PNG" alt-text="Bateratu LoyaltyId gako nagusi gisa.":::

### <a name="match"></a><span data-ttu-id="f7300-169">Lotzea</span><span class="sxs-lookup"><span data-stu-id="f7300-169">Match</span></span>

1. <span data-ttu-id="f7300-170">Joan **Bat etorri** fitxara eta hautatu **Ezarri ordena**.</span><span class="sxs-lookup"><span data-stu-id="f7300-170">Go to the **Match** tab and select **Set Order**.</span></span>

1. <span data-ttu-id="f7300-171">**Nagusia** goitibeherako zerrendan, aukeratu **eCommerceContacts : eCommerce** iturburu nagusi gisa eta sartu erregistro guztiak.</span><span class="sxs-lookup"><span data-stu-id="f7300-171">In the **Primary** drop-down list, choose **eCommerceContacts : eCommerce** as the primary source and include all records.</span></span>

1. <span data-ttu-id="f7300-172">**2. entitatea** goitibeherako zerrendan, aukeratu **loyCustomers : LoyaltyScheme** eta sartu erregistro guztiak.</span><span class="sxs-lookup"><span data-stu-id="f7300-172">In the **Entity 2** drop-down list, choose **loyCustomers : LoyaltyScheme** and include all records.</span></span>

   :::image type="content" source="media/unify-match-order.PNG" alt-text="Bateratu eCommerce eta Loyalty bat-etortzea.":::

1. <span data-ttu-id="f7300-174">Hautatu **Sortu beste arau bat**</span><span class="sxs-lookup"><span data-stu-id="f7300-174">Select **Create a new rule**</span></span>

1. <span data-ttu-id="f7300-175">Gehitu lehenengo baldintza FullName erabilita.</span><span class="sxs-lookup"><span data-stu-id="f7300-175">Add your first condition using FullName.</span></span>

   * <span data-ttu-id="f7300-176">eCommerceContacts entitateari dagokionez, hautatu **FullName** goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="f7300-176">For eCommerceContacts select **FullName** in the drop-down.</span></span>
   * <span data-ttu-id="f7300-177">loyCustomers entitateari dagokionez, hautatu **FullName** goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="f7300-177">For loyCustomers select **FullName** in the drop-down.</span></span>
   * <span data-ttu-id="f7300-178">Aukeratu **Normalizatu** goitibeherako zerrendan eta aukeratu **Mota (Telefonoa, Izena, Helbidea, ...)**.</span><span class="sxs-lookup"><span data-stu-id="f7300-178">Select the **Normalize** drop down and choose **Type (Phone, Name, Address, ...)**.</span></span>
   * <span data-ttu-id="f7300-179">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="f7300-179">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

1. <span data-ttu-id="f7300-180">Idatzi arau berriaren **Izen osoa, posta elektronikoa** izena.</span><span class="sxs-lookup"><span data-stu-id="f7300-180">Enter the name **FullName, Email** for the new rule.</span></span>

   * <span data-ttu-id="f7300-181">Gehitu helbide elektronikoaren bigarren baldintza bat **Gehitu baldintza** hautatuta</span><span class="sxs-lookup"><span data-stu-id="f7300-181">Add a second condition for email address by selecting **Add Condition**</span></span>
   * <span data-ttu-id="f7300-182">ECommerceContacts entitateari dagokionez, aukeratu **Helbide elektronikoa** goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="f7300-182">For entity eCommerceContacts, choose **EMail** in drop-down.</span></span>
   * <span data-ttu-id="f7300-183">loyCustomers entitateari dagokionez, aukeratu **Helbide elektronikoa** goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="f7300-183">For entity loyCustomers, choose **EMail** in the drop-down.</span></span> 
   * <span data-ttu-id="f7300-184">"Normalizatu" hutsik utzi.</span><span class="sxs-lookup"><span data-stu-id="f7300-184">Leave Normalize blank.</span></span> 
   * <span data-ttu-id="f7300-185">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="f7300-185">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

   :::image type="content" source="media/unify-match-rule.PNG" alt-text="Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.":::

7. <span data-ttu-id="f7300-187">Hautatu **gorde** eta **exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="f7300-187">Select **Save** and **Run**.</span></span>

### <a name="merge"></a><span data-ttu-id="f7300-188">Konbinazioa</span><span class="sxs-lookup"><span data-stu-id="f7300-188">Merge</span></span>

1. <span data-ttu-id="f7300-189">Joan **konbinatu** fitxara.</span><span class="sxs-lookup"><span data-stu-id="f7300-189">Go to the **Merge** tab.</span></span>

1. <span data-ttu-id="f7300-190">**loyCustomers** entitatearen **Kontaktuaren IDa** atalean, aldatu bistaratzeko izena **ContactIdLOYALTY** izenera, sartutako beste IDetatik bereizteko.</span><span class="sxs-lookup"><span data-stu-id="f7300-190">On the **ContactId** for **loyCustomers** entity, change the display name to **ContactIdLOYALTY** to differentiate it from the other IDs ingested.</span></span>

   :::image type="content" source="media/unify-merge-contactid.PNG" alt-text="aldatu leialtasun IDaren kontaktuaren IDa.":::

1. <span data-ttu-id="f7300-192">Aukeratu **Gorde** eta **exekutatu** konbinatzeko prozesua hasteko.</span><span class="sxs-lookup"><span data-stu-id="f7300-192">Select **Save** and **Run** to start the Merge Process.</span></span>


## <a name="task-3---configure-the-subscription-churn-prediction"></a><span data-ttu-id="f7300-193">3. zeregina - Konfiguratu harpidetzen galera-tasaren iragarpena</span><span class="sxs-lookup"><span data-stu-id="f7300-193">Task 3 - Configure the subscription churn prediction</span></span>

<span data-ttu-id="f7300-194">Bezeroen profil bateratuak behar bezala jarrita, harpidetzaren galera-tasaren iragarpena exekutatu dezakegu.</span><span class="sxs-lookup"><span data-stu-id="f7300-194">With the unified customer profiles in place, we can now run the subscription churn prediction.</span></span> <span data-ttu-id="f7300-195">Urrats zehatzetarako, ikusi [Harpidetzaren galera-tasaren iragarpena (aurrebista)](predict-subscription-churn.md) artikulu.</span><span class="sxs-lookup"><span data-stu-id="f7300-195">For detailed steps, see the [Subscription churn prediction (preview)](predict-subscription-churn.md) article.</span></span> 

1. <span data-ttu-id="f7300-196">Joan **Adimena** > **Ezagutu** atalera eta hautatu **Bezeroen galera-tasaren eredua**.</span><span class="sxs-lookup"><span data-stu-id="f7300-196">Go to **Intelligence** > **Discover** and select to use the **Customer churn model**.</span></span>

1. <span data-ttu-id="f7300-197">Aukeratu **Harpidetza** aukera eta hautatu **Hasi**.</span><span class="sxs-lookup"><span data-stu-id="f7300-197">Select the **Subscription** option and select **Get started**.</span></span>

1. <span data-ttu-id="f7300-198">Eman **OOB eCommerce harpidetzen galera-tasaren iragarpena** izena ereduari eta **OOBSubscriptionChurnPrediction** irteerako entitateari.</span><span class="sxs-lookup"><span data-stu-id="f7300-198">Name the model **OOB Subscription Churn Prediction** and the output entity **OOBSubscriptionChurnPrediction**.</span></span>

1. <span data-ttu-id="f7300-199">Definitu galera-tasaren ereduaren bi baldintza:</span><span class="sxs-lookup"><span data-stu-id="f7300-199">Define two conditions for the churn model:</span></span>

   * <span data-ttu-id="f7300-200">**Harpidetza amaitu zenetik igarotako egunak**: **gutxienez 60** egun.</span><span class="sxs-lookup"><span data-stu-id="f7300-200">**Days since subscription ended**: **at least 60** days.</span></span> <span data-ttu-id="f7300-201">Harpidetza amaitu eta bezeroak hura berritu ez badu ezarritako epean, galdutzat emango da.</span><span class="sxs-lookup"><span data-stu-id="f7300-201">If a customer doesn't renew the subscription in this period after their subscription ended, they are considered churned.</span></span> 

   * <span data-ttu-id="f7300-202">**Bezeroen galera-tasaren definizioa** : **gutxienez 93** egun.</span><span class="sxs-lookup"><span data-stu-id="f7300-202">**Churn definition**: **at least 93** days.</span></span> <span data-ttu-id="f7300-203">Ereduak behar duen denbora zein bezero galduko diren iragartzeko.</span><span class="sxs-lookup"><span data-stu-id="f7300-203">The duration the model predict which customers might churn.</span></span> <span data-ttu-id="f7300-204">Etorkizunean zenbat eta gehiago begiratu, orduan eta emaitza hain zehatzak izango dira.</span><span class="sxs-lookup"><span data-stu-id="f7300-204">The further in the future you look, the less precise the results.</span></span>

     :::image type="content" source="media/model-subs-levers.PNG" alt-text="Aukeratu iragarpen-leihoa eta galera-tasaren definizioa ereduaren mailakatzaileak.":::

1. <span data-ttu-id="f7300-206">Aukeratu **Gehitu beharrezko datuak** eta hautatu **Gehitu datuak** harpidetzaren historiarako.</span><span class="sxs-lookup"><span data-stu-id="f7300-206">Select **Add required data** and select **Add data** for subscription history.</span></span>

1. <span data-ttu-id="f7300-207">Gehitu **Harpidetza: harpidetzaren historia** entitatea eta esleitu elektronikoko eremuak ereduak eskatzen dituen eremuetara.</span><span class="sxs-lookup"><span data-stu-id="f7300-207">Add the **Subscription : SubscriptionHistory** entity and map the fields from eCommerce to the corresponding fields required by the model.</span></span>

1. <span data-ttu-id="f7300-208">Sartu **Harpidetza: harpidetzaren historia** entitatea **merkataritza elektronikoko kontaktuak: merkataritza elektronikoa**, izendatu harremana **merkataritza elektronikoko harpidetza**.</span><span class="sxs-lookup"><span data-stu-id="f7300-208">Join the **Subscription : SubscriptionHistory** entity with **eCommerceContacts : eCommerce**, name the relationship **eCommerceSubscription**.</span></span>

   :::image type="content" source="media/model-subscription-join.PNG" alt-text="Sartu merkataritza elektronikoko entitateetan.":::

1. <span data-ttu-id="f7300-210">Bezeroen jardueretan, gehitu **web-eko iritziak: webgunea** entitatea eta esleitu web-eko iritziak ereduak eskatzen dituen eremuetara.</span><span class="sxs-lookup"><span data-stu-id="f7300-210">Under Customer Activities, add the **webReviews : Website** entity and map the fields from webReviews to the corresponding fields required by the model.</span></span> 
   - <span data-ttu-id="f7300-211">Gako nagusia: ReviewId</span><span class="sxs-lookup"><span data-stu-id="f7300-211">Primary key: ReviewId</span></span>
   - <span data-ttu-id="f7300-212">Denbora-marka: ReviewDate</span><span class="sxs-lookup"><span data-stu-id="f7300-212">Timestamp: ReviewDate</span></span>
   - <span data-ttu-id="f7300-213">Gertaera: ReviewRating</span><span class="sxs-lookup"><span data-stu-id="f7300-213">Event: ReviewRating</span></span>

1. <span data-ttu-id="f7300-214">Konfiguratu jarduera webguneen iritzietarako.</span><span class="sxs-lookup"><span data-stu-id="f7300-214">Configure an activity for website reviews.</span></span> <span data-ttu-id="f7300-215">Aukeratu **Berrikuspena** jarduera eta sartu **web-eko berrikuspenak: webgunea** entitatean **merkataritza elektronikoko kontaktuak: merkataritza elektronikoa**-rekin.</span><span class="sxs-lookup"><span data-stu-id="f7300-215">Select the activity **Review** and join the **webReviews : Website** entity with **eCommerceContacts : eCommerce**.</span></span>

1. <span data-ttu-id="f7300-216">Aukeratu **Hurrengoa** ereduaren antolaketa ezartzeko.</span><span class="sxs-lookup"><span data-stu-id="f7300-216">Select **Next** to set the model schedule.</span></span>

   <span data-ttu-id="f7300-217">Ereduak aldizka trebatu behar du eredu berriak ikasteko datu berriak sartzen direnean.</span><span class="sxs-lookup"><span data-stu-id="f7300-217">The model needs to train regularly to learn new patterns when there is new data ingested.</span></span> <span data-ttu-id="f7300-218">Adibide honetarako, hautatu **hilero**.</span><span class="sxs-lookup"><span data-stu-id="f7300-218">For this example, select **Monthly**.</span></span>

1. <span data-ttu-id="f7300-219">Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="f7300-219">After reviewing all the details, select **Save and Run**.</span></span>

## <a name="task-4---review-model-results-and-explanations"></a><span data-ttu-id="f7300-220">4. zeregina - Berrikusi ereduen emaitzak eta azalpenak</span><span class="sxs-lookup"><span data-stu-id="f7300-220">Task 4 - Review model results and explanations</span></span>

<span data-ttu-id="f7300-221">Ereduak datuen prestakuntza eta puntuazioa osatuko ditu.</span><span class="sxs-lookup"><span data-stu-id="f7300-221">Let the model complete the training and scoring of the data.</span></span> <span data-ttu-id="f7300-222">Harpidetzen galera-tasaren ereduaren azalpenak berrikus ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="f7300-222">You can now review the subscription churn model explanations.</span></span> <span data-ttu-id="f7300-223">Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-subscription-churn.md#review-a-prediction-status-and-results).</span><span class="sxs-lookup"><span data-stu-id="f7300-223">For more information, see [Review a prediction status and results](predict-subscription-churn.md#review-a-prediction-status-and-results).</span></span>

## <a name="task-5---create-a-segment-of-high-churn-risk-customers"></a><span data-ttu-id="f7300-224">5. zeregina - Sortu galera-arrisku handiko bezeroen segmentu bat</span><span class="sxs-lookup"><span data-stu-id="f7300-224">Task 5 - Create a segment of high churn-risk customers</span></span>

<span data-ttu-id="f7300-225">Ekoizpen eredua martxan jartzeak hemen ikus dezakezun entitate berri bat sortzen du: **Datuak** > **Entitateak**.</span><span class="sxs-lookup"><span data-stu-id="f7300-225">Running the production model creates a new entity that you can see in **Data** > **Entities**.</span></span>   

<span data-ttu-id="f7300-226">Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.</span><span class="sxs-lookup"><span data-stu-id="f7300-226">You can create a new segment based on the entity created by the model.</span></span>

1.  <span data-ttu-id="f7300-227">Joan hona: **Segmentuak**.</span><span class="sxs-lookup"><span data-stu-id="f7300-227">Go to **Segments**.</span></span> <span data-ttu-id="f7300-228">Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**.</span><span class="sxs-lookup"><span data-stu-id="f7300-228">Select **New** and choose **Create from** > **Intelligence**.</span></span> 

   :::image type="content" source="media/segment-intelligence.PNG" alt-text="Ereduaren irteerarekin segmentu bat sortzea.":::

1. <span data-ttu-id="f7300-230">Aukeratu **OOBSubscriptionChurnPrediction** amaiera-puntua eta definitu segmentua:</span><span class="sxs-lookup"><span data-stu-id="f7300-230">Select the **OOBSubscriptionChurnPrediction** endpoint and define the segment:</span></span> 
   - <span data-ttu-id="f7300-231">Eremua: ChurnScore</span><span class="sxs-lookup"><span data-stu-id="f7300-231">Field: ChurnScore</span></span>
   - <span data-ttu-id="f7300-232">Eragilea: hau baino handiagoa</span><span class="sxs-lookup"><span data-stu-id="f7300-232">Operator: greater than</span></span>
   - <span data-ttu-id="f7300-233">Balioa: 0.6</span><span class="sxs-lookup"><span data-stu-id="f7300-233">Value: 0.6</span></span>
   
   :::image type="content" source="media/segment-setup-subs.PNG" alt-text="Konfiguratu harpidetzaren galera-tasaren segmentua.":::

<span data-ttu-id="f7300-235">Harpidetza-negozio honen galera-arrisku handiko bezeroak identifikatzen dituen segmentu dinamikoki eguneratua duzu.</span><span class="sxs-lookup"><span data-stu-id="f7300-235">You now have a segment that is dynamically updated which identifies high churn-risk customers for this subscription business.</span></span>

<span data-ttu-id="f7300-236">Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).</span><span class="sxs-lookup"><span data-stu-id="f7300-236">For more information, see [Create and manage segments](segments.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]