---
title: Esportatu Customer Insights datuak Azure Data Lake Storage Gen2-ra
description: Ikasi Azure Data Lake Storage Gen2-rako konexioa nola konfiguratu.
ms.date: 02/04/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 7c0eef575f745efa6312d7141a6dd96607f9797e
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596622"
---
# <a name="connector-for-azure-data-lake-storage-gen2-preview"></a><span data-ttu-id="49ba5-103">Azure Data Lake Storage Gen2-ko konektorea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="49ba5-103">Connector for Azure Data Lake Storage Gen2 (preview)</span></span>

<span data-ttu-id="49ba5-104">Gorde Customer Insights-eko datuak Azure Data Lake Storage Gen2-n edo hori erabili datuak beste aplikazioetara transferitzeko.</span><span class="sxs-lookup"><span data-stu-id="49ba5-104">Store your Customer Insights data in Azure Data Lake Storage Gen2 or use it to transfer your data to other applications.</span></span>

## <a name="configure-the-connector-for-azure-data-lake-storage-gen2"></a><span data-ttu-id="49ba5-105">Konfiguratu konektorearentzako Azure Data Lake Storage Gen2</span><span class="sxs-lookup"><span data-stu-id="49ba5-105">Configure the connector for Azure Data Lake Storage Gen2</span></span>

1. <span data-ttu-id="49ba5-106">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="49ba5-106">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="49ba5-107">**Azure Data Lake Storage Gen2** atalean hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="49ba5-107">Under **Azure Data Lake Storage Gen2**, select **Set up**.</span></span>

1. <span data-ttu-id="49ba5-108">Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.</span><span class="sxs-lookup"><span data-stu-id="49ba5-108">Give your destination a recognizable name in the **Display name** field.</span></span>

1. <span data-ttu-id="49ba5-109">Sartu **Kontuaren izena**, **Kontuaren gakoa** eta **Edukiontzia** zure Azure Data Lake Storage Gen2-n.</span><span class="sxs-lookup"><span data-stu-id="49ba5-109">Enter **Account name**, **Account key**, and **Container** for your Azure Data Lake Storage Gen2.</span></span>
    - <span data-ttu-id="49ba5-110">Erabiltzeko biltegiratze kontua nola sortu jakiteko Azure Data Lake Storage Gen2-rekin, ikusi [Sortu biltegiratze kontua](/azure/storage/blobs/create-data-lake-storage-account).</span><span class="sxs-lookup"><span data-stu-id="49ba5-110">To learn how to create a storage account to use with Azure Data Lake Storage Gen2, see [Create storage account](/azure/storage/blobs/create-data-lake-storage-account).</span></span> 
    - <span data-ttu-id="49ba5-111">Azure Data Lake Gen2 biltegiratze kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).</span><span class="sxs-lookup"><span data-stu-id="49ba5-111">To learn more about how to find the Azure Data Lake Gen2 storage account name and account key, see [Manage storage account settings in the Azure portal](/azure/storage/common/storage-account-manage).</span></span>

1. <span data-ttu-id="49ba5-112">Hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="49ba5-112">Select **Next**.</span></span>

1. <span data-ttu-id="49ba5-113">Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.</span><span class="sxs-lookup"><span data-stu-id="49ba5-113">Select the box next to each of the entities you want to export to this destination.</span></span>

1. <span data-ttu-id="49ba5-114">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="49ba5-114">Select **Save**.</span></span>

## <a name="export-the-data"></a><span data-ttu-id="49ba5-115">Esportatu datuak</span><span class="sxs-lookup"><span data-stu-id="49ba5-115">Export the data</span></span>

<span data-ttu-id="49ba5-116">Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md#export-data-on-demand).</span><span class="sxs-lookup"><span data-stu-id="49ba5-116">You can [export data on demand](export-destinations.md#export-data-on-demand).</span></span> <span data-ttu-id="49ba5-117">Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="49ba5-117">The export will also run with every [scheduled refresh](system.md#schedule-tab).</span></span>