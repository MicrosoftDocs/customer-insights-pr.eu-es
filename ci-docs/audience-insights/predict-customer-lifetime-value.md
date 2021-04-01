---
title: Bezeroaren balio osoaren iragarpena (CLV)
description: Aurreikusi etorkizunean bezero aktiboen diru-sarrerak.
ms.date: 02/05/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: wameng
manager: shellyha
ms.openlocfilehash: 835a9f3371a8c1b1a10d5c6901c03e1df5379d3d
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5595780"
---
# <a name="customer-lifetime-value-clv-prediction-preview"></a>Bezeroaren bizi-iraupenaren (CLV) balioa (aurreargitalpena)

Aurreikusi bezero aktibo partikularrek zure negozioari ekarriko dioten balizko balioa (diru-sarrerak) etorkizunean zehaztutako denbora-tarte batean. Ezaugarri honek hainbat helburu lortzen lagun zaitzake: 
- Balio handiko bezeroak identifikatu eta ikuspegi hori prozesatu
- Sortu bezeroen segmentu estrategikoak haien balio potentzialean oinarrituta kanpaina pertsonalizatuak egiteko bideratutako salmentekin, marketinarekin eta laguntza esfortzuekin
- Produktuen garapena bideratu bezeroaren balioa handitzen duten ezaugarrietan oinarrituz
- Optimizatu salmenten edo marketinaren estrategia eta aurrekontua zehatzago esleitu bezeroen dibulgaziorako
- Balio handiko bezeroak aitortu eta saritu leialtasun edo sari programen bidez 

## <a name="prerequisites"></a>Aurrebaldintzak

Hasi aurretik, islatu CLV-k duen garrantzia zure negoziorako. Gaur egun, transakzioetan oinarritutako CLV iragarpen onartzen dugu. Bezero baten aurreikusitako balioa negozio-transakzioen historian oinarritzen da. Iragarpena sortzeko, gutxienez behar duzu [Laguntzailea](permissions.md) baimenak.

CLV modeloa konfiguratzeak eta exekutatzeak denbora asko behar ez duenez, kontuan hartu sarrera hobespen desberdinak dituzten hainbat eredu sortzea eta alderatu modeloaren emaitzak, zure negozioaren beharretara hobekien egokitzen den eredua ikusteko.

###  <a name="data-requirements"></a>Datuen eskakizunak

Datu hauek beharrezkoak dira, eta aukerako gisa markatuta daudenean, gomendagarria da modeloaren errendimendua handitzeko. Zenbat eta datu gehiago prozesatu ereduak, orduan eta zehatzagoa izango da iragarpena. Hori dela eta, bezeroen jardueren datu gehiago sartzea gomendatzen dizugu, eskuragarri badago.

- Bezeroaren identifikatzailea: identifikazio bakarra bezero bakoitzarekin transakzioak lotzeko

- Transakzioen historia: transakzio historikoen erregistroa beheko datu semantikoen eskemarekin
    - Transakzioaren IDa: transakzio bakoitzaren identifikatzaile esklusiboa
    - Transakzioaren data: data da, hobe transakzio bakoitzaren denbora-zigilua bada
    - Transakzioaren zenbatekoa: transakzio bakoitzaren diru-balioa (adibidez, diru-sarrera edo irabazien marjina)
    - Itzultzei esleitutako etiketa (aukerakoa): transakzioa itzulera den ala ez adierazten duen balio boolearra 
    - Produktuaren IDa (aukerakoa): transakzioan parte hartu duen produktuaren IDa

- Datu gehigarriak (aukerakoa), adibidez
    - Web-jarduerak: webgunearen bisiten historia, posta elektronikoaren historia
    - Leialtasun-jarduerak: leialtasuna saritzeko puntuak sortzearen eta amortizazioaren historia
    - Bezeroarentzako arreta-zerbitzu erregistroa, zerbitzuaren dei-, kexa- edo itzulketa-historia
- Bezeroen jarduerei buruzko datuak (aukerakoa):
    - Mota bereko jarduerak bereizteko jarduera identifikatzaileak
    - Bezeroaren identifikadoreak maparen jardueretan zure bezeroentzat
    - Jardueren izena eta jardueraren data biltzen dituen jarduera
    - Jardueren datu semantikoen eskemak honakoak dira: 
        - Gako nagusia: jarduera baterako identifikatzaile bakarra
        - Denbora-zigilua: gako nagusian identifikatutako gertaeraren data eta ordua
        - Gertaera (jardueraren izena): erabili nahi duzun gertaeraren izena
        - Xehetasunak (zenbatekoa edo balioa): bezeroaren jarduerari buruzko xehetasunak

## <a name="create-a-customer-lifetime-value-prediction"></a>Sortu bezeroaren bizi-iraupenaren balioaren iragarpena

1. Hartzaileei buruzko xehetasunetan, joan hona: **Adimena** > **Iragarpenak**.

1. Hautatu **Bezeroaren bizi-iraupenaren balioa** fitxa eta hautatu **Erabili eredua**. 

1. **Bezeroaren bizi-iraupenaren balioa (aurrebista)** panelean, hautatu **Hasi erabiltzen**.

1. **Eman izena eredu honi** eta **Irteerako entitatearen izenari** beste eredu edo entitate batzuetatik bereizteko.

1. Hautatu **Hurrengoa**.

### <a name="define-model-preferences"></a>Zehaztu ereduaren hobespenak

1. Ezarri **Iragarpen denbora-tartea** etorkizunean CLV-a noraino iragarri nahi duzun definitzeko.    
   Lehenespenez, unitatea hilabete gisa ezartzen da. Urteetara alda dezakezu etorkizunean gehiago begiratzeko.

   > [!TIP]
   > Ezarritako denbora-tarte baterako CLV zehaztasunez aurreikusteko, datu historikoen aldi konparagarria behar duzu. Adibidez, datozen 12 hilabeteetarako aurreikusi nahi baduzu, gutxienez 18 - 24 hilabeteen datu historikoak izatea gomendatzen da.

1. Zehaztu zer **Bezero aktiboak** zure negoziorako esan nahi du. Ezarri bezeroak aktibo jotzeko gutxienez transakzio bat izan behar duen denbora-tartea. Ereduak bezero aktiboentzako CLV soilik aurreikusiko du. 
   - **Ereduak erosketa tartea kalkulatzen utzi (gomendatua)**: ereduak zure datuak aztertzen ditu eta erosketa historikoetan oinarritutako denbora tartea zehazten du.
   - **Ezarri tartea eskuz**: bezero aktibo baten negozioaren definizio zehatza baduzu, aukeratu aukera hau eta ezarri epea horren arabera.

1. Definitu pertzentila **Balio handiko bezeroa** ereduak zure negozioaren definizioarekin bat datozen emaitzak eman ditzan.
    - **Ereduaren kalkulua (gomendatua)**: ereduak zure datuak aztertzen ditu eta balio handiko bezero bat zure negoziorako zer izan daitekeen zehazten du zure bezeroen transakzio-historian oinarrituta. Ereduak arau heuristikoa erabiltzen du (80/20 arauan edo Pareto-ren printzipioan inspiratuta) balio handiko bezeroen proportzioa aurkitzeko. Garai historikoan zure negozioak % 80 diru-sarrera metatuak lortu zituen bezeroen ehunekoa balio handiko bezeroentzat hartzen da. Normalean, % 30-40 bezero baino gutxiagok % 80 diru-sarrera metatuak lortzen dituzte. Hala ere, zenbaki hori zure negozioaren eta industriaren arabera alda daiteke.    
    - **Bezero aktibo nagusien ehunekoa**: definitu balio handiko bezeroak zure negoziorako ordaindutako bezero aktiboen pertzentila gisa. Adibidez, aukera hau erabil dezakezu balio handiko bezeroak etorkizunean ordaintzen duten bezeroen % 20 gisa definitzeko.

    Zure negozioak balio handiko bezeroak beste modu batean definitzen baditu, [aditzera eman nahiko genukeen bezala](https://go.microsoft.com/fwlink/?linkid=2074172).

1. Hurrengo urratsera joateko, hautatu **Hurrengoa**.

### <a name="add-required-data"></a>Gehitu beharrezko datuak

1. **Beharrezko datuak** urratsean, hautatu **Gehitu datuak** **Bezeroen transakzio-historia** atalean eta aukeratu transakzioen edo erosketen historiari buruzko informazioa ematen duen entitatea, [aurrebaldintzak](#prerequisites) atalean deskribatu moduan.

1. Esleitu eremu semantikoak erosketa-historiako entitateko atributuetara eta hautatu **Hurrengoa**.

   :::image type="content" source="media/clv-add-customer-data-mapping.png" alt-text="Konfigurazio-urratsaren irudia beharrezko datuen atributuak esleitzeko.":::
 
1. Beheko eremuak betetzen ez badira, konfiguratu erosketa-historiaren entitatea *Bezeroaren* entitatera eta hautatu **Gorde**.
    1. Hautatu Transakzio-historiaren entitatea.
    1. Aukeratu erosketa-historiaren entitatean bezeroa identifikatzen duen eremua. Zure Bezeroaren entitatearen bezeroaren ID nagusiarekin erlazionatu behar da.
    1. Hautatu bezero nagusiaren entitatearekin bat datorren lan-fluxuaren entitate bat.
    1. Idatzi izena deskribatzen duena harremana.

      :::image type="content" source="media/clv-add-customer-data-relationship.png" alt-text="Konfigurazio urratsaren irudia bezero entitatearekin harremana definitzeko.":::

1. Hautatu **Hurrengoa**.

### <a name="add-optional-data"></a>Gehitu aukerako datuak

Bezeroen interakzio nagusiak islatzen dituzten datuek (adibidez, webgunea, bezeroarentzako arreta-zerbitzu eta gertaeren erregistroak) testuingurua gehitzen dute transakzio erregistroetan. Zure bezeroen jardueren datuetan aurkitutako eredu gehiagok aurreikuspenen zehaztasuna hobe dezakete. 

1. Urtean **Datu osagarriak (aukerakoa)** urratsa, hautatu **Gehitu datuak**. Aukeratu bezeroaren jardueren entitateari buruzko informazioa ematen duen entitatea [aurrebaldintzetan](#prerequisites) azaltzen den moduan.

1. Esleitu eremu semantikoak bezeroaren jardueraren entitateko atributuetara eta hautatu **Hurrengoa**.

   :::image type="content" source="media/clv-additional-data-mapping.png" alt-text="Konfigurazio-urratsaren datu gehigarrien eremuak esleitzeko.":::

1. Aukeratu gehitzen ari zaren bezeroaren jarduera motarekin bat datorren jarduera mota. Aukeratu lehendik dauden jarduera moten artean edo gehitu jarduera mota berri bat.

1. Konfiguratu harremana bezeroaren jarduera entitatetik *Bezeroa* entitatea.
    
    1. Aukeratu bezeroaren jardueraren taulan bezeroa identifikatzen duen eremua. Zuzenean erlazionatuta egon daiteke zure *Bezero* entitatearen bezeroaren ID nagusiarekin.
    1. Hautatu botoia *Bezero* entitatea bat datorrena zure lehen *Bezeroa* entitatearekin.
    1. Idatzi izena deskribatzen duena harremana.

   :::image type="content" source="media/clv-additional-data.png" alt-text="Konfigurazio-fluxuko urratsaren irudia datu osagarriak gehitzeko eta jarduera konfiguratutako adibideekin konfiguratzeko.":::

1. Sakatu **Gorde**.    
    Gehitu datu gehiago bezeroen beste jarduera batzuk sartu nahi badituzu.

1. Hautatu **Hurrengoa**.

### <a name="set-update-schedule"></a>Konfiguratu antolaketaren eguneratzea

1. **Datuak eguneratzeko egutegia** urratsean, aukeratu maiztasuna zure modeloa berriro trebatzeko azken datuetan oinarrituta. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, hartzaileen xehetasunetan datu berriak sartu ahala. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.


### <a name="review-and-run-the-model-configuration"></a>Berrikusi eta exekutatu modeloaren konfigurazioa

1. **Berrikusi modeloaren xehetasunak** urratsean, balioztatu iragarpenaren konfigurazioa. Aurreikuspen konfigurazioaren edozein ataletara joan zaitezke hautatuta **Editatu** erakutsitako balioaren azpian. Konfigurazio-urrats bat ere hauta dezakezu aurrerapen adierazletik.

1. Balio guztiak ondo konfiguratuta badaude, hautatu **Gorde eta exekutatu** eredua martxan jartzen hasteko. **Nire iragarpenak** fitxan, iragarpen prozesuaren egoera ikus dezakezu. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

## <a name="review-prediction-status-and-results"></a>Berrikusi iragarpenen egoera eta emaitzak

### <a name="review-prediction-status"></a>Berrikusi iragarpenen egoera

1.  Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.
2.  Hautatu berrikusi nahi duzun iragarpena.

- **Iragarpenaren izena**: sortzean emandako iragarpenaren izena.
- **Iragarpen mota**: iragarpenean erabilitako eredu mota
- **Irteerako entitatea**: iragarpenaren irteera gordetzeko entitatearen izena. Joan **Datuak** > **Entitateak** aukerara izen hori duen entitatea aurkitzeko.
- **Iragarritako eremua**: eremu hau iragarpen mota batzuetarako bakarrik betetzen da eta ez da erabiltzen bezeroaren bizi-iraupenaren balioaren iragarpenean.
- **Egoera**: iragarpenaren exekuzioaren egoera.
    - **Ilaran**: iragarpena beste prozesu batzuk osatzeko zain dago.
    - **Freskatzea**: iragarpena une honetan exekutatzen ari da irteerako entitatera isuriko diren emaitzak sortzeko.
    - **Huts egin du**: iragarpenaren exekuzioak huts egin du. Xehetasun gehiago eskuratzeko, [berrikusi egunkariak](#troubleshoot-a-failed-prediction).
    - **Ongi osatu da**: iragarpena ongi osatu da. Aukeratu **Ikusi** elipsi bertikalen azpian iragarpen emaitzak berrikusteko.
- **Editatuta**: aurreikuspenerako konfigurazioa aldatu zen data.
- **Azken freskatua**: iragarpena freskatu den data irteerako entitatean.


### <a name="review-prediction-results"></a>Berrikusi iragarpenen emaitzak

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Aukeratu emaitzak berrikusi nahi dituzun iragarpena.

Emaitza orrialdearen barruan hiru datu nagusi daude.

- **Trebakuntza ereduaren errendimendua** : A, B edo C kalifikazio posibleak dira. Kalifikazio honek iragarpenaren errendimendua adierazten du eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia hartzen lagun zaitzake. Aukeratu **Ikasi puntuazio honi buruz** azpiko ereduaren errendimendu-metrikak eta azken ereduaren errendimendu-kalifikazioa nola atera den hobeto ulertzeko.
  
  :::image type="content" source="media/clv-model-score.png" alt-text="Ereduaren puntuazioaren informazio koadroaren irudia A kalifikazioarekin.":::

  Iragarpen konfiguratzerakoan emandako balio handiko bezeroen definizioa erabiliz, sistemak ebaluatzen du AA ereduak balio handia izan zuen bezero handiak aurreikustean oinarrizko eredu batekin alderatuta.    

  Kalifikazioak arau hauetan oinarrituta zehazten dira:
  - A ereduak zehaztasunez aurreikusi zuen gutxienez % 5eko balio handiko bezero gehiago oinarrizko ereduarekin alderatuta.
  - B ereduak zehaztasunez aurreikusi zuen gutxienez % 0-5 balio handiko bezero gehiago oinarrizko ereduarekin alderatuta.
  - C ereduak zehaztasunez aurreikusi zuen balio handiko bezero gutxiago oinarrizko ereduarekin alderatuta.

  **Ereduaren balorazioa** panelean adimen artifizialeko ereduaren errendimenduari eta oinarrizko ereduari buruzko xehetasun gehiago agertzen dira. Oinarrizko ereduak AI ez oinarritutako ikuspegia erabiltzen du bezeroek bizitzako balioa kalkulatzeko batez ere bezeroek egindako erosketa historikoetan oinarrituta.     
  Oinarrizko ereduaren arabera CLV kalkulatzeko erabilitako formula estandarra:    

  *CLV bezero bakoitzeko = Bezeroak bezeroaren leiho aktiboan egindako batez besteko hileko erosketa * Hilabete kopurua CLV iragarpen aldian * Bezero guztien atxikipen tasa orokorra*

  Adimen artifizialeko eredua oinarrizko ereduarekin alderatzen da, bi modeloen errendimendu metrikan oinarrituta.
  
  - **Balio handiko bezeroak iragartzeko arrakasta-tasa**

    Ikusi aldea adimen artifizialeko eredua erabiliz balio handiko bezeroak iragartzeko oinarrizko ereduarekin alderatuta. Adibidez, % 84 arrakasta-tasak esan nahi du prestakuntzako datuetan balio handiko bezero guztien artean adimen artifizialeko ereduak % 84 zehazki harrapatu zuela. Ondoren, arrakasta-tasa hau oinarrizko ereduaren arrakasta-tasarekin alderatzen dugu, aldaketa erlatiboa jakinarazteko. Balio hau ereduari kalifikazio bat emateko erabiltzen da.

  - **Erroreen metrikak**
    
    Beste metrika batek modeloaren errendimendu orokorra berrikusteko aukera ematen du etorkizuneko balioak iragartzeko akatsen arabera. Errore batez besteko akats karratuaren (RMSE) metrika orokorra erabiltzen dugu errore hori ebaluatzeko. RMSE datu kuantitatiboak iragartzeko eredu baten errorea neurtzeko modu estandarra da. Adimen artifizialeko ereduaren RMSE oinarrizko ereduaren RMSEarekin alderatzen da eta desberdintasun erlatiboa jakinarazi da.

  Adimen artifizialeko ereduak bezeroen sailkapen zehatza lehenesten du zure negozioari ematen dioten balioaren arabera. Beraz, balio handiko bezeroak iragartzeko arrakasta-tasa soilik erabiltzen da azken ereduaren nota lortzeko. RMSE metrika balio arruntetarako sentikorra da. Erosketa balio izugarri altuak dituzten bezeroen ehuneko txikia duzun eszenatokietan, baliteke RMSE metrikak modeloaren errendimenduaren argazki osoa ez ematea.   

- **Bezeroen balioa pertzentilaren arabera**: balio handiko bezeroen definizioa erabiliz, bezeroak balio baxuko eta balio handiko taldetan biltzen dira, CLV iragarpenetan oinarrituta, eta taula batean agertzen dira. Histogramako barren gainetik pasatzean, talde bakoitzeko bezero kopurua eta talde horren batez besteko CLV-a ikus ditzakezu. Datu horiek lagundu dezakete nahi izanez gero [bezeroen segmentuak sortu](segments.md) CLV iragarpenetan oinarrituta.

- **Eragin gehien duten faktoreak**: hainbat faktore hartzen dira kontuan zure CLV iragarpen sortzerakoan adimen artifizialeko ereduan emandako sarrera datuetan oinarrituta. Faktore bakoitzak eredu batek sortzen dituen aurreikuspen agregatuetarako kalkulatutako garrantzia du. Faktore hauek erabil ditzakezu zure iragarpen emaitzak balioztatzen laguntzeko. Faktore horiek CLV zure bezero guztien artean aurreikusteko eragin duten faktore eragileei buruzko informazio gehiago eskaintzen dute.

## <a name="refresh-a-prediction"></a>Iragarpen bat eguneratu

Iragarpenak automatikoki freskatzen dira berean [antolatu zure datuak freskatzeko](system.md#schedule-tab) ezarpenetan konfiguratutako moduan. Eskuz freskatu ditzakezu.

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.
2. Hautatu freskatu nahi duzun iragarpenaren ondoan elipsi bertikalak.
3. Aukeratu **Freskatu**.

## <a name="delete-a-prediction"></a>Ezabatu iragarpena

Iragarpen ezabatzeak bere irteerako entitatea ere kentzen du.

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.
2. Hautatu ezabatu nahi duzun iragarpenaren ondoan elipsi bertikalak.
3. Hautatu **Ezabatu**.

## <a name="troubleshoot-a-failed-prediction"></a>Huts egin duen iragarpen baten arazoak konpontzea

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.
2. Aukeratu elipseak bertikalak errore-egunkariak ikusi nahi dituzun iragarpenaren ondoan.
3. Hautatu **Egunkariak**.
4. Berrikusi errore guztiak. Hainbat akats mota gerta daitezke eta deskribatzen dute zer baldintza eragin duen errorea. Adibidez, zehaztasunez aurreikusteko datu nahikorik ez dagoen akatsa datu gehiago hartzaileen xehetasunetan kargatuta konpondu ohi da.


[!INCLUDE[footer-include](../includes/footer-banner.md)]