---
title: Datu subjektuen eskubideak (DSR) eskaerak DBAOren azpian | Microsoft Docs
description: Erantzun Dynamics 365 Customer Insights hartzaileen xehetasunen gaitasunaren datuen jabearen eskaerei.
ms.date: 08/11/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
ms.openlocfilehash: 6faaeb6a1ee34c3e5c8e7d465b37cee589bc920c
ms.sourcegitcommit: 5704002484cdf85ebbcf4e7e4fd12470fd8e259f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/08/2021
ms.locfileid: "7483638"
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

## <a name="engagement-insights"></a>Parte-hartzearen xehetasunak

### <a name="deleting-and-exporting-event-data-containing-end-user-identifiable-information"></a>Azken erabiltzailearen identifikazio informazioa duten gertaeren datuak ezabatu eta esportatu

Ondorengo ataletan datu pertsonalak izan ditzaketen gertaeren datuak nola ezabatu eta esportatu azaltzen dira.

Datuak ezabatzeko edo esportatzeko:

1. Datuak informazio pertsonalarekin dituzten gertaeren propietateak etiketatu.
2. Ezabatu edo esportatu balio zehatzei lotutako datuak (adibidez: zehaztutako erabiltzaile IDa).

#### <a name="tag-and-update-event-properties"></a>Etiketatu eta eguneratu gertaeren propietateak

Datu pertsonalak gertaeren jabetza mailan etiketatuta daude. Lehenik eta behin, etiketatu ezabatzeko edo esportatzeko kontuan hartzen ari diren propietateak.

Gertaeraren jabetza informazio pertsonala duela etiketatzeko, jarraitu urrats hauei:

1. Ireki gertaera duen lan eremua.

1. Joan **Datuak** > **Ekitaldiak** hautatutako lan eremuan gertakarien zerrenda ikusteko.
  
1. Hautatu etiketatu nahi duzun gertaera.

1. Aukeratu **Editatu propietateak** hautatutako gertaeraren propietate guztiak zerrendatzen dituen panela irekitzeko.
     
1. Aukeratu **...** eta gero aukeratu **Editatu** heltzeko **Eguneratu jabetza** elkarrizketa-koadroa.

   ![Editatu gertaera.](engagement-insights/media/edit-event.png "Editatu gertaera")

1. Hurrengoan **Eguneratu jabetza** leihoa, aukeratu **...** goiko eskuineko izkinan, eta ondoren aukeratu **EUII dauka** kutxa. Aukeratu **Eguneratu** aldaketak gordetzeko.

   ![Gorde aldaketak.](engagement-insights/media/update-property.png "Gorde aldaketak")

   > [!NOTE]
   > Gertaeraren eskema aldatzen den bakoitzean edo gertaera berri bat sortzen duzun bakoitzean, lotutako gertaeren propietateak ebaluatzea eta datu pertsonalak dituztela etiketatzea edo etiketatzea gomendatzen da, beharrezkoa bada.

#### <a name="delete-or-export-tagged-event-data"></a>Ezabatu edo esportatu etiketatutako gertaeren datuak

Gertaeren propietate guztiak aurreko urratsean azaldu bezala egoki etiketatu badira, inguruneko administratzaile batek ezabatzeko eskaera egin dezake etiketatutako gertaeren datuen aurka.

EUII ezabatzeko edo esportatzeko eskaerak kudeatzeko

1. Joan **Administratu** > **Ingurunea** > **Ezarpenak**.

1. Hurrengoan **Kudeatu azken erabiltzailearen identifikazio informazioa (EUII)** atala, hautatu **Kudeatu EUII**.

##### <a name="deletion"></a>Ezabatzea

Ezabatzeko, komaz bereizitako erabiltzaile IDen zerrenda sar dezakezu **Ezabatu azken erabiltzailearen identifikazio informazioa (EUII)** atala. ID horiek uneko inguruneko proiektu guztien etiketatutako gertaeren propietate guztiekin alderatuko dira kate zehatzen bidez. 

Jabetzaren balioa emandako IDetako batekin bat badator, lotutako gertaera behin betiko ezabatuko da. Ekintza honen atzeraezintasuna dela eta, hautatu ondoren ezabaketa berretsi behar duzu **Ezabatu**.

##### <a name="export"></a>Export

Esportazio prozesua ezabatze prozesuaren berdina da gertaeren propietateen balioak definitzeko orduan **Esportatu azken erabiltzailearen identifikazio informazioa (EUII)** atala. Gainera, fitxategi bat eman beharko duzu **Azure blob biltegiratze URLa** esportazio helmuga zehazteko. Azure Blob URLak a izan behar du [Sarbide partekatuko sinadura (SAS)](/azure/storage/common/storage-sas-overview).

Aukeratu ondoren **Esportatu**, bat datozen etiketatutako propietateak dituzten uneko taldearen gertaera guztiak CSV formatuan esportatuko dira esportazio helmugara.

### <a name="good-practices"></a>Jardunbide egokiak

* Saiatu datu pertsonalak dituzten gertaerak ez bidaltzea saihesten.
* EUII datuak dituzten gertaerak bidali behar badituzu, mugatu EUII datuak dituzten gertaeren eta gertaeren propietate kopurua. Egokiena, mugatu horrelako gertaera batera.
* Ziurtatu ahalik eta jende gutxik duela bidalitako datu pertsonaletara sarbidea.
* Datu pertsonalak dituzten gertaeretan, ziurtatu propietate bat ezartzen duzula identifikatzaile bakarra igortzeko, erabiltzaile jakin batekin (adibidez, erabiltzaile IDarekin) erraz lotzeko modukoa. Horrek datuak bereiztea eta datu egokiak esportatzea edo ezabatzea errazten du.
* Etiketatu gertaera bakoitzeko datu bakarra duten datu gisa. Egokiena identifikatzaile bakarra duen bakarra.
* Ez etikotu xehetasun balioak dituzten propietateak (adibidez, eskaera gorputz osoa). Elkarreragin xehetasunen gaitasunak kateen bat etortze zehatza erabiltzen du zein gertaera ezabatu edo esportatu erabakitzeko orduan.

[!INCLUDE[footer-include](includes/footer-banner.md)]