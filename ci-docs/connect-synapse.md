---
title: Hartu datuak Azure Synapse Analytics
description: Erabili datu-base bat Azure Synapse urtean datu-iturburu gisa Dynamics 365 Customer Insights.
ms.date: 02/24/2022
ms.reviewer: v-wendysmith
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
ms.openlocfilehash: 7c758dccf7ea34dd7b8f80d05eff1ed12030526f
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642123"
---
# <a name="connect-an-azure-synapse-data-source-preview"></a>Konektatu bat Azure Synapse datu-iturburu (aurrebista)

Azure Synapse Analytics datu biltegietan eta datu handien sistemetan informaziorako denbora azkartzen duen enpresa analitika-zerbitzu bat da. Azure Synapse Analytics Enpresako datuen biltegian erabiltzen diren SQL teknologia onenak biltzen ditu, datu handietarako erabiltzen diren Spark teknologiak, Data Explorer erregistro eta denbora serieen analisietarako, Pipelines datuak integratzeko eta ETL/ELT eta integrazio sakona beste Azure zerbitzu batzuekin, esaterako.Power BI,Cosmos DB, eta AzureML.

Informazio gehiagorako, ikus [Azure Synapse ikuspegi orokorra](/azure/synapse-analytics/overview-what-is).

## <a name="prerequisites"></a>Aurrebaldintzak

Konexioa konfiguratzeko ondoko baldintza hauek bete behar dira Dynamics 365 Customer Insights to Azure Synapse.

> [!IMPORTANT]
> Ziurtatu guztiak ezartzen dituzula **funtzioak esleitzea** azaldu bezala.  

## <a name="prerequisites-in-customer-insights"></a>Customer Insights-eko aurrebaldintzak

* Bat daukazu **Administratzailea** Customer Insights-en eginkizuna. Lortu informazio gehiago [erabiltzailearen baimenak Customer Insights-en](permissions.md#assign-roles-and-permissions).

Azure-n: 

- Azure harpidetza aktibo bat.

- Berria erabiliz gero Azure Data Lake Storage Gen2 kontua, *Customer Insights-en zerbitzu nagusia* beharrak **Biltegiratze Blob Datuen Laguntzailea** baimenak. Lortu informazio gehiago [batekin konektatuz Azure Data Lake Storage Customer Insights zerbitzu nagusi batekin](connect-service-principal.md). Data Lake Storage Gen2-k **behar du** [izen-leku hierarkikoa](/azure/storage/blobs/data-lake-storage-namespace) gaituta.

- Baliabide taldean Azure Synapse lan-eremua kokatzen da, *zerbitzu nagusia* eta *Customer Insights-en erabiltzailea* esleitu behar da gutxienez **Irakurlea** baimenak. Informazio gehiagorako, ikusi [Esleitu Azure funtzioak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal).

- *Erabiltzailea* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- *[Azure Synapse laneko eremuaren kudeatutako identitatea](/azure/synapse-analytics/security/synapse-workspace-managed-identity)* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean. Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).

- Gainean Azure Synapse lan-eremua, *Customer Insights-en zerbitzu nagusia* beharrak **Synapse Administratzailea** esleitutako rola. Informazio gehiagorako, ikus [Nola konfiguratu sarbide kontrola zure Synapse laneko areako](/azure/synapse-analytics/security/how-to-set-up-access-control).

## <a name="connect-to-data-lake-databases-in-azure-synapse-analytics"></a>Konektatu data Lake datu-baseetara Azure Synapse Analytics

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Aukeratu **Azure Synapse Analytics (Aurrebista)** metodoa.

1. Eman **Izena** datu-iturburu-erako, eta hautatu **Hurrengoa** datu-iturburu sortzeko. 

1. Aukeratu bat [eskuragarri dagoen konexioa](connections.md) to Azure Synapse Analytics edo sortu berri bat.

1. Aukeratu a **Lake Database** hautatutako lan-espaziotik Azure Synapse Analytics konexioa eta hautatu **Hurrengoa**.

1. Hautatu konektatutako datu-basetik sartu beharreko entitateak. 

1. Aukeran, aukeratu datu-entitateak datuen profila onartzeko. 

1. Hautatu **Gorde** zure hautapena aplikatzeko eta sortu berri den datu-iturburu Lake datu-baseko taulei lotuta dauden datuak sartzen hasteko.Azure Synapse Analytics.
