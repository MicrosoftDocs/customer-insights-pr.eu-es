---
title: Esportatu Customer Insights datuak Google Ads-era
description: Ikasi Google Ads-erako konexioa nola konfiguratu.
ms.date: 11/18/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 06aa0b6ff3125d8735adc8c8f9f6dad69087d9f8
ms.sourcegitcommit: ff824bbbd31fd666ab0da682bf48ea31580d242c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "4568397"
---
# <a name="connector-for-google-ads-preview"></a><span data-ttu-id="ee51b-103">Google Ads-eko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="ee51b-103">Connector for Google Ads (preview)</span></span>

<span data-ttu-id="ee51b-104">Esportatu bezeroen profil bateratuetako segmentuak Google Ads-eko hartzaile-zerrendetara eta erabili zerrenda horiek Google Bilaketa-n, Gmail-en, YouTube-n eta Google Display Network-en iragartzeko.</span><span class="sxs-lookup"><span data-stu-id="ee51b-104">Export segments of unified customer profiles to Google Ads audience list and use them to advertise on Google Search, Gmail, YouTube, and Google Display Network.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ee51b-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="ee51b-105">Prerequisites</span></span>

-   <span data-ttu-id="ee51b-106">Baduzu [Google Ads kontua](https://ads.google.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="ee51b-106">You have a [Google Ads account](https://ads.google.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="ee51b-107">Google Ads-en hartzaileak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="ee51b-107">There are existing audiences in Google Ads and the corresponding IDs.</span></span> <span data-ttu-id="ee51b-108">Informazio gehiagorako, ikus [Google Ads-eko hartzaileak](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.).</span><span class="sxs-lookup"><span data-stu-id="ee51b-108">For more information, see [Google Ads audiences](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.).</span></span>
-   <span data-ttu-id="ee51b-109">[Konfiguratutako segmentuak](segments.md) dituzu</span><span class="sxs-lookup"><span data-stu-id="ee51b-109">You have [configured segments](segments.md)</span></span>
-   <span data-ttu-id="ee51b-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa, izena eta abizena adierazten duen eremuak dituzte</span><span class="sxs-lookup"><span data-stu-id="ee51b-110">Unified customer profiles in the exported segments contain fields representing an email address, first name, and last name</span></span>

## <a name="connect-to-google-ads"></a><span data-ttu-id="ee51b-111">Konektatu Google Ads-era</span><span class="sxs-lookup"><span data-stu-id="ee51b-111">Connect to Google Ads</span></span>

1. <span data-ttu-id="ee51b-112">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="ee51b-112">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="ee51b-113">**Google Ads** atalean, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="ee51b-113">Under **Google Ads**, select **Set up**.</span></span>

1. <span data-ttu-id="ee51b-114">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="ee51b-114">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="ee51b-115">Idatzi **[Google Ads bezeroaren IDa](https://support.google.com/google-ads/answer/1704344)**.</span><span class="sxs-lookup"><span data-stu-id="ee51b-115">Enter your **[Google Ads customer ID](https://support.google.com/google-ads/answer/1704344)**.</span></span>

1. <span data-ttu-id="ee51b-116">Sartu **[Google Ads-ek onartutako garatzaile token-a](https://developers.google.com/google-ads/api/docs/first-call/dev-token)**.</span><span class="sxs-lookup"><span data-stu-id="ee51b-116">Enter your **[Google Ads approved developer token](https://developers.google.com/google-ads/api/docs/first-call/dev-token)**.</span></span>

1. <span data-ttu-id="ee51b-117">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="ee51b-117">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="ee51b-118">Sartu zure **[Google Ads hartzaileen IDa](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.)** eta hautatu **Konektatu** Google Ads-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="ee51b-118">Enter your **[Google Ads audience ID](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.)** and select **Connect** to initialize the connection to Google Ads.</span></span>

1. <span data-ttu-id="ee51b-119">Aukeratu **Egiaztatu Google Ads-ekin** eta eman zure Google Ads kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="ee51b-119">Select **Authenticate with Google Ads** and provide your Google Ads credentials.</span></span>

1. <span data-ttu-id="ee51b-120">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="ee51b-120">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

   :::image type="content" source="media/export-segments-googleads.PNG" alt-text="Esportatu pantaila-argazkia Google Ads konexiorako":::

1. <span data-ttu-id="ee51b-122">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="ee51b-122">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="ee51b-123">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="ee51b-123">Configure the connector</span></span>

1. <span data-ttu-id="ee51b-124">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="ee51b-124">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="ee51b-125">Errepikatu urratsak **Izena** eta **abizena** eremuetan.</span><span class="sxs-lookup"><span data-stu-id="ee51b-125">Repeat the same steps for \*\*First name" and **Last name** fields.</span></span>

1. <span data-ttu-id="ee51b-126">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="ee51b-126">Select the segments you want to export.</span></span> <span data-ttu-id="ee51b-127">Guztira 1 milioi bezero profil esporta ditzakezu Google Ads-era.</span><span class="sxs-lookup"><span data-stu-id="ee51b-127">You can export up to 1 million customer profiles in total to Google Ads.</span></span>

1. <span data-ttu-id="ee51b-128">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="ee51b-128">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="ee51b-129">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="ee51b-129">Export the data</span></span>

<span data-ttu-id="ee51b-130">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="ee51b-130">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="ee51b-131">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="ee51b-131">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="ee51b-132">Google Ads-en, zure segmentuak azpian aurki ditzakezu hemen: [Google Ads-eko hartzaileak](https://support.google.com/google-ads/answer/7558048?hl=en/).</span><span class="sxs-lookup"><span data-stu-id="ee51b-132">In Google Ads, you can now find your segments under [Google Ads audiences](https://support.google.com/google-ads/answer/7558048?hl=en/).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="ee51b-133">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="ee51b-133">Known limitations</span></span>

- <span data-ttu-id="ee51b-134">Gehienez milioi bat profil Google Ads-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="ee51b-134">Up to 1 million profiles per export to Google Ads.</span></span>
- <span data-ttu-id="ee51b-135">Google Ads-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="ee51b-135">Exporting to Google Ads is limited to segments.</span></span>
- <span data-ttu-id="ee51b-136">Guztira 1 milioi profil dituzten segmentuak esportatzeak 5 minutu arte iraun dezake hornitzailearen aldetik mugak direla eta.</span><span class="sxs-lookup"><span data-stu-id="ee51b-136">Exporting segments with a total of 1 million profiles can take up to 5 minutes because of limitations on the provider side.</span></span> 
- <span data-ttu-id="ee51b-137">Google Ads zerbitzuan bat etortzeak 48 ordu iraun dezake.</span><span class="sxs-lookup"><span data-stu-id="ee51b-137">The matching in Google Ads can take up to 48 hours.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="ee51b-138">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="ee51b-138">Data privacy and compliance</span></span>

<span data-ttu-id="ee51b-139">Dynamics 365 Customer Insights gaitzen duzunean datuak Google Ads-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="ee51b-139">When you enable Dynamics 365 Customer Insights to transmit data to Google Ads, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="ee51b-140">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Google Ads-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="ee51b-140">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Google Ads meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="ee51b-141">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="ee51b-141">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="ee51b-142">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="ee51b-142">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
