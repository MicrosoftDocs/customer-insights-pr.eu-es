---
title: Aberastu bezeroen profilak datu demografikoekin Experian (aurrebista)
description: -Ri buruzko informazio orokorra Experian hirugarrenen aberastea.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 876853ab42e8c08ad1abacb8d8a205c0aadabcf7
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195921"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a>Aberastu bezeroen profilak datu demografikoekin Experian (aurrebista)

Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta merkaturatzeko zerbitzuetan. Batera Experian Datuak aberasteko zerbitzuak, zure bezeroen ezagutza sakonagoa eraiki dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.

## <a name="supported-countriesregions"></a>Lagundutako herrialde / eskualdeak

Gaur egun, Estatu Batuetan bezeroen profil aberasgarriak onartzen ditugu.

## <a name="prerequisites"></a>Aurrebaldintzak

- Aktibo bat Experian harpidetza. Harpidetza lortzeko, [harremanetarako Experian](https://www.experian.com/marketing-services/contact) zuzenean. [Lortu informazio gehiago Experian datuen eraginari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).

- An Experian [konexioa](connections.md) da [konfiguratuta](#configure-the-connection-for-experian) administratzaile batek.

- Experian SSH gaitutako Secure Transport (ST) konturako erabiltzailearen IDa, alderdiaren IDa eta eredu-zenbakia Experian zuretzat sortua.

## <a name="configure-the-connection-for-experian"></a>Konfiguratu konexio-funtzioak Experian-en

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta eduki bat Experian Erabiltzailearen IDa, alderdiaren IDa eta eredu-zenbakia.

1. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean, edo joan hona **Admin** > **Konexioak** eta hautatu **Konfiguratu** gainean Experian teila.

   :::image type="content" source="media/enrichment-Experian-connection.png" alt-text="Experian konexioaren konfigurazio-panela.":::

1. Sartu konexiorako izen bat eta baliozko erabiltzailearen IDa, alderdiaren IDa eta eredu-zenbakia Experian Garraio Seguru kontua.

1. Berrikusi eta eman zure baimena [Datuen pribatutasuna eta betetzea](#data-privacy-and-compliance) hautatuz **Ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

### <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko Experian, datuak betetze mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz Experian izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732). Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Demografia** tik Experian teila.

   :::image type="content" source="media/experian-tile.png" alt-text="Experian lauza aberastearen ikuspegi orokorra orrialdean.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu datu demografikoekin aberastu nahi duzun profila edo segmentua Experian. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

    :::image type="content" source="media/enrichment-Experian-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Definitu zure profil bateratuetako zein eremu mota erabili behar dituzun datu demografikoak bat etortzeko Experian. Eremuetako bat gutxienez **Izena eta helbidea**, **Mugikorra**, edo **Posta elektronikoa** beharrezkoa da. Bat-etortzeen zehaztasun handiagoa lortzeko, gehitu beste eremu batzuk. Hautatu **Hurrengoa**.

1. Mapeatu zure eremuak datu demografikoekin Experian.

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Eman a **Izena** aberasteko eta **Irteerako entitatearen izena**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

The **Alorka aberastutako bezero kopurua** eremu aberastu bakoitzaren estaldura sakontzea eskaintzen du.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
