---
title: Erabili datu-iturburuak datuak sartzeko
description: Ikasi iturri desberdinetako datuak nola inportatu.
ms.date: 11/03/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
ms.openlocfilehash: a720641f7499fc71ff5bceeba48d296c51f77242
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643938"
---
# <a name="overview-about-data-sources"></a><span data-ttu-id="66262-103">Ikuspegi orokorra datu-iturburuei buruzkoa</span><span class="sxs-lookup"><span data-stu-id="66262-103">Overview about data sources</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="66262-104">Dynamics 365 Customer Insights-eko hartzaileen xehetasunen gaitasuna iturburu multzo zabal bateko datuekin konektatzen da.</span><span class="sxs-lookup"><span data-stu-id="66262-104">The audience insights capability in Dynamics 365 Customer Insights connects to data from a broad set of sources.</span></span> <span data-ttu-id="66262-105">datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*.</span><span class="sxs-lookup"><span data-stu-id="66262-105">Connecting to a data source is often referred to as the process of *data ingestion*.</span></span> <span data-ttu-id="66262-106">Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.</span><span class="sxs-lookup"><span data-stu-id="66262-106">After ingesting the data, you can [unify](data-unification.md) and take action on it.</span></span>

## <a name="add-a-data-source"></a><span data-ttu-id="66262-107">Gehitu datu-iturburua</span><span class="sxs-lookup"><span data-stu-id="66262-107">Add a data source</span></span>

<span data-ttu-id="66262-108">datu-iturburu bat gehitzeko artikulu zehatzak ikusi, aukeratutako aukeraren arabera.</span><span class="sxs-lookup"><span data-stu-id="66262-108">Refer to the detailed articles on how to add a data source, depending on which option you choose.</span></span>

<span data-ttu-id="66262-109">datu-iturburu bat gehi dezakezu hiru modu nagusitan:</span><span class="sxs-lookup"><span data-stu-id="66262-109">You can add a data source in three main ways:</span></span>

- [<span data-ttu-id="66262-110">Dozenaka Power Query lokailuren bidez</span><span class="sxs-lookup"><span data-stu-id="66262-110">Through dozens of Power Query connectors</span></span>](connect-power-query.md)
- [<span data-ttu-id="66262-111">Hurrengotik Common Data Model-eko karpeta bat</span><span class="sxs-lookup"><span data-stu-id="66262-111">From a Common Data Model folder</span></span>](connect-common-data-model.md)
- [<span data-ttu-id="66262-112">Zuretik Common Data Service lakua</span><span class="sxs-lookup"><span data-stu-id="66262-112">From your own Common Data Service lake</span></span>](connect-common-data-service-lake.md)

> [!NOTE]
> <span data-ttu-id="66262-113">Ezin dituzu lokal datu iturrietako datuak gehitu oraindik.</span><span class="sxs-lookup"><span data-stu-id="66262-113">You can't add data from on-premises data sources yet.</span></span>

## <a name="review-ingested-data"></a><span data-ttu-id="66262-114">Berrikusi sartutako datuak</span><span class="sxs-lookup"><span data-stu-id="66262-114">Review ingested data</span></span>

<span data-ttu-id="66262-115">Irentsitako datu-iturburu bakoitzaren izena, bere egoera eta iturri horretako datuak berritu ziren azken aldia ikusiko dituzu.</span><span class="sxs-lookup"><span data-stu-id="66262-115">You'll see the name of each ingested data source, its status, and the last time the data was refreshed for that source.</span></span> <span data-ttu-id="66262-116">Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="66262-116">You can sort the list of data sources by every column.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="66262-117">![Gehitutako datu-iturriak](media/configure-data-datasource-added.png "Gehitutako datu-iturriak")</span><span class="sxs-lookup"><span data-stu-id="66262-117">![Data source added](media/configure-data-datasource-added.png "Data source added")</span></span>

|<span data-ttu-id="66262-118">Egoera</span><span class="sxs-lookup"><span data-stu-id="66262-118">Status</span></span>  |<span data-ttu-id="66262-119">Deskribapena</span><span class="sxs-lookup"><span data-stu-id="66262-119">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="66262-120">Ongi egin da</span><span class="sxs-lookup"><span data-stu-id="66262-120">Successful</span></span>   |<span data-ttu-id="66262-121">Datu-iturburu sartu da **Freskatuta** zutabean denbora-tartea adierazten bada.</span><span class="sxs-lookup"><span data-stu-id="66262-121">Data source was successfully ingested if a time is mentioned in the **Refreshed** column.</span></span>
|<span data-ttu-id="66262-122">Ez da hasi</span><span class="sxs-lookup"><span data-stu-id="66262-122">Not started</span></span>   |<span data-ttu-id="66262-123">Datu-iturburuak oraindik ez du daturik sartu edo oraindik zirriborro moduan daude.</span><span class="sxs-lookup"><span data-stu-id="66262-123">The data source has no data ingested yet or still in draft mode.</span></span>         |
|<span data-ttu-id="66262-124">Freskatzen</span><span class="sxs-lookup"><span data-stu-id="66262-124">Refreshing</span></span>    |<span data-ttu-id="66262-125">Datuen horniketa martxan da.</span><span class="sxs-lookup"><span data-stu-id="66262-125">Data ingestion is in progress.</span></span> <span data-ttu-id="66262-126">Eragiketa hau bertan behera utzi dezakezu **Utzi freskagarria** herrian **Ekintzak** zutabea.</span><span class="sxs-lookup"><span data-stu-id="66262-126">You can cancel this operation by selecting **Stop refreshing** in the **Actions** column.</span></span> <span data-ttu-id="66262-127">datu-iturburu-en freskagarria gelditzeak azken freskatze egoeran itzuliko du.</span><span class="sxs-lookup"><span data-stu-id="66262-127">Stopping the refresh of a data source will revert it to its last refresh state.</span></span>       |
|<span data-ttu-id="66262-128">Ezin izan da egin</span><span class="sxs-lookup"><span data-stu-id="66262-128">Failed</span></span>     |<span data-ttu-id="66262-129">Datuen iradokizunak akatsak izan ditu.</span><span class="sxs-lookup"><span data-stu-id="66262-129">Data ingestion ran into errors.</span></span>         |

<span data-ttu-id="66262-130">Aukeratu **Freskatu egoera** freskatze egoerari buruzko xehetasun gehiago berrikusteko, erroreen xehetasunak eta beherako prozesuen eguneratzeak barne.</span><span class="sxs-lookup"><span data-stu-id="66262-130">Select **Refresh status** to review more details on the refresh status, including error details and downstream process updates.</span></span>

<span data-ttu-id="66262-131">Datuak kargatzea denbora har dezake.</span><span class="sxs-lookup"><span data-stu-id="66262-131">Loading data can take some time.</span></span> <span data-ttu-id="66262-132">Freskatu ondoren, iradokitako datuak berrikusi daitezke **erakundeak** orria.</span><span class="sxs-lookup"><span data-stu-id="66262-132">After a successful refresh, the ingested data can be reviewed from the **Entities** page.</span></span> <span data-ttu-id="66262-133">Informazio gehiago lortzeko, [Entitateak](entities.md).</span><span class="sxs-lookup"><span data-stu-id="66262-133">For more information, see [Entities](entities.md).</span></span>

## <a name="refresh-a-data-source"></a><span data-ttu-id="66262-134">Freskatu datu-iturburu bat</span><span class="sxs-lookup"><span data-stu-id="66262-134">Refresh a data source</span></span>

<span data-ttu-id="66262-135">Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera.</span><span class="sxs-lookup"><span data-stu-id="66262-135">Data sources can be refreshed on an automatic schedule or refreshed manually on demand.</span></span> 

<span data-ttu-id="66262-136">Joan **Administratzailea** > **Sistema** > [**Antolaketa**](system.md#schedule-tab) atalera sartutako datu-iturburu guztien freskatze antolatuak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="66262-136">Go to **Admin** > **System** > [**Schedule**](system.md#schedule-tab) to configure scheduled refreshes of all your ingested data sources.</span></span>

<span data-ttu-id="66262-137">Eskatu ahalako datu-iturburu bat freskatzeko, jarraitu urrats hauek:</span><span class="sxs-lookup"><span data-stu-id="66262-137">To refresh a data source on demand, follow these steps:</span></span>

1. <span data-ttu-id="66262-138">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**</span><span class="sxs-lookup"><span data-stu-id="66262-138">In audience insights, go to **Data** > **Data sources**</span></span>

2. <span data-ttu-id="66262-139">Hautatu freskatu nahi duzun datu-iturburuaren ondoko elipsi bertikala eta hautatu **Freskatu** goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="66262-139">Select the vertical ellipsis next to the data source you want to refresh and select **Refresh** from the drop-down list.</span></span>

3. <span data-ttu-id="66262-140">Datu-iturburua eskuz eguneratzeko aktibatuta dago.</span><span class="sxs-lookup"><span data-stu-id="66262-140">The data source is now triggered for a manual refresh.</span></span> <span data-ttu-id="66262-141">Datu-iturburua freskatuz gero, entitateen eskema zein datu-iturburuan zehaztutako entitateetako datuak eguneratuko dira.</span><span class="sxs-lookup"><span data-stu-id="66262-141">Refreshing a data source will update both the entity schema as well as data for all the entities specified in the data source.</span></span>

4. <span data-ttu-id="66262-142">Aukeratu **Freskatzeari utzi** lehendik dagoen freskatzea bertan behera utzi nahi baduzu, eta datu-iturburua bere azken eguneratze-egoerara itzuliko da.</span><span class="sxs-lookup"><span data-stu-id="66262-142">Select **Stop refreshing** if you want to cancel an existing refresh and the data source will revert to its last refresh status.</span></span>

## <a name="delete-a-data-source"></a><span data-ttu-id="66262-143">Ezabatu datu-iturri bat</span><span class="sxs-lookup"><span data-stu-id="66262-143">Delete a data source</span></span>

1. <span data-ttu-id="66262-144">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="66262-144">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="66262-145">Hautatu kendu nahi duzun datu-iturburu ondoko elipsi bertikala eta hautatu **Ezabatu** goitibeherako menuan.</span><span class="sxs-lookup"><span data-stu-id="66262-145">Select the vertical ellipsis next to the data source you want to remove and select **Delete** from the drop-down menu.</span></span>

3. <span data-ttu-id="66262-146">Berretsi ezabatu nahi duzula.</span><span class="sxs-lookup"><span data-stu-id="66262-146">Confirm your deletion.</span></span>
