---
title: Customer Insights datuak Microsoft Dataverse-n
description: Erabili Customer Insights entitateak taula gisa Microsoft Dataverse-en.
ms.date: 11/25/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
ms.openlocfilehash: 6f74559b34a95ed976a4e353c2dbabe59e1a8839
ms.sourcegitcommit: 9558ff772ee6c944fcb8db4bfc8cda13b38a1bff
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/29/2021
ms.locfileid: "7866919"
---
# <a name="work-with-customer-insights-data-in-microsoft-dataverse"></a>Lan egin Customer Insights datuekin Microsoft Dataverse-en

Customer Insights-ek irteerako entitateak eskuragarri jartzeko aukera eskaintzen du [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro.md). Integrazio honek datuak partekatzeko eta pertsonalizatzeko garapen erraza ahalbidetzen du kode baxuko / koderik gabeko ikuspegiaren bidez. Irteerako entitateak taula gisa egongo dira eskuragarri Dataverse-en. Taula hauek bezalako eszenatokiak ahalbidetzen dituzte [lan-fluxu automatizatuak Power Automate bidez](/power-automate/getting-started),[ereduetan oinarritutako aplikazioak](/powerapps/maker/model-driven-apps/) eta [mihise aplikazioak](/powerapps/maker/canvas-apps/) Power Apps bidez. Datuak Dataverse tauletan oinarritutako beste edozein aplikaziotarako erabil ditzakezu. Uneko inplementazioak batez ere hartzaile eskuragarrien xehetasunen entitateen datuak bezero ID jakin baterako eskuratu daitezkeen bilaketak onartzen ditu.

## <a name="attach-a-dataverse-environment-to-customer-insights"></a>Erantsi Dataverse ingurune bat Customer Insights-era

**Dauden Dataverse inguruneak dituzten erakundeak**

Dagoeneko Dataverse erabiltzen duten erakundeek egin dezakete [erabili lehendik dauden Dataverse inguruneetako bat](create-environment.md) administratzaile batek audientziari buruzko informazioa konfiguratzen duenean. Dataverse inguruneari URLa emanez, haien ikusleei buruzko informazio-ingurune berriari eransten zaio. Ahalik eta errendimendu onena ziurtatzeko, Customer Insights eta Dataverse inguruneak eskualde berean ostatatuta egon behar dira.

**Erakunde berria**

Customer Insights konfiguratzean erakunde berri bat sortzen baduzu, automatikoki Dataverse ingurune berria lortuko duzu.

> [!NOTE]
> Zure erakundeek dagoeneko Dataverse erabiltzen badute maizterrengan, garrantzitsua da gogoratzea [Dataverse ingurunearen sorrera administratzaile batek kontrolatzen du](/power-platform/admin/control-environment-creation.md) . Esate baterako, zure erakunde-kontuarekin audientziari buruzko informazio-ingurune berri bat konfiguratzen ari bazara eta administratzaileak Dataverse proba-inguruneak sortzea desgaitu badu administratzaileentzat izan ezik, ezin duzu proba-ingurune berririk sortu.
> 
> Customer Insights-en sortutako Dataverse proba-inguruneek 3 GB biltegiratzea dute, eta ez dira zenbatuko maizterrak duen ahalmen orokorrean. Ordainpeko harpidetzek Dataverse 15 GB-ko datu-baserako eta 20 GB-ko fitxategiak gordetzeko eskubidea dute.

## <a name="output-entities"></a>Irteerako entitateak

Ikusleen estatistiken irteerako entitate batzuk Dataverse taula gisa daude eskuragarri. Beheko ataletan taula horien itxarondako eskema azaltzen da.

- [Bezero-profila](#customerprofile)
- [AlternateKey](#alternatekey)
- [UnifiedActivity](#unifiedactivity)
- [CustomerMeasure](#customermeasure)
- [Aberastea](#enrichment)
- [Iragarpena](#prediction)
- [Segmentuko kidetasuna](#segment-membership)


### <a name="customerprofile"></a>Bezero-profila

Taula honetan Customer Insights-eko bezeroen profil bateratua dago. Bezeroen profil bateratuaren eskema bateratze prozesuan erabilitako entitateen eta atributuen araberakoa da. Bezeroaren profilaren eskemak normalean atributuen azpimultzo bat dauka [Common Data Model-en CustomerProfile-ri buruzko definiziokoa](/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/customerprofile).

### <a name="alternatekey"></a>AlternateKey

AlternateKey taulan bateratze prozesuan parte hartu duten entitateen gakoak daude.

|Column  |Mota  |Deskribapenak  |
|---------|---------|---------|
|DataSourceName    |String         | Datu-iturburuaren izena. Adibidez: `datasource5`        |
|EntityName        | String        | Hartzaileen xehetasunetako entitatearen izena. Adibidez: `contact1`        |
|AlternateValue    |String         |Bezeroaren IDari esleituta dagoen ID alternatiboa. Adibidez: `cntid_1078`         |
|KeyRing           | Lerro anitzeko testua        | JSON balioa  </br> Lagina: [{"dataSourceName":" datasource5 ",</br>"entityName":" contact1",</br>"preferredKey":" cntid_1078",</br>"gakoak":[" cntid_1078"]}]       |
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

### <a name="segment-membership"></a>Segmentuko kidetasuna

Taula honek bezeroen profilen segmentu-kidetasunaren informazioa dauka.

| Column        | Idatzi | Deskribapenak                        |
|--------------------|--------------|-----------------------------|
| Bezeroaren IDa        | String       | Bezero-profilaren IDa        |
| SegmentProvider      | String       | Segmentuak argitaratzen dituen aplikazioa. Lehenetsia: ikusleen estatistikak         |
| SegmentMembershipType | String       | Bezero mota segmentu honetako kidetzaren erregistroa. Hainbat mota onartzen ditu, hala nola Bezeroa, Kontaktua edo Kontua. Lehenetsia: Bezeroa  |
| Segmentuak       | JSON katea  | Bezeroaren profila kide den segmentu berezien zerrenda      |
| msdynci_identifier  | String   | Segmentuko kidetzaren erregistroaren identifikatzaile bakarra. `CustomerId|SegmentProvider|SegmentMembershipType|Name`  |
| msdynci_segmentmembershipid | GUIDa      | Hemendik sortutako GUID deterministikoa`msdynci_identifier`          |
