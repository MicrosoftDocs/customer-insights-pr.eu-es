---
title: Esportatu Customer Insights datuak Omnisend-era
description: Ikasi konexioa nola konfiguratu eta Omnisend-era esportatu.
ms.date: 05/21/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 8bd692819fa8451ded5e74191ee717f81f87425d
ms.sourcegitcommit: 831765a55775d358447cb7ffa56f2c3b85459084
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6124448"
---
# <a name="export-segments-to-omnisend-preview"></a><span data-ttu-id="412f2-103">Esportatu segmentuak Omnisend-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="412f2-103">Export segments to Omnisend (preview)</span></span>

<span data-ttu-id="412f2-104">Esportatu bezeroen profil bateratuen segmentuak Omnisend-era eta erabili marketin jardueretarako.</span><span class="sxs-lookup"><span data-stu-id="412f2-104">Export segments of unified customer profiles to Omnisend and use them for marketing activities.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="412f2-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="412f2-105">Prerequisites</span></span>

-   <span data-ttu-id="412f2-106">Baduzu [Omnisend kontua](https://www.omnisend.com/) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="412f2-106">You have an [Omnisend account](https://www.omnisend.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="412f2-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="412f2-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="412f2-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="412f2-108">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="412f2-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="412f2-109">Known limitations</span></span>

- <span data-ttu-id="412f2-110">Esportazio bakoitzeko milioi bat profil esportatu ditzakezu Omnisend-era eta 4 ordu behar izan ditzakezu osatzeko.</span><span class="sxs-lookup"><span data-stu-id="412f2-110">You can export up to 1 million profiles per export to Omnisend and it can take up to 4 hours to complete.</span></span>
- <span data-ttu-id="412f2-111">Omnisend-era esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="412f2-111">Exporting to Omnisend is limited to segments.</span></span>
- <span data-ttu-id="412f2-112">Omnisend-era esporta ditzakezun profilen kopurua Omnisend-ekin duzun kontratuaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="412f2-112">The number of profiles that you can export to Omnisend depends on your contract with Omnisend.</span></span>

## <a name="set-up-connection-to-omnisend"></a><span data-ttu-id="412f2-113">Konfiguratu konexioa Omnisend-era</span><span class="sxs-lookup"><span data-stu-id="412f2-113">Set up connection to Omnisend</span></span>

1. <span data-ttu-id="412f2-114">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="412f2-114">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="412f2-115">Hautatu **Gehitu konexioa** eta aukeratu **Omnisend** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="412f2-115">Select **Add connection** and choose **Omnisend** to configure the connection.</span></span>

1. <span data-ttu-id="412f2-116">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="412f2-116">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="412f2-117">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="412f2-117">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="412f2-118">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="412f2-118">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="412f2-119">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="412f2-119">Choose who can use this connection.</span></span> <span data-ttu-id="412f2-120">Berez, administratzaileak soilik dira.</span><span class="sxs-lookup"><span data-stu-id="412f2-120">By default it's only administrators.</span></span> <span data-ttu-id="412f2-121">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="412f2-121">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="412f2-122">Sartu zure [Omnisend-en API gakoa](https://support.omnisend.com/en/articles/1061890-generating-api-key).</span><span class="sxs-lookup"><span data-stu-id="412f2-122">Enter your [Omnisend API key](https://support.omnisend.com/en/articles/1061890-generating-api-key).</span></span>

1. <span data-ttu-id="412f2-123">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="412f2-123">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="412f2-124">Aukeratu **Konektatu** Omnisend-erako konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="412f2-124">Select **Connect** to initialize the connection to Omnisend.</span></span>

1. <span data-ttu-id="412f2-125">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="412f2-125">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="412f2-126">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="412f2-126">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="412f2-127">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="412f2-127">Configure an export</span></span>

<span data-ttu-id="412f2-128">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="412f2-128">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="412f2-129">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="412f2-129">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="412f2-130">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="412f2-130">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="412f2-131">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="412f2-131">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="412f2-132">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Omnisend sekzioan.</span><span class="sxs-lookup"><span data-stu-id="412f2-132">In the **Connection for export** field, choose a connection from the Omnisend section.</span></span> <span data-ttu-id="412f2-133">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="412f2-133">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="412f2-134">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="412f2-134">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="412f2-135">Segmentuak esportatu behar dira Omnisend-era.</span><span class="sxs-lookup"><span data-stu-id="412f2-135">It's required to export segments to Omnisend.</span></span> <span data-ttu-id="412f2-136">Aukeran, Izena, Abizena, Helbidea, Herrialdea/eskualdea, Egoera eta posta-kodea esporta ditzakezu mezu elektroniko pertsonalizatuagoak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="412f2-136">Optionally, you can export First name, Last name, Address, Country/Region, State, City, and Post Code to create more personalized emails.</span></span> <span data-ttu-id="412f2-137">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="412f2-137">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="412f2-138">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="412f2-138">Select **Save**.</span></span>

<span data-ttu-id="412f2-139">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="412f2-139">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="412f2-140">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="412f2-140">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="412f2-141">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="412f2-141">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="412f2-142">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="412f2-142">Data privacy and compliance</span></span>

<span data-ttu-id="412f2-143">Gaitzen duzunean Dynamics 365 Customer Insights datuak Omnisend-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="412f2-143">When you enable Dynamics 365 Customer Insights to transmit data to Ommisend, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="412f2-144">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Omnisend-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz.</span><span class="sxs-lookup"><span data-stu-id="412f2-144">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Omnisend meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="412f2-145">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="412f2-145">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="412f2-146">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="412f2-146">Your Dynamics 365 Customer Insights administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
