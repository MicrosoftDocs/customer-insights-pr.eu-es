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
ms.openlocfilehash: 421e1aa41a54a4b8c34ac27fc7c02e510d2bb588
ms.sourcegitcommit: 624b27bb65a0de1970dc1ac436643b493f0a31cf
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387141"
---
# <a name="service-limits-in-customer-insights"></a>Zerbitzuen mugak Customer Insights-en

 Customer Insights-ek zerbitzuaren fidagarritasuna eta egonkortasuna bermatzeko diseinatutako mugak ditu. Aldaketak egiteko eskaerak [Ideien foroa](https://go.microsoft.com/fwlink/?linkid=2074172).

## <a name="customer-insights"></a>Customer Insights

| Area  | Mugak  | Oharrak |
|-------------|---------------------------------------------------------------------|---------------------------------------------------------------------|
| Segmentuak, neurriak eta iragarpenak | 300  | Guztizko kopurua [segmentuak](segments.md) ,[neurriak](measures.md) , eta [iragarpenak](predictions.md) bateratuta, ezin dira 300 baino gehiago.  |
| Erlazioak | 20 sakontasun maila entitate bideetako erlazioetan. | Sortzerakoan [segmentuak](segments.md) edo [neurriak](measures.md) eraikitzailearen interfazea erabiliz, entitate bide-izenek 20 harreman salto izan ditzakete hasierako entitatearen eta xede entitatearen artean.  |

## <a name="fair-scheduling-of-jobs"></a>Lanpostuen programazio zuzena

Customer Insights partekatutako Azure baliabideak erabiltzen dituen SaaS zerbitzu bat da. Bezeroek intentsitate aldakorreko eta ordutegi ezberdinetako lan-kargak izan ohi dituzte. Azpiko baliabideetarako bidezko sarbidea bermatzeko, sistema-prozesuak ordena egokian exekutatzen direla ziurtatzen dugu. Sistema-prozesuen adibideak datuen bateratzearekin, segmentuen eguneraketekin edo neurrien kalkuluarekin lotutako lanak dira. Azoka-programazioak baliabideen ilaratik babesten zaitu, eskatutako lanpostuen gorakada badago. Aldi berean, Customer Insights-ek ez du bermatzen ilaran jartzen dituzun lan guztiak paraleloan prozesatzen direnik.

[!INCLUDE [footer-include](includes/footer-banner.md)]
