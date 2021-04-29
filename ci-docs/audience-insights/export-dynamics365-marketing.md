---
title: Esportatu Customer Insights datuak Dynamics 365 Marketing-era
description: Ikasi konexioa konfiguratzen eta esportatzen Dynamics 365 Marketing-era.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: a13f6f81f5e2570d3302d88c02755f1d86321a01
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5759594"
---
# <a name="use-segments-in-dynamics-365-marketing-preview"></a><span data-ttu-id="1f663-103">Erabili segmentuak Dynamics 365 Marketing-en (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="1f663-103">Use segments in Dynamics 365 Marketing (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="1f663-104">Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko.</span><span class="sxs-lookup"><span data-stu-id="1f663-104">Use [segments](segments.md) to generate campaigns and contact specific groups of customers with Dynamics 365 Marketing.</span></span> <span data-ttu-id="1f663-105">Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments)</span><span class="sxs-lookup"><span data-stu-id="1f663-105">For more information, see [Use segments from Dynamics 365 Customer Insights with Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments)</span></span>

## <a name="prerequisite-for-a-connection"></a><span data-ttu-id="1f663-106">Konexioaren aurrebaldintza</span><span class="sxs-lookup"><span data-stu-id="1f663-106">Prerequisite for a connection</span></span>

- <span data-ttu-id="1f663-107">Kontaktu-erregistroek Dynamics 365 Marketing-en egon behar dute segmentu bat Customer Insights-etik Marketing-era esportatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="1f663-107">Contact records must be present in Dynamics 365 Marketing before you can export a segment from Customer Insights to Marketing.</span></span> <span data-ttu-id="1f663-108">Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Marketing erabiliz Common Data Services](connect-power-query.md).</span><span class="sxs-lookup"><span data-stu-id="1f663-108">Read more on how to ingest contacts in [Dynamics 365 Marketing using Common Data Services](connect-power-query.md).</span></span>

  > [!NOTE]
  > <span data-ttu-id="1f663-109">Ikuspegien estatistiketatik Marketing segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Marketing instantzietan.</span><span class="sxs-lookup"><span data-stu-id="1f663-109">Exporting segments from audience insights to Marketing will not create new contact records in the Marketing instances.</span></span> <span data-ttu-id="1f663-110">Marketing kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili.</span><span class="sxs-lookup"><span data-stu-id="1f663-110">The contact records from Marketing must be ingested in audience insights and used as a data source.</span></span> <span data-ttu-id="1f663-111">Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.</span><span class="sxs-lookup"><span data-stu-id="1f663-111">They also need to be included in the unified Customer entity to map customer IDs to contact IDs before segments can be exported.</span></span>

## <a name="set-up-connection-to-marketing"></a><span data-ttu-id="1f663-112">Konfiguratu konexioa Marketing-era</span><span class="sxs-lookup"><span data-stu-id="1f663-112">Set up connection to Marketing</span></span>

1. <span data-ttu-id="1f663-113">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="1f663-113">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="1f663-114">Hautatu **Gehitu konexioa** eta aukeratu **Dynamics 365 Marketing** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="1f663-114">Select **Add connection** and choose **Dynamics 365 Marketing** to configure the connection.</span></span>

1. <span data-ttu-id="1f663-115">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="1f663-115">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="1f663-116">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="1f663-116">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="1f663-117">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="1f663-117">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="1f663-118">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="1f663-118">Choose who can use this connection.</span></span> <span data-ttu-id="1f663-119">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="1f663-119">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="1f663-120">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="1f663-120">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="1f663-121">Sartu erakundearen Marketing URLa **Zerbitzariaren helbidea** eremu.</span><span class="sxs-lookup"><span data-stu-id="1f663-121">Enter your organization's Marketing URL in the **Server address** field.</span></span>

1. <span data-ttu-id="1f663-122">Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Marketing kontua.</span><span class="sxs-lookup"><span data-stu-id="1f663-122">In the **Server admin account** section, select **Sign in** and choose a Dynamics 365 Marketing account.</span></span>

1. <span data-ttu-id="1f663-123">Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="1f663-123">Map a customer ID field to the Dynamics 365 Contact ID.</span></span>

1. <span data-ttu-id="1f663-124">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="1f663-124">Select **Save** to complete the connection.</span></span> 

## <a name="configure-an-export"></a><span data-ttu-id="1f663-125">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="1f663-125">Configure an export</span></span>

<span data-ttu-id="1f663-126">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="1f663-126">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="1f663-127">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="1f663-127">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="1f663-128">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="1f663-128">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="1f663-129">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="1f663-129">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="1f663-130">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Dynamics 365 Marketing sekzioan.</span><span class="sxs-lookup"><span data-stu-id="1f663-130">In the **Connection for export** field, choose a connection from the Dynamics 365 Marketing section.</span></span> <span data-ttu-id="1f663-131">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="1f663-131">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="1f663-132">Aukeratu segmentu bat edo gehiago.</span><span class="sxs-lookup"><span data-stu-id="1f663-132">Choose one or more segments.</span></span>

1. <span data-ttu-id="1f663-133">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="1f663-133">Select **Save**.</span></span>

<span data-ttu-id="1f663-134">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="1f663-134">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="1f663-135">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="1f663-135">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="1f663-136">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="1f663-136">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
