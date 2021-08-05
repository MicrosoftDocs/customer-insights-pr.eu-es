---
title: Transakzioen galera-tasaren iragarpena
description: Iragarri bezeroren bat arriskuan dagoen jada produktu eta zerbitzuak erosten ez dituelako.
ms.date: 11/12/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: 28c89693239393d93b7a816535b8c3fffe353935
ms.sourcegitcommit: e57d51ae3cc233f7b6185c074c66efd9800c02c1
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/14/2021
ms.locfileid: "6559390"
---
# <a name="transactional-churn-prediction-preview"></a>Transakzioen galera-tasaren iragarpena (aurrebista)

Transakzioen galera-tasaren iragarpenak bezeroak denbora-tarte jakin batean jada zure produktuak edo zerbitzuak erosiko ote dituen iragartzen laguntzen du. Galera-tasaren iragarpen berriak sor ditzakezu **Adimena** > **Iragarpenak** atalean. Aukeratu **Nire iragarpenak** sortu dituzun beste iragarpen batzuk ikusteko.

> [!TIP]
> Probatu tutoriala transakzioen galera-tasaren iragarpena eskuratzeko lagin-datuak erabiliz: [Transakzioen galera-tasaren iragarpenaren (aurrebista) lagin gida](sample-guide-predict-transactional-churn.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Enpresa-ezagutzak zer negoziorentzako esan nahi du ulertzeko. Denboran oinarritutako galera-tasen definizioak onartzen ditugu, hau da, erosketarik gabeko tarte baten ondoren bezeroa galdutzat jotzen da.
- Zure transakzio / erosketen inguruko datuak eta horien historia:
    - Erosketak / transakzioak bereizteko transakzio identifikatzaileak.
    - Bezeroen identifikadoreak, transakzioak zure bezeroekin lotzeko.
    - Transakzioen gertaeren datak, transakzioaren datak zehazten dituztenak.
    - Erosketak / transakzioak egiteko datu semantikoen eskemak informazio hau behar du:
        - **Transakzioaren IDa:** Erosketa edo transakzio baten identifikatzaile bakarra.
        - **Transakzioaren data:** Erosketaren edo transakzioaren data.
        - **Transakzioaren balioa:** Transakzioaren / elementuaren moneta / zenbakizko balioa.
        - (Aukerakoa) **Produktuaren ID esklusiboa:** Erositako produktuaren edo zerbitzuaren IDa, zure datuak lerro-elementuaren mailan badaude.
        - (Aukerakoa) **Transakzio hau itzulera izan den ala ez:** Transakzioa itzulera izan den edo ez identifikatzen duen egia / gezurra eremua. **Transakzioaren balioa** negatiboa bada, informazio hau itzulera bat ondorioztatzeko ere erabiliko dugu.
- (Aukerakoa) Bezeroen jarduerei buruzko datuak:
    - Mota bereko jarduerak bereizteko jarduera identifikatzaileak.
    - Bezeroaren identifikadoreak maparen jardueretan zure bezeroentzat.
    - Jardueren izena eta jardueraren data biltzen dituen jarduera.
    - Bezeroen jardueren datu semantikoen eskemak honako hauek ditu:
        - **Gako nagusia:** Jarduera baterako identifikatzaile bakarra. Adibidez, webgunea bisitatzea edo bezeroak zure produktuaren lagin bat probatu duela azaltzen duen erabilera erregistroa.
        - **Timestamp:** Giltza nagusian identifikatutako gertaeraren data eta ordua.
        - **Gertaera:** Erabili nahi duzun gertaeraren izena. Adibidez, janari dendako "UserAction" izeneko eremua bezeroak erabilitako kupoi bat izan daiteke.
        - **Xehetasunak:** Ekitaldiaren inguruko informazio zehatza. Adibidez, janari dendako "CouponValue" izeneko eremua izan daiteke kupoiaren moneta-balioa.
- Iradokitako datuen ezaugarriak:
    - Datu historiko nahikoa: gutxienez hautatutako denbora-leihoa bikoitzeko transakzioen datuak. Hobe, transakzioen historia bizpahiru urtekoa. 
    - Erosketa anitz bezero bakoitzeko: modurik onenean, bi transakzio gutxienez bezeroko.
    - Bezero kopurua: gutxienez 10 bezeroaren profilak, ahal dela 1.000 bezero bakarrak baino gehiago. Ereduak huts egingo du 10 bezero baino gutxiagorekin eta datu historiko nahikorik gabe.
    - Datuen osotasuna: emandako entitatearen datu eremuan falta diren balioen % 20 baino gutxiago.

> [!NOTE]
> Bezeroen erosketa maiztasun handiko enpresa batentzat (aste gutxiren buruan) gomendatzen da iragarpen leiho laburragoa eta buelta definitzea hautatzea. Erosketa maiztasun baxua lortzeko (hilero edo urtean behin), aukeratu iragarpen leiho luzeagoa eta desegin definizioa.

## <a name="create-a-transactional-churn-prediction"></a>Sortu transakzioen galera-tasaren iragarpena

1. Customer Insights atalean, joan **Inteligentzia** > **Iragarpenak**.

1. Aukeratu **Bezeroaren galera-tasaren eredua (aurrebista)** lauza eta hautatu **Erabili eredu hau**.
   
1. **Bezeroaren galera-tasaren eredua** panelean, aukeratu **Transakzionala** eta hautatu **Hasi**.

:::image type="content" source="media/select-transaction-churn.PNG" alt-text="Pantaila-argazkia, bezeroaren galera-tasaren ereduaren panelean aukera transakzionala hautatuta.":::

### <a name="name-model"></a>Ezarri izena ereduari

1. Eman ereduari ereduari beste ereduak bereizteko.

1. Eman izena irteerako entitateari letrak eta zenbakiak soilik erabiliz, espaziorik gabe. Horixe da eredu erakundeak erabiliko duen izena. 

1. Hautatu **Hurrengoa**.

### <a name="define-customer-churn"></a>Definitu bezeroak harpidetza bertan behera uzteko unea

1. Ezarri denbora-tarte bat **Identifikatu hurrengoan gal ditzakegun bezeroak** eremuaren galera-tasa iragartzeko. Adibidez, iragarri hurrengo 90 egunetako bezeroen galera-tasa, marketineko mantentze-ahaleginak egokitzeko. Denbora tarte luzeago edo laburragoan galera-arriskua aurreikusteak zaildu dezake galera-arriskuaren profilaren arrazoiak zehaztea, baina zure negozio eskakizun zehatzen araberakoa da. 
   >[!TIP]
   > Aukeratu dezakezu **Gorde eta itxi** edozein unetan aurreikuspena zirriborro gisa gordetzeko. Zirriborroaren iragarpena hemen aurkituko duzu **Nire iragarpenak** jarraitzeko fitxa.

1. Idatzi egun kopurua **Bezero bat galdutzat jotzen da epe honetan ez badu erosketarik egin:** eremuko galera-tasa definitzeko. Adibidez, bezeroak azken 30 egunetan erosketarik egin ez badu, zure negoziorako galdutzat har daitezke. 

1. Jarraitzeko, hautatu **Hurrengoa**

### <a name="add-required-data"></a>Gehitu beharrezko datuak

1. Aukeratu **Gehitu datuak** **Erosketen historia** atalean eta aukeratu transakzioen / erosketen historiari buruzko informazioa ematen duen entitatea, [aurrebaldintzak](#prerequisites) atalean deskribatu moduan.

1. Esleitu eremu semantikoak erosketa-historiako entitateko atributuetara eta hautatu **Hurrengoa**. Eremuen deskribapenak eskuratzeko, begiratu [ezinbesteko baldintza](#prerequisites).

   :::image type="content" source="media/model-map-purchase-entity.PNG" alt-text="Esleitu erosketa-entitatearen eremu semantikoak.":::

1. Beheko eremuak betetzen ez badira, konfiguratu erosketa-historiaren entitatea Bezeroaren entitatera.
    1. Hautatu **Erosketa-historiaren entitatea**.
    1. Aukeratu erosketa-historiaren entitatean bezeroa identifikatzen duen **Eremua**. Zure Bezeroaren entitatearen bezeroaren ID nagusiarekin erlazionatu behar da.
    1. Hautatu botoia **Bezero entitatea** bat datorrena zure lehen bezero-entitatearekin.
    1. Idatzi izena deskribatzen duena harremana.

    :::image type="content" source="media/model-purchase-join.PNG" alt-text="Bezeroarekiko harremana sortu dela erakusten duen erosketa-historiaren orria.":::
   
1. Hautatu **Hurrengoa**.

1. Aukeran, hautatu **Gehitu datuak** **Bezeroaren jarduerak** atalerako. Aukeratu bezeroaren jarduerari buruzko informazioa ematen duen entitatea aurrebaldintzetan azaltzen den moduan.

1. Esleitu eremu semantikoak bezeroaren jardueraren entitateko atributuetara eta hautatu **Hurrengoa**. Eremuen deskribapenak eskuratzeko, begiratu [ezinbesteko baldintza](#prerequisites).

   :::image type="content" source="media/map-transaction-data-fields.png" alt-text="Esleitu bezeroen eremuak transakzio datuetarako.":::

1. Hautatu konfiguratzen ari zaren bezeroaren jarduera motarekin bat datorren jarduera mota bat. Aukeratu **Sortu berria** eta aukeratu erabilgarri dagoen jarduera mota bat edo sortu mota berri bat.

1. Bezeroaren jarduera erakundearen eta bezeroaren entitatearen arteko harremanak konfiguratu beharko dituzu.
    1. Aukeratu bezeroaren jardueraren taulan bezeroa identifikatzen duen eremua. Zuzenean erlazionatuta egon daiteke zure Bezero entitatearen bezeroaren ID nagusiarekin.
    1. Hautatu botoia Bezero entitatea bat datorrena zure lehen bezero-entitatearekin
    1. Idatzi izena deskribatzen duena harremana.

1. Sakatu **Gorde**.

1. Sartu nahiko zenukeen beste bezeroen jarduerarik baduzu, errepikatu goiko urratsak.

1. Hautatu **Hurrengoa**.

### <a name="set-schedule-and-review-configuration"></a>Ezarri programazioa eta berrikusi konfigurazioa

1. Ezarri maiztasuna zure eredua berriro sartzeko. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, datu berriak sartu ahala. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.

1. Berrikusi iragarpenaren konfigurazioa. Aurreko urratsetara itzul zaitezke **Editatu** hautatuta erakutsitako balioaren azpian. Edo konfigurazio urratsa hauta dezakezu aurrerapen adierazlean.

1. Balio guztiak behar bezala konfiguratuta badaude, hautatu **Gorde eta exekutatu** iragarpen prozesua hasteko. Gainean **Nire iragarpenak** fitxan, zure iragarpenen egoera ikus dezakezu. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

## <a name="review-a-prediction-status-and-results"></a>Iragarpen iragarpen egoera eta emaitzak berrikustea

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Hautatu berrikusi nahi duzun iragarpena.
   - **Iragarpenaren izena:** sortzerakoan emandako iragarpenaren izena.
   - **Iragarpen mota:** iragarpenean erabilitako eredu mota
   - **Irteerako entitatea:** Iragarpenaren irteera gordetzeko entitatearen izena. Izen hori duen entitate bat aurki dezakezu **Datuak** > **erakundeak**.    
     Irteerako entitatean, *ChurnScore* da aurreikusitako txandaren probabilitatea eta *IsChurn* oinarritutako etiketa bitarra da *ChurnScore* 0,5 atalasearekin. Baliteke atalase lehenetsiak ez funtzionatzea zure eszenatokian. [Sortu segmentu berria](segments.md#create-a-new-segment) nahi duzun atalasearekin.
     Bezero guztiak ez dira nahitaez bezero aktiboak. Horietako batzuek agian ez dute jarduerarik izan aspalditik eta jadanik txundituta jotzen dira, zure txandaren definizioan oinarrituta. Ez da baliagarria lehendik nahastuta dauden bezeroen arreta arriskua aurreikustea, ez baitira interesatzen den publikoa.
   - **Iragarritako eremua:** Eremu hau iragarpen mota batzuetarako bakarrik betetzen da eta ez da erabiltzen galera-tasaren iragarpenean.
   - **Egoera:** iragarpenaren exekuzioaren egoera.
        - **Ilaran:** iragarpena beste prozesu batzuk exekutatzeko zain dago.
        - **Freskatzen:** iragarpena une honetan exekutatzen ari da irteerako entitatera isuriko diren emaitzak sortzeko.
        - **Huts egin du:** iragarpenaren exekuzioak huts egin du. Xehetasun gehiago eskuratzeko, [berrikusi egunkariak](manage-predictions.md#troubleshoot-a-failed-prediction).
        - **Ongi osatu da:** iragarpena ongi osatu da. Aukeratu **ikusi** elipse bertikalen azpian iragarpena berrikusteko
   - **Hizkuntzak:** Aurreikuspenerako konfigurazioa aldatu zen data.
   - **Azken freskatua:** Iragarpena freskatu den data irteerako entitatean.

1. Hautatu elipse bertikalak emaitzak berrikusteko nahi duzun iragarpenaren ondoan **ikusi**.

   :::image type="content" source="media/model-subs-view.PNG" alt-text="Ikusi kontrola iragarpen baten emaitzak ikusteko.":::   

1. Emaitza orrialdearen barruan hiru datu nagusi daude:
    1. **Prestakuntza ereduaren errendimendua:** A, B edo C puntuazio posibleak dira. Puntuazio honek iragarpenaren errendimendua adierazten du eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia har dezake. Puntuazioak honako arauen arabera zehazten dira:
         
         - **A** ereduak iragarpen guztien gutxienez % 50 zehaztasunez aurreikusi duenean, eta galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino gutxienez % 10 baino handiagoa denean.
            
         - **B** ereduak iragarpen guztien gutxienez % 50 zehaztasunez aurreikusi duenean, eta galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino gehienez % 10 handiagoa denean.
            
         - **C** ereduak iragarpen guztien % 50 baino gutxiago zehaztasunez aurreikusi duenean, edo galdutako bezeroen iragarpenen zehaztasuna oinarrizko tasa baino txikiagoa denean.
               
         - **Oinarria** atalak ereduaren iragarpen denbora-tartearen sarrera hartzen du (adibidez, urtebete) eta ereduak denbora zati desberdinak sortzen ditu 2rekin zatituz, hilabete batera edo gutxiagora iritsi arte. Zatiki horiek denbora tarte horretan erosi ez duten bezeroentzako negozio arau bat sortzeko erabiltzen ditu. Bezero hauek galdutzat jotzen dira. Zein bezero galtzeko aukera dagoen ondoen iragartzen duen denboran oinarritutako negozio-araua hartzen da oinarrizko eredu gisa.
            
    1. **Probabilitatea asetzeko (bezero kopurua):** Bezero-taldeak krisiak eragindako arriskuaren arabera. Datu horrek gero lagundu dezake krisi arrisku handia duten bezeroen segmentu bat sortu nahi baduzu. Horrelako segmentuek segmentu kide izateko zure mozketa nolakoa izan behar den ulertzen lagunduko dute.
       
    1. **Eraginik garrantzitsuenak:** Zure iragarpena sortzerakoan kontuan hartzen diren faktore asko daude. Faktore bakoitzak bere garrantzia kalkulatzen du eredu batek sortzen dituen iragarpen bateratuetarako. Faktore hauek erabil ditzakezu zure iragarpen emaitzak balioztatzen laguntzeko. Bestela, informazio hori gero erabil dezakezu [segmentuak sortu](segments.md) horrek bezeroen kalte arriskuan eragina izan lezake.

## <a name="manage-predictions"></a>Iragarpenak kudeatu

Iragarpenak optimizatzea, konpontzea, freskatzea edo ezabatzea posible da. Berrikusi sarrerako datuen erabilgarritasun txostena iragarpen azkarragoa eta fidagarriagoa nola egin jakiteko. Informazio gehiago lortzeko, ikusi [Kudeatu iragarpenak](manage-predictions.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
