---
title: Sortu inguruneak Customer Insights-en
description: Lizentziapeko harpidetza duten inguruneak sortzeko urratsak Dynamics 365 Customer Insights.
ms.date: 04/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.custom: intro-internal
searchScope:
- ci-home
- customerInsights
ms.openlocfilehash: c64ac94a7e0e743d3c13e32e394cc5d409420622
ms.sourcegitcommit: c00441bc60b978e25f930b06c9d97b46fe462538
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712887"
---
# <a name="create-an-environment-in-customer-insights"></a>Sortu ingurune bat Customer Insights-en

Artikulu honetan zure erakundeak Dynamics 365 Customer Insights harpidetza erosi ondoren ingurune berri bat nola sortu azaltzen da. 

Erakundeek hainbat ingurune sor ditzakete Customer Insights lizentzia bakoitzeko. Zure erakundeak lizentzia bat baino gehiago erosten badu, [jarri harremanetan gure laguntza taldearekin](https://go.microsoft.com/fwlink/?linkid=2079641) erabilgarri dauden ingurune kopurua handitzeko. Edukierari eta gehigarriei buruzko informazio gehiago lortzeko, berrikusi [Dynamics 365 lizentzien gida](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Zerbitzua probatu nahi baduzu, ikusi [Konfiguratu proba ingurunea](trial-signup.md).

## <a name="create-a-new-environment"></a>Sortu ingurune bat

Customer Insights-erako harpidetza-lizentzia bat erosi ondoren, honen administratzaile globalak Microsoft 365 maizterrak ingurunea sortzera gonbidatzen duen mezu elektroniko bat jasotzen du. Erabiltzen hasteko, joan hona: [https://home.ci.ai.dynamics.com/start](https://home.ci.ai.dynamics.com/start). 

Esperientzia gidatu batek ingurune berri baterako beharrezko informazio guztia biltzeko urratsak egiten laguntzen dizu. Behar duzu [administratzaile-baimenak](permissions.md) Customer Insights-en inguruneak sortzeko edo kudeatzeko.

1. Ireki ingurune-hautatzailea eta hautatu **+ Berria**.
  
   :::image type="content" source="media/environment-picker.png" alt-text="Hautatu ingurunearen hautatzailea.":::

1. Jarraitu hurrengo ataletan azaldutako esperientzia gidatua.

### <a name="step-1-provide-environment-information"></a>1. urratsa: ingurumenari buruzko informazioa eman

Urtean **Oinarrizko informazioa** urratsa, aukeratu hutsetik ingurunea sortu nahi duzun edo [kopiatu datuak beste ingurune batetik](manage-environments.md#copy-the-environment-configuration).

   :::image type="content" source="media/environment-settings-dialog.png" alt-text="Elkarrizketa-koadroa Customer Insights ingurune berria sortzeko.":::

Hornitu hurrengo xehetasunak:
   - **Izena**: entitatearen izena. Eremu hau dagoeneko bete da ingurune batetik kopiatzen baduzu, baina alda dezakezu.
   - **Aukeratu negozioa**: Aukeratu ingurune berriaren audientzia nagusia. Kontsumitzaile indibidualekin lan egin dezakezu (negoziotik bezerora) edo [negozio kontuekin](work-with-business-accounts.md) (negoziotik negoziora).
   - **Mota**: Aukeratu Produkzio edo Sandbox ingurunea sortu nahi duzun ala ez. Sandbox inguruneek ez dute programatutako datuak freskatzea onartzen eta aurrez ezartzeko eta probatzeko pentsatuta daude. Sandbox inguruneek unean hautatutako produkzio ingurunearen audientzia nagusia erabiltzen dute.
   - **Eskualdea**: Zerbitzua hedatu eta ostatatzen den eskualdea.

### <a name="step-2-configure-data-storage"></a>2. urratsa: konfiguratu datuen biltegiratzea

urtean **Datuak biltegiratzea** urratsa, aukeratu non gorde Customer Insights datuak.

Bi aukera izango dituzu: **Customer Insights biltegiratzea** (Customer Insights taldeak kudeatzen duen Azure Data Lake) eta **Azure Data Lake Storage** (zeurea Azure Data Lake Storage). Lehenespenez, Customer Insights biltegiratzeko aukera hautatuko da.

:::image type="content" source="media/data-storage-environment.png" alt-text="Aukeratu Azure Data Lake Storage zure datuak gordetzeko.":::

Datuak gordeta Azure Data Lake Storage, onartzen duzu datuak Azure biltegiratze kontu horretarako kokapen geografiko egokira transferitu eta gordeko direla. Kokapen hau datuak gordetzen diren tokitik desberdina izan daiteke Dynamics 365 Customer Insights. Ikasi gehiago [Microsoft Trust Center](https://www.microsoft.com/trust-center).

> [!NOTE]
> Customer Insights-ek gaur egun honako hau onartzen du:  
> - Azure Data Lake Storage ingurunea sortzerakoan hautatu zenuen Azure eskualde bereko kontuak.
> - Azure Data Lake Storage Gen2 diren eta dituzten kontuak *izen-espazio hierarkikoa* gaituta. Azure Data Lake Gen1 biltegiratze-kontuak ez dira onartzen.

Azure Data Lake Storage aukera, baliabideetan oinarritutako aukera bat eta harpidetzan oinarritutako aukera bat autentifikatzeko aukera dezakezu. Informazio gehiagorako, ikus [Konektatu Azure Data Lake Storage kontu batera Azure zerbitzuaren entitate bat erabiliz](connect-service-principal.md). Izeneko edukiontzi bat`customerinsights` biltegiratze-kontuan egon behar du.

Datuak sartzea bezalako sistemaren prozesuak amaitzen direnean, sistemak dagozkion karpetak sortzen ditu zuk zehaztutako biltegiratze kontuan. Datu fitxategiak eta *model.json* fitxategiak sortzen dira eta karpetetan gehitzen dira prozesuaren izenean oinarrituta.

Customer Insights-eko hainbat ingurune sortzen badituzu eta irteerako entitateak ingurune horietako biltegiratze kontuan gordetzea aukeratzen baduzu, Customer Insights-ek karpeta bereiziak sortzen ditu ingurune bakoitzarekin `ci_environmentID` edukiontzian.

### <a name="step-3-connect-to-microsoft-dataverse"></a>3. urratsa: konektatu Microsoft Dataverse
   
**Microsoft Dataverse** urratsak Customer Insights zurekin konektatzeko aukera ematen dizu Dataverse ingurunea.

Eman zurea Microsoft Dataverse Datuak (profilak eta ikuspegiak) oinarritutako negozio-aplikazioekin partekatzeko ingurunea Dataverse, Dynamics 365 Marketing edo ereduetan oinarritutako aplikazioak bezala Power Apps. Utzi eremu hau hutsik zurea ez baduzu Dataverse ingurumena eta bat emango dizugu.

Zurera konektatzen Dataverse inguruneak ere aukera ematen dizu [irensi lokal datu-iturburuetako datuak erabiliz Power Platform datu-fluxuak eta pasabideak](data-sources.md#add-data-from-on-premises-data-sources).

> [!IMPORTANT]
> 1. Bezeroen ikuspegiak eta Dataverse Eskualde berean egon behar da datuak partekatzea ahalbidetzeko.
> 1. Administratzaile global rola izan behar duzu Dataverse ingurunea. Egiaztatu hau bada [Dataverse ingurunea lotzen da](/power-platform/admin/control-user-access#associate-a-security-group-with-a-dataverse-environment) segurtasun-talde jakin batzuetara eta ziurtatu segurtasun-talde horietara gehitzen zarela.
> 1. Lehendik dagoen Customer Insights ingurunerik ez dago horrekin lotuta Dataverse ingurunea. Ikasi nola egin [kendu lehendik dagoen konexio bat a Dataverse ingurunea](manage-environments.md#remove-an-existing-connection-to-a-dataverse-environment).

:::image type="content" source="media/dataverse-provisioning.png" alt-text="datuak partekatzearekin Microsoft Dataverse automatikoki gaituta instantzia garbi berrietarako.":::

Honekin datuak partekatzea gaitzeari buruzko informazio gehiago lortzeko Microsoft Dataverse zuretik Azure Data Lake Storage, ikusi [Konektatu Microsoft Dataverse](manage-environments.md#connect-to-microsoft-dataverse).

Customer Insights-ek ez ditu onartzen hurrengo datuak partekatzeko egoerak:
- Datuak Dataverse-rekin partekatzea gaitzen baduzu, ezin izango duzu [sortu aurreikusitako edo falta diren balioak entitate batean](predictions.md).

### <a name="step-4-finalize-the-settings"></a>4. urratsa: Amaitu Ezarpenak

Urtean **Berrikuspena** urratsa, zehaztutako ezarpen guztiak ikusi. Guztia itxura duenean, hautatu **Sortu** ingurunea konfiguratzeko. 

Ezarpen gehienak geroago alda ditzakezu. Informazio gehiagorako, ikusi [Kudeatu inguruneak](manage-environments.md).

## <a name="work-with-your-new-environment"></a>Lan egin ingurune berriarekin

Berrikusi artikulu hauek Customer Insights konfiguratzen hasteko: 

- [Gehitu erabiltzaile gehiago eta eman baimenak](permissions.md).
- [Sartu zure datu-iturburuak](data-sources.md) eta exekutatu [datuak bateratzeko prozesuaren](data-unification.md) bidez lortzeko [bezeroen profil bateratuak](customer-profiles.md).
- [Aberastu bezeroen profil bateratuak](enrichment-hub.md) edo [exekutatu eredu iragarleak](predictions-overview.md).
- [Sortu segmentuak](segments.md) bezeroak taldekatzeko eta [neurriak](measures.md) KPIak berrikusteko.
- [Konfiguratu konexioak](connections.md) eta [esportazioak](export-destinations.md) zure datuen azpimultzoak beste aplikazio batzuetan prozesatzeko.
