---
title: Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian | Microsoft Docs
description: Datu Gaien eskaerei erantzutea Dynamics 365 Customer Insights.
ms.date: 08/31/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
ms.openlocfilehash: 49251fb46957c4d7ec205b93c9547a3cd380eb11
ms.sourcegitcommit: 624b27bb65a0de1970dc1ac436643b493f0a31cf
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387096"
---
# <a name="data-subject-rights-dsr-requests-under-gdpr"></a>Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian

Europar Batasuneko Datuak Babesteko Araudi Orokorra (GDPR) indarrean dago 2018ko maiatzaren 25az geroztik. Eskubide esanguratsuak ematen dizkie partikularrei beren datuen inguruan. GDPR pertsonen pribatutasun eskubideak babestu eta gaitzea da. Irakurri gehiago Microsoft-ek segurtasunarekin eta betetzearekin duen konpromisoari buruz hemen [Microsoft Trust Center](https://www.microsoft.com/trust-center).

Bezeroek DBAO betekizunak betetzeko konpromisoa dugu. Informazio pertsonala duten datuak ezabatzeko edo esportatzeko eskubidea barne hartzen du, hala nola erabiltzailearen IDak, telefono zenbakiak eta helbide elektronikoak. Administratzaileek datu pertsonalak ezabatzeko edo esportatzeko erabiltzaileen eskaerak ezar ditzakete.

## <a name="responding-to-gdpr-data-subject-delete-requests-for-customer-insights"></a>GDPR datu-gaiak ezabatzeko eskaerak bezeroei buruzko informazioei erantzutea

Erakunde baten bezeroen datu pertsonalak ezabatzeko eskubidea funtsezko babesa da Datuak Babesteko Araudi Orokorrean (DBAO). Datu pertsonalak kentzea barne hartzen ditu datu pertsonal guztiak eta sistemak sortutako erregistroak kentzea, ikuskapenen egunkari informazioa izan ezik.

### <a name="manage-data-subject-delete-requests"></a>Kudeatu datuen gaia ezabatzeko eskaerak

Customer Insights-ek produktuaren barneko esperientzia hauek eskaintzen ditu bezero edo erabiltzaile jakin baten datu pertsonalak ezabatzeko:

- **Kudeatu bezeroen datuak eskatzeko ezabatu**: Customer Insights-en bezeroen datuak Customer Insights-en kanpoko jatorrizko datu iturrietatik ateratzen dira. Egin GDPR ezabatzeko eskaerak jatorrizko datu-iturburu lehendabizi.
- **Kudeatu Customer Insights-eko erabiltzailearen datuak ezabatzeko eskaerak**: Erabiltzaileen datuak Customer Insights-ek sortzen ditu. Egin GDPR ezabatzeko eskaera guztiak Customer Insights-en.

#### <a name="manage-requests-to-delete-customer-data"></a>Kudeatu bezeroen datuak ezabatzeko eskaerak

Customer Insights administratzaile gisa, kendu datu-iturburu atalean ezabatu ziren Customer Insights bezeroen datuak. Egiaztatu GDPR ezabatzeko eskaerak jatorrizko datu-iturburu egin direla.

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.

1. Joan **Datuak** > **Datu-iturburuak**.

1. Ezabatutako bezeroen datuak biltzen dituen zerrendan datu-iturburu bakoitzeko:
   1. Hautatu datu-iturburu eta gero hautatu **Freskatu**.
   1. Begiratu datu-iturburu azpian **Egoera**. Marka egiaztatzeak freskagarria izan dela esan nahi du. Abisu triangelu batek zerbait gaizki joan dela esan nahi du. Abisu triangelua bistaratzen bada, jarri harremanetan D365CI@microsoft.com.

   :::image type="content" source="media/gdpr-data-sources.png" alt-text="DBAO tratamendua bezeroen datuak eskatzeko ezabatu.":::

1. Datu-iturriak arrakastaz freskatu ondoren, exekutatu beherako freskaketak ere. Batez ere, ez baduzu programatuta Customer Insights behin eta berriz eguneratze osoa.

   > [!IMPORTANT]
   > Segmentu estatikoak ez dira freskatze oso batean edo beheranzko freskaketak exekutatzen ezabatzeko eskaera baten ondoren. Bezeroen datuak segmentu estatikoetatik ere kentzen direla ziurtatzeko, birsortu segmentu estatikoak iturburuko datu freskatuekin.

#### <a name="manage-delete-requests-for-user-data"></a>Kudeatu erabiltzailearen datuak ezabatzeko eskaerak

Customer Insights administratzaile gisa, ezabatu Customer Insights erabiltzailearen datuak.

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.

1. Joan **Admin** > **Segurtasuna** > eta hautatu **Erabiltzaileak** fitxa.

1. Hautatu ezabatu nahi dituzun erabiltzaileen kontrol-laukia.

1. Hautatu **Kendu**.

1. Berretsi ezabatzea.

## <a name="responding-to-gdpr-data-subject-export-requests"></a>DBAO datuen subjektuaren esportazio-eskaerei erantzutea

Datuen eramangarritasun-eskubideari esker, pertsona baten datu pertsonalen kopia eska daiteke formatu elektroniko batean ("kontrolatutako egitura, normalean erabilitakoa, makina irakurgarria eta elkarrekin egingarria") beste datu kontroladore bati transmititu ahal izateko.

### <a name="manage-export-and-view-requests"></a>Kudeatu esportazio eta ikusteko eskaerak

Kudeatu bezeroen edo erabiltzaileen datuak esportatzeko eskaerak.

#### <a name="export-customer-data-tenant-admin"></a>Esportatu bezeroen datuak - Beste batzuk (maizterraren kudeatzailea)

Maizter-administratzaile gisa, esportatu bezeroen datuak.

1. Bidali mezu elektroniko bat helbidera D365CI@microsoft.com bezeroaren helbide elektronikoa eskaeran zehaztuz. Customer Insights taldeak mezu elektroniko bat bidaliko du erregistratutako maizter kudeatzaileko helbide elektronikora, datuak esportatzeko berrespena eskatuko du.
2. Onartu eskatutako bezeroari datuak esportatzeko baieztapena.
3. Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.

#### <a name="export-user-data-tenant-admin"></a>Esportatu erabiltzailearen datuak (maizterraren kudeatzailea)

Maizter-administratzaile gisa, esportatu erabiltzailearen datuak.

1. Bidali mezu elektroniko bat helbidera D365CI@microsoft.com erabiltzailearen helbide elektronikoa eskaeran zehaztuz. Customer Insights taldeak mezu elektroniko bat bidaltzen dio erregistratutako maizterraren administratzaile helbidera, datuak esportatzeko berrespena eskatuz.
1. Onartu eskatutako erabiltzailearen datuak esportatzeko baieztapena.
1. Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.

## <a name="data-deletion-handling-in-dynamics-365-customer-insights"></a>Datuak ezabatzeko kudeaketan Dynamics 365 Customer Insights

Datuak ezabatzen dira (datuen partizioak eta datu-instantaneak) datu-partizioak eta datu-instantaneak 30 egun baino gehiago inaktibo egonez gero, hau da, datu-partizio eta argazki berri batekin ordezkatu dira datu-iturburuen freskagarri baten bidez.

Ez dira datu eta argazki guztiak ezabatzen. Datu-partizioa eta datuen argazki berriena aktibo daude Customer Insights-en erabiltzen direlako. Datu berrienei dagokienez, berdin du azken 30 egunetan datu-iturriak freskatu ez izanak.

[!INCLUDE [footer-include](includes/footer-banner.md)]
