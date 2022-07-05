---
title: Saioa birbidaltzea Dynamics 365 Customer Insights Azure Monitor-arekin (aurrebista)
description: Ikasi erregistroak nola bidali Microsoft Azure Monitorea.
ms.date: 12/14/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: article
author: brndkfr
ms.author: bkief
manager: shellyha
searchScope:
- ci-system-diagnostic
- customerInsights
ms.openlocfilehash: 8c72df7054a682244215bbee54968d6aef4bbf59
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9052638"
---
# <a name="log-forwarding-in-dynamics-365-customer-insights-with-azure-monitor-preview"></a>Saioa birbidaltzea Dynamics 365 Customer Insights Azure Monitor-arekin (aurrebista)

Dynamics 365 Customer Insights Azure Monitor-ekin integrazio zuzena eskaintzen du. Azure Monitor baliabideen erregistroek erregistroak kontrolatzeko eta hara bidaltzeko aukera ematen dizute [Azure biltegiratzea](https://azure.microsoft.com/services/storage/),[Azure Log Analytics](/azure/azure-monitor/logs/log-analytics-overview), edo igor itzazu [Azure Event Hubs](https://azure.microsoft.com/services/event-hubs/).

Customer Insights-ek gertaeren erregistro hauek bidaltzen ditu:

- **Ikuskaritza Gertaerak**
  - **APIEgertaera** - Aldaketen jarraipena gaitzen du Dynamics 365 Customer Insights UI.
- **Gertaera Operatiboak**
  - **WorkflowEvent** - Lan-fluxuak konfiguratzeko aukera ematen dizu [Datu-iturriak](data-sources.md),[bateratu](data-unification.md),[aberastu](enrichment-hub.md), eta azkenean [esportatu](export-destinations.md) datuak beste sistema batzuetara. Urrats horiek guztiak banaka egin daitezke (adibidez, esportazio bakarra abiarazi). Orkestratuta ere exekutatu daiteke (adibidez, bateratze-prozesua abiarazten duen datu-iturburuetako datuak freskatzea, aberasketak sartu eta datuak beste sistema batera esportatu ondoren). Informazio gehiagorako, ikusi [WorkflowEvent eskema](#workflow-event-schema).
  - **APIEgertaera** - API dei guztiak bezeroen instantziari Dynamics 365 Customer Insights. Informazio gehiagorako, ikusi [APIEgertaera eskema](#api-event-schema).

## <a name="set-up-the-diagnostic-settings"></a>Konfiguratu diagnostiko ezarpenak

### <a name="prerequisites"></a>Aurrebaldintzak

Customer Insights-en diagnostikoak konfiguratzeko, aurrebaldintza hauek bete behar dira:

- Aktibo bat duzu [Azure Harpidetza](https://azure.microsoft.com/pricing/purchase-options/pay-as-you-go/).
- Zuk daukazu [Administratzailea](permissions.md#admin) baimenak Customer Insights-en.
- Zuk daukazu **Laguntzailea** eta **Erabiltzaileen Sarbide Administratzailea** rola Azure-n helmugako baliabidean. Baliabidea an izan daiteke Azure Data Lake Storage kontua, Azure Event Hub bat edo Azure Log Analytics lan-eremu bat. Informazio gehiagorako, ikus [Gehitu edo kendu Azure rol-esleipenak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal). Baimen hau beharrezkoa da Customer Insights-en diagnostiko-ezarpenak konfiguratzen dituzun bitartean, konfiguratu ondoren alda daiteke.
- [Helmugako baldintzak](/azure/azure-monitor/platform/diagnostic-settings#destination-requirements) Azure biltegiratzeko, Azure Event Hub edo Azure Log Analytics-ek betetzen ditu.
- Gutxienez daukazu **Irakurlea** baliabidea dagokion baliabide taldean eginkizuna.

### <a name="set-up-diagnostics-with-azure-monitor"></a>Konfiguratu diagnostikoak Azure Monitor-ekin

1. Customer Insights atalean, hautatu **Sistema** > **Diagnostikoak** instantzia honetan konfiguratutako diagnostiko-helmugak ikusteko.

1. Hautatu **Gehitu helmuga**.

   > [!div class="mx-imgBorder"]
   > ![Diagnostiko konexioa](media/diagnostics-pane.png "Diagnostiko konexioa")

1. Eman izen bat **Diagnostiko-helmugarako izena** eremua.

1. Aukeratu **Maizterrak** Azure harpidetzaren xede-baliabidearekin eta hautatu **saioa hasi**.

1. Hautatu **Baliabide mota** (Biltegiratze-kontua, gertaeren zentroa edo erregistro-analisiak).

1. Hautatu **Harpidetza** helmuga baliabiderako.

1. Hautatu **Baliabide taldea** helmuga baliabiderako.

1. Hautatu **Baliabidea**.

1. Berretsi **Datuen pribatutasuna eta betetzea** adierazpena.

1. Hautatu **Konektatu sistemara** helmugako baliabidera konektatzeko. Erregistroak helmugan agertzen hasten dira 15 minuturen buruan, APIa erabiltzen bada eta gertaerak sortzen baditu.

### <a name="remove-a-destination"></a>Helmuga bat kendu

1. Joan **Sistema** > **Diagnostikoak**.

1. Hautatu diagnostiko-helmuga zerrendan.

1. urtean **Ekintzak** zutabea, hautatu **Ezabatu** ikonoa.

1. Berretsi ezabatzea erregistro-birbidaltzea geldiarazteko. Azure harpidetzako baliabidea ez da ezabatuko. Esteka hauta dezakezu **Ekintzak** zutabea hautatutako baliabiderako Azure ataria ireki eta bertan ezabatzeko.

## <a name="log-categories-and-event-schemas"></a>Erregistro-kategoriak eta gertaeren eskemak

Gaur egun [API gertaerak](apis.md) eta lan-fluxuaren gertaerak onartzen dira eta kategoria eta eskema hauek aplikatzen dira.
Erregistro-eskemak jarraitzen du [Azure Monitor eskema komuna](/azure/azure-monitor/platform/resource-logs-schema#top-level-common-schema).

### <a name="categories"></a>Kategoriak

Customer Insights-ek bi kategoria eskaintzen ditu:

- **Ikuskaritza-gertaerak** :[API gertaerak](#api-event-schema) zerbitzuan konfigurazio-aldaketen jarraipena egiteko. `POST|PUT|DELETE|PATCH` eragiketak kategoria honetan sartzen dira.
- **Gertaera operatiboak** :[API gertaerak](#api-event-schema) edo [lan-fluxuaren gertaerak](#workflow-event-schema) zerbitzua erabiltzean sortutakoa.  Adibidez,`GET` eskaerak edo lan-fluxu baten exekuzio-gertaerak.

## <a name="configuration-on-the-destination-resource"></a>Helmugako baliabidearen konfigurazioa

Baliabide motaren aukeran oinarrituta, urrats hauek automatikoki aplikatuko dira:

### <a name="storage-account"></a>Biltegiratze-kontua

Customer Insights zerbitzu nagusiak eskuratzen du **Biltegiratze-kontuaren laguntzailea** aukeratutako baliabidean baimena eta bi edukiontzi sortzen ditu hautatutako izen-eremuaren azpian:

- `insight-logs-audit` duten **auditoretza ekitaldiak**
- `insight-logs-operational` duten **ekitaldi operatiboak**

### <a name="event-hub"></a>Gertaeren atala

Customer Insights zerbitzu nagusiak eskuratzen du **Azure Event Hubs datuen jabea** baliabidean baimena eta bi Gertaeren Zentro sortuko ditu hautatutako izen-eremuan:

- `insight-logs-audit` duten **auditoretza ekitaldiak**
- `insight-logs-operational` duten **ekitaldi operatiboak**

### <a name="log-analytics"></a>Log Analytics

Customer Insights zerbitzu nagusiak eskuratzen du **Log Analytics Laguntzailea** baliabideari buruzko baimena. Erregistroak azpian egongo dira eskuragarri **Erregistroak** > **Taulak** > **Erregistroen kudeaketa** hautatutako Log Analytics lan-eremuan. Zabaldu **Erregistroen kudeaketa** irtenbidea eta kokatu`CIEventsAudit` eta`CIEventsOperational` mahaiak.

- `CIEventsAudit` duten **auditoretza ekitaldiak**
- `CIEventsOperational` duten **ekitaldi operatiboak**

azpian **Kontsultak** leihoa, zabaldu **Ikuskaritza** irtenbidea eta bilatu bilatuz emandako adibide-kontsultak `CIEvents`.

## <a name="event-schemas"></a>Gertaeren eskemak

APIko gertaerek eta lan-fluxuko gertaerek egitura eta xehetasun komunak dituzte non desberdinak diren, ikusi [API gertaeren eskema](#api-event-schema) edo [lan-fluxuaren gertaeren eskema](#workflow-event-schema).

### <a name="api-event-schema"></a>API gertaeren eskema

| Eremua             | Datu-mota  | Beharrezkoa/Aukerakoa | Deskribapenak       | Adibidez        |
| ----------------- | --------- | ----------------- | --------------------- | ------------------------ |
| `time`            | Denbora-zigilua | Beharrezkoa          | Gertaeraren ordu-zigilua (UTC)       | `2020-09-08T09:48:14.8050869Z`         |
| `resourceId`      | String    | Beharrezkoa          | Gertaera igorri duen instantziaren ResourceId         | `/SUBSCRIPTIONS/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXX/RESOURCEGROUPS/<RESOURCEGROUPNAME>/`<br>`PROVIDERS/MICROSOFT.D365CUSTOMERINSIGHTS/`<br>`INSTANCES/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXX`  |
| `operationName`   | String    | Beharrezkoa          | Gertaera honek adierazten duen eragiketaren izena.                                                                                                                | `Workflows.GetWorkFlowStatusAsync`                                                                                                                                       |
| `category`        | String    | Beharrezkoa          | Gertaeraren erregistro-kategoria. Edota`Operational` edo `Audit`. POST/PUT/PATCH/DELETE HTTP eskaera guztiak etiketatuta daude`Audit`, gainontzeko guztiarekin`Operational` | `2020-09-08T09:48:14.8050869Z`                                                                                                                                           |
| `resultType`      | String    | Beharrezkoa          | Ekitaldiaren egoera. `Success`,`ClientError`,`Failure`                                                                                                        |                                                                                                                                                                          |
| `resultSignature` | String    | Aukerakoa          | Ekitaldiaren emaitzaren egoera. Eragiketa REST API dei bati dagokiona bada, HTTP egoera kodea da.        | `200`             |
| `durationMs`      | Long      | Aukerakoa          | Eragiketaren iraupena milisegundotan.     | `133`     |
| `callerIpAddress` | String    | Aukerakoa          | Deitzailearen IP helbidea, eragiketa publikoki eskuragarri dagoen IP helbide batetik datorren API dei bati badagokio.                                                 | `144.318.99.233`         |
| `identity`        | String    | Aukerakoa          | Eragiketa egin duen erabiltzailearen edo aplikazioaren identitatea deskribatzen duen JSON objektua.       | Ikusi [Identitatea](#identity-schema) atala.     |  
| `properties`      | String    | Aukerakoa          | Gertaeren kategoria jakin baterako propietate gehiago dituen JSON objektua.      | Ikusi [Propietateak](#api-properties-schema) atala.    |
| `level`           | String    | Beharrezkoa          | Gertaeraren larritasun maila.    | `Informational`,`Warning`,`Error`, edo `Critical`.           |
| `uri`             | String    | Aukerakoa          | Eskaera URI absolutua.    |               |

#### <a name="identity-schema"></a>Identitate eskema

The`identity` JSON objektuak honako egitura du

```json
{
  "Authorization" : {
    "UserRole": "Admin",
    "RequiredRoles": [
      "Contributor",
      "Viewer"
      ]
    },
  "Claims" {
    "claimNameX" : "claimValueX",
    "claimNameY" : "claimValueY"
   }
}  
```

| Eremua                         | Deskribapenak                                                                                                                          |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| `Authorization.UserRole`      | Erabiltzaileari edo aplikazioari esleitutako rola. Informazio gehiagorako, ikus [erabiltzailearen baimenak](permissions.md).                                     |
| `Authorization.RequiredRoles` | Eragiketa egiteko beharrezkoak diren rolak. `Admin` rola baimenduta dago eragiketa guztiak egiteko.                                                    |
| `Claims`                      | Erabiltzailearen edo aplikazioaren JSON web token (JWT) erreklamazioak. Erreklamazio-propietateak erakundearen eta erakundearen arabera aldatzen dira Azure Active Directory konfigurazioa. |

#### <a name="api-properties-schema"></a>APIaren propietateen eskema

[API gertaerak](apis.md) ezaugarri hauek dituzte.

| Eremua                        | Deskribapenak                                                                                                            |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `properties.eventType`       | Beti`ApiEvent`, erregistro-gertaera API gertaera gisa markatuz.                                                                 |
| `properties.userAgent`       | Eskaera bidaltzen duen arakatzailearen agentea edo `unknown`.                                                                        |
| `properties.method`          | HTTP metodoa:`GET/POST/PUT/PATCH/HEAD`.                                                                                |
| `properties.path`            | Eskaeraren bide erlatiboa.                                                                                          |
| `properties.origin`          | Eskuratze bat nondik datorren adierazten duen URIa edo `unknown`.                                                                  |
| `properties.operationStatus` | `Success` HTTP egoera kodea < 400 <br> `ClientError` HTTP egoera kodea < 500 <br> `Error` HTTP egoera>= 500 |
| `properties.tenantId`        | Erakundearen IDa                                                                                                        |
| `properties.tenantName`      | Erakundearen izena.                                                                                              |
| `properties.callerObjectId`  | Azure Active Directory Deitzailearen ObjectId.                                                                         |
| `properties.instanceId`      | Bezeroen ikuspegiak`instanceId`                                                                                         |

### <a name="workflow-event-schema"></a>Lan-fluxuaren gertaeren eskema

Lan-fluxuak hainbat urrats ditu. [Hartu datu-iturriak](data-sources.md),[bateratu](data-unification.md),[aberastu](enrichment-hub.md), eta [esportatu](export-destinations.md) datuak. Urrats horiek guztiak banaka edo ondorengo prozesuekin orkestratu daitezke.

#### <a name="operation-types"></a>Eragiketa motak

| OperationType     | Taldekatu                                     |
| ----------------- | ----------------------------------------- |
| Irenstea         | [Datu iturriak](data-sources.md)           |
| Datuak prestatzea   | [Datu iturriak](data-sources.md)           |
| Mapa               | [Datuak bateratzea](data-unification.md)   |
| Lotu             | [Datuak bateratzea](data-unification.md)   |
| Konbinazioa             | [Datuak bateratzea](data-unification.md)   |
| ProfilStore      | [Bezeroen profilak](customer-profiles.md) |
| Bilatu?            | [Bezeroen profilak](customer-profiles.md) |
| Jarduera          | [Jarduerak](activities.md)                  |
| AttributeMeasures | [Segmentuak eta neurriak](segments.md)      |
| Entitatearen neurriak    | [Segmentuak eta neurriak](segments.md)      |
| Neurketak          | [Segmentuak eta neurriak](segments.md)      |
| Segmentazioa      | [Segmentuak eta neurriak](segments.md)      |
| Aberastea        | [Aberastea](enrichment-hub.md)                                          |
| Inteligentzia      | [Iragarpenak](predictions-overview.md)                                          |
| AiBuilder         | [Iragarpenak](predictions-overview.md)                                          |
| Xehetasunak          | [Iragarpenak](predictions-overview.md)                                          |
| Export            | [Esportazioak](export-destinations.md)                                          |
| Ereduen kudeaketa   | [Iragarpenak](custom-models.md)                                           |
| Erlazioaren izena      | [Datuak bateratzea](relationships.md)                                           |

#### <a name="field-description"></a>Eremuaren deskribapena

| Eremua           | Datu-mota  | Beharrezkoa/Aukerakoa | Deskribapenak                                                                                                                                                   | Adibidez                                                                                                                                                                  |
| --------------- | --------- | ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `time`          | Denbora-zigilua | Beharrezkoa          | Gertaeraren ordu-zigilua (UTC).                                                                                                                                 | `2020-09-08T09:48:14.8050869Z`                                                                                                                                           |
| `resourceId`    | String    | Beharrezkoa          | Gertaera igorri duen instantziaren ResourceId.                                                                                                            | `/SUBSCRIPTIONS/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXX/RESOURCEGROUPS/<RESOURCEGROUPNAME>/`<br>`PROVIDERS/MICROSOFT.D365CUSTOMERINSIGHTS/`<br>`INSTANCES/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXX` |
| `operationName` | String    | Beharrezkoa          | Gertaera honek adierazten duen eragiketaren izena. `{OperationType}.[WorkFlow|Task][Started|Completed]`. Ikusi [Eragiketa Motak](#operation-types) erreferentziarako. | `Segmentation.WorkflowStarted`,<br> `Segmentation.TaskStarted`, <br> `Segmentation.TaskCompleted`, <br> `Segmentation.WorkflowCompleted`                                 |
| `category`      | String    | Beharrezkoa          | Gertaeraren erregistro-kategoria. Beti`Operational` Workflow ekitaldietarako                                                                                           | `Operational`                                                                                                                                                            |
| `resultType`    | String    | Beharrezkoa          | Ekitaldiaren egoera. `Running`,`Skipped`,`Successful`,`Failure`                                                                                            |                                                                                                                                                                          |
| `durationMs`    | Long      | Aukerakoa          | Eragiketaren iraupena milisegundotan.                                                                                                                    | `133`                                                                                                                                                                    |
| `properties`    | String    | Aukerakoa          | Gertaeren kategoria jakin baterako propietate gehiago dituen JSON objektua.                                                                                        | Ikus azpiatala [Lan-fluxuaren propietateak](#workflow-properties-schema)                                                                                                       |
| `level`         | String    | Beharrezkoa          | Gertaeraren larritasun maila.                                                                                                                                  | `Informational`, `Warning` edo `Error`                                                                                                                                   |
|                 |

#### <a name="workflow-properties-schema"></a>Lan-fluxuaren propietateen eskema

Lan-fluxuaren gertaerek propietate hauek dituzte.

| Eremua              | Workflow | Zeregina | Deskribapenak            |
| ------------------------------- | -------- | ---- | ----------- |
| `properties.eventType`                       | Yes      | Yes  | Beti`WorkflowEvent`, gertaera lan-fluxuaren gertaera gisa markatuz.                                                                                                                                                                                                |
| `properties.workflowJobId`                   | Yes      | Yes  | Lan-fluxuaren exekuzioaren identifikatzailea. Lan-fluxuaren exekuzioaren barruan dauden lan-fluxu eta ataza-gertaera guztiek gauza bera dute `workflowJobId`.                                                                                                                                   |
| `properties.operationType`                   | Yes      | Yes  | Eragiketaren identifikatzailea, ikus [Eragiketa motak](#operation-types).                                                                                                                                                                               |
| `properties.tasksCount`                      | Yes      | No   | Lan-fluxua soilik. Lan-fluxuak abiarazten dituen ataza kopurua.                                                                                                                                                                                                       |
| `properties.submittedBy`                     | Yes      | No   | Aukerakoa. Lan-fluxuaren gertaerak soilik. The Azure Active Directory [erabiltzailearen objectId](/azure/marketplace/find-tenant-object-id#find-user-object-id) nork eragin zuen lan-fluxua, ikus ere `properties.workflowSubmissionKind`.                                   |
| `properties.workflowType`                    | Yes      | No   | `full` edo`incremental` freskatu.                                                                                                                                                                                                                            |
| `properties.workflowSubmissionKind`          | Yes      | No   | `OnDemand` edo `Scheduled`.                                                                                                                                                                                                                                  |
| `properties.workflowStatus`                  | Yes      | No   | `Running` edo `Successful`.                                                                                                                                                                                                                                 |
| `properties.startTimestamp`                  | Yes      | Yes  | UTC ordu-zigilua`yyyy-MM-ddThh:mm:ss.SSSSSZ`                                                                                                                                                                                                                  |
| `properties.endTimestamp`                    | Yes      | Yes  | UTC ordu-zigilua`yyyy-MM-ddThh:mm:ss.SSSSSZ`                                                                                                                                                                                                                  |
| `properties.submittedTimestamp`              | Yes      | Yes  | UTC ordu-zigilua`yyyy-MM-ddThh:mm:ss.SSSSSZ`                                                                                                                                                                                                                  |
| `properties.instanceId`                      | Yes      | Yes  | Bezeroen ikuspegiak`instanceId`                                                                                                                                                                                                                              |  
| `properties.identifier`                      | No       | Yes  | - OperationType =`Export`, identifikatzailea esportazio-konfigurazioaren gida da. <br> - OperationType =`Enrichment`, aberastearen gidaria da <br> - OperationTyperako`Measures` eta`Segmentation`, identifikatzailea entitatearen izena da. |
| `properties.friendlyName`                    | No       | Yes  | Esportazio edo prozesatzen den entitatearen izen atsegina.                                                                                                                                                                                           |
| `properties.error`                           | No       | Yes  | Aukerakoa. Errore-mezua xehetasun gehiagorekin.                                                                                                                                                                                                                  |
| `properties.additionalInfo.Kind`             | No       | Yes  | Aukerakoa. OperationTyperako`Export` bakarrik. Esportazio mota identifikatzen du. Informazio gehiagorako, ikus [esportazio-helmugen ikuspegi orokorra](export-destinations.md).                                                                                          |
| `properties.additionalInfo.AffectedEntities` | No       | Yes  | Aukerakoa. OperationTyperako`Export` bakarrik. Esportazioan konfiguratutako entitateen zerrenda dauka.                                                                                                                                                            |
| `properties.additionalInfo.MessageCode`      | No       | Yes  | Aukerakoa. OperationTyperako`Export` bakarrik. Esportaziorako mezu zehatza.                                                                                                                                                                                 |
| `properties.additionalInfo.entityCount`      | No       | Yes  | Aukerakoa. OperationTyperako`Segmentation` bakarrik. Segmentuak zenbat kide dituen adierazten du.                                                                                                                                                    |
