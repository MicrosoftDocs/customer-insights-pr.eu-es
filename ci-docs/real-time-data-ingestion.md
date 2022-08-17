---
title: Denbora errealeko iragazkiak (aurrebista)
description: Customer Insights-en denbora errealeko gaitasunei buruzko informazio orokorra.
ms.date: 10/27/2020
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: Nils-2m
ms.author: nikeller
manager: shellyha
searchScope:
- ci-system-api-usage
- customerInsights
ms.openlocfilehash: 2652e0868f5cc514ab6df9c150a9183cf95ae589
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9246093"
---
# <a name="real-time-data-ingestion-preview"></a>Denbora errealeko iragazkiak (aurrebista)

Denbora errealeko funtzionalitate hurbilak segundo askoren buruan, bezeroek zure produktuekin edo zerbitzuekin egin dituzten azken elkarrekintzak ikusteko aukera ematen du.

[Programatutako freskatzeak](schedule-refresh.md) erregistro kopuru handia eta hainbat eragiketa konplexu biltzen ditu. Lehenik, datuak datu-iturburutik ateratzen dira. Ondoren, datuak bateratu egiten dira, eta gero informazio gehiagorekin aberasten dira. Prozesu bakoitzeko korrikalari bakoitzak minutu batzuk ordu iraun ditzake.

Denbora errealeko funtzioak berehala ematen ditu kontsumorako datuak, ondorengo eguneratze programatuak datu hauek datu-iturburutik atera arte.

Denbora errealeko eguneratzeek iraungitze-denbora dute eta ondoren datu-iturburu-etik ez dute balioa gehitzen:

- Profilaren eguneraketak lau orduz mantenduko dira
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

- [zeharka](#connect-via-the-dynamics-365-customer-insights-connector), erabiliz [Dynamics 365 Customer Insights konektorea](/connectors/customerinsights/)
- [zuzenean](#connect-directly-to-the-real-time-api), kodearekin

Bi moduek baldintza hauek betetzen dituzte:

- Customer Insights ingurunea
- Bezeroen profil bateratuak
- Konfiguratutako eta exekutatutako jarduerak
- Laguntzailea edo administratzailea zure kontua autentifikatzeko baimenak

## <a name="connect-via-the-dynamics-365-customer-insights-connector"></a>Konektatu Dynamics 365 Customer Insights konektorea

Denbora errealeko APIak dedikatu bateko datuak iren ditzake Power Platform konektorea [Dynamics 365 Customer Insights konektorea](/connectors/customerinsights/), inolako koderik idatzi eta hedatu beharrik gabe.    
Lotzaileak APIaren denbora errealeko ekintzak berak egin ditzake. Lizentzia balioduna behar duzu prima konektoreetarako. Informazio gehiagorako, ikusi [Power Apps eta Power Automate FAQ lizentziak](/power-platform/admin/powerapps-flow-licensing-faq).

- Power Platform [Power Apps eta/edo Power Automate](/connectors/)
- Azure [Logic Aplikazioak](/azure/connectors/apis-list)

Fluxuak sortzeari buruzko xehetasun gehiago lortzeko, ikusi [Power Automate dokumentazioa](/power-automate/).

## <a name="connect-directly-to-the-real-time-api"></a>Konektatu zuzenean denbora errealeko APIarekin

Denbora errealeko gaitasunak erabil ditzakezu zure bideratzea eraikiz eta zuzenean denbora errealeko APIarekin konektatuz.    
Jarduera bat sor dezakezu zure iturburu sistemaren formatuan edo UnifiedActivity formatuan. Lortu formatua API dei bat eginez /api/instantziak/{instanceId}/Kudeatu/entitate/UnifiedActivity.

API honen xehetasunak, parametroak eta erantzunak barne, hemen aurki ditzakezu: **Entitatearen datuak** sekzioan, [Customer Insights APIen erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) atalean. Informazio gehiago lortzeko, ikus [Customer Insights APIekin lan egin](apis.md).

## <a name="understand-your-real-time-usage-with-telemetry"></a>Ulertu zure denbora errealeko erabilera telemetriarekin

Lortu denbora errealeko APIrako eskaeren bolumena eta sistemak izan ditzakeen arazoei buruzko informazioa. [Atzitu denbora errealeko telemetria](system.md#view-api-usage). 


[!INCLUDE [footer-include](includes/footer-banner.md)]
