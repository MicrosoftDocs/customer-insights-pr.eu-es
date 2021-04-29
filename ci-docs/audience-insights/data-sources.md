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
ms.openlocfilehash: 0fc13d3ac0a5176637b6fe481dabe0b2aec11649
ms.sourcegitcommit: d89b19b2a3497722b78362aeee688ae7e94915d9
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/13/2021
ms.locfileid: "5887879"
---
# <a name="data-sources-overview"></a><span data-ttu-id="4f38d-103">Datuen iturburuen ikuspegi orokorra</span><span class="sxs-lookup"><span data-stu-id="4f38d-103">Data sources overview</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="4f38d-104">Dynamics 365 Customer Insights-eko hartzaileen xehetasunen gaitasuna iturburu multzo zabal bateko datuekin konektatzen da.</span><span class="sxs-lookup"><span data-stu-id="4f38d-104">The audience insights capability in Dynamics 365 Customer Insights connects to data from a broad set of sources.</span></span> <span data-ttu-id="4f38d-105">datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*.</span><span class="sxs-lookup"><span data-stu-id="4f38d-105">Connecting to a data source is often referred to as the process of *data ingestion*.</span></span> <span data-ttu-id="4f38d-106">Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.</span><span class="sxs-lookup"><span data-stu-id="4f38d-106">After ingesting the data, you can [unify](data-unification.md) and take action on it.</span></span>

## <a name="add-a-data-source"></a><span data-ttu-id="4f38d-107">Gehitu datu-iturburua</span><span class="sxs-lookup"><span data-stu-id="4f38d-107">Add a data source</span></span>

<span data-ttu-id="4f38d-108">datu-iturburu bat gehitzeko artikulu zehatzak ikusi, aukeratutako aukeraren arabera.</span><span class="sxs-lookup"><span data-stu-id="4f38d-108">Refer to the detailed articles on how to add a data source, depending on which option you choose.</span></span>

<span data-ttu-id="4f38d-109">datu-iturburu bat gehi dezakezu hiru modu nagusitan:</span><span class="sxs-lookup"><span data-stu-id="4f38d-109">You can add a data source in three main ways:</span></span>

- [<span data-ttu-id="4f38d-110">Dozenaka Power Query lokailuren bidez</span><span class="sxs-lookup"><span data-stu-id="4f38d-110">Through dozens of Power Query connectors</span></span>](connect-power-query.md)
- [<span data-ttu-id="4f38d-111">Hurrengotik Common Data Model-eko karpeta bat</span><span class="sxs-lookup"><span data-stu-id="4f38d-111">From a Common Data Model folder</span></span>](connect-common-data-model.md)
- [<span data-ttu-id="4f38d-112">Zuretik Common Data Service lakua</span><span class="sxs-lookup"><span data-stu-id="4f38d-112">From your own Common Data Service lake</span></span>](connect-common-data-service-lake.md)

## <a name="add-data-from-on-premises-data-sources"></a><span data-ttu-id="4f38d-113">Gehitu datuak lokal datu iturrietatik</span><span class="sxs-lookup"><span data-stu-id="4f38d-113">Add data from on-premises data sources</span></span>

<span data-ttu-id="4f38d-114">Oinarrian onartzen da lokal datu iturrietako datuak sartzea Audience Insights-en Power Platform datu-fluxuak.</span><span class="sxs-lookup"><span data-stu-id="4f38d-114">Ingesting data from on-premises data sources in Audience Insights is supported based on Power Platform dataflows.</span></span> <span data-ttu-id="4f38d-115">Datu-fluxuak Customer Insights-en gaitu daitezke [eskainiz Microsoft Dataverse inguruneko URLa](manage-environments.md#create-an-environment-in-an-existing-organization) ingurunea konfiguratzerakoan.</span><span class="sxs-lookup"><span data-stu-id="4f38d-115">Dataflows can be enabled in Customer Insights by [providing the Microsoft Dataverse environment URL](manage-environments.md#create-an-environment-in-an-existing-organization) when setting up the environment.</span></span>

<span data-ttu-id="4f38d-116">Elkartu ondoren sortzen diren datu iturriak Dataverse Customer Insights-ekin ingurunea erabiliko da [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz.</span><span class="sxs-lookup"><span data-stu-id="4f38d-116">Data sources that are created after associating a Dataverse environment with Customer Insights will use [Power Platform dataflows](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) by default.</span></span> <span data-ttu-id="4f38d-117">Datu fluxuek on-prem konektibitatea onartzen dute datu pasabideak erabiliz.</span><span class="sxs-lookup"><span data-stu-id="4f38d-117">Dataflows support on-prem connectivity using the data gateways.</span></span> <span data-ttu-id="4f38d-118">Aurretik zeuden datu iturriak kendu eta birsortu Dataverse ingurunea lokal datu atebideak erabiltzeko lotu zen.</span><span class="sxs-lookup"><span data-stu-id="4f38d-118">Remove and recreate data sources that existed before a Dataverse environment was associated to use the on-premises data gateways.</span></span>

<span data-ttu-id="4f38d-119">Dagoen batetik datozen atebideak Power BI edo Power Apps ingurunea ikusgai egongo da eta Customer Insights-en berrerabili dezakezu.</span><span class="sxs-lookup"><span data-stu-id="4f38d-119">Data gateways from an existing Power BI or Power Apps environment will be visible and you can reuse in Customer Insights.</span></span> <span data-ttu-id="4f38d-120">Datu iturrien orrira joateko estekak agertzen dira Power Platform lokal datu atebideak ikusi eta konfiguratzeko ingurunea.</span><span class="sxs-lookup"><span data-stu-id="4f38d-120">The data sources page shows links to go the Power Platform environment where you can view and configure on-premises data gateways.</span></span>

:::image type="content" source="media/data-sources-onpremises-gateways.png" alt-text="Datu iturrien orriaren pantaila-argazkia Power Platform ingurunea.":::

## <a name="review-ingested-data"></a><span data-ttu-id="4f38d-122">Berrikusi sartutako datuak</span><span class="sxs-lookup"><span data-stu-id="4f38d-122">Review ingested data</span></span>

<span data-ttu-id="4f38d-123">Irentsitako datu-iturburu bakoitzaren izena, bere egoera eta iturri horretako datuak berritu ziren azken aldia ikusiko dituzu.</span><span class="sxs-lookup"><span data-stu-id="4f38d-123">You'll see the name of each ingested data source, its status, and the last time the data was refreshed for that source.</span></span> <span data-ttu-id="4f38d-124">Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="4f38d-124">You can sort the list of data sources by every column.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="4f38d-125">![Gehitutako datu-iturriak](media/configure-data-datasource-added.png "Gehitutako datu-iturriak")</span><span class="sxs-lookup"><span data-stu-id="4f38d-125">![Data source added](media/configure-data-datasource-added.png "Data source added")</span></span>

|<span data-ttu-id="4f38d-126">Egoera</span><span class="sxs-lookup"><span data-stu-id="4f38d-126">Status</span></span>  |<span data-ttu-id="4f38d-127">Deskribapena</span><span class="sxs-lookup"><span data-stu-id="4f38d-127">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="4f38d-128">Ongi egin da</span><span class="sxs-lookup"><span data-stu-id="4f38d-128">Successful</span></span>   |<span data-ttu-id="4f38d-129">Datu-iturburu sartu da **Freskatuta** zutabean denbora-tartea adierazten bada.</span><span class="sxs-lookup"><span data-stu-id="4f38d-129">Data source was successfully ingested if a time is mentioned in the **Refreshed** column.</span></span>
|<span data-ttu-id="4f38d-130">Ez da hasi</span><span class="sxs-lookup"><span data-stu-id="4f38d-130">Not started</span></span>   |<span data-ttu-id="4f38d-131">Datu-iturburuak oraindik ez du daturik sartu edo oraindik zirriborro moduan daude.</span><span class="sxs-lookup"><span data-stu-id="4f38d-131">The data source has no data ingested yet or still in draft mode.</span></span>         |
|<span data-ttu-id="4f38d-132">Freskatzen</span><span class="sxs-lookup"><span data-stu-id="4f38d-132">Refreshing</span></span>    |<span data-ttu-id="4f38d-133">Datuen horniketa martxan da.</span><span class="sxs-lookup"><span data-stu-id="4f38d-133">Data ingestion is in progress.</span></span> <span data-ttu-id="4f38d-134">Eragiketa hau bertan behera utzi dezakezu **Utzi freskagarria** herrian **Ekintzak** zutabea.</span><span class="sxs-lookup"><span data-stu-id="4f38d-134">You can cancel this operation by selecting **Stop refreshing** in the **Actions** column.</span></span> <span data-ttu-id="4f38d-135">datu-iturburu-en freskagarria gelditzeak azken freskatze egoeran itzuliko du.</span><span class="sxs-lookup"><span data-stu-id="4f38d-135">Stopping the refresh of a data source will revert it to its last refresh state.</span></span>       |
|<span data-ttu-id="4f38d-136">Ezin izan da egin</span><span class="sxs-lookup"><span data-stu-id="4f38d-136">Failed</span></span>     |<span data-ttu-id="4f38d-137">Datuen iradokizunak akatsak izan ditu.</span><span class="sxs-lookup"><span data-stu-id="4f38d-137">Data ingestion ran into errors.</span></span>         |

<span data-ttu-id="4f38d-138">Hautatu balioa **Egoera** datu-iturburu edozein zutabetan xehetasun gehiago berrikusteko.</span><span class="sxs-lookup"><span data-stu-id="4f38d-138">Select the value in the **Status** column of any data source to review more details.</span></span> <span data-ttu-id="4f38d-139">**Aurrerapenaren xehetasunak** panelean, zabaldu **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="4f38d-139">In the **Progress details** pane, expand **Data sources**.</span></span> <span data-ttu-id="4f38d-140">Aukeratu **Ikusi xehetasunak** freskatze egoerari buruzko xehetasun gehiago berrikusteko, erroreen xehetasunak eta beherako prozesuen eguneratzeak barne.</span><span class="sxs-lookup"><span data-stu-id="4f38d-140">Select **See details** for more information about the refresh status, including error details and downstream process updates.</span></span>

<span data-ttu-id="4f38d-141">Datuak kargatzea denbora har dezake.</span><span class="sxs-lookup"><span data-stu-id="4f38d-141">Loading data can take some time.</span></span> <span data-ttu-id="4f38d-142">Freskatu ondoren, iradokitako datuak berrikusi daitezke **erakundeak** orria.</span><span class="sxs-lookup"><span data-stu-id="4f38d-142">After a successful refresh, the ingested data can be reviewed from the **Entities** page.</span></span> <span data-ttu-id="4f38d-143">Informazio gehiago lortzeko, [Entitateak](entities.md).</span><span class="sxs-lookup"><span data-stu-id="4f38d-143">For more information, see [Entities](entities.md).</span></span>

## <a name="refresh-a-data-source"></a><span data-ttu-id="4f38d-144">Freskatu datu-iturburu bat</span><span class="sxs-lookup"><span data-stu-id="4f38d-144">Refresh a data source</span></span>

<span data-ttu-id="4f38d-145">Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera.</span><span class="sxs-lookup"><span data-stu-id="4f38d-145">Data sources can be refreshed on an automatic schedule or refreshed manually on demand.</span></span> 

<span data-ttu-id="4f38d-146">Joan **Administratzailea** > **Sistema** > [**Antolaketa**](system.md#schedule-tab) atalera sartutako datu-iturburu guztien freskatze antolatuak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="4f38d-146">Go to **Admin** > **System** > [**Schedule**](system.md#schedule-tab) to configure scheduled refreshes of all your ingested data sources.</span></span>

<span data-ttu-id="4f38d-147">Eskatu ahalako datu-iturburu bat freskatzeko, jarraitu urrats hauek:</span><span class="sxs-lookup"><span data-stu-id="4f38d-147">To refresh a data source on demand, follow these steps:</span></span>

1. <span data-ttu-id="4f38d-148">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**</span><span class="sxs-lookup"><span data-stu-id="4f38d-148">In audience insights, go to **Data** > **Data sources**</span></span>

2. <span data-ttu-id="4f38d-149">Hautatu freskatu nahi duzun datu-iturburuaren ondoko elipsi bertikala eta hautatu **Freskatu** goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="4f38d-149">Select the vertical ellipsis next to the data source you want to refresh and select **Refresh** from the drop-down list.</span></span>

3. <span data-ttu-id="4f38d-150">Datu-iturburua eskuz eguneratzeko aktibatuta dago.</span><span class="sxs-lookup"><span data-stu-id="4f38d-150">The data source is now triggered for a manual refresh.</span></span> <span data-ttu-id="4f38d-151">datu-iturburu freskatzeak entitatearen eskema eta datuak eguneratuko ditu datu-iturburu-en zehaztutako entitate guztientzat.</span><span class="sxs-lookup"><span data-stu-id="4f38d-151">Refreshing a data source will update both the entity schema and data for all the entities specified in the data source.</span></span>

4. <span data-ttu-id="4f38d-152">Aukeratu **Freskatzeari utzi** lehendik dagoen freskatzea bertan behera utzi nahi baduzu, eta datu-iturburua bere azken eguneratze-egoerara itzuliko da.</span><span class="sxs-lookup"><span data-stu-id="4f38d-152">Select **Stop refreshing** if you want to cancel an existing refresh and the data source will revert to its last refresh status.</span></span>

## <a name="delete-a-data-source"></a><span data-ttu-id="4f38d-153">Ezabatu datu-iturri bat</span><span class="sxs-lookup"><span data-stu-id="4f38d-153">Delete a data source</span></span>

1. <span data-ttu-id="4f38d-154">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="4f38d-154">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="4f38d-155">Hautatu kendu nahi duzun datu-iturburu ondoko elipsi bertikala eta hautatu **Ezabatu** goitibeherako menuan.</span><span class="sxs-lookup"><span data-stu-id="4f38d-155">Select the vertical ellipsis next to the data source you want to remove and select **Delete** from the drop-down menu.</span></span>

3. <span data-ttu-id="4f38d-156">Berretsi ezabatu nahi duzula.</span><span class="sxs-lookup"><span data-stu-id="4f38d-156">Confirm your deletion.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
