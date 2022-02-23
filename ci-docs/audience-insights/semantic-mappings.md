---
title: Esleipen semantikoak (aurreargitalpena)
description: Kartografia semantikoen ikuspegi orokorra eta nola erabili.
ms.date: 12/01/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: CadeSanthaMSFT
ms.author: cadesantha
manager: shellyha
ms.openlocfilehash: 08b257b97704b219bb3277042516e00deb886a49
ms.sourcegitcommit: 58651d33e0a7d438a2587c9ceeaf7ff58ae3b648
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/02/2021
ms.locfileid: "7881815"
---
# <a name="semantic-mappings-preview"></a>Esleipen semantikoak (aurreargitalpena)

Kartografia semantikoek jarduerarik gabeko datuak aurrez definitutako eskemetara mapatzen uzten dizute. Eskema hauek ikusleen estatistikak laguntzen dituzte zure datuen atributuak hobeto ulertzeko. Kartografia semantikoak eta emandako datuek ikusleei buruzko informazio eta ezaugarri berriak ahalbidetzen dituzte. Zure jardueren datuak eskemetara mapatzeko, berrikusi [jarduerak](activities.md) dokumentazioa.

**Gaur egun mapaketa semantikoak gaituta daude negozio kontuetan oinarritutako inguruneetan**. *ContactProfile* audientzia estatistiketan eskuragarri dagoen mapaketa semantiko bakarra da.

## <a name="define-a-contactprofile-semantic-entity-mapping"></a>Definitu ContactProfile entitateen mapaketa semantikoa

1. Ikusleen ikuspegietan, joan hona **Datuak** > **Kartografia semantikoak (aurrebista)**.

1. Aukeratu **Gehitu mapaketa semantikoa** esperientzia gidatua hasteko.

1. Urtean **Entitatearen datuak** urratsa, ezarri ondoko eremuetarako balioak:

   - **Entitate maparen izena semantikoa**: Eman izena entitateen mapaketa semantikorako.
   - **Iturburuko entitatea**: Hautatu harremanetarako datuak biltzen dituen entitatea.
   - **Gako nagusia**: hautatu eremua bakarrik identifikatzen duena kontaktuaren erregistroa. Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.

   :::image type="content" source="media/Semantic_Mapping_Wizard1.png" alt-text="Konfiguratu entitateen mapaketa semantikoa izena, iturburu entitatea eta gako nagusiarekin.":::

1. Jarraitzeko, hautatu **Hurrengoa**.

1. Urtean **Harremanak** urratsa, konfiguratu xehetasunak zure harremanetarako datuak dagozkien kontuko datuekin konektatzeko. Urrats honek entitateen arteko konexioa bistaratzen du.  

   Inplementatu daitezkeen bi harreman mota daude: **Harreman zuzenak** eta **Zeharkako harremanak**. Informazio gehiagorako, joan hona [harreman zuzeneko eta zeharkako bideak](relationships.md#relationship-paths).

   1. Aukeratu **Gehitu harremana** harremana konfiguratu.
   1. Aukeratu zure iturburuko entitatearen atributua zure harremanetarako entitatea beste entitate batekin konektatzen duena.
   1. Aukeratu entitatea zure harremanetarako entitatearekin konektatzeko. Entitate bat aukeratu dezakezu **Kontuko entitateak** edo **Bitarteko entitatea** atala. Bitarteko entitate bat hautatzen baduzu, bigarren harremana definitu beharko duzu zure xede-kontuko entitatearekin konektatzeko.

      :::image type="content" source="media/Semantic_Mapping_Wizard2.png" alt-text="Aukeratu Kontuko entitatea edo Bitarteko entitatea.":::

   1. Eman **Harremanaren izena**. Zure entitateen arteko harremana lehendik badago, harremanaren izena irakurtzeko soilik da. Harremanik ez badago, harreman berria sortuko da zuk emandako izenarekin.
   1. Aukeratu **Aplikatu** harreman konfigurazioa amaitzeko.

   > [!NOTE]
   > Harreman gehiago konfigura ditzakezu harremanetarako entitatearen eta tarteko entitateekin beste kontu-entitate batzuen artean.
   >  :::image type="content" source="media/Semantic_Mapping_Wizard4.png" alt-text="Hainbat harreman bistaratzeak harremanetarako entitateak kontuko entitateekin lotzen ditu.":::

1. Aukeratu **Hurrengoa** harreman konfigurazioa amaitutakoan.

1. Urtean **Ezarri mota semantikoa** urratsa, aukeratu bat **Mota semantikoa**. Gaur egun, bada bat **Mota semantikoa** deitu *ContactProfile*.

1. Esleitu zure datuak *ContactProfile* **Mota semantikoa** erakutsitako eremuetarako.
   - Eskatutako eremua: kontaktuaren IDa
   - Aukerako eremuak: izen, abizen, Jaiotze data, generoa, posta elektroniko nagusia eta telefono nagusia

   :::image type="content" source="media/Semantic_Mapping_Wizard5.png" alt-text="Mapatu zure harremanetarako datuen atributuak beharrezko eta aukerako eremuekin.":::

1. Jarraitzeko, hautatu **Hurrengoa**.

1. Urtean **Berrikuspena** urratsa, begiratu mapaketa semantikoaren konfigurazioari. Aukeratu **Editatu** dagokion atalak aldaketak egin ditzan.

1. Aukeratu **Gorde** berria gordetzeko **Kartografia semantikoa**.

1. Gorde ondoren, hauta dezakezu **Korrika egin** prozesatu mapaketa semantikoa edo hautatu dezakezu **Itxi** zure mapaketa semantikoa prozesatu gabe gordetzeko.

1. Kartografia semantiko bat aurrerago exekutatzeko, hautatu mapaketa semantikoa eta hautatu **Freskatu**.

[!INCLUDE [progress-details-include](../includes/progress-details-pane.md)]

## <a name="manage-existing-semantic-mappings"></a>Kudeatu lehendik dauden mapaketa semantikoak

Aktibatuta **Datuak** > **Kartografia semantikoak (aurrebista)**, gordetako mapaketa semantiko guztiak ikusi eta kudeatu ditzakezu. Kartografia semantiko bakoitza ilara bereizi baten bidez irudikatzen da. Iturburuko entitateari, mota semantikoari, mapaketa motari eta haren egoerari buruzko xehetasunak aurkituko dituzu.

:::image type="content" source="media/semantic-mapping-options.png" alt-text="Kartografia semantikoak kudeatzeko aukerak.":::

- **Editatu**: ireki konfigurazioa esleipen semantikoaren konfigurazioa berrikuste pausoan. Uneko konfigurazioa alda dezakezu. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.

- **Freskatu**: Aukeratutako mapaketa semantikoa freskatzen du bere konfigurazioaren parte diren entitateetako datu eguneratuenekin. Edozein mapaketa semantiko freskatzeak mota bereko mapaketa semantiko guztiak freskatuko ditu.

- **Aldatu izena**: Elkarrizketa-koadro bat irekitzen du eta bertan beste izen bat sar dezakezu hautatutako mapaketa semantikorako. Aldaketak aplikatzeko, hautatu **Gorde**.

- **Ezabatu**: Elkarrizketa-koadro bat irekitzen du hautatutako mapaketa semantikoa ezabatzen dela berresteko. Kartografia semantiko bat baino gehiago aldi berean ezaba ditzakezu mapaketa semantikoak eta ezabatzeko ikonoa hautatuta. Hautatu **Ezabatu** ezabatzea baieztatzeko.

## <a name="use-a-contactprofile-semantic-entity-mapping-to-create-contact-level-activities"></a>Erabili ContactProfile entitate semantikoen mapaketa kontaktu mailako jarduerak sortzeko

Bat sortu ondoren *Harremanetarako Profila* entitate semantikoen mapak, kontaktuen jarduerak har ditzakezu. Kontu baten jardueraren kronograman ikus dezakezu zein kontaktu zen jarduera bakoitzaren arduraduna. Urrats gehienek jarduera-mapearen konfigurazio tipikoari jarraitzen diote.

   > [!NOTE]
   > Kontaktu mailako jarduerak funtzionatzeko, biak izan behar dituzu **Kontuaren ID** eta **Kontaktu ID** zure jarduera-datuen barruan erregistro bakoitzerako atributuak.

1. [Definitu a *Harremanetarako Profila* entitate semantikoen mapaketa.](#define-a-contactprofile-semantic-entity-mapping) Eta exekutatu mapa semantikoa.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.

1. Hautatu **Gehitu jarduera** jarduera berri bat sortzeko.

1. Jarriari izena eman, hautatu iturburuko jarduera-entitatea eta hautatu jarduera-entitatearen gako nagusia.

1. urtean **Harremanak** urratsa, sortu zure jarduera-iturburuko datuen arteko zeharkako harremana kontuekin, zure harremanetarako datuak bitartekari gisa erabiliz. Informazio gehiagorako, ikus [harreman zuzeneko eta zeharkako bideak](relationships.md#relationship-paths).
   - Deitutako jarduera baterako erlazio adibidea *Erosketak*:
      - **Erosketak Iturburu Jardueren Datuak** > **Harremanetarako datuak** atributuaren gainean **Kontaktu ID**
      - **Harremanetarako datuak** > **Kontuaren datuak** atributuaren gainean **Kontuaren ID**

   :::image type="content" source="media/Contact_Activities1.png" alt-text="Erlazio-konfigurazio adibidea.":::

1. Harremanak konfiguratu ondoren, hautatu **Hurrengoa** eta osatu zure jarduera-maparen konfigurazioa. Jarduerak sortzeari buruzko urrats zehatzak ikusteko, ikus [jarduera bat definitu](activities.md).

1. Exekutatu zure jardueren mapak.

1. Zure kontaktu-mailako jarduerak zure bezeroen denbora-lerroan ikusgai egongo dira orain.

   :::image type="content" source="media/Contact_Activities2.png" alt-text="Azken emaitza kontaktu-jarduerak konfiguratu ondoren":::

### <a name="contact-level-activity-timeline-filtering"></a>Kontaktu-mailako jardueren denbora-lerroaren iragazketa

Kontaktu-mailako jardueren mapa konfiguratu eta exekutatu ondoren, zure bezeroen jardueren kronograma eguneratuko da. Beren ID edo izenak biltzen ditu, zurearen arabera *Harremanetarako Profila* konfigurazioa, jardun zuten jardueretarako. Jarduerak kontaktuen arabera iragazi ditzakezu denbora-lerroan interesatzen zaizkizun kontaktu zehatzak ikusteko. Gainera, kontaktu zehatz bati esleituta ez dauden jarduera guztiak ikus ditzakezu hautatuta **Kontaktu bati mapatu gabeko jarduerak**.

   :::image type="content" source="media/Contact_Activities3.png" alt-text="Kontaktu mailako jardueretarako eskuragarri dauden iragazketa-aukerak.":::

[!INCLUDE[footer-include](../includes/footer-banner.md)]
