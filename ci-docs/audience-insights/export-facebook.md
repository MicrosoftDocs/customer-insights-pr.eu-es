---
title: Esportatu Customer Insights datuak Facebook iragarki-kudeatzailera
description: Ikasi konexioa konfiguratzen eta esportatzen Facebook Iragarkien kudeatzailea.
ms.date: 04/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: e20c7b7fd3989d7621cb7765f38b85c8ab4adfcb
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305095"
---
# <a name="export-segments-list-to-facebook-ads-manager-preview"></a><span data-ttu-id="8d949-103">Esportatu segmentuen zerrenda Facebook Iragarkien kudeatzailea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="8d949-103">Export segments list to Facebook Ads Manager (preview)</span></span>

<span data-ttu-id="8d949-104">Bezeroen profil bateratuen segmentuak esportatu Facebook Iragarkien kudeatzailea kanpainak sortzeko Facebook eta Instagram.</span><span class="sxs-lookup"><span data-stu-id="8d949-104">Export segments of unified customer profiles to Facebook Ads Manager to create campaigns on Facebook and Instagram.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="8d949-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="8d949-105">Prerequisites for connection</span></span>

- <span data-ttu-id="8d949-106">[**Facebook iragarkien kontuak**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) dut [**Facebook negozio-kontua**](https://business.facebook.com/).</span><span class="sxs-lookup"><span data-stu-id="8d949-106">You need to have a [**Facebook Ads Account**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) that includes a [**Facebook Business Account**](https://business.facebook.com/).</span></span>
- <span data-ttu-id="8d949-107">Administratzailea izan behar duzu [**Facebook iragarkien kontua**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account).</span><span class="sxs-lookup"><span data-stu-id="8d949-107">You need to be an administrator on the [**Facebook Ads Account**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="8d949-108">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="8d949-108">Known limitations</span></span>

- <span data-ttu-id="8d949-109">Gehienez 10 milioi bezero profil esportatzeko Facebook Iragarkien kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="8d949-109">Up to 10 million customer profiles per export to Facebook Ads Manager.</span></span>
- <span data-ttu-id="8d949-110">Esportatu Facebook Ads-eko kudeatzailera esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="8d949-110">Export to Facebook Ads Manager is limited to segments.</span></span>
- <span data-ttu-id="8d949-111">Sortu edo eguneratu audientzia pertsonalizatuak hemen Facebook motakoa *bezeroen zerrenda* bakarrik.</span><span class="sxs-lookup"><span data-stu-id="8d949-111">Create or update custom audiences in Facebook of type *customer list* only.</span></span>
- <span data-ttu-id="8d949-112">Guztira 10 milioi profil dituzten segmentuak esportatzen 90 minutu behar izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="8d949-112">Exporting segments with a total of 10 million profiles can take up to 90 minutes to complete.</span></span>

## <a name="set-up-connection-to-facebook-ads-manager"></a><span data-ttu-id="8d949-113">Konfiguratu konexioa Facebook iragarkien kudeatzailea</span><span class="sxs-lookup"><span data-stu-id="8d949-113">Set up connection to Facebook Ads Manager</span></span>

<span data-ttu-id="8d949-114">Erabiltzaileek esportazio bat sortu aurretik, administratzaile batek zerbitzurako konexioa konfiguratu behar du eta laguntzaileei konexioa erabiltzeko baimena eman behar die.</span><span class="sxs-lookup"><span data-stu-id="8d949-114">Before users can create an export, an administrator must configure the connection to the service and allow contributors to use the connection.</span></span>

1. <span data-ttu-id="8d949-115">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="8d949-115">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="8d949-116">Aukeratu **Gehitu konexioa** eta aukeratu **Facebook Iragarkien kudeatzailea** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="8d949-116">Select **Add connection** and choose **Facebook Ads Manager** to configure the connection.</span></span>

1. <span data-ttu-id="8d949-117">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="8d949-117">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="8d949-118">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="8d949-118">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="8d949-119">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="8d949-119">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="8d949-120">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="8d949-120">Choose who can use this connection.</span></span> <span data-ttu-id="8d949-121">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="8d949-121">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="8d949-122">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="8d949-122">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="8d949-123">Autentifikatu Facebook iragarkiekin:</span><span class="sxs-lookup"><span data-stu-id="8d949-123">Authenticate with Facebook Ads:</span></span> 

   1. <span data-ttu-id="8d949-124">Aukeratu **Jarraitu honekin Facebook** zure saioa hasteko Facebook Iragarkien kontua.</span><span class="sxs-lookup"><span data-stu-id="8d949-124">Select **Continue with Facebook** to sign in to your Facebook Ads account.</span></span>

   1. <span data-ttu-id="8d949-125">Onartu **iragarkien kudeaketa** baimena, Facebook-ekin autentifikatu ondoren.</span><span class="sxs-lookup"><span data-stu-id="8d949-125">Allow the **ads_management** permission after authenticating with Facebook.</span></span>

   1. <span data-ttu-id="8d949-126">Hautatu **Facebook iragarki kontua** lan egin nahi duzunarekin.</span><span class="sxs-lookup"><span data-stu-id="8d949-126">Select the **Facebook Ads Account** that you want to work with.</span></span>

   1. <span data-ttu-id="8d949-127">Aukeratu **Lehendik dagoen publiko pertsonalizatua** goitibeherako zerrendatik edo sortu **Publiko pertsonalizatu berria**.</span><span class="sxs-lookup"><span data-stu-id="8d949-127">Select an **Existing custom audience** from the dropdown list or create a **New custom audience**.</span></span> <span data-ttu-id="8d949-128">Informazio gehiago lortzeko, ikus [**Ikusleak Facebook Iragarkien kudeatzailea**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).</span><span class="sxs-lookup"><span data-stu-id="8d949-128">For more information, see [**Audiences in Facebook Ads Manager**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).</span></span>
      > [!NOTE]
      > <span data-ttu-id="8d949-129">Ikusle pertsonalizatuak soilik sor ditzakezu edo eguneratu Facebook motakoa *bezeroen zerrenda* esportazio honekin.</span><span class="sxs-lookup"><span data-stu-id="8d949-129">You can only create or update custom audiences on Facebook of the type *customer list* with this export.</span></span> <span data-ttu-id="8d949-130">Zenbait kasutan, goitibeherako zerrendan mota desberdinetako ikusle pertsonalizatuak ikusten dituzu.</span><span class="sxs-lookup"><span data-stu-id="8d949-130">In some cases, you see custom audiences of different types in the dropdown list.</span></span> <span data-ttu-id="8d949-131">Ez bezalako mota bat hautatzea *bezeroen zerrenda* esportazioak huts egingo du.</span><span class="sxs-lookup"><span data-stu-id="8d949-131">Selecting a different type than *customer list* will result in a failing export.</span></span> 

1. <span data-ttu-id="8d949-132">Berrikusi **Datuen pribatutasuna eta betetzea** eta hautatu **ados**.</span><span class="sxs-lookup"><span data-stu-id="8d949-132">Review the **Data privacy and compliance** and select **I agree**.</span></span>

1. <span data-ttu-id="8d949-133">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="8d949-133">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="8d949-134">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="8d949-134">Configure an export</span></span>

<span data-ttu-id="8d949-135">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="8d949-135">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="8d949-136">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="8d949-136">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="8d949-137">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="8d949-137">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="8d949-138">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="8d949-138">To create a new export, select **Add destination**.</span></span> 

1. <span data-ttu-id="8d949-139">Hurrengoan **Esportaziorako konexioa** Aukeratu konexioa **Facebook Iragarkien kudeatzailea** atala.</span><span class="sxs-lookup"><span data-stu-id="8d949-139">In **Connection for export** choose a connection from the **Facebook Ads Manager** section.</span></span> <span data-ttu-id="8d949-140">Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.</span><span class="sxs-lookup"><span data-stu-id="8d949-140">If you don't see this section name, then no connections of this type are available to you.</span></span>

1. <span data-ttu-id="8d949-141">Sarbidean **Aukeratu zure gako identifikatzaileen eremua** hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** bidali Facebook Iragarkien kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="8d949-141">In the **Choose your key identifier field**, select **Email**, **Name and address**, or **Phone** to send to Facebook Ads Manager.</span></span> 

1. <span data-ttu-id="8d949-142">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="8d949-142">Give your connection a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="8d949-143">Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.</span><span class="sxs-lookup"><span data-stu-id="8d949-143">Map the corresponding attributes from your unified customer entity for the selected key identifier.</span></span>
   > [!TIP]
   > <span data-ttu-id="8d949-144">Aukera onenak hautatuta baldin badaude **Helbide elektronikoa** gako identifikatzaile gisa.</span><span class="sxs-lookup"><span data-stu-id="8d949-144">The best chances for a match occur if you select **Email** as key identifier.</span></span> <span data-ttu-id="8d949-145">Identifikatzaile osagarriak gehitzeak bat egin dezake.</span><span class="sxs-lookup"><span data-stu-id="8d949-145">Adding additional identifiers may improve the matching.</span></span>

1. <span data-ttu-id="8d949-146">Aukeratu **Gehitu atributua** bidali beharreko atributu gehiago mapatzeko Facebook Iragarkien kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="8d949-146">Select **Add attribute** to map more attributes to send to Facebook Ads Manager.</span></span> <span data-ttu-id="8d949-147">Atributuak Facebook Iragarkien kudeatzailea erabiltzaileentzako lagunarteko izen hauek kokatzen dira: **FN** = **izena**, **LN** = **abizena**, **FI** = **Lehen Hasierakoa**, **TELEFONOA** = **Telefonoa**, **GEN** = **Generoa**, **DOB** = **Jaioteguna**, **ST** = **Estatu**, **CT** = **hiria**, **ZIP** = **Posta kodea / zip-kodea**, **HERRIALDEA** = **Herrialdea / Eskualdea**</span><span class="sxs-lookup"><span data-stu-id="8d949-147">Attributes from Facebook Ads Manager are mapping to the following user-friendly names: **FN** = **First Name**, **LN** = **Last Name**, **FI** = **First Initial**, **PHONE** = **Phone**, **GEN** = **Gender**, **DOB** = **Date of birth**, **ST** = **State**, **CT** = **City**, **ZIP** = **Postal code / ZIP Code**, **COUNTRY** = **Country / Region**</span></span>

1. <span data-ttu-id="8d949-148">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="8d949-148">Select the segments you want to export.</span></span>

1. <span data-ttu-id="8d949-149">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="8d949-149">Select **Save**.</span></span>

<span data-ttu-id="8d949-150">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="8d949-150">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="8d949-151">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="8d949-151">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> 

<span data-ttu-id="8d949-152">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="8d949-152">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="8d949-153">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="8d949-153">Data privacy and compliance</span></span>

<span data-ttu-id="8d949-154">Dynamics 365 Customer Insights gaitzen duzunean datuak Facebook-en iragarki-kudeatzailera bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="8d949-154">When you enable Dynamics 365 Customer Insights to transmit data to Facebook Ads Manager, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="8d949-155">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Facebook iragarkiek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="8d949-155">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Facebook Ads meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="8d949-156">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="8d949-156">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="8d949-157">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="8d949-157">Your Dynamics 365 Customer Insights administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
