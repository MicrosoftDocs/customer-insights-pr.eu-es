---
title: Esportatu Customer Insights datuak Google Ads-era
description: Ikasi konexioa konfiguratzen eta Google Ads-era esportatzen.
ms.date: 03/03/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 73f3257a3ae6e8423f45410546535df5e3b400ce
ms.sourcegitcommit: e8e03309ba2515374a70c132d0758f3e1e1851d0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5976303"
---
# <a name="export-segments-to-google-ads-preview"></a><span data-ttu-id="5b3f7-103">Esportatu segmentuak Google Ads-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="5b3f7-103">Export segments to Google Ads (preview)</span></span>

<span data-ttu-id="5b3f7-104">Esportatu bezeroen profil bateratuetako segmentuak Google Ads-eko hartzaile-zerrendetara eta erabili zerrenda horiek Google Bilaketa-n, Gmail-en, YouTube-n eta Google Display Network-en iragartzeko.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-104">Export segments of unified customer profiles to Google Ads audience list and use them to advertise on Google Search, Gmail, YouTube, and Google Display Network.</span></span> 

## <a name="prerequisites-for-connection"></a><span data-ttu-id="5b3f7-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="5b3f7-105">Prerequisites for connection</span></span>

-   <span data-ttu-id="5b3f7-106">Baduzu [Google Ads kontua](https://ads.google.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-106">You have a [Google Ads account](https://ads.google.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="5b3f7-107">Baduzu [Google Ads garatzaileen token homologatua](https://developers.google.com/google-ads/api/docs/first-call/dev-token)</span><span class="sxs-lookup"><span data-stu-id="5b3f7-107">You have an [approved Google Ads Developer token](https://developers.google.com/google-ads/api/docs/first-call/dev-token)</span></span> 
-   <span data-ttu-id="5b3f7-108">Webgunearen baldintzak betetzen dituzu [Bezeroen arteko lotura politika](https://support.google.com/adspolicy/answer/6299717)</span><span class="sxs-lookup"><span data-stu-id="5b3f7-108">You fulfill the requirements of the [Customer Match Policy](https://support.google.com/adspolicy/answer/6299717)</span></span>
-   <span data-ttu-id="5b3f7-109">Webgunearen baldintzak betetzen dituzu [berriro merkaturatzeko zerrenden tamainak](https://support.google.com/google-ads/answer/7558048)</span><span class="sxs-lookup"><span data-stu-id="5b3f7-109">You fulfill the requirements of the [remarketing list sizes](https://support.google.com/google-ads/answer/7558048)</span></span> 

-   <span data-ttu-id="5b3f7-110">Google Ads-en hartzaileak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-110">There are existing audiences in Google Ads and the corresponding IDs.</span></span> <span data-ttu-id="5b3f7-111">Informazio gehiagorako, ikus [Google Ads-eko hartzaileak](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.).</span><span class="sxs-lookup"><span data-stu-id="5b3f7-111">For more information, see [Google Ads audiences](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.).</span></span>
-   <span data-ttu-id="5b3f7-112">[Konfiguratutako segmentuak](segments.md) dituzu</span><span class="sxs-lookup"><span data-stu-id="5b3f7-112">You have [configured segments](segments.md)</span></span>
-   <span data-ttu-id="5b3f7-113">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa, izena eta abizena adierazten duen eremuak dituzte</span><span class="sxs-lookup"><span data-stu-id="5b3f7-113">Unified customer profiles in the exported segments contain fields representing an email address, first name, and last name</span></span>

## <a name="known-limitations"></a><span data-ttu-id="5b3f7-114">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="5b3f7-114">Known limitations</span></span>

- <span data-ttu-id="5b3f7-115">Gehienez milioi bat profil Google Ads-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-115">Up to 1 million profiles per export to Google Ads.</span></span>
- <span data-ttu-id="5b3f7-116">Google Ads-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-116">Exporting to Google Ads is limited to segments.</span></span>
- <span data-ttu-id="5b3f7-117">Guztira 1 milioi profil dituzten segmentuak esportatzeak 5 minutu arte iraun dezake hornitzailearen aldetik mugak direla eta.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-117">Exporting segments with a total of 1 million profiles can take up to 5 minutes because of limitations on the provider side.</span></span> 
- <span data-ttu-id="5b3f7-118">Google Ads zerbitzuan bat etortzeak 48 ordu iraun dezake.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-118">The matching in Google Ads can take up to 48 hours.</span></span>

## <a name="set-up-connection-to-google-ads"></a><span data-ttu-id="5b3f7-119">Konfiguratu konexioa Google Ads-era</span><span class="sxs-lookup"><span data-stu-id="5b3f7-119">Set up connection to Google Ads</span></span>

1. <span data-ttu-id="5b3f7-120">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-120">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="5b3f7-121">Hautatu **Gehitu konexioa** eta aukeratu **Google Ads** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-121">Select **Add connection** and choose **Google Ads** to configure the connection.</span></span>

1. <span data-ttu-id="5b3f7-122">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-122">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="5b3f7-123">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-123">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="5b3f7-124">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-124">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="5b3f7-125">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-125">Choose who can use this connection.</span></span> <span data-ttu-id="5b3f7-126">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-126">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="5b3f7-127">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="5b3f7-127">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="5b3f7-128">Idatzi **[Google Ads bezeroaren IDa](https://support.google.com/google-ads/answer/1704344)**.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-128">Enter your **[Google Ads customer ID](https://support.google.com/google-ads/answer/1704344)**.</span></span>

1. <span data-ttu-id="5b3f7-129">Sartu **[Google Ads-ek onartutako garatzaile token-a](https://developers.google.com/google-ads/api/docs/first-call/dev-token)**.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-129">Enter your **[Google Ads approved developer token](https://developers.google.com/google-ads/api/docs/first-call/dev-token)**.</span></span>

1. <span data-ttu-id="5b3f7-130">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-130">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="5b3f7-131">Aukeratu **Egiaztatu Google Ads-ekin** eta eman zure Google Ads kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-131">Select **Authenticate with Google Ads** and provide your Google Ads credentials.</span></span>

1. <span data-ttu-id="5b3f7-132">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-132">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="5b3f7-133">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-133">Select **Save** to complete the connection.</span></span> 

## <a name="configure-an-export"></a><span data-ttu-id="5b3f7-134">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="5b3f7-134">Configure an export</span></span>

<span data-ttu-id="5b3f7-135">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-135">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="5b3f7-136">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="5b3f7-136">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="5b3f7-137">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-137">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="5b3f7-138">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-138">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="5b3f7-139">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Google Ads sekzioan.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-139">In the **Connection for export** field, choose a connection from the Google Ads section.</span></span> <span data-ttu-id="5b3f7-140">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-140">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="5b3f7-141">Sartu zure **[Google Ads hartzaileen IDa](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.)** eta hautatu **Konektatu** Google Ads-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-141">Enter your **[Google Ads audience ID](https://support.google.com/google-ads/answer/7558048?hl=en#:~:text=Audience%20lists%20is%20a%20section,Display%20Network%20through%20remarketing%20campaigns.)** and select **Connect** to initialize the connection to Google Ads.</span></span>

1. <span data-ttu-id="5b3f7-142">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-142">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="5b3f7-143">Errepikatu urratsak **Izena** eta **abizena** eremuetan.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-143">Repeat the same steps for \*\*First name" and **Last name** fields.</span></span>

1. <span data-ttu-id="5b3f7-144">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-144">Select the segments you want to export.</span></span> <span data-ttu-id="5b3f7-145">Guztira 1 milioi bezero profil esporta ditzakezu Google Ads-era.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-145">You can export up to 1 million customer profiles in total to Google Ads.</span></span>

<span data-ttu-id="5b3f7-146">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-146">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="5b3f7-147">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="5b3f7-147">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="5b3f7-148">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="5b3f7-148">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="5b3f7-149">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="5b3f7-149">Data privacy and compliance</span></span>

<span data-ttu-id="5b3f7-150">Dynamics 365 Customer Insights gaitzen duzunean datuak Google Ads-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-150">When you enable Dynamics 365 Customer Insights to transmit data to Google Ads, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="5b3f7-151">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Google Ads-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-151">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Google Ads meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="5b3f7-152">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="5b3f7-152">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="5b3f7-153">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="5b3f7-153">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
