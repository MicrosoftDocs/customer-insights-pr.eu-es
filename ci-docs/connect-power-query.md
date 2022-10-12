---
title: Konektatu a Power Query datu-iturburu (bideoa dauka)
description: Hartu datuak a bidez Power Query konektorea (bideoa dauka).
ms.date: 09/29/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: how-to
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-data-sources
- ci-create-data-source
- customerInsights
ms.openlocfilehash: 4cc7e57dfb0f8d050e91adc441c24e849882f5d8
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9609861"
---
# <a name="connect-to-a-power-query-data-source"></a>Konektatu a Power Query datu-iturburu

Power Query datuak irensteko konektore multzo zabala eskaintzen du. Konektore hauetako gehienek onartzen dute Dynamics 365 Customer Insights.

Oinarritutako datu-iturriak gehitzea Power Query konektoreak, oro har, atal honetan azaltzen diren urratsak jarraitzen ditu. Hala ere, erabiltzen duzun konektorearen arabera, informazio desberdina behar da. Gehiago jakiteko, ikusi konektore indibidualei buruzko dokumentazioa [Power Query konektorearen erreferentzia](/power-query/connectors/).

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWN6EK]

## <a name="create-a-new-data-source"></a>Sortu datu-iturburua

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Aukeratu **Microsoft Power Query**.

1. Eman a **Izena** eta aukerakoa **Deskribapena** datu-iturburu-erako, eta hautatu **Hurrengoa**.

1. Hautatu bat [erabilgarri dauden konektoreetatik](#available-power-query-data-sources). Adibide honetan, hautatzen dugu **Testua/CSV** konektorea.

1. Idatzi beharrezko datuak **Konexio ezarpenak** hautatutako lokailurako eta hautatu **Hurrengoa** datuen aurrebista ikusteko.

1. Hautatu **Transformatu datuak**.

1. Berrikusi eta hobetu zure datuak **Power Query - Kontsultak editatu** orrialdea. Aukeratutako datu-iturburu sistemetan identifikatutako sistemak ezkerreko panelean agertzen dira.

   :::image type="content" source="media/data-manager-configure-edit-queries.png" alt-text="Editatu eskaera eztabaida":::

1. Eraldatu zure datuak. Hautatu entitate bat editatzeko edo eraldatzeko. Erabili aukerak Power Query eraldaketak aplikatzeko leihoa. Transformazio bakoitza azpian dago zerrendatuta **Aplikaturiko urratsak**. Power Query ugari eskaintzen ditu [aurrez eraikitako eraldaketa](/power-query/power-query-what-is-power-query#transformations) aukerak.

   > [!IMPORTANT]
   > Ondorengo eraldaketak erabiltzea gomendatzen dugu:
   >
   > - CSV fitxategi bateko datuak irensten badituzu, lehenengo ilaran maiz goiburuak agertzen dira. Joan **Eraldatu** eta hautatu **Erabili lehen errenkada goiburu gisa**.
   > - Ziurtatu datu-mota egoki ezarrita dagoela eta datuekin bat datorrela. Adibidez, data eremuetarako, hautatu data mota bat.

1. Zure datu-iturburu-i entitate gehigarriak gehitzeko **Editatu kontsultak** elkarrizketa-koadroa, joan hona **Hasiera** eta hautatu **Lortu datuak**. Errepikatu 5-10 urratsak datu-iturburu honetarako entitate guztiak gehitu arte. Datu-multzo ugari biltzen dituen datu-basea baduzu, datu-multzo bakoitza bere entitatea da.

1. Sakatu **Gorde**. The **Datu-iturriak** orrialdea irekitzen da datu-iturburu berria erakusten **Freskagarria** egoera.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

Datuak kargatzeak denbora behar dezake. Freskatu arrakastatsu baten ondoren, irentsitako datuak berrikusi daitezke [**Entitateak**](entities.md) orrialdea.

> [!CAUTION]
>
> - Oinarritutako datu-iturburu bat Power Query bat sortzen du [datu-fluxua sartu Dataverse](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365). Ez aldatu datu-fluxu baten izena fitxategian Power Platform Customer Insights-en erabiltzen den administrazio-zentroa. Datu-fluxu baten izena aldatzeak arazoak sortzen ditu Customer Insights datu-iturburu eta erreferentziekin.Dataverse datu-fluxua.
> - Aldibereko ebaluazioak egiteko Power Query Customer Insights-en datu iturriek gauza bera dute [freskatu mugak PowerBI.com-en Dataflows bezalakoak](/power-query/power-query-online-limits#refresh-limits). Datuak freskatzeak huts egiten badu ebaluazio-mugara iritsi delako, datu-fluxu bakoitzaren freskatze-egutegia doitzea gomendatzen dugu datu-iturriak aldi berean prozesatzen ez direla ziurtatzeko.

### <a name="available-power-query-data-sources"></a>Eskuragarri Power Query datu-iturriak

Ikusi [Power Query konektorearen erreferentzia](/power-query/connectors/) Customer Insights-era datuak inportatzeko erabil ditzakezun konektoreen zerrendarako.

Konektoreak kontrol-marka duten **Bezeroei buruzko informazioa (Datu-fluxuak)** zutabea erabilgarri dago oinarrituta datu-iturri berriak sortzeko Power Query. Berrikusi konektore zehatz baten dokumentazioa bere aurrebaldintzei buruz gehiago jakiteko.[kontsultaren mugak](/power-query/power-query-online-limits), eta beste xehetasun batzuk.

## <a name="add-data-from-on-premises-data-sources"></a>Gehitu datuak lokal datu iturrietatik

Lokal datu-iturburuetako datuak barneratzea onartzen da Microsoft Power Platform datu-fluxuak (PPDF). Customer Insights-en datu-fluxuak gaitu ditzakezu [du eskainiz Microsoft Dataverse ingurunearen URLa](create-environment.md) ingurunea ezartzerakoan.

A elkartu ondoren sortzen diren datu-iturriak Dataverse Customer Insights erabilera duen ingurunea [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz. Datu fluxuek konektibitate lokala onartzen dute datuetarako atebidea erabiliz. Aurretik zeuden datu-iturriak kendu eta birsor ditzakezu Dataverse ingurunea lotzen zen [lokal datu-atebideak erabiliz](/data-integration/gateway/service-gateway-app).

Dagoeneko datu-paseak Power BI edo Power Apps ingurunea ikusgai egongo da eta Customer Insights-en berrerabili ahal izango dituzu datu-pasabidea eta Customer Insights ingurunea Azure eskualde berean badaude. Datu iturrien orriak estekara erakusten du Microsoft Power Platform lokal datu atebideak ikusi eta konfiguratzeko ingurunea.

> [!IMPORTANT]
> Ziurtatu atebideak azken bertsiora eguneratuta daudela. Eguneratze bat instalatu eta atebide bat birkonfigura dezakezu atebidearen pantailan agertzen den gonbita batetik zuzenean edo [deskargatu azken bertsioa](https://powerapps.microsoft.com/downloads/). Ez baduzu azken atebidearen bertsioa erabiltzen, datu-fluxua freskatzeak huts egingo du errore-mezuekin **Gako-hitza ez da onartzen: konfigurazio-propietateak. Parametroaren izena: gako-hitza**.
>
> Customer Insights-en lokal datu-atebideekin akatsak konfigurazio-arazoek eragiten dituzte sarritan. Datu-atebideei buruzko arazoak konpontzeari buruzko informazio gehiago lortzeko, ikus [Konpondu lokal datu-atebidea](/data-integration/gateway/service-gateway-tshoot).

## <a name="edit-power-query-data-sources"></a>Editatu Power Query datu-iturriak

> [!NOTE]
> Baliteke aplikazioaren prozesuren batean erabiltzen ari diren datu-iturburuetan aldaketarik egitea (segmentazioa edo datuen bateratzea adibidez).
>
> urtean **Ezarpenak** orrialdean, prozesu aktibo bakoitzaren aurrerapenaren jarraipena egin dezakezu. Prozesua amaitutakoan, gailura itzuli dezakezu **Datu iturriak** orria eta egin zure aldaketak.

1. Joan **Datuak** > **Datu-iturburuak**.

1. Eguneratu nahi duzun datu-iturburu-aren ondoan, hautatu **Editatu**.

1. Aplikatu zure aldaketak eta eraldaketak **Power Query - Kontsultak editatu** elkarrizketa-koadroan azaltzen den moduan [Sortu datu-iturburu berri bat](#create-a-new-data-source) atala.

1. Hautatu **Gorde** zure aldaketak aplikatzeko eta itzultzeko **Datu-iturriak** orrialdea.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="common-reasons-for-ingestion-errors-or-corrupt-data"></a>Irenste-akatsen edo datuak hondatzearen ohiko arrazoiak

### <a name="data-type-does-not-match-data"></a>Datu mota ez dator bat datuekin

Datu-mota desegokia ohikoena data-eremu bat data-formatu egokian ezartzen ez denean gertatzen da.

Datuak jatorrian finkatu eta berriro sartu. Edo konpondu Customer Insights-en eraldaketa. Eraldaketa konpontzeko:

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hondatutako datuekin datu-iturburu-ren ondoan, hautatu **Editatu**.

1. Hautatu **Hurrengoa**.

1. Hautatu kontsulta bakoitza eta bilatu okerrak diren "Aplikaturiko Urrats" barruan aplikatutako eraldaketak edo data-formatu batekin eraldatu ez diren data-zutabeak.

   :::image type="content" source="media/PQ_corruped_date.png" alt-text="Power Query- Editatu data-formatu okerra erakutsiz":::

1. Aldatu datu-mota datuekin behar bezala etortzeko.

1. Sakatu **Gorde**. datu-iturburu hori freskatu da.

## <a name="troubleshoot-ppdf-power-query-based-data-source-refresh-issues"></a>Arazoak konpondu PPDF Power Query -oinarritutako datu-iturburu freskatze arazoak

Datuak zaharkituta badaude edo datu-iturburu freskatu ondoren erroreak jasotzen badituzu, egin urrats hauek:

1. Joan hona: [Power Platform](https://make.powerapps.com)

1. Hautatu **Ingurumena** zure Customer Insights instantziarako.

1. Nabigatu **Datu-fluxuak**.

1. Customer Insights-en datu-iturburu-ri dagokion datu-fluxurako, hautatu elipsi bertikala (&vellip;) eta gero hautatu **Erakutsi freskatze-historia**.

1. bada **Egoera** datu-fluxuarena da **Arrakasta**,-ren jabetza Power Query -oinarritutako datu-iturburu agian aldatu izana:

   1. Berrikusi freskatze-programazioa freskatze-historiatik.
   1. Ezarri jabe berriaren ordutegia eta gorde ezarpenak.

1. bada **Egoera** datu-fluxuarena da **Huts egin du**:

   1. Deskargatu freskatze historiaren fitxategia.
   1. Berrikusi deskargatutako fitxategia hutsegitearen arrazoia ikusteko.
   1. Errorea konpondu ezin bada, hautatu **?** laguntza-txartel bat irekitzeko. Sartu deskargatutako freskatze historiaren fitxategia.


[!INCLUDE [footer-include](includes/footer-banner.md)]
