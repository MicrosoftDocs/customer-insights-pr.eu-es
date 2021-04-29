---
title: Esportatu Customer Insights datuak Adobe Campaign Standard-era
description: Ikusi audientzia estatistiken segmentuak nola erabiltzen diren Adobe Campaign Standard-en.
ms.date: 03/29/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: b6c010d84119c2fa8b3ef99017c65f9939bf28c4
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760266"
---
# <a name="use-customer-insights-segments-in-adobe-campaign-standard-preview"></a><span data-ttu-id="2d273-103">Erabili Customer Insights segmentuak nola erabiltzen diren Adobe Campaign Standard-en (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="2d273-103">Use Customer Insights segments in Adobe Campaign Standard (preview)</span></span>

<span data-ttu-id="2d273-104">Erabiltzaileentzako ikusleen estatistiken erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortzea zure marketin kanpainak eraginkorragoak izan daitezen publiko garrantzitsuei zuzenduta.</span><span class="sxs-lookup"><span data-stu-id="2d273-104">As a user of audience insights for Dynamics 365 Customer Insights, you may have created segments to make your marketing campaigns more efficient by targeting relevant audiences.</span></span> <span data-ttu-id="2d273-105">Adobe Experience Platform-eko eta Adobe Campaign Standard bezalako aplikazioetako audientziaren inguruko segmentu bat erabiltzeko, artikulu honetan zehaztutako urrats batzuk jarraitu behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="2d273-105">To use a segment from audience insights in Adobe Experience Platform and applications like Adobe Campaign Standard, you need to follow a few steps outlined in this article.</span></span>

:::image type="content" source="media/ACS-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a><span data-ttu-id="2d273-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="2d273-107">Prerequisites</span></span>

-   <span data-ttu-id="2d273-108">Dynamics 365 Customer Insights lizentzia</span><span class="sxs-lookup"><span data-stu-id="2d273-108">Dynamics 365 Customer Insights license</span></span>
-   <span data-ttu-id="2d273-109">Adobe Campaign Standard lizentzia</span><span class="sxs-lookup"><span data-stu-id="2d273-109">Adobe Campaign Standard license</span></span>
-   <span data-ttu-id="2d273-110">Azure blob-biltegia kontua</span><span class="sxs-lookup"><span data-stu-id="2d273-110">Azure Blob Storage account</span></span>

## <a name="campaign-overview"></a><span data-ttu-id="2d273-111">Kanpainaren informazio orokorra</span><span class="sxs-lookup"><span data-stu-id="2d273-111">Campaign Overview</span></span>

<span data-ttu-id="2d273-112">Adobe Experience Platform-en audientzia estatistiketatik segmentuak nola erabil ditzakezun hobeto ulertzeko, ikus dezagun fikziozko lagin kanpaina.</span><span class="sxs-lookup"><span data-stu-id="2d273-112">To better understand how you can use segments from audience insights in Adobe Experience Platform, let’s look at a fictitious sample campaign.</span></span>

<span data-ttu-id="2d273-113">Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei.</span><span class="sxs-lookup"><span data-stu-id="2d273-113">Let’s assume that your company offers a monthly, subscription-based service to your customers in the United States.</span></span> <span data-ttu-id="2d273-114">Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu.</span><span class="sxs-lookup"><span data-stu-id="2d273-114">You want to identify customers whose subscriptions are due for renewal in the next eight days but haven't yet renewed their subscription.</span></span> <span data-ttu-id="2d273-115">Bezero horiek mantentzeko, promozio eskaintza posta elektroniko bidez bidali nahi diezu, Adobe Campaign Standard erabiliz.</span><span class="sxs-lookup"><span data-stu-id="2d273-115">To keep these customers, you want to send them a promotional offer via email, using Adobe Campaign Standard.</span></span>

<span data-ttu-id="2d273-116">Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu.</span><span class="sxs-lookup"><span data-stu-id="2d273-116">In this example, we want to run the promotional email campaign once.</span></span> <span data-ttu-id="2d273-117">Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen.</span><span class="sxs-lookup"><span data-stu-id="2d273-117">This article doesn’t cover the use-case of running the campaign more than once.</span></span> <span data-ttu-id="2d273-118">Hala ere, ikusleei buruzko informazioa eta Adobe Campaign Standard konfiguratu daitezke kanpaina errepikatuko agertoki batean lan egiteko ere.</span><span class="sxs-lookup"><span data-stu-id="2d273-118">However, audience insights and Adobe Campaign Standard can be configured to work for a recurring campaign scenario too.</span></span>

## <a name="identify-your-target-audience"></a><span data-ttu-id="2d273-119">Identifikatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="2d273-119">Identify your target audience</span></span>

<span data-ttu-id="2d273-120">Gure eszenatokian, bezeroen helbide elektronikoak ikusleen estatistiketan eskuragarri daudela eta haien promozio hobespenak segmentuko kideak identifikatzeko aztertu direla suposatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="2d273-120">In our scenario, we assume that the email addresses of the customers are available in audience insights and their promotional preferences were analyzed to identify members of the segment.</span></span>

<span data-ttu-id="2d273-121">[Ikusleen estatistiketan definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero hauei posta elektroniko bidezko promozioa bidaltzeko asmoa duzu.</span><span class="sxs-lookup"><span data-stu-id="2d273-121">The [segment you defined in audience insights](segments.md) is called **ChurnProneCustomers** and you plan to send these customers the email promotion.</span></span>

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

<span data-ttu-id="2d273-123">Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira.</span><span class="sxs-lookup"><span data-stu-id="2d273-123">The offer email that you want to send out will contain the first name, last name, and the subscription end date of the customer.</span></span> <span data-ttu-id="2d273-124">Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.</span><span class="sxs-lookup"><span data-stu-id="2d273-124">It informs the customers about the discount they’ll get if they renew their subscription before it ends.</span></span>

## <a name="export-your-target-audience"></a><span data-ttu-id="2d273-125">Esportatu zure xede-publikoa</span><span class="sxs-lookup"><span data-stu-id="2d273-125">Export your target audience</span></span>

### <a name="configure-a-connection"></a><span data-ttu-id="2d273-126">Konfiguratu konexioa</span><span class="sxs-lookup"><span data-stu-id="2d273-126">Configure a connection</span></span>

<span data-ttu-id="2d273-127">Gure xede-audientzia identifikatuta, esportazioen konfigurazioa konfiguratu ahal izango dugu ikusleen estatistiketatik Azure blob-biltegia kontura.</span><span class="sxs-lookup"><span data-stu-id="2d273-127">With our target audience identified, we can configure the export from audience insights to an Azure Blob Storage account.</span></span>

1. <span data-ttu-id="2d273-128">Ikusleen ikuspegietan, joan hona **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="2d273-128">In audience insights, go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="2d273-129">Aukeratu **Gehitu konexioa** eta aukeratu **Adobe kanpaina** konexioa konfiguratzeko edo hautatu **Konfiguratu** urtean **Adobe kanpaina** teila</span><span class="sxs-lookup"><span data-stu-id="2d273-129">Select **Add connection** and choose **Adobe Campaign** to configure the connection or select **Set up** in the **Adobe Campaign** tile</span></span>

   :::image type="content" source="media/adobe-campaign-standard-tile.png" alt-text="Adobe Campaign Standard-en konfigurazio lauza.":::

1. <span data-ttu-id="2d273-131">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="2d273-131">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="2d273-132">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="2d273-132">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="2d273-133">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="2d273-133">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="2d273-134">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="2d273-134">Choose who can use this connection.</span></span> <span data-ttu-id="2d273-135">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="2d273-135">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="2d273-136">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="2d273-136">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="2d273-137">Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** Azure Blob biltegiratze-kontuarena, segmentua esportatu nahi duzunera.</span><span class="sxs-lookup"><span data-stu-id="2d273-137">Enter the **Account name**, **Account key**, and **Container** of the Azure Blob Storage account where you want to export the segment to.</span></span>  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 

   - <span data-ttu-id="2d273-139">Azure Blob biltegiratze kontuaren izena eta kontuaren gakoa aurkitzeko informazio gehiago lortzeko, ikus [Kudeatu biltegiratze kontuen ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="2d273-139">To learn more about how to find the Azure Blob storage account name and account key, see [Manage storage account settings in the Azure portal](/azure/storage/common/storage-account-manage).</span></span>

   - <span data-ttu-id="2d273-140">Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span><span class="sxs-lookup"><span data-stu-id="2d273-140">To learn how to create a container, see [Create a container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span></span>

1. <span data-ttu-id="2d273-141">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="2d273-141">Select **Save** to complete the connection.</span></span>

### <a name="configure-an-export"></a><span data-ttu-id="2d273-142">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="2d273-142">Configure an export</span></span>

<span data-ttu-id="2d273-143">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="2d273-143">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="2d273-144">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="2d273-144">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="2d273-145">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="2d273-145">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="2d273-146">Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.</span><span class="sxs-lookup"><span data-stu-id="2d273-146">To create a new export, select **Add export**.</span></span>

1. <span data-ttu-id="2d273-147">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Adobe kanpainaren sekzioan.</span><span class="sxs-lookup"><span data-stu-id="2d273-147">In the **Connection for export** field, choose a connection from the Adobe Campaign section.</span></span> <span data-ttu-id="2d273-148">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="2d273-148">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="2d273-149">Aukeratu esportatu nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="2d273-149">Choose the segment that you want to export.</span></span> <span data-ttu-id="2d273-150">Adibide honetan, **ChurnProneCustomers** da.</span><span class="sxs-lookup"><span data-stu-id="2d273-150">In this example, it’s **ChurnProneCustomers**.</span></span>

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. <span data-ttu-id="2d273-152">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="2d273-152">Select **Next**.</span></span>

1. <span data-ttu-id="2d273-153">Orain mapak egiten ditugu **Iturria** audientzien ikuspegi segmentutik eremura **Helburua** eremuen izenak Adobe Campaign Standard profileko eskeman.</span><span class="sxs-lookup"><span data-stu-id="2d273-153">Now we map the **Source** fields from the audience insights segment to the **Target** field names in the Adobe Campaign Standard profile schema.</span></span>

   :::image type="content" source="media/ACS-field-mapping.png" alt-text="Adobe Campaign Standard konektoreko eremuen mapaketa.":::

   <span data-ttu-id="2d273-155">Atributu gehiago gehitu nahi badituzu, hautatu **Gehitu atributua**.</span><span class="sxs-lookup"><span data-stu-id="2d273-155">If you want to add more attributes, select **Add attribute**.</span></span> <span data-ttu-id="2d273-156">Helburuaren izena iturburuko eremuaren izenetik desberdina izan daiteke, segmentuen irteera ikus dezakezu Adobe Campaign Standard-era segmentuek bi sistemetan izen bera ez badute.</span><span class="sxs-lookup"><span data-stu-id="2d273-156">The target name can be different from the source field name so you can still map segment output from audience insights to Adobe Campaign Standard if the fields don’t have the same name in the two systems.</span></span>

   > [!NOTE]
   > <span data-ttu-id="2d273-157">Helbide elektronikoa identitate-eremu gisa erabiltzen da, baina zure audientzien estatistiken bezeroaren profiletik beste edozein identifikatzaile erabil dezakezu datuak Adobe Campaign Standard-ra mapatzeko.</span><span class="sxs-lookup"><span data-stu-id="2d273-157">Email address is used as an identity field but you can use any other identifier from your audience insights customer profile to map data to Adobe Campaign Standard.</span></span>

1. <span data-ttu-id="2d273-158">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="2d273-158">Select **Save**.</span></span>

<span data-ttu-id="2d273-159">Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="2d273-159">After saving the export destination, you find it on **Data** > **Exports**.</span></span>

<span data-ttu-id="2d273-160">Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="2d273-160">You can now [export the segment on demand](export-destinations.md#run-exports-on-demand).</span></span> <span data-ttu-id="2d273-161">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).</span><span class="sxs-lookup"><span data-stu-id="2d273-161">The export will also run with every [scheduled refresh](system.md).</span></span>

> [!NOTE]
> <span data-ttu-id="2d273-162">Ziurtatu esportatutako segmentuan erregistro kopurua Adobe Campaign Standard lizentziaren baimendutako mugaren barruan dagoela.</span><span class="sxs-lookup"><span data-stu-id="2d273-162">Ensure that the number of records in the exported segment are within the allowed limit of your Adobe Campaign Standard license.</span></span>

<span data-ttu-id="2d273-163">Esportatutako datuak goian konfiguratu duzun Azure blob-biltegia edukiontzian gordetzen dira.</span><span class="sxs-lookup"><span data-stu-id="2d273-163">Exported data is stored in the Azure Blob storage container you configured above.</span></span> <span data-ttu-id="2d273-164">Karpeta bide hau automatikoki sortzen da zure edukiontzian:</span><span class="sxs-lookup"><span data-stu-id="2d273-164">The following folder path is automatically created in your container:</span></span>

<span data-ttu-id="2d273-165">*%ContainerName%/CustomerInsights_%instanceID%/% exportdestination-name%_%segmentname%_%timestamp%.csv*</span><span class="sxs-lookup"><span data-stu-id="2d273-165">*%ContainerName%/CustomerInsights_%instanceID%/% exportdestination-name%_%segmentname%_%timestamp%.csv*</span></span>

<span data-ttu-id="2d273-166">Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv</span><span class="sxs-lookup"><span data-stu-id="2d273-166">Example: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv</span></span>

## <a name="configure-adobe-campaign-standard"></a><span data-ttu-id="2d273-167">Konfiguratu Adobe Campaign Standard</span><span class="sxs-lookup"><span data-stu-id="2d273-167">Configure Adobe Campaign Standard</span></span>

<span data-ttu-id="2d273-168">Audientzia estatistiketatik ateratako segmentu bat esportatzen denean, aurreko urratsean esportazio-helmuga definitzen zenuen bitartean aukeratu dituzun zutabeak ditu.</span><span class="sxs-lookup"><span data-stu-id="2d273-168">When a segment from audience insights is exported, it contains the columns you selected while defining the export destination in the previous step.</span></span> <span data-ttu-id="2d273-169">Datu hauek erabil daitezke [profilak sortu Adobe Campaign Standard zerbitzuan](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).</span><span class="sxs-lookup"><span data-stu-id="2d273-169">This data can be used to [create profiles in Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).</span></span>

<span data-ttu-id="2d273-170">Adobe Campaign Standard-en segmentua erabiltzeko, Adobe Campaign Standard-en profil eskema luzatu behar dugu bi eremu gehigarri sartzeko.</span><span class="sxs-lookup"><span data-stu-id="2d273-170">To use the segment in Adobe Campaign Standard, we need to extend the profile schema in Adobe Campaign Standard to include two additional fields.</span></span> <span data-ttu-id="2d273-171">Ikasi nola egin [profila baliabidea luzatu](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) eremu berriekin Adobe Campaign Standard.</span><span class="sxs-lookup"><span data-stu-id="2d273-171">Learn how to [extend the profile resource](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) with new fields in Adobe Campaign Standard.</span></span>

<span data-ttu-id="2d273-172">Gure adibidean, eremu hauek dira *Segmentuaren izena eta segmentuaren data (aukerakoa).*</span><span class="sxs-lookup"><span data-stu-id="2d273-172">In our example, these fields are *Segment Name and Segment Date (optional).*</span></span>

<span data-ttu-id="2d273-173">Eremu horiek erabiliko ditugu kanpaina honetarako bideratu nahi dugun Adobe Campaign Standard profilak identifikatzeko.</span><span class="sxs-lookup"><span data-stu-id="2d273-173">We will use these fields to identify the profiles in Adobe Campaign Standard we want to target for this campaign.</span></span>

<span data-ttu-id="2d273-174">Adobe Campaign Standard-en inportatzera zoazena baino beste erregistroik ez badago, urrats hau salta dezakezu.</span><span class="sxs-lookup"><span data-stu-id="2d273-174">If there are no other records in Adobe Campaign Standard, other than what you are going to import, you can skip this step.</span></span>

## <a name="import-data-into-adobe-campaign-standard"></a><span data-ttu-id="2d273-175">Inportatu datuak Adobe Campaign Standard-era</span><span class="sxs-lookup"><span data-stu-id="2d273-175">Import data into Adobe Campaign Standard</span></span>

<span data-ttu-id="2d273-176">Dena indarrean dagoela, entzuleen datuetatik prestatutako audientzia datuak Adobe Campaign Standard profilak sortzeko inportatu behar ditugu.</span><span class="sxs-lookup"><span data-stu-id="2d273-176">Now that everything is in place, we need to import the prepared audience data from audience insights into Adobe Campaign Standard to create profiles.</span></span> <span data-ttu-id="2d273-177">Ikasi [nola inportatu profilak Adobe Campaign Standard zerbitzuan](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences) lan-fluxua erabiliz.</span><span class="sxs-lookup"><span data-stu-id="2d273-177">Learn [how to import profiles in Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences) using a workflow.</span></span>

<span data-ttu-id="2d273-178">Beheko irudiko inportazio lan-fluxua 8 orduro exekutatzeko konfiguratuta dago eta esportatutako audientzia estatistiken segmentuak bilatzen ditu (.csv fitxategia Azure blob-biltegian).</span><span class="sxs-lookup"><span data-stu-id="2d273-178">The import workflow in the image below has been configured to run every 8 hours and looks for exported audience insights segments (.csv file in Azure Blob Storage).</span></span> <span data-ttu-id="2d273-179">Lan-fluxuak .csv fitxategiaren edukia zehaztutako zutabe ordenan ateratzen du.</span><span class="sxs-lookup"><span data-stu-id="2d273-179">The workflow extracts the .csv file content in a specified column order.</span></span> <span data-ttu-id="2d273-180">Lan-fluxu hau oinarrizko akatsak kudeatzeko eta erregistro bakoitzak helbide elektronikoa duela ziurtatzeko sortu da, datuak Adobe Campaign Standard-en hidratatu aurretik.</span><span class="sxs-lookup"><span data-stu-id="2d273-180">This workflow has been built to perform basic error handling and ensure that each record has an email address before hydrating the data in Adobe Campaign Standard.</span></span> <span data-ttu-id="2d273-181">Lan-fluxuak ere segmentuaren izena fitxategi-izenetik ateratzen du ACS profileko datuetara sartu aurretik.</span><span class="sxs-lookup"><span data-stu-id="2d273-181">The workflow also extracts the segment name from the filename before upserting into ACS Profile data.</span></span>

:::image type="content" source="media/ACS-import-workflow.png" alt-text="Inportazio lan-fluxuaren pantaila-argazkia Adobe Campaign Standard erabiltzaile interfazean.":::

## <a name="retrieve-the-audience-in-adobe-campaign-standard"></a><span data-ttu-id="2d273-183">Berreskuratu audientzia Adobe Campaign Standard zerbitzuan</span><span class="sxs-lookup"><span data-stu-id="2d273-183">Retrieve the audience in Adobe Campaign Standard</span></span>

<span data-ttu-id="2d273-184">Datuak Adobe Campaign Standard-era inportatu ondoren, zuk [lan fluxua sor dezake](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) eta [kontsulta](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) oinarritutako bezeroak *Segmentuaren izena* eta *Segmentuaren Data* gure lagin kanpainarako identifikatutako profilak hautatzeko.</span><span class="sxs-lookup"><span data-stu-id="2d273-184">Once the data is imported into Adobe Campaign Standard, you [can create a workflow](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) and [query](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) the customers based on the *Segment Name* and *Segment Date* to select profiles that were identified for our sample campaign.</span></span>

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a><span data-ttu-id="2d273-185">Sortu eta bidali mezu elektronikoa Adobe Campaign Standard erabiliz</span><span class="sxs-lookup"><span data-stu-id="2d273-185">Create and send the email using Adobe Campaign Standard</span></span>

<span data-ttu-id="2d273-186">Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.</span><span class="sxs-lookup"><span data-stu-id="2d273-186">Create the email content and then [test and send](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) your email.</span></span>

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Adobe Campaign Standard-ren berritze-eskaintza duen posta elektronikoa.":::
