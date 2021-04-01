---
title: Esportatu Customer Insights datuak Mailchimp-era
description: Ikasi Mailchimp-erako konexioa nola konfiguratu.
ms.date: 10/26/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 9f86616731c3cc3d26370727103ea9c5d4288c8d
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5598186"
---
# <a name="connector-for-mailchimp-preview"></a><span data-ttu-id="b7267-103">Mailchimp-eko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="b7267-103">Connector for Mailchimp (preview)</span></span>

<span data-ttu-id="b7267-104">Esportatu bezero profil bateratuen segmentuak Mailchimp-era buletinak eta posta elektronikoko kanpainak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="b7267-104">Export segments of unified customer profiles to Mailchimp to create newsletters and email campaigns.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b7267-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="b7267-105">Prerequisites</span></span>

-   <span data-ttu-id="b7267-106">Baduzu [Mailchimp kontua](https://mailchimp.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="b7267-106">You have a [Mailchimp account](https://mailchimp.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="b7267-107">Mailchimp-en hartzaileak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="b7267-107">There are existing audiences in Mailchimp and the corresponding IDs.</span></span> <span data-ttu-id="b7267-108">Informazio gehiagorako, ikus [Mailchimp-eko hartzaileak](https://mailchimp.com/help/create-audience/).</span><span class="sxs-lookup"><span data-stu-id="b7267-108">For more information, see [Mailchimp audiences](https://mailchimp.com/help/create-audience/).</span></span>
-   <span data-ttu-id="b7267-109">[Konfiguratutako segmentuak](segments.md) dituzu</span><span class="sxs-lookup"><span data-stu-id="b7267-109">You have [configured segments](segments.md)</span></span>
-   <span data-ttu-id="b7267-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="b7267-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="connect-to-mailchimp"></a><span data-ttu-id="b7267-111">Konektatu Mailchimp-era</span><span class="sxs-lookup"><span data-stu-id="b7267-111">Connect to Mailchimp</span></span>

1. <span data-ttu-id="b7267-112">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="b7267-112">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="b7267-113">**Mailchimp** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="b7267-113">Under **Mailchimp**, select **Set up**.</span></span>

1. <span data-ttu-id="b7267-114">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="b7267-114">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="b7267-115">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="b7267-115">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="b7267-116">Sartu zure **[Mailchimp hartzaileen IDa](https://mailchimp.com/help/find-audience-id/)** eta hautatu **Konektatu** Mailchimp-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="b7267-116">Enter your **[Mailchimp audience ID](https://mailchimp.com/help/find-audience-id/)** and select **Connect** to initialize the connection to Mailchimp.</span></span>

1. <span data-ttu-id="b7267-117">Aukeratu **Egiaztatu Mailchimp-ekin** eta eman zure Mailchimp kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="b7267-117">Select **Authenticate with Mailchimp** and provide your Mailchimp credentials.</span></span>

1. <span data-ttu-id="b7267-118">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="b7267-118">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

   :::image type="content" source="media/export-connect-mailchimp.png" alt-text="Esportatu pantaila-argazkia Mailchimp konexiorako":::

1. <span data-ttu-id="b7267-120">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="b7267-120">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="b7267-121">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="b7267-121">Configure the connector</span></span>

1. <span data-ttu-id="b7267-122">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="b7267-122">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> 

1. <span data-ttu-id="b7267-123">Aukeran, **izena** eta **abizena** esporta ditzakezu mezu pertsonalizatuagoak sortzeko eremu osagarri gisa.</span><span class="sxs-lookup"><span data-stu-id="b7267-123">Optionally, you can export **First name** and **Last name** as additional fields to create more personalized emails.</span></span> <span data-ttu-id="b7267-124">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="b7267-124">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="b7267-125">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="b7267-125">Select the segments you want to export.</span></span> <span data-ttu-id="b7267-126">Guztira 1 milioi bezero profil esporta ditzakezu Mailchimp-era.</span><span class="sxs-lookup"><span data-stu-id="b7267-126">You can export up to 1 million customer profiles in total to Mailchimp.</span></span>

   :::image type="content" source="media/export-segments-mailchimp.png" alt-text="Aukeratu eremuak eta segmentuak Mailchimp-era esportatzeko":::

1. <span data-ttu-id="b7267-128">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="b7267-128">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="b7267-129">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="b7267-129">Export the data</span></span>

<span data-ttu-id="b7267-130">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="b7267-130">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="b7267-131">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="b7267-131">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="b7267-132">Mailchimp-en, zure segmentuak azpian aurki ditzakezu hemen: [Mailchimp-eko hartzaileak](https://mailchimp.com/help/create-audience/).</span><span class="sxs-lookup"><span data-stu-id="b7267-132">In Mailchimp, you can now find your segments under [Mailchimp audiences](https://mailchimp.com/help/create-audience/).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="b7267-133">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="b7267-133">Known limitations</span></span>

- <span data-ttu-id="b7267-134">Gehienez milioi bat profil Mailchimp-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="b7267-134">Up to 1 million profiles per export to Mailchimp.</span></span>
- <span data-ttu-id="b7267-135">Mailchimp-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="b7267-135">Exporting to Mailchimp is limited to segments.</span></span>
- <span data-ttu-id="b7267-136">Guztira 1 milioi profil dituzten segmentuak esportatzeak hiru ordu arte iraun dezake hornitzailearen aldetik mugak direla eta.</span><span class="sxs-lookup"><span data-stu-id="b7267-136">Exporting segments with a total of 1 million profiles can take up to three hours due to limitations on the provider side.</span></span> 
- <span data-ttu-id="b7267-137">Mailchimp-era esporta ditzakezun profilen kopurua Mailchimp-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="b7267-137">The number of profiles that you can export to Mailchimp is dependent and limited on your contract with Mailchimp.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="b7267-138">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="b7267-138">Data privacy and compliance</span></span>

<span data-ttu-id="b7267-139">Dynamics 365 Customer Insights gaitzen duzunean datuak Mailchimp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="b7267-139">When you enable Dynamics 365 Customer Insights to transmit data to Mailchimp, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="b7267-140">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Mailchimp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="b7267-140">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Mailchimp meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="b7267-141">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="b7267-141">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="b7267-142">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="b7267-142">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]