---
title: Kudeatu profil ezezagunak Customer Insights-ekin
description: Lanean sortu eta kudeatzen diren bezero-profil ezezagunekin lan egin Dynamics 365 Customer Insights.
ms.date: 09/14/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: andtapia
ms.author: andreatapia
manager: shellyha
ms.openlocfilehash: 0e12f64a22b93d117009fb8aee76d02a7583e699
ms.sourcegitcommit: 24627d53dcdf607baaab1cc3c299a3584c386173
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/15/2022
ms.locfileid: "9776806"
---
# <a name="manage-unknown-profiles-with-customer-insights"></a>Kudeatu profil ezezagunak Customer Insights-ekin

Interneteko erabiltzaileak sarritan identifikatu gabekoak edo anonimoak dira sarean. Bezero leialenak ere "ezezagunak" direla ager daitezke gailu ezberdinetan saioa hasi ez badute. Marka askorentzat, erabiltzaile ezagunak edo autentifikatuak gutxiengoak dira pertsonalizazioaren inguruan bezeroen itxaropenak gero eta handiagoak diren arren. Hirugarrenen cookieen etorkizuna zalantzan jarrita, erabiltzaileen hobespenak lehenen datuetan oinarrituta kudeatzea funtsezkoa da esperientzia pertsonalizatuak lortzeko.

Pertsonalizazio gogoangarria zure bezeroa ezagutzen duzunaren araberakoa da eta Customer Insights-ek hori egiten laguntzen dizu zure bezero guztien jarraipena eginez.  Ez duzu bezero-bidaia-aren hasieran jasotako datuen erabilera mugatu edo eten beharrik. Customer Insights-ek zure datuak ekar ditzakezu erabiltzaile ezezagunentzako bezero-profila sortzeko. Ondoren, profil hori erabil dezakezu ekintza gehiago egiteko, harremanetarako informazioa falta izan arren. Inportatu lehenen datuak, hala nola web, mugikor edo CRM sistemetatik, Customer Insights-era, bezeroen profilak etengabe aberasteko. Interakzio gehiago bateratzen dituzun heinean, [piztu *ezezaguna* bezero bat sartu *ezagunak* bezeroa](unknown-to-known.md).

## <a name="sample-scenario"></a>Eszenario lagina

Demagun erabiltzaile batek bere gailu mugikorra erabiltzen duela zure merkataritza elektronikoko gunea arakatzeko. Webguneak "mobile_guest123" bisitaria esleitzen du identifikatzaile esklusibo gisa eta zure lineako jardueran oinarritutako jokabide-jarduerak biltzen hasten zara. Adibidez, zein orrialde bisitatu dituzten, zenbat denbora eman duten orrialde horietan edo zein esteka egin duten klik. Ez dakizu haien izena edo helbide elektronikoa, baina datu hauek markei erabiltzaile zehatz honi buruzko informazio esanguratsuak eskaintzen lagun diezaiekete. Era berean, informazio horiek erabil ditzakezu erabiltzaileak gunea bisitatzen duen hurrengo aldian. Kontsultatu "mobile_guest123"-ren bezeroen estatistikak erabiltzailearen segmentu-zerrenda berreskuratzeko, hala nola, "organikoa", "mugikorretarako eskaerak egiteko bezeroak", "balio handiko bezeroak", etab., edo berreskuratu profila web-esperientzia pertsonalizatuak sortzeko. Datuak edozein aktibazio-sistemara ere esporta ditzakezu gauza bera egiteko.

## <a name="prerequisites"></a>Aurrebaldintzak

- Hartu lehenen datuak Customer Insights-en
- Entitate bakoitzak gako nagusi gisa ezartzen den ID bakarra du
- Pertsonalizaziorako gako nagusi bat duen entitate bakoitza bateratu egiten da
- Zure webguneko edukiak kudeatzeko sistemak APIak erabil ditzake (Weba pertsonalizatzeko Customer Insights-ekin zuzeneko komunikazioan oinarrituta)

Hurrengo taulak balio handiko web-gertaerak nola atzeman daitezkeen adibide sinplifikatu bat erakusten du.

|Gertaeraren ID|Gertaera-ordu-zigilua|Erabiltzaile ID|Lehen mailako gakoa|Gertaeraren izena|
|--|--|--|--|--|
|1|09-15-2022 9:00:00|abc123|CookieID1|Produktuen ikuspegia|
|2|09-18-2022 10:05:00|abc123|CookieID1|Produktuen ikuspegia|
|3|09-18-2022 10:10:00|abc123|CookieID1|Gehitu saskian|
|4|09-21-2022 09:05:00|abc123|CookieID1|Produktuen ikuspegia|

## <a name="data-ingestion"></a>Datu-horniketa

Datuak sartzeko dauden aukerei buruzko informazio gehiago lortzeko, ikus [Datu iturrien ikuspegi orokorra](data-sources.md).

## <a name="data-unification"></a>Datuak bateratzea

Bezeroen profilak bateratzeari buruzko informazio gehiago lortzeko, ikus [Datuen bateratzearen ikuspegi orokorra](data-unification.md).

## <a name="get-insights"></a>Lortu xehetasunak

[Aberastu](enrichment-hub.md) zure datuak, eraiki [neurriak](measures.md), eta sortu [segmentuak](segments.md) gehiago aktibatzeko.

Esaterako, produktu-orrialde berdinak arakatu baina ordainketa amaitu ez duten erabiltzaile ezezagunen segmentuak sor ditzakezu.

## <a name="activation"></a>Aktibazioa

Customer Insights-en dituzun datuak eta zure estatistikak lanean hasteko prest daudenez, Customer Insights erabil dezakezu pertsonalizatzeko:

1. Erabili [OData APIa](apis.md) segmentu-kidetasun edo bezero-profil bat berreskuratzeko Adibide gehiago lortzeko, ikus [Customer Insights APIetarako OData kontsultaren adibideak](odata-examples.md).

1. [Esportatu](export-destinations.md) zure datuak zure aktibazio sistemetara.

Adibidea: erabiltzaile ezezagun batek hainbat aldiz bisitatzen du webgune bat eta hainbat larruzko oinetako modeloren produktuen orriak bisitatzen ditu. Customer Insights-en eskuragarri dauden datu horiekin, erabiltzaile ezezaguna larruzko oinetakoetan interesa duten pertsonen segmentuan sar dezakezu. Erabili segmentu hau zure webgunearen pertsonalizazioaren berri emateko. Hurrengo bisitan, webguneak erabiltzaile ezezaguna ezagutzen du eta larruzko oinetakoetan %10eko kupoi bat eskain diezaioke.

[!INCLUDE [footer-include](includes/footer-banner.md)]
