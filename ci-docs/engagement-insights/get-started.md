---
title: Hasi konpromiso estatistiken gaitasunarekin
description: Laguntza baliabideen ikuspegi orokorra azkar hasteko.
ms.reviewer: mhart
ms.author: jefhar
author: mochimochi016
ms.date: 08/31/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: 644b125f5d140627d357630ded88dd6838d6edb7
ms.sourcegitcommit: fecdee73e26816c42d39d160d4d5cfb6c8a91596
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/15/2021
ms.locfileid: "7494579"
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

1. Berrikusi **parte-hartzearen xehetasunen (aurreargitalpena) erabiltzeko baldintzak** eta **pribatutasun adierazpena**, eta ondoren hautatu **arakatu demoa** ezarpenak onartzeko.

1. Arakatu produktua laginaren datu multzo bat erabiliz.

##  <a name="step-3-set-up-a-workspace-and-add-code-to-your-website"></a>3. urratsa: Konfiguratu laneko area eta gehitu kodea zure webgunera

Laneko area bat erabiltzailearen denbora errealeko jarduna ikusi eta txostenak gorde eta kudeatzeko leku bat da. Gehitu kodea zure webgunean biltzen hasteko *gertaerak*, erabiltzaileek jasotzen dituzten jardueren datuak.

1. [Sortu lan-eremua](create-workspace.md) eta gehitu kideak.

1. [Gehitu kodea zure webgunera](instrument-website.md) edo [mugikorretarako aplikazioa](developer-resources.md#capture-events-from-mobile-apps) erabiltzaileen jarduera zure lan-eremura iristen ikusteko.

1. Ikusi [denbora errealeko txosten bat](view-reports.md), erabiltzaile aktiboak arakatzailearen, gailuaren, sistema-eragilearen, kokalekuaren eta hizkuntzaren arabera erakusten dituena. Sortu ere egin dezakezu [txosten pertsonalizatuak](custom-reports.md) zure bistaratzeak sortzeko.
    
## <a name="step-4-export-data-to-other-channels"></a>4. urratsa: Esportatu datuak beste kanal batzuetara

Sortu dezakezu *gertaera finduak* (ikuspegi birtuala) zure web analisi datuen. Ondoren, iragazi eta esportatu datuak Azure Data Lake Storage. Esportatutako datuak datu-iturburu gisa har ditzakezu. Informazio gehiagorako, ikusi [Sortu esteka hartzailearen eta elkarreragin xehetasunen artean](integrate-audience-insights-engagement-insights.md).

1. [Sortu gertaera finduak](refined-events.md) esportaziorako.

1. [Esportatu datuak](export-events.md) Data Lake biltegiratzera.

1. [Sortu esteka bat hartzaileen xehetasunen eta parte-hartzearen xehetasunen artean](integrate-audience-insights-engagement-insights.md) datuak bi gaitasunen artean partekatzeko.

1. Ikasi nola [ezabatu eta esportatu gertaeren datuak barne hartuz informazio pertsonala](delete-export-personal-data.md).
 
## <a name="step-5-stay-connected"></a>5. urratsa: egon zaitez konektatuta

Eskertzen dugu parte-hartzea, eta oharrak kontuan hartuko ditugu etorkizuneko produktuak sortzerakoan. Partekatu zure iritzia eta eman arazo horien berri kanal hauetako baten bidez:
- [Komunitatea](https://go.microsoft.com/fwlink/?linkid=2141648)
- [Eman zure iritzia](https://go.microsoft.com/fwlink/?linkid=2143222)
- [Eskatu laguntza](https://go.microsoft.com/fwlink/?linkid=2145734) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]