---
title: Esportatu Customer Insights datuak Azure Blob biltegi batera
description: Ikasi konexioa konfiguratzen eta esportatzen Blob biltegira.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 294feff2f77c3756fbadb36c90aab430454f5967
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760174"
---
# <a name="export-segment-list-and-other-data-to-azure-blob-storage-preview"></a><span data-ttu-id="0e202-103">Esportatu segmentuen zerrenda eta beste datu batzuk Azure Blob biltegira (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="0e202-103">Export segment list and other data to Azure Blob Storage (preview)</span></span>

<span data-ttu-id="0e202-104">Gorde Customer Insights-eko datuak Azure Blob biltegian edo hori erabili datuak beste aplikazioetara transferitzeko.</span><span class="sxs-lookup"><span data-stu-id="0e202-104">Store your Customer Insights data in a Blob storage or use it to transfer your data to other applications.</span></span>

## <a name="set-up-the-connection-to-blob-storage"></a><span data-ttu-id="0e202-105">Konfiguratu konexioa Blob biltegira</span><span class="sxs-lookup"><span data-stu-id="0e202-105">Set up the connection to Blob storage</span></span>

1. <span data-ttu-id="0e202-106">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="0e202-106">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="0e202-107">Hautatu **Gehitu konexioa** eta aukeratu **Azure Blob biltegia** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="0e202-107">Select **Add connection** and choose **Azure Blob Storage** to configure the connection.</span></span>

1. <span data-ttu-id="0e202-108">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="0e202-108">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="0e202-109">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="0e202-109">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="0e202-110">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="0e202-110">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="0e202-111">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="0e202-111">Choose who can use this connection.</span></span> <span data-ttu-id="0e202-112">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="0e202-112">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="0e202-113">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="0e202-113">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="0e202-114">Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** zure Blob biltegiratze konturako.</span><span class="sxs-lookup"><span data-stu-id="0e202-114">Enter **Account name**, **Account key**, and **Container** for your Blob storage account.</span></span>
    - <span data-ttu-id="0e202-115">Blob biltegiratze kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="0e202-115">To learn more about how to find the Blob storage account name and account key, see [Manage storage account settings in the Azure portal](/azure/storage/common/storage-account-manage).</span></span>
    - <span data-ttu-id="0e202-116">Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span><span class="sxs-lookup"><span data-stu-id="0e202-116">To learn how to create a container, see [Create a container](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).</span></span>

1. <span data-ttu-id="0e202-117">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="0e202-117">Select **Save** to complete the connection.</span></span> 

## <a name="configure-an-export"></a><span data-ttu-id="0e202-118">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="0e202-118">Configure an export</span></span>

<span data-ttu-id="0e202-119">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="0e202-119">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="0e202-120">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="0e202-120">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="0e202-121">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="0e202-121">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="0e202-122">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="0e202-122">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="0e202-123">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Azure Blob biltegiaren sekzioan.</span><span class="sxs-lookup"><span data-stu-id="0e202-123">In the **Connection for export** field, choose a connection from the Azure Blob Storage section.</span></span> <span data-ttu-id="0e202-124">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="0e202-124">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="0e202-125">Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.</span><span class="sxs-lookup"><span data-stu-id="0e202-125">Select the box next to each of the entities you want to export to this destination.</span></span>

1. <span data-ttu-id="0e202-126">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="0e202-126">Select **Save**.</span></span>

<span data-ttu-id="0e202-127">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="0e202-127">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="0e202-128">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="0e202-128">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span>     
<span data-ttu-id="0e202-129">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="0e202-129">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

<span data-ttu-id="0e202-130">Esportatutako datuak konfiguratu duzun Blob biltegirako edukiontzian gordetzen dira.</span><span class="sxs-lookup"><span data-stu-id="0e202-130">Exported data is stored in the Blob storage container you configured.</span></span> <span data-ttu-id="0e202-131">Hurrengo karpeta bideak automatikoki sortzen dira zure edukiontzian:</span><span class="sxs-lookup"><span data-stu-id="0e202-131">The following folder paths are automatically created in your container:</span></span>

- <span data-ttu-id="0e202-132">Sistemak sortutako iturburuko entitate eta entitateetarako: `%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv`</span><span class="sxs-lookup"><span data-stu-id="0e202-132">For source entities and entities generated by the system: `%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv`</span></span>
  - <span data-ttu-id="0e202-133">Adibidez: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/HighValueSegment/2020/08/24/1433/HighValueSegment_1.csv`</span><span class="sxs-lookup"><span data-stu-id="0e202-133">Example: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/HighValueSegment/2020/08/24/1433/HighValueSegment_1.csv`</span></span>
- <span data-ttu-id="0e202-134">Esportatutako entitateentzako model.json webgunean egongo da %ExportDestinationName% maila</span><span class="sxs-lookup"><span data-stu-id="0e202-134">The model.json for the exported entities will be at the %ExportDestinationName% level</span></span>
  - <span data-ttu-id="0e202-135">Adibidez: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/model.json`</span><span class="sxs-lookup"><span data-stu-id="0e202-135">Example: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/model.json`</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
