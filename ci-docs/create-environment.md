---
title: Nola - Sortu ingurune berri bat
description: For-rekin inguruneak sortzeko urratsak Dynamics 365 Customer Insights.
ms.date: 05/31/2022
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
ms.openlocfilehash: 6dfaa09cd80498e9a4e4dea6a07ce6e9d29105e2
ms.sourcegitcommit: 5e26cbb6d2258074471505af2da515818327cf2c
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "9011530"
---
# <a name="how-to-create-a-new-environment"></a>Nola: Ingurune berri bat sortu

Ondoren [harpidetza lizentzia erostea Dynamics 365 Customer Insights](paid-license.md),-ren administratzaile globala Microsoft 365 maizterrak ingurunea sortzera gonbidatzen duen mezu elektroniko bat jasotzen du. Erabiltzen hasteko, joan hona: [https://home.ci.ai.dynamics.com/start](https://home.ci.ai.dynamics.com/start). Egoera honetan, zuzenean joan zaitezke [1. urratsa: oinarrizko informazioa eman](#step-1-provide-basic-information).

Lehenengo ingurunea sortu ondoren, honen administratzaile globala Microsoft 365 maizterrak ahal du [gehitu erabiltzaileak beren erakundetik administratzaile gisa](permissions.md). Aurrerantzean, administratzaile hauek erabiltzaileak eta inguruneak kudea ditzakete. Zure erakundeak lizentzia bat baino gehiago erosten badu Customer Insights-erako, [jarri harremanetan gure laguntza-taldearekin](https://go.microsoft.com/fwlink/?linkid=2079641) erabilgarri dauden inguruneen kopurua handitzeko. Edukierari eta gehigarriei buruzko informazio gehiago lortzeko, berrikusi [Dynamics 365 lizentzien gida](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!TIP]
> Zerbitzua probatu nahi baduzu, ikusi [Konfiguratu proba ingurunea](trial-signup.md).

## <a name="prerequisites"></a>Aurrebaldintzak

Behar duzu [administratzaile-baimenak](permissions.md) Customer Insights-en inguruneak sortzeko edo kudeatzeko.

## <a name="start-the-environment-creation-process"></a>Hasi ingurunea sortzeko prozesua

1. Ireki ingurune-hautatzailea eta hautatu **+ Berria**.
  
   :::image type="content" source="media/environment-picker.png" alt-text="Hautatu ingurunearen hautatzailea.":::

1. Jarraitu hurrengo ataletan azaltzen den esperientzia gidatuari ingurune berri baterako beharrezko informazio guztia emateko. Ingurune bat lehenago konfiguratu baduzu, ere egin dezakezu [kopiatu konfigurazioa](#copy-the-environment-configuration).

## <a name="step-1-provide-basic-information"></a>1. urratsa: oinarrizko informazioa eman

Urtean **Oinarrizko informazioa** urratsa, aukeratu hutsetik ingurunea sortu nahi duzun edo [kopiatu datuak beste ingurune batetik](#copy-the-environment-configuration).

   :::image type="content" source="media/environment-settings-dialog.png" alt-text="Elkarrizketa-koadroa Customer Insights ingurune berria sortzeko.":::

Hornitu hurrengo xehetasunak:

- **Izena**: entitatearen izena. Eremu hau dagoeneko bete da ingurune batetik kopiatzen baduzu, baina alda dezakezu.
- **Aukeratu negozioa**: Aukeratu ingurune berriaren audientzia nagusia. Kontsumitzaile indibidualekin lan egin dezakezu (negoziotik bezerora) edo [negozio kontuekin](work-with-business-accounts.md) (negoziotik negoziora). Zure erakundeak batez ere pertsonekin egiten baditu negozioak, hala nola dendari batekin edo kafetegi batekin, aukeratu banakako kontsumitzaileak. Zure entzule nagusia beste enpresa batzuk badira, adibidez, autoen fabrikatzailea edo paper-enpresa bat, aukeratu negozio-kontuak.
- **Mota**: Aukeratu Produkzio edo Sandbox ingurunea sortu nahi duzun ala ez. Sandbox inguruneek ez dute programatutako datuak freskatzea onartzen eta aurrez ezartzeko eta probatzeko pentsatuta daude. Sandbox inguruneek unean hautatutako produkzio ingurunearen audientzia nagusia erabiltzen dute.
- **Eskualdea**: Zerbitzua hedatu eta ostatatzen den eskualdea. To [zurea erabili Azure Data Lake Storage kontua](own-data-lake-storage.md) edo [lehendik dagoen batekin konektatu Microsoft Dataverse antolakuntza](customer-insights-dataverse.md), Customer Insights inguruneak eskualde berean egon behar du.

## <a name="step-2-configure-data-storage"></a>2. urratsa: konfiguratu datuen biltegiratzea

urtean **Datuak biltegiratzea** urratsa, aukeratu non gorde Customer Insights datuak.

Bi aukera dituzu aukeran:

- **Bezeroen estatistikak biltegiratzea** : Datuen biltegiratzea Customer Insights taldeak kudeatzen du. Aukera lehenetsia da eta zure biltegiratze-kontuan datuak gordetzeko eskakizun zehatzik ez badago, aukera hau erabiltzea gomendatzen dugu.
- **Azure Data Lake Storage**: Zehaztu zurea Azure Data Lake Storage kontua datuak gordetzeko, datuak non gordetzen diren kontrol osoa izan dezazun. Informazio gehiagorako, ikus [Erabili zurea Azure Data Lake Storage kontua](own-data-lake-storage.md).

:::image type="content" source="media/data-storage-environment.png" alt-text="Aukeratu hobetsitako aukera zure datuak gordetzeko.":::

## <a name="step-3-connect-to-microsoft-dataverse"></a>3. urratsa: konektatu Microsoft Dataverse

**Microsoft Dataverse** urratsak Customer Insights zurekin konektatzeko aukera ematen dizu Dataverse ingurunea. Partekatu datuak Dataverse oinarritutako negozio-aplikazioekin erabiltzeko Dataverse, Dynamics 365 Marketing edo ereduetan oinarritutako aplikazioak bezala Power Apps.


Utzi eremu hau hutsik zurea ez baduzu Dataverse ingurunea eta zuretzat bat sortuko dugu.

Informazio gehiagorako, ikus [Lan egin Customer Insights datuekin Microsoft Dataverse](customer-insights-dataverse.md).

:::image type="content" source="media/dataverse-provisioning.png" alt-text="datuak partekatzearekin Microsoft Dataverse sareko ingurune berrietarako automatikoki gaituta.":::

### <a name="step-4-finalize-the-settings"></a>4. urratsa: Amaitu Ezarpenak

urtean **Iritzia** urratsa, joan zehaztutako ezarpen guztiak. Guztia itxura duenean, hautatu **Sortu** ingurunea konfiguratzeko.

Ezarpen batzuk geroago alda ditzakezu. Informazio gehiagorako, ikusi [Kudeatu inguruneak](manage-environments.md).

## <a name="work-with-your-new-environment"></a>Lan egin ingurune berriarekin

Berrikusi artikulu hauek Customer Insights konfiguratzen hasteko:

- [Gehitu erabiltzaile gehiago eta eman baimenak](permissions.md).
- [Sartu zure datu-iturburuak](data-sources.md) eta exekutatu [datuak bateratzeko prozesuaren](data-unification.md) bidez lortzeko [bezeroen profil bateratuak](customer-profiles.md).
- [Aberastu bezeroen profil bateratuak](enrichment-hub.md) edo [exekutatu eredu iragarleak](predictions-overview.md).
- [Sortu segmentuak](segments.md) bezeroak taldekatzeko eta [neurriak](measures.md) KPIak berrikusteko.
- [Konfiguratu konexioak](connections.md) eta [esportazioak](export-destinations.md) zure datuen azpimultzoak beste aplikazio batzuetan prozesatzeko.

## <a name="copy-the-environment-configuration"></a>Kopiatu ingurunearen konfigurazioa

Administratzaile gisa, konfigurazioa lehendik dagoen ingurune batetik kopiatzea aukera dezakezu berri bat sortzen duzunean.

:::image type="content" source="media/environment-settings-dialog.png" alt-text="Ingurumen ezarpenetako ezarpen aukeren pantaila-argazkia.":::

Zure erakundearen eskura dauden ingurune guztien zerrenda ikusiko duzu non datuak kopiatzeko.

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

## <a name="set-up-a-copied-environment"></a>Konfiguratu kopiatutako ingurune bat

Ingurunearen konfigurazioa kopiatzen duzunean, beste urrats batzuk egin behar dituzu kredentzialak berresteko:

- Bezeroen profilak. Lehenik eta behin, autentifikatu eta hartu zure datu-iturriak eta exekutatu datuen bateratzea bezeroen profilak birsortzeko.
- Datu-iturburuaren kredentzialak. datu-iturburu bakoitzaren kredentzialak eman behar dituzu datu-iturriak eskuz autentifikatzeko eta freskatzeko.
- Datu-iturriak Common Data Model karpetatik eta Dataverse. Datu-iturri horiek eskuz sortu behar dituzu iturburu-inguruneko izen berarekin.
- Esportazioetarako eta aberasteko erabiltzen diren konexio sekretuak. Konexioak berriro autentifikatu eta gero aberasketak eta esportazioak berriro aktibatu behar dituzu.

Berrespen-mezu bat ikusiko duzu kopiatutako ingurunea sortzen denean. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.

Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera. Editatu datu-iturriak eta sartu kredentzialak freskatzeko.

:::image type="content" source="media/data-sources-copied.png" alt-text="Kopiatu ziren eta autentifikazioa behar duten datu iturrien zerrenda.":::

Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.

Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.

Esportazio eta aberasketak berriro aktibatu aurretik, joan hona **Admin** > **Konexioak** zure ingurune berriko konexioak berriro autentifikatzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
