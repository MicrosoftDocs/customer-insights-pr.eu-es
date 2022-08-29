---
title: Eguneratu bezero, kontu edo kontaktuen bateratze-ezarpenak
description: Eguneratu bikoiztutako arauak, bat-etortze-arauak edo eremu bateratuak bezeroaren edo kontuaren bateratze-ezarpenetan.
ms.date: 08/12/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: Scott-Stabbert
ms.author: sstabbert
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-match
- ci-merge
- ci-relationships
- customerInsights
ms.openlocfilehash: f2c14c169f5973b5f400989b9eeea593eba09182
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304320"
---
# <a name="update-unification-settings"></a>Eguneratu bateratze-ezarpenak

Profil bateratua sortu ondoren bateratze-ezarpenak berrikusteko edo aldatzeko, egin urrats hauek.

1. Joan **Datuak** > **Bateratu**.

   Banakako bezeroentzat (B-to-C), the **Bateratu** orrialdeak bateratze-urrats bakoitzeko bezero-profil eta fitxa bateratu kopurua bistaratzen du.

   :::image type="content" source="media/m3_unified.png" alt-text="Datuak bateratu ondoren datuak bateratu orriaren pantaila-argazkia." lightbox="media/m3_unified.png":::

   Enpresa kontuetarako (B-to-B), the **Bateratu** orrialdeak kontu bateratze-urrats bakoitzeko kontu bateratuaren profil eta lauza kopurua bistaratzen du. Kontaktuak bateratu baziren, kontaktuen bateratze-urrats bakoitzeko kontaktuen profil eta lauza bateratuen kopurua bistaratzen da. Aukeratu azpian dagoen fitxa egokia **Kontuak bateratu** edo **Batu kontaktuak (aurrebista)** eguneratu nahi duzunaren arabera.

   :::image type="content" source="media/b2b_unified.png" alt-text="Datuak bateratzea orriaren pantaila-argazkia kontua eta kontaktuaren datuak bateratu ondoren." lightbox="media/b2b_unified.png":::

   > [!TIP]
   > The **Bat datozen baldintzak** lauza entitate bat baino gehiago hautatuta badago soilik bistaratzen da.

1. Aukeratu zer eguneratu nahi duzun:
   - [Iturburu-eremuak](#edit-source-fields) entitateak edo atributuak gehitzeko edo atributu motak aldatzeko.
   - [Erregistro bikoiztuak](#manage-deduplication-rules) desduplicazio-arauak kudeatzeko edo hobespenak bateratzeko.
   - [Bat datozen baldintzak](#manage-match-rules) bi entitate edo gehiagotan bat datozen arauak eguneratzeko.
   - [Bezeroen eremu bateratuak](#manage-unified-fields) eremuak konbinatzeko edo baztertzeko. Erlazionatutako profilak multzotan ere taldeka ditzakezu.
   - [Eremu semantikoak](#manage-semantic-fields-for-unified-contacts) kontaktu-eremu bateratuetarako mota semantikoak kudeatzeko.
   - [Harremanak](#manage-contact-and-account-relationships) kontaktua konturako harremana kudeatzeko.

1. Aldaketak egin ondoren, aukeratu hurrengo aukera:

   - [Exekutatu bat datozen baldintzak](#run-matching-conditions) zure bat-etortze-baldintzen kalitatea azkar ebaluatzeko (desduplicazioa eta bat-etortze-arauak) profil bateratua eguneratu gabe. The **Exekutatu bat datozen baldintzak soilik** aukera ez da bistaratzen entitate bakarrerako.
   - [Bateratu profilak](#run-updates-to-the-unified-profile) bat datozen baldintzak exekutatzeko eta profil bateratuaren entitatea eguneratzeko, mendekotasunetan eragin gabe (aberastasunak, segmentuak edo neurriak, esaterako). Menpeko prozesuak ez dira exekutatzen, baina gisa eguneratuko dira [freskatze programazioan zehaztuta](schedule-refresh.md).
   - [Profilak eta mendekotasunak bateratzea](#run-updates-to-the-unified-profile) bat datozen baldintzak exekutatzeko, profil bateratuaren entitatea eguneratzeko eta mendekotasun guztiak eguneratzeko (aberastasunak, segmentuak edo neurriak, esaterako). Prozesu guztiak automatikoki berriro exekutatzen dira. B-to-B-n, bateratzea exekutatzen da profil bateratuak eguneratzen dituzten kontuetan eta kontaktu-entitateetan.

## <a name="edit-source-fields"></a>Editatu iturburu-eremuak

Ezin duzu kendu atributu edo entitate bat dagoeneko bateratuta badaude.

1. Hautatu **Editatu** gainean **Iturburu-eremuak** teila.

   :::image type="content" source="media/m3_source_edit.png" alt-text="Iturburu-eremuen orriaren pantaila-argazkia, gako nagusien, mapatutako eta mapatu gabeko eremuen kopurua erakusten duena":::

   Mapatutako eta mapatu gabeko eremuen kopurua bistaratzen da.

1. Beste atributu edo entitate batzuk gehitzeko, hautatu **Hautatu entitateak eta eremuak**.

1. Aukeran, entitate baten gako nagusia, atributu motak eta txandaka ditzakezu **Kartografia adimenduna** piztu edo itzali. Informazio gehiagorako, ikus [Hautatu iturri-eremuak](map-entities.md).

1. Hautatu **Hurrengoa** desduplicazio-arauetan aldaketak egiteko, edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-unification-settings).

## <a name="manage-deduplication-rules"></a>Kudeatu deduplicazio-arauak

1. Hautatu **Editatu** gainean **Erregistro bikoiztuak** teila.

   :::image type="content" source="media/m3_duplicates_edit.png" alt-text="Bikoiztutako erregistroen orriaren pantaila-argazkia, bikoiztutako erregistro kopurua erakusten duena" lightbox="media/m3_duplicates_edit.png":::

   Aurkitutako erregistro bikoiztuen kopurua azpian agertzen da **Bikoiztuak**. The **Erregistroak bikoiztu egin dira** zutabeak erregistro bikoiztuak zein entitate zituzten eta erregistro bikoiztuen ehunekoa erakusten du.

1. Entitate aberastua erabiltzeko, hautatu **Erabili entitate aberastuak**. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md).

1. Desduplicazio-arauak kudeatzeko, aukeratu aukera hauetako bat:
   - **Sortu arau berri bat** : Hautatu **Gehitu araua** dagokion entitatearen pean. Informazio gehiagorako, ikus [Desduplicazio-arauak definitu](remove-duplicates.md#define-deduplication-rules).
   - **Aldatu arau-baldintzak** : Hautatu araua eta gero **Editatu**. Aldatu eremuak, gehitu edo kendu baldintzak, edo gehitu edo kendu salbuespenak.
   - **Aurrebista** : Hautatu araua eta gero **Aurrebista** arau honen azken exekuzioaren emaitzak ikusteko.
   - **Desaktibatu arau bat** : Hautatu araua eta gero **Desaktibatu** desduplicazio-arau bat gordetzeko, parekatze-prozesutik kanpo uzten duen bitartean.
   - **Bikoiztu arau bat** : Hautatu araua eta gero **Bikoiztu** aldaketekin antzeko arau bat sortzeko.
   - **Ezabatu arau bat** : Hautatu araua eta gero **Ezabatu**.

1. Batzeko hobespenak aldatzeko, hautatu entitatea. Arau bat sortzen bada bakarrik alda ditzakezu hobespenak.
   1. Hautatu **Editatu bateratze-hobespenak** eta aldatu **Erregistroa gordetzeko** aukera.
   1. Entitate baten atributu indibidualetan bateratze-hobespenak aldatzeko, hautatu **Aurreratua** eta egin behar diren aldaketak.

   1. Hautatu **Eginda**.

1. Hautatu **Hurrengoa** bat datozen baldintzetan aldaketak egiteko, edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-unification-settings).

## <a name="manage-match-rules"></a>Kudeatu bat egiteko arauak

Partiduen parametro gehienak birkonfigura eta doitu ditzakezu. Ezin dituzu entitateak gehitu edo ezabatu. Bat-etortze-arauak ez zaizkio aplikatzen entitate bakar bati.

1. Hautatu **Editatu** gainean **Bat datozen baldintzak** teila.

   :::image type="content" source="media/m3_match_edit.png" alt-text="Partiduen arauak eta baldintzak orrialdearen pantaila-argazkia estatistikekin." lightbox="media/m3_match_edit.png":::

   Orriak partida-ordena eta definitutako arauak eta estatistikak bistaratzen ditu:
   - **Iturburu-erregistro bakarrak** erakutsi azken partidaren exekuzioan prozesatu diren iturburu-erregistro indibidualen kopurua.
   - **Erregistroak parekatuak eta bat ez direnak** nabarmendu zenbat erregistro bakar geratzen diren partida-arauak prozesatu ondoren.
   - **Bat datozen erregistroak soilik** erakutsi partida-kopurua zure partida bikote guztietan.

1. Arau guztien emaitzak eta haien puntuazioak ikusteko, hautatu **Ikusi azken lasterketa**. Emaitzak bistaratzen dira, ordezko kontaktuen IDak barne. Emaitzak deskargatu ditzakezu.

1. Arau jakin baten emaitzak eta puntuazioak ikusteko, hautatu araua eta gero **Aurrebista**. Emaitzak bistaratzen dira. Emaitzak deskargatu ditzakezu.

1. Baldintza jakin baten emaitzak arau batean ikusteko, hautatu araua eta gero **Editatu**. Editatu panelean, hautatu **Aurrebista** baldintzapean. Emaitzak deskargatu ditzakezu.

   :::image type="content" source="media/m3_match_condition_preview.png" alt-text="Bat ez datozen eta bat datozen erregistroen irudikapen grafikoa, datuen zerrenda barne.":::

1. Entitate aberastua gehitu baduzu, hautatu **Erabili entitate aberastuak**. Informazio gehiagorako, ikus [Datu iturrietarako aberastea](data-sources-enrichment.md).

1. Arauak kudeatzeko, aukeratu aukera hauetako bat:
   - **Sortu arau berri bat** : Hautatu **Gehitu araua** dagokion entitatearen pean. Informazio gehiagorako, ikus [Partiduen bikoteen arauak zehaztu](match-entities.md#define-rules-for-match-pairs).
   - **Aldatu zure arauen ordena** hainbat arau definitu badituzu: Arrastatu eta jaregin arauak nahi duzun ordenan. Informazio gehiagorako, ikus [Zehaztu partida-ordena](match-entities.md#specify-the-match-order).
   - **Aldatu arau-baldintzak** : Hautatu araua eta gero **Editatu**. Aldatu eremuak, gehitu edo kendu baldintzak, edo gehitu edo kendu salbuespenak.
   - **Desaktibatu arau bat** : Hautatu araua eta gero **Desaktibatu** parekatze-arau bat gordetzea, parekatze-prozesutik kanpo uzten duen bitartean.
   - **Bikoiztu arau bat** : Hautatu araua eta gero **Bikoiztu** aldaketekin antzeko arau bat sortzeko.
   - **Ezabatu arau bat** : Hautatu araua eta gero **Ezabatu**.

1. Hautatu **Hurrengoa** eremu bateratuetan aldaketak egiteko, edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-unification-settings).

## <a name="manage-unified-fields"></a>Kudeatu eremu bateratuak

1. Hautatu **Editatu** gainean **Bezeroen eremu bateratuak** teila.

    :::image type="content" source="media/m3_merge_edit.png" alt-text="Bezeroen eremu bateratuen pantaila-argazkia":::

1. Berrikusi konbinatutako eta baztertutako eremuak, eta egin aldaketak behar izanez gero. Gehitu edo editatu CustomerID gakoa edo taldekatu profilak multzoetan. Informazio gehiagorako, ikus [Bateratu bezeroen eremuak](merge-entities.md).

1. Bezeroetarako edo kontuetarako, hautatu **Hurrengoa** berrikusteko eta [profil bateratua eta mendekotasunak eguneratu](#run-updates-to-the-unified-profile). Edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-unification-settings) aldaketa gehiago egiteko.

   Kontaktuetarako, hautatu **Hurrengoa** eremu semantikoak kudeatzeko. Edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-unification-settings) aldaketa gehiago egiteko.

## <a name="manage-semantic-fields-for-unified-contacts"></a>Kudeatu kontaktu bateratuetarako eremu semantikoak

1. Hautatu **Editatu** gainean **Eremu semantikoak** teila.

1. Eremu bateratu baten mota semantikoa aldatzeko, hautatu mota berri bat. Informazio gehiagorako, ikus [Definitu kontaktu bateratuen eremu semantikoak](data-unification-contacts.md#define-the-semantic-fields-for-unified-contacts).

1. Hautatu **Hurrengoa** kontua eta harremana kudeatzeko, edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-unification-settings) aldaketa gehiago egiteko.

## <a name="manage-contact-and-account-relationships"></a>Kudeatu kontaktu eta kontu harremanak

1. Hautatu **Editatu** gainean **Harremanak** teila.

1. Kontaktua eta kontuaren harremana aldatzeko, aldatu informazio hauetako bat:

   - **Harremanetarako entitatearen atzerriko gakoa** : Aukeratu zure kontaktu-entitatea kontuarekin lotzen duen atributua.
   - **Kontu-entitateari** : Aukeratu kontaktuarekin lotutako kontu-entitatea.

1. Hautatu **Hurrengoa** bateratze-ezarpenak berrikusteko eta [profil bateratua eta mendekotasunak eguneratu](#run-updates-to-the-unified-profile), edo hautatu **Gorde eta itxi** eta itzuli [Eguneratu bateratze-ezarpenak](#update-unification-settings) aldaketa gehiago egiteko.

## <a name="run-matching-conditions"></a>Exekutatu bat datozen baldintzak

Exekutatu bat datozen baldintzak desduplicazioa eta bat-etortze-arauak soilik exekutatzen ditu eta eguneratzen du *Desbikoizpena_* * eta *ConflationMatchPair* entitateak.

1. Tik **Datuak** > **Bateratu** orrialdea, hautatu **Exekutatu bat datozen baldintzak soilik**.

   The **Erregistro bikoiztuak** eta **Bat datozen baldintzak** fitxak erakusten **Ilaran jarrita** edo **Freskagarria** egoera.

   [!INCLUDE [progress-details-pane-include](includes/progress-details-pane.md)]

1. Lotze-prozesua amaitzen denean, hautatu **Editatu** gainean **Bat datozen baldintzak** teila.

   :::image type="content" source="media/match-KPIs.png" alt-text="Partiduen orriko gakoen neurrien pantaila moztua zenbakiekin eta xehetasunekin.":::

1. Aldaketak egiteko, ikus [Kudeatu deduplicazio-arauak](#manage-deduplication-rules) edo [Kudeatu partida-arauak](#manage-match-rules).

1. Exekutatu partida-prozesua berriro edo [exekutatu profilaren eguneraketak](#run-updates-to-the-unified-profile).

## <a name="run-updates-to-the-unified-profile"></a>Exekutatu profil bateratuaren eguneraketak

- Bat datozen baldintzak exekutatzeko eta profil bateratuaren entitatea eguneratzeko *gabe* mendekotasunei eragiten dietenak (adibidez, bezeroen txartelak, aberasteak, segmentuak edo neurriak), hautatu **Bateratu bezeroen profilak**. Kontuetarako, hautatu **Kontuak bateratu** > **Bateratu profilak**. Kontaktuetarako, hautatu **Batu kontaktuak (aurrebista)** > **Bateratu profilak**. Menpeko prozesuak ez dira exekutatzen, baina gisa eguneratuko dira [freskatze programazioan zehaztuta](schedule-refresh.md).
- Bat datozen baldintzak exekutatzeko, eguneratu profil bateratua eta menpekotasun guztiak exekutatzeko, hautatu **Bezeroen profilak eta menpekotasunak bateratzea**. Prozesu guztiak automatikoki berriro exekutatzen dira. Kontuetarako eta kontaktuetarako, hautatu **Kontuak bateratu** > **Profilak eta mendekotasunak bateratzea**. Bat datozen baldintzak bi kontuetarako eta kontaktuetarako exekutatzen dira, profil bateratuak eta gainerako menpekotasun guztiak eguneratuz.

Fitxa guztiak izan ezik **Iturburu-eremuak** erakutsi **Ilaran jarrita** edo **Freskagarria**.

[!INCLUDE [progress-details-pane-include](includes/progress-details-pane.md)]

Korrika arrakastatsu baten emaitzak bistaratzen dira **Bateratu** profil bateratuen kopurua erakusten duen orrialdea.
