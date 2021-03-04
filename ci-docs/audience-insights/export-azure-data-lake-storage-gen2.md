---
title: Esportatu Customer Insights datuak Azure Data Lake Storage Gen2-ra
description: Ikasi Azure Data Lake Storage Gen2-rako konexioa nola konfiguratu.
ms.date: 02/04/2021
ms.reviewer: sthe
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: b00c3d6178150cbc93fe800779f094809d4dc67b
ms.sourcegitcommit: 0260ed244b97c2fd0be5e9a084c4c489358e8d4f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/18/2021
ms.locfileid: "5477164"
---
# <a name="connector-for-azure-data-lake-storage-gen2-preview"></a><span data-ttu-id="17ab9-103">Azure Data Lake Storage Gen2-ko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="17ab9-103">Connector for Azure Data Lake Storage Gen2 (preview)</span></span>

<span data-ttu-id="17ab9-104">Gorde Customer Insights-eko datuak Azure Data Lake Storage Gen2-n edo hori erabili datuak beste aplikazioetara transferitzeko.</span><span class="sxs-lookup"><span data-stu-id="17ab9-104">Store your Customer Insights data in Azure Data Lake Storage Gen2 or use it to transfer your data to other applications.</span></span>

## <a name="configure-the-connector-for-azure-data-lake-storage-gen2"></a><span data-ttu-id="17ab9-105">Konfiguratu konektorearentzako Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="17ab9-105">Configure the connector for Azure Data Lake Storage Gen2</span></span>

1. <span data-ttu-id="17ab9-106">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="17ab9-106">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="17ab9-107">**Azure Data Lake Storage Gen2** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="17ab9-107">Under **Azure Data Lake Storage Gen2**, select **Set up**.</span></span>

1. <span data-ttu-id="17ab9-108">Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.</span><span class="sxs-lookup"><span data-stu-id="17ab9-108">Give your destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="17ab9-109">Sartu **Kontuaren izena**, **Kontuaren gakoa** eta **Edukiontzia** zure Azure Data Lake Storage Gen2-n.</span><span class="sxs-lookup"><span data-stu-id="17ab9-109">Enter **Account name**, **Account key**, and **Container** for your Azure Data Lake Storage Gen2.</span></span>
    - <span data-ttu-id="17ab9-110">Erabiltzeko biltegiratze kontua nola sortu jakiteko Azure Data Lake Storage Gen2-rekin, ikusi [Sortu biltegiratze kontua](https://docs.microsoft.com/azure/storage/blobs/create-data-lake-storage-account).</span><span class="sxs-lookup"><span data-stu-id="17ab9-110">To learn how to create a storage account to use with Azure Data Lake Storage Gen2, see [Create storage account](https://docs.microsoft.com/azure/storage/blobs/create-data-lake-storage-account).</span></span> 
    - <span data-ttu-id="17ab9-111">Azure Data Lake Gen2 biltegiratze kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](https://docs.microsoft.com/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="17ab9-111">To learn more about how to find the Azure Data Lake Gen2 storage account name and account key, see [Manage storage account settings in the Azure portal](https://docs.microsoft.com/azure/storage/common/storage-account-manage).</span></span>

1. <span data-ttu-id="17ab9-112">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="17ab9-112">Select **Next**.</span></span>

1. <span data-ttu-id="17ab9-113">Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.</span><span class="sxs-lookup"><span data-stu-id="17ab9-113">Select the box next to each of the entities you want to export to this destination.</span></span>

1. <span data-ttu-id="17ab9-114">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="17ab9-114">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="17ab9-115">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="17ab9-115">Export the data</span></span>

<span data-ttu-id="17ab9-116">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md#export-data-on-demand).</span><span class="sxs-lookup"><span data-stu-id="17ab9-116">You can [export data on demand](export-destinations.md#export-data-on-demand).</span></span> <span data-ttu-id="17ab9-117">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="17ab9-117">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>
