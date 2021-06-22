---
title: Esportatu Customer Insights datuak Constant Contact
description: Ikasi konexioa konfiguratzen eta esportatzen Constant Contact.
ms.date: 03/22/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 29f4320c798db62609283e3c48f0b47a4f0b982f
ms.sourcegitcommit: 831765a55775d358447cb7ffa56f2c3b85459084
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6124258"
---
# <a name="export-segments-to-constant-contact-preview"></a><span data-ttu-id="79e3a-103">Esportatu segmentuak Constant Contact-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="79e3a-103">Export segments to Constant Contact (preview)</span></span>

<span data-ttu-id="79e3a-104">Esportatu bezeroen profil bateratuen segmentuak Constant Contact eta erabili marketin jardueretarako.</span><span class="sxs-lookup"><span data-stu-id="79e3a-104">Export segments of unified customer profiles to Constant Contact and use them for marketing activities.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="79e3a-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="79e3a-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="79e3a-106">Baduzu [Constant Contact kontua](https://www.constantcontact.com/account-home) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="79e3a-106">You have an [Constant Contact account](https://www.constantcontact.com/account-home) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="79e3a-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="79e3a-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="79e3a-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="79e3a-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="79e3a-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="79e3a-109">Known limitations</span></span>

- <span data-ttu-id="79e3a-110">Esportazio bakoitzeko milioi bat profil esportatu ditzakezu Constant Contact.</span><span class="sxs-lookup"><span data-stu-id="79e3a-110">You can export up to 1 million profiles per export to Constant Contact.</span></span>
- <span data-ttu-id="79e3a-111">Constant Contact esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="79e3a-111">Exporting to Constant Contact is limited to segments.</span></span>
- <span data-ttu-id="79e3a-112">Esportatu gehienez 1 milioi profil Constant Contact, 1 ordu behar ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="79e3a-112">Exporting up to 1 million profiles to Constant Contact can take up to 1 hour to complete.</span></span> 
- <span data-ttu-id="79e3a-113">Etengabeko kontaktua-ra esporta ditzakezun profilen kopurua Constant Contact-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="79e3a-113">The number of profiles that you can export to Constant Contact is dependent and limited on your contract with Constant Contact.</span></span>

## <a name="set-up-connection-to-constant-contact"></a><span data-ttu-id="79e3a-114">Konfiguratu konexioa Constant Contact-era</span><span class="sxs-lookup"><span data-stu-id="79e3a-114">Set up connection to Constant Contact</span></span>

1. <span data-ttu-id="79e3a-115">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="79e3a-115">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="79e3a-116">Hautatu **Gehitu konexioa** eta aukeratu **Constant Contact** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="79e3a-116">Select **Add connection** and choose **Constant Contact** to configure the connection.</span></span>

1. <span data-ttu-id="79e3a-117">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="79e3a-117">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="79e3a-118">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="79e3a-118">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="79e3a-119">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="79e3a-119">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="79e3a-120">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="79e3a-120">Choose who can use this connection.</span></span> <span data-ttu-id="79e3a-121">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="79e3a-121">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="79e3a-122">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="79e3a-122">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="79e3a-123">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="79e3a-123">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="79e3a-124">Aukeratu **Konektatu** Constant Contact konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="79e3a-124">Select **Connect** to initialize the connection to Constant Contact.</span></span>

1. <span data-ttu-id="79e3a-125">Aukeratu **Autenticatu AdRoll-ekin** eta eman zure administratzaile egiaztagiriak Constant Contact-erako.</span><span class="sxs-lookup"><span data-stu-id="79e3a-125">Select **Authenticate with AdRoll** and provide your admin credentials for Constant Contact.</span></span> 

1. <span data-ttu-id="79e3a-126">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="79e3a-126">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="79e3a-127">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="79e3a-127">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="79e3a-128">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="79e3a-128">Configure an export</span></span>

<span data-ttu-id="79e3a-129">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="79e3a-129">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="79e3a-130">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="79e3a-130">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="79e3a-131">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="79e3a-131">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="79e3a-132">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="79e3a-132">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="79e3a-133">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Constant Contact sekzioan.</span><span class="sxs-lookup"><span data-stu-id="79e3a-133">In the **Connection for export** field, choose a connection from the Constant Contact section.</span></span> <span data-ttu-id="79e3a-134">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="79e3a-134">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="79e3a-135">Idatzi zure [**Constant Contact zerrendaren IDa**](https://app.constantcontact.com/pages/contacts/ui#lists).</span><span class="sxs-lookup"><span data-stu-id="79e3a-135">Enter your [**Constant Contact List ID**](https://app.constantcontact.com/pages/contacts/ui#lists).</span></span> <span data-ttu-id="79e3a-136">Ireki zerrenda bat Constant Contact URL zerrendaren IDa aurkitzeko.</span><span class="sxs-lookup"><span data-stu-id="79e3a-136">Open a list in Constant Contact to find the list ID in the URL.</span></span>

1. <span data-ttu-id="79e3a-137">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="79e3a-137">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="79e3a-138">Segmentuak esportatu behar dira Constant Contact.</span><span class="sxs-lookup"><span data-stu-id="79e3a-138">It's required to export segments to Constant Contact.</span></span>

1. <span data-ttu-id="79e3a-139">Aukeran, izena eta abizena esporta ditzakezu mezu pertsonalizatuagoak sortzeko eremu osagarri gisa.</span><span class="sxs-lookup"><span data-stu-id="79e3a-139">Optionally, you can export First name and Last name as additional fields to create more personalized emails.</span></span> <span data-ttu-id="79e3a-140">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="79e3a-140">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="79e3a-141">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="79e3a-141">Select the segments you want to export.</span></span>

1. <span data-ttu-id="79e3a-142">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="79e3a-142">Select **Save**.</span></span>

<span data-ttu-id="79e3a-143">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="79e3a-143">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="79e3a-144">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="79e3a-144">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="79e3a-145">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="79e3a-145">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="79e3a-146">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="79e3a-146">Data privacy and compliance</span></span>

<span data-ttu-id="79e3a-147">Gaitzen duzunean Dynamics 365 Customer Insights datuak Constant Contact-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="79e3a-147">When you enable Dynamics 365 Customer Insights to transmit data to Constant Contact, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="79e3a-148">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Constant Contact-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz.</span><span class="sxs-lookup"><span data-stu-id="79e3a-148">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Constant Contact meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="79e3a-149">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="79e3a-149">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="79e3a-150">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="79e3a-150">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
