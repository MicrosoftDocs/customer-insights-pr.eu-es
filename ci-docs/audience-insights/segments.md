---
title: Hartzaileen xehetasunen segmentuak
description: Segmentuen ikuspegi orokorra eta nola sortu eta kudeatu.
ms.date: 11/01/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 56978c984a91e85e86956e7eac1d59609c349b6a
ms.sourcegitcommit: 834651b933b1e50e7557d44f926a3fb757c1f83a
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/02/2021
ms.locfileid: "7732573"
---
# <a name="segments-overview"></a>Segmentuen informazio orokorra

Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu. Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.

Segmentuaren definizio baten iragazkiekin bat datozen bezeroen profilak aipatzen dira *kideak* segmentu batena. [Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.

## <a name="create-a-new-segment"></a>Sortu segmentu berria

Segmentu berri bat sortzeko hainbat modu daude: 

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- Segmentu konplexua segmentu eraikitzailearekin: [Gurea eraiki](segment-builder.md#create-a-new-segment) 
- Operadore bakarreko segmentu sinpleak: [Segmentu azkarra](segment-builder.md#quick-segments) 
- AI-ren bidezko bezeroak antzeko bezeroak aurkitzeko modua: [Bezero antzekoak](find-similar-customer-segments.md) 
- AI-k oinarritutako iradokizunak neurri edo atributuetan oinarrituta: [Neurriak hobetzeko iradokitako segmentuak](suggested-segments.md) 
- Jardueretan oinarritutako iradokizunak: [Iradokitako segmentuak bezeroen jardueran oinarrituta](suggested-segments-activity.md) 

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- Segmentu konplexua segmentu eraikitzailearekin: [Gurea eraiki](segment-builder.md#create-a-new-segment)

---

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

[!INCLUDE [progress-details-include](../includes/progress-details-pane.md)]

## <a name="export-segments"></a>Esportatu segmentuak

Segmentu bat esportatu dezakezu segmentuen orrialdetik edo [esportazioen orritik](export-destinations.md). 

1. Zoaz **Segmentuak** orrira.

1. Esportatu nahi duzun segmenturako, hautatu **erakutsi gehiago [...]**.

1. Aukeratu **Kudeatu esportazioak** ekintzen goitibeherako zerrendatik.

1. **Segmentuaren esportazioak (aurrebista)** orria irekitzen da. Konfiguratutako esportazio guztiak uneko segmentua duten edo ez taldeka ikus ditzakezu.

   1. Aukeratutako segmentua esportazio batera gehitzeko, **Editatu** dagokion esportazioa dagokion segmentua hautatzeko eta, ondoren, gorde. Banakako bezeroentzako inguruneetan zerrendako esportazioa aukeratu eta hautatu dezakezu **Gehitu segmentua** emaitza bera lortzeko.

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
