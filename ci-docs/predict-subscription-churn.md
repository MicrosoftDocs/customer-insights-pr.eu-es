---
title: Iragar ezazu harpidetza kopurua (bideoa dauka)
description: Aurreikusi bezeroren bat arriskuan dagoen jada enpresaren harpidetza produktu eta zerbitzuak erabiltzen ez dituelako.
ms.date: 09/30/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: 7464707864c418bfcc625ddfd245622131434b33
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610221"
---
# <a name="predict-subscription-churn"></a>Iragarpenen harpidetza kornestatzea

Aurreikusi bezeroren bat arriskuan dagoen jada enpresaren harpidetza produktu eta zerbitzuak erabiltzen ez dituelako. Harpidetza-datuek bezero bakoitzarentzat harpidetza aktiboak eta inaktiboak barne hartzen dituzte, beraz, hainbat sarrera daude bezero ID bakoitzeko.

Negozioen ezagutza izan behar duzu churn-ak zure negozioarentzat zer esan nahi duen ulertzeko. Denboran oinarritutako txandakako definizioak onartzen ditugu, hau da, bezero batek harpidetza amaitu eta denbora-tarte bat egin duela uste da.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWOKNQ]

> [!TIP]
> Saiatu iragarpen harpidetza aukera lagin-datuak erabiliz: [Harpidetza churn iragarpen adibide-gida](sample-guide-predict-subscription-churn.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [kolaboratzaile-baimenak](permissions.md).
- Gutxienez 10 bezero profil, ahal izanez gero 1.000 bezero esklusibo baino gehiago.
- Bezeroaren identifikatzailea, harpidetzak zure bezeroekin lotzeko identifikatzaile bakarra.
- Hautatutako denbora-leihoaren bikoitza gutxienez harpidetza-datuak. Ahal izanez gero, bizpahiru urteko harpidetza datuak. Harpidetza historiak honako hauek izan behar ditu:
  - **Harpidetzaren IDa:** Harpidetza baten identifikatzaile bakarra.
  - **Harpidetzaren amaiera-data:** Bezeroarentzat harpidetza iraungitzen den data.
  - **Harpidetzaren hasiera data:** Bezeroarentzat harpidetza hasten den data.
  - **Transakzioaren data:** Harpidetzaren aldaketaren data. Adibidez, bezero batek harpidetza erosi edo ezeztatzen du.
  - **Aldizkako harpidetza al da:** Egia/faltsua eremu boolearra, harpidetza harpidetza ID berarekin berrituko den zehazten duena, bezeroen esku hartu gabe.
  - **Errepikapenaren maiztasuna (hilabetetan):** Aldizkako harpidetzetarako, harpidetza berrituko den hilabetea. Adibidez, urtero bezero batek beste urtebetez automatikoki berritzen duen harpidetzak 12. balioa du.
  - **Harpidetzaren zenbatekoa** : bezero batek harpidetza berritzeko ordaintzen duen moneta kopurua. Harpidetza maila desberdinetarako ereduak identifikatzen lagun dezake.
- Gutxienez bi jarduera-erregistro kalkulatu nahi diezun bezeroen % 50entzat txandaka. Bezeroaren jarduerak honako hauek izan behar ditu:
  - **Lehen gakoa:** Jarduera baten identifikatzaile bakarra. Adibidez, webgune baten bisita edo bezeroen telesailen pasarte bat ikusi zuen erabilera erregistro bat.
  - **Ordu-zigilua:** Lehen gakoaren bidez identifikatutako gertaeraren data eta ordua.
  - **Gertaera:** Erabili nahi duzun ekitaldiaren izena. Adibidez, streaming bideo zerbitzuko "UserAction" izeneko eremuak "Ikusi" balioa izan dezake.
  - **Xehetasunak:** Ekitaldiaren inguruko informazio zehatza. Adibidez, streaming bideo zerbitzuko "ShowTitle" izeneko eremuak bezeroak ikusi duen bideoaren balioa izan dezake.
- Emandako entitatearen datuen eremuan falta diren balioak % 20 baino gutxiago.

## <a name="create-a-subscription-churn-prediction"></a>Sortu harpidetzaren aurresateko iragarpena

Hautatu **Gorde zirriborroa** edozein unetan iragarpen zirriborro gisa gordetzeko. Iragarpen zirriborroa atalean bistaratzen da **Nire iragarpenak** fitxa.

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Bezeroen txandakako eredua** teila.

1. Hautatu **Harpidetza** bira motarako eta gero **Hasi**.

1. **Eman izena eredu honi** eta **Irteerako entitatearen izenari** beste eredu edo entitate batzuetatik bereizteko.

1. Hautatu **Hurrengoa**.

### <a name="define-customer-churn"></a>Definitu bezeroak harpidetza bertan behera uzteko unea

1. Idatzi kopurua **Harpidetza amaitu zen egunak** zure negozioak bezero bat egoera txarrean dagoela uste duela. Epe hori normalean bezeroa galtzen saihesten saiatzen diren eskaintzei edo beste marketin-ahalegin batzuekin lotuta egon ohi da.

1. Sartu zenbakia **Etorkizuna ikertzeko egunak iragartzeko**. Adibidez, iragarri hurrengo 90 egunetako bezeroen galera-tasa, marketineko mantentze-ahaleginak egokitzeko. Denbora epe luzeago edo laburragoetan churn arriskua aurreikusteak zaildu dezake zure churn arriskuaren profileko faktoreak jorratzea, zure negozioaren eskakizun zehatzen arabera.

1. Hautatu **Hurrengoa**.

### <a name="add-required-data"></a>Gehitu beharrezko datuak

1. Hautatu **Gehitu datuak** rentzat **Harpidetza historia**.

1. Hautatu jarduera semantikoaren mota **Harpidetza** beharrezko harpidetza-historiaren informazioa dauka. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak semantikoki mapatu baziren, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Mapa semantikoa gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.
  
   :::image type="content" source="media/subscription-churn-required.png" alt-text="Gehitu behar diren datuak Harpidetza txandakako eredurako":::

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Hautatu **Gehitu datuak** rentzat **Bezeroen jarduerak**.

1. Hautatu bezeroaren jarduerari buruzko informazioa ematen duen jarduera semantikoa. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak semantikoki mapatu baziren, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Mapa semantikoa gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Gehitu jarduera gehiago edo hautatu **Hurrengoa**.

### <a name="set-update-schedule"></a>Konfiguratu antolaketaren eguneratzea

1. Aukeratu maiztasuna zure eredua birziklatzeko. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, Customer Insights-en datu berriak sartzen diren heinean. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.

### <a name="review-and-run-the-model-configuration"></a>Berrikusi eta exekutatu modeloaren konfigurazioa

The **Berrikusi eta exekutatu** urratsak konfigurazioaren laburpena erakusten du eta iragarpen sortu aurretik aldaketak egiteko aukera ematen du.

1. Hautatu **Editatu** aldaketak berrikusteko eta egiteko edozein urratsetan.

1. Zure hautapenekin pozik bazaude, hautatu **Gorde eta exekutatu** eredua exekutatzen hasteko. Hautatu **Eginda**. The **Nire iragarpenak** fitxa bistaratzen da iragarpen sortzen ari den bitartean. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

[!INCLUDE [progress-details](includes/progress-details-pane.md)]

## <a name="view-prediction-results"></a>Ikusi iragarpen emaitzak

1. Joan **Adimena** > **Iragarpenak**.

1. urtean **Nire iragarpenak** fitxan, hautatu ikusi nahi duzun iragarpen.

Emaitza orrialdearen barruan hiru datu nagusi daude:

- **Prestakuntza ereduaren errendimendua** : A, B edo C kalifikazioek iragarpen-en errendimendua adierazten dute eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia hartzen lagun zaitzake.
  
  :::image type="content" source="media/subscription-churn-modelperformance.PNG" alt-text="Ereduaren puntuazioaren informazio koadroaren irudia A kalifikazioarekin.":::

  Kalifikazioak arau hauetan oinarrituta zehazten dira:
  - **A** ereduak guztizko iragarpenen % 50 zehatz-mehatz aurreikusten duenean, eta iragarpen zehatzen ehunekoa iragarpen zehatzen ehunekoa gutxienez % 10eko bataz besteko iragarpen historikoa baino handiagoa denean.
  - **B** ereduak guztizko aurreikuspenen % 50 gutxienez zehaztasunez aurreikusten duenean, eta iragarpen zehatzen ehunekoa iragarpen zehatzen ehunekoa bataz besteko iragarpen historikoa baino % 10 handiagoa denean.
  - **C** ereduak guztizko iragarpenen % 50 baino gutxiago zehaztasunez aurreikusten duenean, edo iragarpen zehatzen ehunekoa biraka egin duten bezeroen batez besteko iragarpen-tasa historikoa baino txikiagoa denean.
  
- **Probabilitatea asetzeko (bezero kopurua)**: Bezero-taldeak krisiak eragindako arriskuaren arabera. Aukeran, [bezeroen segmentuak sortu](prediction-based-segment.md) txanda-arrisku handiarekin. Horrelako segmentuek segmentu kide izateko zure mozketa nolakoa izan behar den ulertzen lagunduko dute.  

  :::image type="content" source="media/subscription-churn-resultdistribution.PNG" alt-text="Grafoaren emaitzen banaketa erakusten duen grafikoa, % 0-100 bitartekoa":::

- **Eraginik garrantzitsuenak:** Zure iragarpena sortzerakoan kontuan hartzen diren faktore asko daude. Faktore bakoitzak bere garrantzia kalkulatzen du eredu batek sortzen dituen iragarpen bateratuetarako. Erabili faktore hauek zure iragarpen emaitzak balioztatzeko. Edo erabili informazio hau geroago [segmentuak sortu](.//prediction-based-segment.md) horrek bezeroen txanda-arriskuan eragiten lagun dezake.

  :::image type="content" source="media/subscription-churn-influentialfactors.PNG" alt-text="Zerrenda eragin duten faktoreak eta horien garrantzia agerian dauden zerrendak.":::

> [!NOTE]
> Eredu honen irteerako entitatean, *ChurnScore* churn-aren aurreikusitako probabilitatea da eta *IsChurn* oinarritutako etiketa bitarra da *ChurnScore* 0,5 atalasearekin. Atalase lehenetsi honek ez badu funtzionatzen zure eszenatokirako, [segmentu berri bat sortu](segments.md) nahiago duzun atalasearekin. Churn puntuazioa ikusteko, joan hona **Datuak** > **Entitateak** eta ikusi eredu honetarako definitu duzun irteera-entitatearen datu-fitxa.

[!INCLUDE [footer-include](includes/footer-banner.md)]
