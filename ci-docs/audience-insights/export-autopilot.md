---
title: Esportatu Customer Insights datuak Autopilot-era
description: Ikasi konexioa konfiguratzen eta pilotu automatora esportatzen.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: e320a48d5b7c35b530e3a38567b226b804879e4e
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760082"
---
# <a name="export-segments-to-autopilot-preview"></a><span data-ttu-id="4598b-103">Esportatu segmentuak Autopilot-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="4598b-103">Export segments to Autopilot (preview)</span></span>

<span data-ttu-id="4598b-104">Esportatu bezeroen profil bateratuen segmentuak Autopilot kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko Autopilot-en.</span><span class="sxs-lookup"><span data-stu-id="4598b-104">Export segments of unified customer profiles to Autopilot and use them for email marketing in Autopilot.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="4598b-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="4598b-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="4598b-106">Baduzu [Autopilot kontua](https://www.autopilothq.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="4598b-106">You have an [Autopilot account](https://www.autopilothq.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="4598b-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="4598b-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="4598b-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="4598b-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="4598b-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="4598b-109">Known limitations</span></span>

- <span data-ttu-id="4598b-110">Guztira 100.000 bezero-profil esporta ditzakezu Autopilot-era.</span><span class="sxs-lookup"><span data-stu-id="4598b-110">You can export up to 100'000 profiles in total to Autopilot.</span></span>
- <span data-ttu-id="4598b-111">Autopilot-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="4598b-111">Exporting to Autopilot is limited to segments.</span></span>
- <span data-ttu-id="4598b-112">Autopilot-era 100.000 profil gehienera esportatzeak ordu batzuk behar izan ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="4598b-112">Exporting up to 100'000 profiles to Autopilot can take up to a few hours to complete.</span></span> 
- <span data-ttu-id="4598b-113">Autopilot-era esporta ditzakezun profilen kopurua Autopilot-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="4598b-113">The number of profiles that you can export to Autopilot is dependent and limited on your contract with Autopilot.</span></span>

## <a name="set-up-connection-to-autopilot"></a><span data-ttu-id="4598b-114">Konfiguratu konexioa Autopilot-era</span><span class="sxs-lookup"><span data-stu-id="4598b-114">Set up connection to Autopilot</span></span>

1. <span data-ttu-id="4598b-115">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="4598b-115">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="4598b-116">Hautatu **Gehitu konexioa** eta aukeratu **Autopilot** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="4598b-116">Select **Add connection** and choose **Autopilot** to configure the connection.</span></span>

1. <span data-ttu-id="4598b-117">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="4598b-117">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="4598b-118">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="4598b-118">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="4598b-119">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="4598b-119">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="4598b-120">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="4598b-120">Choose who can use this connection.</span></span> <span data-ttu-id="4598b-121">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="4598b-121">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="4598b-122">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="4598b-122">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

3. <span data-ttu-id="4598b-123">Sartu zure [Pilotatze automatikoaren API gakoa](https://autopilot.docs.apiary.io/#).</span><span class="sxs-lookup"><span data-stu-id="4598b-123">Enter your [Autopilot API key](https://autopilot.docs.apiary.io/#).</span></span>

1. <span data-ttu-id="4598b-124">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="4598b-124">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="4598b-125">Aukeratu **Konektatu** Autopilot-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="4598b-125">Select **Connect** to initialize the connection to Autopilot.</span></span>

1. <span data-ttu-id="4598b-126">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="4598b-126">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="4598b-127">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="4598b-127">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="4598b-128">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="4598b-128">Configure an export</span></span>

<span data-ttu-id="4598b-129">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="4598b-129">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="4598b-130">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="4598b-130">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="4598b-131">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="4598b-131">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="4598b-132">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="4598b-132">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="4598b-133">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Autopilot sekzioan.</span><span class="sxs-lookup"><span data-stu-id="4598b-133">In the **Connection for export** field, choose a connection from the Autopilot section.</span></span> <span data-ttu-id="4598b-134">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="4598b-134">If you don't see this section name, there are no connections of this type available to you.</span></span>

3. <span data-ttu-id="4598b-135">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="4598b-135">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="4598b-136">Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena** eta **abizena**.</span><span class="sxs-lookup"><span data-stu-id="4598b-136">Repeat the same steps for other optional fields such as **First name**, **Last name**.</span></span>

1. <span data-ttu-id="4598b-137">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="4598b-137">Select the segments you want to export.</span></span> <span data-ttu-id="4598b-138">Biziki **gomendatzen dugu 100.000 bezero profil baino gehiago ez esportatzea guztira** Autopilot-era.</span><span class="sxs-lookup"><span data-stu-id="4598b-138">We strongly **recommend to not export more than 100'000 customer profiles in total** to Autopilot.</span></span> 

1. <span data-ttu-id="4598b-139">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="4598b-139">Select **Save**.</span></span>

<span data-ttu-id="4598b-140">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="4598b-140">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="4598b-141">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="4598b-141">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="4598b-142">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="4598b-142">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="4598b-143">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="4598b-143">Data privacy and compliance</span></span>

<span data-ttu-id="4598b-144">Dynamics 365 Customer Insights gaitzen duzunean datuak Autopilot-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="4598b-144">When you enable Dynamics 365 Customer Insights to transmit data to Autopilot, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="4598b-145">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Autopilot-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="4598b-145">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Autopilot meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="4598b-146">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="4598b-146">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="4598b-147">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="4598b-147">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
