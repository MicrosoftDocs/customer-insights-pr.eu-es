---
title: Sortu zure bezeroen ikuspegi bateratua
description: Joan datuak bateratzeko prozesua zure datuekin bezeroen profil bateratuen datu multzo bakarra sortzeko.
ms.date: 05/10/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: overview
author: v-wendysmith
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-map
- customerInsights
ms.openlocfilehash: bb8da6f4b9f92f2b265ff9807e04638edae4f814
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755719"
---
# <a name="data-unification-overview"></a>Datuak bateratzeko ikuspegi orokorra

[!INCLUDE [m3-prod-trial-note](includes/m3-prod-trial-note.md)]

[Datu-iturburuak konfiguratu](data-sources.md) ondoren, datuak bateratu ditzakezu. Datuen bateratzeak behin-behinean bereizten diren datu-iturriak bateratzeko aukera ematen dizu datu horien ikuspegi bateratua eskaintzen duen datu-multzo nagusi bakar batean. Kontsumitzaile indibidualentzat (B-to-C) datuak pertsonen inguruan zentratuta daudenentzat, bateratzeak zure bezeroen ikuspegi bateratua eskaintzen du. Datuak kontuetan zentratuta dauden negozio-kontuetarako (B-tik-B), zure kontuen ikuspegi bateratua eskaintzen du bateratzeak.

Datuak entitate bakarrean edo entitate anitzetan batera daitezke. Bateratze ordena honetan egiten da:

1. [Iturburu-eremuak](map-entities.md) (lehen Mapa izenekoa): iturburu-eremuen urratsean, hautatu bateratze-prozesuan sartzeko entitateak eta eremuak. Mapeatu eremuak eremuaren helburua deskribatzen duen mota semantiko arrunt batera.

1. [Erregistro bikoiztuak](remove-duplicates.md) (aurretik Match-en parte da): Erregistro bikoiztuak urratsean, aukeran zehaztu arauak entitate bakoitzaren barruan bezeroen erregistro bikoiztuak kentzeko.

1. [Bat datozen baldintzak](match-entities.md) (lehen Bat-etortzea deitzen zen): bat-etortze-baldintzak urratsean, definitu entitateen arteko bezero-erregistroak bat datozen arauak. Bezero bat bi entitate edo gehiagotan aurkitzen denean, erregistro bateratu bakarra sortzen da entitate bakoitzeko zutabe eta datu guztiekin.

1. [Bezeroen eremu bateratuak](merge-entities.md) (aurretik Bateratu deitua): bezeroen eremu bateratuen urratsean, zehaztu zein iturburu-eremu sartu, baztertu edo batu behar diren bezero-profil bateratu batean.  

1. [Iritzia](review-unification.md) eta profil bateratua sortu.

Datuen bateratzea amaitu ondoren, aukeran egin dezakezu:

- [Entitateen arteko harremanak ezarri](relationships.md) segmentu sofistikatuak sortzeko.
- [Aberastu zure datuak](enrichment-hub.md) zure bezeroei buruzko informazio sorta zabalagoa lortzeko.
- [Jarduerak definitu](activities.md) irensten diren atributu batzuetatik.
- [Eraiki neurriak](measures.md) bezeroen jokabideak eta negozioaren errendimendua hobeto ulertzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
