---
title: Lotu entitateak datuak bateratzeko
description: Lotu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 02/23/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 50b11e7d6f62d7a25eb25a0f2b1c4ad7d859def1
ms.sourcegitcommit: 0b754d194d765afef70d1008db7b347dd1f0ee40
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306013"
---
# <a name="match-entities"></a>Batu entitateak

Binakako faseak zure datu multzoak bezeroaren profil bateratutako datu multzoa nola konbinatu zehazten du. Osatu ondoren [mapa urratsa](map-entities.md) datuak bateratzeko prozesuan, zure entitateekin bat egiteko prest zaude. Partida faseak gutxienez eskatzen du mapatutako bi erakunde.

Partidaren orrialdeak hiru atal ditu: 
- Bat datozen erregistro kopurua laburbiltzen duten funtsezko metrikak
- Partiduen ordena eta arauak entitateen arteko bat etortzeko
- Partida entitateen birplikazio arauak

## <a name="specify-the-match-order"></a>bat etortzearen ordena zehaztu

Joan **Datuak** > **Bateratu** > **Bat etorri** aukerara eta hautatu **Ezarri ordena** bat-etortzearen fasea hasteko.

Partida bakoitzak bi entitate edo gehiago bateratzen ditu entitate bakar eta bateratu batean. Aldi berean, bezeroaren erregistro bakarrak gordetzen ditu. Adibidez, bi entitate hautatu ditugu: **eCommerce: eCommerceContacts** lehen entitate gisa eta **LoyaltyScheme: loyCustomers** bigarren entitate gisa. Entitateen ordenak sistema zein erregistroekin bat egiten saiatuko den zehazten du.

:::image type="content" source="media/match-page.png" alt-text="Partiduen orrialdearen pantaila-argazkia datuak bateratzeko prozesuaren bateratu eremuan.":::
  
Entitate nagusia *eCommerce: eCommerceContacts* hurrengo entitatearekin bat dator *LoyaltyScheme: loyCustomers*. Partiduen lehen urratsetik ateratako datu multzoa hurrengo entitatearekin bat dator bi entitate baino gehiago badituzu.

> [!IMPORTANT]
> Aukeratzen duzun entitatea lehen entitatea zure datu multzo nagusia bateratzeko oinarria izango da. Partida fasean hautatzen diren entitate osagarriak gehituko zaizkie entitate honi. Horrek ez du esan nahi erakunde bateratuak sartuko duenik *guztiak* entitate honetan sartutako datuen artean.
>
> Bi entitateren hierarkia aukeratzen lagun dezaketen bi gogoeta daude:
>
> - Aukeratu entitate nagusia zure bezeroei buruzko profileko datu osatuena eta fidagarriena duen entitatea.
> - Aukeratu beste entitate batzuekin (adibidez, izena, telefono zenbakia edo helbide elektronikoa) beste atributu batzuk dituzten entitatea lehen mailako entitate gisa.

Partiduen ordena zehaztu ondoren, definitutako partidu bikoteak ikusiko dituzu **Erregistroen xehetasunak** atalean **Datuak** > **Bat egin** > **Partidua**. Gako-metrikak hutsik egongo dira partida prozesua amaitu arte.

## <a name="define-rules-for-match-pairs"></a>Partiduen bikoteen arauak zehaztu

Bat egiten duten arauek entitate pare bat lotuko den logika zehazten dute.

**Arauak behar ditu** Entitate baten izenaren ondoan abisatzeak iradokitzen du ez dela bat datorren araurik zehazten pare batentzat. 

:::image type="content" source="media/match-rule-add.png" alt-text="Partiduen erregistroaren xehetasunen atalaren pantaila-argazkia kontrolarekin nabarmendutako arauak gehitzeko.":::

1. Aukeratu **Gehitu arauak** entitate baten menpe **Erregistroen xehetasunak** partida arauak definitzeko atala.

1. Hurrengoan **Sortu araua** panelean, konfiguratu arauaren baldintzak.

   :::image type="content" source="media/match-rule-conditions.png" alt-text="Irekitako partida arau baten pantaila-argazkia baldintzak gehituta.":::

   - **Entitatea / Eremua (lehen ilara)**: Aukeratu erlazionatutako entitate bat eta atributu bat bezeroarentzako litekeena den erregistro propietatea zehazteko. Adibidez, telefono zenbaki bat edo helbide elektronikoa. Saihestu jarduera motako atributuen arabera parekatzea. Esate baterako, erosketa IDak ez du bat-etortzerik izango beste erregistro mota batzuetan.

   - **Entitatea / eremua (bigarren ilara)**: Aukeratu lehen errenkadan zehaztutako entitatearen atributuarekin erlazionatutako atributu bat.

   - **Normalizatu**: Aukeratu hautatutako atributuen normalizazio aukera hauetatik. 
     - Espazio zuria: espazio guztiak ezabatzen ditu. *Kaixo   Mundua* bihurtzen da *KaixoMundua*.
     - Sinboloak: sinbolo eta karaktere berezi guztiak kentzen ditu. *Burua eta Sorbalda* bihurtzen da *HeadShoulder*.
     - Testua minuskulara: karaktere guztiak minuskulara bihurtzen ditu. *MAIUSU GUZTIAK eta Izenburua* bihurtzen da *maiuskula guztiak eta izenburua*.
     - Unicode ASCII: Unicode notazioa ASCII karaktere bihurtzen du. */u00B2* bihurtzen da *2*.
     - Zenbakiak: beste zenbaki sistema batzuk, hala nola zenbaki erromatarrak, zenbaki arabiar bihurtzen ditu. *VIII* bihurtzen *8*.
     - Mota semantikoak: izenak, izenburuak, telefono zenbakiak, helbideak eta abar normalizatzen ditu. 

   - **Zehaztasuna**: zehaztu baldintza hau aplikatzeko zehaztasun maila. 
     - **Oinarrizkoa**: aukeratu *Baxua*, *Ertaina*, *Altua*, eta *Zehazki*. Aukeratu **zehatza** Ehuneko 100 bat datozen erregistroak soilik lotzeko. Hautatu beste maila bat ehuneko 100 berdin-berdina ez duten erregistroekin bat etor dadin.
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

Partiduen arauek baldintza multzoak adierazten dituzte. Entitateak batzeko baldintzetan oinarrituz atributu anitzetan, gehitu arau gehiago

1.  Joan **Datuak** > **Bat egin** > **Partidua** eta hautatu **Gehitu araua** entitatean gehitu nahi dituzun arauan.

2. Jarraitu urratsak [Partiduen bikoteen arauak zehaztu](#define-rules-for-match-pairs).

> [!NOTE]
> Arauen ordena garrantzitsua da. Bat datorren algoritmoa zure lehen arauaren arabera bat egiten saiatzen da eta bigarren araura jarraitzen du lehen arauarekin bat-etortzerik identifikatu ez bada bakarrik.

### <a name="change-the-entity-order-in-match-rules"></a>Aldatu entitateen ordena partiduen arauetan

Partiduen arauen entitateak berrantola ditzakezu prozesatutako ordena aldatzeko. Ordena aldatu delako gatazkatsuak diren arauak kenduko dira. Kendutako arauak birsortu behar dituzu konfigurazio eguneratuarekin.

1. Joan **Datuak** > **Bat egin** > **Bat-etortzea** eta hautatu **Editatu**.

1. **Editatu araua** panelean, hautatu **Mugitu gora edo behera** kontrolatu edo arrastatu eta askatu entitateak ordena aldatzeko.

   :::image type="content" source="media/reorder-match-rules.png" alt-text="Partiduen fasean eskaera-entitateak zein prozesutan prozesatzen diren aldatzeko aukerak.":::

1. Hautatu **Egina** araua gordetzeko.

## <a name="define-deduplication-on-a-match-entity"></a>Definitu bikoiztuak kentzea bat datorren entitate batean

Horrez gain [entitateen arteko partida arauak](#define-rules-for-match-pairs), desduplikazio arauak ere zehaz ditzakezu. *Desplikazioa* erregistroak parekatzerakoan beste prozesu bat da. Erregistro bikoiztuak identifikatzen ditu eta erregistro bakarrean bateratzen ditu. Iturburu erregistroak bateratutako erregistroarekin lotzen dira ID ordezkoekin.

Bikoiztutako erregistroak entitateen arteko bat-etortze prozesuan erabiliko da. Desplikazioa entitate indibidualetan gertatzen da eta partida bikoteetan erabilitako entitate guztiak konfigura daitezke.

Bikoiztuak kentzeko arauak zehaztea ez da derrigorrezkoa. Horrelako araurik konfiguratzen ez bada, sistemak definitutako arauak aplikatuko dira. Erregistro guztiak erregistro bakarrean konbinatzen dituzte entitatearen datuak entitateen arteko parekatzera pasa aurretik errendimendu hobea lortzeko.

### <a name="add-deduplication-rules"></a>Gehitu bikoiztuak kentzeko arauak

1. Joan **Datuak** > **Bateratu** > **Bat egin**.

1. **Konbinatutako bikoiztuak** atalean, hautatu **Ezarri entitateak**. Desduplikazio arauak dagoeneko sortuta badaude, hautatu **Editatu**.

1. **Konbinatu hobespenak** panelean, hautatu bikoiztuak kentzea exekutatu nahi diezun entitateak.

1. Zehaztu erregistro bikoiztuak nola konbinatu eta aukeratu hiru bateratze aukeretako bat:
   - **Beteen daudenak** : Betetako atributu eremueak gehien dituen erregistroa identifikatzen du erregistro nagusi gisa. Hori da konbinatzeko aukera lehenetsia.
   - **Berrienak**: erregistro nagusia identifikatzen du berritasunen arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.
   - **Zaharrenak**: erregistro nagusia identifikatzen du zahartasunaren arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.
 
   > [!div class="mx-imgBorder"]
   > ![Bikoiztuak kentzeko arauak, 1. urratsa](media/match-selfconflation.png "Bikoiztuak kentzeko arauak, 1. urratsa")
 
1. Entitateak hautatuta eta haien konbinatze-hobespenak zehaztutakoan, hautatu **Gehitu araua** entitate mailan bikoiztuak kentzeko arauak definitzeko.
   - **Aukeratu eremua** entitate horretatik eskuragarri dauden eremu guztiak zerrendatzen ditu. Aukeratu eremuak bikoiztuak diren egiaztatu nahi duzun eremua. Aukeratu bezero bakoitzarentzat litekeena den eremua. Adibidez, helbide elektronikoa edo izena, hiria eta telefono zenbakiaren konbinazioa.
   - Zehaztu normalizazio eta zehaztasun ezarpenak.
   - Definitu baldintza gehiago **Gehitu baldintza** aukeratuz.
 
   > [!div class="mx-imgBorder"]
   > ![Bikoiztuak kentzeko arauak, 2. urratsa](media/match-selfconflation-rules.png "Bikoiztuak kentzeko arauak, 2. urratsa")

  Entitate berarako hainbat bikoiztuak kentzeko arau sor ditzakezu. 

1. Bat-egite prozesua exekutatzeak erregistroak taldekatzen ditu bikoiztuak kentzeko arauetan zehaztutako baldintzetan oinarrituta. Erregistroak taldekatu ondoren, bat-egiteen gidalerroa aplikatzen da erregistro nagusia identifikatzeko.

1. Irabazle erregistro hori entitateen arteko bat-etortzeari pasatzen zaio, irabazle ez diren erregistroekin batera (adibidez, ID alternatiboak) bat-etortzeko kalitatea hobetzeko.

1. Partiduen arau pertsonalizatuek definitutako desduplikazio arauak gainidatzi egiten dituzte. Bikoztuak kentzeko arau batek bat datozen erregistroak identifikatzen baditu eta bat datorren arau pertsonalizatua erregistro horiekin inoiz bat ez etortzeko ezarrita badago, bi erregistro horiek ez dira bat etorriko.

1. Ondoren, [exekutatuz bat-egite prozesua](#run-the-match-process), bikoiztuak kentzeko prozesuaren estatistikak ikusiko dituzu gako neurketen lauzetan.

### <a name="deduplication-output-as-an-entity"></a>Irteerako bikoiztuak desegiteko entitate gisa

Desplikazio prozesuak entitate berri bat sortzen du entitate bakoitzarentzako pareko bikoteetatik desplikatutako erregistroak identifikatzeko. Entitate hauek **ConflationMatchPairs:CustomerInsights** balioarekin batera **Sistema** atalean **Entitateak** orrian, **Deduplication_DataSource_Entity** izenarekin.

Bikoiztuak desegiteko irteerako entitate batek informazio hau dauka:
- IDak eta gakoak
  - Gako nagusiaren eremua eta haren ID ordezkoen eremua. ID alternatiboen eremua erregistro baterako identifikatutako ID alternatibo guztiek osatzen dute.
  - Deduplication_GroupId eremuak zehaztutako bikoiztuak desegiteko eremuetan oinarritutako antzeko erregistro guztiak multzokatzen dituen entitate baten barruan identifikatutako taldea edo klusterra erakusten du. Sistema prozesatzeko helburuarekin erabiltzen da. Eskuzko bikoiztuak desegiteko araurik zehazten ez bada eta sistemak definitutako bikoiztuak desegiteko arauak aplikatzen badira, baliteke eremu hori bikoiztuak desegiteko irteerako entitatean ez aurkitzea.
  - Deduplication_WinnerId: eremu honek identifikatutako talde edo klusterren irabazlearen IDa dauka. Deduplication_WinnerId erregistroaren gako nagusiaren balioaren berdina bada, erregistroa irabazle erregistroa dela esan nahi du.
- Bikoiztuak desegiteko arauak definitzeko erabiltzen diren eremuak.
- Arau eta Puntuazio eremuak bikoiztuak desegiteko arauetatik zein aplikatu den eta bat datorren algoritmoak emandako puntuazioa adierazteko.
   
## <a name="run-the-match-process"></a>Bat-egite prozesua burutu

Bat-etortze arauak konfiguratutakoak, entitateen arteko bat-etortzea eta bikoiztuak kentzeko arauak barne, bat-egiteko prozesua exekutatu dezakezu. 

Joan **Datuak** > **Bateratu** > **Bat egin** eta hautatu **Korrika egin** prozesua hasteko. Bat datorren algoritmoak denbora pixka bat behar du osatzeko eta ezin duzu konfigurazioa aldatu osatu arte. Aldaketak egiteko, ezezta dezakezu exekutatzea. Aukeratu lanaren egoera eta hautatu **Utzi lana** gainean **Aurrerapenaren xehetasunak** panela.

Exekuzio arrakastatsuaren emaitza, bezeroaren profileko entitate bateratua, aurkituko duzu **Entitateak** orrialdea. Zure bezero bateratutako entitateari deitzen zaio **Bezeroak** hurrengoan **Profilak** atala. Partida arrakastatsuaren lehenengo lasterketak bateratua sortzen du *Bezeroa* entitatea. Ondorengo partida guztiekin entitate hori zabaltzen da.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

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

## <a name="specify-custom-match-conditions"></a>Zehaztu pertsonalizatutako bat etortzeko baldintzak

Zehaztu egin ditzakezu erregistro jakinek beti edo inoiz bat etortzeko baldintzak. Arau hauek karga daitezke bat etortzeko prozesu estandarra gainidazteko. Adibidez, John Doe I eta John Doe II badaude gure erregistroetan, sistemak pertsona bakar gisa pare dezake. Partida pertsonalizatutako arauek profiletan pertsona desberdinak aipatzen dituztela zehazten dute. 

1. Joan **Datuak** > **Bateratu** > **Bat egin** eta hautatu **Bat-egite pertsonalizatua** hurrengoan **Erregistroen xehetasunak** atala.

  :::image type="content" source="media/custom-match-create.png" alt-text="Bat-egitearen arauen sekzioak bat-egite pertsonalizatuaren kontrolak nabarmenduta pantaila-argazkia.":::

1. Partiduen arau pertsonalizaturik ez baduzu, berria ikusiko duzu **Partida pertsonalizatua** xehetasun gehiagoko panela.

1. Aukeratu **Txantiloia bete** txantiloien fitxategia lortzeko, erakundeek beti bat etorri edo inoiz bat egin behar duten erregistroak zehazteko. Bi fitxategi desberdinetan "beti bat etorri" erregistroak eta "inoiz ez datoz" erregistroak bete behar dituzu.

1. Txantiloiak entitateak eta entitatearen gako nagusien balioak pertsonalizatutako partidan zehazteko eremuak ditu. Adibidez, gako nagusia nahi baduzu *12345* hurrengotik *Salmentak* entitatea beti lehen mailako gakoarekin bat etortzeko *34567* hurrengotik *Harremanetarako* entitatea, bete txantiloia:
    - Entitate1: Salmentak
    - Entitate-gakoa1: 12345
    - Entitatea2: kontaktua
    - Entitate-gakoa2: 34567

   Txantiloi fitxategi berak entitate anitzeko partiden erregistro pertsonalizatuak zehaztu ditzake.
   
   Entitate batean bikoiztuak desegiteko parekatze pertsonalizatua zehaztu nahi baduzu, eman Entitate 1 eta Entitate 2 entitate bera eta ezarri gako primarioen balio desberdinak.

1. Aplikatu nahi dituzun gainidatzi guztiak gehitu ondoren, gorde txantiloiaren fitxategia.

1. Joan hona **Datuak** > **Datu iturburuak** eta txantiloien fitxategiak entitate berri gisa sartu. Iragazi ondoren, bat egin dezakezu Match-ren konfigurazioa zehazteko.

1. Fitxategiak eta erakundeak kargatu ondoren, hautatu hautatu **Norberaren partida** aukera berriro. Aukerak ikusiko dituzu sartu nahi dituzun entitateak zehazteko. Aukeratu beharrezko entitateak goitibeherako menuan.

   :::image type="content" source="media/custom-match-overrides.png" alt-text="Elkarrizketa-koadroaren pantaila bat etortze pertsonalizatuko agertoki baterako gainidatziak aukeratzeko.":::

1. Hautatu erabili nahi dituzun entitateak **Beti bat etorri** eta **Inoiz ez dator bat** hautatu **Egina**.

1. Aukeratu **Gorde** gainean **Bat egin** orrialdea bat datorren konfigurazio pertsonalizatua aplikatzeko.

1. Aukeratu **Exekutatu** gainean **Bat egin** orrialdea parekatze prozesua hasteko. Partiduen zehaztapeneko beste arau batzuk pertsonalizatutako konfigurazio pertsonalizatuaren gainetik daude.

> [!TIP]
> Joan **Datuak** > **Entitateak** eta berrikusi **ConflationMatchPair** gainidatziak aplikatzen direla baieztatzeko entitatea.

## <a name="next-step"></a>Hurrengo urratsa

Partidaren prozesua gutxienez bat bikote egin ondoren, zure datuetan egon daitezkeen kontraesanak konpondu ditzakezu [**konbinatu**](merge-entities.md) Gai.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
