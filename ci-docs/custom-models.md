---
title: Ikaskuntza automatiko eredu pertsonalizatuak | Microsoft Docs
description: Azure Ikaskuntza automatiko-en eredu pertsonalizatuekin lan egin Dynamics 365 Customer Insights.
ms.date: 12/01/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: tutorial
author: zacookmsft
ms.author: zacook
manager: shellyha
searchScope:
- ci-custom-models
- customerInsights
ms.openlocfilehash: 3fad8a6cba71da80d4cc34be4084275e0d0a3622
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9245788"
---
# <a name="custom-machine-learning-models"></a>Ikaskuntza automatiko eredu pertsonalizatuak

> [!NOTE]
> Ikaskuntza automatiko Studiorako laguntza (klasikoa) 2024ko abuztuaren 31n amaituko da. Hona trantsizioa egitea gomendatzen dizugu [Azure Ikaskuntza automatiko](/azure/machine-learning/overview-what-is-azure-machine-learning) data horretarako.
>
> 2021eko abenduaren 1etik aurrera, ezin izango dituzu sortu Ikaskuntza automatiko Studio (klasikoak) baliabide berriak. 2024ko abuztuaren 31ra arte, dauden Ikaskuntza automatiko Studio (klasikoak) baliabideak erabiltzen jarraitu dezakezu. Informazio gehiagorako, ikus [Migratu Azurera Ikaskuntza automatiko](/azure/machine-learning/migrate-overview).


**Adimena** > **Eredu pertsonalizatuak** lan-fluxuak kudeatzeko aukera ematen dizu Azure Machine Learning-eko ereduetan oinarrituta. Lan-fluxuek xehetasunak sortu nahi dituzun datuak aukeratzen eta emaitzak bezeroaren datu bateratuekin esleitzen laguntzen zaituzte. Ikaskuntza automatikoko eredu pertsonalizatuak eraikitzeari buruzko informazio gehiago lortzeko, ikusi [Erabili Azure Machine Learning-en oinarritutako ereduak](azure-machine-learning-experiments.md).

## <a name="responsible-ai"></a>AA arduratsua

Iragarpenek bezeroen esperientzia hobeak sortzeko, negozio gaitasunak eta diru sarrera korronteak hobetzeko gaitasunak eskaintzen dituzte. Zure iragarpenaren balioa orekatzea gomendatzen dizugu, duen eraginaren eta modu etikoan sar daitezkeen alborapenen artean. Lortu informazio gehiago Microsoft-ek [AA arduratsua](https://www.microsoft.com/ai/responsible-ai?activetab=pivot1%3aprimaryr6) jorratzeko moduari buruz. Azure Machine Learning-en [Ikaskuntza automatiko modu arduratsuan erabiltzeko teknika eta prozesu](/azure/machine-learning/concept-responsible-ml) jakinei buruz ikas dezakezu.

## <a name="prerequisites"></a>Aurrebaldintzak

- Eginbide honek bidez argitaratutako web zerbitzuak onartzen ditu [Azure Ikaskuntza automatiko loteen kanalizazioak](/azure/machine-learning/concept-ml-pipelines).

- Ezaugarri hau erabiltzeko Azure Studio Lake instantziarekin lotutako Azure Data Lake Gen2 biltegiratze kontua behar duzu. Informazio gehiago lortzeko, ikusi [Sortu Azure Data Lake Storage Gen2 biltegiratze kontua](/azure/storage/blobs/data-lake-storage-quickstart-create-account).

- Azure Ikaskuntza automatiko kanalizazioekin lan egiteko, Jabearen edo Erabiltzaile Sarbide Administratzailearen baimenak behar dituzu Azure Ikaskuntza automatiko Laneko espazioan.

   > [!NOTE]
   > Datuak zure Customer Insights instantzien eta laneko fluxuko hautatutako Azure web zerbitzu edo kanalizazioen artean transferitzen dira. Datuak Azure zerbitzu batera transmititzen dituzunean, ziurtatu zerbitzua datuak prozesatzeko konfiguratuta dagoen moduak eta kokalekuak betetzen dituela erakundeko datu horien eskakizun legal guztiak.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWRElk]

## <a name="add-a-new-workflow"></a>Gehitu lan-fluxu bat

1. Joan **Adimena** > **Eredu pertsonalizatuak** eta hautatu **Lan-fluxu berria**.

1. Eman zure pertsonalizatutako eredua ezaguna den izena **Izena** eremuan.

   > [!div class="mx-imgBorder"]
   > ![Lan-fluxu berriaren panelaren pantaila.](media/new-workflowv2.png "Lan-fluxu berriaren panelaren pantaila")

1. Hautatu web zerbitzua biltzen duen erakundea **Zure web zerbitzua duen maizterrak**.

1. Azure Ikaskuntza automatiko harpidetza Customer Insights baino beste maizter bat baldin baduzu, hautatu **saioa hasi** hautatutako erakundearen zure egiaztagiriekin.

1. Aukeratu web zerbitzuarekin erlazionatutako **Laneko areak**. 

1. Aukeratu Azure Ikaskuntza automatiko kanalizazioa atalean **Zure eredua duen web zerbitzua** goitibeherako. Ondoren, hautatu **Hurrengoa**.    
   Lortu informazio gehiago [Azure Machine Learning-en bideratze bat diseinatzailea](/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-designer) edo [SDK](/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-python-sdk) erabiliz argitaratzeari buruz. Zure bideratzea [bideratzearen amaiera-puntuan](/azure/machine-learning/how-to-run-batch-predictions-designer#submit-a-pipeline-run) argitaratu behar da.

1. Bakoitzarentzako **Web zerbitzuaren sarrera** hautatu bat datozenak **Erakunde** aukeratu Customer Insights eta aukeratu **hurrengo**.
   > [!NOTE]
   > Eredu pertsonalizatuko lan-fluxuak heuristika aplikatuko du web zerbitzuko sarrerako eremuak entitatearen atributuei esleitzeko eremuaren izenean eta datu motan oinarrituta. Akats bat ikusiko duzu web zerbitzu eremua entitate batera esleitu ezin bada.

   > [!div class="mx-imgBorder"]
   > ![Konfiguratu lan-fluxu bat.](media/intelligence-screen2-updated.png "Konfiguratu lan-fluxu bat")

1. **Ereduaren irteerako parametroak** urratsean ezarri propietate hauek:
      1. Sartu bideratzearen irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.
      1. Aukeratu sortako bideratzearen **Irteerako datu-biltegi parametroaren izena** goitibeherako zerrendan.
      1. Aukeratu sortako bideratzearen **Irteerako bide-izenaren parametroaren izena** goitibeherako zerrendan.

      > [!div class="mx-imgBorder"]
      > ![Ereduaren irteerako parametroen panela.](media/intelligence-screen3-outputparameters.png "Ereduaren irteerako parametroen panela")

1. Hautatu bat egiten duen atributua **Customer ID emaitzetan** goitibeherako zerrendan zeinak zure Customer Insights **Gorde** esleitzen duen.

   > [!div class="mx-imgBorder"]
   > ![Erlazionatu emaitzak bezeroaren datuen panelarekin.](media/intelligence-screen4-relatetocustomer.png "Erlazionatu emaitzak bezeroaren datuen panelarekin")

1. Ikusiko duzu **Lan-fluxua gordeta** pantaila lan-fluxuei buruzko xehetasunak.    
   Azure Ikaskuntza automatiko kanalizazio baterako lan-fluxu bat konfiguratu baduzu, Customer Insights kanalizazioa duen lan-eremuari atxikitzen zaio. Customer Insights-ek a **Laguntzailea** rola Azure lan-eremuan.

1. Hautatu **Eginda**.

1. Orain laneko fluxua exekutatu dezakezu **Eredu pertsonalizatuak** orritik.

## <a name="edit-a-workflow"></a>Editatu lan-fluxua

1. Gainean **Eredu pertsonalizatuak** orrialdea, hautatu elipsi bertikala (&vellip;)-n **Ekintzak** zutabea aurrez sortu eta hautatu duzun lan-fluxu baten ondoan **Editatu**.

1. Laneko fluxuaren izen ezaguna eguneratu dezakezu **Bistaratzeko izena** eremuan, baina ezin duzu konfiguratutako web zerbitzu edo bideratzea aldatu. Hautatu **Hurrengoa**.

1. Bakoitzarentzako **Web zerbitzuaren sarrera**, bat datozenak egunera ditzakezu **Entitatea** Customer Insights-etik. Ondoren, hautatu **Hurrengoa**.

1. **Ereduaren irteerako parametroak** urratsean ezarri propietate hauek:
      1. Sartu bideratzearen irteerako emaitzak sartu nahi dituzun irteerako **Entitatearen izena**.
      1. Aukeratu **irteerako datu-biltegi parametroaren izena** zure probako bideratzerako.
      1. Aukeratu **irteerako bide-izenaren parametroaren izena** zure probako bideratzerako.

1. Hautatu bat egiten duen atributua **Customer ID emaitzetan** goitibeherako zerrendan zeinak zure Customer Insights **Gorde** esleitzen duen.
   Inferentziako irteeratik atributu bat aukeratu bezeroaren entitatearen Bezeroaren ID zutabearen antzeko balioekin. Zure datu multzoan horrelako zutaberik ez baduzu, aukeratu errenkada modu esklusiboan identifikatzen duen atributu bat.

## <a name="run-a-workflow"></a>Lan-fluxuak exekutau

1. Gainean **Eredu pertsonalizatuak** orrialdea, hautatu elipsi bertikala (&vellip;)-n **Ekintzak** zutabea aurrez sortu duzun lan-fluxu baten ondoan.

1. Hautatu **Exekutatu**.

Zure lan-fluxua automatikoki exekutatzen da programatutako freskagarri bakoitzarekin. Argibide gehiago [programatutako freskagarriak konfiguratuz](schedule-refresh.md).

## <a name="delete-a-workflow"></a>Ezabatu lan-fluxua

1. Gainean **Eredu pertsonalizatuak** orrialdea, hautatu elipsi bertikala (&vellip;)-n **Ekintzak** zutabea aurrez sortu duzun lan-fluxu baten ondoan.

1. Hautatu **Ezabatu** eta berretsi ezabatzea.

Zure lan-fluxua ezabatu egingo da. [Entitatea](entities.md) lan-fluxua sortu zuenean sortu zen mantendu egingo da eta ikusi egin daiteke **Entitateak** orrian.

## <a name="results"></a>Emaitzak

Lan-fluxu baten emaitzak Model Output Parameter fasean konfiguratutako entitatean gordetzen dira. Datu hauek atzitu ditzakezu [entitateen orria](entities.md) edo batera [API sarbidea](apis.md).

### <a name="api-access"></a>API Sarbidea

OData kontsulta zehatzak eredu pertsonalizatuko entitate batetik datuak lortzeko, erabili formatu hau:

`https://api.ci.ai.dynamics.com/v1/instances/<your instance id>/data/<custom model output entity name>%3Ffilter%3DCustomerId%20eq%20'<guid value>'`

1. Ordezkatu `<your instance id>` Customer Insights ingurunearen IDarekin, zure nabigatzailearen helbide barran Customer Insights atzitzerakoan aurkituko duzu.

1. Ordezkatu `<custom model output entity>` modeloaren konfigurazio pertsonalizatuko Model Output Parameters urratsean emandako entitatearen izenarekin.

1. Ordezkatu `<guid value>` erregistroan sartu nahi duzun bezeroaren bezeroaren IDarekin. Identifikazio hau normalean aurkitu dezakezu [bezeroen profilen orria](customer-profiles.md) CustomerID eremuan.

## <a name="frequently-asked-questions"></a>Ohiko galderak

- Zergatik ezin dut nire kanalizazioa ikusi eredu pertsonalizatuko lan-fluxua konfiguratzean?    
  Arazo hau kanalizazioko konfigurazio arazo batek eragin ohi du. Ziurtatu [sarrera parametroa konfiguratuta dago](azure-machine-learning-experiments.md#dataset-configuration), eta [irteera datu biltegia eta bide parametroak](azure-machine-learning-experiments.md#import-pipeline-data-into-customer-insights) konfiguratuta daude ere.

- Zer esan nahi du "Ezin izan da gorde adimenaren fluxua" erroreak?    
  Erabiltzaileek normalean errore-mezu hau ikusten dute laneko eremuan Jabea edo Erabiltzaile Sarbide Administratzailea pribilegiorik ez badute. Erabiltzaileak baimen maila handiagoa behar du Customer Insights-ek lan-fluxua zerbitzu gisa prozesatu ahal izateko, erabiltzaile-kredentzialak lan-fluxuaren ondorengo exekuzioetarako erabili beharrean.

[!INCLUDE [footer-include](includes/footer-banner.md)]
