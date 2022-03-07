---
title: Funtzioak eta baimenak
description: Laneko espazioko kideentzako eskuragarri dauden rolen eta baimenen ikuspegi orokorra.
ms.reviewer: mhart
ms.author: jusali
author: jusali
ms.date: 10/01/2021
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: ccc6a1b87b4cc28701e276b6e35432356e7647c4
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8227524"
---
# <a name="roles-and-permissions"></a>Funtzioak eta baimenak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Lan-eremua gertaerak eta txostenak gordetzeko eta kudeatzeko lekua da. Informazio gehiagorako, ikus [Sortu lan gunea eta gehitu kideak](create-workspace.md). 

Laneko espazio batek rol eta baimen hauek sar ditzake:

- *Kidea* rolak laneko espazio batera sar daitezkeen erabiltzaileak dira. Kideak zure lan-eremura esleitu eta haien rolak eta baimenak zehaztu ditzakezu. 
- *Administratzaile* rolek laneko espazioak eta inguruneak kudeatzen dituzte eta beste erabiltzaileentzako konpromisoen inguruko datuak konfiguratzen dituzte. 
- *Laguntzailea* rolak konpromiso-estatistikak konfiguratu behar ez dituzten baina beren txostenak, inbutuak edo segmentuak sortu nahi dituzten analistei zuzenduta daude.

## <a name="permissions"></a>Baimenak
  
Hurrengo taulan rol bakoitzerako baimenak identifikatzen dira. 

| Baimena | Ingurunearen administratzailea | Laneko arearen administratzailea | Ingurunearen kolaboratzailea | Laneko arearen kolaboratzailea | 
|--|--|--|--|--|
| Inguruneak sortu (sortzailea automatikoki ingurune administratzaile bihurtzen da) | X* | X* | X* | X* |  
| Konfiguratu ingurunea (inguruneko kideak, ezabatu ingurunea) | X |  |  |  |  
| Sortu lan-eremuak | X |  |  |  |  
| Konfiguratu laneko eremuak (laneko eremuko kideak, ezabatu laneko eremua) | X | X |  |  |  
| Konfiguratu gertaerak eta gertaera finduak | X | X | |  |  
| Ikusi laneko eremuko gertaerak eta gertaera finduak | X | X | |  |  
| Ikusi laneko eremuko baliabideak (txostenak, segmentuak eta metrika)| X | X | X | X |  
| Sortu txosten pertsonalizatuak eta inbutuak | X | X | X | X |  
| Sortu oinarrizko metrikak eta dimentsioak| X | X |  |  |  
| Sortu segmentuak| X | X | X | X |  

*Aurreikuspenetan soilik probatu ditzakezu probako inguruneak. 

## <a name="add-members"></a>Gehitu kideak

Kideak laneko guneetatik eta inguruneetatik gehitu eta kendu ditzakezu. Informazio gehiagorako, ikus [Inguruneak eta lan-eremuak](manage-environments-workspaces.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
