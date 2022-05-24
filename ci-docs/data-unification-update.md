---
title: Eguneratu bateratze-ezarpenak
description: Eguneratu bikoiztutako arauak, bat-etortze-arauak edo eremu bateratuak bateratze-ezarpenetan.
ms.date: 05/04/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: mukeshpo
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-match
- ci-merge
- ci-relationships
- customerInsights
ms.openlocfilehash: be399da9b98d8803d7d1a90f44a40e0d638a8d47
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755575"
---
# <a name="update-the-unification-settings"></a>Eguneratu bateratze-ezarpenak

[!INCLUDE [m3-prod-trial-note](includes/m3-prod-trial-note.md)]

Profil bateratua sortu ondoren bateratze-ezarpenak berrikusteko edo aldatzeko, egin urrats hauek.

1. Joan **Datuak** > **Bateratu**.

   :::image type="content" source="media/m3_unified.png" alt-text="Datuak bateratu ondoren datuak bateratu orriaren pantaila-argazkia.":::

   > [!TIP]
   > The **Bat datozen baldintzak** lauza entitate bat baino gehiago hautatuta badago soilik bistaratzen da.

1. Aukeratu zer eguneratu nahi duzun:
   - [Iturburu-eremuak](#edit-source-fields) entitateak edo atributuak gehitzeko edo atributu motak aldatzeko.
   - [Erregistro bikoiztuak](#manage-deduplication-rules) desduplicazio-arauak kudeatzeko edo hobespenak bateratzeko.
   - [Bat datozen baldintzak](#manage-match-rules) bi entitate edo gehiagotan bat datozen arauak eguneratzeko.
   - [Bezeroen eremu bateratuak](#manage-unified-fields) eremuak konbinatzeko edo baztertzeko. Erlazionatutako profilak multzotan ere taldeka ditzakezu.

1. Aldaketak egin ondoren, aukeratu hurrengo aukera:

   :::image type="content" source="media/m3_run_match_merge.png" alt-text="Datuak bateratzea orriaren pantaila-argazkia bateratu aukerak nabarmenduta.":::

   - Bezeroen profil bateratua eguneratzeko (mendekotasunekin edo gabe), ikus [Exekutatu bezeroaren profilaren eguneraketak](#run-updates-to-the-unified-customer-profile).
   - Zure parekatze-baldintzen kalitatea ebaluatzeko profil bateratua eguneratu gabe, ikus [Exekutatu bat datozen baldintzak](#run-matching-conditions). The **Exekutatu bat datozen baldintzak soilik** aukera ez da bistaratzen entitate bakarrerako.

## <a name="edit-source-fields"></a>Editatu iturburu-eremuak

Ezin duzu kendu atributu edo entitate bat dagoeneko bateratuta badaude.

1. Hautatu **Editatu** gainean **Iturburu-eremuak** teila.

   :::image type="content" source="media/m3_source_edit.png" alt-text="Iturburu-eremuen orriaren pantaila-argazkia, gako nagusien, mapatutako eta mapatu gabeko eremuen kopurua erakusten duena":::

   Mapatutako eta mapatu gabeko eremuen kopurua bistaratzen da.

1. Hautatu **Hautatu entitateak eta eremuak** beste atributu edo entitate batzuk gehitzeko. Erabili bilaketa edo korritua zure atributuak eta intereseko entitateak aurkitzeko eta hautatzeko. Hautatu **Aplikatu**.

1. Aukeran, entitate baten gako nagusia, atributu motak eta txandaka ditzakezu **Kartografia adimentsua** piztu edo itzali. Informazio gehiagorako, ikus [Hautatu gako nagusia eta mota semantikoa atributuetarako](map-entities.md#select-primary-key-and-semantic-type-for-attributes).

1. Hautatu **Hurrengoa** desduplicazio-arauetan aldaketak egiteko, edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-the-unification-settings).

## <a name="manage-deduplication-rules"></a>Kudeatu deduplicazio-arauak

1. Hautatu **Editatu** gainean **Erregistro bikoiztuak** teila.

   :::image type="content" source="media/m3_duplicates_edit.png" alt-text="Bikoiztutako erregistroen orriaren pantaila-argazkia, bikoiztutako erregistro kopurua erakusten duena" lightbox="media/m3_duplicates_edit.png":::

   Aurkitutako erregistro bikoiztuen kopurua azpian agertzen da **Bikoiztuak**. The **Erregistroak desbikoiztuta** zutabeak erregistro bikoiztuak zein entitate zituzten eta erregistro bikoiztuen ehunekoa erakusten du.

1. Entitate aberastua gehitu baduzu, hautatu **Erabili entitate aberastuak**. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md).

1. Desduplicazio-arauak kudeatzeko, aukeratu aukera hauetako bat:
   - **Sortu arau berri bat** : Hautatu **Gehitu araua** dagokion entitatearen pean. Informazio gehiagorako, ikus [Desduplicazio-arauak definitu](remove-duplicates.md#define-deduplication-rules).
   - **Aldatu arau-baldintzak** : Hautatu araua eta gero **Editatu**. Aldatu eremuak, gehitu edo kendu baldintzak, edo gehitu edo kendu salbuespenak.
   - **Aurrebista** : Hautatu araua eta gero **Aurrebista** arau honen azken exekuzioaren emaitzak ikusteko.
   - **Desaktibatu arau bat** : Hautatu araua eta gero **Desaktibatu** desduplicazio-arau bat gordetzeko, parekatze-prozesutik kanpo uzten duen bitartean.
   - **Bikoiztu arau bat** : Hautatu araua eta gero **Bikoiztu** aldaketekin antzeko arau bat sortzeko.
   - **Ezabatu arau bat** : Hautatu araua eta gero **Ezabatu**.

1. Batzeko hobespenak aldatzeko, hautatu entitatea. Arau bat sortzen bada bakarrik alda ditzakezu hobespenak.
   1. Hautatu **Editatu bateratze-hobespenak** eta aldatu **Gorde beharreko erregistroa** aukera.
   1. Entitate baten atributu indibidualetan bateratze-hobespenak aldatzeko, hautatu **Aurreratua** eta beharrezko aldaketak egin.

      :::image type="content" source="media/m3_adv_merge.png" alt-text="Bateratze-hobespen aurreratuen pantaila-argazkia, posta elektroniko berriena eta helbide osatuena erakusten duena":::

   1. Hautatu **Eginda**.

1. Hautatu **Hurrengoa** bat datozen baldintzetan aldaketak egiteko, edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-the-unification-settings).

## <a name="manage-match-rules"></a>Kudeatu bat egiteko arauak

Partiduen parametro gehienak birkonfigura eta doitu ditzakezu. Ezin dituzu entitateak gehitu edo ezabatu. Bat-etortze-arauak ez zaizkio aplikatzen entitate bakar bati.

1. Hautatu **Editatu** gainean **Bat datozen baldintzak** teila.

   :::image type="content" source="media/m3_match_edit.png" alt-text="Partiduen arauak eta baldintzak orrialdearen pantaila-argazkia estatistikekin." lightbox="media/m3_match_edit.png":::

   Orriak partida-ordena eta definitutako arauak eta estatistikak bistaratzen ditu:
   - **Iturri erregistro bakarrak** azken partidako exekuzioan prozesatutako banako iturrien erregistro kopurua erakusten du.
   - **Partiduen eta ez datozen erregistroak** Partidaren arauak prozesatu ondoren zenbat erregistro bakarra geratzen diren nabarmentzen du.
   - **Erregistro parekatuak soilik** zure bikote bikote guztien partida kopurua erakusten du.

1. Arau guztien emaitzak eta haien puntuazioak ikusteko, hautatu **Ikusi azken lasterketa**. Emaitzak bistaratzen dira, ordezko kontaktuen IDak barne. Emaitzak deskargatu ditzakezu.

1. Arau jakin baten emaitzak eta puntuazioak ikusteko, hautatu araua eta gero **Aurrebista**. Emaitzak bistaratzen dira. Emaitzak deskargatu ditzakezu.

1. Arau batean baldintza jakin baten emaitzak ikusteko, hautatu araua eta gero **Editatu**. Editatu panelean, hautatu **Aurrebista** baldintzapean. Emaitzak deskargatu ditzakezu.

   :::image type="content" source="media/m3_match_condition_preview.png" alt-text="Bat ez datozen eta bat datozen erregistroen irudikapen grafikoa, datuen zerrenda barne.":::

1. Entitate aberastua gehitu baduzu, hautatu **Erabili entitate aberastuak**. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md).

1. Arauak kudeatzeko, aukeratu aukera hauetako bat:
   - **Sortu arau berri bat** : Hautatu **Gehitu araua** dagokion entitatearen pean. Informazio gehiagorako, ikus [Partiduen bikoteen arauak zehaztu](match-entities.md#define-rules-for-match-pairs).
   - **Aldatu zure arauen ordena** hainbat arau definitu badituzu: Arrastatu eta jaregin arauak nahi duzun ordenan. Informazio gehiagorako, ikus [Zehaztu partida-ordena](match-entities.md#specify-the-match-order).
   - **Aldatu arau-baldintzak** : Hautatu araua eta gero **Editatu**. Aldatu eremuak, gehitu edo kendu baldintzak, edo gehitu edo kendu salbuespenak.
   - **Desaktibatu arau bat** : Hautatu araua eta gero **Desaktibatu** parekatze-arau bat gordetzea, parekatze-prozesutik kanpo uzten duen bitartean.
   - **Bikoiztu arau bat** : Hautatu araua eta gero **Bikoiztu** aldaketekin antzeko arau bat sortzeko.
   - **Ezabatu arau bat** : Hautatu araua eta gero **Ezabatu**.

1. Hautatu **Hurrengoa** eremu bateratuetan aldaketak egiteko, edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-the-unification-settings).

## <a name="manage-unified-fields"></a>Kudeatu eremu bateratuak

1. Hautatu **Editatu** gainean **Bezeroen eremu bateratuak** teila.

    :::image type="content" source="media/m3_merge_edit.png" alt-text="Bezeroen eremu bateratuen pantaila-argazkia":::

1. Berrikusi konbinatutako eta baztertutako eremuak eta egin aldaketak behar izanez gero. Gehitu edo editatu CustomerID gakoa edo taldekatu profilak multzotan. Informazio gehiagorako, ikus [Bateratu bezeroen eremuak](merge-entities.md).

1. Hautatu **Hurrengoa** bateratze-ezarpenak berrikusteko eta [eguneratu profil bateratua eta mendekotasunak](#run-updates-to-the-unified-customer-profile), edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-the-unification-settings) aldaketa gehiago egiteko.

## <a name="run-matching-conditions"></a>Exekutatu bat datozen baldintzak

1. Tik **Datuak** > **Bateratu** orrialdea, hautatu **Exekutatu bat datozen baldintzak soilik**.

   The **Erregistro bikoiztuak** eta **Bat datozen baldintzak** fitxak erakusten **Ilaran jarrita** edo **Freskagarria**.

   [!INCLUDE [m3-task-details-include](includes/m3-task-details.md)]

1. Lotze-prozesua amaitzen denean, hautatu **Editatu** gainean **Bat datozen baldintzak** teila.

   :::image type="content" source="media/match-KPIs.png" alt-text="Partiduen orriko gakoen neurrien pantaila moztua zenbakiekin eta xehetasunekin.":::

1. Aldaketak egiteko, ikus [Kudeatu deduplicazio-arauak](#manage-deduplication-rules) edo [Kudeatu partida-arauak](#manage-match-rules).

1. Exekutatu partida-prozesua berriro edo [exekutatu bezeroaren profilaren eguneraketak](#run-updates-to-the-unified-customer-profile).

## <a name="run-updates-to-the-unified-customer-profile"></a>Exekutatu bezeroen profil bateratuaren eguneraketak

1. Tik **Datuak** > **Bateratu** orrialdea, hautatu:

   - **Bateratu bezeroen profilak** : bezeroen profil bateratuaren entitatea eguneratzen du mendekotasunetan eragin gabe (aberastasunak, segmentuak edo neurriak, esaterako). Menpeko prozesuak ez dira exekutatzen, baina gisa eguneratuko dira [freskatze programazioan zehaztuta](system.md#schedule-tab).

   - **Bezeroen profilak eta menpekotasunak bateratzea** : profil bateratua eta mendekotasun guztiak eguneratzen ditu. Prozesu guztiak automatikoki berriro exekutatzen dira. Beheko prozesu guztiak amaitu ondoren, bezeroaren profilak eguneratutako datuak islatzen ditu.

   The **Erregistro bikoiztuak**, **datozen baldintzak**, eta **Bezeroen eremu bateratuak** fitxak erakusten **Ilaran jarrita** edo **Freskagarria**.

   [!INCLUDE [m3-task-details-include](includes/m3-task-details.md)]
