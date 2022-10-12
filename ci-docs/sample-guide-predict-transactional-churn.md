---
title: Transakzioen galera-tasaren iragarpenari buruzko adibide-gida
description: Erabili gida hau erabiltzeko prest dagoen transakzioen galera-tasaren iragarpen-eredua probatzeko.
ms.date: 09/19/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 0ccc32b6e5e96adf6f2fa8c6d52960a07d1513f3
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9609669"
---
# <a name="transactional-churn-prediction-sample-guide"></a>Transakzioen galera-tasaren iragarpenari buruzko adibide-gida

Gida honek lagin-datuak erabiliz iragarpen transakzio churn-en amaierako adibide bat azalduko dizu. Iragarpen hau probatzea gomendatzen dizugu [ingurune berri batean](manage-environments.md).

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafe eta kafe makinak ekoizten dituen enpresa da. Contoso Kafearen webgunearen bidez saltzen dituzte produktuak. Enpresaren helburua da jakitea egunerokotasunean bere produktuak erosten dituzten bezeroetako nortzuk utziko dioten bezero aktibo izateari datozen 60 egunetan. Zein bezero **galtzeko arriskua** dagoen jakiteak marketinarekin erlazionatutako ahalegina bideratzen lagun diezaioke enpresari, arreta bezero horiengan jarrita.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [kolaboratzaile-baimenak](permissions.md).

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Berrikusi artikuluak [datuak sartzeari buruz](data-sources.md) eta [batekin konektatzen Power Query datu-iturburu](connect-power-query.md). Informazio honek, oro har, datuak irensten ezagutzen dituzula suposatzen du.

### <a name="ingest-customer-data-from-ecommerce-platform"></a>Sartu bezero-datuak merkataritza elektronikoko plataformatik

1. Sortu datu-iturburu izeneko bat **merkataritza elektronikoa** eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscontacts.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **Jaioteguna**: Data
   - **Sorrera-data**: Data/ordua/zona

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Bihurtu jaioteguna data.":::

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **eCommerceContacts**

1. Gorde datu-iturburua.

### <a name="ingest-online-purchase-data"></a>Sartu sareko erosketen datuak

1. Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera. Aukeratu **Testua/CSV** konektorea berriro.

1. Sartu lineako erosketen datuen URLa https://aka.ms/ciadclassonline.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **PurchasedOn**: Data/ordua
   - **TotalPrice**: Moneta

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **eCommerceErosketak**.

1. Gorde datu-iturburua.

### <a name="ingest-customer-data-from-loyalty-schema"></a>Sartu bezero-datuak fideltasun-eskematik

1. Sortu datu-iturburu izeneko bat **LeialtasunEgitasmoa** eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscustomerloyalty.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:

   - **Jaioteguna**: Data
   - **RewardsPoints**: Zenbaki osoa
   - **Sorrera-data**: Data/ordua

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **loyBezeroak**.

1. Gorde datu-iturburua.

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

## <a name="task-4---configure-transaction-churn-prediction"></a>4. zeregina - Konfiguratu transakzioen galera-tasaren iragarpena

Bezeroen profil bateratuak ezarrita eta jarduerarekin, exekutatu iragarpen transakzioen txanda.

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Bezeroen txandakako eredua**.

1. Hautatu **Transakzionalak** bira motarako eta gero **Hasi**.

1. Eman **OOB eCommerce transakzioen galera-tasaren iragarpena** izena ereduari eta **OOBeCommerceChurnPrediction** irteerako entitateari.

1. Hautatu **Hurrengoa**.

1. Definitu ereduaren hobespenak:

   - **iragarpen leihoa** :**60** egunak etorkizunean bezeroen txanda aurreikusi nahi dugun definitzeko.

   - **Churn definizioa** :**60** egunak erosketarik gabeko iraupena adierazteko, eta ondoren bezeroa birrindutzat hartzen da.

     :::image type="content" source="media/model-levers.PNG" alt-text="Hautatu ereduaren hobespenak iragarpen Leihoa eta Churn Definizioa.":::

1. Hautatu **Hurrengoa**.

1. Aukeratu **Erosketen historia (beharrezkoa)** eta hautatu **Gehitu datuak** erosketen historiarako.

1. Hautatu **SalesOrderLine** eta eCommercePurchases entitatea eta hautatu **Hurrengoa**. Beharrezko datuak automatikoki betetzen dira jardueratik. Hautatu **Gorde** eta gero **Hurrengoa**.

   :::image type="content" source="media/model-purchase-join.PNG" alt-text="Sartu merkataritza elektronikoko entitateetan.":::

1. Saltatu **Datu gehigarriak (aukerakoa)** urratsa.

1. urtean **Datuen eguneraketak** urratsa, hautatu **Hilerokoa** egutegi eredurako.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.

## <a name="task-5---review-model-results-and-explanations"></a>5. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Berrikusi churn-ereduaren azalpenak. Informazio gehiagorako, ikus [Ikusi iragarpen emaitzak](predict-transactional-churn.md#view-prediction-results).

## <a name="task-6---create-a-segment-of-high-churn-risk-customers"></a>6. zeregina - Sortu galera-arrisku handiko bezeroen segmentu bat

Ekoizpen-eredua exekutatzen entitate berri bat sortzen da, zeina zerrendatuta dagoen **Datuak** > **Entitateak**. Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.

1. Emaitzen orrian, hautatu **Sortu segmentua**.

1. Sortu arau bat erabiliz **OOBeCommerceChurnPrediction** entitatea eta segmentua definitu:
   - **Eremua** : ChurnScore
   - **Eragilea** : baino handiagoa
   - **Balioa** : 0,6

1. Hautatu **Gorde** eta **Korrika egin** segmentua.

Orain dinamikoki eguneratzen den segmentu bat duzu, arrisku handiko bezeroak identifikatzen dituena. Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).

> [!TIP]
> Iragarpen eredu baterako segmentu bat ere sor dezakezu hemendik **Segmentuak** orrialdea hautatuz **Berria** eta aukeratzea **Sortu hemendik** > **Adimena**. Informazio gehiagorako, ikus [Sortu segmentu berri bat segmentu azkarrekin](segment-quick.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
