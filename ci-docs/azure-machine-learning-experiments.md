---
title: Azure Machine Learning-en esperimentuak
description: 'Erabili Azure Machine Learning-en oinarritutako ereduak hemen: Dynamics 365 Customer Insights.'
ms.date: 12/02/2021
ms.subservice: audience-insights
ms.topic: tutorial
author: naravill
ms.author: naravill
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: cefd037a021b669e827f0593d63b938d452963f7
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642106"
---
# <a name="use-azure-machine-learning-based-models"></a>Erabili Azure Machine Learning-en oinarritutako ereduak

Dynamics 365 Customer Insights-eko datu bateratuak negozioaren ikuspegi osagarriak sor ditzaketen ikaskuntza automatiko ereduak eraikitzeko iturria da. Customer Insights Azure Machine Learning-ekin integratzen da zure pertsonalizatutako ereduak erabiltzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- Sartu Customer Insights-era
- Aktibatu Azure Enterprise harpidetza
- [Bezeroen profil bateratuak](data-unification.md)
- [Azure Blob biltegira esportatzeko entitatea](export-azure-blob-storage.md) konfiguratuta

## <a name="set-up-azure-machine-learning-workspace"></a>Konfiguratu Azure Machine Learning-en laneko area

1. Ikusi [sortu Azure Machine Learning-en laneko area](/azure/machine-learning/concept-workspace#-create-a-workspace) atala, laneko area sortzeko aukera desberdinetarako. Errendimendu onena lortzeko, sortu laneko area zure Customer Insights ingurunetik geografikoki hurbilen dagoen Azure eskualde batean.

1. Sar zaitez zure laneko areara [Azure Machine Learning Studio](https://ml.azure.com/) bidez. Laneko arearekin [elkarreragiteko](/azure/machine-learning/concept-workspace#tools-for-workspace-interaction) hainbat modu daude.

## <a name="work-with-azure-machine-learning-designer"></a>Lan egin Azure Machine Learning-en diseinatzailearekin

Azure Ikaskuntza automatiko diseinatzaileak ikusizko mihise bat eskaintzen du, non datu multzoak eta moduluak arrastatu eta jar ditzakezun. Diseinatzailetik sortutako sorta bideratzea Customer Insights-en sar daiteke, hala konfiguratuta badago. 
   
## <a name="working-with-azure-machine-learning-sdk"></a>Azure Machine Learning-en SDKrekin lan egitea

Datu zientzialariek eta AA garatzaileek [Azure Machine Learning-en SDK](/python/api/overview/azure/ml/?preserve-view=true&view=azure-ml-py) erabiltzen dute ikaskuntza automatikoko lan fluxuak eraikitzeko. Gaur egun, SDK erabiliz trebatutako ereduak ezin dira zuzenean Customer Insights-ekin integratu. Eredu hori erabiltzen duen sortako interferentzia-bideratzea behar da Customer Insights-ekin integratzeko.

## <a name="batch-pipeline-requirements-to-integrate-with-customer-insights"></a>Sorta bideratzearen eskakizunak Customer Insights-ekin integratzeko

### <a name="dataset-configuration"></a>Datu multzoaren konfigurazioa

Datu multzoak sortu behar dituzu Customer Insights-eko entitate datuak zure sortako inferentzia-bideratzean erabiltzeko. Datu multzo hauek laneko arean erregistratu behar dira. Gaur egun, [datu multzo tabularrak](/azure/machine-learning/how-to-create-register-datasets#tabulardataset) soilik onartzen ditugu, .csv formatuan. Entitateen datuei dagozkien datu multzoak bideratze-parametro gisa parametrizatu behar dira.
   
* Diseinatzaileko datu multzoen parametroak
   
     Diseinatzailean, ireki **Aukeratu zutabeak datu multzoan** eta hautatu **Ezarri bideratze-parametro gisa**; bertan parametroaren izena ipini behar da.

     > [!div class="mx-imgBorder"]
     > ![Diseinatzaileko datu multzoen parametrizazioa.](media/intelligence-designer-dataset-parameters.png "Diseinatzaileko datu multzoen parametrizazioa")
   
* Datu multzoaren parametroa SDK-n (Python)
   
   ```python
   HotelStayActivity_dataset = Dataset.get_by_name(ws, name='Hotel Stay Activity Data')
   HotelStayActivity_pipeline_param = PipelineParameter(name="HotelStayActivity_pipeline_param", default_value=HotelStayActivity_dataset)
   HotelStayActivity_ds_consumption = DatasetConsumptionConfig("HotelStayActivity_dataset", HotelStayActivity_pipeline_param)
   ```

### <a name="batch-inference-pipeline"></a>Sortako inferentzia-bideratzea
  
* Diseinatzailean, trebakuntza-bideratze bat erabil daiteke inferentzia-bideratze bat sortzeko edo eguneratzeko. Gaur egun, sortako inferentzia-bideratzeak soilik onartzen dira.

* SDK erabiliz, bideratzea amaiera-puntu batean argitaratu dezakezu. Gaur egun, Customer Insights lehenetsitako bideratzearekin integratzen da Machine Learning-en laneko areako sortako bideratzearen amaiera-puntu batean.
   
   ```python
   published_pipeline = pipeline.publish(name="ChurnInferencePipeline", description="Published Churn Inference pipeline")
   pipeline_endpoint = PipelineEndpoint.get(workspace=ws, name="ChurnPipelineEndpoint") 
   pipeline_endpoint.add_default(pipeline=published_pipeline)
   ```

### <a name="import-pipeline-data-into-customer-insights"></a>Inportatu bideratzearen datuak Customer Insights-era

* Diseinatzaileak [Esportatu datuak modulua](/azure/machine-learning/algorithm-module-reference/export-data) eskaintzen du; horrek bideratze baten irteera Azure biltegira esportatzea ahalbidetzen du. Gaur egun, moduluak **Azure blob biltegiratzea** datu-biltegi mota erabili behar du eta **datu-biltegia** eta dagokion **bide-izena** parametrizatu. Customer Insights-ek parametro horiek biak gainidazten ditu bideratzea exekutatzerakoan produktuak eskuragarri duen datu biltegi eta bide-izen batekin.
   > [!div class="mx-imgBorder"]
   > ![Esportatu datuen moduluaren konfigurazioa.](media/intelligence-designer-importdata.png "Esportatu datuen moduluaren konfigurazioa")
   
* Inferentziaren irteera kodea erabiliz idaztean, irteera karga dezakezu laneko areako *erregistratutako datu-biltegiko* bide-izen batera. Bide-izena eta datu-biltegia bideratzean parametrizatuta badaude, Customer Insights-ek inferentzia irteera irakurri eta inportatu ahal izango du. Gaur egun, csv formatuko tabular bakarreko irteera onartzen da. Bide-izenak direktorioa eta fitxategi-izena izan behar ditu.

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


[!INCLUDE [footer-include](includes/footer-banner.md)]