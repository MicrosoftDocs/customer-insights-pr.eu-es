---
title: Bezeroaren bizi-iraupenaren balioaren iragarpenaren lagin gida
description: Erabili lagin gida hau bezeroaren bizi-iraupenaren balio osorako iragarpen modeloa probatzeko.
ms.date: 09/15/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: tutorial
author: yashlundia
ms.author: yalundia
manager: shellyha
ms.openlocfilehash: fec43b279326daa17fb179181f5e310c99d48bb7
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9609623"
---
# <a name="customer-lifetime-value-clv-prediction-sample-guide"></a>Bezeroaren bizi-iraupenaren balioaren iragarpenaren lagin gida

Gida honek Customer lifetime value (CLV) iragarpen Customer Insights-en amaieratik amaierako adibide bat eskaintzen dizu lagin-datuak erabiliz. Iragarpen hau probatzea gomendatzen dizugu [ingurune berri batean](manage-environments.md).

## <a name="scenario"></a>Egoera

Contoso kalitate handiko kafe eta kafe makinak ekoizten dituen enpresa da. Contoso Kafearen webgunearen bidez saltzen dituzte produktuak. Konpainiak bezeroek hurrengo 12 hilabeteetan sor dezaketen balioa (diru-sarrerak) ulertu nahi du. Datozen 12 hilabeteetan bezeroek espero duten balioa ezagutzeak balio handiko bezeroenganako marketin ahalegina bideratzen lagunduko die.

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [kolaboratzaile-baimenak](permissions.md).

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

1. **Gorde** datu-iturburua.

### <a name="ingest-online-purchase-data"></a>Sartu sareko erosketen datuak

1. Gehitu beste datu multzo bat **merkataritza elektronikoa** datu-iturburu berera. Aukeratu **Testua/CSV** konektorea berriro.

1. Idatzi **sareko erosketen** datuen URLa: https://aka.ms/ciadclassonline.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **PurchasedOn**: Data/ordua
   - **TotalPrice**: Moneta

1. urtean **Izena** alboko paneleko eremuan, izena aldatu zure datu-iturburu **eCommerceErosketak**.

1. **Gorde** datu-iturburua.

### <a name="ingest-customer-data-from-loyalty-schema"></a>Sartu bezero-datuak fideltasun-eskematik

1. Sortu datu-iturburu izeneko bat **LeialtasunEgitasmoa** eta hautatu **Testua/CSV** konektorea.

1. Sartu leialtasun-bezeroen URLa https://aka.ms/ciadclasscustomerloyalty.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **Jaioteguna**: Data
   - **RewardsPoints**: Zenbaki osoa
   - **Sorrera-data**: Data/ordua

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **loyBezeroak**.

1. **Gorde** datu-iturburua.

### <a name="ingest-customer-data-from-website-reviews"></a>Sartu bezeroaren datuak webguneen berrikuspenetatik

1. Sortu datu-iturburu izeneko bat **Webgunea** eta hautatu **Testua/CSV** konektorea.

1. Sartu webgunearen berrikuspenetarako URLa https://aka.ms/CI-ILT/WebReviews.

1. Datuak editatzen dituzun bitartean, hautatu **Eraldatu** eta gero **Erabili lehen errenkada goiburu gisa**.

1. Eguneratu jarraian zerrendatutako zutabeen datu motak:
   - **ReviewRating**: zenbaki hamartarra
   - **Iritziaren data**: Data

1. urtean **Izena** eskuineko paneleko eremuan, aldatu izena zure datu-iturburu **Iritziak**.

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

1. Gehitu beste jarduera bat eta mapa bere eremuen izenak dagozkien eremuekin:
   - **Jarduera-entitatea** : Iritziak:Webgunea
   - **Lehen gakoa** : ReviewId
   - **Denbora-zigilua** : BerrikuspenData
   - **Ekitaldi-jarduera** : ActivityTypeDisplay
   - **Xehetasun gehigarria** : BerrikuspenBalorazioa
   - **Jarduera mota** : Berrikuspena

1. Exekutatu jarduera.

## <a name="task-4---configure-customer-lifetime-value-prediction"></a>4. ataza - Konfiguratu bezeroaren bizi-iraupenaren balioaren iragarpena

Bezeroen profil bateratuak ezarrita eta sortutako jarduerarekin, exekutatu bezeroaren bizitzako balioa (CLV) iragarpen. Urrats zehatzak ikusteko, ikus [Bezeroaren bizitza osorako balioa iragarpen](predict-customer-lifetime-value.md).

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Bezeroaren bizitzako balioa** teila.

1. Hautatu **Hasi erabiltzen**.

1. Eman izen hau ereduari: **OOB eCommerce CLV iragarpena** eta hau irteerako entitateari: **OOBeCommerceCLVPrediction**.

1. Definitu ereduaren hobespenak:
   - **iragarpen denbora-tartea** :**12 hilabete edo urtebete** etorkizunean noraino aurreikusteko CLV definitzeko.
   - **Bezero aktiboak** :**Utzi ereduak erosketa-tartea kalkulatzea** hau da, bezero batek aktibotzat jotzeko gutxienez transakzio bat izan behar duen denbora-tartea.
   - **Balio handiko bezeroa** : eskuz definitzeko balio handiko bezeroak gisa **bezero aktiboen % 30 nagusiak**.

    :::image type="content" source="media/clv-model-preferences.png" alt-text="Lehentasun urratsa CLV ereduaren esperientzia gidatuan.":::

1. Hautatu **Hurrengoa**.

1. **Beharrezko datuak** urratsean, hautatu **Gehitu datuak** transakzioen historiaren datuak emateko.

    :::image type="content" source="media/clv-model-required.png" alt-text="Gehitu beharrezko datuen urratsa CLV eredurako esperientzia gidatuan.":::

1. Hautatu **SalesOrderLine** eta eCommercePurchases entitatea eta hautatu **Hurrengoa**. Beharrezko datuak automatikoki betetzen dira jardueratik. Hautatu **Gorde** eta gero **Hurrengoa**.

1. The **Datu gehigarriak (aukerakoa)** urratsak bezeroen jarduera-datu gehiago gehitzeko aukera ematen dizu bezeroen interakzioei buruzko informazio gehiago lortzeko. Adibide honetarako, hautatu **Gehitu datuak** eta gehitu web berrikuspen jarduera.

1. Hautatu **Hurrengoa**.

1. urtean **Datuen eguneraketak** urratsa, hautatu **Hilerokoa** egutegi eredurako.

1. Hautatu **Hurrengoa**.

1. Xehetasun guztiak aztertu ondoren, hautatu **Gorde eta Exekutatu**.

## <a name="task-5---review-model-results-and-explanations"></a>5. zeregina - Berrikusi ereduen emaitzak eta azalpenak

Ereduak datuen prestakuntza eta puntuazioa osatuko ditu. Berrikusi [CLV ereduaren emaitzak eta azalpenak](predict-customer-lifetime-value.md#view-prediction-results).

## <a name="task-6---create-a-segment-of-high-value-customers"></a>6. ataza - Sortu balio handiko bezeroen segmentu bat

Eredua exekutatzeak entitate berri bat sortzen du, **Datuak** > **Entitateak** zerrendan agertzen dena. Ereduak sortutako entitatean oinarrituta bezeroen segmentu berri bat sor dezakezu.

1. Emaitzen orrian, hautatu **Sortu segmentua**.

1. Sortu arau bat erabiliz **OOBeCommerceCLVPiragarpena** entitatea eta segmentua definitu:
   - **Eremua** : CLVScore
   - **Eragilea** : baino handiagoa
   - **Balioa** : 1500

1. Hautatu **Gorde** eta **Korrika egin** segmentua.

Datozen 12 hilabeteetan $1500ko diru sarrera baino gehiago sortuko dituztela aurreikusten duten bezeroak identifikatzen dituen segmentu bat duzu orain. Segmentu hau dinamikoki eguneratzen da datu gehiago irensten badira. Informazio gehiagorako, ikusi [Sortu eta kudeatu segmentuak](segments.md).

> [!TIP]
> Iragarpen eredu baterako segmentu bat ere sor dezakezu hemendik **Segmentuak** orrialdea hautatuz **Berria** eta aukeratzea **Sortu hemendik** > **Adimena**. Informazio gehiagorako, ikus [Sortu segmentu berri bat segmentu azkarrekin](segment-quick.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
