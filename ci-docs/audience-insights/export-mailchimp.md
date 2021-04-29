---
title: Esportatu Customer Insights datuak Mailchimp-era
description: Ikasi konexioa konfiguratzen eta Mailchimp-era esportatzen.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: b94a8e8b6bb867ca04a64007d592b22fbd700618
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5759863"
---
# <a name="export-segment-lists-to-mailchimp-preview"></a><span data-ttu-id="399c9-103">Esportatu segmentuen zerrendak Mailchimp (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="399c9-103">Export segment lists to Mailchimp (preview)</span></span>

<span data-ttu-id="399c9-104">Esportatu bezero profil bateratuen segmentuak Mailchimp-era buletinak eta posta elektronikoko kanpainak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="399c9-104">Export segments of unified customer profiles to Mailchimp to create newsletters and email campaigns.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="399c9-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="399c9-105">Prerequisites for connection</span></span>

-   <span data-ttu-id="399c9-106">Baduzu [Mailchimp kontua](https://mailchimp.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="399c9-106">You have a [Mailchimp account](https://mailchimp.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="399c9-107">Mailchimp-en hartzaileak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="399c9-107">There are existing audiences in Mailchimp and the corresponding IDs.</span></span> <span data-ttu-id="399c9-108">Informazio gehiagorako, ikus [Mailchimp-eko hartzaileak](https://mailchimp.com/help/create-audience/).</span><span class="sxs-lookup"><span data-stu-id="399c9-108">For more information, see [Mailchimp audiences](https://mailchimp.com/help/create-audience/).</span></span>
-   <span data-ttu-id="399c9-109">[Konfiguratutako segmentuak](segments.md) dituzu</span><span class="sxs-lookup"><span data-stu-id="399c9-109">You have [configured segments](segments.md)</span></span>
-   <span data-ttu-id="399c9-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="399c9-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="399c9-111">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="399c9-111">Known limitations</span></span>

- <span data-ttu-id="399c9-112">Gehienez milioi bat profil Mailchimp-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="399c9-112">Up to 1 million profiles per export to Mailchimp.</span></span>
- <span data-ttu-id="399c9-113">Mailchimp-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="399c9-113">Exporting to Mailchimp is limited to segments.</span></span>
- <span data-ttu-id="399c9-114">Milioi profileko segmentuak esportatzeak hiru ordu arte iraun dezake.</span><span class="sxs-lookup"><span data-stu-id="399c9-114">Exporting segments with 1 million profiles can take up to three hours.</span></span> 
- <span data-ttu-id="399c9-115">Mailchimp-era esporta ditzakezun profilen kopurua Mailchimp-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="399c9-115">The number of profiles that you can export to Mailchimp is dependent and limited on your contract with Mailchimp.</span></span>

## <a name="set-up-connection-to-mailchimp"></a><span data-ttu-id="399c9-116">Konfiguratu konexioa Mailchimp-era</span><span class="sxs-lookup"><span data-stu-id="399c9-116">Set up connection to Mailchimp</span></span>

1. <span data-ttu-id="399c9-117">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="399c9-117">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="399c9-118">Hautatu **Gehitu konexioa** eta aukeratu **Autopilot** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="399c9-118">Select **Add connection** and choose **Autopilot** to configure the connection.</span></span>

1. <span data-ttu-id="399c9-119">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="399c9-119">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="399c9-120">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="399c9-120">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="399c9-121">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="399c9-121">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="399c9-122">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="399c9-122">Choose who can use this connection.</span></span> <span data-ttu-id="399c9-123">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="399c9-123">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="399c9-124">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="399c9-124">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="399c9-125">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="399c9-125">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="399c9-126">Aukeratu **Konektatu** Mailchimp konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="399c9-126">Select **Connect** to initialize the connection to Mailchimp.</span></span>

1. <span data-ttu-id="399c9-127">Aukeratu **Egiaztatu Mailchimp-ekin** eta eman zure Mailchimp kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="399c9-127">Select **Authenticate with Mailchimp** and provide your Mailchimp credentials.</span></span>

1. <span data-ttu-id="399c9-128">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="399c9-128">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="399c9-129">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="399c9-129">Select **Save** to complete the connection.</span></span> 

## <a name="configure-the-connector"></a><span data-ttu-id="399c9-130">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="399c9-130">Configure the connector</span></span>

<span data-ttu-id="399c9-131">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="399c9-131">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="399c9-132">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="399c9-132">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="399c9-133">Joan **Datuak**> **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="399c9-133">Go to **Data**> **Exports**.</span></span>

1. <span data-ttu-id="399c9-134">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="399c9-134">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="399c9-135">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Mailchimp sekzioan.</span><span class="sxs-lookup"><span data-stu-id="399c9-135">In the **Connection for export** field, choose a connection from the Mailchimp section.</span></span> <span data-ttu-id="399c9-136">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="399c9-136">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="399c9-137">Idatzi **[Mailchimp audientzia ID](https://mailchimp.com/help/find-audience-id/)**</span><span class="sxs-lookup"><span data-stu-id="399c9-137">Enter your **[Mailchimp audience ID](https://mailchimp.com/help/find-audience-id/)**</span></span>

3. <span data-ttu-id="399c9-138">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="399c9-138">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> 

1. <span data-ttu-id="399c9-139">Aukeran, esporta dezakezu **izen** eta **abizen** mezu elektroniko pertsonalizatuagoak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="399c9-139">Optionally, you can export **First name** and **Last name** to create more personalized emails.</span></span> <span data-ttu-id="399c9-140">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="399c9-140">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="399c9-141">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="399c9-141">Select the segments you want to export.</span></span> <span data-ttu-id="399c9-142">Guztira 1 milioi bezero profil esporta ditzakezu Mailchimp-era.</span><span class="sxs-lookup"><span data-stu-id="399c9-142">You can export up to 1 million customer profiles in total to Mailchimp.</span></span>

1. <span data-ttu-id="399c9-143">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="399c9-143">Select **Save**.</span></span>

<span data-ttu-id="399c9-144">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="399c9-144">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="399c9-145">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="399c9-145">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="399c9-146">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="399c9-146">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="399c9-147">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="399c9-147">Data privacy and compliance</span></span>

<span data-ttu-id="399c9-148">Dynamics 365 Customer Insights gaitzen duzunean datuak Mailchimp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="399c9-148">When you enable Dynamics 365 Customer Insights to transmit data to Mailchimp, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="399c9-149">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Mailchimp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="399c9-149">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Mailchimp meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="399c9-150">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="399c9-150">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="399c9-151">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="399c9-151">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
