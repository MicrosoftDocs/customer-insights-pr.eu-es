---
title: Hartzaileen xehetasunen segmentuak
description: Segmentuen ikuspegi orokorra eta nola sortu eta kudeatu.
ms.date: 03/30/2022
ms.subservice: audience-insights
ms.topic: overview
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-customers-page
- ci-enrichment-details
- ci-segments
- ci-segment-details
- customerInsights
ms.openlocfilehash: 68e71df3853470af47228c7365f25db3a71d15b0
ms.sourcegitcommit: 9ef2cf99b847e7bd8f890f83d84b3a4045aaf8cc
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/01/2022
ms.locfileid: "8529524"
---
# <a name="segments-overview"></a>Segmentuen informazio orokorra

Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu. Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.

Segmentuaren definizio baten iragazkiekin bat datozen bezeroen profilak aipatzen dira *kideak* segmentu batena. [Zerbitzuaren muga](/dynamics365/customer-insights/service-limits) batzuk aplikatzen dira.

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

Joan zaitez **Segmentuak** orrialdean gordetako segmentu guztiak ikusteko eta kudeatzeko.

Segmentu bakoitza segmentuari buruzko informazio osagarria biltzen duen errenkada batez irudikatuta dago.

:::image type="content" source="media/segments-selected-segment.png" alt-text="Aukeratutako segmentua aukerak goitibeherako zerrendarekin eta eskuragarri dauden aukerekin." lightbox="media/segments-selected-segment.png":::

Ekintza hauek erabilgarri daude segmentu bat hautatzen duzunean:

- **ikusi** segmentuko xehetasunak, kideen zenbaketa joera segmentuko kideen aurrebista barne.
- **Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.
- **Editatu** segmentuak bere propietateak aldatzeko.
- **Sortu bikoiztuak** segmentu baten. Bere propietateak berehala editatzea edo bikoiztua gordetzea aukeratu dezakezu.
- **Freskatu** segmentuak azken datuak sartuko ditu.
- **Aktibatu** edo **Desaktibatu** segmentua. Segmentu inaktiboetan, segmentuaren definizioa badago, baina oraindik ez du bezeroik. Segmentu aktibo batek segmentuaren definizioarekin bat datozen bezeroak bilatzen ditu. A bada [freskatze programatua](system.md#schedule-tab) konfiguratuta dago, segmentu inaktiboek dute **Egoera** gisa zerrendatuta **Saltatuta**, freskatzen saiatu ere ez zela egin adieraziz. Segmentu inaktiboa aktibatzen denean, freskatu egingo da eta programatutako freskapenetan sartuko da.
  Bestela, erabil dezakezu **Ordutegiak beranduago** funtzionaltasuna **Aktibatu / Desaktibatu** goitibehera, segmentu jakin bat aktibatzeko eta desaktibatzeko etorkizuneko data eta ordua zehazteko.
- **[Bilatu antzeko bezeroak](find-similar-customer-segments.md)** segmentutik.
- **Aldatu izena** segmentuari.
- **Etiketa** to [kudeatu etiketak](work-with-tags-columns.md#manage-tags) segmenturako.
- **Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.
- **Kudeatu esportazioak** esportazioekin lotutako segmentua ikusteko eta kudeatzeko. [Lortu esportazioei buruzko informazio gehiago.](export-destinations.md)
- **Ezabatu** segmentua.
- **Zutabeak** to [pertsonalizatu zutabeak](work-with-tags-columns.md#customize-columns) pantaila hori.
- **Iragazkia** to [iragazkia etiketetan](work-with-tags-columns.md#filter-on-tags).
- **Bilatu izena** segmentuaren izenaren arabera bilatzeko.

## <a name="refresh-segments"></a>Freskatu segmentuak

Segmentu guztiak freskatu ditzakezu aldi berean hautatuta **Freskatu guztiak** gainean **segmentuak** orrialdea edo segmentu bat edo gehiago freskatu ditzakezu hautatzen dituzunean eta aukeratutakoan **Freskatu** aukeren artean. Bestela, berriztagarria den aldizka konfigura dezakezu **administratzailea** > **Sistema** > **Ordutegiak**. Berriro errepikatzen den freskagarri bat konfiguratzen denean, arau hauek aplikatzen dira:
- Mota duten segmentu guztiak **Dinamikoa** edo **Hedapena** ezarritako kadentzian automatikoki freskatuko da. Freskatzea amaitzen denean **Egoera** segmentua freskatzeko arazoren bat egon den adierazten du. The **Azken freskatua** Azken freskatze arrakastatsuaren denbora-zigilua erakusten du. Errore bat gertatzen bada, hautatu errorea gertatutakoari buruzko xehetasunak ikusteko.
- Mota duten segmentuak **Estatikoa** *ez* automatikoki freskatu. The **Azken freskatua** Segmentu estatikoak eskuz exekutatu edo freskatu ziren azken aldiaren denbora-zigilua erakusten du.

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
