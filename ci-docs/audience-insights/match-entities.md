---
title: Lotu entitateak datuak bateratzeko
description: Lotu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 02/07/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-match
- ci-merge
- ci-map
- customerInsights
ms.openlocfilehash: 3c0dd9c417e569ed37d8122c637072893732418a
ms.sourcegitcommit: bb1f9e96023490ab340c114f54200ab4dd48da78
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/02/2022
ms.locfileid: "8372612"
---
# <a name="match-entities"></a>Batu entitateak

Binakako faseak zure datu multzoak bezeroaren profil bateratutako datu multzoa nola konbinatu zehazten du. Osatu ondoren [mapa urratsa](map-entities.md) datuak bateratzeko prozesuan, zure entitateekin bat egiteko prest zaude. Partida faseak gutxienez eskatzen du mapatutako bi erakunde.

Partidaren orrialdeak hiru atal ditu: 
- Bat datozen erregistro kopurua laburbiltzen duten funtsezko metrikak
- Partiduen ordena eta arauak entitateen arteko bat etortzeko
- Partida entitateen birplikazio arauak

## <a name="specify-the-match-order"></a>bat etortzearen ordena zehaztu

Partida bakoitzak bi entitate edo gehiago bateratzen ditu entitate bakar eta bateratu batean. Aldi berean, bezeroaren erregistro bakarrak gordetzen ditu. Bat-etortze-ordenak sistemak erregistroekin bat egiten saiatzen den ordena adierazten du.

> [!IMPORTANT]
> Aukeratzen duzun entitatea lehen entitatea zure datu multzo nagusia bateratzeko oinarria izango da. Partida fasean hautatzen diren entitate osagarriak gehituko zaizkie entitate honi. Horrek ez du esan nahi erakunde bateratuak sartuko duenik *guztiak* entitate honetan sartutako datuen artean.
>
> Bi entitateren hierarkia aukeratzen lagun dezaketen bi gogoeta daude:
>
> - Aukeratu entitate nagusia zure bezeroei buruzko profileko datu osatuena eta fidagarriena duen entitatea.
> - Aukeratu beste entitate batzuekin komunean hainbat atributu dituen entitatea (adibidez, izena, telefono-zenbakia edo helbide elektronikoa) entitate nagusi gisa.

1. Joan **Datuak** > **Bateratu** > **Bat etorri** aukerara eta hautatu **Ezarri ordena** bat-etortzearen fasea hasteko.
1. Hautatu **Entitatearen agindua**. Adibidez, hautatu **eCommerce:eCommerceContacts** entitate nagusi gisa eta **LoyaltyScheme:loyCustomers** bigarren entitate gisa. 
1. Entitateko erregistro guztiak bezero esklusibo gisa eta ondorengo entitate guztiekin bat egiteko, hautatu **Sartu guztiak**.
1. Hautatu **Eginda**. 

Bat-etortze-ordena zehaztu ondoren, definitutako bat-etortze-bikoteak agertzen dira **Bat datozen erregistroen xehetasunak** atalean **Datuak** > **Bateratu** > **Partidua**. Funtsezko neurketak hutsik daude parekatze-prozesua amaitu arte.

:::image type="content" source="media/match-page.png" alt-text="Partiduen orrialdearen pantaila-argazkia datuak bateratzeko prozesuaren bateratu eremuan.":::
  
Entitate nagusia *eCommerce: eCommerceContacts* hurrengo entitatearekin bat dator *LoyaltyScheme: loyCustomers*. Lehenengo bat-etortze-urratsetik ateratzen den datu-multzoa hurrengo entitatearekin bat dator bi entitate baino gehiago badituzu.

## <a name="define-rules-for-match-pairs"></a>Partiduen bikoteen arauak zehaztu

Bat egiten duten arauek entitate pare bat lotuko den logika zehazten dute.

**Arauak behar ditu** Entitate baten izenaren ondoan abisatzeak iradokitzen du ez dela bat datorren araurik zehazten pare batentzat. 

:::image type="content" source="media/match-rule-add.png" alt-text="Partiduen erregistroaren xehetasunen atalaren pantaila-argazkia kontrolarekin nabarmendutako arauak gehitzeko.":::

1. Hautatu **Gehitu araua** entitate baten pean **Bat datozen erregistroen xehetasunak** atala partida-arauak definitzeko.

1. Hurrengoan **Sortu araua** panelean, konfiguratu arauaren baldintzak.

   :::image type="content" source="media/match-rule-conditions.png" alt-text="Irekitako partida arau baten pantaila-argazkia baldintzak gehituta.":::

   - **Entitatea / Eremua (lehen ilara)**: Aukeratu erlazionatutako entitate bat eta atributu bat bezeroarentzako litekeena den erregistro propietatea zehazteko. Adibidez, telefono zenbaki bat edo helbide elektronikoa. Saihestu jarduera motako atributuen arabera parekatzea. Esate baterako, erosketa IDak ez du bat-etortzerik izango beste erregistro mota batzuetan.

   - **Entitatea / eremua (bigarren ilara)**: Aukeratu lehen errenkadan zehaztutako entitatearen atributuarekin erlazionatutako atributu bat.

   - **Normalizatu**: Aukeratu hautatutako atributuen normalizazio aukera hauetatik. 
     - Zenbakiak: beste zenbaki sistema batzuk, hala nola zenbaki erromatarrak, zenbaki arabiar bihurtzen ditu. *VIII* bihurtzen *8*.
     - Sinboloak: sinbolo eta karaktere berezi guztiak kentzen ditu. *Burua eta Sorbalda* bihurtzen da *HeadShoulder*.
     - Testua minuskulara: karaktere guztiak minuskulara bihurtzen ditu. *MAIUSU GUZTIAK eta Izenburua* bihurtzen da *maiuskula guztiak eta izenburua*.
     - Mota (Telefonoa, Izena, Helbidea, Erakundea): izenak, izenburuak, telefono zenbakiak, helbideak, etab. 
     - Unicode ASCII: Unicode notazioa ASCII karaktere bihurtzen du. */u00B2* bihurtzen da *2*.
     - Espazio zuria: espazio guztiak ezabatzen ditu. *Kaixo   Mundua* bihurtzen da *KaixoMundua*.

   - **Zehaztasuna**: zehaztu baldintza hau aplikatzeko zehaztasun maila. 
     - **Oinarrizkoa**: aukeratu *Baxua*, *Ertaina*, *Altua*, eta *Zehazki*. Hautatu **Zehatza** ehuneko 100ean bat datozen erregistroak soilik lotzeko. Hautatu beste maila bat ehuneko 100 berdin-berdina ez duten erregistroekin bat etor dadin.
     - **Pertsonalizatua**: ezarri erregistroek bat etorri behar duten ehunekoa. Sistemak atalase hori gainditzen duten erregistroak baino ez ditu bat etorriko.

1. Eman **Izena** araurako.

1. [Gehitu baldintza gehiago](#add-conditions-to-a-rule) edo hautatu **Eginda** araua amaitzeko.

1. Aukeran [gehitu arau gehiago](#add-rules-to-a-match-pair).

1. Aldaketak aplikatzeko, hautatu **Gorde**.

### <a name="add-conditions-to-a-rule"></a>Gehitu baldintzak araura

Entitateekin parekatzeko atributuek baldintza anitz betetzen badituzte, gehitu baldintza gehiago parekatze arau bati. Baldintzak AND operadore logikoarekin lotuta daude eta, beraz, baldintza guztiak betetzen badira soilik exekutatzen dira.

1. Joan **Datuak** > **Bat egin** > **Partidua** eta hautatu **Editatu** baldintzak gehitu nahi dituzun arauan.

1. Sarbidean **Editatu araua** hautatu panela **Gehitu baldintza**.

1. Hautatu **Egina** araua gordetzeko.

### <a name="add-rules-to-a-match-pair"></a>Gehitu arauak partida bikoteari

Partiduen arauek baldintza multzoak adierazten dituzte. Entitateak hainbat atribututan oinarritutako baldintzen arabera lotzeko, gehitu arau gehiago.

1.  Joan **Datuak** > **Bat egin** > **Partidua** eta hautatu **Gehitu araua** entitatean gehitu nahi dituzun arauan.

2. Jarraitu urratsak [Partiduen bikoteen arauak zehaztu](#define-rules-for-match-pairs).

> [!NOTE]
> Arauen ordena garrantzitsua da. Bat datorren algoritmoa zure lehen arauaren arabera bat egiten saiatzen da eta bigarren araura jarraitzen du lehen arauarekin bat-etortzerik identifikatu ez bada bakarrik.

### <a name="change-the-entity-order-in-match-rules"></a>Aldatu entitateen ordena partiduen arauetan

Parekatze-arauetarako entitateak berrantola ditzakezu prozesatzen diren ordena aldatzeko. Ordena aldatu delako gatazkatsuak diren arauak kenduko dira. Kendutako arauak birsortu behar dituzu konfigurazio eguneratuarekin.

1. Joan **Datuak** > **Bat egin** > **Bat-etortzea** eta hautatu **Editatu**.

1. **Editatu araua** panelean, hautatu **Mugitu gora edo behera** kontrolatu edo arrastatu eta askatu entitateak ordena aldatzeko.

   :::image type="content" source="media/reorder-match-rules.png" alt-text="Partiduen fasean eskaera-entitateak zein prozesutan prozesatzen diren aldatzeko aukerak.":::

1. Hautatu **Egina** araua gordetzeko.

## <a name="define-deduplication-on-a-match-entity"></a>Definitu bikoiztuak kentzea bat datorren entitate batean

Horrez gain [entitateen arteko partida arauak](#define-rules-for-match-pairs), desduplikazio arauak ere zehaz ditzakezu. *Desplikazioa* erregistroak parekatzerakoan beste prozesu bat da. Erregistro bikoiztuak identifikatzen ditu eta erregistro bakarrean bateratzen ditu. Iturburu erregistroak bateratutako erregistroarekin lotzen dira ID ordezkoekin.

Bikoiztutako erregistroak entitateen arteko parekatze-prozesuan erabiltzen dira. Desduplicazioa entitate indibidualetan gertatzen da eta partida-bikoteetan erabiltzen den entitate guztietan konfigura daiteke.

Bikoiztuak kentzeko arauak zehaztea ez da derrigorrezkoa. Horrelako araurik konfiguratzen ez bada, sistemak definitutako arauak aplikatuko dira. Erregistro guztiak erregistro bakarrean konbinatzen dituzte entitatearen datuak entitateen arteko parekatzera pasa aurretik errendimendu hobea lortzeko.

### <a name="add-deduplication-rules"></a>Gehitu bikoiztuak kentzeko arauak

1. Joan **Datuak** > **Bateratu** > **Bat egin**.

1. urtean **Desbikoiztutako erregistroen xehetasunak** atalean, hautatu **Ezarri entitateak**. Desduplikazio arauak dagoeneko sortuta badaude, hautatu **Editatu**.

1. **Konbinatu hobespenak** panelean, hautatu bikoiztuak kentzea exekutatu nahi diezun entitateak.

   1. Zehaztu erregistro bikoiztuak nola konbinatu eta aukeratu hiru bateratze aukeretako bat:
      - **Beteen daudenak** : Betetako atributu eremueak gehien dituen erregistroa identifikatzen du erregistro nagusi gisa. Hori da konbinatzeko aukera lehenetsia.
      - **Berrienak**: erregistro nagusia identifikatzen du berritasunen arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.
      - **Zaharrenak**: erregistro nagusia identifikatzen du zahartasunaren arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.

   1. Aukeran, entitate baten atributu indibidualetan deduplicazio-arauak definitzeko, hautatu **Aurreratua**. Adibidez, posta elektroniko berriena ETA helbiderik osatuena erregistro ezberdinetatik gordetzea aukera dezakezu. Zabaldu entitatea bere atributu guztiak ikusteko eta zein aukera erabili atributu indibidualetarako. Azkenaldian oinarritutako aukera bat aukeratzen baduzu, berritasuna definitzen duen data/orduaren eremua ere zehaztu behar duzu. 
 
      > [!div class="mx-imgBorder"]
      > ![Bikoiztuak kentzeko arauak, 1. urratsa.](media/match-selfconflation.png "Bikoiztuak kentzeko arauak, 1. urratsa")

   1. Hautatu **Eginda** desduplicaziorako zure bateratze-hobespenak aplikatzeko.
 
1. Entitateak hautatuta eta haien konbinatze-hobespenak zehaztutakoan, hautatu **Gehitu araua** entitate mailan bikoiztuak kentzeko arauak definitzeko.
   - **Aukeratu eremua** entitate horretatik eskuragarri dauden eremu guztiak zerrendatzen ditu. Aukeratu eremuak bikoiztuak diren egiaztatu nahi duzun eremua. Aukeratu bezero bakoitzarentzat litekeena den eremua. Adibidez, helbide elektronikoa edo izena, hiria eta telefono zenbakiaren konbinazioa.
   - Zehaztu normalizazio eta zehaztasun ezarpenak.
   - Definitu baldintza gehiago **Gehitu baldintza** aukeratuz.
 
   > [!div class="mx-imgBorder"]
   > ![Bikoiztuak kentzeko arauak, 2. urratsa.](media/match-selfconflation-rules.png "Bikoiztuak kentzeko arauak, 2. urratsa")

  Entitate berarako hainbat bikoiztuak kentzeko arau sor ditzakezu. 

1. Bat-egite prozesua exekutatzeak erregistroak taldekatzen ditu bikoiztuak kentzeko arauetan zehaztutako baldintzetan oinarrituta. Erregistroak taldekatu ondoren, bat-egiteen gidalerroa aplikatzen da erregistro nagusia identifikatzeko.

1. Irabazle erregistro hori entitateen arteko bat-etortzeari pasatzen zaio, irabazle ez diren erregistroekin batera (adibidez, ID alternatiboak) bat-etortzeko kalitatea hobetzeko.

1. Partiduen arau pertsonalizatuek definitutako desduplikazio arauak gainidatzi egiten dituzte. Bikoztuak kentzeko arau batek bat datozen erregistroak identifikatzen baditu eta bat datorren arau pertsonalizatua erregistro horiekin inoiz bat ez etortzeko ezarrita badago, bi erregistro horiek ez dira bat etorriko.

1. Ondoren [partida-prozesua martxan jartzea](#run-the-match-process), desduplicazioaren estatistikak ikusiko dituzu neurketa gakoen lauzetan.

### <a name="deduplication-output-as-an-entity"></a>Irteerako bikoiztuak desegiteko entitate gisa

Desplikazio prozesuak entitate berri bat sortzen du entitate bakoitzarentzako pareko bikoteetatik desplikatutako erregistroak identifikatzeko. Entitate hauek **ConflationMatchPairs:CustomerInsights** balioarekin batera **Sistema** atalean **Entitateak** orrian, **Deduplication_DataSource_Entity** izenarekin.

Bikoiztuak desegiteko irteerako entitate batek informazio hau dauka:
- IDak eta gakoak
  - Gako nagusiaren eremua eta haren ID ordezkoen eremua. ID alternatiboen eremua erregistro baterako identifikatutako ID alternatibo guztiek osatzen dute.
  - Deduplication_GroupId eremuak zehaztutako bikoiztuak desegiteko eremuetan oinarritutako antzeko erregistro guztiak multzokatzen dituen entitate baten barruan identifikatutako taldea edo klusterra erakusten du. Sistema prozesatzeko helburuarekin erabiltzen da. Eskuzko bikoiztuak desegiteko araurik zehazten ez bada eta sistemak definitutako bikoiztuak desegiteko arauak aplikatzen badira, baliteke eremu hori bikoiztuak desegiteko irteerako entitatean ez aurkitzea.
  - Deduplication_WinnerId: eremu honek identifikatutako talde edo klusterren irabazlearen IDa dauka. Deduplication_WinnerId erregistroaren gako nagusiaren balioaren berdina bada, erregistroa irabazle erregistroa dela esan nahi du.
- Bikoiztuak desegiteko arauak definitzeko erabiltzen diren eremuak.
- Arau eta Puntuazio eremuak bikoiztuak desegiteko arauetatik zein aplikatu den eta bat datorren algoritmoak emandako puntuazioa adierazteko.
 
## <a name="include-enriched-entities-preview"></a>Sartu entitate aberastuak (aurrebista)

datu-iturburu mailan entitateak aberastu badituzu, hautatu itzazu parekatze-prozesua exekutatu aurretik. Entitate aberastuek zure bateratzearen emaitzak hobe ditzakete. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md). 

1. Joan **Datuak** > **Bateratu** > **Partidua** eta hautatu **Erabili entitate aberastuak** orriaren goialdean.

1. Tik **Erabili entitate aberastuak** panela, aukeratu entitate aberastu bat edo gehiago.

1. Hautatu **Eginda**. Iturburu-entitatea erabiltzen den lekuan (adibidez, bat-etortze-ordena edo arauak), automatikoki entitate aberastura aldatzen da.
  
## <a name="run-the-match-process"></a>Bat-egite prozesua burutu

Bat-etortze arauak konfiguratutakoak, entitateen arteko bat-etortzea eta bikoiztuak kentzeko arauak barne, bat-egiteko prozesua exekutatu dezakezu. 

Joan **Datuak** > **Bateratu** > **Bat egin** eta hautatu **Korrika egin** prozesua hasteko. Bat datorren algoritmoak denbora pixka bat behar du osatzeko eta ezin duzu konfigurazioa aldatu osatu arte. Aldaketak egiteko, ezezta dezakezu exekutatzea. Aukeratu lanaren egoera eta hautatu **Utzi lana** gainean **Aurrerapenaren xehetasunak** panela.

Exekuzio arrakastatsuaren emaitza, bezeroaren profileko entitate bateratua, aurkituko duzu **Entitateak** orrialdea. Zure bezero bateratutako entitateari deitzen zaio **Bezeroak** hurrengoan **Profilak** atala. Partida arrakastatsuaren lehenengo lasterketak bateratua sortzen du *Bezeroa* entitatea. Ondorengo partida guztiekin entitate hori zabaltzen da.

[!INCLUDE [progress-details-include](../includes/progress-details-pane.md)]

## <a name="review-and-validate-your-matches"></a>Berrikusi eta balioztatu partiduak

Joan **Datuak** > **Bateratu** > **Bat egin** zure bikoteen kalitatea ebaluatzeko eta beharrezkoa izanez gero hobetzeko.

Orriaren goialdeko fitxek gako-metrikak erakusten dituzte, bat datozen erregistroen eta bikoiztuen kopurua laburbilduz.

:::image type="content" source="media/match-KPIs.png" alt-text="Partiduen orriko gakoen neurrien pantaila moztua zenbakiekin eta xehetasunekin.":::

- **Iturri erregistro bakarrak** azken partidako exekuzioan prozesatutako banako iturrien erregistro kopurua erakusten du.
- **Partiduen eta ez datozen erregistroak** Partidaren arauak prozesatu ondoren zenbat erregistro bakarra geratzen diren nabarmentzen du.
- **Erregistro parekatuak soilik** zure bikote bikote guztien partida kopurua erakusten du.

Partida bakoitzaren emaitzak eta bere arauak ebaluatu ditzakezu **Erregistroen xehetasunak** mahaia. Konparatu partida bikotetik ateratako erregistro kopurua behar bezala parekatutako erregistroen ehunekoarekin.

Berrikusi partida bikote baten arauak arau mailan arrakastaz bat datozen erregistroen ehunekoa ikusteko. Aukeratu elipsia (...) eta hautatu **Partidaren aurrebista** erregistro horiek guztiak arau mailan ikusteko. Erregistro batzuei begirada bat ematea gomendatzen dizugu, ondo egokitu direla egiaztatzeko.

Saiatu baldintzetan zehaztasun atalase desberdinetan balio optimoa aurkitzeko.

  1. Aukeratu elipsia (...) esperimentatu nahi duzun arauaren eta hautatu **Editatu**.

  2. Aldatu zehaztasunen balioak berrikusi nahi dituzun baldintzetan.

  3. Aukeratu **Aurrebista** beraz, ikusi hautatutako egoerarekin bat datozen eta parekatutako erregistro kopurua.

## <a name="manage-match-rules"></a>Kudeatu bat egiteko arauak

Partiduen parametro gehienak birkonfigura eta doitu ditzakezu.

:::image type="content" source="media/match-rules-management.png" alt-text="Goitibeherako menuaren pantaila bat etortzeko arauen aukerekin.":::

- **Aldatu zure arauen ordena** hainbat arau zehaztu badituzu. Partiduen arauak berrantola ditzakezu **Mugitu gora** eta **Mugitu Behera** aukerak edo arrastatu eta jaregin.

- **Aldatu arauen baldintzak** hautatuz **Editatu** eta aukeratu eremu desberdinak.

- **Desaktibatu arau bat** bat-etortzeko araua gordetzeko, bat etortzeko prozesutik kanpo uzten duen bitartean.

- **Bikoiztu zure arauak** bat datorren araua zehaztu baduzu eta antzeko arau bat aldaketekin sortu nahi baduzu, hautatu **Bikoiztu**.

- **Ezabatu arau bat** hautatu **Ezabatu** ikurra.

## <a name="advanced-options"></a>Aukera aurreratuak

### <a name="add-exceptions-to-a-rule"></a>Gehitu salbuespenak arau bati

Kasu gehienetan, entitateen parekatzeak datu bateratuak dituzten erabiltzaile-profil bakarrak eramaten ditu. Positibo faltsuen eta negatibo faltsuen kasu bakanak modu dinamikoan zuzentzeko, bat-etortze-arau baterako salbuespenak defini ditzakezu. Salbuespenak bat-etortze-arauak prozesatu ondoren aplikatzen dira eta salbuespen-irizpideak betetzen dituzten erregistro guztiak bat etortzea saihesten da.

Adibidez, zure parekatze-arauak abizen, hiria eta jaioteguna konbinatzen baditu, sistemak profil berdinarekin bizi diren abizen bera duten bikiak identifikatuko lituzke. Profilekin bat ez datorren salbuespen bat zehaztu dezakezu konbinatzen dituzun entitateetako izen berdinak ez badira.

1. Joan **Datuak** > **Bat egin** > **Partidua** eta hautatu **Editatu** baldintzak gehitu nahi dituzun arauan.

1. urtean **Editatu araua** panela, hautatu **Gehitu salbuespena**.

1. Zehaztu salbuespen irizpideak. 

1. Hautatu **Egina** araua gordetzeko.

### <a name="specify-custom-match-conditions"></a>Zehaztu pertsonalizatutako bat etortzeko baldintzak

Bat-etortze-logika lehenetsia gainidazten duten baldintzak zehaztu ditzakezu. Lau aukera daude eskuragarri: 

|Aukera  |Deskribapenak |Adibidez  |
|---------|---------|---------|
|Beti bat etorri behar du     | Beti bat datozen balioak definitzen ditu.         |  Beti lotu *Mikel* eta *MikeR*.       |
|Ez du inoiz bat etorri behar     | Inoiz bat ez datozen balioak definitzen ditu.        | Inoiz ez parekatu *Joan* eta *Jonathan*.        |
|Salbuespen pertsonalizatua     | Partida-fasean sistemak beti alde batera utzi behar dituen balioak zehazten ditu. |  Ez ikusi balioei *11111* eta *Ezezaguna* partidan zehar.        |
|Aliasen esleipena    | Sistemak balio berdintzat hartu behar dituen balioak definitzea.         | Kontuan hartu *Joe* berdina izateko *Joseph*.        |

1. Joan **Datuak** > **Bateratu** > **Bat egin** eta hautatu **Bat-egite pertsonalizatua** hurrengoan **Erregistroen xehetasunak** atala.

   :::image type="content" source="media/custom-match-create.png" alt-text="Bat-egitearen arauen sekzioak bat-egite pertsonalizatuaren kontrolak nabarmenduta pantaila-argazkia.":::

1. urtean **Pertsonalizatua** panela, joan **Erregistroak** fitxa.

1. Aukeratu bat-etortze pertsonalizatua aukera **Mota pertsonalizatua** goitibeherako eta hautatu **Deskargatu txantiloia**. Bat-etortze-aukera bakoitzerako txantiloi bat behar duzu.

1. Ireki deskargatutako txantiloi fitxategia eta bete xehetasunak. Txantiloiak entitateak eta entitatearen gako nagusien balioak pertsonalizatutako partidan zehazteko eremuak ditu. Adibidez, gako nagusia nahi baduzu *12345* hurrengotik *Salmentak* entitatea beti lehen mailako gakoarekin bat etortzeko *34567* hurrengotik *Harremanetarako* entitatea, bete txantiloia:
    - Entitate1: Salmentak
    - Entitate-gakoa1: 12345
    - Entitatea2: kontaktua
    - Entitate-gakoa2: 34567

   Txantiloi fitxategi berak entitate anitzeko partiden erregistro pertsonalizatuak zehaztu ditzake.
   
   Entitate batean bikoiztuak desegiteko parekatze pertsonalizatua zehaztu nahi baduzu, eman Entitate 1 eta Entitate 2 entitate bera eta ezarri gako primarioen balio desberdinak.

1. Gainbatze guztiak gehitu ondoren, gorde txantiloi fitxategia.

1. Joan hona **Datuak** > **Datu iturburuak** eta txantiloien fitxategiak entitate berri gisa sartu.

1. Fitxategiak eta erakundeak kargatu ondoren, hautatu hautatu **Norberaren partida** aukera berriro. Aukerak ikusiko dituzu sartu nahi dituzun entitateak zehazteko. Hautatu goitibeherako menuan beharrezko entitateak eta hautatu **Eginda**.

   :::image type="content" source="media/custom-match-overrides.png" alt-text="Elkarrizketa-koadroaren pantaila bat etortze pertsonalizatuko agertoki baterako gainidatziak aukeratzeko.":::

1. Parekatze pertsonalizatua aplikatzea erabili nahi duzun bat-etortze-aukeraren araberakoa da. 

   - Izan ere **Beti lotu** edo **Inoiz ez parekatu**, jarraitu hurrengo urratsera.
   - Izan ere **Saihesbide pertsonalizatua** edo **Aliasaren mapaketa**, hautatu **Editatu** lehendik dagoen bat-etortze-arau batean edo sortu arau berri bat. Normalizazioak goitibeherako aukeran, aukeratu **Saihesbide pertsonalizatua** edo **Aliasaren mapaketa** aukera eta hautatu **Eginda**.

1. Aukeratu **Gorde** gainean **Bat egin** orrialdea bat datorren konfigurazio pertsonalizatua aplikatzeko.

1. Aukeratu **Exekutatu** gainean **Bat egin** orrialdea parekatze prozesua hasteko. Partiduen zehaztapeneko beste arau batzuk pertsonalizatutako konfigurazio pertsonalizatuaren gainetik daude.

#### <a name="known-issues"></a>Ohiko konfigurazio-arazoak

- Auto-konflazioak ez ditu datu normalizatuak erakusten deduplicazio-entitateetan. Hala ere, normalizazioa barnetik aplikatzen du deduplicazioan. Normalizazio guztietarako diseinatuta dago. 
- Mota semantikoen ezarpena kentzen bada **Mapa** bat-etortze-arau batek Alias-mapping edo Saihesbide pertsonalizatua erabiltzen duenean, normalizazioa ez da aplikatuko. Bat-etortze-arauan normalizazioa konfiguratu ondoren mota semantikoa garbitzen baduzu bakarrik gertatzen da, mota semantikoa ezezaguna izango delako.


## <a name="next-step"></a>Hurrengo urratsa

Gutxienez partida-bikote baten partida-prozesua amaitu ondoren, jarraitu [**Batu**](merge-entities.md) urratsa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
