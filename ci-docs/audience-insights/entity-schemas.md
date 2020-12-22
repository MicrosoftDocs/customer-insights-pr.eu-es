---
title: Customer Insights entitateen eskemak Common Data Model-en
description: Egin lan entitateekin Common Data Model-en.
ms.date: 04/17/2020
ms.reviewer: mukeshpo
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 2cf01029ef6b64fe566022d09ce65bca3603189c
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643893"
---
# <a name="entity-schemas-in-common-data-model"></a>Entitateen eskema datu arrunten ereduan

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

[Datu eredu arrunta](https://docs.microsoft.com/common-data-model/) adierazpen-zehaztapena da, eta negozioen eta produktibitatearen aplikazioetan gehien erabiltzen diren kontzeptuak eta jarduerak ordezkatzen dituzten entitate estandarren definizioa. Eredu hori datu behaketa eta analitikoetara ere hedatzen ari da. Datu arrunten ereduak negozio-erakunde zehaztuak, modularrak eta hedagarriak eskaintzen ditu (hala nola, Kontua, Negozio Unitatea, Kasua, Kontaktua, Leadea, Aukera eta Produktua), baita saltzaileekin, langileekin eta bezeroekin elkarreraginak ere, hala nola jarduerak eta zerbitzua maila hitzarmenak. Edonork eraiki eta hedatu ahal izango ditu Datu Ereduen eredu arrunten definizioak negozioetarako berariazko ideiak osatzeko.

Hau partekatutako datuen eredua da, aplikazioei eta datuen integratzaileei errazago lankidetzan aritzeko aukera ematea, datuen definizio bateratua emanez. Datu arrunten ereduak metadatuen sistema aberatsa biltzen du entitate estandarrak, harremanak, hierarkiak, ezaugarriak eta beste. Dynamics 365 aplikazioetatik du jatorria eta GitHuben irekita dago 260 estandar entitate baino gehiagorekin. Barneko eta kanpoko bazkideen sistema handi batek industriari buruzko kontzeptuak laguntzen ditu Datu Eredu Orokorrean.

Sistema eta plataforma ugarik gaur egungo datu eredua ezartzen dute, besteak beste Power BI datu fluxuak eta Azure Data zerbitzuak. Dagoeneko onartzen da Common Data Service, Dynamics 365, Power Apps, Power BI eta Azure datuen hurrengo zerbitzuak (zuzenean) [Open Data Initiative](https://www.microsoft.com/open-data-initiative).

## <a name="customer-insights-entity-schemas"></a>Customer Insights entitatearen eskemak

Bezeroaren 360 graduko ikuspegia ezartzeko eta Customer Insights ereduak Data arrunten ereduan eskuragarri jartzeko, zabaltasunerako, entitateen eskema hauek argitaratu ditugu:

| Entitatea | Azalpena |
|---------|---------|
|[Jarduera pertsonalizatuak](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/customeractivity) | Negozioarentzako behatoki balioa duen erabiltzaile batek egiten duen jarduera. |
|[Bezero-profila](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/customerprofile) | Pertsona edo erakunde bat burutu duen edo negozio jarduerak batean egiteko ahalmena duen. |
|[Neurketaren definizioa](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/measuredefinition) | Zero dimentsio edo gehiagoren arabera zatitutako KPIen definizioa (adibidez, hileroko erabiltzaile aktiboak, bezeroaren guztizko gastua, bezeroaren erosketen batez besteko kostua) |
|[Segmentua](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/segment) | Ezaugarri komunak erakusten dituzten kideen multzoa definitzen du. |
|[Segmentuaren kideak](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/segmentmembership) | Segmentu jakin batean parte hartzen duten kideak. |

Informazio gehiago lortzeko, ikusi dokumentazioari buruzko dokumentazioa [Customer Insights entitatearen eskemak Datuen eredu arruntean](https://docs.microsoft.com/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/overview).

## <a name="view-entities-using-the-common-data-model-entity-navigator"></a>Ikusi entitateak datu ereduen entitate nabigatzailea erabiliz

Entitateak ikus ditzakezu [Common Data Model-en entitateen nabigatzailean](https://microsoft.github.io/CDM/). Hautatu botoia **Kargatu GitHub-etik!** Botoian eta nabigatu **foundationCommon** > **crmCommon** > **soluzioak** > **customerInsights** non aurkituko duzu Customer Insights entitateen zerrenda eta horien definizioak.
> [!div class="mx-imgBorder"]
> ![CDM Entity Navigator CustomerActivity entitatea erakusten duena](media/CDM-entity-navigator.png "CDM Entity Navigator CustomerActivity entitatea erakusten duena")
