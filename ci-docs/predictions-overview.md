---
title: Onartutako iragarpen agertokiei buruzko ikuspegi orokorra
description: Dynamics 365 Customer Insights aplikazioak lantzen dituen iragarpen agertokiak eta aukerak.
ms.date: 03/24/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: overview
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: 11b0efeecf8bea893272e67d29b1c6622771110c
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642184"
---
# <a name="predictions-overview"></a>Iragarpenen ikuspegi orokorra

Dynamics 365 Customer Insights adimen artifiziala eta Ikaskuntza automatikoa baliatzeko aukera ugari ditu, datuak iragartzeko. 

## <a name="out-of-box-models"></a>Erabiltzeko prest dauden ereduak

Datuak aurreikusten hasteko modurik errazena aurrez zehaztutako ereduak dira, maiz erabiltzeko prest dauden eredu gisa aipatzen direnak. Datu eta egitura jakin batzuk besterik ez dituzte eskatzen estatistikak azkar sortzeko. Gaur egun, eredu hauek daude eskuragarri: 

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- [Bezeroaren bizi-iraupenaren balioa](predict-customer-lifetime-value.md): Bezero batek negozioarekin izandako elkarrekintza osoan zehar izan dezakeen diru sarrera iragartzen du.
- [Produktuen gomendioa](predict-product-recommendation.md): Produktu iragarleen gomendio multzoak iradokitzen ditu erosketa portaeran eta antzeko erosketa ereduak dituzten bezeroetan oinarrituta.
- [Harpidetzen galera-tasa](predict-subscription-churn.md): bezeroak enpresaren harpidetza-produktu eta -zerbitzuak erabiltzeari uzteko arriskua duen iragar dezake.
- [Transakzioen galera-tasa](predict-transactional-churn.md): Aurreikusi bezero batek zure produktuak edo zerbitzuak denbora tarte jakin batean erosiko ez dituen ala ez.
- [Sentimenduen analisia](sentiment-analysis.md) : Bezeroen iritzien sentimendua aztertzea eta maiz aipatzen diren negozio-alderdiak identifikatzea.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- [Transakzioen galera-tasa](predict-transactional-churn.md): Aurreikusi bezero batek zure produktuak edo zerbitzuak denbora tarte jakin batean erosiko ez dituen ala ez.

---

> [!TIP]
> Kutxaz kanpoko ereduak aldizka freskatzea gomendatzen dugu datu eguneratuekin, zure negozioaren erabilera kasua zehatz-mehatz informatzen dutela ziurtatzeko. Datuak ad hoc freskatzen dira sistemak datu-iturri berriak edo eguneratuak sartzen dituenean. Hala ere, ereduek kasu honetan soilik berregokituko dute eta lehendik dauden prestakuntza-datuak erabiltzen jarraituko dute.
> 
> Bat konfigura dezakezu **Eguneratu ordutegia** konfigurazio-esperientzian eredua birziklatzeko egutegia ezarriz. Eredua berriro trebatu eta puntuatu egingo da ordutegi honetan, eta edozein unetan alda dezakezu.


## <a name="azure-machine-learning-integration"></a>Azure ikaskuntza automatikoaren integrazioa

Erakunde batek dagoeneko Azure Ikaskuntza automatikoaren esperientzietan oinarritutako Ikaskuntza automatikoko eszenatokiak erabiltzen baditu, Customer Insights-eko eredu pertsonalizatuen ezaugarriak puntuak konektatzen laguntzen du. Sortu xehetasunak sortu nahi dituzun datuak aukeratzen lagunduko dizuten lan-fluxuak eta emaitzak zure bezeroen profil bateratuei esleitu. Informazio gehiago lortzeko, ikus [Ikaskuntza automatiko eredu pertsonalizatuak](custom-models.md).

## <a name="ai-builder-prediction"></a>AI Builder iragarpen

Batzuetan, datu multzoak osatu gabe daude eta balio batzuk falta dira. Customer Insights-ek Bezeroaren entitate eta segmentuetarako falta diren balioak aurreikusten lagun dezake. Informazio gehiagorako, ikus [Osatu zure datu partzialak iragarpenekin](predictions.md).