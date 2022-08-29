---
title: Esleipen semantikoak (aurreargitalpena)
description: Kartografia semantikoen ikuspegi orokorra eta nola erabili.
ms.date: 08/12/2022
ms.subservice: audience-insights
ms.reviewer: v-wendysmith
ms.topic: conceptual
author: CadeSanthaMSFT
ms.author: cadesantha
manager: shellyha
searchScope:
- ci-semantic-mapping
- customerInsights
ms.openlocfilehash: 8780c11c8b091717349f0fd75a36b99c3a63ab49
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9303861"
---
# <a name="semantic-mappings-preview"></a>Esleipen semantikoak (aurreargitalpena)

> [!NOTE]
> The **Mapeo semantikoak** orria orri hau erabiliz kontaktuen profilak sortu diren negozio-inguruneetarako (B-to-B) soilik dago erabilgarri. Harremanetarako profil indibidualak sortzen eta kudeatzen jarrai dezakezu **Mapeo semantikoak** orrialdea. Edo, [bateratu zure harremanetarako datuak](data-unification-contacts.md) bikoiztuak kentzeko, entitateen arteko bat-etortzeak identifikatzeko eta kontaktu profil bateratu bat sortzeko. Ondoren, kontaktu profil bateratua erabil dezakezu kontaktu mailako jarduerak sortzeko.

Kartografia semantikoek jarduerarik gabeko datuak aurrez definitutako eskemetara mapatzen uzten dizute. Eskema hauek Customer Insights-i zure datuen atributuak hobeto ulertzen laguntzen dute. Mapa semantikoak eta emandako datuek Customer Insights-en ikuspegi eta eginbide berriak ahalbidetzen dituzte. Zure jardueren datuak eskemetara mapatzeko, berrikusi [jarduerak](activities.md) dokumentazioa.

## <a name="define-a-contactprofile-semantic-entity-mapping"></a>Definitu ContactProfile entitateen mapaketa semantikoa

1. Joan **Datuak** > **Mapeo semantikoak (aurrebista)**.

1. Aukeratu **Gehitu mapaketa semantikoa** esperientzia gidatua hasteko.

1. Urtean **Entitatearen datuak** urratsa, ezarri ondoko eremuetarako balioak:

   - **Entitate semantikoaren maparen izena** : izena zure entitate semantikoaren mapak egiteko.
   - **Jatorri Entitatea** : harremanetarako datuak biltzen dituen entitatea.
   - **Lehen gakoa** : kontaktu-erregistro bat modu esklusiboan identifikatzen duen eremua. Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.

   :::image type="content" source="media/Semantic_Mapping_Wizard1.png" alt-text="Konfiguratu entitateen mapaketa semantikoa izena, iturburu entitatea eta gako nagusiarekin.":::

1. Hautatu **Hurrengoa**.

1. Urtean **Harremanak** urratsa, konfiguratu xehetasunak zure harremanetarako datuak dagozkien kontuko datuekin konektatzeko. Urrats honek entitateen arteko konexioa bistaratzen du.  

   Inplementatu daitezkeen bi harreman mota daude: **Harreman zuzenak** eta **Zeharkako harremanak**. Informazio gehiagorako, joan hona [harreman zuzeneko eta zeharkako bideak](relationships.md#relationship-paths).

   1. Hautatu **Gehitu harremana** harremana konfiguratzeko.
   1. Aukeratu zure iturburuko entitatearen atributua zure harremanetarako entitatea beste entitate batekin konektatzen duena.
   1. Aukeratu entitatea zure harremanetarako entitatearekin konektatzeko. Aukeratu entitate bat **Kontu-entitateak** edo **Bitarteko entitatea** atala. Tarteko entitate bat hautatzen baduzu, definitu bigarren harreman bat zure xede-kontuaren entitatearekin konektatzeko.

      :::image type="content" source="media/Semantic_Mapping_Wizard2.png" alt-text="Aukeratu Kontuko entitatea edo Bitarteko entitatea.":::

   1. Eman **Harremanaren izena**. Zure entitateen arteko harremana lehendik badago, harremanaren izena irakurtzeko soilik da. Harremanik ez badago, harreman berria sortuko da zuk emandako izenarekin.
   1. Aukeratu **Aplikatu** harreman konfigurazioa amaitzeko.

   > [!NOTE]
   > Harreman gehiago konfigura ditzakezu harremanetarako entitatearen eta tarteko entitateekin beste kontu-entitate batzuen artean.
   
     :::image type="content" source="media/Semantic_Mapping_Wizard4.png" alt-text="Hainbat harreman bistaratzeak harremanetarako entitateak kontuko entitateekin lotzen ditu.":::

1. Hautatu **Hurrengoa**.

1. Urtean **Ezarri mota semantikoa** urratsa, aukeratu bat **Mota semantikoa**. Gaur egun, bada bat **Mota semantikoa** deitu *ContactProfile*.

1. Mapeatu zure kontaktuaren ID-ra *HarremanetarakoProfila* mota semantikoa **Harremanetarako IDa**. Aukeran, mapatu beste eremu batzuk, hala nola izen, abizen, generoa edo posta elektronikoa.

   :::image type="content" source="media/Semantic_Mapping_Wizard5.png" alt-text="Mapatu zure harremanetarako datuen atributuak beharrezko eta aukerako eremuekin.":::

1. Hautatu **Hurrengoa**.

1. urtean **Berrikuspena** urratsa, berrikusi mapa semantikoaren konfigurazioa. Aldaketak egiteko, hautatu **Editatu** dagokion atalerako.

1. Sakatu **Gorde**.

1. Mapa semantikoa prozesatzeko, hautatu **Korrika egin**. Edo hautatu **Itxi** zure mapa semantikoa prozesatu gabe gordetzeko. Geroago exekutatzeko, hautatu mapa semantikoa eta hautatu **Freskatu**.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="manage-existing-semantic-mappings"></a>Kudeatu lehendik dauden mapaketa semantikoak

Joan **Datuak** > **Mapeo semantikoak (aurrebista)** gordetako mapa semantikoak, haien iturburu-entitatea, mota semantikoa, mapa mota eta egoera ikusteko.

:::image type="content" source="media/semantic-mapping-options.png" alt-text="Kartografia semantikoak kudeatzeko aukerak.":::

Hautatu mapa semantikoa erabilgarri dauden ekintzak ikusteko.
- **Editatu** egungo konfigurazioa. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.
- **Freskatu** azken datuak sartzeko mapa semantikoa. Edozein mapaketa semantiko freskatzeak mota bereko mapaketa semantiko guztiak freskatuko ditu.
- **Aldatu izena** mapa semantikoa. Sakatu **Gorde**.
- **Ezabatu** mapa semantikoa. Kartografia semantiko bat baino gehiago aldi berean ezabatzeko, hautatu mapa semantikoak eta ezabatzeko ikonoa. Hautatu **Ezabatu** ezabatzea baieztatzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
