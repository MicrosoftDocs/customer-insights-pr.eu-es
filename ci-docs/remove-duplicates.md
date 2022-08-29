---
title: Kendu bikoiztuak datuak bateratu aurretik
description: Bateratze prozesuaren bigarren urratsa bikoiztuak aurkitzen direnean zein erregistro gorde behar den hautatzea da.
recommendations: false
ms.date: 08/01/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: sstabbert
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-map
- ci-match
- customerInsights
ms.openlocfilehash: 3f84c1c149f0befcbe489ccdd8a666ce6d5d798a
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304458"
---
# <a name="remove-duplicates-before-unifying-data"></a>Kendu bikoiztuak datuak bateratu aurretik

Baterako aukerako urrats honek erregistro bikoiztuak ezabatzeko arauak ezar ditzakezu **barruan** entitate bat. Desduplicazioak bezero batentzako hainbat erregistro identifikatzen ditu eta gorde beharreko erregistrorik onena hautatzen du (oinarrizko bateratze-hobespenetan oinarrituta) edo erregistroak bateratzen ditu (baketa-hobespen aurreratuetan oinarrituta). Iturburu erregistroak bateratutako erregistroarekin lotzen dira ID ordezkoekin. Arauak konfiguratzen ez badira, sistemak definitutako arauak aplikatuko dira.

## <a name="default-deduplication"></a>Lehenetsitako deduplicazioa

Sistemak definitutako arauak aplikatzen dira deduplicazio-araurik gehitzen ez bada.

- Gako nagusia desbikoiztuta dago.
  Gako nagusi bera duten edozein erregistrotarako, hau **Gehienak beteta** erregistroa (balio nulu gutxien duena) da irabazlea.
- Entitateen arteko bat-etortze-arau guztiak aplikatzen zaizkio entitateari.
  Adibidez: Bat-etortze-urratsean, A entitatea B entitatearekin bat egiten bada *Izen osoa* eta *Jaioteguna*, orduan A entitatea ere bikoiztu egiten da *Izen osoa* eta *Jaioteguna*. Zeren *Izen osoa* eta *Jaioteguna* A entitatean bezero bat identifikatzeko baliozko gakoak dira, gako hauek A entitatean bezero bikoiztuak identifikatzeko ere balio dute.

## <a name="include-enriched-entities-preview"></a>Sartu entitate aberastuak (aurrebista)

datu-iturburu mailan entitateak aberastu badituzu zure bateratzearen emaitzak hobetzen laguntzeko, hautatu itzazu. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md).

1. Gainean **Erregistro bikoiztuak** orrialdea, hautatu **Erabili entitate aberastuak** orriaren goialdean.

1. Tik **Erabili entitate aberastuak** panela, aukeratu entitate aberastu bat edo gehiago.

1. Hautatu **Eginda**.

## <a name="define-deduplication-rules"></a>Desduplicazio-arauak definitu

1. Gainean **Erregistro bikoiztuak** orrialdea, hautatu entitate bat eta hautatu **Gehitu araua** deduplicazio-arauak definitzeko.

   :::image type="content" source="media/m3_duplicates_showmore.png" alt-text="Bikoiztutako erregistroen orriaren pantaila-argazkia entitatea nabarmenduta eta Gehitu araua bistaratuta"  lightbox="media/m3_duplicates_showmore.png":::

   1. urtean **Gehitu araua** panelean, sartu informazio hau:
      - **Hautatu eremua** : Aukeratu bikoiztuak dauden egiaztatu nahi duzun entitateko eremu erabilgarrien zerrendatik. Aukeratu bezero bakoitzarentzat litekeena den eremua. Adibidez, helbide elektronikoa edo izena, hiria eta telefono zenbakiaren konbinazioa.
      - **Normalizatu**: Aukeratu hautatutako atributuen normalizazio aukera hauetatik.
        - **Zenbakiak** : Beste zenbaki-sistema batzuk, esate baterako, zenbaki erromatarrak, zenbaki arabiar bihurtzen ditu. *VIII* bihurtzen *8*.
        - **Sinboloak** : ikur eta karaktere berezi guztiak kentzen ditu. *Burua eta Sorbalda* bihurtzen da *HeadShoulder*.
        - **Testua minuskula bihurtu: karaktere guztiak minuskula bihurtzen ditu**. *MAIUSU GUZTIAK eta Izenburua* bihurtzen da *maiuskula guztiak eta izenburua*.
        - **Mota (Telefonoa, Izena, Helbidea, Erakundea)** : Izenak, izenburuak, telefono zenbakiak, helbideak eta abar estandarizatzen ditu.
        - **Unicode ASCIIra** : Unicode notazioa ASCII karaktere bihurtzen du. */u00B2* bihurtzen da *2*.
        - **Zuriunea** : zuriune guztiak kentzen ditu. *Kaixo   Mundua* bihurtzen da *KaixoMundua*.
      - **Zehaztasuna**: zehaztu baldintza hau aplikatzeko zehaztasun maila.
        - **Oinarrizkoa** : Aukeratu *Baxua (%30)*, *(%60)*, *(%80)*, eta *Zehatza (%100)*. Hautatu **Zehatza** ehuneko 100ean bat datozen erregistroak soilik lotzeko.
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

   1. Aukeran, entitate baten atributu indibidualetan bateratze-hobespenak definitzeko, hautatu **Aurreratua** panelaren behealdean. Adibidez, posta elektroniko berriena ETA helbiderik osatuena erregistro ezberdinetatik gordetzea aukera dezakezu. Zabaldu entitatea bere atributu guztiak ikusteko eta zein aukera erabili atributu indibidualetarako. Azkenaldian oinarritutako aukera bat aukeratzen baduzu, berritasuna definitzen duen data/ordu eremu bat ere zehaztu behar duzu.

      :::image type="content" source="media/m3_adv_merge.png" alt-text="Bateratze-hobespenen panel aurreratuak azken posta elektronikoa eta helbide osoa erakusten ditu":::

   1. Hautatu **Eginda** zure bateratze-hobespenak aplikatzeko.

1. Desduplicazio-arauak eta bateratze-hobespenak zehaztu ondoren, hautatu **Hurrengoa**.
  
> [!div class="nextstepaction"]
> [Entitate bakar baterako hurrengo urratsa: Eremuak bateratu](merge-entities.md)

> [!div class="nextstepaction"]
> [Entitate anitzentzako hurrengo urratsa: Baldintzak bat etortzea](match-entities.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
