---
title: Harpidetza Churn iragarpen
description: Aurreikusi bezeroren bat arriskuan dagoen jada enpresaren harpidetza produktu eta zerbitzuak erabiltzen ez dituelako.
ms.date: 08/19/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: f9397729d2f79d079b4dea2ee92d0823b6d987e4
ms.sourcegitcommit: fb9f118b4e16b5aabb3e503463efca21718f5d72
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799715"
---
# <a name="subscription-churn-prediction-preview"></a>Harpidetzeko aurresateko iragarpena (aurrebista)

Harpidetza aurreikuspena lagundu egiten du iragartzen bezeroren bat arriskuan dagoen jada enpresaren harpidetza produktu eta zerbitzuak erabiltzen ez dituelako. Harpidetzearen aurreikuspen berriak sor ditzakezu **Adimena** > **iragarpenak** orria. Aukeratu **Nire iragarpenak** sortu dituzun beste iragarpen batzuk ikusteko.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWOKNQ]

> [!TIP]
> Probatu tutoriala harpidetzen galera-tasaren iragarpena eskuratzeko lagin-datuak erabiliz: [Harpidetzen galera-tasaren iragarpenaren lagin gida](sample-guide-predict-subscription-churn.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [kolaboratzaile-baimenak](permissions.md).
- Enpresa-ezagutzak zer negoziorentzako esan nahi du ulertzeko. Denbora oinarritutako kurnearen definizioak onartzen ditugu. Bezeroak harpidetza amaitu ondoren denbora tarte bat iraulita duela esan daiteke.
- Zure harpidetzei eta historiari buruzko datuak:
    - Harpidetzak identifikatzeko harpidetzak.
    - Bezeroen identifikatzaileak zure bezeroekin harpidetzak batzeko.
    - Harpidetzako gertaeren datak, hasierako datak, amaiera datak eta harpidetze gertaerak zehazten dituzten datak definitzen dituztenak.
    - Harpidetzari buruzko informazioa harpidetza errepikakorra den eta maiztasunez berritzen den zehazteko.
    - Harpidetzak egiteko datu semantikoen eskema informazio hau behar da:
        - **Harpidetza ID:** Harpidetza baten identifikatzaile bakarra.
        - **Harpidetza Amaiera Data:** Harpidetza bezeroak iraungitzen duen data.
        - **Harpidetza Hasiera Data:** Harpidetza bezeroak hasten duen data.
        - **Transakzio data:** Harpidetza aldaketa gertatu zen data. Adibidez, bezero batek harpidetza erosi edo ezeztatzen du.
        - **Harpidetza errepikatua da:** Egiazko / gezurra den eremu boolearra, harpidetzaren ID berdinekin berrituko den zehazten duena bezeroaren esku hartu gabe
        - **Errepikapen maiztasuna (hilabeteetan):** Harpidetzak errepikatzeko, harpidetza berriztatuko da. Hilabeteetan irudikatzen da. Adibidez, urtero bezero batek beste urtebetez automatikoki berritzen duen harpidetzak 12. balioa du.
        - (Hautazkoa) **Harpidetza-zenbatekoa:** Harpidetza berritzeagatik bezero batek ordaintzen duen moneta zenbatekoa. Harpidetza maila desberdinetarako ereduak identifikatzen lagun dezake.
- Bezeroaren jarduerei buruzko datuak:
    - Mota bereko jarduerak bereizteko jarduera identifikatzaileak.
    - Bezeroaren identifikadoreak maparen jardueretan zure bezeroentzat.
    - Jardueren izena eta jardueraren data biltzen dituen jarduera.
    - Bezeroen jardueren datu semantikoen eskemak honako hauek ditu:
        - **Gako nagusia:** Jarduera baterako identifikatzaile bakarra. Adibidez, webgune baten bisita edo bezeroen telesailen pasarte bat ikusi zuen erabilera erregistro bat.
        - **Timestamp:** Giltza nagusian identifikatutako gertaeraren data eta ordua.
        - **Gertaera:** Erabili nahi duzun gertaeraren izena. Adibidez, streaming bideo zerbitzuko "UserAction" izeneko eremuak "Ikusi" balioa izan dezake.
        - **Xehetasunak:** Ekitaldiaren inguruko informazio zehatza. Adibidez, streaming bideo zerbitzuko "ShowTitle" izeneko eremuak bezeroak ikusi duen bideoaren balioa izan dezake.
- Iradokitako datuen ezaugarriak:
    - Datu historiko nahikoak: harpidetzaren datuak hautatutako denbora-leihoaren bikoitza gutxienez. Ahal izanez gero, bizpahiru urteko harpidetza datuak.
    - Harpidetzaren egoera: datuek bezero bakoitzarentzako harpidetza aktiboak eta inaktiboak biltzen dituzte, beraz, bezeroaren ID bakoitzeko sarrera ugari daude.
    - Bezero kopurua: gutxienez 10 bezeroaren profilak, ahal dela 1.000 bezero bakarrak baino gehiago. Ereduak huts egingo du 10 bezero baino gutxiagorekin eta datu historiko nahikorik gabe.
    - Datuen osotasuna: emandako entitatearen datu eremuan falta diren balioen % 20 baino gutxiago.
   
   > [!NOTE]
   > Gutxienez bi jarduera erregistro beharko dituzu kalkulatu nahi dituzun bezeroen % 50.

## <a name="create-a-subscription-churn-prediction"></a>Sortu harpidetzaren aurresateko iragarpena

1. Hartzaileei buruzko xehetasunetan, joan hona: **Adimena** > **Iragarpenak**.
1. Hautatu botoia **Harpidetza kornearen eredua (aurrebista)** fitxa eta hautatu **Erabili eredu hau**.
   > [!div class="mx-imgBorder"]
   > ![Harpidetza Churn ereduko fitxa erabil ezazu Eredu hau botoiarekin.](media/subscription-churn-usethismodel.PNG "Harpidetza Churn ereduko fitxa erabil ezazu Eredu hau botoiarekin")

### <a name="name-model"></a>Ezarri izena ereduari

1. Eman ereduari ereduari beste ereduak bereizteko.
1. Eman izena irteerako entitateari letrak eta zenbakiak soilik erabiliz, espaziorik gabe. Horixe da eredu erakundeak erabiliko duen izena. Ondoren, hautatu **Hurrengoa**.

### <a name="define-customer-churn"></a>Definitu bezeroak harpidetza bertan behera uzteko unea

1. Idatzi kopurua **Harpidetza amaitu zen egunak** zure negozioak bezero bat egoera txarrean dagoela uste duela. Epea normalean, bezeroen galerak ekiditen saiatzean eskaintzak edo bestelako marketin-ahaleginak bezalako negozio-jarduerak gustatzen zaizkio.
1. Idatzi kopurua **Egunak etorkizuna ikertzeko txanda iragartzeko** txanda iragartzeko leiho bat ezartzeko. Adibidez, zure bezeroek hurrengo 90 egunetan eragingo duten arriskua aurreikusteko marketinari eusteko ahaleginetara egokitzeko. Denbora epe luzeago edo laburragoetan churn arriskua aurreikusteak zaildu dezake zure churn arriskuaren profileko faktoreak jorratzea, zure negozioaren eskakizun zehatzen arabera. Jarraitzeko, hautatu **Hurrengoa**
   >[!TIP]
   > Aukeratu dezakezu **Gorde eta itxi** edozein unetan aurreikuspena zirriborro gisa gordetzeko. Zirriborroaren iragarpena hemen aurkituko duzu **Nire iragarpenak** jarraitzeko fitxa.

### <a name="add-required-data"></a>Gehitu beharrezko datuak

1. Aukeratu **Datuak gehitu** egiteko **Harpidetzearen historia** eta aukeratu harpidetze historiaren informazioa ematen duen entitatea [ezinbesteko baldintza](#prerequisites).
1. Beheko eremuak ez badira populatzen, konfiguratu harremana zure harpidedun historiatik entitateak Bezeroaren entitatera.
    1. Hautatu botoia **Harpidedunen historia entitatea**.
    1. Hautatu botoia **eremua** harpidedunen historiako entitatean identifikatzen duen bezeroa. Zure Bezeroaren entitatearen bezeroaren ID nagusiarekin erlazionatu behar da.
    1. Hautatu botoia **Bezero entitatea** bat datorrena zure lehen bezero-entitatearekin.
    1. Idatzi izena deskribatzen duena harremana.
       > [!div class="mx-imgBorder"]
       > ![Harpidetzearen historia orrialdea bezeroarekiko harremanaren sorrera erakusten duena.](media/subscription-churn-subscriptionhistoryrelationship.PNG "Harpidetzearen historia orrialdea bezeroarekiko harremanaren sorrera erakusten duena")
1. Hautatu **Hurrengoa**.
1. Egin mapen eremu semantikoak harpidedunen historiaren entitatean eta hautatu **Gorde**. Eremuen deskribapenak eskuratzeko, begiratu [ezinbesteko baldintza](#prerequisites).
   > [!div class="mx-imgBorder"]
   > ![Harpidetzaren historiaren orria hautatutako harpidetze historiaren entitateko eremuetan mapatuta dauden atributu semantikoak erakusten ditu.](media/subscription-churn-subscriptionhistorymapping.PNG "Harpidetzaren historiaren orria hautatutako harpidetze historiaren entitateko eremuetan mapatuta dauden atributu semantikoak erakusten ditu")
1. Hautatu **Gehitu datuak** **Bezeroaren jarduerak** eta aukeratu entitatea ematen duena bezeroaren jarduera informazioa aurrebaldintzetan deskribatu bezala.
1. Hautatu konfiguratzen ari zaren bezeroaren jarduera motarekin bat datorren jarduera mota bat.  Aukeratu **Sortu berria** eta eman izena, behar duzun jarduera motarekin bat datorren aukera bat ikusten ez baduzu.
1. Bezeroaren jarduera erakundearen eta bezeroaren entitatearen arteko harremanak konfiguratu beharko dituzu.
    1. Aukeratu bezeroa identifikatzen duen eremua bezeroaren jarduera taulan, zuzenean lotuta egon daiteke zure Bezeroaren entitatearen bezeroaren IDarekin.
    1. Hautatu botoia Bezero entitatea bat datorrena zure lehen bezero-entitatearekin
    1. Idatzi izena deskribatzen duena harremana.
1. Hautatu **Hurrengoa**.
1. Egin mapen eremu semantikoak bezeroaren jarduera entitatean eta hautatu **Gorde**. Eremuen deskribapenak eskuratzeko, begiratu [ezinbesteko baldintza](#prerequisites).
1. (Aukerakoa) Beste bezeroen jarduera batzuk sartu nahi badituzu, errepikatu goiko pausoak.
   > [!div class="mx-imgBorder"]
   > ![Definitu entitate-harremana.](media/subscription-churn-customeractivitiesmapping.PNG "Bezeroaren jarduerak orria hautatutako bezeroaren jarduera entitateko eremuetan mapatuta dauden atributu semantikoak erakusten ditu")
1. Hautatu **Hurrengoa**.

### <a name="set-schedule-and-review-configuration"></a>Ezarri programazioa eta berrikusi konfigurazioa

1. Ezarri maiztasuna zure eredua berriro sartzeko. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, hartzaileen xehetasunetan datu berriak sartu ahala. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.
1. Hautatu **Hurrengoa**.
1. Berrikusi konfigurazioa. Aurreikuspen konfigurazioaren edozein ataletara joan zaitezke hautatuta **Editatu** erakutsitako balioaren azpian. Edo konfigurazio urratsa hauta dezakezu aurrerapen adierazlean.
1. Balio guztiak behar bezala konfiguratuta badaude, hautatu **Gorde eta exekutatu** iragarpen prozesua hasteko. Gainean **Nire iragarpenak** fitxan, zure iragarpenen egoera ikus dezakezu. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

## <a name="review-a-prediction-status-and-results"></a>Iragarpen iragarpen egoera eta emaitzak berrikustea

1. Joan **Nire iragarpenak** fitxan **Adimen** > **iragarpenak**.
   > [!div class="mx-imgBorder"]
   > ![Nire iragarpenak orriaren ikuspegia.](media/subscription-churn-mypredictions.PNG "Nire iragarpenak orriaren ikuspegia")
1. Hautatu berrikusi nahi duzun iragarpena.
   - **Iragarpen izena:** Sortzerakoan emandako iragarpenaren izena.
   - **Iragarpen mota:** Iragarpenak egiteko erabilitako eredu mota
   - **Irteerako entitatea:** Iragarpenaren irteera gordetzeko entitatearen izena. Izen hori duen entitate bat aurki dezakezu **Datuak** > **erakundeak**.    
     Irteerako entitatean, *ChurnScore* da aurreikusitako txandaren probabilitatea eta *IsChurn* oinarritutako etiketa bitarra da *ChurnScore* 0,5 atalasearekin. Baliteke atalase lehenetsiak ez funtzionatzea zure eszenatokian. [Sortu segmentu berria](segments.md#create-a-new-segment) nahi duzun atalasearekin.
   - **Iragarritako eremua:** Aurreikuspen mota batzuetarako bakarrik dago eremua, eta ez da harpidetzaren kutxa iragarpenean erabiltzen.
   - **Egoera:** Iragarpenaren exekutatutako egoera.
        - **ilaran:** Aurreikuspena beste prozesu batzuen zain egongo da.
        - **freskatzen:** Aurreikuspenak une honetan "puntuazio" prozesatzen ari da irteera entitatean sartuko diren emaitzak sortzeko.
        - **Huts:** iragarpenak huts egin du. Aukeratu **Erregistroak** xehetasun gehiagorako.
        - **Ondorengoa:** iragarpenak arrakasta izan du. Aukeratu **ikusi** elipse bertikalen azpian iragarpena berrikusteko
   - **Hizkuntzak:** Aurreikuspenerako konfigurazioa aldatu zen data.
   - **Azken freskatua:** Iragarpena freskatu den data irteerako entitatean.
1. Hautatu elipse bertikalak emaitzak berrikusteko nahi duzun iragarpenaren ondoan **ikusi**.
   > [!div class="mx-imgBorder"]
   > ![Aurreikuspen bat egiteko, editatu, freskatu, ikusi, erregistroak eta ezabatu behar diren iragarpenak egiteko iragarki baterako aukerak.](media/subscription-churn-verticalellipses.PNG "Aurreikuspen bat egiteko, editatu, freskatu, ikusi, erregistroak eta ezabatu behar diren iragarpenak egiteko iragarki baterako aukerak")
1. Emaitza orrialdearen barruan hiru datu nagusi daude:
    1. **Prestakuntza ereduaren errendimendua:** A, B edo C puntuazio posibleak dira. Puntuazio honek iragarpenaren errendimendua adierazten du eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia har dezake.
        - Puntuazioak honako arauen arabera zehazten dira:
            - **A** ereduak zehaztasunez aurreikusitako guztiaren % 50 gutxienez, eta prezio zehatzen portzentajea kriskitatu duten bezeroen batez besteko maiztasun-tasa historikoa baino txikiagoa den batez besteko tasa % 10ean.
            - **B** ereduak zehaztasunez aurreikusitako guztiaren % 50 gutxienez, eta prezio zehatzen portzentajea kriskitatu duten bezeroen batez besteko maiztasun-tasa historikoa baino txikiagoa den batez besteko tasa % 10era arte.
            - **C** ereduak zehaztasunez aurreikusitako guztiaren % 50 gutxiago aurreikusten duenean, edo prezipitazio zehatzen portzentajea bezeroen prezio arruntaren batez bestekoa baino txikiagoa bada.
               > [!div class="mx-imgBorder"]
               > ![Ereduaren errendimenduaren emaitza ikusi.](media/subscription-churn-modelperformance.PNG "Ereduaren errendimenduaren emaitza ikusi")
    1. **Probabilitatea asetzeko (bezero kopurua):** Bezero-taldeak krisiak eragindako arriskuaren arabera. Datu horrek gero lagundu dezake krisi arrisku handia duten bezeroen segmentu bat sortu nahi baduzu. Horrelako segmentuek segmentu kide izateko zure mozketa nolakoa izan behar den ulertzen lagunduko dute.
       > [!div class="mx-imgBorder"]
       > ![Grafoaren emaitzen banaketa erakusten duen grafikoa, % 0-100 bitartekoa.](media/subscription-churn-resultdistribution.PNG "Grafoaren emaitzen banaketa erakusten duen grafikoa, % 0-100 bitartekoa")
    1. **Eraginik garrantzitsuenak:** Zure iragarpena sortzerakoan kontuan hartzen diren faktore asko daude. Faktore bakoitzak eredu batek sortzen dituen aurreikuspen agregatuetarako kalkulatutako garrantzia du. Faktore hauek erabil ditzakezu zure iragarpen emaitzak balioztatzen laguntzeko. Bestela, informazio hori gero erabil dezakezu [segmentuak sortu](segments.md) horrek bezeroen kalte arriskuan eragina izan lezake.
       > [!div class="mx-imgBorder"]
       > ![Zerrenda eragin duten faktoreak eta horien garrantzia agerian dauden zerrendak.](media/subscription-churn-influentialfactors.PNG "Zerrenda eragin duten faktoreak eta horien garrantzia agerian dauden zerrendak")

## <a name="manage-predictions"></a>Iragarpenak kudeatu

Iragarpenak optimizatzea, konpontzea, freskatzea edo ezabatzea posible da. Berrikusi sarrerako datuen erabilgarritasun txostena iragarpen azkarragoa eta fidagarriagoa nola egin jakiteko. Informazio gehiago lortzeko, ikusi [Kudeatu iragarpenak](manage-predictions.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
