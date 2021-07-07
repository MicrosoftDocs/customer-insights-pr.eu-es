---
title: Transakzioen galera-tasaren iragarpenari buruzko adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen transakzioen galera-tasaren iragarpen-eredua probatzeko.
ms.date: 11/19/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: diegogranados117
ms.author: digranad
manager: shellyha
ms.openlocfilehash: 49dad45c951f3c00d77ddd99faec48bfccada8b0
ms.sourcegitcommit: 0b754d194d765afef70d1008db7b347dd1f0ee40
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306105"
---
# <a name="transactional-churn-prediction-preview-sample-guide"></a>Transakzioen galera-tasaren iragarpenari (aurrebista) buruzko adibide-gida

Gida honek Customer Insights zerbitzuko transakzioen galera-tasaren iragarpenaren adibide oso bat aurkeztuko dizu, jarraian emandako datuak erabilita. Gida honetan erabilitako datu guztiak ez dira bezeroen benetako datuak eta Contoso datu-basean aurkitu da *Demo* ingurunea zure Customer Insights harpidetzaren barruan.

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafea eta kafe makinak ekoizten dituen enpresa da eta Contoso Coffee webgunearen bidez saltzen dituzte. Enpresaren helburua da jakitea egunerokotasunean bere produktuak erosten dituzten bezeroetako nortzuk utziko dioten bezero aktibo izateari datozen 60 egunetan. Zein bezero **galtzeko arriskua** dagoen jakiteak marketinarekin erlazionatutako ahalegina bideratzen lagun diezaioke enpresari, arreta bezero horiengan jarrita.

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

   [!div class="mx-imgBorder"]
   ![Bihurtu jaioteguna data](media/ecommerce-dob-date.PNG "eraldatu jaiotze data datara")

1. Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**

1. Gorde datu-iturburua.

### <a name="ingest-online-purchase-data"></a>Sartu sareko erosketen datuak

1. Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera. Aukeratu **Testua/CSV** konektorea berriro.

1. Idatzi **sareko erosketen** datuen URLa: https://aka.ms/ciadclassonline.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **PurchasedOn**: Data/ordua
   - **TotalPrice**: Moneta
   
1. Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommercePurchases**.

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

1. Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**. 

   :::image type="content" source="media/unify-ecommerce-loyalty.PNG" alt-text="bateratu ecommerce eta loyalty datu-iturburuak.":::

1. Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.

   :::image type="content" source="media/unify-loyaltyid.PNG" alt-text="Bateratu LoyaltyId gako nagusi gisa.":::

### <a name="match"></a>Lotu

1. Joan **Bat etorri** fitxara eta hautatu **Ezarri ordena**.

1. Urtean **Lehen Hezkuntza** goitibeherako zerrenda, aukeratu **eCommerceContacts: eCommerce** iturri nagusi gisa eta erregistro guztiak barne.

1. Urtean **2. entitatea** goitibeherako zerrenda, aukeratu **loyCustomers: LoyaltyScheme** eta erregistro guztiak sartu.

   :::image type="content" source="media/unify-match-order.PNG" alt-text="Bateratu eCommerce eta Loyalty bat-etortzea.":::

1. Hautatu **Sortu beste arau bat**

1. Gehitu lehenengo baldintza FullName erabilita.

   * ECommerceContacts aukeratzeko **Izen abizenak** goitibeherakoan.
   * loyCustomers aukeratzeko **Izen abizenak** goitibeherakoan.
   * Aukeratu **Normalizatu** goitibeherako zerrendan eta aukeratu **Mota (Telefonoa, Izena, Helbidea, ...)**.
   * Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.

1. Idatzi arau berriaren **Izen osoa, posta elektronikoa** izena.

   * Gehitu helbide elektronikoaren bigarren baldintza bat **Gehitu baldintza** hautatuta
   * ECommerceContacts entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan.
   * loyCustomers entitateari dagokionez, aukeratu **Mezu elektronikoa** goitibeherakoan. 
   * "Normalizatu" hutsik utzi. 
   * Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.

   :::image type="content" source="media/unify-match-rule.PNG" alt-text="Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.":::

7. Hautatu **gorde** eta **exekutatu**.

### <a name="merge"></a>Konbinazioa

1. Joan **konbinatu** fitxara.

1. **loyCustomers** entitatearen **Kontaktuaren IDa** atalean, aldatu bistaratzeko izena **ContactIdLOYALTY** izenera, sartutako beste IDetatik bereizteko.

   :::image type="content" source="media/unify-merge-contactid.PNG" alt-text="aldatu leialtasun IDaren kontaktuaren IDa.":::

1. Aukeratu **Gorde** eta **exekutatu** konbinatzeko prozesua hasteko.



## <a name="task-3---configure-transaction-churn-prediction"></a>3. zeregina - Konfiguratu transakzioen galera-tasaren iragarpena

Bezeroen profil bateratuak behar bezala jarrita, harpidetzaren galera-tasaren iragarpena exekutatu dezakegu. Urrats zehatzetarako, ikusi [Harpidetzaren galera-tasaren iragarpena (aurrebista)](predict-subscription-churn.md) artikulu. 

1. Joan **Adimena** > **Ezagutu** atalera eta hautatu **Bezeroen galera-tasaren eredua**.

1. Aukeratu **Transakzionala** aukera eta hautatu **Hasi**.

1. Eman **OOB eCommerce transakzioen galera-tasaren iragarpena** izena ereduari eta **OOBeCommerceChurnPrediction** irteerako entitateari.

1. Definitu galera-tasaren ereduaren bi baldintza:

   * **Iragarpen leihoa**: **gutxienez 60** egun. Ezarpen honek definitzen du etorkizunean noraino iragarri nahi dugun bezeroaren galera-tasa.

   * **Bezeroen galera-tasaren definizioa** : **gutxienez 60** egun. Erosketa gabeko iraupena, bezero bat galdutzat hartu ondoren.

     :::image type="content" source="media/model-levers.PNG" alt-text="Aukeratu iragarpen-leihoa eta galera-tasaren definizioa ereduaren mailakatzaileak.":::

1. Aukeratu **Erosketen historia (beharrezkoa)** eta hautatu **Gehitu datuak** erosketen historiarako.

1. Gehitu **merkataritza elektronikoko erosketak: elektronikoa** entitatea eta esleitu elektronikoko eremuak ereduak eskatzen dituen eremuetara.

1. Sartu **merkataritza elektroniko erosketak: merkataritza elektronikoa** entitatera **merkataritza elektroniko kontaktuak: merkataritza elektronikoa** entitatearekin.

   :::image type="content" source="media/model-purchase-join.PNG" alt-text="Sartu merkataritza elektronikoko entitateetan.":::

1. Aukeratu **Hurrengoa** ereduaren antolaketa ezartzeko.

   Ereduak aldizka trebatu behar du eredu berriak ikasteko datu berriak sartzen direnean. Adibide honetarako, hautatu **hilero**.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.

## <a name="task-4---review-model-results-and-explanations"></a>4. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Harpidetzen galera-tasaren ereduaren azalpenak berrikus ditzakezu. Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-subscription-churn.md#review-a-prediction-status-and-results).

## <a name="task-5---create-a-segment-of-high-churn-risk-customers"></a>5. zeregina - Sortu galera-arrisku handiko bezeroen segmentu bat

Ekoizpen eredua martxan jartzeak hemen ikus dezakezun entitate berri bat sortzen du: **Datuak** > **Entitateak**.   

Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.

1.  Joan hona: **Segmentuak**. Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**. 

   :::image type="content" source="media/segment-intelligence.PNG" alt-text="Ereduaren irteerarekin segmentu bat sortzea.":::

1. Aukeratu **OOBSubscriptionChurnPrediction** amaiera-puntua eta definitu segmentua: 
   - Eremua: ChurnScore
   - Eragilea: hau baino handiagoa
   - Balioa: 0.6
   
   :::image type="content" source="media/segment-setup-subs.PNG" alt-text="Konfiguratu harpidetzaren galera-tasaren segmentua.":::

Harpidetza-negozio honen galera-arrisku handiko bezeroak identifikatzen dituen segmentu dinamikoki eguneratua duzu.

Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]