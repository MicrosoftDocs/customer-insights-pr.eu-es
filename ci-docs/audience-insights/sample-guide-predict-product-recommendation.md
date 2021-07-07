---
title: Produktuak gomendatzeko iragarpenaren adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen produktuak gomendatzeko iragarpen-eredua probatzeko.
ms.date: 02/10/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: diegogranados117
ms.author: digranad
manager: shellyha
ms.openlocfilehash: a85ee598ec747d0594755314e83a127ce0f2af95
ms.sourcegitcommit: 0b754d194d765afef70d1008db7b347dd1f0ee40
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306151"
---
# <a name="product-recommendation-prediction-preview-sample-guide"></a><span data-ttu-id="0b5bb-103">Produktuak gomendatzeko iragarpenaren (aurreargitalpena) adibide-gida</span><span class="sxs-lookup"><span data-stu-id="0b5bb-103">Product recommendation prediction (preview) sample guide</span></span>

<span data-ttu-id="0b5bb-104">Produktuak gomendatzeko iragarpenaren adibide bat azalduko dizugu, behean emandako lagin datuak erabiliz.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-104">We'll walk you through an end to end example of product recommendation prediction using the sample data provided below.</span></span>

## <a name="scenario"></a><span data-ttu-id="0b5bb-105">Egoera</span><span class="sxs-lookup"><span data-stu-id="0b5bb-105">Scenario</span></span>

<span data-ttu-id="0b5bb-106">Contoso kalitate handiko kafea eta kafe makinak ekoizten dituen enpresa da eta Contoso Coffee webgunearen bidez saltzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-106">Contoso is a company that produces high-quality coffee and coffee machines, which they sell through their Contoso Coffee website.</span></span> <span data-ttu-id="0b5bb-107">Haien helburua da bezeroei zein produktu gomendatu behar dieten ulertzea.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-107">Their goal is to understand which products should they recommend to their recurring customers.</span></span> <span data-ttu-id="0b5bb-108">Bezero gehiago zer diren jakitea **erosteko litekeena**, marketineko ahalegina aurrezten lagun diezaiekete elementu zehatzetan arreta jarriz.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-108">Knowing what customers are more **likely to purchase**, can help them save marketing efforts by focusing on specific items.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0b5bb-109">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="0b5bb-109">Prerequisites</span></span>

- <span data-ttu-id="0b5bb-110">Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-110">At least [Contributor permissions](permissions.md) in Customer Insights.</span></span>
- <span data-ttu-id="0b5bb-111">Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-111">We recommend that you implement the following steps [in a new environment](manage-environments.md).</span></span>

## <a name="task-1---ingest-data"></a><span data-ttu-id="0b5bb-112">1. zeregina - Datuen sarrera</span><span class="sxs-lookup"><span data-stu-id="0b5bb-112">Task 1 - Ingest data</span></span>

<span data-ttu-id="0b5bb-113">Berrikusi zehazki [datuen sarrerari](data-sources.md) eta [Power Query konektoreak erabiliz datu-iturburuak inportatzeari](connect-power-query.md) buruzko artikuluak.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-113">Review the articles [about data ingestion](data-sources.md) and [importing data sources using Power Query connectors](connect-power-query.md) specifically.</span></span> <span data-ttu-id="0b5bb-114">Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-114">The following information assumes you familiarized with ingesting data in general.</span></span>

### <a name="ingest-customer-data-from-ecommerce-platform"></a><span data-ttu-id="0b5bb-115">Sartu bezero-datuak merkataritza elektronikoko plataformatik</span><span class="sxs-lookup"><span data-stu-id="0b5bb-115">Ingest customer data from eCommerce platform</span></span>

1. <span data-ttu-id="0b5bb-116">Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-116">Create a data source named **eCommerce**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="0b5bb-117">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscontacts.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-117">Enter the URL for eCommerce contacts https://aka.ms/ciadclasscontacts.</span></span>

1. <span data-ttu-id="0b5bb-118">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-118">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="0b5bb-119">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="0b5bb-119">Update the datatype for the columns listed below:</span></span>
   - <span data-ttu-id="0b5bb-120">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="0b5bb-120">**DateOfBirth**: Date</span></span>
   - <span data-ttu-id="0b5bb-121">**Sorrera-data**: Data/ordua/zona</span><span class="sxs-lookup"><span data-stu-id="0b5bb-121">**CreatedOn**: Date/Time/Zone</span></span>

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

5. <span data-ttu-id="0b5bb-123">Eskuinaldeko paneleko "Izena" eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**</span><span class="sxs-lookup"><span data-stu-id="0b5bb-123">In the 'Name' field on the right-hand pane, rename your data source from **Query** to **eCommerceContacts**</span></span>

6. <span data-ttu-id="0b5bb-124">**Gorde** datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-124">**Save** the data source.</span></span>

### <a name="ingest-online-purchase-data"></a><span data-ttu-id="0b5bb-125">Sartu sareko erosketen datuak</span><span class="sxs-lookup"><span data-stu-id="0b5bb-125">Ingest online purchase data</span></span>

1. <span data-ttu-id="0b5bb-126">Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-126">Add another data set to the same **eCommerce** data source.</span></span> <span data-ttu-id="0b5bb-127">Aukeratu **Testua/CSV** konektorea berriro.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-127">Choose the **Text/CSV** connector again.</span></span>

1. <span data-ttu-id="0b5bb-128">Idatzi **sareko erosketen** datuen URLa: https://aka.ms/ciadclassonline.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-128">Enter the URL for **Online Purchases** data https://aka.ms/ciadclassonline.</span></span>

1. <span data-ttu-id="0b5bb-129">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-129">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="0b5bb-130">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="0b5bb-130">Update the datatype for the columns listed below:</span></span>
   - <span data-ttu-id="0b5bb-131">**PurchasedOn**: Data/ordua</span><span class="sxs-lookup"><span data-stu-id="0b5bb-131">**PurchasedOn**: Date/Time</span></span>
   - <span data-ttu-id="0b5bb-132">**TotalPrice**: Moneta</span><span class="sxs-lookup"><span data-stu-id="0b5bb-132">**TotalPrice**: Currency</span></span>

1. <span data-ttu-id="0b5bb-133">Alboko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommercePurchases**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-133">In the **Name** field on the side pane, rename your data source from **Query** to **eCommercePurchases**.</span></span>

1. <span data-ttu-id="0b5bb-134">**Gorde** datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-134">**Save** the data source.</span></span>


### <a name="ingest-customer-data-from-loyalty-schema"></a><span data-ttu-id="0b5bb-135">Sartu bezero-datuak fideltasun-eskematik</span><span class="sxs-lookup"><span data-stu-id="0b5bb-135">Ingest customer data from loyalty schema</span></span>

1. <span data-ttu-id="0b5bb-136">Sortu **LoyaltyScheme** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-136">Create a data source named **LoyaltyScheme**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="0b5bb-137">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscustomerloyalty.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-137">Enter the URL for eCommerce contacts https://aka.ms/ciadclasscustomerloyalty.</span></span>

1. <span data-ttu-id="0b5bb-138">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-138">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="0b5bb-139">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="0b5bb-139">Update the datatype for the columns listed below:</span></span>
   - <span data-ttu-id="0b5bb-140">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="0b5bb-140">**DateOfBirth**: Date</span></span>
   - <span data-ttu-id="0b5bb-141">**RewardsPoints**: Zenbaki osoa</span><span class="sxs-lookup"><span data-stu-id="0b5bb-141">**RewardsPoints**: Whole Number</span></span>
   - <span data-ttu-id="0b5bb-142">**Sorrera-data**: Data/ordua</span><span class="sxs-lookup"><span data-stu-id="0b5bb-142">**CreatedOn**: Date/Time</span></span>

1. <span data-ttu-id="0b5bb-143">Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-143">In the **Name** field on the right-hand pane, rename your data source from **Query** to **loyCustomers**.</span></span>

1. <span data-ttu-id="0b5bb-144">**Gorde** datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-144">**Save** the data source.</span></span>

## <a name="task-2---data-unification"></a><span data-ttu-id="0b5bb-145">2. zeregina - Datuen bateratzea</span><span class="sxs-lookup"><span data-stu-id="0b5bb-145">Task 2 - Data unification</span></span>

<span data-ttu-id="0b5bb-146">Datuak irentsi ondoren, datuak bateratzeko prozesua hasten dugu bezeroaren profil bateratua sortzeko.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-146">After ingesting the data, we now begin the data unification process to create a unified customer profile.</span></span> <span data-ttu-id="0b5bb-147">Informazio gehiago lortzeko, ikusi [Datuen bateratzea](data-unification.md).</span><span class="sxs-lookup"><span data-stu-id="0b5bb-147">For more information, see [Data unification](data-unification.md).</span></span>

### <a name="map"></a><span data-ttu-id="0b5bb-148">Esleitu</span><span class="sxs-lookup"><span data-stu-id="0b5bb-148">Map</span></span>

1. <span data-ttu-id="0b5bb-149">Behin datuak sartuta, esleitu merkataritza elektronikoko eta fideltasun-datuetako kontaktuak ohiko datu motei.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-149">After ingesting the data, map contacts from eCommerce and Loyalty data to common data types.</span></span> <span data-ttu-id="0b5bb-150">Joan hona: **Datuak** > **Bateratu** > **Esleitu**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-150">Go to **Data** > **Unify** > **Map**.</span></span>

2. <span data-ttu-id="0b5bb-151">Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-151">Select the entities that represent the customer profile – **eCommerceContacts** and **loyCustomers**.</span></span>

   ![bateratu ecommerce eta loyalty datu-iturburuak.](media/unify-ecommerce-loyalty.png)

3. <span data-ttu-id="0b5bb-153">Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-153">Select **ContactId** as the primary key for **eCommerceContacts** and **LoyaltyID** as the primary key for **loyCustomers**.</span></span>

   ![Bateratu LoyaltyId gako nagusi gisa.](media/unify-loyaltyid.png)

### <a name="match"></a><span data-ttu-id="0b5bb-155">Lotu</span><span class="sxs-lookup"><span data-stu-id="0b5bb-155">Match</span></span>

1. <span data-ttu-id="0b5bb-156">Joan **Bat etorri** fitxara eta hautatu **Ezarri ordena**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-156">Go to the **Match** tab and select **Set Order**.</span></span>

2. <span data-ttu-id="0b5bb-157">Urtean **Lehen Hezkuntza** goitibeherako zerrenda, aukeratu **eCommerceContacts: eCommerce** iturri nagusi gisa eta erregistro guztiak barne.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-157">In the **Primary** dropdown list, choose **eCommerceContacts : eCommerce** as the primary source and include all records.</span></span>

3. <span data-ttu-id="0b5bb-158">Urtean **2. entitatea** goitibeherako zerrenda, aukeratu **loyCustomers: LoyaltyScheme** eta erregistro guztiak sartu.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-158">In the **Entity 2** dropdown list, choose **loyCustomers : LoyaltyScheme** and include all records.</span></span>

   ![Bateratu eCommerce eta Loyalty bat-etortzea.](media/unify-match-order.png)

4. <span data-ttu-id="0b5bb-160">Hautatu **Sortu beste arau bat**</span><span class="sxs-lookup"><span data-stu-id="0b5bb-160">Select **Create a new rule**</span></span>

5. <span data-ttu-id="0b5bb-161">Gehitu lehenengo baldintza FullName erabilita.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-161">Add your first condition using FullName.</span></span>

   - <span data-ttu-id="0b5bb-162">ECommerceContacts aukeratzeko **Izen abizenak** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-162">For eCommerceContacts select **FullName** in the dropdown.</span></span>
   - <span data-ttu-id="0b5bb-163">loyCustomers aukeratzeko **Izen abizenak** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-163">For loyCustomers select **FullName** in the dropdown.</span></span>
   - <span data-ttu-id="0b5bb-164">Aukeratu **Normalizatu** goitibeherako zerrendan eta aukeratu **Mota (Telefonoa, Izena, Helbidea, ...)**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-164">Select the **Normalize** drop down and choose **Type (Phone, Name, Address, ...)**.</span></span>
   - <span data-ttu-id="0b5bb-165">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-165">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

6. <span data-ttu-id="0b5bb-166">Idatzi arau berriaren **Izen osoa, posta elektronikoa** izena.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-166">Enter the name **FullName, Email** for the new rule.</span></span>

   - <span data-ttu-id="0b5bb-167">Gehitu helbide elektronikoaren bigarren baldintza bat **Gehitu baldintza** hautatuta</span><span class="sxs-lookup"><span data-stu-id="0b5bb-167">Add a second condition for email address by selecting **Add Condition**</span></span>
   - <span data-ttu-id="0b5bb-168">ECommerceContacts entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-168">For entity eCommerceContacts, choose **EMail** in dropdown.</span></span>
   - <span data-ttu-id="0b5bb-169">loyCustomers entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-169">For entity loyCustomers, choose **EMail** in the dropdown.</span></span>
   - <span data-ttu-id="0b5bb-170">"Normalizatu" hutsik utzi.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-170">Leave Normalize blank.</span></span>
   - <span data-ttu-id="0b5bb-171">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-171">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

   ![Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.](media/unify-match-rule.png)

7. <span data-ttu-id="0b5bb-173">Hautatu **gorde** eta **exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-173">Select **Save** and **Run**.</span></span>

### <a name="merge"></a><span data-ttu-id="0b5bb-174">Konbinazioa</span><span class="sxs-lookup"><span data-stu-id="0b5bb-174">Merge</span></span>

1. <span data-ttu-id="0b5bb-175">Joan **konbinatu** fitxara.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-175">Go to the **Merge** tab.</span></span>

1. <span data-ttu-id="0b5bb-176">**loyCustomers** entitatearen **Kontaktuaren IDa** atalean, aldatu bistaratzeko izena **ContactIdLOYALTY** izenera, sartutako beste IDetatik bereizteko.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-176">On the **ContactId** for **loyCustomers** entity, change the display name to **ContactIdLOYALTY** to differentiate it from the other IDs ingested.</span></span>

   ![aldatu leialtasun IDaren kontaktuaren IDa.](media/unify-merge-contactid.png)

1. <span data-ttu-id="0b5bb-178">Aukeratu **Gorde** eta **exekutatu** konbinatzeko prozesua hasteko.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-178">Select **Save** and **Run** to start the Merge Process.</span></span>

## <a name="task-3---configure-product-recommendation-prediction"></a><span data-ttu-id="0b5bb-179">3. zeregina: konfiguratu produktuaren gomendioa iragarpena</span><span class="sxs-lookup"><span data-stu-id="0b5bb-179">Task 3 - Configure product recommendation prediction</span></span>

<span data-ttu-id="0b5bb-180">Bezeroen profil bateratuak behar bezala jarrita, harpidetzaren galera-tasaren iragarpena exekutatu dezakegu.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-180">With the unified customer profiles in place, we can now run the subscription churn prediction.</span></span>

1. <span data-ttu-id="0b5bb-181">Joan **Adimena** > **Iragarpena** aukerara eta aukeratu **Produktuen gomendioa**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-181">Go to **Intelligence** > **Prediction** choose **Product recommendation**.</span></span>

1. <span data-ttu-id="0b5bb-182">Hautatu **Hasi erabiltzen**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-182">Select **Get started**.</span></span>

1. <span data-ttu-id="0b5bb-183">Eman izena ereduari **OOB produktuaren gomendio eredua iragarpena** eta irteerako entitatea **OOBProductRecomendationModelPrediction**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-183">Name the model **OOB Product Recommendation Model Prediction** and the output entity **OOBProductRecommendationModelPrediction**.</span></span>

1. <span data-ttu-id="0b5bb-184">Definitu ereduaren hiru baldintza:</span><span class="sxs-lookup"><span data-stu-id="0b5bb-184">Define three conditions for the model:</span></span>

   - <span data-ttu-id="0b5bb-185">**Produktu kopurua**: ezarri balio hau **5**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-185">**Number of products**: Set this value to **5**.</span></span> <span data-ttu-id="0b5bb-186">Ezarpen honek bezeroei zenbat produktu gomendatu nahi dizkiezu definitzen du.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-186">This setting defines how many products you want to recommend to your customers.</span></span>

   - <span data-ttu-id="0b5bb-187">**Espero diren erosketak errepikatu**: Aukeratu **Bai** zure bezeroek aurretik erositako gomendioan produktuak sartu nahi dituzula adierazteko.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-187">**Repeat purchases expected**: Select **Yes** to indicate that you want to include products in the recommendation that your customers have purchased before.</span></span>

   - <span data-ttu-id="0b5bb-188">**Atzera begiratu leihoa:** aukeratu gutxienez **365 egun**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-188">**Look back window:** Select at least **365 days**.</span></span> <span data-ttu-id="0b5bb-189">Ezarpen honek zenbat egun atzera dezakezun eredua ikusteko aukera, informazio hori erabili ahal izateko bezeroek ikusiko duten gomendioak hobetzeko.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-189">This setting defines how far the model will look back at the customer's activity to use it as input to their recommendations.</span></span>
   
   :::image type="content" source="media/product-recommendation-model-preferences.png" alt-text="Produktuaren gomendio-ereduaren eredu-hobespenak.":::

1. <span data-ttu-id="0b5bb-191">Aukeratu **Beharrezko datuak** eta hautatu **Gehitu datuak** erosketen historiarako.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-191">Select **Required data** and select **Add data** for purchase history.</span></span>

1. <span data-ttu-id="0b5bb-192">Gehitu **merkataritza elektronikoko erosketak: elektronikoa** entitatea eta esleitu elektronikoko eremuak ereduak eskatzen dituen eremuetara.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-192">Add the **eCommercePurchases : eCommerce** entity and map the fields from eCommerce to the corresponding fields required by the model.</span></span>

1. <span data-ttu-id="0b5bb-193">Sartu **merkataritza elektroniko erosketak: merkataritza elektronikoa** entitatera **merkataritza elektroniko kontaktuak: merkataritza elektronikoa** entitatearekin.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-193">Join the **eCommercePurchases : eCommerce** entity with **eCommerceContacts : eCommerce**.</span></span>

   ![Sartu merkataritza elektronikoko entitateetan.](media/model-purchase-join.png)

1. <span data-ttu-id="0b5bb-195">Aukeratu **Hurrengoa** ereduaren antolaketa ezartzeko.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-195">Select **Next** to set the model schedule.</span></span>

   <span data-ttu-id="0b5bb-196">Ereduak aldizka trebatu behar du eredu berriak ikasteko datu berriak sartzen direnean.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-196">The model needs to train regularly to learn new patterns when there is new data ingested.</span></span> <span data-ttu-id="0b5bb-197">Adibide honetarako, hautatu **hilero**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-197">For this example, select **Monthly**.</span></span>

1. <span data-ttu-id="0b5bb-198">Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-198">After reviewing all the details, select **Save and Run**.</span></span>


## <a name="task-4---review-model-results-and-explanations"></a><span data-ttu-id="0b5bb-199">4. zeregina - Berrikusi ereduen emaitzak eta azalpenak</span><span class="sxs-lookup"><span data-stu-id="0b5bb-199">Task 4 - Review model results and explanations</span></span>

<span data-ttu-id="0b5bb-200">Ereduak datuen prestakuntza eta puntuazioa osatuko ditu.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-200">Let the model complete the training and scoring of the data.</span></span> <span data-ttu-id="0b5bb-201">Produktuak gomendatzeko ereduaren azalpenak berrikus ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-201">You can now review the product recommendation model explanations.</span></span> <span data-ttu-id="0b5bb-202">Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-subscription-churn.md#review-a-prediction-status-and-results).</span><span class="sxs-lookup"><span data-stu-id="0b5bb-202">For more information, see [Review a prediction status and results](predict-subscription-churn.md#review-a-prediction-status-and-results).</span></span>

## <a name="task-5---create-a-segment-of-high-purchased-products"></a><span data-ttu-id="0b5bb-203">5. zeregina: sortu erositako produktuen segmentu bat</span><span class="sxs-lookup"><span data-stu-id="0b5bb-203">Task 5 - Create a segment of high purchased products</span></span>

<span data-ttu-id="0b5bb-204">Ekoizpen eredua martxan jartzeak hemen ikus dezakezun entitate berri bat sortzen du: **Datuak** > **Entitateak**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-204">Running the production model creates a new entity that you can see in **Data** > **Entities**.</span></span>

<span data-ttu-id="0b5bb-205">Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-205">You can create a new segment based on the entity created by the model.</span></span>

1. <span data-ttu-id="0b5bb-206">Joan hona: **Segmentuak**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-206">Go to **Segments**.</span></span> <span data-ttu-id="0b5bb-207">Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**.</span><span class="sxs-lookup"><span data-stu-id="0b5bb-207">Select **New** and choose **Create from** > **Intelligence**.</span></span>

   ![Ereduaren irteerarekin segmentu bat sortzea.](media/segment-intelligence.png)

1. <span data-ttu-id="0b5bb-209">Aukeratu **OOBProductRecommendationModelPrediction** amaiera-puntua eta definitu segmentua:</span><span class="sxs-lookup"><span data-stu-id="0b5bb-209">Select the **OOBProductRecommendationModelPrediction** endpoint and define the segment:</span></span>

   - <span data-ttu-id="0b5bb-210">Eremua: ProductID</span><span class="sxs-lookup"><span data-stu-id="0b5bb-210">Field: ProductID</span></span>
   - <span data-ttu-id="0b5bb-211">Eragilea: balioa</span><span class="sxs-lookup"><span data-stu-id="0b5bb-211">Operator: Value</span></span>
   - <span data-ttu-id="0b5bb-212">Balioa: hautatu produktuaren hiru ID nagusiak</span><span class="sxs-lookup"><span data-stu-id="0b5bb-212">Value: Select the top three product IDs</span></span>

   :::image type="content" source="media/product-recommendation-quick-segment.png" alt-text="Sortu segmentu bat ereduaren emaitzetatik.":::

<span data-ttu-id="0b5bb-214">Gomendatutako hiru produktuak erosteko prest dauden bezeroak identifikatzen dituen segmentu dinamikoki eguneratua duzu orain</span><span class="sxs-lookup"><span data-stu-id="0b5bb-214">You now have a segment that is dynamically updated which identifies the customers who are more willing to purchase the three most recommended products</span></span> 

<span data-ttu-id="0b5bb-215">Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).</span><span class="sxs-lookup"><span data-stu-id="0b5bb-215">For more information, see [Create and manage segments](segments.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
