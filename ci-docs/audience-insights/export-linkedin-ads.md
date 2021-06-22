---
title: Esportatu Customer Insights datuak LinkedIn Ads-era
description: Ikasi konexioa konfiguratzen eta LinkedIn Ads-era esportatzen.
ms.date: 05/12/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 1c7b0c728bc4d4cf6b5aea79396cf0779fbf298d
ms.sourcegitcommit: 831765a55775d358447cb7ffa56f2c3b85459084
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6124449"
---
# <a name="export-segments-to-linkedin-ads-preview"></a><span data-ttu-id="a02b8-103">Esportatu segmentuak LinkedIn Ads-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="a02b8-103">Export segments to LinkedIn Ads (preview)</span></span>

<span data-ttu-id="a02b8-104">Esportatu bezeroen profil bateratuen segmentuak LinkedIn Ads-era bat datozen hartzaileak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="a02b8-104">Export segments of unified customer profiles to LinkedIn Ads to create matched audiences.</span></span> <span data-ttu-id="a02b8-105">Erabili bat datozen hartzaileak enpresaren bideratzerako eta kontaktuen bideratzerako.</span><span class="sxs-lookup"><span data-stu-id="a02b8-105">Use the matched audiences for company targeting and contact targeting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a02b8-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="a02b8-106">Prerequisites</span></span>

-   <span data-ttu-id="a02b8-107">Badituzu [LinkedIn Campaign Manager kontua](https://business.linkedin.com/marketing-solutions/ads) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="a02b8-107">You have an [LinkedIn Campaign Manager account](https://business.linkedin.com/marketing-solutions/ads) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="a02b8-108">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="a02b8-108">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="a02b8-109">Esportatutako segmentuetako bezeroen profilek helbide elektronikoa duen eremu bat dute.</span><span class="sxs-lookup"><span data-stu-id="a02b8-109">Customer profiles in the exported segments contain a field with an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="a02b8-110">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="a02b8-110">Known limitations</span></span>

- <span data-ttu-id="a02b8-111">Esportazio bakoitzeko 100.000 profil esportatu ditzakezu LinkedIn Ads-era.</span><span class="sxs-lookup"><span data-stu-id="a02b8-111">You can export up to 100K profiles per export to LinkedIn Ads.</span></span>
- <span data-ttu-id="a02b8-112">LinkedIn Ads-era esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="a02b8-112">Exporting to LinkedIn Ads is limited to segments.</span></span>
- <span data-ttu-id="a02b8-113">Esportatu gehienez 100.000 profil LinkedIn Ads-era, 10 minutu behar ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="a02b8-113">Exporting up to 100K profiles to LinkedIn Ads can take up to 10 minutes to complete.</span></span> 

## <a name="set-up-the-connection-to-linkedin-ads"></a><span data-ttu-id="a02b8-114">Konfiguratu konexioa LinkedIn Ads-era</span><span class="sxs-lookup"><span data-stu-id="a02b8-114">Set up the connection to LinkedIn Ads</span></span>

1. <span data-ttu-id="a02b8-115">Ikusleen ikuspegietan, joan hona **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="a02b8-115">In audience insights, go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="a02b8-116">Hautatu **Gehitu konexioa** eta aukeratu **LinkedIn Ads** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="a02b8-116">Select **Add connection** and choose **LinkedIn Ads** to configure the connection.</span></span>

1. <span data-ttu-id="a02b8-117">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="a02b8-117">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="a02b8-118">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="a02b8-118">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="a02b8-119">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="a02b8-119">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="a02b8-120">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="a02b8-120">Choose who can use this connection.</span></span> <span data-ttu-id="a02b8-121">Inolako neurririk hartzen ez baduzu, lehenetsia da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="a02b8-121">If you take no action, the default is administrators.</span></span> <span data-ttu-id="a02b8-122">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="a02b8-122">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="a02b8-123">Eman zure [LinkedIn Campaign Manager Kontuaren IDa](https://www.linkedin.com/help/lms/answer/a424270).</span><span class="sxs-lookup"><span data-stu-id="a02b8-123">Provide your [LinkedIn Campaign Manager Account ID](https://www.linkedin.com/help/lms/answer/a424270).</span></span>

1. <span data-ttu-id="a02b8-124">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="a02b8-124">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="a02b8-125">Aukeratu **Konektatu** Campaign Monitor konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="a02b8-125">Select **Connect** to initialize the connection to Campaign Monitor.</span></span>

1. <span data-ttu-id="a02b8-126">Aukeratu **Autentifikatu LinkedIn-ekin** eta eman zure administratzaile egiaztagiriak LinkedIn Campaign Manager-erako.</span><span class="sxs-lookup"><span data-stu-id="a02b8-126">Select **Authenticate with LinkedIn** and provide your admin credentials for LinkedIn Campaign Manager.</span></span>

1. <span data-ttu-id="a02b8-127">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="a02b8-127">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="a02b8-128">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="a02b8-128">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="a02b8-129">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="a02b8-129">Configure an export</span></span>

<span data-ttu-id="a02b8-130">Esportazio bat konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="a02b8-130">You can configure an export if you have access to a connection of this type.</span></span> <span data-ttu-id="a02b8-131">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="a02b8-131">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="a02b8-132">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="a02b8-132">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="a02b8-133">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="a02b8-133">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="a02b8-134">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa LinkedIn Ads sekzioan.</span><span class="sxs-lookup"><span data-stu-id="a02b8-134">In the **Connection for export** field, choose a connection from the LinkedIn Ads section.</span></span> <span data-ttu-id="a02b8-135">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="a02b8-135">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="a02b8-136">Aukeratu egin nahi dituzun datuak esportatu nahi dituzun ala ez [kontaktuen bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/contact-targeting) edo [enpresen bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/account-targeting) egiteko LinkedIn-en.</span><span class="sxs-lookup"><span data-stu-id="a02b8-136">Choose whether you want to export data to do [contact targeting](https://business.linkedin.com/marketing-solutions/ad-targeting/contact-targeting) or [company targeting](https://business.linkedin.com/marketing-solutions/ad-targeting/account-targeting) on LinkedIn.</span></span> 

1. <span data-ttu-id="a02b8-137">**Datuen bat etortzea** atalean, hautatu bezeroaren profil bateratuko bezero baten helbide elektronikoa adierazten duen eremua.</span><span class="sxs-lookup"><span data-stu-id="a02b8-137">In the **Data matching** section, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="a02b8-138">Segmentuak esportatu behar dira LinkedIn Ads-era.</span><span class="sxs-lookup"><span data-stu-id="a02b8-138">It's required to export segments to LinkedIn Ads.</span></span>

1. <span data-ttu-id="a02b8-139">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="a02b8-139">Select the segments you want to export.</span></span> <span data-ttu-id="a02b8-140">LinkedIn Campaign Manager-eko bat datozen hartzaileak automatikoki sortuko dira esportatzeko hautatu dituzun segmentuen izenarekin.</span><span class="sxs-lookup"><span data-stu-id="a02b8-140">The matched audiences in LinkedIn Campaign Manager will automatically be created with the name of the segments that you selected to export.</span></span> <span data-ttu-id="a02b8-141">Segmentu bakoitzak bat datorren hartzaile bereizi bat sortuko du.</span><span class="sxs-lookup"><span data-stu-id="a02b8-141">Each segment will result in a separate matched audience.</span></span> 

1. <span data-ttu-id="a02b8-142">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="a02b8-142">Select **Save**.</span></span>

<span data-ttu-id="a02b8-143">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="a02b8-143">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="a02b8-144">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="a02b8-144">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="a02b8-145">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="a02b8-145">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="a02b8-146">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="a02b8-146">Data privacy and compliance</span></span>

<span data-ttu-id="a02b8-147">Gaitzen duzunean Dynamics 365 Customer Insights datuak LinkedIn Ads-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="a02b8-147">When you enable Dynamics 365 Customer Insights to transmit data to LinkedIn Ads, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="a02b8-148">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara LinkedIn Ads-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz.</span><span class="sxs-lookup"><span data-stu-id="a02b8-148">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that LinkedIn Ads meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="a02b8-149">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="a02b8-149">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="a02b8-150">Funtzio hau erabiltzeari uzteko, esportazioaren helburuko kokaleku hori ken dezake Dynamics 365 Customer Insights administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="a02b8-150">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to stop the use of this functionality.</span></span>
