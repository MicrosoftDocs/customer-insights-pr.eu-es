---
title: Sortu zure bezeroen ikuspegi bateratua
description: Joan datuak bateratze-prozesua zure datuekin kontu edo bezero-profilen datu-multzo nagusi bakarra sortzeko.
ms.date: 08/12/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: overview
author: Scott-Stabbert
ms.author: sstabbert
manager: shellyha
searchScope:
- ci-map
- customerInsights
ms.openlocfilehash: c2a81776eab147c4b5209a6fbf89c0f4c9853d1d
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304412"
---
# <a name="data-unification-overview"></a>Datuak bateratzeko ikuspegi orokorra

[Datu-iturburuak konfiguratu](data-sources.md) ondoren, datuak bateratu ditzakezu. Datuen bateratzeak behin-behineko datu-iturburuak bateratzeko aukera ematen dizu datu horien ikuspegi bateratua eskaintzen duen datu-multzo nagusi bakar batean.

Kontsumitzaile indibidualentzat (B-to-C) datuak pertsonen inguruan zentratuta daudenentzat, bateratzeak zure bezeroen ikuspegi bateratua eskaintzen du. Datuak kontuetan zentratuta dauden negozio-kontuetarako (B-tik-B), zure kontuen ikuspegi bateratua eskaintzen du bateratzeak. [Kontaktuen bateratzea (aurrebista)](data-unification-contacts.md) kontu horietako kontaktuak bereizita bateratu eta kontuekin lotzeko aukera ematen du.

Datuak entitate bakarrean edo entitate anitzetan batera daitezke.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

Bateratze-prozesuak zure datu-iturburuetako bezeroen datuak mapatzen ditu, bikoiztuak kentzen ditu, entitateen arteko datuak bat egiten ditu eta profil bateratua sortzen du. Bateratze ordena honetan egiten da:

1. [Iturburu-eremuak](map-entities.md) (lehen Mapa izenekoa): iturburu-eremuen urratsean, hautatu bateratze-prozesuan sartzeko entitateak eta eremuak. Mapeatu eremuak eremuaren helburua deskribatzen duen mota semantiko arrunt batera.

1. [Erregistro bikoiztuak](remove-duplicates.md) (aurretik Match-en parte da): Erregistro bikoiztuak urratsean, aukeran zehaztu arauak entitate bakoitzaren barruan bezeroen erregistro bikoiztuak kentzeko.

1. [Bat datozen baldintzak](match-entities.md) (aurretik Bat-etortzea deitua): bat-etortze-baldintzak urratsean, definitu entitateen arteko bezero-erregistroak bat datozen arauak. Bezero bat bi entitate edo gehiagotan aurkitzen denean, erregistro bateratu bakarra sortzen da entitate bakoitzeko zutabe eta datu guztiekin.

1. [Bezeroen eremu bateratuak](merge-entities.md) (aurretik Bateratu deitua): bezeroen eremu bateratuen urratsean, zehaztu zein iturburu-eremu sartu, baztertu edo batu behar diren bezero-profil bateratu batean.  

1. [Berrikuspena](review-unification.md) eta profil bateratua sortu.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

Bateratze-prozesuak zure datu-iturburuetako kontu-datuak mapatzen ditu, bikoiztuak kentzen ditu, entitateen arteko datuak bat egiten ditu eta profil bateratua sortzen du. Bateratze ordena honetan egiten da:

1. [Iturburu-eremuak](map-entities.md) (lehen Mapa izenekoa): iturburu-eremuen urratsean, hautatu kontu bateratu prozesuan sartu beharreko entitateak eta eremuak. Mapeatu eremuak eremuaren helburua deskribatzen duen mota semantiko arrunt batera.

1. [Erregistro bikoiztuak](remove-duplicates.md) (aurretik Bat-etortzearen zatia): Erregistro bikoiztuak urratsean, aukeran definitu arauak entitate bakoitzaren barruan bikoiztutako kontuen erregistroak kentzeko.

1. [Bat datozen baldintzak](match-entities.md) (lehen Bat-etortzea deitua): bat-etortze-baldintzak urratsean, definitu entitateen arteko kontu-erregistroak bat datozen arauak. Kontu bat bi entitate edo gehiagotan aurkitzen denean, erregistro bateratu bakarra sortzen da entitate bakoitzeko zutabe eta datu guztiekin.

1. [Bezeroen eremu bateratuak](merge-entities.md) (aurretik Bateratu deitua): bezeroen eremu bateratuen urratsean, zehaztu zein iturburu-eremu sartu, baztertu edo batu behar diren bezero-profil bateratu batean.  

1. [Berrikuspena](review-unification.md) eta profil bateratua sortu.

Kontuak bateratu ondoren, aukeran egin dezakezu [bateratu kontaktuak (aurrebista)](data-unification-contacts.md) kontu horietarako eta lotu kontaktu bateratuak kontu bateratuekin.

---

Datuen bateratzea amaitu ondoren, aukeran egin dezakezu:

- [Entitateen arteko harremanak ezarri](relationships.md) segmentu sofistikatuak sortzeko.
- [Aberastu zure datuak](enrichment-hub.md) zure bezeroei buruzko informazio sorta zabalagoa lortzeko.
- [Jarduerak definitu](activities.md) irensten diren atributu batzuetatik.
- [Eraiki neurriak](measures.md) bezeroen jokabideak eta negozioaren errendimendua hobeto ulertzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
