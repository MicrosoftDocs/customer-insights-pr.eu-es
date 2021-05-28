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
ms.openlocfilehash: 3c0b4690e18285aa37eef481b3cfac951884ead6
ms.sourcegitcommit: fcc94f55dc2dce84eae188d582801dc47696c9cc
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/20/2021
ms.locfileid: "6085515"
---
# <a name="data-sources-overview"></a><span data-ttu-id="c2384-103">Datuen iturburuen ikuspegi orokorra</span><span class="sxs-lookup"><span data-stu-id="c2384-103">Data sources overview</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="c2384-104">Dynamics 365 Customer Insights-eko hartzaileen xehetasunen gaitasuna iturburu multzo zabal bateko datuekin konektatzen da.</span><span class="sxs-lookup"><span data-stu-id="c2384-104">The audience insights capability in Dynamics 365 Customer Insights connects to data from a broad set of sources.</span></span> <span data-ttu-id="c2384-105">datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*.</span><span class="sxs-lookup"><span data-stu-id="c2384-105">Connecting to a data source is often referred to as the process of *data ingestion*.</span></span> <span data-ttu-id="c2384-106">Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.</span><span class="sxs-lookup"><span data-stu-id="c2384-106">After ingesting the data, you can [unify](data-unification.md) and take action on it.</span></span>

## <a name="add-a-data-source"></a><span data-ttu-id="c2384-107">Gehitu datu-iturburua</span><span class="sxs-lookup"><span data-stu-id="c2384-107">Add a data source</span></span>

<span data-ttu-id="c2384-108">datu-iturburu bat gehitzeko artikulu zehatzak ikusi, aukeratutako aukeraren arabera.</span><span class="sxs-lookup"><span data-stu-id="c2384-108">Refer to the detailed articles on how to add a data source, depending on which option you choose.</span></span>

<span data-ttu-id="c2384-109">datu-iturburu bat gehi dezakezu hiru modu nagusitan:</span><span class="sxs-lookup"><span data-stu-id="c2384-109">You can add a data source in three main ways:</span></span>

- [<span data-ttu-id="c2384-110">Dozenaka Power Query lokailuren bidez</span><span class="sxs-lookup"><span data-stu-id="c2384-110">Through dozens of Power Query connectors</span></span>](connect-power-query.md)
- [<span data-ttu-id="c2384-111">Hurrengotik Common Data Model-eko karpeta bat</span><span class="sxs-lookup"><span data-stu-id="c2384-111">From a Common Data Model folder</span></span>](connect-common-data-model.md)
- [<span data-ttu-id="c2384-112">Zuretik Common Data Service lakua</span><span class="sxs-lookup"><span data-stu-id="c2384-112">From your own Common Data Service lake</span></span>](connect-common-data-service-lake.md)

## <a name="add-data-from-on-premises-data-sources"></a><span data-ttu-id="c2384-113">Gehitu datuak lokal datu iturrietatik</span><span class="sxs-lookup"><span data-stu-id="c2384-113">Add data from on-premises data sources</span></span>

<span data-ttu-id="c2384-114">Oinarrian onartzen da lokal datu iturrietako datuak sartzea Audience Insights-en Power Platform datu-fluxuak.</span><span class="sxs-lookup"><span data-stu-id="c2384-114">Ingesting data from on-premises data sources in Audience Insights is supported based on Power Platform dataflows.</span></span> <span data-ttu-id="c2384-115">Datu-fluxuak Customer Insights-en gaitu daitezke [eskainiz Microsoft Dataverse inguruneko URLa](manage-environments.md#create-an-environment-in-an-existing-organization) ingurunea konfiguratzerakoan.</span><span class="sxs-lookup"><span data-stu-id="c2384-115">Dataflows can be enabled in Customer Insights by [providing the Microsoft Dataverse environment URL](manage-environments.md#create-an-environment-in-an-existing-organization) when setting up the environment.</span></span>

<span data-ttu-id="c2384-116">Elkartu ondoren sortzen diren datu iturriak Dataverse Customer Insights-ekin ingurunea erabiliko da [Power Platform datu-fluxuak](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) lehenetsiz.</span><span class="sxs-lookup"><span data-stu-id="c2384-116">Data sources that are created after associating a Dataverse environment with Customer Insights will use [Power Platform dataflows](/power-query/dataflows/overview-dataflows-across-power-platform-dynamics-365) by default.</span></span> <span data-ttu-id="c2384-117">Datu fluxuek konektibitate lokala onartzen dute datuetarako atebidea erabiliz.</span><span class="sxs-lookup"><span data-stu-id="c2384-117">Dataflows support on-premises connectivity using the data gateway.</span></span> <span data-ttu-id="c2384-118">Kendu eta sortu berriro Dataverse ingurunea [datuetarako atebide lokalen erabilerarekin](/powerapps/maker/data-platform/using-dataflows-with-on-premises-data.md) erlazionatu baino lehen zeuden datu-iturburuak.</span><span class="sxs-lookup"><span data-stu-id="c2384-118">Remove and recreate data sources that existed before a Dataverse environment was associated to [use the on-premises data gateways](/powerapps/maker/data-platform/using-dataflows-with-on-premises-data.md).</span></span>

<span data-ttu-id="c2384-119">Dagoen batetik datozen atebideak Power BI edo Power Apps ingurunea ikusgai egongo da eta Customer Insights-en berrerabili dezakezu.</span><span class="sxs-lookup"><span data-stu-id="c2384-119">Data gateways from an existing Power BI or Power Apps environment will be visible and you can reuse in Customer Insights.</span></span> <span data-ttu-id="c2384-120">Datu iturrien orrira joateko estekak agertzen dira Power Platform lokal datu atebideak ikusi eta konfiguratzeko ingurunea.</span><span class="sxs-lookup"><span data-stu-id="c2384-120">The data sources page shows links to go the Power Platform environment where you can view and configure on-premises data gateways.</span></span>

## <a name="review-ingested-data"></a><span data-ttu-id="c2384-121">Berrikusi sartutako datuak</span><span class="sxs-lookup"><span data-stu-id="c2384-121">Review ingested data</span></span>

<span data-ttu-id="c2384-122">Irentsitako datu-iturburu bakoitzaren izena, bere egoera eta iturri horretako datuak berritu ziren azken aldia ikusiko dituzu.</span><span class="sxs-lookup"><span data-stu-id="c2384-122">You'll see the name of each ingested data source, its status, and the last time the data was refreshed for that source.</span></span> <span data-ttu-id="c2384-123">Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="c2384-123">You can sort the list of data sources by every column.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c2384-124">![Gehitutako datu-iturriak](media/configure-data-datasource-added.png "Gehitutako datu-iturriak")</span><span class="sxs-lookup"><span data-stu-id="c2384-124">![Data source added](media/configure-data-datasource-added.png "Data source added")</span></span>

|<span data-ttu-id="c2384-125">Egoera</span><span class="sxs-lookup"><span data-stu-id="c2384-125">Status</span></span>  |<span data-ttu-id="c2384-126">Deskribapena</span><span class="sxs-lookup"><span data-stu-id="c2384-126">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="c2384-127">Ongi egin da</span><span class="sxs-lookup"><span data-stu-id="c2384-127">Successful</span></span>   |<span data-ttu-id="c2384-128">Datu-iturburu sartu da **Freskatuta** zutabean denbora-tartea adierazten bada.</span><span class="sxs-lookup"><span data-stu-id="c2384-128">Data source was successfully ingested if a time is mentioned in the **Refreshed** column.</span></span>
|<span data-ttu-id="c2384-129">Ez da hasi</span><span class="sxs-lookup"><span data-stu-id="c2384-129">Not started</span></span>   |<span data-ttu-id="c2384-130">Datu-iturburuak oraindik ez du daturik sartu edo oraindik zirriborro moduan daude.</span><span class="sxs-lookup"><span data-stu-id="c2384-130">The data source has no data ingested yet or still in draft mode.</span></span>         |
|<span data-ttu-id="c2384-131">Freskatzen</span><span class="sxs-lookup"><span data-stu-id="c2384-131">Refreshing</span></span>    |<span data-ttu-id="c2384-132">Datuen horniketa martxan da.</span><span class="sxs-lookup"><span data-stu-id="c2384-132">Data ingestion is in progress.</span></span> <span data-ttu-id="c2384-133">Eragiketa hau bertan behera utzi dezakezu **Utzi freskagarria** herrian **Ekintzak** zutabea.</span><span class="sxs-lookup"><span data-stu-id="c2384-133">You can cancel this operation by selecting **Stop refreshing** in the **Actions** column.</span></span> <span data-ttu-id="c2384-134">datu-iturburu-en freskagarria gelditzeak azken freskatze egoeran itzuliko du.</span><span class="sxs-lookup"><span data-stu-id="c2384-134">Stopping the refresh of a data source will revert it to its last refresh state.</span></span>       |
|<span data-ttu-id="c2384-135">Ezin izan da egin</span><span class="sxs-lookup"><span data-stu-id="c2384-135">Failed</span></span>     |<span data-ttu-id="c2384-136">Datuen iradokizunak akatsak izan ditu.</span><span class="sxs-lookup"><span data-stu-id="c2384-136">Data ingestion ran into errors.</span></span>         |

<span data-ttu-id="c2384-137">Hautatu balioa **Egoera** datu-iturburu edozein zutabetan xehetasun gehiago berrikusteko.</span><span class="sxs-lookup"><span data-stu-id="c2384-137">Select the value in the **Status** column of any data source to review more details.</span></span> <span data-ttu-id="c2384-138">**Aurrerapenaren xehetasunak** panelean, zabaldu **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="c2384-138">In the **Progress details** pane, expand **Data sources**.</span></span> <span data-ttu-id="c2384-139">Aukeratu **Ikusi xehetasunak** freskatze egoerari buruzko xehetasun gehiago berrikusteko, erroreen xehetasunak eta beherako prozesuen eguneratzeak barne.</span><span class="sxs-lookup"><span data-stu-id="c2384-139">Select **See details** for more information about the refresh status, including error details and downstream process updates.</span></span>

<span data-ttu-id="c2384-140">Datuak kargatzea denbora har dezake.</span><span class="sxs-lookup"><span data-stu-id="c2384-140">Loading data can take some time.</span></span> <span data-ttu-id="c2384-141">Freskatu ondoren, iradokitako datuak berrikusi daitezke **erakundeak** orria.</span><span class="sxs-lookup"><span data-stu-id="c2384-141">After a successful refresh, the ingested data can be reviewed from the **Entities** page.</span></span> <span data-ttu-id="c2384-142">Informazio gehiago lortzeko, [Entitateak](entities.md).</span><span class="sxs-lookup"><span data-stu-id="c2384-142">For more information, see [Entities](entities.md).</span></span>

## <a name="refresh-a-data-source"></a><span data-ttu-id="c2384-143">Freskatu datu-iturburu bat</span><span class="sxs-lookup"><span data-stu-id="c2384-143">Refresh a data source</span></span>

<span data-ttu-id="c2384-144">Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera.</span><span class="sxs-lookup"><span data-stu-id="c2384-144">Data sources can be refreshed on an automatic schedule or refreshed manually on demand.</span></span> 

<span data-ttu-id="c2384-145">Joan **Administratzailea** > **Sistema** > [**Antolaketa**](system.md#schedule-tab) atalera sartutako datu-iturburu guztien freskatze antolatuak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="c2384-145">Go to **Admin** > **System** > [**Schedule**](system.md#schedule-tab) to configure scheduled refreshes of all your ingested data sources.</span></span>

<span data-ttu-id="c2384-146">Eskatu ahalako datu-iturburu bat freskatzeko, jarraitu urrats hauek:</span><span class="sxs-lookup"><span data-stu-id="c2384-146">To refresh a data source on demand, follow these steps:</span></span>

1. <span data-ttu-id="c2384-147">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**</span><span class="sxs-lookup"><span data-stu-id="c2384-147">In audience insights, go to **Data** > **Data sources**</span></span>

2. <span data-ttu-id="c2384-148">Hautatu freskatu nahi duzun datu-iturburuaren ondoko elipsi bertikala eta hautatu **Freskatu** goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="c2384-148">Select the vertical ellipsis next to the data source you want to refresh and select **Refresh** from the drop-down list.</span></span>

3. <span data-ttu-id="c2384-149">Datu-iturburua eskuz eguneratzeko aktibatuta dago.</span><span class="sxs-lookup"><span data-stu-id="c2384-149">The data source is now triggered for a manual refresh.</span></span> <span data-ttu-id="c2384-150">datu-iturburu freskatzeak entitatearen eskema eta datuak eguneratuko ditu datu-iturburu-en zehaztutako entitate guztientzat.</span><span class="sxs-lookup"><span data-stu-id="c2384-150">Refreshing a data source will update both the entity schema and data for all the entities specified in the data source.</span></span>

4. <span data-ttu-id="c2384-151">Aukeratu **Freskatzeari utzi** lehendik dagoen freskatzea bertan behera utzi nahi baduzu, eta datu-iturburua bere azken eguneratze-egoerara itzuliko da.</span><span class="sxs-lookup"><span data-stu-id="c2384-151">Select **Stop refreshing** if you want to cancel an existing refresh and the data source will revert to its last refresh status.</span></span>

## <a name="delete-a-data-source"></a><span data-ttu-id="c2384-152">Ezabatu datu-iturri bat</span><span class="sxs-lookup"><span data-stu-id="c2384-152">Delete a data source</span></span>

1. <span data-ttu-id="c2384-153">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="c2384-153">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="c2384-154">Hautatu kendu nahi duzun datu-iturburu ondoko elipsi bertikala eta hautatu **Ezabatu** goitibeherako menuan.</span><span class="sxs-lookup"><span data-stu-id="c2384-154">Select the vertical ellipsis next to the data source you want to remove and select **Delete** from the drop-down menu.</span></span>

3. <span data-ttu-id="c2384-155">Berretsi ezabatu nahi duzula.</span><span class="sxs-lookup"><span data-stu-id="c2384-155">Confirm your deletion.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
