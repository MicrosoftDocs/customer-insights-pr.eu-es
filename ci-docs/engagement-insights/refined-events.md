---
title: Sortu eta aldatu gertaerak
description: Nola sortu eta aldatu gertaerak.
ms.reviewer: mhart
ms.author: jefhar
author: mochimochi016
ms.date: 10/01/2021
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: dbafa2231daa82c34ee2ec8292111575e95af675
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8228188"
---
# <a name="create-and-modify-events"></a>Sortu eta aldatu gertaerak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Gertaera erabiltzaileen portaera adierazten duten datuak dira, adibidez, webgune bateko jarduerak.

- *Oinarria* gertaera erregistratzen du erabiltzaile batek ikusten duenean orria (ikusi gertaera) edo elkarreragiten duen edukiarekin (ekintzaren gertaera).
- *Findu* gertaera oinarrizko gertaeraren ikuspegi birtuala da. Gertaera finduak definitzen dituzu propietateak kenduz eta gehituz edo gertaerak propietate balioetan oinarrituta iragaziz.

## <a name="prerequisites"></a>Aurrebaldintzak

Gertaerak lortzeko, zure webguneko datuak behar dute lehenik konektatuta egotea elkarreragin-xehetasunetara kode zatiarekin. Informazio gehiagorako, ikus [Instalatu web SDK webgune batean](instrument-website.md).

 :::image type="content" source="media/new-events-connect-data.png" alt-text="Konektatu datuak lehenik.":::

## <a name="create-refined-events"></a>Sortu gertaera mugatuak

Erabili gertaera finduak oinarrizko gertaeraren esparrua murrizteko [esportatu](export-events.md) edo esposiziorako beharrezkoak ez diren propietateak kentzeko.

> [!NOTE]
> Web SDK zure webgunera gehitu ondoren, oinarrizko gertaerak ikusi eta gertaera finduak sor ditzakezu. 

Oinarrizko gertaerak ikusteko:

1. Ezkerreko nabigazio-panelean, joan **datuak** atalera.

1. Aukeratu **Ekitaldiak** laneko eremuko gertaera guztien zerrenda ikusteko.

    :::image type="content" source="media/data-events.png" alt-text="Ikusi gertaerak.":::

Oinarrizko gertaera batetik gertaera findu bat sortzeko: 

1. Joan **Datuak** > **Ekitaldiak** eta hautatu **+ Ekitaldi berriak** pantailaren goialdean.

1. Urtean **Gertakari berriak** elkarrizketa-koadroa, hautatu **Sortu gertaera finduak** eta, ondoren, hautatu **Hurrengoa**.
   
     :::image type="content" source="media/new-events-wizard.png" alt-text="Gertaera berrien morroia.":::
     
1. Urtean **Gertakari berriak** elkarrizketa-koadroa, sartu informazio hau:

   - Hautatu gertaera bat **Oinarrizko gertaerak** goitibehera.
   - Idatzi izena **findutako gertaerak bistaratzeko izena** kutxa.
   - Aukeran, eguneratu iradokitakoa **Benetako izena** espazioak erabili gabe.

1. Aukeratu **Sortu** zure ezarpenak aplikatzeko.

Orain gertaera findua zure **Ekitaldiak** zerrenda.

### <a name="edit-event-name"></a>Editatu gertaeraren izena

Oinarrizko edo gertaera findu baten izena eta propietateak alda ditzakezu.

1. Joan **Datuak** > **Gertaerak**. 

1. Aukeratu **Gehiago [...]** gertaera baterako eta hautatu **Editatu izena**.
    
     :::image type="content" source="media/create-refined-events-options.png" alt-text="Gertaera finduak sortzeko aukerak.":::

3. Eguneratu gertaeraren izena eta hautatu **Aldatu izena**.

### <a name="view-the-details-of-a-refined-event"></a>Ikusi gertaera findu baten xehetasunak:

1. Urtean **Ekitaldia** zerrendan, hautatu zure oinarria edo gertaera findua. 

1. Aukeratu **Gehitu eta kendu propietateak** pantailaren goialdean irekitzeko **Editatu propietateak** panela. 

     :::image type="content" source="media/add-remove-properties.png" alt-text="Gehitu eta kendu propietateak.":::

1. Erabili kontrol laukiak erakutsi nahi dituzun propietateak eta ezkutatu nahi dituzunak hautatzeko. 

   :::image type="content" source="media/edit-properties-refined-events.png" alt-text="Editatu finkatutako gertaeren propietateak.":::

1. Aukeratu **Berretsi** zure hautapena aplikatzeko eta, ondoren, hautatu **Gorde**.


### <a name="edit-selected-properties-for-a-refined-event"></a>Editatu hautatutako propietateak gertaera findu baterako

1. Joan **Datuak** > **Ekitaldiak** eta hautatu findutako gertaerak ikuspegi zehatza irekitzeko.
1. Aukeratu **Gehitu eta kendu propietateak**. 
1. Editatu kontrol-laukien hautapena.
1. Aukeratu **Berretsi** eta gero **Gorde** aldaketak aplikatzeko.

Gertaerak esportatzeari buruzko informazioa lortzeko, ikusi [Esportatu gertaerak](export-events.md).
[!INCLUDE[footer-include](../includes/footer-banner.md)]
