---
title: Esleitu entitateak datuak bateratzeko
description: Esleitu datuak bezeroen profil bateratuak sortzeko.
ms.date: 09/25/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
ms.openlocfilehash: e98c7717f7707d43a9fd1fc6f6b0e9c49e4e7ee0
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404989"
---
# <a name="map-entities-and-attributes"></a>Mapen entitateak eta atributuak

**Esleipena** hartzaileen xehetasunen datuen bateratze prozesuko lehen etapa da. Kartografiak hiru fase ditu:

- *Erakundeen hautaketa*: Identifikatu datu multzo batera daramaten entitate konbinagarriek zure bezeroei buruzko informazio osoagoa.
- *Ezaugarri hautaketa*: Entitate bakoitzeko, identifikatu konbinatu eta bateratu nahi dituzun zutabeak *bat-etortze* eta *konbinatu* faseak. Zutabe horiei *Atributuak* deitzen zaie.
- *Gako nagusia eta mota semantikoa hautatzea*: Entitate bakoitzerako, identifikatu entitate horren gako nagusi gisa definitu nahi duzun atributu bat eta atributu bakoitzerako, identifikatu atributu hori hobekien deskribatzen duen mota semantikoa.

Informazio gehiago lortzeko datuen bateratzeari buruzko informazio gehiago lortzeko, ikus [bateratzeko](data-unification.md).

## <a name="select-the-first-entities"></a>Hautatu lehenengo entitateak

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Bat egin** > **Esleitu**.

2. Hasi mapa fasea aukeratuz **Erakundeak hautatu**.

3. Aukeratu erabili nahi dituzun entitateak eta atributuak *partida* eta *batu* faseak. Beharrezko atributuak banaka hauta ditzakezu entitate batetik edo entitate bateko atributu guztiak sar ditzakezu **Sartu eremu guztiak** kontrol-laukia entitate mailan. Gutxienez bi entitate hautatzea gomendatzen dugu datuak bateratzeko prozesuan etekina ateratzeko.

   > [!div class="mx-imgBorder"]
   > ![Gehitu entitateak adibidea](media/data-manager-configure-map-add-entities-example.png "Gehitu entitateak adibidea")

   Adibide honetan, **eCommerceContacts** eta **loyBezeroak** entitateak. Entitate horiek aukeratuta, lineako negozioen bezeroak fidelizazio programako kide diren jakiteko.
   
   Atributu eta entitate guztietan gako-hitzak bilatu ditzakezu mapatu nahi dituzun beharrezko atributuak hautatzeko.
   
     > [!div class="mx-imgBorder"]
   > ![Bilatu eremuen adibidea](media/data-manager-configure-map-search-fields-example.png "Bilatu eremuen adibidea")

4. Aukeratu **Aplikatu** zure hautapenak baieztatzeko.

## <a name="select-primary-key-and-semantic-type-for-attributes"></a>Aukeratu gako nagusia eta mota semantikoa atributuetarako

Zure entitateak hautatu ondoren, **Mapa** orrialdeak zure berrikuspenerako hautatutako entitateak zerrendatzen ditu. Definitu entitate baten gako nagusia eta identifikatu entitatean atributu baten mota semantikoa.

- **Lehen mailako gakoa**: Aukeratu ezazu atributu bat entitate bakoitzerako gako nagusi gisa. Atributu bat baliozko gako nagusia izan dadin, ez lituzke balio bikoiztuak, falta diren balioak edo balio baliorik sartu behar. Katea, osoko zenbakia eta GUID datu motaren atributuak gako nagusi gisa onartzen dira eta aukeratu ahal izateko eremu batean bistaratuko dira.

- **Atributu semantiko mota**: Zure atributuen kategoriak, hala nola helbide elektronikoa edo izena. AI ereduak semantika iragarpen adimendunetarako erabiltzeko, denbora aurreztu eta zehaztasuna hobetzeko, ezarri **Kartografia adimenduna** hurrengora **Aktibatu**. Kartografia adimendunak AI-n oinarritutako semantika gomendioa nabarmentzen du **Mota** zelaia. Ezartzen baduzu **Itzali**, gure ohiko mapen gomendioak ikusiko dituzu. Edozein mota semantiko hauta dezakezu eskuragarri dauden aukeren zerrendan eta iradokitako hautaketa gainidatzi.

> [!div class="mx-imgBorder"]
> ![Atributu mota eta iragarpen semantikoa](media/data-manager-configure-map-add-attributes-semantic-prediction.png "Atributu mota eta iragarpen semantikoa")

Semantika pertsonalizatu mota bat gehitzea ere posible da. Hautatu atributu horren mota-eremua eta idatzi zure semantika-mota pertsonalizatutako izena. Modu honetan, sistemak auto-identifikatutako auto atributu motak ere alda ditzakezu.

Mota semantikoa automatikoki identifikatzen den atributu guztiak taldean biltzen dira **Berrikusi mapatutako eremuak** atala. Berrikusi atributu hauek eta horien mota semantikoak, zure erakundeak datuen bateratzearen bateratze-urratsean konbinatzeko erabiliko direlako.

Automatikoki mota semantiko batera mapatzen ez diren atributuak fitxategian biltzen dira **Definitu datuak mapatu gabeko eremuetan** atala. Hautatu mapatu gabeko atributuen mota semantikoaren eremua edo idatzi zure atributu mota izen pertsonalizatua.

> [!div class="mx-imgBorder"]
> ![Gako nagusia eta atributu mota](media/data-manager-configure-map-add-attributes.png "Gako nagusia eta atributu mota")

> [!NOTE]
> Eremu batek Person.FullName mota semantikoarekin mapatu beharko luke bezeroaren izena bezero txartelean betetzeko. Bestela, bezeroen txartelak izenik gabe agertuko dira. 

## <a name="add-and-remove-attributes-and-entities"></a>Gehitu eta kendu atributuak eta entitateak

1. Aktibatuta **Bat egin** > **Mapa**, hautatu **Editatu eremuak**.

2. **Editatu eremuak** panelean, gehitu edo kendu atributuak eta entitateak. Erabili bilaketa edo korritua zure atributuak eta intereseko entitateak aurkitzeko eta hautatzeko. Ezin duzu atributu edo entitate bat kendu dagoeneko parekatuta badaude.

   > [!div class="mx-imgBorder"]
   > ![Gehitu edo kendu atributuak](media/configure-data-map-edit.png "Gehitu edo kendu atributuak")

3. Hautatu **Aplikatu**.

## <a name="add-images-to-profiles"></a>Gehitu irudiak profiletan

Entitateak URLak baditu jendaurrean eskuragarri dauden profileko irudiak edo logotipoak bidaltzeko, bezeroaren profil bateratuari gehitu diezaiokezu.

Hautatu entitatea eta aurkitu URLa duen profila irudia duen eremua. **Mota** sarrerako eremuan eskuz sartu hurrengo balioa: 
- Pertsona batentzat: Pertsona.ProfileImage
- Erakunde batentzat: Organization.LogoImage

Jarraitu bateratze urratsekin eta ziurtatu irudiaren URLa duen atributua gehitzen dela [Batu](merge-entities.md) urratsa.

## <a name="set-attributes-for-organizations"></a>Ezarri erakundeentzako atributuak

Erakundeentzako (aurrebista), atributu mota "Organization.Name" kokatu behar da
> [!div class="mx-imgBorder"]
> ![Gako nagusia eta atributu mota B2B](media/configure-data-map-edit-b2b.png "Gako nagusia eta atributu mota B2B")

## <a name="next-step"></a>Hurrengo urratsa

Datuak bateratzeko prozesuaren baitan, joan **Bat-etortzea** orria. Bisitatu [**Bat-etortzea**](match-entities.md) fase honen berri izateko.

> [!TIP]
> Ikusi hurrengo bideoa: [Lehen urratsak: Bezeroaren profil bateratua sortzea](https://youtu.be/oBfGEhucAxs).
