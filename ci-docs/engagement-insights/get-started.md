---
title: Hasi konpromiso estatistiken gaitasunarekin
description: Laguntza baliabideen ikuspegi orokorra azkar hasteko.
ms.reviewer: mhart
ms.author: jefhar
author: mochimochi016
ms.date: 12/21/2020
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: 5ee1567cea834670a16aaa3253912b7957ce26b3
ms.sourcegitcommit: 86739a3f238162fc96837270b5d184e648fab15c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "7405343"
---
# <a name="get-started-with-dynamics-365-customer-insights-engagement-insights-capability-public-preview"></a>Hasi Dynamics 365 Customer Insights elkarreragin xehetasunen gaitasuna (aurrebista publikoa)

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Elkarreragin xehetasunak, gaitasuna , bezeroen portaera zure webgunean biltzeko eta neurtzeko aukera ematen du. Ikuslegoaren ikuspegi gaitasunarekin integratzen da, denbora errealeko portaeraren analisi aberatsak bezeroaren profileko txostenekin batera ikusi ahal izateko. Artikulu honetako estekek zure ingurunea azkar konfiguratzen eta konfiguratzen lagunduko dizute.

## <a name="step-1-review-prerequisites"></a>1. urratsa: berrikusi aurrebaldintzak

Lehenik, aktiboa izan behar duzu Microsoft Azure Active Directory erabiltzaile kontua. Ondoren, irakurri hurrengo artikuluak konpromisoen inguruko lan-eremua konfiguratu aurretik.

- Berrikusi eta onartu [Zerbitzu-baldintzak](terms-of-service.md) Microsoft-ekin.  
- Irakurri [Kudeatu cookieak eta erabiltzaileen baimena](user-consent-storage.md) artikulua. Artikulu hau aztertu ondoren, ebaluatu zure erabiltzaile baimenaren jakinarazpena eguneratu behar duzun ala ez. Aurretik "funtsezkoak ez" diren cookie-rik ez baduzu, ziurrenik zure webgunearen politika eguneratu beharko duzu.
- Berrikusi [glosarioa](glossary.md) funtsezko termino eta kontzeptuak azkar sartzeko.

## <a name="step-2-explore-engagement-insights"></a>2. Urratsa: arakatu konpromisoak

Konpromiso estatistikak bisitatzen dituzunean lehenengo aldiz ezarpenak konfiguratu ditzakezu, gidalerroak berrikusi eta produktua azter dezakezu.

1. Saioa hasi [elkarreragin xehetasunen gaitasunaren ataria](https://pi.dynamics.com) zure Microsoft Azure Active Directory erabiltzaile kontua. (Zure ikastetxeko edo laneko kontua izan daiteke.)

1. Aukeratu zure eskualdea eta erabili kontrol-laukia posta elektroniko bidez eguneratzeak eta eskaintzak jasotzeko hautatzea nahi duzun adierazteko.

1. Berrikusi **elkarreragin xehetasunak (aurrebista) Erabilera baldintzak** eta **Pribatutasun-adierazpena**, eta hautatu **Arakatu demoa** onartzeko.

1. Arakatu produktua laginaren datu multzo bat erabiliz.

##  <a name="step-3-set-up-a-workspace-and-add-code-to-your-website"></a>3. urratsa: Konfiguratu laneko area eta gehitu kodea zure webgunera

Laneko eremua erabiltzaileen jarduera denbora errealean ikus dezakezu, eta txostenak gorde eta kudeatu. Gehitu kodea zure webgunean biltzen hasteko *gertaerak*, erabiltzaileek jasotzen dituzten jardueren datuak.

1. [Sortu lan-eremua](create-workspace.md) eta gehitu kideak.

1. [Gehitu kodea zure webgunera](instrument-website.md) edo [mugikorretarako aplikazioa](developer-resources.md#capture-events-from-mobile-apps) erabiltzaileen jarduera zure lan-eremura iristen ikusteko.

1. Ikusi [denbora errealeko txostena](view-reports.md) erabiltzaile aktiboak arakatzailearen, gailuaren, sistema eragilearen, kokapenaren eta hizkuntzaren arabera erakutsiz. Sortu ere egin dezakezu [txosten pertsonalizatuak](custom-reports.md) zure bistaratzeak sortzeko.
    
## <a name="step-4-export-data-to-other-channels"></a>4. urratsa: Esportatu datuak beste kanal batzuetara

Sortu dezakezu *gertaera finduak* (ikuspegi birtuala) zure web analisi datuen. Ondoren, iragazi eta esportatu datuak Azure Data Lake Storage. Esportatutako datuak datu-iturburu gisa har ditzakezu. Informazio gehiagorako, ikusi [Sortu esteka hartzailearen eta elkarreragin xehetasunen artean](integrate-audience-insights-engagement-insights.md).

1. [Sortu gertaera finduak](refined-events.md) esportaziorako.

1. [Esportatu datuak](export-events.md) Data Lake biltegiratzera.

1. Ikasi nola [ezabatu eta esportatu gertaeren datuak barne hartuz informazio pertsonala](delete-export-personal-data.md).
 
## <a name="step-5-stay-connected"></a>5. urratsa: egon zaitez konektatuta

Zure parte-hartze aktiboa eskertzen dugu eta etorkizuneko oharrak garatzeko iritzi garrantzitsu guztiak kontuan hartzeko asmoa dugu. Partekatu zure iritzia eta eman arazo horien berri kanal hauetako baten bidez:
- [Komunitatea](https://go.microsoft.com/fwlink/?linkid=2141648)
- [Eman zure iritzia](https://go.microsoft.com/fwlink/?linkid=2143222)
- [Eskatu laguntza](https://go.microsoft.com/fwlink/?linkid=2145734) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
