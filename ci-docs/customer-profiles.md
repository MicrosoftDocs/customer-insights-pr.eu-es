---
title: Ikusi bezeroen profilak
description: Ikusi zure bezeroen datu bateratuak bilaketa eta iragazkia erabiliz barne
ms.date: 06/08/2022
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
ms.openlocfilehash: 6cdf47e6997f230811dcb0f2cf5542f3a6db2367
ms.sourcegitcommit: c45c3e044034bf866b0662f80a59166cee4ababe
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188078"
---
# <a name="view-customer-profiles"></a>Ikusi bezeroen profilak

Bezeroen profilak eskuragarri dituzu behin [bateratua sortu *Bezeroa* entitate](data-unification.md). Zure bezeroen profil bateratuen ikuspegi konbinatua bistaratzen da **Bezeroak** orrialdea. Bezeroak norbanakoak edo erakundeak izan daitezke.

Joan zaitez **Bezeroak** orrialdea zure bezeroak eta haien profilak ikusteko. Bezeroen profil bakoitza fitxa baten bidez irudikatzen da. Erabili paginazio kontrolak erregistro gehiago lortzeko. Txartelak eremuko eremuak erakusten ditu *Bezeroa* fitxategian definitutako entitatea **Bilatu eta iragazi indizea**. Txartel bakoitzaren barruko eremuen ordena sistemak hautatzen du.

> [!NOTE]
> Aukeratzen duzunean fitxak ikusten ez badituzu **Bezeroak**, zure administratzaileak behar du [definitu gutxienez bilaketa daitekeen atributu bat](search-filter-index.md) urtean **Bilatu eta iragazi indizea**.

:::image type="content" source="media/customers-page-result-tiles-B2C.png" alt-text="Bezeroen orria emaitza lauzak erakusten ditu.":::

Hautatu ekintza hauetako bat:
- [Ikusi bezeroaren xehetasunak](#view-customer-details)
- [Kudeatu bilaketa eta iragazki indizea](search-filter-index.md) (administratzaileak soilik)
- [Iragazi bezeroak](#filter-customers)
- **Zabaldu txartelak** edo **Tolestu txartelak** bezeroaren fitxan bistaratzen den informazioa zabaltzeko edo tolesteko
- **Ordenatu** atributu jakin bat
- [Bilatu bezeroentzako](#search-for-customers)

  > [!NOTE]
  > Bilaketa eta iragazkia erabiltzeko, administratzaileak bilaketa-atributuak konfiguratu eta iragaz daitezkeen eremuak definitu behar ditu bilaketa eta iragazkien indizea erabiliz.

## <a name="search-for-customers"></a>Bilatu bezeroentzako

Bilatu bezeroak izen bat edo beste atributuren bat sartuta **Bilatu bezeroak**. Bila daitezkeen atributuak administratzaileak definitzen ditu eta bateratutik datoz *Bezeroa* entitate.

> [!NOTE]
> **Katea** bilaketan sartzen den datu mota bakarra da. Erabili ezazu **Bilatu bezeroak** Bezeroak orrialdeko eremua bezeroak bilatzeko.

## <a name="filter-customers"></a>Iragazi bezeroak

Iragazi bezeroak arabera *Bezeroa* entitate-eremuak. Eremu iragazgarriak administratzaileak definitzen ditu.

1. Gainean **Bezeroak** orrialdea, hautatu **Erakutsi iragazkiak**. Iragazkiaren panela bistaratzen da.

1. Egiaztatu bezeroak iragazi nahi dituzun atributuen ondoko laukiak.

1. Kendu iragazki guztiak hautatuta **Garbitu iragazkiak** edo garbitu hautatutako atributu baten ondoan dagoen kontrol-lauki bat.

1. Hautatu **Ezkutatu iragazkiak** iragazkien panela ixteko.

1. Iragazkien emaitzak a gisa gordetzeko [segmentua](segments.md), hautatu **Gorde iragazkiak segmentu gisa**.
   1. Sartu izen bat segmentuarentzat.
   1. Hautatu **Gorde** segmentua gordetzeko.
   1. Aukeratu segmentua orain exekutatu nahi duzun hautatuta **Aktibatu** edo exekutatu **Geroago**.

## <a name="view-customer-details"></a>Ikusi bezeroaren xehetasunak

Gainean **Bezeroak** orrialdean, hautatu bezeroaren fitxa bat hautatutako bezeroaren xehetasunak ikusteko.

:::image type="content" source="media/customers-details-B2C.png" alt-text="Bezeroaren xehetasunen orria.":::

Bezeroaren xehetasunek honako hau barne hartzen dute:

**Bezeroaren profilaren fitxa** bateratuaren balio desberdinak erakusten ditu *Bezeroa* entitate. Eremu batek hautatutako bezero-profilerako baliorik ez badu, ez da agertuko helbidearen eremua izan ezik. Fitxa ataletan egituratuta dago:

- Lehenengo atalean aurrez zehaztutako eremu multzo bat agertzen da eta jarraian bilaketa eta iragazki indizearen zati diren eremu guztiak agertzen dira. Helbideekin erlazionatutako eremu guztiak lerro bakarrean konbinatzen dira, profilak helbide-informaziorik ez badu ere erakusten du.
- **Bezero honen kontaktuak** negozio-kontuetarako inguruneetan bistaratzea. Kontaktu bakoitza bere eremuekin erakusten da. Eremu hutsak ezkutatuta daude.
- **Eremu gehigarriak** hautatutako bezeroaren gainerako eremuak erakusten ditu, IDak izan ezik.
- **NANak** ID guztiak zerrendatzen ditu dagokion entitate-izenpean. Eremuak ID gisa identifikatzen dira euren semantikaren arabera.

**Jardueren kronograma** datuak erakusten ditu konfiguratu baduzu [jarduerak](activities.md). Denbora-lerroaren ikuspegiak hautatutako bezeroaren kronologikoki antolatutako jarduerak biltzen ditu, azken jardueratik hasita.

**Xehetasunak**:

- **Neurriak** erakutsi konfiguratu baduzu [bezeroen atributuen neurriak](measures.md). Zure bezeroen inguruan kalkulatutako KPIak sartzen dira bezero bakoitzaren mailan.

- **Balizko interesak, balizko markak** erakutsi a konfiguratu duzun [marka edo interes afinitate aberastea](enrichment-microsoft.md). Aukeratutako profilaren antzekoa den profila duten beste bezero batzuetan oinarritutako marka eta interes potentzialak adierazten ditu.

-ra itzultzeko **Bezeroak** orrialdea, hautatu **Itzuli Bezeroetara**.

## <a name="next-steps"></a>Hurrengo urratsak

[Gehitu datu iturri gehiago](data-sources.md), [profil bateratuak aberastu](enrichment-hub.md), edo [segmentuak sortu](segments.md) bezeroen profil bateratuekin lan egiteko beste aplikazio batzuetan.

[!INCLUDE [footer-include](includes/footer-banner.md)]
