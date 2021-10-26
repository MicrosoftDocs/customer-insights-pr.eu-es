---
title: Sortu eta kudeatu inguruneak
description: Ikasi zerbitzuan izena ematen eta inguruneak kudeatzen.
ms.date: 10/14/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
ms.reviewer: mhart
author: NimrodMagen
ms.author: nimagen
manager: shellyha
ms.openlocfilehash: ce2fdd435a81bb04148057554c5958e3ab59f125
ms.sourcegitcommit: 53b133a716c73cb71e8bcbedc6273cec70ceba6c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/15/2021
ms.locfileid: "7645111"
---
# <a name="manage-environments"></a>Kudeatu inguruneak

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

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
- Common Data Model karpetako datu iturriak eta Dataverse kudeatzen du Data Lake. Datu iturri horiek eskuz sortu beharko dituzu iturri ingurunean izen berdinekin.

Ingurumena kopiatzean, berrespen mezu bat ikusiko duzu ingurune berria sortu dela. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.

Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera. Editatu datu-iturriak eta sartu kredentzialak freskatzeko.

:::image type="content" source="media/data-sources-copied.png" alt-text="Kopiatu ziren eta autentifikazioa behar duten datu iturrien zerrenda.":::

Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.

Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.

## <a name="reset-an-existing-environment"></a>Berrezarri lehendik dagoen ingurunea

Administratzaile gisa, ingurunea egoera hutsera berrezar dezakezu konfigurazio guztiak ezabatu eta sartutako datuak kendu nahi badituzu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan. 

2.  Aukeratu berrezarri nahi duzun ingurunea eta hautatu elipsia (**...**). 

3. Aukeratu **Berrezarri** aukera. 

4.  Ezabapena berresteko, idatzi ingurunearen izena eta hautatu **Berrezarri**.

## <a name="delete-an-existing-environment"></a>Aurretik bazegoen ingurune bat ezabatu

Administratzaile gisa, kudeatzen duzun ingurunea ezabatu dezakezu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

2.  Aukeratu berrezarri nahi duzun ingurunea eta hautatu elipsia (**...**). 

3. Aukeratu **Ezabatu** aukera. 

4.  Ezabatzea berresteko, idatzi ingurumenaren izena eta hautatu **Ezabatu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
