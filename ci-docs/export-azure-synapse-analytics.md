---
title: Esportatu datuak hona Azure Synapse Analytics (aurrebista)
description: Ikasi konexioa nola konfiguratu Azure Synapse Analytics.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: f9c9ee55f2874ae1dcaf82f2ff17ed0fbbb7804d
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196379"
---
# <a name="export-data-to-azure-synapse-analytics-preview"></a>Esportatu datuak hona Azure Synapse Analytics (aurrebista)

Azure Synapse datu-biltegi eta makrodatuen sistemen ikuspegi luzea lortzeko denbora azkartzen duen analisi zerbitzua da. Zure Customer Insights datuak gehitu eta erabil ditzakezu hemen: [Azure Synapse](/azure/synapse-analytics/overview-what-is).

## <a name="prerequisites"></a>Aurrebaldintzak

> [!NOTE]
> Ziurtatu guztiak ezartzen dituzula **funtzioak esleitzea** azaldu bezala.

- Customer Insights atalean, zure Azure Active Directory (AD) erabiltzaile-kontuak bat izan behar du [Administratzaile rola](permissions.md#assign-roles-and-permissions).

Azure-n:

- Azure harpidetza aktibo bat.

- Berria erabiliz gero Azure Data Lake Storage Gen2 kontua, [Customer Insights-en zerbitzu nagusia](connect-service-principal.md) ditu **Biltegiratze Blob Datuen Laguntzailea** baimenak. Data Lake Storage Gen2-k **behar du** [izen-leku hierarkikoa](/azure/storage/blobs/data-lake-storage-namespace) gaituta.

- Baliabide taldean non Azure Synapse lan-eremua kokatzen da, *zerbitzu nagusia* eta *Azure AD Customer Insights-en administratzaile-baimenak dituen erabiltzailea* esleitu behar dira gutxienez **Irakurlea**[baimenak](/azure/role-based-access-control/role-assignments-portal).

- The *Azure AD Customer Insights-en administratzaile-baimenak dituen erabiltzailea* ditu **Biltegiratze Blob Datuen Laguntzailea** baimenak Azure Data Lake Storage Datuak kokatuta dauden eta honekin lotuta dauden Gen2 kontua Azure Synapse lan-eremua. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- The *[Azure Synapse laneko gune kudeatutako identitatea](/azure/synapse-analytics/security/synapse-workspace-managed-identity)* ditu **Biltegiratze Blob Datuen Laguntzailea** baimenak Azure Data Lake Storage Datuak kokatuta dauden eta honekin lotuta dauden Gen2 kontua Azure Synapse lan-eremua. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- Gainean Azure Synapse lan-eremua, *Customer Insights-en zerbitzu nagusia* ditu **Synapse Administratzailea**[esleitutako rola](/azure/synapse-analytics/security/how-to-set-up-access-control).

## <a name="set-up-connection-to-azure-synapse"></a>Konfiguratu konexioa Azure Synapse

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Azure Synapse Analytics**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu edo bilatu Customer Insights datuak erabili nahi dituzun harpidetza. Harpidetza hautatu bezain laster, hauta dezakezu **Laneko area**, **Biltegiratze kontua**, eta **Edukiontzia**.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)] Esportazioa partekatutako konexio batekin konfiguratzeko, gutxienez behar duzu **Laguntzailea** baimenak Customer Insights-en.

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Azure Synapse Analytics atala. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Ezagutzeko modukoa eman **Bistaratzeko izena** zure esportaziorako eta **Datu-basearen izena**. Esportazioa berri bat sortuko da [Azure Synapse lakuaren datu-basea](/azure/synapse-analytics/database-designer/concepts-lake-database) konexioan zehaztutako lan eremuan.

1. Hautatu zein entitatetara esportatu nahi duzun Azure Synapse Analytics.
   > [!NOTE]
   > [Common Data Model karpetan](connect-common-data-model.md) oinarritutako datu iturriak ez dira onartzen.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

Synapse Analytics-era esportatu diren datuak kontsultatzeko, behar duzu **Biltegiratze Blob Datuen irakurgailua** esportazioen lan-eremuan helmugako biltegiratze sarbidea.

## <a name="update-an-export"></a>Eguneratu esportazio bat

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Editatu** eguneratu nahi duzun esportazioan.

   - **Gehitu** edo **Kendu** hautapeneko entitateak. Entitateak hautaketatik kentzen badira, ez dira Synapse Analytics datu basetik ezabatuko. Hala ere, etorkizuneko datuak freskatzeak ez ditu datu-base horretako kendutako entitateak eguneratuko.

   - **Datu-basearen izena aldatzea** Synapse Analytics datu-base berria sortzen du. Aurretik konfiguratutako izenaren datu baseak ez du eguneratzerik jasoko etorkizuneko freskatze-eragiketetan.

[!INCLUDE [footer-include](includes/footer-banner.md)]
