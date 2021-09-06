---
title: Onartutako iragarpen agertokiei buruzko ikuspegi orokorra
description: Dynamics 365 Customer Insights aplikazioak lantzen dituen iragarpen agertokiak eta aukerak.
ms.date: 05/18/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: get-started
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: 57c61895d636273fc90a0ac5a942fd0c9abf583c687ae20621949554e581cdf8
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7035994"
---
# <a name="predictions-overview"></a>Iragarpenen ikuspegi orokorra

Dynamics 365 Customer Insights adimen artifiziala eta Ikaskuntza automatikoa baliatzeko aukera ugari ditu, datuak iragartzeko. 

## <a name="out-of-box-models"></a>Erabiltzeko prest dauden ereduak

Datuak aurreikusten hasteko modurik errazena aurrez zehaztutako ereduak dira, maiz erabiltzeko prest dauden eredu gisa aipatzen direnak. Datu eta egitura jakin batzuk besterik ez dituzte eskatzen estatistikak azkar sortzeko. Gaur egun, eredu hauek daude eskuragarri: 
- [Bezeroaren bizi-iraupenaren balioa](predict-customer-lifetime-value.md): Bezero batek negozioarekin izandako elkarrekintza osoan zehar izan dezakeen diru sarrera iragartzen du. 
- [Produktuen gomendioa](predict-product-recommendation.md): Produktu iragarleen gomendio multzoak iradokitzen ditu erosketa portaeran eta antzeko erosketa ereduak dituzten bezeroetan oinarrituta.
- [Harpidetzen galera-tasa](predict-subscription-churn.md): bezeroak enpresaren harpidetza-produktu eta -zerbitzuak erabiltzeari uzteko arriskua duen iragar dezake.
- [Transakzioen galera-tasa](predict-transactional-churn.md): Aurreikusi bezero batek zure produktuak edo zerbitzuak denbora tarte jakin batean erosiko ez dituen ala ez.

## <a name="azure-machine-learning-integration"></a>Azure ikaskuntza automatikoaren integrazioa

Erakunde batek dagoeneko Azure Ikaskuntza automatikoaren esperientzietan oinarritutako Ikaskuntza automatikoko eszenatokiak erabiltzen baditu, Customer Insights-eko eredu pertsonalizatuen ezaugarriak puntuak konektatzen laguntzen du. Sortu xehetasunak sortu nahi dituzun datuak aukeratzen lagunduko dizuten lan-fluxuak eta emaitzak zure bezeroen profil bateratuei esleitu. Informazio gehiago lortzeko, ikus [Ikaskuntza automatiko eredu pertsonalizatuak](custom-models.md).

## <a name="ai-builder-prediction"></a>AI Builder-en iragarpena

Batzuetan, datu multzoak osatu gabe daude eta balio batzuk falta dira. Customer Insights-ek Bezeroaren entitate eta segmentuetarako falta diren balioak aurreikusten lagun dezake. Informazio gehiagorako, ikus [Osatu zure datu partzialak iragarpenekin](predictions.md).
