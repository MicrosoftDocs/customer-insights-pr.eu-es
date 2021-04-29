---
title: LiveRamp konektorea
description: Ikasi konexioa eta esportazioa LiveRamp-era nola konfiguratu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 987457966fe1fc034d9e3cd2a1ce33902c7a84f4
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760312"
---
# <a name="export-segments-to-liverampreg-preview"></a><span data-ttu-id="100f1-103">Esportatu segmentuak LiveRamp-era&reg; (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="100f1-103">Export segments to LiveRamp&reg; (preview)</span></span>

<span data-ttu-id="100f1-104">Aktibatu zure datuak LiveRamp-en 500 plataforma baino gehiagorekin konektatzeko telebista digitaletan, sozialetan eta telebistetan.</span><span class="sxs-lookup"><span data-stu-id="100f1-104">Activate your data in LiveRamp to connect with over 500 platforms across digital, social, and TVs.</span></span> <span data-ttu-id="100f1-105">Lan egin LiveRamp-ekin zure datuekin iragarki-kanpainak zuzentzeko, ezabatzeko eta pertsonalizatzeko.</span><span class="sxs-lookup"><span data-stu-id="100f1-105">Work with your data in LiveRamp to target, suppress, and personalize ad campaigns.</span></span>

## <a name="prerequisites-for-a-connection"></a><span data-ttu-id="100f1-106">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="100f1-106">Prerequisites for a connection</span></span>

- <span data-ttu-id="100f1-107">Konektore hau erabiltzeko LiveRamp-eko harpidetza behar duzu.</span><span class="sxs-lookup"><span data-stu-id="100f1-107">You need a LiveRamp subscription to use this connector.</span></span>
- <span data-ttu-id="100f1-108">Harpidetza lortzeko, [jarri harremanetan LiveRamp-ekin](https://liveramp.com/contact/) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="100f1-108">To get a subscription, [contact LiveRamp](https://liveramp.com/contact/) directly.</span></span> <span data-ttu-id="100f1-109">[Argibide gehiago LiveRamp Onboarding-i buruz](https://liveramp.com/our-platform/data-onboarding/).</span><span class="sxs-lookup"><span data-stu-id="100f1-109">[Learn more about LiveRamp Onboarding](https://liveramp.com/our-platform/data-onboarding/).</span></span>

## <a name="set-up-connection-to-liveramp"></a><span data-ttu-id="100f1-110">Konfiguratu konexioa LiveRamp-era</span><span class="sxs-lookup"><span data-stu-id="100f1-110">Set up connection to LiveRamp</span></span>

1. <span data-ttu-id="100f1-111">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="100f1-111">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="100f1-112">Hautatu **Gehitu konexioa** eta aukeratu **LiveRamp** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="100f1-112">Select **Add connection** and choose **LiveRamp** to configure the connection.</span></span>

1. <span data-ttu-id="100f1-113">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="100f1-113">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="100f1-114">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="100f1-114">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="100f1-115">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="100f1-115">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="100f1-116">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="100f1-116">Choose who can use this connection.</span></span> <span data-ttu-id="100f1-117">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="100f1-117">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="100f1-118">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="100f1-118">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="100f1-119">Eman **Erabiltzaile izena** eta **Pasahitza** zure LiveRamp Secure FTP (SFTP) kontuan.</span><span class="sxs-lookup"><span data-stu-id="100f1-119">Provide a **Username** and **Password** for your LiveRamp Secure FTP (SFTP) account.</span></span>
<span data-ttu-id="100f1-120">Kredentzial hauek zure LiveRamp Onboarding kredentzialak desberdinak izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="100f1-120">These credentials may be different from your LiveRamp Onboarding credentials.</span></span>

1. <span data-ttu-id="100f1-121">Aukeratu **Ziurtatu** LiveRamp-ekin konexioa probatzeko.</span><span class="sxs-lookup"><span data-stu-id="100f1-121">Select **Verify** to test the connection to LiveRamp.</span></span>

1. <span data-ttu-id="100f1-122">Egiaztatu ondoren, eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="100f1-122">After successful verification, provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span>

1. <span data-ttu-id="100f1-123">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="100f1-123">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="100f1-124">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="100f1-124">Configure an export</span></span>

<span data-ttu-id="100f1-125">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="100f1-125">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="100f1-126">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="100f1-126">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="100f1-127">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="100f1-127">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="100f1-128">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="100f1-128">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="100f1-129">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa LiveRamp sekzioan.</span><span class="sxs-lookup"><span data-stu-id="100f1-129">In the **Connection for export** field, choose a connection from the LiveRamp section.</span></span> <span data-ttu-id="100f1-130">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="100f1-130">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="100f1-131">Sarbidean **Aukeratu zure gako identifikatzailea** eremua, hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** identitatearen ebazpenerako LiveRamp-era bidali.</span><span class="sxs-lookup"><span data-stu-id="100f1-131">In the **Choose your key identifier** field, select **Email**,  **Name and address**, or **Phone** to send to LiveRamp for identity resolution.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="100f1-132">![LiveRamp konektorea atributuen mapak](media/export-liveramp-segments.png "LiveRamp konektorea atributuen mapak")</span><span class="sxs-lookup"><span data-stu-id="100f1-132">![LiveRamp connector with attribute mapping](media/export-liveramp-segments.png "LiveRamp connector with attribute mapping")</span></span>

1. <span data-ttu-id="100f1-133">Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.</span><span class="sxs-lookup"><span data-stu-id="100f1-133">Map the corresponding attributes from your unified customer entity for the selected key identifier.</span></span>

1. <span data-ttu-id="100f1-134">Hautatu **Gehitu atributua** LiveRamp-era bidalitako atributu gehiago jarraitzeko.</span><span class="sxs-lookup"><span data-stu-id="100f1-134">Select **Add attribute** to map more attributes to send to LiveRamp.</span></span>

   > [!TIP]
   > <span data-ttu-id="100f1-135">LiveRamp erabiltzaileari gako identifikatzaile atributu gehiago bidaltzeak baliteke partidu tasa handiagoa lortzea.</span><span class="sxs-lookup"><span data-stu-id="100f1-135">Sending more key identifier attributes to LiveRamp is likely to get you a higher match rate.</span></span>

1. <span data-ttu-id="100f1-136">Hautatu LiveRamp-era esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="100f1-136">Select the segments you want to export to LiveRamp.</span></span>

1. <span data-ttu-id="100f1-137">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="100f1-137">Select **Save**.</span></span>

<span data-ttu-id="100f1-138">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="100f1-138">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="100f1-139">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="100f1-139">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="100f1-140">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="100f1-140">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 


## <a name="data-privacy-and-compliance"></a><span data-ttu-id="100f1-141">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="100f1-141">Data privacy and compliance</span></span>

<span data-ttu-id="100f1-142">Dynamics 365 Customer Insights gaitzen duzunean datuak Liveramp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="100f1-142">When you enable Dynamics 365 Customer Insights to transmit data to Liveramp, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="100f1-143">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Liveramp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="100f1-143">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Liveramp meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="100f1-144">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="100f1-144">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="100f1-145">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="100f1-145">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
