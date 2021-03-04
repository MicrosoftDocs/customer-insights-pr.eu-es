---
title: Lotu entitateak datuak bateratzeko
description: Lotu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 10/14/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
ms.openlocfilehash: 05afd17b7f1b34f7f24a8fa8cb2dc32c1649d40f
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267463"
---
# <a name="match-entities"></a>Batu entitateak

Mapen fasea amaitu ondoren, entitateekin bat egiteko prest zaude. Binakako faseak zure datu multzoak bezeroaren profil bateratutako datu multzoa nola konbinatu zehazten du. Partida faseak gutxienez eskatzen du [mapatutako bi erakunde](map-entities.md).

## <a name="specify-the-match-order"></a>bat etortzearen ordena zehaztu

Joan **Datuak** > **Bateratu** > **Bat etorri** aukerara eta hautatu **Ezarri ordena** bat-etortzearen fasea hasteko.

Partida bakoitzak bi entitate edo gehiago entitate bakarrean elkartzen ditu eta bezero bakoitzaren erregistro bakarra jarraitzen du. Hurrengo adibidean, hiru entitate aukeratu ditugu: **HarremanetarakoCSV: TestData** gisa **Lehen** Erakunde, **WebAccountCSV: TestData** gisa **2. entitatea**, eta **CallRecordSmall: TestData** gisa **3. entitatea**. Aukeren goiko diagramak partidaren ordena nola gauzatuko den azaltzen du.

> [!div class="mx-imgBorder"]
> ![Editatu datuekin bat datozen ordena](media/configure-data-match-order-edit-page.png "Editatu datuekin bat datozen ordena")
  
The **Lehen** entitatearekin bat dator **2. entitatea**. Lehen partidaren emaitza den datu-multzoarekin bat dator **3. entitatea**.
Adibide honetan bi partida baino ez ditugu aukeratu, baina sistemak gehiago onartzen du.

> [!IMPORTANT]
> Aukeratzen duzun entitatea **Lehen** entitatea zure datu multzo nagusia bateratzeko oinarria izango da. Partida fasean hautatzen diren entitate osagarriak gehituko zaizkie entitate honi. Aldi berean, horrek ez du esan nahi erakunde bateratuak barne hartuko duenik *guztiak* entitate honetan sartutako datuak.
>
> Bi entitateren hierarkia aukeratzen lagun dezaketen bi gogoeta daude:
>
> - Zein entitate jotzen duzu zure bezeroei buruzko datu osatuena eta fidagarriena izatea?
> - Identifikatu berri duzun entitateak baditu beste entitate batzuek (adibidez, izena, telefono zenbakia edo helbide elektronikoa) partekatutako atributuak? Bestela, aukeratu zure bigarren entitate fidagarriena.

Aukeratu **Egina** zure partidaren ordena gordetzeko.

## <a name="define-rules-for-your-first-match-pair"></a>Definitu zure lehen bikote bikotearen arauak

Partiduen ordena zehaztu ondoren, zehaztutako partiduak ikusiko dituzu **Bat-etortzea** orria. Pantailaren goiko aldean fitxak hutsik egongo dira bat datozen ordena exekutatu arte.

> [!div class="mx-imgBorder"]
> ![Definitu arauak](media/configure-data-match-need-rules.png "Definitu arauak")

The **Beharrak arauak** abisuak iradokitzen du ez dela partida pareko arau bat definitzen. Bat egiten duten arauek entitate pare bat lotuko den logika zehazten dute.

1. Zure lehenengo araua zehazteko, ireki tekla **Arauaren definizioa** panela bat datorren bat datorren lerroan hautatutako partiden taulan (1) eta ondoren hautatuta **Sortu arau berria** (2).

   > [!div class="mx-imgBorder"]
   > ![Sortu arau berria](media/configure-data-match-new-rule2.png "Sortu arau berria")

2. Sarbidean **Editatu araua** panela, konfiguratu arau horren baldintzak. Baldintza bakoitza derrigorrezko hautapenak biltzen dituzten bi errenkadek adierazten dute.

   > [!div class="mx-imgBorder"]
   > ![Arau-panel berria](media/configure-data-match-new-rule-condition.png "Arau-panel berria")

   Entitatea / Eremua (lehenengoa) - Lehenengo bikote bikotearen entitatearekin bat egiteko erabiliko den atributua. Adibidez, telefono zenbaki bat edo helbide elektronikoa izan daitezke. Aukeratu bezeroarentzat bakarra izango den atributu bat.

   > [!TIP]
   > Saihestu ez datozenekin bat egiten jarduera motako atributuen arabera. Beste modu batera esanda, atributu bat jarduera dela dirudi, irizpide eskasak izan litezke.  

   Entitatea / Eremua (bigarrena) - Bigarren bikote bikotearen entitatearekin bat egiteko erabiliko den atributua.

   Normalizatu - **Normalizazio metodoa**: Hautatutako atributuetarako hainbat normalizazio aukera daude. Adibidez, puntuazioa kentzea edo espazioak kentzea

   Erakundearen izenak normalizatzeko (Aurrebista), hauta dezakezu **Mota (Telefonoa, Izena, Erakundea)**

   > [!div class="mx-imgBorder"]
   > ![Normalizazio-B2B](media/match-normalization-b2b.png "Normalizazio-B2B")

   Zehaztasun maila - Baldintza honetarako erabiliko den zehaztasun maila. Partiduen egoera baterako zehaztasun maila ezartzeak bi mota izan ditzake: **Oinarrizko** eta **pertsonalizatua**.  
   - Oinarrizkoa: lau aukera daude: baxua, ertaina, altua eta zehatza. Aukeratu **zehatza** Ehuneko 100 bat datozen erregistroak soilik lotzeko. Hautatu beste maila bat ehuneko 100 berdin-berdina ez duten erregistroekin bat etor dadin.
   - Pertsonalizatua: erabil ezazu graduatzailea erregistroek bat egin behar duten edo sartu behar duten balio portzentaia pertsonalizatzeko **pertsonalizatua** eremu. Sistemak atalase hau gainditzen duten erregistroak soilik batuko ditu konbinatutako bikote bikote gisa. Labaingaiaren balioak 0 eta 1 artean daude. Beraz, 0,64k ehuneko 64 adierazten du.

3. Hautatu **Egina** araua gordetzeko.

### <a name="add-multiple-conditions"></a>Gehitu hainbat baldintza

Zure entitateekin bat etor dadin baldintza ugari betetzen badira soilik, gehitu AND eragile baten bidez lotzen diren baldintza gehiago.

1. Sarbidean **Editatu araua** hautatu panela **Gehitu baldintza**. Baldintzak ezabatu ditzakezu lehendik dagoen baldintza baten kentzeko botoia hautatuta.

2. Hautatu **Egina** araua gordetzeko.

## <a name="add-multiple-rules"></a>Gehitu hainbat arau

Baldintza bakoitza atributu pare bakar bati aplikatzen zaio, eta arauek baldintza multzoak adierazten dituzte. Zure entitateak atributu multzo desberdinekin parekatzeko, arau gehiago gehi ditzakezu.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Bat egin** > **Bat etorri**.

2. Hautatu eguneratu nahi duzun entitatea eta hautatu **Gehitu arauak**.

3. Jarraitu prozedura deskribatutako moduan [Definitu zure lehen bikote bikotearen arauak](#define-rules-for-your-first-match-pair).

> [!NOTE]
> Arau ordena garrantzitsua da. Bat egiten duen algoritmoa zure lehenengo araua oinarri hartuta bat egiten saiatzen da eta bigarren araura jarraitzen du soilik lehenengo arauaren menpean identifikatu ez bada.

## <a name="define-deduplication-on-a-match-entity"></a>Definitu bikoiztuak kentzea bat datorren entitate batean

Goiko ataletan azaldutako entitateen arteko lotura arauak zehaztearekin batera, bikoiztuak kentzearen arauak ere zehaztu ditzakezu. *Bikoiztuak kentzea* prozesu bat da. Erregistro bikoiztuak identifikatzen ditu, erregistro bakarrean konbinatzen ditu eta jatorrizko erregistro guztiak bateratutako erregistro honekin lotzen ditu konbinatutako erregistroarena ez den beste ID batzuekin.

Erregistro bikoiztu bat identifikatu ondoren, erregistro hori entitateen arteko bat-etortze prozesuan erabiliko da. Bikoiztuak ketzea entitate mailan ezartzen da eta bat egite prozesuan erabilitako entitate guztiei aplika dakieke.

### <a name="add-deduplication-rules"></a>Gehitu bikoiztuak kentzeko arauak

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Bat egin** > **Bat etorri**.

1. **Konbinatutako bikoiztuak** atalean, hautatu **Ezarri entitateak**.

1. **Konbinatu hobespenak** atalean, hautatu bikoiztuak kentzea aplikatu nahi diezun entitateak.

1. Zehaztu erregistro bikoiztuak nola bateratu eta aukeratu hiru bateratze aukeretako bat:
   - *Beteen daudenak* : Betetako atributu gehien dituen erregistroa identifikatzen du erregistro nagusi gisa. Hori da konbinatzeko aukera lehenetsia.
   - *Berrienak*: erregistro nagusia identifikatzen du berritasunen arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.
   - *Zaharrenak*: erregistro nagusia identifikatzen du zahartasunaren arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.
 
   > [!div class="mx-imgBorder"]
   > ![Bikoiztuak kentzeko arauak, 1. urratsa](media/match-selfconflation.png "Bikoiztuak kentzeko arauak, 1. urratsa")
 
1. Entitateak hautatuta eta haien konbinatze-hobespenak zehaztutakoan, hautatu **Sortu arau berria** entitate mailan bikoiztuak kentzeko arauak definitzeko.
   - **Aukeratu eremua** aukerak iturburuko datuen bikoiztuak nahi dituzun entitate horretatik eskuragarri dauden eremu guztiak zerrendatzen ditu.
   - Zehaztu normalizazio- eta zehaztasun-ezarpenak, entitate gurutzatuen bat-etortzean zehaztutako antzera.
   - Baldintza osagarriak defini ditzakezu **Gehitu baldintza** aukeratuz.
 
   > [!div class="mx-imgBorder"]
   > ![Bikoiztuak kentzeko arauak, 2. urratsa](media/match-selfconflation-rules.png "Bikoiztuak kentzeko arauak, 2. urratsa")

  Entitate berarako hainbat bikoiztuak kentzeko arau sor ditzakezu. 

1. Bat-egite prozesua exekutatzeak erregistroak taldekatzen ditu bikoiztuak kentzeko arauetan zehaztutako baldintzetan oinarrituta. Erregistroak taldekatu ondoren, bat-egiteen gidalerroa aplikatzen da erregistro nagusia identifikatzeko.

1. Irabazle erregistro hori entitateen arteko bat-etortzeari pasatzen zaio, irabazle ez diren erregistroekin batera (adibidez, ID alternatiboak) bat-etortzeko kalitatea hobetzeko.

1. Beti bat datoz eta inoiz ez datoz bat bikoiztuak kentzeko arauen gainidazteak bat-etortze arau pertsonalizatuak. Bikoztuak kentzeko arau batek bat datozen erregistroak identifikatzen baditu eta bat datorren arau pertsonalizatua erregistro horiekin inoiz bat ez etortzeko ezarrita badago, bi erregistro horiek ez dira bat etorriko.

1. Bat egite prozesua exekutatu ondoren, bikoiztuak kentzeko prozesuaren estatistikak ikusiko dituzu.
   
> [!NOTE]
> Bikoiztuak kentzeko arauak zehaztea ez da derrigorrezkoa. Horrelako araurik konfiguratzen ez bada, sistemak definitutako arauak aplikatuko dira. Balio konbinazio bera (bat-etortze zehatza) gako nagusitik eta bat datozen arauetako eremuak erregistro bakarrean partekatzen dituzten erregistro guztiak biltzen dituzte entitateen datuak entitateen arteko loturari errendimendu hobea eta sistemaren ongizatea lortzeko.

## <a name="run-your-match-order"></a>Egin zure partidaren eskaera

Bat-etortze arauak definitu ondoren, entitateen arteko bat-etortzea eta bikoiztuak kentzeko arauak barne, bat-egiteko eskaera exekutatu dezakezu. Gainean **Bat-etortzea** orria, hautatu **Exekutatu** prozesua hasteko. Bat egiten duen algoritmoak denbora batzuk behar izan ditu osatzeko. Ezin dituzu propietateak aldatu **Bat-etortzea** orria partidako prozesua amaitu arte. Bertan sortu zen bezeroaren profil bateratuko entitatea aurkituko duzu **erakundeak** orria. Zure bezero erakunde bateratua deitzen da **ConflationMatchPairs: CustomerInsights**.

Aldaketa gehigarriak egiteko eta pausoa berriro egiteko, aurrerapen bateratzea bertan behera utzi dezakezu. Aukeratu **Freskagarria ...** testua eta hautatu **Lana bertan behera utzi** behean agertzen den alboko panelean.

Partiduen prozesua amaitutakoan, **Freskagarria ...** testua aldatu egingo da **Arrakastatsua** eta orrialdearen funtzionalitate guztiak berriro erabil ditzakezu.

Lehen partidaren prozesuak entitate maisu bateratu bat sortzen du. Ondorengo norgehiagoka guztiek entitate horren hedapena ekarri dute.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="deduplication-output-as-an-entity"></a>Irteerako bikoiztuak desegiteko entitate gisa
Entitate gurutzatuen parekatze gisa sortutako entitate nagusi bateratuaz gain, bikoiztuak desegiteko prozesuak entitate berri bat sortzen du partidu agindutik bikoiztuak desegiteko erregistroak identifikatzeko. Entitate hauek **ConflationMatchPairs:CustomerInsights** balioarekin batera **Sistema** atalean **Entitateak** orrian, **Deduplication_Datasource_Entity** izenarekin.

Bikoiztuak desegiteko irteerako entitate batek informazio hau dauka:
- IDak eta gakoak
  - Gako nagusiaren eremua eta haren ID ordezkoen eremua. ID alternatiboen eremua erregistro baterako identifikatutako ID alternatibo guztiek osatzen dute.
  - Deduplication_GroupId eremuak zehaztutako bikoiztuak desegiteko eremuetan oinarritutako antzeko erregistro guztiak multzokatzen dituen entitate baten barruan identifikatutako taldea edo klusterra erakusten du. Sistema prozesatzeko helburuarekin erabiltzen da. Eskuzko bikoiztuak desegiteko araurik zehazten ez bada eta sistemak definitutako bikoiztuak desegiteko arauak aplikatzen badira, baliteke eremu hori bikoiztuak desegiteko irteerako entitatean ez aurkitzea.
  - Deduplication_WinnerId: eremu honek identifikatutako talde edo klusterren irabazlearen IDa dauka. Deduplication_WinnerId erregistroaren gako nagusiaren balioaren berdina bada, erregistroa irabazle erregistroa dela esan nahi du.
- Bikoiztuak desegiteko arauak definitzeko erabiltzen diren eremuak.
- Arau eta Puntuazio eremuak bikoiztuak desegiteko arauetatik zein aplikatu den eta bat datorren algoritmoak emandako puntuazioa adierazteko.

## <a name="review-and-validate-your-matches"></a>Berrikusi eta balioztatu partiduak

Ebaluatu zure bikote bikoteen kalitatea eta findu:

- Gainean **Bat-etortzea** orrialdean, bi fitxak aurkituko dituzu zure datuei buruzko hasierako ikuspegi erakusten dutenak.

  - **Bezero bakarrak**: sistemak identifikatutako profil bakarraren kopurua erakusten du.
  - **Bat datozen erregistroak**: zure partida pare guztietan agertzen diren kopurua erakusten du.

- Sarbidean **Loturaren ordena** taulan, partidako bikote bakoitzaren emaitzak ebaluatu ahal izango dituzu partidu-bikoteen entitate honek izan dituen erregistro kopurua alderatuz arrakastaz batutako erregistroen portzentajearekin.

- Sarbidean **arauak** erakundeko atal bat **Loturaren ordena** taulan, arau mailan arrakastaz batutako erregistroen ehunekoa aurkituko duzu. Arau baten ondoko taularen sinboloa hautatuta, erregistro horiek guztiak ikus ditzakezu arau mailan. Erregistroen azpimultzo bat berrikustea gomendatzen dugu, behar bezala egokitu direla egiaztatzeko.

- Zure baldintzen inguruan zehaztasun-atalase desberdinak probatu, balio optimoa identifikatzeko.

  1. Hautatu elipsia (...) esperimentatu nahi duzun bikote pareko araua eta aukeratu **Editatu**.

  2. Hautatu esperimentatzeko erabili nahi duzun baldintza. Irizpide bakoitza errenkada batean irudikatuta dago **Bat-etortzearen araua** panela.

  3. Zer ikusiko duzu **Irizpideen aurrebista** orria baldintza baterako aukeratu duzun zehaztasun mailaren araberakoa da. Aukeratu aukeratutako baldintzaren parekatutako eta parekatu gabeko erregistro kopurua.

     Atalase-maila desberdinen eraginak hobeto ezagutzea. Atalase bakoitzaren azpian zenbat erregistro parekatuko diren konparatu eta erregistroak aukera bakoitzaren azpian ikus ditzakezu. Aukeratu fitxa bakoitza eta aztertu datuak taulako atalean.

## <a name="optimize-your-matches"></a>Optimizatu zure partiduak

Handitu kalitatea zure parekuko parametro batzuk konfiguratuz:

- **Aldatu partidaren ordena** hautatuta **Editatu** eta aldatu partiduen ordenako eremuak.

  > [!div class="mx-imgBorder"]
  > ![Editatu datuekin bat datozen ordena](media/configure-data-match-order-edit.png "Editatu datuekin bat datozen ordena")

- **Aldatu zure arauen ordena** hainbat arau zehaztu badituzu. Partiduen arauak berriro ordenatu ditzakezu **Mugitu gora** eta **Mugitu behera** aukerak partidako arauen sarean.

  > [!div class="mx-imgBorder"]
  > ![Aldatu arauen ordena](media/configure-data-change-rule-order.png "Aldatu arauen ordena")

- **Bikoiztu arauak** bat datorren arau bat zehaztu baduzu eta aldaketekin antzeko araua sortu nahi baduzu. Egin ezazu hautatuta **bikoiztua**.

  > [!div class="mx-imgBorder"]
  > ![Bikoiztu arau bat](media/configure-data-duplicate-rule.png "Bikoiztu arau bat")

- **Desaktibatu arau bat** bat-etortzeko araua gordetzeko, bat etortzeko prozesutik kanpo uzten duen bitartean.

  > [!div class="mx-imgBorder"]
  > ![Desaktibatu arau bat](media/configure-data-deactivate-rule.png "Desaktibatu arau bat")

- **Editatu zure arauak** aukeratuz **Editatu** sinboloa. Hurrengo aldaketa mota hauek aplika ditzakezu:

  - Aldatu egoera baterako atributuak: Hautatu atributu berriak baldintza zehatzen errenkadaren barruan.
  - Aldatu baldintza baten atalasea: doitu zehaztapeneko labaina.
  - Aldatu baldintza normalizazio metodoa: Eguneratu normalizazio metodoa.

## <a name="specify-your-custom-match-records"></a>Zehaztu norberaren bat datozen erregistroak

Zehaztu egin ditzakezu erregistro jakinek beti edo inoiz bat etortzeko baldintzak. Arau hauek neurrira kargatu daitezke partidu prozesura.

1. Hautatu botoia **Norberaren partida** Aukera aukeran **Loturaren ordena** pantaila.

   > [!div class="mx-imgBorder"]
   > ![Sortu bat-etortze pertsonalizatua](media/custom-match-create.png "Sortu bat-etortze pertsonalizatua")

2. Kargatutako entitaterik ez baduzu, berri bat ikusiko duzu **Norberaren partida** Xehetasunak bete behar dituzun elkarrizketa-koadroa. Xehetasun hauek lehenago eman badituzu, joan 8. urratsean.

   > [!div class="mx-imgBorder"]
   > ![Partida pertsonalizatua elkarrizketa-koadro berria](media/custom-match-new-dialog-box.png "Partida pertsonalizatua elkarrizketa-koadro berria")

3. Aukeratu **Txantiloia bete** txantiloien fitxategia lortzeko, erakundeek beti bat etorri edo inoiz bat egin behar duten erregistroak zehazteko. Bi fitxategi desberdinetan "beti bat etorri" erregistroak eta "inoiz ez datoz" erregistroak bete behar dituzu.

4. Txantiloiak entitateak eta entitatearen gako nagusien balioak pertsonalizatutako partidan zehazteko eremuak ditu. Adibidez, Salmenta entitatearen 12345 gako nagusia nahi baduzu, beti harremanetan jarri 34567 gako nagusiarekin harremanetan jartzeko, entitate hau honela zehaztu behar duzu:
    - Entitate1: Salmentak
    - Entitate-gakoa1: 12345
    - Entitatea2: kontaktua
    - Entitate-gakoa2: 34567

   Txantiloi fitxategi berak entitate anitzeko partiden erregistro pertsonalizatuak zehaztu ditzake.
   
   Entitate batean bikoiztuak desegiteko parekatze pertsonalizatua zehaztu nahi baduzu, eman Entitate 1 eta Entitate 2 entitate bera eta ezarri gako primarioen balio desberdinak.

5. Aplikatu nahi dituzun gainidatzi guztiak gehitu ondoren, gorde txantiloiaren fitxategia.

6. Joan hona **Datuak** > **Datu iturburuak** eta txantiloien fitxategiak entitate berri gisa sartu. Iragazi ondoren, bat egin dezakezu Match-ren konfigurazioa zehazteko.

7. Fitxategiak eta erakundeak kargatu ondoren, hautatu hautatu **Norberaren partida** aukera berriro. Aukerak ikusiko dituzu sartu nahi dituzun entitateak zehazteko. Hautatu eskatutako entitateak goitibeherako menuan.

   > [!div class="mx-imgBorder"]
   > ![Pertsonalizatu loturen gainidazketak](media/custom-match-overrides.png "Pertsonalizatu loturen gainidazketak")

8. Hautatu erabili nahi dituzun entitateak **Beti bat etorri** eta **Inoiz ez dator bat** hautatu **Egina**.

9. Aukeratu **Gorde** gainean **Bat-etortzea** konfiguratu berri duzun berdinketaren konfigurazioaren orria.

10. Aukeratu **Exekutatu** gainean **Bat-etortzea** bat datorren orrialdea eta bat datorren pertsonalizazio konfigurazioa indarrean egongo da. Sistemaren bat datozen arauek konfigurazio-multzoa gainidazten dute.

11. Bat egiten denean, egiaztatu dezakezu **ConflationMatchPair** entitatea berrordainketak partiduetan aplikatzen direla baieztatzeko.

## <a name="next-step"></a>Hurrengo urratsa

Partidaren prozesua gutxienez bat bikote egin ondoren, zure datuetan egon daitezkeen kontraesanak konpondu ditzakezu [**konbinatu**](merge-entities.md) Gai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]