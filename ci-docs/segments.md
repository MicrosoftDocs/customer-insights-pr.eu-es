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
ms.openlocfilehash: 4bcfbb50b893ca7e6ec4607d3c156a3c6979f775
ms.sourcegitcommit: 8a28e9458b857adf8e90e25e43b9bc422ebbb2cd
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/18/2022
ms.locfileid: "9170666"
---
# <a name="segments-overview"></a>Segmentuen informazio orokorra

Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu. Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.

Segmentu baten definizio baten iragazkiekin bat datozen bezeroen profilak deitzen dira *kideak* segmentu batena. [Zerbitzuaren muga](/dynamics365/customer-insights/service-limits) batzuk aplikatzen dira.

## <a name="create-a-segment"></a>Sortu segmentu bat

Aukeratu nola sortu segmentu bat zure xede-publikoaren arabera.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- Segmentu konplexuak segmentu-sorgailuarekin: [Eraiki zeurea](segment-builder.md)
- Operadore bakarreko segmentu sinpleak: [Segmentu azkarra](segment-quick.md)
- AI bidezko modua antzeko bezeroak aurkitzeko: [Antzeko bezeroak](find-similar-customer-segments.md)
- Neurri edo atributuetan oinarritutako AI bidezko iradokizunak: [Neurrietan oinarritutako iradokitako segmentuak](suggested-segments.md)
- Jardueretan oinarritutako iradokizunak: [Iradokitako segmentuak bezeroen jardueran oinarrituta](suggested-segments-activity.md)

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- Segmentu sinpleak edo konplexuak segmentu-sorgailuarekin: [Eraiki zeurea](segment-builder.md)

---

## <a name="manage-existing-segments"></a>Kudeatu lehendik dauden segmentuak

Joan zaitez **Segmentuak** orrialdean sortu dituzun segmentuak, haien egoera eta egoera, kide kopurua eta datuak freskatu diren azken aldia ikusteko. Segmentuen zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun segmentua aurkitzeko.

Hautatu segmentu bat erabilgarri dauden ekintzak ikusteko.

:::image type="content" source="media/segments-selected-segment.png" alt-text="Aukeratutako segmentua aukerak goitibeherako zerrendarekin eta eskuragarri dauden aukerekin." lightbox="media/segments-selected-segment.png":::

- [**Ikusi**](#view-segment-details) segmentuaren xehetasunak, kideen kopuruaren joera eta segmentuko kideen aurrebista barne.
- **Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.
- **Editatu** segmentuak bere propietateak aldatzeko.
- **Sortu bikoiztuak** segmentu baten. Bere propietateak berehala editatzea edo bikoiztua gordetzea aukera dezakezu.
- [**Freskatu**](#refresh-segments) azken datuak sartzeko segmentua.
- **Aktibatu** edo **Desaktibatu** segmentua. Segmentu inaktiboak ez dira freskatuko a bitartean [programatutako freskagarritasuna](system.md#schedule-tab) eta izan **Egoera** gisa zerrendatuta **Saltatu**, freskatze bat ere saiatu ez dela adieraziz. Segmentu aktiboak beren motaren arabera freskatzen dira: estatikoak edo dinamikoak.
- **Estatikoa egin** edo **Dinamizatu** segmentu mota. Segmentu estatikoak eskuz freskatu behar dira. Segmentu dinamikoak automatikoki freskatzen dira sistemaren freskagarrietan.
- [**Bilatu antzeko bezeroak**](find-similar-customer-segments.md) segmentutik.
- **Aldatu izena** segmentuari.
- **Etiketa** to [kudeatu etiketak](work-with-tags-columns.md#manage-tags) segmenturako.
- [**Kudeatu esportazioak**](#export-segments) esportazioekin lotutako segmentuak ikusteko eta kudeatzeko. [Lortu esportazioei buruzko informazio gehiago.](export-destinations.md)
- **Ezabatu** segmentua.
- **Zutabeak** to [pertsonalizatu zutabeak](work-with-tags-columns.md#customize-columns) pantaila hori.
- **Iragazkia** to [iragazkia etiketetan](work-with-tags-columns.md#filter-on-tags).
- **Bilatu izena** segmentuaren izenaren arabera bilatzeko.

## <a name="view-segment-details"></a>Ikusi segmentuaren xehetasunak

Gainean **Segmentuak** orrialdean, hautatu segmentu bat prozesatzeko historia eta segmentu kideak ikusteko.

Orriaren goiko aldean joera grafikoa dago, kideen zenbateko aldaketak bistaratzen dituena. Pasa datuak gainetik kideak data jakin batean ikusteko. Aldatu bistaratzeko denbora-tartea.

:::image type="content" source="media/segment-time-range.png" alt-text="Segmentuaren denbora-tartea.":::

Beheko aldean segmentuko kideen zerrenda dago.

> [!NOTE]
> Zerrenda honetan agertzen diren eremuak zure segmentuko entitateen atributuetan oinarrituta daude.
>
>Zerrenda bat datorren segmentuko kideen aurrebista da eta zure segmentuko lehen 100 erregistroak erakusten ditu, behar bezala baloratu eta haren definizioak berrikusteko. Bat datozen erregistro guztiak ikusteko, [segmentua esportatu](export-destinations.md).

## <a name="refresh-segments"></a>Freskatu segmentuak

Segmentuak programazio automatiko batean freskatu daitezke edo eskuz, eskaeraren arabera. Segmentu bat edo gehiago eskuz freskatzeko, hautatu eta aukeratu **Freskatu**.

To [programatu freskatze automatikoa](system.md#schedule-tab), joan **Admin** > **Sistema** > **Ordutegia**. Arau hauek aplikatzen dira:

- Mota duten segmentu guztiak **Dinamikoa** edo **Hedapena** ezarritako kadentzian automatikoki freskatuko da. Freskatzea amaitutakoan, **Egoera** segmentua freskatzeko arazoren bat egon den adierazten du. The **Azken freskatua** Azken freskatze arrakastatsuaren denbora-zigilua erakusten du. Errore bat gertatzen bada, hautatu errorea gertatu denari buruzko xehetasunak ikusteko.
- Mota duten segmentuak **Estatikoa** *ez* automatikoki freskatu. The **Azken freskatua** segmentu estatiko eskuz exekutatu edo freskatu den azken aldiaren denbora-zigilua erakusten du.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="export-segments"></a>Esportatu segmentuak

Esportatu segmentuak beste aplikazio batzuetara datuak gehiago erabiltzeko. Esportatu segmentu bat segmentuen orrialdetik edo [esportazio orria](export-destinations.md).

1. Joan zaitez **Segmentuak** orrialdea eta hautatu esportatu nahi duzun segmentua.

1. Hautatu **Kudeatu esportazioak**. **Segmentuaren esportazioak (aurrebista)** orria irekitzen da. Ikusi konfiguratutako esportazio guztiak uneko segmentua duten ala ez taldekatuta.

   1. Aukeratutako segmentua esportazio batera gehitzeko, **Editatu** dagokion esportazioa dagokion segmentua hautatzeko eta, ondoren, gorde. Bezero indibidualentzako inguruneetan, hautatu esportazioa zerrendan eta hautatu **Gehitu segmentua** emaitza bera lortzeko.

   1. Aukeratutako segmentuarekin esportazio berri bat sortzeko, hautatu **Gehitu esportazioa**. Esportazioak sortzeari buruzko informazio gehiago lortzeko, ikusi [Konfiguratu esportazio berria](export-destinations.md#set-up-a-new-export).

1. Aukeratu **Itzuli** segmentuen orri nagusira itzultzeko.

## <a name="track-usage-of-a-segment"></a>Jarraitu segmentu baten erabilera

Beran oinarritzen diren aplikazioetan segmentuak erabiltzen badituzu Microsoft Dataverse Customer Insights-ekin konektatuta dagoen erakundea, segmentu baten erabileraren jarraipena egin dezakezu. Izan ere [Dynamics 365 Marketing-en bezeroen bidaietan erabiltzen diren Customer Insights segmentuak](/dynamics365/marketing/real-time-marketing-ci-profile), sistemak segmentu horren erabileraren berri ematen dizu.

Customer Insights ingurunean edo marketineko bezero-bidaia batean erabiltzen ari den segmentu bat editatzean, pankarta bat [segmentu eraikitzailea](segment-builder.md) mendekotasunen berri ematen dizu. Ikuskatu mendekotasunaren xehetasunak zuzenean pankartatik edo hautatuz **Erabilera** segmentu-eraikitzailean.

The **Segmentuaren erabilera** panelean segmentu honen erabilerari buruzko xehetasunak erakusten ditu Dataverse oinarritutako aplikazioak. Bezeroen bidaietan erabiltzen diren segmentuetarako, segmentu hori erabiltzen den Marketing-en bidaia ikuskatzeko esteka aurkituko duzu. Marketing aplikaziora sartzeko baimenak badituzu, ikusi xehetasun gehiago bertan.

:::image type="content" source="media/segment-usage-pane.png" alt-text="Alboko panela segmentu-eraikitzailean segmentuen erabileraren xehetasunekin.":::

Sistemak jarraipenaren segmentu baten erabileraren berri ematen dizu hura ezabatzen saiatzen zarenean. Ezabatzera zoazen segmentua Marketing-en bezero-bidaia batean erabiltzen bada, bidaia hori gelditu egingo da segmentuko erabiltzaile guztientzat. Bidaia marketin kanpaina baten parte bada, ezabatzeak kanpaina horri berari eragingo dio. Hala ere, oraindik segmentua ezaba dezakezu abisuak izan arren.

:::image type="content" source="media/segment-usage-delete.png" alt-text="Elkarrizketa-koadroa segmentu ezabatzea berresteko, segmentu bat erabiltzen denean Dataverse aplikazio.":::

### <a name="supported-apps"></a>Onartutako aplikazioak

Une honetan erabileraren jarraipena egiten da Dataverse - Oinarritutako aplikazioak:

- [Bezeroen bidaiak Dynamics 365 Marketing-en](/dynamics365/marketing/real-time-marketing-ci-profile)

[!INCLUDE [footer-include](includes/footer-banner.md)]
