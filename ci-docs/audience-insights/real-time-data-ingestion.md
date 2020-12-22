---
title: Denbora errealean datuak sartzea eta mugak
description: Hartzaileen xehetasunetako denbora errealeko gaitasunen inguruko informazio orokorra.
ms.date: 10/27/2020
ms.reviewer: nikeller
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: b00a72e6a67e33c8e70ccc6139c5e62020f9d3e1
ms.sourcegitcommit: b50c754481d0af6d0cf4b550775d7b31d95846ef
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/06/2020
ms.locfileid: "4689160"
---
# <a name="real-time-data-ingestion-preview"></a>Denbora errealeko iragazkiak (aurrebista)

Denbora errealeko funtzionalitate hurbilak segundo askoren buruan, bezeroek zure produktuekin edo zerbitzuekin egin dituzten azken elkarrekintzak ikusteko aukera ematen du.

[Programatutako freskatzeak](system.md#schedule-tab) erregistro kopuru handia eta hainbat eragiketa konplexu biltzen ditu. Lehenik, datuak datu-iturburutik ateratzen dira. Ondoren, datuak bateratu egiten dira, eta gero informazio gehiagorekin aberasten dira. Prozesu bakoitzeko korrikalari bakoitzak minutu batzuk ordu iraun ditzake.

Denbora errealeko funtzioak berehala ematen ditu kontsumorako datuak, ondorengo eguneratze programatuak datu hauek datu-iturburutik atera arte.

Denbora errealeko eguneratzeek iraungitze-denbora dute eta ondoren datu-iturburu-etik ez dute balioa gehitzen:

- Profilaren eguneratzeak 4 orduz mantenduko dira
- Jarduerak 30 egunez mantenduko dira

Balio hauek API dei parametroak alda ditzakezu. Zure datu iturriak zure egia iturri izaten jarraituko dutela ziurtatzea dute helburu. Denbora errealeko eguneratzeak denbora gehiagoz sartzea nahi baduzu, datu-iturburu batean gehitu behar dituzu hurrengo programatutako freskatzean atera ahal izateko.

## <a name="real-time-update-of-the-unified-customer-profile-fields"></a>Bezeroaren profil bateratutako eremuak eguneratzeko denbora erreala

Eguneratutako profilak bezeroaren txartelaren ikuspegian edo beste edozein bistaratzetan agertuko dira segundo gutxiren buruan.

Denbora errealeko eragiketak datuak bateratu ondoren gertatu direlako, bateratutako bezeroen profiletara soilik aplikatzen dira. Horrenbestez, denbora errealeko profilaren aldaketek ez dituzte eguneratuko neurriak, segmentuen kideak edo aberastasunak.

### <a name="limitations"></a>Mugak

- Bezeroen profilak eguneratu daitezke, baina ez dira sortu edo ezabatu.
- Eguneratzeak denbora errealeko kanpoko sistemetara esportatu, adibidez Power BI, momentuz ezinezkoa da.

## <a name="real-time-creation-of-activities"></a>Denbora errealean jarduerak sortzea

Denbora errealeko APIari esker, zure iturburuko sistematik (iturburuko erregistro indibiduala) jarduera berri bat argitara dezakezu bezeroaren profil bateratura. Jarduera berria bateratutako bezero gisa egongo da eskuragarri bezeroaren profil kronologikoan segundotan. Kronologia bezeroaren txartelaren ikuspegian edo konfiguratu duzun beste edozein kronologiaren integrazioan ikus dezakezu.

> [!NOTE]
>
> - Jarduerak ukaezinak dira. Sortutakoan ez dira aldatzen.
> - Une honetan, segmentuak eta neurriak ez dira eguneratuko jarduera berrian oinarrituta.
> - Denbora errealeko APIaren bidez soilik gehitzen diren jarduerak ez dira esportazioen zati eta ez dira PowerBIn agertuko.

Denbora errealeko APIarekin konektatzeko bi modu daude:

- [zeharka](#connect-via-the-dynamics-365-customer-insights-connector), erabiliz [Dynamics 365 Customer Insights konektorea](https://docs.microsoft.com/connectors/customerinsights/)
- [zuzenean](#connect-directly-to-the-real-time-api), kodearekin

Bi moduek baldintza hauek betetzen dituzte:

- Customer Insights ingurunea
- Bezeroen profil bateratuak
- Konfiguratutako eta exekutatutako jarduerak
- Laguntzailea edo administratzailea zure kontua autentifikatzeko baimenak

## <a name="connect-via-the-dynamics-365-customer-insights-connector"></a>Konektatu Dynamics 365 Customer Insights konektorea

Denbora errealeko APIak dedikatu bateko datuak iren ditzake Power Platform konektorea [Dynamics 365 Customer Insights konektorea](https://docs.microsoft.com/connectors/customerinsights/), inolako koderik idatzi eta hedatu beharrik gabe.    
Lotzaileak APIaren denbora errealeko ekintzak berak egin ditzake. Lizentzia balioduna behar duzu prima konektoreetarako. Informazio gehiagorako, ikusi [Power Apps eta Power Automate FAQ lizentziak](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq).

- Power Platform [Power Apps eta/edo Power Automate](https://docs.microsoft.com/connectors/)
- Azure [Logic Aplikazioak](https://docs.microsoft.com/azure/connectors/apis-list)

Fluxuak sortzeari buruzko xehetasun gehiago lortzeko, ikusi [Power Automate dokumentazioa](https://docs.microsoft.com/power-automate/).

## <a name="connect-directly-to-the-real-time-api"></a>Konektatu zuzenean denbora errealeko APIarekin

Denbora errealeko gaitasunak erabil ditzakezu zure bideratzea eraikiz eta zuzenean denbora errealeko APIarekin konektatuz.    
Jarduera bat sor dezakezu zure iturburu sistemaren formatuan edo UnifiedActivity formatuan. Lortu formatua API dei bat eginez /api/instantziak/{instanceId}/Kudeatu/entitate/UnifiedActivity.

API honen xehetasunak, parametroak eta erantzunak barne, hemen aurki ditzakezu: **Entitatearen datuak** sekzioan, [Customer Insights APIen erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) atalean. Informazio gehiago lortzeko, ikus [Customer Insights APIekin lan egin](apis.md).

## <a name="understand-your-real-time-usage-with-telemetry"></a>Ulertu zure denbora errealeko erabilera telemetriarekin

Lortu denbora errealeko APIrako eskaeren bolumena eta sistemak izan ditzakeen arazoei buruzko informazioa. Ahal duzu [sartu denbora errealeko telemetriara](system.md#api-usage-tab) joanda **admin** > **Sistema** > **APIaren erabilera**. **Eragiketak** taulan, denbora errealeko metodoak erabiltzen dituzten API eragiketetarako errenkadek botoi bat dute denbora errealeko APIaren erabilera ikusteko. Botoia sinbolo binokular batekin bistaratzen da. Aukeratu botoia APIaren denbora errealeko uneko inguruneko erabilerari buruzko xehetasunak dituen alboko panela irekitzeko.

Erabili **Taldeka** hautatzailea zure denbora errealean elkarreraginak nola aurkeztu hobeto aukeratzeko azken 24 orduetatik azken 30 egunetara bitarteko denbora-lerro batean. Datuak API metodoaren, entitatearen izen kualifikatua (irenstutako entitatea), sortutako (gertaeraren iturria), emaitza (arrakasta edo hutsegitea) edo errore kodeak arabera talka ditzakezu. Datuak historia-taula gisa eta taula gisa eskuragarri daude.
