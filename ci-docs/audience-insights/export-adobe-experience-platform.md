---
title: Esportatu Customer Insights datuak Adobe Experience Platform-era
description: Ikusi audientzia estatistiken segmentuak nola erabiltzen diren Adobe Experience Platform-en.
ms.date: 02/26/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: d1856861562be55c6d1d051050fe965560fa42f8
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596254"
---
# <a name="use-customer-insights-segments-in-adobe-experience-platform-preview"></a><span data-ttu-id="8b886-103">Erabili Customer Insights segmentuak nola erabiltzen diren Adobe Experience Platform-en (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="8b886-103">Use Customer Insights segments in Adobe Experience Platform (preview)</span></span>

<span data-ttu-id="8b886-104">Erabiltzaileentzako ikusleen estatistiken erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortzea zure marketin kanpainak eraginkorragoak izan daitezen publiko garrantzitsuei zuzenduta.</span><span class="sxs-lookup"><span data-stu-id="8b886-104">As a user of audience insights for Dynamics 365 Customer Insights, you may have created segments to make your marketing campaigns more efficient by targeting relevant audiences.</span></span> <span data-ttu-id="8b886-105">Adobe Experience Platform-eko eta Adobe Campaign Standard bezalako aplikazioetako audientziaren inguruko segmentu bat erabiltzeko, artikulu honetan zehaztutako urrats batzuk jarraitu behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="8b886-105">To use a segment from audience insights in Adobe Experience Platform and applications like Adobe Campaign Standard, you need to follow a few steps outlined in this article.</span></span>

:::image type="content" source="media/AEP-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a><span data-ttu-id="8b886-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="8b886-107">Prerequisites</span></span>

-   <span data-ttu-id="8b886-108">Dynamics 365 Customer Insights lizentzia</span><span class="sxs-lookup"><span data-stu-id="8b886-108">Dynamics 365 Customer Insights license</span></span>
-   <span data-ttu-id="8b886-109">Adobe Experience Platform lizentzia</span><span class="sxs-lookup"><span data-stu-id="8b886-109">Adobe Experience Platform license</span></span>
-   <span data-ttu-id="8b886-110">Adobe Campaign Standard lizentzia</span><span class="sxs-lookup"><span data-stu-id="8b886-110">Adobe Campaign Standard license</span></span>
-   <span data-ttu-id="8b886-111">Azure blob-biltegia kontua</span><span class="sxs-lookup"><span data-stu-id="8b886-111">Azure Blob Storage account</span></span>

## <a name="campaign-overview"></a><span data-ttu-id="8b886-112">Kanpainaren informazio orokorra</span><span class="sxs-lookup"><span data-stu-id="8b886-112">Campaign Overview</span></span>

<span data-ttu-id="8b886-113">Adobe Experience Platform-en audientzia estatistiketatik segmentuak nola erabil ditzakezun hobeto ulertzeko, ikus dezagun fikziozko lagin kanpaina.</span><span class="sxs-lookup"><span data-stu-id="8b886-113">To better understand how you can use segments from audience insights in Adobe Experience Platform, let’s look at a fictitious sample campaign.</span></span>

<span data-ttu-id="8b886-114">Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei.</span><span class="sxs-lookup"><span data-stu-id="8b886-114">Let’s assume that your company offers a monthly, subscription-based service to your customers in the United States.</span></span> <span data-ttu-id="8b886-115">Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu.</span><span class="sxs-lookup"><span data-stu-id="8b886-115">You want to identify customers whose subscriptions are due for renewal in the next eight days but haven't yet renewed their subscription.</span></span> <span data-ttu-id="8b886-116">Bezero horiek mantentzeko, promozio eskaintza posta elektroniko bidez bidali nahi diezu, Adobe Experience Platform erabiliz.</span><span class="sxs-lookup"><span data-stu-id="8b886-116">To keep these customers, you want to send them a promotional offer via email, using Adobe Experience Platform.</span></span>

<span data-ttu-id="8b886-117">Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu.</span><span class="sxs-lookup"><span data-stu-id="8b886-117">In this example, we want to run the promotional email campaign once.</span></span> <span data-ttu-id="8b886-118">Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen.</span><span class="sxs-lookup"><span data-stu-id="8b886-118">This article doesn’t cover the use-case of running the campaign more than once.</span></span>

## <a name="identify-your-target-audience"></a><span data-ttu-id="8b886-119">Identifikatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="8b886-119">Identify your target audience</span></span>

<span data-ttu-id="8b886-120">Gure eszenatokian, bezeroen helbide elektronikoak ikusleen estatistiketan eskuragarri daudela eta haien promozio hobespenak segmentuko kideak identifikatzeko aztertu direla suposatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="8b886-120">In our scenario, we assume that the email addresses of the customers are available in audience insights and their promotional preferences were analyzed to identify members of the segment.</span></span>

<span data-ttu-id="8b886-121">[Ikusleen estatistiketan definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero hauei posta elektroniko bidezko promozioa bidaltzeko asmoa duzu.</span><span class="sxs-lookup"><span data-stu-id="8b886-121">The [segment you defined in audience insights](segments.md) is called **ChurnProneCustomers** and you plan to send these customers the email promotion.</span></span>

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

<span data-ttu-id="8b886-123">Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira.</span><span class="sxs-lookup"><span data-stu-id="8b886-123">The offer email that you want to send out will contain the first name, last name, and the subscription end date of the customer.</span></span> <span data-ttu-id="8b886-124">Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.</span><span class="sxs-lookup"><span data-stu-id="8b886-124">It informs the customers about the discount they’ll get if they renew their subscription before it ends.</span></span>

## <a name="export-your-target-audience"></a><span data-ttu-id="8b886-125">Esportatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="8b886-125">Export your target audience</span></span>

<span data-ttu-id="8b886-126">Gure xede-audientzia identifikatuta, esportazioen konfigurazioa konfiguratu ahal izango dugu ikusleen estatistiketatik Azure blob-biltegia kontura.</span><span class="sxs-lookup"><span data-stu-id="8b886-126">With our target audience identified, we can configure the export from audience insights to an Azure Blob Storage account.</span></span>

1. <span data-ttu-id="8b886-127">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="8b886-127">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="8b886-128">Hurrengoan **Azure blob-biltegia** fitxa, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="8b886-128">In the **Azure Blob Storage** tile, select **Set up**.</span></span>

   :::image type="content" source="media/export-azure-blob-storage-tile.png" alt-text="Azure blob-biltegiko konfigurazio lauza.":::

1. <span data-ttu-id="8b886-130">Eman **Bistaratzeko izena** esportazio helmuga berri honetarako eta ondoren sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** segmentua esportatu nahi duzun Azure blob-biltegia kontukoa.</span><span class="sxs-lookup"><span data-stu-id="8b886-130">Provide a **Display name** for this new export destination and then enter the **Account name**, **Account key**, and **Container** of the Azure Blob Storage account where you want to export the segment to.</span></span>  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 

   - <span data-ttu-id="8b886-132">Azure Blob biltegiratze kontuaren izena eta kontuaren gakoa aurkitzeko informazio gehiago lortzeko, ikus [Kudeatu biltegiratze kontuen ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="8b886-132">To learn more about how to find the Azure Blob storage account name and account key, see [Manage storage account settings in the Azure portal](/azure/storage/common/storage-account-manage).</span></span>

   - <span data-ttu-id="8b886-133">Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span><span class="sxs-lookup"><span data-stu-id="8b886-133">To learn how to create a container, see [Create a container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span></span>

1. <span data-ttu-id="8b886-134">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="8b886-134">Select **Next**.</span></span>

1. <span data-ttu-id="8b886-135">Aukeratu esportatu nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="8b886-135">Choose the segment that you want to export.</span></span> <span data-ttu-id="8b886-136">Adibide honetan, **ChurnProneCustomers** da.</span><span class="sxs-lookup"><span data-stu-id="8b886-136">In this example, it’s **ChurnProneCustomers**.</span></span>

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. <span data-ttu-id="8b886-138">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="8b886-138">Select **Save**.</span></span>

<span data-ttu-id="8b886-139">Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Administratzailea** > **Esportazioak** > **Nire esportazio helmugak**.</span><span class="sxs-lookup"><span data-stu-id="8b886-139">After saving the export destination, you find it on **Admin** > **Exports** > **My export destinations**.</span></span>

:::image type="content" source="media/export-destination-azure-blob-storage.png" alt-text="Pantaila-argazkia esportazioen zerrenda eta lagin-segmentua nabarmenduta.":::

<span data-ttu-id="8b886-141">Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#export-data-on-demand).</span><span class="sxs-lookup"><span data-stu-id="8b886-141">You can now [export the segment on demand](export-destinations.md#export-data-on-demand).</span></span> <span data-ttu-id="8b886-142">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).</span><span class="sxs-lookup"><span data-stu-id="8b886-142">The export will also run with every [scheduled refresh](system.md).</span></span>

> [!NOTE]
> <span data-ttu-id="8b886-143">Ziurtatu esportatutako segmentuan erregistro kopurua Adobe Campaign Standard lizentziaren baimendutako mugaren barruan dagoela.</span><span class="sxs-lookup"><span data-stu-id="8b886-143">Ensure that the number of records in the exported segment are within the allowed limit of your Adobe Campaign Standard license.</span></span>

<span data-ttu-id="8b886-144">Esportatutako datuak goian konfiguratu duzun Azure blob-biltegia edukiontzian gordetzen dira.</span><span class="sxs-lookup"><span data-stu-id="8b886-144">Exported data is stored in the Azure Blob storage container you configured above.</span></span> <span data-ttu-id="8b886-145">Karpeta bide hau automatikoki sortzen da zure edukiontzian:</span><span class="sxs-lookup"><span data-stu-id="8b886-145">The following folder path is automatically created in your container:</span></span>

<span data-ttu-id="8b886-146">*%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*</span><span class="sxs-lookup"><span data-stu-id="8b886-146">*%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*</span></span>

<span data-ttu-id="8b886-147">Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/ChurnSegmentDemo/2021/02/16/1433/ChurnProneCustomers_1.csv</span><span class="sxs-lookup"><span data-stu-id="8b886-147">Example: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/ChurnSegmentDemo/2021/02/16/1433/ChurnProneCustomers_1.csv</span></span>

<span data-ttu-id="8b886-148">*Eredua.json* esportatutako entitateak *%ExportDestinationName%* maila.</span><span class="sxs-lookup"><span data-stu-id="8b886-148">The *model.json* for the exported entities resides at the *%ExportDestinationName%* level.</span></span>

<span data-ttu-id="8b886-149">Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo/model.json</span><span class="sxs-lookup"><span data-stu-id="8b886-149">Example: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo/model.json</span></span>

## <a name="define-experience-data-model-xdm-in-adobe-experience-platform"></a><span data-ttu-id="8b886-150">Definitu Experience Data Model (XDM) Adobe Experience Platform-en</span><span class="sxs-lookup"><span data-stu-id="8b886-150">Define Experience Data Model (XDM) in Adobe Experience Platform</span></span>

<span data-ttu-id="8b886-151">Audientzia estatistiketatik esportatutako datuak Adobe Experience Platform programan erabili aurretik, Experience Data Model eskema eta [konfiguratu datuak denbora errealean bezeroaren profilerako](https://experienceleague.adobe.com/docs/experience-platform/profile/tutorials/dataset-configuration.html#tutorials).</span><span class="sxs-lookup"><span data-stu-id="8b886-151">Before the exported data from audience insights can be used within Adobe Experience Platform, we need to define the Experience Data Model schema and [configure the data for the Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/tutorials/dataset-configuration.html#tutorials).</span></span>

<span data-ttu-id="8b886-152">Ikasi [zer den XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) eta ulertu [eskemaren konposizioaren oinarriak](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schema).</span><span class="sxs-lookup"><span data-stu-id="8b886-152">Learn [what XDM is](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) and understand the [basics of schema composition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schema).</span></span>

## <a name="import-data-into-adobe-experience-platform"></a><span data-ttu-id="8b886-153">Inportatu datuak Adobe Experience Platformera</span><span class="sxs-lookup"><span data-stu-id="8b886-153">Import data into Adobe Experience Platform</span></span>

<span data-ttu-id="8b886-154">Dena indarrean dagoela, entzuleen datuetatik prestatutako audientzia datuak Adobe Experience Platformera inportatu behar ditugu.</span><span class="sxs-lookup"><span data-stu-id="8b886-154">Now that everything is in place, we need to import the prepared audience data from audience insights into Adobe Experience Platform.</span></span>

<span data-ttu-id="8b886-155">Lehenik eta behin, [sortu Azure blob-biltegia iturburu konexioa](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/blob.html#getting-started).</span><span class="sxs-lookup"><span data-stu-id="8b886-155">First, [create an Azure Blob Storage source connection](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/blob.html#getting-started).</span></span>    

<span data-ttu-id="8b886-156">Iturburu konexioa definitu ondoren, [konfiguratu datu-fluxua](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html#ui-tutorials) hodeiko biltegiratze batch konexiorako segmentuen irteera audientzia estatistiketatik Adobe Experience Platformera inportatzeko.</span><span class="sxs-lookup"><span data-stu-id="8b886-156">After defining the source connection, [configure a dataflow](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html#ui-tutorials) for a cloud storage batch connection to import the segment output from audience insights into Adobe Experience Platform.</span></span>

## <a name="create-an-audience-in-adobe-campaign-standard"></a><span data-ttu-id="8b886-157">Sortu audientzia Adobe Campaign Standard zerbitzuan</span><span class="sxs-lookup"><span data-stu-id="8b886-157">Create an audience in Adobe Campaign Standard</span></span>

<span data-ttu-id="8b886-158">Kanpaina honen mezu elektronikoa bidaltzeko, Adobe Campaign Standard erabiliko dugu.</span><span class="sxs-lookup"><span data-stu-id="8b886-158">To send the email for this campaign, we will use Adobe Campaign Standard.</span></span> <span data-ttu-id="8b886-159">Datuak Adobe Experience Platform-era inportatu ondoren, behar dugu [audientzia sortu](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/get-started-profiles-and-audiences.html#permission) Adobe Campaign Standard-n Adobe Experience Platform-eko datuak erabiliz.</span><span class="sxs-lookup"><span data-stu-id="8b886-159">After importing the data into Adobe Experience Platform, we need to [create an audience](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/get-started-profiles-and-audiences.html#permission) in Adobe Campaign Standard using the data in Adobe Experience Platform.</span></span>

<span data-ttu-id="8b886-160">Ikasi nola egin [erabili segmentu eraikitzailea](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/working-with-adobe-experience-platform/aep-using-segment-builder.html#building-a-segment) Adobe Campaign Standard-en Adobe Experience Platform-eko datuetan oinarritutako audientzia definitzeko.</span><span class="sxs-lookup"><span data-stu-id="8b886-160">Learn how to [use segment builder](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/working-with-adobe-experience-platform/aep-using-segment-builder.html#building-a-segment) in Adobe Campaign Standard to define an audience based on the data in Adobe Experience Platform.</span></span>

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a><span data-ttu-id="8b886-161">Sortu eta bidali mezu elektronikoa Adobe Campaign Standard erabiliz</span><span class="sxs-lookup"><span data-stu-id="8b886-161">Create and send the email using Adobe Campaign Standard</span></span>

<span data-ttu-id="8b886-162">Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.</span><span class="sxs-lookup"><span data-stu-id="8b886-162">Create the email content and then [test and send](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) your email.</span></span>

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Adobe Campaign Standard-ren berritze-eskaintza duen posta elektronikoa.":::