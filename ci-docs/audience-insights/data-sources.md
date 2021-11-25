---
title: Erabili datu-iturburuak datuak sartzeko
description: Ikasi iturri desberdinetako datuak nola inportatu.
ms.date: 11/01/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: 27cbd0346b1219c7812f4b90327dd27b645c2b8e
ms.sourcegitcommit: 834651b933b1e50e7557d44f926a3fb757c1f83a
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/02/2021
ms.locfileid: "7732112"
---
# <a name="data-sources-overview"></a>Datuen iturburuen ikuspegi orokorra

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Dynamics 365 Customer Insights-n ikusleei buruzko informazio-gaitasuna iturri multzo zabal bateko datuekin konektatzen da. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.

## <a name="add-a-data-source"></a>Gehitu datu-iturburua

datu-iturburu bat gehitzeko artikulu zehatzak ikusi, aukeratutako aukeraren arabera.

datu-iturburu bat gehi dezakezu hiru modu nagusitan:

- [Dozenaka Power Query lokailuren bidez](connect-power-query.md)
- [Hurrengotik Common Data Model-eko karpeta bat](connect-common-data-model.md)
- [Zure Microsoft Dataverse lakutik](connect-dataverse-managed-lake.md)

## <a name="add-data-from-on-premises-data-sources"></a>Gehitu datuak lokal datu iturrietatik

Lokal datu-iturburuetako datuak ikusleei buruzko informazioetan sartzea onartzen da Microsoft Power Platform datu-fluxuetan oinarrituta. Datu-fluxuak Customer Insights-en gaitu daitezke [Microsoft Dataverse ingurunearen URLa emanez](create-environment.md) ingurunea ezartzerakoan.

Dataverse ingurune bat Customer Insights-ekin lotu ondoren sortzen diren datu-iturburuak erabiliko dituzte [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz. Datu fluxuek konektibitate lokala onartzen dute datuetarako atebidea erabiliz. Kendu eta birsortu Dataverse ingurunea lotu aurretik zeuden datu-iturriak [erabili lokal datu-pasabideak](/data-integration/gateway/service-gateway-app).

Lehendik dagoen Power BI edo Power Apps inguruneko datu-atebideak ikusgai egongo dira eta Customer Insights-en berrerabili ahal izango duzu. Datu-iturburuen orrialdeak Microsoft Power Platform ingurunera joateko estekak erakusten ditu, non lokal datu-atebideak ikusi eta konfigura ditzakezun.

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
