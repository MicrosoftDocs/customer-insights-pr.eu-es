---
title: Enpresako profilak aberastea hirugarrenen Leadspace aberastearekin
description: Leadspace-ren hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 11/24/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-MS
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 41c56aece043c2d7658fd2655713e1e98775edec
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597634"
---
# <a name="enrichment-of-company-profiles-with-leadspace-preview"></a>Enpresen profilak aberastea Leadspace-rekin (aurrebista)

Leadspace B2B Bezeroaren Datuen Plataforma eskaintzen duen datuen zientzia enpresa da. Enpresentzako bezeroen profil bateratuak dituzten bezeroei beren datuak aberasteko aukera ematen die. Aberasteek atributu osagarriak barne hartzen dituzte esaterako, enpresaren tamaina, kokalekua, sektorea, etab.

## <a name="prerequisites"></a>Aurrebaldintzak

Leadspace konfiguratzeko eta konfiguratzeko, honako baldintza hauek bete behar dira:

- Leadspace lizentzia aktiboa duzu eta "betiko gakoa" (**Leadspace-ko token** deitzen zaio). Jar zaitez harremanetan zuzenean [Leadspace](https://www.leadspace.com/products/leadspace-on-demand/) beren produktuari buruzko xehetasunak lortzeko.
- [Administratzaile](permissions.md#administrator) baimenak dituzu.
- Duzu [bezeroen profil bateratuak](customer-profiles.md) enpresentzat.

## <a name="configuration"></a>Konfigurazioa

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Aberastea**.

1. Aukeratu **Aberastu nire datuak** Leadspace fitxan.

   :::image type="content" source="media/leadspace-tile.png" alt-text="Leadspace lauzaren pantaila-argazkia.":::

1. Aukeratu **Hasi** eta, ondoren, sartu **Leadspace token** aktibo bat (betiko giltza). Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia. Berretsi bi sarrerak **Konektatu Leadspace-ra** hautatuta.

1. Aukeratu **Esleitu datuak** eta aukeratu Microsoft Leadspace-ko enpresako datuekin aberastu nahi duzun datu multzoa. *Bezeroen* entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

   :::image type="content" source="media/enrichment-leadspace-select-segment.png" alt-text="Aukeratu bezeroaren profila eta segmentua aberasteko.":::

1. Sakatu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu erabili beharko liratekeen Leadspace enpresako datuekin bat etortzeko. **Enpresaren izena** eremua beharrezkoa da. Bat-etortzeen zehaztasun handiagoa lortzeko, beste bi eremu, **Enpresaren webgunea** eta **Enpresaren kokapena**, gehitu daitezke.

   :::image type="content" source="media/enrichment-leadspace-mapping.png" alt-text="Leadspace eremuak esleitzeko panela.":::
   
1. Aukeratu **Aplikatu** eremuen esleipena osatzeko.

1. Aukeratu **Exekutatu** enpresaren profilak aberasteko. Aberasteak behar duen denbora bateratutako bezeroen profil kopuruaren araberakoa da.

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberastea freskatu ondoren, azpian dagoen enpresa aberastutako datuak berrikus ditzakezu [Nire aberastasunak](enrichment-hub.md). Azken eguneraketaren ordua eta aberastutako profil kopurua aurki ditzakezu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

Informazio gehiago lortzeko, ikus [Leadspace API](https://support.leadspace.com/hc/en-us/sections/201997649-API).

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Leadspace-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Leadspace-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]