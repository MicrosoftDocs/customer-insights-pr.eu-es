---
title: Esportatu Customer Insights datuak Adobe Campaign Standard-era
description: Ikusi audientzia estatistiken segmentuak nola erabiltzen diren Adobe Campaign Standard-en.
ms.date: 02/26/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: a5d0154c3d7c473dcba03fac0847bafcf97de2f2
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596300"
---
# <a name="use-customer-insights-segments-in-adobe-campaign-standard-preview"></a><span data-ttu-id="b7135-103">Erabili Customer Insights segmentuak nola erabiltzen diren Adobe Campaign Standard-en (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="b7135-103">Use Customer Insights segments in Adobe Campaign Standard (preview)</span></span>

<span data-ttu-id="b7135-104">Erabiltzaileentzako ikusleen estatistiken erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortzea zure marketin kanpainak eraginkorragoak izan daitezen publiko garrantzitsuei zuzenduta.</span><span class="sxs-lookup"><span data-stu-id="b7135-104">As a user of audience insights for Dynamics 365 Customer Insights, you may have created segments to make your marketing campaigns more efficient by targeting relevant audiences.</span></span> <span data-ttu-id="b7135-105">Adobe Experience Platform-eko eta Adobe Campaign Standard bezalako aplikazioetako audientziaren inguruko segmentu bat erabiltzeko, artikulu honetan zehaztutako urrats batzuk jarraitu behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="b7135-105">To use a segment from audience insights in Adobe Experience Platform and applications like Adobe Campaign Standard, you need to follow a few steps outlined in this article.</span></span>

:::image type="content" source="media/ACS-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a><span data-ttu-id="b7135-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="b7135-107">Prerequisites</span></span>

-   <span data-ttu-id="b7135-108">Dynamics 365 Customer Insights lizentzia</span><span class="sxs-lookup"><span data-stu-id="b7135-108">Dynamics 365 Customer Insights license</span></span>
-   <span data-ttu-id="b7135-109">Adobe Campaign Standard lizentzia</span><span class="sxs-lookup"><span data-stu-id="b7135-109">Adobe Campaign Standard license</span></span>
-   <span data-ttu-id="b7135-110">Azure blob-biltegia kontua</span><span class="sxs-lookup"><span data-stu-id="b7135-110">Azure Blob Storage account</span></span>

## <a name="campaign-overview"></a><span data-ttu-id="b7135-111">Kanpainaren informazio orokorra</span><span class="sxs-lookup"><span data-stu-id="b7135-111">Campaign Overview</span></span>

<span data-ttu-id="b7135-112">Adobe Experience Platform-en audientzia estatistiketatik segmentuak nola erabil ditzakezun hobeto ulertzeko, ikus dezagun fikziozko lagin kanpaina.</span><span class="sxs-lookup"><span data-stu-id="b7135-112">To better understand how you can use segments from audience insights in Adobe Experience Platform, let’s look at a fictitious sample campaign.</span></span>

<span data-ttu-id="b7135-113">Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei.</span><span class="sxs-lookup"><span data-stu-id="b7135-113">Let’s assume that your company offers a monthly, subscription-based service to your customers in the United States.</span></span> <span data-ttu-id="b7135-114">Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu.</span><span class="sxs-lookup"><span data-stu-id="b7135-114">You want to identify customers whose subscriptions are due for renewal in the next eight days but haven't yet renewed their subscription.</span></span> <span data-ttu-id="b7135-115">Bezero horiek mantentzeko, promozio eskaintza posta elektroniko bidez bidali nahi diezu, Adobe Campaign Standard erabiliz.</span><span class="sxs-lookup"><span data-stu-id="b7135-115">To keep these customers, you want to send them a promotional offer via email, using Adobe Campaign Standard.</span></span>

<span data-ttu-id="b7135-116">Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu.</span><span class="sxs-lookup"><span data-stu-id="b7135-116">In this example, we want to run the promotional email campaign once.</span></span> <span data-ttu-id="b7135-117">Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen.</span><span class="sxs-lookup"><span data-stu-id="b7135-117">This article doesn’t cover the use-case of running the campaign more than once.</span></span> <span data-ttu-id="b7135-118">Hala ere, ikusleei buruzko informazioa eta Adobe Campaign Standard konfiguratu daitezke kanpaina errepikatuko agertoki batean lan egiteko ere.</span><span class="sxs-lookup"><span data-stu-id="b7135-118">However, audience insights and Adobe Campaign Standard can be configured to work for a recurring campaign scenario too.</span></span>

## <a name="identify-your-target-audience"></a><span data-ttu-id="b7135-119">Identifikatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="b7135-119">Identify your target audience</span></span>

<span data-ttu-id="b7135-120">Gure eszenatokian, bezeroen helbide elektronikoak ikusleen estatistiketan eskuragarri daudela eta haien promozio hobespenak segmentuko kideak identifikatzeko aztertu direla suposatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="b7135-120">In our scenario, we assume that the email addresses of the customers are available in audience insights and their promotional preferences were analyzed to identify members of the segment.</span></span>

<span data-ttu-id="b7135-121">[Ikusleen estatistiketan definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero hauei posta elektroniko bidezko promozioa bidaltzeko asmoa duzu.</span><span class="sxs-lookup"><span data-stu-id="b7135-121">The [segment you defined in audience insights](segments.md) is called **ChurnProneCustomers** and you plan to send these customers the email promotion.</span></span>

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

<span data-ttu-id="b7135-123">Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira.</span><span class="sxs-lookup"><span data-stu-id="b7135-123">The offer email that you want to send out will contain the first name, last name, and the subscription end date of the customer.</span></span> <span data-ttu-id="b7135-124">Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.</span><span class="sxs-lookup"><span data-stu-id="b7135-124">It informs the customers about the discount they’ll get if they renew their subscription before it ends.</span></span>

## <a name="export-your-target-audience"></a><span data-ttu-id="b7135-125">Esportatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="b7135-125">Export your target audience</span></span>

<span data-ttu-id="b7135-126">Gure xede-audientzia identifikatuta, esportazioen konfigurazioa konfiguratu ahal izango dugu ikusleen estatistiketatik Azure blob-biltegia kontura.</span><span class="sxs-lookup"><span data-stu-id="b7135-126">With our target audience identified, we can configure the export from audience insights to an Azure Blob Storage account.</span></span>

1. <span data-ttu-id="b7135-127">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="b7135-127">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="b7135-128">**Adobe Campaign** lauzan, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="b7135-128">In the **Adobe Campaign** tile, select **Set up**.</span></span>

   :::image type="content" source="media/adobe-campaign-standard-tile.png" alt-text="Adobe Campaign Standard-en konfigurazio lauza.":::

1. <span data-ttu-id="b7135-130">Eman **Bistaratzeko izena** esportazio helmuga berri honetarako eta ondoren sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** segmentua esportatu nahi duzun Azure blob-biltegia kontukoa.</span><span class="sxs-lookup"><span data-stu-id="b7135-130">Provide a **Display name** for this new export destination and then enter the **Account name**, **Account key**, and **Container** of the Azure Blob Storage account where you want to export the segment to.</span></span>  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 

   - <span data-ttu-id="b7135-132">Azure Blob biltegiratze kontuaren izena eta kontuaren gakoa aurkitzeko informazio gehiago lortzeko, ikus [Kudeatu biltegiratze kontuen ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="b7135-132">To learn more about how to find the Azure Blob storage account name and account key, see [Manage storage account settings in the Azure portal](/azure/storage/common/storage-account-manage).</span></span>

   - <span data-ttu-id="b7135-133">Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span><span class="sxs-lookup"><span data-stu-id="b7135-133">To learn how to create a container, see [Create a container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span></span>

1. <span data-ttu-id="b7135-134">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="b7135-134">Select **Next**.</span></span>

1. <span data-ttu-id="b7135-135">Aukeratu esportatu nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="b7135-135">Choose the segment that you want to export.</span></span> <span data-ttu-id="b7135-136">Adibide honetan, **ChurnProneCustomers** da.</span><span class="sxs-lookup"><span data-stu-id="b7135-136">In this example, it’s **ChurnProneCustomers**.</span></span>

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. <span data-ttu-id="b7135-138">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="b7135-138">Select **Next**.</span></span>

1. <span data-ttu-id="b7135-139">Orain mapak egiten ditugu **Iturria** audientzien ikuspegi segmentutik eremura **Helburua** eremuen izenak Adobe Campaign Standard profileko eskeman.</span><span class="sxs-lookup"><span data-stu-id="b7135-139">Now we map the **Source** fields from the audience insights segment to the **Target** field names in the Adobe Campaign Standard profile schema.</span></span>

   :::image type="content" source="media/ACS-field-mapping.png" alt-text="Adobe Campaign Standard konektoreko eremuen mapaketa.":::

   <span data-ttu-id="b7135-141">Atributu gehiago gehitu nahi badituzu, hautatu **Gehitu atributua**.</span><span class="sxs-lookup"><span data-stu-id="b7135-141">If you want to add more attributes, select **Add attribute**.</span></span> <span data-ttu-id="b7135-142">Helburuaren izena iturburuko eremuaren izenetik desberdina izan daiteke, segmentuen irteera ikus dezakezu Adobe Campaign Standard-era segmentuek bi sistemetan izen bera ez badute.</span><span class="sxs-lookup"><span data-stu-id="b7135-142">The target name can be different from the source field name so you can still map segment output from audience insights to Adobe Campaign Standard if the fields don’t have the same name in the two systems.</span></span>

   > [!NOTE]
   > <span data-ttu-id="b7135-143">Helbide elektronikoa identitate-eremu gisa erabiltzen da, baina zure audientzien estatistiken bezeroaren profiletik beste edozein identifikatzaile erabil dezakezu datuak Adobe Campaign Standard-ra mapatzeko.</span><span class="sxs-lookup"><span data-stu-id="b7135-143">Email address is used as an identity field but you can use any other identifier from your audience insights customer profile to map data to Adobe Campaign Standard.</span></span>

1. <span data-ttu-id="b7135-144">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="b7135-144">Select **Save**.</span></span>

<span data-ttu-id="b7135-145">Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Administratzailea** > **Esportazioak** > **Nire esportazio helmugak**.</span><span class="sxs-lookup"><span data-stu-id="b7135-145">After saving the export destination, you find it on **Admin** > **Exports** > **My export destinations**.</span></span>

:::image type="content" source="media/export-destination-adobe-campaign-standard.png" alt-text="Pantaila-argazkia esportazioen zerrenda eta lagin-segmentua nabarmenduta.":::

<span data-ttu-id="b7135-147">Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#export-data-on-demand).</span><span class="sxs-lookup"><span data-stu-id="b7135-147">You can now [export the segment on demand](export-destinations.md#export-data-on-demand).</span></span> <span data-ttu-id="b7135-148">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).</span><span class="sxs-lookup"><span data-stu-id="b7135-148">The export will also run with every [scheduled refresh](system.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b7135-149">Ziurtatu esportatutako segmentuan erregistro kopurua Adobe Campaign Standard lizentziaren baimendutako mugaren barruan dagoela.</span><span class="sxs-lookup"><span data-stu-id="b7135-149">Ensure that the number of records in the exported segment are within the allowed limit of your Adobe Campaign Standard license.</span></span>

<span data-ttu-id="b7135-150">Esportatutako datuak goian konfiguratu duzun Azure blob-biltegia edukiontzian gordetzen dira.</span><span class="sxs-lookup"><span data-stu-id="b7135-150">Exported data is stored in the Azure Blob storage container you configured above.</span></span> <span data-ttu-id="b7135-151">Karpeta bide hau automatikoki sortzen da zure edukiontzian:</span><span class="sxs-lookup"><span data-stu-id="b7135-151">The following folder path is automatically created in your container:</span></span>

<span data-ttu-id="b7135-152">*%ContainerName%/CustomerInsights_%instanceID%/% exportdestination-name%_%segmentname%_%timestamp%.csv*</span><span class="sxs-lookup"><span data-stu-id="b7135-152">*%ContainerName%/CustomerInsights_%instanceID%/% exportdestination-name%_%segmentname%_%timestamp%.csv*</span></span>

<span data-ttu-id="b7135-153">Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv</span><span class="sxs-lookup"><span data-stu-id="b7135-153">Example: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv</span></span>

## <a name="configure-adobe-campaign-standard"></a><span data-ttu-id="b7135-154">Konfiguratu Adobe Campaign Standard</span><span class="sxs-lookup"><span data-stu-id="b7135-154">Configure Adobe Campaign Standard</span></span>

<span data-ttu-id="b7135-155">Audientzia estatistiketatik ateratako segmentu bat esportatzen denean, aurreko urratsean esportazio-helmuga definitzen zenuen bitartean aukeratu dituzun zutabeak ditu.</span><span class="sxs-lookup"><span data-stu-id="b7135-155">When a segment from audience insights is exported, it contains the columns you selected while defining the export destination in the previous step.</span></span> <span data-ttu-id="b7135-156">Datu hauek erabil daitezke [profilak sortu Adobe Campaign Standard zerbitzuan](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).</span><span class="sxs-lookup"><span data-stu-id="b7135-156">This data can be used to [create profiles in Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).</span></span>

<span data-ttu-id="b7135-157">Adobe Campaign Standard-en segmentua erabiltzeko, Adobe Campaign Standard-en profil eskema luzatu behar dugu bi eremu gehigarri sartzeko.</span><span class="sxs-lookup"><span data-stu-id="b7135-157">To use the segment in Adobe Campaign Standard, we need to extend the profile schema in Adobe Campaign Standard to include two additional fields.</span></span> <span data-ttu-id="b7135-158">Ikasi nola egin [profila baliabidea luzatu](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) eremu berriekin Adobe Campaign Standard.</span><span class="sxs-lookup"><span data-stu-id="b7135-158">Learn how to [extend the profile resource](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) with new fields in Adobe Campaign Standard.</span></span>

<span data-ttu-id="b7135-159">Gure adibidean, eremu hauek dira *Segmentuaren izena eta segmentuaren data (aukerakoa).*</span><span class="sxs-lookup"><span data-stu-id="b7135-159">In our example, these fields are *Segment Name and Segment Date (optional).*</span></span>

<span data-ttu-id="b7135-160">Eremu horiek erabiliko ditugu kanpaina honetarako bideratu nahi dugun Adobe Campaign Standard profilak identifikatzeko.</span><span class="sxs-lookup"><span data-stu-id="b7135-160">We will use these fields to identify the profiles in Adobe Campaign Standard we want to target for this campaign.</span></span>

<span data-ttu-id="b7135-161">Adobe Campaign Standard-en inportatzera zoazena baino beste erregistroik ez badago, urrats hau salta dezakezu.</span><span class="sxs-lookup"><span data-stu-id="b7135-161">If there are no other records in Adobe Campaign Standard, other than what you are going to import, you can skip this step.</span></span>

## <a name="import-data-into-adobe-campaign-standard"></a><span data-ttu-id="b7135-162">Inportatu datuak Adobe Campaign Standard-era</span><span class="sxs-lookup"><span data-stu-id="b7135-162">Import data into Adobe Campaign Standard</span></span>

<span data-ttu-id="b7135-163">Dena indarrean dagoela, entzuleen datuetatik prestatutako audientzia datuak Adobe Campaign Standard profilak sortzeko inportatu behar ditugu.</span><span class="sxs-lookup"><span data-stu-id="b7135-163">Now that everything is in place, we need to import the prepared audience data from audience insights into Adobe Campaign Standard to create profiles.</span></span> <span data-ttu-id="b7135-164">Ikasi [nola inportatu profilak Adobe Campaign Standard zerbitzuan](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences) lan-fluxua erabiliz.</span><span class="sxs-lookup"><span data-stu-id="b7135-164">Learn [how to import profiles in Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences) using a workflow.</span></span>

<span data-ttu-id="b7135-165">Beheko irudiko inportazio lan-fluxua 8 orduro exekutatzeko konfiguratuta dago eta esportatutako audientzia estatistiken segmentuak bilatzen ditu (.csv fitxategia Azure blob-biltegian).</span><span class="sxs-lookup"><span data-stu-id="b7135-165">The import workflow in the image below has been configured to run every 8 hours and looks for exported audience insights segments (.csv file in Azure Blob Storage).</span></span> <span data-ttu-id="b7135-166">Lan-fluxuak .csv fitxategiaren edukia zehaztutako zutabe ordenan ateratzen du.</span><span class="sxs-lookup"><span data-stu-id="b7135-166">The workflow extracts the .csv file content in a specified column order.</span></span> <span data-ttu-id="b7135-167">Lan-fluxu hau oinarrizko akatsak kudeatzeko eta erregistro bakoitzak helbide elektronikoa duela ziurtatzeko sortu da, datuak Adobe Campaign Standard-en hidratatu aurretik.</span><span class="sxs-lookup"><span data-stu-id="b7135-167">This workflow has been built to perform basic error handling and ensure that each record has an email address before hydrating the data in Adobe Campaign Standard.</span></span> <span data-ttu-id="b7135-168">Lan-fluxuak ere segmentuaren izena fitxategi-izenetik ateratzen du ACS profileko datuetara sartu aurretik.</span><span class="sxs-lookup"><span data-stu-id="b7135-168">The workflow also extracts the segment name from the filename before upserting into ACS Profile data.</span></span>

:::image type="content" source="media/ACS-import-workflow.png" alt-text="Inportazio lan-fluxuaren pantaila-argazkia Adobe Campaign Standard erabiltzaile interfazean.":::

## <a name="retrieve-the-audience-in-adobe-campaign-standard"></a><span data-ttu-id="b7135-170">Berreskuratu audientzia Adobe Campaign Standard zerbitzuan</span><span class="sxs-lookup"><span data-stu-id="b7135-170">Retrieve the audience in Adobe Campaign Standard</span></span>

<span data-ttu-id="b7135-171">Datuak Adobe Campaign Standard-era inportatu ondoren, zuk [lan fluxua sor dezake](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) eta [kontsulta](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) oinarritutako bezeroak *Segmentuaren izena* eta *Segmentuaren Data* gure lagin kanpainarako identifikatutako profilak hautatzeko.</span><span class="sxs-lookup"><span data-stu-id="b7135-171">Once the data is imported into Adobe Campaign Standard, you [can create a workflow](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) and [query](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) the customers based on the *Segment Name* and *Segment Date* to select profiles that were identified for our sample campaign.</span></span>

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a><span data-ttu-id="b7135-172">Sortu eta bidali mezu elektronikoa Adobe Campaign Standard erabiliz</span><span class="sxs-lookup"><span data-stu-id="b7135-172">Create and send the email using Adobe Campaign Standard</span></span>

<span data-ttu-id="b7135-173">Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.</span><span class="sxs-lookup"><span data-stu-id="b7135-173">Create the email content and then [test and send](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) your email.</span></span>

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Adobe Campaign Standard-ren berritze-eskaintza duen posta elektronikoa.":::