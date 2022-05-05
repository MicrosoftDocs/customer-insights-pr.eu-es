---
title: Erabili datu-iturburuak datuak sartzeko
description: Ikasi iturri desberdinetako datuak nola inportatu.
ms.date: 03/18/2022
ms.subservice: audience-insights
ms.topic: overview
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-data-sources
- ci-create-data-source
- customerInsights
ms.openlocfilehash: bcc50c6fa8f8e2a66ef6164bfa9022e068c0e374
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642007"
---
# <a name="data-sources-overview"></a>Datuen iturburuen ikuspegi orokorra



Dynamics 365 Customer Insights iturri multzo zabal bateko datuetara konektatzen da. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.

## <a name="add-a-data-source"></a>Gehitu datu-iturburua

Ikusi artikulu zehatzak datu-iturburu bat nola gehitu jakiteko, aukeratzen duzun aukeraren arabera.

Datu iturri hauek gehi ditzakezu:

- [Dozenaka bidez Power Query konektoreak](connect-power-query.md)
- [Hurrengotik Common Data Model-eko karpeta bat](connect-common-data-model.md)
- [Zuretik Microsoft Dataverse lakua](connect-dataverse-managed-lake.md)
- [Batetik Azure Synapse Analytics datu-basea](connect-synapse.md)

> [!NOTE]
> Probako bertsioa erabiltzen ari bazara, inportazio metodoen atalean a **Customer Insights datu-liburutegia** aukera. Aukeratu aukera hau hainbat industriarentzat erabilgarri dagoen datu-multzo lagin bat hautatzeko. Informazio gehiagorako, ikus [Dynamics 365 Customer Insights epaiketa](trial-signup.md).

## <a name="add-data-from-on-premises-data-sources"></a>Gehitu datuak lokal datu iturrietatik

Lokal datu-iturburuetako datuak barneratzea onartzen da Microsoft Power Platform datu-fluxuak. Customer Insights-en Datu-fluxuak gaitu ditzakezu [emanez Microsoft Dataverse ingurunearen URLa](create-environment.md) ingurunea ezartzerakoan.

A elkartu ondoren sortzen diren datu-iturriak Dataverse Customer Insights erabilera duen ingurunea [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz. Datu fluxuek konektibitate lokala onartzen dute datuetarako atebidea erabiliz. Aurretik zeuden datu-iturriak kendu eta birsor ditzakezu Dataverse ingurunea lotzen zen [lokal datu-pasabideak erabiliz](/data-integration/gateway/service-gateway-app).

Dagoen batetik datozen atebideak Power BI edo Power Apps ingurunea ikusgai egongo da eta Customer Insights-en berrerabili dezakezu. Datu iturrien orriak estekara erakusten du Microsoft Power Platform lokal datu atebideak ikusi eta konfiguratzeko ingurunea.

> [!IMPORTANT]
> Ziurtatu atebideak azken bertsiora eguneratuta daudela. Eguneratze bat instalatu eta atebide bat birkonfigura dezakezu atebidearen pantailan agertzen den gonbit batetik zuzenean edo [deskargatu azken bertsioa](https://powerapps.microsoft.com/downloads/). Ez baduzu azken atebidearen bertsioa erabiltzen, datu-fluxua freskatzeak huts egingo du errore-mezuekin **Gako-hitza ez da onartzen: konfigurazio-propietateak. Parametroaren izena: gako-hitza**.

## <a name="review-ingested-data"></a>Berrikusi sartutako datuak
Zure inguruneak badu Power Platform datu-fluxuak, **Datu-iturriak** orrialdeak hiru atal ditu: 
- **Partekatua** : Customer Insights administratzaile guztiek kudeatu ditzaketen datu-iturriak. Power BI datu-fluxuak, zure biltegiratze-kontua eta a Dataverse -kudeatutako data lake partekatutako datu-iturrien adibideak dira.
- **Nik kudeatzen dut** :Power Platform sortu eta zuk bakarrik kudea ditzakezu datu-fluxuak. Customer Insights-eko beste administratzaileek datu-fluxu hauek soilik ikus ditzakete, baina ez editatu, freskatu edo ezabatu.
- **Beste batzuek kudeatzen dute** :Power Platform beste administratzaileek sortutako datu-fluxuak. Horiek bakarrik ikus ditzakezu. Edozein laguntza lortzeko harremanetan jartzeko datu-fluxuaren jabea zerrendatzen du.
> [!NOTE]
> Entitate guztiak beste erabiltzaileek ikusi eta erabil ditzakete. Erabiltzaileen testuingurua datu-iturburuei soilik aplikatzen zaie eta ez datu-fluxu horien ondoriozko entitateei.

Ezetz bada Power Platform datu-fluxuak erabiltzen dira, ez duzu talde edo atalik ikusiko. The **Datu-iturriak** orrialdeak datu-iturburu guztien zerrenda baino ez dauka.

Irentsitako datu-iturburu bakoitzaren izena, bere egoera eta iturri horretako datuak berritu ziren azken aldia ikusiko dituzu. Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.

> [!div class="mx-imgBorder"]
> ![Gehitutako datu-iturriak.](media/configure-data-datasource-added.png "Gehitutako datu-iturriak")

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

Datuak kargatzeak denbora behar dezake. Freskatu ondoren, iradokitako datuak berrikusi daitezke **erakundeak** orria. Informazio gehiago lortzeko, [Entitateak](entities.md).

## <a name="refresh-a-data-source"></a>Freskatu datu-iturburu bat

Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera. 

Joan **Administratzailea** > **Sistema** > [**Antolaketa**](system.md#schedule-tab) atalera sartutako datu-iturburu guztien freskatze antolatuak konfiguratzeko.

Eskatu ahalako datu-iturburu bat freskatzeko, jarraitu urrats hauek:

1. Joan **Datuak** > **Datu-iturburuak**.

2. Aukeratu elipsi bertikala freskatu eta hautatu nahi duzun datu-iturburu ondoan **Freskatu** goitibeherako zerrendatik.

3. Datu-iturburua eskuz eguneratzeko aktibatuta dago. datu-iturburu freskatzeak entitatearen eskema eta datuak eguneratuko ditu datu-iturburu-en zehaztutako entitate guztientzat.

4. Aukeratu **Freskatzeari utzi** lehendik dagoen freskatzea bertan behera utzi nahi baduzu, eta datu-iturburua bere azken eguneratze-egoerara itzuliko da.

## <a name="delete-a-data-source"></a>Ezabatu datu-iturri bat

1. Joan **Datuak** > **Datu-iturburuak**.

2. Aukeratu elipsi bertikala ezabatu eta hautatu nahi duzun datu-iturburu ondoan **Ezabatu** goitibeherako menutik.

3. Berretsi ezabatu nahi duzula.


[!INCLUDE [footer-include](includes/footer-banner.md)]
