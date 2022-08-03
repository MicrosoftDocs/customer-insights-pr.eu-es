---
title: Esleipen semantikoak (aurreargitalpena)
description: Kartografia semantikoen ikuspegi orokorra eta nola erabili.
ms.date: 12/01/2021
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: CadeSanthaMSFT
ms.author: cadesantha
manager: shellyha
searchScope:
- ci-semantic-mapping
- customerInsights
ms.openlocfilehash: 7c9588ac7a132ca6f43cf26ea3a744109a0dd2b8
ms.sourcegitcommit: ad74ace653db9a25fce4343adef7db1c9b0d8904
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183616"
---
# <a name="semantic-mappings-preview"></a>Esleipen semantikoak (aurreargitalpena)

Kartografia semantikoek jarduerarik gabeko datuak aurrez definitutako eskemetara mapatzen uzten dizute. Eskema hauek Customer Insights-i zure datuen atributuak hobeto ulertzen laguntzen diote. Mapa semantikoak eta emandako datuek Customer Insights-en ikuspegi eta eginbide berriak ahalbidetzen dituzte. Zure jardueren datuak eskemetara mapatzeko, berrikusi [jarduerak](activities.md) dokumentazioa.

**Gaur egun mapaketa semantikoak gaituta daude negozio kontuetan oinarritutako inguruneetan**. *HarremanetarakoProfila* Customer Insights-en gaur egun eskuragarri dagoen mapa semantiko mota bakarra da.

## <a name="define-a-contactprofile-semantic-entity-mapping"></a>Definitu ContactProfile entitateen mapaketa semantikoa

1. Joan **Datuak** > **Mapeo semantikoak (aurrebista)**.

1. Aukeratu **Gehitu mapaketa semantikoa** esperientzia gidatua hasteko.

1. Urtean **Entitatearen datuak** urratsa, ezarri ondoko eremuetarako balioak:

   - **Entitate semantikoaren maparen izena** : izena zure entitate semantikoaren mapak egiteko.
   - **Iturburu Entitatea** : harremanetarako datuak biltzen dituen entitatea.
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

## <a name="use-a-contactprofile-semantic-entity-mapping-to-create-contact-level-activities"></a>Erabili ContactProfile entitate semantikoen mapaketa kontaktu mailako jarduerak sortzeko

Bat sortu ondoren *Harremanetarako Profila* entitate semantikoen mapaketa, kontaktuen jarduerak har ditzakezu. Kontu baten jardueraren kronograman ikus dezakezu zein kontaktu zen jarduera bakoitzaren arduraduna. Urrats gehienek jarduera-mapearen konfigurazio tipikoari jarraitzen diote.

   > [!NOTE]
   > Kontaktu mailako jarduerak funtzionatzeko, biak izan behar dituzu **Kontuaren ID** eta **Kontaktu ID** zure jarduera-datuen barruan erregistro bakoitzerako atributuak.

1. [Definitu a *HarremanetarakoProfila* entitate semantikoen mapaketa](#define-a-contactprofile-semantic-entity-mapping) eta exekutatu mapa semantikoa.

1. Joan **Datuak** > **Jarduerak**.

1. Hautatu **Gehitu jarduera** jarduera berri bat sortzeko.

1. Jarriari izena eman, hautatu iturburuko jarduera-entitatea eta hautatu jarduera-entitatearen gako nagusia.

1. urtean **Harremanak** urratsa, sortu zure jarduera-iturburuko datuen arteko zeharkako harremana kontuekin, zure harremanetarako datuak bitartekari gisa erabiliz. Informazio gehiagorako, ikus [zuzeneko eta zeharkako harreman bideak](relationships.md#relationship-paths).
   - Deitutako jarduera baterako erlazio adibidea *Erosketak*:
      - **Erosketak Iturburu Jardueren Datuak** > **Harremanetarako datuak** atributuaren gainean **Kontaktu ID**
      - **Harremanetarako datuak** > **Kontuaren datuak** atributuaren gainean **Kontuaren ID**

   :::image type="content" source="media/Contact_Activities1.png" alt-text="Erlazio-konfigurazio adibidea.":::

1. Harremanak konfiguratu ondoren, hautatu **Hurrengoa** eta osatu zure jarduera-maparen konfigurazioa. Jarduerak sortzeari buruzko urrats zehatzak ikusteko, ikus [jarduera bat definitu](activities.md).

1. Exekutatu zure jardueren mapak.

1. Kontaktu-mailako jardueren mapa exekutatu ondoren, hautatu **Bezeroak**. Kontaktu-mailako jarduerak zure bezeroaren denbora-lerroan bistaratzen dira.

   :::image type="content" source="media/Contact_Activities2.png" alt-text="Azken emaitza kontaktu-jarduerak konfiguratu ondoren":::

### <a name="contact-level-activity-timeline-filtering"></a>Kontaktu mailako jardueren denbora-lerroaren iragazketa

Zure bezeroen jardueren kronogramak haien IDak edo izenak barne hartzen ditu, zurearen arabera *HarremanetarakoProfila* konfigurazioa, jardun zuten jardueretarako. Iragazi jarduerak kontaktuen arabera denbora-lerroan interesatzen zaizkizun kontaktu zehatzak ikusteko. Kontaktu jakin bati esleituta ez dauden jarduera guztiak ikusteko, hautatu **Kontaktu bati mapatu gabeko jarduerak**.

:::image type="content" source="media/Contact_Activities3.png" alt-text="Kontaktu mailako jardueretarako eskuragarri dauden iragazketa-aukerak.":::

[!INCLUDE [footer-include](includes/footer-banner.md)]
