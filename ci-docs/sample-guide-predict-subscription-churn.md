---
title: Harpidetzaren galera-tasaren iragarpenaren lagin-gida
description: Erabil ezazu lagin-gida hau harpidetzen galera-tasaren iragarpenaren eredua probatzeko.
ms.date: 09/19/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: tutorial
author: m-hartmann
ms.author: wameng
manager: shellyha
searchScope:
- ci-create-prediction
- customerInsights
ms.openlocfilehash: 7e754be9a2cb9450949c6b3667bbd37aa39cf0bf
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9609991"
---
# <a name="subscription-churn-prediction-sample-guide"></a>Harpidetzaren galera-tasaren iragarpenaren lagin-gida

Gida honek iragarpen harpidetza churn-en amaierako adibide bat azalduko dizu lagin-datuak erabiliz. Iragarpen hau probatzea gomendatzen dizugu [ingurune berri batean](manage-environments.md).

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafe eta kafe makinak ekoizten dituen enpresa da. Contoso Kafearen webgunearen bidez saltzen dituzte produktuak. Berriki harpidetza negozioa hasi zuten euren bezeroek aldiro kafea hartzeko. Haien helburua hurrengo hilabeteetan harpidetutako bezeroek harpidetza bertan behera utz dezaketen ulertzea da. Euren bezeroetatik zein den jakitea **litekeena da birrintzea** marketin-ahaleginak aurrezten lagun diezaieke horiek mantentzen zentratuz.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Laguntzaileen baimenak](permissions.md) Customer Insights.

## <a name="task-1---ingest-data"></a>1. zeregina - Datuen sarrera

Berrikusi artikuluak [datuak sartzeari buruz](data-sources.md) eta [batekin konektatzen Power Query datu-iturburu](connect-power-query.md). Informazio honek, oro har, datuak irensten ezagutzen dituzula suposatzen du.

### <a name="ingest-customer-data-from-ecommerce-platform"></a>Sartu bezero-datuak merkataritza elektronikoko plataformatik

1. Sortu Power Query datu-iturburu izeneko bat **merkataritza elektronikoa** eta hautatu **Testua/CSV** konektorea.

1. Idatzi merkataritza elektronikoko kontaktuen URLa: https://aka.ms/ciadclasscontacts.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **Sorrera-data**: Data/ordua/zona

   :::image type="content" source="media/ecommerce-dob-date.PNG" alt-text="Eraldatu jaiotze data datara.":::

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **eCommerceContacts**

1. Gorde datu-iturburua.

### <a name="ingest-customer-data-from-loyalty-schema"></a>Sartu bezero-datuak fideltasun-eskematik

1. Sortu datu-iturburu izeneko bat **LeialtasunEgitasmoa** eta hautatu **Testua/CSV** konektorea.

1. Sartu leialtasun-bezeroen URLa https://aka.ms/ciadclasscustomerloyalty.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **RewardsPoints**: Zenbaki osoa
   - **Sorrera-data**: Data/ordua

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **loyBezeroak**.

1. Gorde datu-iturburua.

### <a name="ingest-subscription-information"></a>Sartu harpidetzari buruzko informazioa

1. Sortu datu-iturburu izeneko bat **Harpidetza Historia** eta hautatu **Testua/CSV** konektorea.

1. Sartu harpidetzen URLa https://aka.ms/ciadchurnsubscriptionhistory.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Harpidetzaren IDa**: osoko zenbakia
   - **Harpidetza kopurua**: Moneta
   - **Harpidetzaren amaiera-data**: Data / Ordua
   - **Harpidetzaren hasiera-data**: Data / Ordua
   - **Transakzioaren data**: Data / Ordua
   - **Errepikakorra da**: Egia / gezurra
   - **Automatikoki berritzen da**: Egia / gezurra
   - **Errepikapen-maiztasuna, hilabetetan**: osoko zenbakia

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **Harpidetza Historia**.

1. Gorde datu-iturburua.

### <a name="ingest-customer-data-from-website-reviews"></a>Sartu bezeroaren datuak webguneen berrikuspenetatik

1. Sortu datu-iturburu izeneko bat **Webgunea** eta hautatu **Testua/CSV** konektorea.

1. Sartu webgunearen berrikuspenetarako URLa https://aka.ms/ciadclasswebsite.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Iritziaren batez besteko balorazioa**: osoko zenbakia
   - **Iritziaren data**: Data

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **webIritziak**.

## <a name="task-2---data-unification"></a>2. zeregina - Datuen bateratzea

Berrikusi artikulua [datuen bateratzeari buruz](data-unification.md). Informazio honek datuen bateratzea orokorrean ezagutzen duzula suposatzen du.

[!INCLUDE [sample-guide-unification](includes/sample-guide-unification.md)]

## <a name="task-3---create-transaction-history-activity"></a>3. ataza - Transakzioen historiako jarduera sortzea

Berrikusi artikulua [bezeroen jarduerei buruz](activities.md). Ondorengo informazioak, oro har, jarduerak sortzen ezagutzen dituzula suposatzen du.

1. Sortu izeneko jarduera bat **Harpidetza Historia** nirekin *Harpidetza* entitatea eta bere gako nagusia, **BezeroarenId**.

1. Sortu arteko harremana *SubscriptionHistory:Harpidetza* eta *eCommerceContacts: eCommerce* rekin **Bezeroaren ID** bi entitateak konektatzeko atzerriko gako gisa.

1. Hautatu **Harpidetza mota** rentzat **GertaeraJarduera** eta **HarpidetzaAmaieraData** rentzat **Denbora-zigilua**.

1. Hautatu **Harpidetza** rentzat **Jarduera mota** eta jardueraren datuak semantikoki mapatzea.

1. Exekutatu jarduera.

1. Gehitu beste jarduera bat eta mapa bere eremuen izenak dagozkien eremuekin:
   - Bezeroaren jardueren entitatea: Reviews:Website
   - Gako nagusia: Website.Reviews.ReviewId
   - Denbora-marka: Website.Reviews.ReviewDate
   - Gertaera (jardueraren izena): Website.Reviews.ActivityTypeDisplay
   - Xehetasunak (zenbatekoa edo balioa): Website.Reviews.ReviewRating

1. Exekutatu jarduera.

## <a name="task-4---configure-the-subscription-churn-prediction"></a>4. zeregina - Konfiguratu harpidetzen galera-tasaren iragarpena

Bezeroen profil bateratuak ezarrita eta jarduera sortuta, exekutatu iragarpen harpidetza sorta. Urrats zehatzak ikusteko, ikus [Harpidetza txanda iragarpen](predict-subscription-churn.md).

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Bezeroen txandakako eredua** teila.

1. Hautatu **Harpidetza** bira motarako eta gero **Hasi**.

1. Eman **OOB eCommerce harpidetzen galera-tasaren iragarpena** izena ereduari eta **OOBSubscriptionChurnPrediction** irteerako entitateari.

1. Definitu ereduaren hobespenak:
   - **Harpidetza amaitu zenetik egun batzuk** :**60** egunak bezero bat birrindutzat hartzen dela adierazteko, harpidetza amaitu eta epe horretan harpidetza berritzen ez badu.
   - **Etorkizuna ikertzeko egunak iragartzeko** :**93** egun, hau da, ereduak zein bezerok iragar ditzaketen aurreikusten duen iraupena. Etorkizunean zenbat eta gehiago begiratu, orduan eta emaitza hain zehatzak izango dira.

   :::image type="content" source="media/model-subs-levers.PNG" alt-text="Hautatu ereduaren hobespenak eta churn definizioa.":::

1. Hautatu **Hurrengoa**.

1. urtean **Beharrezko datuak** urratsa, hautatu **Gehitu datuak** harpidetza historia emateko.

1. Hautatu **Harpidetza** eta SubscriptionHistory entitatea eta hautatu **Hurrengoa**. Beharrezko datuak automatikoki betetzen dira jardueratik. Sakatu **Gorde**.

1. Bezeroaren jarduerak atalean, hautatu **Gehitu datuak**.

1. Adibide honetarako, gehitu web berrikuspen jarduera.

1. Hautatu **Hurrengoa**.

1. urtean **Datuen eguneraketak** urratsa, hautatu **Hilerokoa** egutegi eredurako.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.

## <a name="task-5---review-model-results-and-explanations"></a>5. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Berrikusi harpidetza txandakako ereduaren azalpenak. Informazio gehiagorako, ikus [Ikusi iragarpen emaitzak](predict-subscription-churn.md#view-prediction-results).

## <a name="task-6---create-a-segment-of-high-churn-risk-customers"></a>6. zeregina - Sortu galera-arrisku handiko bezeroen segmentu bat

Eredua exekutatzeak entitate berri bat sortzen du, **Datuak** > **Entitateak** zerrendan agertzen dena. Ereduak sortutako entitatean oinarritutako segmentu berri bat sor dezakezu.

1. Emaitzen orrian, hautatu **Sortu segmentua**.

1. Sortu arau bat erabiliz **OOBsubscriptionChurnPrediction** entitatea eta segmentua definitu:
   - **Eremua** : ChurnScore
   - **Eragilea** : baino handiagoa
   - **Balioa** : 0,6

1. Hautatu **Gorde** eta **Korrika egin** segmentua.

Harpidetza-negozio honen galera-arrisku handiko bezeroak identifikatzen dituen segmentu dinamikoki eguneratua duzu. Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).

> [!TIP]
> Iragarpen eredu baterako segmentu bat ere sor dezakezu hemendik **Segmentuak** orrialdea hautatuz **Berria** eta aukeratzea **Sortu hemendik** > **Adimena**. Informazio gehiagorako, ikus [Sortu segmentu berri bat segmentu azkarrekin](segment-quick.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
