---
title: Osatu datu partzialak iragarpenak erabiliz
description: Erabili iragarpenak bezeroen datu osatugabeak betetzeko.
ms.date: 05/05/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: zacook
manager: shellyha
ms.openlocfilehash: 66f0b16b5d05741ab98ca5ce2157da8c46b6d9e0
ms.sourcegitcommit: 5379c2b77d613d071a177f509e6417ebf3c47516
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/26/2020
ms.locfileid: "4648696"
---
# <a name="complete-your-partial-data-with-predictions"></a><span data-ttu-id="b0af7-103">Osatu zure datu partzialak iragarpenekin</span><span class="sxs-lookup"><span data-stu-id="b0af7-103">Complete your partial data with predictions</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="b0af7-104">Aurreikuspenek erraz iragarritako balioak sor ditzakezu bezeroaren ulermena hobetzeko.</span><span class="sxs-lookup"><span data-stu-id="b0af7-104">Predictions lets you easily create predicted values that can enhance your understanding of a customer.</span></span> <span data-ttu-id="b0af7-105">**Adimena** > **Iragarpenak** orrian, **Nire iragarpenak** atala hauta dezakezu hartzaileei buruzko xehetasunen beste atal batzuetan konfiguratu dituzun iragarpenak ikusteko eta pertsonalizatzeko aukera ematen dizu.</span><span class="sxs-lookup"><span data-stu-id="b0af7-105">On the **Intelligence** > **Predictions** page, you can select **My predictions** to see predictions that you've configured in other parts of audience insights, and allow you to further customize them.</span></span>

> [!NOTE]
> <span data-ttu-id="b0af7-106">Ezin duzu funtzio hau erabili zure inguruak Azure Data Lake Gen 2 biltegia erabiltzen badu.</span><span class="sxs-lookup"><span data-stu-id="b0af7-106">You can't use this feature if your environment uses Azure Data Lake Gen 2 storage.</span></span>
>
> <span data-ttu-id="b0af7-107">Aurreikuspenen funtzionalitateak bitarteko automatizatuak erabiltzen ditu datuak ebaluatzeko eta datu horietan oinarritutako iragarpenak egiteko, eta, beraz, profilak egiteko metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Araudi Orokorrak ("DBAO") definitzen baitu.</span><span class="sxs-lookup"><span data-stu-id="b0af7-107">The predictions feature uses automated means to evaluate data and make predictions based on that data, and therefore has the capability to be used as a method of profiling, as that term is defined by the General Data Protection Regulation ("GDPR").</span></span> <span data-ttu-id="b0af7-108">Bezeroak funtzio hau erabiltzeko datuak prozesatzeko DBAO edo beste lege edo arau batzuen menpe egon daiteke.</span><span class="sxs-lookup"><span data-stu-id="b0af7-108">Customer's use of this feature to process data may be subject to GDPR or other laws or regulations.</span></span> <span data-ttu-id="b0af7-109">Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, iragarpenez aplikagarriak diren lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.</span><span class="sxs-lookup"><span data-stu-id="b0af7-109">You are responsible for ensuring that your use of Dynamics 365 Customer Insights, including predictions, complies with all applicable laws and regulations, including laws related to privacy, personal data, biometric data, data protection, and confidentiality of communications.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b0af7-110">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="b0af7-110">Prerequisites</span></span>

<span data-ttu-id="b0af7-111">Zure erakundeak iragarpenen funtzioa erabili ahal izateko, ziurtatu baldintza hauek bete aurretik:</span><span class="sxs-lookup"><span data-stu-id="b0af7-111">Before your organization can use the predictions feature, the following prerequisites must be met:</span></span>

1. <span data-ttu-id="b0af7-112">Zure erakundeak instantzia bat du [konfiguratuta Common Data Service](https://docs.microsoft.com/ai-builder/build-model#prerequisites) zerbitzuan eta Customer Insights-en erakunde berean dago.</span><span class="sxs-lookup"><span data-stu-id="b0af7-112">Your organization has an instance [set up in the Common Data Service](https://docs.microsoft.com/ai-builder/build-model#prerequisites) and it's in the same organization as Customer Insights.</span></span>

2. <span data-ttu-id="b0af7-113">Zure ingurunea Common Data Service instantziari erantsita dago.</span><span class="sxs-lookup"><span data-stu-id="b0af7-113">Your environment is attached to your Common Data Service instance.</span></span>

<span data-ttu-id="b0af7-114">Zu bazara [ingurune berria sortu](manage-environments.md), konfiguratu iturburuan **Ingurua sortu** elkarrizketa-koadroa eta hautatu **aurreratua**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-114">If you're [creating a new environment](manage-environments.md), configure it in the **Create an environment** dialog and select **Advanced**.</span></span> <span data-ttu-id="b0af7-115">Ingurua sortu baduzu, joan bere ezarpenetara eta hautatu **aurreratua**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-115">If you've already created an environment, go to its settings and select **Advanced**.</span></span> <span data-ttu-id="b0af7-116">Edozein modutan, **Erabili iragarpenak** atalean, sartu zure ingurunea lotu nahi duzun Common Data Service instantziaren URLa.</span><span class="sxs-lookup"><span data-stu-id="b0af7-116">Either way, in the **Use predictions** section, enter the Common Data Service instance URL to which you want to attach your environment.</span></span>

## <a name="create-a-prediction-in-the-customer-entity"></a><span data-ttu-id="b0af7-117">Sortu iragarpenak bezeroaren entitatean</span><span class="sxs-lookup"><span data-stu-id="b0af7-117">Create a prediction in the Customer entity</span></span>

1. <span data-ttu-id="b0af7-118">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Entitateak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-118">In audience insights, go to **Data** > **Entities**.</span></span>

2. <span data-ttu-id="b0af7-119">Hautatu **Bezeroa** entitatea.</span><span class="sxs-lookup"><span data-stu-id="b0af7-119">Select the **Customer** entity.</span></span>

3. <span data-ttu-id="b0af7-120">Sarbidean **Bezeroa: CustomerInsights** entitatea, hautatu aukeran **eremuak** fitxa.</span><span class="sxs-lookup"><span data-stu-id="b0af7-120">In the **Customer:CustomerInsights** entity, select on the **Fields** tab.</span></span>

4. <span data-ttu-id="b0af7-121">Bilatu balioak aurreikusteko nahi duzun atributu izena eta ondoren hautatu **Orokorra** ikonoa hemen **Laburpen** zutabea.</span><span class="sxs-lookup"><span data-stu-id="b0af7-121">Find the attribute name you wish to predict values for, then select the **Overview** icon in the **Summary** column.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="b0af7-122">![Ikuspegi orokorra](media/intelligence-overviewicon.png "Ikuspegi orokorra")</span><span class="sxs-lookup"><span data-stu-id="b0af7-122">![Overview icon](media/intelligence-overviewicon.png "Overview icon")</span></span>

5. <span data-ttu-id="b0af7-123">Zure atributua lortzeko balio gutxi falta bada, hautatu **Falta diren balioak aurreikustea** zure iragarpenarekin jarraitzeko.</span><span class="sxs-lookup"><span data-stu-id="b0af7-123">If there's a high rate of missing values for your attribute, select **Predict missing values** to continue with your prediction.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="b0af7-124">![Egoera orokorra falta diren balioen iragarpen botoia erakusten da](media/intelligence-overviewpredictmissingvalues.png "Egoera orokorra falta diren balioen iragarpen botoia erakusten da")</span><span class="sxs-lookup"><span data-stu-id="b0af7-124">![Overview status with predict missing values button shown](media/intelligence-overviewpredictmissingvalues.png "Overview status with predict missing values button shown")</span></span>

6. <span data-ttu-id="b0af7-125">Eman a **Bistaratu izena** eta **Irteerako entitatearen izena** iragarpenaren emaitzetarako.</span><span class="sxs-lookup"><span data-stu-id="b0af7-125">Provide a **Display name** and an **Output entity name** for the results of the prediction.</span></span>

7. <span data-ttu-id="b0af7-126">Aurrez okupatutako aukeren zerrenda batek iragarritako kategoria batera non mapatu ditzakezun erakutsiko du.</span><span class="sxs-lookup"><span data-stu-id="b0af7-126">A pre-populated list of options will show where you can map the values to a predicted category.</span></span> <span data-ttu-id="b0af7-127">Kasu honetan, zure kategoriako aukerak 0 edo 1 izango dira, iragarpenaren benetako / gezurra edo bitarra izaerara mapatzen duten heinean.</span><span class="sxs-lookup"><span data-stu-id="b0af7-127">In this case, your only category options will be 0 or 1, as they map to the true/false or binary nature of the prediction.</span></span> <span data-ttu-id="b0af7-128">Kategoria zutabean, esleitu "0" gisa sailkatu nahi dituzun eremu-balioak azken iragarpenean "0"-ra, eta "1" gisa sailkatu nahi dituzun elementuak "1" eremura azken iragarpenean.</span><span class="sxs-lookup"><span data-stu-id="b0af7-128">In the Category column, map the field values you'd like to be classified as "0" in the final prediction to "0", and the items you'd like to be classified as "1" in the final prediction to "1".</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="b0af7-129">![Adibidez, mapen eremuaren balioak kategorietan erakusteko](media/intelligence-categorymapping.png "Adibidez, mapen eremuaren balioak kategorietan erakusteko")</span><span class="sxs-lookup"><span data-stu-id="b0af7-129">![Example showing mapped field values to categories](media/intelligence-categorymapping.png "Example showing mapped field values to categories")</span></span>

8. <span data-ttu-id="b0af7-130">Aukeratu **Egina** eta iragarpena prozesatuko da.</span><span class="sxs-lookup"><span data-stu-id="b0af7-130">Select **Done** and the prediction will be processed.</span></span> <span data-ttu-id="b0af7-131">Tratamenduak denbora gutxi iraungo du, datuen tamainaren eta konplexutasunaren arabera.</span><span class="sxs-lookup"><span data-stu-id="b0af7-131">The processing will take some time, depending on the size and complexity of data.</span></span> <span data-ttu-id="b0af7-132">Emaitzak entitate berri batean egongo dira eskuragarri **Irteerako entitatearen izena** sortu zenuen iragarpenaz.</span><span class="sxs-lookup"><span data-stu-id="b0af7-132">Results will be available in a new entity based on the **Output entity name** of the prediction you created.</span></span>

## <a name="create-a-prediction-while-creating-a-segment"></a><span data-ttu-id="b0af7-133">Sortu iragarpenak segmentu bat sortzen duzun bitartean</span><span class="sxs-lookup"><span data-stu-id="b0af7-133">Create a prediction while creating a segment</span></span>

<span data-ttu-id="b0af7-134">Aukera zehatz baterako falta diren balioa aurreikustea ere posible da segmentu bat sortzerakoan.</span><span class="sxs-lookup"><span data-stu-id="b0af7-134">Predicting missing values for a specific attribute of choice is also possible when creating a segment.</span></span> <span data-ttu-id="b0af7-135">Zehazki, zure bezero entitate bateratuan edo Customer_Measure entitatean oinarritutako segmentua azkar sortzen duzunean.</span><span class="sxs-lookup"><span data-stu-id="b0af7-135">Specifically, when you quickly create a segment based on either your unified Customer entity or Customer_Measure entity.</span></span>

<span data-ttu-id="b0af7-136">Fluxu horren baitan atributu zehatz bat aukeratu behar duzu zure segmentua nola bezeroaren gogobetetzea, erosketa zenbatekoa.</span><span class="sxs-lookup"><span data-stu-id="b0af7-136">As part of this flow, you'll choose a specific attribute to base your segment on, such as Customer Satisfaction or Purchase Amount.</span></span> <span data-ttu-id="b0af7-137">Segmentuak sortzean, sistemak metodo bat proposatuko du atributu honentzako falta diren balioak aurreikusteko.</span><span class="sxs-lookup"><span data-stu-id="b0af7-137">Upon segment creation, the system will suggest a method for predicting any missing values for this attribute.</span></span>

1. <span data-ttu-id="b0af7-138">Hartzaileen xehetasunetan, joan hona: **Segmentuak** eta hautatu **Profilak** lauza.</span><span class="sxs-lookup"><span data-stu-id="b0af7-138">In audience insights, go to **Segments** and select the **Profiles** tile.</span></span>

2. <span data-ttu-id="b0af7-139">Aukeratu a **eremua** segmentu bat sortu eta hautatu bat **Operadorea** eta hautatu **Berrikusi**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-139">Choose a **Field** to create a segment on and select an **Operator**, then select **Review**.</span></span>

3. <span data-ttu-id="b0af7-140">Eman a **izena** eta **Bistaratu izena** segmentuarentzat.</span><span class="sxs-lookup"><span data-stu-id="b0af7-140">Provide a **Name** and a **Display name** for the segment.</span></span>

4. <span data-ttu-id="b0af7-141">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-141">Select **Save**.</span></span>

5. <span data-ttu-id="b0af7-142">Sortu berri duzun segmentuak datu osatugabeak baditu iturburu eremuan, falta diren balioak aurreikustea aukeratu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="b0af7-142">If the segment you created has incomplete data in the source field, you can choose to predict the missing values.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="b0af7-143">![Iragarpen botoia](media/segments-predictoption.png "Iragarpen botoia")</span><span class="sxs-lookup"><span data-stu-id="b0af7-143">![Prediction button](media/segments-predictoption.png "Prediction button")</span></span>

6. <span data-ttu-id="b0af7-144">Eman a **Bistaratu izena** eta **Irteerako entitatearen izena** iragarpenaren emaitzetarako.</span><span class="sxs-lookup"><span data-stu-id="b0af7-144">Provide a **Display name** and an **Output entity name** for the results of the prediction.</span></span>

7. <span data-ttu-id="b0af7-145">Hautatu **Eginda**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-145">Select **Done**.</span></span> <span data-ttu-id="b0af7-146">Zure iragarpena laster sortuko da eta entitate berri batean izenarekin **Irteerako entitatearen izena**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-146">Your prediction will be generated shortly in a new entity with the name you provided for the **Output entity name**.</span></span>

## <a name="view-a-prediction"></a><span data-ttu-id="b0af7-147">Ikusi iragarpena</span><span class="sxs-lookup"><span data-stu-id="b0af7-147">View a prediction</span></span>

1. <span data-ttu-id="b0af7-148">Hartzaileen xehetasunetan, joan hona: **Adimena** > **Iragarpenak** > **Nire iragarpenak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-148">In audience insights, go to **Intelligence** > **Predictions** > **My predictions**.</span></span>

2. <span data-ttu-id="b0af7-149">Hautatu berrikusi nahi duzun iragarpena.</span><span class="sxs-lookup"><span data-stu-id="b0af7-149">Select the prediction you want to review.</span></span>

3. <span data-ttu-id="b0af7-150">Hautatu elipsi eremuan **Ekintzak** zutabea eta aukeratu **ikusi**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-150">Select the ellipsis in the **Actions** column and choose **View**.</span></span>

4. <span data-ttu-id="b0af7-151">Zure iragarpena ikusita hainbat datu puntu ikusiko dituzu.</span><span class="sxs-lookup"><span data-stu-id="b0af7-151">You'll see a number of data points in the view of your prediction.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="b0af7-152">![Iragarpenen orria](media/intelligence-predictionsviewpage.png "Iragarpenen orria")</span><span class="sxs-lookup"><span data-stu-id="b0af7-152">![Predictions page](media/intelligence-predictionsviewpage.png "Predictions page")</span></span>

   - <span data-ttu-id="b0af7-153">**Aurreikusitako balioak** Erakusten den mapeketa erakusten du Eremuaren balioa kategorian mapak egiteko fasean.</span><span class="sxs-lookup"><span data-stu-id="b0af7-153">**Predicted values** shows the mapping you created during the Field value to Category mapping phase.</span></span> <span data-ttu-id="b0af7-154">Horiek dira kategoria jakin batera mapatu diren zure datu-baseko balioak.</span><span class="sxs-lookup"><span data-stu-id="b0af7-154">These are the values in your dataset that have been mapped to a specific category.</span></span>
   <span data-ttu-id="b0af7-155">-**Goi mailako eragileak** kategoria zehatz batera mapak egitean iragarpenen konfiantzan eragina izan dezaketen datu-multzoko faktoreak dira.</span><span class="sxs-lookup"><span data-stu-id="b0af7-155">-**Top influencers** are the factors within your dataset that were most likely to influence the prediction's confidence of your Field value being mapped to a specific category.</span></span>
   - <span data-ttu-id="b0af7-156">**Errendimendua** Iragarpenak nola egiten diren adierazten du.</span><span class="sxs-lookup"><span data-stu-id="b0af7-156">**Performance** indicates how the predictions are doing.</span></span> <span data-ttu-id="b0af7-157">Hautatu esteka gehiago ikasteko.</span><span class="sxs-lookup"><span data-stu-id="b0af7-157">Select the link to learn more.</span></span>
   - <span data-ttu-id="b0af7-158">**Aurreikusi** Aurreikusitako irteera-datuen laginak erakusten ditu eta aurreikusitako balioa 0 ziurgabetasuna eta 1 ziurtatuta dauzkagula.</span><span class="sxs-lookup"><span data-stu-id="b0af7-158">**Preview** shows samples of the output dataset from your prediction and the likelihood, or our confidence, of the predicted value where 0 is uncertain, and 1 is certain.</span></span>

## <a name="update-a-prediction"></a><span data-ttu-id="b0af7-159">Eguneratu iragarpena</span><span class="sxs-lookup"><span data-stu-id="b0af7-159">Update a prediction</span></span>

1. <span data-ttu-id="b0af7-160">Hartzaileen xehetasunetan, joan hona: **Adimena** > **Iragarpenak** > **Nire iragarpenak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-160">In audience insights, go to **Intelligence** > **Predictions** > **My predictions**.</span></span>

2. <span data-ttu-id="b0af7-161">Hautatu eguneratu nahi duzun iragarpena, eta hautatu ... **eguneratu** ikonoa.</span><span class="sxs-lookup"><span data-stu-id="b0af7-161">Select the prediction you want to update and select the **Update** icon.</span></span>

3. <span data-ttu-id="b0af7-162">Aurreikuspena prozesatzeko programatuta egongo da.</span><span class="sxs-lookup"><span data-stu-id="b0af7-162">The prediction will be scheduled for processing.</span></span> <span data-ttu-id="b0af7-163">Azkenean eguneratu den momentua ikus dezakezu **eguneratua** zutabe honen **iragarpenak** orria.</span><span class="sxs-lookup"><span data-stu-id="b0af7-163">You can see the time it was last updated in the **Updated** column of the **Predictions** page.</span></span>

## <a name="edit-a-prediction"></a><span data-ttu-id="b0af7-164">Editatu iragarpena</span><span class="sxs-lookup"><span data-stu-id="b0af7-164">Edit a prediction</span></span>

<span data-ttu-id="b0af7-165">Aurreikuspen bat sortu ondoren, AI Builder-en eredua pertsonalizatu dezakezu zure ereduaren eraginkortasuna areagotzeko.</span><span class="sxs-lookup"><span data-stu-id="b0af7-165">After you've created a prediction, you can customize the model in the AI Builder to increase the effectiveness of your model.</span></span>  

1. <span data-ttu-id="b0af7-166">Hartzaileen xehetasunetan, joan hona: **Adimena** > **Iragarpenak** > **Nire iragarpenak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-166">In audience insights, go to **Intelligence** > **Predictions** > **My predictions**.</span></span>

2. <span data-ttu-id="b0af7-167">Hautatu editatu nahi duzun iragarpena.</span><span class="sxs-lookup"><span data-stu-id="b0af7-167">Select the prediction you want to edit.</span></span>

3. <span data-ttu-id="b0af7-168">Hautatu elipsi eremuan **Ekintzak** zutabea eta aukeratu **ikusi**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-168">Select the ellipsis in the **Actions** column and choose **View**.</span></span>

4. <span data-ttu-id="b0af7-169">Hautatu **Pertsonalizatu AI Builder-en**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-169">Select **Customize in AI Builder**.</span></span>

5. <span data-ttu-id="b0af7-170">Eguneratu zure eredua AI Builder-en.</span><span class="sxs-lookup"><span data-stu-id="b0af7-170">Update your model in the AI Builder.</span></span> <span data-ttu-id="b0af7-171">[Argibide gehiago AI builder ereduak kudeatzeari buruz](https://docs.microsoft.com/ai-builder/manage-model#retrain-and-republish-existing-models).</span><span class="sxs-lookup"><span data-stu-id="b0af7-171">[Learn more about managing models in the AI builder](https://docs.microsoft.com/ai-builder/manage-model#retrain-and-republish-existing-models).</span></span>

<span data-ttu-id="b0af7-172">Zure iragarpenaren hurrengo exekutatuak sortu duzun eredu eguneratua erabiliko du.</span><span class="sxs-lookup"><span data-stu-id="b0af7-172">The next run of your prediction will use the updated model you've created.</span></span>

> [!NOTE]
> <span data-ttu-id="b0af7-173">AI Builder-en sortutako eredu berriak ez dira hartzaileen xehetasunetan bistaratuko, eredua goian zerrendatutako esperientzietatik sortu izan ezean.</span><span class="sxs-lookup"><span data-stu-id="b0af7-173">New models created in AI Builder will not be displayed in audience insights unless the model was created from the experiences listed above.</span></span>

## <a name="remove-a-prediction"></a><span data-ttu-id="b0af7-174">Kendu iragarpena</span><span class="sxs-lookup"><span data-stu-id="b0af7-174">Remove a prediction</span></span>

1. <span data-ttu-id="b0af7-175">Hartzaileen xehetasunetan, joan hona: **Adimena** > **Iragarpenak** > **Nire iragarpenak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-175">In audience insights, go to **Intelligence** > **Predictions** > **My predictions**.</span></span>

2. <span data-ttu-id="b0af7-176">Hautatu ezabatu nahi duzun iragarpena.</span><span class="sxs-lookup"><span data-stu-id="b0af7-176">Select the prediction you want to delete.</span></span>

3. <span data-ttu-id="b0af7-177">Hautatu elipsi eremuan **Ekintzak** zutabea eta aukeratu **Ezabatu**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-177">Select the ellipsis in the **Actions** column and choose **Delete**.</span></span>

4. <span data-ttu-id="b0af7-178">Berretsi ezabatzea.</span><span class="sxs-lookup"><span data-stu-id="b0af7-178">Confirm the deletion.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b0af7-179">Irtenbideak</span><span class="sxs-lookup"><span data-stu-id="b0af7-179">Troubleshooting</span></span>

<span data-ttu-id="b0af7-180">Eranskina ezin baduzu osatu Common Data Service prozesua akats bat dela eta, prozesua eskuz betetzen saia zaitezke.</span><span class="sxs-lookup"><span data-stu-id="b0af7-180">If you can't complete the attach Common Data Service process due to an error, you can try to complete the process manually.</span></span> <span data-ttu-id="b0af7-181">Erantsitako prozesuan gerta daitezkeen bi arazo ezagutzen dira:</span><span class="sxs-lookup"><span data-stu-id="b0af7-181">There are two known issues that can occur in the attach process:</span></span>

- <span data-ttu-id="b0af7-182">Bezeroaren txartelaren osagarriaren soluzioa ez dago instalatuta.</span><span class="sxs-lookup"><span data-stu-id="b0af7-182">The Customer Card Add-in solution is not installed.</span></span>
    1. <span data-ttu-id="b0af7-183">Jarraitu argibideak [instalatu eta konfiguratu irtenbidea](customer-card-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="b0af7-183">Complete the instructions to [install and configure the solution](customer-card-add-in.md).</span></span>

- <span data-ttu-id="b0af7-184">Aplikazio baimenak ez dira eman.</span><span class="sxs-lookup"><span data-stu-id="b0af7-184">App permissions aren't granted.</span></span>
    1. <span data-ttu-id="b0af7-185">Joan [https://admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com)-ra.</span><span class="sxs-lookup"><span data-stu-id="b0af7-185">Go to [https://admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com).</span></span>
    1. <span data-ttu-id="b0af7-186">Hautatu **Inguruneak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-186">Select **Environments**.</span></span>
    1. <span data-ttu-id="b0af7-187">Hautatu baimena gehitu eta aukeratu nahi duzun ingurunearen ondoan **ezarpenak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-187">Select the ellipsis next to the environment you want to add the permission to and select **Settings**.</span></span>
    1. <span data-ttu-id="b0af7-188">Zabaldu **Erabiltzaileak + baimenak** eta hautatu **erabiltzaileak**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-188">Expand **Users + permissions** and select **Users**.</span></span>
    1. <span data-ttu-id="b0af7-189">Aukeratu **+ Berria** eta hautatu **Erabiltzailea**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-189">Select **+ New** and select **User**.</span></span>
    1. <span data-ttu-id="b0af7-190">Aukeratu **Aplikazioaren erabiltzailea** hautatuta ez badago, eta sartu informazio hau:</span><span class="sxs-lookup"><span data-stu-id="b0af7-190">Select **Application User** if it's not already selected and enter the following information:</span></span>
        - <span data-ttu-id="b0af7-191">**Erabiltzaile-izena:** cihelp@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b0af7-191">**User Name:** cihelp@microsoft.com</span></span>
        - <span data-ttu-id="b0af7-192">**Aplikazioaren ID-a:** 38c77d00-5fcb-4cce-9d93-af4738258e3c</span><span class="sxs-lookup"><span data-stu-id="b0af7-192">**Application ID:** 38c77d00-5fcb-4cce-9d93-af4738258e3c</span></span>
        - <span data-ttu-id="b0af7-193">**Izena:** Bezeroa</span><span class="sxs-lookup"><span data-stu-id="b0af7-193">**First Name:** Customer</span></span>
        - <span data-ttu-id="b0af7-194">**Abizena:** xehetasunak</span><span class="sxs-lookup"><span data-stu-id="b0af7-194">**Last Name:** Insights</span></span>
        - <span data-ttu-id="b0af7-195">**Posta elektroniko nagusia:** cihelp@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="b0af7-195">**Primary Email:** cihelp@microsoft.com</span></span>
    1. <span data-ttu-id="b0af7-196">Hautatu **Gorde eta itxi**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-196">Select **Save & Close**.</span></span>
    1. <span data-ttu-id="b0af7-197">Hautatu sortu duzun erabiltzailea.</span><span class="sxs-lookup"><span data-stu-id="b0af7-197">Select the user you just created.</span></span>
    1. <span data-ttu-id="b0af7-198">Aukeratu **Kudeatu Rolak** goiko menu-barran.</span><span class="sxs-lookup"><span data-stu-id="b0af7-198">Select **Manage Roles** in the top menu bar.</span></span>
    1. <span data-ttu-id="b0af7-199">Aukeratu **Sistemaren administratzailea** eta hautatu **Ados**.</span><span class="sxs-lookup"><span data-stu-id="b0af7-199">Select **System Administrator**, then select **OK**.</span></span>
