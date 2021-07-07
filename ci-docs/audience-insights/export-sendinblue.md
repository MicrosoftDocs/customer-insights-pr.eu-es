---
title: Esportatu Customer Insights datuak Sendinblue-ra
description: Ikasi konexioa nola konfiguratu eta Sendinblue-ra esportatu.
ms.date: 06/29/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 58ca0ae5ad4a3a291f4336984d14fefb23a58ab3
ms.sourcegitcommit: 057079532e31c12bac36f374857ba3dc847d6ad0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314571"
---
# <a name="export-segments-to-sendinblue-preview"></a><span data-ttu-id="6f113-103">Esportatu segmentuak Sendinblue-ra (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="6f113-103">Export segments to Sendinblue (preview)</span></span>

<span data-ttu-id="6f113-104">Esportatu bezero profil bateratuen segmentuak kanpaniak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzei etekinik handiena ateratzeko Sendinblue bidez.</span><span class="sxs-lookup"><span data-stu-id="6f113-104">Export segments of unified customer profiles to generate campaigns, provide email marketing and use specific groups of customers with Sendinblue.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="6f113-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="6f113-105">Prerequisites for connection</span></span>

-   <span data-ttu-id="6f113-106">Baduzu [Sendinblue kontua](https://www.sendinblue.com/) eta dagozkien administratzaile egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="6f113-106">You have a [Sendinblue account](https://www.sendinblue.com/) and corresponding administrator credentials.</span></span>
-   <span data-ttu-id="6f113-107">Sendinblue-n dauden zerrendak eta dagozkien IDak daude.</span><span class="sxs-lookup"><span data-stu-id="6f113-107">There are existing lists in Sendinblue and the corresponding IDs.</span></span>
-   <span data-ttu-id="6f113-108">[Konfiguratutako segmentuak](segments.md) dituzu.</span><span class="sxs-lookup"><span data-stu-id="6f113-108">You have [configured segments](segments.md).</span></span>
-   <span data-ttu-id="6f113-109">Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.</span><span class="sxs-lookup"><span data-stu-id="6f113-109">Unified customer profiles in the exported segments contain a field representing an email address.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="6f113-110">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="6f113-110">Known limitations</span></span>

- <span data-ttu-id="6f113-111">Gehienez milioi bat profileko Sendinblue esportazio bakoitzeko.</span><span class="sxs-lookup"><span data-stu-id="6f113-111">Up to 1 million profiles per export to Sendinblue.</span></span>
- <span data-ttu-id="6f113-112">Sendinblue-ra esportatzea segmentuetara mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="6f113-112">Exporting to Sendinblue is limited to segments.</span></span>
- <span data-ttu-id="6f113-113">Guztira 1 milioi profil dituzten segmentuak esportatzeak 90 minutu iraun dezake.</span><span class="sxs-lookup"><span data-stu-id="6f113-113">Exporting segments with a total of 1 million profiles can take up to 90 minutes.</span></span> 
- <span data-ttu-id="6f113-114">Sendinblue-ra esporta ditzakezun profilen kopurua Sendinblue-rekin duzun kontratuaren menpe dago eta mugatua da.</span><span class="sxs-lookup"><span data-stu-id="6f113-114">The number of profiles that you can export to Sendinblue is dependent and limited on your contract with Sendinblue.</span></span>

## <a name="set-up-connection-to-sendinblue"></a><span data-ttu-id="6f113-115">Konfiguratu Sendinblue-ra konexioa</span><span class="sxs-lookup"><span data-stu-id="6f113-115">Set up connection to Sendinblue</span></span>

1. <span data-ttu-id="6f113-116">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="6f113-116">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="6f113-117">Aukeratu **Gehitu konexioa** eta aukeratu **Sendinblue** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="6f113-117">Select **Add connection** and choose **Sendinblue** to configure the connection.</span></span>

1. <span data-ttu-id="6f113-118">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="6f113-118">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="6f113-119">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="6f113-119">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="6f113-120">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="6f113-120">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="6f113-121">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="6f113-121">Choose who can use this connection.</span></span> <span data-ttu-id="6f113-122">Berez, administratzaileak soilik dira.</span><span class="sxs-lookup"><span data-stu-id="6f113-122">By default it's only administrators.</span></span> <span data-ttu-id="6f113-123">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="6f113-123">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="6f113-124">Sartu zure **[SendinBlue API gakoa](https://developers.sendinblue.com/docs/getting-started#:~:text=Get%20your%20API%20key&text=You%20can%20create%20one%20from,your%20settings%20This%20API%20key)**.</span><span class="sxs-lookup"><span data-stu-id="6f113-124">Enter your **[SendinBlue API key](https://developers.sendinblue.com/docs/getting-started#:~:text=Get%20your%20API%20key&text=You%20can%20create%20one%20from,your%20settings%20This%20API%20key)**.</span></span>

1. <span data-ttu-id="6f113-125">Aukeratu **Ados** baieztatzeko **Datuen pribatutasuna eta betetzea** eta hautatu **Konektatu** Sendinblue-rekin konexioa hasieratzeko.</span><span class="sxs-lookup"><span data-stu-id="6f113-125">Select **I agree** to confirm the **Data privacy and compliance** and select **Connect** to initialize the connection to Sendinblue.</span></span>

1. <span data-ttu-id="6f113-126">Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="6f113-126">Select **Add yourself as export user** and provide your Customer Insights credentials.</span></span>

1. <span data-ttu-id="6f113-127">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="6f113-127">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="6f113-128">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="6f113-128">Configure an export</span></span>

<span data-ttu-id="6f113-129">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="6f113-129">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="6f113-130">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="6f113-130">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="6f113-131">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="6f113-131">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="6f113-132">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="6f113-132">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="6f113-133">Urtean **Esportaziorako konexioa** eremuan, aukeratu konexio bat Sendinblue atalean.</span><span class="sxs-lookup"><span data-stu-id="6f113-133">In the **Connection for export** field, choose a connection from the Sendinblue section.</span></span> <span data-ttu-id="6f113-134">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="6f113-134">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="6f113-135">Sartu zure **SendinBlue zerrendaren IDa**</span><span class="sxs-lookup"><span data-stu-id="6f113-135">Enter your **Sendinblue list ID**</span></span> 

1. <span data-ttu-id="6f113-136">**Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena.</span><span class="sxs-lookup"><span data-stu-id="6f113-136">In the **Data matching** section, in the **Email** field, select the field in your unified customer profile that represents a customer's email address.</span></span> 

1. <span data-ttu-id="6f113-137">Aukeran, esporta dezakezu **Izena**, **Abizena** eta **Telefonoa** mezu elektroniko pertsonalizatuagoak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="6f113-137">Optionally, you can export **First name**, **Last name**, and **Phone**  to create more personalized emails.</span></span> <span data-ttu-id="6f113-138">Aukeratu **Gehitu atributua** eremu horiek esleitzeko.</span><span class="sxs-lookup"><span data-stu-id="6f113-138">Select **Add attribute** to map these fields.</span></span>

1. <span data-ttu-id="6f113-139">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="6f113-139">Select the segments you want to export.</span></span> 

1. <span data-ttu-id="6f113-140">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="6f113-140">Select **Save**.</span></span>

<span data-ttu-id="6f113-141">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="6f113-141">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="6f113-142">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="6f113-142">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="6f113-143">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="6f113-143">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="6f113-144">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="6f113-144">Data privacy and compliance</span></span>

<span data-ttu-id="6f113-145">Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko Sendinblue-ra, datuak betetze mugatik kanpo transferitzea baimentzen duzu, Dynamics 365 Customer Insights datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="6f113-145">When you enable Dynamics 365 Customer Insights to transmit data to Sendinblue, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="6f113-146">Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz Sendinblue izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu.</span><span class="sxs-lookup"><span data-stu-id="6f113-146">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Sendinblue meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="6f113-147">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="6f113-147">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="6f113-148">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="6f113-148">Your Dynamics 365 Customer Insights administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
