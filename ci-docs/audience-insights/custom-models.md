---
title: Ikaskuntza automatiko eredu pertsonalizatuak | Microsoft Docs
description: Azure Ikaskuntza automatiko-en eredu pertsonalizatuekin lan egin Dynamics 365 Customer Insights.
ms.date: 11/19/2020
ms.reviewer: zacook
ms.service: dynamics-365-ai
ms.topic: tutorial
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 34489faaecc5da1ce3dd68d799b3e0e0d9672ab7
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267219"
---
# <a name="custom-machine-learning-models"></a><span data-ttu-id="fe1f6-103">Ikaskuntza automatiko eredu pertsonalizatuak</span><span class="sxs-lookup"><span data-stu-id="fe1f6-103">Custom machine learning models</span></span>

<span data-ttu-id="fe1f6-104">**Adimena** > **Eredu pertsonalizatuak** lan-fluxuak kudeatzeko aukera ematen dizu Azure Machine Learning-eko ereduetan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-104">**Intelligence** > **Custom models** lets you manage workflows based on Azure Machine Learning models.</span></span> <span data-ttu-id="fe1f6-105">Lan-fluxuek xehetasunak sortu nahi dituzun datuak aukeratzen eta emaitzak bezeroaren datu bateratuekin esleitzen laguntzen zaituzte.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-105">Workflows help you choose the data you want to generate insights from and map the results to your unified customer data.</span></span> <span data-ttu-id="fe1f6-106">Ikaskuntza automatikoko eredu pertsonalizatuak eraikitzeari buruzko informazio gehiago lortzeko, ikusi [Erabili Azure Machine Learning-en oinarritutako ereduak](azure-machine-learning-experiments.md).</span><span class="sxs-lookup"><span data-stu-id="fe1f6-106">For more information about building custom ML models, see [Use Azure Machine Learning-based models](azure-machine-learning-experiments.md).</span></span>

## <a name="responsible-ai"></a><span data-ttu-id="fe1f6-107">AA arduratsua</span><span class="sxs-lookup"><span data-stu-id="fe1f6-107">Responsible AI</span></span>

<span data-ttu-id="fe1f6-108">Iragarpenek bezeroen esperientzia hobeak sortzeko, negozio gaitasunak eta diru sarrera korronteak hobetzeko gaitasunak eskaintzen dituzte.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-108">Predictions offer capabilities to create better customer experiences, improve business capabilities, and revenue streams.</span></span> <span data-ttu-id="fe1f6-109">Zure iragarpenaren balioa orekatzea gomendatzen dizugu, duen eraginaren eta modu etikoan sar daitezkeen alborapenen artean.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-109">We strongly recommend you balance the value of your prediction against the impact it has and biases that may be introduced in an ethical manner.</span></span> <span data-ttu-id="fe1f6-110">Lortu informazio gehiago Microsoft-ek [AA arduratsua](https://www.microsoft.com/ai/responsible-ai?activetab=pivot1%3aprimaryr6) jorratzeko moduari buruz.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-110">Learn more about how Microsoft is [addressing Responsible AI](https://www.microsoft.com/ai/responsible-ai?activetab=pivot1%3aprimaryr6).</span></span> <span data-ttu-id="fe1f6-111">Azure Machine Learning-en [Ikaskuntza automatiko modu arduratsuan erabiltzeko teknika eta prozesu](https://docs.microsoft.com/azure/machine-learning/concept-responsible-ml) jakinei buruz ikas dezakezu.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-111">You can also learn about [techniques and processes for responsible machine learning](https://docs.microsoft.com/azure/machine-learning/concept-responsible-ml) specific to Azure Machine Learning.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fe1f6-112">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="fe1f6-112">Prerequisites</span></span>

- <span data-ttu-id="fe1f6-113">Gaur egun, eginbide honek [Machine Learning Studio (klasikoa)](https://studio.azureml.net) eta [Azure Machine Learning sortako bideratzeak](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines) onartzen ditu.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-113">Currently, this feature supports web services published through [Machine Learning Studio (classic)](https://studio.azureml.net) and [Azure Machine Learning batch pipelines](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines).</span></span>

- <span data-ttu-id="fe1f6-114">Ezaugarri hau erabiltzeko Azure Studio Lake instantziarekin lotutako Azure Data Lake Gen2 biltegiratze kontua behar duzu.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-114">You need an Azure Data Lake Gen2 storage account associated with your Azure Studio instance to use this feature.</span></span> <span data-ttu-id="fe1f6-115">Informazio gehiago lortzeko, ikusi [Sortu Azure Data Lake Storage Gen2 biltegiratze kontua](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-quickstart-create-account)</span><span class="sxs-lookup"><span data-stu-id="fe1f6-115">For more information, see [Create an Azure Data Lake Storage Gen2 storage account](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-quickstart-create-account)</span></span>

## <a name="add-a-new-workflow"></a><span data-ttu-id="fe1f6-116">Gehitu lan-fluxu bat</span><span class="sxs-lookup"><span data-stu-id="fe1f6-116">Add a new workflow</span></span>

1. <span data-ttu-id="fe1f6-117">Joan **Adimena** > **Eredu pertsonalizatuak** eta hautatu **Lan-fluxu berria**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-117">Go to **Intelligence** > **Custom models** and select **New workflow**.</span></span>

1. <span data-ttu-id="fe1f6-118">Eman zure pertsonalizatutako eredua ezaguna den izena **Izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-118">Give your custom model a recognizable name in the **Name** field.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="fe1f6-119">![Lan-fluxu berriaren panelaren pantaila](media/new-workflowv2.png "Lan-fluxu berriaren panelaren pantaila")</span><span class="sxs-lookup"><span data-stu-id="fe1f6-119">![Screenshot of the New workflow pane](media/new-workflowv2.png "Screenshot of the New workflow pane")</span></span>

1. <span data-ttu-id="fe1f6-120">Hautatu web zerbitzua biltzen duen erakundea **Zure web zerbitzua duen maizterrak**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-120">Select the organization that contains the web service in **Tenant that contains your web service**.</span></span>

1. <span data-ttu-id="fe1f6-121">Azure Ikaskuntza automatiko harpidetza Customer Insights baino beste maizter bat baldin baduzu, hautatu **saioa hasi** hautatutako erakundearen zure egiaztagiriekin.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-121">If your Azure Machine Learning subscription is in a different tenant than Customer Insights, select **Sign in** with your credentials for the selected organization.</span></span>

1. <span data-ttu-id="fe1f6-122">Aukeratu web zerbitzuarekin erlazionatutako **Laneko areak**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-122">Select the **Workspaces** associated with your web service.</span></span> <span data-ttu-id="fe1f6-123">Bi atal daude zerrendatuta, bata Azure Machine Learning v1-entzat (Machine Learning Studio (klasikoa)) eta bestea Azure Machine Learning v2-rentzat (Azure Machine Learning).</span><span class="sxs-lookup"><span data-stu-id="fe1f6-123">There are two sections listed, one for Azure Machine Learning v1 (Machine Learning Studio (classic)) and Azure Machine Learning v2 (Azure Machine Learning).</span></span> <span data-ttu-id="fe1f6-124">Ez badakizu ziur zein laneko espazio den egokia Machine Learning Studio (klasikoa) web zerbitzurako, hautatu **Edozein**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-124">If you're not sure which workspace is the right one for your Machine Learning Studio (classic) web service, select **Any**.</span></span>

1. <span data-ttu-id="fe1f6-125">Aukeratu Machine Learning Studio (klasikoa) web zerbitzua edo Azure Machine Learning-en bideratzea **Zure eredua duen web zerbitzua** goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-125">Choose the Machine Learning Studio (classic) web service or Azure Machine Learning pipeline in the **Web service that contains your model** dropdown.</span></span> <span data-ttu-id="fe1f6-126">Ondoren, hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-126">Then, select **Next**.</span></span>
   - <span data-ttu-id="fe1f6-127">Lortu informazio gehiago [Machine Learning Studio-n (klasikoa) web zerbitzuan argitaratzeari buruz](https://docs.microsoft.com/azure/machine-learning/studio/deploy-a-machine-learning-web-service#deploy-it-as-a-new-web-service)</span><span class="sxs-lookup"><span data-stu-id="fe1f6-127">Learn more about [publishing a web service in Machine Learning Studio (classic)](https://docs.microsoft.com/azure/machine-learning/studio/deploy-a-machine-learning-web-service#deploy-it-as-a-new-web-service)</span></span>
   - <span data-ttu-id="fe1f6-128">Lortu informazio gehiago [Azure Machine Learning-en bideratze bat diseinatzailea](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-designer) edo [SDK](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-python-sdk) erabiliz argitaratzeari buruz.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-128">Learn more about [publishing a pipeline in Azure Machine Learning using the designer](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-designer) or [SDK](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-python-sdk).</span></span> <span data-ttu-id="fe1f6-129">Zure bideratzea [bideratzearen amaiera-puntuan](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer#submit-a-pipeline-run) argitaratu behar da.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-129">Your pipeline must be published under a [pipeline endpoint](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer#submit-a-pipeline-run).</span></span>

1. <span data-ttu-id="fe1f6-130">**Web zerbitzuaren sarrera** bakoitzeko,hautatu bat datorren **Entitatea** hartzaileei buruzko xehetasunetan eta sakatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-130">For each **Web service input**, select the matching **Entity** from audience insights and select **Next**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="fe1f6-131">Eredu pertsonalizatuko lan-fluxuak heuristika aplikatuko du web zerbitzuko sarrerako eremuak entitatearen atributuei esleitzeko eremuaren izenean eta datu motan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-131">The custom model workflow will apply heuristics to map the web service input fields to the entity attributes based on the name and data type of the field.</span></span> <span data-ttu-id="fe1f6-132">Akats bat ikusiko duzu web zerbitzu eremua entitate batera esleitu ezin bada.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-132">You'll see an error if a web service field can't be mapped to an entity.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="fe1f6-133">![Konfiguratu lan-fluxu bat](media/intelligence-screen2-updated.png "Konfiguratu lan-fluxu bat")</span><span class="sxs-lookup"><span data-stu-id="fe1f6-133">![Configure a workflow](media/intelligence-screen2-updated.png "Configure a workflow")</span></span>
   
1. <span data-ttu-id="fe1f6-134">**Ereduaren irteerako parametroak** urratsean ezarri propietate hauek:</span><span class="sxs-lookup"><span data-stu-id="fe1f6-134">In the **Model Output Parameters** step, set the following properties:</span></span>
   - <span data-ttu-id="fe1f6-135">Machine Learning Studio (klasikoa)</span><span class="sxs-lookup"><span data-stu-id="fe1f6-135">Machine Learning Studio (classic)</span></span>
      1. <span data-ttu-id="fe1f6-136">Sartu web zerbitzuaren irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-136">Enter the output **Entity name** you want web service output results to flow into.</span></span>
   - <span data-ttu-id="fe1f6-137">Azure ikaskuntza automatikoa</span><span class="sxs-lookup"><span data-stu-id="fe1f6-137">Azure Machine Learning</span></span>
      1. <span data-ttu-id="fe1f6-138">Sartu bideratzearen irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-138">Enter the output **Entity name** you want pipeline output results to flow into.</span></span>
      1. <span data-ttu-id="fe1f6-139">Aukeratu sortako bideratzearen **Irteerako datu-biltegi parametroaren izena** goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-139">Select the **Output data store parameter name** of your batch pipeline from the dropdown.</span></span>
      1. <span data-ttu-id="fe1f6-140">Aukeratu sortako bideratzearen **Irteerako bide-izenaren parametroaren izena** goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-140">Select the **Output Path parameter name** of your batch pipeline from the dropdown.</span></span>
      
      > [!div class="mx-imgBorder"]
      > <span data-ttu-id="fe1f6-141">![Ereduaren irteerako parametroen panela](media/intelligence-screen3-outputparameters.png "Ereduaren irteerako parametroen panela")</span><span class="sxs-lookup"><span data-stu-id="fe1f6-141">![Model Output Parameter Pane](media/intelligence-screen3-outputparameters.png "Model Output Parameter Pane")</span></span>

1. <span data-ttu-id="fe1f6-142">Hautatu bat egiten duen atributua **Customer ID emaitzetan** goitibeherako zerrendan zeinak zure bezeroa identifikatzen duen eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-142">Select the matching attribute from the **Customer ID in results** drop-down list that identifies customers and select **Save**.</span></span>
   
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="fe1f6-143">![Erlazionatu emaitzak bezeroaren datuen panelarekin](media/intelligence-screen4-relatetocustomer.png "Erlazionatu emaitzak bezeroaren datuen panelarekin")</span><span class="sxs-lookup"><span data-stu-id="fe1f6-143">![Relate results to Customer data pane](media/intelligence-screen4-relatetocustomer.png "Relate results to Customer data pane")</span></span>

1. <span data-ttu-id="fe1f6-144">Ikusiko duzu **Lan-fluxua gordeta** pantaila lan-fluxuei buruzko xehetasunak.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-144">You'll see the **Workflow Saved** screen with details about the workflow.</span></span>    
   <span data-ttu-id="fe1f6-145">Azure Machine Learning-eko bideratze baterako lan-fluxua konfiguratu baduzu, hartzaileei buruzko informazioa bideratzea duen laneko arean txertatuko da.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-145">If you configured a workflow for an Azure Machine Learning pipeline, audience insights will attach to the workspace that contains the pipeline.</span></span> <span data-ttu-id="fe1f6-146">Hartzaileei buruzko xehetasunek **Kolaboratzaile** funtzioa izango dute Azure laneko arean.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-146">Audience insights will get a **Contributor** role on the Azure workspace.</span></span>

1. <span data-ttu-id="fe1f6-147">Hautatu **Eginda**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-147">Select **Done**.</span></span>

1. <span data-ttu-id="fe1f6-148">Orain laneko fluxua exekutatu dezakezu **Eredu pertsonalizatuak** orritik.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-148">You can now run the workflow from the **Custom Models** page.</span></span>

## <a name="edit-a-workflow"></a><span data-ttu-id="fe1f6-149">Editatu lan-fluxua</span><span class="sxs-lookup"><span data-stu-id="fe1f6-149">Edit a workflow</span></span>

1. <span data-ttu-id="fe1f6-150">Gainean **Neurrira egindako ereduak** orrialdean, hautatu elipsis bertikala **Ekintzak** lehen sortu eta hautatu duzun fluxu ondoko zutabea **Editatu**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-150">On the **Custom Models** page, select the vertical ellipsis in the **Actions** column next to a workflow you've previously created and select **Edit**.</span></span>

1. <span data-ttu-id="fe1f6-151">Laneko fluxuaren izen ezaguna eguneratu dezakezu **Bistaratzeko izena** eremuan, baina ezin duzu konfiguratutako web zerbitzu edo bideratzea aldatu.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-151">You can update your workflow's recognizable name in the **Display name** field, but you can't change the configured web service or pipeline.</span></span> <span data-ttu-id="fe1f6-152">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-152">Select **Next**.</span></span>

1. <span data-ttu-id="fe1f6-153">**Web zerbitzuaren sarrera** bakoitzeko, bat datorren **Entitatea** egunera dezakezu hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-153">For each **Web service input**, you can update the matching **Entity** from audience insights.</span></span> <span data-ttu-id="fe1f6-154">Ondoren, hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-154">Then, select **Next**.</span></span>

1. <span data-ttu-id="fe1f6-155">**Ereduaren irteerako parametroak** urratsean ezarri propietate hauek:</span><span class="sxs-lookup"><span data-stu-id="fe1f6-155">In the **Model Output Parameters** step, set the following properties:</span></span>
   - <span data-ttu-id="fe1f6-156">Machine Learning Studio (klasikoa)</span><span class="sxs-lookup"><span data-stu-id="fe1f6-156">Machine Learning Studio (classic)</span></span>
      1. <span data-ttu-id="fe1f6-157">Sartu web zerbitzuaren irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-157">Enter the output **Entity name** you want web service output results to flow into.</span></span>
   - <span data-ttu-id="fe1f6-158">Azure ikaskuntza automatikoa</span><span class="sxs-lookup"><span data-stu-id="fe1f6-158">Azure Machine Learning</span></span>
      1. <span data-ttu-id="fe1f6-159">Sartu bideratzearen irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-159">Enter the output **Entity name** you want pipeline output results to flow into.</span></span>
      1. <span data-ttu-id="fe1f6-160">Aukeratu **irteerako datu-biltegi parametroaren izena** zure probako bideratzerako.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-160">Select the **Output data store parameter name** for your test pipeline.</span></span>
      1. <span data-ttu-id="fe1f6-161">Aukeratu **irteerako bide-izenaren parametroaren izena** zure probako bideratzerako.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-161">Select the **Output Path parameter name** for your test pipeline.</span></span>

1. <span data-ttu-id="fe1f6-162">Hautatu bat egiten duen atributua **Customer ID emaitzetan** goitibeherako zerrendan zeinak zure bezeroa identifikatzen duen eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-162">Select the matching attribute from the **Customer ID in results** drop-down list that identifies customers and select **Save**.</span></span>
   <span data-ttu-id="fe1f6-163">Inferentziako irteeratik atributu bat aukeratu behar duzu bezeroaren entitatearen Bezeroaren ID zutabearen antzeko balioekin.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-163">You need to choose an attribute from the inference output with values similar to the Customer ID column of the Customer entity.</span></span> <span data-ttu-id="fe1f6-164">Zure datu multzoan horrelako zutaberik ez baduzu, aukeratu errenkada modu esklusiboan identifikatzen duen atributu bat.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-164">If don't have such a column in your data set, choose an attribute that uniquely identifies the row.</span></span>

## <a name="run-a-workflow"></a><span data-ttu-id="fe1f6-165">Lan-fluxuak exekutau</span><span class="sxs-lookup"><span data-stu-id="fe1f6-165">Run a workflow</span></span>

1. <span data-ttu-id="fe1f6-166">**Pertsonalizatutako ereduak** orrian, hautatu elipsi bertikala **Ekintzak** zutabean aurrez sortu duzun lan-korrontearen ondoan.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-166">On the **Custom Models** page, select the vertical ellipsis in the **Actions** column next to a workflow you've previously created.</span></span>

1. <span data-ttu-id="fe1f6-167">Hautatu **Exekutatu**.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-167">Select **Run**.</span></span>

<span data-ttu-id="fe1f6-168">Zure lan-fluxua automatikoki exekutatzen da programatutako freskagarri bakoitzarekin.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-168">Your workflow also runs automatically with every scheduled refresh.</span></span> <span data-ttu-id="fe1f6-169">Argibide gehiago [programatutako freskagarriak konfiguratuz](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="fe1f6-169">Learn more about [setting up scheduled refreshes](system.md#schedule-tab).</span></span>

## <a name="delete-a-workflow"></a><span data-ttu-id="fe1f6-170">Ezabatu lan-fluxua</span><span class="sxs-lookup"><span data-stu-id="fe1f6-170">Delete a workflow</span></span>

1. <span data-ttu-id="fe1f6-171">**Pertsonalizatutako ereduak** orrian, hautatu elipsi bertikala **Ekintzak** zutabean aurrez sortu duzun lan-korrontearen ondoan.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-171">On the **Custom Models** page, select the vertical ellipsis in the **Actions** column next to a workflow you've previously created.</span></span>

1. <span data-ttu-id="fe1f6-172">Hautatu **Ezabatu** eta berretsi ezabatzea.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-172">Select **Delete** and confirm your deletion.</span></span>

<span data-ttu-id="fe1f6-173">Zure lan-fluxua ezabatu egingo da.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-173">Your workflow will be deleted.</span></span> <span data-ttu-id="fe1f6-174">[Entitatea](entities.md) lan-fluxua sortu zuenean sortu zen mantendu egingo da eta ikusi egin daiteke **Entitateak** orrian.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-174">The [entity](entities.md) that was created when you created the workflow persists, and can be viewed from the **Entities** page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]