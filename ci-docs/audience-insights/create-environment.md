---
title: Sortu inguruneak Customer Insights-en
description: Lizentziapeko harpidetza duten inguruneak sortzeko urratsak Dynamics 365 Customer Insights.
ms.date: 10/14/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: MichelleDevaney
ms.author: midevane
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: 914af46d2d82f3556d149f2836680c902f826d50
ms.sourcegitcommit: 31985755c7c973fb1eb540c52fd1451731d2bed2
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/22/2021
ms.locfileid: "7673376"
---
# <a name="create-an-environment-in-audience-insights"></a>Sortu ingurune bat audientziaren xehetasunetan

Artikulu honetan zure erakundeak Dynamics 365 Customer Insights harpidetza erosi ondoren ingurune berri bat nola sortu azaltzen da. 

Erakundeek sor dezakete *bi* Customer Insights lizentzia bakoitzeko inguruneak. Zure erakundeak lizentzia bat baino gehiago erosten badu, [jarri harremanetan gure laguntza taldearekin](https://go.microsoft.com/fwlink/?linkid=2079641) erabilgarri dauden ingurune kopurua handitzeko. Gaitasun eta gaitasun osagarriei buruzko informazio gehiago lortzeko, deskargatu [Dynamics 365 lizentzien gida](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Zerbitzua probatu nahi baduzu, ikusi [Konfiguratu proba ingurunea](../trial-signup.md).

## <a name="create-a-new-environment"></a>Sortu ingurune bat

Customer Insights-erako harpidetza lizentzia erosi ondoren, Microsoft 365 maizterreko administratzaile orokorrak ingurunea sortzera gonbidatzen duen mezu elektronikoa jasotzen du. Erabiltzen hasteko, joan hona: [https://home.ci.ai.dynamics.com/start](https://home.ci.ai.dynamics.com/start). 

Esperientzia gidatu batek ingurune berri baterako beharrezko informazio guztia biltzeko urratsak egiten laguntzen dizu. Behar duzu [administratzaile baimenak](permissions.md) inguruneak sortzeko edo kudeatzeko ikusleen ikuspegietan.

1. Ikusleen estatistiketan, ireki ingurunea hautatzeko eta hautatu **+ Berria**.
  
   :::image type="content" source="../engagement-insights/media/environment-picker.png" alt-text="Hautatu ingurunearen hautatzailea.":::

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

Urtean **Datuak biltegiratzea** urratsa, aukeratu non gorde datuak ikusleen estatistiketatik.

Bi aukera izango dituzu: **Customer Insights biltegiratzea** (Customer Insights taldeak kudeatzen duen Azure Data Lake) eta **Azure Data Lake Storage** (zeurea Azure Data Lake Storage). Lehenespenez, Customer Insights biltegiratzeko aukera hautatuko da.

:::image type="content" source="media/data-storage-environment.png" alt-text="Aukeratu Azure Data Lake Storage audientziari buruzko datuak gordetzeko.":::

Datuak gordeta Azure Data Lake Storage, onartzen duzu datuak Azure biltegiratze kontu horretarako kokapen geografiko egokira transferitu eta gordeko direla. Kokapen hau datuak gordetzen diren tokitik desberdina izan daiteke Dynamics 365 Customer Insights. Ikasi gehiago [Microsoft Trust Center](https://www.microsoft.com/trust-center).

> [!NOTE]
> Customer Insights-ek gaur egun honako hau onartzen du:
> - Entitate ingestatuak Power BI batean gordetako datu-fluxuak Microsoft Dataverse -kudeatutako Data Lake.  
> - Azure Data Lake Storage ingurunea sortzerakoan hautatu zenuen Azure eskualde bereko kontuak.
> - Azure Data Lake Storage dituzten kontuak *izen espazio hierarkikoa* gaituta.

Azure Data Lake Storage aukera, baliabideetan oinarritutako aukera bat eta harpidetzan oinarritutako aukera bat autentifikatzeko aukera dezakezu. Informazio gehiagorako, ikus [Konektatu Azure Data Lake Storage kontu batera Azure zerbitzuaren entitate bat erabiliz](connect-service-principal.md). **Edukiontzia** izena izango da `customerinsights` eta ezin da aldatu.

Datuak sartzea bezalako sistemaren prozesuak amaitzen direnean, sistemak dagozkion karpetak sortzen ditu zuk zehaztutako biltegiratze kontuan. Datu fitxategiak eta *model.json* fitxategiak sortzen dira eta karpetetan gehitzen dira prozesuaren izenean oinarrituta.

Customer Insights-eko hainbat ingurune sortzen badituzu eta irteerako entitateak ingurune horietako biltegiratze kontuan gordetzea aukeratzen baduzu, Customer Insights-ek karpeta bereiziak sortzen ditu ingurune bakoitzarekin `ci_environmentID` edukiontzian.

### <a name="step-3-connect-to-microsoft-dataverse"></a>3. urratsa: konektatu Microsoft Dataverse
   
**Microsoft Dataverse** urratsak Customer Insights zurekin konektatzeko aukera ematen dizu Dataverse ingurunea.

Erabiltzeko [kutxaz kanpoko iragarpen modeloak](predictions-overview.md#out-of-box-models), konfiguratu datuak partekatzearekin Dataverse. Edo datuen iradokizuna gaitu dezakezu lokal datu iturrietatik, Microsoft Dataverse zure erakundeak administratzen duen ingurumen URLa. Aukeratu **Gaitu datuak partekatzea** Customer Insights-en irteerako datuak partekatzeko Dataverse kudeatutako Data Lake.

:::image type="content" source="media/dataverse-data-sharing.png" alt-text="Konfigurazioaren aukerak gaitzeko datuak partekatzeko Microsoft Dataverse.":::

> [!NOTE]
> Customer Insights-ek ez ditu onartzen hurrengo datuak partekatzeko egoerak:
> - Datu guztiak zure kabuz gordetzen badituzu Azure Data Lake Storage, ezin izango duzu datuak partekatzea gaitu Dataverse Kudeatutako Data Lake.
> - Datuak Dataverse-rekin partekatzea gaitzen baduzu, ezin izango duzu [sortu aurreikusitako edo falta diren balioak entitate batean](predictions.md).

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
