---
title: Esportatu findutako gertaerak
description: Nola esportatu gertaera finduak eta oinarrizko gertaerak.
ms.reviewer: mhart
ms.author: jusali
author: jusali
ms.date: 10/01/2021
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: d062e2982c1041454b083630404f2b68f0da9669
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8232873"
---
# <a name="export-events"></a>Esportatu gertaerak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Gertaera batek erabiltzaileen portaera adierazten du. Jarduera batek erabiltzaile batek orri bat ikustean (Ikusi gertaera) edo edukiarekin elkarreragiten du (Ekintza gertaera). Txosten batean bistaratu nahi dituzun datuen zein propietate erabaki dezakezunean, datuen ikuspegi birtual honi a deitzen zaio *gertaera findua*. Informazio gehiagorako, ikus [Sortu eta aldatu gertaerak](refined-events.md).

- Gertaerak eta gertaera finduak kanpoko biltegira esporta ditzakezu. 
- Esportazioak aurrerapen datuen korrontea dira. Ezin duzu korrontea berriro bete. 
- Esportazioek eskema finkoak dituzte. Gertaera bati propietate pertsonalizatuak gehitzen badizkiozu, ez dira sartuko. Esportazio berri bat sortu beharko duzu.

## <a name="prerequisites"></a>Aurrebaldintzak

Esportazioa konfiguratu aurretik, sarbidea eta harpidetza aktiboa izan behar duzu Azure atarian. Biltegiratze kontuaren informazioa esportazio prozesuan zehar beharko duzu. 

### <a name="create-an-azure-data-lake-storage-gen-2-accounts"></a>Sortu Azure Data Lake Storage 2. belaunaldiko kontuak

1. Hasi saioa Azure atarian eta [sortu biltegiratze kontu berria](/azure/storage/common/storage-account-create). 

1. Ziurtatu gaitzen duzula **Izen espazio hierarkikoa** gainean **Aurreratua** fitxa. 

   :::image type="content" source="media/enable-hierarchical-namespace.png" alt-text="Gaitu hierarkikoa den izen-eremua fitxa aurreratuan.":::

1. Behin zabaldu ondoren, joan sortu berri den biltegiratze kontura. Nabigazio panelean, hautatu **Ezarpenak** > **Sarbide gakoak**. 

1. Kopiatu **Kontuaren izena** eta **Gakoa** esportazio berri bat sortzerakoan erabiltzeko.
   :::image type="content" source="media/storage-account-access-keys.png" alt-text="Atzitu gakoak biltegiratze-kontuan.":::

## <a name="export-events"></a>Esportatu gertaerak

Bi modu daude ekartzeko **Esportatu gertaerak** elkarrizketa: 
- Joan **Datuak** > **Esportazioak** eta hautatu **Esportazio berria**.
- Joan **Datuak** > **Ekitaldiak**, hautatu **Gehiago [...]** esportatu eta hautatu nahi duzun gertaeraren ondoan **Esportatu** goitibeherako menuan. 

:::image type="content" source="media/new-export.png" alt-text="Sortu esportatze berria.":::

Esportazio bat sortzeko urratsen bidez gidatzen zaitu:

1. Eman **Esportatu izena** eta, ondoren, hautatu **Hurrengoa**.

1. Urtean **Ekitaldiak hautatzea** goitibeherako zerrendan, aukeratu esportazioan sartzeko oinarrizko gertaerak eta gertaera finduak. 

1. Urtean **Fitxategien egitura** atalean, hautatu kadentzia (orduka edo egunero) helmugako biltegian fitxategi berriak sortzeko eta, ondoren, hautatu **Hurrengoa**. Ekitaldiak etengabe esportatzen dira iritsi ahala.

1. Urtean **Aukeratu formatua** elkarrizketa-koadroan, hautatu esportatzeko formatua. Aukeratu artean **Datuen eredu arrunta**, **CSV**, eta **JSON** formatuak. Esportazioa beste Dynamics 365 aplikazio batzuekin erabiltzeko, gomendatzen dizugu **Datuen eredu arrunta** formatua.

1. Urtean **Aukeratu helmuga** elkarrizketa - koadroa, zehaztu Azure Data Lake Storage Gen 2 kokapena.
    1. **ADLS Gen 2 kontuaren izena** esportazioa gorde nahi duzun biltegiratze kontuaren izena da. 
    1. **Karpeten bidea** esportazioa non gorde behar den fitxategi sisteman eta biltegiratze kontuaren direktorio egituran non definitu behar den definitzen du.
    1. **Gako partekatua** eskuragarri dago Azure atarian biltegiratze konturako.

1. Berrikusi eta berretsi hautapenak amaitzeko.

## <a name="view-and-manage-exports"></a>Ikusi eta kudeatu esportatzeak

Esportazioa konfiguratu ondoren, joan hona **Datuak** > **Esportazioak** ikusteko. Aukeratu **Gehiago [...]** dauden esportazioek editatzeko edo ezabatzeko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
