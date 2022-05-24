---
title: Bateratu bezeroaren edo kontuaren eremuak
description: Konbinatu entitateak bezeroen profil bateratuak sortzeko.
recommendations: false
ms.date: 05/04/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: mukeshpo
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-merge
- ci-match
- ci-relationships
- customerInsights
ms.openlocfilehash: 78e2528d4a3058f879d83952f72ed88a1da065b6
ms.sourcegitcommit: 6a5f4312a2bb808c40830863f26620daf65b921d
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8740842"
---
# <a name="unify-customer-fields"></a>Bateratu bezeroen eremuak

[!INCLUDE [m3-prod-trial-note](includes/m3-prod-trial-note.md)]

Bateratze-prozesuaren urrats honetan, aukeratu eta baztertu zure profil bateratuko entitatearen barruan batzeko atributuak. Adibidez, hiru entitatek posta elektronikoko datuak bazituzten, baliteke hiru posta elektronikoko eremu bereiziak gordetzea edo profil bateratu baterako posta elektronikoko eremu bakarrean batu nahi izatea. Atributu batzuk automatikoki konbinatzen ditu sistemak. Bezeroen ID egonkorrak eta bakarrak sor ditzakezu eta erlazionatutako profilak multzo batean taldeka ditzakezu.

:::image type="content" source="media/m3_unify.png" alt-text="Batu orria datuak bateratzeko prozesuan bezeroaren profil bateratua definitzen duten eremu bateratuekin taula erakusten duena.":::

## <a name="review-and-update-the-customer-fields"></a>Berrikusi eta eguneratu bezeroaren eremuak

1. Berrikusi hemen bateratuko diren eremuen zerrenda **Bezeroaren eremuak** taulako fitxa. Egin aldaketak hala badagokio.

   1. Edozein eremu konbinatuetarako, hau egin dezakezu:
      - [Editatu](#edit-a-merged-field)
      - [Aldatu izena](#rename-fields)
      - [Bereizi](#separate-merged-fields)
      - [Baztertu](#exclude-fields)
      - [Mugitu gora edo behera](#change-the-order-of-fields)

   1. Edozein eremutarako, hau egin dezakezu:
      - [Konbinatu eremuak](#combine-fields-manually)
      - [Konbinatu eremu talde bat](#combine-a-group-of-fields)
      - [Aldatu izena](#rename-fields)
      - [Baztertu](#exclude-fields)
      - [Mugitu gora edo behera](#change-the-order-of-fields)

1. Aukeran, [sortu bezeroaren IDaren konfigurazioa](#configure-customer-id-generation).

1. Aukeran, [taldekatu profilak etxeetan edo klusterretan](#group-profiles-into-households-or-clusters).

> [!div class="nextstepaction"]
> [Hurrengo urratsa: berrikusi bateratzea](review-unification.md)

### <a name="edit-a-merged-field"></a>Editatu konbinatutako eremua

1. Hautatu bateratutako eremu bat eta aukeratu **Editatu**. Konbinatu eremuak panela bistaratzen da.

1. Zehaztu nola konbinatu eremuak hiru aukera hauetatik:
    - **Garrantzia**: balio nagusia identifikatzen du parte hartzen duten zehaztutako eremuen garrantziaren sailkapenean oinarrituta. Hori da konbinatzeko aukera lehenetsia. Garrantziaren araberako sailkapena ezartzeko, hautatu **Eraman gora/behera**.

      :::image type="content" source="media/importance-merge-option.png" alt-text="Garrantziaren aukera eremuak konbinatzeko elkarrizketan.":::

    - **Azkena**: balio nagusia identifikatzen du, berritasunaren arabera. Berritasuna definitzeko, data edo zenbakizko eremua behar da eremuak konbinatzeko esparruan parte hartzen duen entitate bakoitzerako.

      :::image type="content" source="media/recency-merge-option.png" alt-text="Berritasunaren aukera eremuak konbinatzeko elkarrizketan.":::

    - **Zaharrena**: balio nagusia identifikatzen du, zahartasunaren arabera. Berritasuna definitzeko, data edo zenbakizko eremua behar da eremuak konbinatzeko esparruan parte hartzen duen entitate bakoitzerako.

1. Eremu gehiago gehitu ditzakezu bateratze prozesuan parte hartzeko.

1. Konbinatutako eremuaren izena alda dezakezu.

1. Aldaketak aplikatzeko, hautatu **Eginda**.

### <a name="rename-fields"></a>Aldatu izena eremuei

Aldatu bateratutako edo bereizitako eremuen bistaratzeko izena. Ezin duzu aldatu irteerako entitatearen izena.

1. Hautatu eremua eta aukeratu **Aldatu izena**.

1. Sartu bistaratzeko izen berria.

1. Hautatu **Eginda**.

### <a name="separate-merged-fields"></a>Zatitu konbinatutako eremuak

Batutako eremuak bereizteko, bilatu atributua taulan. Bereizitako eremuak bezeroaren profil bateratuan banakako datu gisa agertzen dira.

1. Hautatu bateratutako eremua eta aukeratu **Eremu bereiziak**.

1. Berretsi zatiketa.

### <a name="exclude-fields"></a>Baztertu eremuak

Baztertu bateratutako edo bereizitako eremu bat bezeroaren profil bateratutik. Eremua beste prozesu batzuetan erabiltzen bada, adibidez segmentu batean, ezabatu prozesu hauetatik bezeroaren profiletik baztertu aurretik.

1. Hautatu eremu bat eta aukeratu **Baztertu**.

1. Berretsi bazterketa.

Baztertutako eremu guztien zerrenda ikusteko, hautatu **Baztertutako eremuak**. Beharrezkoa izanez gero, baztertutako eremua irakur dezakezu.

### <a name="change-the-order-of-fields"></a>Aldatu eremuen ordena

Entitate batzuek besteek baino xehetasun gehiago dituzte. Entitate batek eremu bati buruzko azken datuak biltzen baditu, baliteke bat egitean lehentasuna eman diezaiokezu beste entitateei.

1. Hautatu eremua.
  
1. Aukeratu **Mugitu gora/behera** ordena ezartzeko edo arrastatu eta jaregin nahi duzun posizioan.

### <a name="combine-fields-manually"></a>Konbinatu eremuak eskuz

Konbinatu bereizitako eremuak atributu bateratu bat sortzeko.

1. Hautatu **Konbinatu** > **Eremuak**. Konbinatu eremuak panela bistaratzen da.

1. Zehaztu konbinazio nagusiaren gidalerroak **Konbinatu eremuak honen arabera** goitibeherako menuan.

1. Hautatu **Gehitu eremua** eremu gehiago konbinatzeko.

1. Eman **Izena** bat eta **Irteerako eremuaren izena**.

1. Aldaketak aplikatzeko, hautatu **Eginda**.

### <a name="combine-a-group-of-fields"></a>Konbinatu eremu talde bat

Tratatu eremu multzo bat unitate bakar gisa. Adibidez, gure erregistroek Helbidea1, Helbidea2, Hiria, Estatua eta Zip eremuak badituzu, ez dugu nahi beste erregistro baten Helbidea2 batean batu, gure datuak osatuagoak izango liratekeela pentsatuz.

1. Hautatu **Konbinatu** > **Eremu multzoa**.

1. Zehaztu bateratze irabazlearen politika **Sailkatu taldeak arabera** goitibeherako.

1. Hautatu **Gehitu** eta aukeratu eremu edo talde gehiago gehitu nahi dituzun eremuei.

1. Eman a **Izena** eta bat **Irteera izena** eremu konbinatu bakoitzeko.

1. Eman a **Izena** eremuen talderako.

1. Aldaketak aplikatzeko, hautatu **Eginda**.

## <a name="configure-customer-id-generation"></a>Konfiguratu bezeroaren IDa sortzea

Definitu nola sortu bezeroaren ID balioak, bezeroen profilaren identifikatzaile esklusiboak. Datuak bateratzeko prozesuko eremuak bateratzeko urratsak bezeroaren profilaren identifikatzaile esklusiboa sortzen du. Identifikatzailea da *BezeroarenId* urtean *Bezeroa* datuak bateratzeko prozesuaren ondoriozko entitatea.

The *BezeroarenId*  nuluak ez diren irabazlearen gako nagusien lehen balioaren hash batean oinarritzen da. Gako hauek datuak bateratzeko erabiltzen diren entitateetatik datoz eta bat-etortze-ordenaren eragina dute.Beraz, sortutako bezero IDa alda daiteke lehen mailako gako-balioa bat-etortze-ordenaren entitate nagusian aldatzen denean. Baliteke gako nagusiaren balioa ez izatea beti bezero bera ordezkatzea.

Bezeroaren ID egonkor bat sortzeak portaera hori ekiditeko aukera ematen dizu.

1. Hautatu **Gakoak** fitxa.

1. Pasa ezazu gainean **BezeroarenId** errenkatu eta hautatu **Konfiguratu**.
   :::image type="content" source="media/customize-stable-id.png" alt-text="IDaren sorrera pertsonalizatzeko kontrola.":::

1. Hautatu gehienez bost eremu, bezeroaren ID esklusiboaz osatuta egongo direnak eta egonkorragoak izango direnak. Konfigurazioarekin bat ez datozen erregistroek sistemak konfiguratutako IDa erabiltzen dute haren ordez.  

1. Hautatu **Eginda**.

## <a name="group-profiles-into-households-or-clusters"></a>Taldeko profilak etxeetan edo klusterretan

Erlazionatutako profilak kluster batean taldekatzeko arauak defini ditzakezu. Gaur egun bi kluster mota daude eskuragarri - etxekoak eta pertsonalizatutakoak. Sistemak automatikoki aurrez zehaztutako arauak dituen etxea aukeratzen du *Bezeroa* entitateak eremu semantikoak ditu *Person.LastName* eta *Location.Address*. Klusterra ere sor dezakezu zure arau eta baldintzekin, antzekoa [partida arauak](match-entities.md#define-rules-for-match-pairs).

1. Hautatu **Aurreratua** > **Sortu klusterra**.

   :::image type="content" source="media/create-cluster.png" alt-text="Kontrolatu kluster berria sortzeko.":::

1. Aukeratu **Etxekoa** edo bat **Pertsonalizatua** klusterra. Eremu semantikoak bada *Person.LastName* eta *Location.Address* existitzen dira *Bezeroa* entitatea, etxea automatikoki hautatzen da.

1. Eman klusterraren izena eta hautatu **Eginda**.

1. Aukeratu **Klusterrak** fitxa sortu duzun klusterra aurkitzeko.

1. Zehaztu arauak eta baldintzak zure klusterra definitzeko.

1. Hautatu **Eginda**. Klusterra bateratze-prozesua amaitzean sortzen da. Kluster-identifikatzaileak eremu berri gisa gehitzen dira *Bezeroa* entitate.

> [!div class="nextstepaction"]
> [Hurrengo urratsa: berrikusi bateratzea](review-unification.md)

[!INCLUDE [footer-include](includes/footer-banner.md)]
