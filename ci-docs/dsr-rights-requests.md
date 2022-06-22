---
title: Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian | Microsoft Docs
description: Datu Gaien eskaerei erantzutea Dynamics 365 Customer Insights.
ms.date: 05/23/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
ms.openlocfilehash: c71305ab835b0f4f75adcce716e795959f898e47
ms.sourcegitcommit: 8e9f0a9693fd8d91ad0227735ff03688fef5406f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/10/2022
ms.locfileid: "8947353"
---
# <a name="data-subject-rights-dsr-requests-under-gdpr"></a>Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian

Europar Batasuneko Datuak Babesteko Araudi Orokorra (GDPR) indarrean dago 2018ko maiatzaren 25az geroztik. Eskubide esanguratsuak ematen dizkie partikularrei beren datuen inguruan. GDPR pertsonen pribatutasun eskubideak babestu eta gaitzea da. Microsoft-ek segurtasunarekin eta betetzearekin duen konpromisoari buruzko informazio gehiago irakur dezakezu hemen [Microsoft Trust Center](https://www.microsoft.com/trust-center).

Bezeroek DBAO betekizunak betetzeko konpromisoa dugu. Informazio pertsonala barne hartzen duten datuak ezabatu eta esportatzeko eskubidea biltzen du, hala nola erabiltzaile IDak, telefono zenbakiak eta helbide elektronikoak. Administratzaileek datu pertsonalak ezabatzeko edo esportatzeko erabiltzaileen eskaerak ezar ditzakete.

## <a name="dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights

### <a name="responding-to-gdpr-data-subject-delete-requests-for-dynamics-365-customer-insights"></a>DBAO datuen subjektuaren ezabatze-eskaerei erantzutea Dynamics 365 Customer Insights-erakos

Erakunde baten bezeroen datu pertsonalak ezabatzeko eskubidea funtsezko babesa da Datuak Babesteko Araudi Orokorrean (DBAO). Datu pertsonalak kentzea barne hartzen ditu datu pertsonal guztiak eta sistemak sortutako erregistroak kentzea, ikuskapenen egunkari informazioa izan ezik.

#### <a name="manage-data-subject-delete-requests"></a>Kudeatu datuen gaia ezabatzeko eskaerak

Customer Insights-ek produktuaren barneko esperientzia hauek eskaintzen ditu bezero edo erabiltzaile jakin baten datu pertsonalak ezabatzeko:

- **Kudeatu bezeroen datuak eskatzeko ezabatu**: Customer Insights-en bezeroen datuak Customer Insights-en kanpoko jatorrizko datu iturrietatik ateratzen dira. DBAO ezabatzeko eskaera guztiak jatorrizko datu-iturburu-en egin behar dira.
- **Kudeatu Customer Insights-eko erabiltzailearen datuak ezabatzeko eskaerak**: Erabiltzaileen datuak Customer Insights-ek sortzen ditu. DBAO ezabatzeko eskaera guztiak Customer Insights zerbitzuan egin behar dira.

##### <a name="manage-requests-to-delete-customer-data"></a>Kudeatu bezeroen datuak ezabatzeko eskaerak

Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake datu-iturburu-en ezabatu diren bezeroen datuak kentzeko:

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.
2. Joan **Datuak** > **Datu iturriak**
3. Ezabatutako bezeroen datuak biltzen dituen zerrendan datu-iturburu bakoitzeko:
   1. Hautatu elipsi bertikala (&vellip;) eta gero hautatu **Freskatu**.
   2. Begiratu datu-iturburu azpian **Egoera**. Marka egiaztatzeak freskagarria izan dela esan nahi du. Abisu triangelu batek zerbait gaizki joan dela esan nahi du. Abisu triangelua bistaratzen bada, jarri harremanetan D365CI@microsoft.com.

> [!div class="mx-imgBorder"]
> ![DBAO tratamendua bezeroen datuak eskatzeko ezabatu.](media/gdpr-data-sources.png "DBAO tratamendua bezeroen datuak eskatzeko ezabatu")

##### <a name="manage-delete-requests-for-user-data"></a>Kudeatu erabiltzailearen datuak ezabatzeko eskaerak

Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake Customer Insights erabiltzailearen datuak ezabatzeko:

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.
2. Joan **Admin** > **Segurtasuna** > **Baimenak**.
3. Hautatu ezabatu nahi dituzun erabiltzailearen kontrol-laukiak.
4. Hautatu **Kendu**.

### <a name="responding-to-gdpr-data-subject-export-requests"></a>DBAO datuen subjektuaren esportazio-eskaerei erantzutea

Datuak Babesteko Erregelamendu Orokorrerako (GDPR) zure bidaian zurekin lankidetzan aritzeko gure konpromisoaren baitan, dokumentazioa garatu dugu, interesdunen eskaerei erantzuten laguntzeko.

#### <a name="manage-export-and-view-requests"></a>Kudeatu esportazio eta ikusteko eskaerak

Datuen eramangarritasun-eskubideari esker, pertsona baten datu pertsonalen kopia eska daiteke formatu elektroniko batean ("kontrolatutako egitura, normalean erabilitakoa, makina irakurgarria eta elkarrekin egingarria") beste datu kontroladore bati transmititu ahal izateko.

##### <a name="export-customer-data-tenant-admin"></a>Esportatu bezeroen datuak - Beste batzuk (maizterraren kudeatzailea)

Maizter administratzaileak urrats hauek jarraitzen ditu datuak esportatzeko:

1. Bidali mezu elektroniko bat helbidera D365CI@microsoft.com bezeroaren helbide elektronikoa eskaeran zehaztuz. Customer Insights taldeak mezu elektroniko bat bidaliko du erregistratutako maizter kudeatzaileko helbide elektronikora, datuak esportatzeko berrespena eskatuko du.
2. Onartu eskatutako bezeroari datuak esportatzeko baieztapena.
3. Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.

##### <a name="export-user-data-tenant-admin"></a>Esportatu erabiltzailearen datuak (maizterraren kudeatzailea)

1. Bidali mezu elektroniko bat helbidera D365CI@microsoft.com erabiltzailearen helbide elektronikoa eskaeran zehaztuz. Customer Insights taldeak mezu elektroniko bat bidaliko du erregistratutako maizter kudeatzaileko helbide elektronikora, datuak esportatzeko berrespena eskatuko du.
2. Onartu eskatutako erabiltzailearen datuak esportatzeko baieztapena.
3. Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.

[!INCLUDE [footer-include](includes/footer-banner.md)]