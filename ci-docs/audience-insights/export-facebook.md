---
title: Esportatu Customer Insights datuak Facebook iragarki-kudeatzailera
description: Ikasi konexioa konfiguratzen eta esportatzen Facebook Iragarkien kudeatzailea.
ms.date: 04/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: ca32906a98bc734639fb369d6f5a92e8888fd850
ms.sourcegitcommit: 6d5dd572f75ba4c0303ec77c3b74e4318d52705c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906795"
---
# <a name="export-segments-list-to-facebook-ads-manager-preview"></a><span data-ttu-id="35eff-103">Esportatu segmentuen zerrenda Facebook Iragarkien kudeatzailea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="35eff-103">Export segments list to Facebook Ads Manager (preview)</span></span>

<span data-ttu-id="35eff-104">Bezeroen profil bateratuen segmentuak esportatu Facebook Iragarkien kudeatzailea kanpainak sortzeko Facebook eta Instagram.</span><span class="sxs-lookup"><span data-stu-id="35eff-104">Export segments of unified customer profiles to Facebook Ads Manager to create campaigns on Facebook and Instagram.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="35eff-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="35eff-105">Prerequisites for connection</span></span>

- <span data-ttu-id="35eff-106">Izan behar duzu [**Facebook iragazki-kontua**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) barne hartzen duena [**Facebook negozio-kontua**](https://business.facebook.com/).</span><span class="sxs-lookup"><span data-stu-id="35eff-106">You need to have a [**Facebook Ad Account**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) that includes a [**Facebook Business Account**](https://business.facebook.com/).</span></span>
- <span data-ttu-id="35eff-107">[**Facebook Iragarkien kontuaren**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) administratzaile izan behar duzu.</span><span class="sxs-lookup"><span data-stu-id="35eff-107">You need to be an administrator on the [**Facebook Ad Account**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="35eff-108">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="35eff-108">Known limitations</span></span>

- <span data-ttu-id="35eff-109">Gehienez 10 milioi bezeroren profila esportazio bakoitzeko Facebook Ads kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="35eff-109">Up to 10 million customer profile per export to Facebook Ads Manager.</span></span>
- <span data-ttu-id="35eff-110">Esportatu Facebook Ads-eko kudeatzailera esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="35eff-110">Export to Facebook Ads Manager is limited to segments.</span></span>
- <span data-ttu-id="35eff-111">Sortu edo eguneratu audientzia pertsonalizatuak hemen Facebook motakoa *bezeroen zerrenda* bakarrik.</span><span class="sxs-lookup"><span data-stu-id="35eff-111">Create or update custom audiences in Facebook of type *customer list* only.</span></span>
- <span data-ttu-id="35eff-112">Guztira 10 milioi profil dituzten segmentuak esportatzen 90 minutu behar izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="35eff-112">Exporting segments with a total of 10 million profiles can take up to 90 minutes to complete.</span></span>

## <a name="set-up-connection-to-facebook-ads-manager"></a><span data-ttu-id="35eff-113">Konfiguratu konexioa Facebook iragarkien kudeatzailea</span><span class="sxs-lookup"><span data-stu-id="35eff-113">Set up connection to Facebook Ads Manager</span></span>

<span data-ttu-id="35eff-114">Erabiltzaileek esportazio bat sortu aurretik, administratzaile batek zerbitzurako konexioa konfiguratu behar du eta laguntzaileei konexioa erabiltzeko baimena eman behar die.</span><span class="sxs-lookup"><span data-stu-id="35eff-114">Before users can create an export, an administrator must configure the connection to the service and allow contributors to use the connection.</span></span>

1. <span data-ttu-id="35eff-115">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="35eff-115">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="35eff-116">Aukeratu **Gehitu konexioa** eta aukeratu **Facebook Iragarkien kudeatzailea** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="35eff-116">Select **Add connection** and choose **Facebook Ads Manager** to configure the connection.</span></span>

1. <span data-ttu-id="35eff-117">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="35eff-117">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="35eff-118">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="35eff-118">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="35eff-119">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="35eff-119">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="35eff-120">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="35eff-120">Choose who can use this connection.</span></span> <span data-ttu-id="35eff-121">Inolako neurririk hartzen ez baduzu, lehenetsia izango da **Administratzaileak**.</span><span class="sxs-lookup"><span data-stu-id="35eff-121">If you take no action, the default will be **Administrators**.</span></span> <span data-ttu-id="35eff-122">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="35eff-122">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="35eff-123">Autentifikatu Facebook iragarkiekin:</span><span class="sxs-lookup"><span data-stu-id="35eff-123">Authenticate with Facebook Ads:</span></span> 

   1. <span data-ttu-id="35eff-124">Aukeratu **Jarraitu aurrera Facebook** saioa hasteko Facebook Iragarkien kontua.</span><span class="sxs-lookup"><span data-stu-id="35eff-124">Select **Continue with Facebook** to sign in to your Facebook Ad Account.</span></span>

   1. <span data-ttu-id="35eff-125">Onartu **iragarkien kudeaketa** baimena, Facebook-ekin autentifikatu ondoren.</span><span class="sxs-lookup"><span data-stu-id="35eff-125">Allow the **ads_management** permission after authenticating with Facebook.</span></span>

   1. <span data-ttu-id="35eff-126">Hautatu **Facebook iragarki kontua** lan egin nahi duzunarekin.</span><span class="sxs-lookup"><span data-stu-id="35eff-126">Select the **Facebook Ads Account** that you want to work with.</span></span>

   1. <span data-ttu-id="35eff-127">Aukeratu bat **Existitzen den audientzia pertsonalizatua** goitibeherako zerrendatik edo sortu bat **Ohiko audientzia berriak**.</span><span class="sxs-lookup"><span data-stu-id="35eff-127">Select an **Existing custom audience** from the drop-down list or create a **New custom audience**.</span></span> <span data-ttu-id="35eff-128">Informazio gehiago lortzeko, ikus [**Ikusleak Facebook Iragarkien kudeatzailea**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).</span><span class="sxs-lookup"><span data-stu-id="35eff-128">For more information, see [**Audiences in Facebook Ads Manager**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).</span></span>
      > [!NOTE]
      > <span data-ttu-id="35eff-129">Ikusle pertsonalizatuak soilik sor ditzakezu edo eguneratu Facebook motakoa *bezeroen zerrenda* esportazio honekin.</span><span class="sxs-lookup"><span data-stu-id="35eff-129">You can only create or update custom audiences on Facebook of the type *customer list* with this export.</span></span> <span data-ttu-id="35eff-130">Zenbait kasutan, goitibeherako zerrendan mota desberdinetako ikusle pertsonalizatuak ikusten dituzu.</span><span class="sxs-lookup"><span data-stu-id="35eff-130">In some cases, you see custom audiences of different types in the drop-down list.</span></span> <span data-ttu-id="35eff-131">Ez bezalako mota bat hautatzea *bezeroen zerrenda* esportazioak huts egingo du.</span><span class="sxs-lookup"><span data-stu-id="35eff-131">Selecting a different type than *customer list* will result in a failing export.</span></span> 

1. <span data-ttu-id="35eff-132">Berrikusi **Datuen pribatutasuna eta betetzea** eta hautatu **ados**.</span><span class="sxs-lookup"><span data-stu-id="35eff-132">Review the **Data privacy and compliance** and select **I agree**.</span></span>

1. <span data-ttu-id="35eff-133">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="35eff-133">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="35eff-134">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="35eff-134">Configure an export</span></span>

<span data-ttu-id="35eff-135">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="35eff-135">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="35eff-136">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="35eff-136">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="35eff-137">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="35eff-137">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="35eff-138">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="35eff-138">To create a new export, select **Add destination**.</span></span> 

1. <span data-ttu-id="35eff-139">Hurrengoan **Esportaziorako konexioa** Aukeratu konexioa **Facebook Iragarkien kudeatzailea** atala.</span><span class="sxs-lookup"><span data-stu-id="35eff-139">In **Connection for export** choose a connection from the **Facebook Ads Manager** section.</span></span> <span data-ttu-id="35eff-140">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="35eff-140">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="35eff-141">Sarbidean **Aukeratu zure gako identifikatzaileen eremua** hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** bidali Facebook Iragarkien kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="35eff-141">In the **Choose your key identifier field**, select **Email**, **Name and address**, or **Phone** to send to Facebook Ads Manager.</span></span> 

1. <span data-ttu-id="35eff-142">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="35eff-142">Give your connection a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="35eff-143">Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.</span><span class="sxs-lookup"><span data-stu-id="35eff-143">Map the corresponding attributes from your unified customer entity for the selected key identifier.</span></span>
   > <span data-ttu-id="35eff-144">[AHOLKULUA] Partidua lortzeko aukera onenak hautatuta baldin badaude **Emaila** gako identifikatzaile gisa.</span><span class="sxs-lookup"><span data-stu-id="35eff-144">[TIP] The best chances for a match occur if you select **Email** as key identifier.</span></span> <span data-ttu-id="35eff-145">Identifikatzaile osagarriak gehitzeak bat egin dezake.</span><span class="sxs-lookup"><span data-stu-id="35eff-145">Adding additional identifiers may improve the matching.</span></span>

1. <span data-ttu-id="35eff-146">Aukeratu **Gehitu atributua** bidali beharreko atributu gehiago mapatzeko Facebook Iragarkien kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="35eff-146">Select **Add attribute** to map more attributes to send to Facebook Ads Manager.</span></span> <span data-ttu-id="35eff-147">Atributuak Facebook Iragarkien kudeatzailea erabiltzaileentzako lagunarteko izen hauek kokatzen dira: **FN** = **izena**, **LN** = **abizena**, **FI** = **Lehen Hasierakoa**, **TELEFONOA** = **Telefonoa**, **GEN** = **Generoa**, **DOB** = **Jaioteguna**, **ST** = **Estatu**, **CT** = **hiria**, **ZIP** = **Posta kodea / zip kodea**, **HERRIALDEA** = **Herrialdea / Eskualdea**</span><span class="sxs-lookup"><span data-stu-id="35eff-147">Attributes from Facebook Ads Manager are mapping to the following user-friendly names: **FN** = **First Name**, **LN** = **Last Name**, **FI** = **First Initial**, **PHONE** = **Phone**, **GEN** = **Gender**, **DOB** = **Date of birth**, **ST** = **State**, **CT** = **City**, **ZIP** = **Postal code / Zip code**, **COUNTRY** = **Country / Region**</span></span>

1. <span data-ttu-id="35eff-148">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="35eff-148">Select the segments you want to export.</span></span>

1. <span data-ttu-id="35eff-149">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="35eff-149">Select **Save**.</span></span>

<span data-ttu-id="35eff-150">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="35eff-150">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="35eff-151">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="35eff-151">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="35eff-152">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="35eff-152">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="35eff-153">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="35eff-153">Data privacy and compliance</span></span>

<span data-ttu-id="35eff-154">Dynamics 365 Customer Insights gaitzen duzunean datuak  Facebook-en iragarki-kudeatzailera bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="35eff-154">When you enable Dynamics 365 Customer Insights to transmit data to Facebook Ads Manager, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="35eff-155">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Facebook iragarkiek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="35eff-155">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Facebook Ads meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="35eff-156">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="35eff-156">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="35eff-157">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="35eff-157">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
