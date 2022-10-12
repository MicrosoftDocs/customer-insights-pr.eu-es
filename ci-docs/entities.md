---
title: Entitateak Customer Insights-en
description: Ikusi datuak Entitateen orrian.
ms.date: 08/04/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-entities
- customerInsight
ms.openlocfilehash: e365945b27e7c985ca5371c6b72619610b6f3af1
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610083"
---
# <a name="entities-in-customer-insights"></a>Entitateak Customer Insights-en

Ondoren [zure datu-iturriak konfiguratuz](data-sources.md), joan **erakundeak** iradokitako datuen kalitatea ebaluatzeko orria. Entitateak datu multzo gisa hartzen dira. Dynamics 365 Customer Insights-eko hainbat gaitasun entitate horien inguruan eraikitzen dira. Hurbiletik berrikusteak gaitasun horien irteera balioztatzen lagun dezake.

Customer Insights-en zure datuak aberasten edo segmentuak, neurriak eta jarduerak sortzen ari zaren bitartean, ekintza horietatik sortzen diren entitateak pantailan bistaratzen dira.**Entitateak** orrialdea.

## <a name="view-a-list-of-entities"></a>Ikusi entitateen zerrenda

Joan **Datuak** > **Entitateak** entitateen zerrenda ikusteko. Entitate bakoitzerako hurrengo informazioa bistaratzen da.

- **Izena** : Datu-entitatearen izena. Entitate izenaren ondoan abisu sinbolo bat ikusiz gero, entitate horretako datuak ez dira behar bezala kargatu esan nahi du.
- **Iturria** : Entitatea irentsi duen datu-iturburu mota.
- **Eguneratua** : Entitatea azken aldiz eguneratu zen ordua.
- **Egoera** : Entitatearen azken eguneraketari buruzko xehetasunak.

## <a name="explore-a-specific-entitys-data"></a>Arakatu entitate jakin baten datuak

1. Joan **Datuak** > **Entitateak**.
1. Hautatu entitate bat xehetasunen orria irekitzeko.  
1. Arakatu entitate horretarako sartutako eremu eta erregistro desberdinak.

- The **Atributuak** fitxa lehenespenez hautatuta dago eta hautatutako entitatearen xehetasunak erakusten ditu, hala nola eremu-izenak, datu-motak eta motak. **Mota** zutabeak Datuen eredu arruntari lotutako sistemak erakusten ditu, sistemak edo identifikatutako autoak [eskuz mapatuta](map-entities.md) erabiltzaileek. Mota hauek atributuen datu motetatik desberdinak izan daitezkeen mota semantikoak dira. Esaterako, eremua *Posta elektronikoa* behean datu mota bat dauka *Katea* baina bere (semantikoa) Common Data Model mota izan daiteke *Posta elektronikoa*, *elektroniko helbidea*, edo *Nortasuna.Zerbitzua.Eposta*.

   :::image type="content" source="media/data-manager-entities-fields.png" alt-text="Eremuen taula.":::

   > [!NOTE]
   > Orrialde honek zure entitatearen datuen lagin bat baino ez du erakusten. Datu multzo osoa ikusteko, joan hona **Datu-iturriak** orrialdea, hautatu entitate bat, hautatu **Editatu**, eta, ondoren, ikusi entitate honen datuak Power Query atalean azaltzen den editorea [Datu-iturriak](data-sources.md).

   Entitatean irensten diren datuei buruz gehiago jakiteko, **Laburpen** zutabeak datu-ezaugarri garrantzitsu batzuk eskaintzen ditu, hala nola, nuluak, falta diren balioak, balio esklusiboak, zenbaketak eta banaketak, zure datuetarako aplikagarria dena. Hautatu diagramaren ikonoa datuen laburpena ikusteko.

   :::image type="content" source="media/data-manager-entities-summary.png" alt-text="Datuen laburpen-taula.":::

- The **Datuak** fitxak entitatearen erregistro indibidualei buruzko xehetasunak erakusten ditu. Zerrendatutako xehetasunak entitatearen datu-motaren araberakoak dira.

   :::image type="content" source="media/data-manager-entities-data.png" alt-text="Hautatu entitate bat.":::

- The **Txostenak** fitxak (entitate batzuentzat erabilgarri) zure datuak ikus ditzakezu txosten bat sortuz, zutabe hauek barne:

  - **Txostenaren izena** : Txostenaren izena.
  - **Sortua** : Entitatea sortu duen pertsonaren izena.
  - **Sortu** : Entitatearen sorreraren data eta ordua.
  - **Egileak editatua** : Entitatea aldatu duen pertsonaren izena.
  - **Editatua** : Erakundearen aldaketaren data eta ordua.

[!INCLUDE [footer-include](includes/footer-banner.md)]
