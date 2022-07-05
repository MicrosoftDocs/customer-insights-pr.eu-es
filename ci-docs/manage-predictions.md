---
title: Iragarpenak kudeatu
description: Ikasi iragarpenak kudeatzen, konpontzen eta zehazten.
ms.date: 11/01/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: a180f6462452d9830d0daa150a35a9d0acad925a
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9082841"
---
# <a name="manage-predictions"></a>Iragarpenak kudeatu

Artikulu honetan iragarpen agertoki gehienek partekatzen dituzten zenbait zeregin aztertzen dira.

## <a name="troubleshoot-a-failed-prediction"></a>Huts egin duen iragarpen baten arazoak konpontzea

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Aukeratu elipseak bertikalak errore-egunkariak ikusi nahi dituzun iragarpenaren ondoan.

1. Hautatu **Egunkariak**.

1. Berrikusi errore guztiak. Hainbat akats mota gerta daitezke eta deskribatzen dute zer baldintza eragin duen errorea. Adibidez, errore batek ez dauka datu nahikoak zehaztasunez iragartzeko ohikoa da ebaztea kargatzea datu osagarriak Customer Insights-en.

## <a name="input-data-usability-report"></a>Sarrerako datuen erabilgarritasun-txostena

Sarrerako datuak erabiltzeko txostena Sarrerako datuen erabilgarritasun txostenak erabiltzeko prest dauden iragarpenek sor ditzaketen akats eta abisuen ikuspegi bateratua eskaintzen du. Ereduaren errendimendua hobetzeko gomendioak ere ematen ditu.

Txostena eredu batek bere prestakuntza prozesua amaitu ondoren eskuragarri dago. Eredu bakoitzerako bereizita sortu da, ondo osatu den edo ez kontuan hartu gabe.

### <a name="view-the-input-data-usability-report"></a>Ikusi sarrerako datuen erabilgarritasun-txostena

Erabiltzeko prest dagoen eredu batek prestakuntza-urratsa amaitu ondoren, ikusi txostena:
- Aukeratu modeloaren izenaren ondoan dauden elipseak eta aukeratu **Sarrerako datuen erabilgarritasun txostena**.
- Aukeratu eredu baten egoera hautatu **Ikusi Sarrerako datuak erabiltzeko txostena** alboko panelean.
- Zerrendako ereduetako bat aukeratu eta hautatu **Sarrerako datuen erabilgarritasun txostena** komando barran.
- Ireki ereduen emaitzen orria eta hautatu **Sarrerako datuen erabilgarritasun txostena** komando barran.

### <a name="information-in-the-input-data-usability-report"></a>Sarrerako datuen erabilgarritasun txostenari buruzko informazioa

Txostenaren hurrengo zutabeek informazio lagungarria dute ereduaren datuak hobetzeko.

:::image type="content" source="media/input-data-usability-report.png" alt-text="Sarrerako datuen erabilgarritasun txostenaren adibidea, akatsak, abisuak eta gomendioak dituen taula erakusten duena.":::

- **Izena:** Errorearen, abisuaren edo gomendioaren izen deskribatzailea.
- **Urratsera:** Ereduaren fasea, trena edo puntuazioa, informazioa aipatzen du.
- **Estatu:** Informazioaren larritasuna (errorea, abisua, gomendioa).
- **Zutabearen izena:** Modeloaren errendimendua hobetzeko aldatu behar den entitate bateko zutabea.
- **Entitatearen izena:** Ereduaren errendimendua hobetzeko aldatu behar den entitatearen izena.
- **Xehetasunak:** Erroreari, abisuari edo gomendioari buruzko xehetasunak.

## <a name="refresh-a-prediction"></a>Iragarpen bat eguneratu

Aurreikuspenak automatikoki berritu egingo dira [programatu zure datuak freskatzea](system.md#schedule-tab) ezarpenetan konfiguratuta. Eskuz freskatu ditzakezu.

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Hautatu freskatu nahi duzun iragarpenaren ondoan elipsi bertikalak.

1. Aukeratu **Freskatu**.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="delete-a-prediction"></a>Ezabatu iragarpena

Iragarpen ezabatzeak bere irteerako entitatea ere kentzen du.

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Hautatu ezabatu nahi duzun iragarpenaren ondoan elipsi bertikalak.

1. Hautatu **Ezabatu**.
