---
title: Power BI konektorea (Aurrebista)
description: Ikusi nola erabili laguntzailearen estudioa Dynamics 365 Customer Insights konektorea Power BI-n.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 656a695b8b3f1ec2b5fbaad69feba7f1f0b73dee
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196655"
---
# <a name="power-bi-connector-preview"></a>Power BI konektorea (Aurrebista)

Sortu bistaratzeak zure datuetarako Microsoft Power BI Mahaigaina. Sortu ikuspegi gehiago eta sortu txostenak zure bezeroen datu bateratuekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- Bezeroen profil bateratuak.
- Bertsioaren azken bertsioa [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) zure ordenagailuan instalatuta dago. [Lortu hauei buruzko informazio gehiago: Power BI Desktop](/power-bi/desktop-what-is-desktop)

## <a name="configure-the-connector-for-power-bi"></a>Konfiguratu konektorea Power BI

1. Power BI Desktop hautatu **Fitxategia** > **Lortu datuak**.

1. Hautatu **Ikusi gehiago** eta bilatu **Dynamics 365 Customer Insights**

1. Hautatu **Konektatu**.

1. **saioa hasi** Customer Insights-erako erabiltzen duzun antolakuntza-kontu bera daukazu eta hautatu **konektatu**.
   > [!NOTE]
   > Urrats honetan adierazten duzun kontua Customer Insights-etik datuak eskuratzeko erabiltzen da eta ez du zertan saioa hasita duzun bera izan behar Power BI. Datuak eskuratzeko erabiltzen den kontua berrezartzeko, ireki Power BI eta joan hona: **Fitxategia** > **Aukerak** > **Ezarpenak** > **Datu-iturburuen ezarpenak**. Datu iturrien zerrendan, hautatu **Dynamics 365 Customer Insights Saioa hasi** eta hautatu **Garbitu baimenak**.  

1. urtean **Nabigatzailea** elkarrizketa-koadroa, ikusi sarbidea duzun ingurune guztien zerrenda. Zabaldu ingurune bat eta ireki edozein karpeta (entitateak, neurriak, segmentuak, aberasteak). Adibidez, ireki **Entitateak** karpeta, inporta ditzakezun entitate guztiak ikusteko.

   :::image type="content" source="media/power-bi-navigator.png" alt-text="Power BI Konektagailuaren nabigatzailea.":::

1. Hautatu sartu beharreko entitateen ondoko kontrol laukiak **kargatu**. Hainbat entitate hautatu ahalko dituzu, ingurune anitzetan.

   Kargatzeko elkarrizketa-koadro bat bistaratuko da zure entitateak kargatzen diren bitartean. Aukeratutako entitate guztiak kargatu ondoren, erabili ahalmenak Power BI datuak ikusteko.

## <a name="large-data-sets"></a>Datu multzo handiak

Customer Insights konektorea Power BI bezeroentzako milioi bat profil dituzten datu multzoetarako lan egiteko diseinatuta dago. Datu-multzo handiagoak inportatzeak funtziona dezake, baina denbora luzea behar du eta denbora-muga iraun dezake Power BI mugak. Informazio gehiagorako, ikus [Power BI: Datu multzo handien gomendioak](/power-bi/admin/service-premium-what-is#large-datasets).

### <a name="work-with-a-subset-of-data"></a>Lan egin datu azpimultzo batekin

Kontuan hartu zure datuen azpimultzo batekin lan egitea. Adibidez, sortu [segmentuak](segments.md) bezeroen erregistro guztiak esportatu beharrean Power BI.

## <a name="troubleshooting"></a>Arazoak konpontzea

### <a name="customer-insights-environment-doesnt-show-in-power-bi"></a>Customer Insights ingurunea ez da agertzen Power BI-n

Bat baino gehiago dituzten inguruneak [harremana](relationships.md) Customer Insights-en bi entitate berdinen artean definitua ez da eskuragarri egongo Power BI konektorea.

Bikoiztutako erlazioak identifikatu eta kentzea.

1. Joan **Datuak** > **Harremanak** falta zaizun inguruneari buruz Power BI.
1. Bikoiztutako harremanak identifikatu:
   - Egiaztatu bi entitate berdinen artean erlazio bat baino gehiago definitzen den.
   - Egiaztatu batasun prozesuan sartutako bi entitateen artean sortutako erlaziorik dagoen. Bateratze prozesuan sartutako entitate guztien artean harreman inplizitua dago definituta.
1. Kendu identifikatutako harreman bikoiztuak.

Bikoiztutako harremanak kendu ondoren, saiatu konfiguratzen Power BI konektorea berriro.

### <a name="errors-on-date-fields-when-loading-entities-in-power-bi-desktop"></a>Data-eremuen erroreak entitateak kargatzean Power BI Desktop-en

MM/DD/YYYY bezalako data-formatua duten eremuak dituzten entitateak kargatzean, akatsak aurki ditzakezu tokiko formatu bat ez datozenengatik. Bat-etortze hori zurea denean gertatzen da Power BI Desktop fitxategia ingelesez (Estatu Batuak) ez den beste toki batean ezarrita dago, Customer Insights-en data-eremuak AEB formatuan gordetzen direlako.

Power BI Desktop fitxategiak ezarpen lokal bakarra du, datuak berreskuratzean aplikatzen dena. Data akatsak konpontzeko, [ezarri .BPI fitxategiaren lokalizazioa](/power-bi/fundamentals/supported-languages-countries-regions#choose-the-language-or-locale-of-power-bi-desktop) ingelesera (Estatu Batuak).

[!INCLUDE [footer-include](includes/footer-banner.md)]
