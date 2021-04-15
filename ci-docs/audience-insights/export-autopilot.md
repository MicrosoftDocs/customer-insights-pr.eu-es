---
title: Esportatu Customer Insights datuak Autopilot-era
description: Ikasi Autopilot-erako konexioa nola konfiguratu.
ms.date: 12/08/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 6d039c4afd84eaad942d214d4e6fb8ef7b1ec72a
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596108"
---
# <a name="connector-for-autopilot-preview"></a><span data-ttu-id="0f92e-103">Autopilot-eko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="0f92e-103">Connector for Autopilot (preview)</span></span>

<span data-ttu-id="0f92e-104">Esportatu bezeroen profil bateratuen segmentuak Autopilot kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko Autopilot-en.</span><span class="sxs-lookup"><span data-stu-id="0f92e-104">Export segments of unified customer profiles to Autopilot and use them for email marketing in Autopilot.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="0f92e-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="0f92e-105">Prerequisites</span></span>

-   <span data-ttu-id="0f92e-106">Baduzu [Autopilot kontua](https://www.autopilothq.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="0f92e-106">You have an [Autopilot account](https://www.autopilothq.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="0f92e-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="0f92e-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="0f92e-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="0f92e-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="connect-to-autopilot"></a><span data-ttu-id="0f92e-109">Konektatu Autopilot-era</span><span class="sxs-lookup"><span data-stu-id="0f92e-109">Connect to Autopilot</span></span>

1. <span data-ttu-id="0f92e-110">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="0f92e-110">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="0f92e-111">**Autopilot** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="0f92e-111">Under **Autopilot**, select **Set up**.</span></span>

1. <span data-ttu-id="0f92e-112">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="0f92e-112">Give your export destination a recognizable name in the **Display name** field.</span></span>

   :::image type="content" source="media/export-autopilot.PNG" alt-text="Autopilot konexioaren konfigurazio panela.":::

1. <span data-ttu-id="0f92e-114">Sartu zure **Autopilot API gakoa** [Autopilot API gakoa](https://autopilot.docs.apiary.io/#).</span><span class="sxs-lookup"><span data-stu-id="0f92e-114">Enter your **Autopilot API key** [Autopilot API key](https://autopilot.docs.apiary.io/#).</span></span>

1. <span data-ttu-id="0f92e-115">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="0f92e-115">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="0f92e-116">Aukeratu **Konektatu** Autopilot-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="0f92e-116">Select **Connect** to initialize the connection to Autopilot.</span></span>

1. <span data-ttu-id="0f92e-117">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="0f92e-117">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="0f92e-118">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="0f92e-118">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="0f92e-119">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="0f92e-119">Configure the connector</span></span>

1. <span data-ttu-id="0f92e-120">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="0f92e-120">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="0f92e-121">Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena** eta **abizena**.</span><span class="sxs-lookup"><span data-stu-id="0f92e-121">Repeat the same steps for other optional fields such as **First name**, **Last name**.</span></span>

1. <span data-ttu-id="0f92e-122">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="0f92e-122">Select the segments you want to export.</span></span> <span data-ttu-id="0f92e-123">Biziki **gomendatzen dugu 100.000 bezero profil baino gehiago ez esportatzea guztira** Autopilot-era.</span><span class="sxs-lookup"><span data-stu-id="0f92e-123">We strongly **recommend to not export more than 100'000 customer profiles in total** to Autopilot.</span></span> 

1. <span data-ttu-id="0f92e-124">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="0f92e-124">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="0f92e-125">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="0f92e-125">Export the data</span></span>

<span data-ttu-id="0f92e-126">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="0f92e-126">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="0f92e-127">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="0f92e-127">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="0f92e-128">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="0f92e-128">Known limitations</span></span>

- <span data-ttu-id="0f92e-129">Guztira 100.000 bezero-profil esporta ditzakezu Autopilot-era.</span><span class="sxs-lookup"><span data-stu-id="0f92e-129">You can export up to 100'000 profiles in total to Autopilot.</span></span>
- <span data-ttu-id="0f92e-130">Autopilot-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="0f92e-130">Exporting to Autopilot is limited to segments.</span></span>
- <span data-ttu-id="0f92e-131">Autopilot-era 100.000 profil gehienera esportatzeak ordu batzuk behar izan ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="0f92e-131">Exporting up to 100'000 profiles to Autopilot can take up to a few hours to complete.</span></span> 
- <span data-ttu-id="0f92e-132">Autopilot-era esporta ditzakezun profilen kopurua Autopilot-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="0f92e-132">The number of profiles that you can export to Autopilot is dependent and limited on your contract with Autopilot.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="0f92e-133">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="0f92e-133">Data privacy and compliance</span></span>

<span data-ttu-id="0f92e-134">Dynamics 365 Customer Insights gaitzen duzunean datuak Autopilot-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="0f92e-134">When you enable Dynamics 365 Customer Insights to transmit data to Autopilot, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="0f92e-135">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Autopilot-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="0f92e-135">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Autopilot meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="0f92e-136">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="0f92e-136">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="0f92e-137">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="0f92e-137">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]