---
title: Produktuen gomendioen iragarpena
description: Aurreikusi litekeena dela bezeroak eros ditzakeen produktuak edo haiekin elkarreragitea.
ms.date: 03/17/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: 01704f78cfe1f6ceeee19ff825fc65150894d4ed
ms.sourcegitcommit: 6b07c9c3102761be162e4842f3c9fbc19f948a9b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "6095541"
---
# <a name="product-recommendation-prediction-preview"></a>Produktu-gomendioen iragarpena (aurreargitalpena)

Produktuen gomendio ereduak produktu iragarleentzako gomendio multzoak sortzen ditu. Gomendioak aurreko erosketa portaeran eta antzeko erosketa ereduak dituzten bezeroetan oinarritzen dira. Produktu gomendioen iragarpen berriak sor ditzakezu **Adimena** > **Iragarpenak** orrialdea. Aukeratu **Nire iragarpenak** sortu dituzun beste iragarpen batzuk ikusteko.

Produktuen gomendioak tokiko lege eta araudien eta bezeroen itxaropenen mende egon daitezke, eredua bereziki kontuan hartzeko diseinatuta ez dagoena.  Aurreikuspen gaitasun honen erabiltzaile gisa, **gomendioak berrikusi behar dituzu zure bezeroei entregatu aurretik** aplika daitezkeen lege edo arauak eta bezeroen itxaropenak gomendatzen dituzunaren arabera betetzen dituzula ziurtatzeko. 

Gainera, modelo honen irteerak produktuaren IDan oinarritutako gomendioak emango dizkizu. Bidalketa-mekanismoak aurreikusitako produktuaren IDak mapatu beharko ditu zure bezeroek eduki egokia izan dezaten, lokalizazioa, irudiaren edukia eta negozioaren inguruko bestelako edukia edo portaera kontuan izan dezaten.

## <a name="sample-guide"></a>Lagin-gida

Ezaugarri hau probatzea interesatzen bazaizu baina beheko baldintzak betetzeko datuak ez badituzu, [lagin inplementazio bat sortu](sample-guide-predict-product-recommendation.md) dezakezu.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.

- Negozioaren ezagutza zure negozioarentzako produktu mota desberdinak ulertzeko eta zure bezeroek haiekin nola elkarreragiten duten jakiteko. Zure bezeroek aurretik erositako produktuak gomendatzea edo produktu berrietarako gomendioak onartzen ditugu.

- Zure transakzio eta erosketen inguruko datuak eta horien historia:
    - Erosketak edo transakzioak bereizteko transakzio identifikatzaileak.
    - Bezeroen identifikadoreak, transakzioak zure bezeroei esleitzeko.
    - Transakzioen gertaeren datak, transakzioaren datak zehazten dituztenak.
    - Transakzioaren produktuaren IDa.
    - (Aukerakoa) Produktuen katalogoko datuen entitatea produktuen iragazkia erabiltzeko.
    - (Aukerakoa) Transakzio bat itzultze bat den.
    - Datu semantikoen eskemak informazio hau behar du:
        - **Transakzioaren IDa:** Erosketa edo transakzio baten identifikatzaile bakarra.
        - **Transakzioaren data:** Erosketaren edo transakzioaren data.
        - **Transakzioaren balioa:** transakzioaren edo elementuaren zenbakizko balioa.
        - **Produktuaren ID esklusiboa:** erositako produktuaren edo zerbitzuaren IDa, zure datuak lerro-elementuaren mailan badaude.
        - (Aukerakoa) **Erosi edo itzuli:** Balioa duen eremu boolearra *egia* transakzio bat itzulketa izan zela identifikatzen du. Erosketa edo Itzulketa datuak ematen ez badira eredua eta **Transakzioaren balioa** negatiboa da, informazio hau itzulera bat ondorioztatzeko ere erabiliko dugu.
- Iradokitako datuen ezaugarriak:
    - Datu historiko nahikoak: gutxienez urtebeteko datu transakzionalak, ahal izanez gero, bizpahiru urte, urtaroak sartzeko.
    - Erosketa anitz bezero bakoitzeko: hiru transakzio edo gehiago Bezeroaren ID bakoitzeko
    - Bezero kopurua: gutxienez 100 bezero, ahal dela 10.000 bezero baino gehiago. Ereduak huts egingo du 100 bezero baino gutxiagorekin.

> [!NOTE]
> - Ereduak zure bezeroen transakzioen historia eskatzen du. Transakzio baten definizioa nahiko malgua da. Erabiltzaile-produktu elkarreragina deskribatzen duten datu guztiek sarrera gisa funtziona dezakete. Adibidez, produktu bat erostea, klasea hartzea edo ekitaldi batera joatea.
> - Une honetan transakzioen historiako entitate bakarra konfigura daiteke. Erosketa entitate bat baino gehiago badaude, elkartu Power Query-en datuak kontsumitu aurretik.
> - Ordena eta eskaeraren xehetasunak entitate desberdinak badira, batu haiekin ereduan erabili aurretik. Ereduak ez du entitate bateko eskaera IDarekin edo ordainagiriaren IDarekin soilik funtzionatzen.


## <a name="create-a-product-recommendation-prediction"></a>Sortu produktuak gomendatzeko iragarpena

1. Customer Insights atalean, joan **Inteligentzia** > **Iragarpenak**.

1. Aukeratu **Produktuen gomendioen eredua (aurrebista)** lauza eta hautatu **Erabili eredu hau**.
   > [!div class="mx-imgBorder"]
   > ![Produktuen gomendioaren ereduaren lauza Erabili eredu botoiarekin](media/product-recommendation-usethismodel.PNG "Produktuen gomendioaren ereduaren lauza Erabili eredu botoiarekin")

1. Berrikusi ereduaren eskakizunei buruzko informazioa. Beharrezko datuak badituzu, hautatu **Hasi erabiltzen**.

### <a name="name-model"></a>Ezarri izena ereduari

1. Eman ereduari ereduari beste ereduak bereizteko.

1. Idatzi irteerako entitatearen izen bat letrak eta zenbakiak soilik erabiliz, zuriunerik gabe. Horixe da eredu erakundeak erabiliko duen izena. Ondoren, hautatu **Hurrengoa**.

### <a name="define-product-recommendation-configuration"></a>Definitu produktuaren gomendioen konfigurazioa

1. Ezarri **Produktu kopurua** bezero bati gomendatu nahi diozu. Balio hori zure bidalketa metodoak datuak nola betetzen dituen araberakoa da. Hiru produktu gomendatzen badituzu, ezarri balio hori horren arabera.
   
   >[!TIP]
   > Aukeratu dezakezu **Gorde eta itxi** edozein unetan aurreikuspena zirriborro gisa gordetzeko. Iragarpen zirriborroa hemen aurkituko duzu **Nire iragarpenak** fitxa.

1. Aukeratu **Bezeroek berriki erosi dituzten produktuak iradoki** nahi dituzun.

1. *Ez* aukeratu baduzu, gomendatu duela gutxi erositako produktuak, ezarri **Atzera begiratu leihoa**. Ezarpen honek produktuak erabiltzaileari berriro gomendatu aurretik ereduak kontuan hartzen duen denbora-tartea zehazten du. Adibidez, adierazi bezero batek bi urtean behin ordenagailu eramangarri bat erosten duela. Leiho honetan azken bi urteetako erosketa historia ikusiko da, eta elementuren bat aurkitzen badute, elementua gomendioetatik iragazi egingo da.

1. Hautatu **Hurrengoa**

### <a name="add-required-data"></a>Gehitu beharrezko datuak

1. Aukeratu **Gehitu datuak** **Bezeroen transakzio-historia** atalean eta aukeratu transakzioen / erosketen historiari buruzko informazioa ematen duen entitatea, [aurrebaldintzak](#prerequisites) atalean deskribatu moduan.

1. Esleitu eremu semantikoak erosketa-historiako entitateko atributuetara eta hautatu **Hurrengoa**. Eremuen deskribapenak eskuratzeko, begiratu [ezinbesteko baldintza](#prerequisites).
   > [!div class="mx-imgBorder"]
   > ![Definitu entitate-harremana](media/product-recommendation-purchasehistorymapping.PNG "Erosketa-historia orria hautatutako erosketa historia entitateko esleitutako atributu semantikoak erakusten ditu")

1. Eremuak betetzen ez badira, konfiguratu erosketa-historiaren entitatea *Bezeroaren* entitatean.
    1. Hautatu **Erosketa-historiaren entitatea**.
    1. Aukeratu erosketa-historiaren entitatean bezeroa identifikatzen duen **Eremua**. Zure *Bezeroaren* entitatearen bezeroaren ID nagusiarekin erlazionatu behar da.
    1. Hautatu botoia **Bezero entitatea** bat datorrena zure lehen bezero-entitatearekin.
    1. Idatzi izena deskribatzen duena harremana.
       > [!div class="mx-imgBorder"]
       > ![Bezeroarekiko harremana sortu dela erakusten duen erosketa-historiaren orria](media/model-purchase-join.png "Bezeroarekiko harremana sortu dela erakusten duen erosketa-historiaren orria")

1. Sakatu **Gorde**.

1. Hautatu **Hurrengoa**.

### <a name="configure-product-filters"></a>Konfiguratu produktu-iragazkiak

Batzuetan, produktu batzuk bakarrik dira onuragarriak edo egokiak eraikitzen duzun iragarpen motarako. Produktuen iragazkiek bezeroei gomendatzeko ezaugarri zehatzak dituzten produktuen azpimultzoa identifikatzen uzten dizute. Ereduak ereduak ikasteko erabilgarri dauden produktu guztiak erabiliko ditu, baina produktuaren iragazkiarekin bat datozen produktuak soilik erabiliko ditu bere irteeran.

1. Hurrengoan **Gehitu produktuaren informazioa** urratsa, gehitu zure produktuen katalogoa produktu bakoitzari buruzko informazioarekin. Mapan hautatu behar den informazioa **Hurrengoa**.

3. Hurrengoan **Produktuen iragazkiak** urratsa, aukeratu aukera hauen artean.

   * **Ez dago iragazkirik**: Erabili produktu guztiak iragarpen gomendioan.

   * **Produktu iragazki zehatzak zehaztu**: Erabili produktu zehatzak produktuaren gomendioan iragarpen.

1. Hautatu **Hurrengoa**.

1. Produktuen iragazkia definitzea aukeratzen baduzu, orain definitu behar duzu. Hurrengoan **Produktuen katalogoaren atributuak** panelean, hautatu atributuak zure *Produktuen Katalogoaren entitatea* iragazkian sartu nahi duzula.

   :::image type="content" source="media/product-filters-sidepane.png" alt-text="Produktuen katalogoaren entitatean egotzitako alboko panela, produktuen iragazkiak hautatzeko.":::

1. Aukeratu produktuaren iragazkia erabiltzea nahi duzun **eta** edo **edo** konektoreak produktuaren katalogoko atributuen hautaketa logikoki konbinatzeko.
   
   :::image type="content" source="media/product-filters-sample.png" alt-text="Produktuen iragazkien laginaren konfigurazioa AND konektoreak logikoekin konbinatuta.":::

1. Hautatu **Hurrengoa**.

### <a name="set-update-schedule-and-review-configuration"></a>Ezarri eguneratze egutegia eta berrikusi konfigurazioa

1. Ezarri maiztasuna zure eredua berriro sartzeko. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, datu berriak Customer Insights-era inportatzen direnez. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.

1. Berrikusi konfigurazioa. Aurreikuspen konfigurazioaren edozein ataletara joan zaitezke hautatuta **Editatu** erakutsitako balioaren azpian. Edo konfigurazio urratsa hauta dezakezu aurrerapen adierazlean.

1. Balio guztiak behar bezala konfiguratuta badaude, hautatu **Gorde eta exekutatu** iragarpen prozesua hasteko. Gainean **Nire iragarpenak** fitxan, zure iragarpenen egoera ikus dezakezu. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

## <a name="review-a-prediction-status-and-results"></a>Iragarpen iragarpen egoera eta emaitzak berrikustea

1. Joan **Nire iragarpenak** fitxan **Adimen** > **iragarpenak**.
   > [!div class="mx-imgBorder"]
   > ![Nire iragarpenak orriaren ikuspegia](media/product-recommendation-mypredictions.PNG "Nire iragarpenak orriaren ikuspegia")

1. Hautatu berrikusi nahi duzun iragarpena.
   - **Iragarpen izena:** Sortzerakoan emandako iragarpenaren izena.
   - **Iragarpen mota:** Iragarpenak egiteko erabilitako eredu mota
   - **Irteerako entitatea:** Iragarpenaren irteera gordetzeko entitatearen izena. Izen hori duen entitate bat aurki dezakezu **Datuak** > **erakundeak**.    
      *Puntuazioa* irteerako entitatean gomendioaren neurri kuantitatiboa da. Ereduak puntuazio altuagoa duten produktuak gomendatzen ditu puntuazio txikiagoa duten produktuen aldean.
   - **Aurreikusitako eremua:** Eremu hau iragarpen mota batzuetarako bakarrik betetzen da eta ez da erabiltzen Produktuen gomendioan iragarpen.
   - **Egoera:** Iragarpenaren exekutatutako egoera.
        - **ilaran:** Aurreikuspena beste prozesu batzuen zain egongo da.
        - **freskatzen:** Aurreikuspenak une honetan "puntuazio" prozesatzen ari da irteera entitatean sartuko diren emaitzak sortzeko.
        - **Huts:** iragarpenak huts egin du. Aukeratu **Erregistroak** xehetasun gehiagorako.
        - **Ondorengoa:** iragarpenak arrakasta izan du. Aukeratu **ikusi** elipse bertikalen azpian iragarpena berrikusteko
   - **Hizkuntzak:** Aurreikuspenerako konfigurazioa aldatu zen data.
   - **Azken freskatua:** Iragarpena freskatu den data irteerako entitatean.

1. Hautatu elipse bertikalak emaitzak berrikusteko nahi duzun iragarpenaren ondoan **ikusi**.
   > [!div class="mx-imgBorder"]
   > ![Aurreikuspen bat egiteko, editatu, freskatu, ikusi, erregistroak eta ezabatu behar diren iragarpenak egiteko iragarki baterako aukerak](media/product-recommendation-verticalellipses.PNG "Aurreikuspen bat egiteko, editatu, freskatu, ikusi, erregistroak eta ezabatu behar diren iragarpenak egiteko iragarki baterako aukerak")

1. Emaitzen orrian barruan bost datu atal nagusi daude:
    1. **Prestakuntza ereduaren errendimendua:** A, B edo C puntuazio posibleak dira. Puntuazio honek iragarpenaren errendimendua adierazten du eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia har dezake.
        - Puntuazioak honako arauen arabera zehazten dira:
            - **A** eredua kontuan hartuko da **A** motako kalitatea "Arrakasta @ K" metrika oinarrizko lerroan gutxienez % 10 bada. 
            - **B** eredua kontuan hartuko da **B** motako kalitatea "Arrakasta @ K" metrika oinarrizko lerroan gutxienez % 0-10 bada.
            - **C** eredua kontuan hartuko da **C** motako kalitatea "Arrakasta @ K" metrika oinarrizko lerroan baino gutxiago bada.
               
               > [!div class="mx-imgBorder"]
               > ![Ereduaren errendimenduaren emaitza ikusi](media/product-recommendation-modelperformance.PNG "Ereduaren errendimenduaren emaitza ikusi")
            - **Oinarria**: ereduak bezero guztien artean erosketa kopuruaren arabera gomendatzen diren produktu onenak hartzen ditu eta ereduak identifikatutako ikasitako arauak erabiltzen ditu bezeroentzako gomendio multzo bat sortzeko. Iragarpenak goiko produktuekin alderatzen dira, produktua erosi zuten bezero kopuruaren arabera kalkulatuta. Bezero batek gutxienez erositako produktuetan ere ikusi den produktu bat gutxienez gomendatutako produktuetan baldin badu, oinarrizko oinarritzat hartzen da. 100 bezeroen artean produktu gomendatua erosi duten 10 bezero horien artean, oinarrizko % 10 izango litzateke.
            - **Arrakasta @ K**: transakzioen balidazio multzoa erabiliz, gomendioak sortzen dira bezero guztientzat eta transakzioen balidazio multzoarekin alderatzen dira. Adibidez, 12 hilabeteko epean, 12. hilabetea datuen balidazio multzo gisa alboratu daiteke. Ereduak gutxienez 12. hilean erosiko zenukeen gauza bat iragartzen badu aurreko 11 hilabeteetan ikasitakoaren arabera, bezeroak "Arrakasta @ K" metrika handituko luke.
    
    1. **Iradokitako produktu gehienak (kalkuluarekin):** Zure bezeroentzat aurreikusitako lehen bost produktuak.
       > [!div class="mx-imgBorder"]
       > ![Gomendatutako 5 produktu onenak erakusten dituen grafikoa](media/product-recommendation-topproducts.PNG "Gomendatutako 5 produktu onenak erakusten dituen grafikoa")
    
    1. **Gomendio faktore nagusiak:** Ereduak bezeroen transakzioen historia erabiltzen du produktuen gomendioak emateko. Iraganeko erosketetan oinarritutako ereduak ikasten ditu eta bezeroen eta produktuen arteko antzekotasunak aurkitzen ditu. Antzekotasun horiek produktuen gomendioak sortzeko erabiltzen dira.
    Jarraian, ereduak sortutako produktuaren gomendioan eragina izan dezaketen faktoreak daude. 
        - **Iraganeko transakzioak**: Iraganeko erosketa ereduak modeloak erabiltzen zituen produktuen gomendioak sortzeko. Adibidez, ereduak a gomendatu dezake _Azaleko arku sagua_ duela gutxi norbaitek erosi badu _3. azaleko liburua_ eta _Azaleko boligrafoa_. Ereduak jakin zuen historikoki bezero askok erosi zutela _Azaleko arku sagua_ erosi ondoren _3. azaleko liburua_ eta _Azaleko boligrafoa_.
        - **Bezeroen antzekotasuna**: Gomendatutako produktu bat antzeko erosketa ereduak erakusten dituzten beste bezero batzuek erosi zuten historikoki. Adibidez, John gomendatu zuten _Azaleko entzungailuak 2_ izan ere, duela gutxi Jennifer eta Bradek erosi dute _Azaleko entzungailuak 2_. Ereduak uste du John Jennifer eta Braden antzekoa dela historikoki erosketa eredu antzekoak izan dituztelako.
        - **Produktuaren antzekotasuna**: Gomendatutako produktu bat bezeroak aurretik erositako beste produktu batzuen antzekoa da. Ereduak bi produktu antzekoak direla uste du elkarrekin edo antzeko bezeroek erosi badituzte. Adibidez, norbaitek gomendio bat jasotzen du _USB biltegiratze unitatea_ aurretik erosi dutelako _USB-C-tik USB egokitzailea_ eta ereduak hori uste du _USB biltegiratze unitatea_ antzekoa da _USB-C-tik USB egokitzailea_ erosketa eredu historikoetan oinarrituta.

        Produktuen gomendio guztietan faktore horietako batek edo gehiagok eragiten dute. Eragindako faktore bakoitzak rol bat izan duen gomendioen ehunekoa taula batean ikus daiteke. Hurrengo adibidean, gomendioen % 100ek iraganeko transakzioen eragina izan zuten, % 60ek bezeroen antzekotasunaren eta % 22 produktuaren antzekotasunaren arabera. Pasa zaitez diagramako barren gainean eragin faktoreek zer portzentaia izan duten jakiteko.

        > [!div class="mx-imgBorder"]
        > ![Gomendioen faktore gakoak](media/product-recommendation-keyrecommendationfactors.png "Ereduak produktuaren gomendioak sortzeko ikasitako funtsezko gomendio faktoreak")
       
     
   1. **Datuen estatistikak**: Kontuan hartu den ereduaren transakzioen, bezeroen eta produktuen kopuruaren ikuspegi orokorra ematen du. Ereduak ikasteko eta produktuen gomendioak sortzeko erabili ziren sarrerako datuetan oinarritzen da.

      > [!div class="mx-imgBorder"]
      > ![Datuen estatistikak](media/product-recommendation-datastatistics.png "Ereduak ikasteko ereduak erabilitako datuen inguruko datuen estatistikak")

      Atal honetan ereduak ereduak ikasteko eta produktuen gomendioak sortzeko ereduak erabili zituen datu puntuen inguruko estatistikak erakusten dira. Iragazkia, modeloaren konfigurazioan konfiguratuta dagoen moduan, modeloak sortutako irteeran aplikatuko da. Hala ere, ereduak eskura dauden datu guztiak erabiltzen ditu ereduak ikasteko. Hori dela eta, modeloaren konfigurazioan produktuen iragazkia erabiltzen baduzu, atal honetan ereduak ereduak ikasteko aztertu dituen produktuen kopurua erakutsiko da, definitutako iragazki-irizpideekin bat datozen produktuen kopuruarekin alderatuta.

   1. **Konfiantza handiko produktuen gomendioak:** ereduak bezeroak eros ditzakeela uste duten bezeroei emandako gomendioen lagina.    
      Produktuen katalogoa gehitzen bada, produktuen IDak produktuen izenekin ordezkatuko dira. Produktuen izenek iragarpenen inguruko informazio erabilgarriagoa eta intuitiboagoa eskaintzen dute.
       > [!div class="mx-imgBorder"]
       > ![Bezero partikular batzuentzako konfiantza handiko iradokizunak erakusten dituen zerrenda](media/product-recommendation-highconfidence.PNG "Bezero partikular batzuentzako konfiantza handiko iradokizunak erakusten dituen zerrenda")

## <a name="manage-predictions"></a>Iragarpenak kudeatu

Iragarpenak optimizatzea, konpontzea, freskatzea edo ezabatzea posible da. Berrikusi sarrerako datuen erabilgarritasun txostena iragarpen azkarragoa eta fidagarriagoa nola egin jakiteko. Informazio gehiago lortzeko, ikusi [Kudeatu iragarpenak](manage-predictions.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
