---
title: Iragarpenen ikuspegi orokorra
description: Dynamics 365 Customer Insights aplikazioak lantzen dituen iragarpen agertokiak eta aukerak.
ms.date: 09/29/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: overview
author: zacookmsft
ms.author: zacook
manager: shellyha
ms.openlocfilehash: f8c61d7530126890d26ce482a27a0f97a39e836c
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610175"
---
# <a name="predictions-overview"></a>Iragarpenen ikuspegi orokorra

Dynamics 365 Customer Insights adimen artifiziala eta Ikaskuntza automatikoa baliatzeko aukera ugari ditu, datuak iragartzeko.

## <a name="out-of-box-models"></a>Erabiltzeko prest dauden ereduak

Datuak aurreikusten hasteko modurik errazena aurrez zehaztutako ereduak dira, maiz erabiltzeko prest dauden eredu gisa aipatzen direnak. Datu eta egitura jakin batzuk besterik ez dituzte eskatzen estatistikak azkar sortzeko. Eredu hauek eskuragarri daude:

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- [Bezeroaren bizi-iraupenaren balioa](predict-customer-lifetime-value.md): Bezero batek negozioarekin izandako elkarrekintza osoan zehar izan dezakeen diru sarrera iragartzen du.
- [Produktuen gomendioa](predict-product-recommendation.md): Produktu iragarleen gomendio multzoak iradokitzen ditu erosketa portaeran eta antzeko erosketa ereduak dituzten bezeroetan oinarrituta.
- [Harpidetzen galera-tasa](predict-subscription-churn.md): bezeroak enpresaren harpidetza-produktu eta -zerbitzuak erabiltzeari uzteko arriskua duen iragar dezake.
- [Transakzio txandaka](predict-transactional-churn.md) : bezero indibidual batek denbora-tarte jakin batean zure produktuak edo zerbitzuak gehiago erosiko ez dituen ala ez aurreikusten du.
- [Sentimenduen analisia](sentiment-analysis.md) : Bezeroen iritzien sentimendua aztertzen du eta maiz aipatzen diren negozio-alderdiak identifikatzen ditu.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- [Transakzio txandaka](predict-transactional-churn.md) : Bezero-kontu batek zure produktuak edo zerbitzuak denbora-tarte jakin batean gehiago erosiko ez dituen aurreikusten du.

---

> [!TIP]
> Kutxaz kanpoko ereduak aldizka freskatzea gomendatzen dugu datu eguneratuekin, zure negozioaren erabilera kasua zehatz-mehatz informatzen dutela ziurtatzeko. Datuak ad hoc freskatzen dira sistemak datu-iturri berriak edo eguneratuak sartzen dituenean. Hala ere, ereduek kasu honetan soilik berregokituko dute eta lehendik dauden prestakuntza-datuak erabiltzen jarraituko dute.
>
> Konfiguratu bat **Eguneratu ordutegia** konfigurazioan zehar eredua birziklatzeko egutegia ezarriz. Eredua berriro trebatu eta puntuatu egingo da ordutegi honetan, eta edozein unetan alda dezakezu.

## <a name="azure-machine-learning-integration"></a>Azure ikaskuntza automatikoaren integrazioa

Erakunde batek dagoeneko Azure Ikaskuntza automatikoaren esperientzietan oinarritutako Ikaskuntza automatikoko eszenatokiak erabiltzen baditu, Customer Insights-eko eredu pertsonalizatuen ezaugarriak puntuak konektatzen laguntzen du. Sortu xehetasunak sortu nahi dituzun datuak aukeratzen lagunduko dizuten lan-fluxuak eta emaitzak zure bezeroen profil bateratuei esleitu. Informazio gehiago lortzeko, ikus [Ikaskuntza automatiko eredu pertsonalizatuak](custom-models.md).

## <a name="manage-existing-predictions"></a>Kudeatu lehendik dauden iragarpenak

Joan zaitez **Adimena** > **Iragarpenak** orrialdea. Gainean **Nire iragarpenak** fitxan, ikusi sortu dituzun iragarpenak, haien iragarpen mota, irteerako entitatearen izena, egoera, iragarpen editatu zen azken aldia eta datuak freskatu ziren azken aldia. Iragarpenen zerrenda edozein zutaberen arabera ordena dezakezu.

Hautatu iragarpen bat erabilgarri dauden ekintzak ikusteko.

:::image type="content" source="media/predictions.png" alt-text="Nire iragarpen orria.":::

- **Editatu** iragarpen bere propietateak aldatzeko.
- [**Freskatu**](#refresh-a-prediction) iragarpen azken datuak sartzeko.
- **Ikusi** iragarpen xehetasunak.
- [**Sarrerako datuen erabilgarritasun txostena**](#view-the-input-data-usability-report) akatsak, abisuak eta gomendioak ikusteko.
- **Ezabatu** iragarpen.

### <a name="refresh-a-prediction"></a>Iragarpen bat eguneratu

Iragarpenak programazio automatiko batean freskatu daitezke edo eskuz, eskaeraren arabera. Iragarpen guztiak eskuz freskatzeko, hautatu **Freskatu guztiak**. Iragarpen bat eskuz freskatzeko, hautatu eta hautatu **Freskatu**. To [programatu freskatze automatikoa](schedule-refresh.md), joan **Admin** > **Sistema** > **Ordutegia**.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

### <a name="view-the-input-data-usability-report"></a>Ikusi sarrerako datuen erabilgarritasun-txostena

Sarrerako datuak erabiltzeko txostena Sarrerako datuen erabilgarritasun txostenak erabiltzeko prest dauden iragarpenek sor ditzaketen akats eta abisuen ikuspegi bateratua eskaintzen du. Ereduaren errendimendua hobetzeko gomendioak ere ematen ditu.

Txostena eredu batek bere prestakuntza prozesua amaitu ondoren eskuragarri dago. Eredu bakoitzerako bereizita sortzen da, prestakuntza arrakastaz amaitu ala ez kontuan hartu gabe.

Gainean **Nire iragarpenak** fitxa, hautatu iragarpen eta aukeratu **Sarrerako datuen erabilgarritasun txostena**. Edo iragarpen xehetasunen ikuspegitik, hautatu **Sarrerako datuen erabilgarritasun txostena**.

:::image type="content" source="media/input-data-usability-report.png" alt-text="Sarrerako datuen erabilgarritasun txostenaren adibidea, akatsak, abisuak eta gomendioak dituen taula erakusten duena.":::

Txostenak barne hartzen ditu:

- **Izena:** Errorearen, abisuaren edo gomendioaren izen deskribatzailea.
- **Urratsera:** Ereduaren fasea, trena edo puntuazioa, informazioa aipatzen du.
- **Estatu:** Informazioaren larritasuna (errorea, abisua, gomendioa).
- **Zutabearen izena:** Modeloaren errendimendua hobetzeko aldatu behar den entitate bateko zutabea.
- **Entitatearen izena:** Ereduaren errendimendua hobetzeko aldatu behar den entitatearen izena.
- **Xehetasunak:** Erroreari, abisuari edo gomendioari buruzko xehetasunak.

[!INCLUDE [footer-include](includes/footer-banner.md)]
