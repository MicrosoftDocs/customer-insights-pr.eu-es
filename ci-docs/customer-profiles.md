---
title: Ikusi bezeroen profilak
description: Lortu zure bezeroen datu bateratuen ikuspegi konbinatua.
ms.date: 05/13/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: Nils-2m
ms.author: nikeller
manager: shellyha
searchScope:
- ci-customers-page
- ci-customer-card
- ci-activities
- ci-activities-wizard
- customerInsights
ms.openlocfilehash: 9bb7abc04afe38d73e1df9b252e1864fa6570d7e
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755766"
---
# <a name="customer-profiles"></a>Bezeroen profilak

**Bezeroak** orrialdeak zure bezeroen profil bateratuen ikuspegi konbinatua erakusten du. Bezeroen profilak behin eskuragarri daude [sortu du Bezeroen entitate bateratua](data-unification.md). Orriak bezeroak bilatzeko eta bilaketa horretarako aurkibidea definitzeko aukera ematen dizu.

Bezeroak norbanakoak edo erakundeak izan daitezke. Bezeroen profil bakoitza fitxa baten bidez irudikatzen da. Erabili paginazio kontrolak erregistro gehiago lortzeko. Txartelak eremuko eremuak erakusten ditu *Bezeroa* fitxategian definitutako entitatea **Bilatu eta iragazi indizea**. Txartel bakoitzaren barruko eremuen ordena sistemak hautatzen du.

Aukeratu fitxa bat hautatutako bezeroarentzako datuak ikusteko izeneko orri dedikatu batean [Bezeroaren xehetasunen orria](customer-profiles.md#customer-details-page).

> [!div class="mx-imgBorder"]
> ![Bezeroen orria emaitza fitxak erakusten ditu](media/customers-page-result-tiles-B2C.png "Bezeroen orria emaitza fitxak erakusten ditu")

> [!NOTE]
> Aukeratzean fitxak ikusi ezin badituzu **Bezeroak** nabigazioan, zure administratzaileak behar du [definitu gutxienez bila daitekeen atributu bat](search-filter-index.md) urtean **Bilatu eta iragazi indizea**.

## <a name="search-for-customers"></a>Bilatu bezeroentzako

Bilatu bezeroak izen bat edo beste atributuren bat bilaketa laukian sartuz. Bilaketa fitxategiaren barruan soilik funtzionatzen du *Bezeroa* datuak bateratzeko prozesuan sortutako entitatea.

Administratzaile gisa, bilaketa atributuak konfigura ditzakezu **Bilatu eta iragazi indizea** orria. Informazio gehiagorako, joan hona [Kudeatu bilaketa eta iragazki indizea](search-filter-index.md).

## <a name="filter-customers"></a>Iragazi bezeroak

Bezeroen arabera iragazi ditzakezu *Bezeroa* entitate eremuak. Bilaketaren antzera, zure administratzaileak lehendabizi eremuak ezin izango ditu definitu **Bilatu eta iragazi indizea** orria.

1. Aukeratu **Erakutsi iragazkiak** gainean **Bezeroak** orrialdea.

1. Egiaztatu bezeroak iragazi nahi dituzun atributuen ondoko laukiak.

1. Kendu iragazkiak **Garbitu iragazkiak** hautatuta **Bezeroak** orrian.

## <a name="customer-details-page"></a>Bezeroaren xehetasunen orria

Aukeratu bezeroaren lauzetako bat **Bezeroaren xehetasunen orria** irekitzeko. Ikuspegi honek aukeratutako bezeroaren informazio bateratua du. Bezeroaren datuen artean honako eduki hau dago:

**Bezeroaren profilaren fitxa**: Fitxa honek bateratuaren balio desberdinak erakusten ditu *Bezeroa* entitatea. Eremu batek aukeratutako bezeroaren profilerako baliorik ez badu, ez da erakutsiko. Fitxa ataletan egituratuta dago:

- Lehenengo atalean aurrez zehaztutako eremu multzo bat agertzen da eta jarraian bilaketa eta iragazki indizearen zati diren eremu guztiak agertzen dira. Helbideekin lotutako eremu guztiak lerro bakarrean konbinatzen dira profilak eremu horiek baditu.
- **Bezero honen kontaktuak**: Enpresa kontuetarako inguruneetan, bezero honi lotutako kontaktu guztiak ikusiko dituzu bigarren atal gisa. Kontaktu bakoitza bere eremuekin erakusten da. Eremu hutsak ezkutatuta daude.
- **Eremu osagarriak**: Aukeratutako bezeroaren gainerako eremuak erakusten ditu, IDak izan ezik.
- **IDak**: ID guztiak dagokien entitatearen izenarekin zerrendatzen ditu. Eremuak beren semantikaren bidez identifikatzen dira ID gisa, eta horrela sailkatzen dituzte.

**Jardueren kronograma**: Datuak erakusten ditu jarduerak konfiguratuta badituzu. Denbora-lerroaren ikuspegiak hautatutako bezeroaren kronologikoki antolatutako jarduerak biltzen ditu, azken jardueratik hasita. Informazio gehiagorako, joan [Bezeroaren jarduerak](activities.md).

**Xehetasunak**:

- **Neurriak**: Bezeroaren atributu neurri bat edo gehiago konfiguratu zenituen erakusten du. Zure bezeroen inguruan kalkulatutako KPIak sartzen dira bezero bakoitzaren mailan. Informazio gehiagorako, joan hona [Neurriak zehaztu eta kudeatu](measures.md).

- **Interes potentzialak, marka potentzialak**: Marka edo interes afinitate aberastasuna konfiguratu zenuen erakusten du. Aukeratutako profilaren antzekoa den profila duten beste bezero batzuetan oinarritutako marka eta interes potentzialak adierazten ditu. Informazio gehiagorako, joan hona [Bezeroen profilak aberastu marka eta interesen arteko kidetasunekin](enrichment-microsoft.md).

Bezeroen bilaketa orrira itzultzeko, hautatu **Itzuli Bezeroetara**.

## <a name="next-steps"></a>Hurrengo urratsak

[Gehitu datu iturri gehiago](data-sources.md), [profil bateratuak aberastu](enrichment-hub.md), edo [segmentuak sortu](segments.md) bezeroen profil bateratuekin lan egiteko beste aplikazio batzuetan.

[!INCLUDE [footer-include](includes/footer-banner.md)]
