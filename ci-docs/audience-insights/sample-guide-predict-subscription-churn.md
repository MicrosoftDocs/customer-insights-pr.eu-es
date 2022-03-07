---
title: Harpidetzaren galera-tasaren iragarpenaren lagin-gida
description: Erabil ezazu lagin-gida hau harpidetzen galera-tasaren iragarpenaren eredua probatzeko.
ms.date: 11/19/2020
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: wameng
manager: shellyha
searchScope:
- ci-create-prediction
- customerInsights
ms.openlocfilehash: 5de57155b47b74efa4c5ef2fe63a3c87505644be
ms.sourcegitcommit: 73cb021760516729e696c9a90731304d92e0e1ef
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/25/2022
ms.locfileid: "8355598"
---
# <a name="subscription-churn-prediction-sample-guide"></a>Harpidetzaren galera-tasaren iragarpenaren lagin-gida

Harpidetzaren galera-tasaren iragarpenaren adibide bat azalduko dizugu, behean emandako lagin datuak erabiliz. 

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafea eta kafe-makinak sortzen dituen enpresa bat da. Horiek Contoso Coffee webgunearen bidez saltzen dituzte. Berriki harpidetza negozioa hasi zuten euren bezeroek aldiro kafea hartzeko. Haien helburua da ulertzea harpidetutako bezeroetako zeintzuk utz dezaketen harpidetza bertan behera hurrengo hilabeteetan. Zein bezero **galtzeko arriskua** dagoen jakiteak marketinarekin erlazionatutako ahalegina bideratzen lagun diezaioke enpresari, arreta bezero horiengan jarrita.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Berrikusi artikuluak [datuak sartzeari buruz](data-sources.md) eta [datu-iturriak erabiliz inportatzea Power Query konektoreak](connect-power-query.md) zehazki. Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin. 

### <a name="ingest-customer-data-from-ecommerce-platform"></a>Sartu bezero-datuak merkataritza elektronikoko plataformatik

1. Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscontacts.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **Jaioteguna**: Data
   - **Sorrera-data**: Data/ordua/zona

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

1. Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**

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

### <a name="ingest-subscription-information"></a>Sartu harpidetzari buruzko informazioa

1. Sortu **Harpidetzaren historia** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua / CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa https://aka.ms/ciadchurnsubscriptionhistory.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **Harpidetzaren IDa**: osoko zenbakia
   - **Harpidetza kopurua**: Moneta
   - **Harpidetzaren amaiera-data**: Data / Ordua
   - **Harpidetzaren hasiera-data**: Data / Ordua
   - **Transakzioaren data**: Data / Ordua
   - **Errepikakorra da**: Egia / gezurra
   - **Automatikoki berritzen da**: Egia / gezurra
   - **Errepikapen-maiztasuna, hilabetetan**: osoko zenbakia

1. Eskuineko paneleko **Izena** eremuan, aldatu **Kontsulta** izena datu-iturburuari eta idatzi **SubscriptionHistory**.

1. Gorde datu-iturburua.

### <a name="ingest-customer-data-from-website-reviews"></a>Sartu bezeroaren datuak webguneen berrikuspenetatik

1. Sortu **Webgunea** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua / CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa https://aka.ms/ciadclasswebsite.

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **Iritziaren batez besteko balorazioa**: osoko zenbakia
   - **Iritziaren data**: Data

1. Eskuineko paneleko 'Izena' eremuan, aldatu **Kontsulta** izena datu-iturburuari eta ipini **web-eko iritziak**.

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


## <a name="task-3---configure-the-subscription-churn-prediction"></a>3. zeregina - Konfiguratu harpidetzen galera-tasaren iragarpena

Bezeroen profil bateratuak behar bezala jarrita, harpidetzaren galera-tasaren iragarpena exekutatu dezakegu. Urrats zehatzak ikusteko, ikusi [Harpidetza txanda iragarpen](predict-subscription-churn.md) Artikulu. 

1. Joan **Adimena** > **Ezagutu** atalera eta hautatu **Bezeroen galera-tasaren eredua**.

1. Aukeratu **Harpidetza** aukera eta hautatu **Hasi**.

1. Eman **OOB eCommerce harpidetzen galera-tasaren iragarpena** izena ereduari eta **OOBSubscriptionChurnPrediction** irteerako entitateari.

1. Definitu galera-tasaren ereduaren bi baldintza:

   * **Harpidetza amaitu zenetik igarotako egunak**: **gutxienez 60** egun. Harpidetza amaitu eta bezeroak hura berritu ez badu ezarritako epean, galdutzat emango da. 

   * **Bezeroen galera-tasaren definizioa** : **gutxienez 93** egun. Ereduak behar duen denbora zein bezero galduko diren iragartzeko. Etorkizunean zenbat eta gehiago begiratu, orduan eta emaitza hain zehatzak izango dira.

     :::image type="content" source="media/model-subs-levers.PNG" alt-text="Aukeratu iragarpen-leihoa eta galera-tasaren definizioa ereduaren mailakatzaileak.":::

1. Aukeratu **Gehitu beharrezko datuak** eta hautatu **Gehitu datuak** harpidetzaren historiarako.

1. Gehitu **Harpidetza: harpidetzaren historia** entitatea eta esleitu elektronikoko eremuak ereduak eskatzen dituen eremuetara.

1. Sartu **Harpidetza: harpidetzaren historia** entitatea **merkataritza elektronikoko kontaktuak: merkataritza elektronikoa**, izendatu harremana **merkataritza elektronikoko harpidetza**.

   :::image type="content" source="media/model-subscription-join.PNG" alt-text="Sartu merkataritza elektronikoko entitateetan.":::

1. Bezeroen jardueretan, gehitu **web-eko iritziak: webgunea** entitatea eta esleitu web-eko iritziak ereduak eskatzen dituen eremuetara. 
   - Gako nagusia: ReviewId
   - Denbora-marka: ReviewDate
   - Gertaera: ReviewRating

1. Konfiguratu jarduera webguneen iritzietarako. Aukeratu **Berrikuspena** jarduera eta sartu **web-eko berrikuspenak: webgunea** entitatean **merkataritza elektronikoko kontaktuak: merkataritza elektronikoa**-rekin.

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