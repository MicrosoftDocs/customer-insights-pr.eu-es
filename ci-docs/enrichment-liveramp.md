---
title: Aberastu bezeroen profilak LiveRamp-eko identitate-datuekin (aurrebista)
description: Aberastu bezeroen profilak LiveRamp datuekin.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 49bf558209ca91ab9d8db945862a57adccee1f6b
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196333"
---
# <a name="enrich-customer-profiles-with-identity-data-from-liveramp-preview"></a>Aberastu bezeroen profilak LiveRamp-eko identitate-datuekin (aurrebista)

LiveRamp-ek lineaz kanpoko identitatearen ebazpen determinista eta bezeroen datuen finkapena eskaintzen du. Zure bezeroen datuetan identifikatzaile pertsonalak mapa ditzakezu AbiliTec identitate grafikoarekin eta AbiliTec IDak jaso. Orduan ID hauek erabil ditzakezu zure bezeroen datuak hobeto bateratzeko.

## <a name="supported-countriesregions"></a>Lagundutako herrialde / eskualdeak

Une honetan, bezeroen profilak LiveRamp datuekin aberastea onartzen dugu Estatu Batuetan soilik.

## <a name="prerequisites"></a>Aurrebaldintzak

- LiveRamp harpidetza aktiboa. Harpidetza bat lortzeko, jarri harremanetan LiveRamp kontuko taldearekin edo hona [dynamics@liveramp.com](mailto:dynamics@liveramp.com) informazio gehiagorako.

- AbiliTec harpidetza aktibo bat bezeroaren IDa eta sekretua APIra sartzeko. Informazio gehiagorako, ikus [AbiliTec API Developer Hub](https://developers.liveramp.com/abilitec-api/).

- LiveRamp bat [konexioa](connections.md) da [konfiguratuta](#configure-the-connection-for-liveramp) administratzaile batek.

## <a name="configure-the-connection-for-liveramp"></a>Konfiguratu LiveRamp-erako konexioa

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta LiveRamp bezero ID eta sekretu aktibo bat izan.

1. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean, edo joan hona **Admin** > **Konexioak** eta hautatu **Konfiguratu** LiveRamp fitxan.

   :::image type="content" source="media/liveramp-connection.png" alt-text="LiveRamp AbiliTec zerbitzurako konexioa konfiguratzeko konfigurazio-panela.":::

1. Sartu konexiorako izen bat eta baliozko LiveRamp bezero ID bat eta sekretu bat.

1. Berrikusi eta eman zure baimena [Datuen pribatutasuna eta betetzea](#data-privacy-and-compliance) hautatuz **Ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

### <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights LiveRamp-era datuak transmititzeko, datuen transferentzia onartzen duzu betetze-mugatik kanpo Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina LiveRamp-ek izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeko ardura zara. Informazio gehiagorako, berrikusi [Microsoft Pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732). Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Identitatea** LiveRamp fitxatik.

   :::image type="content" source="media/liveramp-tile.png" alt-text="Identitate-lauza aberastearen ikuspegi orokorraren orrian.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu LiveRamp-eko identitate-datuekin aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Definitu zure profil bateratuetako zein eremu mota erabili LiveRamp-eko identitate-datuak bat etortzeko. Gutxienez eremuetako bat **Izena eta helbidea**, **elektronikoa**, edo **Mugikorra** beharrezkoa da. Bat-etortzeen zehaztasun handiagoa lortzeko, gehitu beste eremu batzuk. Hautatu **Hurrengoa**.

1. Mapeatu zure eremuak LiveRamp-eko identifikazio-datuekin.

   :::image type="content" source="media/liveramp-data-mapping.png" alt-text="LiveRamp aberasteko datuak mapatzeko aukerak.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Eman a **Izena** aberasteko eta **Irteerako entitatearen izena**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

The **Alorka aberastutako bezero kopurua** eremu aberastu bakoitzaren estaldura sakontzea eskaintzen du.

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Erabili AbiliTec IDak bezeroen profilak pertsonan oinarritutako ikuspegi batean finkatzeko.
[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
