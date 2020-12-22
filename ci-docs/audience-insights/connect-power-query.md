---
title: Sartu datuak Power Query konektore baten bidez
description: Konektoreak datu-iturburuetarako oinarrituz Power Query-n.
ms.date: 09/29/2020
ms.reviewer: adkuppa
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 8a170cc5b64b4b383501021232c83948e838a0e2
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404976"
---
# <a name="connect-to-a-power-query-data-source"></a>Konektatu Power Query datu-iturburu batera

Power Query-ek konektore multzo zabala eskaintzen du datuak irensteko. Konektore hauetako gehienek onartzen dute Dynamics 365 Customer Insights. Power Query konektoreetan oinarritutako datu iturriak gehitzeak hurrengo atalean azaldutako urratsak jarraitzen ditu. Hala ere, erabiltzen duzun konektorearen arabera, informazio desberdina behar da. Informazio gehiagorako, ikusi banakako konektoreei buruzko dokumentazioa [Power Query konektore erreferentzia](https://docs.microsoft.com/power-query/connectors/).

## <a name="create-a-new-data-source"></a>Sortu datu-iturburua

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Aukeratu **Inportatu datuak** metodoa eta hautatu **Hurrengoa**.

1. Eman **Izena** datu-iturburu-erako, eta hautatu **Hurrengoa** datu-iturburu sortzeko.

1. Hautatu bat [erabilgarri dauden konektoreetatik](#available-power-query-data-sources). Adibide honetarako, hautatu dugu **Testua/CSV** konektore.

1. Idatzi beharrezko datuak **Konexio ezarpenak** hautatutako lokailurako eta hautatu **Hurrengoa** datuen aurrebista ikusteko.

1. Hautatu **Transformatu datuak**. Urrats honetan entitateak gehituko dituzu zure datu-iturburu-era. Entitateak datu multzoak dira. Datu-multzo ugari biltzen dituen datu-basea baduzu, datu-multzo bakoitza bere entitatea da.

1. **Power Query - Editatu kontsultak** Elkarrizketa-koadroak datuak berrikusi eta hobetzeko aukera ematen du. Aukeratutako datu-iturburu sistemetan identifikatutako sistemak ezkerreko panelean agertzen dira.

   > [!div class="mx-imgBorder"]
   > ![Editatu eskaera eztabaida](media/data-manager-configure-edit-queries.png "Editatu eskaera eztabaida")

1. Zure datuak ere eralda ditzakezu. Hautatu entitate bat editatzeko edo eraldatzeko. Erabili Power Query leihoan dauden aukerak transformazioak aplikatzeko. Eraldaketa bakoitza azpian agertzen da **Urrats aplikatuak**. Power Query-ek aurrez eraikitako eraldaketa aukera ugari eskaintzen ditu. Informazio gehiagorako, ikusi [Power Query eraldaketak](https://docs.microsoft.com/power-query/power-query-what-is-power-query#transformations).

1. Entitate osagarriak gehi ditzakezu zure datu-iturburu hautatuta **Lortu datuak** herrian **Editatu zalantzak** elkarrizketa.

   Eraldaketa hauek oso gomendagarriak dira:

   - CSV fitxategi bateko datuak irensten badituzu, lehenengo ilaran maiz goiburuak agertzen dira. Joan **Transformatu mahaia** eta hautatu **Erabili goiburuak lehen ilara gisa**.
   - Ziurtatu datu mota behar bezala ezarrita dagoela.

1. Hautatu **Gorde** Power Query leihoaren azpian gordetzeko eraldaketak. Gorde ondoren, zure datu-iturburu aktibatuta aurkituko duzu **Datu-iturburuak** > **Datu iturriak**.

1. Gainean **Datu iturriak** orrialdean, datu-iturburu berria dagoela ohartuko zara **Freskagarria** egoera.

## <a name="available-power-query-data-sources"></a>Eskuragarri dauden Power Query datu iturriak

Ikusi [Power Query konektore erreferentzia](https://docs.microsoft.com/power-query/connectors/) datuak Customer Insights inportatzeko hauta ditzakezun konektoreen zerrenda eguneratua lortzeko. 

Konektoreak kontrol-markarekin **Customer Insights (datu-fluxuak)** zutabea eskuragarri dago Power Query oinarritutako datu iturri berriak sortzeko. Berrikusi konektore zehatz baten dokumentazioa, bere aurretiazko baldintzak, mugak eta bestelako xehetasunak ezagutzeko.

## <a name="edit-power-query-data-sources"></a>Editatu Power Query datu iturriak

> [!NOTE]
> Agian ez da posible aplikazioaren prozesuetako batean erabiltzen ari diren datu iturrietan aldaketak egitea (*segmentazio*, *bat-etortzea*, edo *konbinatu*, adibidez). 
>
> . Erabiliz **ezarpenak** orrialdea, prozesu aktibo bakoitzaren bilakaeraren jarraipena egin dezakezu. Prozesua amaitutakoan, gailura itzuli dezakezu **Datu iturriak** orria eta egin zure aldaketak.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Hautatu aldatu nahi duzun datu-iturburu ondoko elipsi bertikala **Editatu** goitibeherako menuan.

   > [!div class="mx-imgBorder"]
   > ![Editatu aukera](media/edit-option-data-sources.png "Editatu aukera")

3. Aplikatu aldaketak eta eraldaketak **Power Query - Editatu kontsultak** elkarrizketa - koadroan deskribatutako moduan [Sortu datu-iturburu berria](#create-a-new-data-source) atala.

4. Aukeratu **Gorde** Power Query-en aldaketak gordetzeko aldaketak egin ondoren.
