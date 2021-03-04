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
# <a name="custom-machine-learning-models"></a>Ikaskuntza automatiko eredu pertsonalizatuak

**Adimena** > **Eredu pertsonalizatuak** lan-fluxuak kudeatzeko aukera ematen dizu Azure Machine Learning-eko ereduetan oinarrituta. Lan-fluxuek xehetasunak sortu nahi dituzun datuak aukeratzen eta emaitzak bezeroaren datu bateratuekin esleitzen laguntzen zaituzte. Ikaskuntza automatikoko eredu pertsonalizatuak eraikitzeari buruzko informazio gehiago lortzeko, ikusi [Erabili Azure Machine Learning-en oinarritutako ereduak](azure-machine-learning-experiments.md).

## <a name="responsible-ai"></a>AA arduratsua

Iragarpenek bezeroen esperientzia hobeak sortzeko, negozio gaitasunak eta diru sarrera korronteak hobetzeko gaitasunak eskaintzen dituzte. Zure iragarpenaren balioa orekatzea gomendatzen dizugu, duen eraginaren eta modu etikoan sar daitezkeen alborapenen artean. Lortu informazio gehiago Microsoft-ek [AA arduratsua](https://www.microsoft.com/ai/responsible-ai?activetab=pivot1%3aprimaryr6) jorratzeko moduari buruz. Azure Machine Learning-en [Ikaskuntza automatiko modu arduratsuan erabiltzeko teknika eta prozesu](https://docs.microsoft.com/azure/machine-learning/concept-responsible-ml) jakinei buruz ikas dezakezu.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gaur egun, eginbide honek [Machine Learning Studio (klasikoa)](https://studio.azureml.net) eta [Azure Machine Learning sortako bideratzeak](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines) onartzen ditu.

- Ezaugarri hau erabiltzeko Azure Studio Lake instantziarekin lotutako Azure Data Lake Gen2 biltegiratze kontua behar duzu. Informazio gehiago lortzeko, ikusi [Sortu Azure Data Lake Storage Gen2 biltegiratze kontua](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-quickstart-create-account)

## <a name="add-a-new-workflow"></a>Gehitu lan-fluxu bat

1. Joan **Adimena** > **Eredu pertsonalizatuak** eta hautatu **Lan-fluxu berria**.

1. Eman zure pertsonalizatutako eredua ezaguna den izena **Izena** eremuan.

   > [!div class="mx-imgBorder"]
   > ![Lan-fluxu berriaren panelaren pantaila](media/new-workflowv2.png "Lan-fluxu berriaren panelaren pantaila")

1. Hautatu web zerbitzua biltzen duen erakundea **Zure web zerbitzua duen maizterrak**.

1. Azure Ikaskuntza automatiko harpidetza Customer Insights baino beste maizter bat baldin baduzu, hautatu **saioa hasi** hautatutako erakundearen zure egiaztagiriekin.

1. Aukeratu web zerbitzuarekin erlazionatutako **Laneko areak**. Bi atal daude zerrendatuta, bata Azure Machine Learning v1-entzat (Machine Learning Studio (klasikoa)) eta bestea Azure Machine Learning v2-rentzat (Azure Machine Learning). Ez badakizu ziur zein laneko espazio den egokia Machine Learning Studio (klasikoa) web zerbitzurako, hautatu **Edozein**.

1. Aukeratu Machine Learning Studio (klasikoa) web zerbitzua edo Azure Machine Learning-en bideratzea **Zure eredua duen web zerbitzua** goitibeherako zerrendan. Ondoren, hautatu **Hurrengoa**.
   - Lortu informazio gehiago [Machine Learning Studio-n (klasikoa) web zerbitzuan argitaratzeari buruz](https://docs.microsoft.com/azure/machine-learning/studio/deploy-a-machine-learning-web-service#deploy-it-as-a-new-web-service)
   - Lortu informazio gehiago [Azure Machine Learning-en bideratze bat diseinatzailea](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-designer) edo [SDK](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-python-sdk) erabiliz argitaratzeari buruz. Zure bideratzea [bideratzearen amaiera-puntuan](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer#submit-a-pipeline-run) argitaratu behar da.

1. **Web zerbitzuaren sarrera** bakoitzeko,hautatu bat datorren **Entitatea** hartzaileei buruzko xehetasunetan eta sakatu **Hurrengoa**.
   > [!NOTE]
   > Eredu pertsonalizatuko lan-fluxuak heuristika aplikatuko du web zerbitzuko sarrerako eremuak entitatearen atributuei esleitzeko eremuaren izenean eta datu motan oinarrituta. Akats bat ikusiko duzu web zerbitzu eremua entitate batera esleitu ezin bada.

   > [!div class="mx-imgBorder"]
   > ![Konfiguratu lan-fluxu bat](media/intelligence-screen2-updated.png "Konfiguratu lan-fluxu bat")
   
1. **Ereduaren irteerako parametroak** urratsean ezarri propietate hauek:
   - Machine Learning Studio (klasikoa)
      1. Sartu web zerbitzuaren irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.
   - Azure ikaskuntza automatikoa
      1. Sartu bideratzearen irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.
      1. Aukeratu sortako bideratzearen **Irteerako datu-biltegi parametroaren izena** goitibeherako zerrendan.
      1. Aukeratu sortako bideratzearen **Irteerako bide-izenaren parametroaren izena** goitibeherako zerrendan.
      
      > [!div class="mx-imgBorder"]
      > ![Ereduaren irteerako parametroen panela](media/intelligence-screen3-outputparameters.png "Ereduaren irteerako parametroen panela")

1. Hautatu bat egiten duen atributua **Customer ID emaitzetan** goitibeherako zerrendan zeinak zure bezeroa identifikatzen duen eta hautatu **Gorde**.
   
   > [!div class="mx-imgBorder"]
   > ![Erlazionatu emaitzak bezeroaren datuen panelarekin](media/intelligence-screen4-relatetocustomer.png "Erlazionatu emaitzak bezeroaren datuen panelarekin")

1. Ikusiko duzu **Lan-fluxua gordeta** pantaila lan-fluxuei buruzko xehetasunak.    
   Azure Machine Learning-eko bideratze baterako lan-fluxua konfiguratu baduzu, hartzaileei buruzko informazioa bideratzea duen laneko arean txertatuko da. Hartzaileei buruzko xehetasunek **Kolaboratzaile** funtzioa izango dute Azure laneko arean.

1. Hautatu **Eginda**.

1. Orain laneko fluxua exekutatu dezakezu **Eredu pertsonalizatuak** orritik.

## <a name="edit-a-workflow"></a>Editatu lan-fluxua

1. Gainean **Neurrira egindako ereduak** orrialdean, hautatu elipsis bertikala **Ekintzak** lehen sortu eta hautatu duzun fluxu ondoko zutabea **Editatu**.

1. Laneko fluxuaren izen ezaguna eguneratu dezakezu **Bistaratzeko izena** eremuan, baina ezin duzu konfiguratutako web zerbitzu edo bideratzea aldatu. Hautatu **Hurrengoa**.

1. **Web zerbitzuaren sarrera** bakoitzeko, bat datorren **Entitatea** egunera dezakezu hartzaileei buruzko xehetasunetan. Ondoren, hautatu **Hurrengoa**.

1. **Ereduaren irteerako parametroak** urratsean ezarri propietate hauek:
   - Machine Learning Studio (klasikoa)
      1. Sartu web zerbitzuaren irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.
   - Azure ikaskuntza automatikoa
      1. Sartu bideratzearen irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.
      1. Aukeratu **irteerako datu-biltegi parametroaren izena** zure probako bideratzerako.
      1. Aukeratu **irteerako bide-izenaren parametroaren izena** zure probako bideratzerako.

1. Hautatu bat egiten duen atributua **Customer ID emaitzetan** goitibeherako zerrendan zeinak zure bezeroa identifikatzen duen eta hautatu **Gorde**.
   Inferentziako irteeratik atributu bat aukeratu behar duzu bezeroaren entitatearen Bezeroaren ID zutabearen antzeko balioekin. Zure datu multzoan horrelako zutaberik ez baduzu, aukeratu errenkada modu esklusiboan identifikatzen duen atributu bat.

## <a name="run-a-workflow"></a>Lan-fluxuak exekutau

1. **Pertsonalizatutako ereduak** orrian, hautatu elipsi bertikala **Ekintzak** zutabean aurrez sortu duzun lan-korrontearen ondoan.

1. Hautatu **Exekutatu**.

Zure lan-fluxua automatikoki exekutatzen da programatutako freskagarri bakoitzarekin. Argibide gehiago [programatutako freskagarriak konfiguratuz](system.md#schedule-tab).

## <a name="delete-a-workflow"></a>Ezabatu lan-fluxua

1. **Pertsonalizatutako ereduak** orrian, hautatu elipsi bertikala **Ekintzak** zutabean aurrez sortu duzun lan-korrontearen ondoan.

1. Hautatu **Ezabatu** eta berretsi ezabatzea.

Zure lan-fluxua ezabatu egingo da. [Entitatea](entities.md) lan-fluxua sortu zuenean sortu zen mantendu egingo da eta ikusi egin daiteke **Entitateak** orrian.


[!INCLUDE[footer-include](../includes/footer-banner.md)]