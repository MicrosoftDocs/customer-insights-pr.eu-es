---
title: Esportatu Customer Insights datuak SFTP ostalarietara
description: Ikusi nola konfiguratu konexioa SFTP ostalaria.
ms.date: 06/05/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: c2529744d7a26a06324b79cad6a8001d75903545
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643488"
---
# <a name="connector-for-sftp-preview"></a><span data-ttu-id="63e4b-103">Konektorea SFTP-rako (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="63e4b-103">Connector for SFTP (preview)</span></span>

<span data-ttu-id="63e4b-104">Erabili hirugarrenen aplikazioetako bezero-datuak horiek fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) ostalarira transferituz.</span><span class="sxs-lookup"><span data-stu-id="63e4b-104">Use your customer data in third-party applications by exporting them to a Secure File Transfer Protocol(SFTP) host.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63e4b-105">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="63e4b-105">Prerequisites</span></span>

- <span data-ttu-id="63e4b-106">SFTP ostalari baten eta dagozkien egiaztagirien eskuragarritasuna.</span><span class="sxs-lookup"><span data-stu-id="63e4b-106">Availability of a SFTP host and corresponding credentials.</span></span>

## <a name="connect-to-sftp"></a><span data-ttu-id="63e4b-107">Konektatu SFTP-ra</span><span class="sxs-lookup"><span data-stu-id="63e4b-107">Connect to SFTP</span></span>

1. <span data-ttu-id="63e4b-108">Joan **Administratzailea** > **Esportazio-helburuak** atalera.</span><span class="sxs-lookup"><span data-stu-id="63e4b-108">Go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="63e4b-109">Azpian **SFTP** hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="63e4b-109">Under **SFTP**, select **Set up**.</span></span>

1. <span data-ttu-id="63e4b-110">Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.</span><span class="sxs-lookup"><span data-stu-id="63e4b-110">Give your destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="63e4b-111">Eman SFTP kontuaren **Erabiltzaile izena**, **Pasahitza** eta **Ostalari izena**.</span><span class="sxs-lookup"><span data-stu-id="63e4b-111">Provide a **Username**, **Password** and **Hostname** for your SFTP account.</span></span> <span data-ttu-id="63e4b-112">Adibidez: zure SFTP zerbitzariaren erroko karpeta /root/folder bada eta datuak /root/folder/ci_export_destination_folder karpetara esportatzea nahi baduzu, ostalariak honakoa izan beharko luke: sftp://<server_address>/ci_export_destination_folder".</span><span class="sxs-lookup"><span data-stu-id="63e4b-112">Example: If your SFTP server's root folder is /root/folder, and you would like the data to be exported to /root/folder/ci_export_destination_folder, the the host should be sftp://<server_address>/ci_export_destination_folder".</span></span>

1. <span data-ttu-id="63e4b-113">Hautatu **Egiaztatu** konexioa probatzeko.</span><span class="sxs-lookup"><span data-stu-id="63e4b-113">Select **Verify** to test the connection.</span></span>

1. <span data-ttu-id="63e4b-114">Egiaztatu ondoren, aukeratu zure datuak esportatu nahi dituzun **konprimitutako** edo **konprimitu gabea** eta hautatu **eremuaren mugatzailea** esportatutako fitxategietarako.</span><span class="sxs-lookup"><span data-stu-id="63e4b-114">After successful verification, choose if you want to export your data **Zipped** or **Unzipped**, and select the **field delimiter** for the exported files.</span></span>

1. <span data-ttu-id="63e4b-115">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="63e4b-115">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="63e4b-116">Aukeratu **hurrengoa** esportazioa konfiguratzen hasteko.</span><span class="sxs-lookup"><span data-stu-id="63e4b-116">Select **Next** to start configuring the export.</span></span>

## <a name="configure-the-connection"></a><span data-ttu-id="63e4b-117">Konfiguratu konexioa</span><span class="sxs-lookup"><span data-stu-id="63e4b-117">Configure the connection</span></span>

1. <span data-ttu-id="63e4b-118">Hautatu **bezeroaren atributuak** esportatu nahi dituzunak.</span><span class="sxs-lookup"><span data-stu-id="63e4b-118">Select the **customer attributes** you want to export.</span></span> <span data-ttu-id="63e4b-119">Ezaugarri bat edo gehiago esporta ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="63e4b-119">You can export one or multiple attributes.</span></span>

1. <span data-ttu-id="63e4b-120">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="63e4b-120">Select **Next**.</span></span>

1. <span data-ttu-id="63e4b-121">Hautatu esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="63e4b-121">Select the segments you want to export.</span></span>

1. <span data-ttu-id="63e4b-122">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="63e4b-122">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="63e4b-123">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="63e4b-123">Export the data</span></span>

<span data-ttu-id="63e4b-124">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="63e4b-124">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="63e4b-125">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="63e4b-125">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="63e4b-126">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="63e4b-126">Data privacy and compliance</span></span>

<span data-ttu-id="63e4b-127">Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="63e4b-127">When you enable Dynamics 365 Customer Insights to transmit data via SFTP, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="63e4b-128">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="63e4b-128">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that the export destination meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="63e4b-129">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="63e4b-129">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="63e4b-130">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="63e4b-130">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>
