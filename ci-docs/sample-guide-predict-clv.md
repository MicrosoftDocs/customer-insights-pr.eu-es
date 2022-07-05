---
title: Bezeroaren bizi-iraupenaren balioaren iragarpenaren lagin gida
description: Erabili lagin gida hau bezeroaren bizi-iraupenaren balio osorako iragarpen modeloa probatzeko.
ms.date: 03/31/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: tutorial
author: yashlundia
ms.author: yalundia
manager: shellyha
ms.openlocfilehash: 2013533ed225a396d21e51e63297d7608ce58ac6
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9051622"
---
# <a name="customer-lifetime-value-clv-prediction-sample-guide"></a>Bezeroaren bizi-iraupenaren balioaren iragarpenaren lagin gida

Gida honek Bezeroaren bizi-iraupenaren balio osoko (CLV) iragarpen adibidearen amaierako adibidea azalduko dizu Customer Insights-en, lagin-datuak erabiliz.

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafe eta kafe makinak ekoizten dituen enpresa da. Contoso Kafearen webgunearen bidez saltzen dituzte produktuak. Konpainiak bezeroek hurrengo 12 hilabeteetan sor dezaketen balioa (diru-sarrerak) ulertu nahi du. Datozen 12 hilabeteetan bezeroek espero duten balioa ezagutzeak balio handiko bezeroenganako marketin ahalegina bideratzen lagunduko die.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Berrikusi artikuluak [datuak sartzeari buruz](data-sources.md) eta [datu-iturriak erabiliz inportatzea Power Query konektoreak](connect-power-query.md). Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.

### <a name="ingest-customer-data-from-ecommerce-platform"></a>Sartu bezero-datuak merkataritza elektronikoko plataformatik

1. Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa [https://aka.ms/ciadclasscontacts](https://aka.ms/ciadclasscontacts).

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **Sorrera-data**: Data/ordua/zona

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

1. Eskuinaldeko paneleko "Izena" eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**

1. **Gorde** datu-iturburua.

### <a name="ingest-online-purchase-data"></a>Sartu sareko erosketen datuak

1. Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera. Aukeratu **Testua/CSV** konektorea berriro.

1. Idatzi **sareko erosketen** datuen URLa: https://aka.ms/ciadclassonline.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **PurchasedOn**: Data/ordua
   - **TotalPrice**: Moneta

1. Alboko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommercePurchases**.

1. **Gorde** datu-iturburua.

### <a name="ingest-customer-data-from-loyalty-schema"></a>Sartu bezero-datuak fideltasun-eskematik

1. Sortu **LoyaltyScheme** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscustomerloyalty.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **RewardsPoints**: Zenbaki osoa
   - **Sorrera-data**: Data/ordua

1. Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **loyCustomers**.

1. **Gorde** datu-iturburua.

### <a name="ingest-customer-data-from-website-reviews"></a>Sartu bezeroaren datuak webguneen berrikuspenetatik

1. Sortu **Webgunea** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua / CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/CI-ILT/WebReviews.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **ReviewRating**: zenbaki hamartarra
   - **Iritziaren data**: Data

1. Eskuineko paneleko 'Izena' eremuan, aldatu zure datu-iturburuaren izena **Kontsulta**-tik **Iritziak**-era.

1. **Gorde** datu-iturburua.

## <a name="task-2---data-unification"></a>2. zeregina - Datuen bateratzea

[!INCLUDE [sample-guide-unification](includes/sample-guide-unification.md)]

## <a name="task-3---configure-customer-lifetime-value-prediction"></a>3. ataza - Konfiguratu bezeroaren bizi-iraupenaren balioaren iragarpena

Bezeroen profil bateratuak ongi jarrita, bezeroaren bizi-iraupenaren balioaren iragarpena exekutatu dezakegu. Urrats zehatzak ikusteko, ikus [Bezeroaren bizitza osorako balioa iragarpen](predict-customer-lifetime-value.md).

1. Joan **Adimena**  > **Iragarpenak** eta hautatu **Bezeroaren bizi-iraupenaren balioaren eredua**.

1. Joan alboko paneleko informaziora eta hautatu **Hasi**.

1. Eman izen hau ereduari: **OOB eCommerce CLV iragarpena** eta hau irteerako entitateari: **OOBeCommerceCLVPrediction**.

1. Definitu modeloaren hobespenak CLV eredurako:
   - **iragarpenaren denbora-tartea**: **12 hilabete edo 1 urte**. Ezarpen honek bezeroaren bizi-iraupenaren balioaren iragartzeko etorkizunean noraino definitzen duen definitzen du.
   - **Bezero aktiboak** : Zehaztu bezero aktiboek zer esan nahi duten zure negozioarentzat. Ezarri bezeroak aktibo izateko gutxienez transakzio bat izan behar duen denbora-tarte historikoa. Ereduak bezero aktiboentzako CLV soilik aurreikusiko du. Aukeratu ereduak transakzio datu historikoetan oinarritutako denbora-tartea kalkulatzen utzi edo denbora-tarte jakin bat eman behar duen. Lagin gida honetan, **ereduak erosketa tartea kalkula dezan uzten diogu**, hau da aukera lehenetsia.
   - **Balio handiko bezeroak** : Definitu balio handiko bezeroak gehien ordaintzen dituzten bezeroen pertzentila gisa. Ereduak sarrera hori erabiltzen du balio handiko bezeroen negozioaren definizioarekin bat datozen emaitzak emateko. Ereduak balio handiko bezeroak definitzea hauta dezakezu. Perzentila eratortzen duen arau heuristikoa erabiltzen du. Balio handiko bezeroak defini ditzakezu gehien ordaintzen duten bezeroen pertzentil gisa. Lagin gida honetan, balio handiko bezeroak eskuz definitzen ditugu **ordaintzen duten bezero aktiboen % 30** gisa eta hautatu **Hurrengoa**.

    :::image type="content" source="media/clv-model-preferences.png" alt-text="Lehentasun urratsa CLV ereduaren esperientzia gidatuan.":::

1. **Beharrezko datuak** urratsean, hautatu **Gehitu datuak** transakzioen historiaren datuak emateko.

1. Gehitu **eCommerceErosketak: eCommerce** entitatea eta esleitu ereduak eskatzen dituen atributuak:
   - Transakzioaren IDa: eCommerce.eCommercePurchases.PurchaseId
   - Transakzioaren data: eCommerce.eCommercePurchases.PurchasedOn
   - Transakzioaren zenbatekoa: eCommerce.eCommercePurchases.TotalPrice
   - Produktuaren IDa: eCommerce.eCommercePurchases.ProductId

1. Hautatu **Hurrengoa**.

1. Konfiguratu **eCommerceErosketak: eCommerce** entitatea eta **eCommerceContacts: eCommerce** entitatearen arteko erlazioa.

1. **Datu osagarriak (aukerakoa)** urratsak bezeroen jardueren datu gehiago gehitzeko aukera ematen du. Datu horiek bezeroek zure negozioarekin dituzten elkarreraginak ezagutzeko informazio gehiago lortzen lagun dezakete, eta horrek CLVra ekar dezake. Bezeroen arteko elkarreragin nagusiak gehitzeak, esaterako web erregistroak, bezeroarentzako arreta-zerbitzu erregistroak edo saritze-programen historia, iragarpenen zehaztasuna hobe dezake. Aukeratu **Gehitu datuak** bezeroen jardueren datu gehiago sartzeko.

1. Gehitu bezeroaren jardueraren entitatea eta esleitu haren eremuen izenak ereduak eskatzen dituen eremuetara:
   - Bezeroaren jardueren entitatea: Reviews:Website
   - Gako nagusia: Website.Reviews.ReviewId
   - Denbora-marka: Website.Reviews.ReviewDate
   - Gertaera (jardueraren izena): Website.Reviews.ActivityTypeDisplay
   - Xehetasunak (zenbatekoa edo balioa): Website.Reviews.ReviewRating

1. Aukeratu **Hurrengoa** eta konfiguratu jarduera eta transakzio datuen eta bezeroen datuen arteko harremana:  
   - Jarduera mota: aukeratu lehendik daudenetatik
   - Jardueraren etiketa: Review
   - Dagokion etiketa: Website.Reviews.UserId
   - Bezeroaren entitatea: eCommerceContacts:eCommerce
   - Harremana: WebsiteReviews

1. Aukeratu **Hurrengoa** ereduaren antolaketa ezartzeko.

   Ereduak aldizka entrenatu behar du iradokitako datu berriak daudenean eredu berriak ikasteko. Adibide honetarako, aukeratu **Hilero**.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.

## <a name="task-4---review-model-results-and-explanations"></a>4. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Ondoren, CLV ereduaren emaitzak eta azalpenak berrikus ditzakezu. Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-customer-lifetime-value.md#review-prediction-status-and-results).

## <a name="task-5---create-a-segment-of-high-value-customers"></a>5. ataza - Sortu balio handiko bezeroen segmentu bat

Eredua exekutatzeak entitate berri bat sortzen du, **Datuak** > **Entitateak** zerrendan agertzen dena. Ereduak sortutako entitatean oinarrituta bezeroen segmentu berri bat sor dezakezu.

1. Joan hona: **Segmentuak**. 

1. Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**.

   ![Ereduaren irteerarekin segmentu bat sortzea.](media/segment-intelligence.png)

1. Aukeratu **OOBeCommerceCLVPrediction** entitatea eta definitu segmentua:
  - Eremua: CLVScore
  - Eragilea: hau baino handiagoa
  - Balioa: 1500

1. Aukeratu **Berrikuspena** eta **Gorde** segmentua.

Datozen 12 hilabeteetan $1500ko diru sarrera baino gehiago sortuko dituztela aurreikusten duten bezeroak identifikatzen dituen segmentu bat duzu orain. Segmentu hau dinamikoki eguneratzen da datu gehiago irensten badira.

Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).
