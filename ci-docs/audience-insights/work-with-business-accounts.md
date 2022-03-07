---
title: Hasteko negozio kontuekin helburu nagusia den publiko gisa
description: Ikasi negozio kontuekin helburu nagusia den publiko gisa Dynamics 365 Customer Insights.
ms.date: 10/19/2021
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.custom: intro-internal
ms.author: wimohabb
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-semantic-mapping
- ci-connections
- customerInsights
ms.openlocfilehash: 88882dc727c37262c9f204fbc8049abe17bd21a3
ms.sourcegitcommit: 73cb021760516729e696c9a90731304d92e0e1ef
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/25/2022
ms.locfileid: "8353527"
---
# <a name="work-with-business-accounts-in-audience-insights"></a>Lana negozio kontuekin audientzia estatistiketan

Ikusleek gaitasuna erakusten dute Dynamics 365 Customer Insights zure ingurunea konfiguratzeko aukera ematen dizu lehen helburu publiko desberdinetarako: kontsumitzaile partikularrak (B-to-C) eta negozio kontuak (B-to-B). B-to-C eszenatokietan, datuak norbanakoen inguruan zentratzen dira. B-to-B eszenatokietan, xede-publiko nagusiak kontuak - erakundeak edo enpresak - eta kontaktuak dira. Artikulu honek negozio kontuetarako ingurune batekin hasi zaitezke. Ezaugarri-arloen desberdintasunak zerrendatzen ditu ikusleen estatistiketan, zure ingurunearen ikuspegiaren arabera. Desberdintasunei buruzko informazio gehiago nahi izanez gero, berrikusi funtzioen arloetako dokumentuak. 

## <a name="create-an-environment-for-business-accounts"></a>Sortu ingurune bat negozio-kontuetarako

Administratzaileek ahal dute [ingurune bat sortu lehendik dagoen erakunde batean](create-environment.md). Ingurune berri bat sortzeko prozesuaren pauso batek administratzaileei inguruneko xede publikoa eskatzen die. Lizentzia erosi ondoren ikusleei buruzko informazioaren hasierako konfigurazioa bada, esperientzia gidatu batek lehen ingurunea sortzen lagunduko du.

Ahal duzu [datuak irenstea](data-sources.md) onartutako iturri guztietako datu iturri gisa negozio kontuetarako eta erlazionatutako kontaktuetarako.

Datuak bateratu ondoren, [zehaztu kontu hierarkiak](relationships.md#set-up-account-hierarchies) harreman konfigurazioaren zati gisa. Ere egin dezakezu [konfiguratu mapaketa semantikoak](semantic-mappings.md) harremanetarako eta kontuko entitateak konektatzeko. 

## <a name="switch-between-primary-target-audience"></a>Aukeratu publiko nagusiaren artean

Zure erakundeak bezero eta negozio kontuen banakako inguruneak mantentzen baditu, ezkerreko paneleko aldatzailea erabil dezakezu xede publiko nagusia aukeratzeko.

:::image type="content" source="media/switch-primary-target-audience.png" alt-text="Aldagailua bezero nagusien eta negozio kontuen artean hartzaile nagusia aldatzeko.":::

## <a name="supported-feature-areas"></a>Onartutako eginbide-eremuak

- [Jarduerak](activities.md): Kontuak eta erlazionatutako harremanetarako laguntza, jarduerak sortzeko eta kronograman erakusteko.
- [Harremanak](relationships.md): Jardueren morroiak entitateen arteko harremanak sortzen laguntzen du, kontu ikuspegiak kontaktuen jarduera guztiak erakutsi ditzan. Kontaktuek kontaktuen ikuspegia ikusteko xehetasunak egin ditzakete eta hierarkiak erabil daitezke kontuko aktibitateen batuketetarako.
- [Neurriak](measures.md): Neurrien sortzailetik sortutako neurriak kalkulu batekin onartzen ditu. Aukerako ezarpen batek azpikontuak biltzeko aukera ematen du neurriak sortzerakoan.
- [Segmentuak](segments.md): Segmentu-sortzailearekin hutsetik sortzen diren segmentuak onartzen ditu. Operadore berriek kontuen hierarkia txertatzea ahalbidetzen dute segmentuak eraikitzerakoan.
- [Datuak sartzea](data-sources.md): Arlo honetako eginbide guztiak berdinak dira negozio kontuetarako eta bezero partikularrek.
- [Datuak bateratzea](data-unification.md): Arlo honetako eginbide guztiak berdinak dira negozio kontuetarako eta bezero partikularrek.
- [Aberastea](enrichment-hub.md): Zenbait aberastasun mota bezeroen agertoki indibidualetarako soilik daude eskuragarri, beste batzuk negozio kontuetarako soilik.
- [Iragarpenak eta kutxaz kanpoko ereduak](predictions-overview.md): Transaction churn iragarpen-ek urrats gehigarriak ditu negozio kontuetarako. Beste iragarpen batzuk bezeroentzako bakarrik daude eskuragarri.
- [Aktibazioa eta esportazioa](export-destinations.md): Esportazioak negozio kontuak eta bezero partikularrak eskuragarri daude. Zenbait esportaziok konfigurazio gehigarria eta azpiko segmentuetan proiektatutako harremanetarako informazioa eskatzen dute negozio kontuetarako balio dezaten.
- [Sistemaren ezarpenak](system.md) eta [erabiltzailearen kudeaketa](permissions.md): eremu horretako eginbide guztiak berdinak dira negozio-kontuetarako eta banakako bezeroentzako.

