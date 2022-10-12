---
title: Aztertu bezeroen iritzia (aurrebista)
description: Ikasi bezeroen iritziei buruzko sentimenduen analisiaren eredua nola erabiltzen Dynamics 365 Customer Insights.
ms.date: 09/14/2022
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: wmelewong
ms.author: wameng
manager: shellyha
ms.openlocfilehash: 61ce9fb18efa6152dddb2e31f4fd0366a31ac2c7
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610443"
---
# <a name="analyze-sentiment-in-customer-feedback-preview"></a>Aztertu sentimendua bezeroen iritzietan (aurrebista)

Sentimenduen analisiak bezeroen sentimendua sintetizatzeko eta negozio-alderdiak hobetzeko aukera gisa identifikatzea ahalbidetzen dizu. Customer Insights eginbide honek ondo zer funtzionatzen duen eta zer zuzendu behar duzun ulertzen laguntzen dizu. Bezeroen gogobetetze eta leialtasun handia eragiten duten esperientziak ahalbidetzen dituzten negozio-ekintzak gidatzen lagun zaitzake.

## <a name="overview"></a>Informazio orokorra

Sentimenduak aztertzeko eginbideak bezero ID bakoitzeko bi informazio eratorri sortzen ditu. Sentimendu puntuazioa (-5etik 5era) eta negozio-alderdi aplikagarrien zerrenda (negozio-arloak) batera, bezeroen iritzia hobeto ulertzen laguntzen dizutenak.

Azterketa honek laguntzen dizu:
- Lortu bezeroen sentimenduen ikuspegi orokorra marka edo erakunde baten aurrean
- Identifikatu sentimendu negatiboa duten bezeroak zure kanpainak eta konpromisoak bideratzeko eta etekin handiagoa lortzeko optimizatzeko  
- Bezeroek adierazitako arazoekin negozio-alderdiak identifikatzea  
- Segmentatu bezeroak beren sentimenduaren arabera kanpaina pertsonalizatuak egiteko, salmenta, marketina eta laguntza esfortzuekin zuzenduta
- Optimizatu negozio-eragiketak bezeroek aipatu dituzten kezka edo aukerei zuzenduta
- Ongi dabiltzan negozio-alderdiak ezagutzea eta bezero pozik saritzea leialtasun eta sustapen programen bidez

Ereduak iritzien iruzkinei iritzi-puntuazio edo negozio-alderdi jakin bat esleitzeko ereduaren erabakian eragina izan duten hitzen zerrenda eskaintzen du.  

Bi erabiltzen ditugu **Hizkuntza Naturalaren Prozesamenduaren (NLP) ereduak** : Lehenengoak iritzi-iruzkin bakoitzari sentimendu puntuazio bat esleitzen dio. Bigarren ereduak iritzi bakoitza negozio-alderdi aplikagarri guztiekin lotzen du. Ereduak sare sozialetako, txikizkako, jatetxeetako, kontsumoko produktuetako eta automobilgintzako industrietako iturrietako datu publikoetan trebatzen dira.
  
Ereduari iritzi-datuekin lotzeko aurrez definitutako negozio-alderdiak hauek dira:
- Kontuen kudeaketa
- Ordainketa eta ordainketa
- Bezeroentzako laguntza-zerbitzua
- Dendan jasotzeko
- Ontziak bidaltzea eta berreskuratzea
- Aurrez erreserbatzea
- Prezioa
- Pribatutasuna eta segurtasuna
- Promozioak eta sariak
- Ordainagiria eta bermea
- Itzultzeko trukea eta baliogabetzea
- Betetzeko zehaztasuna
- Webgune/aplikazioen kalitatea

> [!NOTE]
> Gaur egun, ingeleseko bezeroen iritzien inguruko sentimenduen analisia onartzen dugu. Etorkizunean hizkuntza gehiago onartuko dira. Beste hizkuntza batzuetan iritziak kargatzen badira, ereduak emaitzak emango ditu oraindik. Hala ere, emaitza hauek ez dira zehatzak izango.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Kolaboratzaileen baimenak](permissions.md)
- [Bateratua](data-unification.md) testuaren iritziaren datuak. Oso gomendatzen dizugu [konfiguratu zure iritzi-datuen entitateak mota semantikoko jarduera-entitate gisa](map-entities.md#select-primary-key-and-semantic-type-for-attributes) (Iritzi mota).
- Bezeroaren ID bateratua (UCID) datuen bateratzetik testu-erantzunaren datu-erregistroak bezero indibidual batekin lotzeko.
- Oharren IDa
- Iritziaren denbora-zigilua
- Oharren testua

Customer Insights-ek gehienez 10 milioi iritzi-erregistro prozesatu ditzake eredu bakarrerako. Ereduak 128 hitz arteko iruzkinak azter ditzake. Iritzi-iruzkin bat luzeagoa bada, analisiak lehen 128 hitzak bakarrik hartzen ditu kontuan.

> [!NOTE]
> Iritzi-entitate bakarra konfigura daiteke. Iritzi-entitate anitz badaude, konbinatu Power Query datuak sartu aurretik.

## <a name="configure-a-sentiment-analysis"></a>Konfiguratu sentimenduen analisia

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Bezeroen sentimenduen azterketa (aurrebista)** teila.

1. Hautatu **Hasi erabiltzen**.

1. **Izena** analisia eta eman **Negozio-alderdiaren irteera-entitatearen izena** eta **Sentimendu puntuazioa irteerako entitatearen izena**.

1. Hautatu **Hurrengoa**.

1. Hautatu **Gehitu datuak** rentzat **Bezeroen iritzia**.

1. Hautatu jarduera semantikoaren mota **Iritzia** feedback datuak dituena. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

   :::image type="content" source="media/sentiment-add-feedback-activities.png" alt-text="Sentimenduak aztertzeko iritzi-jarduerak hautatzeko konfigurazio-urratsa.":::

1. Hautatu sentimenduak aztertzeko erabili nahi dituzun jarduerak, eta hautatu **Hurrengoa**.

1. Mapeatu zure datuetako atributuak ereduaren atributuekin. 

1. Sakatu **Gorde**.

1. Hautatu **Hurrengoa**. The **Berrikusi eta exekutatu** urratsak konfigurazioaren laburpena erakusten du eta analisia sortu aurretik aldaketak egiteko aukera ematen du.

1. Hautatu **Editatu** aldaketak berrikusteko eta egiteko edozein urratsetan.

1. Zure hautapenekin pozik bazaude, hautatu **Gorde eta exekutatu** eredua exekutatzen hasteko. Hautatu **Eginda**. The **Nire iragarpenak** fitxa bistaratzen da iragarpen sortzen ari den bitartean. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

[!INCLUDE [progress-details](includes/progress-details-pane.md)]

## <a name="view-analysis-results"></a>Ikusi analisiaren emaitzak

1. Joan **Adimena** > **Iragarpenak**.

1. -n **Nire iragarpenak** fitxan, hautatu ikusi nahi duzun iragarpen.

Emaitzen bi fitxa daude.

### <a name="sumary-tab"></a>Laburpen fitxa

Emaitzen orrialdean datuen lau atal nagusi daude.

- **Sentimenduaren batez besteko puntuazioa** : Sentimenduen puntuazioak bezero guztien sentimendu orokorra ulertzen laguntzen dizu.
  - **Negatiboa** (-5 > 2)
  - **Neutroa** (-1 > 1)
  - **Positiboa** (2 > 5)
  
  :::image type="content" source="media/overall-customer-sentiment.png" alt-text="Bezeroen sentimendu orokorraren irudikapen bisuala.":::

- **Bezeroen banaketa sentimendu puntuazioaren arabera** : Bezeroak talde negatibo, neutro eta positiboetan sailkatzen dira, euren sentimenduen puntuazioaren arabera. Pasatu sakatu histogramako barren gainetik talde bakoitzeko bezero kopurua eta batez besteko sentimenduaren puntuazioa ikusteko. Datu hauek lagun zaitzake [bezeroen segmentuak sortu](prediction-based-segment.md) beren sentimenduen puntuazioetan oinarrituta.  

  :::image type="content" source="media/distribution-customer-sentiment.png" alt-text="Barra-diagrama bezeroaren sentimendua erakusten duen hiru sentimendu-taldeetan.":::

- **Sentimenduaren batez besteko puntuazioa denboran zehar** : Bezeroaren sentimendua alda daiteke denborarekin. Zure bezeroen sentimenduen joerak ematen ditugu zure datuen denbora tarterako. Ikuspegi honek sasoiko sustapenek, produktuen aurkezpenek edo denbora mugatutako beste esku-hartzeek bezeroen sentimenduan duten eragina neurtzen laguntzen dizu. Ikusi grafikoa goitibeherako menuan interesa duen urtea hautatuz.

  :::image type="content" source="media/sentiment-score-over-time.png" alt-text="Historia-diagrama, denboran zehar sentimenduaren puntuazioa lerro gisa irudikatuta.":::

- **Negozioaren alderdien arteko sentimendua** : negozio-alderdietako batez besteko sentimenduak zure negozioaren zein alderdik bezeroak asetzen dituzten edo arreta gehiago behar duten neurtzen laguntzen dizu. Onartutako negozio-alderdiren batekin lerrokatzen ez diren iritzi-erregistroak azpian sailkatuta daude **Bestela**. Ordenatu datuak edozein zutabe hautatuz.

  :::image type="content" source="media/sentiment-across-business-aspects.png" alt-text="Lotutako sentimendu-balioarekin eta hori aipatzen duten bezeroen kopurua duten negozio-alderdien zerrenda.":::

  Hautatu negozio-alderdi baten izena ereduak negozio-alderdi bat nola identifikatzen duen ikusteko:

  - **Eragin handiko hitzak** : AI ereduak bezeroen iritzietan negozio-alderdi baten identifikazioan eragin zuten hitz nagusiak.
    **Erakutsi hitz iraingarriak** : Jatorrizko bezeroen iritzien datuen zerrendan hitz iraingarriak sartzeko aukera ematen dizu. Lehenespenez, desaktibatuta dago.  Hitz iraingarrien maskaratzeak AI eredu batek funtzionatzen du eta baliteke hitz iraingarri guztiak ez hautemateko. Espero bezala iragazi ez den hitz iraingarri bat hautematen baduzu, jakinarazi iezaguzu.

    :::image type="content" source="media/offensive-words-sentiment.png" alt-text="Eragin handiko hitzen zerrenda, hitz iraingarriak erakusteko edo ezkutatzeko etengailuarekin.":::

  - **Feedback laginak** : benetako iritzi-erregistroak zure datuetan. Hitzak kolorez kodetzen dira negozio-alderdi baten identifikazioan duten eraginaren arabera.

### <a name="influential-words-analysis-tab"></a>Eragin handiko hitzak aztertzeko fitxa

Sentimendu ereduak nola funtzionatzen duen azaltzen duten informazio osagarriaren hiru atal daude.
  
- **Sentimendu positiboan laguntzen duten hitz nagusiak** : AI ereduak bezeroen iritzietan sentimendu positiboa antzematean eragin duten hitz nagusiak.  

- **Sentimendu negatiboan laguntzen duten hitz nagusiak** : AI ereduak bezeroen iritzietan sentimendu negatiboa identifikatzean eragin duten hitz nagusiak.

- **Feedback laginak** : Benetako iritzi-erregistroak, bat sentimendu negatiboa duena eta bestea sentimendu positiboa duena. Iritzi-erregistroetako hitzak esleitutako sentimendu puntuazioari egindako ekarpenaren arabera nabarmentzen dira. Sentimendu positiboa lortzen laguntzen duten hitzak berdez nabarmentzen dira. Puntuazio negatiboa lortzen duten hitzak gorriz nabarmentzen dira.
   Hautatu **Gehiago ikusi** feedback-lagin gehiago kargatzeko.
  
   :::image type="content" source="media/sentiment-feedback-samples.png" alt-text="Bezeroen iritziei buruzko sentimenduen analisiaren adibideak.":::

**Erakutsi hitz iraingarriak** : Jatorrizko bezeroen iritzien datuen zerrendan hitz iraingarriak sartzeko aukera ematen dizu. Lehenespenez, desaktibatuta dago.  Hitz iraingarrien maskaratzeak AI eredu batek funtzionatzen du eta baliteke hitz iraingarri guztiak ez hautemateko. Espero bezala iragazi ez den hitz iraingarri bat hautematen baduzu, jakinarazi iezaguzu.

## <a name="act-on-analysis-results"></a>Analisien emaitzen gainean jardutea

Sentimenduen analisiaren emaitzetatik bezeroen segmentu berriak sortzeko, hautatu **Sortu segmentuak** ereduaren emaitza orriaren goialdean.

## <a name="potential-bias"></a>Alborapen potentziala

Adimen artifizial iragarlea erabiltzen duen edozein funtzion bezala, bezeroen sentimendua aurreikusteko erabiltzen dituzun datuetan alborapen potentziala egon liteke. Esate baterako, iritziak digitalki soilik biltzen badituzu, baliteke zurekin pertsonalki negozioak nagusiki egiten dituzten bezeroen iritziak galtzea, eta horrek funtzioaren irteeran eragiten du.

Ezaugarri honek datuak ebaluatzeko eta datu horietan oinarritutako iragarpenak egiteko bitarteko automatizatuak erabiltzen dituenez, beraz, profila egiteko metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Erregelamendu Orokorrak ("GDPR") definitzen baitu. Ezaugarri hau datuak tratatzeko zure erabilera DBAO edo beste lege edo arau batzuen menpe egon daiteke. Zure erabilera ziurtatzeaz arduratzen zara Dynamics 365 Customer Insights, sentimenduen azterketa barne, aplikagarriak diren lege eta arau guztiak betetzen ditu, pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak barne.

[!INCLUDE [footer-include](includes/footer-banner.md)]

