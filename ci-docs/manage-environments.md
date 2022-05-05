---
title: Sortu eta kudeatu inguruneak
description: Ikasi zerbitzuan izena ematen eta inguruneak kudeatzen.
ms.date: 03/28/2022
ms.subservice: audience-insights
ms.topic: how-to
ms.reviewer: mhart
author: adkuppa
ms.author: adkuppa
manager: shellyha
searchScope:
- ci-system-about
- customerInsights
ms.openlocfilehash: fcdb7f073ff73322ff69d0a8684391819a809d00
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642152"
---
# <a name="manage-environments"></a>Kudeatu inguruneak

## <a name="switch-environments"></a>Aldatu inguruneak

Hautatu botoia **Ingurumena** kontrol orria orriaren goiko eskuinaldean inguruneak aldatzeko.

:::image type="content" source="media/home-page-environment-switcher.png" alt-text="Inguruaz aldatzeko kontrolaren pantaila-argazkia.":::

Administratzaileek inguruneak [sortu](create-environment.md) eta kudeatu ditzakete.

## <a name="edit-an-existing-environment"></a>Editatu lehendik dagoen ingurunea

Dauden inguruneen xehetasun batzuk editatu ditzakezu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

2.  Hautatu **Editatu** ikonoa.

3. Urtean **Editatu ingurunea** koadroan, ingurunearen ezarpenak egunera ditzakezu.

Informazio gehiago lortzeko ingurune-ezarpenetan, ikusi [Sortu ingurune berri bat](create-environment.md).

## <a name="connect-to-microsoft-dataverse"></a>Konektatu Microsoft Dataverse-ra
   
**Microsoft Dataverse** urratsak Customer Insights zurekin konektatzeko aukera ematen dizu Dataverse ingurunea. 

Eman zurea Microsoft Dataverse Datuak (profilak eta ikuspegiak) oinarritutako negozio-aplikazioekin partekatzeko ingurunea Dataverse, Dynamics 365 Marketing edo ereduetan oinarritutako aplikazioak bezala Power Apps.

Erabiltzeko [kutxaz kanpoko iragarpen modeloak](predictions-overview.md#out-of-box-models), konfiguratu datuak partekatzearekin Dataverse. Edo datuen iradokizuna gaitu dezakezu lokal datu iturrietatik, Microsoft Dataverse zure erakundeak administratzen duen ingurumen URLa.

Datuak partekatzeko aukera gaitu Microsoft Dataverse datuak partekatzeko kontrol-laukia hautatuz gero, zure datu-iturrien eta beste prozesu guztien behin-behineko freskatze osoa abiaraziko da.

> [!IMPORTANT]
> 1. Bezeroen ikuspegiak eta Dataverse Eskualde berean egon behar da datuak partekatzea ahalbidetzeko.
> 1. Administratzaile global rola izan behar duzu Dataverse ingurunea. Egiaztatu hau bada [Dataverse ingurunea lotzen da](/power-platform/admin/control-user-access#associate-a-security-group-with-a-dataverse-environment) segurtasun-talde jakin batzuetara eta ziurtatu segurtasun-talde horietara gehitzen zarela.
> 1. Lehendik dagoen Customer Insights ingurunerik ez dago horrekin lotuta Dataverse ingurunea. Ikasi nola egin [kendu lehendik dagoen konexio bat a Dataverse ingurunea](#remove-an-existing-connection-to-a-dataverse-environment).

:::image type="content" source="media/dataverse-enable-datasharing.png" alt-text="Konfigurazioaren aukerak gaitzeko datuak partekatzeko Microsoft Dataverse.":::

### <a name="enable-data-sharing-with-dataverse-from-your-own-azure-data-lake-storage-preview"></a>Gaitu honekin datuak partekatzea Dataverse zuretik Azure Data Lake Storage (Aurrebista)

Zure ingurunea zurea erabiltzeko konfiguratuta badago Azure Data Lake Storage Customer Insights datuak gordetzeko, datuak partekatzea gaituz Microsoft Dataverse konfigurazio gehigarri bat behar du.

1. Sortu bi segurtasun talde zure Azure harpidetzan - bat **Irakurlea** segurtasun taldea eta bat **Laguntzailea** segurtasun taldea eta ezarri Microsoft Dataverse bi segurtasun taldeen jabe gisa zerbitzua.
2. Kudeatu sarbide-kontrol-zerrenda (ACL) biltegiratze-kontuko CustomerInsights edukiontzian segurtasun talde hauen bidez. Gehitu Microsoft Dataverse zerbitzua eta edozein Dataverse oinarritutako negozio-aplikazioak Dynamics 365 Marketing to the **Irakurlea** segurtasun taldearekin **irakurtzeko soilik** baimenak. Gehitu *bakarrik* Customers Insights aplikaziora **Laguntzailea** segurtasun taldea biak emateko **irakurri eta idatzi** profilak eta ikuspegiak idazteko baimenak.
   
#### <a name="prerequisites"></a>Aurrebaldintzak

PowerShell scriptak exekutatzeko honako hiru modulu hauek inportatu behar dituzu. 

1. Instalatu azken bertsioa [Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).
   1. Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta hautatu **Exekutatu administratzaile gisa**.
   1. Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.
2. Inportatu hiru modulu.
    1. PowerShell leihoan, sartu`Install-Module -Name Az.Accounts` eta jarraitu urratsak. 
    1. Errepikatu`Install-Module -Name Az.Resources` eta `Install-Module -Name Az.Storage`.

#### <a name="configuration-steps"></a>Konfigurazioaren pausoak

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
        - Exekutatu PowerShell script hau Windows PowerShell-en zurea duen Azure harpidetza IDa emanez Azure Data Lake Storage, biltegiratze-kontuaren izena, baliabide-taldearen izena eta Reader eta Contributor segurtasun-taldeen ID balioak. Ireki PowerShell script-a editore batean informazio gehigarria eta inplementatutako logika berrikusteko.
        - Kopiatu irteerako katea scripta behar bezala exekutatu ondoren. Irteerako kateak honela dauka:`https: //DVBYODLDemo/customerinsights?rg=285f5727-a2ae-4afd-9549-64343a0gbabc&cg=720d2dae-4ac8-59f8-9e96-2fa675dbdabc`
        
2. Sartu goitik kopiatutako irteera-katea **Baimenen identifikatzailea** ingurunearen konfigurazio-urratsaren eremua Microsoft Dataverse.

:::image type="content" source="media/dataverse-enable-datasharing-BYODL.png" alt-text="Zure konfigurazio-aukerak datuak partekatzea gaitzeko Azure Data Lake Storage rekin Microsoft Dataverse .":::

Customer Insights-ek ez ditu onartzen hurrengo datuak partekatzeko egoerak:
- Datuak Dataverse-rekin partekatzea gaitzen baduzu, ezin izango duzu [sortu aurreikusitako edo falta diren balioak entitate batean](predictions.md).
- Datuak partekatzea gaitzen baduzu Dataverse, ezin izango duzu ikusi aukerako PowerBI Embedded txostenik zure Customer Insights ingurunean.

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

## <a name="copy-the-environment-configuration"></a>Kopiatu ingurunearen konfigurazioa

Administratzaile gisa, konfigurazioa lehendik dagoen ingurune batetik kopiatzea aukera dezakezu berri bat sortzen duzunean. 

:::image type="content" source="media/environment-settings-dialog.png" alt-text="Ingurumen ezarpenetako ezarpen aukeren pantaila-argazkia.":::

Zure erakundearen eskura dauden ingurune guztien zerrenda ikusiko duzu non datuak kopiatzeko.

Hurrengo konfigurazio ezarpenak kopiatzen dira:

- Hornitutako edo inportatutako datu-iturburuak
- Datuen bateratzea (mapa, bat etorri, batu) konfigurazioa
- Segmentuak
- Neurriak
- Erlazioak
- Jarduerak
- Bilaketa eta iragazkien indizea
- Esportatze-helburuak
- Programatutako freskatzea
- Aberasteak
- Ereduen kudeaketa
- Funtzio-zereginak

## <a name="set-up-a-copied-environment"></a>Konfiguratu kopiatutako ingurune bat

Ingurunearen konfigurazioa kopiatzen duzunean, datu hauek dira *ez* kopiatua:

- Bezeroen profilak.
- Datu-iturburuaren kredentzialak. Datu-iturburu bakoitzerako kredentzialak eman beharko dituzu eta datu iturriak eskuz freskatu.
- Common Data Model karpetako eta Dataverse-k kudeatutako datu-biltegiko datu-iturburuak. Datu iturri horiek eskuz sortu beharko dituzu iturri ingurunean izen berdinekin.
- Esportazioetarako eta aberasteko erabiltzen diren konexio sekretuak. Konexioak berriro autentifikatu eta gero aberasketak eta esportazioak berriro aktibatu behar dituzu. 

Ingurumena kopiatzean, berrespen mezu bat ikusiko duzu ingurune berria sortu dela. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.

Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera. Editatu datu-iturriak eta sartu kredentzialak freskatzeko.

:::image type="content" source="media/data-sources-copied.png" alt-text="Kopiatu ziren eta autentifikazioa behar duten datu iturrien zerrenda.":::

Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.

Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.

Esportazio eta aberasketak berriro aktibatu aurretik, joan hona **Admin** > **Konexioak** zure ingurune berriko konexioak berriro autentifikatzeko.

## <a name="change-the-owner-of-an-environment"></a>Ingurune baten jabea aldatu

Hainbat erabiltzailek Customer Insights-en administratzaile-baimenak izan ditzaketen arren, erabiltzaile bakarra da ingurune baten jabea. Lehenespenez, administratzailea da hasieran ingurune bat sortzen duena. Ingurune baten administratzaile gisa, administratzaile baimenak dituen beste erabiltzaile bati jabetza esleitu diezaiokezu.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu **Editatu** ikonoa.

1. urtean **Editatu ingurunea** kutxa, joan **Oinarrizko informazioa** urratsa.

1. urtean **Ingurunearen jabea aldatu** eremuan, aukeratu ingurunearen jabe berria.  

1. Hautatu **Berrikusi eta amaitu**, orduan **Eguneratu** aldaketak aplikatzeko. 

## <a name="claim-ownership-of-an-environment"></a>Ingurune baten jabetza aldarrikatu

Ingurune baten jabeak erakundea uzten badu edo bere erabiltzaile-kontua ezabatzen bada, inguruneak ez du jaberik izango. Administratzaile-baimenak dituen erabiltzaileak jabetza erreklamatu eta jabe berria izan daiteke. Inguruaren jabe izaten jarraitu dezakete edo [aldatu jabetza beste administratzaile bati](#change-the-owner-of-an-environment). 

Jabetza erreklamatzeko, hautatu **Jabetu** Customer Insights-en orrialde bakoitzaren goialdean agertzen den botoia, jatorrizko jabeak erakundea utzi zuenean.

## <a name="reset-an-existing-environment"></a>Berrezarri lehendik dagoen ingurunea

Ingurune baten jabe gisa, ingurune bat egoera huts batera berrezarri dezakezu konfigurazio guztiak ezabatu eta irentsitako datuak kendu nahi badituzu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan. 

2.  Aukeratu berrezarri nahi duzun ingurunea eta hautatu elipsia (**...**). 

3. Aukeratu **Berrezarri** aukera. 

4.  Ezabapena berresteko, idatzi ingurunearen izena eta hautatu **Berrezarri**.

## <a name="delete-an-existing-environment"></a>Aurretik bazegoen ingurune bat ezabatu

Ingurune baten jabe gisa, zuk kudeatzen duzun ingurune bat ezaba dezakezu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

2.  Aukeratu berrezarri nahi duzun ingurunea eta hautatu elipsia (**...**). 

3. Aukeratu **Ezabatu** aukera. 

4.  Ezabatzea berresteko, idatzi ingurumenaren izena eta hautatu **Ezabatu**.

> [!NOTE]
> Ingurune bat ezabatzeak ez du elkartea kentzen a Dataverse ingurunea.Ikasi [kendu lehendik dagoen konexio bat a Dataverse ingurunea](#remove-an-existing-connection-to-a-dataverse-environment).


[!INCLUDE [footer-include](includes/footer-banner.md)]
