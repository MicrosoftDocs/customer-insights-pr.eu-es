---
title: Bilatu eta iragazi bezeroen profilak
description: Aurki itzazu zehaztutako atributuetarako bezeroen profil bateratuei eta iragazkiari buruzko informazioa.
ms.date: 01/19/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
manager: shellyha
ms.openlocfilehash: e53d87c4f633cba09fecbc1c219f0ac2ec6bb5598a7902cbcf7398d26d6d7c6b
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7029384"
---
# <a name="customer-profiles-search--filter-index"></a>Bezeroen profilak: Bilatu eta iragazi indizea

Zure bezeroen datuak bateratzearen emaitza Bezeroaren Profilaren entitatea da zure bezero base guztiari ikuspegi bateratua ematen diona. Azkar egiteko [bezero edo talde jakin bati buruzko informazioa bilatu](customer-profiles.md), konfigura dezakezu **Bilatu** eta **Iragazi** gaitasunak **Bezeroak** orria. Irakurri gehiago administratzaileek gailuan atributuak edita ditzaketen jakiteko **Bilatu eta iragazi indizea** orrialdea, erabiltzaileak bilatzeko eta iragazteko erabilgarri daudenak.

> [!div class="mx-imgBorder"]
> ![Bilaketa-iragazkia.](media/search-filter.png "Bilaketa-iragazkia")

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

3. Aukeratu **Exekutatu** zure ezarpenak aplikatzeko prest dagoenean.

## <a name="next-steps"></a>Hurrengo urratsak

Berrikusi [profil bateratuen orria](customer-profiles.md) profilak bilatzeko edo aurkitutako eremuak erabiltzeko profil bateratu guztien azpimultzoa ikusteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]