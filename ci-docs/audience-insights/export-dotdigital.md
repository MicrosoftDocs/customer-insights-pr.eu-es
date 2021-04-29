---
title: Esportatu Customer Insights datuak DotDigital-era
description: Ikasi konexioa nola konfiguratu eta DotDigital-era esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 235bcdfa4a7c4c1a382778bd4f66c1a9f5b7beb1
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5759944"
---
# <a name="export-segment-lists-to-dotdigital-preview"></a><span data-ttu-id="29895-103">Esportatu segmentuen zerrendak DotDigital (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="29895-103">Export segment lists to DotDigital (preview)</span></span>

<span data-ttu-id="29895-104">Esportatu bezeroen profil bateratuen segmentuak DotDigital helbide liburuetara eta erabili kanpainetarako, posta elektroniko bidezko marketinerako eta DotDigital-ekin bezero segmentuak eraikitzeko.</span><span class="sxs-lookup"><span data-stu-id="29895-104">Export segments of unified customer profiles to DotDigital address books and use them for campaigns, email marketing, and to build customer segments with DotDigital.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="29895-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="29895-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="29895-106">Baduzu [DotDigital kontua](https://dotdigital.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="29895-106">You have a [DotDigital account](https://dotdigital.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="29895-107">DotDigital-en helbide-liburuak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="29895-107">There are existing address books in DotDigital and the corresponding IDs.</span></span> <span data-ttu-id="29895-108">IDa URLan aurki daiteke helbide-liburua hautatu eta irekitzean.</span><span class="sxs-lookup"><span data-stu-id="29895-108">The ID can be found in the URL when you select and open an address book.</span></span> <span data-ttu-id="29895-109">Informazio gehiagorako, ikus [DotDigital helbide-liburuak](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span><span class="sxs-lookup"><span data-stu-id="29895-109">For more information, see [DotDigital address books](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span></span>
-   <span data-ttu-id="29895-110">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="29895-110">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="29895-111">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="29895-111">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="29895-112">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="29895-112">Known limitations</span></span>

- <span data-ttu-id="29895-113">Gehienez milioi bat profil DotDigital-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="29895-113">Up to 1 million profiles per export to DotDigital.</span></span>
- <span data-ttu-id="29895-114">DotDigital-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="29895-114">Exporting to DotDigital is limited to segments.</span></span>
- <span data-ttu-id="29895-115">Guztira 1 milioi profil dituzten segmentuak esportatzeak 3 ordu arte iraun dezake hornitzailearen aldetik mugak direla eta.</span><span class="sxs-lookup"><span data-stu-id="29895-115">Exporting segments with a total of 1 million profiles can take up to 3 hours because of limitations on the provider side.</span></span> 
- <span data-ttu-id="29895-116">DotDigital-era esporta ditzakezun profilen kopurua DotDigital-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="29895-116">The number of profiles that you can export to DotDigital is dependent and limited on your contract with DotDigital.</span></span>

## <a name="set-up-connection-to-dotdigital"></a><span data-ttu-id="29895-117">Konfiguratu konexioa DotDigital-era</span><span class="sxs-lookup"><span data-stu-id="29895-117">Set up connection to DotDigital</span></span>

1. <span data-ttu-id="29895-118">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="29895-118">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="29895-119">Hautatu **Gehitu konexioa** eta aukeratu **DotDigital** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="29895-119">Select **Add connection** and choose **DotDigital** to configure the connection.</span></span>

1. <span data-ttu-id="29895-120">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="29895-120">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="29895-121">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="29895-121">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="29895-122">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="29895-122">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="29895-123">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="29895-123">Choose who can use this connection.</span></span> <span data-ttu-id="29895-124">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="29895-124">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="29895-125">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="29895-125">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="29895-126">Idatzi **DotDigital-eko erabiltzaile-izena eta pasahitza**.</span><span class="sxs-lookup"><span data-stu-id="29895-126">Enter your **DotDigital username and password**.</span></span>

1. <span data-ttu-id="29895-127">Sartu zure **[DotDigital helbide liburuaren IDa](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book)**.</span><span class="sxs-lookup"><span data-stu-id="29895-127">Enter your **[DotDigital address book ID](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book)**.</span></span>

1. <span data-ttu-id="29895-128">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="29895-128">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="29895-129">Aukeratu **Konektatu** DotDigital-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="29895-129">Select **Connect** to initialize the connection to DotDigital.</span></span>

1. <span data-ttu-id="29895-130">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="29895-130">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="29895-131">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="29895-131">Select **Save** to complete the connection.</span></span> 

## <a name="configure-an-export"></a><span data-ttu-id="29895-132">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="29895-132">Configure an export</span></span>

<span data-ttu-id="29895-133">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="29895-133">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="29895-134">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="29895-134">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="29895-135">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="29895-135">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="29895-136">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="29895-136">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="29895-137">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa DotDigital sekzioan.</span><span class="sxs-lookup"><span data-stu-id="29895-137">In the **Connection for export** field, choose a connection from the DotDigital section.</span></span> <span data-ttu-id="29895-138">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="29895-138">If you don't see this section name, there are no connections of this type available to you.</span></span>


1. <span data-ttu-id="29895-139">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="29895-139">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="29895-140">Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **Izen osoa**, **Generoa**, eta **Posta kodea**.</span><span class="sxs-lookup"><span data-stu-id="29895-140">Repeat the same steps for other optional fields such as **First name**, **Last name**, **Full name**, **Gender**, and **Post code**.</span></span>

1. <span data-ttu-id="29895-141">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="29895-141">Select the segments you want to export.</span></span> <span data-ttu-id="29895-142">Guztira 1 milioi bezero profil esporta ditzakezu DotDigital-era.</span><span class="sxs-lookup"><span data-stu-id="29895-142">You can export up to 1 million customer profiles in total to DotDigital.</span></span>

1. <span data-ttu-id="29895-143">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="29895-143">Select **Save**.</span></span>

<span data-ttu-id="29895-144">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="29895-144">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="29895-145">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="29895-145">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="29895-146">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="29895-146">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 
 
<span data-ttu-id="29895-147">DotDigital-en, zure segmentuak hemen aurki ditzakezu: [DotDigital-eko helbide liburuak](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span><span class="sxs-lookup"><span data-stu-id="29895-147">In DotDigital, you can now find your segments in [DotDigital address books](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span></span>


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="29895-148">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="29895-148">Data privacy and compliance</span></span>

<span data-ttu-id="29895-149">Dynamics 365 Customer Insights gaitzen duzunean datuak DotDigital-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="29895-149">When you enable Dynamics 365 Customer Insights to transmit data to DotDigital, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="29895-150">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da DotDigital-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="29895-150">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that DotDigital meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="29895-151">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="29895-151">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="29895-152">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="29895-152">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
