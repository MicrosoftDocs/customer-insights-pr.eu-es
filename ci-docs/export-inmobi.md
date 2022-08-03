---
title: Esportatu Customer Insights datuak InMobi-ra
description: Ikasi konexioa nola konfiguratu eta InMobi-ra esportatzen.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: ef486ad6786ef01be977f3d6bda69ce8a2b081c7
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195873"
---
# <a name="export-customer-insights-data-to-inmobi-preview"></a>Esportatu Customer Insights datuak InMobi-ra (aurrebista)

Esportatu zure Customer Insights instantziako segmentu-zerrendak edo bestelako datuak [InMobi](https://www.inmobi.com/).

## <a name="prerequisites"></a>Aurrebaldintzak

- An [InMobi kontua](https://www.inmobi.com/) eta administratzailearen kredentzialak.
- An [Azure Blob Storage kontua](/azure/storage/blobs/create-data-lake-storage-account) izena eta kontu-gakoa. Izena eta gakoa aurkitzeko, ikus [Kudeatu biltegiratze-kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
- An [Azure Blob biltegiratze edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container) InMobi datuak esportatzeko.
- InMobi-k konexio zuzena sortuko du zure Blob biltegiarekin eta zure datuak InMobi-ra inportazio automatiko bat konfiguratuko du. Jarri harremanetan zure InMobiko ordezkariarekin prozesua hasteko.

## <a name="known-limitations"></a>Muga ezagunak

- Azure Blob Storage-rako, aukeratu artean [Errendimendu estandarra eta Premium errendimendu maila](/azure/storage/blobs/storage-blob-performance-tiers). Premiu, errendimendu maila aukeratzen baduzu, hautatu [premium blokeak blob kontu mota gisa](/azure/storage/common/storage-account-overview#types-of-storage-accounts).

## <a name="set-up-connection-to-azure-blob-storage"></a>Konfiguratu konexioa Azure Blob Storage-rekin

[Konfiguratu konexio bat zure Azure Blob Storage-rako](export-azure-blob-storage.md).

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[Konfiguratu esportazio bat](export-azure-blob-storage.md#configure-an-export).

[!INCLUDE [footer-include](includes/footer-banner.md)]
