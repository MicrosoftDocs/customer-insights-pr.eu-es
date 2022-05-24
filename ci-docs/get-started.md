---
title: Hasi Dynamics 365 Customer Insights erabiltzen
description: Customer Insights-en ikuspegi orokorrak baliabideak azkar hasten laguntzen du.
ms.reviewer: v-wendysmith
ms.author: mhart
author: m-hartmann
ms.date: 04/12/2022
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.custom: intro-internal
searchScope:
- ci-home
- customerInsights
ms.openlocfilehash: 1a19d83930d667bdca5301dcc5a3ffa5db6a7bdc
ms.sourcegitcommit: 6a5f4312a2bb808c40830863f26620daf65b921d
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8741118"
---
# <a name="get-started-with-dynamics-365-customer-insights"></a>Hasi Dynamics 365 Customer Insights erabiltzen

Customer Insights-ek zure bezeroak hobeto ulertzen lagun zaitzake. Konektatu iturri transakzionaleko, jokabideko eta behatokiko hainbat iturritako datuak, 360 graduko bezeroaren ikuspegia sortzeko. Erabil itzazu ikuspegi horiek bezeroen inguruko esperientzia eta prozesuak gidatzeko. Bateratu eta ulertu bezeroen datuak eta balia itzazu ikuspegi eta ekintza adimentsuetarako.

## <a name="step-1-create-an-environment"></a>1. urratsa: Sortu ingurune bat

Hasteko, ingurune bat sortu behar duzu bertan lan egiteko. Zure erakundeak lizentzia erosi badu, ikusi [Ingurune bat sortu](create-environment.md). Customer Insights-en proba bat hasteko, ikusi [Konfiguratu proba-ingurune bat](trial-signup.md).

## <a name="step-2-explore-customer-insights"></a>2. urratsa: arakatu bezeroen ikuspegiak

Customer Insights-en saioa hasten duzun lehen aldian, ezarpenak konfigura ditzakezu eta produktua arakatu.

1. [hasi saioa Customer Insights-en](https://home.ci.ai.dynamics.com) zure Microsoft erabiliz Azure Active Directory (AAD) erabiltzaile-kontua.

1. [Aldatu ingurunea](manage-environments.md#switch-environments) demo datuak ikusteko eta [arakatu Customer Insights](home.md).

## <a name="step-3-ingest-unify-and-set-up-relationships-for-your-data"></a>3. urratsa: sartu, bateratu eta ezarri datuen erlazioak

Profil bateratuak dira xehetasunak lortu eta datuetan eragiteko oinarria. Ekarri hainbat baliabidetako datuak eta exekutatu datuak bateratzeko prozesua, profil bateratuak konbinatzeko. Zehaztu sartutako entitateen arteko erlazioak eta erabili aberaste-eginbideak profiletan informazioa gehitzeko.

1. Sartu datua hainbat aukeretatik datu-iturburuak sortuz. Aukeratu artean [Power Query konektoreak](connect-power-query.md), a [Common Data Model karpeta](connect-common-data-model.md), edo [Microsoft Dataverse](connect-dataverse-managed-lake.md). 

1. Exekutatu [datuak bateratzeko prozesua](data-unification.md) identifikatuz [iturri-eremuak](map-entities.md), kenduz [bikoiztuak](remove-duplicates.md),[bat datozen baldintzak](match-entities.md), eta [eremuak bateratzea](merge-entities.md).

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

1. Berrikusi integrazio-aukerak, adibidez, beste Dynamics 365 aplikazioekin [Bezero Txartelaren gehigarria](customer-card-add-in.md).  


[!INCLUDE [footer-include](includes/footer-banner.md)]
