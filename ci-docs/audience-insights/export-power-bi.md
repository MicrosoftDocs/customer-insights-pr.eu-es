---
title: Power BI konektorea
description: Ikusi nola erabili laguntzailearen estudioa Dynamics 365 Customer Insights konektorea Power BI-n.
ms.date: 09/21/2020
ms.reviewer: sthe
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 0607a4644ac7d7beb19e4faecf012efcd197d48c
ms.sourcegitcommit: 0260ed244b97c2fd0be5e9a084c4c489358e8d4f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/18/2021
ms.locfileid: "5477073"
---
# <a name="connector-for-power-bi-preview"></a>Konektorea Power BI-rako (aurrebista)

Sortu zure datuentzako bistaratzeak Power BI Desktop-ekin. Sortu ikuspegi gehiago eta sortu txostenak zure bezeroen datu bateratuekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- Bezeroen profil bateratuak dituzu.
- Bertsioaren azken bertsioa [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) zure ordenagailuan instalatuta dago. [Lortu hauei buruzko informazio gehiago: Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)

## <a name="configure-the-connector-for-power-bi"></a>Konfiguratu konektorea Power BI

1. Power BI Desktop hautatu **Fitxategia** > **Lortu datuak**.

1. Hautatu **Ikusi gehiago** eta bilatu **Dynamics 365 Customer Insights**

1. Hautatu **Konektatu**.

1. **saioa hasi** Customer Insights-erako erabiltzen duzun antolakuntza-kontu bera daukazu eta hautatu **konektatu**.
   > [!NOTE]
   > Urrats honetan adierazten duzun kontua Customer Insights-etik datuak eskuratzeko erabiltzen da eta ez du zertan saioa hasita duzun bera izan behar Power BI. Datuak eskuratzeko erabiltzen den kontua berrezartzeko, ireki Power BI eta joan hona: **Fitxategia** > **Aukerak** > **Ezarpenak** > **Datu-iturburuen ezarpenak**. Datu iturrien zerrendan, hautatu **Dynamics 365 Customer Insights Saioa hasi** eta hautatu **Garbitu baimenak**.  

1. **Nabigatzailea** elkarrizketa-koadroa. sarbidea duzun ingurune guztien zerrenda ikusiko duzu. Zabaldu ingurune bat eta ireki edozein karpeta (entitateak, neurriak, segmentuak, aberasteak). Adibidez, ireki **Entitateak** karpeta, inporta ditzakezun entitate guztiak ikusteko.

   ![Power BI Konektagailuaren nabigatzailea](media/power-bi-navigator.png "Power BI Konektagailuaren nabigatzailea")

1. Hautatu sartu beharreko entitateen ondoko kontrol laukiak **kargatu**. Hainbat entitate hautatu ahalko dituzu, ingurune anitzetan.

1. Entitateak kargatzen dituzun bitartean, kargatzeko elkarrizketa-koadroa ikusiko duzu. Aukeratutako entitate guztiak kargatu ondoren, Power BI-ren gaitasunak erabil ditzakezu datuak bistaratzeko.

## <a name="large-data-sets"></a>Datu multzo handiak

Customer Insights konektorea Power BI bezeroentzako milioi bat profil dituzten datu multzoetarako lan egiteko diseinatuta dago. Datu multzo handiagoak inportatzeak funtziona dezake, baina denbora asko behar da. Gainera, prozesuak denbora-muga izan dezake Power BI mugak. Informazio gehiagorako, ikus [Power BI: Datu multzo handien gomendioak](https://docs.microsoft.com/power-bi/admin/service-premium-what-is#large-datasets). 

### <a name="work-with-a-subset-of-data"></a>Lan egin datu azpimultzo batekin

Kontuan hartu zure datuen azpimultzo batekin lan egitea. Adibidez, [segmentuak](segments.md) sor ditzakezu bezeroaren erregistro guztiak Power BI-ra esportatu beharrean.

## <a name="troubleshooting"></a>Arazoak konpontzea

### <a name="customer-insights-environment-doesnt-show-in-power-bi"></a>Customer Insights ingurunea ez da agertzen Power BI-n

Bat baino gehiago dituzten inguruneak [erlazioa](relationships.md) ikusleen estatistiketan bi entitate berdinen artean definitutakoak ez dira erabilgarri egongo Power BI konektorea.

Bikoiztutako harremanak identifikatu eta kendu ditzakezu.

1. Ikusleen ikuspegietan, joan hona **Datuak** > **Erlazioak** falta zaizun inguruneari buruz Power BI-n.
2. Bikoiztutako harremanak identifikatu:
   - Egiaztatu bi entitate berdinen artean erlazio bat baino gehiago definitzen den.
   - Egiaztatu batasun prozesuan sartutako bi entitateen artean sortutako erlaziorik dagoen. Bateratze prozesuan sartutako entitate guztien artean harreman inplizitua dago definituta.
3. Kendu identifikatutako harreman bikoiztuak.

Bikoiztutako harremanak kendu ondoren, saiatu konfiguratzen Power BI konektorea berriro. Ingurumena erabilgarri egon beharko litzateke orain.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

