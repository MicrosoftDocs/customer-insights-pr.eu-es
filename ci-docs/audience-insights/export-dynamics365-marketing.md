---
title: Esportatu Customer Insights datuak Dynamics 365 Marketing-era
description: Ikasi Dynamics 365 Marketing konexioa nola konfiguratu.
ms.date: 02/01/2021
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: a06920b8ff25d7102ccd14ae68cf42fe91fa1ee6
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269039"
---
# <a name="connector-for-dynamics-365-marketing-preview"></a><span data-ttu-id="96d7c-103">Dynamics 365 Marketing konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="96d7c-103">Connector for Dynamics 365 Marketing (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="96d7c-104">Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="96d7c-104">Use [segments](segments.md) to generate campaigns and contact specific groups of customers with Dynamics 365 Marketing.</span></span> <span data-ttu-id="96d7c-105">Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](https://docs.microsoft.com/dynamics365/marketing/customer-insights-segments)</span><span class="sxs-lookup"><span data-stu-id="96d7c-105">For more information, see [Use segments from Dynamics 365 Customer Insights with Dynamics 365 Marketing](https://docs.microsoft.com/dynamics365/marketing/customer-insights-segments)</span></span>

## <a name="prerequisite"></a><span data-ttu-id="96d7c-106">Aurrebaldintza</span><span class="sxs-lookup"><span data-stu-id="96d7c-106">Prerequisite</span></span>

- <span data-ttu-id="96d7c-107">Kontaktu-erregistroek Dynamics 365 Marketing-en egon behar dute segmentu bat Customer Insights-etik Marketing-era esportatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="96d7c-107">Contact records must be present in Dynamics 365 Marketing before you can export a segment from Customer Insights to Marketing.</span></span> <span data-ttu-id="96d7c-108">Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Marketing erabiliz Common Data Services](connect-power-query.md).</span><span class="sxs-lookup"><span data-stu-id="96d7c-108">Read more on how to ingest contacts in [Dynamics 365 Marketing using Common Data Services](connect-power-query.md).</span></span>

  > [!NOTE]
  > <span data-ttu-id="96d7c-109">Ikuspegien estatistiketatik Marketing segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Marketing instantzietan.</span><span class="sxs-lookup"><span data-stu-id="96d7c-109">Exporting segments from audience insights to Marketing will not create new contact records in the Marketing instances.</span></span> <span data-ttu-id="96d7c-110">Marketing kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili.</span><span class="sxs-lookup"><span data-stu-id="96d7c-110">The contact records from Marketing must be ingested in audience insights and used as a data source.</span></span> <span data-ttu-id="96d7c-111">Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.</span><span class="sxs-lookup"><span data-stu-id="96d7c-111">They also need to be included in the unified Customer entity to map customer IDs to contact IDs before segments can be exported.</span></span>

## <a name="configure-the-connector-for-marketing"></a><span data-ttu-id="96d7c-112">Konfiguratu konektorea Marketinerako</span><span class="sxs-lookup"><span data-stu-id="96d7c-112">Configure the connector for Marketing</span></span>

1. <span data-ttu-id="96d7c-113">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="96d7c-113">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="96d7c-114">**Dynamics 365 Marketing** azpian hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="96d7c-114">Under **Dynamics 365 Marketing**, select **Set up**.</span></span>

1. <span data-ttu-id="96d7c-115">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="96d7c-115">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="96d7c-116">Sartu erakundearen Marketing URLa **Zerbitzariaren helbidea** eremu.</span><span class="sxs-lookup"><span data-stu-id="96d7c-116">Enter your organization's Marketing URL in the **Server address** field.</span></span>

1. <span data-ttu-id="96d7c-117">Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Marketing kontua.</span><span class="sxs-lookup"><span data-stu-id="96d7c-117">In the **Server admin account** section, select **Sign in** and choose a Dynamics 365 Marketing account.</span></span>

1. <span data-ttu-id="96d7c-118">Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="96d7c-118">Map a customer ID field to the Dynamics 365 Contact ID.</span></span>

1. <span data-ttu-id="96d7c-119">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="96d7c-119">Select **Next**.</span></span>

1. <span data-ttu-id="96d7c-120">Aukeratu segmentu bat edo gehiago.</span><span class="sxs-lookup"><span data-stu-id="96d7c-120">Choose one or more segments.</span></span>

1. <span data-ttu-id="96d7c-121">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="96d7c-121">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="96d7c-122">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="96d7c-122">Export the data</span></span>

<span data-ttu-id="96d7c-123">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="96d7c-123">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="96d7c-124">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="96d7c-124">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]