---
title: Erabili dimentsio demografikoak portaeraren datuak banatzeko (tamaina zaindua)
description: Erabili profil bateratuak zaindu beharreko dimentsioak bezeroaren profilaren propietateak ikusleen estatistikak gaitzeko.
ms.date: 07/27/2021
ms.topic: conceptual
author: mkisel
ms.author: mkisel
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 95395e09bc0ba5ba93138957c62105f31c709e91
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8232952"
---
# <a name="use-demographic-dimensions-for-splitting-behavioral-data"></a>Erabili dimentsio demografikoak portaeraren datuak banatzeko

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Profileko dimentsio demografiko bateratuak erabiliz, konpromiso estatistikek erabiltzaileek ikusleen estatistiken profileko propietateetara sar ditzakete. Orduan erabili ditzakezu propietate horiek portaera datuen analisi interaktiboetan, barne hartuz datuak kapturatuta elkarreragin xehetasunak zure webgune edo mugikorreko aplikazioan.

>[!NOTE]
> Parte-hartzearen xehetasunek gertaeren propietateen erabiltzeko prest dauden dimentsioak ditu. Informazio gehiago: [Ikusi eta sortu dimentsioak](dimensions.md)

## <a name="prerequisite"></a>Aurrebaldintza

- Segmentuak eta bezeroen profilak sortzen diren bezero profilaren loturiko audientzia estatistikak biltzen dituen konpromisoari buruzko ingurunea. Informazio gehiago: [Sortu esteka bat hartzaile xehetasun eta elkarreragin xehetasunen artean](integrate-audience-insights-engagement-insights.md)

> [!NOTE]
> Ikusleen estatistiken eta engaiamenduen inguruko inguruneen arteko esteka sortu ondoren, baliteke bezeroaren profilaren propietateei buruzko datuak soilik izatea, konpromisoen inguruko informazioaren dimentsio gisa erabilgarriak izan daitezkeenak. Informazio gehiagorako, joan [Gaitu hartzailearen xehetasunak bateratutako profilen atributuak eta segmentuak](integrate-audience-insights-engagement-insights.md#enable-audience-insights-unified-profiles-attributes-and-segments).

## <a name="create-a-new-custom-report"></a>Sortu txosten (pertsonazalizatu) berria

1. Ezkerreko panelean, hautatu **Pertsonalizatua** > **Txosten berria**, eta hautatu nahi duzun metrika. (Adibide honetarako, aukeratu dugu **Orrialde ikustaldiak orduka** txostena.)

    :::image type="content" source="media/curated-dimensions1.png" alt-text="Hautatu estatistika.":::

2. Visualization editorean, hautatu **Neurriak** eta, ondoren, hautatu **Demografikoa** urtean **Dimentsio mota** goitibeherako menua.

    :::image type="content" source="media/curated-dimensions2.png" alt-text="Aukeratu demografikoa.":::

3. Aukeratu **Seinalea.Bezeroa.*xxx*** dimentsioa. (Adibide honek Signal.Customer.Country erakusten du.)

    :::image type="content" source="media/curated-dimensions3.png" alt-text="Hautatu dimentsio bat.":::
  
## <a name="limitations"></a>Murriztapenak

Une honetan erabili dezakezu dimentsio demografikoak portaeraren datuak banatzeko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
