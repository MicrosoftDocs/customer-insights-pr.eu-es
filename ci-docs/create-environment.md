---
title: Sortu ingurune bat
description: Inguruak sortzeko urratsak Dynamics 365 Customer Insights.
ms.date: 08/15/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
ms.custom: intro-internal
searchScope:
- ci-home
- customerInsights
ms.openlocfilehash: 0a45e2fd2bdb7b85883a536f8b42ee650e54db7e
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304228"
---
# <a name="create-a-new-environment"></a>Sortu ingurune bat

Ondoren [harpidetza lizentzia erostea Dynamics 365 Customer Insights](paid-license.md), ren administratzaile globala Microsoft 365 maizterrak ingurunea sortzera gonbidatzen duen mezu elektroniko bat jasotzen du. Erabiltzen hasteko, joan hona: [https://home.ci.ai.dynamics.com/start](https://home.ci.ai.dynamics.com/start). Eszenatoki honetan, hasi [1. urratsa: oinarrizko informazioa eman](#step-1-provide-basic-information).

Lehenengo ingurunea sortu ondoren, honen administratzaile globala Microsoft 365 maizterrak ahal du [gehitu bere erakundeko erabiltzaileak administratzaile gisa](permissions.md). Administratzaile hauek erabiltzaileak eta inguruneak kudea ditzakete. Zure erakundeak lizentzia bat baino gehiago erosten badu Customer Insights-erako, [jarri harremanetan gure laguntza-taldearekin](https://go.microsoft.com/fwlink/?linkid=2079641) eskuragarri dauden inguruneen kopurua handitzeko. Edukierari eta gehigarriei buruzko informazio gehiago lortzeko, berrikusi [Dynamics 365 lizentzien gida](https://go.microsoft.com/fwlink/?LinkId=866544). Ingurune osagarriak sortzeko gaitasuna duzunean, joan hona [Hasi ingurunea sortzeko prozesua](#start-the-environment-creation-process).

> [!TIP]
> Zerbitzua probatu nahi baduzu, ikusi [Konfiguratu proba ingurunea](trial-signup.md).

## <a name="prerequisites"></a>Aurrebaldintzak

[Administratzailearen baimenak](permissions.md) Bezeroen Insights-en

## <a name="start-the-environment-creation-process"></a>Hasi ingurunea sortzeko prozesua

1. Ireki ingurune-hautatzailea eta hautatu **+ Berria**.
  
   :::image type="content" source="media/environment-picker.png" alt-text="Hautatu ingurunearen hautatzailea.":::

1. Jarraitu hurrengo ataletan azaltzen den esperientzia gidatuari ingurune berri baterako beharrezko informazio guztia emateko.

## <a name="step-1-provide-basic-information"></a>1. urratsa: oinarrizko informazioa eman

1. Aukeratu ingurune bat hutsetik sortu edo beste ingurune bateko datuak kopiatu nahi dituzun. [Datuak beste ingurune batetik kopiatzea](#copy-the-environment-configuration) urrats gehigarriak eskatzen ditu.

   :::image type="content" source="media/environment-settings-dialog.png" alt-text="Elkarrizketa-koadroa Customer Insights ingurune berria sortzeko.":::

1. Hornitu hurrengo xehetasunak:

   - **Izena** : Ingurune honen izena. Eremu hau dagoeneko bete da ingurune batetik kopiatzen baduzu, baina alda dezakezu.
   - **Aukeratu zure negozioa** : Ingurune berrirako lehen audientzia: banakako kontsumitzaileak (B-to-C) edo [negozio kontuak](work-with-business-accounts.md) (B-tik-B). Zure erakundeak batez ere pertsonekin egiten baditu negozioak, hala nola dendari batekin edo kafetegi batekin, aukeratu banakako kontsumitzaileak. Zure entzule nagusia beste enpresa batzuk badira, adibidez, autoen fabrikatzailea edo paper-enpresa bat, aukeratu negozio-kontuak.
   - **Mota** : Ingurune mota: ekoizpena edo sandbox. Sandbox inguruneek ez dute programatutako datuak freskatzea onartzen eta aurrez ezartzeko eta probatzeko pentsatuta daude. Sandbox inguruneek unean hautatutako produkzio ingurunearen audientzia nagusia erabiltzen dute.
   - **Eskualdea** : zerbitzua zabaldu eta ostatatutako eskualdea. To [zurea erabili Azure Data Lake Storage kontua](own-data-lake-storage.md) edo [lehendik dagoen batekin konektatu Microsoft Dataverse antolakuntza](customer-insights-dataverse.md), Customer Insights inguruneak eskualde berean egon behar du.

1. Hautatu **Hurrengoa**.

## <a name="step-2-configure-data-storage"></a>2. urratsa: konfiguratu datuen biltegiratzea

1. Aukeratu non gorde Customer Insights datuak:

   - **Bezeroei buruzko informazio biltegiratzea** : Datuen biltegiratzea automatikoki kudeatzen da. Aukera lehenetsia da eta zure biltegiratze-kontuan datuak gordetzeko eskakizun zehatzik ez badago, aukera hau erabiltzea gomendatzen dugu.
   - **Azure Data Lake Storage**: Zurea Azure Data Lake Storage kontua datuak gordetzeko, datuak non gordetzen diren kontrol osoa izan dezazun. Jarraitu urratsak [Erabili zurea Azure Data Lake Storage kontua](own-data-lake-storage.md).

   :::image type="content" source="media/data-storage-environment.png" alt-text="Aukeratu hobetsitako aukera zure datuak gordetzeko.":::

1. Hautatu **Hurrengoa**.

## <a name="step-3-connect-to-microsoft-dataverse"></a>3. urratsa: konektatu Microsoft Dataverse

Bat baduzu Dataverse ingurunea, konektatu Customer Insights. Partekatu datuak Dataverse oinarritutako negozio-aplikazioekin erabiltzeko Dataverse, Dynamics 365 Marketing edo ereduetan oinarritutako aplikazioak bezala Power Apps.

1. Jarraitu urratsak [Lan egin Customer Insights datuekin Microsoft Dataverse](customer-insights-dataverse.md).

   :::image type="content" source="media/dataverse-provisioning.png" alt-text="datuak partekatzearekin Microsoft Dataverse sareko ingurune berrietarako automatikoki gaituta.":::

1. Hautatu **Hurrengoa**.

## <a name="step-4-finalize-the-settings"></a>4. urratsa: Amaitu Ezarpenak

Berrikusi zehaztutako ezarpenak. Guztia itxura duenean, hautatu **Sortu** ingurunea konfiguratzeko.

Ezarpen batzuk geroago aldatzeko, ikus [Kudeatu inguruneak](manage-environments.md).

## <a name="work-with-your-new-environment"></a>Lan egin ingurune berriarekin

Berrikusi artikulu hauek Customer Insights konfiguratzen hasteko:

- [Gehitu erabiltzaile gehiago eta eman baimenak](permissions.md).
- [Sartu zure datu-iturburuak](data-sources.md) eta exekutatu [datuak bateratzeko prozesuaren](data-unification.md) bidez lortzeko [bezeroen profil bateratuak](customer-profiles.md).
- [Aberastu bezeroen profil bateratuak](enrichment-hub.md) edo [exekutatu eredu iragarleak](predictions-overview.md).
- [Sortu segmentuak](segments.md) bezeroak taldekatzeko eta [neurriak](measures.md) KPIak berrikusteko.
- [Konfiguratu konexioak](connections.md) eta [esportazioak](export-destinations.md) zure datuen azpimultzoak beste aplikazio batzuetan prozesatzeko.

## <a name="copy-the-environment-configuration"></a>Kopiatu ingurunearen konfigurazioa

Administratzaile gisa, konfigurazioa lehendik dagoen ingurune batetik kopiatzea aukeratu baduzu, hautatu zure erakundeko ingurune erabilgarri guztien zerrendatik.

:::image type="content" source="media/environment-settings-dialog.png" alt-text="Ingurumen ezarpenetako ezarpen aukeren pantaila-argazkia.":::

Hurrengo konfigurazio ezarpenak kopiatzen dira:

- Bidez inportatutako datu-iturriak Power Query
- Datuak bateratzeko konfigurazioa
- Segmentuak
- Neurketak
- Erlazioak
- Ekintzak
- Bilaketa eta iragazkien indizea
- Esportazioak
- Freskatu antolaketa
- Aberasteak
- Iragarpen ereduak
- Funtzio-zereginak

### <a name="set-up-a-copied-environment"></a>Konfiguratu kopiatutako ingurune bat

Ingurunearen konfigurazioa kopiatzen duzunean, berrespen-mezu bat bistaratzen da kopiatutako ingurunea sortu denean. Egin urrats hauek kredentzialak berresteko.

1. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko. Datu iturri guztiek erakusten dute **Beharrezko kredentzialak** egoera.

   :::image type="content" source="media/data-sources-copied.png" alt-text="Kopiatu ziren eta autentifikazioa behar duten datu iturrien zerrenda.":::

1. Editatu datu-iturriak eta sartu kredentzialak freskatzeko. Datu-iturriak Common Data Model karpetatik eta Dataverse eskuz sortu behar da iturburu-ingurunean dagoen izen berarekin.

1. Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Bateratu** > **Bezeroen profilak eta menpekotasunak bateratzea** datuak bateratzeko prozesua hasteko eta bezeroen entitate bateratua sortzeko.

   > [!TIP]
   > Kontuetarako eta kontaktuetarako, hautatu **Kontuak bateratu** > **Profilak eta mendekotasunak bateratzea**.

1. Datuen bateratzea amaitzen denean, joan hona **Neurriak** eta **Segmentuak** freskatzeko.

1. Joan **Admin** > **Konexioak** zure ingurune berriko konexioak berriro autentifikatzeko.

1. Joan **Datuak** > **Aberastea** eta **Datuak** > **Esportazioak** horiek berriro aktibatzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
