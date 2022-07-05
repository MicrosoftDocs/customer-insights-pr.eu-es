---
title: Esportatu datuak Azure Blob biltegiratze batera (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Blob biltegira.
ms.date: 06/09/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 059c8364ca0f3740bc0e4ffeeeba94246c9e5696
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9055475"
---
# <a name="export-data-to-an-azure-blob-storage-preview"></a>Esportatu datuak Azure Blob biltegiratze batera (aurrebista)

Gorde Customer Insights-eko datuak Azure Blob biltegian edo hori erabili datuak beste aplikazioetara transferitzeko.

## <a name="known-limitations"></a>Muga ezagunak

1. Azure blob biltegiratzeko, hauen artean aukeratu dezakezu [Errendimendu estandarra eta Premium errendimendu maila](/azure/storage/blobs/storage-blob-performance-tiers). Premiu, errendimendu maila aukeratzen baduzu, hautatu [premium blokeak blob kontu mota gisa](/azure/storage/common/storage-account-overview#types-of-storage-accounts).

## <a name="set-up-the-connection-to-blob-storage"></a>Konfiguratu konexioa Blob biltegira

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Azure Blob biltegia** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** zure Blob biltegiratze konturako.
    - Blob Storage kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
    - Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

1. Hautatu **Gorde** konexioa osatzeko. 

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

> [!IMPORTANT]
> Azure blob biltegiratze kontuaren softwarea ezabatzeko ezarpena aktibatzen baduzu, esportazioak huts egingo du. Desaktibatu behin behineko ezabatzea datuak blobetara esportatzeko. Informazio gehiagorako, ikus [Gaitu blob-en behin behineko ezabatzea](/azure/storage/blobs/soft-delete-blob-enable)

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Azure Blob biltegiaren sekzioan. Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.

1. Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).

Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).

Esportatutako datuak konfiguratu duzun Blob biltegirako edukiontzian gordetzen dira. Hurrengo karpeta bideak automatikoki sortzen dira zure edukiontzian:

- Sistemak sortutako iturburuko entitate eta entitateetarako:   
  `%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv`  
  - Adibidez: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/HighValueSegment/2020/08/24/1433/HighValueSegment_1.csv`
  
  > [!TIP]
  > Datu kopuru handia duten entitateen esportazioak CSV fitxategi anitz ekar ditzake esportazio bakoitzerako karpeta berean. Esportazioen zatiketa errendimendu arrazoiengatik gertatzen da esportazio bat burutzeko behar den denbora minimizatzeko.

- Esportatutako entitateentzako model.json egongo da %ExportDestinationName% mailan.  
  - Adibidez: `Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/model.json`

[!INCLUDE [footer-include](includes/footer-banner.md)]
