---
title: Produktuak gomendatzeko iragarpenaren adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen produktuak gomendatzeko iragarpen-eredua probatzeko.
ms.date: 05/16/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: wameng
manager: shellyha
searchScope:
- ci-predictions
- ci-create-prediction
- customerInsights
ms.openlocfilehash: cc72cce15fa0c9e92dbf202c803e99514c9ce2b1
ms.sourcegitcommit: 82f417cfb0a16600e9f552d7a21d598cc8f5a267
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/16/2022
ms.locfileid: "8762671"
---
# <a name="product-recommendation-prediction-sample-guide"></a>Produktuak gomendatzeko iragarpenaren adibide-gida

Produktuak gomendatzeko iragarpenaren adibide bat azalduko dizugu, behean emandako lagin datuak erabiliz.

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafea eta kafe-makinak sortzen dituen enpresa bat da. Horiek Contoso Coffee webgunearen bidez saltzen dituzte. Haien helburua da bezeroei zein produktu gomendatu behar dieten ulertzea. Bezero gehiago zer diren jakitea **erosteko litekeena**, marketineko ahalegina aurrezten lagun diezaiekete elementu zehatzetan arreta jarriz.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.
- Honako urrats hauek [ingurune berri batean](manage-environments.md) inplementatzea gomendatzen dizugu.

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Berrikusi artikuluak [datuak sartzeari buruz](data-sources.md) eta [datu-iturriak erabiliz inportatzea Power Query konektoreak](connect-power-query.md) zehazki. Honako informazio honetan, ulertzen da ohituta zaudela orokorrean datuen sarrerarekin.

### <a name="ingest-customer-data-from-ecommerce-platform"></a>Sartu bezero-datuak merkataritza elektronikoko plataformatik

1. Sortu **merkataritza elektronikoa** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.

1. Sartu merkataritza elektronikoko kontaktuen URLa: [https://aka.ms/ciadclasscontacts](https://aka.ms/ciadclasscontacts).

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **Sorrera-data**: Data/ordua/zona

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

1. Eskuinaldeko paneleko "Izena" eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommerceContacts**

1. **Gorde** datu-iturburua.

### <a name="ingest-online-purchase-data"></a>Sartu sareko erosketen datuak

1. Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera. Aukeratu **Testua/CSV** konektorea berriro.

1. Sartu URLa **Lineako Erosketak** datuak [https://aka.ms/ciadclassonline](https://aka.ms/ciadclassonline).

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **PurchasedOn**: Data/ordua
   - **TotalPrice**: Moneta

1. Alboko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **eCommercePurchases**.

1. **Gorde** datu-iturburua.

### <a name="ingest-customer-data-from-loyalty-schema"></a>Sartu bezero-datuak fideltasun-eskematik

1. Sortu **LoyaltyScheme** izeneko datu-iturburu bat, aukeratu inportatzeko aukera eta hautatu **Testua/CSV** konektorea.

1. Sartu merkataritza elektronikoko kontaktuen URLa [https://aka.ms/ciadclasscustomerloyalty](https://aka.ms/ciadclasscustomerloyalty).

1. Datuak editatu bitartean, hautatu **Bihurtu**, eta, ondoren, **Erabili lehenengo errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **RewardsPoints**: Zenbaki osoa
   - **Sorrera-data**: Data/ordua

1. Eskuinaldeko paneleko **Izena** eremuan, aldatu izena **Kontsulta** datu-iturburuari eta ipini izen hau: **loyCustomers**.

1. **Gorde** datu-iturburua.

## <a name="task-2---data-unification"></a>2. zeregina - Datuen bateratzea

[!INCLUDE [sample-guide-unification](includes/sample-guide-unification.md)]

## <a name="task-3---configure-product-recommendation-prediction"></a>3. zeregina: konfiguratu produktuaren gomendioa iragarpena

Bezeroen profil bateratuak ezarrita, orain iragarpen produktuaren gomendioa exekutatu dezakegu.

1. Joan **Adimena** > **Iragarpena** aukerara eta aukeratu **Produktuen gomendioa**.

1. Hautatu **Hasi erabiltzen**.

1. Eman izena ereduari **OOB produktuaren gomendio eredua iragarpena** eta irteerako entitatea **OOBProductRecomendationModelPrediction**.

1. Definitu ereduaren hiru baldintza:

   - **Produktu kopurua**: ezarri balio hau **5**. Ezarpen honek bezeroei zenbat produktu gomendatu nahi dizkiezu definitzen du.

   - **Espero diren erosketak errepikatu**: Aukeratu **Bai** zure bezeroek aurretik erositako gomendioan produktuak sartu nahi dituzula adierazteko.

   - **Atzera begiratu leihoa:** aukeratu gutxienez **365 egun**. Ezarpen honek zenbat egun atzera dezakezun eredua ikusteko aukera, informazio hori erabili ahal izateko bezeroek ikusiko duten gomendioak hobetzeko.

   :::image type="content" source="media/product-recommendation-model-preferences.png" alt-text="Produktuaren gomendio-ereduaren eredu-hobespenak.":::

1. urtean **Gehitu beharrezko datuak** urratsa, hautatu **Gehitu datuak**.

1. urtean **Gehitu datuak** panela, aukeratu **SalesOrderLine** erosketen historiako entitate gisa. Une honetan, litekeena da oraindik konfiguratuta ez egotea. Ireki esteka panelean jarduera sortzeko urrats hauekin:
   1. Sartu bat **Jardueraren izena** eta aukeratu *eCommercePurchases: eCommerce* gisa **Jarduera-entitatea**. The **Lehen gakoa** da *ErosketaId*.
   1. Definitu eta izendatu harremana *eCommerceContacts: eCommerce entitatea* eta aukeratu **Kontaktu ID** kanpoko gako gisa.
   1. Jarduerak bateratzeko, ezarri **Ekitaldi-jarduera** gisa *Prezio totala* eta Denbora-zigilua *Erosia*. Eremu gehiago zehaz ditzakezu atalean azaltzen den moduan [Bezeroen jarduerak](activities.md).
   1. Izan ere **Jarduera mota**, aukeratu *SalesOrderLine*. Kartografiatu jarduera-eremu hauek:
      - Eskaera-lerroaren IDa: PurchaseId
      - Eskaera ID: PurchaseId
      - Eskaeraren datuak: PurchasedOn
      - Produktuaren ID: ProductId
      - Zenbatekoa: Prezioa guztira
   1. Berrikusi eta amaitu jarduera ereduaren konfiguraziora itzuli aurretik.

1. Itzuli **Aukeratu jarduerak** urratsa, aukeratu sortu berria den jarduera **Jarduerak** atala. Hautatu **Hurrengoa** eta atributu-mapea dagoeneko beteta dago. Hautatu **Gorde**.

1. Lagin-gida honetan, saltatzen dugu **Gehitu produktuaren informazioa** eta **Produktu-iragazkiak** ezarri produktuaren informazio-daturik ez dugulako.

1. urtean **Datuen eguneraketak** urratsa, ezarri ereduaren ordutegia.

   Ereduak aldizka trebatu behar du eredu berriak ikasteko datu berriak sartzen direnean. Adibide honetarako, hautatu **hilero**.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**. Minutu batzuk beharko dira eredua lehen aldiz exekutatzeko.

## <a name="task-4---review-model-results-and-explanations"></a>4. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Produktuak gomendatzeko ereduaren azalpenak berrikus ditzakezu. Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-transactional-churn.md#review-a-prediction-status-and-results).

## <a name="task-5---create-a-segment-of-high-purchased-products"></a>5. zeregina: sortu erositako produktuen segmentu bat

Ekoizpen eredua martxan jartzeak hemen ikus dezakezun entitate berri bat sortzen du: **Datuak** > **Entitateak**.

Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.

1. Joan hona: **Segmentuak**. Hautatu **Berria** eta aukeratu **Sortu Inteligentziatik**.

   ![Ereduaren irteerarekin segmentu bat sortzea.](media/segment-intelligence.png)

1. Aukeratu **OOBProductRecommendationModelPrediction** amaiera-puntua eta definitu segmentua:

   - Eremua: ProductID
   - Balioa: hautatu produktuaren hiru ID nagusiak

   :::image type="content" source="media/product-recommendation-quick-segment.png" alt-text="Sortu segmentu bat ereduaren emaitzetatik.":::

Orain dinamikoki eguneratzen den segmentu bat duzu, hiru produktu gomendatuenak erosteko interesa izan dezaketen bezeroak identifikatzen dituena.

Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
