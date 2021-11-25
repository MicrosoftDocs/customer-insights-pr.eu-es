---
title: Esleipen semantikoak (aurreargitalpena)
description: Kartografia semantikoen ikuspegi orokorra eta nola erabili.
ms.date: 11/01/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: CadeSanthaMSFT
ms.author: cadesantha
manager: shellyha
ms.openlocfilehash: f23c622572ff9f967eca07de7898419d1ffc18b0
ms.sourcegitcommit: 834651b933b1e50e7557d44f926a3fb757c1f83a
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/02/2021
ms.locfileid: "7731928"
---
# <a name="semantic-mappings"></a>Esleipen semantikoa

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
