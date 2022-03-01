---
title: Esportazio-helburuak
description: Esportatu datuak eta kudeatu esportatzeko helmugak.
ms.date: 07/21/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 9032d99357db86e66588eda544211a5f8eb2f23b
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643848"
---
# <a name="export-destinations-preview"></a>Esportazio-helburuak (aurrebista)

**Esportaziorako helmugak** orrialdeak datuak esportatzeko ezarri dituzun kokapen guztiak erakusten dizkizu. Helmuga berriak ere gehitu ditzakezu esportaziorako. Gainera, unean eskuragarri dauden esportatzeko aukerak erakusten ditu. Lortu ikuspegi orokorra, deskribapena eta jakin zer egin dezakezu hedagarritasun aukera bakoitzarekin. Esportatu profilak, neurriak eta segmentuak bateratzea negoziorako garrantzitsuak diren aplikazioetara.

Joan **admin** > **Esportaziorako helmugak** zabalgarritasun aukera hauek aurkitzeko:

- [Dynamics 365 Bezeroaren txartelaren osagarria](customer-card-add-in.md)
- [Facebook Iragarkien kudeatzailearen konektorea](export-facebook.md)
- [Power Automate konektorea](export-power-automate.md)
- [Power Apps konektorea](export-power-apps.md)
- [Power BI konektorea](export-power-bi.md)
- [DotDigital](export-dotdigital.md)
- [Dynamics 365 Sales](export-dynamics365-sales.md)
- [Dynamics 365 Marketing](export-dynamics365-marketing.md)
- [Azure Blob Storage](export-azure-blob-storage.md)
- [LiveRamp&reg; konektorea](export-liveramp.md)
- [Bot egiteko Microsoft Teams](export-teams-bot.md)
- [Mailchimp](export-mailchimp.md)
- [Customer Insights API](apis.md)

## <a name="add-a-new-export-destination"></a>Gehitu beste esportazio-helburu bat

Esportazio helmugak gehitzeko, [administratzaile baimenak](permissions.md) dituzu. Microsoft zerbitzuetara esportatzen baduzu, bi zerbitzuak erakunde berean daudela suposatuko dugu.

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. Sar ezazu teklara **Nire esportazio helmuga** fitxa.

1. Hautatu **Gehitu helmuga** esportatzeko helmuga berria sortzeko.

1. Sarbidean **Helmuga gehitu** hautatu panela **Mota** esportazio-helmuga goitibeherakoan.

1. Eman beharrezko xehetasunak eta hautatu **hurrengo** esportazio-helmuga sortzeko.

Aukeratu ere egin dezakezu **Konfiguratu** teila batean **Ezagutu** fitxa.

## <a name="view-export-destinations"></a>Ikusi Esportatu helburuak

Esportazio helmugak sortu ondoren, ondoko taulan aurkituko dituzu **Nire esportazio helmuga** fitxa. Taula honek hiru zutabe ditu:

- **Bistaratu izena**: Helmuga sortzerakoan idatzi duzun izena.
- **Mota**: Helmuga sortzean zuk ezarri duzun esportazio helmuga mota.
- **Noiz sortua**: helburua sortu zenuen data.

## <a name="edit-an-export-destination"></a>Editatu esportatze helmuga

1. Hautatu elipsi bertikala editatu nahi duzun Export helmugarako.

   > [!div class="mx-imgBorder"]
   > ![Elipsi bertikala](media/export-destinations-page-ellipsis.png "Elipsi bertikala")

1. Hautatu **Editatu** goitibeherako menuan.

1. Aldatu eguneratzea eskatzen duten balioak eta hautatu **Gorde**.

## <a name="export-data-on-demand"></a>Esportatu datuak eskatu ahala

Esportazio helmugarako konektore bat konfiguratu ondoren, esportazio guztiekin egingo da [programatutako freskagarria](system.md#schedule-tab).

Programatutako freskapenaren zain egon gabe datuak esportatzeko, joan **Nire esportazio helmuga** fitxan **administratzailea** > **Esportaziorako helmugak**.

> [!div class="mx-imgBorder"]
> ![Elipsi bertikala](media/export-destinations-page-ellipsis.png "Elipsi bertikala")

- Aukeratu **Esportatu** zerrendaren gainetik esportazioa helmuga guztietara aldi berean exekutatzeko.
- Hautatu elipsia (...) zerrendako elementu baten ostean eta ondoren hautatu **Esportatu** Aukera esportazioa helmuga bakar baterako exekutatzeko aukera.

## <a name="remove-an-export-destination"></a>Ezabatu Export helmuga

Esportazio helmuga bat kentzeko, hasi nagusitik **Esportaziorako helmugak** orria.

1. Hautatu elipsi bertikala kendu nahi duzun Export helmugarako.

   > [!div class="mx-imgBorder"]
   > ![Elipsi bertikala](media/export-destinations-page-ellipsis.png "Elipsi bertikala")

2. Hautatu **Kendu** goitibeherako menuan.

3. Baieztatu kentzea aukeratuz **Kendu** berrespen-pantailan.
