---
title: Hasi konpromiso estatistiken gaitasunarekin
description: Laguntza baliabideen ikuspegi orokorra azkar hasteko.
ms.reviewer: mhart
ms.author: jefhar
author: mochimochi016
ms.date: 10/01/2021
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: c435810e712bbbf69f8f1cfb582fc0a971566de6
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8225528"
---
# <a name="get-started-with-dynamics-365-customer-insights-engagement-insights-capability-public-preview"></a>Hasi Dynamics 365 Customer Insights elkarreragin xehetasunen gaitasuna (aurrebista publikoa)

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Elkarreragin xehetasunak, gaitasuna , bezeroen portaera zure webgunean biltzeko eta neurtzeko aukera ematen du. Ikuslegoaren ikuspegi gaitasunarekin integratzen da, denbora errealeko portaeraren analisi aberatsak bezeroaren profileko txostenekin batera ikusi ahal izateko. Artikulu honetako estekek zure ingurunea azkar konfiguratzen eta konfiguratzen lagunduko dizute.

## <a name="step-1-review-prerequisites"></a>1. urratsa: berrikusi aurrebaldintzak

Lehenik, Microsoft Azure Active Directory (AAD) erabiltzaile-kontu aktibo bat izan behar duzu. Ondoren, irakurri hurrengo artikuluak konpromisoen inguruko lan-eremua konfiguratu aurretik.

- Berrikusi eta onartu [Erabiltzeko baldintzak](terms-of-service.md) Microsoft-ekin.  
- Irakurri [Kudeatu cookieak eta erabiltzaileen baimena](user-consent-storage.md) artikulua. Ondoren, ebaluatu erabiltzailearen onarpenaren jakinarazpena eguneratu behar duzun. Aurretik "funtsezkoak ez" diren cookie-rik ez baduzu, ziurrenik zure webgunearen politika eguneratu beharko duzu.
- Berrikusi [glosarioa](glossary.md) funtsezko termino eta kontzeptuak azkar sartzeko.

## <a name="step-2-explore-engagement-insights"></a>2. Urratsa: arakatu konpromisoak

Hartzaileen xehetasunak ikusten dituzun lehen aldian, ezarpenak konfiguratu, gidalerroak berrikusi eta gaitasuna arakatu dezakezu.

1. Hasi saioa [parte-hartzearen xehetasunen gaitasunaren atarian](https://home.ci.ai.dynamics.com/app/engagement-insights) Microsoft AAD erabiltzailearen (eskolako edo laneko) kontuarekin.

1. Hautatu eskualdea eta egin klik koadroan mezu elektroniko bidezko eguneratzeak eta eskaintzak jaso nahi badituzu.

1. Berrikusi elkarreragin-xehetasunak (aurrebista) **erabiltzeko baldintzak** eta **pribatutasun adierazpena**, eta ondoren hautatu **arakatu demoa** ezarpenak onartzeko.

1. Arakatu produktua laginaren datu multzo bat erabiliz.

##  <a name="step-3-set-up-a-workspace-and-create-reports"></a>3. urratsa: Konfiguratu laneko area eta sortu txostenak

Laneko area bat erabiltzailearen denbora errealeko jarduna ikusi eta txostenak gorde eta kudeatzeko leku bat da. Gehitu kodea zure webgunean biltzen hasteko *gertaerak*, erabiltzaileek jasotzen dituzten jardueren datuak.

1. [Sortu lan-eremua](create-workspace.md) eta gehitu kideak.

1. Gehitu kodea zure [webgunera](instrument-website.md) edo [mugikorretarako aplikazioa](developer-resources.md#capture-events-from-mobile-apps) erabiltzaileen jarduera zure lan-eremura iristen ikusteko.

1. Ikusi [denbora errealeko txosten bat](view-reports.md), erabiltzaile aktiboak arakatzailearen, gailuaren, sistema-eragilearen, kokalekuaren eta hizkuntzaren arabera erakusten dituena. Sortu ere egin dezakezu [txosten pertsonalizatuak](custom-reports.md) zure bistaratzeak sortzeko.

1. Sortu [dimentsioak](dimensions.md) bisitariak erabiltzaile berrien eta berriaren arabera sailkatzeko, [metrika](metrics.md) erabiltzaileen portaera hobeto ulertzen laguntzeko eta [segmentuak](segments.md) bisitarien azpimultzoak identifikatzeko ezaugarrien edo webgunearen elkarreraginen arabera.
    
## <a name="step-4-export-data-to-other-channels"></a>4. urratsa: Esportatu datuak beste kanal batzuetara

Sortu dezakezu *gertaera finduak* (ikuspegi birtuala) zure web analisi datuen. Ondoren, iragazi eta esportatu datuak Azure Data Lake Storage. Esportatutako datuak datu-iturburu gisa har ditzakezu.

1. [Sortu gertaera finduak](refined-events.md) esportaziorako.

1. [Esportatu datuak](export-events.md) hurrengora Azure Data Lake Storage.

1. [Sortu esteka bat hartzaileen xehetasunen eta parte-hartzearen xehetasunen artean](integrate-audience-insights-engagement-insights.md) datuak bi gaitasunen artean partekatzeko.

1. [Aurretik autentifikatutako erabiltzaileen web gertaerak ezagutu](unknown-to-known.md) nirekin **ezezaguna ezaguna** ezaugarria.

1. Ikasi nola [ezabatu eta esportatu gertaeren datuak barne hartuz informazio pertsonala](delete-export-personal-data.md).

## <a name="step-5-create-and-manage-funnel-reports"></a>5. urratsa: Sortu eta kudeatu inbutu-txostenak

Inbutu txosten batek bezero-bidaia batean gertatzen diren pausoei buruzko informazioa biltzen du zure webgunearen edo mugikorretarako aplikazioaren bidez. Kutxaz kanpoko profilen txostenak eta txosten pertsonalizatuak sortzeaz gain, inbutuen txostena sor dezakezu bezeroek erosketa egin aurretik egiten dituzten bideak identifikatzeko. 

1. [Sortu inbutuaren txostena](funnel-reports.md) erabakiak informatzeko eta optimizatzeko eta prozesuaren hobekuntzarako eremuak identifikatzeko.

1. Sortu kanalen arteko inbutuen txostenak, mugikorretarako aplikazioa konpromisoen inguruko datuekin instrumentatu ondoren [Android SDK](get-started-android.md) edo [iOS SDK](get-started-ios.md).

1. Erabili [inbutuaren xehetasunak](funnel-reports.md#funnel-insights) xehetasun gehiago lortzeko bezeroaren portaeran inbutuaren xehetasuneko urratsei buruz.
 
## <a name="step-6-stay-connected"></a>6. urratsa: egon zaitez konektatuta

Eskertzen dugu parte-hartzea, eta oharrak kontuan hartuko ditugu etorkizuneko produktuak sortzerakoan. Partekatu zure iritzia eta eman arazo horien berri kanal hauetako baten bidez:
- [Komunitatea](https://go.microsoft.com/fwlink/?linkid=2141648)
- [Eman zure iritzia](https://go.microsoft.com/fwlink/?linkid=2143222)
- [Eskatu laguntza](https://go.microsoft.com/fwlink/?linkid=2145734) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
