---
title: Kudeatu adostasun-arau lehenetsiak segmentuetan
description: Adostasuna kudeatzeko gaitasunarekin, baimen-arau lehenetsiak desgaitu edo alda ditzakezu gainidatziak gaituta badaude.
ms.date: 12/01/2021
ms.topic: how-to
author: anubhav-t
ms.author: antando
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 764eeca9d99c95a34d9bd4c11d79f8b8e90701e2
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755201"
---
# <a name="disable-or-change-default-consent-rules"></a>Desgaitu edo aldatu baimen-arau lehenetsiak

Zure erakundeek erabiltzen badute [baimena kudeatzeko gaitasuna](consent-management/overview.md) rekin Dynamics 365 Customer Insights,[administratzaileek baimen-arauak bete ditzakete](activate-consent.md) segmentuetarako. 

Segmentu-eremuan betearazitako baimen-arauekin, segmentu bakoitzak baimenaren egiaztapenaren eta arauen egoeraren berri ematen du. Gainidatzeak onartzen badira, adostasun-arau lehenetsiak desaktibatu egingo dira segmentu zehatzetarako. Segmentu baten sortzaile bakoitzak adostasun-arau gehiago gehi diezazkioke arau lehenetsien gainean segmentu bati. 

## <a name="for-administrators"></a>Administratzaileentzat

:::image type="content" source="consent-management/media/consent-rules-segment.png" alt-text="Segmentu-sortzailea adostasun-arauen aukerekin.":::

**Adostasun-arau lehenetsiak desaktibatzeko:**

1. urtean **Adostasun arauak** jakinarazpena, hautatu **Ikusi xehetasunak**. 

1. Ezarri **Adostasun arau lehenetsiak** txandakatu **Desaktibatuta**.

**Adostasun-arau gehiago gehitzeko:**

1. urtean **Adostasun arauak** jakinarazpena, hautatu **Ikusi xehetasunak**. 

1. Hautatu **Gehitu baimen-arauak** eta aukeratu adostasun-arau bat **Hautatu adostasun datu mota** goitibeherako.

1. Hautatu **Gorde** arau berria segmentuari aplikatzeko.

## <a name="for-contributors"></a>Kolaboratzaileentzat

Segmentu bat behartutako baimen-araurik gabe sortzeko, zure administratzailearekin lan egin behar duzu segmentuan desgaitzeko. Hala ere, zure baimen-arau propioak gehi ditzakezu zure jabe eta kudeatzen dituzun segmentuetan.

Hiru urratseko prozesua da: 
1. [Sortu segmentua](segments.md) Customer Insights-en eta gorde ezazu. 

1. Partekatu segmentuaren izena zure administratzailearekin eta eskatu [gaitu zure segmenturako baliogabetzeak](activate-consent.md). 

1. Ireki zure segmentuak berriro. urtean **Adostasun arauak** jakinarazpena, hautatu **Ikusi xehetasunak** eta gehitu aplikatu nahi dituzun baimen-arauak. Orduan, **Gorde** eta **Korrika egin** zure segmentua.



[!INCLUDE [footer-include](includes/footer-banner.md)] 
