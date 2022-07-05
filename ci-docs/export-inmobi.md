---
title: Esportatu Customer Insights datuak InMobi-ra
description: Ikasi konexioa nola konfiguratu eta InMobi-ra esportatu.
ms.date: 06/27/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 8261c8adfe231792e70fc85432237cf73d5cd5a7
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9059603"
---
# <a name="export-segment-list-and-other-data-to-inmobi-preview"></a>Esportatu segmentu-zerrenda eta beste datu batzuk InMobi-ra (aurrebista)

Esportatu zure Customer Insights instantziako segmentu-zerrendak edo bestelako datuak [InMobi](https://www.inmobi.com/).

## <a name="prerequisites"></a>Aurrebaldintzak

1. Bat daukazu [InMobi kontua](https://www.inmobi.com/) eta administratzailearen kredentzialak.
1. Azure Blob biltegiratze-kontuaren izena eta dagokion kontu-gakoa dituzu. Informazio gehiagorako, ikus [Kudeatu biltegiratze-kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage). Biltegiratze-kontuan edukiontzi bat dago inMobi datuak esportatzeko. Informazio gehiagorako, ikus [Sortu edukiontzi bat](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).
1. InMobi-k zuzeneko konexioa sortuko du zure Blob biltegiarekin eta zure datuak InMobi-ra inportazio automatiko bat konfiguratuko du. Jarri harremanetan InMobiko ordezkariarekin prozesua hasteko.

## <a name="known-limitations"></a>Muga ezagunak

1. Azure Blob Storagerako, artean aukeratu dezakezu [Errendimendu estandarra eta Premium errendimendu maila](/azure/storage/blobs/storage-blob-performance-tiers). Premiu, errendimendu maila aukeratzen baduzu, hautatu [premium blokeak blob kontu mota gisa](/azure/storage/common/storage-account-overview#types-of-storage-accounts).

## <a name="set-up-the-connection-to-azure-blob-storage-and-configure-an-export"></a>Konfiguratu Azure Blob Storage-rako konexioa eta konfiguratu esportazio bat

1. Jarraitu argibideei [konfiguratu zure Azure Blob biltegiratze konexioa](export-azure-blob-storage.md).
2. Jarraitu argibideei [esportazio bat konfiguratu](export-azure-blob-storage.md#configure-an-export).

[!INCLUDE [footer-include](includes/footer-banner.md)]
