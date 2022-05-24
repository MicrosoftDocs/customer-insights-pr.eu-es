---
title: Kendu bikoiztuak datuak bateratu aurretik
description: Bateratze prozesuaren bigarren urratsa bikoiztuak aurkitzen direnean zein erregistro gorde behar den hautatzea da.
recommendations: false
ms.date: 04/22/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: mukeshpo
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-map
- ci-match
- customerInsights
ms.openlocfilehash: 27dff3551ab411a12c273536d7431d651c48573e
ms.sourcegitcommit: 6a5f4312a2bb808c40830863f26620daf65b921d
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8742918"
---
# <a name="remove-duplicates-before-unifying-data"></a>Kendu bikoiztuak datuak bateratu aurretik

[!INCLUDE [m3-prod-trial-note](includes/m3-prod-trial-note.md)]

Bateratze-urrats honek aukera ematen dizu entitate baten barruan erregistro bikoiztuak kudeatzeko arauak konfiguratzeko. *Desduplikatzea* erregistro bikoiztuak identifikatzen ditu eta erregistro batean batzen ditu. Iturburu erregistroak bateratutako erregistroarekin lotzen dira ID ordezkoekin. Arauak konfiguratzen ez badira, sistemak definitutako arauak aplikatuko dira.

## <a name="include-enriched-entities-preview"></a>Sartu entitate aberastuak (aurrebista)

datu-iturburu mailan entitateak aberastu badituzu zure bateratzearen emaitzak hobetzen laguntzeko, hautatu itzazu. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md).

1. Gainean **Erregistro bikoiztuak** orrialdea, hautatu **Erabili entitate aberastuak** orriaren goialdean.

1. Tik **Erabili entitate aberastuak** panela, aukeratu entitate aberastu bat edo gehiago.

1. Hautatu **Eginda**.

## <a name="define-deduplication-rules"></a>Desduplicazio-arauak definitu

1. Gainean **Erregistro bikoiztuak** orrialdea, hautatu entitate bat eta hautatu **Gehitu araua** deduplicazio-arauak definitzeko.

   :::image type="content" source="media/m3_duplicates_showmore.png" alt-text="Bikoiztutako erregistroen orrien pantaila-argazkia Erakutsi gehiago nabarmenduta":::

   1. urtean **Gehitu araua** panelean, sartu informazio hau:
      - **Hautatu eremua** : Aukeratu bikoiztuak dauden egiaztatu nahi duzun entitateko eremu erabilgarrien zerrendatik. Aukeratu bezero bakoitzarentzat litekeena den eremua. Adibidez, helbide elektronikoa edo izena, hiria eta telefono zenbakiaren konbinazioa.
      - **Normalizatu**: Aukeratu hautatutako atributuen normalizazio aukera hauetatik.
        - **Zenbakiak** : Beste zenbaki-sistema batzuk, esate baterako, zenbaki erromatarrak, zenbaki arabiar bihurtzen ditu. *VIII* bihurtzen *8*.
        - **Sinboloak** : ikur eta karaktere berezi guztiak kentzen ditu. *Burua eta Sorbalda* bihurtzen da *HeadShoulder*.
        - **Testua minuskula bihurtu: karaktere guztiak minuskula bihurtzen ditu**. *MAIUSU GUZTIAK eta Izenburua* bihurtzen da *maiuskula guztiak eta izenburua*.
        - **Mota (Telefonoa, Izena, Helbidea, Erakundea)** : Izenak, izenburuak, telefono zenbakiak, helbideak, etab estandarizatzen ditu.
        - **Unicode ASCIIra** : Unicode notazioa ASCII karaktere bihurtzen du. */u00B2* bihurtzen da *2*.
        - **Zuriunea** : zuriune guztiak kentzen ditu. *Kaixo   Mundua* bihurtzen da *KaixoMundua*.
      - **Zehaztasuna**: zehaztu baldintza hau aplikatzeko zehaztasun maila.
        - **Oinarrizkoa** : Aukeratu *Baxua (%30)*, *(%60)*, *(%80)*, eta *Zehatza (% 100)*. Hautatu **Zehatza** ehuneko 100ean bat datozen erregistroak soilik lotzeko.
        - **Pertsonalizatua**: ezarri erregistroek bat etorri behar duten ehunekoa. Sistemak atalase hori gainditzen duten erregistroak baino ez ditu bat etorriko.
      - **Izena** : Arauaren izena.

      :::image type="content" source="media/m3_duplicates_add.png" alt-text="Bikoiztuak kentzeko Gehitu araua panelaren pantaila-argazkia.":::

   1. Aukeran, hautatu **Gehitu** > **Gehitu baldintza** arauari baldintza gehiago gehitzeko. Baldintzak AND operadore logikoarekin lotuta daude eta, beraz, baldintza guztiak betetzen badira soilik exekutatzen dira.

   1. Aukeran, **Gehitu** > **Gehitu salbuespena** to [gehitu salbuespenak arauari](match-entities.md#add-exceptions-to-a-rule). Salbuespenak positibo faltsuen eta negatibo faltsuen kasu bakanei aurre egiteko erabiltzen dira.

   1. Hautatu **Eginda** araua sortzeko.

1. Aukeran [gehitu arau gehiago](#define-deduplication-rules).

1. Hautatu entitate bat eta gero **Editatu bateratze-hobespenak**.

1. urtean **Bateratu hobespenak** panela:
   1. Aukeratu hiru aukeretako bat bikoiztua aurkitzen bada zein erregistro gorde behar den zehazteko:
      - **Beteen daudenak** : Betetako atributu eremueak gehien dituen erregistroa identifikatzen du erregistro nagusi gisa. Hori da konbinatzeko aukera lehenetsia.
      - **Berrienak**: erregistro nagusia identifikatzen du berritasunen arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.
      - **Zaharrenak**: erregistro nagusia identifikatzen du zahartasunaren arabera. Berritasuna definitzeko data edo zenbakizko eremua behar du.
      
      Berdinketa gertatuz gero, irabazlearen errekorra MAX(PK) edo gako nagusiaren balio handiagoa duena da.
      
   1. Aukeran, entitate baten atributu indibidualetan bateratze-hobespenak definitzeko, hautatu **Aurreratua** panelaren behealdean. Adibidez, posta elektroniko berriena ETA helbiderik osatuena erregistro ezberdinetatik gordetzea aukera dezakezu. Zabaldu entitatea bere atributu guztiak ikusteko eta zein aukera erabili atributu indibidualetarako. Azkenaldian oinarritutako aukera bat aukeratzen baduzu, berritasuna definitzen duen data/orduaren eremua ere zehaztu behar duzu.

      :::image type="content" source="media/m3_adv_merge.png" alt-text="Bateratze-hobespenen panel aurreratuak azken posta elektronikoa eta helbide osoa erakusten ditu":::

   1. Hautatu **Eginda** zure bateratze-hobespenak aplikatzeko.

1. Desduplicazio-arauak eta bateratze-hobespenak zehaztu ondoren, hautatu **Hurrengoa**.
  
> [!div class="nextstepaction"]
> [Entitate bakar baterako hurrengo urratsa: Eremuak bateratu](merge-entities.md)

> [!div class="nextstepaction"]
> [Entitate anitzentzako hurrengo urratsa: Baldintzak bat etortzea](match-entities.md)

## <a name="deduplication-output-as-an-entity"></a>Irteerako bikoiztuak desegiteko entitate gisa

Desduplicazio-prozesuak desbikoiztutako entitate berri bat sortzen du iturburuko entitate bakoitzeko. Entitate hauek **ConflationMatchPairs:CustomerInsights** balioarekin batera **Sistema** atalean **Entitateak** orrian, **Deduplication_DataSource_Entity** izenarekin.

Bikoiztuak desegiteko irteerako entitate batek informazio hau dauka:

- IDak eta gakoak
  - Gako nagusia eta Ordezko ID eremuak. Ordezko ID eremua erregistro baterako identifikatutako ordezko ID guztiek osatzen dute.
  - Deduplication_GroupId eremuak zehaztutako bikoiztuak desegiteko eremuetan oinarritutako antzeko erregistro guztiak multzokatzen dituen entitate baten barruan identifikatutako taldea edo klusterra erakusten du. Sistema prozesatzeko helburuarekin erabiltzen da. Eskuzko bikoiztuak desegiteko araurik zehazten ez bada eta sistemak definitutako bikoiztuak desegiteko arauak aplikatzen badira, baliteke eremu hori bikoiztuak desegiteko irteerako entitatean ez aurkitzea.
  - Deduplication_WinnerId: eremu honek identifikatutako talde edo klusterren irabazlearen IDa dauka. Deduplication_WinnerId erregistroaren gako nagusiaren balioaren berdina bada, erregistroa irabazle erregistroa dela esan nahi du.
- Bikoiztuak desegiteko arauak definitzeko erabiltzen diren eremuak.
- Arau eta Puntuazio eremuak bikoiztuak desegiteko arauetatik zein aplikatu den eta bat datorren algoritmoak emandako puntuazioa adierazteko.

[!INCLUDE[footer-include](includes/footer-banner.md)]
