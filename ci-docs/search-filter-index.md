---
title: Kudeatu bezeroen profilen bilaketa eta iragazki indizea
description: Aurki itzazu zehaztutako atributuetarako bezeroen profil bateratuei eta iragazkiari buruzko informazioa.
ms.date: 07/22/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
manager: shellyha
searchScope:
- ci-search-filter
- customerInsights
ms.openlocfilehash: dfbfcbff3ffb3e4483252377e591229631d38556
ms.sourcegitcommit: c45c3e044034bf866b0662f80a59166cee4ababe
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/22/2022
ms.locfileid: "9187894"
---
# <a name="manage-the-search--filter-index-for-customer-profiles"></a>Kudeatu bezeroen profilen bilaketa eta iragazki indizea

Zure bezeroen datuak bateratzearen emaitza a da *Bezeroa* zure bezero-base osoaren ikuspegi bateratua eskaintzen duen entitatea. Erabiltzaileek azkar egin dezaten [bezero edo bezero talde jakin bati buruzko informazioa aurkitzea](customer-profiles.md), administratzaile batek konfiguratu behar du **Bilatu** eta **Iragazkia** rako gaitasunak **Bezeroak** orrialdea.

   :::image type="content" source="media/search-filter.png" alt-text="Bilaketa-iragazkia":::

## <a name="define-searchable-attributes-and-indexed-fields"></a>Definitu bilaketa daitezkeen atributuak eta indexatutako eremuak

Administratzaile gisa bilaketa daitezkeen atributuak definitzen dituzun lehen aldia bada, definitu lehenik indexatutako eremuak. Erabiltzaileek bezeroak bilatu eta iragazi ditzaketen atributu guztiak aukeratzea gomendatzen dizugu **Bezeroak** orria. -n dauden atributuak soilik *Bezeroa* datuak bateratzeko prozesuan sortutako entitatea zehaztu daiteke.

1. Joan **Bezeroak** eta hautatu **Bilatu eta iragazi indizea**.

1. Hautatu **+ Gehitu**.

1. Hautatu indexatutako eremu gisa gehitu nahi dituzun zerrendako atributuak eta egin klik **Aplikatu**.

1. Atributu gehiago gehitzeko, hautatu **Gehitu**. Hautatutako atributu bat kentzeko, hautatu atributua eta gero **Ezabatu**.

   :::image type="content" source="media/search-filter-index.png" alt-text="Bilatu eta iragazi indize orria.":::

1. Hautatu **Korrika egin** bilaketa eta iragazki ezarpenak aplikatzeko prest zaudenean. Aldaketak prozesatu ondoren, ikusi itzazu [bezeroen txartelak Bezeroaren orrian](customer-profiles.md).

## <a name="define-filtering-options-for-a-given-attribute"></a>Definitu atributu jakin baterako iragazteko aukerak

Konfiguratu bezeroak iragazteko erabil daitezkeen eremuak **Bezeroak** orrialdea.

1. Joan **Bezeroak** eta hautatu **Bilatu eta iragazi indizea**.

1. Hautatu atributu bat eta **Gehitu iragazkia**. Definitu emaitza kopurua eta zein ordenatan antolatuko diren. Atributuaren datu-motaren arabera, panel hauetako bat agertuko da.

   - Kate motako atributuak: zehaztu nahi den emaitza kopurua **Kate-iragazkia** panela eta antolatuko diren ordena-politika.

   - Zenbakizko-motako atributuak: Zehaztu tarteak **Zenbaki-iragazkia** panela eta antolatuko diren ordena-politika.

   - Data-motako atributuak: Zehaztu zein tarteak **Data-iragazkia** panela eta antolatuko diren ordena-politika.

1. Hautatu **Ados**. Errepikatu iragazi nahi dituzun atributu guztietan.

1. Hautatu **Korrika egin** bilaketa eta iragazki ezarpenak aplikatzeko prest zaudenean. Aldaketak prozesatu ondoren, ikusi itzazu [bezeroen txartelak Bezeroaren orrian](customer-profiles.md).

## <a name="view-indexed-customer-fields"></a>Ikusi indexatutako bezeroen eremuak

The **Bilatu eta iragazi indizea** orrialdeak informazio hau bistaratzen du:

- **Izena** : atributuaren izena adierazten du *Bezeroa* entitate.
- **Datu mota**: Datu mota katea, zenbakia edo data den zehazten du.
- **Bilaketa barne**: Ezartzen du atributu hau bezeroan bilatzeko **Bezeroak** orrialdea **Bilatu** eremu.
- **Gehitu iragazkia**: Kontrola atributu hau iragaztean nola erabil daitekeen definitzeko **Bezeroak** orria.

## <a name="next-steps"></a>Hurrengo urratsak

Berrikusi [profil bateratuen orria](customer-profiles.md) profilak bilatzeko edo aurkitutako eremuak erabiltzeko profil bateratu guztien azpimultzoa ikusteko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
