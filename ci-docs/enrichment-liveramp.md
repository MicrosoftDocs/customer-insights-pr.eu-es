---
title: LiveRamp identitate-datuak aberastea
description: Aberastu bezeroen profilak LiveRamp datuekin.
ms.date: 03/02/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 0727818f6df565d9a031966a68d521ae7167e484
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642090"
---
# <a name="enrich-customer-profiles-with-identity-data-from-liveramp-preview"></a>Aberastu bezeroen profilak LiveRamp-eko identitate-datuekin (aurrebista) 

LiveRamp-ek lineaz kanpoko identitatearen ebazpen deterministikoa eta bezeroen datuen finkapena eskaintzen du. Zure bezeroen datuetan identifikatzaile pertsonalak mapa ditzakezu AbiliTec identitate grafikoarekin eta AbiliTec IDak jaso. Orduan ID hauek erabil ditzakezu zure bezeroen datuak hobeto bateratzeko. 

## <a name="prerequisites"></a>Aurrebaldintzak 

Aberastea konfiguratzeko, aurrebaldintza hauek bete behar dira: 

- LiveRamp harpidetza aktiboa duzu. Harpidetza bat lortzeko, jarri harremanetan LiveRamp kontuko taldearekin edo hona [dynamics@liveramp.com](mailto:dynamics@liveramp.com) informazio gehiagorako.   

- AbiliTec harpidetza aktibo bat bezeroaren IDa eta sekretua APIra sartzeko. Informazio gehiagorako, ikus [AbiliTec API Developer Hub](https://developers.liveramp.com/abilitec-api/). 

## <a name="supported-countriesregions"></a>Lagundutako herrialde / eskualdeak 

Gaur egun, bezeroen profilak LiveRamp datuekin aberastea onartzen dugu Estatu Batuetan soilik. 

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea 

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa. 

1. Hautatu **Aberastu nire datuak** gainean **Identitatea** teila. 

   :::image type="content" source="media/liveramp-tile.png" alt-text="Identitate-lauza aberastearen ikuspegi orokorraren orrian.":::

1. Hautatu goitibeherako zerrendako [konexio](connections.md) bat. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, konexio bat sor dezakezu hautatuta **Gehitu konexioa**. Aukeratu **LiveRamp** goitibeherako zerrendatik. 

1. Hautatu **Hurrengoa** eta aukeratu **Bezeroaren datu multzoa** LiveRamp-eko identitate-datuekin aberastu nahi duzu. Hautatu dezakezu *Bezeroa* entitatea zure bezero-profil guztiak aberasteko edo hautatzeko a *segmentua* entitateak segmentu horretan jasotako bezero-profilak soilik aberasteko. 

1. Hautatu **Hurrengoa** eta definitu zure profil bateratuetako zein eremu mota erabili behar diren LiveRamp-en bat datozen identitate-datuak bilatzeko. Gutxienez eremuetako bat **Izena eta helbidea**, **·**, edo **Posta elektronikoa** beharrezkoa da. 

   > [!TIP]
   > Zenbat eta gako-identifikatzaile eta eremu gehiago mapatu, orduan eta aukera handiagoa izango da bat-etortze-tasa handiagoa izateko 

1. Mapeatu zure bateratuko eremuak *Bezeroa* LiveRamp-en AbiliTec ID grafikoarekin lotzeko erabiliko den entitatea. 

   :::image type="content" source="media/liveramp-data-mapping.png" alt-text="LiveRamp aberasteko datuak mapatzeko aukerak.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko. 

1. Eman a **Izena** aberasteko eta **Irteerako entitatea**. 

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren. 

## <a name="configure-the-connection-for-liveramp"></a>Konfiguratu LiveRamp-erako konexioa 

Administratzailea izan behar duzu [konexioak konfiguratu](connections.md). Hautatu **Gehitu konexioa** aberastea konfiguratzean edo joan **Admin** > **Konexioak** eta hautatu **Konfiguratu** gainean **LiveRamp** teila. 

:::image type="content" source="media/liveramp-connection.png" alt-text="LiveRamp AbiliTec zerbitzurako konexioa konfiguratzeko konfigurazio-panela.":::

1. Izan ere **Bistaratzeko izena**, idatzi konexioaren izena. 

1. Eman baliozko LiveRamp bezero ID bat eta sekretu bat. 

1. Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia. 

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko. 

1. Konexioa osatzeko, hautatu **Gorde**. 

## <a name="enrichment-results"></a>Aberastearen emaitzak 

Aberaste-prozesua hasteko, hautatu Exekutatu komando-barran. Era berean, sistemari aberastea automatikoki exekutatzen utzi diezaiokezu a [programatutako freskagarritasuna](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren araberakoa da. 

Aberaste-prozesua amaitu ondoren, aberastu berri diren bezero-profilen datuak berrikusi ditzakezu azpian **Nire aberastasunak**. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu. 

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikuspegi aberastua** datuak. 

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Erabili AbiliTec IDak bezeroen profilak pertsonan oinarritutako ikuspegi batean finkatzeko. 
[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea 

Gaitzen duzunean Dynamics 365 Customer Insights LiveRamp-era datuak transmititzeko, datuak betetze-mugetatik kanpo transferitzea onartzen duzu Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina LiveRamp-ek izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeko ardura zara. Informazio gehiagorako, berrikusi [Microsoft Pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732). Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko. 


[!INCLUDE [footer-include](includes/footer-banner.md)]
