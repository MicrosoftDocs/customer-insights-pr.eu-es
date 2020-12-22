---
title: Esportatu Customer Insights datuak Dynamics 365 Sales-era
description: Ikasi Dynamics 365 Sales konexioa nola konfiguratu.
ms.date: 08/21/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: af0824e69dfdf620a0ac756e32a9bd3dd85e5151
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643803"
---
# <a name="connector-for-dynamics-365-sales-preview"></a><span data-ttu-id="d46dd-103">Dynamics 365 Sales konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="d46dd-103">Connector for Dynamics 365 Sales (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="d46dd-104">Dynamics 365 Sales-ekin marketin-zerrendak sortzeko, lan-fluxuen segimendua egiteko eta eskaintzak bidaltzeko, erabili bezeroen datuak.</span><span class="sxs-lookup"><span data-stu-id="d46dd-104">Use your customer data to create marketing lists, follow up workflows, and send out promotions with Dynamics 365 Sales.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="d46dd-105">Aurrebaldintza</span><span class="sxs-lookup"><span data-stu-id="d46dd-105">Prerequisite</span></span>

<span data-ttu-id="d46dd-106">[Common Data Service erabiliz sartutako Dynamics 365 Sales-eko](connect-power-query.md) kontaktuen erregistroak.</span><span class="sxs-lookup"><span data-stu-id="d46dd-106">Contact records [from Dynamics 365 Sales ingested using Common Data Service](connect-power-query.md).</span></span>

## <a name="configure-the-connector-for-sales"></a><span data-ttu-id="d46dd-107">Konfiguratu konektorea Sales-erako</span><span class="sxs-lookup"><span data-stu-id="d46dd-107">Configure the connector for Sales</span></span>

1. <span data-ttu-id="d46dd-108">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="d46dd-108">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="d46dd-109">**Dynamics 365 Sales** azpian hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="d46dd-109">Under **Dynamics 365 Sales**, select **Set up**.</span></span>

1. <span data-ttu-id="d46dd-110">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="d46dd-110">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="d46dd-111">Sartu erakundearen Salmentako URLa **Zerbitzariaren helbidea** eremu.</span><span class="sxs-lookup"><span data-stu-id="d46dd-111">Enter your organization's Sales URL in the **Server address** field.</span></span>

1. <span data-ttu-id="d46dd-112">Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Sales kontua.</span><span class="sxs-lookup"><span data-stu-id="d46dd-112">In the **Server admin account** section, select **Sign in** and choose a Dynamics 365 Sales account.</span></span>

1. <span data-ttu-id="d46dd-113">Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="d46dd-113">Map a customer ID field to the Dynamics 365 Contact ID.</span></span>

1. <span data-ttu-id="d46dd-114">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="d46dd-114">Select **Next**.</span></span>

1. <span data-ttu-id="d46dd-115">Aukeratu segmentu bat edo gehiago.</span><span class="sxs-lookup"><span data-stu-id="d46dd-115">Choose one or more segments.</span></span>

1. <span data-ttu-id="d46dd-116">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="d46dd-116">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="d46dd-117">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="d46dd-117">Export the data</span></span>

<span data-ttu-id="d46dd-118">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="d46dd-118">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="d46dd-119">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="d46dd-119">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>
