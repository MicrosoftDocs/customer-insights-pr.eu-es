---
title: Hartu datuak a bidez Power Query konektorea (bideoa dauka)
description: -n oinarritutako datu-iturburuetarako konektoreak Power Query.
ms.date: 05/09/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: matgos
manager: shellyha
searchScope:
- ci-data-sources
- ci-create-data-source
- customerInsights
ms.openlocfilehash: b99c3b446e580f455f9678d54d9db414aea9b331
ms.sourcegitcommit: 5e26cbb6d2258074471505af2da515818327cf2c
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "9011642"
---
# <a name="connect-to-a-power-query-data-source"></a>Konektatu a Power Query datu-iturburu

Power Query datuak irensteko konektore multzo zabala eskaintzen du. Konektore hauetako gehienek onartzen dute Dynamics 365 Customer Insights.

Oinarritutako datu-iturriak gehitzea Power Query konektoreak, oro har, atal honetan adierazitako urratsak jarraitzen ditu. Hala ere, erabiltzen duzun konektorearen arabera, informazio desberdina behar da. Gehiago jakiteko, ikusi konektore indibidualei buruzko dokumentazioa [Power Query konektorearen erreferentzia](/power-query/connectors/).

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWN6EK]

## <a name="create-a-new-data-source"></a>Sortu datu-iturburua

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Aukeratu **Microsoft Power Query**.

1. Eman a **Izena** eta aukerakoa **Deskribapena** datu-iturburu-erako, eta hautatu **Hurrengoa**.

1. Hautatu bat [erabilgarri dauden konektoreetatik](#available-power-query-data-sources). Adibide honetan, hautatzen dugu **Testua/CSV** konektorea.

1. Idatzi beharrezko datuak **Konexio ezarpenak** hautatutako lokailurako eta hautatu **Hurrengoa** datuen aurrebista ikusteko.

1. Hautatu **Transformatu datuak**. Urrats honetan entitateak gehituko dituzu zure datu-iturburu-era. Entitateak datu multzoak dira. Datu-multzo ugari biltzen dituen datu-basea baduzu, datu-multzo bakoitza bere entitatea da.

1. The **Power Query - Editatu kontsultak** elkarrizketa-koadroak datuak berrikusi eta findu ditzakezu. Aukeratutako datu-iturburu sistemetan identifikatutako sistemak ezkerreko panelean agertzen dira.

   :::image type="content" source="media/data-manager-configure-edit-queries.png" alt-text="Editatu eskaera eztabaida":::

1. Zure datuak ere eralda ditzakezu. Hautatu entitate bat editatzeko edo eraldatzeko. Erabili aukerak Power Query eraldaketak aplikatzeko leihoa. Transformazio bakoitza azpian dago zerrendatuta **Aplikaturiko urratsak**. Power Query aurrez eraikitako eraldaketa aukera ugari eskaintzen ditu. Informazio gehiagorako, ikus [Power Query Eraldaketak](/power-query/power-query-what-is-power-query#transformations).

   Ondorengo eraldaketak erabiltzea gomendatzen dugu:

   - CSV fitxategi bateko datuak irensten badituzu, lehenengo ilaran maiz goiburuak agertzen dira. Joan **Eraldatu** eta hautatu **Erabili lehen errenkada goiburu gisa**.
   - Ziurtatu datu mota behar bezala ezarrita dagoela. Adibidez, data eremuetarako, hautatu data mota bat.

1. Zure datu-iturburu-i entitate gehigarriak gehitzeko **Editatu kontsultak** elkarrizketa-koadroa, joan hona **Hasiera** eta hautatu **Lortu datuak**. Errepikatu 6-10 urratsak datu-iturburu honetarako entitate guztiak gehitu arte.

1. Sakatu **Gorde**. The **Datu iturriak** orrialdea irekitzen da datu-iturburu berria erakusten **Freskagarria** egoera.

### <a name="available-power-query-data-sources"></a>Eskuragarri Power Query datu-iturriak

Ikusi [Power Query konektorearen erreferentzia](/power-query/connectors/) Customer Insights-era datuak inportatzeko erabil ditzakezun konektoreen zerrendarako.

Konektoreak kontrol-marka duten **Bezeroei buruzko informazioa (Datu-fluxuak)** zutabea erabilgarri dago oinarrituta datu-iturri berriak sortzeko Power Query. Berrikusi konektore zehatz baten dokumentazioa bere aurrebaldintzei buruz gehiago jakiteko, [kontsultaren mugak](/power-query/power-query-online-limits), eta beste xehetasun batzuk.

## <a name="add-data-from-on-premises-data-sources"></a>Gehitu datuak lokal datu iturrietatik

Lokal datu-iturburuetako datuak barneratzea onartzen da Microsoft Power Platform datu-fluxuak (PPDF). Customer Insights-en datu-fluxuak gaitu ditzakezu [emanez Microsoft Dataverse ingurunearen URLa](create-environment.md) ingurunea ezartzerakoan.

A elkartu ondoren sortzen diren datu-iturriak Dataverse Customer Insights erabilera duen ingurunea [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz. Datu fluxuek konektibitate lokala onartzen dute datuetarako atebidea erabiliz. Aurretik zeuden datu-iturriak kendu eta birsor ditzakezu Dataverse ingurunea lotzen zen [lokal datu-pasabideak erabiliz](/data-integration/gateway/service-gateway-app).

Dagoen batetik datozen atebideak Power BI edo Power Apps ingurunea ikusgai egongo da eta Customer Insights-en berrerabili dezakezu. Datu iturrien orriak estekara erakusten du Microsoft Power Platform lokal datu atebideak ikusi eta konfiguratzeko ingurunea.

> [!IMPORTANT]
> Ziurtatu atebideak azken bertsiora eguneratuta daudela. Eguneratze bat instalatu eta atebide bat birkonfigura dezakezu atebidearen pantailan agertzen den gonbita batetik zuzenean edo [deskargatu azken bertsioa](https://powerapps.microsoft.com/downloads/). Ez baduzu azken atebidearen bertsioa erabiltzen, datu-fluxua freskatzeak huts egingo du errore-mezuekin **Gako-hitza ez da onartzen: konfigurazio-propietateak. Parametroaren izena: gako-hitza**.

## <a name="edit-power-query-data-sources"></a>Editatu Power Query datu-iturriak

> [!NOTE]
> Agian ez da posible aplikazioaren prozesuetako batean erabiltzen ari diren datu iturrietan aldaketak egitea (*segmentazio*, *bat-etortzea*, edo *konbinatu*, adibidez).
>
> urtean **Ezarpenak** orrialdean, prozesu aktibo bakoitzaren aurrerapenaren jarraipena egin dezakezu. Prozesua amaitutakoan, gailura itzuli dezakezu **Datu iturriak** orria eta egin zure aldaketak.

1. Joan **Datuak** > **Datu-iturburuak**.

1. Eguneratu nahi duzun datu-iturburu-aren ondoan, hautatu **Editatu**.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

1. Aplikatu zure aldaketak eta eraldaketak **Power Query - Editatu kontsultak** elkarrizketa-koadroan azaltzen den moduan [Sortu datu-iturburu berri bat](#create-a-new-data-source) atala.

1. Hautatu **Gorde** urtean Power Query aldaketak amaitu ondoren, aldaketak gordetzeko.
