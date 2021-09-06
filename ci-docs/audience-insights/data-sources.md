---
title: Erabili datu-iturburuak datuak sartzeko
description: Ikasi iturri desberdinetako datuak nola inportatu.
ms.date: 04/12/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: 75d597158233f75f0eb5f94389f9dba199d81719f2bbe4e5cc58d2a3afc7dcf8
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7032835"
---
# <a name="data-sources-overview"></a>Datuen iturburuen ikuspegi orokorra

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Dynamics 365 Customer Insights-eko hartzaileen xehetasunen gaitasuna iturburu multzo zabal bateko datuekin konektatzen da. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.

## <a name="add-a-data-source"></a>Gehitu datu-iturburua

datu-iturburu bat gehitzeko artikulu zehatzak ikusi, aukeratutako aukeraren arabera.

datu-iturburu bat gehi dezakezu hiru modu nagusitan:

- [Dozenaka Power Query lokailuren bidez](connect-power-query.md)
- [Hurrengotik Common Data Model-eko karpeta bat](connect-common-data-model.md)
- [Zuretik Microsoft Dataverse lakua](connect-dataverse-managed-lake.md)

## <a name="add-data-from-on-premises-data-sources"></a>Gehitu datuak lokal datu iturrietatik

Oinarrian onartzen da lokal datu iturrietako datuak sartzea parte-hartzaileen xehetasunen Microsoft Power Platform datu-fluxuak. Datu-fluxuak Customer Insights-en gaitu daitezke [eskainiz Microsoft Dataverse inguruneko URLa](get-started-paid.md) ingurunea konfiguratzerakoan.

Elkartu ondoren sortzen diren datu iturriak Dataverse Customer Insights-ekin ingurunea erabiliko da [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz. Datu fluxuek konektibitate lokala onartzen dute datuetarako atebidea erabiliz. Kendu eta sortu berriro Dataverse ingurunea [datuetarako atebide lokalen erabilerarekin](/data-integration/gateway/service-gateway-app) erlazionatu baino lehen zeuden datu-iturburuak.

Dagoen batetik datozen atebideak Power BI edo Power Apps ingurunea ikusgai egongo da eta Customer Insights-en berrerabili dezakezu. Datu iturrien orriak estekara erakusten du Microsoft Power Platform lokal datu atebideak ikusi eta konfiguratzeko ingurunea.

## <a name="review-ingested-data"></a>Berrikusi sartutako datuak

Irentsitako datu-iturburu bakoitzaren izena, bere egoera eta iturri horretako datuak berritu ziren azken aldia ikusiko dituzu. Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.

> [!div class="mx-imgBorder"]
> ![Gehitutako datu-iturriak.](media/configure-data-datasource-added.png "Gehitutako datu-iturriak")

|Fasea  |Deskribapenak  |
|---------|---------|
|Osatuta   |Datu-iturburu sartu da **Freskatuta** zutabean denbora-tartea adierazten bada.
|Ez da hasi   |Datu-iturburuak oraindik ez du daturik sartu edo oraindik zirriborro moduan daude.         |
|Freskatzen    |Datuen horniketa martxan da. Eragiketa hau bertan behera utzi dezakezu **Utzi freskagarria** herrian **Ekintzak** zutabea. datu-iturburu-en freskagarria gelditzeak azken freskatze egoeran itzuliko du.       |
|Ezin izan da egin     |Datuen iradokizunak akatsak izan ditu.         |

Hautatu balioa **Egoera** datu-iturburu edozein zutabetan xehetasun gehiago berrikusteko. **Aurrerapenaren xehetasunak** panelean, zabaldu **Datu-iturburuak**. Aukeratu **Ikusi xehetasunak** freskatze egoerari buruzko xehetasun gehiago berrikusteko, erroreen xehetasunak eta beherako prozesuen eguneratzeak barne.

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
