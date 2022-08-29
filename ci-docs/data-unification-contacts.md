---
title: Sortu kontaktu profil bateratua (aurrebista)
description: Joan datuak bateratzeko prozesua kontaktuen datu-multzo nagusi bakarra sortzeko.
ms.date: 08/12/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: overview
author: Scott-Stabbert
ms.author: sstabbert
manager: shellyha
searchScope:
- ci-map
- ci-match
- ci-merge
- customerInsights
ms.openlocfilehash: 721f47563582a94b5b8244ca5d5d7d1350695512
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9305058"
---
# <a name="create-a-unified-contact-profile-preview"></a>Sortu kontaktu profil bateratua (aurrebista)

Ondoren [negozio-kontuak bateratzea](map-entities.md), aukeran, kontu horietako kontaktuak batera ditzakezu eta kontaktu bateratuak kontu bateratuekin lotu ditzakezu. Kontaktuak bateratzeko prozesuak hainbat datu-iturritako kontaktuen datuak mapatzen ditu, bikoiztuak kentzen ditu, entitateen arteko datuak bat egiten ditu, mapa semantikoa konfiguratzen du, kontaktuen eta kontuen arteko harremanak sortzen ditu eta gero kontaktu profil bateratua sortzen du.

[!INCLUDE [m3-first-run-note](includes/m3-first-run-note.md)]

Lehen urratsak kontuak bateratzeko urratsen berdinak dira.

## <a name="prerequisites"></a>Aurrebaldintzak

Kontuen eta kontaktuen erregistroek konektatzen dituen gako esklusibo bat izan behar dute (atzerriko gakoa deitzen dena). Adibidez, kontua eta kontaktua elkarrekin lotzen dituen kontuaren erregistroan eta kontaktuen erregistroan dagoen kontu ID bat.

## <a name="preview-limitations"></a>Aurrebistaren mugak

- Kontu baterako estekarik ez duten kontaktuak kentzen dira.
- Kontu bat desbikoiztuta badago, irabazlearen erregistroa identifikatzen da bateratze-hobespenetan oinarrituta. Galtzaileen erregistroak ez dira hautatzen eta, beraz, kentzen dira. Galtzen diren erregistroekin lotutako kontaktuak ezeztatu egiten dira.
- Kontu batek hainbat kontaktu izan ditzake, baina kontaktu bat kontu bakar bati lotuta dago.
- Mapa semantikoaren urratsean mapatutako kontaktu-atributuak dira Bezero-txartelean bistaratu daitezkeen atributu bakarrak. Hala ere, 17 atributu daude eskuragarri.

## <a name="select-source-fields"></a>Hautatu iturri-eremuak

1. Azpian **Batu kontaktuak (aurrebista)**, hautatu **Hasi**.

1. [Hautatu entitateak eta eremuak](map-entities.md) zure kontaktu datuen iturrietarako, gako nagusiak eta atributu motak barne.

1. Hautatu **Hurrengoa**.

## <a name="remove-duplicate-records"></a>Kendu erregistro bikoiztuak

1. Aukeran, [deduplicazio-arauak definitzea](remove-duplicates.md) hautatutako entitateentzat.

1. Hautatu **Hurrengoa**.

## <a name="match-conditions"></a>Partiduen baldintzak

1. [Partiduen ordena eta arauak zehaztu](match-entities.md) entitate gurutzatuak parekatzeko.

1. Hautatu **Hurrengoa**.

## <a name="unify-contact-fields"></a>Batu kontaktuen eremuak

1. [Konbinatu eta baztertu harremanetarako eremuak](merge-entities.md).

1. Hautatu **Hurrengoa**.

## <a name="define-the-semantic-fields-for-unified-contacts"></a>Definitu kontaktu bateratuen eremu semantikoak

Bateratze-prozesuko urrats honek zure kontaktu-eremu bateratuak mota semantikoekin mapatzen ditu. B-to-B-n, bezeroen txartelek kontuak erakusten dituzte. Txartela hautatzen denean, kontuarekin lotutako kontaktu guztiak bistaratzen dira. Urrats honetan mapatzen dituzun eremuak txarteletan agertuko diren eremuak dira.

1. Hautatu eremu bateratu bakoitzari lotzen zaion mota semantikoa. Hautatu **Bat ere ez** mota semantikorik eskuragarri ez badago.

   :::image type="content" source="media/semantic_mapping.png" alt-text="Mota semantikoak definitzeko eremu semantikoen orriaren pantaila-argazkia." lightbox="media/semantic_mapping.png":::

1. Eremu bateratu guztiak mapatu ondoren, hautatu **Hurrengoa**.

## <a name="set-the-relationship-between-contacts-and-accounts"></a>Ezarri kontaktuen eta kontuen arteko harremana

Bateratze-prozesuko urrats honek zure kontaktu-datuak dagozkion kontu-datuekin lotzen ditu.

1. Entitate bakoitzeko, sartu informazio hau:

   - **Harremanetarako entitatearen atzerriko gakoa** : Aukeratu zure kontaktu-entitatea kontuarekin lotzen duen atributua.
   - **Kontu-entitateari** : Aukeratu kontaktuarekin lotutako kontu-entitatea.

   :::image type="content" source="media/contact_relationship.png" alt-text="Harreman orriaren pantaila-argazkia kontaktua eta kontua entitateak konektatzeko.":::

1. Hautatu **Hurrengoa**.

## <a name="review-contact-unification"></a>Berrikusi kontaktuen bateratzea

Berrikusi aldaketen laburpena, sortu profil bateratua eta berrikusi emaitzak.

### <a name="review-and-create-contact-profiles"></a>Berrikusi eta sortu kontaktu-profilak

Bateratze-prozesuko azken urrats honek prozesuaren urratsen laburpena erakusten du eta aldaketak egiteko aukera ematen du kontaktu profil bateratua sortu aurretik.

:::image type="content" source="media/b2b_review_contacts.png" alt-text="Berrikusi eta sortu kontaktu profilak pantaila-argazkia.":::

1. Hautatu **Editatu** kontaktuak bateratzeko edozein urratsetan aldaketak berrikusteko eta egiteko.

1. Zure hautapenekin pozik bazaude, hautatu **Sortu harremanetarako profilak**. The **Bateratu** orrialdea bistaratzen da kontaktu profil bateratua sortzen ari den bitartean.
  
   :::image type="content" source="media/b2b_unify_refreshing.png" alt-text="Unify Contacts orriaren pantaila-argazkia Ilaran edo Freskatzen erakusten duten lauzekin.":::

   [!INCLUDE [progress-details-pane-include](includes/progress-details-pane.md)]

Bateratze algoritmoak denbora pixka bat behar du osatzeko eta ezin duzu konfigurazioa aldatu amaitu arte.

### <a name="view-the-results-of-contact-unification"></a>Ikusi kontaktuen bateratzearen emaitzak

Bateratzea amaitu ondoren, **Datuak** > **Bateratu** orrialdeak kontaktu profil bateratuen kopurua erakusten du. Batasun-prozesuko urrats bakoitzaren emaitzak fitxa bakoitzean bistaratzen dira. Adibidez, **Iturburu-eremuak** mapatutako atributu kopurua (eremuak) erakusten du eta **Erregistro bikoiztuak** aurkitutako erregistro bikoiztuen kopurua erakusten du.

:::image type="content" source="media/unified_contacts.png" alt-text="Kontaktuak bateratu ondoren Datuak bateratzea orriaren pantaila-argazkia.":::

> [!TIP]
> The **Bat datozen baldintzak** lauza entitate bat baino gehiago hautatuta badago soilik bistaratzen da.

Emaitzak berrikustea gomendatzen dizugu, batez ere zure kalitatea [partida arauak](data-unification-update.md#manage-match-rules) eta hobetu behar izanez gero.

Beharrezkoa denean, [egin aldaketak kontaktuen bateratze-ezarpenetan](data-unification-update.md) eta berriro exekutatu profil bateratua.

### <a name="verify-output-entities-from-data-unification"></a>Egiaztatu datuen bateratzetik irteerako entitateak

Joan **Datuak** > **Entitateak** irteerako entitateak egiaztatzeko.

Kontaktu-profilaren entitate bateratua, deitua *HarremanetarakoProfila*, pantailan **Entitate semantikoak** atala. Lehenengo bateratze-exekutatu arrakastatsuak bateratua sortzen du *HarremanetarakoProfila* entitate. Ondorengo exekuzio guztiek entitate hori zabaltzen dute.

The *KontaktuakBezeroa* entitatea (aurrebista) sortu eta bistaratzen da **Profilak** atala. Entitate honek kontaktuen datuak ditu kontuetarako estekarik gabe. Entitate hau kontaktuen bateratzearen mapa semantikorako eta harremanetarako urratsetarako sarrera gisa erabiltzen da.

Desduplicazio eta konflazio entitateak sortu eta bistaratzen dira **Sistema** atala. Iturburuko entitate bakoitzeko desbikoiztutako entitate bat sortzen da izenarekin **Deduplication_DataSource_Entity**. The **KontaktuakConflationMatchPairs** entitateak entitateen arteko bat-etortzeei buruzko informazioa dauka.

Bikoiztuak desegiteko irteerako entitate batek informazio hau dauka:
- IDak eta gakoak
  - Gako nagusia eta Ordezko ID eremuak. Ordezko ID eremua erregistro baterako identifikatutako ordezko ID guztiek osatzen dute.
  - Deduplication_GroupId eremuak zehaztutako bikoiztuak desegiteko eremuetan oinarritutako antzeko erregistro guztiak multzokatzen dituen entitate baten barruan identifikatutako taldea edo klusterra erakusten du. Sistema prozesatzeko helburuarekin erabiltzen da. Eskuzko bikoiztuak desegiteko araurik zehazten ez bada eta sistemak definitutako bikoiztuak desegiteko arauak aplikatzen badira, baliteke eremu hori bikoiztuak desegiteko irteerako entitatean ez aurkitzea.
  - Deduplication_WinnerId: eremu honek identifikatutako talde edo klusterren irabazlearen IDa dauka. Deduplication_WinnerId erregistroaren gako nagusiaren balioaren berdina bada, erregistroa irabazle erregistroa dela esan nahi du.
- Bikoiztuak desegiteko arauak definitzeko erabiltzen diren eremuak.
- Arau eta Puntuazio eremuak bikoiztuak desegiteko arauetatik zein aplikatu den eta bat datorren algoritmoak emandako puntuazioa adierazteko.

## <a name="next-step"></a>Hurrengo urratsa

Konfiguratu [jarduerak](activities.md),[aberastea](enrichment-hub.md), edo [harremanak](relationships.md) zure kontaktuei buruzko informazio gehiago lortzeko.
