---
title: Egin lan negozio-kontuekin
description: Lortu informazio negozio-kontuei buruz helburu nagusi gisa Dynamics 365 Customer Insights.
ms.date: 10/19/2021
ms.subservice: audience-insights
ms.topic: conceptual
author: v-wendysmith
ms.custom: intro-internal
ms.author: wimohabb
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-semantic-mapping
- ci-connections
- customerInsights
ms.openlocfilehash: abb77a720ab737520a905b0c93b65573e669109f
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9303901"
---
# <a name="work-with-business-accounts"></a>Egin lan negozio-kontuekin

The Dynamics 365 Customer Insights zure ingurunea helburu nagusi desberdinetarako konfiguratzeko aukera ematen dizu: kontsumitzaile indibidualak (B-to-C) eta negozio-kontuak (B-to-B). B-to-C eszenatokietan, datuak norbanakoen inguruan zentratzen dira. B-to-B eszenatokietan, xede-publiko nagusiak kontuak - erakundeak edo enpresak - eta kontaktuak dira. Artikulu honek negozio kontuetarako ingurune batekin hasi zaitezke. Customer Insights-en eginbide-eremuen desberdintasunak zerrendatzen ditu, zure ingurunearen ikuspegiaren arabera. Desberdintasunei buruzko informazio gehiago nahi izanez gero, berrikusi funtzioen arloetako dokumentuak. 

## <a name="create-an-environment-for-business-accounts"></a>Sortu ingurune bat negozio-kontuetarako

Administratzaileek ahal dute [ingurune bat sortu lehendik dagoen erakunde batean](create-environment.md). Ingurune berri bat sortzeko prozesuaren pauso batek administratzaileei inguruneko xede publikoa eskatzen die. Lizentzia erosi ondoren hasierako konfigurazioa bada, esperientzia gidatu batek lehen ingurunea sortzen laguntzen du.

Ahal duzu [datuak irenstea](data-sources.md) onartutako iturri guztietako datu iturri gisa negozio kontuetarako eta erlazionatutako kontaktuetarako.

 [Bateratu](data-unification.md) zure kontuaren datuak eta ondoren zure kontaktu datuak kontaktu eta kontu entitateak konektatzeko.

## <a name="switch-between-primary-target-audience"></a>Aukeratu publiko nagusiaren artean

Zure erakundeak bezero eta negozio kontuen banakako inguruneak mantentzen baditu, ezkerreko paneleko aldatzailea erabil dezakezu xede publiko nagusia aukeratzeko.

:::image type="content" source="media/switch-primary-target-audience.png" alt-text="Aldagailua bezero nagusien eta negozio kontuen artean hartzaile nagusia aldatzeko.":::

## <a name="supported-feature-areas"></a>Onartutako eginbide-eremuak

- [Jarduerak](activities.md): Kontuak eta erlazionatutako harremanetarako laguntza, jarduerak sortzeko eta kronograman erakusteko.
- [Harremanak](relationships.md): Jardueren morroiak entitateen arteko harremanak sortzen laguntzen du, kontu ikuspegiak kontaktuen jarduera guztiak erakutsi ditzan. Kontaktuek kontaktuen ikuspegia ikusteko xehetasunak egin ditzakete eta hierarkiak erabil daitezke kontuko aktibitateen batuketetarako.
- [Neurriak](measures.md): Neurrien sortzailetik sortutako neurriak kalkulu batekin onartzen ditu. Aukerako ezarpen batek azpikontuak biltzeko aukera ematen du neurriak sortzerakoan.
- [Segmentuak](segments.md): Segmentu-sortzailearekin hutsetik sortzen diren segmentuak onartzen ditu. Segmentuak kontuetan edo kontaktuetan oinarritu daitezke.
- [Datuak sartzea](data-sources.md): Arlo honetako eginbide guztiak berdinak dira negozio kontuetarako eta bezero partikularrek.
- B-to-B datu-bateratze B-to-C datu-bateratzearen oso antzekoa da, baina urrats gehigarri bat dauka kontaktuak bateratzeko kontua bateratu ondoren. Ikusi [Enpresa kontuak (B-to-B)](data-unification.md).
- [Aberastea](enrichment-hub.md): Zenbait aberastasun mota bezeroen agertoki indibidualetarako soilik daude eskuragarri, beste batzuk negozio kontuetarako soilik.
- [Iragarpenak eta kutxaz kanpoko ereduak](predictions-overview.md): Transaction churn iragarpen-ek urrats gehigarriak ditu negozio kontuetarako. Beste iragarpen batzuk bezeroentzako bakarrik daude eskuragarri.
- [Aktibazioa eta esportazioa](export-destinations.md): Esportazioak negozio kontuak eta bezero partikularrak eskuragarri daude. Zenbait esportaziok konfigurazio gehigarria eta azpiko segmentuetan proiektatutako harremanetarako informazioa eskatzen dute negozio kontuetarako balio dezaten.
- [Sistemaren ezarpenak](system.md) eta [erabiltzailearen kudeaketa](permissions.md): eremu horretako eginbide guztiak berdinak dira negozio-kontuetarako eta banakako bezeroentzako.

[!INCLUDE [footer-include](includes/footer-banner.md)]
