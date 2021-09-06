---
title: Zeregin partekatuak iragarpen agertokietarako
description: Ikasi iragarpenak kudeatzen, konpontzen eta zehazten.
ms.date: 05/17/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: diegogranados117
ms.author: digranad
manager: shellyha
ms.openlocfilehash: eaccf23a81ca4de19763b761cc5a27c14515fe522ee36dc78f294208b681966e
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036450"
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

- Izena: errore, abisu edo gomendioaren izen deskribatzailea.
- Urratsa: ereduaren fasea, entrenamendua edo puntuazioa, informazioa aipatzen da.
- Egoera: informazioaren larritasuna (errorea, abisua, gomendioa).
- Zutabe izena: ereduaren errendimendua hobetzeko aldatu behar den entitate bateko zutabea.
- Entitatearen izena: ereduaren errendimendua hobetzeko aldatu behar den entitate baten izena.
- Xehetasunak: akatsari, abisuari edo gomendioari buruzko xehetasunak.

## <a name="refresh-a-prediction"></a>Iragarpen bat eguneratu

Aurreikuspenak automatikoki berritu egingo dira [programatu zure datuak freskatzea](system.md#schedule-tab) ezarpenetan konfiguratuta. Eskuz freskatu ditzakezu.

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Hautatu freskatu nahi duzun iragarpenaren ondoan elipsi bertikalak.

1. Aukeratu **Freskatu**.

## <a name="delete-a-prediction"></a>Ezabatu iragarpena

Iragarpen ezabatzeak bere irteerako entitatea ere kentzen du.

1. Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.

1. Hautatu ezabatu nahi duzun iragarpenaren ondoan elipsi bertikalak.

1. Hautatu **Ezabatu**.
