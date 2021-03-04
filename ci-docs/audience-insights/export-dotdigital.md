---
title: Esportatu Customer Insights datuak DotDigital-era
description: Ikasi DotDigital-erako konexioa nola konfiguratu.
ms.date: 11/14/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 573a22e24f84c65fc4d21faf823cace801cc7ea3
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269085"
---
# <a name="connector-for-dotdigital-preview"></a><span data-ttu-id="4d149-103">DotDigital-eko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="4d149-103">Connector for DotDigital (preview)</span></span>

<span data-ttu-id="4d149-104">Esportatu bezeroen profil bateratuen segmentuak DotDigital helbide liburuetara eta erabili kanpainetarako, posta elektroniko bidezko marketinerako eta DotDigital-ekin bezero segmentuak eraikitzeko.</span><span class="sxs-lookup"><span data-stu-id="4d149-104">Export segments of unified customer profiles to DotDigital address books and use them for campaigns, email marketing, and to build customer segments with DotDigital.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="4d149-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="4d149-105">Prerequisites</span></span>

-   <span data-ttu-id="4d149-106">Baduzu [DotDigital kontua](https://dotdigital.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="4d149-106">You have a [DotDigital account](https://dotdigital.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="4d149-107">DotDigital-en helbide-liburuak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="4d149-107">There are existing address books in DotDigital and the corresponding IDs.</span></span> <span data-ttu-id="4d149-108">IDa URLan aurki daiteke helbide-liburua hautatu eta irekitzean.</span><span class="sxs-lookup"><span data-stu-id="4d149-108">The ID can be found in the URL when you select and open an address book.</span></span> <span data-ttu-id="4d149-109">Informazio gehiagorako, ikus [DotDigital helbide-liburuak](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span><span class="sxs-lookup"><span data-stu-id="4d149-109">For more information, see [DotDigital address books](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span></span>
-   <span data-ttu-id="4d149-110">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="4d149-110">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="4d149-111">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="4d149-111">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="connect-to-dotdigital"></a><span data-ttu-id="4d149-112">Konektatu DotDigital-era</span><span class="sxs-lookup"><span data-stu-id="4d149-112">Connect to DotDigital</span></span>

1. <span data-ttu-id="4d149-113">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="4d149-113">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="4d149-114">**DotDigital** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="4d149-114">Under **DotDigital**, select **Set up**.</span></span>

1. <span data-ttu-id="4d149-115">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="4d149-115">Give your export destination a recognizable name in the **Display name** field.</span></span>

   :::image type="content" source="media/DotDigital_config.PNG" alt-text="DotDigital esportaziorako konfigurazio panela.":::

1. <span data-ttu-id="4d149-117">Idatzi **DotDigital-eko erabiltzaile-izena eta pasahitza**.</span><span class="sxs-lookup"><span data-stu-id="4d149-117">Enter your **DotDigital username and password**.</span></span>

1. <span data-ttu-id="4d149-118">Sartu zure **[DotDigital helbide liburuaren IDa](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book)**.</span><span class="sxs-lookup"><span data-stu-id="4d149-118">Enter your **[DotDigital address book ID](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book)**.</span></span>

1. <span data-ttu-id="4d149-119">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="4d149-119">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="4d149-120">Aukeratu **Konektatu** DotDigital-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="4d149-120">Select **Connect** to initialize the connection to DotDigital.</span></span>

1. <span data-ttu-id="4d149-121">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="4d149-121">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="4d149-122">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="4d149-122">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="4d149-123">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="4d149-123">Configure the connector</span></span>

1. <span data-ttu-id="4d149-124">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="4d149-124">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="4d149-125">Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **Izen osoa**, **Generoa**, eta **Posta kodea**.</span><span class="sxs-lookup"><span data-stu-id="4d149-125">Repeat the same steps for other optional fields such as **First name**, **Last name**, **Full name**, **Gender**, and **Post code**.</span></span>

1. <span data-ttu-id="4d149-126">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="4d149-126">Select the segments you want to export.</span></span> <span data-ttu-id="4d149-127">Guztira 1 milioi bezero profil esporta ditzakezu DotDigital-era.</span><span class="sxs-lookup"><span data-stu-id="4d149-127">You can export up to 1 million customer profiles in total to DotDigital.</span></span>

1. <span data-ttu-id="4d149-128">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="4d149-128">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="4d149-129">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="4d149-129">Export the data</span></span>

<span data-ttu-id="4d149-130">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="4d149-130">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="4d149-131">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="4d149-131">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="4d149-132">DotDigital-en, zure segmentuak hemen aurki ditzakezu: [DotDigital-eko helbide liburuak](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span><span class="sxs-lookup"><span data-stu-id="4d149-132">In DotDigital, you can now find your segments in [DotDigital address books](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="4d149-133">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="4d149-133">Known limitations</span></span>

- <span data-ttu-id="4d149-134">Gehienez milioi bat profil DotDigital-era esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="4d149-134">Up to 1 million profiles per export to DotDigital.</span></span>
- <span data-ttu-id="4d149-135">DotDigital-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="4d149-135">Exporting to DotDigital is limited to segments.</span></span>
- <span data-ttu-id="4d149-136">Guztira 1 milioi profil dituzten segmentuak esportatzeak 3 ordu arte iraun dezake hornitzailearen aldetik mugak direla eta.</span><span class="sxs-lookup"><span data-stu-id="4d149-136">Exporting segments with a total of 1 million profiles can take up to 3 hours because of limitations on the provider side.</span></span> 
- <span data-ttu-id="4d149-137">DotDigital-era esporta ditzakezun profilen kopurua DotDigital-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="4d149-137">The number of profiles that you can export to DotDigital is dependent and limited on your contract with DotDigital.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="4d149-138">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="4d149-138">Data privacy and compliance</span></span>

<span data-ttu-id="4d149-139">Dynamics 365 Customer Insights gaitzen duzunean datuak DotDigital-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="4d149-139">When you enable Dynamics 365 Customer Insights to transmit data to DotDigital, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="4d149-140">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da DotDigital-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="4d149-140">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that DotDigital meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="4d149-141">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="4d149-141">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="4d149-142">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="4d149-142">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]