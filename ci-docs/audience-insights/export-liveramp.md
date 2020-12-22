---
title: LiveRamp konektorea
description: Ikasi datuak LiveRamp-era esportatzen.
ms.date: 12/02/2020
ms.reviewer: kishorem
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 86aa8c66a47ee61741082c95f05d2e5ce3f06f35
ms.sourcegitcommit: 334633cbd58f5659d20b4f87252c1a10cc7130db
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/03/2020
ms.locfileid: "4667169"
---
# <a name="liverampreg-connector-preview"></a><span data-ttu-id="3f040-103">LiveRamp&reg; konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="3f040-103">LiveRamp&reg; connector (preview)</span></span>

<span data-ttu-id="3f040-104">Aktibatu zure datuak LiveRamp-en, 500 plataforma baino gehiagorekin konektatzeko digital, sozial eta telebistetako ekosistemetan.</span><span class="sxs-lookup"><span data-stu-id="3f040-104">Activate your data in LiveRamp to connect with over 500 platforms across digital, social, and TV ecosystems.</span></span> <span data-ttu-id="3f040-105">Lan egin LiveRamp-ekin zure datuekin iragarki-kanpainak zuzentzeko, ezabatzeko eta pertsonalizatzeko.</span><span class="sxs-lookup"><span data-stu-id="3f040-105">Work with your data in LiveRamp to target, suppress, and personalize ad campaigns.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3f040-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="3f040-106">Prerequisites</span></span>

- <span data-ttu-id="3f040-107">Konektore hau erabiltzeko LiveRamp-eko harpidetza behar duzu.</span><span class="sxs-lookup"><span data-stu-id="3f040-107">You need a LiveRamp subscription to use this connector.</span></span>
- <span data-ttu-id="3f040-108">Harpidetza lortzeko, [jarri harremanetan LiveRamp-ekin](https://liveramp.com/contact/) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="3f040-108">To get a subscription, [contact LiveRamp](https://liveramp.com/contact/) directly.</span></span> <span data-ttu-id="3f040-109">[Argibide gehiago LiveRamp Onboarding-i buruz](https://liveramp.com/our-platform/data-onboarding/).</span><span class="sxs-lookup"><span data-stu-id="3f040-109">[Learn more about LiveRamp Onboarding](https://liveramp.com/our-platform/data-onboarding/).</span></span>

## <a name="connect-to-liveramp"></a><span data-ttu-id="3f040-110">Konektatu LiveRamp-era</span><span class="sxs-lookup"><span data-stu-id="3f040-110">Connect to LiveRamp</span></span>

1. <span data-ttu-id="3f040-111">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="3f040-111">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="3f040-112">**LiveRamp** lauzan, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="3f040-112">In the **LiveRamp** tile, select **Set up**.</span></span>

1. <span data-ttu-id="3f040-113">Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.</span><span class="sxs-lookup"><span data-stu-id="3f040-113">Give your destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="3f040-114">Eman **Erabiltzaile izena** eta **Pasahitza** zure LiveRamp Secure FTP (SFTP) kontuan.</span><span class="sxs-lookup"><span data-stu-id="3f040-114">Provide a **Username** and **Password** for your LiveRamp Secure FTP (SFTP) account.</span></span>
<span data-ttu-id="3f040-115">Kredentzial hauek zure LiveRamp Onboarding kredentzialak desberdinak izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="3f040-115">These credentials may be different from your LiveRamp Onboarding credentials.</span></span>

1. <span data-ttu-id="3f040-116">Aukeratu **Ziurtatu** LiveRamp-ekin konexioa probatzeko.</span><span class="sxs-lookup"><span data-stu-id="3f040-116">Select **Verify** to test the connection to LiveRamp.</span></span>

1. <span data-ttu-id="3f040-117">Egiaztatu ondoren, eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="3f040-117">After successful verification, provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span>

1. <span data-ttu-id="3f040-118">Aukeratu **hurrengo** LiveRamp konektorea konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="3f040-118">Select **Next** to set up the LiveRamp connector.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="3f040-119">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="3f040-119">Configure the connector</span></span>

1. <span data-ttu-id="3f040-120">Sarbidean **Aukeratu zure gako identifikatzailea** eremua, hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** identitatearen ebazpenerako LiveRamp-era bidali.</span><span class="sxs-lookup"><span data-stu-id="3f040-120">In the **Choose your key identifier** field, select **Email**,  **Name and address**, or **Phone** to send to LiveRamp for identity resolution.</span></span>

1. <span data-ttu-id="3f040-121">Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.</span><span class="sxs-lookup"><span data-stu-id="3f040-121">Map the corresponding attributes from your unified customer entity for the selected key identifier.</span></span>

1. <span data-ttu-id="3f040-122">Aukeratu **Gehitu atributua** LiveRamp-era bidaltzeko atributu osagarriak mapatzeko.</span><span class="sxs-lookup"><span data-stu-id="3f040-122">Select **Add attribute** to map additional attributes to send to LiveRamp.</span></span>

   > [!TIP]
   > <span data-ttu-id="3f040-123">LiveRamp erabiltzaileari gako identifikatzaile atributu gehiago bidaltzeak baliteke partidu tasa handiagoa lortzea.</span><span class="sxs-lookup"><span data-stu-id="3f040-123">Sending more key identifier attributes to LiveRamp is likely to get you a higher match rate.</span></span>

1. <span data-ttu-id="3f040-124">Hautatu LiveRamp-era esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="3f040-124">Select the segments you want to export to LiveRamp.</span></span>

1. <span data-ttu-id="3f040-125">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="3f040-125">Select **Save**.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="3f040-126">![LiveRamp konektorea atributuen mapak](media/export-liveramp-segments.png "LiveRamp konektorea atributuen mapak")</span><span class="sxs-lookup"><span data-stu-id="3f040-126">![LiveRamp connector with attribute mapping](media/export-liveramp-segments.png "LiveRamp connector with attribute mapping")</span></span>

## <a name="export-the-data"></a><span data-ttu-id="3f040-127">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="3f040-127">Export the data</span></span>

<span data-ttu-id="3f040-128">Esportazioa laster hasiko da esportaziorako baldintza guztiak bete badira.</span><span class="sxs-lookup"><span data-stu-id="3f040-128">The export will start shortly if all prerequisites for export have been completed.</span></span> <span data-ttu-id="3f040-129">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="3f040-129">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>
<span data-ttu-id="3f040-130">Esportazioa behar bezala burututa, LiveRamp Onboarding zerbitzuan saioa egin dezakezu zure datuak aktibatzeko eta banatzeko.</span><span class="sxs-lookup"><span data-stu-id="3f040-130">Once the export is successfully completed, you can sign in to LiveRamp Onboarding to activate and distribute your data.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="3f040-131">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="3f040-131">Data privacy and compliance</span></span>

<span data-ttu-id="3f040-132">Dynamics 365 Customer Insights gaitzen duzunean datuak Liveramp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="3f040-132">When you enable Dynamics 365 Customer Insights to transmit data to Liveramp, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="3f040-133">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Liveramp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="3f040-133">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Liveramp meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="3f040-134">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="3f040-134">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="3f040-135">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="3f040-135">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>