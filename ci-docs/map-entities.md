---
title: Hautatu iturri-eremuak datuak bateratzeko
description: Bateratze-prozesuaren lehen urratsa entitateak, atributuak, gako nagusiak eta mota semantikoak hautatzea da datuak bezeroen profil bateratuarekin mapatzeko.
recommendations: false
ms.date: 04/22/2022
ms.subservice: audience-insights
ms.topic: tutorial
author: v-wendysmith
ms.author: mukeshpo
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-map
- ci-match
- customerInsights
ms.openlocfilehash: a75218c996b277e00924f2b7b38ea686a1f4dc38
ms.sourcegitcommit: 3c5b0b40b2b45e420015bbdd228ce0e610245e6f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/12/2022
ms.locfileid: "9139767"
---
# <a name="select-source-fields-for-data-unification"></a>Hautatu iturri-eremuak datuak bateratzeko

Bateratzearen lehen urratsa bateratu nahi dituzun zure datu multzoetako entitateak eta eremuak hautatzea da. Hautatu bezeroekin erlazionatutako xehetasunak dituzten entitateak, hala nola izena, helbidea, telefono zenbakia eta posta elektronikoa. Entitate bat edo gehiago hauta ditzakezu.

## <a name="select-entities-and-fields"></a>Hautatu entitateak eta eremuak

1. Joan **Datuak** > **Bateratu**.

   :::image type="content" source="media/m3_unify_land.png" alt-text="Lehen exekuzio esperientziarako bateratze-orriaren pantaila-argazkia Hasi nabarmenduta.":::

1. Hautatu **Hasi erabiltzen**.

1. Gainean **Iturburu-eremuak** orrialdea, hautatu **Hautatu entitateak eta eremuak**. The **Hautatu entitateak eta eremuak** panelak bistaratzen ditu.

1. Hautatu gutxienez entitate bat.

1. Hautatutako entitate bakoitzeko, identifikatu bezeroen erregistroekin bat etortzeko erabili nahi dituzun eremuak eta profil bateratuan sartzeko. Eremu horiei deitzen zaie *Atributuak*. Beharrezko atributuak hauta ditzakezu banan-banan entitate batetik edo entitate bateko atributu guztiak sar ditzakezu entitate mailan kontrol-laukia hautatuta. Atributu eta entitate guztietan gako-hitzak bilatu ditzakezu mapatu nahi dituzun beharrezko atributuak hautatzeko.

   :::image type="content" source="media/m3_select_entities.png" alt-text="Hautatutako entitateen eta atributuen pantaila-argazkia.":::

   Adibide honetan, gehitzen ari gara **Kontaktuak** eta **Bezeroen Leialtasuna** entitateak. Entitate horiek aukeratuta, lineako negozioen bezeroak fidelizazio programako kide diren jakiteko.

1. Aukeratu **Aplikatu** zure hautapenak baieztatzeko. Hautatutako entitateak eta atributuak bistaratzen dira.

## <a name="select-primary-key-and-semantic-type-for-attributes"></a>Aukeratu gako nagusia eta mota semantikoa atributuetarako

   :::image type="content" source="media/m3_select_primary.png" alt-text="Hautatutako entitateen pantaila-argazkia, gako nagusia hautatu gabe." lightbox="media/m3_select_primary.png":::

Entitate bakoitzeko, egin urrats hauek.

1. Aukeratu **Lehen gakoa**. Gako nagusia entitatearen atributu bakarra da. Atributu bat baliozko gako nagusia izan dadin, ez lituzke balio bikoiztuak, falta diren balioak edo balio baliorik sartu behar. Katea, osokoa eta GUID datu motako atributuak gako nagusi gisa onartzen dira.

1. Semantika iragarpen adimentsurako AI ereduak erabiltzeko, aurreztu denbora eta hobetu zehaztasuna, ziurtatu **Kartografia adimenduna** piztuta dago. Kartografia adimendunak AI-n oinarritutako semantika gomendioa nabarmentzen du **Mota** zelaia. Iradokitako hautaketa gainidatzi dezakezu eskuragarri dagoen aukeren zerrendatik edozein mota semantiko aukeratuz.

1. Atributu bakoitzeko, aukeratu semantika bat **Mota** atributu hori hobekien deskribatzen duena, hala nola izena, hiria edo helbide elektronikoa.

   > [!NOTE]
   > Eremu batek mota semantikoarekin mapatu behar du *Pertsona.Izen osoa* bezero-txartelean bezeroaren izena betetzeko. Bestela, bezeroen txartelak izenik gabe agertuko dira.

   1. Sistemak identifikatutako atributu mota bat aldatzeko, hautatu beste mota bat. Mota ez badago, sortu mota semantiko pertsonalizatu bat hautatuta **Mota** atributuaren eremua eta zure mota semantiko pertsonalizatuaren izena idatziz.

   1. URL bat duen atributu bat gehitzeko publikoki eskuragarri dauden profileko irudi edo logotipoetan, hautatu URLa duen entitatea eta eremua. urtean **Mota** eremuan, idatzi honako hau:
      - Pertsona batentzat: Pertsona.ProfileImage
      - Erakunde batentzat: Organization.LogoImage

   1. Kontuaren izenaren atributu baterako, idatzi "Organization.Name" atalean **Mota** eremua.

1. Berrikusi mota semantiko bat automatikoki identifikatzen diren atributuak. Atributu hauek azpian daude zerrendatuta **Berrikusi mapatutako eremuak**. Mota bereko atributuak soilik konbina daitezke **Bezeroen eremu bateratuak** urratsa. Mota semantikoak ikuspegiak automatikoki iradokitzeko erabiltzen dira. Ziurtatu aukeratu dituzun motak koherenteak direla hautatutako entitate guztietan.

1. Mota semantiko batekin automatikoki mapatzen ez diren atributuetarako, hautatu mota semantikoko eremu bat, idatzi zure atributu mota pertsonalizatuaren izena edo utzi mapatu gabe. Atributu hauek azpian daude zerrendatuta **Definitu datuak mapatu gabeko eremuetan**.

1. Entitate bakoitzaren urratsak amaitu ondoren, hautatu **Gorde iturri-eremuak**.

1. Hautatu **Hurrengoa**.

> [!div class="nextstepaction"]
> [Hurrengo urratsa: Kendu bikoiztuak](remove-duplicates.md)

[!INCLUDE [footer-include](includes/footer-banner.md)]
