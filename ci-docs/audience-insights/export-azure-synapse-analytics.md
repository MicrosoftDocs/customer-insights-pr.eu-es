---
title: Esportatu Customer Insights datuak Azure Synapse Analytics-era
description: Ikasi konexioa nola konfiguratu Azure Synapse Analytics-en.
ms.date: 04/12/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 822082d661863e737ea3d3a749a6c878db766967
ms.sourcegitcommit: e8e03309ba2515374a70c132d0758f3e1e1851d0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5977362"
---
# <a name="export-data-to-azure-synapse-analytics-preview"></a>Esportatu datuak Azure Synapse Analytics-era (aurreargitalpena)

Azure Synapse datu-biltegi eta makrodatuen sistemen ikuspegi luzea lortzeko denbora azkartzen duen analisi zerbitzua da. Zure Customer Insights datuak gehitu eta erabil ditzakezu hemen: [Azure Synapse](/azure/synapse-analytics/overview-what-is).

## <a name="prerequisites"></a>Aurrebaldintzak

Customer Insights-etik konexioa konfiguratzeko honako baldintza hauek bete behar dira Azure Synapse.

> [!NOTE]
> Ziurtatu guztiak ezartzen dituzula **funtzioak esleitzea** azaldu bezala.  

## <a name="prerequisites-in-customer-insights"></a>Customer Insights-eko aurrebaldintzak

* Baduzu **Administratzailea** funtzioa hartzaileen xehetasunetan. Lortu informazio gehiago [erabiltzaileen baimenak ezartzea audientzia estatistiketan](permissions.md#assign-roles-and-permissions)

Azure-n: 

- Azure harpidetza aktibo bat.

- Azure Data Lake Storage Gen2 kontu berria erabiltzen baduzu, *hartzaileei buruzko informazioaren zerbitzu nagusia* beharrak **Biltegiko blob-datuen laguntzailea** baimenak. Lortu informazio gehiago [Azure Data Lake Storage Gen2 kontu batera konektatzea Azure zerbitzuaren nagusiarekin hartzaileei buruzko informazioa lortzeko](connect-service-principal.md). Data Lake Storage Gen2-k **behar du** [izen-leku hierarkikoa](/azure/storage/blobs/data-lake-storage-namespace) gaituta.

- Baliabide taldean Azure Synapse laneko area dago *zerbitzu nagusia* eta *erabiltzailea ikusleentzako estatistiketarako* gutxienez esleitu behar da **Irakurlea** baimenak. Informazio gehiagorako, ikusi [Esleitu Azure funtzioak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal).

- *Erabiltzailea* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- *[Azure Synapse laneko eremuaren kudeatutako identitatea](/azure/synapse-analytics/security/synapse-workspace-managed-identity)* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- Azure Synapse laneko arean *hartzaileei buruzko informazioaren zerbitzu nagusiak* **Synapse-ren administratzailea** funtzioa behar du. Informazio gehiagorako, ikus [Nola konfiguratu sarbide kontrola zure Synapse laneko areako](/azure/synapse-analytics/security/how-to-set-up-access-control).

## <a name="set-up-the-connection-and-export-to-azure-synapse"></a>Konfiguratu eta esportatu konexioa Azure Synapse-ra

### <a name="configure-a-connection"></a>Konfiguratu konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **Azure Synapse Analytics** edo hautatu **Konfiguratu** **Azure Synapse Analytics** lauzan konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena Bistaratze izena eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu edo bilatu Customer Insights datuak erabili nahi dituzun harpidetza. Harpidetza hautatu bezain laster, hauta dezakezu **Laneko area**, **Biltegiratze kontua**, eta **Edukiontzia**.

1. Konexioa gordetzeko, hautatu **Gorde**.

### <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa **Azure Synapse Analytics** sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako [konexiorik](connections.md) erabilgarri.

1. Ezagutzeko modukoa eman **Bistaratzeko izena** zure esportaziorako eta **Datu-basearen izena**.

1. Aukeratu zein entitatetara esportatu nahi duzun Azure Synapse Analytics-era.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).

### <a name="update-an-export"></a>Eguneratu esportazio bat

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Editatu** eguneratu nahi duzun esportazioan.

   - **Gehitu** edo **Kendu** hautapeneko entitateak. Entitateak hautaketatik kentzen badira, ez dira Synapse Analytics datu basetik ezabatuko. Hala ere, etorkizuneko datuak freskatzeak ez ditu datu-base horretako kendutako entitateak eguneratuko.

   - **Datu-basearen izena aldatzea** Synapse Analytics datu-base berria sortzen du. Aurretik konfiguratutako izenaren datu baseak ez du eguneratzerik jasoko etorkizuneko freskatze-eragiketetan.
