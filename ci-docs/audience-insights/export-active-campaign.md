---
title: Esportatu Customer Insights datuak ActiveCampaign-ra
description: Ikasi konexioa nola konfiguratu eta ActiveCampaign-ra esportatu.
ms.date: 06/29/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 6d85fa9836618e27f7f3da6ce17c07b4bc89e187
ms.sourcegitcommit: 057079532e31c12bac36f374857ba3dc847d6ad0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314572"
---
# <a name="export-segments-to-activecampaign-preview"></a><span data-ttu-id="63f45-103">Esportatu segmentuak ActiveCampaign-ra (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="63f45-103">Export segments to ActiveCampaign (preview)</span></span>

<span data-ttu-id="63f45-104">Esportatu bezero profil bateratuen segmentuak ActiveCampaign-era eta erabili marketin-jardueretarako.</span><span class="sxs-lookup"><span data-stu-id="63f45-104">Export segments of unified customer profiles to ActiveCampaign and use them for marketing activities.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63f45-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="63f45-105">Prerequisites</span></span>

-   <span data-ttu-id="63f45-106">Baduzu [ActiveCampaign kontua](https://www.activecampaign.com/) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="63f45-106">You have an [ActiveCampaign account](https://www.activecampaign.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="63f45-107">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="63f45-107">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="63f45-108">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa duen eremu bat dute.</span><span class="sxs-lookup"><span data-stu-id="63f45-108">Unified customer profiles in the exported segments contain a field with an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="63f45-109">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="63f45-109">Known limitations</span></span>

- <span data-ttu-id="63f45-110">Esportazio bakoitzeko milioi bat profil esportatu ditzakezu ActiveCampaign-era eta 90 minutu behar izan ditzakezu osatzeko.</span><span class="sxs-lookup"><span data-stu-id="63f45-110">You can export up to 1 million profiles per export to ActiveCampaign and it can take up to 90 minutes to complete.</span></span>
- <span data-ttu-id="63f45-111">ActiveCampaign-era esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="63f45-111">Exporting to ActiveCampaign is limited to segments.</span></span>
- <span data-ttu-id="63f45-112">ActiveCampaign-era esporta ditzakezun profilen kopurua ActiveCampaign-ekin duzun kontratuaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="63f45-112">The number of profiles that you can export to ActiveCampaign depends on your contract with ActiveCampaign.</span></span>

## <a name="set-up-connection-to-activecampaign"></a><span data-ttu-id="63f45-113">Konfiguratu ActiveCampaign-era konexioa</span><span class="sxs-lookup"><span data-stu-id="63f45-113">Set up connection to ActiveCampaign</span></span>

1. <span data-ttu-id="63f45-114">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="63f45-114">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="63f45-115">Aukeratu **Gehitu konexioa** eta aukeratu **ActiveCampaign** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="63f45-115">Select **Add connection** and choose **ActiveCampaign** to configure the connection.</span></span>

1. <span data-ttu-id="63f45-116">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="63f45-116">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="63f45-117">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="63f45-117">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="63f45-118">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="63f45-118">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="63f45-119">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="63f45-119">Choose who can use this connection.</span></span> <span data-ttu-id="63f45-120">Berez, administratzaileak soilik dira.</span><span class="sxs-lookup"><span data-stu-id="63f45-120">By default, it's only administrators.</span></span> <span data-ttu-id="63f45-121">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="63f45-121">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="63f45-122">Sartu zure [ActiveCampaign API gakoa eta REST amaiera puntuko ostalari izena](https://help.activecampaign.com/hc/articles/207317590-Getting-started-with-the-API#how-to-obtain-your-activecampaign-api-url-and-key).</span><span class="sxs-lookup"><span data-stu-id="63f45-122">Enter your [ActiveCampaign API Key and REST Endpoint Hostname](https://help.activecampaign.com/hc/articles/207317590-Getting-started-with-the-API#how-to-obtain-your-activecampaign-api-url-and-key).</span></span> <span data-ttu-id="63f45-123">REST Endpoint ostalari izena ostalari izena soilik da, gabe https://.</span><span class="sxs-lookup"><span data-stu-id="63f45-123">The REST Endpoint Hostname is the hostname only, without https://.</span></span> 

1. <span data-ttu-id="63f45-124">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="63f45-124">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="63f45-125">Aukeratu **Konektatu** ActiveCampaign konexioaren hautapena berresteko.</span><span class="sxs-lookup"><span data-stu-id="63f45-125">Select **Connect** to initialize the connection to ActiveCampaign.</span></span>

1. <span data-ttu-id="63f45-126">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="63f45-126">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="63f45-127">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="63f45-127">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="63f45-128">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="63f45-128">Configure an export</span></span>

<span data-ttu-id="63f45-129">Esportazio bat konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="63f45-129">You can configure an export if you have access to a connection of this type.</span></span> <span data-ttu-id="63f45-130">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="63f45-130">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="63f45-131">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="63f45-131">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="63f45-132">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="63f45-132">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="63f45-133">Urtean **Esportaziorako konexioa** eremuan, aukeratu konexio bat ActiveCampaign atalean.</span><span class="sxs-lookup"><span data-stu-id="63f45-133">In the **Connection for export** field, choose a connection from the ActiveCampaign section.</span></span> <span data-ttu-id="63f45-134">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="63f45-134">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="63f45-135">Sartu zure [**ActiveCampaign zerrendaren IDa**](https://help.activecampaign.com/hc/articles/360000030559-How-to-create-a-list-in-ActiveCampaign).</span><span class="sxs-lookup"><span data-stu-id="63f45-135">Enter your [**ActiveCampaign List ID**](https://help.activecampaign.com/hc/articles/360000030559-How-to-create-a-list-in-ActiveCampaign).</span></span>    

3. <span data-ttu-id="63f45-136">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="63f45-136">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="63f45-137">ActiveCampaign-era esportatzea segmentuetara beharrezkoa da.</span><span class="sxs-lookup"><span data-stu-id="63f45-137">It's required to export segments to ActiveCampaign.</span></span> <span data-ttu-id="63f45-138">Aukeran, esporta dezakezu Izena, Abizena eta Telefonoa mezu elektroniko pertsonalizatuagoak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="63f45-138">Optionally, you can export First name, Last name, and Phone to create more personalized emails.</span></span> <span data-ttu-id="63f45-139">Aukeratu Gehitu atributua eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="63f45-139">Select Add attribute to map these fields.</span></span>

1. <span data-ttu-id="63f45-140">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="63f45-140">Select **Save**.</span></span>

<span data-ttu-id="63f45-141">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="63f45-141">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="63f45-142">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="63f45-142">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="63f45-143">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="63f45-143">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="63f45-144">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="63f45-144">Data privacy and compliance</span></span>

<span data-ttu-id="63f45-145">Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko ActiveCampaign-era, datuak betetze mugatik kanpo transferitzea baimentzen duzu, Dynamics 365 Customer Insights datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="63f45-145">When you enable Dynamics 365 Customer Insights to transmit data to ActiveCampaign, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="63f45-146">Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz ActiveCampaign izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu.</span><span class="sxs-lookup"><span data-stu-id="63f45-146">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that ActiveCampaign meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="63f45-147">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="63f45-147">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>

<span data-ttu-id="63f45-148">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="63f45-148">Your Dynamics 365 Customer Insights administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
