---
title: Egin lan Customer Insights datuekin Microsoft Dataverse-n
description: Ikasi nola konektatu Customer Insights eta Microsoft Dataverse eta esportatzen diren irteerako entitateak ulertu Dataverse.
ms.date: 08/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-system-diagnostic
- customerInsights
ms.openlocfilehash: 9433c411a2c7eb0db137c6392578993d47be82a2
ms.sourcegitcommit: 8559ca47a22d1d7cd9be13531c2eaf0c1083942b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/12/2022
ms.locfileid: "9671236"
---
# <a name="work-with-customer-insights-data-in-microsoft-dataverse"></a>Egin lan Customer Insights datuekin Microsoft Dataverse-n

Customer Insights-ek irteerako entitateak hemen eskuragarri jartzeko aukera eskaintzen du: [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Integrazio honek datuak partekatzeko erraza eta garapen pertsonalizatua ahalbidetzen du kode baxuko/koderik gabeko ikuspegi baten bidez. The [irteerako entitateak](#output-entities) taula gisa eskuragarri daude a Dataverse ingurunea. Datuak oinarritutako beste edozein aplikaziotarako erabil ditzakezu Dataverse mahaiak. Taula hauek lan-fluxu automatizatuak bezalako eszenatokiak ahalbidetzen dituzte Power Automate edo aplikazioak eraikitzearekin Power Apps.

Zurera konektatzen Dataverse inguruneak ere aukera ematen dizu [irensi lokal datu-iturburuetako datuak erabiliz Power Platform datu-fluxuak eta pasabideak](connect-power-query.md#add-data-from-on-premises-data-sources).

## <a name="prerequisites"></a>Aurrebaldintzak

- Bezeroen ikuspegiak eta Dataverse inguruneak eskualde berean egon behar dira.
- Administratzaile rol globala ezarrita dago Dataverse ingurunea. Egiaztatu hau bada [Dataverse ingurunea lotzen da](/power-platform/admin/control-user-access#associate-a-security-group-with-a-dataverse-environment) segurtasun-talde jakin batzuetara eta ziurtatu segurtasun-talde horietan gehitzen zarela.
- Ez dago dagoeneko lotutako beste Customer Insights ingurunerik Dataverse konektatu nahi duzun ingurunea. Ikasi nola egin [kendu lehendik dagoen konexio bat a Dataverse ingurunea](#remove-an-existing-connection-to-a-dataverse-environment).
- A Microsoft Dataverse biltegiratze-kontu bakar batera konektatuta dagoen ingurunea ingurunea horrela konfiguratzen baduzu [erabili zure Azure Data Lake Storage](own-data-lake-storage.md).

## <a name="dataverse-storage-capacity-entitlement"></a>Dataverse biltegiratze ahalmenaren eskubidea

Customer Insights harpidetzak zure erakundearen edukiera gehigarria izateko eskubidea ematen dizu [Dataverse biltegiratze ahalmena](/power-platform/admin/capacity-storage). Gehitutako edukiera zure harpidetzak erabiltzen dituen profil kopuruaren araberakoa da.

**Adibidez:**

15 GB datu-baseen biltegiratzea eta 20 GB fitxategi biltegiratzea lortzen duzula 100.000 bezero-profil bakoitzeko. Zure harpidetzak 300.000 bezero-profil biltzen baditu, zure biltegiratze-ahalmena 45 GB (3 x 15 GB) datu-baseen biltegiratzea eta 60 GB fitxategiak biltegiratzea (3 x 20 GB) da. Era berean, 30K kontu dituen B-to-B harpidetza baduzu, zure biltegiratze-ahalmena 45 GB (3 x 15 GB) datu-baseen biltegiratzea eta 60 GB fitxategi biltegiratzea da (3 x 20 GB).

Erregistro-ahalmena ez da gehitzen eta finkoa zure erakundearentzat.

Edukiera-eskubide zehatzei buruzko informazio gehiago lortzeko, ikus [Dynamics 365 Lizentzien Gida](https://go.microsoft.com/fwlink/?LinkId=866544).

## <a name="connect-a-dataverse-environment-to-customer-insights"></a>Konektatu a Dataverse ingurunea Customer Insights

The **Microsoft Dataverse** urratsak Customer Insights zurearekin konektatzeko aukera ematen dizu Dataverse ingurunea bitartean [Customer Insights ingurune bat sortzea](create-environment.md).

:::image type="content" source="media/dataverse-provisioning.png" alt-text="datuak partekatzearekin Microsoft Dataverse ingurune berrietarako automatikoki gaituta.":::

1. Eman URLa zure Dataverse ingurunea edo utzi hutsik zuretzako sortu dezan.

   > [!NOTE]
   > Customer Insights eta konexioa ezarri ondoren Dataverse, ez aldatu erakundearen izena Dataverse ingurunea. Erakundearen izena erabiltzen da Dataverse URLak eta aldatutako izenak Customer Insights-ekin lotura hausten dute.

   [Power Platform administratzaileek kontrola dezakete nork sor dezakeen berria Dataverse inguruneak](/power-platform/admin/control-environment-creation). Customer Insights ingurune berri bat konfiguratzen saiatzen ari bazara eta ezin baduzu, baliteke administratzaileak desgaitu izana Dataverse denentzako inguruneak administratzaileak izan ezik.

1. Zure Data Lake Storage kontua erabiltzen ari bazara:
   1. Hautatu **Gaitu datuak partekatzea** rekin Dataverse.
   1. Sartu **Baimenen identifikatzailea**. Baimenaren identifikatzailea lortzeko, [gaitu datuak partekatzeko Dataverse zuretik Azure Data Lake Storage](#enable-data-sharing-with-dataverse-from-your-own-azure-data-lake-storage-preview).

## <a name="enable-data-sharing-with-dataverse-from-your-own-azure-data-lake-storage-preview"></a>Gaitu honekin datuak partekatzea Dataverse zuretik Azure Data Lake Storage (aurrebista)

In [zurea Azure Data Lake Storage kontua](own-data-lake-storage.md), egiaztatu erabiltzaileak Customer Insights ingurunea konfiguratzen duela gutxienez **Biltegiratze Blob Datuen irakurgailua** baimenak`customerinsights` biltegiratze kontuan edukiontzia.

> [!NOTE]
> Datuak partekatzea zurea erabiltzen baduzu soilik aplikagarria da Azure Data Lake Storage kontua. Ezarpen hau ez dago erabilgarri Customer Insights inguruneak lehenetsia erabiltzen badu Dataverse biltegiratzea.

### <a name="limitations"></a>Murriztapenak

- Bakarrik bat-bateko mapaketa a artean Dataverse antolakuntza eta an Azure Data Lake Storage kontua. Behin a Dataverse erakundea biltegiratze-kontu batera konektatuta dago, ezin da beste biltegiratze-kontu batera konektatu. Muga horrek eragozten du Dataverse biltegiratze-kontu bat baino gehiago betetzetik.
- Datuak partekatzeak ez du funtzionatuko zure atzitzeko Azure Private Link konfigurazio bat behar bada Azure Data Lake Storage kontua suebaki baten atzean dagoelako. Dataverse Une honetan, ez du onartzen esteka pribatuaren bidez amaierako puntu pribatuetarako konexioa.

### <a name="set-up-security-groups-on-your-own-azure-data-lake-storage"></a>Konfiguratu segurtasun taldeak zure kabuz Azure Data Lake Storage

1. Sortu bi segurtasun talde zure Azure harpidetzan - bat **Irakurlea** segurtasun taldea eta bat **Laguntzailea** segurtasun taldea eta ezarri Microsoft Dataverse bi segurtasun taldeen jabe gisa zerbitzua.

1. Kudeatu Sarbide Kontrol Zerrenda (ACL) aplikazioan`customerinsights` edukiontzia zure biltegiratze kontuan segurtasun talde hauen bidez.
   1. Gehitu Microsoft Dataverse zerbitzua eta edozein Dataverse oinarritutako negozio-aplikazioak Dynamics 365 Marketing to the **Irakurlea** segurtasun taldearekin **irakurtzeko soilik** baimenak.
   1. Gehitu *bakarrik* Customers Insights aplikaziora **Laguntzailea** segurtasun taldea biak emateko **irakurri eta idatzi** profilak eta ikuspegiak idazteko baimenak.

### <a name="set-up-powershell"></a>Konfiguratu PowerShell

Konfiguratu PowerShell PowerShell scriptak exekutatzeko.

1. Instalatu azken bertsioa [Azure Active Directory Graph for PowerShell](/powershell/azure/active-directory/install-adv2).
   1. Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta hautatu **Exekutatu administratzaile gisa**.
   1. Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.

1. Inportatu hiru modulu.
   1. PowerShell leihoan, sartu`Install-Module -Name Az.Accounts` eta jarraitu urratsak.
   1. Errepikatu`Install-Module -Name Az.Resources` eta `Install-Module -Name Az.Storage`.

### <a name="execute-powershell-scripts-and-obtain-the-permission-identifier"></a>Exekutatu PowerShell scriptak eta lortu Baimen Identifikatzailea

1. Deskargatu gure ingeniaritik exekutatu behar dituzun PowerShell script-ak [GitHub repositorioa](https://github.com/trin-msft/byol).
   - `CreateSecurityGroups.ps1`: maizterrak administratzeko baimenak behar ditu.
   - `ByolSetup.ps1`: biltegiratze-kontu/edukiontzi mailan biltegiratze-kontu/edukiontziko biltegiratze-kontu/edukiontziko biltegiratze-datuen jabearen baimenak behar ditu. Script honek zuretzako baimena sortuko du. Zure rol-esleipena eskuz ken daiteke scripta behar bezala exekutatu ondoren.

1. Exekutatu`CreateSecurityGroups.ps1` Windows PowerShell-en zurea duen Azure harpidetza IDa emanez Azure Data Lake Storage. Ireki PowerShell script-a editore batean informazio gehigarria eta inplementatutako logika berrikusteko.

   Script honek bi segurtasun talde sortzen ditu zure Azure harpidetzan: bat Reader taldearentzat eta beste bat Contributor taldearentzat. Microsoft Dataverse zerbitzua da bi segurtasun talde horien jabea.

1. Gorde script honek sortutako segurtasun-taldeen ID balio biak hemen erabiltzeko`ByolSetup.ps1` gidoia.

   > [!NOTE]
   > Segurtasun-taldeen sorrera desgaitu daiteke zure maizterrean. Kasu horretan, eskuzko konfigurazioa beharko litzateke eta zure Azure AD administratzaileak beharko luke [gaitu segurtasun taldeak sortzea](/azure/active-directory/enterprise-users/groups-self-service-management).

1. Exekutatu`ByolSetup.ps1` Windows PowerShell-en zurea duen Azure harpidetza IDa emanez Azure Data Lake Storage, biltegiratze-kontuaren izena, baliabide-taldearen izena eta Reader eta Contributor segurtasun taldearen ID balioak. Ireki PowerShell script-a editore batean informazio gehigarria eta inplementatutako logika berrikusteko.

   Script honek beharrezko roletan oinarritutako sarbide-kontrola gehitzen du Microsoft Dataverse zerbitzua eta edozein Dataverse oinarritutako negozio-aplikazioak. Gainera, Sarbide Kontrol Zerrenda (ACL) eguneratzen du`customerinsights` -rekin sortutako segurtasun taldeentzako edukiontzia`CreateSecurityGroups.ps1` gidoia. Kolaboratzaile taldea ematen da *rwx* baimena eta Irakurle taldea ematen da *rx* baimena soilik.

1. Kopiatu itxura duen irteerako katea:`https://DVBYODLDemo/customerinsights?rg=285f5727-a2ae-4afd-9549-64343a0gbabc&cg=720d2dae-4ac8-59f8-9e96-2fa675dbdabc`

1. Sartu kopiatutako irteera-katea atalean **Baimenen identifikatzailea** ingurunearen konfigurazio-urratsaren eremua Microsoft Dataverse.

   :::image type="content" source="media/dataverse-enable-datasharing-BYODL.png" alt-text="Zure konfigurazio-aukerak datuak partekatzea gaitzeko Azure Data Lake Storage rekin Microsoft Dataverse .":::

## <a name="remove-an-existing-connection-to-a-dataverse-environment"></a>Kendu lehendik dagoen konexio bat a Dataverse ingurunea

Batera konektatzean Dataverse ingurunea, errore-mezua **CDS erakunde hau Customer Insights-en beste instantzia bati atxikita dago jada** esan nahi du Dataverse ingurunea dagoeneko erabiltzen da Customer Insights ingurunean. Lehendik dagoen konexioa kendu dezakezu administratzaile global gisa Dataverse ingurunea. Ordu pare bat behar izan ditzake aldaketak betetzeko.

1. Joan [Power Apps](https://make.powerapps.com)-ra.
1. Hautatu ingurunea ingurune-hautatzailetik.
1. Joan **Irtenbideak**.
1. Desinstalatu edo ezabatu izeneko irtenbidea **Dynamics 365 Customer Insights Bezero txartelaren gehigarria (aurrebista)**.

EDO

1. Ireki zure Dataverse ingurunea.
1. Joan **Ezarpen aurreratuak** > **Irtenbideak**.
1. Desinstalatu **CustomerInsightsCustomerCard** irtenbidea.

Mendekotasunengatik konexioa kentzeak huts egiten badu, mendekotasunak ere kendu behar dituzu. Informazio gehiagorako, ikus [Mendekotasunak kentzea](/power-platform/alm/removing-dependencies).

## <a name="output-entities"></a>Irteerako entitateak

Customer Insights-en irteerako entitate batzuk taula gisa daude eskuragarri Dataverse. Beheko ataletan taula horien itxarondako eskema azaltzen da.

- [Bezero-profila](#customerprofile)
- [ContactProfile](#contactprofile)
- [AlternateKey](#alternatekey)
- [UnifiedActivity](#unifiedactivity)
- [CustomerMeasure](#customermeasure)
- [Aberastea](#enrichment)
- [Iragarpena](#prediction)
- [Segmentuko kidetasuna](#segment-membership)

### <a name="customerprofile"></a>Bezero-profila

Taula honetan Customer Insights-eko bezeroen profil bateratua dago. Bezeroen profil bateratu baten eskema datuak bateratzeko prozesuan erabiltzen diren entitate eta atributuen araberakoa da. Bezeroaren profilaren eskemak normalean atributuen azpimultzo bat dauka [Common Data Model-en CustomerProfile-ri buruzko definiziokoa](/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/solutions/customerinsights/customerprofile). B-to-B eszenatokirako, bezeroaren profilak kontu bateratuak ditu, eta eskemak normalean atributuen azpimultzo bat dauka.[Kontuaren datu-eredu komunaren definizioa](/common-data-model/schema/core/applicationcommon/foundationcommon/crmcommon/account).

### <a name="contactprofile"></a>ContactProfile

ContactProfile batek kontaktu bati buruzko informazio bateratua dauka. Kontaktuak dira [kontu batean mapatutako pertsonak](data-unification-contacts.md) B-to-B eszenatoki batean.

| Column                       | Idatzi                | Deskribapenak     |
| ---------------------------- | ------------------- | --------------- |
|  Urtebetetze data            | DateTime       |  Kontaktuaren jaioteguna               |
|  Hiria                 | Testu-mezua |  Harremanetarako helbidearen hiria               |
|  Kontaktu ID            | Testu-mezua |  Kontaktu-profilaren IDa               |
|  KontaktuProfileId     | Identifikatzaile esklusiboa   |  Kontaktuaren GUID               |
|  HerrialdeaEdoEskualdea      | Testu-mezua |  Harremanetarako helbidearen herrialdea/eskualdea               |
|  Bezeroaren IDa           | Testu-mezua |  Kontaktua mapatutako kontuaren IDa               |
|  EntityName           | Testu-mezua |  Datuak nondik datozen entitatea                |
|  FirstName            | Testu-mezua |  Kontaktuaren izen               |
|  Generoa               | Testu-mezua |  Kontaktuaren generoa               |
|  IDa                   | Testu-mezua |  GUID deterministikoan oinarrituta`Identifier`               |
|  Identifikatzailea           | Testu-mezua |  Kontaktu-profilaren barne IDa:`ContactProfile|CustomerId|ContactId`               |
|  JobTitle             | Testu-mezua |  Kontaktuaren lanpostuaren izena               |
|  LastName             | Testu-mezua |  Kontaktuaren abizen               |
|  PostalCode           | Testu-mezua |  Kontaktuaren helbidearen posta-kodea               |
|  Helbide elektroniko nagusia         | Testu-mezua |  Kontaktuaren helbide elektronikoa               |
|  Lehen Telefonoa         | Testu-mezua |  Kontaktuaren telefono zenbakia               |
|  StateOrProvince      | Testu-mezua |  Harremanetarako helbidearen estatua edo probintzia               |
|  Helbidea        | Testu-mezua |  Harremanetarako helbidearen kalea               |

### <a name="alternatekey"></a>AlternateKey

AlternateKey taulan bateratze prozesuan parte hartu duten entitateen gakoak daude.

|Column  |Idatzi  |Deskribapenak  |
|---------|---------|---------|
|DataSourceName    |Testu-mezua         | Datu-iturburuaren izena. Adibidez: `datasource5`        |
|EntityName        | Testu-mezua        | Customer Insights-en entitatearen izena. Adibidez: `contact1`        |
|AlternateValue    |Testu-mezua         |Bezeroaren IDari esleituta dagoen ID alternatiboa. Adibidez: `cntid_1078`         |
|KeyRing           | Testu-mezua        | JSON balioa  </br> Lagina: [{"dataSourceName":" datasource5 ",</br>"entityName":" contact1",</br>"preferredKey":" cntid_1078",</br>"keys":[" cntid_1078"]}]       |
|Bezeroaren IDa         | Testu-mezua        | Bezeroen profil bateratuaren IDa.         |
|AlternateKeyId     | Identifikatzaile esklusiboa        |  AlternateKey-n oinarritutako GUID deterministikoa`Identifier`      |
|Identifikatzailea |   Testu-mezua      |   `DataSourceName|EntityName|AlternateValue`  </br> Lagina: `testdatasource|contact1|cntid_1078`    |

### <a name="unifiedactivity"></a>UnifiedActivity

Taula honetan Customer Insights-en eskuragarri dauden erabiltzaileen jarduerak daude.

| Column            | Idatzi        | Deskribapenak                                                                              |
|-------------------|-------------|------------------------------------------------------------------------------------------|
| Bezeroaren IDa        | Testu-mezua      | Bezero-profilaren IDa                                                                      |
| ActivityId        | Testu-mezua      | Bezeroaren jardueraren barneko IDa (gako nagusia)                                       |
| SourceEntityName  | Testu-mezua      | Iturburuko entitatearen izena                                                                |
| SourceActivityId  | Testu-mezua      | Jatorrizko entitatearen gako nagusia                                                       |
| ActivityType      | Testu-mezua      | Jarduera semantiko mota edo jarduera pertsonalizatuaren izena                                        |
| ActivityTimeStamp | DateTime    | Jardueraren denbora-zigilua                                                                      |
| lanpostua             | Testu-mezua      | Jardueraren izenburua edo izena.                                                               |
| Deskribapenak       | Testu-mezua      | Jardueraren azalpena                                                                     |
| URLa               | Testu-mezua      | Estekatu jardueraren berariazko kanpoko URL batera                                         |
| SemanticData      | Testu-mezua | Jarduera motari dagozkion esleipen semantikoen eremuetarako balio gakoen bikoteen zerrenda biltzen du |
| RangeIndex        | Testu-mezua      | Unix denbora-marka, jardueren denbora-lerroa eta barruti-kontsulta eraginkorrak ordenatzeko erabiltzen dena |
| UnifiedActivityId   | Identifikatzaile esklusiboa | Bezeroaren jardueraren barneko IDa (ActivityId) |

### <a name="customermeasure"></a>CustomerMeasure

Taula honetan bezeroaren atributuetan oinarritutako neurrien irteerako datuak daude.

| Column             | Idatzi             | Deskribapenak                 |
|--------------------|------------------|-----------------------------|
| Bezeroaren IDa         | Testu-mezua           | Bezero-profilaren IDa        |
| Neurketak           | Testu-mezua      | Neurriaren izena eta emandako bezeroarentzako balioen gako balio bikoteen zerrenda biltzen du |
| Identifikatzailea | Testu-mezua           | `Customer_Measure|CustomerId` |
| CustomerMeasureId | Identifikatzaile esklusiboa     | Bezero-profilaren IDa |

### <a name="enrichment"></a>Aberastea

Taula honetan aberasteko prozesuaren irteera dago.

| Column               | Idatzi             |  Deskribapenak                                          |
|----------------------|------------------|------------------------------------------------------|
| Bezeroaren IDa           | Testu-mezua           | Bezero-profilaren IDa                                 |
| EnrichmentProvider   | Testu-mezua           | Aberastearen hornitzailearen izena                                  |
| EnrichmentType       | Testu-mezua           | Aberaste mota                                      |
| Balioak               | Testu-mezua      | Aberasteko prozesuak sortutako atributuen zerrenda |
| AberasteId | Identifikatzaile esklusiboa            | Hemendik sortutako GUID deterministikoa`Identifier` |
| Identifikatzailea   | Testu-mezua           | `EnrichmentProvider|EnrichmentType|CustomerId`         |

### <a name="prediction"></a>Iragarpena

Taula honetan ereduaren iragarpenen irteera dago.

| Column               | Idatzi        | Deskribapenak                                          |
|----------------------|-------------|------------------------------------------------------|
| Bezeroaren IDa           | Testu-mezua      | Bezero-profilaren IDa                                  |
| ModelProvider        | Testu-mezua      | Ereduaren hornitzailearen izena                                      |
| Eredua                | Testu-mezua      | Ereduaren izena                                                |
| Balioak               | Testu-mezua | Ereduak sortutako atributuen zerrenda |
| IragarpenId | Identifikatzaile esklusiboa       | Hemendik sortutako GUID deterministikoa`Identifier` |
| Identifikatzailea   | Testu-mezua      |  `Model|ModelProvider|CustomerId`                      |

### <a name="segment-membership"></a>Segmentuko kidetasuna

Taula honek bezeroen profilen segmentu-kidetasunaren informazioa dauka.

| Column        | Idatzi | Deskribapenak                        |
|--------------------|--------------|-----------------------------|
| Bezeroaren IDa        | Testu-mezua       | Bezero-profilaren IDa        |
| SegmentProvider      | Testu-mezua       | Segmentuak argitaratzen dituen aplikazioa.      |
| SegmentMembershipType | Testu-mezua       | Segmentu honetako kidetzaren erregistroko bezero mota. Hainbat mota onartzen ditu, hala nola Bezeroa, Kontaktua edo Kontua. Lehenetsia: Bezeroa  |
| Segmentuak       | Testu-mezua  | Bezeroaren profila kide den segmentu berezien zerrenda      |
| Identifikatzailea  | Testu-mezua   | Segmentuko kidetzaren erregistroaren identifikatzaile bakarra. `CustomerId|SegmentProvider|SegmentMembershipType|Name`  |
| Segmentaren Kide-Id | Identifikatzaile esklusiboa      | Hemendik sortutako GUID deterministikoa`Identifier`          |

[!INCLUDE [footer-include](includes/footer-banner.md)]
