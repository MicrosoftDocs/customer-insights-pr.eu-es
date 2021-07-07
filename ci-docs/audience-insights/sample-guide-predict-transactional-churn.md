---
title: Transakzioen galera-tasaren iragarpenari buruzko adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen transakzioen galera-tasaren iragarpen-eredua probatzeko.
ms.date: 11/19/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: diegogranados117
ms.author: digranad
manager: shellyha
ms.openlocfilehash: 49dad45c951f3c00d77ddd99faec48bfccada8b0
ms.sourcegitcommit: 0b754d194d765afef70d1008db7b347dd1f0ee40
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306105"
---
# <a name="transactional-churn-prediction-preview-sample-guide"></a><span data-ttu-id="2a9bf-103">Transakzioen galera-tasaren iragarpenari (aurrebista) buruzko adibide-gida</span><span class="sxs-lookup"><span data-stu-id="2a9bf-103">Transactional churn prediction (preview) sample guide</span></span>

<span data-ttu-id="2a9bf-104">Gida honek Customer Insights zerbitzuko transakzioen galera-tasaren iragarpenaren adibide oso bat aurkeztuko dizu, jarraian emandako datuak erabilita.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-104">This guide will walk you through an end to end example of Transactional Churn prediction in Customer Insights using the data provided below.</span></span> <span data-ttu-id="2a9bf-105">Gida honetan erabilitako datu guztiak ez dira bezeroen benetako datuak eta Contoso datu-basean aurkitu da *Demo* ingurunea zure Customer Insights harpidetzaren barruan.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-105">All data used in this guide is not real customer data and is part of the Contoso dataset found in the *Demo* environment within your Customer Insights Subscription.</span></span>

## <a name="scenario"></a><span data-ttu-id="2a9bf-106">Egoera</span><span class="sxs-lookup"><span data-stu-id="2a9bf-106">Scenario</span></span>

<span data-ttu-id="2a9bf-107">Contoso kalitate handiko kafea eta kafe makinak ekoizten dituen enpresa da eta Contoso Coffee webgunearen bidez saltzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-107">Contoso is a company that produces high-quality coffee and coffee machines, which they sell through their Contoso Coffee website.</span></span> <span data-ttu-id="2a9bf-108">Enpresaren helburua da jakitea egunerokotasunean bere produktuak erosten dituzten bezeroetako nortzuk utziko dioten bezero aktibo izateari datozen 60 egunetan.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-108">Their goal is to know which customers who typically purchase their products on a regular basis, will stop being active customers in the next 60 days.</span></span> <span data-ttu-id="2a9bf-109">Zein bezero **galtzeko arriskua** dagoen jakiteak marketinarekin erlazionatutako ahalegina bideratzen lagun diezaioke enpresari, arreta bezero horiengan jarrita.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-109">Knowing which of their customers is **likely to churn**, can help them save marketing efforts by focusing on keeping them.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2a9bf-110">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="2a9bf-110">Prerequisites</span></span>

- <span data-ttu-id="2a9bf-111">Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-111">At least [Contributor permissions](permissions.md) in Customer Insights.</span></span>
- <span data-ttu-id="2a9bf-112">Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-112">We recommend that you implement the following steps [in a new environment](manage-environments.md).</span></span>

## <a name="task-1---ingest-data"></a><span data-ttu-id="2a9bf-113">1. zeregina - Datuen sarrera</span><span class="sxs-lookup"><span data-stu-id="2a9bf-113">Task 1 - Ingest data</span></span>

<span data-ttu-id="2a9bf-114">Berrikusi zehazki [datuen sarrerari](data-sources.md) eta [Power Query konektoreak erabiliz datu-iturburuak inportatzeari](connect-power-query.md) buruzko artikuluak.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-114">Review the articles [about data ingestion](data-sources.md) and [importing data sources using Power Query connectors](connect-power-query.md) specifically.</span></span> <span data-ttu-id="2a9bf-115">Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-115">The following information assumes you familiarized with ingesting data in general.</span></span> 

### <a name="ingest-customer-data-from-ecommerce-platform"></a><span data-ttu-id="2a9bf-116">Sartu bezero-datuak merkataritza elektronikoko plataformatik</span><span class="sxs-lookup"><span data-stu-id="2a9bf-116">Ingest customer data from eCommerce platform</span></span>

1. <span data-ttu-id="2a9bf-117">Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-117">Create a data source named **eCommerce**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="2a9bf-118">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscontacts.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-118">Enter the URL for eCommerce contacts https://aka.ms/ciadclasscontacts.</span></span>

1. <span data-ttu-id="2a9bf-119">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-119">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="2a9bf-120">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="2a9bf-120">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="2a9bf-121">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="2a9bf-121">**DateOfBirth**: Date</span></span>
   - <span data-ttu-id="2a9bf-122">**Sorrera-data**: Data/ordua/zona</span><span class="sxs-lookup"><span data-stu-id="2a9bf-122">**CreatedOn**: Date/Time/Zone</span></span>

   [!div class="mx-imgBorder"]
   <span data-ttu-id="2a9bf-123">![Bihurtu jaioteguna data](media/ecommerce-dob-date.PNG "eraldatu jaiotze data datara")</span><span class="sxs-lookup"><span data-stu-id="2a9bf-123">![Transform DoB to Date](media/ecommerce-dob-date.PNG "transform date of birth to date")</span></span>

1. <span data-ttu-id="2a9bf-124">Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-124">In the **Name** field on the right-hand pane, rename your data source from **Query** to **eCommerceContacts**</span></span>

1. <span data-ttu-id="2a9bf-125">Gorde datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-125">Save the data source.</span></span>

### <a name="ingest-online-purchase-data"></a><span data-ttu-id="2a9bf-126">Sartu sareko erosketen datuak</span><span class="sxs-lookup"><span data-stu-id="2a9bf-126">Ingest online purchase data</span></span>

1. <span data-ttu-id="2a9bf-127">Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-127">Add another data set to the same **eCommerce** data source.</span></span> <span data-ttu-id="2a9bf-128">Aukeratu **Testua/CSV** konektorea berriro.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-128">Choose the **Text/CSV** connector again.</span></span>

1. <span data-ttu-id="2a9bf-129">Idatzi **sareko erosketen** datuen URLa: https://aka.ms/ciadclassonline.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-129">Enter the URL for **Online Purchases** data https://aka.ms/ciadclassonline.</span></span>

1. <span data-ttu-id="2a9bf-130">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-130">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="2a9bf-131">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="2a9bf-131">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="2a9bf-132">**PurchasedOn**: Data/ordua</span><span class="sxs-lookup"><span data-stu-id="2a9bf-132">**PurchasedOn**: Date/Time</span></span>
   - <span data-ttu-id="2a9bf-133">**TotalPrice**: Moneta</span><span class="sxs-lookup"><span data-stu-id="2a9bf-133">**TotalPrice**: Currency</span></span>
   
1. <span data-ttu-id="2a9bf-134">Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommercePurchases**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-134">In the **Name** field on the right-hand pane, rename your data source from **Query** to **eCommercePurchases**.</span></span>

1. <span data-ttu-id="2a9bf-135">Gorde datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-135">Save the data source.</span></span>

### <a name="ingest-customer-data-from-loyalty-schema"></a><span data-ttu-id="2a9bf-136">Sartu bezero-datuak fideltasun-eskematik</span><span class="sxs-lookup"><span data-stu-id="2a9bf-136">Ingest customer data from loyalty schema</span></span>

1. <span data-ttu-id="2a9bf-137">Sortu **LoyaltyScheme** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-137">Create a data source named **LoyaltyScheme**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="2a9bf-138">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscustomerloyalty.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-138">Enter the URL for eCommerce contacts https://aka.ms/ciadclasscustomerloyalty.</span></span>

1. <span data-ttu-id="2a9bf-139">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-139">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="2a9bf-140">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="2a9bf-140">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="2a9bf-141">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="2a9bf-141">**DateOfBirth**: Date</span></span>
   - <span data-ttu-id="2a9bf-142">**RewardsPoints**: Zenbaki osoa</span><span class="sxs-lookup"><span data-stu-id="2a9bf-142">**RewardsPoints**: Whole Number</span></span>
   - <span data-ttu-id="2a9bf-143">**Sorrera-data**: Data/ordua</span><span class="sxs-lookup"><span data-stu-id="2a9bf-143">**CreatedOn**: Date/Time</span></span>

1. <span data-ttu-id="2a9bf-144">Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-144">In the **Name** field on the right-hand pane, rename your data source from **Query** to **loyCustomers**.</span></span>

1. <span data-ttu-id="2a9bf-145">Gorde datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-145">Save the data source.</span></span>


## <a name="task-2---data-unification"></a><span data-ttu-id="2a9bf-146">2. zeregina - Datuen bateratzea</span><span class="sxs-lookup"><span data-stu-id="2a9bf-146">Task 2 - Data unification</span></span>

<span data-ttu-id="2a9bf-147">Behin datuak sartuta, **Esleitu, bat etorri, konbinatu** prozesuarekin hasiko gara, bezeroaren profil bateratu bat sortzeko.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-147">After ingesting the data we now begin the **Map, Match, Merge** process to create a unified customer profile.</span></span> <span data-ttu-id="2a9bf-148">Informazio gehiago lortzeko, ikusi [Datuen bateratzea](data-unification.md).</span><span class="sxs-lookup"><span data-stu-id="2a9bf-148">For more information, see [Data unification](data-unification.md).</span></span>

### <a name="map"></a><span data-ttu-id="2a9bf-149">Esleitu</span><span class="sxs-lookup"><span data-stu-id="2a9bf-149">Map</span></span>

1. <span data-ttu-id="2a9bf-150">Behin datuak sartuta, esleitu merkataritza elektronikoko eta fideltasun-datuetako kontaktuak ohiko datu motei.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-150">After ingesting the data, map contacts from eCommerce and Loyalty data to common data types.</span></span> <span data-ttu-id="2a9bf-151">Joan hona: **Datuak** > **Bateratu** > **Esleitu**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-151">Go to **Data** > **Unify** > **Map**.</span></span>

1. <span data-ttu-id="2a9bf-152">Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-152">Select the entities that represent the customer profile – **eCommerceContacts** and **loyCustomers**.</span></span> 

   :::image type="content" source="media/unify-ecommerce-loyalty.PNG" alt-text="bateratu ecommerce eta loyalty datu-iturburuak.":::

1. <span data-ttu-id="2a9bf-154">Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-154">Select **ContactId** as the primary key for **eCommerceContacts** and **LoyaltyID** as the primary key for **loyCustomers**.</span></span>

   :::image type="content" source="media/unify-loyaltyid.PNG" alt-text="Bateratu LoyaltyId gako nagusi gisa.":::

### <a name="match"></a><span data-ttu-id="2a9bf-156">Lotu</span><span class="sxs-lookup"><span data-stu-id="2a9bf-156">Match</span></span>

1. <span data-ttu-id="2a9bf-157">Joan **Bat etorri** fitxara eta hautatu **Ezarri ordena**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-157">Go to the **Match** tab and select **Set Order**.</span></span>

1. <span data-ttu-id="2a9bf-158">Urtean **Lehen Hezkuntza** goitibeherako zerrenda, aukeratu **eCommerceContacts: eCommerce** iturri nagusi gisa eta erregistro guztiak barne.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-158">In the **Primary** dropdown list, choose **eCommerceContacts : eCommerce** as the primary source and include all records.</span></span>

1. <span data-ttu-id="2a9bf-159">Urtean **2. entitatea** goitibeherako zerrenda, aukeratu **loyCustomers: LoyaltyScheme** eta erregistro guztiak sartu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-159">In the **Entity 2** dropdown list, choose **loyCustomers : LoyaltyScheme** and include all records.</span></span>

   :::image type="content" source="media/unify-match-order.PNG" alt-text="Bateratu eCommerce eta Loyalty bat-etortzea.":::

1. <span data-ttu-id="2a9bf-161">Hautatu **Sortu beste arau bat**</span><span class="sxs-lookup"><span data-stu-id="2a9bf-161">Select **Create a new rule**</span></span>

1. <span data-ttu-id="2a9bf-162">Gehitu lehenengo baldintza FullName erabilita.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-162">Add your first condition using FullName.</span></span>

   * <span data-ttu-id="2a9bf-163">ECommerceContacts aukeratzeko **Izen abizenak** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-163">For eCommerceContacts select **FullName** in the dropdown.</span></span>
   * <span data-ttu-id="2a9bf-164">loyCustomers aukeratzeko **Izen abizenak** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-164">For loyCustomers select **FullName** in the dropdown.</span></span>
   * <span data-ttu-id="2a9bf-165">Aukeratu **Normalizatu** goitibeherako zerrendan eta aukeratu **Mota (Telefonoa, Izena, Helbidea, ...)**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-165">Select the **Normalize** drop down and choose **Type (Phone, Name, Address, ...)**.</span></span>
   * <span data-ttu-id="2a9bf-166">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-166">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

1. <span data-ttu-id="2a9bf-167">Idatzi arau berriaren **Izen osoa, posta elektronikoa** izena.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-167">Enter the name **FullName, Email** for the new rule.</span></span>

   * <span data-ttu-id="2a9bf-168">Gehitu helbide elektronikoaren bigarren baldintza bat **Gehitu baldintza** hautatuta</span><span class="sxs-lookup"><span data-stu-id="2a9bf-168">Add a second condition for email address by selecting **Add Condition**</span></span>
   * <span data-ttu-id="2a9bf-169">ECommerceContacts entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-169">For entity eCommerceContacts, choose **EMail** in dropdown.</span></span>
   * <span data-ttu-id="2a9bf-170">loyCustomers entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-170">For entity loyCustomers, choose **EMail** in the dropdown.</span></span> 
   * <span data-ttu-id="2a9bf-171">"Normalizatu" hutsik utzi.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-171">Leave Normalize blank.</span></span> 
   * <span data-ttu-id="2a9bf-172">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-172">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

   :::image type="content" source="media/unify-match-rule.PNG" alt-text="Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.":::

7. <span data-ttu-id="2a9bf-174">Hautatu **gorde** eta **exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-174">Select **Save** and **Run**.</span></span>

### <a name="merge"></a><span data-ttu-id="2a9bf-175">Konbinazioa</span><span class="sxs-lookup"><span data-stu-id="2a9bf-175">Merge</span></span>

1. <span data-ttu-id="2a9bf-176">Joan **konbinatu** fitxara.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-176">Go to the **Merge** tab.</span></span>

1. <span data-ttu-id="2a9bf-177">**loyCustomers** entitatearen **Kontaktuaren IDa** atalean, aldatu bistaratzeko izena **ContactIdLOYALTY** izenera, sartutako beste IDetatik bereizteko.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-177">On the **ContactId** for **loyCustomers** entity, change the display name to **ContactIdLOYALTY** to differentiate it from the other IDs ingested.</span></span>

   :::image type="content" source="media/unify-merge-contactid.PNG" alt-text="aldatu leialtasun IDaren kontaktuaren IDa.":::

1. <span data-ttu-id="2a9bf-179">Aukeratu **Gorde** eta **exekutatu** konbinatzeko prozesua hasteko.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-179">Select **Save** and **Run** to start the Merge Process.</span></span>



## <a name="task-3---configure-transaction-churn-prediction"></a><span data-ttu-id="2a9bf-180">3. zeregina - Konfiguratu transakzioen galera-tasaren iragarpena</span><span class="sxs-lookup"><span data-stu-id="2a9bf-180">Task 3 - Configure transaction churn prediction</span></span>

<span data-ttu-id="2a9bf-181">Bezeroen profil bateratuak behar bezala jarrita, harpidetzaren galera-tasaren iragarpena exekutatu dezakegu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-181">With the unified customer profiles in place, we can now run the subscription churn prediction.</span></span> <span data-ttu-id="2a9bf-182">Urrats zehatzetarako, ikusi [Harpidetzaren galera-tasaren iragarpena (aurrebista)](predict-subscription-churn.md) artikulu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-182">For detailed steps, see the [Subscription churn prediction (preview)](predict-subscription-churn.md) article.</span></span> 

1. <span data-ttu-id="2a9bf-183">Joan **Adimena** > **Ezagutu** atalera eta hautatu **Bezeroen galera-tasaren eredua**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-183">Go to **Intelligence** > **Discover** and select to use the **Customer churn model**.</span></span>

1. <span data-ttu-id="2a9bf-184">Aukeratu **Transakzionala** aukera eta hautatu **Hasi**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-184">Select the **Transactional** option and select **Get started**.</span></span>

1. <span data-ttu-id="2a9bf-185">Eman **OOB eCommerce transakzioen galera-tasaren iragarpena** izena ereduari eta **OOBeCommerceChurnPrediction** irteerako entitateari.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-185">Name the model **OOB eCommerce Transaction Churn Prediction** and the output entity **OOBeCommerceChurnPrediction**.</span></span>

1. <span data-ttu-id="2a9bf-186">Definitu galera-tasaren ereduaren bi baldintza:</span><span class="sxs-lookup"><span data-stu-id="2a9bf-186">Define two conditions for the churn model:</span></span>

   * <span data-ttu-id="2a9bf-187">**Iragarpen leihoa**: **gutxienez 60** egun.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-187">**Prediction window**: **at least 60** days.</span></span> <span data-ttu-id="2a9bf-188">Ezarpen honek definitzen du etorkizunean noraino iragarri nahi dugun bezeroaren galera-tasa.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-188">This setting defines how far into the future do we want to predict customer churn.</span></span>

   * <span data-ttu-id="2a9bf-189">**Bezeroen galera-tasaren definizioa** : **gutxienez 60** egun.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-189">**Churn definition**: **at least 60** days.</span></span> <span data-ttu-id="2a9bf-190">Erosketa gabeko iraupena, bezero bat galdutzat hartu ondoren.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-190">The duration without purchase after which a customer is considered churned.</span></span>

     :::image type="content" source="media/model-levers.PNG" alt-text="Aukeratu iragarpen-leihoa eta galera-tasaren definizioa ereduaren mailakatzaileak.":::

1. <span data-ttu-id="2a9bf-192">Aukeratu **Erosketen historia (beharrezkoa)** eta hautatu **Gehitu datuak** erosketen historiarako.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-192">Select **Purchase History (required)** and select **Add data** for purchase history.</span></span>

1. <span data-ttu-id="2a9bf-193">Gehitu **merkataritza elektronikoko erosketak: elektronikoa** entitatea eta esleitu elektronikoko eremuak ereduak eskatzen dituen eremuetara.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-193">Add the **eCommercePurchases : eCommerce** entity and map the fields from eCommerce to the corresponding fields required by the model.</span></span>

1. <span data-ttu-id="2a9bf-194">Sartu **merkataritza elektroniko erosketak: merkataritza elektronikoa** entitatera **merkataritza elektroniko kontaktuak: merkataritza elektronikoa** entitatearekin.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-194">Join the **eCommercePurchases : eCommerce** entity with **eCommerceContacts : eCommerce**.</span></span>

   :::image type="content" source="media/model-purchase-join.PNG" alt-text="Sartu merkataritza elektronikoko entitateetan.":::

1. <span data-ttu-id="2a9bf-196">Aukeratu **Hurrengoa** ereduaren antolaketa ezartzeko.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-196">Select **Next** to set the model schedule.</span></span>

   <span data-ttu-id="2a9bf-197">Ereduak aldizka trebatu behar du eredu berriak ikasteko datu berriak sartzen direnean.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-197">The model needs to train regularly to learn new patterns when there is new data ingested.</span></span> <span data-ttu-id="2a9bf-198">Adibide honetarako, hautatu **hilero**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-198">For this example, select **Monthly**.</span></span>

1. <span data-ttu-id="2a9bf-199">Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-199">After reviewing all the details, select **Save and Run**.</span></span>

## <a name="task-4---review-model-results-and-explanations"></a><span data-ttu-id="2a9bf-200">4. zeregina - Berrikusi ereduen emaitzak eta azalpenak</span><span class="sxs-lookup"><span data-stu-id="2a9bf-200">Task 4 - Review model results and explanations</span></span>

<span data-ttu-id="2a9bf-201">Ereduak datuen prestakuntza eta puntuazioa osatuko ditu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-201">Let the model complete the training and scoring of the data.</span></span> <span data-ttu-id="2a9bf-202">Harpidetzen galera-tasaren ereduaren azalpenak berrikus ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-202">You can now review the subscription churn model explanations.</span></span> <span data-ttu-id="2a9bf-203">Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-subscription-churn.md#review-a-prediction-status-and-results).</span><span class="sxs-lookup"><span data-stu-id="2a9bf-203">For more information, see [Review a prediction status and results](predict-subscription-churn.md#review-a-prediction-status-and-results).</span></span>

## <a name="task-5---create-a-segment-of-high-churn-risk-customers"></a><span data-ttu-id="2a9bf-204">5. zeregina - Sortu galera-arrisku handiko bezeroen segmentu bat</span><span class="sxs-lookup"><span data-stu-id="2a9bf-204">Task 5 - Create a segment of high churn-risk customers</span></span>

<span data-ttu-id="2a9bf-205">Ekoizpen eredua martxan jartzeak hemen ikus dezakezun entitate berri bat sortzen du: **Datuak** > **Entitateak**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-205">Running the production model creates a new entity that you can see in **Data** > **Entities**.</span></span>   

<span data-ttu-id="2a9bf-206">Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-206">You can create a new segment based on the entity created by the model.</span></span>

1.  <span data-ttu-id="2a9bf-207">Joan hona: **Segmentuak**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-207">Go to **Segments**.</span></span> <span data-ttu-id="2a9bf-208">Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-208">Select **New** and choose **Create from** > **Intelligence**.</span></span> 

   :::image type="content" source="media/segment-intelligence.PNG" alt-text="Ereduaren irteerarekin segmentu bat sortzea.":::

1. <span data-ttu-id="2a9bf-210">Aukeratu **OOBSubscriptionChurnPrediction** amaiera-puntua eta definitu segmentua:</span><span class="sxs-lookup"><span data-stu-id="2a9bf-210">Select the **OOBSubscriptionChurnPrediction** endpoint and define the segment:</span></span> 
   - <span data-ttu-id="2a9bf-211">Eremua: ChurnScore</span><span class="sxs-lookup"><span data-stu-id="2a9bf-211">Field: ChurnScore</span></span>
   - <span data-ttu-id="2a9bf-212">Eragilea: hau baino handiagoa</span><span class="sxs-lookup"><span data-stu-id="2a9bf-212">Operator: greater than</span></span>
   - <span data-ttu-id="2a9bf-213">Balioa: 0.6</span><span class="sxs-lookup"><span data-stu-id="2a9bf-213">Value: 0.6</span></span>
   
   :::image type="content" source="media/segment-setup-subs.PNG" alt-text="Konfiguratu harpidetzaren galera-tasaren segmentua.":::

<span data-ttu-id="2a9bf-215">Harpidetza-negozio honen galera-arrisku handiko bezeroak identifikatzen dituen segmentu dinamikoki eguneratua duzu.</span><span class="sxs-lookup"><span data-stu-id="2a9bf-215">You now have a segment that is dynamically updated which identifies high churn-risk customers for this subscription business.</span></span>

<span data-ttu-id="2a9bf-216">Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).</span><span class="sxs-lookup"><span data-stu-id="2a9bf-216">For more information, see [Create and manage segments](segments.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]