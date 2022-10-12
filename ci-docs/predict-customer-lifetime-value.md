---
title: Iragarri bezeroaren bizi-iraupena (CLV)
description: Aurreikusi etorkizunean bezero aktiboen diru-sarrerak.
ms.date: 09/30/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: wameng
manager: shellyha
searchScope:
- ci-predictions
- ci-create-prediction
- ci-custom-models
- customerInsights
ms.openlocfilehash: f27462ac327027e50e23387ac9f75a671db9a86d
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610359"
---
# <a name="predict-customer-lifetime-value-clv"></a>Iragarri bezeroaren bizi-iraupena (CLV)

Aurreikusi bezero aktibo partikularrek zure negozioari ekarriko dioten balizko balioa (diru-sarrerak) etorkizunean zehaztutako denbora-tarte batean. Iragarpen honek laguntzen dizu:

- Identifikatu balio handiko bezeroak eta prozesatu informazio hori.
- Sortu bezero-segmentu estrategikoak beren balio potentzialaren arabera kanpaina pertsonalizatuak egiteko, salmenta, marketina eta laguntza-esfortzuak zuzenduta.
- Gidatu produktuaren garapena bezeroaren balioa handitzen duten ezaugarrietan arreta jarriz.
- Optimizatu salmenta- edo marketin-estrategia eta esleitu aurrekontua zehatzago bezeroei helarazteko.
- Balio handiko bezeroak aintzat hartu eta saritu leialtasun- edo sari-programen bidez.

Zehaztu zer esan nahi duen CLV zure negoziorako. Transakzioetan oinarritutako CLV iragarpen onartzen dugu. Bezero baten aurreikusitako balioa negozio-transakzioen historian oinarritzen da. Demagun hainbat eredu sortzea sarrera-hobespen ezberdinekin eta alderatu ereduaren emaitzak zure negozioaren beharretara hobekien egokitzen den eredua ikusteko.

> [!TIP]
> Probatu CLV iragarpen lagin-datuak erabiliz: [Bezeroaren bizitzako balioa (CLV) iragarpen adibide-gida](sample-guide-predict-clv.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzailea](permissions.md) baimenak
- Gutxienez 100 bezero bakar, ahal izanez gero 10.000 bezero baino gehiago
- Bezeroaren identifikatzailea, transakzioak bezero indibidual batekin lotzeko identifikatzaile bakarra
- Gutxienez urtebeteko transakzioen historia, ahal dela bi edo hiru urte. Egokiena, gutxienez bizpahiru transakzio bezeroaren ID bakoitzeko, hobe da hainbat datatan zehar. Transakzioen historiak honako hauek izan behar ditu:
  - **Transakzioaren IDa**: transakzio bakoitzaren identifikatzaile esklusiboa
  - **Transakzio data** : transakzio bakoitzaren data edo ordua
  - **Transakzioaren zenbatekoa**: transakzio bakoitzaren diru-balioa (adibidez, diru-sarrera edo irabazien marjina)
  - **Itzulketei esleitutako etiketa** : balio boolearra egia/faltsua, transakzioa itzulera den ala ez adierazten duena
  - **Produktuaren IDa** : transakzioan parte hartzen duen produktuaren IDa
- Bezeroaren jarduerei buruzko datuak:
  - **Lehen gakoa** : jarduera baten identifikatzaile bakarra
  - **Denbora-zigilua** : Lehen gakoaren bidez identifikatutako gertaeraren data eta ordua
  - **Gertaera (jardueraren izena)** : Erabili nahi duzun gertaeraren izena
  - **Xehetasunak (zenbatekoa edo balioa)**: bezeroaren jarduerari buruzko xehetasunak
- Datu gehigarriak, hala nola:
  - Web-jarduerak: Webgunearen bisitaren historia edo posta elektronikoaren historia
  - Leialtasun-jarduerak: Leialtasun-sari puntuen metaketa eta erreskate-historia
  - Bezeroarentzako arreta-zerbitzu erregistroa: zerbitzu-deiak, kexak edo itzulketen historia
  - Bezeroaren profilaren informazioa
- Beharrezko eremuetan % 20 baino gutxiago falta dira balioak

> [!NOTE]
> Transakzioen historiako entitate bakarra konfigura daiteke. Erosketa edo transakzio entitate anitz badaude, konbinatu Power Query datuak sartu aurretik.

## <a name="create-a-customer-lifetime-value-prediction"></a>Sortu bezeroaren bizi-iraupenaren balioaren iragarpena

Hautatu **Gorde zirriborroa** edozein unetan iragarpen zirriborro gisa gordetzeko. Iragarpen zirriborroa atalean bistaratzen da **Nire iragarpenak** fitxa.

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Bezeroaren bizitzako balioa** teila.

1. Hautatu **Hasi erabiltzen**.

1. **Eman izena eredu honi** eta **Irteerako entitatearen izenari** beste eredu edo entitate batzuetatik bereizteko.

1. Hautatu **Hurrengoa**.

### <a name="define-model-preferences"></a>Zehaztu ereduaren hobespenak

1. Ezarri **Iragarpen denbora-tartea** etorkizunean CLV-a noraino iragarri nahi duzun definitzeko. Lehenespenez, unitatea hilabete gisa ezartzen da.

   > [!TIP]
   > Ezarritako denbora-tarterako CLV zehatz-mehatz aurreikusteko, datu historikoen aldi konparagarria behar da. Adibidez, hurrengo 12 hilabeteetarako CLV aurreikusi nahi baduzu, izan gutxienez 18-24 hilabeteko datu historikoak.

1. Ezarri bezeroak aktibo jotzeko gutxienez transakzio bat izan behar duen denbora-tartea. Ereduak CLV-rako soilik aurreikusten du **Bezero aktiboak**.
   - **Utzi ereduak erosketa tartea kalkulatzea (gomendatua)** : Modeloak zure datuak aztertzen ditu eta denbora-tarte bat zehazten du erosketa historikoetan oinarrituta.
   - **Ezarri tartea eskuz** : Bezero aktiboa definitzeko denbora-tartea.

1. Definitu pertzentilaren **Balio handiko bezeroa**.
    - **Ereduaren kalkulua (gomendatua)** : Ereduak 80/20 araua erabiltzen du. Garai historikoan zure negozioak % 80 diru-sarrera metatuak lortu zituen bezeroen ehunekoa balio handiko bezeroentzat hartzen da. Normalean, % 30-40 bezero baino gutxiagok % 80 diru-sarrera metatuak lortzen dituzte. Hala ere, zenbaki hori zure negozioaren eta industriaren arabera alda daiteke.
    - **Bezero aktibo nagusien ehunekoa** : pertzentila espezifikoa balio handiko bezero batentzat. Adibidez, sartu **25** balio handiko bezeroak etorkizuneko bezero ordaintzaileen %25 nagusi gisa definitzea.

    Zure negozioak balio handiko bezeroak beste modu batean definitzen baditu, [aditzera eman nahiko genukeen bezala](https://go.microsoft.com/fwlink/?linkid=2074172).

1. Hautatu **Hurrengoa**.

### <a name="add-required-data"></a>Gehitu beharrezko datuak

1. Hautatu **Gehitu datuak** rentzat **Bezeroaren transakzioen historia**.

1. Hautatu jarduera semantiko mota, **Salmenta Eskaera** edo **SalesOrderLine**, transakzioen historia jasotzen duena. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak semantikoki mapatu baziren, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Mapa semantikoa gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.
  
   :::image type="content" source="media/CLV-add-required.PNG" alt-text="Gehitu CLV eredurako beharrezko datuak":::

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Gehitu jarduera gehiago edo hautatu **Hurrengoa**.

### <a name="add-optional-activity-data"></a>Gehitu aukerako jarduera-datuak

Bezeroen interakzio nagusiak islatzen dituzten datuek (adibidez, webgunea, bezeroarentzako arreta-zerbitzu eta gertaeren erregistroak) testuingurua gehitzen dute transakzio erregistroetan. Zure bezeroen jardueren datuetan aurkitutako eredu gehiagok aurreikuspenen zehaztasuna hobe dezakete.

1. Hautatu **Gehitu datuak** azpian **Hobetu ereduaren estatistikak jarduera-datu gehigarriekin**.

1. Aukeratu gehitzen ari zaren bezeroaren jarduera motarekin bat datorren jarduera mota. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak mapatu bazituzten, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Kartografiarik gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Hautatu **Hurrengoa**.

1. [Gehitu aukerako bezeroen datuak](#add-optional-customer-data) edo hautatu **Hurrengoa** eta joan [Ezarri eguneratze-egutegia](#set-update-schedule).

### <a name="add-optional-customer-data"></a>Gehitu aukerako bezeroen datuak

Hautatu normalean erabiltzen diren bezeroen profilaren 18 atributuren artean, ereduan sarrera gisa sartzeko. Atributu hauek eredu-emaitza pertsonalizatuagoak, garrantzitsuagoak eta ekintzaileagoak lor ditzakete zure negozioaren erabilera-kasuetarako.

Adibidez: Contoso Kafeak bezeroaren bizitzako balioa aurreikusi nahi du balio handiko bezeroei zuzenduta, espreso makina berriaren aurkezpenarekin lotutako eskaintza pertsonalizatu batekin. Contoso-ek CLV eredua erabiltzen du eta bezeroen profilaren 18 atributu guztiak gehitzen ditu euren balio handieneko bezeroetan zein faktorek eragiten duten ikusteko. Bezeroen kokapena bezero horiengan eragin handiena duen faktorea dela ikusten dute.
Informazio horrekin, tokiko ekitaldi bat antolatzen dute espresso-makina abian jartzeko eta bertako saltzaileekin elkartzen dira eskaintza pertsonalizatuetarako eta ekitaldian esperientzia berezi bat izateko. Informazio hori gabe, Contoso-ek baliteke marketin-mezu generikoak soilik bidali eta balio handiko bezeroen tokiko segmentu honetarako pertsonalizatzeko aukera galdu izana.

1. Hautatu **Gehitu datuak** azpian **Are gehiago, are gehiago areagotu ereduaren ezagutza bezeroen datu gehigarriekin**.

1. Izan ere **Entitatea**, aukeratu **Bezeroa: CustomerInsights** bezeroaren atributuen datuekin mapatzen den bezero profil bateratua hautatzeko. Izan ere **Bezeroaren IDa**, aukeratu **System.Customer.CustomerId**.

1. Mapeatu eremu gehiago datuak zure bezeroen profil bateratuetan eskuragarri baldin badaude.

   :::image type="content" source="media/clv-optional-customer-profile-mapping.png" alt-text="Bezeroen profilaren datuetarako mapatutako eremuen adibidea.":::

1. Sakatu **Gorde**.

1. Hautatu **Hurrengoa**.

### <a name="set-update-schedule"></a>Konfiguratu antolaketaren eguneratzea

1. Aukeratu azken datuetan oinarrituta zure eredua berriro trebatzeko maiztasuna. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, Customer Insights-en datu berriak sartzen diren heinean. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.

### <a name="review-and-run-the-model-configuration"></a>Berrikusi eta exekutatu modeloaren konfigurazioa

The **Berrikusi eta exekutatu** urratsak konfigurazioaren laburpena erakusten du eta iragarpen sortu aurretik aldaketak egiteko aukera ematen du.

1. Hautatu **Editatu** aldaketak berrikusteko eta egiteko edozein urratsetan.

1. Zure hautapenekin pozik bazaude, hautatu **Gorde eta exekutatu** eredua exekutatzen hasteko. Hautatu **Eginda**. The **Nire iragarpenak** fitxa bistaratzen da iragarpen sortzen ari den bitartean. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

[!INCLUDE [progress-details](includes/progress-details-pane.md)]

## <a name="view-prediction-results"></a>Ikusi iragarpen emaitzak

1. Joan **Adimena** > **Iragarpenak**.

1. urtean **Nire iragarpenak** fitxan, hautatu ikusi nahi duzun iragarpen.

Emaitza orrialdearen barruan hiru datu nagusi daude.

- **Prestakuntza ereduaren errendimendua** : A, B edo C kalifikazioek iragarpen-en errendimendua adierazten dute eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia hartzen lagun zaitzake.
  
  :::image type="content" source="media/clv-model-score.png" alt-text="Ereduaren puntuazioaren informazio koadroaren irudia A kalifikazioarekin.":::

  Customer Insights-ek balio handiko bezeroen iragarpenean AI ereduak nola jokatu duen ebaluatzen du oinarrizko eredu batekin alderatuta.

  Kalifikazioak arau hauetan oinarrituta zehazten dira:
  - **A** ereduak zehaztasunez aurreikusi zuen gutxienez % 5eko balio handiko bezero gehiago oinarrizko ereduarekin alderatuta.
  - **B** ereduak zehaztasunez aurreikusi zuen gutxienez % 0-5 balio handiko bezero gehiago oinarrizko ereduarekin alderatuta.
  - **C** ereduak zehaztasunez aurreikusi zuen balio handiko bezero gutxiago oinarrizko ereduarekin alderatuta.
  
  Hautatu [**Ikasi puntuazio honi buruz**](#learn-about-the-score) irekitzeko **Ereduaren balorazioa** AI ereduaren errendimenduari eta oinarrizko ereduari buruzko xehetasun gehiago erakusten dituen panela. Hobeto ulertzen lagunduko dizu ereduaren errendimendu-neurriak eta azken ereduaren errendimendu-kalifikazioa nola atera den. Oinarrizko ereduak AI ez oinarritutako ikuspegia erabiltzen du bezeroek bizitzako balioa kalkulatzeko batez ere bezeroek egindako erosketa historikoetan oinarrituta.

- **Bezeroen balioa pertzentilaren arabera** : Balio baxuko eta balio handiko bezeroek taula batean bistaratzen dituzte. Pasa zaitez histogramako barren gainetik talde bakoitzeko bezero kopurua eta talde horren batez besteko CLV ikusteko. Aukeran, [bezeroen segmentuak sortu](prediction-based-segment.md) beren CLV iragarpenetan oinarrituta.
  
   :::image type="content" source="media/CLV-value-percent.png" alt-text="Bezeroen balioa pertzentilaren arabera CLV eredurako":::

- **Eragin gehien duten faktoreak**: hainbat faktore hartzen dira kontuan zure CLV iragarpen sortzerakoan adimen artifizialeko ereduan emandako sarrera datuetan oinarrituta. Faktore bakoitzak eredu batek sortzen dituen aurreikuspen agregatuetarako kalkulatutako garrantzia du. Erabili faktore hauek zure iragarpen emaitzak balioztatzeko. Faktore horiek CLV zure bezero guztien artean aurreikusteko eragin duten faktore eragileei buruzko informazio gehiago eskaintzen dute.
  
   :::image type="content" source="media/CLV-influence-factors.png" alt-text="CLV ereduan eragin handiena duten faktoreak":::

### <a name="learn-about-the-score"></a>Ikasi puntuazioari buruz

Oinarrizko ereduaren arabera CLV kalkulatzeko erabilitako formula estandarra:

 _**CLV bezero bakoitzarentzat** = Bezeroak bezero aktiboaren leihoan egindako hileroko batez besteko erosketa * CLV iragarpen aldiko hilabete kopurua * Bezero guztien atxikipen-tasa orokorra_

Adimen artifizialeko eredua oinarrizko ereduarekin alderatzen da, bi modeloen errendimendu metrikan oinarrituta.
  
- **Balio handiko bezeroak iragartzeko arrakasta-tasa**

  Ikusi aldea adimen artifizialeko eredua erabiliz balio handiko bezeroak iragartzeko oinarrizko ereduarekin alderatuta. Adibidez, % 84 arrakasta-tasak esan nahi du prestakuntzako datuetan balio handiko bezero guztien artean adimen artifizialeko ereduak % 84 zehazki harrapatu zuela. Ondoren, arrakasta-tasa hau oinarrizko ereduaren arrakasta-tasarekin alderatzen dugu, aldaketa erlatiboa jakinarazteko. Balio hau ereduari kalifikazio bat emateko erabiltzen da.

- **Erroreen metrikak**

  Ikusi ereduaren errendimendu orokorra etorkizuneko balioak aurreikusteko erroreari dagokionez. Errore batez besteko akats karratuaren (RMSE) metrika orokorra erabiltzen dugu errore hori ebaluatzeko. RMSE datu kuantitatiboak iragartzeko eredu baten errorea neurtzeko modu estandarra da. Adimen artifizialeko ereduaren RMSE oinarrizko ereduaren RMSEarekin alderatzen da eta desberdintasun erlatiboa jakinarazi da.

Adimen artifizialeko ereduak bezeroen sailkapen zehatza lehenesten du zure negozioari ematen dioten balioaren arabera. Beraz, balio handiko bezeroak iragartzeko arrakasta-tasa soilik erabiltzen da azken ereduaren nota lortzeko. RMSE metrika balio arruntetarako sentikorra da. Erosketa balio izugarri altuak dituzten bezeroen ehuneko txikia duzun eszenatokietan, baliteke RMSE metrikak modeloaren errendimenduaren argazki osoa ez ematea.

[!INCLUDE [footer-include](includes/footer-banner.md)]
