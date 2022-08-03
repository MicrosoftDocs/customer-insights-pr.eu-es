---
title: Esportatu datuak hona Azure Data Lake Storage 2. belaunaldia (aurrebista)
description: Ikasi Azure Data Lake Storage Gen2-rako konexioa nola konfiguratu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 55a61e4d9166df7809a64aeb1168a730402aaed6
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196425"
---
# <a name="export-data-to-azure-data-lake-storage-gen2-preview"></a>Esportatu datuak hona Azure Data Lake Storage 2. belaunaldia (aurrebista)

Gorde Customer Insights datuak Azure Data Lake Storage Gen2 kontua edo erabili datuak beste aplikazio batzuetara transferitzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Azure Data Lake Gen2-rekin erabiltzeko biltegiratze-kontua](/azure/storage/blobs/create-data-lake-storage-account). Biltegiratze-kontuaren izena eta gakoa aurkitzeko, ikus [Kudeatu biltegiratze-kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
- An [Azure Blob biltegiratze edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

## <a name="known-limitations"></a>Muga ezagunak

- Izan ere Azure Data Lake Storage Gen2, aukeratu artean [Errendimendu estandarra eta Premium errendimendu maila](/azure/storage/blobs/create-data-lake-storage-account). Premiu, errendimendu maila aukeratzen baduzu, hautatu [premium blokeak blob kontu mota gisa](/azure/storage/common/storage-account-overview#types-of-storage-accounts).

## <a name="set-up-connection-to-azure-data-lake-storage-gen2"></a>Konfiguratu konexioa Azure Data Lake Storage Gen2

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Azure Data Lake 2. belaunaldia**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Kontuaren izena**, **Kontuaren gakoa** eta **Edukiontzia** zure Azure Data Lake Storage Gen2-n.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Azure Data Lake ataleko. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu karpetaren izena Azure Data Lake Storage Gen2 biltegiratzea.

1. Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

Esportatutako datuak konfiguratu duzun Azure Data Lake 2. belaunaldiaren biltegirako edukiontzian gordetzen dira.

> [!TIP]
> Datu kopuru handia duten entitateen esportazioak CSV fitxategi anitz ekar ditzake esportazio bakoitzerako karpeta berean. Esportazioen zatiketa errendimendu arrazoiengatik gertatzen da esportazio bat burutzeko behar den denbora gutxitzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
