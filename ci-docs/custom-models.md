---
title: Ikaskuntza automatiko eredu pertsonalizatuak | Microsoft Docs
description: Azure Ikaskuntza automatiko-en eredu pertsonalizatuekin lan egin Dynamics 365 Customer Insights.
ms.date: 09/19/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: tutorial
author: zacookmsft
ms.author: zacook
manager: shellyha
searchScope:
- ci-custom-models
- customerInsights
ms.openlocfilehash: 89553b511d249fd586e36a1c4944a977513b0643
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9609723"
---
# <a name="custom-machine-learning-models"></a>Ikaskuntza automatiko eredu pertsonalizatuak

> [!NOTE]
> Ikaskuntza automatiko Studiorako (klasikoa) laguntza 2024ko abuztuaren 31n amaituko da. Hona trantsizioa egitea gomendatzen dizugu [Azure Ikaskuntza automatiko](/azure/machine-learning/overview-what-is-azure-machine-learning) data horretarako.
>
> 2021eko abenduaren 1etik aurrera, ezin izango dituzu sortu Ikaskuntza automatiko Studio (klasikoak) baliabide berriak. 2024ko abuztuaren 31ra arte, dauden Ikaskuntza automatiko Studio (klasikoak) baliabideak erabiltzen jarraitu dezakezu. Informazio gehiagorako, ikus [Migratu Azurera Ikaskuntza automatiko](/azure/machine-learning/migrate-overview).

Modelo pertsonalizatuak Azure Ikaskuntza automatiko ereduetan oinarritutako lan-fluxuak kudeatzeko aukera ematen dizu. Lan-fluxuek xehetasunak sortu nahi dituzun datuak aukeratzen eta emaitzak bezeroaren datu bateratuekin esleitzen laguntzen zaituzte. Ikaskuntza automatikoko eredu pertsonalizatuak eraikitzeari buruzko informazio gehiago lortzeko, ikusi [Erabili Azure Machine Learning-en oinarritutako ereduak](azure-machine-learning-experiments.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Bidez argitaratutako web zerbitzuak [Azure Ikaskuntza automatiko loteen kanalizazioak](/azure/machine-learning/concept-ml-pipelines).
- Pipeline a azpian argitaratu behar da [kanalizazio amaierako puntua](/azure/machine-learning/how-to-run-batch-predictions-designer#submit-a-pipeline-run).
- An [Azure Data Lake Gen2 biltegiratze-kontua](/azure/storage/blobs/data-lake-storage-quickstart-create-account) zure Azure Studio instantziari lotuta.
- Azure Ikaskuntza automatiko lan-esparruetarako kanalizazioekin, Jabearen edo Erabiltzaileen sarbidearen administratzaileen baimenak Azure Ikaskuntza automatiko lan-eremurako.

  > [!NOTE]
  > Datuak zure Customer Insights instantzien eta laneko fluxuko hautatutako Azure web zerbitzu edo kanalizazioen artean transferitzen dira. Datuak Azure zerbitzu batera transmititzen dituzunean, ziurtatu zerbitzua datuak prozesatzeko konfiguratuta dagoen moduak eta kokalekuak betetzen dituela erakundeko datu horien eskakizun legal guztiak.

## <a name="add-a-new-workflow"></a>Gehitu lan-fluxu bat

1. Joan **Adimena** > **Eredu pertsonalizatuak** eta hautatu **Lan-fluxu berria**.

1. Eman antzemangarri bat **Izena**.

   :::image type="content" source="media/new-workflowv2.png" alt-text="Lan-fluxu berriaren panelaren pantaila.":::

1. Hautatu web zerbitzua biltzen duen erakundea **Zure web zerbitzua duen maizterrak**.

1. Azure Ikaskuntza automatiko harpidetza Customer Insights baino beste maizter bat baldin baduzu, hautatu **saioa hasi** hautatutako erakundearen zure egiaztagiriekin.

1. Aukeratu web zerbitzuarekin erlazionatutako **Laneko areak**.

1. Aukeratu Azure Ikaskuntza automatiko kanalizazioa atalean **Zure eredua duen web zerbitzua** goitibeherako. Ondoren, hautatu **Hurrengoa**.
   Lortu informazio gehiago [Azure Machine Learning-en bideratze bat diseinatzailea](/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-designer) edo [SDK](/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-python-sdk) erabiliz argitaratzeari buruz.

1. **Web zerbitzuaren sarrera** bakoitzeko, hautatu bat egiten duen **Entitatea** Customer Insights-en. Ondoren, hautatu **Hurrengoa**.
   > [!NOTE]
   > Eredu pertsonalizatuko lan-fluxuak heuristika aplikatuko du web zerbitzuko sarrerako eremuak entitatearen atributuei esleitzeko eremuaren izenean eta datu motan oinarrituta. Akats bat ikusiko duzu web zerbitzu eremua entitate batera esleitu ezin bada.

   :::image type="content" source="media/intelligence-screen2-updated.png" alt-text="Konfiguratu lan-fluxu bat.":::

1. Izan ere **Ereduaren irteera-parametroak**, ezarri propietate hauek:
   - **Entitatearen izena** kanalizazioko irteerako emaitzetarako
   - **Irteera datu-biltegi parametroaren izena** zure loteen kanalizazioa
   - **Irteerako bidea parametroaren izena** zure loteen kanalizazioa

   :::image type="content" source="media/intelligence-screen3-outputparameters.png" alt-text="Ereduaren irteerako parametroen panela.":::

1. Hautatu bat datorren atributua **Bezeroaren IDa emaitzetan** bezeroak identifikatzen eta hautatzen dituena **Gorde**.

   :::image type="content" source="media/intelligence-screen4-relatetocustomer.png" alt-text="Erlazionatu emaitzak bezeroaren datuen panelarekin.":::

   The **Lan-fluxua gordeta** pantailak lan-fluxuari buruzko xehetasunak erakusten ditu. Azure Ikaskuntza automatiko kanalizazio baterako lan-fluxu bat konfiguratu baduzu, Customer Insights kanalizazioa duen lan-eremuari atxikitzen zaio. Customer Insights-ek a **Laguntzailea** rola Azure lan-eremuan.

1. Hautatu **Eginda**. The **Eredu pertsonalizatuak** orrialdeak bistaratzen ditu.

1. Hautatu elipsi bertikala (&vellip;) lan-fluxurako eta hautatu **Korrika egin**. Zure lan-fluxua automatikoki exekutatzen da guztietan [programatutako freskagarritasuna](schedule-refresh.md).

## <a name="manage-an-existing-workflow"></a>Kudeatu lehendik dagoen lan-fluxu bat

Joan **Adimena** > **Eredu pertsonalizatuak** sortu dituzun lan-fluxuak ikusteko.

Hautatu lan-fluxu bat erabilgarri dauden ekintzak ikusteko.

- **Editatu** lan-fluxu bat
- **Korrika egin** lan-fluxu bat
- [**Ezabatu**](#delete-a-workflow) lan-fluxu bat

### <a name="edit-a-workflow"></a>Editatu lan-fluxua

1. Joan **Adimena** > **Eredu pertsonalizatuak**.

1. Eguneratu nahi duzun lan-fluxuaren ondoan, hautatu elipsi bertikala (&vellip;) eta hautatu **Editatu**.

1. Aldatu **Bistaratzeko izena** behar izanez gero, eta hautatu **Hurrengoa**.

1. Bakoitzarentzako **Web zerbitzuaren sarrera**, eguneratu bat datozenak **Entitatea** Customer Insights-etik, behar izanez gero. Ondoren, hautatu **Hurrengoa**.

1. Izan ere **Ereduaren irteera-parametroak**, aldatu hauetako bat:
   - **Entitatearen izena** kanalizazioko irteerako emaitzetarako
   - **Irteera datu-biltegi parametroaren izena** zure loteen kanalizazioa
   - **Irteerako bidea parametroaren izena** zure loteen kanalizazioa

1. Aldatu bat datorren atributua honetatik **Bezeroaren IDa emaitzetan** bezeroak identifikatzeko. Inferentziako irteeratik atributu bat aukeratu bezeroaren entitatearen Bezeroaren ID zutabearen antzeko balioekin. Zure datu multzoan halako zutaberik ez baduzu, aukeratu errenkada esklusiboki identifikatzen duen atributu bat.

1. Sakatu **Gorde**

### <a name="delete-a-workflow"></a>Ezabatu lan-fluxua

1. Joan **Adimena** > **Eredu pertsonalizatuak**.

1. Ezabatu nahi duzun lan-fluxuaren ondoan, hautatu elipsi bertikala (&vellip;) eta hautatu **Ezabatu**.

1. Berretsi ezabatu nahi duzula.

Zure lan-fluxua ezabatu egingo da. The [entitate](entities.md) sortu zenean lan-fluxua bere horretan jarraitzen du, eta hemendik ikus daiteke **Datuak** > **Entitateak** orrialdea.

## <a name="view-the-results"></a>Ikusi emaitzak

Lan-fluxu baten emaitzak definitutako entitatearen izenean gordetzen dira **Ereduaren irteera-parametroak**. Atzitu datu hauetatik [**Datuak** > **Entitateak** orrialdea](entities.md) edo rekin [API sarbidea](apis.md).

### <a name="api-access"></a>API Sarbidea

OData kontsulta zehatzak eredu pertsonalizatuko entitate batetik datuak lortzeko, erabili formatu hau:

`https://api.ci.ai.dynamics.com/v1/instances/<your instance id>/data/<custom model output entity name>%3Ffilter%3DCustomerId%20eq%20'<guid value>'`

1. Ordezkatu`<your instance id>` Customer Insights ingurunearen IDarekin, zure arakatzailearen helbide-barran agertzen dena Customer Insights-era sartzean.

1. Ordezkatu`<custom model output entity>` horretarako emandako entitate izenarekin **Ereduaren irteera-parametroak**.

1. Ordezkatu`<guid value>` sartu nahi duzun bezeroaren IDarekin. ID hau bistaratzen da [bezeroen profilen orria](customer-profiles.md) CustomerID eremuan.

## <a name="frequently-asked-questions"></a>Maiz egiten diren galderak

- Zergatik ezin dut nire kanalizazioa ikusi eredu pertsonalizatuko lan-fluxua konfiguratzean?
  Arazo hau kanalizazioko konfigurazio arazo batek eragin ohi du. Ziurtatu [sarrera parametroa konfiguratuta dago](azure-machine-learning-experiments.md#dataset-configuration), eta [irteera datu biltegia eta bide parametroak](azure-machine-learning-experiments.md#import-pipeline-data-into-customer-insights) konfiguratuta daude ere.

- Zer esan nahi du "Ezin izan da gorde adimenaren fluxua" erroreak? 
  Erabiltzaileek normalean errore-mezu hau ikusten dute laneko eremuan Jabea edo Erabiltzaile Sarbide Administratzailea pribilegiorik ez badute. Erabiltzaileak baimen maila handiagoa behar du Customer Insights-ek lan-fluxua zerbitzu gisa prozesatu ahal izateko, erabiltzaile-kredentzialak lan-fluxuaren ondorengo exekuzioetarako erabili beharrean.

- Nire eredu pertsonalizatuaren lan-fluxurako amaiera-puntu / esteka pribatu bat onartzen al da?
  Customer Insights-ek oraingoz ez du onartzen eredu pertsonalizatuetarako amaiera-puntu pribatua, baina eskuzko konponbidea eskuragarri dago. Mesedez, jarri harremanetan laguntzarekin xehetasunak lortzeko.

## <a name="responsible-ai"></a>AA arduratsua

Iragarpenek bezeroen esperientzia hobeak sortzeko, negozio gaitasunak eta diru sarrera korronteak hobetzeko gaitasunak eskaintzen dituzte. Zure iragarpenaren balioa orekatzea gomendatzen dizugu, duen eraginaren eta modu etikoan sar daitezkeen alborapenen artean. Lortu informazio gehiago Microsoft-ek [AA arduratsua](https://www.microsoft.com/ai/responsible-ai?activetab=pivot1%3aprimaryr6) jorratzeko moduari buruz. Azure Machine Learning-en [Ikaskuntza automatiko modu arduratsuan erabiltzeko teknika eta prozesu](/azure/machine-learning/concept-responsible-ml) jakinei buruz ikas dezakezu.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWRElk]

[!INCLUDE [footer-include](includes/footer-banner.md)]
