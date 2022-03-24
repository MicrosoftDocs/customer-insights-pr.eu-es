---
title: Sortu eta kudeatu inguruneak
description: Ikasi zerbitzuan izena ematen eta inguruneak kudeatzen.
ms.date: 02/09/2022
ms.subservice: audience-insights
ms.topic: how-to
ms.reviewer: mhart
author: NimrodMagen
ms.author: nimagen
manager: shellyha
searchScope:
- ci-system-about
- customerInsights
ms.openlocfilehash: 4f4e5a8415f6c2128b0480edf67f317124eeeba9
ms.sourcegitcommit: 50d32a4cab01421a5c3689af789e20857ab009c4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376861"
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

Erabiltzeko [kutxaz kanpoko iragarpen modeloak](predictions-overview.md#out-of-box-models), konfiguratu datuak partekatzearekin Dataverse. Edo datuen iradokizuna gaitu dezakezu lokal datu iturrietatik, Microsoft Dataverse zure erakundeak administratzen duen ingurumen URLa.

> [!IMPORTANT]
> Bezeroen ikuspegiak eta Dataverse Eskualde berean egon behar da datuak partekatzea gaitzeko.

:::image type="content" source="media/dataverse-provisioning.png" alt-text="Konfigurazioaren aukerak gaitzeko datuak partekatzeko Microsoft Dataverse.":::

> [!NOTE]
> Customer Insights-ek ez ditu onartzen hurrengo datuak partekatzeko egoerak:
> - Datu guztiak zure kabuz gordetzen badituzu Azure Data Lake Storage, ezin izango duzu datuak partekatzea gaitu Dataverse Kudeatutako Data Lake.
> - Datuak Dataverse-rekin partekatzea gaitzen baduzu, ezin izango duzu [sortu aurreikusitako edo falta diren balioak entitate batean](predictions.md).

## <a name="copy-the-environment-configuration"></a>Kopiatu ingurunearen konfigurazioa

Ingurune berri bat sortzen duzunean, konfigurazioa lehendik dagoen ingurune batetik kopiatzea aukeratu dezakezu. 

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

Datu hauek *ez* dira kopiatu:

- Bezeroen profilak.
- Datu-iturburuaren kredentzialak. Datu-iturburu bakoitzerako kredentzialak eman beharko dituzu eta datu iturriak eskuz freskatu.

- Common Data Model karpetako eta Dataverse-k kudeatutako datu-biltegiko datu-iturburuak. Datu iturri horiek eskuz sortu beharko dituzu iturri ingurunean izen berdinekin.

Ingurumena kopiatzean, berrespen mezu bat ikusiko duzu ingurune berria sortu dela. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.

Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera. Editatu datu-iturriak eta sartu kredentzialak freskatzeko.

:::image type="content" source="media/data-sources-copied.png" alt-text="Kopiatu ziren eta autentifikazioa behar duten datu iturrien zerrenda.":::

Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.

Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.

## <a name="change-the-owner-of-an-environment"></a>Ingurune baten jabea aldatu

Hainbat erabiltzailek Customer Insights-en administratzaile-baimenak izan ditzaketen arren, erabiltzaile bakarra da ingurune baten jabea. Lehenespenez, administratzailea da hasiera batean ingurune bat sortzen duena. Ingurune baten administratzaile gisa, administratzaile baimenak dituen beste erabiltzaile bati jabetza esleitu diezaiokezu.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
