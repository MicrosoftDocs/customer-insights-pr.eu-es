---
title: Funtzioak eta baimenak
description: Laneko espazioko kideentzako eskuragarri dauden rolen eta baimenen ikuspegi orokorra.
ms.reviewer: mhart
ms.author: jusali
author: jusali
ms.date: 07/06/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: 6d7f4db4a130fc15a69b380c892538db5492d96d8e13f3c070c6a6b9bd098371
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036678"
---
# <a name="roles-and-permissions"></a>Funtzioak eta baimenak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Lan gunea gertaerak eta txostenak gordetzeko eta nola kudeatzen duzuna da. Kidea laneko espazio batera sar daitekeen erabiltzailea da. Kideak zure lan-eremura esleitu eta haien rolak eta baimenak zehaztu ditzakezu. Administratzaile rolek laneko espazioak eta inguruneak kudeatzen dituzte eta beste erabiltzaileentzako konpromisoen inguruko datuak konfiguratzen dituzte. Laguntzaile rolak konpromiso estatistikak konfiguratu behar ez dituzten baina beren txostenak, inbutuak edo segmentuak sortu nahi dituzten analistei zuzenduta daude.

## <a name="permissions"></a>Baimenak
  
Ondorengo taulan rol bakoitzerako baimenak identifikatzen dira. 

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
