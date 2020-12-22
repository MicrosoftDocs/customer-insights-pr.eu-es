---
title: Esportatu Customer Insights datuak Dynamics 365 Marketing-era
description: Ikasi Dynamics 365 Marketing konexioa nola konfiguratu.
ms.date: 08/21/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 163387779b64bd78ef08e2d96a5f1c9615062f28
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643758"
---
# <a name="connector-for-dynamics-365-marketing-preview"></a><span data-ttu-id="213e0-103">Dynamics 365 Marketing konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="213e0-103">Connector for Dynamics 365 Marketing (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="213e0-104">Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="213e0-104">Use [segments](segments.md) to generate campaigns and contact specific groups of customers with Dynamics 365 Marketing.</span></span> <span data-ttu-id="213e0-105">Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](https://docs.microsoft.com/dynamics365/marketing/customer-insights-segments)</span><span class="sxs-lookup"><span data-stu-id="213e0-105">For more information, see [Use segments from Dynamics 365 Customer Insights with Dynamics 365 Marketing](https://docs.microsoft.com/dynamics365/marketing/customer-insights-segments)</span></span>

## <a name="prerequisite"></a><span data-ttu-id="213e0-106">Aurrebaldintza</span><span class="sxs-lookup"><span data-stu-id="213e0-106">Prerequisite</span></span>

<span data-ttu-id="213e0-107">[Common Data Service-n sartutako Dynamics 365 Marketing-eko](connect-power-query.md) kontaktuen erregistroak.</span><span class="sxs-lookup"><span data-stu-id="213e0-107">Contact records [from Dynamics 365 Marketing ingested Common Data Service](connect-power-query.md).</span></span>

## <a name="configure-the-connector-for-marketing"></a><span data-ttu-id="213e0-108">Konfiguratu konektorea Marketinerako</span><span class="sxs-lookup"><span data-stu-id="213e0-108">Configure the connector for Marketing</span></span>

1. <span data-ttu-id="213e0-109">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="213e0-109">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="213e0-110">**Dynamics 365 Marketing** azpian hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="213e0-110">Under **Dynamics 365 Marketing**, select **Set up**.</span></span>

1. <span data-ttu-id="213e0-111">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="213e0-111">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="213e0-112">Sartu erakundearen Marketing URLa **Zerbitzariaren helbidea** eremu.</span><span class="sxs-lookup"><span data-stu-id="213e0-112">Enter your organization's Marketing URL in the **Server address** field.</span></span>

1. <span data-ttu-id="213e0-113">Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Marketing kontua.</span><span class="sxs-lookup"><span data-stu-id="213e0-113">In the **Server admin account** section, select **Sign in** and choose a Dynamics 365 Marketing account.</span></span>

1. <span data-ttu-id="213e0-114">Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="213e0-114">Map a customer ID field to the Dynamics 365 Contact ID.</span></span>

1. <span data-ttu-id="213e0-115">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="213e0-115">Select **Next**.</span></span>

1. <span data-ttu-id="213e0-116">Aukeratu segmentu bat edo gehiago.</span><span class="sxs-lookup"><span data-stu-id="213e0-116">Choose one or more segments.</span></span>

1. <span data-ttu-id="213e0-117">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="213e0-117">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="213e0-118">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="213e0-118">Export the data</span></span>

<span data-ttu-id="213e0-119">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="213e0-119">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="213e0-120">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="213e0-120">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>
