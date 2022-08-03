---
title: Datuak bateratzeko baldintzak bat etortzea
description: Lotu entitateak bezeroen profil bateratuak sortzeko.
recommendations: false
ms.date: 05/05/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: mukeshpo
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-match
- ci-merge
- ci-map
- customerInsights
ms.openlocfilehash: e3e4e37d5b4c9caf2520a789d5f78ef33b491793
ms.sourcegitcommit: 3c5b0b40b2b45e420015bbdd228ce0e610245e6f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/12/2022
ms.locfileid: "9139682"
---
# <a name="match-conditions-for-data-unification"></a>Datuak bateratzeko baldintzak bat etortzea

Bateratzearen urrats honek entitateen arteko parekatze-ordena eta arauak definitzen ditu. Urrats honek gutxienez bi entitate behar ditu.

> [!NOTE]
> Zure partida-baldintzak sortu eta hautatu ondoren **Hurrengoa**, ezin duzu hautatutako entitate edo atributu bat kendu. Behar izanez gero, hautatu **Itzuli** hautatutako entitateak eta atributuak berrikusteko, jarraitu aurretik.

## <a name="include-enriched-entities-preview"></a>Sartu entitate aberastuak (aurrebista)

datu-iturburu mailan entitateak aberastu badituzu zure bateratzearen emaitzak hobetzen laguntzeko, hautatu itzazu. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md). Entitate aberastuak hautatu badituzu **Erregistro bikoiztuak** orrialdea, ez dituzu berriro hautatu behar.

1. Gainean **Bat datozen baldintzak** orrialdea, hautatu **Erabili entitate aberastuak** orriaren goialdean.

1. Tik **Erabili entitate aberastuak** panela, aukeratu entitate aberastu bat edo gehiago.

1. Hautatu **Eginda**.

## <a name="specify-the-match-order"></a>bat etortzearen ordena zehaztu

Partida bakoitzak bi entitate edo gehiago bateratzen ditu entitate bakar eta bateratu batean. Aldi berean, bezeroaren erregistro bakarrak gordetzen ditu. Bat-etortze-ordenak sistemak erregistroekin bat egiten saiatzen den ordena adierazten du.

> [!IMPORTANT]
> Zerrendako lehen entitateari entitate nagusia deitzen zaio. Entitate nagusiak zure profil bateratuen datu-multzoaren oinarri gisa balio du. Hautatzen diren entitate gehigarriak entitate honi gehituko zaizkio.
>
> Gogoeta garrantzitsuak:
>
> - Aukeratu zure bezeroei buruzko profil-datu osatuena eta fidagarriena duen entitatea entitate nagusi gisa.
> - Aukeratu beste entitate batzuekin komunean hainbat atributu dituen entitatea (adibidez, izena, telefono-zenbakia edo helbide elektronikoa) entitate nagusi gisa.

1. Gainean **Bat datozen baldintzak** orrialdean, erabili gora eta behera mugitu geziak entitateak nahi duzun ordenan mugitzeko, edo arrastatu eta jaregin. Adibidez, hautatu **Kontaktuak: merkataritza elektronikoa** entitate nagusi gisa eta **Bezeroaren Leialtasuna: Leialtasuna** bigarren entitate gisa.

1. Entitateko erregistro guztiak bezero esklusibo gisa edukitzeko, bat-etortzerik aurkitzen bada ere, hautatu **Sartu erregistro guztiak**. Entitate honetako erregistroak beste edozein entitatetako erregistroekin bat ez datozenak profil bateratuan sartzen dira. Partidurik ez duten erregistroei singleton deitzen zaie.
  
Lehen entitatea *Kontaktuak: merkataritza elektronikoa* hurrengo entitatearekin parekatzen da *Bezeroaren Leialtasuna: Leialtasuna*. Lehen bat-etortze-urratsetik ateratzen den datu-multzoa hurrengo entitatearekin bat dator bi entitate baino gehiago badituzu.

:::image type="content" source="media/m3_match.png" alt-text="Entitateetarako hautatutako partida-ordenaren pantaila-argazkia." lightbox="media/m3_match.png":::

## <a name="define-rules-for-match-pairs"></a>Partiduen bikoteen arauak zehaztu

Bat egiten duten arauek entitate pare bat lotuko den logika zehazten dute. Arau bat baldintza batek edo gehiagok osatzen dute.

Entitate-izen baten ondoan dagoen abisuak esan nahi du ez dagoela bat-etortze-araurik definitu bat-etortze-bikote baterako.

1. Hautatu **Gehitu araua** entitate-bikote batek partida-arauak definitzeko.

1. urtean **Gehitu araua** panelean, konfiguratu arauaren baldintzak.

   :::image type="content" source="media/m3_add_rule.png" alt-text="Gehitu araua panelaren pantaila-argazkia.":::

   - **Hautatu Entitatea/Eremua (lehen lerroa)** : Aukeratu erlazionatutako entitate bat eta atributu bat bezero batentzat litekeena den erregistro-propietate bat zehazteko. Adibidez, telefono zenbaki bat edo helbide elektronikoa. Saihestu jarduera motako atributuen arabera parekatzea. Esate baterako, erosketa IDak ez du bat-etortzerik izango beste erregistro mota batzuetan.

   - **Hautatu Entitatea/Eremua (bigarren errenkada)** : Aukeratu lehen lerroan zehaztutako entitatearen atributuarekin erlazionatutako atributu bat.

   - **Normalizatu**: Aukeratu hautatutako atributuen normalizazio aukera hauetatik.
     - **Zenbakiak** : Beste zenbaki-sistema batzuk, esate baterako, zenbaki erromatarrak, zenbaki arabiar bihurtzen ditu. *VIII* bihurtzen *8*.
     - **Sinboloak** : ikur eta karaktere berezi guztiak kentzen ditu. *Burua eta Sorbalda* bihurtzen da *HeadShoulder*.
     - **Testua minuskulaz** : Karaktere guztiak minuskula bihurtzen ditu. *MAIUSU GUZTIAK eta Izenburua* bihurtzen da *maiuskula guztiak eta izenburua*.
     - **Mota (Telefonoa, Izena, Helbidea, Erakundea)** : izenak, izenburuak, telefono zenbakiak, helbideak eta erakundeak estandarizatzen ditu.
     - **Unicode ASCIIra** : Unicode notazioa ASCII karaktere bihurtzen du. */u00B2* bihurtzen da *2*.
     - **Zuriunea** : zuriune guztiak kentzen ditu. *Kaixo   Mundua* bihurtzen da *KaixoMundua*.

   - **Zehaztasuna**: zehaztu baldintza hau aplikatzeko zehaztasun maila.
     - **Oinarrizkoa** : Aukeratu *Baxua (%30)*, *(%60)*, *(%80)*, eta *Zehatza (%100)*. Hautatu **Zehatza** ehuneko 100ean bat datozen erregistroak soilik lotzeko.
     - **Pertsonalizatua**: ezarri erregistroek bat etorri behar duten ehunekoa. Sistemak atalase hori gainditzen duten erregistroak baino ez ditu bat etorriko.

   - **Izena** : Arauaren izena.

1. Entitateak bat etortzeko atributuek baldintza anitz betetzen badituzte soilik, hautatu **Gehitu** > **Gehitu baldintza** partida-arau bati baldintza gehiago gehitzeko. Baldintzak AND operadore logikoarekin lotuta daude eta, beraz, baldintza guztiak betetzen badira soilik exekutatzen dira.

1. Aukeran, kontuan hartu aukera aurreratuak adibidez [salbuespenak](#add-exceptions-to-a-rule) edo [bat etortzeko baldintza pertsonalizatuak](#specify-custom-match-conditions).

1. Hautatu **Eginda** araua amaitzeko.

1. Aukeran [gehitu arau gehiago](#add-rules-to-a-match-pair).

1. Sakatu **Hurrengoa**.

> [!div class="nextstepaction"]
> [Hurrengo urratsa: Eremuak bateratu](merge-entities.md)

### <a name="add-rules-to-a-match-pair"></a>Gehitu arauak partida bikoteari

Partiduen arauek baldintza multzoak adierazten dituzte. Entitateak hainbat atribututan oinarritutako baldintzen arabera lotzeko, gehitu arau gehiago.

1. Hautatu **Gehitu araua** arauak gehitu nahi dituzun entitatean.

1. Jarraitu urratsak [Partiduen bikoteen arauak zehaztu](#define-rules-for-match-pairs).

> [!NOTE]
> Arauen ordena garrantzitsua da. Bat-etortze-algoritmoa bezero-erregistro jakin batekin bat egiten saiatzen da zure lehen arauaren arabera eta bigarren araura jarraitzen du lehen arauarekin bat-etortzerik identifikatu ez bada.

## <a name="advanced-options"></a>Aukera aurreratuak

### <a name="add-exceptions-to-a-rule"></a>Gehitu salbuespenak arau bati

Kasu gehienetan, entitateen parekatzeak datu bateratuak dituzten bezero-profil bakarrak dakartza. Positibo faltsuen eta negatibo faltsuen kasu bakanak modu dinamikoan zuzentzeko, bat-etortze-arau baterako salbuespenak defini ditzakezu. Salbuespenak bat-etortze-arauak prozesatu ondoren aplikatzen dira eta salbuespen-irizpideak betetzen dituzten erregistro guztiak bat etortzea saihesten da.

Adibidez, zure parekatze-arauak abizen, hiria eta jaioteguna konbinatzen baditu, sistemak profil berdinarekin bizi diren abizen bera duten bikiak identifikatuko lituzke. Profilekin bat ez datorren salbuespen bat zehaztu dezakezu konbinatzen dituzun entitateetako izen berdinak ez badira.

1. urtean **Editatu araua** panela, hautatu **Gehitu** > **Gehitu salbuespena**.

1. Zehaztu salbuespen irizpideak.

1. Hautatu **Egina** araua gordetzeko.

### <a name="specify-custom-match-conditions"></a>Zehaztu pertsonalizatutako bat etortzeko baldintzak

Bat-etortze-logika lehenetsia gainidazten duten baldintzak zehaztu ditzakezu. Lau aukera daude eskuragarri:

|Aukera  |Deskribapenak |Adibidez  |
|---------|---------|---------|
|Beti bat etorri behar du     | Beti bat datozen balioak definitzen ditu.         |  Beti parekatu *Mikel* eta *MikeR*.       |
|Ez du inoiz bat etorri behar     | Inoiz bat ez datozen balioak definitzen ditu.        | Inoiz ez parekatu *Joan* eta *Jonathan*.        |
|Salbuespen pertsonalizatua     | Partida-fasean sistemak beti alde batera utzi behar dituen balioak zehazten ditu. |  Ez ikusi balioei *11111* eta *Ezezaguna* partidan zehar.        |
|Aliasen esleipena    | Sistemak balio berdintzat hartu behar dituen balioak definitzea.         | Kontuan hartu *Joe* berdina izateko *Joseph*.        |

1. Hautatu **Pertsonalizatua**.

   :::image type="content" source="media/m3_match_custom.png" alt-text="Botoi pertsonalizatua":::

1. Aukeratu **Mota pertsonalizatua** eta hautatu **Deskargatu txantiloia**. Bat-etortze-aukera bakoitzerako txantiloi bat behar duzu.

1. Ireki deskargatutako txantiloi fitxategia eta bete xehetasunak. Txantiloiak entitateak eta entitatearen gako nagusien balioak pertsonalizatutako partidan zehazteko eremuak ditu. Adibidez, gako nagusia nahi baduzu *12345* hurrengotik *Salmentak* entitatea beti lehen mailako gakoarekin bat etortzeko *34567* hurrengotik *Harremanetarako* entitatea, bete txantiloia:
    - Entitate1: Salmentak
    - Entitate-gakoa1: 12345
    - Entitatea2: kontaktua
    - Entitate-gakoa2: 34567

   Txantiloi fitxategi berak entitate anitzeko partiden erregistro pertsonalizatuak zehaztu ditzake.

   Entitate batean bikoiztuak desegiteko parekatze pertsonalizatua zehaztu nahi baduzu, eman Entitate 1 eta Entitate 2 entitate bera eta ezarri gako primarioen balio desberdinak.

1. Gainbatze guztiak gehitu ondoren, gorde txantiloi fitxategia.

1. Joan hona **Datuak** > **Datu iturburuak** eta txantiloien fitxategiak entitate berri gisa sartu.

1. Fitxategiak kargatu ondoren, hautatu **Pertsonalizatua** aukera berriro. Hautatu goitibeherako menuan beharrezko entitateak eta hautatu **Eginda**.

   :::image type="content" source="media/custom-match-overrides.png" alt-text="Elkarrizketa-koadroaren pantaila bat etortze pertsonalizatuko agertoki baterako gainidatziak aukeratzeko.":::

1. Parekatze pertsonalizatua aplikatzea erabili nahi duzun bat-etortze-aukeraren araberakoa da.

   - Izan ere **Beti lotu** edo **Inoiz ez parekatu**, jarraitu hurrengo urratsera.
   - Izan ere **Saihesbidea** edo **Aliasaren mapaketa**, hautatu **Editatu** lehendik dagoen bat-etortze-arau batean edo sortu arau berri bat. Normalizazioak goitibeherako aukeran, aukeratu **Saihesbide pertsonalizatua** edo **Aliasaren mapaketa** aukera eta hautatu **Eginda**.

1. Hautatu **Eginda** gainean **Pertsonalizatua** panela etortze pertsonalizatuaren konfigurazioa aplikatzeko.

> [!div class="nextstepaction"]
> [Hurrengo urratsa: Eremuak bateratu](merge-entities.md)

[!INCLUDE [footer-include](includes/footer-banner.md)]
