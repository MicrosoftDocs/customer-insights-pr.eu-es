---
title: Esportatu Customer Insights datuak SFTP ostalarietara
description: Ikusi nola konfiguratu konexioa SFTP ostalaria.
ms.date: 01/27/2021
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: ddba55b3ca159c0095371e46385dcf1d3ed4a63d
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267983"
---
# <a name="connector-for-sftp-preview"></a><span data-ttu-id="9e71d-103">Konektorea SFTP-rako (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="9e71d-103">Connector for SFTP (preview)</span></span>

<span data-ttu-id="9e71d-104">Erabili hirugarrenen aplikazioetako bezero-datuak horiek fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) ostalarira transferituz.</span><span class="sxs-lookup"><span data-stu-id="9e71d-104">Use your customer data in third-party applications by exporting them to a Secure File Transfer Protocol (SFTP) host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9e71d-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="9e71d-105">Prerequisites</span></span>

- <span data-ttu-id="9e71d-106">SFTP ostalariaren erabilgarritasuna eta dagozkien egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="9e71d-106">Availability of an SFTP host and corresponding credentials.</span></span>

## <a name="connect-to-sftp"></a><span data-ttu-id="9e71d-107">Konektatu SFTP-ra</span><span class="sxs-lookup"><span data-stu-id="9e71d-107">Connect to SFTP</span></span>

1. <span data-ttu-id="9e71d-108">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="9e71d-108">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="9e71d-109">Azpian **SFTP** hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="9e71d-109">Under **SFTP**, select **Set up**.</span></span>

1. <span data-ttu-id="9e71d-110">Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.</span><span class="sxs-lookup"><span data-stu-id="9e71d-110">Give your destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="9e71d-111">Eman SFTP kontuaren **Erabiltzaile-izena**, **Pasahitza**, **Ostalari-izena** eta **Esportazio-karpeta**.</span><span class="sxs-lookup"><span data-stu-id="9e71d-111">Provide a **Username**, **Password**, **Hostname**, and **Export folder** for your SFTP account.</span></span>

1. <span data-ttu-id="9e71d-112">Hautatu **Egiaztatu** konexioa probatzeko.</span><span class="sxs-lookup"><span data-stu-id="9e71d-112">Select **Verify** to test the connection.</span></span>

1. <span data-ttu-id="9e71d-113">Egiaztatu ondoren, aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimitu gabe**, eta hautatu **eremu-mugatzailea** esportatutako fitxategietarako.</span><span class="sxs-lookup"><span data-stu-id="9e71d-113">After successful verification, choose if you want to export your data **Gzipped** or **Unzipped**, and select the **field delimiter** for the exported files.</span></span>

1. <span data-ttu-id="9e71d-114">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="9e71d-114">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="9e71d-115">Aukeratu **hurrengoa** esportazioa konfiguratzen hasteko.</span><span class="sxs-lookup"><span data-stu-id="9e71d-115">Select **Next** to start configuring the export.</span></span>

## <a name="configure-the-export"></a><span data-ttu-id="9e71d-116">Konfiguratu esportazioa</span><span class="sxs-lookup"><span data-stu-id="9e71d-116">Configure the export</span></span>

1. <span data-ttu-id="9e71d-117">Aukeratu entitateak, adibidez, esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="9e71d-117">Select the entities, for example segments, you want to export.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9e71d-118">Aukeratutako entitate bakoitzak gehienez bost irteera fitxategi izango ditu esportatzean.</span><span class="sxs-lookup"><span data-stu-id="9e71d-118">Each selected entity will be up to five output files when exported.</span></span> 

1. <span data-ttu-id="9e71d-119">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="9e71d-119">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="9e71d-120">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="9e71d-120">Export the data</span></span>

<span data-ttu-id="9e71d-121">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="9e71d-121">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="9e71d-122">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="9e71d-122">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>

## <a name="known-limitations"></a><span data-ttu-id="9e71d-123">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="9e71d-123">Known limitations</span></span>

- <span data-ttu-id="9e71d-124">Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="9e71d-124">The runtime of an export depends on your system performance.</span></span> <span data-ttu-id="9e71d-125">Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa.</span><span class="sxs-lookup"><span data-stu-id="9e71d-125">We recommend two CPU cores and 1 Gb of memory as minimal configuration of your server.</span></span> 
- <span data-ttu-id="9e71d-126">Gehienez 100 milioi bezero profil dituzten entitate esportatzaileek 90 minutu iraun dezakete gomendatutako gutxieneko konfigurazioa erabiltzen duten bi PUZ nukleorekin eta 1 Gb memoria.</span><span class="sxs-lookup"><span data-stu-id="9e71d-126">Exporting entities with up to 100 million customer profiles can take 90 minutes when using the recommended minimal configuration of two CPU cores and 1 Gb of memory.</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="9e71d-127">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="9e71d-127">Data privacy and compliance</span></span>

<span data-ttu-id="9e71d-128">Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="9e71d-128">When you enable Dynamics 365 Customer Insights to transmit data via SFTP, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="9e71d-129">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="9e71d-129">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that the export destination meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="9e71d-130">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="9e71d-130">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="9e71d-131">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="9e71d-131">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]