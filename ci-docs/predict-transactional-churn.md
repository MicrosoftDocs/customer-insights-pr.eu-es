---
title: Transakzio txanda iragarpen (bideoa dauka)
description: Iragarri bezeroren bat arriskuan dagoen jada produktu eta zerbitzuak erosten ez dituelako.
ms.date: 09/30/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: fd8df0f0a168ddfab9e8ad3af9e1f1fc0bc1b7a2
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610497"
---
# <a name="predict-transaction-churn"></a>Iragarri transakzio churn

Transakzioen galera-tasaren iragarpenak bezeroak denbora-tarte jakin batean jada zure produktuak edo zerbitzuak erosiko ote dituen iragartzen laguntzen du.

Negozioen ezagutza izan behar duzu churn-ak zure negozioarentzat zer esan nahi duen ulertzeko. Denboran oinarritutako galera-tasen definizioak onartzen ditugu, hau da, erosketarik gabeko tarte baten ondoren bezeroa galdutzat jotzen da.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWN6Eg]

Negozio kontuetan oinarritutako inguruneetarako, kontu baten transazio transaktiboa aurreikus dezakegu, baita kontuaren konbinazioa eta produktuen kategoria bezalako beste informazio maila ere. Esaterako, dimentsio bat gehitzeak "Contoso" kontuak "bulegoko papera" produktu-kategoria erosteari uzteko aukera duen zehazten lagun dezake. Gainera, negozio kontuetarako, AI ere erabil dezakegu kontu bat bigarren mailako informazio kategoria bat lortzeko litekeena den arrazoien zerrenda sortzeko.

> [!TIP]
> Saiatu iragarpen transakzioen txanda lagin-datuak erabiliz: [Transaction churn iragarpen adibide-gida](sample-guide-predict-transactional-churn.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [kolaboratzaile-baimenak](permissions.md).
- Gutxienez 10 bezero profil, ahal izanez gero 1.000 bezero esklusibo baino gehiago.
- Bezeroaren identifikatzailea, transakzioak zure bezeroekin lotzeko identifikatzaile bakarra.
- Aukeratutako denbora-leihoaren bikoitza gutxienez transakzio-datuak, adibidez, bi edo hiru urteko transakzioen historia. Egokiena bezero bakoitzeko gutxienez bi transakzio. Transakzioen historiak honako hauek izan behar ditu:
  - **Transakzioaren IDa** : erosketa edo transakzio baten identifikatzaile bakarra.
  - **Transakzioaren data** : Erosketaren edo transakzioaren data.
  - **Transakzioaren balioa** : transakzioaren moneta edo zenbakizko balioaren zenbatekoa.
  - **Produktu ID bakarra** : erositako produktuaren edo zerbitzuaren ID zure datuak lerro-elementu mailan badaude.
  - **Transakzio hau itzulera izan den ala ez** : transakzioa itzulera izan den edo ez identifikatzen duen egia/faltsua eremua. bada **Transakzioaren balioa** negatiboa da, itzulera bat ondorioztatzen dugu.
- Bezeroaren jardueraren datuak:
  - Bezeroaren identifikatzailea, zure bezeroei jarduerak mapatzeko identifikatzaile bakarra.
  - **Lehen gakoa:** Jarduera baten identifikatzaile bakarra. Adibidez, webgunea bisitatzea edo bezeroak zure produktuaren lagin bat probatu duela azaltzen duen erabilera erregistroa.
  - **Ordu-zigilua:** Lehen gakoaren bidez identifikatutako gertaeraren data eta ordua.
  - **Gertaera:** Erabili nahi duzun ekitaldiaren izena. Adibidez, janari dendako "UserAction" izeneko eremua bezeroak erabilitako kupoi bat izan daiteke.
  - **Xehetasunak:** Ekitaldiaren inguruko informazio zehatza. Adibidez, janari dendako "CouponValue" izeneko eremua izan daiteke kupoiaren moneta-balioa.
- Emandako entitatearen datuen eremuan falta diren balioen % 20 baino gutxiago

Enpresa-kontuetarako (B-to-B), gehitu bezero-datuak atributu estatikoagoetara lerrokatuta, ereduak ondoen funtzionatzen duela ziurtatzeko:
- **Bezeroaren ID:** Bezero baten identifikatzaile bakarra.
- **Sortze data:** Hasieran bezeroa gehitu zen data.
- **Estatua edo probintzia:** Bezero baten estatuko edo probintziaren kokapena.
- **Herrialdea:** Bezero baten herrialdea.
- **Industria:** Bezero baten industria mota. Adibidez, kafea erretzeko "Industria" izeneko eremuak bezeroa txikizkaria den ala ez adieraz dezake.
- **Sailkapena:** Zure negoziorako bezero baten kategorizazioa. Adibidez, kafe-txigorgailu batean "ValueSegment" izeneko eremua bezeroaren maila izan daiteke bezeroaren tamainaren arabera.

> [!NOTE]
> Bezeroen erosketa maiztasun handiko enpresa batentzat (aste gutxiren buruan) gomendatzen da iragarpen leiho laburragoa eta buelta definitzea hautatzea. Erosketa maiztasun baxua lortzeko (hilero edo urtean behin), aukeratu iragarpen leiho luzeagoa eta desegin definizioa.

## <a name="create-a-transaction-churn-prediction"></a>Sortu transakzioa bertan behera uzteko iragarpena

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Bezeroen txandakako eredua** teila.

1. Hautatu **Transakzioa** bira motarako eta gero **Hasi**.

1. **Eman izena eredu honi** eta **Irteerako entitatearen izenari** beste eredu edo entitate batzuetatik bereizteko.

1. Hautatu **Hurrengoa**.

### <a name="define-customer-churn"></a>Definitu bezeroak harpidetza bertan behera uzteko unea

Hautatu **Gorde zirriborroa** edozein unetan iragarpen zirriborro gisa gordetzeko. Iragarpen zirriborroa atalean bistaratzen da **Nire iragarpenak** fitxa.

1. Ezarri **iragarpen leihoa**. Adibidez, iragarri hurrengo 90 egunetako bezeroen galera-tasa, marketineko mantentze-ahaleginak egokitzeko. Denbora tarte luzeago edo laburragoan galera-arriskua aurreikusteak zaildu dezake galera-arriskuaren profilaren arrazoiak zehaztea, baina zure negozio eskakizun zehatzen araberakoa da.

1. Sartu txandaka definitzeko egun kopurua **Churn definizioa** eremua. Esate baterako, bezero batek azken 30 egunetan erosketarik egin ez badu, baliteke zure negoziorako birrindutakotzat jotzea.

1. Hautatu **Hurrengoa**.

### <a name="add-purchase-history"></a>Gehitu erosketa-historia

1. Hautatu **Gehitu datuak** rentzat **Bezeroaren transakzioen historia**.

1. Hautatu jarduera semantiko mota, **Salmenta Eskaera** edo **SalesOrderLine**, transakzioen historiako informazioa biltzen duena. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak semantikoki mapatu baziren, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Mapa semantikoa gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.

   :::image type="content" source="media/transaction-churn-select-activity.PNG" alt-text="Alboko panela, mota semantikoan jarduera jakinak aukeratzeko eragiketa erakusten.":::

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Gehitu jarduera gehiago edo hautatu **Hurrengoa**.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

### <a name="add-additional-data-optional"></a>Gehitu datu gehigarriak (aukerakoa)

1. Hautatu **Gehitu datuak** rentzat **Bezeroen jarduerak**.

1. Hautatu erabili nahi dituzun datuak dituen jarduera semantiko mota. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak semantikoki mapatu baziren, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Mapa semantikoa gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Hautatu **Hurrengoa**

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

### <a name="select-prediction-level"></a>Hautatu iragarpenaren maila

Iragarpen gehienak bezero mailan sortzen dira. Zenbait egoeratan, baliteke hori ez izatea negozioaren beharrei erantzuteko adina. Erabili eginbide hau bezero baten sukurtsal baten urritasuna aurreikusteko, adibidez, bezero osoarentzako baino.

1. Hautatu **Aukeratu entitatea bigarren maila baterako**. Aukera erabilgarri ez badago, ziurtatu aurreko atala bete duzula.

1. Zabaldu bigarren maila aukeratu nahi zenukeen entitateak edo erabili bilaketa-iragazkiaren koadroa hautatutako aukerak iragazteko.

1. Aukeratu bigarren maila gisa erabili nahi duzun atributua, eta hautatu **Gehitu**.

1. Hautatu **Hurrengoa**.

> [!NOTE]
> Atal honetan eskuragarri dauden entitateak aurreko atalean aukeratu duzun entitatearekin harremana dutelako erakusten dira. Gehitu nahi duzun entitatea ikusten ez baduzu, ziurtatu baliozko harremana duela **Harremanak**. Bat-bateko eta askoko harremanek soilik balio dute konfigurazio honetarako.

### <a name="add-additional-data-optional"></a>Gehitu datu gehigarriak (aukerakoa)

1. Hautatu **Gehitu datuak** rentzat **Bezeroen jarduerak**.

1. Hautatu erabili nahi dituzun datuak dituen jarduera semantiko mota. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak semantikoki mapatu baziren, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Mapa semantikoa gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Hautatu **Hurrengoa**

1. Aukeran, hautatu **Gehitu datuak** hurrengorako **Bezeroen datuak**.

1. Mapatu atributu semantikoak zure bezeroen datuetako eremuetara identifikatutako moduan. Erabilitako eremuetako datuak ez dira askotan aldatu behar ereduaren errendimendu onena bermatzeko. Adibidez, hilero aldatzen den "Sailkapena" eremua hautatzeak iragarpen-en erabilitako azken balioa izango du, nahiz eta historikoki balio bera ez aplikatu bezeroari iragarpen ereduak eraikitzerakoan.

1. Hautatu **Hurrengoa**.

### <a name="provide-an-optional-list-of-benchmark-accounts"></a>Eman erreferentziazko kontuen aukerako zerrenda

Gehitu erreferentzia gisa erabili nahi dituzun negozioen bezeroen eta kontuen zerrenda. The [erreferentziazko kontu hauen xehetasunak](#view-prediction-results) sartu beren churn puntuazioa eta eragin handiena izan duten ezaugarriak iragarpen.

1. Hautatu **+ Gehitu bezeroak**.

1. Aukeratu erreferentzia gisa jokatzen duten bezeroak.

1. Hautatu **Hurrengoa**.

---

### <a name="set-update-schedule"></a>Konfiguratu antolaketaren eguneratzea

1. Horretarako **Datuen eguneraketak** urratsa, aukeratu maiztasun bat zure eredua berriro trebatzeko. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, Customer Insights-en datu berriak sartzen diren heinean. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.

### <a name="review-and-run-the-model-configuration"></a>Berrikusi eta exekutatu modeloaren konfigurazioa

The **Berrikusi eta exekutatu** urratsak konfigurazioaren laburpena erakusten du eta iragarpen sortu aurretik aldaketak egiteko aukera ematen du.

1. Hautatu **Editatu** aldaketak berrikusteko eta egiteko edozein urratsetan.

1. Zure hautapenekin pozik bazaude, hautatu **Gorde eta exekutatu** eredua exekutatzen hasteko. Hautatu **Eginda**. The **Nire iragarpenak** fitxa bistaratzen da iragarpen sortzen ari den bitartean. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

[!INCLUDE [progress-details](includes/progress-details-pane.md)]

## <a name="view-prediction-results"></a>Ikusi iragarpen emaitzak

1. Joan **Adimena** > **Iragarpenak**.

1. urtean **Nire iragarpenak** fitxan, hautatu ikusi nahi duzun iragarpen.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

Emaitza orrialdearen barruan hiru datu nagusi daude:

[!INCLUDE [predict-transaction-results](includes/predict-transaction-results.md)]

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

Emaitza orrialdearen barruan hiru datu nagusi daude:

[!INCLUDE [predict-transaction-results](includes/predict-transaction-results.md)]

An **Ezaugarri eragingarrien azterketa** informazio-orriak lau datu atal ditu:

- Eskuineko panelean, hautatu elementu bat **Goi mailako bezeroak** edo **Erreferentziazko bezeroak**. Bi zerrendak txandaren puntuazioaren balio txikiagoaren arabera ordenatuta daude, puntuazioa bezeroarentzat bakarrik den edo bezeroentzako puntuazio konbinatua eta produktuen kategoria bezalako bigarren maila. Hautatutako elementuak orrialde honetako edukia zehazten du.

  - **Goi mailako bezeroak**: Churn arrisku handiena duten eta churn arrisku txikiena duten 10 bezeroen zerrenda.
  - **Erreferentziazko bezeroak**: Eredua konfiguratzerakoan hautatu diren 10 bezeroen zerrenda.

- **Churn puntuazioa:** Eskuineko panelean hautatutako elementuaren desaktibazio puntuazioa erakusten du.

- **Arriskuaren banaketa:** Bezeroen arteko ugaltze-arriskuaren banaketa eta hautatutako bezeroa dagoen pertzentilea erakusten du.

- **Ezaugarri nagusiak churn-arriskua areagotzen eta murrizten dute:** Hautatutako elementuaren txandakako arriskua handitu eta murriztu zuten bost ezaugarri nagusiak zerrendatzen ditu eskuineko panelean. Elementu horren ezaugarriak duen balioa eta eragin duen ezaugarri bakoitzaren churn puntuazioan duen eragina erakusten du. Ezaugarri bakoitzaren batez besteko balioa bezeroaren segmentu baxu, ertain eta altuan ere agertzen da. Aukeratutako elementurako eragin handieneko funtzioen balioak hobeto testuinguratzen eta bezeroen segmentu baxu, ertain eta altuarekin alderatzen laguntzen du.

  - Baxua: 0 eta 0,33 arteko churn puntuazioa duten kontu eta bigarren mailako konbinazioak edo konbinazioak.
  - Ertaina: 0,33 eta 0,66 arteko churn puntuazioa duten kontuak edo konbinazioak eta bigarren mailak.
  - Altua: 0,66 baino handiagoa den txandakako puntuazioa duten kontuak edo konbinazioak eta bigarren mailak.

  Kontu mailan desaktibazioa iragartzen duzunean, kontu guztiak kontsideratzen dira desaktibazio segmentuen batez besteko ezaugarrien balioak lortzeko. Kontu bakoitzeko bigarren mailako mailak iragartzeko, txandakako segmentuen deribazioa alboko panelean hautatutako elementuaren bigarren mailaren araberakoa da. Adibidez, elementu batek produktu-kategoriaren bigarren maila bat badu (bulegoko hornigaiak), orduan produktu-kategoria gisa bulego-materialak dituzten elementuak soilik hartuko dira kontuan churn-segmentuen batez besteko ezaugarri-balioak ateratzean. Logika hau aplikatzen da elementuaren ezaugarrien balioen alderaketa bidezko, baxu, ertain eta altuko segmentuen batez besteko balioekin alderatzea.

  Zenbait kasutan, baxua, ertaina edo altua den segmentuen batez besteko balioa hutsik dago edo ez dago erabilgarri, goiko definizioan oinarrituta ez baitago dagokion churn segmentuetako elementurik.

  Batez besteko baxu, ertain eta goi zutabeen balioen interpretazioa desberdina da herrialdea edo industria bezalako ezaugarri kategorientzat. "Batez besteko" ezaugarri-balioaren nozioa ezaugarri kategorikoei aplikatzen ez zaienez, zutabe hauetako balioak urritasun baxuko, ertaineko edo handiko segmentuetako bezeroen proportzioa dira, elementu kategorikoaren balio bera dutenak alboko panelean hautatutako elementuarekin alderatuta.

---

 > [!NOTE]
 > Eredu honen irteerako entitatean, *ChurnScore* churn-aren aurreikusitako probabilitatea erakusten du eta *IsChurn* oinarritutako etiketa bitarra da *ChurnScore* 0,5 atalasearekin. Atalase lehenetsi honek ez badu funtzionatzen zure eszenatokirako, [segmentu berri bat sortu](segments.md#create-a-segment) nahiago duzun atalasearekin. Bezero guztiak ez dira nahitaez bezero aktiboak. Horietako batzuek agian ez dute jarduerarik izan aspalditik eta jadanik txundituta jotzen dira, zure txandaren definizioan oinarrituta. Ez da baliagarria lehendik nahastuta dauden bezeroen arriskua aurreikustea, ez baitira interesatzen zaien publikoa.
>
> Churn puntuazioa ikusteko, joan hona **Datuak** > **Entitateak** eta ikusi eredu honetarako definitu duzun irteera-entitatearen datu-fitxa.

[!INCLUDE [footer-include](includes/footer-banner.md)]
