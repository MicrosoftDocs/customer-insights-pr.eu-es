---
title: Zerbitzuen mugak Customer Insights-en
description: Ulertu Customer Insights SaaS zerbitzuko mugak eta murrizketak.
ms.date: 08/30/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 7f38b7d9985368fc38107f1f360f0603a7fcc8e6
ms.sourcegitcommit: 3c7cdfc8bd83ca236e4777240e08a541dc955d34
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/07/2022
ms.locfileid: "9411725"
---
# <a name="service-limits-in-customer-insights"></a>Zerbitzuen mugak Customer Insights-en

 Customer Insights-ek zerbitzuaren fidagarritasuna eta egonkortasuna bermatzeko diseinatutako mugak ditu. Aldaketak egiteko eskaerak [Ideien foroa](https://go.microsoft.com/fwlink/?linkid=2074172).

## <a name="customer-insights"></a>Customer Insights

| Area  | Mugak  | Oharrak |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Segmentuak, neurriak eta iragarpenak | 300  | Guztizko kopurua [segmentuak](segments.md),[neurriak](measures.md), eta [iragarpenak](predictions-overview.md) bateratuta, ezin dira 300 baino gehiago.  |
| Erlazioak | 20 sakontasun maila entitate bideetako erlazioetan. | Sortzerakoan [segmentuak](segments.md) edo [neurriak](measures.md) eraikitzailearen interfazea erabiliz, entitate bide-izenek 20 harreman salto izan ditzakete hasierako entitatearen eta xede entitatearen artean.  |

## <a name="fair-scheduling-of-jobs"></a>Lanpostuen programazio zuzena

Customer Insights partekatutako Azure baliabideak erabiltzen dituen SaaS zerbitzu bat da. Bezeroek intentsitate aldakorreko eta ordutegi desberdinetako lan-kargak izan ohi dituzte. Azpiko baliabideetarako bidezko sarbidea bermatzeko, sistemaren prozesuak ordena egokian exekutatzen direla ziurtatzen dugu. Sistema-prozesuen adibideak datuen bateratzearekin, segmentuen eguneraketekin edo neurrien kalkuluarekin lotutako lanak dira. Azoka-programazioak baliabideen ilaratik babesten zaitu, eskatutako lanpostuen gorakada badago. Aldi berean, Customer Insights-ek ez du bermatzen ilaran jartzen dituzun lan guztiak paraleloan prozesatzen direnik.

[!INCLUDE [footer-include](includes/footer-banner.md)]
