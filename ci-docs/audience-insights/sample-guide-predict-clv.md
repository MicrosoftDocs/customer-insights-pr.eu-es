---
title: Bezeroaren bizi-iraupenaren balioa iragarpenaren lagin gida
description: Erabili lagin gida hau bezeroaren bizi-iraupenaren balio osorako iragarpen modeloa probatzeko.
ms.date: 05/25/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: yashlundia
ms.author: yalundia
manager: shellyha
ms.openlocfilehash: 19c1fbadb79ba22c0dc11aa7c3b5b2415add70a7
ms.sourcegitcommit: 0b754d194d765afef70d1008db7b347dd1f0ee40
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306334"
---
# <a name="customer-lifetime-value-clv-prediction-sample-guide"></a><span data-ttu-id="5e37d-103">Bezeroaren bizi-iraupenaren balioaren iragarpenaren lagin gida</span><span class="sxs-lookup"><span data-stu-id="5e37d-103">Customer lifetime value (CLV) prediction sample guide</span></span>

<span data-ttu-id="5e37d-104">Gida honek Bezeroaren bizi-iraupenaren balio osoko (CLV) iragarpen adibidearen amaierako adibidea azalduko dizu Customer Insights-en, lagin-datuak erabiliz.</span><span class="sxs-lookup"><span data-stu-id="5e37d-104">This guide will walk you through an end to end example of Customer lifetime value (CLV) prediction in Customer Insights using sample data.</span></span>

## <a name="scenario"></a><span data-ttu-id="5e37d-105">Egoera</span><span class="sxs-lookup"><span data-stu-id="5e37d-105">Scenario</span></span>

<span data-ttu-id="5e37d-106">Contoso kalitate handiko kafea eta kafe makinak ekoizten dituen enpresa da.</span><span class="sxs-lookup"><span data-stu-id="5e37d-106">Contoso is a company that produces high-quality coffee and coffee machines.</span></span> <span data-ttu-id="5e37d-107">Produktuak Contoso Coffee webgunearen bidez saltzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="5e37d-107">They sell the products through their Contoso Coffee website.</span></span> <span data-ttu-id="5e37d-108">Konpainiak bezeroek hurrengo 12 hilabeteetan sor dezaketen balioa (diru-sarrerak) ulertu nahi du.</span><span class="sxs-lookup"><span data-stu-id="5e37d-108">The company wants to understand the value (revenue) that their customers can generate in the next 12 months.</span></span> <span data-ttu-id="5e37d-109">Datozen 12 hilabeteetan bezeroek espero duten balioa ezagutzeak balio handiko bezeroenganako marketin ahalegina bideratzen lagunduko die.</span><span class="sxs-lookup"><span data-stu-id="5e37d-109">Knowing the expected value of their customers in the next 12 months will help them steer their marketing efforts on high value customers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5e37d-110">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="5e37d-110">Prerequisites</span></span>

- <span data-ttu-id="5e37d-111">Gutxienez [Laguntzailearen baimenak](permissions.md) hartzaileen xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="5e37d-111">At least [Contributor permissions](permissions.md) in audience insights.</span></span>
- <span data-ttu-id="5e37d-112">Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.</span><span class="sxs-lookup"><span data-stu-id="5e37d-112">We recommend that you implement the following steps [in a new environment](manage-environments.md).</span></span>

## <a name="task-1---ingest-data"></a><span data-ttu-id="5e37d-113">1. zeregina - Datuen sarrera</span><span class="sxs-lookup"><span data-stu-id="5e37d-113">Task 1 - Ingest data</span></span>

<span data-ttu-id="5e37d-114">Errepasatu [datuen irensteari](data-sources.md) eta [datu iturriak Power Query konektoreen bidez inportatzeari](connect-power-query.md) buruzko artikuluak.</span><span class="sxs-lookup"><span data-stu-id="5e37d-114">Review the articles [about data ingestion](data-sources.md) and [importing data sources using Power Query connectors](connect-power-query.md).</span></span> <span data-ttu-id="5e37d-115">Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.</span><span class="sxs-lookup"><span data-stu-id="5e37d-115">The following information assumes you familiarized with ingesting data in general.</span></span>

### <a name="ingest-customer-data-from-ecommerce-platform"></a><span data-ttu-id="5e37d-116">Sartu bezero-datuak merkataritza elektronikoko plataformatik</span><span class="sxs-lookup"><span data-stu-id="5e37d-116">Ingest customer data from eCommerce platform</span></span>

1. <span data-ttu-id="5e37d-117">Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="5e37d-117">Create a data source named  **eCommerce** , choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="5e37d-118">Idatzi merkataritza elektronikoko kontaktuen URLa [https://aka.ms/ciadclasscontacts](https://aka.ms/ciadclasscontacts).</span><span class="sxs-lookup"><span data-stu-id="5e37d-118">Enter the URL for eCommerce contacts [https://aka.ms/ciadclasscontacts](https://aka.ms/ciadclasscontacts).</span></span>

1. <span data-ttu-id="5e37d-119">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-119">While editing the data, select  **Transform**  and then  **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="5e37d-120">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="5e37d-120">Update the datatype for the columns listed below:</span></span>
   - <span data-ttu-id="5e37d-121">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="5e37d-121">**DateOfBirth** : Date</span></span>
   - <span data-ttu-id="5e37d-122">**Sorrera-data**: Data/ordua/zona</span><span class="sxs-lookup"><span data-stu-id="5e37d-122">**CreatedOn** : Date/Time/Zone</span></span>

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

1. <span data-ttu-id="5e37d-124">Eskuinaldeko paneleko "Izena" eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**</span><span class="sxs-lookup"><span data-stu-id="5e37d-124">In the 'Name' field on the right-hand pane, rename your data source from **Query** to **eCommerceContacts**</span></span>

1. <span data-ttu-id="5e37d-125">**Gorde** datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="5e37d-125">**Save** the data source.</span></span>

### <a name="ingest-online-purchase-data"></a><span data-ttu-id="5e37d-126">Sartu sareko erosketen datuak</span><span class="sxs-lookup"><span data-stu-id="5e37d-126">Ingest online purchase data</span></span>

1. <span data-ttu-id="5e37d-127">Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera.</span><span class="sxs-lookup"><span data-stu-id="5e37d-127">Add another data set to the same **eCommerce** data source.</span></span> <span data-ttu-id="5e37d-128">Aukeratu **Testua/CSV** konektorea berriro.</span><span class="sxs-lookup"><span data-stu-id="5e37d-128">Choose the **Text/CSV** connector again.</span></span>

1. <span data-ttu-id="5e37d-129">Idatzi **sareko erosketen** datuen URLa: https://aka.ms/ciadclassonline.</span><span class="sxs-lookup"><span data-stu-id="5e37d-129">Enter the URL for **Online Purchases** data https://aka.ms/ciadclassonline.</span></span>

1. <span data-ttu-id="5e37d-130">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-130">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="5e37d-131">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="5e37d-131">Update the datatype for the columns listed below:</span></span>
   - <span data-ttu-id="5e37d-132">**PurchasedOn**: Data/ordua</span><span class="sxs-lookup"><span data-stu-id="5e37d-132">**PurchasedOn**: Date/Time</span></span>
   - <span data-ttu-id="5e37d-133">**TotalPrice**: Moneta</span><span class="sxs-lookup"><span data-stu-id="5e37d-133">**TotalPrice**: Currency</span></span>

1. <span data-ttu-id="5e37d-134">Alboko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommercePurchases**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-134">In the **Name** field on the side pane, rename your data source from **Query** to **eCommercePurchases**.</span></span>

1. <span data-ttu-id="5e37d-135">**Gorde** datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="5e37d-135">**Save** the data source.</span></span>

### <a name="ingest-customer-data-from-loyalty-schema"></a><span data-ttu-id="5e37d-136">Sartu bezero-datuak fideltasun-eskematik</span><span class="sxs-lookup"><span data-stu-id="5e37d-136">Ingest customer data from loyalty schema</span></span>

1. <span data-ttu-id="5e37d-137">Sortu **LoyaltyScheme** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="5e37d-137">Create a data source named **LoyaltyScheme**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="5e37d-138">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscustomerloyalty.</span><span class="sxs-lookup"><span data-stu-id="5e37d-138">Enter the URL for eCommerce contacts https://aka.ms/ciadclasscustomerloyalty.</span></span>

1. <span data-ttu-id="5e37d-139">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-139">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="5e37d-140">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="5e37d-140">Update the datatype for the columns listed below:</span></span>
   - <span data-ttu-id="5e37d-141">**Jaioteguna**: Data</span><span class="sxs-lookup"><span data-stu-id="5e37d-141">**DateOfBirth**: Date</span></span>
   - <span data-ttu-id="5e37d-142">**RewardsPoints**: Zenbaki osoa</span><span class="sxs-lookup"><span data-stu-id="5e37d-142">**RewardsPoints**: Whole Number</span></span>
   - <span data-ttu-id="5e37d-143">**Sorrera-data**: Data/ordua</span><span class="sxs-lookup"><span data-stu-id="5e37d-143">**CreatedOn**: Date/Time</span></span>

1. <span data-ttu-id="5e37d-144">Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-144">In the **Name** field on the right-hand pane, rename your data source from **Query** to **loyCustomers**.</span></span>

1. <span data-ttu-id="5e37d-145">**Gorde** datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="5e37d-145">**Save** the data source.</span></span>

### <a name="ingest-customer-data-from-website-reviews"></a><span data-ttu-id="5e37d-146">Sartu bezeroaren datuak webguneen berrikuspenetatik</span><span class="sxs-lookup"><span data-stu-id="5e37d-146">Ingest customer data from website reviews</span></span>

1. <span data-ttu-id="5e37d-147">Sortu **Webgunea** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua / CSV** konektorea.</span><span class="sxs-lookup"><span data-stu-id="5e37d-147">Create a data source named **Website**, choose the import option, and select the **Text/CSV** connector.</span></span>

1. <span data-ttu-id="5e37d-148">Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/CI-ILT/WebReviews.</span><span class="sxs-lookup"><span data-stu-id="5e37d-148">Enter the URL for eCommerce contacts https://aka.ms/CI-ILT/WebReviews.</span></span>

1. <span data-ttu-id="5e37d-149">Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-149">While editing the data, select **Transform** and then **Use First Row as Headers**.</span></span>

1. <span data-ttu-id="5e37d-150">Eguneratu jarraian zerrendatutako zutabeen datu motak:</span><span class="sxs-lookup"><span data-stu-id="5e37d-150">Update the datatype for the columns listed below:</span></span>

   - <span data-ttu-id="5e37d-151">**ReviewRating**: zenbaki hamartarra</span><span class="sxs-lookup"><span data-stu-id="5e37d-151">**ReviewRating**: Decimal number</span></span>
   - <span data-ttu-id="5e37d-152">**Iritziaren data**: Data</span><span class="sxs-lookup"><span data-stu-id="5e37d-152">**ReviewDate**: Date</span></span>

1. <span data-ttu-id="5e37d-153">Eskuineko paneleko 'Izena' eremuan, aldatu zure datu-iturburuaren izena **Kontsulta**-tik **Iritziak**-era.</span><span class="sxs-lookup"><span data-stu-id="5e37d-153">In the 'Name' field on the right-hand pane, rename your data source from **Query** to **Reviews**.</span></span>

1. <span data-ttu-id="5e37d-154">**Gorde** datu-iturburua.</span><span class="sxs-lookup"><span data-stu-id="5e37d-154">**Save** the data source.</span></span>

## <a name="task-2---data-unification"></a><span data-ttu-id="5e37d-155">2. zeregina - Datuen bateratzea</span><span class="sxs-lookup"><span data-stu-id="5e37d-155">Task 2 - Data unification</span></span>

<span data-ttu-id="5e37d-156">Datuak irentsi ondoren, datuak bateratzeko prozesua hasten dugu bezeroaren profil bateratua sortzeko.</span><span class="sxs-lookup"><span data-stu-id="5e37d-156">After ingesting the data, we now begin the data unification process to create a unified customer profile.</span></span> <span data-ttu-id="5e37d-157">Informazio gehiago lortzeko, ikusi [Datuen bateratzea](data-unification.md).</span><span class="sxs-lookup"><span data-stu-id="5e37d-157">For more information, see [Data unification](data-unification.md).</span></span>

### <a name="map"></a><span data-ttu-id="5e37d-158">Esleitu</span><span class="sxs-lookup"><span data-stu-id="5e37d-158">Map</span></span>

1. <span data-ttu-id="5e37d-159">Behin datuak sartuta, esleitu merkataritza elektronikoko eta fideltasun-datuetako kontaktuak ohiko datu motei.</span><span class="sxs-lookup"><span data-stu-id="5e37d-159">After ingesting the data, map contacts from eCommerce and Loyalty data to common data types.</span></span> <span data-ttu-id="5e37d-160">Joan hona: **Datuak** > **Bateratu** > **Esleitu**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-160">Go to **Data** > **Unify** > **Map**.</span></span>

1. <span data-ttu-id="5e37d-161">Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-161">Select the entities that represent the customer profile – **eCommerceContacts** and **loyCustomers**.</span></span> <span data-ttu-id="5e37d-162">Ondoren, hautatu **Aplikatu**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-162">Then, select **Apply**.</span></span>

   ![bateratu ecommerce eta loyalty datu-iturburuak.](media/unify-ecommerce-loyalty.png)

1. <span data-ttu-id="5e37d-164">Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.</span><span class="sxs-lookup"><span data-stu-id="5e37d-164">Select **ContactId** as the primary key for **eCommerceContacts** and **LoyaltyID** as the primary key for **loyCustomers**.</span></span>

   ![Bateratu LoyaltyId gako nagusi gisa.](media/unify-loyaltyid.png)

1. <span data-ttu-id="5e37d-166">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-166">Select **Save**.</span></span>

### <a name="match"></a><span data-ttu-id="5e37d-167">Lotu</span><span class="sxs-lookup"><span data-stu-id="5e37d-167">Match</span></span>

1. <span data-ttu-id="5e37d-168">Joan **Bat etorri** fitxara eta hautatu **Ezarri ordena**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-168">Go to the **Match** tab and select **Set Order**.</span></span>

1. <span data-ttu-id="5e37d-169">Urtean **Lehen Hezkuntza** goitibeherako zerrenda, aukeratu **eCommerceContacts: eCommerce** iturri nagusi gisa eta erregistro guztiak barne.</span><span class="sxs-lookup"><span data-stu-id="5e37d-169">In the **Primary** dropdown list, choose **eCommerceContacts : eCommerce** as the primary source and include all records.</span></span>

1. <span data-ttu-id="5e37d-170">Urtean **2. entitatea** goitibeherako zerrenda, aukeratu **loyCustomers: LoyaltyScheme** eta erregistro guztiak sartu.</span><span class="sxs-lookup"><span data-stu-id="5e37d-170">In the **Entity 2** dropdown list, choose **loyCustomers : LoyaltyScheme** and include all records.</span></span>

   ![Bateratu eCommerce eta Loyalty bat-etortzea.](media/unify-match-order.png)

1. <span data-ttu-id="5e37d-172">Hautatu **Gehitu araua**</span><span class="sxs-lookup"><span data-stu-id="5e37d-172">Select **Add rule**</span></span>

1. <span data-ttu-id="5e37d-173">Gehitu lehenengo baldintza FullName erabilita.</span><span class="sxs-lookup"><span data-stu-id="5e37d-173">Add your first condition using FullName.</span></span>

   - <span data-ttu-id="5e37d-174">ECommerceContacts aukeratzeko **Izen abizenak** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="5e37d-174">For eCommerceContacts select **FullName** in the dropdown.</span></span>
   - <span data-ttu-id="5e37d-175">loyCustomers aukeratzeko **Izen abizenak** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="5e37d-175">For loyCustomers select **FullName** in the dropdown.</span></span>
   - <span data-ttu-id="5e37d-176">Aukeratu **Normalizatu** goitibehera eta aukeratu **Mota (Telefonoa, Izena, Helbidea, ...)**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-176">Select the **Normalize** dropdown and choose **Type (Phone, Name, Address, ...)**.</span></span>
   - <span data-ttu-id="5e37d-177">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-177">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

1. <span data-ttu-id="5e37d-178">Idatzi arau berriaren **Izen osoa, posta elektronikoa** izena.</span><span class="sxs-lookup"><span data-stu-id="5e37d-178">Enter the name **FullName, Email** for the new rule.</span></span>

   - <span data-ttu-id="5e37d-179">Gehitu helbide elektronikoaren bigarren baldintza bat **Gehitu baldintza** hautatuta</span><span class="sxs-lookup"><span data-stu-id="5e37d-179">Add a second condition for email address by selecting **Add Condition**</span></span>
   - <span data-ttu-id="5e37d-180">ECommerceContacts entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="5e37d-180">For entity eCommerceContacts, choose **EMail** in dropdown.</span></span>
   - <span data-ttu-id="5e37d-181">loyCustomers entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan.</span><span class="sxs-lookup"><span data-stu-id="5e37d-181">For entity loyCustomers, choose **EMail** in the dropdown.</span></span>
   - <span data-ttu-id="5e37d-182">"Normalizatu" hutsik utzi.</span><span class="sxs-lookup"><span data-stu-id="5e37d-182">Leave Normalize blank.</span></span>
   - <span data-ttu-id="5e37d-183">Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-183">Set **Precision Level**: **Basic** and **Value**: **High**.</span></span>

   ![Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.](media/unify-match-rule.png)

1. <span data-ttu-id="5e37d-185">Hautatu **Eginda**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-185">Select **Done**.</span></span>

1. <span data-ttu-id="5e37d-186">Hautatu **gorde** eta **exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-186">Select **Save** and **Run**.</span></span>

### <a name="merge"></a><span data-ttu-id="5e37d-187">Konbinazioa</span><span class="sxs-lookup"><span data-stu-id="5e37d-187">Merge</span></span>

1. <span data-ttu-id="5e37d-188">Joan **konbinatu** fitxara.</span><span class="sxs-lookup"><span data-stu-id="5e37d-188">Go to the **Merge** tab.</span></span>

1. <span data-ttu-id="5e37d-189">**loyCustomers** entitatearen **Kontaktuaren IDa** atalean, aldatu bistaratzeko izena **ContactIdLOYALTY** izenera, sartutako beste IDetatik bereizteko.</span><span class="sxs-lookup"><span data-stu-id="5e37d-189">On the **ContactId** for **loyCustomers** entity, change the display name to **ContactIdLOYALTY** to differentiate it from the other IDs ingested.</span></span>

   ![aldatu leialtasun IDaren kontaktuaren IDa.](media/unify-merge-contactid.png)

1. <span data-ttu-id="5e37d-191">Hautatu **gorde** eta **exekutatu konbinazio eta beherako prozesuak**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-191">Select **Save** and **Run merge and downstream processes**.</span></span>

## <a name="task-3---configure-customer-lifetime-value-prediction"></a><span data-ttu-id="5e37d-192">3. ataza - Konfiguratu bezeroaren bizi-iraupenaren balioaren iragarpena</span><span class="sxs-lookup"><span data-stu-id="5e37d-192">Task 3 - Configure customer lifetime value prediction</span></span>

<span data-ttu-id="5e37d-193">Bezeroen profil bateratuak ongi jarrita, bezeroaren bizi-iraupenaren balioaren iragarpena exekutatu dezakegu.</span><span class="sxs-lookup"><span data-stu-id="5e37d-193">With the unified customer profiles in place, we can now run the customer lifetime value prediction.</span></span> <span data-ttu-id="5e37d-194">Urrats zehatzak lortzeko, ikus [Bezeroaren bizi-iraupenaren balioaren iragarpena (aurrebista)](predict-customer-lifetime-value.md).</span><span class="sxs-lookup"><span data-stu-id="5e37d-194">For detailed steps, see [Customer Lifetime Value prediction (preview)](predict-customer-lifetime-value.md).</span></span>

1. <span data-ttu-id="5e37d-195">Joan **Adimena**  > **Iragarpenak** eta hautatu **Bezeroaren bizi-iraupenaren balioaren eredua**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-195">Go to  **Intelligence**  > **Predictions**  and select the **Customer lifetime value model**.</span></span>

1. <span data-ttu-id="5e37d-196">Joan alboko paneleko informaziora eta hautatu **Hasi**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-196">Go through the information in the side pane and select **Get started**.</span></span>

1. <span data-ttu-id="5e37d-197">Eman izen hau ereduari: **OOB eCommerce CLV iragarpena** eta hau irteerako entitateari: **OOBeCommerceCLVPrediction**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-197">Name the model **OOB eCommerce CLV Prediction** and the output entity  **OOBeCommerceCLVPrediction**.</span></span>

1. <span data-ttu-id="5e37d-198">Definitu modeloaren hobespenak CLV eredurako:</span><span class="sxs-lookup"><span data-stu-id="5e37d-198">Define model preferences for the CLV model:</span></span>
   - <span data-ttu-id="5e37d-199">**iragarpenaren denbora-tartea**: **12 hilabete edo 1 urte**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-199">**Prediction time period**: **12 months or 1 year**.</span></span> <span data-ttu-id="5e37d-200">Ezarpen honek bezeroaren bizi-iraupenaren balioaren iragartzeko etorkizunean noraino definitzen duen definitzen du.</span><span class="sxs-lookup"><span data-stu-id="5e37d-200">This setting defines how far into the future to predict customer lifetime value.</span></span>
   - <span data-ttu-id="5e37d-201">**Bezero aktiboak** : Zehaztu bezero aktiboek zer esan nahi duten zure negozioarentzat.</span><span class="sxs-lookup"><span data-stu-id="5e37d-201">**Active customers**: Specify what active customers mean for your business.</span></span> <span data-ttu-id="5e37d-202">Ezarri bezeroak aktibo izateko gutxienez transakzio bat izan behar duen denbora-tarte historikoa.</span><span class="sxs-lookup"><span data-stu-id="5e37d-202">Set the historical time frame in which a customer must have had at least one transaction to be considered active.</span></span> <span data-ttu-id="5e37d-203">Ereduak bezero aktiboentzako CLV soilik aurreikusiko du.</span><span class="sxs-lookup"><span data-stu-id="5e37d-203">The model will only predict CLV for active customers.</span></span> <span data-ttu-id="5e37d-204">Aukeratu ereduak transakzio datu historikoetan oinarritutako denbora-tartea kalkulatzen utzi edo denbora-tarte jakin bat eman behar duen.</span><span class="sxs-lookup"><span data-stu-id="5e37d-204">Choose between letting the model calculate the time period based on historical transaction data or provide a specific time frame.</span></span> <span data-ttu-id="5e37d-205">Lagin gida honetan, **ereduak erosketa tartea kalkula dezan uzten diogu**, hau da aukera lehenetsia.</span><span class="sxs-lookup"><span data-stu-id="5e37d-205">In this sample guide, we **let the model calculate purchase interval**, which is the default option.</span></span>
   - <span data-ttu-id="5e37d-206">**Balio handiko bezeroak** : Definitu balio handiko bezeroak gehien ordaintzen dituzten bezeroen pertzentila gisa.</span><span class="sxs-lookup"><span data-stu-id="5e37d-206">**High value customers**: Define high value customers as a percentile of top-paying customers.</span></span> <span data-ttu-id="5e37d-207">Ereduak sarrera hori erabiltzen du balio handiko bezeroen negozioaren definizioarekin bat datozen emaitzak emateko.</span><span class="sxs-lookup"><span data-stu-id="5e37d-207">The model uses this input to provide results that fit your business definition of high value customers.</span></span> <span data-ttu-id="5e37d-208">Ereduak balio handiko bezeroak definitzea hauta dezakezu.</span><span class="sxs-lookup"><span data-stu-id="5e37d-208">You can choose to let the model define high value customers.</span></span> <span data-ttu-id="5e37d-209">Perzentila eratortzen duen arau heuristikoa erabiltzen du.</span><span class="sxs-lookup"><span data-stu-id="5e37d-209">It uses a heuristic rule that derives the percentile.</span></span> <span data-ttu-id="5e37d-210">Balio handiko bezeroak defini ditzakezu gehien ordaintzen duten bezeroen pertzentil gisa.</span><span class="sxs-lookup"><span data-stu-id="5e37d-210">You can also define high value customers as a percentile of top future paying customers.</span></span> <span data-ttu-id="5e37d-211">Lagin gida honetan, balio handiko bezeroak eskuz definitzen ditugu **ordaintzen duten bezero aktiboen % 30** gisa eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-211">In this sample guide, we manually define high value customers as **top 30% of active paying customers** and select **Next**.</span></span>

    :::image type="content" source="media/clv-model-preferences.png" alt-text="Lehentasun urratsa CLV ereduaren esperientzia gidatuan.":::

1. <span data-ttu-id="5e37d-213">**Beharrezko datuak** urratsean, hautatu **Gehitu datuak** transakzioen historiaren datuak emateko.</span><span class="sxs-lookup"><span data-stu-id="5e37d-213">In the **Required Data** step, select **Add data** to provide the transaction history data.</span></span>

1. <span data-ttu-id="5e37d-214">Gehitu **eCommerceErosketak: eCommerce** entitatea eta esleitu ereduak eskatzen dituen atributuak:</span><span class="sxs-lookup"><span data-stu-id="5e37d-214">Add the **eCommercePurchases : eCommerce** entity and map the attributes that are required by the model:</span></span>
   - <span data-ttu-id="5e37d-215">Transakzioaren IDa: eCommerce.eCommercePurchases.PurchaseId</span><span class="sxs-lookup"><span data-stu-id="5e37d-215">Transaction ID: eCommerce.eCommercePurchases.PurchaseId</span></span>
   - <span data-ttu-id="5e37d-216">Transakzioaren data: eCommerce.eCommercePurchases.PurchasedOn</span><span class="sxs-lookup"><span data-stu-id="5e37d-216">Transaction date: eCommerce.eCommercePurchases.PurchasedOn</span></span>
   - <span data-ttu-id="5e37d-217">Transakzioaren zenbatekoa: eCommerce.eCommercePurchases.TotalPrice</span><span class="sxs-lookup"><span data-stu-id="5e37d-217">Transaction amount: eCommerce.eCommercePurchases.TotalPrice</span></span>
   - <span data-ttu-id="5e37d-218">Produktuaren IDa: eCommerce.eCommercePurchases.ProductId</span><span class="sxs-lookup"><span data-stu-id="5e37d-218">Product ID: eCommerce.eCommercePurchases.ProductId</span></span>

1. <span data-ttu-id="5e37d-219">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-219">Select **Next**.</span></span>

1. <span data-ttu-id="5e37d-220">Konfiguratu **eCommerceErosketak: eCommerce** entitatea eta **eCommerceContacts: eCommerce** entitatearen arteko erlazioa.</span><span class="sxs-lookup"><span data-stu-id="5e37d-220">Set up the relationship between the **eCommercePurchases : eCommerce** entity and  **eCommerceContacts : eCommerce**.</span></span>

1. <span data-ttu-id="5e37d-221">**Datu osagarriak (aukerakoa)** urratsak bezeroen jardueren datu gehiago gehitzeko aukera ematen du.</span><span class="sxs-lookup"><span data-stu-id="5e37d-221">The **Additional data (optional)** step allows you to add more customer activity data.</span></span> <span data-ttu-id="5e37d-222">Datu horiek bezeroek zure negozioarekin dituzten elkarreraginak ezagutzeko informazio gehiago lortzen lagun dezakete, eta horrek CLVra ekar dezake.</span><span class="sxs-lookup"><span data-stu-id="5e37d-222">This data can help to get more insights for customer interactions with your business, which can contribute to CLV.</span></span> <span data-ttu-id="5e37d-223">Bezeroen arteko elkarreragin nagusiak gehitzeak, esaterako web erregistroak, bezeroarentzako arreta-zerbitzu erregistroak edo saritze-programen historia, iragarpenen zehaztasuna hobe dezake.</span><span class="sxs-lookup"><span data-stu-id="5e37d-223">Adding key customer interactions like web logs, customer service logs, or rewards program history can improve the accuracy of predictions.</span></span> <span data-ttu-id="5e37d-224">Aukeratu **Gehitu datuak** bezeroen jardueren datu gehiago sartzeko.</span><span class="sxs-lookup"><span data-stu-id="5e37d-224">Select **Add data** to include more customer activity data.</span></span>

1. <span data-ttu-id="5e37d-225">Gehitu bezeroaren jardueraren entitatea eta esleitu haren eremuen izenak ereduak eskatzen dituen eremuetara:</span><span class="sxs-lookup"><span data-stu-id="5e37d-225">Add the customer activity entity and map its fields names to the corresponding fields required by the model:</span></span>
   - <span data-ttu-id="5e37d-226">Bezeroaren jardueren entitatea: Reviews:Website</span><span class="sxs-lookup"><span data-stu-id="5e37d-226">Customer activity entity: Reviews:Website</span></span>
   - <span data-ttu-id="5e37d-227">Gako nagusia: Website.Reviews.ReviewId</span><span class="sxs-lookup"><span data-stu-id="5e37d-227">Primary key: Website.Reviews.ReviewId</span></span>
   - <span data-ttu-id="5e37d-228">Denbora-marka: Website.Reviews.ReviewDate</span><span class="sxs-lookup"><span data-stu-id="5e37d-228">Timestamp: Website.Reviews.ReviewDate</span></span>
   - <span data-ttu-id="5e37d-229">Gertaera (jardueraren izena): Website.Reviews.ActivityTypeDisplay</span><span class="sxs-lookup"><span data-stu-id="5e37d-229">Event (activity name): Website.Reviews.ActivityTypeDisplay</span></span>
   - <span data-ttu-id="5e37d-230">Xehetasunak (zenbatekoa edo balioa): Website.Reviews.ReviewRating</span><span class="sxs-lookup"><span data-stu-id="5e37d-230">Details (amount or value): Website.Reviews.ReviewRating</span></span>

1. <span data-ttu-id="5e37d-231">Aukeratu **Hurrengoa** eta konfiguratu jarduera eta transakzio datuen eta bezeroen datuen arteko harremana:</span><span class="sxs-lookup"><span data-stu-id="5e37d-231">Select **Next** and configure the activity and the relationship between the transaction data and the customer data:</span></span>  
   - <span data-ttu-id="5e37d-232">Jarduera mota: aukeratu lehendik daudenetatik</span><span class="sxs-lookup"><span data-stu-id="5e37d-232">Activity type: Choose existing</span></span>
   - <span data-ttu-id="5e37d-233">Jardueraren etiketa: Review</span><span class="sxs-lookup"><span data-stu-id="5e37d-233">Activity label: Review</span></span>
   - <span data-ttu-id="5e37d-234">Dagokion etiketa: Website.Reviews.UserId</span><span class="sxs-lookup"><span data-stu-id="5e37d-234">Corresponding label: Website.Reviews.UserId</span></span>
   - <span data-ttu-id="5e37d-235">Bezeroaren entitatea: eCommerceContacts:eCommerce</span><span class="sxs-lookup"><span data-stu-id="5e37d-235">Customer entity: eCommerceContacts:eCommerce</span></span>
   - <span data-ttu-id="5e37d-236">Harremana: WebsiteReviews</span><span class="sxs-lookup"><span data-stu-id="5e37d-236">Relationship: WebsiteReviews</span></span>

1. <span data-ttu-id="5e37d-237">Aukeratu **Hurrengoa** ereduaren antolaketa ezartzeko.</span><span class="sxs-lookup"><span data-stu-id="5e37d-237">Select **Next** to set the model schedule.</span></span>

   <span data-ttu-id="5e37d-238">Ereduak aldizka entrenatu behar du iradokitako datu berriak daudenean eredu berriak ikasteko.</span><span class="sxs-lookup"><span data-stu-id="5e37d-238">The model needs to train regularly to learn new patterns when there's new data ingested.</span></span> <span data-ttu-id="5e37d-239">Adibide honetarako, aukeratu **Hilero**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-239">For this example, choose **Monthly**.</span></span>

1. <span data-ttu-id="5e37d-240">Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-240">After reviewing all the details, select  **Save and Run**.</span></span>

## <a name="task-4---review-model-results-and-explanations"></a><span data-ttu-id="5e37d-241">4. zeregina - Berrikusi ereduen emaitzak eta azalpenak</span><span class="sxs-lookup"><span data-stu-id="5e37d-241">Task 4 - Review model results and explanations</span></span>

<span data-ttu-id="5e37d-242">Ereduak datuen prestakuntza eta puntuazioa osatuko ditu.</span><span class="sxs-lookup"><span data-stu-id="5e37d-242">Let the model complete the training and scoring of the data.</span></span> <span data-ttu-id="5e37d-243">Ondoren, CLV ereduaren emaitzak eta azalpenak berrikus ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="5e37d-243">Next, you can review the CLV model results and explanations.</span></span> <span data-ttu-id="5e37d-244">Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-customer-lifetime-value.md#review-prediction-status-and-results).</span><span class="sxs-lookup"><span data-stu-id="5e37d-244">For more information, see [Review a prediction status and results](predict-customer-lifetime-value.md#review-prediction-status-and-results).</span></span>

## <a name="task-5---create-a-segment-of-high-value-customers"></a><span data-ttu-id="5e37d-245">5. ataza - Sortu balio handiko bezeroen segmentu bat</span><span class="sxs-lookup"><span data-stu-id="5e37d-245">Task 5 - Create a segment of high value customers</span></span>

<span data-ttu-id="5e37d-246">Eredua exekutatzeak entitate berri bat sortzen du, **Datuak** > **Entitateak** zerrendan agertzen dena.</span><span class="sxs-lookup"><span data-stu-id="5e37d-246">Running the model creates a new entity, which is listed on **Data** > **Entities**.</span></span> <span data-ttu-id="5e37d-247">Ereduak sortutako entitatean oinarrituta bezeroen segmentu berri bat sor dezakezu.</span><span class="sxs-lookup"><span data-stu-id="5e37d-247">You can create a new customer segment based on the entity created by the model.</span></span>

1. <span data-ttu-id="5e37d-248">Joan hona: **Segmentuak**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-248">Go to **Segments**.</span></span> 

1. <span data-ttu-id="5e37d-249">Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**.</span><span class="sxs-lookup"><span data-stu-id="5e37d-249">Select  **New** and choose **Create from** > **Intelligence**.</span></span>

   ![Ereduaren irteerarekin segmentu bat sortzea.](media/segment-intelligence.png)

1. <span data-ttu-id="5e37d-251">Aukeratu **OOBeCommerceCLVPrediction** entitatea eta definitu segmentua:</span><span class="sxs-lookup"><span data-stu-id="5e37d-251">Select the  **OOBeCommerceCLVPrediction** entity and define the segment:</span></span>
  - <span data-ttu-id="5e37d-252">Eremua: CLVScore</span><span class="sxs-lookup"><span data-stu-id="5e37d-252">Field: CLVScore</span></span>
  - <span data-ttu-id="5e37d-253">Eragilea: hau baino handiagoa</span><span class="sxs-lookup"><span data-stu-id="5e37d-253">Operator: greater than</span></span>
  - <span data-ttu-id="5e37d-254">Balioa: 1500</span><span class="sxs-lookup"><span data-stu-id="5e37d-254">Value: 1500</span></span>

1. <span data-ttu-id="5e37d-255">Aukeratu **Berrikuspena** eta **Gorde** segmentua.</span><span class="sxs-lookup"><span data-stu-id="5e37d-255">Select **Review** and **Save** the segment.</span></span>

<span data-ttu-id="5e37d-256">Datozen 12 hilabeteetan $1500ko diru sarrera baino gehiago sortuko dituztela aurreikusten duten bezeroak identifikatzen dituen segmentu bat duzu orain.</span><span class="sxs-lookup"><span data-stu-id="5e37d-256">You now have a segment that identifies customers who are predicted to generate more than $1500 of revenue in the next 12 months.</span></span> <span data-ttu-id="5e37d-257">Segmentu hau dinamikoki eguneratzen da datu gehiago irensten badira.</span><span class="sxs-lookup"><span data-stu-id="5e37d-257">This segment gets updated dynamically if more data is ingested.</span></span>

<span data-ttu-id="5e37d-258">Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).</span><span class="sxs-lookup"><span data-stu-id="5e37d-258">For more information, see [Create and manage segments](segments.md).</span></span>
