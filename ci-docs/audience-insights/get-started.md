---
title: Hasi hartzaileen xehetasunen gaitasuna erabiltzen Dynamics 365 Customer Insights-en
description: Hartzaileen xehetasunei buruzko informazio orokorrak azkar hasten laguntzen die baliabideei.
ms.reviewer: mhart
ms.author: mhart
author: m-hartmann
ms.date: 08/31/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: aaaf1848df175469d8af07754ac153b777781ffb
ms.sourcegitcommit: 971716c761871cee390519cacef617dac21ecd60
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466562"
---
# <a name="get-started-with-dynamics-365-customer-insights-audience-insights-capability"></a>Hasi Dynamics 365 Customer Insights-en hartzaileen xehetasunen gaitasuna erabiltzen

Hartzaileen xehetasunek bezeroak hobeto ulertzen lagun zaitzakete. Konektatu iturri transakzionaleko, jokabideko eta behatokiko hainbat iturritako datuak, 360 graduko bezeroaren ikuspegia sortzeko. Erabil itzazu ikuspegi horiek bezeroen inguruko esperientzia eta prozesuak gidatzeko. Bateratu eta ulertu bezeroen datuak eta balia itzazu ikuspegi eta ekintza adimentsuetarako.

## <a name="step-1-create-an-environment"></a>1. urratsa: Sortu ingurune bat

Hasteko, ingurune bat sortu behar duzu bertan lan egiteko. Erakundeak lizentzia bat erosi badu jada, ikusi [Hasi erabiltzen ordainpeko harpidetzarekin](get-started-paid.md). Hartzaileen xehetasunen probaldia hasteko, iksui [Konfiguratu probako ingurunea](get-started-trial.md). 

## <a name="step-2-explore-audience-insights"></a>2. urratsa: arakatu hartzaileen xehetasunak

Hartzaileen xehetasunetan saioa hasten duzun lehen aldian, ezarpenak konfiguratu eta produktua arakatu dezakezu.

1. [Hasi saioa hartzaileen xehetasunetan](https://home.ci.ai.dynamics.com) Microsoft Azure Active Directory (AAD) erabiltzaile-kontua erabiliz.

1. [Aldatu ingurunea](manage-environments.md#switch-environments) demo datuak ikusteko eta [hartzaileen xehetasunak arakatzeko](home.md).

##  <a name="step-3-ingest-unify-and-set-up-relationships-for-your-data"></a>3. urratsa: sartu, bateratu eta ezarri datuen erlazioak

Profil bateratuak dira xehetasunak lortu eta datuetan eragiteko oinarria. Ekarri hainbat baliabidetako datuak eta exekutatu datuak bateratzeko prozesua, profil bateratuak konbinatzeko. Zehaztu sartutako entitateen arteko erlazioak eta erabili aberaste-eginbideak profiletan informazioa gehitzeko. 

1. Sartu datua hainbat aukeretatik datu-iturburuak sortuz. Aukeratu hauen artean: [Power Query konektoreak](connect-power-query.md), [Common Data Model karpeta](connect-common-data-model.md) edo [Microsoft Dataverse](connect-common-data-service-lake.md). 

1. Exekutatu [datuak bateratzeko prozesua](data-unification.md), [esleitu](map-entities.md), [bat-etorri](match-entities.md), eta [konbinatu](merge-entities.md) urratsak osatuz.

1. Ezagutu [sistemak sortzen dituen entitateak](entities.md) eta sortu [erlazioak sartutako entitateen artean](relationships.md).
    
## <a name="step-4-enhance-unified-profiles-with-predictions-activities-and-measures"></a>4. urratsa: hobetu profil bateratuak iragarpen, jarduera eta neurriekin

Profil bateratuen konfigurazioarekin, datuak hobetu ditzakezu eta eurek ematen duten informazioa areagotu.

1. Aukeratu aberasteen hornitzaileen liburutegi zabaletik [bezeroen datuak aberasteko](enrichment-hub.md).

1. Erabili [erabiltzeko prest dauden ereduak](predictions-overview.md) galeraren probabilitatea edo aurreikusitako irabaziak iragartzeko.

1. [Konfiguratu jarduerak](activities.md) sartutako datuetan oinarrituta eta bistaratu bezeroekin duzun hartu-emana denbora-lerro kronologikoan. 

1. [Sortu neurriak](measures.md) negozio-xedeak eta KPIak neurtzeko.
 
## <a name="step-5-create-segments-and-activate-data-through-various-export-options"></a>5. urratsa: sortu segmentuak eta aktibatu datuak hainbat esportazio-aukeraren bidez

Datuak osatuta daudenean eta bezeroei buruzko informazio zabala dutenean, datuekin lanean asteko ordua da. 

1. [Sortu segmentuak](segments.md), bezeroaren oinarriaren azpimultzoak, ziurtatzeko ekintzak egokiak direla zehaztutako bezeroentzat.

1. Arakatu [esportazio-aukeren](export-destinations.md) katalogo zabala, non bezeroaren datuak erabil baititzakezun. Adibidez, datuak erabil ditzakezu promozioak kudeatzeko eta marketin digitalarekin harremanetan jartzeko.

1. Berrikusi integrazio-aukerak, adibidez [parte-hartzearen xehetasunekiko konexio zuzenarekin](../engagement-insights/integrate-audience-insights-engagement-insights.md) edo Dynamics 365-eko beste aplikazioekiko [bezero-txartelaren gehigarriarekin](customer-card-add-in.md).  


[!INCLUDE[footer-include](../includes/footer-banner.md)]
