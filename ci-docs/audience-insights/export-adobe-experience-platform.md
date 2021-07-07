---
title: Esportatu Customer Insights datuak Adobe Experience Platform-era
description: Ikusi audientzia estatistiken segmentuak nola erabiltzen diren Adobe Experience Platform-en.
ms.date: 03/29/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: 1045d0e373fd5ea8987684e51bd9a07b7b535ee3
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305509"
---
# <a name="use-customer-insights-segments-in-adobe-experience-platform-preview"></a><span data-ttu-id="49c69-103">Erabili Customer Insights segmentuak nola erabiltzen diren Adobe Experience Platform-en (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="49c69-103">Use Customer Insights segments in Adobe Experience Platform (preview)</span></span>

<span data-ttu-id="49c69-104">-N ikusleei buruzko informazioaren erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortzea zure marketin kanpainak eraginkorragoak izan daitezen publiko garrantzitsuei zuzenduta.</span><span class="sxs-lookup"><span data-stu-id="49c69-104">As a user of audience insights in Dynamics 365 Customer Insights, you may have created segments to make your marketing campaigns more efficient by targeting relevant audiences.</span></span> <span data-ttu-id="49c69-105">Adobe Experience Platform-eko eta Adobe Campaign Standard bezalako aplikazioetako audientziaren inguruko segmentu bat erabiltzeko, artikulu honetan zehaztutako urrats batzuk jarraitu behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="49c69-105">To use a segment from audience insights in Adobe Experience Platform and applications like Adobe Campaign Standard, you need to follow a few steps outlined in this article.</span></span>

:::image type="content" source="media/AEP-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a><span data-ttu-id="49c69-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="49c69-107">Prerequisites</span></span>

-   <span data-ttu-id="49c69-108">Dynamics 365 Customer Insights lizentzia</span><span class="sxs-lookup"><span data-stu-id="49c69-108">Dynamics 365 Customer Insights license</span></span>
-   <span data-ttu-id="49c69-109">Adobe Experience Platform lizentzia</span><span class="sxs-lookup"><span data-stu-id="49c69-109">Adobe Experience Platform license</span></span>
-   <span data-ttu-id="49c69-110">Adobe Campaign Standard lizentzia</span><span class="sxs-lookup"><span data-stu-id="49c69-110">Adobe Campaign Standard license</span></span>
-   <span data-ttu-id="49c69-111">Azure blob-biltegia kontua</span><span class="sxs-lookup"><span data-stu-id="49c69-111">Azure Blob Storage account</span></span>

## <a name="campaign-overview"></a><span data-ttu-id="49c69-112">Kanpainaren informazio orokorra</span><span class="sxs-lookup"><span data-stu-id="49c69-112">Campaign Overview</span></span>

<span data-ttu-id="49c69-113">Adobe Experience Platform-en audientzia estatistiketatik segmentuak nola erabil ditzakezun hobeto ulertzeko, ikus dezagun fikziozko lagin kanpaina.</span><span class="sxs-lookup"><span data-stu-id="49c69-113">To better understand how you can use segments from audience insights in Adobe Experience Platform, let’s look at a fictitious sample campaign.</span></span>

<span data-ttu-id="49c69-114">Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei.</span><span class="sxs-lookup"><span data-stu-id="49c69-114">Let’s assume that your company offers a monthly, subscription-based service to your customers in the United States.</span></span> <span data-ttu-id="49c69-115">Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu.</span><span class="sxs-lookup"><span data-stu-id="49c69-115">You want to identify customers whose subscriptions are due for renewal in the next eight days but haven't yet renewed their subscription.</span></span> <span data-ttu-id="49c69-116">Bezero horiek mantentzeko, promozio eskaintza posta elektroniko bidez bidali nahi diezu, Adobe Experience Platform erabiliz.</span><span class="sxs-lookup"><span data-stu-id="49c69-116">To keep these customers, you want to send them a promotional offer via email, using Adobe Experience Platform.</span></span>

<span data-ttu-id="49c69-117">Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu.</span><span class="sxs-lookup"><span data-stu-id="49c69-117">In this example, we want to run the promotional email campaign once.</span></span> <span data-ttu-id="49c69-118">Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen.</span><span class="sxs-lookup"><span data-stu-id="49c69-118">This article doesn’t cover the use-case of running the campaign more than once.</span></span>

## <a name="identify-your-target-audience"></a><span data-ttu-id="49c69-119">Identifikatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="49c69-119">Identify your target audience</span></span>

<span data-ttu-id="49c69-120">Gure eszenatokian, bezeroen helbide elektronikoak ikusleen estatistiketan eskuragarri daudela eta haien promozio hobespenak segmentuko kideak identifikatzeko aztertu direla suposatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="49c69-120">In our scenario, we assume that the email addresses of the customers are available in audience insights and their promotional preferences were analyzed to identify members of the segment.</span></span>

<span data-ttu-id="49c69-121">[Ikusleen estatistiketan definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero hauei posta elektroniko bidezko promozioa bidaltzeko asmoa duzu.</span><span class="sxs-lookup"><span data-stu-id="49c69-121">The [segment you defined in audience insights](segments.md) is called **ChurnProneCustomers** and you plan to send these customers the email promotion.</span></span>

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

<span data-ttu-id="49c69-123">Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira.</span><span class="sxs-lookup"><span data-stu-id="49c69-123">The offer email that you want to send out will contain the first name, last name, and the subscription end date of the customer.</span></span> <span data-ttu-id="49c69-124">Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.</span><span class="sxs-lookup"><span data-stu-id="49c69-124">It informs the customers about the discount they’ll get if they renew their subscription before it ends.</span></span>

## <a name="export-your-target-audience"></a><span data-ttu-id="49c69-125">Esportatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="49c69-125">Export your target audience</span></span>

<span data-ttu-id="49c69-126">Gure xede-audientzia identifikatuta, esportazioen konfigurazioa konfiguratu ahal izango dugu ikusleen estatistiketatik Azure blob-biltegia kontura.</span><span class="sxs-lookup"><span data-stu-id="49c69-126">With our target audience identified, we can configure the export from audience insights to an Azure Blob Storage account.</span></span>

### <a name="configure-a-connection"></a><span data-ttu-id="49c69-127">Konfiguratu konexioa</span><span class="sxs-lookup"><span data-stu-id="49c69-127">Configure a connection</span></span>

1. <span data-ttu-id="49c69-128">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="49c69-128">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="49c69-129">Aukeratu **Gehitu konexioa** eta aukeratu **Azure blob biltegiratzea** edo hautatu **Konfiguratu** urtean **Azure blob biltegiratzea** lauza konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="49c69-129">Select **Add connection** and choose **Azure Blob Storage** or select **Set up** in the **Azure Blob Storage** tile to configure the connection.</span></span>

   :::image type="content" source="media/export-azure-blob-storage-tile.png" alt-text="Azure blob-biltegiko konfigurazio lauza."::: 

1. <span data-ttu-id="49c69-131">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="49c69-131">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="49c69-132">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="49c69-132">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="49c69-133">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="49c69-133">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="49c69-134">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="49c69-134">Choose who can use this connection.</span></span> <span data-ttu-id="49c69-135">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="49c69-135">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="49c69-136">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="49c69-136">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="49c69-137">Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** segmentua esportatu nahi duzun Blob Storage konturako.</span><span class="sxs-lookup"><span data-stu-id="49c69-137">Enter **Account name**, **Account key**, and **Container** for your Blob Storage account where you want to export the segment to.</span></span>  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 
   
    - <span data-ttu-id="49c69-139">Blob Storage kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="49c69-139">To learn more about how to find the Blob Storage account name and account key, see [Manage storage account settings in the Azure portal](/azure/storage/common/storage-account-manage).</span></span>
    - <span data-ttu-id="49c69-140">Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span><span class="sxs-lookup"><span data-stu-id="49c69-140">To learn how to create a container, see [Create a container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span></span>

1. <span data-ttu-id="49c69-141">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="49c69-141">Select **Save** to complete the connection.</span></span> 

### <a name="configure-an-export"></a><span data-ttu-id="49c69-142">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="49c69-142">Configure an export</span></span>

<span data-ttu-id="49c69-143">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="49c69-143">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="49c69-144">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="49c69-144">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="49c69-145">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="49c69-145">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="49c69-146">Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.</span><span class="sxs-lookup"><span data-stu-id="49c69-146">To create a new export, select **Add export**.</span></span>

1. <span data-ttu-id="49c69-147">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Azure Blob biltegiaren sekzioan.</span><span class="sxs-lookup"><span data-stu-id="49c69-147">In the **Connection for export** field, choose a connection from the Azure Blob Storage section.</span></span> <span data-ttu-id="49c69-148">Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.</span><span class="sxs-lookup"><span data-stu-id="49c69-148">If you don't see this section name, then no connections of this type are available to you.</span></span>

1. <span data-ttu-id="49c69-149">Aukeratu esportatu nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="49c69-149">Choose the segment that you want to export.</span></span> <span data-ttu-id="49c69-150">Adibide honetan, **ChurnProneCustomers** da.</span><span class="sxs-lookup"><span data-stu-id="49c69-150">In this example, it’s **ChurnProneCustomers**.</span></span>

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. <span data-ttu-id="49c69-152">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="49c69-152">Select **Save**.</span></span>

<span data-ttu-id="49c69-153">Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="49c69-153">After saving the export destination, you find it on **Data** > **Exports**.</span></span>

<span data-ttu-id="49c69-154">Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="49c69-154">You can now [export the segment on demand](export-destinations.md#run-exports-on-demand).</span></span> <span data-ttu-id="49c69-155">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).</span><span class="sxs-lookup"><span data-stu-id="49c69-155">The export will also run with every [scheduled refresh](system.md).</span></span>

> [!NOTE]
> <span data-ttu-id="49c69-156">Ziurtatu esportatutako segmentuan erregistro kopurua Adobe Campaign Standard lizentziaren baimendutako mugaren barruan dagoela.</span><span class="sxs-lookup"><span data-stu-id="49c69-156">Ensure that the number of records in the exported segment are within the allowed limit of your Adobe Campaign Standard license.</span></span>

<span data-ttu-id="49c69-157">Esportatutako datuak goian konfiguratu duzun Azure blob Storage edukiontzian gordetzen dira.</span><span class="sxs-lookup"><span data-stu-id="49c69-157">Exported data is stored in the Azure Blob Storage container you configured above.</span></span> <span data-ttu-id="49c69-158">Karpeta bide hau automatikoki sortzen da zure edukiontzian:</span><span class="sxs-lookup"><span data-stu-id="49c69-158">The following folder path is automatically created in your container:</span></span>

<span data-ttu-id="49c69-159">*%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*</span><span class="sxs-lookup"><span data-stu-id="49c69-159">*%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*</span></span>

<span data-ttu-id="49c69-160">Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/ChurnSegmentDemo/2021/02/16/1433/ChurnProneCustomers_1.csv</span><span class="sxs-lookup"><span data-stu-id="49c69-160">Example: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/ChurnSegmentDemo/2021/02/16/1433/ChurnProneCustomers_1.csv</span></span>

<span data-ttu-id="49c69-161">*Eredua.json* esportatutako entitateak *%ExportDestinationName%* maila.</span><span class="sxs-lookup"><span data-stu-id="49c69-161">The *model.json* for the exported entities resides at the *%ExportDestinationName%* level.</span></span>

<span data-ttu-id="49c69-162">Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo/model.json</span><span class="sxs-lookup"><span data-stu-id="49c69-162">Example: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo/model.json</span></span>

## <a name="define-experience-data-model-xdm-in-adobe-experience-platform"></a><span data-ttu-id="49c69-163">Definitu Experience Data Model (XDM) Adobe Experience Platform-en</span><span class="sxs-lookup"><span data-stu-id="49c69-163">Define Experience Data Model (XDM) in Adobe Experience Platform</span></span>

<span data-ttu-id="49c69-164">Audientzia estatistiketatik esportatutako datuak Adobe Experience Platform programan erabili aurretik, Experience Data Model eskema eta [konfiguratu datuak denbora errealean bezeroaren profilerako](https://experienceleague.adobe.com/docs/experience-platform/profile/tutorials/dataset-configuration.html#tutorials).</span><span class="sxs-lookup"><span data-stu-id="49c69-164">Before the exported data from audience insights can be used within Adobe Experience Platform, we need to define the Experience Data Model schema and [configure the data for the Real-time Customer Profile](https://experienceleague.adobe.com/docs/experience-platform/profile/tutorials/dataset-configuration.html#tutorials).</span></span>

<span data-ttu-id="49c69-165">Ikasi [zer den XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) eta ulertu [eskemaren konposizioaren oinarriak](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schema).</span><span class="sxs-lookup"><span data-stu-id="49c69-165">Learn [what XDM is](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) and understand the [basics of schema composition](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schema).</span></span>

## <a name="import-data-into-adobe-experience-platform"></a><span data-ttu-id="49c69-166">Inportatu datuak Adobe Experience Platformera</span><span class="sxs-lookup"><span data-stu-id="49c69-166">Import data into Adobe Experience Platform</span></span>

<span data-ttu-id="49c69-167">Dena indarrean dagoela, entzuleen datuetatik prestatutako audientzia datuak Adobe Experience Platformera inportatu behar ditugu.</span><span class="sxs-lookup"><span data-stu-id="49c69-167">Now that everything is in place, we need to import the prepared audience data from audience insights into Adobe Experience Platform.</span></span>

<span data-ttu-id="49c69-168">Lehenik eta behin, [sortu Azure blob-biltegia iturburu konexioa](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/blob.html#getting-started).</span><span class="sxs-lookup"><span data-stu-id="49c69-168">First, [create an Azure Blob Storage source connection](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/blob.html#getting-started).</span></span>    

<span data-ttu-id="49c69-169">Iturburu konexioa definitu ondoren, [konfiguratu datu-fluxua](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html#ui-tutorials) hodeiko biltegiratze batch konexiorako segmentuen irteera audientzia estatistiketatik Adobe Experience Platformera inportatzeko.</span><span class="sxs-lookup"><span data-stu-id="49c69-169">After defining the source connection, [configure a dataflow](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html#ui-tutorials) for a cloud storage batch connection to import the segment output from audience insights into Adobe Experience Platform.</span></span>

## <a name="create-an-audience-in-adobe-campaign-standard"></a><span data-ttu-id="49c69-170">Sortu audientzia Adobe Campaign Standard zerbitzuan</span><span class="sxs-lookup"><span data-stu-id="49c69-170">Create an audience in Adobe Campaign Standard</span></span>

<span data-ttu-id="49c69-171">Kanpaina honen mezu elektronikoa bidaltzeko, Adobe Campaign Standard erabiliko dugu.</span><span class="sxs-lookup"><span data-stu-id="49c69-171">To send the email for this campaign, we'll use Adobe Campaign Standard.</span></span> <span data-ttu-id="49c69-172">Datuak Adobe Experience Platform-era inportatu ondoren, behar dugu [audientzia sortu](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/get-started-profiles-and-audiences.html#permission) Adobe Campaign Standard-n Adobe Experience Platform-eko datuak erabiliz.</span><span class="sxs-lookup"><span data-stu-id="49c69-172">After importing the data into Adobe Experience Platform, we need to [create an audience](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/get-started-profiles-and-audiences.html#permission) in Adobe Campaign Standard using the data in Adobe Experience Platform.</span></span>


<span data-ttu-id="49c69-173">Ikasi nola egin [erabili segmentu eraikitzailea](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/audience-destinations/aep-using-segment-builder.html) Adobe Campaign Standard-en Adobe Experience Platform-eko datuetan oinarritutako audientzia definitzeko.</span><span class="sxs-lookup"><span data-stu-id="49c69-173">Learn how to [use segment builder](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/audience-destinations/aep-using-segment-builder.html) in Adobe Campaign Standard to define an audience based on the data in Adobe Experience Platform.</span></span>

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a><span data-ttu-id="49c69-174">Sortu eta bidali mezu elektronikoa Adobe Campaign Standard erabiliz</span><span class="sxs-lookup"><span data-stu-id="49c69-174">Create and send the email using Adobe Campaign Standard</span></span>

<span data-ttu-id="49c69-175">Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.</span><span class="sxs-lookup"><span data-stu-id="49c69-175">Create the email content and then [test and send](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) your email.</span></span>

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Adobe Campaign Standard-ren berritze-eskaintza duen posta elektronikoa.":::
