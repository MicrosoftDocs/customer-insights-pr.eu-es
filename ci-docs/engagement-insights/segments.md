---
title: Ikusi eta sortu segmentuak
description: Segmentuak nola sortu, editatu eta ezabatu eta non erabili.
ms.reviewer: mhart
ms.author: jusali
author: jusali
ms.date: 06/09/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: cedcd58373428dd35ba29ce8fdd00007257f8fa59b0d25bc584b4e832df13604
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036133"
---
# <a name="view-and-create-segments"></a>Ikusi eta sortu segmentuak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Segmentuei esker, bisitarien azpimultzoak identifikatu ditzakezu ezaugarrien edo webgunearen elkarreraginen arabera. Segmentuei esker iragazkiak aplikatu eta azpimultzo horiek aztertu ditzakezu. Analisiak zure negozioaren joerak aztertzen eta erantzuten lagun dezake. 

:::image type="content" source="media/segments-page.png" alt-text="Laneko espazio batean dauden segmentuen zerrenda erakusten duen parte-hartzearen xehetasunen aplikazioaren pantaila-argazkia.":::

## <a name="view-segments"></a>Ikusi segmentuak

1. Ezkerreko nabigazio-panelean, joan **datuak** atalera. 

1. Aukeratu **Segmentuak** fitxa laneko eremuko segmentu guztien zerrenda ikusteko. 

## <a name="create-a-segment"></a>Sortu segmentu bat

Segmentuak eragile logikoekin lotuta dauden arau eta baldintzez osatuta daude. Baldintzek iragazkiak aplikatzen dituzte hautatutako dimentsio batean. Segmentu bakoitzak gehienez bost dimentsio erabil ditzake.

Hurrengo adibidean arau bakarrean bi baldintza dituen segmentua erakusten da. Chrome nabigatzailea eta iOS edo Android sistema eragilea dituen gailu bateko webguneko eskaera guztiak iragazten ditu.

:::image type="content" source="media/segment-sample.png" alt-text="Arau batean bi baldintza dituzten segmentuen adibidea webguneko gertaerak iragazteko.":::

Atal honetan a nola sortu deskribatzen da *segmentu hutsa* hutsetik.

1. Joan hona: **Datuak** > **Segmentuak**.

1. Hautatu **Segmentu berria**.

1. **Baliabideen liburutegia** atalean, aukeratu zein atributuren arabera iragazi nahi duzun. Gaur egun, dimentsioetan oinarritutako segmentuak bakarrik sor ditzakezu.

1. Aukeratu operadorea eta balio bat hautatutako atributurako. Eragiketa hauek onartzen dira.
   - **da**: bat-etortze zehatza behar du balioak sartzeko. **Honen berdina** erabiltzen du balio bakarrerako edo **edozein** balio anitz sartzeko.
   - **ez da**: bat-etortze zehatza behar du balioak kanpoan uzteko. **Honen berdina** erabiltzen du balio bakarrerako edo **edozein** balio anitz sartzeko.
   - **honekin hasten da**: bat datozen balioekin hasten den katea.
   - **honekin amaitzen da**: bat datozen balioekin amaitzen den katea.
   - **dauka**: bat datorren balioetan jasotako katea.

1. Talde bati baldintza gehiago gehitzeko, bi operadore logiko erabil ditzakezu. Multzo operadoreak erabiltzean proiektatutako atributuak kontuan hartzen dira.
   - **ETA** operadorea: Bi baldintza segmentazio prozesuaren baitan bete behar dira. Aukera hau baliagarria da entitate desberdinetan baldintzak definitzen dituzunean.
   - **EDO** operadorea: Baldintzaren bat segmentazio prozesuaren zati gisa bete behar da. Aukera hau oso baliagarria da hainbat baldintza definitzen dituzunean entitate berarentzat.

1. Hautatu **gorde** eta jarri izena segmentuari. 

Segmentua Segmentuak orrian agertuko da eta laneko eremuko txosten eta inbutu guztiei aplika diezaiekezu.

## <a name="use-a-segment-in-a-report-or-funnel"></a>Erabili segmentu bat txosten edo inbutu batean

Segmentuak txosten bati edo inbutu bati aplika diezaiekezu, segmentuaren baldintzetan oinarrituta. Hala ere, ezin dituzu segmentuak denbora errealeko erabilera txostenean aplikatu.

:::image type="content" source="media/segment-reports-filter.png" alt-text="Orrialde bistaratutako txostena goitibeherako zerrenda zabaldua zein segmentu aplikatu aukeratzeko.":::

Segmentu bat aplikatzeko, ireki txostena edo inbutua. Aukeratu **Gehitu baldintza** eta aukeratu **Iragazi segmentuaren arabera**. Hautatu zerrendatik aplikatu nahi duzun segmentua. Segmentua txostenean aplikatuko da. Diagrama batek segmentua onartzen ez badu, errore bat agertzen da.
 
*Gehienez hiru segmentu* aplika ditzakezu txosten edo inbutu batean.

## <a name="edit-a-segment"></a>Editatu segmentu bat

1. Joan hona: **Datuak** > **Segmentuak**.
1. Aukeratu zerrendako segmentua, hori irekitzeko. 
1. Aldatu edo gehitu balioak, beharraren arabera.
1. Aldaketak aplikatzeko, hautatu **Gorde**.

## <a name="change-the-name-of-a-segment"></a>Aldatu segmentu baten izena

1. Joan hona: **Datuak** > **Segmentuak**.
1. Segmentuen zerrendan, hautatu **Gehiago [...]**. 
1. Aukeratu **Editatu izena** goitibeherako zerrendatik.
1. Idatzi izen berria eta sakatu **Jarri izen berria**.

## <a name="delete-a-segment"></a>Ezabatu segmentu bat

1. Joan hona: **Datuak** > **Segmentuak**.
1. Segmentuen zerrendan, hautatu **Gehiago [...]**. 
1. Aukeratu **Ezabatu** goitibeherako zerrendatik.
1. Berresteko, hautatu **ezabatu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
