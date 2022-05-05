---
title: Esportatu Customer Insights datuak Azure Synapse Analytics
description: Ikasi konexioa nola konfiguratu Azure Synapse Analytics.
ms.date: 04/11/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: e77227e1e353c02cfb13e26a8ecbe0768ba6c0fa
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642085"
---
# <a name="export-data-to-azure-synapse-analytics-preview"></a>Esportatu datuak hona Azure Synapse Analytics (Aurrebista)

Azure Synapse datu-biltegi eta makrodatuen sistemen ikuspegi luzea lortzeko denbora azkartzen duen analisi zerbitzua da. Zure Customer Insights datuak gehitu eta erabil ditzakezu hemen: [Azure Synapse](/azure/synapse-analytics/overview-what-is).

## <a name="prerequisites"></a>Aurrebaldintzak

Customer Insights-etik konexioa konfiguratzeko honako baldintza hauek bete behar dira Azure Synapse.

> [!NOTE]
> Ziurtatu guztiak ezartzen dituzula **funtzioak esleitzea** azaldu bezala.  

## <a name="prerequisites-in-customer-insights"></a>Customer Insights-eko aurrebaldintzak

* Zure Azure Active Directory (AD) erabiltzaile-kontuak bat du **Administratzailea** Customer Insights-en eginkizuna. Lortu informazio gehiago [erabiltzaileen baimenak ezartzea](permissions.md#assign-roles-and-permissions).

Azure-n: 

- Azure harpidetza aktibo bat.

- Berria erabiliz gero Azure Data Lake Storage Gen2 kontua, *Customer Insights-en zerbitzu nagusia* beharrak **Biltegiratze Blob Datuen Laguntzailea** baimenak. Lortu informazio gehiago [Azure Data Lake Storage Gen2 kontu batera konektatzea Azure zerbitzuaren nagusiarekin hartzaileei buruzko informazioa lortzeko](connect-service-principal.md). Data Lake Storage Gen2-k **behar du** [izen-leku hierarkikoa](/azure/storage/blobs/data-lake-storage-namespace) gaituta.

- Baliabide taldean Azure Synapse lan-eremua kokatzen da, *zerbitzu nagusia* eta *Azure AD Customer Insights-en administratzaile-baimenak dituen erabiltzailea* esleitu behar dira gutxienez **Irakurlea** baimenak. Informazio gehiagorako, ikusi [Esleitu Azure funtzioak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal).

- The *Azure AD Customer Insights-en administratzaile-baimenak dituen erabiltzailea* beharrak **Biltegiratze Blob Datuen Laguntzailea** buruzko baimenak Azure Data Lake Storage Gen2 kontua non dauden datuak kokatuta eta honekin lotuta Azure Synapse lan-eremua. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- *[Azure Synapse laneko eremuaren kudeatutako identitatea](/azure/synapse-analytics/security/synapse-workspace-managed-identity)* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- Gainean Azure Synapse lan-eremua, *Customer Insights-en zerbitzu nagusia* beharrak **Synapse Administratzailea** esleitutako rola. Informazio gehiagorako, ikus [Nola konfiguratu sarbide kontrola zure Synapse laneko areako](/azure/synapse-analytics/security/how-to-set-up-access-control).

## <a name="set-up-the-connection-and-export-to-azure-synapse"></a>Konfiguratu eta esportatu konexioa Azure Synapse-ra

### <a name="configure-a-connection"></a>Konfiguratu konexioa

Konexio bat sortzeko, zerbitzu nagusiak eta Customer Insights-en erabiltzaile-kontua behar dira **Irakurlea** buruzko baimenak *baliabide taldea* non dagoen Synapse Analytics lan-eremua. Gainera, Synapse Analytics lan-eremuko zerbitzu nagusiak eta erabiltzaileak behar dira **Synapse Administratzailea** baimenak. 

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Azure Synapse Analytics** edo hautatu **Konfiguratu** gainean **Azure Synapse Analytics** fitxa konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena Bistaratze izena eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu edo bilatu Customer Insights datuak erabili nahi dituzun harpidetza. Harpidetza hautatu bezain laster, hauta dezakezu **Laneko area**, **Biltegiratze kontua**, eta **Edukiontzia**.

1. Konexioa gordetzeko, hautatu **Gorde**.

### <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Esportazioa partekatutako konexio batekin konfiguratzeko, gutxienez behar duzu **Laguntzailea** baimenak Customer Insights-en. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat **Azure Synapse Analytics** atala. Atal honen izena ikusten ez baduzu, ez dago mota honetako [konexiorik](connections.md) erabilgarri.

1. Ezagutzeko modukoa eman **Bistaratzeko izena** zure esportaziorako eta **Datu-basearen izena**.

1. Hautatu zein entitatetara esportatu nahi duzun Azure Synapse Analytics.
   > [!NOTE]
   > [Common Data Model karpetan](connect-common-data-model.md) oinarritutako datu iturriak ez dira onartzen.

2. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).

Synapse Analytics-era esportatu diren datuak kontsultatzeko, behar duzu **Biltegiratze Blob Datuen irakurgailua** esportazioen lan-eremuan helmugako biltegiratze sarbidea. 

### <a name="update-an-export"></a>Eguneratu esportazio bat

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Editatu** eguneratu nahi duzun esportazioan.

   - **Gehitu** edo **Kendu** hautapeneko entitateak. Entitateak hautaketatik kentzen badira, ez dira Synapse Analytics datu basetik ezabatuko. Hala ere, etorkizuneko datuak freskatzeak ez ditu datu-base horretako kendutako entitateak eguneratuko.

   - **Datu-basearen izena aldatzea** Synapse Analytics datu-base berria sortzen du. Aurretik konfiguratutako izenaren datu baseak ez du eguneratzerik jasoko etorkizuneko freskatze-eragiketetan.
