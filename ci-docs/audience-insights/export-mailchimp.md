---
title: Esportatu Customer Insights datuak Mailchimp-era
description: Ikasi Mailchimp-erako konexioa nola konfiguratu.
ms.date: 10/26/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 2b465b32fa956e3f45a23f471dc3a3183def16ef
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267158"
---
# <a name="connector-for-mailchimp-preview"></a><span data-ttu-id="271b6-103">Mailchimp-eko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="271b6-103">Connector for Mailchimp (preview)</span></span>

<span data-ttu-id="271b6-104">Esportatu bezero profil bateratuen segmentuak Mailchimp-era buletinak eta posta elektronikoko kanpainak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="271b6-104">Export segments of unified customer profiles to Mailchimp to create newsletters and email campaigns.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="271b6-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="271b6-105">Prerequisites</span></span>

-   <span data-ttu-id="271b6-106">Baduzu [Mailchimp kontua](https://mailchimp.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="271b6-106">You have a [Mailchimp account](https://mailchimp.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="271b6-107">Mailchimp-en hartzaileak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="271b6-107">There are existing audiences in Mailchimp and the corresponding IDs.</span></span> <span data-ttu-id="271b6-108">Informazio gehiagorako, ikus [Mailchimp-eko hartzaileak](https://mailchimp.com/help/create-audience/).</span><span class="sxs-lookup"><span data-stu-id="271b6-108">For more information, see [Mailchimp audiences](https://mailchimp.com/help/create-audience/).</span></span>
-   <span data-ttu-id="271b6-109">[Konfiguratutako segmentuak](segments.md) dituzu</span><span class="sxs-lookup"><span data-stu-id="271b6-109">You have [configured segments](segments.md)</span></span>
-   <span data-ttu-id="271b6-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="271b6-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="connect-to-mailchimp"></a><span data-ttu-id="271b6-111">Konektatu Mailchimp-era</span><span class="sxs-lookup"><span data-stu-id="271b6-111">Connect to Mailchimp</span></span>

1. <span data-ttu-id="271b6-112">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="271b6-112">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="271b6-113">**Mailchimp** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="271b6-113">Under **Mailchimp**, select **Set up**.</span></span>

1. <span data-ttu-id="271b6-114">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="271b6-114">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="271b6-115">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="271b6-115">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="271b6-116">Sartu zure **[Mailchimp hartzaileen IDa](https://mailchimp.com/help/find-audience-id/)** eta hautatu **Konektatu** Mailchimp-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="271b6-116">Enter your **[Mailchimp audience ID](https://mailchimp.com/help/find-audience-id/)** and select **Connect** to initialize the connection to Mailchimp.</span></span>

1. <span data-ttu-id="271b6-117">Aukeratu **Egiaztatu Mailchimp-ekin** eta eman zure Mailchimp kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="271b6-117">Select **Authenticate with Mailchimp** and provide your Mailchimp credentials.</span></span>

1. <span data-ttu-id="271b6-118">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="271b6-118">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

   :::image type="content" source="media/export-connect-mailchimp.png" alt-text="Esportatu pantaila-argazkia Mailchimp konexiorako":::

1. <span data-ttu-id="271b6-120">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="271b6-120">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="271b6-121">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="271b6-121">Configure the connector</span></span>

1. <span data-ttu-id="271b6-122">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="271b6-122">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> 

1. <span data-ttu-id="271b6-123">Aukeran, **izena** eta **abizena** esporta ditzakezu mezu pertsonalizatuagoak sortzeko eremu osagarri gisa.</span><span class="sxs-lookup"><span data-stu-id="271b6-123">Optionally, you can export **First name** and **Last name** as additional fields to create more personalized emails.</span></span> <span data-ttu-id="271b6-124">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="271b6-124">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="271b6-125">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="271b6-125">Select the segments you want to export.</span></span> <span data-ttu-id="271b6-126">Guztira 1 milioi bezero profil esporta ditzakezu Mailchimp-era.</span><span class="sxs-lookup"><span data-stu-id="271b6-126">You can export up to 1 million customer profiles in total to Mailchimp.</span></span>

   :::image type="content" source="media/export-segments-mailchimp.png" alt-text="Aukeratu eremuak eta segmentuak Mailchimp-era esportatzeko":::

1. <span data-ttu-id="271b6-128">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="271b6-128">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="271b6-129">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="271b6-129">Export the data</span></span>

<span data-ttu-id="271b6-130">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="271b6-130">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="271b6-131">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="271b6-131">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="271b6-132">Mailchimp-en, zure segmentuak azpian aurki ditzakezu hemen: [Mailchimp-eko hartzaileak](https://mailchimp.com/help/create-audience/).</span><span class="sxs-lookup"><span data-stu-id="271b6-132">In Mailchimp, you can now find your segments under [Mailchimp audiences](https://mailchimp.com/help/create-audience/).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="271b6-133">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="271b6-133">Known limitations</span></span>

- <span data-ttu-id="271b6-134">Gehienez milioi bat profil Mailchimp-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="271b6-134">Up to 1 million profiles per export to Mailchimp.</span></span>
- <span data-ttu-id="271b6-135">Mailchimp-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="271b6-135">Exporting to Mailchimp is limited to segments.</span></span>
- <span data-ttu-id="271b6-136">Guztira 1 milioi profil dituzten segmentuak esportatzeak hiru ordu arte iraun dezake hornitzailearen aldetik mugak direla eta.</span><span class="sxs-lookup"><span data-stu-id="271b6-136">Exporting segments with a total of 1 million profiles can take up to three hours due to limitations on the provider side.</span></span> 
- <span data-ttu-id="271b6-137">Mailchimp-era esporta ditzakezun profilen kopurua Mailchimp-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="271b6-137">The number of profiles that you can export to Mailchimp is dependent and limited on your contract with Mailchimp.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="271b6-138">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="271b6-138">Data privacy and compliance</span></span>

<span data-ttu-id="271b6-139">Dynamics 365 Customer Insights gaitzen duzunean datuak Mailchimp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="271b6-139">When you enable Dynamics 365 Customer Insights to transmit data to Mailchimp, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="271b6-140">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Mailchimp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="271b6-140">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Mailchimp meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="271b6-141">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="271b6-141">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="271b6-142">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="271b6-142">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]