---
title: Transakzioen galera-tasaren iragarpenari buruzko adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen transakzioen galera-tasaren iragarpen-eredua probatzeko.
ms.date: 05/11/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 3edbf2a471313379c28db874d7f19c3265a23299
ms.sourcegitcommit: 6a5f4312a2bb808c40830863f26620daf65b921d
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8741304"
---
# <a name="transactional-churn-prediction-sample-guide"></a>Transakzioen galera-tasaren iragarpenari buruzko adibide-gida

Gida honek Customer Insights zerbitzuko transakzioen galera-tasaren iragarpenaren adibide oso bat aurkeztuko dizu, jarraian emandako datuak erabilita. Gidan erabilitako datuak ez dira bezero-datu errealak eta Customer Insights harpidetzako *Demo* ingurunean aurkitutako Contoso datu multzoaren parte dira.

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafea eta kafe-makinak sortzen dituen enpresa bat da. Horiek Contoso Coffee webgunearen bidez saltzen dituzte. Enpresaren helburua da jakitea egunerokotasunean bere produktuak erosten dituzten bezeroetako nortzuk utziko dioten bezero aktibo izateari datozen 60 egunetan. Zein bezero **galtzeko arriskua** dagoen jakiteak marketinarekin erlazionatutako ahalegina bideratzen lagun diezaioke enpresari, arreta bezero horiengan jarrita.

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

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Bihurtu jaioteguna data.":::

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

[!INCLUDE [sample-guide-unification](includes/sample-guide-unification.md)]

## <a name="task-3---configure-transaction-churn-prediction"></a>3. zeregina - Konfiguratu transakzioen galera-tasaren iragarpena

Bezeroen profil bateratuak ezarrita, orain iragarpen transakzioen txanda exekutatu dezakegu. Urrats zehatzak ikusteko, ikusi [Transakzio txanda iragarpen](predict-transactional-churn.md) Artikulu. 

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

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Orain birrintze ereduaren azalpenak berrikus ditzakezu. Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-transactional-churn.md#review-a-prediction-status-and-results).

## <a name="task-5---create-a-segment-of-high-churn-risk-customers"></a>5. zeregina - Sortu galera-arrisku handiko bezeroen segmentu bat

Ekoizpen eredua martxan jartzeak hemen ikus dezakezun entitate berri bat sortzen du: **Datuak** > **Entitateak**.   

Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.

1.  Joan hona: **Segmentuak**. Aukeratu **Berria** eta aukeratu **Sortu hemendik** > **Adimena**. 

   :::image type="content" source="media/segment-intelligence.PNG" alt-text="Ereduaren irteerarekin segmentu bat sortzea.":::

1. Hautatu **OOBeCommerceChurnPrediction** amaierako puntua eta definitu segmentua: 
   - Eremua: ChurnScore
   - Eragilea: hau baino handiagoa
   - Balioa: 0.6

Orain dinamikoki eguneratzen den segmentu bat duzu, arrisku handiko bezeroak identifikatzen dituena.

Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).


[!INCLUDE [footer-include](includes/footer-banner.md)]
