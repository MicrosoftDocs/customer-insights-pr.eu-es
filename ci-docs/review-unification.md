---
title: Berrikusi datuen bateratzea
description: Berrikusi datuak bateratzeko urratsak, sortu bezeroen profil bateratuak eta berrikusi emaitzak
ms.date: 08/12/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: adkuppa
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-match
- ci-merge
- ci-relationships
- customerInsights
ms.openlocfilehash: b4d77effc347e40fecde625a1a42a24900456471
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9303952"
---
# <a name="review-data-unification"></a>Berrikusi datuen bateratzea

Berrikusi aldaketen laburpena, sortu profil bateratua eta berrikusi emaitzak.

## <a name="review-and-create-customer-profiles"></a>Berrikusi eta sortu bezero-profilak

Bateratze-prozesuaren azken urrats honek prozesuaren urratsen laburpena erakusten du eta profil bateratua sortu aurretik aldaketak egiteko aukera ematen du.

[!INCLUDE [m3-first-run-note](includes/m3-first-run-note.md)]

:::image type="content" source="media/m3_review.png" alt-text="Berrikusi eta bezeroen profilak sortu pantaila-argazkia.":::

1. Hautatu **Editatu** datuak bateratzeko edozein urratsetan aldaketak berrikusteko eta egiteko.

1. Zure hautapenekin pozik bazaude, hautatu **Sortu bezeroen profilak** (edo **Sortu kontu-profilak** B-tik Brako). The **Bateratu** orria bistaratzen da bezeroaren profil bateratua sortzen ari den bitartean.

   :::image type="content" source="media/m3_unify_refreshing.png" alt-text="Unify orriaren pantaila-argazkia Ilaran edo Freskatzen erakusten duten lauzekin.":::

   [!INCLUDE [progress-details-pane-include](includes/progress-details-pane.md)]

Bateratze algoritmoak denbora pixka bat behar du osatzeko eta ezin duzu konfigurazioa aldatu amaitu arte.

## <a name="view-the-results-of-data-unification"></a>Ikusi datuak bateratzearen emaitzak

Bateratzearen ondoren, **Datuak** > **Bateratu** orrialdeak bezeroen profil bateratuen kopurua erakusten du (edo B-to-B-rako kontu profilak). Batasun-prozesuko urrats bakoitzaren emaitzak fitxa bakoitzean bistaratzen dira. Adibidez, **Iturburu-eremuak** mapatutako atributu kopurua (eremuak) erakusten du eta **Erregistro bikoiztuak** aurkitutako erregistro bikoiztuen kopurua erakusten du.

:::image type="content" source="media/m3_unified.png" alt-text="Datuak bateratu ondoren datuak bateratu orriaren pantaila-argazkia.":::

> [!TIP]
> The **Bat datozen baldintzak** lauza entitate bat baino gehiago hautatuta badago soilik bistaratzen da.

Emaitzak berrikustea gomendatzen dizugu, batez ere zure kalitatea [partida arauak](data-unification-update.md#manage-match-rules) eta hobetu behar izanez gero.

Beharrezkoa denean, [egin aldaketak bateratze-ezarpenetan](data-unification-update.md) eta berriro exekutatu profil bateratua.

### <a name="verify-output-entities-from-data-unification"></a>Egiaztatu datuen bateratzetik irteerako entitateak

Joan **Datuak** > **Entitateak** irteerako entitateak egiaztatzeko.

Bezeroen profilaren entitate bateratua, deitua *Bezeroa*, pantailan **Profilak** atala. Lehenengo bateratze-exekutatu arrakastatsuak bateratua sortzen du *Bezeroa* entitate. Ondorengo exekuzio guztiek entitate hori zabaltzen dute.

Desduplicazio eta konflazio entitateak sortu eta bistaratzen dira **Sistema** atala. Iturburuko entitate bakoitzeko desbikoiztutako entitate bat sortzen da izenarekin **Deduplication_DataSource_Entity**. The **ConflationMatchPairs** entitateak entitateen arteko bat-etortzeei buruzko informazioa dauka.

Bikoiztuak desegiteko irteerako entitate batek informazio hau dauka:
- IDak eta gakoak
  - Gako nagusia eta Ordezko ID eremuak. Ordezko ID eremua erregistro baterako identifikatutako ordezko ID guztiek osatzen dute.
  - Deduplication_GroupId eremuak zehaztutako bikoiztuak desegiteko eremuetan oinarritutako antzeko erregistro guztiak multzokatzen dituen entitate baten barruan identifikatutako taldea edo klusterra erakusten du. Sistema prozesatzeko helburuarekin erabiltzen da. Eskuzko bikoiztuak desegiteko araurik zehazten ez bada eta sistemak definitutako bikoiztuak desegiteko arauak aplikatzen badira, baliteke eremu hori bikoiztuak desegiteko irteerako entitatean ez aurkitzea.
  - Deduplication_WinnerId: eremu honek identifikatutako talde edo klusterren irabazlearen IDa dauka. Deduplication_WinnerId erregistroaren gako nagusiaren balioaren berdina bada, erregistroa irabazle erregistroa dela esan nahi du.
- Bikoiztuak desegiteko arauak definitzeko erabiltzen diren eremuak.
- Arau eta Puntuazio eremuak bikoiztuak desegiteko arauetatik zein aplikatu den eta bat datorren algoritmoak emandako puntuazioa adierazteko.

## <a name="next-step"></a>Hurrengo urratsa

- B-to-B-rako, egin aukeran [kontaktuen bateratzea](data-unification-contacts.md).

- B-to-C-rako, konfiguratu [jarduerak](activities.md),[aberastasunak](enrichment-hub.md),[harremanak](relationships.md), edo [neurriak](measures.md) zure bezeroei buruzko informazio gehiago lortzeko.

[!INCLUDE[footer-include](includes/footer-banner.md)]
