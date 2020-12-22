---
title: Esportatu Customer Insights datuak Marketo-ra
description: Ikasi Marketo-rako konexioa nola konfiguratu.
ms.date: 11/12/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 34ccee2894f1f2b552d0c6a88a6810e2dfc677a3
ms.sourcegitcommit: 0b1d3ca11b8ba362a959da0eea15c37e9cdba084
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "4570388"
---
# <a name="connector-for-marketo-preview"></a><span data-ttu-id="f4791-103">Marketo-ko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="f4791-103">Connector for Marketo (preview)</span></span>

<span data-ttu-id="f4791-104">Kanpainak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzak erabiltzeko Marketo bidez, esportatu bezeroen profil bateratuetako segmentuak.</span><span class="sxs-lookup"><span data-stu-id="f4791-104">Export segments of unified customer profiles to generate campaigns, provide email marketing and use specific groups of customers with Marketo.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f4791-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="f4791-105">Prerequisites</span></span>

-   <span data-ttu-id="f4791-106">Baduzu [Marketo kontua](https://login.marketo.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="f4791-106">You have a [Marketo account](https://login.marketo.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="f4791-107">Marketo-n zerrendak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="f4791-107">There are existing lists in Marketo and the corresponding IDs.</span></span> <span data-ttu-id="f4791-108">Informazio gehiagorako, ikus [Marketo-ko zerrendak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span><span class="sxs-lookup"><span data-stu-id="f4791-108">For more information, see [Marketo lists](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span></span>
-   <span data-ttu-id="f4791-109">[Konfiguratutako segmentuak](segments.md) dituzu.</span><span class="sxs-lookup"><span data-stu-id="f4791-109">You have [configured segments](segments.md).</span></span>
-   <span data-ttu-id="f4791-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="f4791-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="connect-to-marketo"></a><span data-ttu-id="f4791-111">Konektatu Marketo-ra</span><span class="sxs-lookup"><span data-stu-id="f4791-111">Connect to Marketo</span></span>

1. <span data-ttu-id="f4791-112">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="f4791-112">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="f4791-113">**Marketo** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="f4791-113">Under **Marketo**, select **Set up**.</span></span>

1. <span data-ttu-id="f4791-114">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="f4791-114">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="f4791-115">Sartu zure **[Marketo-ren bezeroaren IDa, Bezeroaren sekretua eta REST amaiera-puntuaren ostalari izena](https://developers.marketo.com/rest-api/authentication/)**.</span><span class="sxs-lookup"><span data-stu-id="f4791-115">Enter your **[Marketo client ID, Client secret and REST Endpoint Hostname](https://developers.marketo.com/rest-api/authentication/)**.</span></span>

1. <span data-ttu-id="f4791-116">Sartu zure **[Marketo zerrendaren IDa](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)**</span><span class="sxs-lookup"><span data-stu-id="f4791-116">Enter your **[Marketo list ID](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)**</span></span> 

1. <span data-ttu-id="f4791-117">Aukeratu **ados** **Datu-pribatutasuna eta arau-betetzea** onartzeko eta hautatu **Konektatu** Marketo-rekin konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="f4791-117">Select **I agree** to confirm the **Data privacy and compliance** and select **Connect** to initialize the connection to Marketo.</span></span>

1. <span data-ttu-id="f4791-118">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="f4791-118">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

   :::image type="content" source="media/export-connect-marketo.png" alt-text="Esportatu pantaila-argazkia Marketo konexiorako":::

1. <span data-ttu-id="f4791-120">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="f4791-120">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="f4791-121">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="f4791-121">Configure the connector</span></span>

1. <span data-ttu-id="f4791-122">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="f4791-122">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> 

1. <span data-ttu-id="f4791-123">Aukeran **izena**, **abizena**, **herria**, **probintzia**, eta **herrialdea/eskualdea** esporta ditzakezu eremu gehigarri gisa, mezu elektroniko pertsonalizatuagoak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="f4791-123">Optionally, you can export **First name**, **Last name**, **City**, **State**, and **Country/Region**  as additional fields to create more personalized emails.</span></span> <span data-ttu-id="f4791-124">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="f4791-124">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="f4791-125">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="f4791-125">Select the segments you want to export.</span></span> <span data-ttu-id="f4791-126">Guztira 1 milioi bezero profil esporta ditzakezu Marketo-ra.</span><span class="sxs-lookup"><span data-stu-id="f4791-126">You can export up to 1 million customer profiles in total to Marketo.</span></span>

   :::image type="content" source="media/export-segment-marketo.png" alt-text="Aukeratu eremuak eta segmentuak Marketo-ra esportatzeko":::

1. <span data-ttu-id="f4791-128">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="f4791-128">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="f4791-129">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="f4791-129">Export the data</span></span>

<span data-ttu-id="f4791-130">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="f4791-130">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="f4791-131">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="f4791-131">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="f4791-132">Marketo-n, zure segmentuak azpian aurki ditzakezu hemen: [Marketo-ko hartzaileak](ttps://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span><span class="sxs-lookup"><span data-stu-id="f4791-132">In Marketo, you can now find your segments under [Marketo lists](ttps://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="f4791-133">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="f4791-133">Known limitations</span></span>

- <span data-ttu-id="f4791-134">Gehienez milioi bat profil Marketo-ra esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="f4791-134">Up to 1 million profiles per export to Marketo.</span></span>
- <span data-ttu-id="f4791-135">Marketo-ra esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="f4791-135">Exporting to Marketo is limited to segments.</span></span>
- <span data-ttu-id="f4791-136">Guztira 1 milioi profil dituzten segmentuak esportatzen 3 ordu behar izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="f4791-136">Exporting segments with a total of 1 million profiles can take up to 3 hours.</span></span> 
- <span data-ttu-id="f4791-137">Marketo-ra esporta ditzakezun profilen kopurua Marketo-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="f4791-137">The number of profiles that you can export to Marketo is dependent and limited on your contract with Marketo.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="f4791-138">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="f4791-138">Data privacy and compliance</span></span>

<span data-ttu-id="f4791-139">Dynamics 365 Customer Insights gaitzen duzunean datuak Marketo-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="f4791-139">When you enable Dynamics 365 Customer Insights to transmit data to Marketo, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="f4791-140">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Marketo-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="f4791-140">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Marketo meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="f4791-141">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="f4791-141">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="f4791-142">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="f4791-142">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
