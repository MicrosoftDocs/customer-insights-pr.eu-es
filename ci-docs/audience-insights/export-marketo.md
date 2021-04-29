---
title: Esportatu Customer Insights datuak Marketo-ra
description: Ikasi konexioa konfiguratzen eta Marketo-ra esportatzen.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 01290d5fae7af1737b73373d75e334ae1ed67d37
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5759806"
---
# <a name="export-segments-to-marketo-preview"></a><span data-ttu-id="674c3-103">Esportatu segmentuak Marketo-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="674c3-103">Export segments to Marketo (preview)</span></span>

<span data-ttu-id="674c3-104">Kanpainak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzak erabiltzeko Marketo bidez, esportatu bezeroen profil bateratuetako segmentuak.</span><span class="sxs-lookup"><span data-stu-id="674c3-104">Export segments of unified customer profiles to generate campaigns, provide email marketing and use specific groups of customers with Marketo.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="674c3-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="674c3-105">Prerequisites for connection</span></span>

-   <span data-ttu-id="674c3-106">Baduzu [Marketo kontua](https://login.marketo.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="674c3-106">You have a [Marketo account](https://login.marketo.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="674c3-107">Marketo-n zerrendak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="674c3-107">There are existing lists in Marketo and the corresponding IDs.</span></span> <span data-ttu-id="674c3-108">Informazio gehiagorako, ikus [Marketo-ko zerrendak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span><span class="sxs-lookup"><span data-stu-id="674c3-108">For more information, see [Marketo lists](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span></span>
-   <span data-ttu-id="674c3-109">[Konfiguratutako segmentuak](segments.md) dituzu.</span><span class="sxs-lookup"><span data-stu-id="674c3-109">You have [configured segments](segments.md).</span></span>
-   <span data-ttu-id="674c3-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="674c3-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="674c3-111">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="674c3-111">Known limitations</span></span>

- <span data-ttu-id="674c3-112">Gehienez milioi bat profil Marketo-ra esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="674c3-112">Up to 1 million profiles per export to Marketo.</span></span>
- <span data-ttu-id="674c3-113">Marketo-ra esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="674c3-113">Exporting to Marketo is limited to segments.</span></span>
- <span data-ttu-id="674c3-114">Guztira 1 milioi profil dituzten segmentuak esportatzen 3 ordu behar izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="674c3-114">Exporting segments with a total of 1 million profiles can take up to 3 hours.</span></span> 
- <span data-ttu-id="674c3-115">Marketo-ra esporta ditzakezun profilen kopurua Marketo-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="674c3-115">The number of profiles that you can export to Marketo is dependent and limited on your contract with Marketo.</span></span>

## <a name="set-up-connection-to-marketo"></a><span data-ttu-id="674c3-116">Konfiguratu konexioa Marketo-ra</span><span class="sxs-lookup"><span data-stu-id="674c3-116">Set up connection to Marketo</span></span>

1. <span data-ttu-id="674c3-117">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="674c3-117">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="674c3-118">Hautatu **Gehitu konexioa** eta aukeratu **Marketo** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="674c3-118">Select **Add connection** and choose **Marketo** to configure the connection.</span></span>

1. <span data-ttu-id="674c3-119">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="674c3-119">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="674c3-120">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="674c3-120">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="674c3-121">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="674c3-121">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="674c3-122">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="674c3-122">Choose who can use this connection.</span></span> <span data-ttu-id="674c3-123">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="674c3-123">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="674c3-124">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="674c3-124">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="674c3-125">Sartu zure **[Marketo-ren bezeroaren IDa, Bezeroaren sekretua eta REST amaiera-puntuaren ostalari izena](https://developers.marketo.com/rest-api/authentication/)**.</span><span class="sxs-lookup"><span data-stu-id="674c3-125">Enter your **[Marketo client ID, Client secret, and REST Endpoint Hostname](https://developers.marketo.com/rest-api/authentication/)**.</span></span>

1. <span data-ttu-id="674c3-126">Aukeratu **ados** **Datu-pribatutasuna eta arau-betetzea** onartzeko eta hautatu **Konektatu** Marketo-rekin konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="674c3-126">Select **I agree** to confirm the **Data privacy and compliance** and select **Connect** to initialize the connection to Marketo.</span></span>

1. <span data-ttu-id="674c3-127">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="674c3-127">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="674c3-128">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="674c3-128">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="674c3-129">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="674c3-129">Configure an export</span></span>

<span data-ttu-id="674c3-130">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="674c3-130">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="674c3-131">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="674c3-131">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="674c3-132">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="674c3-132">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="674c3-133">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="674c3-133">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="674c3-134">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Marketo sekzioan.</span><span class="sxs-lookup"><span data-stu-id="674c3-134">In the **Connection for export** field, choose a connection from the Marketo section.</span></span> <span data-ttu-id="674c3-135">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="674c3-135">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="674c3-136">Sartu zure **[Marketo zerrendaren IDa](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)**</span><span class="sxs-lookup"><span data-stu-id="674c3-136">Enter your **[Marketo list ID](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)**</span></span> 

1. <span data-ttu-id="674c3-137">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="674c3-137">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> 

1. <span data-ttu-id="674c3-138">Aukeran, esporta dezakezu **Izena**, **Abizena**, **Hiria**, **Egoera**, eta **Herrialdea/eskualdea** mezu elektroniko pertsonalizatuagoak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="674c3-138">Optionally, you can export **First name**, **Last name**, **City**, **State**, and **Country/Region**  to create more personalized emails.</span></span> <span data-ttu-id="674c3-139">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="674c3-139">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="674c3-140">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="674c3-140">Select the segments you want to export.</span></span> <span data-ttu-id="674c3-141">Guztira 1 milioi bezero profil esporta ditzakezu Marketo-ra.</span><span class="sxs-lookup"><span data-stu-id="674c3-141">You can export up to 1 million customer profiles in total to Marketo.</span></span>

1. <span data-ttu-id="674c3-142">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="674c3-142">Select **Save**.</span></span>

<span data-ttu-id="674c3-143">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="674c3-143">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="674c3-144">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="674c3-144">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="674c3-145">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="674c3-145">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> <span data-ttu-id="674c3-146">Marketo-n, zure segmentuak azpian aurki ditzakezu hemen: [Marketo-ko hartzaileak](ttps://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span><span class="sxs-lookup"><span data-stu-id="674c3-146">In Marketo, you can now find your segments under [Marketo lists](ttps://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span></span>


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="674c3-147">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="674c3-147">Data privacy and compliance</span></span>

<span data-ttu-id="674c3-148">Dynamics 365 Customer Insights gaitzen duzunean datuak Marketo-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="674c3-148">When you enable Dynamics 365 Customer Insights to transmit data to Marketo, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="674c3-149">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Marketo-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="674c3-149">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Marketo meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="674c3-150">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="674c3-150">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="674c3-151">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="674c3-151">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]