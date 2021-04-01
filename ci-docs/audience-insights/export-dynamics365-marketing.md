---
title: Esportatu Customer Insights datuak Dynamics 365 Marketing-era
description: Ikasi Dynamics 365 Marketing konexioa nola konfiguratu.
ms.date: 02/01/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 892aff643872f11307a2c43e5670edab657d7848
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597588"
---
# <a name="connector-for-dynamics-365-marketing-preview"></a><span data-ttu-id="ac221-103">Dynamics 365 Marketing konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="ac221-103">Connector for Dynamics 365 Marketing (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="ac221-104">Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="ac221-104">Use [segments](segments.md) to generate campaigns and contact specific groups of customers with Dynamics 365 Marketing.</span></span> <span data-ttu-id="ac221-105">Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments)</span><span class="sxs-lookup"><span data-stu-id="ac221-105">For more information, see [Use segments from Dynamics 365 Customer Insights with Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments)</span></span>

## <a name="prerequisite"></a><span data-ttu-id="ac221-106">Aurrebaldintza</span><span class="sxs-lookup"><span data-stu-id="ac221-106">Prerequisite</span></span>

- <span data-ttu-id="ac221-107">Kontaktu-erregistroek Dynamics 365 Marketing-en egon behar dute segmentu bat Customer Insights-etik Marketing-era esportatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="ac221-107">Contact records must be present in Dynamics 365 Marketing before you can export a segment from Customer Insights to Marketing.</span></span> <span data-ttu-id="ac221-108">Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Marketing erabiliz Common Data Services](connect-power-query.md).</span><span class="sxs-lookup"><span data-stu-id="ac221-108">Read more on how to ingest contacts in [Dynamics 365 Marketing using Common Data Services](connect-power-query.md).</span></span>

  > [!NOTE]
  > <span data-ttu-id="ac221-109">Ikuspegien estatistiketatik Marketing segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Marketing instantzietan.</span><span class="sxs-lookup"><span data-stu-id="ac221-109">Exporting segments from audience insights to Marketing will not create new contact records in the Marketing instances.</span></span> <span data-ttu-id="ac221-110">Marketing kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili.</span><span class="sxs-lookup"><span data-stu-id="ac221-110">The contact records from Marketing must be ingested in audience insights and used as a data source.</span></span> <span data-ttu-id="ac221-111">Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.</span><span class="sxs-lookup"><span data-stu-id="ac221-111">They also need to be included in the unified Customer entity to map customer IDs to contact IDs before segments can be exported.</span></span>

## <a name="configure-the-connector-for-marketing"></a><span data-ttu-id="ac221-112">Konfiguratu konektorea Marketinerako</span><span class="sxs-lookup"><span data-stu-id="ac221-112">Configure the connector for Marketing</span></span>

1. <span data-ttu-id="ac221-113">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="ac221-113">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="ac221-114">**Dynamics 365 Marketing** azpian hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="ac221-114">Under **Dynamics 365 Marketing**, select **Set up**.</span></span>

1. <span data-ttu-id="ac221-115">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="ac221-115">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="ac221-116">Sartu erakundearen Marketing URLa **Zerbitzariaren helbidea** eremu.</span><span class="sxs-lookup"><span data-stu-id="ac221-116">Enter your organization's Marketing URL in the **Server address** field.</span></span>

1. <span data-ttu-id="ac221-117">Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Marketing kontua.</span><span class="sxs-lookup"><span data-stu-id="ac221-117">In the **Server admin account** section, select **Sign in** and choose a Dynamics 365 Marketing account.</span></span>

1. <span data-ttu-id="ac221-118">Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="ac221-118">Map a customer ID field to the Dynamics 365 Contact ID.</span></span>

1. <span data-ttu-id="ac221-119">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="ac221-119">Select **Next**.</span></span>

1. <span data-ttu-id="ac221-120">Aukeratu segmentu bat edo gehiago.</span><span class="sxs-lookup"><span data-stu-id="ac221-120">Choose one or more segments.</span></span>

1. <span data-ttu-id="ac221-121">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="ac221-121">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="ac221-122">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="ac221-122">Export the data</span></span>

<span data-ttu-id="ac221-123">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="ac221-123">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="ac221-124">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="ac221-124">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]