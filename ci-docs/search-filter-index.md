---
title: 'Bezeroen profilak: Bilatu eta iragazi indizea'
description: Aurki itzazu zehaztutako atributuetarako bezeroen profil bateratuei eta iragazkiari buruzko informazioa.
ms.date: 11/01/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
manager: shellyha
searchScope:
- ci-search-filter
- customerInsights
ms.openlocfilehash: fc076e341f744ac2922dcacdf5f20ae8ecbdbaa0
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9050794"
---
# <a name="customer-profiles-search--filter-index"></a>Bezeroen profilak: Bilatu eta iragazi indizea

Zure bezeroen datuak bateratzearen emaitza Bezeroaren Profilaren entitatea da zure bezero base guztiari ikuspegi bateratua ematen diona. Azkar egiteko [bezero edo talde jakin bati buruzko informazioa bilatu](customer-profiles.md), konfigura dezakezu **Bilatu** eta **Iragazi** gaitasunak **Bezeroak** orria. Irakurri gehiago administratzaileek gailuan atributuak edita ditzaketen jakiteko **Bilatu eta iragazi indizea** orrialdea, erabiltzaileak bilatzeko eta iragazteko erabilgarri daudenak.

   :::image type="content" source="media/search-filter.png" alt-text="Bilaketa-iragazkia":::

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="add-fields-and-specify-attributes"></a>Gehitu eremuak eta zehaztu atributuak

Bilaketa atributuak administratzaile gisa definitzen dituzun lehen aldia bada, indexatu beharreko eremuak lehenik definitu behar dituzu. Erabiltzaileek bezeroak bilatu eta iragazi ditzaketen atributu guztiak aukeratzea gomendatzen dizugu **Bezeroak** orria. Datuak bateratzeko prozesuan sortutako Bezero Profilaren entitatean dauden atributuak soilik zehaztu ditzakezu.

1. Ireki **Bezeroak** orria eta hautatu **Bilatu eta iragazi indizea**.

2. Hautatu **+ Gehitu** zehazteko indexatutako eremuak.

3. Hautatu indexatutako eremu gisa gehitu nahi dituzun zerrendan atributuak. Atributu gehiago gehitu ditzakezu **Gehitu** hautatuta. Aukeratutako atributuak ere kendu ditzakezu **Kendu** sinboloa.

## <a name="explore-the-indexed-customer-fields-table"></a>Arakatu indexatutako bezeroen eremuen taula

Taulan aurkezten da hurrengo informazioa.

- **izena**: Atributuaren izena Bezero Profilaren entitatean agertzen den bezala adierazten du.
- **Datu mota**: Datu mota katea, zenbakia edo data den zehazten du.
- **Bilaketa barne**: Ezartzen du atributu hau bezeroan bilatzeko **Bezeroak** orrialdea **Bilatu** eremu.
- **Gehitu iragazkia**: Kontrola atributu hau iragaztean nola erabil daitekeen definitzeko **Bezeroak** orria.

## <a name="editing-filtering-options-for-a-given-attribute"></a>Emandako atributu baten iragazketa aukerak editatzea

The **Iragazi** menuan **Bezeroak** orrialdeak hainbat atributu-maila izan ditzake (adibidez, bezeroak iragazteko adin-talde desberdinak).

1. Aukeratu **Gehitu iragazkia** atributu jakin batentzako gaiari buruz **Bilatu eta iragazi indizea** orria. Emaitza kopurua eta zer antolatuko diren zehaztu dezakezu. Atributuaren datu motaren arabera, panela hau agertzen da.

- Kate motako atributuak: zehaztu nahi duzun emaitzen kopurua **Kate-iragazkiaren aukerak** taulan eta emaitzok antolatzeko baldintzak.

- Zenbaki motako atributuak: zehaztu **Zenbaki-iragazkiaren aukerak** taulan gehitzeko interbaloak eta hauek antolatzeko baldintzak.

- Datu motako atributuak: zehaztu **Datu-iragazkiaren aukerak** taulan gehitzeko interbaloak eta hauek antolatzeko baldintzak.

2. Aldaketak aplikatzeko, hautatu **Gorde**.

3. Aukeratu **Exekutatu** zure ezarpenak aplikatzeko prest dagoenean. Behin aldaketak prozesatuta, [Bezeroen orriko bezero-txarteletan](customer-profiles.md) aurkituko dituzu. 

## <a name="next-steps"></a>Hurrengo urratsak

Berrikusi [profil bateratuen orria](customer-profiles.md) profilak bilatzeko edo aurkitutako eremuak erabiltzeko profil bateratu guztien azpimultzoa ikusteko.


[!INCLUDE [footer-include](includes/footer-banner.md)]
