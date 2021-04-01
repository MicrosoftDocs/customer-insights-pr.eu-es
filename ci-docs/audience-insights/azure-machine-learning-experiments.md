---
title: Azure Machine Learning-en esperimentuak
description: 'Erabili Azure Machine Learning-en oinarritutako ereduak hemen: Dynamics 365 Customer Insights.'
ms.date: 11/30/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: naravill
ms.author: naravill
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: edd2cf488b52cef87b09b90336e48fdc7f470a68
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597404"
---
# <a name="use-azure-machine-learning-based-models"></a><span data-ttu-id="b0588-103">Erabili Azure Machine Learning-en oinarritutako ereduak</span><span class="sxs-lookup"><span data-stu-id="b0588-103">Use Azure Machine Learning-based models</span></span>

<span data-ttu-id="b0588-104">Dynamics 365 Customer Insights-eko datu bateratuak negozioaren ikuspegi osagarriak sor ditzaketen ikaskuntza automatiko ereduak eraikitzeko iturria da.</span><span class="sxs-lookup"><span data-stu-id="b0588-104">The unified data in Dynamics 365 Customer Insights is a source for building machine learning models that can generate additional business insights.</span></span> <span data-ttu-id="b0588-105">Customer Insights Machine Learning Studio-rekin (klasikoa) eta Azure Machine Learning-ekin integratzen da zure eredu pertsonalizatuak erabiltzeko.</span><span class="sxs-lookup"><span data-stu-id="b0588-105">Customer Insights integrates with Machine Learning Studio (classic) and Azure Machine Learning to use your own custom models.</span></span> <span data-ttu-id="b0588-106">Joan [Machine Learning Studio (klasikoa) esperimentuak](machine-learning-studio-experiments.md) atalera Machine Learning Studio-n (klasikoa) eraikitako esperimentuen adibideak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="b0588-106">Refer to [Machine Learning Studio (classic) experiments](machine-learning-studio-experiments.md) for examples of experiments built on Machine Learning Studio (classic).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b0588-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="b0588-107">Prerequisites</span></span>

- <span data-ttu-id="b0588-108">Sartu Customer Insights-era</span><span class="sxs-lookup"><span data-stu-id="b0588-108">Access to Customer Insights</span></span>
- <span data-ttu-id="b0588-109">Aktibatu Azure Enterprise harpidetza</span><span class="sxs-lookup"><span data-stu-id="b0588-109">Active Azure Enterprise subscription</span></span>
- [<span data-ttu-id="b0588-110">Bezeroen profil bateratuak</span><span class="sxs-lookup"><span data-stu-id="b0588-110">Unified customer profiles</span></span>](data-unification.md)
- <span data-ttu-id="b0588-111">[Azure Blob biltegira esportatzeko entitatea](export-azure-blob-storage.md) konfiguratuta</span><span class="sxs-lookup"><span data-stu-id="b0588-111">[Entity export to Azure Blob storage](export-azure-blob-storage.md) configured</span></span>

## <a name="set-up-azure-machine-learning-workspace"></a><span data-ttu-id="b0588-112">Konfiguratu Azure Machine Learning-en laneko area</span><span class="sxs-lookup"><span data-stu-id="b0588-112">Set up Azure Machine Learning workspace</span></span>

1. <span data-ttu-id="b0588-113">Ikusi [sortu Azure Machine Learning-en laneko area](/azure/machine-learning/concept-workspace#-create-a-workspace) atala, laneko area sortzeko aukera desberdinetarako.</span><span class="sxs-lookup"><span data-stu-id="b0588-113">See [create a Azure Machine Learning workspace](/azure/machine-learning/concept-workspace#-create-a-workspace) for different options to create the workspace.</span></span> <span data-ttu-id="b0588-114">Errendimendu onena lortzeko, sortu laneko area zure Customer Insights ingurunetik geografikoki hurbilen dagoen Azure eskualde batean.</span><span class="sxs-lookup"><span data-stu-id="b0588-114">For best performance, create the workspace in an Azure region that is geographically closest to your Customer Insights environment.</span></span>

1. <span data-ttu-id="b0588-115">Sar zaitez zure laneko areara [Azure Machine Learning Studio](https://ml.azure.com/) bidez.</span><span class="sxs-lookup"><span data-stu-id="b0588-115">Access your workspace through the [Azure Machine Learning Studio](https://ml.azure.com/).</span></span> <span data-ttu-id="b0588-116">Laneko arearekin [elkarreragiteko](/azure/machine-learning/concept-workspace#tools-for-workspace-interaction) hainbat modu daude.</span><span class="sxs-lookup"><span data-stu-id="b0588-116">There are several [ways to interact](/azure/machine-learning/concept-workspace#tools-for-workspace-interaction) with your workspace.</span></span>

## <a name="work-with-azure-machine-learning-designer"></a><span data-ttu-id="b0588-117">Lan egin Azure Machine Learning-en diseinatzailearekin</span><span class="sxs-lookup"><span data-stu-id="b0588-117">Work with Azure Machine Learning designer</span></span>

<span data-ttu-id="b0588-118">Azure Machine Learning-en diseinatzaileak mihise bisuala eskaintzen du, datu multzoak eta moduluak arrastatu eta jaregin ahal izateko, Machine Learning Studio-ren (klasikoa) antzera.</span><span class="sxs-lookup"><span data-stu-id="b0588-118">Azure Machine Learning designer provides a visual canvas where you can drag and drop datasets and modules, similar to Machine Learning Studio (classic).</span></span> <span data-ttu-id="b0588-119">Diseinatzailetik sortutako sorta bideratzea Customer Insights-en sar daiteke, hala konfiguratuta badago.</span><span class="sxs-lookup"><span data-stu-id="b0588-119">A batch pipeline created from the designer can be integrated into Customer Insights if they are configured accordingly.</span></span> 
   
## <a name="working-with-azure-machine-learning-sdk"></a><span data-ttu-id="b0588-120">Azure Machine Learning-en SDKrekin lan egitea</span><span class="sxs-lookup"><span data-stu-id="b0588-120">Working with Azure Machine Learning SDK</span></span>

<span data-ttu-id="b0588-121">Datu zientzialariek eta AA garatzaileek [Azure Machine Learning-en SDK](/python/api/overview/azure/ml/?preserve-view=true&view=azure-ml-py) erabiltzen dute ikaskuntza automatikoko lan fluxuak eraikitzeko.</span><span class="sxs-lookup"><span data-stu-id="b0588-121">Data scientists and AI developers use the [Azure Machine Learning SDK](/python/api/overview/azure/ml/?preserve-view=true&view=azure-ml-py) to build machine learning workflows.</span></span> <span data-ttu-id="b0588-122">Gaur egun, SDK erabiliz trebatutako ereduak ezin dira zuzenean Customer Insights-ekin integratu.</span><span class="sxs-lookup"><span data-stu-id="b0588-122">Currently, models trained using the SDK can't be integrated directly with Customer Insights.</span></span> <span data-ttu-id="b0588-123">Eredu hori erabiltzen duen sortako interferentzia-bideratzea behar da Customer Insights-ekin integratzeko.</span><span class="sxs-lookup"><span data-stu-id="b0588-123">A batch inference pipeline that consumes that model is required for integration with Customer Insights.</span></span>

## <a name="batch-pipeline-requirements-to-integrate-with-customer-insights"></a><span data-ttu-id="b0588-124">Sorta bideratzearen eskakizunak Customer Insights-ekin integratzeko</span><span class="sxs-lookup"><span data-stu-id="b0588-124">Batch pipeline requirements to integrate with Customer Insights</span></span>

### <a name="dataset-configuration"></a><span data-ttu-id="b0588-125">Datu multzoaren konfigurazioa</span><span class="sxs-lookup"><span data-stu-id="b0588-125">Dataset Configuration</span></span>

<span data-ttu-id="b0588-126">Datu multzoak sortu behar dituzu Customer Insights-eko entitate datuak zure sortako inferentzia-bideratzean erabiltzeko.</span><span class="sxs-lookup"><span data-stu-id="b0588-126">You need to create datasets to use entity data from Customer Insights to your batch inference pipeline.</span></span> <span data-ttu-id="b0588-127">Datu multzo hauek laneko arean erregistratu behar dira.</span><span class="sxs-lookup"><span data-stu-id="b0588-127">These datasets need to be registered in the workspace.</span></span> <span data-ttu-id="b0588-128">Gaur egun, [datu multzo tabularrak](/azure/machine-learning/how-to-create-register-datasets#tabulardataset) soilik onartzen ditugu, .csv formatuan.</span><span class="sxs-lookup"><span data-stu-id="b0588-128">Currently, we only support [tabular datasets](/azure/machine-learning/how-to-create-register-datasets#tabulardataset) in .csv format.</span></span> <span data-ttu-id="b0588-129">Entitateen datuei dagozkien datu multzoak bideratze-parametro gisa parametrizatu behar dira.</span><span class="sxs-lookup"><span data-stu-id="b0588-129">The datasets that correspond to entity data need to be parameterized as a pipeline parameter.</span></span>
   
* <span data-ttu-id="b0588-130">Diseinatzaileko datu multzoen parametroak</span><span class="sxs-lookup"><span data-stu-id="b0588-130">Dataset parameters in Designer</span></span>
   
     <span data-ttu-id="b0588-131">Diseinatzailean, ireki **Aukeratu zutabeak datu multzoan** eta hautatu **Ezarri bideratze-parametro gisa**; bertan parametroaren izena ipini behar da.</span><span class="sxs-lookup"><span data-stu-id="b0588-131">In the designer, open **Select Columns in Dataset** and select **Set as pipeline parameter** where you provide a name for the parameter.</span></span>

     > [!div class="mx-imgBorder"]
     > <span data-ttu-id="b0588-132">![Diseinatzaileko datu multzoen parametrizazioa](media/intelligence-designer-dataset-parameters.png "Diseinatzaileko datu multzoen parametrizazioa")</span><span class="sxs-lookup"><span data-stu-id="b0588-132">![Dataset parameterization in designer](media/intelligence-designer-dataset-parameters.png "Dataset parameterization in designer")</span></span>
   
* <span data-ttu-id="b0588-133">Datu multzoaren parametroa SDK-n (Python)</span><span class="sxs-lookup"><span data-stu-id="b0588-133">Dataset parameter in SDK (Python)</span></span>
   
   ```python
   HotelStayActivity_dataset = Dataset.get_by_name(ws, name='Hotel Stay Activity Data')
   HotelStayActivity_pipeline_param = PipelineParameter(name="HotelStayActivity_pipeline_param", default_value=HotelStayActivity_dataset)
   HotelStayActivity_ds_consumption = DatasetConsumptionConfig("HotelStayActivity_dataset", HotelStayActivity_pipeline_param)
   ```

### <a name="batch-inference-pipeline"></a><span data-ttu-id="b0588-134">Sortako inferentzia-bideratzea</span><span class="sxs-lookup"><span data-stu-id="b0588-134">Batch inference pipeline</span></span>
  
* <span data-ttu-id="b0588-135">Diseinatzailean, trebakuntza-bideratze bat erabil daiteke inferentzia-bideratze bat sortzeko edo eguneratzeko.</span><span class="sxs-lookup"><span data-stu-id="b0588-135">In the designer, a training pipeline can be used to create or update an inference pipeline.</span></span> <span data-ttu-id="b0588-136">Gaur egun, sortako inferentzia-bideratzeak soilik onartzen dira.</span><span class="sxs-lookup"><span data-stu-id="b0588-136">Currently, only batch inference pipelines are supported.</span></span>

* <span data-ttu-id="b0588-137">SDK erabiliz, bideratzea amaiera-puntu batean argitaratu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="b0588-137">Using the SDK, you can publish the pipeline to an endpoint.</span></span> <span data-ttu-id="b0588-138">Gaur egun, Customer Insights lehenetsitako bideratzearekin integratzen da Machine Learning-en laneko areako sortako bideratzearen amaiera-puntu batean.</span><span class="sxs-lookup"><span data-stu-id="b0588-138">Currently, Customer Insights integrates with the default pipeline in a batch pipeline endpoint in the Machine Learning workspace.</span></span>
   
   ```python
   published_pipeline = pipeline.publish(name="ChurnInferencePipeline", description="Published Churn Inference pipeline")
   pipeline_endpoint = PipelineEndpoint.get(workspace=ws, name="ChurnPipelineEndpoint") 
   pipeline_endpoint.add_default(pipeline=published_pipeline)
   ```

### <a name="import-pipeline-data-into-customer-insights"></a><span data-ttu-id="b0588-139">Inportatu bideratzearen datuak Customer Insights-era</span><span class="sxs-lookup"><span data-stu-id="b0588-139">Import pipeline data into Customer Insights</span></span>

* <span data-ttu-id="b0588-140">Diseinatzaileak [Esportatu datuak modulua](/azure/machine-learning/algorithm-module-reference/export-data) eskaintzen du; horrek bideratze baten irteera Azure biltegira esportatzea ahalbidetzen du.</span><span class="sxs-lookup"><span data-stu-id="b0588-140">The designer provides the [Export Data module](/azure/machine-learning/algorithm-module-reference/export-data) that allows the output of a pipeline to be exported to Azure storage.</span></span> <span data-ttu-id="b0588-141">Gaur egun, moduluak **Azure blob biltegiratzea** datu-biltegi mota erabili behar du eta **datu-biltegia** eta dagokion **bide-izena** parametrizatu.</span><span class="sxs-lookup"><span data-stu-id="b0588-141">Currently, the module must use the datastore type **Azure Blob Storage** and parameterize the **Datastore** and relative **Path**.</span></span> <span data-ttu-id="b0588-142">Customer Insights-ek parametro horiek biak gainidazten ditu bideratzea exekutatzerakoan produktuak eskuragarri duen datu biltegi eta bide-izen batekin.</span><span class="sxs-lookup"><span data-stu-id="b0588-142">Customer Insights overrides both these parameters during pipeline execution with a datastore and path that is accessible to the product.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="b0588-143">![Esportatu datuen moduluaren konfigurazioa](media/intelligence-designer-importdata.png "Esportatu datuen moduluaren konfigurazioa")</span><span class="sxs-lookup"><span data-stu-id="b0588-143">![Export Data Module Configuration](media/intelligence-designer-importdata.png "Export Data Module Configuration")</span></span>
   
* <span data-ttu-id="b0588-144">Inferentziaren irteera kodea erabiliz idaztean, irteera karga dezakezu laneko areako *erregistratutako datu-biltegiko* bide-izen batera.</span><span class="sxs-lookup"><span data-stu-id="b0588-144">When writing the inference output using code, you can upload the output to the a path within a *registered datastore* in the workspace.</span></span> <span data-ttu-id="b0588-145">Bide-izena eta datu-biltegia bideratzean parametrizatuta badaude, Customer Insights-ek inferentzia irteera irakurri eta inportatu ahal izango du.</span><span class="sxs-lookup"><span data-stu-id="b0588-145">If the path and datastore are parameterized in the pipeline, Customer insights will be able to read and import the inference output.</span></span> <span data-ttu-id="b0588-146">Gaur egun, csv formatuko tabular bakarreko irteera onartzen da.</span><span class="sxs-lookup"><span data-stu-id="b0588-146">Currently, a single tabular output in csv format is supported.</span></span> <span data-ttu-id="b0588-147">Bide-izenak direktorioa eta fitxategi-izena izan behar ditu.</span><span class="sxs-lookup"><span data-stu-id="b0588-147">The path must include the directory and filename.</span></span>

   ```python
   # In Pipeline setup script
      OutputPathParameter = PipelineParameter(name="output_path", default_value="HotelChurnOutput/HotelChurnOutput.csv")
      OutputDatastoreParameter = PipelineParameter(name="output_datastore", default_value="workspaceblobstore")
   ...
   # In pipeline execution script
      run = Run.get_context()
      ws = run.experiment.workspace
      datastore = Datastore.get(ws, output_datastore) # output_datastore is parameterized
      directory_name =  os.path.dirname(output_path)  # output_path is parameterized.
      
      # Datastore.upload() or Dataset.File.upload_directory() are supported methods to uplaod the data
      # datastore.upload(src_dir=<<working directory>>, target_path=directory_name, overwrite=False, show_progress=True)
      output_dataset = Dataset.File.upload_directory(src_dir=<<working directory>>, target = (datastore, directory_name)) # Remove trailing "/" from directory_name
   ```


[!INCLUDE[footer-include](../includes/footer-banner.md)]