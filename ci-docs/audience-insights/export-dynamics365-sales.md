---
title: Esportatu Customer Insights datuak Dynamics 365 Sales-era
description: Ikasi konexioa nola konfiguratu eta Dynamics 365 Sales-era esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: fc1a05ba4d21d96aa1a9724d158687bbb86949b6
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5759576"
---
# <a name="use-segments-in-dynamics-365-sales-preview"></a><span data-ttu-id="3ab0a-103">Erabili segmentuak Dynamics 365 Sales-en (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="3ab0a-103">Use segments in Dynamics 365 Sales (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="3ab0a-104">Dynamics 365 Sales-ekin marketin-zerrendak sortzeko, lan-fluxuen segimendua egiteko eta eskaintzak bidaltzeko, erabili bezeroen datuak.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-104">Use your customer data to create marketing lists, follow up workflows, and send out promotions with Dynamics 365 Sales.</span></span>

## <a name="prerequisite-for-connection"></a><span data-ttu-id="3ab0a-105">Konexiorako aurrebaldintza</span><span class="sxs-lookup"><span data-stu-id="3ab0a-105">Prerequisite for connection</span></span>

1. <span data-ttu-id="3ab0a-106">Kontaktu-erregistroek Dynamics 365 Sales-en egon behar dute segmentu bat Customer Insights-etik Sales-era esportatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-106">Contact records must be present in Dynamics 365 Sales before you can export a segment from Customer Insights to Sales.</span></span> <span data-ttu-id="3ab0a-107">Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Sales erabiliz Common Data Services](connect-power-query.md).</span><span class="sxs-lookup"><span data-stu-id="3ab0a-107">Read more on how to ingest contacts in [Dynamics 365 Sales using Common Data Services](connect-power-query.md).</span></span>

   > [!NOTE]
   > <span data-ttu-id="3ab0a-108">Ikuspegien estatistiketatik salmentetara segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Sales instantzietan.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-108">Exporting segments from audience insights to Sales will not create new contact records in the Sales instances.</span></span> <span data-ttu-id="3ab0a-109">Sales kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-109">The contact records from Sales must be ingested in audience insights and used as a data source.</span></span> <span data-ttu-id="3ab0a-110">Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-110">They also need to be included in the unified Customer entity to map customer IDs to contact IDs before segments can be exported.</span></span>

## <a name="set-up-the-connection-to-sales"></a><span data-ttu-id="3ab0a-111">Konfiguratu konexioa Sales-era</span><span class="sxs-lookup"><span data-stu-id="3ab0a-111">Set up the connection to Sales</span></span>

1. <span data-ttu-id="3ab0a-112">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-112">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="3ab0a-113">Hautatu **Gehitu konexioa** eta aukeratu **Dynamics 365 Sales** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-113">Select **Add connection** and choose **Dynamics 365 Sales** to configure the connection.</span></span>

1. <span data-ttu-id="3ab0a-114">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-114">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="3ab0a-115">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-115">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="3ab0a-116">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-116">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="3ab0a-117">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-117">Choose who can use this connection.</span></span> <span data-ttu-id="3ab0a-118">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-118">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="3ab0a-119">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="3ab0a-119">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="3ab0a-120">Sartu erakundearen Salmentako URLa **Zerbitzariaren helbidea** eremu.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-120">Enter your organization's Sales URL in the **Server address** field.</span></span>

1. <span data-ttu-id="3ab0a-121">Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Sales kontua.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-121">In the **Server admin account** section, select **Sign in** and choose a Dynamics 365 Sales account.</span></span>

1. <span data-ttu-id="3ab0a-122">Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-122">Map a customer ID field to the Dynamics 365 Contact ID.</span></span>

1. <span data-ttu-id="3ab0a-123">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-123">Select **Save** to complete the connection.</span></span> 

## <a name="configure-an-export"></a><span data-ttu-id="3ab0a-124">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="3ab0a-124">Configure an export</span></span>

<span data-ttu-id="3ab0a-125">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-125">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="3ab0a-126">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="3ab0a-126">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="3ab0a-127">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-127">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="3ab0a-128">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-128">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="3ab0a-129">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Dynamics 365 Sales sekzioan.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-129">In the **Connection for export** field, choose a connection from the Dynamics 365 Sales section.</span></span> <span data-ttu-id="3ab0a-130">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-130">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="3ab0a-131">Aukeratu segmentu bat edo gehiago.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-131">Choose one or more segments.</span></span>

1. <span data-ttu-id="3ab0a-132">Sakatu **Gorde**</span><span class="sxs-lookup"><span data-stu-id="3ab0a-132">Select **Save**</span></span>

<span data-ttu-id="3ab0a-133">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="3ab0a-133">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="3ab0a-134">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="3ab0a-134">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="3ab0a-135">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="3ab0a-135">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
