---
title: Transakzio txanda iragarpen (bideoa dauka)
description: Iragarri bezeroren bat arriskuan dagoen jada produktu eta zerbitzuak erosten ez dituelako.
ms.date: 01/13/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: e55ca8c6926fa0bda05aaf52fd799ca25f7f585f
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642188"
---
# <a name="transaction-churn-prediction"></a>Transakzio churn iragarpena

Transakzioen galera-tasaren iragarpenak bezeroak denbora-tarte jakin batean jada zure produktuak edo zerbitzuak erosiko ote dituen iragartzen laguntzen du. Galera-tasaren iragarpen berriak sor ditzakezu **Adimena** > **Iragarpenak** atalean. Aukeratu **Nire iragarpenak** sortu dituzun beste iragarpen batzuk ikusteko. 

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWN6Eg]

Negozio kontuetan oinarritutako inguruneetarako, kontu baten transazio transaktiboa aurreikus dezakegu, baita kontuaren konbinazioa eta produktuen kategoria bezalako beste informazio maila ere. Dimentsio bat gehituz gero, "Contoso" kontuak "bulegoko papergintza" produktuaren kategoria erosteari utziko dion jakin daiteke. Gainera, negozio kontuetarako, AI ere erabil dezakegu kontu bat bigarren mailako informazio kategoria bat lortzeko litekeena den arrazoien zerrenda sortzeko.

> [!TIP]
> Saiatu iragarpen transakzioen txandarako tutoriala adibide-datuak erabiliz: [Transaction churn iragarpen adibide-gida](sample-guide-predict-transactional-churn.md).

## <a name="prerequisites"></a>Aurrebaldintzak

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Enpresa-ezagutzak zer negoziorentzako esan nahi du ulertzeko. Denboran oinarritutako galera-tasen definizioak onartzen ditugu, hau da, erosketarik gabeko tarte baten ondoren bezeroa galdutzat jotzen da.
- Zure transakzio / erosketen inguruko datuak eta horien historia:
    - Erosketak / transakzioak bereizteko transakzio identifikatzaileak.
    - Bezeroen identifikadoreak, transakzioak zure bezeroekin lotzeko.
    - Transakzioen gertaeren datak, transakzioaren datak zehazten dituztenak.
    - Erosketak / transakzioak egiteko datu semantikoen eskemak informazio hau behar du:
        - **Transakzioaren IDa**: Erosketa edo transakzio baten identifikatzaile bakarra.
        - **Transakzioaren data**: Erosketaren edo transakzioaren data.
        - **Transakzioaren balioa**: Transakzioaren / elementuaren moneta / zenbakizko balioa.
        - (Aukerakoa) **Produktuaren ID esklusiboa**: Erositako produktuaren edo zerbitzuaren IDa, zure datuak lerro-elementuaren mailan badaude.
        - (Aukerakoa) **Transakzio hau itzulera izan den ala ez**: Transakzioa itzulera izan den edo ez identifikatzen duen egia / gezurra eremua. **Transakzioaren balioa** negatiboa bada, informazio hau itzulera bat ondorioztatzeko ere erabiliko dugu.
- (Aukerakoa) Bezeroen jarduerei buruzko datuak:
    - Mota bereko jarduerak bereizteko jarduera identifikatzaileak.
    - Bezeroaren identifikadoreak maparen jardueretan zure bezeroentzat.
    - Jardueren izena eta jardueraren data biltzen dituen jarduera.
    - Bezeroen jardueren datu semantikoen eskemak honako hauek ditu:
        - **Gako nagusia:** Jarduera baterako identifikatzaile bakarra. Adibidez, webgunea bisitatzea edo bezeroak zure produktuaren lagin bat probatu duela azaltzen duen erabilera erregistroa.
        - **Timestamp:** Giltza nagusian identifikatutako gertaeraren data eta ordua.
        - **Gertaera:** Erabili nahi duzun gertaeraren izena. Adibidez, janari dendako "UserAction" izeneko eremua bezeroak erabilitako kupoi bat izan daiteke.
        - **Xehetasunak:** Ekitaldiaren inguruko informazio zehatza. Adibidez, janari dendako "CouponValue" izeneko eremua izan daiteke kupoiaren moneta-balioa.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Enpresa-ezagutzak zer negoziorentzako esan nahi du ulertzeko. Denboran oinarritutako galera-tasen definizioak onartzen ditugu, hau da, erosketarik gabeko tarte baten ondoren bezeroa galdutzat jotzen da.
- Zure transakzio / erosketen inguruko datuak eta horien historia:
    - Erosketak / transakzioak bereizteko transakzio identifikatzaileak.
    - Bezeroen identifikadoreak, transakzioak zure bezeroekin lotzeko.
    - Transakzioen gertaeren datak, transakzioaren datak zehazten dituztenak.
    - Erosketak / transakzioak egiteko datu semantikoen eskemak informazio hau behar du:
        - **Transakzioaren IDa**: Erosketa edo transakzio baten identifikatzaile bakarra.
        - **Transakzioaren data**: Erosketaren edo transakzioaren data.
        - **Transakzioaren balioa**: Transakzioaren / elementuaren moneta / zenbakizko balioa.
        - (Aukerakoa) **Produktuaren ID esklusiboa**: Erositako produktuaren edo zerbitzuaren IDa, zure datuak lerro-elementuaren mailan badaude.
        - (Aukerakoa) **Transakzio hau itzulera izan den ala ez**: Transakzioa itzulera izan den edo ez identifikatzen duen egia / gezurra eremua. **Transakzioaren balioa** negatiboa bada, informazio hau itzulera bat ondorioztatzeko ere erabiliko dugu.
- (Aukerakoa) Bezeroen jarduerei buruzko datuak:
    - Mota bereko jarduerak bereizteko jarduera identifikatzaileak.
    - Bezeroaren identifikadoreak maparen jardueretan zure bezeroentzat.
    - Jardueren izena eta jardueraren data biltzen dituen jarduera.
    - Bezeroen jardueren datu semantikoen eskemak honako hauek ditu:
        - **Gako nagusia:** Jarduera baterako identifikatzaile bakarra. Adibidez, webgunea bisitatzea edo bezeroak zure produktuaren lagin bat probatu duela azaltzen duen erabilera erregistroa.
        - **Timestamp:** Giltza nagusian identifikatutako gertaeraren data eta ordua.
        - **Gertaera:** Erabili nahi duzun gertaeraren izena. Adibidez, janari dendako "UserAction" izeneko eremua bezeroak erabilitako kupoi bat izan daiteke.
        - **Xehetasunak:** Ekitaldiaren inguruko informazio zehatza. Adibidez, janari dendako "CouponValue" izeneko eremua izan daiteke kupoiaren moneta-balioa.
- (Aukerakoa) Zure bezeroei buruzko datuak:
    - Datu hauek atributu estatikoagoetara lerrokatu beharko lirateke, ereduak errendimendu onena izan dezan.
    - Bezeroen datuen datu semantikoen eskemak honakoak dira:
        - **CustomerID:** Bezero batentzako identifikatzaile bakarra.
        - **Sortze-data:** Bezeroa hasieran gehitu zen data.
        - **Estatua edo Probintzia:** Bezeroaren estatua edo probintziaren kokapena.
        - **Herrialdea:** Bezero baten herrialdea.
        - **Industria:** Bezeroaren industria mota. Adibidez, kafea erretzeko "Industria" izeneko eremuak bezeroa txikizkaria den ala ez adieraz dezake.
        - **Sailkapena:** Zure negoziorako bezero baten sailkapena. Adibidez, kafe-txigorgailu batean "ValueSegment" izeneko eremua bezeroaren maila izan daiteke bezeroaren tamainaren arabera.

---

- Iradokitako datuen ezaugarriak:
    - Datu historiko nahikoa: gutxienez hautatutako denbora-leihoa bikoitzeko transakzioen datuak. Hobe, transakzioen historia bizpahiru urtekoa. 
    - Erosketa anitz bezero bakoitzeko: modurik onenean, bi transakzio gutxienez bezeroko.
    - Bezero kopurua: gutxienez 10 bezeroaren profilak, ahal dela 1.000 bezero bakarrak baino gehiago. Ereduak huts egingo du 10 bezero baino gutxiagorekin eta datu historiko nahikorik gabe.
    - Datuen osotasuna: emandako entitatearen datu eremuan falta diren balioen % 20 baino gutxiago.

> [!NOTE]
> Bezeroen erosketa maiztasun handiko enpresa batentzat (aste gutxiren buruan) gomendatzen da iragarpen leiho laburragoa eta buelta definitzea hautatzea. Erosketa maiztasun baxua lortzeko (hilero edo urtean behin), aukeratu iragarpen leiho luzeagoa eta desegin definizioa.

## <a name="create-a-transaction-churn-prediction"></a>Sortu transakzioa bertan behera uzteko iragarpena

1. Customer Insights atalean, joan **Inteligentzia** > **Iragarpenak**.

1. Hautatu **Bezeroen txandakako eredua** fitxa eta hautatu **Erabili eredu hau**.

1. Urtean **Bezeroaren buelta eredua** panela, aukeratu **Transakzioa** eta hautatu **Hasi**.

:::image type="content" source="media/select-transaction-churn.PNG" alt-text="Pantaila pantaila hautatutako transakzio aukerarekin Customer churn model panelean.":::
 
### <a name="name-model"></a>Ezarri izena ereduari

1. Eman ereduari ereduari beste ereduak bereizteko.

1. Eman izena irteerako entitateari letrak eta zenbakiak soilik erabiliz, espaziorik gabe. Horixe da eredu erakundeak erabiliko duen izena. 

1. Hautatu **Hurrengoa**.

### <a name="define-customer-churn"></a>Definitu bezeroak harpidetza bertan behera uzteko unea

1. Ezarri **iragarpen leihoa**. Adibidez, iragarri hurrengo 90 egunetako bezeroen galera-tasa, marketineko mantentze-ahaleginak egokitzeko. Denbora tarte luzeago edo laburragoan galera-arriskua aurreikusteak zaildu dezake galera-arriskuaren profilaren arrazoiak zehaztea, baina zure negozio eskakizun zehatzen araberakoa da.
   >[!TIP]
   > Hautatu dezakezu **Gorde zirriborroa** edozein unetan iragarpen zirriborro gisa gordetzeko. Zirriborroaren iragarpena hemen aurkituko duzu **Nire iragarpenak** jarraitzeko fitxa.

1. Sartu churn definitzeko egun kopurua **Churn definizioa** eremua. Adibidez, bezeroak azken 30 egunetan erosketarik egin ez badu, zure negoziorako galdutzat har daitezke. 

1. Jarraitzeko, hautatu **Hurrengoa**.

### <a name="add-required-data"></a>Gehitu beharrezko datuak

1. Hautatu **gehitu datuak** eta aukeratu transakzioaren edo erosketa-historiaren informazioa duen jarduera mota alboko paneletik.

1. Azpian **Aukeratu jarduerak**, aukeratu jarduera zehatzak kalkulua zentratu nahi duzun hautatutako jarduera motatik.

   :::image type="content" source="media/transaction-churn-select-activity.PNG" alt-text="Alboko panela, mota semantikoan jarduera jakinak aukeratzeko eragiketa erakusten.":::

   Jarduera ez badiozu oraindik mota semantiko bati esleitu, hautatu **Editatu** hori egiteko. Jarduera semantikoak esleitzeko esperientzia gidatua irekiko da. Esleitu datuak hautatutako jarduera motako dagokien eremuekin.

1. Esleitu atributu semantikoak eredua exekutatu ahal izateko behar diren eremuei. Beheko eremuak betetzen ez badira, konfiguratu erosketa-historiaren entitatea *Bezeroaren* entitatera. Sakatu **Gorde**.

1. urtean **Gehitu beharrezko datuak** urratsa, hautatu **Hurrengoa** jarraitzeko jarduera gehiago gehitu nahi ez badituzu.


# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

### <a name="add-additional-data-optional"></a>Gehitu datu gehigarriak (aukerakoa)

Konfiguratu harremana bezeroaren jarduera entitatetik *Bezeroa* entitatea.

1. Aukeratu bezeroaren jardueraren taulan bezeroa identifikatzen duen eremua. Zuzenean erlazionatuta egon daiteke zure *Bezero* entitatearen bezeroaren ID nagusiarekin.

1. Aukeratu zure entitate nagusia *Bezeroa* entitatea.

1. Idatzi izena deskribatzen duena harremana.

#### <a name="customer-activities"></a>Bezeroen jarduerak

1. Aukeran, hautatu **Gehitu datuak** **Bezeroaren jarduerak** atalerako.

1. Aukeratu erabili nahi dituzun datuak dituen jarduera mota semantikoa, eta hautatu jarduera bat edo gehiago atalean **Jarduerak** atala.

1. Hautatu konfiguratzen ari zaren bezeroaren jarduera motarekin bat datorren jarduera mota bat. Aukeratu **Sortu berria** eta aukeratu erabilgarri dagoen jarduera mota bat edo sortu mota berri bat.

1. Hautatu **Hurrengoa**, gero **Gorde**.

1. Sartu nahiko zenukeen beste bezeroen jarduerarik baduzu, errepikatu goiko urratsak.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

### <a name="select-prediction-level"></a>Hautatu iragarpenaren maila

Iragarpen gehienak bezero mailan sortzen dira. Zenbait egoeratan, baliteke hori ez izatea negozioaren beharrei erantzuteko adina. Ezaugarri hau erabil dezakezu bezero baten adar bati buelta emateko, adibidez, bezeroarentzat oro har.

1. Bezeroak baino maila altuagoan iragarpen sortzeko, hautatu **Aukeratu entitatea bigarren maila baterako**. Aukera erabilgarri ez badago, ziurtatu aurreko atala bete duzula.

1. Zabaldu bigarren maila aukeratu nahi zenukeen entitateak edo erabili bilaketa-iragazkiaren koadroa hautatutako aukerak iragazteko.

1. Aukeratu bigarren maila gisa erabili nahi duzun atributua, eta hautatu **Gehitu**.

1. Hautatu **Hurrengoa**.

> [!NOTE]
> Atal honetan eskuragarri dauden entitateak aurreko atalean aukeratu duzun entitatearekin harremana dutelako erakusten dira. Gehitu nahi duzun entitatea ikusten ez baduzu, ziurtatu baliozko harremana duela **Harremanak**. Bat-bateko eta askoko harremanek soilik balio dute konfigurazio honetarako.

### <a name="add-additional-data-optional"></a>Gehitu datu gehigarriak (aukerakoa)

Konfiguratu harremana bezeroaren jarduera entitatetik *Bezeroa* entitatea.

1. Aukeratu bezeroaren jardueraren taulan bezeroa identifikatzen duen eremua. Zuzenean erlazionatuta egon daiteke zure *Bezero* entitatearen bezeroaren ID nagusiarekin.

1. Aukeratu zure entitate nagusia *Bezeroa* entitatea.

1. Idatzi izena deskribatzen duena harremana.

#### <a name="customer-activities"></a>Bezeroen jarduerak

1. Aukeran, hautatu **Gehitu datuak** **Bezeroaren jarduerak** atalerako.

1. Aukeratu erabili nahi dituzun datuak dituen jarduera mota semantikoa, eta hautatu jarduera bat edo gehiago atalean **Jarduerak** atala.

1. Hautatu konfiguratzen ari zaren bezeroaren jarduera motarekin bat datorren jarduera mota bat. Aukeratu **Sortu berria** eta aukeratu erabilgarri dagoen jarduera mota bat edo sortu mota berri bat.

1. Hautatu **Hurrengoa**, gero **Gorde**.

1. Sartu nahiko zenukeen beste bezeroen jarduerarik baduzu, errepikatu goiko urratsak.

#### <a name="customers-data"></a>Bezeroen datuak

1. Aukeran, hautatu **Gehitu datuak** hurrengorako **Bezeroen datuak**.

1. Mapatu atributu semantikoak zure bezeroen datuetako eremuetara identifikatutako moduan. Erabilitako eremuetako datuak ez dira askotan aldatu behar ereduaren errendimendu onena bermatzeko. Adibidez, hilero aldatzen den "Sailkapena" eremua hautatzeak iragarpen-en erabilitako azken balioa izango du, nahiz eta historikoki balio bera ez aplikatu bezeroari iragarpen ereduak eraikitzerakoan.

1. Hautatu **Hurrengoa**.

### <a name="provide-an-optional-list-of-benchmark-accounts"></a>Eman erreferentziazko kontuen aukerako zerrenda

Gehitu erreferentzia gisa erabili nahi dituzun negozioen bezeroen eta kontuen zerrenda. Lortuko duzu [erreferentziazko kontu horien xehetasunak](#review-a-prediction-status-and-results) besteak beste, haien txandaren puntuazioa eta haien txandaren eragina izan zuten ezaugarri garrantzitsuenak iragarpen.

1. Hautatu **+ Gehitu bezeroak**.

1. Aukeratu erreferentzia gisa jokatzen duten bezeroak.

1. Jarraitzeko, hautatu **Hurrengoa**.

---

### <a name="set-schedule-and-review-configuration"></a>Ezarri programazioa eta berrikusi konfigurazioa

1. Ezarri maiztasuna zure eredua berriro sartzeko. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, datu berriak sartu ahala. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.

1. Berrikusi iragarpenaren konfigurazioa. Aurreko urratsetara itzul zaitezke **Editatu** hautatuta erakutsitako balioaren azpian. Edo konfigurazio urratsa hauta dezakezu aurrerapen adierazlean.

1. Balio guztiak behar bezala konfiguratuta badaude, hautatu **Gorde eta exekutatu** iragarpen prozesua hasteko. Gainean **Nire iragarpenak** fitxan, zure iragarpenen egoera ikus dezakezu. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

## <a name="review-a-prediction-status-and-results"></a>Iragarpen iragarpen egoera eta emaitzak berrikustea

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Hautatu berrikusi nahi duzun iragarpena.
   - **Iragarpenaren izena**: sortzean emandako iragarpenaren izena.
   - **Iragarpen mota**: iragarpenean erabilitako eredu mota
   - **Irteerako entitatea**: iragarpenaren irteera gordetzeko entitatearen izena. Izen hori duen entitate bat aurki dezakezu **Datuak** > **erakundeak**.
     Irteerako entitatean, *ChurnScore* da aurreikusitako txandaren probabilitatea eta *IsChurn* oinarritutako etiketa bitarra da *ChurnScore* 0,5 atalasearekin. Baliteke atalase lehenetsiak ez funtzionatzea zure eszenatokian. [Sortu segmentu berria](segments.md#create-a-new-segment) nahi duzun atalasearekin.
     Bezero guztiak ez dira nahitaez bezero aktiboak. Horietako batzuek agian ez dute jarduerarik izan aspalditik eta jadanik txundituta jotzen dira, zure txandaren definizioan oinarrituta. Ez da baliagarria lehendik nahastuta dauden bezeroen arriskua aurreikustea, ez baitira interesatzen zaien publikoa.
   - **Iragarritako eremua**: Eremu hau iragarpen mota batzuetarako bakarrik betetzen da eta ez da erabiltzen galera-tasaren iragarpenean.
   - **Egoera**: iragarpenaren exekuzioaren egoera.
        - **Ilaran**: iragarpena beste prozesu batzuk exekutatzeko zain dago.
        - **Freskatzen**: iragarpena une honetan exekutatzen ari da irteerako entitatera isuriko diren emaitzak sortzeko.
        - **Huts egin du**: iragarpenaren exekuzioak huts egin du. Xehetasun gehiago eskuratzeko, [berrikusi egunkariak](manage-predictions.md#troubleshoot-a-failed-prediction).
        - **Ongi osatu da**: iragarpena ongi osatu da. Aukeratu **ikusi** elipse bertikalen azpian iragarpena berrikusteko
   - **Editatuta**: aurreikuspenerako konfigurazioa aldatu zen data.
   - **Azken freskatua**: iragarpena freskatu den data irteerako entitatean.

1. Hautatu elipse bertikalak emaitzak berrikusteko nahi duzun iragarpenaren ondoan **ikusi**.

   :::image type="content" source="media/model-subs-view.PNG" alt-text="Ikusi kontrola iragarpen baten emaitzak ikusteko.":::

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

1. Emaitza orrialdearen barruan hiru datu nagusi daude:
   - **Prestakuntza ereduaren errendimendua**: A, B edo C puntuazio posibleak dira. Puntuazio honek iragarpenaren errendimendua adierazten du eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia har dezake. Puntuazioak honako arauen arabera zehazten dira: 
        - **A** ereduak iragarpen guztien gutxienez % 50 zehaztasunez aurreikusi duenean, eta galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino gutxienez % 10 baino handiagoa denean.
            
        - **B** ereduak iragarpen guztien gutxienez % 50 zehaztasunez aurreikusi duenean, eta galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino gehienez % 10 handiagoa denean.
            
        - **C** ereduak iragarpen guztien % 50 baino gutxiago zehaztasunez aurreikusi duenean, edo galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino txikiagoa denean.
               
        - **Oinarria** atalak ereduaren iragarpen denbora-tartearen sarrera hartzen du (adibidez, urtebete) eta ereduak denbora zati desberdinak sortzen ditu 2rekin zatituz, hilabete batera edo gutxiagora iritsi arte. Zatiki horiek denbora tarte horretan erosi ez duten bezeroentzako negozio arau bat sortzeko erabiltzen ditu. Bezero hauek galdutzat jotzen dira. Zein bezero galtzeko aukera dagoen ondoen iragartzen duen denboran oinarritutako negozio-araua hartzen da oinarrizko eredu gisa.
            
    - **Probabilitatea asetzeko (bezero kopurua)**: Bezero-taldeak krisiak eragindako arriskuaren arabera. Datu horrek gero lagundu dezake krisi arrisku handia duten bezeroen segmentu bat sortu nahi baduzu. Horrelako segmentuek segmentu kide izateko zure mozketa nolakoa izan behar den ulertzen lagunduko dute.
       
    - **Eraginik garrantzitsuenak**: Zure iragarpena sortzerakoan kontuan hartzen diren faktore asko daude. Faktore bakoitzak bere garrantzia kalkulatzen du eredu batek sortzen dituen iragarpen bateratuetarako. Faktore hauek erabil ditzakezu zure iragarpen emaitzak balioztatzen laguntzeko, edo informazio hau geroago erabil dezakezu [segmentuak sortu](segments.md) horrek bezeroentzako txandakako arriskuan eragina izan dezake.


# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

1. Emaitza orrialdearen barruan hiru datu nagusi daude:
   - **Prestakuntza ereduaren errendimendua**: A, B edo C puntuazio posibleak dira. Puntuazio honek iragarpenaren errendimendua adierazten du eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia har dezake. Puntuazioak honako arauen arabera zehazten dira: 
        - **A** ereduak iragarpen guztien gutxienez % 50 zehaztasunez aurreikusi duenean, eta galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino gutxienez % 10 baino handiagoa denean.
            
        - **B** ereduak iragarpen guztien gutxienez % 50 zehaztasunez aurreikusi duenean, eta galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino gehienez % 10 handiagoa denean.
            
        - **C** ereduak iragarpen guztien % 50 baino gutxiago zehaztasunez aurreikusi duenean, edo galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino txikiagoa denean.
               
        - **Oinarria** atalak ereduaren iragarpen denbora-tartearen sarrera hartzen du (adibidez, urtebete) eta ereduak denbora zati desberdinak sortzen ditu 2rekin zatituz, hilabete batera edo gutxiagora iritsi arte. Zatiki horiek denbora tarte horretan erosi ez duten bezeroentzako negozio arau bat sortzeko erabiltzen ditu. Bezero hauek galdutzat jotzen dira. Zein bezero galtzeko aukera dagoen ondoen iragartzen duen denboran oinarritutako negozio-araua hartzen da oinarrizko eredu gisa.
            
    - **Probabilitatea asetzeko (bezero kopurua)**: Bezero-taldeak krisiak eragindako arriskuaren arabera. Datu horrek gero lagundu dezake krisi arrisku handia duten bezeroen segmentu bat sortu nahi baduzu. Horrelako segmentuek segmentu kide izateko zure mozketa nolakoa izan behar den ulertzen lagunduko dute.
       
    - **Eraginik garrantzitsuenak**: Zure iragarpena sortzerakoan kontuan hartzen diren faktore asko daude. Faktore bakoitzak bere garrantzia kalkulatzen du eredu batek sortzen dituen iragarpen bateratuetarako. Faktore hauek erabil ditzakezu zure iragarpen emaitzak balioztatzen laguntzeko, edo informazio hau geroago erabil dezakezu [segmentuak sortu](segments.md) horrek bezeroentzako txandakako arriskuan eragina izan dezake.


1. Enpresa kontuetarako, aurkitu **Eraginaren ezaugarrien analisia** informazio orria. Lau datu atal ditu:

    - Eskuineko panelean hautatutako elementuak zehazten du orrialde honetako edukia. Aukeratu elementu bat **Goi mailako bezeroak** edo **Erreferentziazko bezeroak**. Bi zerrendak txandaren puntuazioaren balio txikiagoaren arabera ordenatuta daude, puntuazioa bezeroarentzat bakarrik den edo bezeroentzako puntuazio konbinatua eta produktuen kategoria bezalako bigarren maila.
        
        - **Goi mailako bezeroak**: Churn arrisku handiena duten eta churn arrisku txikiena duten 10 bezeroen zerrenda. 
        - **Erreferentziazko bezeroak**: Eredua konfiguratzerakoan hautatu diren 10 bezeroen zerrenda.
 
    - **Churn puntuazioa:** Eskuineko panelean hautatutako elementuaren desaktibazio puntuazioa erakusten du.
    
    - **Churn arriskuaren banaketa:** Bezeroen arteko arriskuaren banaketa eta hautatutako bezeroa dagoen pertzentila erakusten ditu. 
    
    - **Gailu arriskua handitzen eta gutxitzen duten ezaugarri nagusiak:** Eskuineko paneleko hautatutako elementurako, biribiltzeko arriskua handitu eta murriztu duten bost ezaugarri nagusiak zerrendatzen dira. Eragin duen eginbide bakoitzerako, elementuak duen ezaugarriaren balioa eta horrek eragina du txandaren puntuazioan. Ezaugarri bakoitzaren batez besteko balioa bezeroaren segmentu baxu, ertain eta altuan ere agertzen da. Aukeratutako elementurako eragin handieneko funtzioen balioak hobeto testuinguratzen eta bezeroen segmentu baxu, ertain eta altuarekin alderatzen laguntzen du.

       - Baxua: kontuak edo kontu eta bigarren mailako konbinazioak 0 eta 0,33 arteko desoreka puntuazioarekin
       - Ertaina: kontuak edo kontuen eta bigarren mailen konbinazioak 0,33 eta 0,66 arteko desoreka puntuazioarekin
       - Altua: kontuak edo kontuen eta bigarren mailen konbinazioak 0,66 baino handiagoko desoreka puntuazioarekin
    
       Kontu mailan desaktibazioa iragartzen duzunean, kontu guztiak kontsideratzen dira desaktibazio segmentuen batez besteko ezaugarrien balioak lortzeko. Kontu bakoitzeko bigarren mailako mailak iragartzeko, txandakako segmentuen deribazioa alboko panelean hautatutako elementuaren bigarren mailaren araberakoa da. Adibidez, artikulu batek produktu kategoria bigarren maila badu = bulegoko materiala, bulegoko materiala produktu kategoria gisa duten elementuak baino ez dira kontuan hartuko produktuen batez besteko ezaugarrien balioak ateratzerakoan. Logika hau aplikatzen da elementuaren ezaugarrien balioen alderaketa bidezko, baxu, ertain eta altuko segmentuen batez besteko balioekin alderatzea.

       Zenbait kasutan, baxua, ertaina edo altua den segmentuen batez besteko balioa hutsik dago edo ez dago erabilgarri, goiko definizioan oinarrituta ez baitago dagokion churn segmentuetako elementurik.
       
       > [!NOTE]
       > Batez besteko baxu, ertain eta goi zutabeen balioen interpretazioa desberdina da herrialdea edo industria bezalako ezaugarri kategorientzat. "Batez besteko" ezaugarri-balioaren nozioa ezaugarri kategorikoei aplikatzen ez zaienez, zutabe hauetako balioak urritasun baxuko, ertaineko edo handiko segmentuetako bezeroen proportzioa dira, elementu kategorikoaren balio bera dutenak alboko panelean hautatutako elementuarekin alderatuta.

---

## <a name="manage-predictions"></a>Iragarpenak kudeatu

Iragarpenak optimizatzea, konpontzea, freskatzea edo ezabatzea posible da. Berrikusi sarrerako datuen erabilgarritasun txostena iragarpen azkarragoa eta fidagarriagoa nola egin jakiteko. Informazio gehiagorako, joan [Kudeatu iragarpenak](manage-predictions.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
