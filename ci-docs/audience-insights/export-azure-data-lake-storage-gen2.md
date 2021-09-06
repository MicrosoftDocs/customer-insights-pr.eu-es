---
title: Esportatu Customer Insights datuak Azure Data Lake Storage Gen2-ra
description: Ikasi Azure Data Lake Storage Gen2-rako konexioa nola konfiguratu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: c4408e52550b6648e2a001041dc0acdb5063d6a6ef1b8e4bba3321bf25fefcfc
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7031964"
---
# <a name="set-up-the-connection-to-azure-data-lake-storage-gen2-preview"></a>Konfiguratu konexioa Azure Data Lake Storage 2. belaunaldia (aurrebista)

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Azure Data Lake 2. belaunaldia** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Kontuaren izena**, **Kontuaren gakoa** eta **Edukiontzia** zure Azure Data Lake Storage Gen2-n.
    - Erabiltzeko biltegiratze kontua nola sortu jakiteko Azure Data Lake Storage Gen2-rekin, ikusi [Sortu biltegiratze kontua](/azure/storage/blobs/create-data-lake-storage-account). 
    - Azure Data Lake 2. belaunaldia biltegiratze-kontuaren izena eta kontuaren gakoari buruz gehiago jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).

1. Hautatu **Gorde** konexioa osatzeko. 

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa **Azure Data Lake** sekziotik. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Hautatu helmugara esportatu nahi duzun entitate bakoitzaren ondoko laukia.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

Esportatutako datuak konfiguratu duzun Azure Data Lake 2. belaunaldiaren biltegirako edukiontzian gordetzen dira. 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
