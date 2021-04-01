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
# <a name="connector-for-azure-data-lake-storage-gen2-preview"></a>Azure Data Lake Storage Gen2-ko konektorea (aurrebista)

Gorde Customer Insights-eko datuak Azure Data Lake Storage Gen2-n edo hori erabili datuak beste aplikazioetara transferitzeko.

## <a name="configure-the-connector-for-azure-data-lake-storage-gen2"></a>Konfiguratu konektorearentzako Azure Data Lake Storage Gen2

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Azure Data Lake Storage Gen2** atalean hautatu **Konfiguratu**.

1. Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.

1. Sartu **Kontuaren izena**, **Kontuaren gakoa** eta **Edukiontzia** zure Azure Data Lake Storage Gen2-n.
    - Erabiltzeko biltegiratze kontua nola sortu jakiteko Azure Data Lake Storage Gen2-rekin, ikusi [Sortu biltegiratze kontua](/azure/storage/blobs/create-data-lake-storage-account). 
    - Azure Data Lake Gen2 biltegiratze kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).

1. Hautatu **Hurrengoa**.

1. Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md#export-data-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).