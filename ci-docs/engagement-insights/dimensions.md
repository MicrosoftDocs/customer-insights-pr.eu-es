---
title: Ikusi eta sortu dimentsioak
description: Nola sortu, editatu eta ezabatu dimentsioak.
ms.reviewer: mhart
ms.author: jusali
author: jusali
ms.date: 06/09/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: b575c5e84197d76f53a722bac60c5af928c917f9671720ede1de38c4a7478be4
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7033982"
---
# <a name="view-and-create-dimensions"></a>Ikusi eta sortu dimentsioak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Dimentsioa datuak deskribatu, iragazi edo taldeka ditzakeen gertaera baten atributua da. Zure webgunean marketin promozioa egiten ari bazara, dimentsioak erabil ditzakezu bisitariak erabiltzaile berrien eta itzultzen diren erabiltzaileen arabera sailkatzeko.  

Parte-hartzearen xehetasunek gertaeren propietateen erabiltzeko prest dauden dimentsioak ditu. Adibidez:

- Arakatzailearen izena
- Orriaren izena
- Gailuaren modeloa
- Sistema eragilea
- Herrialdea

## <a name="view-dimensions"></a>Ikusi dimentsioak

Dimentsioak lehendik dauden gertaeren propietateetan oinarritzen dira. Parte-hartzearen xehetasunen jarraipenerako kodea erabiltzen duzunean, sistemaren dimentsioak automatikoki sortzen dira.

1. Ezkerreko nabigazio-panelean, joan **datuak** atalera. 
1. Aukeratu **Dimentsioak** laneko eremuko dimentsio guztien zerrenda ikusteko. 
   > [!NOTE]
   > Sistemak sortutako dimentsioak irakurtzeko soilik dira. Ezin dituzu editatu. Dimentsio pertsonalizatuak bakarrik sor eta editatu ditzakezu.

## <a name="create-a-dimension"></a>Sortu dimentsio bat

Sistemak sortutako dimentsioez gain, inguruneko eta laneko eremuko administratzaileek dimentsio pertsonalizatuak sor ditzakete. Dimentsio pertsonalizatuak oinarrizko gertaeren propietate lehenetsietan oinarrituta daude edo [gertaera baten propietate pertsonalizatuak](advanced-SDK-implementation.md) erabil ditzakete.

1. Joan hona: **Datuak** > **Dimentsioak**.
1. Hautatu **Gehitu dimentsio bat**.

   :::image type="content" source="media/add-dimension.png" alt-text="Gehitu dimentsio bat gertaera bati.":::

1. **Sortu dimentsio bat** panelean, hautatu dimentsioa oinarritzeko propietate bat. Propietateen zerrendan dimentsio bati esleitu gabeko laneko eremuko propietate guztiak erakutsiko dira.
1. **Bistaratzeko izena** koadroan, idatzi izena. Aukeran, azalpena gehi dezakezu.
1. Dimentsioa gordetzeko, hautatu **sortu**. Minutu bat behar izan dezake dimentsioa [txosten pertsonalizatuan](custom-reports.md) edo [segmentuan](segments.md) erabili ahal izateko. 

## <a name="edit-a-dimension"></a>Editatu dimentsio bat

Dimentsio baten izena eta deskribapena alda ditzakezu.

1. Joan hona: **Datuak** > **Dimentsioak**.
1. Hautatu ezabatu nahi duzun dimentsioa.
1. **Editatu dimentsioa** panelean, eguneratu dimentsioa.
1. Aldaketak gordetzeko, sakatu **Aplikatu**.

## <a name="delete-a-dimension"></a>Ezabatu dimentsio bat

Erabiltzaileak sortutako dimentsioak soilik ezaba ditzakezu, baina ezin dituzu sistemaren dimentsioak kendu.

Dimentsio bat ezabatzea behin betikoa da. Ezabatutako dimentsioa erabiltzen duten txostenek eta segmentuek ez dute funtzionatuko. 

1. Joan hona: **Datuak** > **Dimentsioak**.
1. Hautatu ezabatu nahi duzun dimentsioa.
1. **Editatu dimentsioa** panelean, hautatu **ezabatu dimentsioa**.

   :::image type="content" source="media/delete-dimension.png" alt-text="Ezabatu dimentsio bat gertaera batetik.":::

1. Sartu **BAIMENDU EZABATZEA** (maiuskulaz) ezabaketa berresteko. 
1. Hautatu **Ezabatu**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
