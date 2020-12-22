---
title: Esportatu Customer Insights datuak Facebook iragarki-kudeatzailera
description: Ikusi nola konfiguratu konexioa Facebook Iragarkien kudeatzailea.
ms.date: 06/05/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 8260e3b5e529f3d54678d9d6e11aebb2795e27fd
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643668"
---
# <a name="connector-for-facebook-ads-manager-preview"></a><span data-ttu-id="e9f2e-103">Konektatzailea Facebook Iragarkien kudeatzailea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="e9f2e-103">Connector for Facebook Ads Manager (preview)</span></span>

<span data-ttu-id="e9f2e-104">Bezeroen profil bateratuen segmentuak esportatu Facebook Iragarkien kudeatzailea kanpainak sortzeko Facebook eta Instagram.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-104">Export segments of unified customer profiles to Facebook Ads Manager to create campaigns on Facebook and Instagram.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e9f2e-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="e9f2e-105">Prerequisites</span></span>

- <span data-ttu-id="e9f2e-106">[**Facebook Iragarkien kontua**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) eduki behar duzu, zeinak [**Facebook negozio-kontu**](https://business.facebook.com/) bat barne hartzen duen.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-106">You need to have a [**Facebook Ad Account**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) which includes a [**Facebook Business Account**](https://business.facebook.com/).</span></span>
- <span data-ttu-id="e9f2e-107">[**Facebook Iragarkien kontuaren**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) administratzaile izan behar duzu.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-107">You need to be an administrator on the [**Facebook Ad Account**](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account).</span></span>

## <a name="connect-to-facebook-ads-manager"></a><span data-ttu-id="e9f2e-108">Konektatu Facebook Iragarkien kudeatzailea</span><span class="sxs-lookup"><span data-stu-id="e9f2e-108">Connect to Facebook Ads Manager</span></span>

1. <span data-ttu-id="e9f2e-109">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-109">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="e9f2e-110">Azpian **Facebook Iragarkien kudeatzailea** hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-110">Under **Facebook Ads Manager**, select **Set up**.</span></span>

1. <span data-ttu-id="e9f2e-111">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-111">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="e9f2e-112">Aukeratu **Jarraitu aurrera Facebook** saioa hasteko Facebook Iragarkien kontua.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-112">Select **Continue with Facebook** to sign in to your Facebook Ad Account.</span></span>

1. <span data-ttu-id="e9f2e-113">Onartu **iragarkien kudeaketa** baimena, Facebook-ekin autentifikatu ondoren.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-113">Allow the **ads_management** permission after authenticating with Facebook.</span></span>

1. <span data-ttu-id="e9f2e-114">Hautatu **Facebook iragarki kontua** lan egin nahi duzunarekin.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-114">Select the **Facebook Ads Account** that you want to work with.</span></span>

1. <span data-ttu-id="e9f2e-115">Aukeratu bat **Existitzen den audientzia pertsonalizatua** goitibeherako zerrendatik edo sortu bat **Ohiko audientzia berriak**.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-115">Select an **Existing custom audience** from the drop-down list or create a **New custom audience**.</span></span> <span data-ttu-id="e9f2e-116">Informazio gehiago lortzeko, ikus [**Ikusleak Facebook Iragarkien kudeatzailea**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).</span><span class="sxs-lookup"><span data-stu-id="e9f2e-116">For more information, see [**Audiences in Facebook Ads Manager**](https://www.facebook.com/business/help/744354708981227?id=2469097953376494).</span></span>

1. <span data-ttu-id="e9f2e-117">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-117">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="e9f2e-118">Aukeratu **hurrengoa** esportazioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-118">Select **Next** to configure the export.</span></span>

## <a name="configure-the-connector"></a><span data-ttu-id="e9f2e-119">Konfiguratu konektorea</span><span class="sxs-lookup"><span data-stu-id="e9f2e-119">Configure the connector</span></span>

1. <span data-ttu-id="e9f2e-120">Sarbidean **Aukeratu zure gako identifikatzaileen eremua** hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** bidali Facebook Iragarkien kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-120">In the **Choose your key identifier field**, select **Email**, **Name and address**, or **Phone** to send to Facebook Ads Manager.</span></span>

1. <span data-ttu-id="e9f2e-121">Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-121">Map the corresponding attributes from your unified customer entity for the selected key identifier.</span></span>
   > <span data-ttu-id="e9f2e-122">[AHOLKULUA] Partidua lortzeko aukera onenak hautatuta baldin badaude **Emaila** gako identifikatzaile gisa.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-122">[TIP] The best chances for a match occur if you select **Email** as key identifier.</span></span> <span data-ttu-id="e9f2e-123">Identifikatzaile osagarriak gehitzeak bat egin dezake.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-123">Adding additional identifiers may improve the matching.</span></span>

1. <span data-ttu-id="e9f2e-124">Aukeratu **Gehitu atributua** bidali beharreko atributu osagarriak mapatzeko Facebook Iragarkien kudeatzailea.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-124">Select **Add attribute** to map additional attributes to send to Facebook Ads Manager.</span></span> <span data-ttu-id="e9f2e-125">Atributuak Facebook Iragarkien kudeatzailea erabiltzaileentzako lagunarteko izen hauek kokatzen dira: **FN** = **izena**, **LN** = **abizena**, **FI** = **Lehen Hasierakoa**, **TELEFONOA** = **Telefonoa**, **GEN** = **Generoa**, **DOB** = **Jaioteguna**, **ST** = **Estatu**, **CT** = **hiria**, **ZIP** = **Posta kodea / zip kodea**, **HERRIALDEA** = **Herrialdea / Eskualdea**</span><span class="sxs-lookup"><span data-stu-id="e9f2e-125">Attributes from Facebook Ads Manager are mapping to the following user friendly names: **FN** = **First Name**, **LN** = **Last Name**, **FI** = **First Initial**, **PHONE** = **Phone**, **GEN** = **Gender**, **DOB** = **Date of birth**, **ST** = **State**, **CT** = **City**, **ZIP** = **Postal code / Zip code**, **COUNTRY** = **Country / Region**</span></span>

1. <span data-ttu-id="e9f2e-126">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-126">Select the segments you want to export.</span></span>

1. <span data-ttu-id="e9f2e-127">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-127">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="e9f2e-128">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="e9f2e-128">Export the data</span></span>

<span data-ttu-id="e9f2e-129">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="e9f2e-129">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="e9f2e-130">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="e9f2e-130">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="e9f2e-131">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="e9f2e-131">Data privacy and compliance</span></span>

<span data-ttu-id="e9f2e-132">Dynamics 365 Customer Insights gaitzen duzunean datuak  Facebook-en iragarki-kudeatzailera bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-132">When you enable Dynamics 365 Customer Insights to transmit data to Facebook Ads Manager, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="e9f2e-133">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Facebook iragarkiek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-133">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Facebook Ads meet any privacy or security obligations you may have.</span></span> <span data-ttu-id="e9f2e-134">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="e9f2e-134">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="e9f2e-135">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="e9f2e-135">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
