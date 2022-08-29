---
title: Hautatu iturri-eremuak datuak bateratzeko
description: Bateratze-prozesuaren lehen urratsa entitateak, atributuak, gako nagusiak eta mota semantikoak hautatzea da datuak bezeroen profil bateratuarekin mapatzeko.
recommendations: false
ms.date: 08/12/2022
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
ms.openlocfilehash: bc120aa7a3713e1184ff278edf0942925faafa12
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304550"
---
# <a name="select-source-fields-for-data-unification"></a>Hautatu iturri-eremuak datuak bateratzeko

Bateratzearen lehen urratsa bateratu nahi dituzun zure datu-multzoetako entitateak eta eremuak hautatzea da. Hautatu bezeroekin lotutako xehetasunak dituzten entitateak, hala nola izena, helbidea, telefono zenbakia eta posta elektronikoa. Entitate bat edo gehiago hauta ditzakezu.

[!INCLUDE [m3-first-run-note](includes/m3-first-run-note.md)]

## <a name="select-entities-and-fields"></a>Hautatu entitateak eta eremuak

1. Joan **Datuak** > **Bateratu**.

   Banakako bezeroentzat (B-to-C), the **Bateratu** lurreratze orria bistaratzen da **Hasi** lehen urratsean, **Iturburu-eremuak**.

   :::image type="content" source="media/m3_unify_land.png" alt-text="Bezero indibidualentzako lehen exekuzio esperientziarako bateratu helmuga-orriaren pantaila-argazkia.":::

   Enpresa kontuetarako (B-to-B), the **Bateratu** lurreratze orria bistaratzen da **Kontuak bateratu** erakusten **Hasi** lehen urratsean, **Iturburu-eremuak**. The **Batu kontaktuak (aurrebista)** urratsak aukerakoak dira eta kontua bateratzearen zain daude.

   :::image type="content" source="media/b2b_unify_land.png" alt-text="Enpresa-kontuetarako lehen exekuzio esperientziarako bateratu helmuga-orriaren pantaila-argazkia.":::

1. Hautatu **Hasi erabiltzen**.

1. Gainean **Iturburu-eremuak** orrialdea, hautatu **Hautatu entitateak eta eremuak**. The **Hautatu entitateak eta eremuak** panelak bistaratzen ditu.

1. Hautatu gutxienez entitate bat.

1. Hautatutako entitate bakoitzeko, identifikatu bezeroen erregistroekin bat etortzeko erabili nahi dituzun eremuak eta profil bateratuan sartzeko. Eremu horiei deitzen zaie *Atributuak*. Beharrezko atributuak hauta ditzakezu banan-banan entitate batetik edo entitate bateko atributu guztiak sar ditzakezu entitate mailan kontrol-laukia hautatuta. Atributu eta entitate guztietan gako-hitzak bilatu ditzakezu mapatu nahi dituzun beharrezko atributuak hautatzeko.

   :::image type="content" source="media/m3_select_entities.png" alt-text="Hautatutako entitateen eta atributuen pantaila-argazkia.":::

   Adibide honetan, gehitzen ari gara **eCommerceContacts** eta **loyCustomer** entitateak. Entitate horiek aukeratuta, lineako negozioen bezeroak fidelizazio programako kide diren jakiteko.

1. Aukeratu **Aplikatu** zure hautapenak baieztatzeko. Hautatutako entitateak eta atributuak bistaratzen dira.

## <a name="select-primary-key-and-semantic-type-for-attributes"></a>Aukeratu gako nagusia eta mota semantikoa atributuetarako

   :::image type="content" source="media/m3_select_primary.png" alt-text="Hautatutako entitateen pantaila-argazkia, oraindik hautatu gabe dagoen gako nagusia." lightbox="media/m3_select_primary.png":::

Entitate bakoitzeko, egin urrats hauek.

1. Aukeratu **Lehen gakoa**. Gako nagusia entitatearen atributu bakarra da. Atributu bat baliozko gako nagusia izan dadin, ez lituzke balio bikoiztuak, falta diren balioak edo balio baliorik sartu behar. Katea, osokoa eta GUID datu motako atributuak gako nagusi gisa onartzen dira.

1. Denbora aurrezten eta zehaztasuna hobetzen duen semantika iragarpen adimendunetarako AI ereduak erabiltzeko, ziurtatu **Kartografia adimenduna** piztuta dago. Mapa adimendunak AIan oinarritutako gomendio semantikoak eskaintzen ditu **Mota** eremua.

1. Atributu bakoitzeko, aukeratu semantika bat **Mota** atributu hori hobekien deskribatzen duena, hala nola izena, hiria edo helbide elektronikoa.

   > [!NOTE]
   > B-to-C-n, eremu batek mota semantikoarekin mapatu beharko luke *Pertsona.Izen osoa* bezero-txartelean bezeroaren izena betetzeko. B-to-B-n, kontuaren izena mapatu behar da *Organization.Name*. Bestela, bezeroen txartelak izenik gabe agertuko dira.

   1. Sistemak identifikatutako atributu mota bat gainidazteko, hautatu beste aukera bat. Mota ez badago, sortu mota semantiko pertsonalizatu bat hautatuta **Mota** atributuaren eremuan eta zure mota semantiko pertsonalizatuaren izena sartu.

   1. URL bat duen atributu bat gehitzeko publikoki eskuragarri dauden profileko irudi edo logotipoetan, hautatu URLa duen entitatea eta eremua. urtean **Mota** eremuan, idatzi honako hau:
      - Pertsona batentzat: Pertsona.ProfileImage
      - Erakunde batentzat: Organization.LogoImage

1. Berrikusi mota semantiko bat automatikoki identifikatzen diren atributuak. Atributu hauek azpian daude zerrendatuta **Berrikusi mapatutako eremuak**. Mota bereko atributuak soilik konbina daitezke **Bateratu bezeroen eremuak** urratsa. Mota semantikoak ikuspegiak automatikoki iradokitzeko erabiltzen dira. Ziurtatu aukeratu dituzun motak koherenteak direla hautatutako entitate guztietan.

1. Mota semantiko batekin automatikoki mapatzen ez diren atributuetarako, hautatu mota semantikoko eremu bat, idatzi zure atributu mota pertsonalizatuaren izena edo utzi mapatu gabe. Atributu hauek azpian daude zerrendatuta **Definitu datuak mapatu gabeko eremuetan**.

1. Entitate bakoitzaren urratsak amaitu ondoren, hautatu **Gorde iturri-eremuak**.

1. Hautatu **Hurrengoa**.

> [!div class="nextstepaction"]
> [Hurrengo urratsa: Kendu bikoiztuak](remove-duplicates.md)

[!INCLUDE [footer-include](includes/footer-banner.md)]
