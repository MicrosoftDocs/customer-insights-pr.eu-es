---
title: Bezeroen iritzietarako analisi semantikoa
description: Ikasi bezeroen iritziei buruzko sentimenduen analisiaren eredua nola erabiltzen Dynamics 365 Customer Insights.
ms.date: 12/23/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: wmelewong
ms.author: wameng
manager: shellyha
ms.openlocfilehash: 05e530a1bc96c5fd9c7a3bc0197563d8fe330387
ms.sourcegitcommit: cb71e39de9b891c24bd5cd9c014eb3eeb537ac24
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 01/10/2022
ms.locfileid: "7951102"
---
# <a name="analyze-sentiment-in-customer-feedback-preview"></a>Aztertu sentimendua bezeroen iritzietan (Aurrebista)

Bezeroek kalitate handiko produktuak, zerbitzuak eta esperientziak espero dituzte egun. Batez ere iritzia partekatzen duten bezeroak. Erakundeentzat oso zaila da gero eta datu-bolumena aztertzea zehaztasuna eta lan-kostu handiagoak murriztu gabe. Dynamics 365 Customer Insights sentimenduen analisi-eredu bat eskaintzen du bezeroen iritzietarako, erakundeei beren datuak zehatzago eta kostu txikiagoan aztertzeko aukera ematen diena.

Sentimenduen analisiak bezeroen sentimendua sintetizatu eta negozio-alderdiak hobetzeko aukera gisa identifikatzea ahalbidetzen dizu. Customer Insights eginbide honek ondo zer funtzionatzen duen eta zer zuzendu behar duzun ulertzen laguntzen dizu. Zentratu negozioaren arlo garrantzitsu eta eragingarrienetan zure bezeroen esperientzia hobetzeko. Azken finean, bezeroen gogobetetze eta leialtasun handia eragiten duten esperientziak ahalbidetzen dituzten negozio-ekintzak gidatzen lagun zaitzake.

## <a name="overview"></a>Informazio orokorra

Sentimenduak aztertzeko eginbideak bezero ID bakoitzeko bi informazio eratorri sortzen ditu. Sentimendu puntuazioa (-5etik 5era) eta negozio-alderdi aplikagarrien zerrenda (negozio-arloak) batera bezeroen iritzia hobeto ulertzen lagunduko dizu. 

Informazio honek emaitza hauek lortzen lagun zaitzake: 
- Lortu bezeroen sentimenduen ikuspegi orokorra marka edo erakunde baten aurrean
- Identifikatu sentimendu negatiboa duten bezeroak zure kanpainak eta konpromisoak bideratzeko eta etekin handiagoa lortzeko optimizatzeko  
- Bezeroek adierazitako arazoekin negozio-alderdiak identifikatzea  
- Segmentatu bezeroak beren sentimenduaren arabera kanpaina pertsonalizatuak egiteko salmenta, marketina eta laguntza esfortzuekin
- Optimizatu negozio-eragiketak bezeroek aipatu dituzten kezka edo aukerei zuzenduta
- Ongi dabiltzan negozio-alderdiak ezagutzea eta bezero pozik saritzea leialtasun eta sustapen programen bidez

Ereduen emaitzetan fida zaitezkeela ziurtatzeko, ereduek erabakiak nola hartzen dituztenei buruzko informazio gardena eskaintzen dugu. Iritzi-iruzkinei iritzi-puntuazio edo negozio-alderdi jakin bat esleitzeko ereduen erabakia eragin duten hitzen zerrenda jasoko duzu.  

Bi erabiltzen ditugu **Hizkuntza Naturalaren Prozesamenduaren (NLP) ereduak** : Lehenengoak iritzi-iruzkin bakoitzari sentimendu puntuazio bat esleitzen dio. Bigarren ereduak feedback bakoitza aplikagarriak diren negozio-alderdi guztiekin lotzen du. Ereduak sare sozialetako, txikizkako, jatetxeetako, kontsumo-produktuetako eta automobilgintzako industrietako iturrietako datu publikoetan trebatzen dira.    
  
- Ereduak feedback datuekin lotzeko aurrez definitutako negozio-alderdiak hauek dira:
-   Kontuen kudeaketa
-   Ordainketa eta ordainketa
-   Bezeroentzako laguntza-zerbitzua
-   Dendan jasotzeko
-   Ontziak bidaltzea eta berreskuratzea
-   Aurrez erreserbatzea
-   Prezioa
-   Pribatutasuna eta segurtasuna
-   Promozioak eta sariak
-   Ordainagiria eta bermea
-   Itzultzeko trukea eta baliogabetzea
-   Betetze-zehaztasuna
-   Webgune/aplikazioen kalitatea

> [!NOTE]
> Gaur egun, ingeleseko bezeroen iritzien inguruko sentimenduen analisia onartzen dugu. Etorkizunean hizkuntza gehiago onartuko dira. Beste hizkuntza batzuetako iritzia kargatzen bada, ereduak emaitzak emango ditu oraindik. Hala ere, emaitza hauek ez dira zehatzak izango. 

## <a name="prerequisites"></a>Aurrebaldintzak

Sentimenduen analisia testu-erantzunaren datuetan oinarritzen da [datuak bateratzeko prozesua](data-unification.md). Oso gomendatzen dizugu [konfiguratu zure iritzi-datuen entitateak mota semantikoko jarduera-entitate gisa](map-entities.md#select-primary-key-and-semantic-type-for-attributes) (Feedback mota) aurretik. 

Sentimenduen analisi-eredu bat konfiguratzeko, behar duzu gutxienez [Kolaboratzaileen baimenak](permissions.md).

Customer Insights-ek gehienez 10 milioi feedback-erregistro prozesatu ditzake eredu bakarrerako. Ereduak 128 hitz arteko iruzkinak azter ditzake. Iritzi-iruzkin bat luzeagoa bada, analisiak lehen 128 hitzak bakarrik hartzen ditu kontuan.

### <a name="data-requirements"></a>Datuen eskakizunak
  
Datu-atributu hauek behar dira:
- Bezeroaren ID bateratua (UCID) testu-erantzunaren datu-erregistroak bezero indibidual batekin lotzeko. ID hau ren emaitza da [datuak bateratzeko prozesua](data-unification.md).
- Oharren IDa
- Iritziaren denbora-zigilua
- Oharren testua   

> [!TIP]
> Sentimenduen analisiak zure bezeroen testuaren iritzia eskatzen du. Iritzi-entitate bakarra konfigura daiteke une honetan. Iritzi-entitate anitz badaude, horiek bateratu ditzakezu Power Query datuak sartzen hasi baino lehen.

## <a name="configure-a-sentiment-analysis"></a>Konfiguratu sentimenduen analisia 

1. Customer Insights atalean, joan **Inteligentzia** > **Iragarpenak**.

1. Gainean **Bezeroen sentimenduaren analisia** fitxa, hautatu **Erabili eredua**.

1. urtean **Bezeroen sentimenduen analisia (aurrebista)** panela, hautatu **Hasi**.

1. urtean **Ereduaren izena** urratsa, eman a **Izena** zure azterketarako. 

1. Eman **Negozio-alderdiaren irteera-entitatearen izena** eta **Sentimendu puntuazioa irteerako entitatearen izena**, gero hautatu **Hurrengoa**.

1. urtean **Beharrezko datuak** urratsa, hautatu **Gehitu datuak**.

   :::image type="content" source="media/sentiment-add-data.png" alt-text="Gehitu datu-fluxua sentimenduen analisiaren ereduan.":::

1. urtean **Gehitu datuak** panela, aukeratu mota semantikoa **Iritzia** zerrendatik.

   :::image type="content" source="media/sentiment-add-feedback-activities.png" alt-text="Konfigurazio-urratsa iritziak aztertzeko jarduerak hautatzeko.":::

1. Hautatu sentimenduak aztertzeko erabili nahi dituzun jarduerak, eta hautatu **Hurrengoa**.
 
1. Mapeatu zure datuetako atributuak ereduaren atributuekin. Hautatu **Gorde** zure hautaketak aplikatzeko. 

1. Datuen maparen egoera ikusten duzu. Jarraitzeko, hautatu **Hurrengoa**. 

1. urtean **Berrikusi zure modeloaren xehetasunak** urratsa, baliozkotu zure sentimenduen analisiaren konfigurazioa. Iragarpen konfigurazioaren edozein ataletara itzul zaitezke. Hautatu **Gorde eta exekutatu** analisia hasteko. 

   :::image type="content" source="media/sentiment-model-review-config.png" alt-text="Berrikusi konfiguratutako elementu guztiak erakusten dituen sentimendu-ereduaren urratsa.":::

1. Hautatu **Eginda** konfigurazio esperientzia uzteko. Prozesua hainbat ordu behar izan daiteke burutzeko erabilitako datu kopuruaren arabera. 

## <a name="review-analysis-status"></a>Berrikusi analisiaren egoera

1.  Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.
2.  Hautatu berrikusi nahi duzun iragarpena.
- **Iragarpenaren izena**: sortzean emandako iragarpenaren izena.
- **iragarpen mota** : iragarpen-erako erabilitako eredu mota.
- **Irteerako entitatea**: iragarpenaren irteera gordetzeko entitatearen izena. Joan **Datuak** > **Entitateak** aukerara izen hori duen entitatea aurkitzeko.
- **Iragarritako eremua**: eremu hau iragarpen mota batzuetarako bakarrik betetzen da eta ez da erabiltzen bezeroaren bizi-iraupenaren balioaren iragarpenean.
- **Egoera**: iragarpenaren exekuzioaren egoera.
  - **Ilaran**: iragarpena beste prozesu batzuk osatzeko zain dago.
  - **Freskatzea**: iragarpena une honetan exekutatzen ari da irteerako entitatera isuriko diren emaitzak sortzeko.
  - **Huts egin du**: iragarpenaren exekuzioak huts egin du. Xehetasun gehiago eskuratzeko, berrikusi egunkariak.
  - **Ongi osatu da**: iragarpena ongi osatu da. Aukeratu Ikusi elipsi bertikalen azpian iragarpen emaitzak berrikusteko.
- **Editatuta**: aurreikuspenerako konfigurazioa aldatu zen data.
- **Azken freskatua** : iragarpen-ek emaitzak freskatu zituen irteerako entitatean.

## <a name="manage-sentiment-analysis"></a>Kudeatu sentimenduen analisia

Iragarpenak optimizatu, konpondu, freskatu edo ezabatu ditzakezu. Berrikusi sarrerako datuen erabilgarritasun txostena iragarpen azkarragoa eta fidagarriagoa nola egin jakiteko. Informazio gehiago lortzeko, ikusi [Kudeatu iragarpenak](manage-predictions.md).

## <a name="review-analysis-results"></a>Berrikusi analisiaren emaitzak
 
1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa. 
1. Hautatu emaitzak berrikusi nahi dituzun iragarpen-en izena. Kasu honetan, hautatu berrikusi nahi duzun sentimendu-analisia. 

### <a name="summary-tab"></a>Laburpena fitxa

Emaitzen orrialdean datuen lau atal nagusi daude. 

- **Sentimenduaren batez besteko puntuazioa** : bezero guztien sentimendu orokorra ulertzen laguntzen dizu. Sentimenduen puntuazioak hiru kategoriatan biltzen dira: 
  1.    Negatiboa (-5 > 2)
  2.    Neutroa (-1 > 1)
  3.    Positiboa (2 > 5) 
  
  :::image type="content" source="media/overall-customer-sentiment.png" alt-text="Bezeroen sentimendu orokorraren irudikapen bisuala.":::

- **Bezeroen banaketa sentimendu puntuazioaren arabera** : Bezeroak talde negatibo, neutro eta positiboetan sailkatzen dira, euren sentimenduen puntuazioaren arabera. Pasatu sakatu histogramako barren gainetik talde bakoitzeko bezero kopurua eta batez besteko sentimenduaren puntuazioa ikusteko. Datu hauek lagun zaitzake [bezeroen segmentuak sortu](segments.md) beren sentimenduen puntuazioetan oinarrituta.  

  :::image type="content" source="media/distribution-customer-sentiment.png" alt-text="Barra-diagrama bezeroaren sentimendua erakusten duen hiru sentimendu taldeetan.":::

- **Sentimenduaren batez besteko puntuazioa denboran zehar** : Bezeroaren sentimendua alda daiteke denborarekin. Zure bezeroen sentimenduen joerak ematen ditugu zure datuen denbora tarterako. Ikuspegi honek sasoiko sustapenek, produktuen aurkezpenek edo denbora mugatu duten beste esku-hartzeek bezeroen sentimenduan duten eragina neurtzen lagun zaitzake. Ikusi grafikoa goitibeherako menuan interesa duen urtea hautatuz. 

  :::image type="content" source="media/sentiment-score-over-time.png" alt-text="Historia-diagrama, denboran zehar sentimenduaren puntuazioa lerro gisa irudikatuta.":::
 
- **Negozioaren alderdien arteko sentimendua** : Taula honek negozioaren alderdien batez besteko sentimendua zerrendatzen du. Zure negozioaren zein alderdik dagoeneko bezeroak asetzen dituzten edo arreta handiagoa eskatzen duten alderdiak neurtzen lagun zaitzake. Onartutako negozio-alderdiren batekin lerrokatzen ez diren iritzi-erregistroak azpian sailkatuta daude **Bestela**. Taula alfabetikoki ordenatuta dago lehenespenez. Sailkapena alda dezakezu taulako goiburu bat hautatuta.

  :::image type="content" source="media/sentiment-across-business-aspects.png" alt-text="Lotutako sentimendu-balioa duten negozio-alderdien zerrenda eta hori aipatzen duten bezero-kopurua.":::
 
  Hautatu negozio-alderdi baten izena ereduak negozio-alderdi bat nola identifikatzen duen informazio gehigarria ikusteko. Panel honetan bi zati daude: 

  - **Eragin handiko hitzak** : bezeroen iritzietan AI ereduak negozio-alderdi baten identifikazioan eragina izan duten hitz nagusiak erakusten ditu. 
    **Erakutsi hitz iraingarriak** : Jatorrizko bezeroen iritzien datuen zerrendan hitz iraingarriak sartzeko aukera ematen dizu. Lehenespenez, desaktibatuta dago.  Hitz iraingarrien maskaratzeak AI eredu batek funtzionatzen du eta baliteke hitz iraingarri guztiak ez hautemateko. Sailkapena errepikatzen eta entrenatzen jarraitzen dugu errendimendu optimorako. Espero bezala iragazi ez den hitz iraingarri bat hautematen baduzu, jakinarazi iezaguzu. 
    
    :::image type="content" source="media/offensive-words-sentiment.png" alt-text="Eragin handiko hitzen zerrenda, hitz iraingarriak erakusteko edo ezkutatzeko etengailuarekin.":::
 
  - **Feedback laginak** : benetako iritzi-erregistroak erakusten ditu zure datuetan. Hitzak kolorez kodetzen dira negozio-alderdi baten identifikazioan duten eraginaren arabera. 


### <a name="influential-words-analysis-tab"></a>Eragin handiko hitzak aztertzeko fitxa

Sentimendu ereduak nola funtzionatzen duen azaltzen duten informazio gehigarriko hiru atal daude.
  
1. **Sentimendu positiboan laguntzen duten hitz nagusiak** : Bezeroen iritzietan AI ereduak sentimendu positiboaren identifikazioan eragina izan duten hitz nagusiak erakusten ditu.  
2. **Sentimendu negatiboan laguntzen duten hitz nagusiak** : AI ereduak sentimendu negatiboa identifikatzean eragina izan duten hitz nagusiak erakusten ditu bezeroen iritzietan.  
3. **Feedback laginak** : benetako iritzien erregistroak erakusten ditu, bata sentimendu negatiboa duena eta bestea sentimendu positiboa duena. Iritzi-erregistroetako hitzak esleitutako sentimendu puntuazioari egindako ekarpenaren arabera nabarmentzen dira. Sentimendu positiboa lortzen laguntzen duten hitzak berdez nabarmentzen dira. Puntuazio negatiboa lortzen duten hitzak gorriz nabarmentzen dira.
   Hautatu **Gehiago ikusi** sentimendu-ereduaren funtzionamenduari buruzko informazio eta testuinguru gehiago ematen duten iritzi-lagin gehiago kargatzeko.
   
   :::image type="content" source="media/sentiment-feedback-samples.png" alt-text="Bezeroen iritziei buruzko sentimenduen analisiaren adibideak.":::
 
**Erakutsi hitz iraingarriak** : Jatorrizko bezeroen iritzien datuen zerrendan hitz iraingarriak sartzeko aukera ematen dizu. Lehenespenez, desaktibatuta dago.  Hitz iraingarrien maskaratzeak AI eredu batek funtzionatzen du eta baliteke hitz iraingarri guztiak ez hautemateko. Sailkapena errepikatzen eta entrenatzen jarraitzen dugu errendimendu optimorako. Espero bezala iragazi ez den hitz iraingarri bat hautematen baduzu, jakinarazi iezaguzu. 

## <a name="act-on-analysis-results"></a>Analisien emaitzen gainean jardutea

Erraz has zaitezke bezeroen segmentu berriak sortzen sentimenduen analisiaren emaitzen orrialdetik hautatuta **Sortu segmentuak** ereduaren emaitza orriaren goialdean.

:::image type="content" source="media/create-segment-model.png" alt-text="Komando-barra iragarpen modeloetan aukerak dituena.":::
 
## <a name="potential-bias"></a>Alborapen potentziala

Adimen artifizial iragarlea erabiltzen duen edozein eginbiderekin gertatzen den bezala, bezeroen sentimendua iragartzeko erabiltzen dituzun datuen alborapen potentzialaz jabetu beharko zenuke. Esaterako, iritziak digitalki bakarrik biltzen badituzu, zurekin batez ere negozioak egiten dituzten bezeroen iritziak galdu ditzakezu, eta horrek eginbidearen irteeran eragina izan dezake.

Ezaugarri honek datuak ebaluatzeko eta datu horietan oinarritutako iragarpenak egiteko bitarteko automatizatuak erabiltzen dituenez, beraz, profila egiteko metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Erregelamendu Orokorrak ("GDPR") definitzen baitu. Ezaugarri hau datuak tratatzeko zure erabilera DBAO edo beste lege edo arau batzuen menpe egon daiteke. Zure erabilera ziurtatzeaz arduratzen zara Dynamics 365 Customer Insights, sentimenduen azterketa barne, aplikagarriak diren lege eta araudi guztiak betetzen ditu, pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak barne.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

