---
title: Produktuen gomendioen iragarpena
description: Aurreikusi litekeena dela bezeroak eros ditzakeen produktuak edo haiekin elkarreragitea.
ms.date: 02/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: 5ae78b6bbc51fd8a25bc408050a23479698a1414
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5598048"
---
# <a name="product-recommendation-prediction-preview"></a>Produktu-gomendioen iragarpena (aurreargitalpena)

Produktuen gomendio ereduak produktu iragarleentzako gomendio multzoak sortzen ditu. Gomendioak aurreko erosketa portaeran eta antzeko erosketa ereduak dituzten bezeroetan oinarritzen dira. Produktu gomendioen iragarpen berriak sor ditzakezu **Adimena** > **Iragarpenak** orrialdea. Aukeratu **Nire iragarpenak** sortu dituzun beste iragarpen batzuk ikusteko.

Produktuen gomendioak tokian tokiko lege eta araudien menpe egon daitezke, baita bezeroen itxaropenen araberakoak ere, eredua berariaz kontuan hartzeko diseinatuta ez dagoena.  Aurreikuspen gaitasun honen erabiltzaile gisa, **gomendioak berrikusi behar dituzu zure bezeroei entregatu aurretik** aplika daitezkeen lege edo arauak betetzen dituzula ziurtatzeko, baita bezeroek itxaropenak gomendatzen dizkizugunetarako ere. 

Gainera, modelo honen irteerak produktuaren IDan oinarritutako gomendioak emango dizkizu. Entregatzeko mekanismoak aurreikusitako produktuen IDak hartu beharko ditu eta bezeroei eduki egokira esleitu beharko ditu lokalizazioa, irudiaren edukia eta negozioaren beste eduki edo portaera jakin bat izan dezaten.

## <a name="sample-guide"></a>Lagin-gida

Ezaugarri hau probatzea interesatzen bazaizu baina beheko baldintzak betetzeko datuak ez badituzu, [lagin inplementazio bat sortu](sample-guide-predict-product-recommendation.md) dezakezu.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Negozioaren ezagutza zure negozioarentzako produktu mota desberdinak ulertzeko eta zure bezeroek haiekin nola elkarreragiten duten jakiteko. Zure bezeroek aurretik erositako produktuak gomendatzea edo produktu berrietarako gomendioak onartzen ditugu.
- Zure transakzio eta erosketen inguruko datuak eta horien historia:
    - Erosketak edo transakzioak bereizteko transakzio identifikatzaileak.
    - Bezeroen identifikadoreak, transakzioak zure bezeroei esleitzeko.
    - Transakzioen gertaeren datak, transakzioaren datak zehazten dituztenak.
    - (Aukerakoa) transakzioaren produktuaren IDa.
    - (Aukerakoa) Transakzio bat itzultze bat den.
    - Datu semantikoen eskemak informazio hau behar du:
        - **Transakzioaren IDa:** Erosketa edo transakzio baten identifikatzaile bakarra.
        - **Transakzioaren data:** erosketaren edo transakzioaren data.
        - **Transakzioaren balioa:** transakzioaren edo elementuaren zenbakizko balioa.
        - **Produktuaren ID esklusiboa:** erositako produktuaren edo zerbitzuaren IDa, zure datuak lerro-elementuaren mailan badaude.
        - (Aukerakoa) **Transakzio hau itzulera den:** transakzioa itzulera izan den edo ez identifikatzen duen egia ala gezurra eremua. **Transakzioaren balioa** negatiboa bada, informazio hau itzulera bat ondorioztatzeko ere erabiliko dugu.


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

1. *Ez* aukeratu baduzu, gomendatu duela gutxi erositako produktuak, ezarri **Atzera begiratu leihoa**. Ezarpen honek produktuak erabiltzaileari berriro gomendatu aurretik ereduak kontuan hartzen duen denbora-tartea zehazten du. Adibidez, adierazi bezero batek ordenagailu eramangarri bat erosten duela 2 urtean behin. Leiho honetan azken 2 urteetako erosketa historia ikusiko da, eta elementuren bat aurkitzen badute, elementua gomendioetatik iragazi egingo da.

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

### <a name="set-schedule-and-review-configuration"></a>Ezarri programazioa eta berrikusi konfigurazioa

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
   - **Iragarritako eremua:** Eremu hau iragarpen mota batzuetarako bakarrik betetzen da eta ez da erabiltzen galera-tasaren iragarpenean.
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

1. Emaitza orrialdearen barruan hiru datu nagusi daude:
    1. **Prestakuntza ereduaren errendimendua:** A, B edo C puntuazio posibleak dira. Puntuazio honek iragarpenaren errendimendua adierazten du eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia har dezake.
        - Puntuazioak honako arauen arabera zehazten dira:
            - **A** eredua kontuan hartuko da **A** motako kalitatea "Arrakasta @ K" metrika oinarrizko lerroan gutxienez % 10 bada. 
            - **B** eredua kontuan hartuko da **B** motako kalitatea "Arrakasta @ K" metrika oinarrizko lerroan gutxienez % 0-10 bada.
            - **C** eredua kontuan hartuko da **C** motako kalitatea "Arrakasta @ K" metrika oinarrizko lerroan baino txikiagoa bada.
               
               > [!div class="mx-imgBorder"]
               > ![Ereduaren errendimenduaren emaitza ikusi](media/product-recommendation-modelperformance.PNG "Ereduaren errendimenduaren emaitza ikusi")
            - **Oinarria**: ereduak bezero guztien artean erosketa kopuruaren arabera gomendatzen diren produktu onenak hartzen ditu eta ereduak identifikatutako ikasitako arauak erabiltzen ditu bezeroentzako gomendio multzo bat sortzeko. Iragarpenak goiko produktuekin alderatzen dira, produktua erosi zuten bezero kopuruaren arabera kalkulatuta. Bezero batek gutxienez erositako produktuetan ere ikusi den produktu bat gutxienez gomendatutako produktuetan baldin badu, oinarrizko oinarritzat hartzen da. 100 bezeroen artean produktu gomendatua erosi duten 10 bezero horien artean, oinarrizko % 10 izango litzateke.
            - **Arrakasta @ K**: transakzioen balidazio multzoa erabiliz, gomendioak sortzen dira bezero guztientzat eta transakzioen balidazio multzoarekin alderatzen dira. Adibidez, 12 hilabeteko epean, 12. hilabetea datuen balidazio multzo gisa alboratu daiteke. Ereduak gutxienez 12. hilean erosiko zenukeen gauza bat iragartzen badu aurreko 11 hilabeteetan ikasitakoaren arabera, bezeroak "Arrakasta @ K" metrika handituko luke.
    
    1. **Iradokitako produktu gehienak (kalkuluarekin):** zure bezeroentzat aurreikusitako lehen 5 produktuak.
       > [!div class="mx-imgBorder"]
       > ![Gomendatutako 5 produktu onenak erakusten dituen grafikoa](media/product-recommendation-topproducts.PNG "Gomendatutako 5 produktu onenak erakusten dituen grafikoa")
    
    1. **Konfiantza handiko produktuen gomendioak:** ereduak bezeroak eros ditzakeela uste duten bezeroei emandako gomendioen lagina.
       > [!div class="mx-imgBorder"]
       > ![Bezero partikular batzuentzako konfiantza handiko iradokizunak erakusten dituen zerrenda](media/product-recommendation-highconfidence.PNG "Bezero partikular batzuentzako konfiantza handiko iradokizunak erakusten dituen zerrenda")

## <a name="fix-a-failed-prediction"></a>Konpondu huts egindako iragarpena

1. Joan **Nire iragarpenak** fitxan **Adimen** > **iragarpenak**.

1. Hautatu akatsen erregistroak ikusi nahi dituzun iragarpena eta hautatu **Egunkariak**.

1. Berrikusi errore guztiak. Hainbat akats mota gerta daitezke eta deskribatzen dute zer baldintza eragin duen errorea. Adibidez, errore batek ez dauka datu nahikoak zehaztasunez iragartzeko ohikoa da ebaztea kargatzea datu osagarriak Customer Insights-en.

## <a name="refresh-a-prediction"></a>Iragarpen bat eguneratu

Iragarpenak automatikoki freskatzen dira berean [antolatu zure datuak freskatzeko](system.md#schedule-tab) ezarpenetan konfiguratutako moduan.

1. Joan **Nire iragarpenak** fitxan **Adimen** > **iragarpenak**.

1. Hautatu freskatu nahi duzun iragarpenaren ondoan elipsi bertikalak.

1. Aukeratu **Freskatu**.

## <a name="delete-a-prediction"></a>Ezabatu iragarpena

Iragarpen ezabatzeak irteerako entitatea ere kentzen du.

1. Joan **Nire iragarpenak** fitxan **Adimen** > **iragarpenak**.

1. Hautatu ezabatu nahi duzun iragarpenaren ondoan elipsi bertikalak.

1. Hautatu **Ezabatu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]