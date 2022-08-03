---
title: Esportatu datuak Azure Blob biltegiratze batera (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Blob biltegira.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 22593ed05f403a40fe494e30f807b57658594f01
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195689"
---
# <a name="export-data-to-an-azure-blob-storage-preview"></a>Esportatu datuak Azure Blob biltegiratze batera (aurrebista)

Gorde Customer Insights-eko datuak Azure Blob biltegian edo hori erabili datuak beste aplikazioetara transferitzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- An [Azure Blob Storage kontua](/azure/storage/blobs/create-data-lake-storage-account) izena eta kontu-gakoa. Izena eta gakoa aurkitzeko, ikus [Kudeatu biltegiratze-kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
- An [Azure Blob biltegiratze edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

## <a name="known-limitations"></a>Muga ezagunak

- Azure Blob Storage-rako, aukeratu artean [Errendimendu estandarra eta Premium errendimendu maila](/azure/storage/blobs/storage-blob-performance-tiers). Premiu, errendimendu maila aukeratzen baduzu, hautatu [premium blokeak blob kontu mota gisa](/azure/storage/common/storage-account-overview#types-of-storage-accounts).

## <a name="set-up-connection-to-blob-storage"></a>Konfiguratu Blob biltegiratze konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Azure Blob biltegiratzea**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** zure Blob biltegiratze konturako.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfiguratzeko, eduki behar duzu [baimena](export-destinations.md#set-up-a-new-export) konexio mota honetarako.

> [!IMPORTANT]
> Piztu baduzu [ezabatze leuneko ezarpena](/azure/storage/blobs/soft-delete-blob-enable) Azure Blob Storage konturako, esportazioek huts egingo dute. Desaktibatu behin behineko ezabatzea datuak blobetara esportatzeko.

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Azure Blob biltegiaren sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu Blob biltegiratzeko karpeta-izena.

1. Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

Esportatutako datuak konfiguratu duzun Blob biltegirako edukiontzian gordetzen dira. Hurrengo karpeta bideak automatikoki sortzen dira zure edukiontzian:

- Sistemak sortutako iturburuko entitate eta entitateetarako:   
  *%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*  

  Adibidea: Dynamics365CustomerInsights/CustomerInsights_ abcd1234-4312-11f4-93dc-24f72f43e7d5 /BlobExport/HighValueSegment/2020/08/24/1433/HighValueSegment_1.csv
  
  > [!TIP]
  > Datu kopuru handia duten entitateen esportazioak CSV fitxategi anitz ekar ditzake esportazio bakoitzerako karpeta berean. Esportazioen zatiketa errendimendu arrazoiengatik gertatzen da esportazio bat burutzeko behar den denbora gutxitzeko.

- Esportatutako entitateen model.json helbidean dago *%ExportDestinationName%* maila.  
  
  Adibidea: Dynamics365CustomerInsights/CustomerInsights_ abcd1234-4312-11f4-93dc-24f72f43e7d5 /BlobExport/model.json

[!INCLUDE [footer-include](includes/footer-banner.md)]
