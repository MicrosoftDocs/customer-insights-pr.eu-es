---
title: Customer Insights datuak Microsoft Dataverse-n
description: Erabili Customer Insights entitateak taula gisa Microsoft Dataverse-n.
ms.date: 06/15/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
ms.openlocfilehash: 220e01a06711a5d35b8df09e265017a6d8fd0490
ms.sourcegitcommit: 5c9c54ffe045017c19f0042437ada2c101dcaa0f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "6650027"
---
# <a name="work-with-customer-insights-data-in-microsoft-dataverse"></a>Egin lan Customer Insights datuekin Microsoft Dataverse-n

Customer Insights-ek irteerako entitateak hemen eskuragarri jartzeko aukera eskaintzen du: [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro.md). Integrazio honek datuak partekatzeko eta pertsonalizatzeko garapen erraza ahalbidetzen du kode baxuko / koderik gabeko ikuspegiaren bidez. Irteerako entitateak taulan erabilgarri egongo dira Dataverse-n. Taula hauek bezalako agertokiak gaitzen dituzte: [laneko fluxu automatizatuak Power Automate-n](/power-automate/getting-started), [ereduetan oinarritutako aplikazioak](/powerapps/maker/model-driven-apps/) eta [mihise aplikazioak](/powerapps/maker/canvas-apps/) Power Apps-en bidez. Dataverse tauletan oinarritutako beste edozein aplikaziotan erabil ditzakezu datuak. Uneko inplementazioak batez ere hartzaile eskuragarrien xehetasunen entitateen datuak bezero ID jakin baterako eskuratu daitezkeen bilaketak onartzen ditu.

## <a name="attach-a-dataverse-environment-to-customer-insights"></a>Erantsi Dataverse ingurunea Customer Insights-era

**Lehendik dauden Dataverse inguruneak dituzten erakundeak**

Dagoeneko Dataverse erabiltzen duten erakundeek [lehendik dagoen Dataverse inguruneetako bat](get-started-paid.md) erabil dezakete administratzaile batek hartzaileen xehetasunak konfiguratzen dituenean. Dataverse ingurunearen URLa emanez, entzuleen xehetasunen ingurune berriarekin lotzen da. Ahalik eta errendimendu onena bermatzeko, Customer Insights eta Dataverse inguruneek eskualde berean egon behar dute.

Dataverse ingurunea eransteko, zabaldu **Ezarpen aurreratuak** hartzaileen xehetasunen ingurunea sortzerakoan. Eman **Microsoft Dataverse inguruneko URLa** eta hautatu **Gaitu datuak partekatzea** kontrol-laukia.

:::image type="content" source="media/Datasharing-with-DataverseMDL.png" alt-text="alt.":::

**Erakunde berria**

Customer Insights konfiguratzerakoan erakunde berri bat sortzen baduzu, automatikoki Dataverse ingurune berri bat lortuko duzu.

> [!NOTE]
> Zure erakundeek dagoeneko erabiltzen badute Dataverse beren maizterrean, garrantzitsua da gogoratzea [Dataverse ingurunea sortzea administratzaile batek kontrolatzen duela](/power-platform/admin/control-environment-creation.md) . Adibidez, zure erakundearen kontuarekin hartzaileen xehetasunen ingurune berria konfiguratzen ari bazara eta administratzaileak desgaitu badu Dataverse probako inguruneak sortzea administratzaileentzat izan ezik, ezin duzu probako ingurune berririk sortu.
> 
> Customer Insights-en sortutako Dataverse probako inguruneek 3 GB-ko biltegiratzea dute, eta ez dira maizterrari dagokion edukiera osorako balioko. Ordaindutako harpidetzek Dataverse 15 GBko datu-baserako eta 20 GBko fitxategiak biltegiratzeko eskubidea dute.

## <a name="output-entities"></a>Irteerako entitateak

Hartzaileen xehetasunetatik ateratako entitate batzuk taula moduan daude eskuragarri Dataverse-n. Beheko ataletan taula horien itxarondako eskema azaltzen da.

- [Bezero-profila](#customerprofile)
- [AlternateKey](#alternatekey)
- [UnifiedActivity](#unifiedactivity)
- [CustomerMeasure](#customermeasure)
- [Aberastea](#enrichment)
- [Iragarpena](#prediction)


### <a name="customerprofile"></a>Bezero-profila

Taula honetan Customer Insights-eko bezeroen profil bateratua dago. Bezeroen profil bateratuaren eskema bateratze prozesuan erabilitako entitateen eta atributuen araberakoa da. Bezeroaren profilaren eskemak normalean atributuen azpimultzo bat dauka [Common Data Model-en CustomerProfile-ri buruzko definiziokoa](/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/customerprofile).

### <a name="alternatekey"></a>AlternateKey

AlternateKey taulan bateratze prozesuan parte hartu duten entitateen gakoak daude.

|Column  |Mota  |Deskribapenak  |
|---------|---------|---------|
|DataSourceName    |String         | Datu-iturburuaren izena. Adibidez: `datasource5`        |
|EntityName        | String        | Hartzaileen xehetasunetako entitatearen izena. Adibidez: `contact1`        |
|AlternateValue    |String         |Bezeroaren IDari esleituta dagoen ID alternatiboa. Adibidez: `cntid_1078`         |
|KeyRing           | Lerro anitzeko testua        | JSON balioa  </br> Lagina: [{"dataSourceName":" datasource5 ",</br>"entityName":" contact1",</br>"preferredKey":" cntid_1078",</br>"keys":[" cntid_1078"]}]       |
|Bezeroaren IDa         | String        | Bezeroen profil bateratuaren IDa.         |
|AlternateKeyId     | GUIDa         |  AlternateKey GUID determinista msdynci_identifier-en oinarrituta       |
|msdynci_identifier |   String      |   `DataSourceName|EntityName|AlternateValue`  </br> Lagina: `testdatasource|contact1|cntid_1078`    |

### <a name="unifiedactivity"></a>UnifiedActivity

Taula honetan Customer Insights-en eskuragarri dauden erabiltzaileen jarduerak daude.

| Column            | Mota        | Deskribapenak                                                                              |
|-------------------|-------------|------------------------------------------------------------------------------------------|
| Bezeroaren IDa        | String      | Bezero-profilaren IDa                                                                      |
| ActivityId        | String      | Bezeroaren jardueraren barneko IDa (gako nagusia)                                       |
| SourceEntityName  | String      | Iturburuko entitatearen izena                                                                |
| SourceActivityId  | String      | Jatorrizko entitatearen gako nagusia                                                       |
| ActivityType      | String      | Jarduera semantiko mota edo jarduera pertsonalizatuaren izena                                        |
| ActivityTimeStamp | DATETIME    | Jardueraren denbora-zigilua                                                                      |
| Kargua             | String      | Jardueraren izenburua edo izena.                                                               |
| Deskribapenak       | String      | Jardueraren azalpena                                                                     |
| URLa               | String      | Estekatu jardueraren berariazko kanpoko URL batera                                         |
| SemanticData      | JSON katea | Jarduera motari dagozkion esleipen semantikoen eremuetarako balio gakoen bikoteen zerrenda biltzen du |
| RangeIndex        | String      | Unix denbora-marka, jardueren denbora-lerroa eta barruti-kontsulta eraginkorrak ordenatzeko erabiltzen dena |
| mydynci_unifiedactivityid   | GUIDa | Bezeroaren jardueraren barneko IDa (ActivityId) |

### <a name="customermeasure"></a>CustomerMeasure

Taula honetan bezeroaren atributuetan oinarritutako neurrien irteerako datuak daude.

| Column             | Mota             | Deskribapenak                 |
|--------------------|------------------|-----------------------------|
| Bezeroaren IDa         | String           | Bezero-profilaren IDa        |
| Neurketak           | JSON katea      | Neurriaren izena eta emandako bezeroarentzako balioen gako balio bikoteen zerrenda biltzen du | 
| msdynci_identifier | String           | `Customer_Measure|CustomerId` |
| msdynci_customermeasureid | GUIDa      | Bezero-profilaren IDa |


### <a name="enrichment"></a>Aberastea

Taula honetan aberasteko prozesuaren irteera dago.

| Column               | Mota             |  Deskribapenak                                          |
|----------------------|------------------|------------------------------------------------------|
| Bezeroaren IDa           | String           | Bezero-profilaren IDa                                 |
| EnrichmentProvider   | String           | Aberastearen hornitzailearen izena                                  |
| EnrichmentType       | String           | Aberaste mota                                      |
| Balioak               | JSON katea      | Aberasteko prozesuak sortutako atributuen zerrenda |
| msdynci_enrichmentid | GUIDa             | Msdynci_identifier-etik sortutako GUID determinista |
| msdynci_identifier   | String           | `EnrichmentProvider|EnrichmentType|CustomerId`         |

### <a name="prediction"></a>Iragarpena

Taula honetan ereduaren iragarpenen irteera dago.

| Column               | Mota        | Deskribapenak                                          |
|----------------------|-------------|------------------------------------------------------|
| Bezeroaren IDa           | String      | Bezero-profilaren IDa                                  |
| ModelProvider        | String      | Ereduaren hornitzailearen izena                                      |
| Eredua                | String      | Ereduaren izena                                                |
| Balioak               | JSON katea | Ereduak sortutako atributuen zerrenda |
| msdynci_predictionid | GUIDa        | Msdynci_identifier-etik sortutako GUID determinista | 
| msdynci_identifier   | String      |  `Model|ModelProvider|CustomerId`                      |
