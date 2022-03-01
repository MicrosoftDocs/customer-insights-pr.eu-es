---
title: Entitateen eta entitateen bide-izenen arteko erlazioak
description: Sortu eta kudeatu datu-iturburu anitzetako entitateen arteko harremanak.
ms.date: 06/01/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: MichelleDevaney
ms.author: midevane
manager: shellyha
ms.openlocfilehash: d5b9566ec88096fec31d8e164a51598159ec26d4
ms.sourcegitcommit: ece48f80a7b470fb33cd36e3096b4f1e9190433a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/03/2021
ms.locfileid: "6171149"
---
# <a name="relationships-between-entities"></a>Harremanak entitateen artean

Harremanek entitateak konektatzen dituzte eta zure datuen grafikoa definitzen dute entitateek identifikatzaile komuna partekatzen dutenean, atzerriko gakoa. Atzerriko gako honi entitate batetik bestera erreferentzia egin dakioke. Konektatutako entitateek datu-iturri anitzetan oinarritutako segmentuak eta neurriak definitzeko aukera ematen dute.

Hiru harreman mota daude: 
- Editatu ezin diren sistema harremanak, sistemak datuak bateratzeko prozesuaren zati gisa sortuak
- Editatu ezin diren herentziazko harremanak, datu iturriak sartzetik automatikoki sortzen direnak 
- Erabiltzaileek sortutako eta konfiguratutako harreman pertsonalizatu editagarriak

## <a name="non-editable-system-relationships"></a>Editatu ezin diren sistemen harremanak

Datuak bateratzerakoan, sistemako harremanak automatikoki sortzen dira bat-etortze adimentsuan oinarrituta. Harreman hauek Bezeroaren Profilaren erregistroak dagozkien beste erregistroekin erlazionatzen lagunduko dute. Hurrengo diagramak sisteman oinarritutako hiru erlazio sortu direla erakusten du. Bezeroaren entitatea beste entitate batzuekin bateratzen da *Bezeroaren* entitate bateratua ekoizteko.

:::image type="content" source="media/relationships-entities-merge.png" alt-text="1-n hiru harreman dituen bezero entitatearen harreman bideekin diagrama.":::

- ***CustomerToContact* harremana** *Bezeroaren* entitatearen eta *kontaktuaren* entitatearen artean sortu zen. *Bezero* entitateak **Contact_contactID** gako-eremua lortzen du *kontaktuaren* entitatearen **contactID** gako eremuarekin erlazionatzeko.
- ***CustomerToAccount* harremana** *bezeroaren* entitatearen eta *kontuaren* entitatearen artean sortu zen. *Bezeroaren* entitateak **Account_accountID** gako eremua lortzen du *kontua* entitatearen **accountID** gako eremuarekin erlazionatzeko.
- ***CustomerToWebAccount* harremana** *bezeroaren* entitatearen eta *WebAccount* entitatearen artean sortu zen. *Bezeroaren* entitateak **WebAccount_webaccountID** gako eremua lortzen du *WebAccount* entitatearen **webaccountID** gako eremuarekin erlazionatzeko.

## <a name="non-editable-inherited-relationships"></a>Editatu ezin diren heredatutako harremanak

Datuak irensteko prozesuan, sistemak datu iturriak egiaztatzen ditu lehendik dauden harremanetarako. Harremanik ez badago, sistemak automatikoki sortzen ditu. Harreman horiek beheranzko prozesuetan ere erabiltzen dira.

## <a name="create-a-custom-relationship"></a>Sortu erlazio pertsonalizatu bat

Harremanak atzerriko gakoa duen *iturburu-entitatea* eta iturburuko entitatearen atzerriko gakoak adierazten duen *xede-entitatea* ditu. 

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Harremanak**.

2. Hautatu **Harreman berria**.

3. **Erlazio berria** panelean, eman ondorengo informazioa:

   :::image type="content" source="media/relationship-add.png" alt-text="Harreman alboko panel berria sarrera eremu hutsekin.":::

   - **Harremanaren izena**: Harremanaren xedea islatzen duen izena. Adibidez: CustomerToSupportCase.
   - **Deskribapena**: Erlazio-funtzioaren azalpena.
   - **Iturburuko entitatea**: Harremanean iturburu gisa erabiltzen den entitatea. Adibidez: SupportCase.
   - **Helburuko entitatea**: Harremanean helburu gisa erabiltzen den entitatea. Adibidez: Customer.
   - **Iturriaren kardinalitatea** : Zehaztu iturburuko entitatearen kardinalitatea. Kardinalitateak multzo bateko elementu posibleen kopurua deskribatzen du. Beti xede-kardinalitatearekin lotzen da. Aukera dezakezu **Bat** edo **Asko**. Banan-banan eta banan-banako harremanak bakarrik onartzen dira.  
     - Hainbatetik baterako: iturburu erregistro anitz xede erregistro batekin erlazionatu daitezke. Adibidez: bezero bakar baten laguntza kasu ugari.
     - Batetik baterako: iturburuko erregistro bakarra xede erregistro batekin erlazionatzen da. Adibidez: fidelizazio ID bakarra bezero bakarrarentzat.

     > [!NOTE]
     > Hainbatetik hainbaterako harremanak hainbatetik baterako bi harreman eta lotura duen entitate bat erabiliz sor daitezke, sorburuko entitatea eta xede-entitatea lotzen dituena.

   - **Helmugako kardinalitatea**: helmugako entitatearen erregistroen kardinalitatea aukeratu. 
   - **Iturburu gako eremua** : Iturburuko entitateko atzerriko gako eremua. Adibidez: SupportCase-k CaseID erabil dezake atzerriko gako eremu gisa.
   - **Helburuko gako eremua**: xede entitatearen gako eremua. Adibidez bezeroak erabil dezake **Bezeroaren IDa** gako eremua.

4. Erlazio pertsonalizatua sortzeko, hautatu **Gorde**.

## <a name="view-relationships"></a>Ikusi erlazioak

Harremanak orrian sortu diren harreman guztiak zerrendatzen dira. Errenkada bakoitzak erlazio bat adierazten du, iturburu-entitateari, xede-entitateari eta kardinalitateari buruzko xehetasunak ere biltzen dituena. 

:::image type="content" source="media/relationships-list.png" alt-text="Harremanen eta aukeren zerrenda Harremanak orriko ekintza barran.":::

Orrialde honek lehendik dauden eta harreman berrietarako aukera multzo bat eskaintzen du: 
- **Erlazio berria:** [Sortu erlazio pertsonalizatu bat](#create-a-custom-relationship).
- **Bistaratzailea**: [Arakatu harremanen bistaratzailea](#explore-the-relationship-visualizer) dauden erlazioen eta haien kardinalitatearen sare-diagrama ikusteko.
- **Iragazi honen arabera**: Aukeratu zerrendan erakutsi beharreko harreman mota.
- **Bilatu harremanak**: Erabili testuan oinarritutako bilaketa erlazioen propietateetan.

### <a name="explore-the-relationship-visualizer"></a>Arakatu harremanen bistaratzailea

Harremanen bistaratzaileak konektatuta dauden entitateeen eta haien kardinalitatearen sare-diagrama erakusten du.

Ikuspegia pertsonalizatzeko, koadroen kokapena alda dezakezu mihisean arrastatuz.

:::image type="content" source="media/relationship-visualizer.png" alt-text="Erlazio bistaratzailearen sare diagramaren pantaila-argazkia erlazionatutako entitateen arteko konexioekin.":::

Aukera erabilgarriak: 
- **Esportatu irudi gisa**: Uneko ikuspegia irudi fitxategi gisa gorde.
- **Aldatu diseinu horizontal / bertikalera**: Entitateen eta harremanen lerrokatzea aldatu.
- **Editatu**: Harreman pertsonalizatuen propietateak eguneratu editatzeko panelean eta gorde aldaketak.

## <a name="manage-existing-relationships"></a>Kudeatu lehendik dauden erlazioak 

Harremanak orrian, harreman bakoitza errenkada batez irudikatzen da. 

Aukeratu harremana eta aukeratu aukera hauetako bat: 
 
- **Editatu**: Harreman pertsonalizatuen propietateak eguneratu editatzeko panelean eta gorde aldaketak.
- **Ezabatu**: Harreman pertsonalizatuak ezabatu.
- **Ikusi**: Sistemak sortutako eta heredatutako harremanak ikusi. 

## <a name="next-step"></a>Hurrengo urratsa

Sistema eta pertsonalizatutako harremanak sekretuak isilik ez dituzten datu iturri anitzetan oinarritutako [segmentuak sortzeko](segments.md) erabiltzen dira.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
