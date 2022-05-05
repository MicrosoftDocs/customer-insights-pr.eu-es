---
title: Power BI konektorea
description: Ikusi nola erabili laguntzailearen estudioa Dynamics 365 Customer Insights konektorea Power BI-n.
ms.date: 07/23/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: e901114703a43b4b4e751e0a93eb4876d7636c00
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642154"
---
# <a name="connector-for-power-bi-preview"></a>Konektorea Power BI-rako (aurrebista)

Sortu zure datuentzako bistaratzeak Power BI Desktop-ekin. Sortu ikuspegi gehiago eta sortu txostenak zure bezeroen datu bateratuekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- Bezeroen profil bateratuak dituzu.
- Bertsioaren azken bertsioa [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) zure ordenagailuan instalatuta dago. [Lortu hauei buruzko informazio gehiago: Power BI Desktop](/power-bi/desktop-what-is-desktop)

## <a name="configure-the-connector-for-power-bi"></a>Konfiguratu konektorea Power BI

1. Power BI Desktop hautatu **Fitxategia** > **Lortu datuak**.

1. Hautatu **Ikusi gehiago** eta bilatu **Dynamics 365 Customer Insights**

1. Hautatu **Konektatu**.

1. **saioa hasi** Customer Insights-erako erabiltzen duzun antolakuntza-kontu bera daukazu eta hautatu **konektatu**.
   > [!NOTE]
   > Urrats honetan adierazten duzun kontua Customer Insights-etik datuak eskuratzeko erabiltzen da eta ez du zertan saioa hasita duzun bera izan behar Power BI. Datuak eskuratzeko erabiltzen den kontua berrezartzeko, ireki Power BI eta joan hona: **Fitxategia** > **Aukerak** > **Ezarpenak** > **Datu-iturburuen ezarpenak**. Datu iturrien zerrendan, hautatu **Dynamics 365 Customer Insights Saioa hasi** eta hautatu **Garbitu baimenak**.  

1. **Nabigatzailea** elkarrizketa-koadroa. sarbidea duzun ingurune guztien zerrenda ikusiko duzu. Zabaldu ingurune bat eta ireki edozein karpeta (entitateak, neurriak, segmentuak, aberasteak). Adibidez, ireki **Entitateak** karpeta, inporta ditzakezun entitate guztiak ikusteko.

   ![Power BI Konektagailuaren nabigatzailea.](media/power-bi-navigator.png "Power BI Konektagailuaren nabigatzailea")

1. Hautatu sartu beharreko entitateen ondoko kontrol laukiak **kargatu**. Hainbat entitate hautatu ahalko dituzu, ingurune anitzetan.

1. Entitateak kargatzen dituzun bitartean, kargatzeko elkarrizketa-koadroa ikusiko duzu. Aukeratutako entitate guztiak kargatu ondoren, Power BI-ren gaitasunak erabil ditzakezu datuak bistaratzeko.

## <a name="large-data-sets"></a>Datu multzo handiak

Customer Insights konektorea Power BI bezeroentzako milioi bat profil dituzten datu multzoetarako lan egiteko diseinatuta dago. Datu multzo handiagoak inportatzeak funtziona dezake, baina denbora asko behar da. Gainera, prozesuak denbora-muga izan dezake Power BI mugak. Informazio gehiagorako, ikus [Power BI: Datu multzo handien gomendioak](/power-bi/admin/service-premium-what-is#large-datasets). 

### <a name="work-with-a-subset-of-data"></a>Lan egin datu azpimultzo batekin

Kontuan hartu zure datuen azpimultzo batekin lan egitea. Adibidez, [segmentuak](segments.md) sor ditzakezu bezeroaren erregistro guztiak Power BI-ra esportatu beharrean.

## <a name="troubleshooting"></a>Arazoak konpontzea

### <a name="customer-insights-environment-doesnt-show-in-power-bi"></a>Customer Insights ingurunea ez da agertzen Power BI-n

Bat baino gehiago dituzten inguruneak [harremana](relationships.md) Customer Insights-en bi entitate berdinen artean definitua ez da eskuragarri egongo Power BI konektorea.

Bikoiztutako harremanak identifikatu eta kendu ditzakezu.

1. Joan **Datuak** > **Harremanak** falta zaizun inguruneari buruz Power BI.
2. Bikoiztutako harremanak identifikatu:
   - Egiaztatu bi entitate berdinen artean erlazio bat baino gehiago definitzen den.
   - Egiaztatu batasun prozesuan sartutako bi entitateen artean sortutako erlaziorik dagoen. Bateratze prozesuan sartutako entitate guztien artean harreman inplizitua dago definituta.
3. Kendu identifikatutako harreman bikoiztuak.

Bikoiztutako harremanak kendu ondoren, saiatu konfiguratzen Power BI konektorea berriro. Ingurumena erabilgarri egon beharko litzateke orain.

### <a name="errors-on-date-fields-when-loading-entities-in-power-bi-desktop"></a>Data-eremuen erroreak entitateak kargatzean Power BI Desktop-en

UUUU/HH/EE bezalako data formatua duten eremuak dituzten entitateak kargatzean, akatsak topatuko dituzu bat ez datozen lokal formatuak direla eta. Bat-etortze hori zurea denean gertatzen da Power BI Desktop fitxategia ingelesez (Estatu Batuak) ez den beste toki batean ezarrita dago, Customer Insights-en data-eremuak AEB formatuan gordetzen direlako.

Power BI Desktop fitxategiak ezarpen lokal bakarra du, datuak berreskuratzean aplikatzen dena. Data-eremu hauek behar bezala interpretatu ahal izateko, ezarri .BPI fitxategiaren lokalizazioa ingelesera (Estatu Batuak). [Ikasi webgune baten eskualdeko eremuak nola aldatu Power BI mahaigaineko fitxategian](/power-bi/fundamentals/supported-languages-countries-regions#choose-the-language-or-locale-of-power-bi-desktop).

[!INCLUDE [footer-include](includes/footer-banner.md)]
