---
title: Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian | Microsoft Docs
description: Erantzun Dynamics 365 Customer Insights hartzaileen xehetasunen gaitasunaren datuen jabearen eskaerei.
ms.date: 05/14/2020
ms.reviewer: wimohabb
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: ed9aa09fba938606611c6ce86c2b250c5e19c606
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5268671"
---
# <a name="data-subject-rights-dsr-requests-under-gdpr"></a><span data-ttu-id="c0ec4-103">Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian</span><span class="sxs-lookup"><span data-stu-id="c0ec4-103">Data Subject Rights (DSR) requests under GDPR</span></span>

## <a name="responding-to-gdpr-data-subject-delete-requests-for-dynamics-365-customer-insights-audience-insights-capability"></a><span data-ttu-id="c0ec4-104">Erantzun Dynamics 365 Customer Insights hartzaileen xehetasunen gaitasunaren DBAO datuen jabearen ezabatze-eskaerei</span><span class="sxs-lookup"><span data-stu-id="c0ec4-104">Responding to GDPR data subject delete requests for Dynamics 365 Customer Insights audience insights capability</span></span>

<span data-ttu-id="c0ec4-105">Erakunde baten bezeroen datu pertsonalak ezabatzeko eskubidea funtsezko babesa da Datuak Babesteko Araudi Orokorrean (DBAO).</span><span class="sxs-lookup"><span data-stu-id="c0ec4-105">The “right to erasure” by the removal of personal data from an organization’s customer data is a key protection in the General Data Protection Regulation (GDPR).</span></span> <span data-ttu-id="c0ec4-106">Datu pertsonalak kentzea barne hartzen ditu datu pertsonal guztiak eta sistemak sortutako erregistroak kentzea, ikuskapenen egunkari informazioa izan ezik.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-106">Removing personal data includes removing all personal data and system-generated logs, except audit log information.</span></span>

### <a name="manage-data-subject-delete-requests"></a><span data-ttu-id="c0ec4-107">Kudeatu datuen gaia ezabatzeko eskaerak</span><span class="sxs-lookup"><span data-stu-id="c0ec4-107">Manage data subject delete requests</span></span>

<span data-ttu-id="c0ec4-108">Hartzaileen xehetasunek bezero jakin baten edo erabiltzailearen datu pertsonalak ezabatzeko honako produktuak eskaintzen dituen esperientzia eskaintzen du:</span><span class="sxs-lookup"><span data-stu-id="c0ec4-108">Audience insights offers the following in-product experiences to delete personal data for a specific customer or user:</span></span>

- <span data-ttu-id="c0ec4-109">**Kudeatu bezeroen datuak eskatzeko ezabatu**: Customer Insights-en bezeroen datuak Customer Insights-en kanpoko jatorrizko datu iturrietatik ateratzen dira.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-109">**Manage delete requests for customer data**: Customer data in Customer Insights is ingested from original data sources external to Customer Insights.</span></span> <span data-ttu-id="c0ec4-110">DBAO ezabatzeko eskaera guztiak jatorrizko datu-iturburu-en egin behar dira.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-110">All GDPR delete requests must be performed in the original data source.</span></span>
- <span data-ttu-id="c0ec4-111">**Kudeatu Customer Insights-eko erabiltzailearen datuak ezabatzeko eskaerak**: Erabiltzaileen datuak Customer Insights-ek sortzen ditu.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-111">**Manage delete requests for Customer Insights user data**: Data for users is created by Customer Insights.</span></span> <span data-ttu-id="c0ec4-112">DBAO ezabatzeko eskaera guztiak Customer Insights zerbitzuan egin behar dira.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-112">All GDPR delete requests must be performed in Customer Insights.</span></span>

#### <a name="manage-delete-requests-for-customer-data"></a><span data-ttu-id="c0ec4-113">Kudeatu bezeroen datuak eskatzeko ezabatu</span><span class="sxs-lookup"><span data-stu-id="c0ec4-113">Manage delete requests for customer data</span></span>

<span data-ttu-id="c0ec4-114">Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake datu-iturburu-en ezabatu diren bezeroen datuak kentzeko:</span><span class="sxs-lookup"><span data-stu-id="c0ec4-114">A Customer Insights admin can follow these steps to remove customer data that was deleted in the data source:</span></span>

1. <span data-ttu-id="c0ec4-115">Hasi saioa Dynamics 365 Customer Insights aplikazioan.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-115">Sign in to Dynamics 365 Customer Insights.</span></span>
2. <span data-ttu-id="c0ec4-116">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**</span><span class="sxs-lookup"><span data-stu-id="c0ec4-116">In audience insights, go to **Data** > **Data sources**</span></span>
3. <span data-ttu-id="c0ec4-117">Ezabatutako bezeroen datuak biltzen dituen zerrendan datu-iturburu bakoitzeko:</span><span class="sxs-lookup"><span data-stu-id="c0ec4-117">For each data source in the list that contains deleted customer data:</span></span>
   1. <span data-ttu-id="c0ec4-118">Hautatu (...) eta ondoren, hautatu **Freskatu**.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-118">Select (...) and then select **Refresh**.</span></span>
   2. <span data-ttu-id="c0ec4-119">Begiratu datu-iturburu azpian **Egoera**.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-119">Check the status of the data source under **Status**.</span></span> <span data-ttu-id="c0ec4-120">Marka egiaztatzeak freskagarria izan dela esan nahi du.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-120">A check mark means the refresh was successful.</span></span> <span data-ttu-id="c0ec4-121">Abisu triangelu batek zerbait gaizki joan dela esan nahi du.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-121">A warning triangle means something went wrong.</span></span> <span data-ttu-id="c0ec4-122">Abisu triangelua bistaratzen bada, jarri harremanetan D365CI@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-122">If a warning triangle is displayed, contact D365CI@microsoft.com.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c0ec4-123">![DBAO tratamendua bezeroen datuak eskatzeko ezabatu](media/gdpr-data-sources.png "DBAO tratamendua bezeroen datuak eskatzeko ezabatu")</span><span class="sxs-lookup"><span data-stu-id="c0ec4-123">![Handling GDPR delete requests for customer data](media/gdpr-data-sources.png "Handling GDPR delete requests for customer data")</span></span>

#### <a name="manage-delete-requests-for-user-data"></a><span data-ttu-id="c0ec4-124">Kudeatu erabiltzailearen datuak ezabatzeko eskaerak</span><span class="sxs-lookup"><span data-stu-id="c0ec4-124">Manage delete requests for user data</span></span>

<span data-ttu-id="c0ec4-125">Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake Customer Insights erabiltzailearen datuak ezabatzeko:</span><span class="sxs-lookup"><span data-stu-id="c0ec4-125">A Customer Insights admin can follow these steps to delete Customer Insights user data:</span></span>

1. <span data-ttu-id="c0ec4-126">Hasi saioa Dynamics 365 Customer Insights aplikazioan.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-126">Sign in to Dynamics 365 Customer Insights.</span></span>
2. <span data-ttu-id="c0ec4-127">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Baimenak**.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-127">In audience insights, go to **Admin** > **Permissions**.</span></span>
3. <span data-ttu-id="c0ec4-128">Hautatu ezabatu nahi dituzun erabiltzailearen kontrol-laukiak.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-128">Select the check box for the user you want to delete.</span></span>
4. <span data-ttu-id="c0ec4-129">Hautatu **Kendu**.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-129">Select **Remove**.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="c0ec4-130">![Kudeatu erabiltzailearen datuen DBAO ezabatzeko eskaerak](media/gdpr-permissions.png "Kudeatu erabiltzailearen datuen DBAO ezabatzeko eskaerak")</span><span class="sxs-lookup"><span data-stu-id="c0ec4-130">![Handling GDPR delete requests foruser data](media/gdpr-permissions.png "Handling GDPR delete requests for user data")</span></span>

## <a name="responding-to-gdpr-data-subject-export-requests"></a><span data-ttu-id="c0ec4-131">DBAO datuen subjektuaren esportazio-eskaerei erantzutea</span><span class="sxs-lookup"><span data-stu-id="c0ec4-131">Responding to GDPR data subject export requests</span></span>

<span data-ttu-id="c0ec4-132">Datuak Babesteko Araudi Orokorra (DBAO) bidaian zurekin lotzeko konpromisoaren zati gisa, prestatzen laguntzeko dokumentazioa garatu dugu.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-132">As part of our commitment to partner with you on your journey to the General Data Protection Regulation (GDPR), we’ve developed documentation to help you prepare.</span></span> <span data-ttu-id="c0ec4-133">Dokumentazio honetan, hartzaileen xehetasunak erabiltzean DBAO betetzea sustatzeko har ditzakezun urratsak deskribatzen dira.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-133">This documentation describes steps you can take today to support GDPR compliance when using audience insights.</span></span>

### <a name="manage-export-and-view-requests"></a><span data-ttu-id="c0ec4-134">Kudeatu esportazio eta ikusteko eskaerak</span><span class="sxs-lookup"><span data-stu-id="c0ec4-134">Manage export and view requests</span></span>

<span data-ttu-id="c0ec4-135">Datuen eramangarritasun-eskubideari esker, pertsona baten datu pertsonalen kopia eska daiteke formatu elektroniko batean ("kontrolatutako egitura, normalean erabilitakoa, makina irakurgarria eta elkarrekin egingarria") beste datu kontroladore bati transmititu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-135">The right of data portability allows data subjects to request a copy of their personal data in an electronic format (a “structured, commonly used, machine readable, and interoperable format”) that can be transmitted to another data controller.</span></span>

#### <a name="export-customer-data-tenant-admin"></a><span data-ttu-id="c0ec4-136">Esportatu bezeroen datuak - Beste batzuk (maizterraren kudeatzailea)</span><span class="sxs-lookup"><span data-stu-id="c0ec4-136">Export customer data (tenant admin)</span></span>

<span data-ttu-id="c0ec4-137">Maizter administratzaileak urrats hauek jarraitzen ditu datuak esportatzeko:</span><span class="sxs-lookup"><span data-stu-id="c0ec4-137">A tenant administrator can follow these steps to export data:</span></span>

1. <span data-ttu-id="c0ec4-138">Bidali mezu elektroniko bat helbidera D365CI@microsoft.com bezeroaren helbide elektronikoa eskaeran zehaztuz.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-138">Send an email to D365CI@microsoft.com specifying the customer’s email address in the request.</span></span> <span data-ttu-id="c0ec4-139">Customer Insights taldeak mezu elektroniko bat bidaliko du erregistratutako maizter kudeatzaileko helbide elektronikora, datuak esportatzeko berrespena eskatuko du.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-139">The Customer Insights team will send an email to the registered tenant admin email address, asking for confirmation to export data.</span></span>
2. <span data-ttu-id="c0ec4-140">Onartu eskatutako bezeroari datuak esportatzeko baieztapena.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-140">Acknowledge the confirmation to export the data for the requested customer.</span></span>
3. <span data-ttu-id="c0ec4-141">Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-141">Receive the exported data through the tenant admin email address.</span></span>

#### <a name="export-user-data-tenant-admin"></a><span data-ttu-id="c0ec4-142">Esportatu erabiltzailearen datuak (maizterraren kudeatzailea)</span><span class="sxs-lookup"><span data-stu-id="c0ec4-142">Export user data (tenant admin)</span></span>

1. <span data-ttu-id="c0ec4-143">Bidali mezu elektroniko bat helbidera D365CI@microsoft.com erabiltzailearen helbide elektronikoa eskaeran zehaztuz.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-143">Send an email to D365CI@microsoft.com specifying the user’s email address in the request.</span></span> <span data-ttu-id="c0ec4-144">Customer Insights taldeak mezu elektroniko bat bidaliko du erregistratutako maizter kudeatzaileko helbide elektronikora, datuak esportatzeko berrespena eskatuko du.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-144">The Customer Insights team will send an email to the registered tenant admin email address, asking for confirmation to export data.</span></span>
2. <span data-ttu-id="c0ec4-145">Onartu eskatutako erabiltzailearen datuak esportatzeko baieztapena.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-145">Acknowledge the confirmation to export the data for the requested user.</span></span>
3. <span data-ttu-id="c0ec4-146">Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.</span><span class="sxs-lookup"><span data-stu-id="c0ec4-146">Receive the exported data through the tenant admin email address.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]