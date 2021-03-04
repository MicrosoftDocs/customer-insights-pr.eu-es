---
title: Produktuak gomendatzeko iragarpenaren adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen produktuak gomendatzeko iragarpen-eredua probatzeko.
ms.date: 02/10/2021
ms.reviewer: digranad
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 0ee873d9b7caa5f891cb2d5b8c665dec90ad0e59
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270464"
---
# <a name="product-recommendation-prediction-preview-sample-guide"></a>Produktuak gomendatzeko iragarpenaren (aurreargitalpena) adibide-gida

Produktuak gomendatzeko iragarpenaren adibide bat azalduko dizugu, behean emandako lagin datuak erabiliz.

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafea eta kafe-makinak sortzen dituen enpresa bat da. Horiek Contoso Coffee webgunearen bidez saltzen dituzte. Haien helburua da bezeroei zein produktu gomendatu behar dieten ulertzea. Bezero gehiago zer diren jakitea **erosteko litekeena**, marketineko ahalegina aurrezten lagun diezaiekete elementu zehatzetan arreta jarriz.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Berrikusi zehazki [datuen sarrerari](data-sources.md) eta [Power Query konektoreak erabiliz datu-iturburuak inportatzeari](connect-power-query.md) buruzko artikuluak. Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.

### <a name="ingest-customer-data-from-ecommerce-platform"></a>Sartu bezero-datuak merkataritza elektronikoko plataformatik

1. Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscontacts.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **Sorrera-data**: Data/ordua/zona

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

5. Eskuinaldeko paneleko "Izena" eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**

6. **Gorde** datu-iturburua.

### <a name="ingest-online-purchase-data"></a>Sartu sareko erosketen datuak

1. Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera. Aukeratu **Testua/CSV** konektorea berriro.

1. Idatzi **sareko erosketen** datuen URLa: https://aka.ms/ciadclassonline.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **PurchasedOn**: Data/ordua
   - **TotalPrice**: Moneta

1. Alboko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommercePurchases**.

1. Gorde datu-iturburua.


### <a name="ingest-customer-data-from-loyalty-schema"></a>Sartu bezero-datuak fideltasun-eskematik

1. Sortu **LoyaltyScheme** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscustomerloyalty.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **RewardsPoints**: Zenbaki osoa
   - **Sorrera-data**: Data/ordua

1. Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **loyCustomers**.

1. Gorde datu-iturburua.

## <a name="task-2---data-unification"></a>2. zeregina - Datuen bateratzea

Behin datuak sartuta, **Esleitu, bat etorri, konbinatu** prozesuarekin hasiko gara, bezeroaren profil bateratu bat sortzeko. Informazio gehiago lortzeko, ikusi [Datuen bateratzea](data-unification.md).

### <a name="map"></a>Esleitu

1. Behin datuak sartuta, esleitu merkataritza elektronikoko eta fideltasun-datuetako kontaktuak ohiko datu motei. Joan hona: **Datuak** > **Bateratu** > **Esleitu**.

2. Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**.

   ![bateratu ecommerce eta loyalty datu-iturburuak.](media/unify-ecommerce-loyalty.png)

3. Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.

   ![Bateratu LoyaltyId gako nagusi gisa.](media/unify-loyaltyid.png)

### <a name="match"></a>Lotzea

1. Joan **Bat etorri** fitxara eta hautatu **Ezarri ordena**.

2. **Nagusia** goitibeherako zerrendan, aukeratu **eCommerceContacts : eCommerce** iturburu nagusi gisa eta sartu erregistro guztiak.

3. **2. entitatea** goitibeherako zerrendan, aukeratu **loyCustomers : LoyaltyScheme** eta sartu erregistro guztiak.

   ![Bateratu eCommerce eta Loyalty bat-etortzea.](media/unify-match-order.png)

4. Hautatu **Sortu beste arau bat**

5. Gehitu lehenengo baldintza FullName erabilita.

   - eCommerceContacts entitateari dagokionez, hautatu **FullName** goitibeherako zerrendan.
   - loyCustomers entitateari dagokionez, hautatu **FullName** goitibeherako zerrendan.
   - Aukeratu **Normalizatu** goitibeherako zerrendan eta aukeratu **Mota (Telefonoa, Izena, Helbidea, ...)**.
   - Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.

6. Idatzi arau berriaren **Izen osoa, posta elektronikoa** izena.

   - Gehitu helbide elektronikoaren bigarren baldintza bat **Gehitu baldintza** hautatuta
   - ECommerceContacts entitateari dagokionez, aukeratu **Helbide elektronikoa** goitibeherako zerrendan.
   - loyCustomers entitateari dagokionez, aukeratu **Helbide elektronikoa** goitibeherako zerrendan.
   - "Normalizatu" hutsik utzi.
   - Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.

   ![Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.](media/unify-match-rule.png)

7. Hautatu **gorde** eta **exekutatu**.

### <a name="merge"></a>Konbinazioa

1. Joan **konbinatu** fitxara.

1. **loyCustomers** entitatearen **Kontaktuaren IDa** atalean, aldatu bistaratzeko izena **ContactIdLOYALTY** izenera, sartutako beste IDetatik bereizteko.

   ![aldatu leialtasun IDaren kontaktuaren IDa.](media/unify-merge-contactid.png)

1. Aukeratu **Gorde** eta **exekutatu** konbinatzeko prozesua hasteko.

## <a name="task-3---configure-product-recommendation-prediction"></a>3. zeregina: konfiguratu produktuaren gomendioa iragarpena

Bezeroen profil bateratuak behar bezala jarrita, harpidetzaren galera-tasaren iragarpena exekutatu dezakegu.

1. Joan **Adimena** > **Iragarpena** aukerara eta aukeratu **Produktuen gomendioa**.

1. Hautatu **Hasi erabiltzen**.

1. Eman izena ereduari **OOB produktuaren gomendio eredua iragarpena** eta irteerako entitatea **OOBProductRecomendationModelPrediction**.

1. Definitu ereduaren hiru baldintza:

   - **Produktu kopurua**: ezarri balio hau **5**. Ezarpen honek bezeroei zenbat produktu gomendatu nahi dizkiezu definitzen du.

   - **Bezeroek berriki erosi dituzten produktuak iradokitzen al dituzu?**: aukeratu **Bai** zure bezeroek aurretik erositako gomendioan produktuak sartu nahi dituzula adierazteko.

   - **Atzera begiratu leihoa:** aukeratu gutxienez **365 egun**. Ezarpen honek zenbat egun atzera dezakezun eredua ikusteko aukera, informazio hori erabili ahal izateko bezeroek ikusiko duten gomendioak hobetzeko.
   
   :::image type="content" source="media/product-recommendation-model-preferences.png" alt-text="Produktuaren gomendio-ereduaren eredu-hobespenak.":::

1. Aukeratu **Beharrezko datuak** eta hautatu **Gehitu datuak** erosketen historiarako.

1. Gehitu **merkataritza elektronikoko erosketak: elektronikoa** entitatea eta esleitu elektronikoko eremuak ereduak eskatzen dituen eremuetara.

1. Sartu **merkataritza elektroniko erosketak: merkataritza elektronikoa** entitatera **merkataritza elektroniko kontaktuak: merkataritza elektronikoa** entitatearekin.

   ![Sartu merkataritza elektronikoko entitateetan.](media/model-purchase-join.png)

1. Aukeratu **Hurrengoa** ereduaren antolaketa ezartzeko.

   Ereduak aldizka trebatu behar du eredu berriak ikasteko datu berriak sartzen direnean. Adibide honetarako, hautatu **hilero**.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.


## <a name="task-4---review-model-results-and-explanations"></a>4. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Produktuak gomendatzeko ereduaren azalpenak berrikus ditzakezu. Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-subscription-churn.md#review-a-prediction-status-and-results).

## <a name="task-5---create-a-segment-of-high-purchased-products"></a>5. zeregina: sortu erositako produktuen segmentu bat

Ekoizpen eredua martxan jartzeak hemen ikus dezakezun entitate berri bat sortzen du: **Datuak** > **Entitateak**.

Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.

1. Joan hona: **Segmentuak**. Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**.

   ![Ereduaren irteerarekin segmentu bat sortzea.](media/segment-intelligence.png)

1. Aukeratu **OOBProductRecommendationModelPrediction** amaiera-puntua eta definitu segmentua:

   - Eremua: ProductID
   - Eragilea: balioa
   - Balioa: hautatu produktuaren hiru ID nagusiak

   :::image type="content" source="media/product-recommendation-quick-segment.png" alt-text="Sortu segmentu bat ereduaren emaitzetatik.":::

Gomendatutako hiru produktuak erosteko prest dauden bezeroak identifikatzen dituen segmentu dinamikoki eguneratua duzu orain 

Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]