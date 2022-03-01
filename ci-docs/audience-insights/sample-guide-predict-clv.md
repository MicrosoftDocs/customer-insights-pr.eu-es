---
title: Bezeroaren bizi-iraupenaren balioa iragarpenaren lagin gida
description: Erabili lagin gida hau bezeroaren bizi-iraupenaren balio osorako iragarpen modeloa probatzeko.
ms.date: 05/25/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: yashlundia
ms.author: yalundia
manager: shellyha
ms.openlocfilehash: 73d294a285b4ad706bec7fe925c1daa0b839ddd6
ms.sourcegitcommit: 7b6189e47ed1f87e7ce35d40e4cf7a6730f31ef2
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129930"
---
# <a name="customer-lifetime-value-clv-prediction-sample-guide"></a>Bezeroaren bizi-iraupenaren balioaren iragarpenaren lagin gida

Gida honek Bezeroaren bizi-iraupenaren balio osoko (CLV) iragarpen adibidearen amaierako adibidea azalduko dizu Customer Insights-en, lagin-datuak erabiliz.

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafea eta kafe makinak ekoizten dituen enpresa da. Produktuak Contoso Coffee webgunearen bidez saltzen dituzte. Konpainiak bezeroek hurrengo 12 hilabeteetan sor dezaketen balioa (diru-sarrerak) ulertu nahi du. Datozen 12 hilabeteetan bezeroek espero duten balioa ezagutzeak balio handiko bezeroenganako marketin ahalegina bideratzen lagunduko die.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzailearen baimenak](permissions.md) hartzaileen xehetasunetan.
- Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Errepasatu [datuen irensteari](data-sources.md) eta [datu iturriak Power Query konektoreen bidez inportatzeari](connect-power-query.md) buruzko artikuluak. Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.

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

Datuak irentsi ondoren, datuak bateratzeko prozesua hasten dugu bezeroaren profil bateratua sortzeko. Informazio gehiago lortzeko, ikusi [Datuen bateratzea](data-unification.md).

### <a name="map"></a>Esleitu

1. Behin datuak sartuta, esleitu merkataritza elektronikoko eta fideltasun-datuetako kontaktuak ohiko datu motei. Joan hona: **Datuak** > **Bateratu** > **Esleitu**.

1. Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**. Ondoren, hautatu **Aplikatu**.

   ![bateratu ecommerce eta loyalty datu-iturburuak.](media/unify-ecommerce-loyalty.png)

1. Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.

   ![Bateratu LoyaltyId gako nagusi gisa.](media/unify-loyaltyid.png)

1. Sakatu **Gorde**.

### <a name="match"></a>Lotu

1. Joan **Bat etorri** fitxara eta hautatu **Ezarri ordena**.

1. **Nagusia** goitibeherako zerrendan, aukeratu **eCommerceContacts : eCommerce** iturburu nagusi gisa eta sartu erregistro guztiak.

1. **2. entitatea** goitibeherako zerrendan, aukeratu **loyCustomers : LoyaltyScheme** eta sartu erregistro guztiak.

   ![Bateratu eCommerce eta Loyalty bat-etortzea.](media/unify-match-order.png)

1. Hautatu **Gehitu araua**

1. Gehitu lehenengo baldintza FullName erabilita.

   - eCommerceContacts entitateari dagokionez, hautatu **FullName** goitibeherako zerrendan.
   - loyCustomers entitateari dagokionez, hautatu **FullName** goitibeherako zerrendan.
   - Aukeratu **Normalizatu** goitibeherako zerrendan eta aukeratu **Mota (Telefonoa, Izena, Helbidea, ...)**.
   - Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.

1. Idatzi arau berriaren **Izen osoa, posta elektronikoa** izena.

   - Gehitu helbide elektronikoaren bigarren baldintza bat **Gehitu baldintza** hautatuta
   - ECommerceContacts entitateari dagokionez, aukeratu **Helbide elektronikoa** goitibeherako zerrendan.
   - loyCustomers entitateari dagokionez, aukeratu **Helbide elektronikoa** goitibeherako zerrendan.
   - "Normalizatu" hutsik utzi.
   - Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.

   ![Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.](media/unify-match-rule.png)

1. Hautatu **Eginda**.

1. Hautatu **gorde** eta **exekutatu**.

### <a name="merge"></a>Konbinazioa

1. Joan **konbinatu** fitxara.

1. **loyCustomers** entitatearen **Kontaktuaren IDa** atalean, aldatu bistaratzeko izena **ContactIdLOYALTY** izenera, sartutako beste IDetatik bereizteko.

   ![aldatu leialtasun IDaren kontaktuaren IDa.](media/unify-merge-contactid.png)

1. Hautatu **gorde** eta **exekutatu konbinazio eta beherako prozesuak**.

## <a name="task-3---configure-customer-lifetime-value-prediction"></a>3. ataza - Konfiguratu bezeroaren bizi-iraupenaren balioaren iragarpena

Bezeroen profil bateratuak ongi jarrita, bezeroaren bizi-iraupenaren balioaren iragarpena exekutatu dezakegu. Urrats zehatzak lortzeko, ikus [Bezeroaren bizi-iraupenaren balioaren iragarpena (aurrebista)](predict-customer-lifetime-value.md).

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
