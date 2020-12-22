---
title: Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian | Microsoft Docs
description: Erantzun Dynamics 365 Customer Insights hartzaileen xehetasunen gaitasunaren datuen jabearen eskaerei.
ms.date: 05/14/2020
ms.reviewer: wimohabb
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: f276a73feca52023391ad92fbc84359921b85328
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404983"
---
# <a name="data-subject-rights-dsr-requests-under-gdpr"></a>Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian

## <a name="responding-to-gdpr-data-subject-delete-requests-for-dynamics-365-customer-insights-audience-insights-capability"></a>Erantzun Dynamics 365 Customer Insights hartzaileen xehetasunen gaitasunaren DBAO datuen jabearen ezabatze-eskaerei

Erakunde baten bezeroen datu pertsonalak ezabatzeko eskubidea funtsezko babesa da Datuak Babesteko Araudi Orokorrean (DBAO). Datu pertsonalak kentzea barne hartzen ditu datu pertsonal guztiak eta sistemak sortutako erregistroak kentzea, ikuskapenen egunkari informazioa izan ezik.

### <a name="manage-data-subject-delete-requests"></a>Kudeatu datuen gaia ezabatzeko eskaerak

Hartzaileen xehetasunek bezero jakin baten edo erabiltzailearen datu pertsonalak ezabatzeko honako produktuak eskaintzen dituen esperientzia eskaintzen du:

- **Kudeatu bezeroen datuak eskatzeko ezabatu**: Customer Insights-en bezeroen datuak Customer Insights-en kanpoko jatorrizko datu iturrietatik ateratzen dira. DBAO ezabatzeko eskaera guztiak jatorrizko datu-iturburu-en egin behar dira.
- **Kudeatu Customer Insights-eko erabiltzailearen datuak ezabatzeko eskaerak**: Erabiltzaileen datuak Customer Insights-ek sortzen ditu. DBAO ezabatzeko eskaera guztiak Customer Insights zerbitzuan egin behar dira.

#### <a name="manage-delete-requests-for-customer-data"></a>Kudeatu bezeroen datuak eskatzeko ezabatu

Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake datu-iturburu-en ezabatu diren bezeroen datuak kentzeko:

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.
2. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**
3. Ezabatutako bezeroen datuak biltzen dituen zerrendan datu-iturburu bakoitzeko:
   1. Hautatu (...) eta ondoren, hautatu **Freskatu**.
   2. Begiratu datu-iturburu azpian **Egoera**. Marka egiaztatzeak freskagarria izan dela esan nahi du. Abisu triangelu batek zerbait gaizki joan dela esan nahi du. Abisu triangelua bistaratzen bada, jarri harremanetan D365CI@microsoft.com.

> [!div class="mx-imgBorder"]
> ![DBAO tratamendua bezeroen datuak eskatzeko ezabatu](media/gdpr-data-sources.png "DBAO tratamendua bezeroen datuak eskatzeko ezabatu")

#### <a name="manage-delete-requests-for-user-data"></a>Kudeatu erabiltzailearen datuak ezabatzeko eskaerak

Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake Customer Insights erabiltzailearen datuak ezabatzeko:

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.
2. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Baimenak**.
3. Hautatu ezabatu nahi dituzun erabiltzailearen kontrol-laukiak.
4. Hautatu **Kendu**.

> [!div class="mx-imgBorder"]
> ![Kudeatu erabiltzailearen datuen DBAO ezabatzeko eskaerak](media/gdpr-permissions.png "Kudeatu erabiltzailearen datuen DBAO ezabatzeko eskaerak")

## <a name="responding-to-gdpr-data-subject-export-requests"></a>DBAO datuen subjektuaren esportazio-eskaerei erantzutea

Datuak Babesteko Araudi Orokorra (DBAO) bidaian zurekin lotzeko konpromisoaren zati gisa, prestatzen laguntzeko dokumentazioa garatu dugu. Dokumentazio honetan, hartzaileen xehetasunak erabiltzean DBAO betetzea sustatzeko har ditzakezun urratsak deskribatzen dira.

### <a name="manage-export-and-view-requests"></a>Kudeatu esportazio eta ikusteko eskaerak

Datuen eramangarritasun-eskubideari esker, pertsona baten datu pertsonalen kopia eska daiteke formatu elektroniko batean ("kontrolatutako egitura, normalean erabilitakoa, makina irakurgarria eta elkarrekin egingarria") beste datu kontroladore bati transmititu ahal izateko.

#### <a name="export-customer-data-tenant-admin"></a>Esportatu bezeroen datuak - Beste batzuk (maizterraren kudeatzailea)

Maizter administratzaileak urrats hauek jarraitzen ditu datuak esportatzeko:

1. Bidali mezu elektroniko bat helbidera D365CI@microsoft.com bezeroaren helbide elektronikoa eskaeran zehaztuz. Customer Insights taldeak mezu elektroniko bat bidaliko du erregistratutako maizter kudeatzaileko helbide elektronikora, datuak esportatzeko berrespena eskatuko du.
2. Onartu eskatutako bezeroari datuak esportatzeko baieztapena.
3. Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.

#### <a name="export-user-data-tenant-admin"></a>Esportatu erabiltzailearen datuak (maizterraren kudeatzailea)

1. Bidali mezu elektroniko bat helbidera D365CI@microsoft.com erabiltzailearen helbide elektronikoa eskaeran zehaztuz. Customer Insights taldeak mezu elektroniko bat bidaliko du erregistratutako maizter kudeatzaileko helbide elektronikora, datuak esportatzeko berrespena eskatuko du.
2. Onartu eskatutako erabiltzailearen datuak esportatzeko baieztapena.
3. Jaso esportatutako datuak maizter admin helbide elektronikoaren bidez.
