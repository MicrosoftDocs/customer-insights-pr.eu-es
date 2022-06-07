---
title: Egin lan Customer Insights datuekin Microsoft Dataverse-n
description: Ikasi nola konektatu Customer Insights eta Microsoft Dataverse eta esportatzen diren irteerako entitateak ulertu Dataverse.
ms.date: 05/30/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-system-diagnostic
- customerInsights
ms.openlocfilehash: 3848e143bc7cb2f345bc698a274b92148ef00669
ms.sourcegitcommit: f5af5613afd9c3f2f0695e2d62d225f0b504f033
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/01/2022
ms.locfileid: "8833661"
---
# <a name="work-with-customer-insights-data-in-microsoft-dataverse"></a>Egin lan Customer Insights datuekin Microsoft Dataverse-n

Customer Insights-ek irteerako entitateak gisa erabilgarri jartzeko aukera eskaintzen du [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Integrazio honek datuak partekatzeko erraza eta garapen pertsonalizatua ahalbidetzen du kode baxuko/koderik gabeko ikuspegi baten bidez. The [irteerako entitateak](#output-entities) taula gisa eskuragarri daude a Dataverse ingurunea. Datuak oinarritutako beste edozein aplikaziotarako erabil ditzakezu Dataverse mahaiak. Taula hauek lan-fluxu automatizatuak bezalako eszenatokiak ahalbidetzen dituzte Power Automate edo aplikazioak eraikitzearekin Power Apps.

Zurera konektatzen Dataverse inguruneak ere aukera ematen dizu [irensi lokal datu-iturburuetako datuak erabiliz Power Platform datu-fluxuak eta pasabideak](data-sources.md#add-data-from-on-premises-data-sources).

## <a name="prerequisites"></a>Aurrebaldintzak

- Bezeroen ikuspegiak eta Dataverse inguruneak eskualde berean egon behar dira.
- Administratzaile rol globala izan behar duzu Dataverse ingurunea. Egiaztatu hau bada [Dataverse ingurunea lotzen da](/power-platform/admin/control-user-access#associate-a-security-group-with-a-dataverse-environment) segurtasun-talde jakin batzuetara eta ziurtatu segurtasun-talde horietan gehitzen zarela.
- Ez dago beste Customer Insights ingurunerik dagoeneko lotuta Dataverse konektatu nahi duzun ingurunea. Ikasi nola egin [kendu lehendik dagoen konexio bat a Dataverse ingurunea](#remove-an-existing-connection-to-a-dataverse-environment).
- A Microsoft Dataverse ingurunea biltegiratze-kontu bakar batera bakarrik konekta daiteke. Ingurunea konfiguratzen baduzu soilik aplikatzen da [erabili zure Azure Data Lake Storage](own-data-lake-storage.md).

## <a name="connect-a-dataverse-environment-to-customer-insights"></a>Konektatu a Dataverse ingurunea Customer Insights

The **Microsoft Dataverse** urratsak Customer Insights zurearekin konektatzeko aukera ematen dizu Dataverse ingurunea bitartean [Customer Insights ingurunea sortzea](create-environment.md).

:::image type="content" source="media/dataverse-provisioning.png" alt-text="datuak partekatzearekin Microsoft Dataverse sareko ingurune berrietarako automatikoki gaituta.":::

Administratzaileek Customer Insights konfigura dezakete lehendik dagoen bat konektatzeko Dataverse ingurunea. URLa emanez Dataverse ingurunea, bere Customer Insights ingurune berrira atxikitzen ari da.

Lehendik dagoen bat erabili nahi ez baduzu Dataverse ingurunea, sistemak ingurune berri bat sortzen du zure maizterren Customer Insights datuetarako. [Power Platform administratzaileek inguruneak nork sor ditzakeen kontrola dezakete](/power-platform/admin/control-environment-creation). Customer Insights ingurune berri bat konfiguratzen ari zarenean eta administratzaileak hau sortzea desgaitu duenean Dataverse administratzaileentzat izan ezik, ezingo duzu ingurune berririk sortu.

**Gaitu datuak partekatzea** rekin Dataverse datuak partekatzeko kontrol-laukia hautatuta.

Zure Data Lake Storage kontua erabiltzen ari bazara, hau ere behar duzu **Baimenen identifikatzailea**. Baimen-identifikatzailea nola lortu informazio gehiago lortzeko, berrikusi hurrengo atala.

## <a name="enable-data-sharing-with-dataverse-from-your-own-azure-data-lake-storage-preview"></a>Gaitu honekin datuak partekatzea Dataverse zuretik Azure Data Lake Storage (Aurrebista)

Datuak partekatzeko aukera gaitu Microsoft Dataverse zure ingurunea denean [zurea erabiltzen du Azure Data Lake Storage kontua](own-data-lake-storage.md) konfigurazio gehigarri bat behar du. Customer Insights ingurunea konfiguratzen duen erabiltzaileak gutxienez eduki behar du **Biltegiratze Blob Datuen irakurgailua** buruzko baimenak *CustomerInsights* edukiontzian Azure Data Lake Storage kontua.

1. Sortu bi segurtasun talde zure Azure harpidetzan - bat **Irakurlea** segurtasun taldea eta bat **Laguntzailea** segurtasun taldea eta ezarri Microsoft Dataverse bi segurtasun taldeen jabe gisa zerbitzua.
2. Kudeatu sarbide-kontrol-zerrenda (ACL) biltegiratze-kontuko CustomerInsights edukiontzian segurtasun talde hauen bidez. Gehitu Microsoft Dataverse zerbitzua eta edozein Dataverse oinarritutako negozio-aplikazioak Dynamics 365 Marketing to the **Irakurlea** segurtasun taldearekin **irakurtzeko soilik** baimenak. Gehitu *bakarrik* Customers Insights aplikaziora **Laguntzailea** segurtasun taldea biak emateko **irakurri eta idatzi** profilak eta ikuspegiak idazteko baimenak.

### <a name="limitations"></a>Murriztapenak

Erabiltzerakoan bi muga daude Dataverse zurearekin Azure Data Lake Storage kontua:

- A-ren arteko bat-bateko mapeoa dago Dataverse antolakuntza eta an Azure Data Lake Storage kontua. Behin a Dataverse erakundea biltegiratze-kontu batera konektatuta dago, ezin da beste biltegiratze-kontu batera konektatu. Muga horrek eragozten du a Dataverse ez ditu biltegiratze-kontu bat baino gehiago betetzen.
- Datuak partekatzeak ez du funtzionatuko Azure Private Link konfigurazio bat behar bada zure Azure Data Lake biltegiratze-kontura sartzeko, suebaki baten atzean dagoelako. Dataverse Une honetan ez du onartzen esteka pribatuaren bidez amaierako puntu pribatuetarako konexioa.

### <a name="set-up-powershell"></a>Konfiguratu PowerShell

PowerShell script-ak exekutatzeko, lehenik eta behin PowerShell horren arabera konfiguratu behar duzu.

1. Instalatu azken bertsioa [Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).
   1. Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta hautatu **Exekutatu administratzaile gisa**.
   1. Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.
2. Inportatu hiru modulu.
    1. PowerShell leihoan, sartu`Install-Module -Name Az.Accounts` eta jarraitu urratsak.
    1. Errepikatu`Install-Module -Name Az.Resources` eta `Install-Module -Name Az.Storage`.

### <a name="configuration-steps"></a>Konfigurazioaren pausoak

1. Deskargatu gure ingeniaritik exekutatu behar dituzun PowerShell script-ak [GitHub repositorioa](https://github.com/trin-msft/byol).
    1. `CreateSecurityGroups.ps1`
       - Behar duzu *maizter admin* PowerShell script hau exekutatzeko baimenak.
       - PowerShell script honek bi segurtasun talde sortzen ditu zure Azure harpidetzan. Bat Irakurle taldearentzat eta beste bat Kolaboratzaile taldearentzat eta egingo du Microsoft Dataverse Zerbitzua bi segurtasun talde hauen jabe gisa.
       - Exekutatu PowerShell script hau Windows PowerShell-en zurea duen Azure harpidetza IDa emanez Azure Data Lake Storage. Ireki PowerShell script-a editore batean informazio gehigarria eta inplementatutako logika berrikusteko.
       - Gorde script honek sortutako segurtasun-taldeen ID balioak, hauek erabiliko ditugulako`ByolSetup.ps1` gidoia.

        > [!NOTE]
        > Segurtasun-taldeen sorrera desgaitu daiteke maizterrean. Kasu horretan, eskuzko konfigurazioa beharko litzateke eta zure Azure AD administratzaileak beharko luke [gaitu segurtasun taldeak sortzea](/azure/active-directory/enterprise-users/groups-self-service-management).

    2. `ByolSetup.ps1`
        - Behar duzu *Biltegiratze Blob Datuen jabea* biltegiratze kontu/edukiontzi mailan baimenak script hau exekutatzeko edo script honek bat sortuko dizu. Zure rol-esleipena eskuz ken daiteke scripta behar bezala exekutatu ondoren.
        - PowerShell script honek tolean oinarritutako sarbide-kontrola (RBAC) gehitzen du Microsoft Dataverse zerbitzua eta edozein Dataverse oinarritutako negozio-aplikazioak. Era berean, Sarbide Kontrol Zerrenda (ACL) eguneratzen du CustomerInsights edukiontzian sortutako segurtasun taldeetarako.`CreateSecurityGroups.ps1` gidoia. Kolaboratzaile taldeak izango du *rwx* baimena eta Irakurle taldeak izango du *rx* baimena soilik.
        - Exekutatu PowerShell script hau Windows PowerShell-en zurea duen Azure harpidetza IDa emanez Azure Data Lake Storage, biltegiratze-kontuaren izena, baliabide-taldearen izena eta Reader eta Contributor segurtasun taldearen ID balioak. Ireki PowerShell script-a editore batean informazio gehigarria eta inplementatutako logika berrikusteko.
        - Kopiatu irteerako katea scripta behar bezala exekutatu ondoren. Irteerako kateak honela dauka:`https://DVBYODLDemo/customerinsights?rg=285f5727-a2ae-4afd-9549-64343a0gbabc&cg=720d2dae-4ac8-59f8-9e96-2fa675dbdabc`

2. Sartu goitik kopiatutako irteera-katea **Baimenen identifikatzailea** ingurunearen konfigurazio-urratsaren eremua Microsoft Dataverse.

:::image type="content" source="media/dataverse-enable-datasharing-BYODL.png" alt-text="Zure konfigurazio-aukerak datuak partekatzea gaitzeko Azure Data Lake Storage rekin Microsoft Dataverse .":::

### <a name="remove-an-existing-connection-to-a-dataverse-environment"></a>Kendu lehendik dagoen konexio bat a Dataverse ingurunea

Batera konektatzean Dataverse ingurunea, errore-mezua **CDS erakunde hau Customer Insights-en beste instantzia bati atxikita dago jada** esan nahi du Dataverse ingurunea dagoeneko erabiltzen da Customer Insights ingurunean. Lehendik dagoen konexioa kendu dezakezu administratzaile global gisa Dataverse ingurunea. Ordu pare bat behar izan ditzake aldaketak betetzeko.

1. Joan [Power Apps](https://make.powerapps.com)-ra.
1. Hautatu ingurunea ingurune-hautatzailetik.
1. Joan **Irtenbideak**
1. Desinstalatu edo ezabatu izeneko soluzioa **Dynamics 365 Customer Insights Bezero txartelaren gehigarria (aurrebista)**.

EDO

1. Ireki zure Dataverse ingurunea.
1. Joan **Ezarpen aurreratuak** > **Irtenbideak**.
1. Desinstalatu **CustomerInsightsCustomerCard** irtenbidea.

Menpekotasunengatik konexioa kentzeak huts egiten badu, mendekotasunak ere kendu behar dituzu. Informazio gehiagorako, ikus [Mendekotasunak kentzea](/power-platform/alm/removing-dependencies).

## <a name="output-entities"></a>Irteerako entitateak

Customer Insights-en irteerako entitate batzuk taula gisa eskuragarri daude Dataverse. Beheko ataletan taula horien itxarondako eskema azaltzen da.

- [Bezero-profila](#customerprofile)
- [AlternateKey](#alternatekey)
- [UnifiedActivity](#unifiedactivity)
- [CustomerMeasure](#customermeasure)
- [Aberastea](#enrichment)
- [Iragarpena](#prediction)
- [Segmentuko kidetasuna](#segment-membership)

### <a name="customerprofile"></a>Bezero-profila

Taula honetan Customer Insights-eko bezeroen profil bateratua dago. Bezeroen profil bateratuaren eskema datuak bateratzeko prozesuan erabiltzen diren entitateen eta atributuen araberakoa da. Bezeroaren profilaren eskemak normalean atributuen azpimultzo bat dauka [Common Data Model-en CustomerProfile-ri buruzko definiziokoa](/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/customerprofile).

### <a name="alternatekey"></a>AlternateKey

AlternateKey taulan bateratze prozesuan parte hartu duten entitateen gakoak daude.

|Column  |Mota  |Deskribapenak  |
|---------|---------|---------|
|DataSourceName    |String         | Datu-iturburuaren izena. Adibidez: `datasource5`        |
|EntityName        | String        | Customer Insights-en entitatearen izena. Adibidez: `contact1`        |
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

### <a name="segment-membership"></a>Segmentuko kidetasuna

Taula honek bezeroen profilen segmentu-kidetasunaren informazioa dauka.

| Column        | Idatzi | Deskribapenak                        |
|--------------------|--------------|-----------------------------|
| Bezeroaren IDa        | String       | Bezero-profilaren IDa        |
| SegmentProvider      | String       | Segmentuak argitaratzen dituen aplikazioa.      |
| SegmentMembershipType | String       | Bezero mota segmentu honetako kidetzaren erregistroa. Hainbat mota onartzen ditu, hala nola Bezeroa, Kontaktua edo Kontua. Lehenetsia: Bezeroa  |
| Segmentuak       | JSON katea  | Bezeroaren profila kide den segmentu berezien zerrenda      |
| msdynci_identifier  | String   | Segmentuko kidetzaren erregistroaren identifikatzaile bakarra. `CustomerId|SegmentProvider|SegmentMembershipType|Name`  |
| msdynci_segmentmembershipid | GUIDa      | Hemendik sortutako GUID deterministikoa`msdynci_identifier`          |

<!--
## FAQ: Update existing environments to use Microsoft Dataverse

Between mid-May 2022 and June 13, 2022, administrators can update the environment settings with a Dataverse environment that Customer Insights can use. On June 13, 2022, your environment will be updated automatically and we'll create a Dataverse environment on your tenant for you.

1. My environment uses my own Azure Data Lake Storage account. Do I still need to update?

   If there's already a Dataverse environment configured in your environment, the update isn't required. If no Dataverse is environment configured, the **Update now** button will create a Dataverse environment and update from the Customer Insights database to a Dataverse database.

1. Will we get extra Dataverse capacity, or will the update use my existing Dataverse capacity?

   - If there's already a Dataverse environment configured in your Customer Insights environment, or connected with other Dynamics 365 or Power Apps applications, the capacity remains unchanged.
   - If the Dataverse environment is new, it will add new storage and database capacity. The capacity added varies per environment and entitlements. You'll get 3 GB for trial and sandbox environment. Production environments get 15 GB.

1. I proceeded with the update and it seems like nothing happened. Is the update complete?

   If the notification in Customer Insights doesn't show anymore, the update is complete. You can check the status of the update by reviewing your environment settings.

1. Why do I still see the banner after completing the update steps?

   It can happen due to an upgrade or refresh failure. Contact support.

1. I received a "Failed to provision Dataverse environment" error after starting the update. What happened?

   It can happen due to an upgrade or refresh failure. Contact support.
   Common causes:
    - Insufficient capacity. There's no more capacity to create more environments. For more information, see [Manage capacity action](/power-platform/admin/capacity-storage#actions-to-take-for-a-storage-capacity-deficit).
    - Region mismatch between tenant region and Customer Insights environment region in the Australia and India regions.
    - Insufficient privileges to provision Dataverse. The users starting the update needs a Dynamics 365 admin role.
    - -->
