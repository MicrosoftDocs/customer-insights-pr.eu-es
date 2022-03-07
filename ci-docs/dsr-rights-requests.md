---
title: Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian | Microsoft Docs
description: Erantzun Dynamics 365 Customer Insights hartzaileen xehetasunen gaitasunaren datuen jabearen eskaerei.
ms.date: 08/11/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
ms.openlocfilehash: e095eb4f8e194f314d7d6baf6fa6a7a319319d2a
ms.sourcegitcommit: 1946d7af0bd2ca216885bec3c5c95009996d9a28
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/25/2022
ms.locfileid: "8350254"
---
# <a name="data-subject-rights-dsr-requests-under-gdpr"></a>Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian

Europar Batasuneko Datuak Babesteko Araudi Orokorra (GDPR) indarrean dago 2018ko maiatzaren 25az geroztik. Eskubide esanguratsuak ematen dizkie partikularrei beren datuen inguruan. GDPR pertsonen pribatutasun eskubideak babestu eta gaitzea da. Microsoft-ek segurtasunarekin eta betetzearekin duen konpromisoari buruzko informazio gehiago irakur dezakezu hemen [Microsoft Trust Center](https://www.microsoft.com/trust-center).

Bezeroek DBAO betekizunak betetzeko konpromisoa dugu. Informazio pertsonala barne hartzen duten datuak ezabatu eta esportatzeko eskubidea biltzen du, hala nola erabiltzaile IDak, telefono zenbakiak eta helbide elektronikoak. Administratzaileek datu pertsonalak ezabatzeko edo esportatzeko erabiltzaileen eskaerak ezar ditzakete.

## <a name="audience-insights"></a>Hartzaileen xehetasunak

### <a name="responding-to-gdpr-data-subject-delete-requests-for-dynamics-365-customer-insights-audience-insights-capability"></a>Erantzun Dynamics 365 Customer Insights hartzaileen xehetasunen gaitasunaren DBAO datuen jabearen ezabatze-eskaerei

Erakunde baten bezeroen datu pertsonalak ezabatzeko eskubidea funtsezko babesa da Datuak Babesteko Araudi Orokorrean (DBAO). Datu pertsonalak kentzea barne hartzen ditu datu pertsonal guztiak eta sistemak sortutako erregistroak kentzea, ikuskapenen egunkari informazioa izan ezik.

#### <a name="manage-data-subject-delete-requests"></a>Kudeatu datuen gaia ezabatzeko eskaerak

Hartzaileen xehetasunek bezero jakin baten edo erabiltzailearen datu pertsonalak ezabatzeko honako produktuak eskaintzen dituen esperientzia eskaintzen du:

- **Kudeatu bezeroen datuak eskatzeko ezabatu**: Customer Insights-en bezeroen datuak Customer Insights-en kanpoko jatorrizko datu iturrietatik ateratzen dira. DBAO ezabatzeko eskaera guztiak jatorrizko datu-iturburu-en egin behar dira.
- **Kudeatu Customer Insights-eko erabiltzailearen datuak ezabatzeko eskaerak**: Erabiltzaileen datuak Customer Insights-ek sortzen ditu. DBAO ezabatzeko eskaera guztiak Customer Insights zerbitzuan egin behar dira.

##### <a name="manage-requests-to-delete-customer-data"></a>Kudeatu bezeroen datuak ezabatzeko eskaerak

Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake datu-iturburu-en ezabatu diren bezeroen datuak kentzeko:

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.
2. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**
3. Ezabatutako bezeroen datuak biltzen dituen zerrendan datu-iturburu bakoitzeko:
   1. Hautatu (...) eta ondoren, hautatu **Freskatu**.
   2. Begiratu datu-iturburu azpian **Egoera**. Marka egiaztatzeak freskagarria izan dela esan nahi du. Abisu triangelu batek zerbait gaizki joan dela esan nahi du. Abisu triangelua bistaratzen bada, jarri harremanetan D365CI@microsoft.com.

> [!div class="mx-imgBorder"]
> ![DBAO tratamendua bezeroen datuak eskatzeko ezabatu.](audience-insights/media/gdpr-data-sources.png "DBAO tratamendua bezeroen datuak eskatzeko ezabatu")

##### <a name="manage-delete-requests-for-user-data"></a>Kudeatu erabiltzailearen datuak ezabatzeko eskaerak

Customer Insights kudeatzaile batek urrats hauek jarraitu ditzake Customer Insights erabiltzailearen datuak ezabatzeko:

1. Hasi saioa Dynamics 365 Customer Insights aplikazioan.
2. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Baimenak**.
3. Hautatu ezabatu nahi dituzun erabiltzailearen kontrol-laukiak.
4. Hautatu **Kendu**.

### <a name="responding-to-gdpr-data-subject-export-requests"></a>DBAO datuen subjektuaren esportazio-eskaerei erantzutea

Datuak Babesteko Araudi Orokorra (DBAO) bidaian zurekin lotzeko konpromisoaren zati gisa, prestatzen laguntzeko dokumentazioa garatu dugu. Dokumentazio honetan, hartzaileen xehetasunak erabiltzean DBAO betetzea sustatzeko har ditzakezun urratsak deskribatzen dira.

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

## <a name="consent-management-preview"></a>Baimenaren kudeaketa (aurrebista)

Baimenak kudeatzeko gaitasunak ez ditu zuzenean erabiltzaileen datuak biltzen. Beste aplikazio batzuetan erabiltzaileek emandako baimen-datuak soilik inportatzen eta prozesatzen ditu.

Erabiltzaile espezifikoei buruzko adostasun-datuak kentzeko, kendu adostasuna kudeatzeko gaitasunean jasotako datu-iturrietatik. datu-iturburu freskatu ondoren, kendutako datuak Baimen Zentroan ere ezabatuko dira. Baimen-entitatea erabiltzen duten aplikazioek iturburuan kendutako datuak ere ezabatuko dituzte a ondoren [freskatu](audience-insights/system.md#refresh-processes). Datu-iturriak azkar freskatzea gomendatzen dugu datu-gaiaren eskaera bati erantzun ondoren erabiltzailearen datuak beste prozesu eta aplikazio guztietatik kentzeko.


<!-- ## Engagement insights (preview)

### Deleting and exporting event data containing end user identifiable information

The following sections describe how to delete and export event data that might contain personal data.

To delete or export data:

1. Tag event properties that contain data with personal information.
2. Delete or export data associated with specific values (for example: a specified user ID).

#### Tag and update event properties

Personal data is tagged on an event property level. First, tag the properties being considered for deletion or export.

To tag an event property as containing personal information, follow these steps:

1. Open the workspace containing the event.

1. Go to **Data** > **Events** to see the list of events in the selected workspace.
  
1. Select the event you want to tag.

1. Select **Edit properties** to open the pane listing all properties of the selected event.
     
1. Select **...** and then choose **Edit** to reach the **Update property** dialog.

   ![Edit event.](engagement-insights/media/edit-event.png "Edit event")

1. In the **Update Property** window, choose **...** in the upper right corner, and then choose the **Contains EUII** box. Choose **Update** to save your changes.

   ![Save your changes.](engagement-insights/media/update-property.png "Save your changes")

   > [!NOTE]
   > Every time the event schema changes or you create a new event, it's recommended that you evaluate the associated event properties and tag or untag them as containing personal data, if necessary.

#### Delete or export tagged event data

If all event properties have been tagged appropriately as described in the previous step, an environment admin can issue a deletion request against the tagged event data.

To manage EUII deletion or export requests

1. Go to **Admin** > **Environment** > **Settings**.

1. In the **Manage end user identifiable information (EUII)** section, select **Manage EUII**.

##### Deletion

For deletion, you can enter a list of comma-separated user IDs in the **Delete end user identifiable information (EUII)** section. These IDs will then be compared with all tagged event properties of all projects in the current environment via exact string matching. 

If a property value matches one of the provided IDs, the associated event will be permanently deleted. Due to the irreversibility of this action, you must confirm the deletion after selecting **Delete**.

##### Export

The export process is identical to the deletion process when it comes to defining event property values in the **Export end user identifiable information (EUII)** section. Additionally, you'll need to provide an **Azure blob storage URL** to specify the export destination. The Azure Blob URL must include a [Shared Access Signature (SAS)](/azure/storage/common/storage-sas-overview).

After selecting **Export**, all events of the current team that contain matching tagged properties will be exported in CSV format to the export destination.

### Good practices

* Try to avoid sending any events that contain personal data.
* If you need to send events containing EUII data, limit the number of events and event properties that contain EUII data. Ideally, limit yourself to one such event.
* Make sure that as few people as possible have access to the sent personal data.
* For events containing personal data, make sure that you set one property to emit a unique identifier that can easily be linked to a specific user (for example, a user ID). This makes it easier to segregate data and to export or delete the right data.
* Only tag one property per event as containing personal data. Ideally one that only contains a unique identifier.
* Do not tag properties containing verbose values (for example, an entire request body). Engagement insights capability uses exact string matching when deciding which events to delete or export. -->

[!INCLUDE[footer-include](includes/footer-banner.md)]