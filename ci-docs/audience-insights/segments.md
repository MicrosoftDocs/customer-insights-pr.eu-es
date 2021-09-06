---
title: Hartzaileen xehetasunen segmentuak
description: Segmentuen ikuspegi orokorra eta nola sortu eta kudeatu.
ms.date: 05/03/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: f1003b53b17e3ba2c37c0f2d94b89f7e97c2b6f10e28b7bbe93160e4c7f08d54
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036358"
---
# <a name="segments-overview"></a>Segmentuen informazio orokorra

Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu. Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.

Segmentuaren definizio baten iragazkiekin bat datozen bezeroen profilak aipatzen dira *kideak* segmentu batena. [Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.

## <a name="create-a-new-segment"></a>Sortu segmentu berria

Segmentu berri bat sortzeko hainbat modu daude: 

- Segmentu konplexua segmentu eraikitzailearekin: [Segmentu hutsa](segment-builder.md#create-a-new-segment)
- Operadore bakarreko segmentu sinpleak: [Segmentu azkarra](segment-builder.md#quick-segments)
- AI-ren bidezko bezeroak antzeko bezeroak aurkitzeko modua: [Bezero antzekoak](find-similar-customer-segments.md)
- AI-k oinarritutako iradokizunak neurri edo atributuetan oinarrituta: [Neurriak hobetzeko iradokitako segmentuak](suggested-segments.md)
- Jardueretan oinarritutako iradokizunak: [Iradokitako segmentuak bezeroen jardueran oinarrituta](suggested-segments-activity.md)

## <a name="manage-existing-segments"></a>Kudeatu lehendik dauden segmentuak

Joan **Segmentuak** orrian, gordetako segmentu guztiak ikusi eta kudeatzeko.

Segmentu bakoitza segmentuari buruzko informazio osagarria biltzen duen errenkada batez irudikatuta dago.

:::image type="content" source="media/segments-selected-segment.png" alt-text="Aukeratutako segmentua aukerak goitibeherako zerrendarekin eta eskuragarri dauden aukerekin.":::

Segmentu bat hautatzean ekintza hauek erabilgarri daude:

- **ikusi** segmentuko xehetasunak, kideen zenbaketa joera segmentuko kideen aurrebista barne.
- **Editatu** segmentuak bere propietateak aldatzeko.
- **Sortu bikoiztuak** segmentu baten. Bere propietateak berehala editatzea edo bikoiztua gordetzea aukeratu dezakezu.
- **Freskatu** segmentuak azken datuak sartuko ditu.
- **Aktibatu** edo **Desaktibatu** segmentua. Segmentuek bi egoera posible dituzte: aktiboak edo inaktiboak. Egoera hauek oso ondo etortzen dira segmentu bat editatzerakoan. Segmentu inaktiboetan, segmentuaren definizioa badago, baina oraindik ez du bezeroik. Segmentu bat aktibatzean, egoera "inaktibo" izatetik "aktibo" izatera pasatzen da eta segmentuaren definizioarekin bat datozen bezeroak bilatzen hasiko da. A bada [freskatze programatua](system.md#schedule-tab) konfiguratuta dago, segmentu inaktiboek dute **Egoera** gisa zerrendatuta **Saltatuta**, freskatzen saiatu ere ez zela egin adieraziz. Segmentu inaktiboa aktibatzen denean, freskatu egingo da eta programatutako freskapenetan sartuko da.
  Bestela, erabil dezakezu **Ordutegiak beranduago** funtzionaltasuna **Aktibatu / Desaktibatu** goitibehera, segmentu jakin bat aktibatzeko eta desaktibatzeko etorkizuneko data eta ordua zehazteko.
- **Aldatu izena** segmentuari.
- **Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.
- **Kudeatu esportazioak** esportazioekin lotutako segmentua ikusteko eta kudeatzeko. [Lortu esportazioei buruzko informazio gehiago.](export-destinations.md)
- **Ezabatu** segmentua.

## <a name="refresh-segments"></a>Freskatu segmentuak

Segmentu guztiak freskatu ditzakezu aldi berean hautatuta **Freskatu guztiak** gainean **segmentuak** orrialdea edo segmentu bat edo gehiago freskatu ditzakezu hautatzen dituzunean eta aukeratutakoan **Freskatu** aukeren artean. Bestela, berriztagarria den aldizka konfigura dezakezu **administratzailea** > **Sistema** > **Ordutegiak**.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="export-segments"></a>Esportatu segmentuak

Segmentu bat esportatu dezakezu segmentuen orrialdetik edo [esportazioen orritik](export-destinations.md). 

1. Zoaz **Segmentuak** orrira.

1. Esportatu nahi duzun segmenturako, hautatu **erakutsi gehiago [...]**.

1. Aukeratu **Kudeatu esportazioak** ekintzen goitibeherako zerrendatik.

1. **Segmentuaren esportazioak (aurrebista)** orria irekitzen da. Uneko segmentua duten edo ez duten esportazioen arabera taldekatutako konfiguratutako esportazio guztiak ikus ditzakezu.

   1. Aukeratutako segmentua esportazio batera gehitzeko, hautatu esportazioa zerrendan eta hautatu **Gehitu segmentua**.

   1. Aukeratutako segmentuarekin esportazio berri bat sortzeko, hautatu **Gehitu esportazioa**. Esportazioak sortzeari buruzko informazio gehiago lortzeko, ikusi [Konfiguratu esportazio berria](export-destinations.md#set-up-a-new-export).

1. Aukeratu **Itzuli** segmentuen orri nagusira itzultzeko.

## <a name="view-processing-history-and-segment-members"></a>Ikusi prozesaketaren historia eta segmentuko kideak

Segurtasun bati buruzko datu bateratuak ikus ditzakezu haren xehetasunak berrikusiz.

**Segmentuak** orrian, hautatu berrikusi nahi duzun segmentua.

Orriaren goiko aldean joera grafikoa dago, kideen zenbateko aldaketak bistaratzen dituena. Pasa datuak gainetik kideak data jakin batean ikusteko.

Bistaratzeko denbora-markoa eguneratu dezakezu.

> [!div class="mx-imgBorder"]
> ![Segmentuaren denbora-tartea.](media/segment-time-range.png "Segmentuaren denbora-tartea")

Beheko aldean segmentuko kideen zerrenda dago.

> [!NOTE]
> Zerrenda honetan agertzen diren eremuak zure segmentuko entitateen atributuetan oinarrituta daude.
>
>Zerrenda bat datorren segmentuko kideen aurrebista da eta zure segmentuko lehen 100 erregistroak erakusten ditu, behar bezala baloratu eta haren definizioak berrikusteko. Bat datozen erregistro guztiak ikusteko, beharrezkoa da [esportatu segmentua](export-destinations.md).

[!INCLUDE[footer-include](../includes/footer-banner.md)] 
