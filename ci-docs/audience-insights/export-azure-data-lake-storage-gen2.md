---
title: Esportatu Customer Insights datuak Azure Data Lake Storage Gen2-ra
description: Ikasi Azure Data Lake Storage Gen2-rako konexioa nola konfiguratu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: f431b707e1d65ffe47f8b3aa1c52abaa964e871a
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5760036"
---
# <a name="set-up-the-connection-to-azure-data-lake-storage-gen2-preview"></a><span data-ttu-id="1d2a9-103">Konfiguratu konexioa Azure Data Lake Storage 2. belaunaldia (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="1d2a9-103">Set up the connection to Azure Data Lake Storage Gen2 (preview)</span></span>

1. <span data-ttu-id="1d2a9-104">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-104">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="1d2a9-105">Hautatu **Gehitu konexioa** eta aukeratu **Azure Data Lake 2. belaunaldia** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-105">Select **Add connection** and choose **Azure Data Lake Gen 2** to configure the connection.</span></span>

1. <span data-ttu-id="1d2a9-106">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-106">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="1d2a9-107">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-107">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="1d2a9-108">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-108">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="1d2a9-109">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-109">Choose who can use this connection.</span></span> <span data-ttu-id="1d2a9-110">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-110">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="1d2a9-111">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="1d2a9-111">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="1d2a9-112">Sartu **Kontuaren izena**, **Kontuaren gakoa** eta **Edukiontzia** zure Azure Data Lake Storage Gen2-n.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-112">Enter **Account name**, **Account key**, and **Container** for your Azure Data Lake Storage Gen2.</span></span>
    - <span data-ttu-id="1d2a9-113">Erabiltzeko biltegiratze kontua nola sortu jakiteko Azure Data Lake Storage Gen2-rekin, ikusi [Sortu biltegiratze kontua](/azure/storage/blobs/create-data-lake-storage-account).</span><span class="sxs-lookup"><span data-stu-id="1d2a9-113">To learn how to create a storage account to use with Azure Data Lake Storage Gen2, see [Create storage account](/azure/storage/blobs/create-data-lake-storage-account).</span></span> 
    - <span data-ttu-id="1d2a9-114">Azure Data Lake 2. belaunaldia biltegiratze-kontuaren izena eta kontuaren gakoari buruz gehiago jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="1d2a9-114">To learn more about Azure Data Lake Gen2 storage account name and account key, see [Manage storage account settings in the Azure portal](/azure/storage/common/storage-account-manage).</span></span>

1. <span data-ttu-id="1d2a9-115">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-115">Select **Save** to complete the connection.</span></span> 

## <a name="configure-an-export"></a><span data-ttu-id="1d2a9-116">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="1d2a9-116">Configure an export</span></span>

<span data-ttu-id="1d2a9-117">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-117">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="1d2a9-118">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="1d2a9-118">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="1d2a9-119">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-119">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="1d2a9-120">Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-120">To create a new export, select **Add export**.</span></span>

1. <span data-ttu-id="1d2a9-121">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa **Azure Data Lake** sekziotik.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-121">In the **Connection for export** field, choose a connection from the **Azure Data Lake** section.</span></span> <span data-ttu-id="1d2a9-122">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-122">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="1d2a9-123">Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-123">Select the box next to each of the entities you want to export to this destination.</span></span>

1. <span data-ttu-id="1d2a9-124">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-124">Select **Save**.</span></span>

<span data-ttu-id="1d2a9-125">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-125">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="1d2a9-126">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="1d2a9-126">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="1d2a9-127">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="1d2a9-127">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

<span data-ttu-id="1d2a9-128">Esportatutako datuak konfiguratu duzun Azure Data Lake 2. belaunaldiaren biltegirako edukiontzian gordetzen dira.</span><span class="sxs-lookup"><span data-stu-id="1d2a9-128">Exported data is stored in the Azure Data Lake Gen 2 storage container you configured.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
