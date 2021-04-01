---
title: Esportatu Customer Insights datuak SendGrid-era
description: Ikasi SendGrid-erako konexioa nola konfiguratu.
ms.date: 12/08/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 1a1f679fa42d47d524ebfdd6e931ae2822565f77
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597266"
---
# <a name="connector-for-sendgrid-preview"></a><span data-ttu-id="b4437-103">SendGrid-eko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="b4437-103">Connector for SendGrid (preview)</span></span>

<span data-ttu-id="b4437-104">Esportatu bezeroen profil bateratuen segmentuak SendGrid kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko SendGrid-en.</span><span class="sxs-lookup"><span data-stu-id="b4437-104">Export segments of unified customer profiles to SendGrid contact lists and use them for campaigns and email marketing in SendGrid.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="b4437-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="b4437-105">Prerequisites</span></span>

-   <span data-ttu-id="b4437-106">Baduzu [SendGrid kontua](https://sendgrid.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="b4437-106">You have a [SendGrid account](https://sendgrid.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="b4437-107">SendGrid-en kontaktu-zerrendak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="b4437-107">There are existing contact lists in SendGrid and the corresponding IDs.</span></span> <span data-ttu-id="b4437-108">Informazio gehiagorako, ikus [SendGrid: kudeatu kontaktuak](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts).</span><span class="sxs-lookup"><span data-stu-id="b4437-108">For more information, see [SendGrid - Manage contacts](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts).</span></span>
-   <span data-ttu-id="b4437-109">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="b4437-109">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="b4437-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="b4437-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="connect-to-sendgrid"></a><span data-ttu-id="b4437-111">Konektatu SendGrid-era</span><span class="sxs-lookup"><span data-stu-id="b4437-111">Connect to SendGrid</span></span>

1. <span data-ttu-id="b4437-112">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="b4437-112">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="b4437-113">**SendGrid** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="b4437-113">Under **SendGrid**, select **Set up**.</span></span>

1. <span data-ttu-id="b4437-114">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="b4437-114">Give your export destination a recognizable name in the **Display name** field.</span></span>

   :::image type="content" source="media/export-sendgrid.PNG" alt-text="SendGrid esportazio konfigurazio panela.":::

1. <span data-ttu-id="b4437-116">Sartu zure **SendGrid API gakoa** [SendGrid API gakoa](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).</span><span class="sxs-lookup"><span data-stu-id="b4437-116">Enter your **SendGrid API key** [SendGrid API key](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).</span></span>

1. <span data-ttu-id="b4437-117">Sartu zure **[SendGrid zerrendaren IDa](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts)**.</span><span class="sxs-lookup"><span data-stu-id="b4437-117">Enter your **[SendGrid list ID](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts)**.</span></span>

1. <span data-ttu-id="b4437-118">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="b4437-118">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="b4437-119">Aukeratu **Konektatu** SendGrid-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="b4437-119">Select **Connect** to initialize the connection to SendGrid.</span></span>

1. <span data-ttu-id="b4437-120">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="b4437-120">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="b4437-121">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="b4437-121">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="b4437-122">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="b4437-122">Configure the connector</span></span>

1. <span data-ttu-id="b4437-123">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="b4437-123">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="b4437-124">Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **herrialdea/eskualdea**, **estatua**, **hiria** eta **posta kodea**.</span><span class="sxs-lookup"><span data-stu-id="b4437-124">Repeat the same steps for other optional fields such as **First name**, **Last name**, **Country/Region**, **State**, **City**, and **Post code**.</span></span>

1. <span data-ttu-id="b4437-125">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="b4437-125">Select the segments you want to export.</span></span> <span data-ttu-id="b4437-126">Biziki **gomendatzen dugu 100.000 bezero profil baino gehiago ez esportatzea guztira** SendGrid-era.</span><span class="sxs-lookup"><span data-stu-id="b4437-126">We strongly **recommend to not export more than 100'000 customer profiles in total** to SendGrid.</span></span> 

1. <span data-ttu-id="b4437-127">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="b4437-127">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="b4437-128">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="b4437-128">Export the data</span></span>

<span data-ttu-id="b4437-129">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="b4437-129">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="b4437-130">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="b4437-130">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="b4437-131">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="b4437-131">Known limitations</span></span>

- <span data-ttu-id="b4437-132">Gehienez 100.000 profil guztira SendGrid-era.</span><span class="sxs-lookup"><span data-stu-id="b4437-132">Up to 100'000 profiles in total to SendGrid.</span></span>
- <span data-ttu-id="b4437-133">SendGrid-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="b4437-133">Exporting to SendGrid is limited to segments.</span></span>
- <span data-ttu-id="b4437-134">SendGrid-era 100.000 profil gehienera esportatzeak ordu batzuk behar izan ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="b4437-134">Exporting up to 100'000 profiles to SendGrid can take up to a few hours to complete.</span></span> 
- <span data-ttu-id="b4437-135">SendGrid-era esporta ditzakezun profilen kopurua SendGrid-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="b4437-135">The number of profiles that you can export to SendGrid is dependent and limited on your contract with SendGrid.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="b4437-136">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="b4437-136">Data privacy and compliance</span></span>

<span data-ttu-id="b4437-137">Dynamics 365 Customer Insights gaitzen duzunean datuak SendGrid-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="b4437-137">When you enable Dynamics 365 Customer Insights to transmit data to SendGrid, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="b4437-138">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da SendGrid-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="b4437-138">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that SendGrid meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="b4437-139">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="b4437-139">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="b4437-140">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="b4437-140">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]