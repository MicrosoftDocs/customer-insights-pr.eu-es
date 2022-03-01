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
# <a name="connector-for-azure-data-lake-storage-gen2-preview"></a>Azure Data Lake Storage Gen2-ko konektorea (aurrebista)

Gorde Customer Insights-eko datuak Azure Data Lake Storage Gen2-n edo hori erabili datuak beste aplikazioetara transferitzeko.

## <a name="configure-the-connector-for-azure-data-lake-storage-gen2"></a>Konfiguratu konektorearentzako Azure Data Lake Storage Gen2

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Azure Data Lake Storage Gen2** atalean hautatu **Konfiguratu**.

1. Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.

1. Sartu **Kontuaren izena**, **Kontuaren gakoa** eta **Edukiontzia** zure Azure Data Lake Storage Gen2-n.
    - Erabiltzeko biltegiratze kontua nola sortu jakiteko Azure Data Lake Storage Gen2-rekin, ikusi [Sortu biltegiratze kontua](https://docs.microsoft.com/azure/storage/blobs/create-data-lake-storage-account). 
    - Azure Data Lake Gen2 biltegiratze kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](https://docs.microsoft.com/azure/storage/common/storage-account-manage).

1. Hautatu **Hurrengoa**.

1. Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md#export-data-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).
