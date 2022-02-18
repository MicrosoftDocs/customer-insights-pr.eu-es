---
title: Hartu datuak a bidez Power Query konektorea (bideoa dauka)
description: -n oinarritutako datu-iturburuetarako konektoreak Power Query.
ms.date: 12/06/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.openlocfilehash: 727cb9a4d754b6dbd74d6ecab1b183d41f713d8f
ms.sourcegitcommit: aadee829eff111c95eb30c0a97a68dcc87994acf
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092057"
---
# <a name="connect-to-a-power-query-data-source"></a>Konektatu a Power Query datu-iturburu

Power Query datuak irensteko konektore multzo zabala eskaintzen du. Konektore hauetako gehienek onartzen dute Dynamics 365 Customer Insights. 

Oinarritutako datu-iturriak gehitzea Power Query konektoreak, oro har, atal honetan azaltzen diren urratsak jarraitzen ditu. Hala ere, erabiltzen duzun konektorearen arabera, informazio desberdina behar da. Gehiago jakiteko, ikusi konektore indibidualei buruzko dokumentazioa [Power Query konektorearen erreferentzia](/power-query/connectors/).

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWN6EK]

## <a name="create-a-new-data-source"></a>Sortu datu-iturburua

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Aukeratu **Microsoft Power Query**.

1. Eman **Izena** datu-iturburu-erako, eta hautatu **Hurrengoa** datu-iturburu sortzeko.

1. Hautatu bat [erabilgarri dauden konektoreetatik](#available-power-query-data-sources). Adibide honetan, hautatzen dugu **Testua/CSV** konektorea.

1. Idatzi beharrezko datuak **Konexio ezarpenak** hautatutako lokailurako eta hautatu **Hurrengoa** datuen aurrebista ikusteko.

1. Hautatu **Transformatu datuak**. Urrats honetan entitateak gehituko dituzu zure datu-iturburu-era. Entitateak datu multzoak dira. Datu-multzo ugari biltzen dituen datu-basea baduzu, datu-multzo bakoitza bere entitatea da.

1. The **Power Query - Editatu kontsultak** elkarrizketa-koadroak datuak berrikusi eta findu ditzakezu. Aukeratutako datu-iturburu sistemetan identifikatutako sistemak ezkerreko panelean agertzen dira.

   > [!div class="mx-imgBorder"]
   > ![Editatu eskaera eztabaida.](media/data-manager-configure-edit-queries.png "Editatu eskaera eztabaida")

1. Zure datuak ere eralda ditzakezu. Hautatu entitate bat editatzeko edo eraldatzeko. Erabili aukerak Power Query eraldaketak aplikatzeko leihoa. Eraldaketa bakoitza azpian agertzen da **Urrats aplikatuak**. Power Query aurrez eraikitako eraldaketa aukera ugari eskaintzen ditu. Informazio gehiagorako, ikus [Power Query Eraldaketak](/power-query/power-query-what-is-power-query#transformations).

   Ondorengo eraldaketak erabiltzea gomendatzen dugu:

   - CSV fitxategi bateko datuak irensten badituzu, lehenengo ilaran maiz goiburuak agertzen dira. Joan **Eraldatu** eta hautatu **Erabili lehen errenkada goiburu gisa**.
   - Ziurtatu datu mota behar bezala ezarrita dagoela. Adibidez, data eremuetarako, hautatu data mota bat.

1. Zure datu-iturburu-i entitate gehigarriak gehitzeko **Editatu kontsultak** elkarrizketa-koadroa, joan hona **Hasiera** eta hautatu **Lortu datuak**.

1. Hautatu **Gorde** behealdean Power Query eraldaketak gordetzeko leihoa. Gorde ondoren, zure datu-iturburu aktibatuta aurkituko duzu **Datu-iturburuak** > **Datu iturriak**.

1. Gainean **Datu iturriak** orrialdean, datu-iturburu berria dagoela ohartuko zara **Freskagarria** egoera.

## <a name="available-power-query-data-sources"></a>Eskuragarri Power Query datu-iturriak

Ikusi [Power Query konektorearen erreferentzia](/power-query/connectors/) Customer Insights-era datuak inportatzeko erabil ditzakezun konektoreen zerrendarako. 

Konektoreak kontrol-marka duten **Bezeroei buruzko informazioa (Datu-fluxuak)** zutabea erabilgarri dago datu-iturri berriak sortzeko Power Query. Berrikusi konektore zehatz baten dokumentazioa, bere aurretiazko baldintzak, mugak eta bestelako xehetasunak ezagutzeko.

## <a name="edit-power-query-data-sources"></a>Editatu Power Query datu-iturriak

> [!NOTE]
> Agian ez da posible aplikazioaren prozesuetako batean erabiltzen ari diren datu iturrietan aldaketak egitea (*segmentazio*, *bat-etortzea*, edo *konbinatu*, adibidez). 
>
> urtean **Ezarpenak** orrialdean, prozesu aktibo bakoitzaren aurrerapenaren jarraipena egin dezakezu. Prozesua amaitutakoan, gailura itzuli dezakezu **Datu iturriak** orria eta egin zure aldaketak.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Aukeratu elipsi bertikala aldatu eta hautatu nahi duzun datu-iturburu ondoan **Editatu** goitibeherako menutik.

   > [!div class="mx-imgBorder"]
   > ![Editatu aukera.](media/edit-option-data-sources.png "Editatu aukera")

   [!INCLUDE [progress-details-include](../includes/progress-details-pane.md)]
   
3. Aplikatu zure aldaketak eta eraldaketak **Power Query - Editatu kontsultak** elkarrizketa-koadroan azaltzen den moduan [Sortu datu-iturburu berri bat](#create-a-new-data-source) atala.

4. Hautatu **Gorde** urtean Power Query aldaketak amaitu ondoren, aldaketak gordetzeko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
