---
title: Ikusi eta sortu metrikak
description: Nola sortu, editatu eta ezabatu estatistikak.
ms.reviewer: mhart
ms.author: jusali
author: jusali
ms.date: 06/09/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: 97189168e0f5586aad8be8089a1f9e27893c2115c7e805ddaab1efc00e11b860
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7034254"
---
# <a name="view-and-create-metrics"></a>Ikusi eta sortu metrikak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Estatistikek zure bisitarien portaera ulertzen laguntzen dute. Gertaeren propietateak biltzen dituzte eta zure web propietateen estatistikak eta errendimendua neurtzen dituzte.  

Demagun marketineko promozioa egiten ari zarela zure webgunean. Estatistikak erabil ditzakezu promozioan zehar zure webgunera etorri diren bisitari edo erabiltzaileen kopuruaren jarraipena egiteko. Estatistikak aztertzeak zure webguneko audientzia hobeto ulertzen lagunduko dizu. Estatistikak eta [dimentsioak](dimensions.md) konbinatuz [txosten pertsonalizatu](custom-reports.md) batean, portaera neurtzeko aukera ematen dizu zure erabiltzaileak ulertzeko. Adibidez, bisitariak kategoria berrietan eta lehengo kategorietan bereiz ditzakezu taldeen interes eta asmo desberdintasunak identifikatzeko.

## <a name="view-metrics"></a>Ikusi estatistikak

Parte-hartzearen xehetasunek gertaeren propietateen erabilitako agregazioak biltzen ditu sistemaren estatistika gisa: 

- Bisitariak
- Bisitak
- Orriaren ikuspegiak
- Klik kopurua

Sistemaren estatistika hauek oinarrizko gertaeretan dauden gertaeren propietateetan oinarritzen dira.

1. Ezkerreko nabigazio-panelean, joan **datuak** atalera. 
1. Aukeratu **Estatistikak** fitxa laneko eremuan estatistika guztien zerrenda ikusteko. 
   > [!NOTE]
   > Sistemak sortutako estatistikak irakurtzeko soilik dira. Ezin dituzu aldatu edo ezabatu. Estatistika pertsonalizatuak sortu eta editatu ditzakezu.

## <a name="create-a-metric"></a>Sortu estatistika

Ingurumeneko eta laneko espazioko administratzaileek estatistikak sor ditzakete. Gertaeren propietateak lan-eremura bidali behar dira estatistika sortu aurretik. Oinarrizko gertaerek bidalitako gertaeren propietateetan oinarritutako estatistikak sor ditzakezu edo web SDKerabil dezakezu [gertaeren propietate pertsonalizatuak bidaltzeko](advanced-SDK-implementation.md).

1. Joan **Datuak** > **estatistikak** atalera.
1. Hautatu **estatistika berria**.

   :::image type="content" source="media/new-metric.png" alt-text="Gehitu estatistika gertaera bati.":::

1. Formatuari dagokionez, hautatu **Zenbaki osoak** edo **Bikoitza** datu mota. Zenbaki osoa zenbaki osoa da. Bikoitzari dagokionez, hamartarren bat eta hiru artean aukeratu ditzakezu.
1. **Baliabideen liburutegia** panelean, bilatu estatistika oinarritzeko gertaeraren propietatea.
1. Aukeratu **plus ikurra (+)** formulan erabiltzeko propietatearen ondoan. Propietate batean oinarritutako formula bat soilik sor dezakezu. 
1. Hautatu funtzio agregatu hauetako bat. 

   - Batuketa: balio guztien aritmetika 
   - Batez bestekoa: balio guztien batez bestekoa
   - Zenbakia: balioen kopuru osoa
   - Balio esklusiboen kopurua: balio esklusiboen kopuru osoa

   Estatistika definitu ondoren, azken orduko estatistikaren jardueren aurrebista ikusiko duzu.

1. Sakatu **Gorde**. 
1. Idatzi estatistikaren izena eta, ondoren, hautatu **Hurrengoa**.

Estatistikak minutu bat behar izan ditzake [txosten pertsonalizatuak sortzeko](custom-reports.md) erabili ahal izateko.

## <a name="edit-a-metric"></a>Editatu estatistika bat

1. Joan **Datuak** > **estatistikak** atalera.
1. Hautatu estatistika zerrendan.
1. Estatistikaren definizioa aldatu
1. Sakatu **Gorde**.

## <a name="change-the-name-of-a-metric"></a>Aldatu estatistika baten izena

1. Joan **Datuak** > **estatistikak** atalera.
1. Aukeratu **Gehiago [...]** estatistikarako eta aukeratu **Editatu izena**.
1. Aldatu izena. 
1. Aukeratu **Aldatu izena**.

## <a name="delete-a-metric"></a>Ezabatu estatistika bat

1. Joan **Datuak** > **estatistikak** atalera.
1. Aukeratu **Gehiago [...]** estatistikarako eta aukeratu **ezabatu**.

   :::image type="content" source="media/delete-metric.png" alt-text="Ezabatu estatistika gertaera batetik.":::

1. Hautatu **Ezabatu** ezabatzea baieztatzeko.

[!INCLUDE[footer-include](../includes/footer-banner.md)]