---
title: Ikusi bezeroen profilak
description: Lortu zure bezeroen datu bateratuen ikuspegi konbinatua.
ms.date: 12/01/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
manager: shellyha
ms.openlocfilehash: 8ab55d101f98169b8f794ce580ddd0a71ede6642
ms.sourcegitcommit: dab2cbf818fafc9436e685376df94c5e44e4b144
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/13/2021
ms.locfileid: "6554603"
---
# <a name="customer-profiles"></a>Bezeroen profilak

**Bezeroak** orriak zure bezeroen ikuspegi konbinatua erakusten du, [datu-iturburu guztietatik](data-sources.md) bildutako profileko datuetan oinarrituta. Bezeroen profilak behin erabilgarri daude [sortu Bezeroaren erakunde bateratua](data-unification.md). Ziurtatu datuak bateratzeko prozesua betetzen duzula zure bezeroen ikuspegi aberatsagoak lortzeko. Orriak bezeroak bilatzeko aukera ere ematen du.

Bezeroak pertsona edo erakundeak izan daitezke (aurrebista). Bezero edo erakundearen profil bakoitza fitxa batez irudikatuta dago. Aukeratu fitxa bat bezero edo erakunde zehatz horri buruzko informazio osagarria ikusteko. Erabili orrialdearen kontrolaren orrialdearen beheko kontrolak erregistro osagarriak ikusteko.

> [!div class="mx-imgBorder"] 
> ![B2C bezeroen profilak.](media/profiles-customers.png "B2C bezeroen profilak")

Erakundeak (Aurrebista)
> [!div class="mx-imgBorder"] 
> ![B2B bezeroen profilak.](media/profile-customers-b2b.png "B2B bezeroen profilak")

> [!NOTE]
> Hautatzen dituzunean fitxak ezin badituzu ikusi **Bezeroak** nabigazioan, zure administratzaileak egin behar du [definitu gutxienez bilaketa atributu bat](search-filter-index.md) gainean **Bilatu eta iragazi indizea**.

## <a name="search-for-customers"></a>Bilatu bezeroentzako

Bilatu bezeroak izen bat edo beste atributuren bat bilaketa laukian sartuz. Bilaketa datuak bateratzeko prozesuan sortutako Bezero Profilaren entitatearen barruan bakarrik funtzionatzen du.

Administratzaile gisa, bilaketa atributuak konfigura ditzakezu **Bilatu eta iragazi indizea** orria. Informazio gehiago lortzeko, ikus [Kudeatu bilaketa eta iragazki indizea](search-filter-index.md).

## <a name="filter-customers"></a>Iragazi bezeroak

Bezeroak Profilaren entitatearen eremuak iragazi ditzakezu. Bilaketaren antzera, zure administratzaileak lehendabizi eremuak ezin izango ditu definitu **Bilatu eta iragazi indizea** orria.

1. Hautatu **Iragazi** **Bezeroak** orrian.

2. Egiaztatu bezeroak iragazi nahi dituzun atributuen ondoko laukiak.

   > [!div class="mx-imgBorder"] 
   > ![Bezeroen profilak.](media/profiles-customers3.png "Bezeroen profilak")

3. Kendu iragazkiak **Garbitu iragazkiak** hautatuta **Bezeroak** orrian.

##  <a name="customer-details-page"></a>Bezeroaren xehetasunen orria

Aukeratu bezeroaren lauzetako bat **Bezeroaren xehetasunen orria** irekitzeko. Ikuspegi honek aukeratutako bezeroaren informazio bateratua du.

Bezeroaren xehetasunek honako hau barne hartzen dute:

-   **Bezeroaren profilaren lauza**: Lauza honek bezeroaren profileko entitate bateratuaren balio desberdinak erakusten ditu. Xehetasun horien artean helbide elektronikoa, izena, hiria, eta abar sartzen dira. 

-   **Interes potentzialak, marka potentzialak**: Lehen mailako aberastasuna konfiguratu zenuen erakusten du. Bezero honen antzeko profila duten bezeroek izan ditzaketen markekiko interes eta afinitate potentzialak adierazten ditu. Informazio gehiago lortzeko, ikus [Aberastu bezeroen profilak marka eta interes kidetasunekin](enrichment-microsoft.md).

-   **Neurriak**: Mota zehatz bateko neurri bat edo gehiago konfiguratu zenituen erakusten du: bezeroaren atributuaren neurriak. Zure bezeroen inguruan kalkulatutako KPIak sartzen dira bezero bakoitzaren mailan. Informazio gehiagorako, ikusi [Neurriak zehaztea eta kudeatzea](measures.md).

-   **Jardueren kronologia**: Jarduerak konfiguratu dituzun erakusten du. Ikuspegi kronologikoak bezero honen kronologikoki ordenatutako jarduerak biltzen ditu, azken jardueratik hasita. Informazio gehiago lortzeko, ikus [Bezeroaren jarduerak](activities.md).

Aukeratu **Itzuli Bezeroetara** bezeroen bilaketa orrira itzultzeko.

## <a name="next-steps"></a>Hurrengo urratsak

[Gehitu datu iturri gehiago](data-sources.md) edo [bezeroen segmentuak sortu](segments.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
