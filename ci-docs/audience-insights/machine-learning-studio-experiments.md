---
title: Machine Learning Studio (klasikoa) zerbitzuaren esperimentuak
description: 'Erabili Machine Learning Studio (klasikoa) zerbitzuko ereduak hemen: Dynamics 365 Customer Insights.'
ms.date: 12/03/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: ameetj
manager: shellyha
ms.openlocfilehash: 556b6810db0ed2733a3f086291757bd85b77e371
ms.sourcegitcommit: a9b2cf598f256d07a48bba8617347ee90024a1dd
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/03/2020
ms.locfileid: "4669003"
---
# <a name="use-models-based-on-azure-machine-learning-studio-classic"></a>Erabili Azure Machine Learning Studio (klasikoa) zerbitzuan oinarritutako ereduak

Dynamics 365 Customer Insights-eko datu bateratuak negozioaren ikuspegi osagarriak sor ditzaketen ikaskuntza automatiko ereduak eraikitzeko iturria da. Customer Insights Machine Learning Studio-rekin (klasikoa) integratzen da zure eredu pertsonalizatuak erabiltzeko. Azure Machine Learning-en garatutako ereduak Customer Insights-ekin nola integratzen diren ikusteko, ikusi [Azure Machine Learning-eko esperimentuak](azure-machine-learning-experiments.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Sartu Customer Insights-era
- Aktibatu Azure Enterprise harpidetza
- [Bezeroen profil bateratuak](data-unification.md)
- [Erakundeak Azure Blob biltegira esportatzea](export-azure-blob-storage.md) konfiguratu

## <a name="set-up-machine-learning-studio-classic"></a>Konfiguratu Machine Learning Studio (klasikoa)

Lehen urrats batean, Machine Learning Studio-ko (klasikoa) laneko area sortu behar dugu eta zerbitzua ireki.

1. Joan[https://www.portal.azure.com](https://www.portal.azure.com/) eta hasi saioa.

1. Hautatu **Sortu baliabidea**.

1. Bilatu **Ikaskuntza automatiko Studio lan-eremua** eta hautatu **Sortu**.

1. Idatzi beharrezko xehetasunak honetara [sortu lan-eremua](https://docs.microsoft.com/azure/machine-learning/studio/create-workspace). Aukeratu **Web zerbitzuen planaren prezioen maila** inportatzeko asmoa duzun datu kopuruaren arabera. Errendimendu onena lortzeko, hautatu geografikoki hurbilen dagoen **kokalekua**.

1. Baliabidea sortu ondoren, Ikaskuntza automatiko Studio laneko espazioen panela agertuko da. Aukeratu **Ikaskuntza automatiko Studio abiarazi**.

   ![Azure Ikaskuntza automatiko Studio erabiltzailearen interfazea](media/azure-machine-learning-studio.png)

## <a name="work-with-azure-machine-learning-studio"></a>Lan egin Azure Machine Learning Studio

Esperimentu berri bat sor dezakezu edo lehendik dagoen esperimentu txantiloia inportatu lagin galeriatik. Hiru agertoki estandarretarako lagin esperimentuak daude:

- [Churn iragarpen](#churn-analysis)

- [Bezeroaren balio osoa](#customer-lifetime-value-prediction)

- [Produktuaren gomendioa edo hurrengo ekintza onena](#productrecommendation-or-next-best-action)

1. Esperimentu berria sortu edo esperimentuen txantiloia erabiltzen baduzu galeriatik, konfiguratu behar duzu **Inportatu datuak** propietate. Erabili esperientzia gidatua edo eman zuzenean xehetasunak zure datuak dituen Azure blob biltegira sartzeko.  

   ![Azure Machine Learning Studio esperimentua](media/azure-machine-learning-studio-experiment.png)

1. Orain, prozesatzeko neurrira egindako hoditeria eraiki dezakezu datuak garbitu eta aurreprozesatzeko, funtzioak ateratzeko eta eredu egokia prestatzeko.

1. Modeloaren errendimendua probatu eta optimizatu.

1. Eredu baten kalitatearekin konforme zaudenean, hautatu **Ezarri web zerbitzua** > **Aurreikusitako web zerbitzua**. Aukera honek prestatutako esperientziatik prestatutako eredua eta featutazio-hodiak inportatzen ditu iragarpen zerbitzu batera. Iragarpen zerbitzuak beste datu multzo bat har dezake prestakuntza esperimentuan erabilitako eskemarekin, iragarpenak egiteko.

   ![Ezarri web zerbitzu iragargarria](media/predictive-webservice-control.png)

1. Aurreikusitako web zerbitzuen esperimentua arrakastatsua izan ondoren, auto planifikaziorako erabil dezakezu. Web zerbitzua Customer Insights zerbitzuarekin lan egiteko, hautatu **Ezarri web zerbitzua** > **Ezarri Web Zerbitzua [Berria] Aurrebista**. [Ikasi gehiago web-zerbitzu bat inplementatzearen inguruan](https://docs.microsoft.com/azure/machine-learning/studio/deploy-a-machine-learning-web-service).

   ![Inplementatu web zerbitzu iragargarria](media/predictive-webservice-deploy.png)

## <a name="sample-models-from-the-gallery"></a>Galeriako eredu ereduak

Artikulu honetako modeloetarako Contoso Hotelaren fikziozko eszenatokia erabiliko dugu. Contoso Hotelak datu hauek biltzen ditu:

- Hotel-egonaldiaren jardueraz osatutako CRM datuak. Datu multzoak erregistratutako bezero bakoitzeko egonaldien daten inguruko informazioa biltzen du. Erreserba, gela motak, gastuaren xehetasunak eta abar buruzko informazioa ere ematen ditu. Datuek lau urte irauten dute, 2014ko urtarriletik 2018ko urtarrila.
- Hoteleko bezeroen bezeroen profilak. Profil hauek bezero bakoitzari buruzko informazioa biltzen dute, horien izena, jaioteguna, posta helbidea, generoa eta telefono zenbakia.
- Hotelak eskaintzen dituen zerbitzuen erabilera, esaterako, bainuetxea, garbitegia, WiFi edo mezularitza. Informazio hau erregistratutako bezero bakoitzerako erregistratzen da. Normalean, zerbitzuen erabilera egonaldiarekin lotuta dago. Zenbait kasutan, bezeroek hotelean egon gabe erabil ditzakete zerbitzuak.

## <a name="churn-analysis"></a>Churn azterketa

Churn analisia negozio arlo desberdinetan aplikatzen da. Adibide honetan, zerbitzuen galera-tasa aztertuko dugu, batez ere hotelen zerbitzuen testuinguruan, lehen azaldu bezala. Bukaerako muturreko bideratze eredu baten lanaren adibidea eskaintzen du. Beste edozein ereduaren bideratzea edozein galera-tasaren ereduren abiapuntu gisa erabil daiteke.

### <a name="definition-of-churn"></a>Churn definizioa

Churn definizioa eszenatokiaren arabera alda daiteke. Adibide honetan, azken urtean hotela bisitatu ez duen gonbidatu bat galdutzat etiketatuta egon beharko litzateke.  

Esperimentuaren txantiloia galeriatik inportatu daiteke. Lehenik eta behin, ziurtatu datuak inportatzen dituzula **Hotel Ostatu Jarduera**, **Bezeroaren datuak**, eta **Zerbitzuaren erabilera datuak** Azure Blob biltegitik.

   ![Inportatu datuak Churn ereduari dagokionez](media/import-data-azure-blob-storage.png)

### <a name="featurization"></a>Eginbideak egin

Galera-tasaren definizioa oinarritzat hartuta, etiketan eragina izango duten ezaugarri gordinak identifikatzen ditugu lehenik. Ondoren, ezaugarri gordin hauek Ikaskuntza automatiko ereduekin erabil daitezkeen zenbakizko funtzioetan prozesatzen ditugu. Datuen integrazioa Customer Insights-en gertatzen da, beraz, taula hauek konbina ditzakegu *Bezeroaren IDa* erabiliz.

   ![Sartu inportatutako datuak](media/join-imported-data.png)

Galera-tasaren analisia egiteko ereduaren sorrera zaila izan daiteke. Datuak denboraren funtzio bat dira egunero egiten diren hotel jarduera berriekin. Featizazio garaian, datu dinamikotik ezaugarri estatikoak sortu nahi ditugu. Kasu honetan, hoteleko jardueratik ezaugarri ugari sortzen ditugu urtebeteko leiho labainkorrekin. Gela mota edo erreserba mota bezalako ezaugarri kategoriak ere bereizten ditugu, kodetze beroa erabiliz.  

Ezaugarrien behin betiko zerrenda:

| **Zenbakia**  | **jatorrizko_zutabea**          | **Eratorritako Ezaugarriak**                                                                                                                      |
|-------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| 1           | Gela mota                    | RoomTypeLargeCount, RoomTypeSmallCount                                                                                                    |
| 2           | Erreserba mota                 | BookingTypeOnlineCount, BookingTypePhoneCallCount                                                                                         |
| 3           | Bidaia Kategoria              | TravelCategoryBusinessCount, TravelCategoryLeisureCount                                                                                   |
| 4           | Dolarrak gastatu                | TotalDollarSpent                                                                                                                          |
| 5           | Sarrera eta Ordainketen datak  | StayDayCount, StayDayCount2016, StayDayCount2015, StayDayCount2014, StayCount, StayCount2016. StayCount2015, StayCount2014                |
| 6           | Zerbitzuaren erabilpena                | UsageTenure, ConciergeUsage, CourierUsage, DryCleaningUsage, GymUsage, PhoneUsage, RestaurantUsage, SpaUsage, TelevisionUsage, WifiUsage  |

### <a name="model-selection"></a>Ereduen hautapena

Orain erabili beharreko algoritmo egokiena aukeratu behar dugu. Kasu honetan, ezaugarri gehienak ezaugarri kategorietan oinarritzen dira. Normalean, erabaki zuhaitzetan oinarritutako ereduak ondo funtzionatzen dute. Zenbakizko ezaugarriak soilik badaude, sare neuronalak aukera hobea izan liteke. Laguntza bektore makina (SVM) ere hautagai ona da horrelako egoeretan; hala ere, sintonia pixka bat behar du errendimendu onena ateratzeko. Aukeratzen dugu **Bi klasez bultzatutako erabaki zuhaitza** lehen eredu gisa eta ondoren **Bi klaseko SVM** bigarren eredu gisa. Azure Machine Learning Studio-k A / B probak egiteko aukera ematen dizu, beraz, onuragarria da bi ereduekin hastea.

Hurrengo irudian Azure Ikaskuntza automatiko Studio-ren ereduaren prestakuntza eta ebaluazio hoditeria erakusten dira:

![Churn eredua Azure Machine Learning Studio-n](media/azure-machine-learning-model.png)

**Permutazioaren ezaugarrien garrantzia** izeneko teknika ere aplikatzen dugu, ereduen optimizazioaren alderdi garrantzitsua. Eraikitako modeloek ez dute ezer zehatzik inolako ezaugarri zehatzek azken iragarpen-en duten eraginaren inguruan. Funtzioen garrantziaren kalkulagailuak algoritmo pertsonalizatua erabiltzen du eredu zehatz baten emaitzetan banakako ezaugarrien eragina kalkulatzeko. Funtzioen garrantzia +1 eta -1 artean normalizatzen da. Eragin negatiboarekin, kasuan kasuko funtzioak emaitzaren gaineko eragin intuitiboa du eta eredutik kendu beharko litzateke. Eragin positiboak adierazten du funtzioak asko laguntzen duela iragarpen. Balio hauek ez dira korrelazio koefizienteak neurri desberdinak direlako. Informazio gehiago lortzeko, ikus [Permutazioaren ezaugarrien garrantzia](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/permutation-feature-importance).

[Galera-tasaren esperimentu osoa Azure AI galerian eskuragarri dago](https://gallery.azure.ai/Experiment/Hotel-Churn-Predictive-Exp).

## <a name="customer-lifetime-value-prediction"></a>Bezeroaren balio osoaren iragarpena

Bezeroen bizi-iraupenaren balioaren (CLTV) kalkulua negozio batek bezeroak ebaluatu eta segmentatzeko erabil dezakeen funtsezko neurrietako bat da. Ostalaritza negozioarentzat, kritikoa da haien bezeroak ezagutzea. Adibidez, bezero onak osatzen dituzten faktoreak ulertzea informazio garrantzitsua da. Hoteleko zuzendaritzak bezeroaren ordainketa altuak asetzeko eta zein hobekuntza bideratu behar dituzten baloratzen laguntzen du. Erabaki horiek eragin zuzena izan dezakete salmentetan eta irabazietan.  

### <a name="definition-of-cltv"></a>CLTV-ren definizioa

Adibide gisa, bezero baten CLTVa definitzen dugu bezeroak hurrengo 365 egunetan gastatuko duen zenbatekoarekin. Azken hiru urteetako datuak erabiliko ditugu bezero guztiek balio hori aurreikusteko.

### <a name="featurization"></a>Eginbideak egin

Kasu honetan, featización ez da nahiko egoeraren antzekoa izango. Hala ere, etiketak eta aurreikusitako balioak goian zehaztutakoa baino ez dira.

### <a name="model-selection"></a>Ereduen hautapena

CLTV aurreikustea erregresio arazoa da, aurreikusitako balioa etengabeko balio aldagai positiboa baita. Ezaugarrien propietateak kontuan hartuta, hautatzen dugu **erabakiaren zuhaitzaren erregresioa areagotu zuen** algoritmo gisa eta **sare neutralen erregresioa** eredua entrenatzeko beste algoritmo gisa.

## <a name="product-recommendation-or-next-best-action"></a>Produktuaren gomendioa edo hurrengo ekintza onena

Hotelaren agertoki batean produktuaren gomendioa hotelak bezeroei eskaintzen dizkien zerbitzuak gomendatzera interpretatzen da. Helburua bezeroei zerbitzu egokiak aukeratzea da, haien erabilera ahalik eta gehien aprobetxatzeko. Bideo bidezko streaming zerbitzua duten erabiltzaileentzako gomendioen antzekoa da.

### <a name="definition-of-product-recommendation-or-next-best-action"></a>Produktu-gomendioa edo hurrengo ekintza onenaren definizioa

Helburua zerbitzuaren erabileraren dolarraren zenbatekoa maximizatzea bezala definitzen dugu, hoteleko bezeroei zerbitzu egokienak eskainiz beren interesaren arabera.

### <a name="featurization"></a>Eginbideak egitea

Galera-tasaren eredua bezala, hoteleko zerbitzuaren bezeroaren IDa bezeroaren IDarekin batzen ari gara bezeroaren ID bakoitzeko etengabe gomendioak eraikitzeko.

![Gomendio ereduaren ezaugarri](media/azure-machine-learning-model-featurization.png)

Datuak hiru entitate desberdinetatik jasotzen dira eta ezaugarri horietatik eratorritakoak dira. Gomendioaren arazoaren ezaugarri nagusia ezberdina da Churn edo CLTV eszenatokiekin alderatuta. Gomendio ereduak sarrera datuak behar ditu hiru funtzio multzoren moduan.

### <a name="model-selection"></a>Ereduen hautapena

Produktuak edo zerbitzuak iragartzen ditugu **Train Matchbox Recommender** algoritmoa erabili eta eredua trebatzeko.

![Produktuen gomendioa algoritmoa](media/azure-machine-learning-model-recommendation-algorithm.png)

**Train Matchbox Recommender** ereduak prestakuntza zerbitzuaren erabilera datuetan, bezeroaren deskribapenean (aukerakoa) eta zerbitzuaren deskribapenean hartzen dituen hiru sarrerako portuak. Eredua puntuatzeko hiru modu desberdin daude. Bata eredua ebaluaziorako da, non normalizatutako zenbateko irabazia metatutako puntuazioa (NDCG) puntuazioa kalkulatzen den puntuatutako elementuak sailkatzeko. Esperimentu honetan, NDCG puntuazioa 0.97 da. Beste bi aukerak eredua puntuatzea da zerbitzuen katalogo gomendagarrian, edo erabiltzaileek aurretik erabili ez dituzten elementuetan soilik puntuatzea.

Zerbitzuen katalogo osorako gomendioen banaketari buruz gehiago begiratuz, telefonoa, WiFi-a eta mezularitza-zerbitzua gomendagarriak diren zerbitzu nagusiak direla ohartzen gara. Hau bat dator zerbitzuaren kontsumoaren datuen banaketetatik topatu duguna:

![Gomendio-ereduaren irteerakoa](media/azure-machine-learning-model-output.png)

[Produktuaren gomendio-esperimentua osoa Azure AI galerian atzi daiteke.](https://gallery.azure.ai/Experiment/Recommendation-4)

## <a name="integrate-custom-models"></a>Integratu pertsonalizatutako ereduak

Aurreikuspen hauek Customer Insights-en erabiltzeko, beharrezkoa da iragarpenak **esportatzea** bezeroaren IDekin batera. [Esportatu Azure Blob biltegiratze kokapenera](https://docs.microsoft.com/azure/storage/common/storage-import-export-data-from-blobs), iturburuko datuak esportatzen dituzun leku berera. Aurreikusitako web zerbitzua aldizka exekutatu daiteke eta puntuazioak eguneratzeko.

Eredu pertsonalizatuak sortutako datuak zure bezeroen datuak gehiago aberasteko erabil daitezke. Informazio gehiago lortzeko, ikus [Ikaskuntza automatiko eredu pertsonalizatuak](custom-models.md).
