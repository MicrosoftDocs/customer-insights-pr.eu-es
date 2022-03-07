---
title: Erabili datu-iturburuak datuak sartzeko
description: Ikasi iturri desberdinetako datuak nola inportatu.
ms.date: 12/06/2021
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
ms.openlocfilehash: e7bcf82c4fe3625ef791ec2b0a7651be0356a006
ms.sourcegitcommit: 73cb021760516729e696c9a90731304d92e0e1ef
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/25/2022
ms.locfileid: "8354034"
---
# <a name="data-sources-overview"></a>Datuen iturburuen ikuspegi orokorra



Dynamics 365 Customer Insights-eko hartzaileen xehetasunen gaitasuna iturburu multzo zabal bateko datuekin konektatzen da. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.

## <a name="add-a-data-source"></a>Gehitu datu-iturburua

Ikusi artikulu zehatzak datu-iturburu bat nola gehitu jakiteko, aukeratzen duzun aukeraren arabera.

Datu iturri hauek gehi ditzakezu:

- [Dozenaka bidez Power Query konektoreak](connect-power-query.md)
- [Hurrengotik Common Data Model-eko karpeta bat](connect-common-data-model.md)
- [Zuretik Microsoft Dataverse lakua](connect-dataverse-managed-lake.md)
- [Batetik Azure Synapse Analytics datu-basea](connect-synapse.md)

> [!NOTE]
> Probako bertsioa erabiltzen ari bazara, inportazio metodoen atalean a **Customer Insights datu-liburutegia** aukera. Aukeratu aukera hau hainbat industriatarako erabilgarri dagoen datu-multzo lagin bat hautatzeko. Informazio gehiagorako, ikus [Dynamics 365 Customer Insights epaiketa](../trial-signup.md).

## <a name="add-data-from-on-premises-data-sources"></a>Gehitu datuak lokal datu iturrietatik

Oinarrian onartzen da lokal datu iturrietako datuak sartzea parte-hartzaileen xehetasunen Microsoft Power Platform datu-fluxuak. Customer Insights-en Datu-fluxuak gaitu ditzakezu [emanez Microsoft Dataverse ingurunearen URLa](create-environment.md) ingurunea ezartzerakoan.

A elkartu ondoren sortzen diren datu-iturriak Dataverse Customer Insights erabilera duen ingurunea [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz. Datu fluxuek konektibitate lokala onartzen dute datuetarako atebidea erabiliz. Aurretik zeuden datu-iturriak kendu eta birsor ditzakezu Dataverse ingurunea lotzen zen [lokal datu-pasabideak erabiliz](/data-integration/gateway/service-gateway-app).

Dagoen batetik datozen atebideak Power BI edo Power Apps ingurunea ikusgai egongo da eta Customer Insights-en berrerabili dezakezu. Datu iturrien orriak estekara erakusten du Microsoft Power Platform lokal datu atebideak ikusi eta konfiguratzeko ingurunea.

## <a name="review-ingested-data"></a>Berrikusi sartutako datuak

Irentsitako datu-iturburu bakoitzaren izena, bere egoera eta iturri horretako datuak berritu ziren azken aldia ikusiko dituzu. Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.

> [!div class="mx-imgBorder"]
> ![Gehitutako datu-iturriak.](media/configure-data-datasource-added.png "Gehitutako datu-iturriak")

[!INCLUDE [progress-details-include](../includes/progress-details-pane.md)]

Datuak kargatzeak denbora behar dezake. Freskatu ondoren, iradokitako datuak berrikusi daitezke **erakundeak** orria. Informazio gehiago lortzeko, [Entitateak](entities.md).

## <a name="refresh-a-data-source"></a>Freskatu datu-iturburu bat

Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera. 

Joan **Administratzailea** > **Sistema** > [**Antolaketa**](system.md#schedule-tab) atalera sartutako datu-iturburu guztien freskatze antolatuak konfiguratzeko.

Eskatu ahalako datu-iturburu bat freskatzeko, jarraitu urrats hauek:

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Aukeratu elipsi bertikala freskatu eta hautatu nahi duzun datu-iturburu ondoan **Freskatu** goitibeherako zerrendatik.

3. Datu-iturburua eskuz eguneratzeko aktibatuta dago. datu-iturburu freskatzeak entitatearen eskema eta datuak eguneratuko ditu datu-iturburu-en zehaztutako entitate guztientzat.

4. Aukeratu **Freskatzeari utzi** lehendik dagoen freskatzea bertan behera utzi nahi baduzu, eta datu-iturburua bere azken eguneratze-egoerara itzuliko da.

## <a name="delete-a-data-source"></a>Ezabatu datu-iturri bat

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Aukeratu elipsi bertikala ezabatu eta hautatu nahi duzun datu-iturburu ondoan **Ezabatu** goitibeherako menutik.

3. Berretsi ezabatu nahi duzula.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
