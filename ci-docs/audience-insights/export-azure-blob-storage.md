---
title: Esportatu Customer Insights datuak Azure Blob biltegira
description: Ikasi Azure Blob biltegirako konexioa nola konfiguratu.
ms.date: 09/18/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 0986ee5caf5fa079994ca584fb2c4d9294ddb80b
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596162"
---
# <a name="connector-for-azure-blob-storage-preview"></a>Azure Blob biltegirako konektorea (aurrebista)

Gorde Customer Insights-eko datuak Azure Blob biltegian edo erabili datuak beste aplikazioetara transferitzeko.

## <a name="configure-the-connector-for-azure-blob-storage"></a>Konfiguratu konektorea Azure Blob biltegiratzea

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Azure Blob biltegia** hautatu **Konfiguratu**.

1. Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **edukiontzi** zure Azure Blob biltegirako kontuan.
    - Azure Blob biltegiratze kontuaren izena eta kontuaren gakoa aurkitzeko informazio gehiago lortzeko, ikus [Kudeatu biltegiratze kontuen ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
    - Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

1. Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.

1. Hautatu **Hurrengoa**.

1. Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.

1. Sakatu **Gorde**.

Esportatutako datuak zuk konfiguratutako Azure Blob biltegian gordetzen dira. Hurrengo karpeta bideak automatikoki sortzen dira zure edukiontzian:

- Sistemak sortutako iturburuko entitate eta entitateetarako: `%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv`
  - Adibidez: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/HighValueSegment/2020/08/24/1433/HighValueSegment_1.csv`
- Model.json esportatutako entitateetarako mantenduko dira %ExportDestinationName% mailan
  - Adibidez: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/model.json`

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md#export-data-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).


[!INCLUDE[footer-include](../includes/footer-banner.md)]