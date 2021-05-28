---
title: Esportatu Customer Insights datuak Marketo-ra
description: Ikasi konexioa konfiguratzen eta Marketo-ra esportatzen.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: b5a644e286bd44d4ebf7d1837255326c005b48d6
ms.sourcegitcommit: 74cd4fa9cbb784d9dff174c0eec7b4dcb408d66b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059301"
---
# <a name="export-segments-to-marketo-preview"></a><span data-ttu-id="890d0-103">Esportatu segmentuak Marketo-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="890d0-103">Export segments to Marketo (preview)</span></span>

<span data-ttu-id="890d0-104">Kanpainak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzak erabiltzeko Marketo bidez, esportatu bezeroen profil bateratuetako segmentuak.</span><span class="sxs-lookup"><span data-stu-id="890d0-104">Export segments of unified customer profiles to generate campaigns, provide email marketing and use specific groups of customers with Marketo.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="890d0-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="890d0-105">Prerequisites for connection</span></span>

-   <span data-ttu-id="890d0-106">Baduzu [Marketo kontua](https://login.marketo.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="890d0-106">You have a [Marketo account](https://login.marketo.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="890d0-107">Marketo-n zerrendak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="890d0-107">There are existing lists in Marketo and the corresponding IDs.</span></span> <span data-ttu-id="890d0-108">Informazio gehiagorako, ikus [Marketo-ko zerrendak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span><span class="sxs-lookup"><span data-stu-id="890d0-108">For more information, see [Marketo lists](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span></span>
-   <span data-ttu-id="890d0-109">[Konfiguratutako segmentuak](segments.md) dituzu.</span><span class="sxs-lookup"><span data-stu-id="890d0-109">You have [configured segments](segments.md).</span></span>
-   <span data-ttu-id="890d0-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="890d0-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="890d0-111">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="890d0-111">Known limitations</span></span>

- <span data-ttu-id="890d0-112">Gehienez milioi bat profil Marketo-ra esportatzeko.</span><span class="sxs-lookup"><span data-stu-id="890d0-112">Up to 1 million profiles per export to Marketo.</span></span>
- <span data-ttu-id="890d0-113">Marketo-ra esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="890d0-113">Exporting to Marketo is limited to segments.</span></span>
- <span data-ttu-id="890d0-114">Guztira 1 milioi profil dituzten segmentuak esportatzen 3 ordu behar izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="890d0-114">Exporting segments with a total of 1 million profiles can take up to 3 hours.</span></span> 
- <span data-ttu-id="890d0-115">Marketo-ra esporta ditzakezun profilen kopurua Marketo-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="890d0-115">The number of profiles that you can export to Marketo is dependent and limited on your contract with Marketo.</span></span>

## <a name="set-up-connection-to-marketo"></a><span data-ttu-id="890d0-116">Konfiguratu konexioa Marketo-ra</span><span class="sxs-lookup"><span data-stu-id="890d0-116">Set up connection to Marketo</span></span>

1. <span data-ttu-id="890d0-117">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="890d0-117">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="890d0-118">Hautatu **Gehitu konexioa** eta aukeratu **Marketo** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="890d0-118">Select **Add connection** and choose **Marketo** to configure the connection.</span></span>

1. <span data-ttu-id="890d0-119">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="890d0-119">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="890d0-120">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="890d0-120">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="890d0-121">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="890d0-121">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="890d0-122">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="890d0-122">Choose who can use this connection.</span></span> <span data-ttu-id="890d0-123">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="890d0-123">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="890d0-124">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="890d0-124">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="890d0-125">Sartu zure **[Marketo-ren bezeroaren IDa, Bezeroaren sekretua eta REST amaiera-puntuaren ostalari izena](https://developers.marketo.com/rest-api/authentication/)**.</span><span class="sxs-lookup"><span data-stu-id="890d0-125">Enter your **[Marketo client ID, Client secret, and REST Endpoint Hostname](https://developers.marketo.com/rest-api/authentication/)**.</span></span> <span data-ttu-id="890d0-126">REST Endpoint ostalari izena ostalari izena soilik da, gabe `https://`.</span><span class="sxs-lookup"><span data-stu-id="890d0-126">The REST Endpoint Hostname is the hostname only, without `https://`.</span></span> <span data-ttu-id="890d0-127">Adibidez: `xyz-abc-123.mktorest.com`.</span><span class="sxs-lookup"><span data-stu-id="890d0-127">Example: `xyz-abc-123.mktorest.com`.</span></span> 

1. <span data-ttu-id="890d0-128">Aukeratu **ados** **Datu-pribatutasuna eta arau-betetzea** onartzeko eta hautatu **Konektatu** Marketo-rekin konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="890d0-128">Select **I agree** to confirm the **Data privacy and compliance** and select **Connect** to initialize the connection to Marketo.</span></span>

1. <span data-ttu-id="890d0-129">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="890d0-129">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="890d0-130">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="890d0-130">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="890d0-131">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="890d0-131">Configure an export</span></span>

<span data-ttu-id="890d0-132">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="890d0-132">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="890d0-133">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="890d0-133">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="890d0-134">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="890d0-134">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="890d0-135">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="890d0-135">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="890d0-136">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Marketo sekzioan.</span><span class="sxs-lookup"><span data-stu-id="890d0-136">In the **Connection for export** field, choose a connection from the Marketo section.</span></span> <span data-ttu-id="890d0-137">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="890d0-137">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="890d0-138">Idatzi **[Marketo zerrendaren IDa](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)**.</span><span class="sxs-lookup"><span data-stu-id="890d0-138">Enter your **[Marketo list ID](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)**.</span></span> <span data-ttu-id="890d0-139">Zerrendaren IDa zenbaki hutsa da.</span><span class="sxs-lookup"><span data-stu-id="890d0-139">The list ID is a purely numerical value.</span></span> <span data-ttu-id="890d0-140">Adibidez, Marketo zerrendaren IDa ST12345A7 bada, kendu karakterea zenbakien aurretik eta ondoren eta idatzi `12345`.</span><span class="sxs-lookup"><span data-stu-id="890d0-140">For example, if your Marketo list ID is ST12345A7, remove the character before and after the numerals and enter `12345`.</span></span> 

1. <span data-ttu-id="890d0-141">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="890d0-141">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> 

1. <span data-ttu-id="890d0-142">Aukeran, esporta dezakezu **Izena**, **Abizena**, **Hiria**, **Egoera** eta **Herrialdea/eskualdea** mezu elektroniko pertsonalizatuagoak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="890d0-142">Optionally, you can export **First name**, **Last name**, **City**, **State**, and **Country/Region**  to create more personalized emails.</span></span> <span data-ttu-id="890d0-143">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="890d0-143">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="890d0-144">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="890d0-144">Select the segments you want to export.</span></span> <span data-ttu-id="890d0-145">Guztira 1 milioi bezero profil esporta ditzakezu Marketo-ra.</span><span class="sxs-lookup"><span data-stu-id="890d0-145">You can export up to 1 million customer profiles in total to Marketo.</span></span>

1. <span data-ttu-id="890d0-146">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="890d0-146">Select **Save**.</span></span>

<span data-ttu-id="890d0-147">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="890d0-147">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="890d0-148">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="890d0-148">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="890d0-149">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="890d0-149">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> <span data-ttu-id="890d0-150">Marketo-n, zure segmentuak azpian aurki ditzakezu hemen: [Marketo-ko hartzaileak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span><span class="sxs-lookup"><span data-stu-id="890d0-150">In Marketo, you can now find your segments under [Marketo lists](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).</span></span>


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="890d0-151">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="890d0-151">Data privacy and compliance</span></span>

<span data-ttu-id="890d0-152">Dynamics 365 Customer Insights gaitzen duzunean datuak Marketo-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="890d0-152">When you enable Dynamics 365 Customer Insights to transmit data to Marketo, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="890d0-153">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Marketo-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="890d0-153">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Marketo meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="890d0-154">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="890d0-154">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="890d0-155">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="890d0-155">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
