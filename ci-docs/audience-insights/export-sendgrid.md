---
title: Esportatu Customer Insights datuak SendGrid-era
description: Ikasi konexioa nola konfiguratu eta SendGrid-era esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 5d3d61d2b5b68079c7717e41dee5a2f698f2b62c
ms.sourcegitcommit: e8e03309ba2515374a70c132d0758f3e1e1851d0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5976901"
---
# <a name="export-segments-to-sendgrid-preview"></a><span data-ttu-id="a8775-103">Esportatu segmentuak SendGrid-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="a8775-103">Export segments to SendGrid (preview)</span></span>

<span data-ttu-id="a8775-104">Esportatu bezeroen profil bateratuen segmentuak SendGrid kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko SendGrid-en.</span><span class="sxs-lookup"><span data-stu-id="a8775-104">Export segments of unified customer profiles to SendGrid contact lists and use them for campaigns and email marketing in SendGrid.</span></span> 

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="a8775-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="a8775-105">Prerequisites for a connection</span></span>

-   <span data-ttu-id="a8775-106">Baduzu [SendGrid kontua](https://sendgrid.com/) eta dagozkion administratzaile kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="a8775-106">You have a [SendGrid account](https://sendgrid.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="a8775-107">SendGrid-en kontaktu-zerrendak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="a8775-107">There are existing contact lists in SendGrid and the corresponding IDs.</span></span> <span data-ttu-id="a8775-108">Informazio gehiagorako, ikus [SendGrid: kudeatu kontaktuak](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts).</span><span class="sxs-lookup"><span data-stu-id="a8775-108">For more information, see [SendGrid - Manage contacts](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts).</span></span>
-   <span data-ttu-id="a8775-109">Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="a8775-109">You have [configured segments](segments.md) in audience insights.</span></span>
-   <span data-ttu-id="a8775-110">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="a8775-110">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="a8775-111">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="a8775-111">Known limitations</span></span>

- <span data-ttu-id="a8775-112">Gehienez 100.000 profil guztira SendGrid-era.</span><span class="sxs-lookup"><span data-stu-id="a8775-112">Up to 100'000 profiles in total to SendGrid.</span></span>
- <span data-ttu-id="a8775-113">SendGrid-era esportatzea segmentuetara mugatuta dago.</span><span class="sxs-lookup"><span data-stu-id="a8775-113">Exporting to SendGrid is limited to segments.</span></span>
- <span data-ttu-id="a8775-114">SendGrid-era 100.000 profil gehienera esportatzeak ordu batzuk behar izan ditzake osatzeko.</span><span class="sxs-lookup"><span data-stu-id="a8775-114">Exporting up to 100'000 profiles to SendGrid can take up to a few hours to complete.</span></span> 
- <span data-ttu-id="a8775-115">SendGrid-era esporta ditzakezun profilen kopurua SendGrid-ekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="a8775-115">The number of profiles that you can export to SendGrid is dependent and limited on your contract with SendGrid.</span></span>

## <a name="set-up-connection-to-sendgrid"></a><span data-ttu-id="a8775-116">Konfiguratu konexioa SendGrid-era</span><span class="sxs-lookup"><span data-stu-id="a8775-116">Set up connection to SendGrid</span></span>

1. <span data-ttu-id="a8775-117">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="a8775-117">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="a8775-118">Hautatu **Gehitu konexioa** eta aukeratu **SendGrid** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="a8775-118">Select **Add connection** and choose **SendGrid** to configure the connection.</span></span>

1. <span data-ttu-id="a8775-119">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="a8775-119">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="a8775-120">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="a8775-120">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="a8775-121">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="a8775-121">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="a8775-122">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="a8775-122">Choose who can use this connection.</span></span> <span data-ttu-id="a8775-123">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="a8775-123">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="a8775-124">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="a8775-124">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="a8775-125">Sartu zure **SendGrid API gakoa** [SendGrid API gakoa](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).</span><span class="sxs-lookup"><span data-stu-id="a8775-125">Enter your **SendGrid API key** [SendGrid API key](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).</span></span>

1. <span data-ttu-id="a8775-126">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="a8775-126">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="a8775-127">Aukeratu **Konektatu** SendGrid-eko konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="a8775-127">Select **Connect** to initialize the connection to SendGrid.</span></span>

1. <span data-ttu-id="a8775-128">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="a8775-128">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="a8775-129">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="a8775-129">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="a8775-130">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="a8775-130">Configure an export</span></span>

<span data-ttu-id="a8775-131">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="a8775-131">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="a8775-132">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="a8775-132">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="a8775-133">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="a8775-133">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="a8775-134">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="a8775-134">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="a8775-135">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SendGrid sekzioan.</span><span class="sxs-lookup"><span data-stu-id="a8775-135">In the **Connection for export** field, choose a connection from the SendGrid section.</span></span> <span data-ttu-id="a8775-136">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="a8775-136">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="a8775-137">Sartu zure **[SendGrid zerrendaren IDa](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts)**.</span><span class="sxs-lookup"><span data-stu-id="a8775-137">Enter your **[SendGrid list ID](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts)**.</span></span>

1. <span data-ttu-id="a8775-138">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="a8775-138">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> <span data-ttu-id="a8775-139">Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **herrialdea/eskualdea**, **estatua**, **hiria** eta **posta kodea**.</span><span class="sxs-lookup"><span data-stu-id="a8775-139">Repeat the same steps for other optional fields such as **First name**, **Last name**, **Country/Region**, **State**, **City**, and **Post code**.</span></span>

1. <span data-ttu-id="a8775-140">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="a8775-140">Select the segments you want to export.</span></span> <span data-ttu-id="a8775-141">Biziki **gomendatzen dugu 100.000 bezero profil baino gehiago ez esportatzea guztira** SendGrid-era.</span><span class="sxs-lookup"><span data-stu-id="a8775-141">We strongly **recommend to not export more than 100'000 customer profiles in total** to SendGrid.</span></span> 

1. <span data-ttu-id="a8775-142">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="a8775-142">Select **Save**.</span></span>

<span data-ttu-id="a8775-143">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="a8775-143">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="a8775-144">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="a8775-144">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="a8775-145">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="a8775-145">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="a8775-146">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="a8775-146">Data privacy and compliance</span></span>

<span data-ttu-id="a8775-147">Dynamics 365 Customer Insights gaitzen duzunean datuak SendGrid-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="a8775-147">When you enable Dynamics 365 Customer Insights to transmit data to SendGrid, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="a8775-148">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da SendGrid-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="a8775-148">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that SendGrid meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="a8775-149">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="a8775-149">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="a8775-150">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="a8775-150">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]