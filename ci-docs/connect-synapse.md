---
title: Konektatu bat Azure Synapse datu-iturburu (aurrebista)
description: Erabili datu-base bat Azure Synapse urtean datu-iturburu gisa Dynamics 365 Customer Insights.
ms.date: 03/25/2022
ms.reviewer: v-wendysmith
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
ms.openlocfilehash: c4ae65613a02df38a30f907dae72d413bf1a702f
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9052684"
---
# <a name="connect-an-azure-synapse-analytics-data-source-preview"></a>Konektatu bat Azure Synapse Analytics datu-iturburu (aurrebista)

Azure Synapse Analytics datu biltegietan eta datu handien sistemetan informaziorako denbora azkartzen duen enpresa analitika-zerbitzu bat da. Azure Synapse Analytics Enpresako datuen biltegian erabiltzen diren SQL teknologia onenak biltzen ditu, datu handietarako erabiltzen diren Spark teknologiak, Data Explorer erregistro eta denbora serieen analisietarako, Pipelines datuak integratzeko eta ETL/ELT eta integrazio sakona beste Azure zerbitzu batzuekin, esaterako.Power BI,Cosmos DB, eta AzureML.

Informazio gehiagorako, ikus [Azure Synapse ikuspegi orokorra](/azure/synapse-analytics/overview-what-is).

## <a name="prerequisites"></a>Aurrebaldintzak

> [!IMPORTANT]
> Ziurtatu guztiak ezartzen dituzula **funtzioak esleitzea** azaldu bezala.  

**Bezeroen Insights atalean**:

* Bat daukazu **Administratzailea** Customer Insights-en eginkizuna. Lortu informazio gehiago [erabiltzailearen baimenak Customer Insights-en](permissions.md#assign-roles-and-permissions).

**Azuren**:

- Azure harpidetza aktibo bat.

- Berria erabiliz gero Azure Data Lake Storage Gen2 kontua, *Customer Insights-en zerbitzu nagusia* beharrak **Biltegiratze Blob Datuen Laguntzailea** baimenak. Lortu informazio gehiago [batekin konektatuz Azure Data Lake Storage Customer Insights zerbitzu nagusi batekin](connect-service-principal.md). Data Lake Storage Gen2-k **behar du** [izen-leku hierarkikoa](/azure/storage/blobs/data-lake-storage-namespace) gaituta.

- Baliabide taldean Azure Synapse lan-eremua kokatzen da, *zerbitzu nagusia* eta *Customer Insights-en erabiltzailea* esleitu behar da gutxienez **Irakurlea** baimenak. Informazio gehiagorako, ikusi [Esleitu Azure funtzioak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal).

- *Erabiltzailea* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- *[Azure Synapse laneko eremuaren kudeatutako identitatea](/azure/synapse-analytics/security/synapse-workspace-managed-identity)* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- Gainean Azure Synapse lan-eremua, *Customer Insights-en zerbitzu nagusia* beharrak **Synapse Administratzailea** esleitutako rola. Informazio gehiagorako, ikus [Nola konfiguratu sarbide kontrola zure Synapse laneko areako](/azure/synapse-analytics/security/how-to-set-up-access-control).

## <a name="connect-to-the-data-lake-database-in-azure-synapse-analytics"></a>Konektatu data Lake datu-basera Azure Synapse Analytics

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Aukeratu **Azure Synapse Analytics (Aurrebista)** metodoa.

   :::image type="content" source="media/data_sources_synapse.png" alt-text="Synapse Analytics datuetara konektatzeko elkarrizketa-koadroa":::
  
1. Sartu a **Izena** datu-iturburu eta aukerakoa **Deskribapena**.

1. Aukeratu bat [eskuragarri dagoen konexioa](connections.md) to Azure Synapse Analytics edo sortu berri bat.

1. Aukeratu a **Datu-basea** hautatutako lan-espaziotik Azure Synapse Analytics konexioa eta hautatu **Hurrengoa**. Gaur egun, datu-base mota soilik onartzen dugu *Lakuaren datu-basea*.

1. Hautatu konektatutako datu-basetik sartu beharreko entitateak eta hautatu **Hurrengoa**.

1. Aukeran, aukeratu datu-entitateak datuen profila onartzeko.

1. Hautatu **Gorde** zure hautapena aplikatzeko eta sortu berri den datu-iturburu Lake datu-baseko taulei lotuta dauden datuak sartzen hasteko.Azure Synapse Analytics. The **Datu iturriak** orrialdea irekitzen da datu-iturburu berria erakusten **Freskagarria** egoera.
