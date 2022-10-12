---
title: Produktuak gomendatzeko iragarpenaren adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen produktuak gomendatzeko iragarpen-eredua probatzeko.
ms.date: 09/19/2022
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
ms.openlocfilehash: 2b42a89e3f4ec8cf4f0769128b8536973365f1cb
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610129"
---
# <a name="product-recommendation-prediction-sample-guide"></a>Produktuak gomendatzeko iragarpenaren adibide-gida

Gida honek iragarpen produktuaren gomendioaren amaieratik amaierako adibide bat eskaintzen dizu lagin-datuak erabiliz. Iragarpen hau probatzea gomendatzen dizugu [ingurune berri batean](manage-environments.md).

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafe eta kafe makinak ekoizten dituen enpresa da. Contoso Kafearen webgunearen bidez saltzen dituzte produktuak. Haien helburua da bezeroei zein produktu gomendatu behar dieten ulertzea. Bezeroak zer diren gehiago jakitea **erosteko aukera** marketin-ahaleginak aurrezten lagun diezaieke elementu zehatzetan zentratuz.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Berrikusi artikuluak [datuak sartzeari buruz](data-sources.md) eta [batekin konektatzen Power Query datu-iturburu](connect-power-query.md). Informazio honek, oro har, datuak irensten ezagutzen dituzula suposatzen du.

### <a name="ingest-customer-data-from-ecommerce-platform"></a>Sartu bezero-datuak merkataritza elektronikoko plataformatik

1. Sortu Power Query datu-iturburu izeneko bat **merkataritza elektronikoa** eta hautatu **Testua/CSV** konektorea.

1. Sartu merkataritza elektronikoko kontaktuen URLa:https://aka.ms/ciadclasscontacts.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **Sorrera-data**: Data/ordua/zona

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **eCommerceContacts**.

1. **Gorde** datu-iturburua.

### <a name="ingest-online-purchase-data"></a>Sartu sareko erosketen datuak

1. Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera. Aukeratu **Testua/CSV** konektorea berriro.

1. Sartu lineako erosketen datuen URLa https://aka.ms/ciadclassonline.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **PurchasedOn**: Data/ordua
   - **TotalPrice**: Moneta

1. urtean **Izena** alboko paneleko eremuan, izena aldatu zure datu-iturburu **eCommerceErosketak**.

1. **Gorde** datu-iturburua.

### <a name="ingest-customer-data-from-loyalty-schema"></a>Sartu bezero-datuak fideltasun-eskematik

1. Sortu datu-iturburu izeneko bat **LeialtasunEgitasmoa** eta hautatu **Testua/CSV** konektorea.

1. Sartu bezero leialen URLa https://aka.ms/ciadclasscustomerloyalty.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **RewardsPoints**: Zenbaki osoa
   - **Sorrera-data**: Data/ordua

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **loyBezeroak**.

1. **Gorde** datu-iturburua.

## <a name="task-2---data-unification"></a>2. zeregina - Datuen bateratzea

Berrikusi artikulua [datuen bateratzeari buruz](data-unification.md). Informazio honek datuen bateratzea orokorrean ezagutzen duzula suposatzen du.

[!INCLUDE [sample-guide-unification](includes/sample-guide-unification.md)]

## <a name="task-3---create-transaction-history-activity"></a>3. ataza - Transakzioen historiako jarduera sortzea

Berrikusi artikulua [bezeroen jarduerei buruz](activities.md). Ondorengo informazioak, oro har, jarduerak sortzen ezagutzen dituzula suposatzen du.

1. Sortu izeneko jarduera bat **eCommerceErosketak** nirekin *eCommercePurchases: eCommerce* entitatea eta bere gako nagusia, **ErosketaId**.

1. Sortu arteko harremana *eCommercePurchases: eCommerce* eta *eCommerceContacts: eCommerce* rekin **Kontaktu ID** bi entitateak konektatzeko atzerriko gako gisa.

1. Hautatu **Prezio totala** rentzat **GertaeraJarduera** eta **Erosian** rentzat **Denbora-zigilua**.

1. Hautatu **SalesOrderLine** rentzat **Jarduera mota** eta jardueraren datuak semantikoki mapatzea.

1. Exekutatu jarduera.

## <a name="task-4---configure-product-recommendation-prediction"></a>4. zeregina: konfiguratu produktuaren gomendioa iragarpena

Bezeroen profil bateratuak ezarrita eta jarduera sortuta, exekutatu iragarpen produktuaren gomendioa.

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Produktuen gomendioak (aurrebista)** teila.

1. Hautatu **Hasi erabiltzen**.

1. Eman izena ereduari **OOB produktuaren gomendio eredua iragarpena** eta irteerako entitatea **OOBProductRecomendationModelPrediction**.

1. Hautatu **Hurrengoa**.

1. Definitu ereduaren hobespenak:
   - **Produktu kopurua** :**5** zure bezeroei zenbat produktu gomendatu nahi dituzun definitzeko.
   - **Errepikatu erosketak espero dira** :**Bai** aurretik erositako produktuak gomendioan sartzeko.
   - **Begiratu atzera leihoa:** **365 egun** ereduak noraino begiratuko duen atzera definitzeko produktu bat berriro gomendatu aurretik.

   :::image type="content" source="media/product-recommendation-model-preferences.png" alt-text="Produktuaren gomendio-ereduaren eredu-hobespenak.":::

1. Hautatu **Hurrengoa**.

1. urtean **Gehitu erosketen historia** urratsa, hautatu **Gehitu datuak**.

1. Hautatu **SalesOrderLine** eta eCommercePurchases entitatea eta hautatu **Hurrengoa**. Beharrezko datuak automatikoki betetzen dira jardueratik. Hautatu **Gorde** eta gero **Hurrengoa**.

1. Saltatu **Gehitu produktuaren informazioa** eta **Produktu-iragazkiak** urratsak ez ditugulako produktuari buruzko informazio-daturik.

1. urtean **Datuen eguneraketak** urratsa, hautatu **Hilerokoa** egutegi eredurako.

1. Hautatu **Hurrengoa**.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.

## <a name="task-5---review-model-results-and-explanations"></a>5. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Berrikusi [produktuaren gomendio ereduaren azalpenak](predict-transactional-churn.md#view-prediction-results).

## <a name="task-6---create-a-segment-of-high-purchased-products"></a>6. zeregina: sortu erositako produktuen segmentu bat

Eredua exekutatzeak entitate berri bat sortzen du, **Datuak** > **Entitateak** zerrendan agertzen dena. Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.

1. Emaitzen orrian, hautatu **Sortu segmentua**.

1. Sortu arau bat erabiliz **OOBProductRecommendationModelPrediction** entitatea eta definitu segmentua:
   - **Eremua** : Produktuaren ID
   - **Balioa** : Hautatu hiru produktuen ID nagusiak

1. Hautatu **Gorde** eta **Korrika egin** segmentua.

Orain dinamikoki eguneratzen den segmentu bat duzu, bost produktu gomendatuenak erosteko interesa izan dezaketen bezeroak identifikatzen dituena. Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).

> [!TIP]
> Iragarpen eredu baterako segmentu bat ere sor dezakezu hemendik **Segmentuak** orrialdea hautatuz **Berria** eta aukeratzea **Sortu hemendik** > **Adimena**. Informazio gehiagorako, ikus [Sortu segmentu berri bat segmentu azkarrekin](segment-quick.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
