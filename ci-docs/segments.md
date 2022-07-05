---
title: Segmentuen informazio orokorra
description: Segmentuen ikuspegi orokorra eta nola sortu eta kudeatu.
ms.date: 05/20/2022
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
ms.openlocfilehash: 8b2c2f9b84bf8b7f37d1468b871946ecb3e6aa98
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9050932"
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
- **Sortu bikoiztuak** segmentu baten. Bere propietateak berehala editatzea edo bikoiztua gordetzea aukera dezakezu.
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

- Mota duten segmentu guztiak **Dinamikoa** edo **Hedapena** ezarritako kadentzian automatikoki freskatuko da. Freskatzea amaitutakoan **Egoera** segmentua freskatzeko arazoren bat egon den adierazten du. The **Azken freskatua** Azken freskatze arrakastatsuaren denbora-zigilua erakusten du. Errore bat gertatzen bada, hautatu errorea gertatu denari buruzko xehetasunak ikusteko.
- Mota duten segmentuak **Estatikoa** *ez* automatikoki freskatu. The **Azken freskatua** Segmentu estatikoak eskuz exekutatu edo freskatu diren azkeneko denbora-zigilua erakusten du.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="export-segments"></a>Esportatu segmentuak

Segmentu bat esportatu dezakezu segmentuen orrialdetik edo [esportazioen orritik](export-destinations.md). 

1. Zoaz **Segmentuak** orrira.

1. Hautatu elipsi bertikala (&vellip;) esportatu nahi duzun segmenturako.

1. Aukeratu **Kudeatu esportazioak** ekintzen goitibeherako zerrendatik.

1. **Segmentuaren esportazioak (aurrebista)** orria irekitzen da. Konfiguratutako esportazio guztiak uneko segmentua duten edo ez taldeka ikus ditzakezu.

   1. Aukeratutako segmentua esportazio batera gehitzeko, **Editatu** dagokion esportazioa dagokion segmentua hautatzeko eta, ondoren, gorde. Bezero indibidualentzako inguruneetan, horren ordez esportazioa hautatu dezakezu zerrendan eta hautatu **Gehitu segmentua** emaitza bera lortzeko.

   1. Aukeratutako segmentuarekin esportazio berri bat sortzeko, hautatu **Gehitu esportazioa**. Esportazioak sortzeari buruzko informazio gehiago lortzeko, ikusi [Konfiguratu esportazio berria](export-destinations.md#set-up-a-new-export).

1. Aukeratu **Itzuli** segmentuen orri nagusira itzultzeko.

## <a name="track-usage-of-a-segment"></a>Jarraitu segmentu baten erabilera

Aplikazioetan segmentuak erabiltzen badituzu, berdinetan oinarritzen direnak Microsoft Dataverse Customer Insights-ekin konektatuta dagoen erakundea, segmentu baten erabileraren jarraipena egin dezakezu. Izan ere [Dynamics 365 Marketing-en bezeroen bidaietan erabiltzen diren Customer Insights segmentuak](/dynamics365/marketing/real-time-marketing-ci-profile), sistemak segmentu horren erabileraren berri ematen dizu.

Customer Insights ingurunean edo marketineko bezero-bidaia batean erabiltzen ari den segmentu bat editatzean, pankarta bat [segmentu eraikitzailea](segment-builder.md) mendekotasunen berri ematen dizu. Mendekotasunaren xehetasunak zuzenean ikus ditzakezu pankartatik edo hautatuz **Erabilera** segmentu-eraikitzailean.

The **Segmentuaren erabilera** panelean segmentu honen erabilerari buruzko xehetasunak erakusten ditu Dataverse oinarritutako aplikazioak. Bezeroen bidaietan erabiltzen diren segmentuetarako, segmentu hori erabiltzen den Marketing-en bidaia ikuskatzeko esteka aurkituko duzu. Marketing aplikaziora sartzeko baimenak badituzu, xehetasun gehiago atzi ditzakezu bertan.

:::image type="content" source="media/segment-usage-pane.png" alt-text="Alboko panela segmentuen erabileraren xehetasunekin segmentu-sortzailean.":::

Sistemak jarraipenaren segmentu baten erabileraren berri ematen dizu hura ezabatzen saiatzen zarenean. Ezabatzera zoazen segmentua Marketing-en bezero-bidaia batean erabiltzen bada, bidaia hori gelditu egingo da segmentuko erabiltzaile guztientzat. Bidaia marketin kanpaina baten parte bada, ezabatzeak kanpaina horri berari eragingo dio. Hala ere, oraindik segmentua ezaba dezakezu abisuak izan arren.

:::image type="content" source="media/segment-usage-delete.png" alt-text="Elkarrizketa-koadroa segmentua ezabatzea berresteko, segmentu bat erabiltzen denean Dataverse aplikazio.":::

### <a name="supported-apps"></a>Onartutako aplikazioak

Une honetan erabileraren jarraipena egiten da Dataverse - Oinarritutako aplikazioak:

- [Bezeroen bidaiak Dynamics 365 Marketing-en](/dynamics365/marketing/real-time-marketing-ci-profile)

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

[!INCLUDE [footer-include](includes/footer-banner.md)]
