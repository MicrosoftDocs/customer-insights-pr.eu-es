---
title: Esportatu Customer Insights datuak Dynamics 365 Sales-era
description: Ikasi Dynamics 365 Sales konexioa nola konfiguratu.
ms.date: 02/01/2021
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 0013c4e6a96401d6cdbea55ed38f85f5e10dcc56
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5268993"
---
# <a name="connector-for-dynamics-365-sales-preview"></a><span data-ttu-id="5b5ba-103">Dynamics 365 Sales konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="5b5ba-103">Connector for Dynamics 365 Sales (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="5b5ba-104">Dynamics 365 Sales-ekin marketin-zerrendak sortzeko, lan-fluxuen segimendua egiteko eta eskaintzak bidaltzeko, erabili bezeroen datuak.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-104">Use your customer data to create marketing lists, follow up workflows, and send out promotions with Dynamics 365 Sales.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="5b5ba-105">Aurrebaldintza</span><span class="sxs-lookup"><span data-stu-id="5b5ba-105">Prerequisite</span></span>

1. <span data-ttu-id="5b5ba-106">Kontaktu-erregistroek Dynamics 365 Sales-en egon behar dute segmentu bat Customer Insights-etik Sales-era esportatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-106">Contact records must be present in Dynamics 365 Sales before you can export a segment from Customer Insights to Sales.</span></span> <span data-ttu-id="5b5ba-107">Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Sales erabiliz Common Data Services](connect-power-query.md).</span><span class="sxs-lookup"><span data-stu-id="5b5ba-107">Read more on how to ingest contacts in [Dynamics 365 Sales using Common Data Services](connect-power-query.md).</span></span>

   > [!NOTE]
   > <span data-ttu-id="5b5ba-108">Ikuspegien estatistiketatik salmentetara segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Sales instantzietan.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-108">Exporting segments from audience insights to Sales will not create new contact records in the Sales instances.</span></span> <span data-ttu-id="5b5ba-109">Sales kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-109">The contact records from Sales must be ingested in audience insights and used as a data source.</span></span> <span data-ttu-id="5b5ba-110">Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-110">They also need to be included in the unified Customer entity to map customer IDs to contact IDs before segments can be exported.</span></span>

## <a name="configure-the-connector-for-sales"></a><span data-ttu-id="5b5ba-111">Konfiguratu konektorea Sales-erako</span><span class="sxs-lookup"><span data-stu-id="5b5ba-111">Configure the connector for Sales</span></span>

1. <span data-ttu-id="5b5ba-112">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-112">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="5b5ba-113">**Dynamics 365 Sales** azpian hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-113">Under **Dynamics 365 Sales**, select **Set up**.</span></span>

1. <span data-ttu-id="5b5ba-114">Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-114">Give your export destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="5b5ba-115">Sartu erakundearen Salmentako URLa **Zerbitzariaren helbidea** eremu.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-115">Enter your organization's Sales URL in the **Server address** field.</span></span>

1. <span data-ttu-id="5b5ba-116">Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Sales kontua.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-116">In the **Server admin account** section, select **Sign in** and choose a Dynamics 365 Sales account.</span></span>

1. <span data-ttu-id="5b5ba-117">Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-117">Map a customer ID field to the Dynamics 365 Contact ID.</span></span>

1. <span data-ttu-id="5b5ba-118">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-118">Select **Next**.</span></span>

1. <span data-ttu-id="5b5ba-119">Aukeratu segmentu bat edo gehiago.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-119">Choose one or more segments.</span></span>

1. <span data-ttu-id="5b5ba-120">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="5b5ba-120">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="5b5ba-121">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="5b5ba-121">Export the data</span></span>

<span data-ttu-id="5b5ba-122">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="5b5ba-122">You can [export data on demand](export-destinations.md).</span></span> <span data-ttu-id="5b5ba-123">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="5b5ba-123">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]