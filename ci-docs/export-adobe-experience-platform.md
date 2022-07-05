---
title: Esportatu segmentuak hona Adobe Experience Platform (aurrebista)
description: Ikasi Customer Insights segmentuak erabiltzen Adobe Experience Platform.
ms.date: 03/29/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: c29b8264019669ffd954a298ce3a633c852477fa
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9052496"
---
# <a name="export-segments-to-adobe-experience-platform-preview"></a>Esportatu segmentuak hona Adobe Experience Platform (aurrebista)

-ren erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortu izana zure marketin-kanpainak eraginkorragoak izan daitezen, publiko garrantzitsuak zuzenduta. Customer Insights-en segmentu bat erabiltzeko Adobe Experience Platform eta bezalako aplikazioak Adobe Kanpainaren estandarra, artikulu honetan azaltzen diren urrats batzuk jarraitu behar dituzu.

:::image type="content" source="media/AEP-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a>Aurrebaldintzak

-   Dynamics 365 Customer Insights lizentzia
-   Adobe Experience Platform lizentzia
-   Adobe Campaign Standard lizentzia
-   Azure blob-biltegia kontua

## <a name="campaign-overview"></a>Kanpainaren informazio orokorra

Customer Insights-en segmentuak nola erabil ditzakezun hobeto ulertzeko Adobe Experience Platform, ikus dezagun fikziozko lagin-kanpaina bat.

Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei. Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu. Bezero hauek mantentzeko, posta elektroniko bidez promozio eskaintza bidali nahi diezu Adobe Experience Platform.

Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu. Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen.

## <a name="identify-your-target-audience"></a>Identifikatu zure xede-publikoa

Gure eszenatokian, bezeroen helbide elektronikoak Customer Insights-en eskuragarri daudela suposatzen dugu eta haien sustapen-hobespenak aztertu dira segmentuko kideak identifikatzeko.

The [Customer Insights-en definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero horiei posta elektronikoko promozioa bidaltzeko asmoa duzu.

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira. Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.

## <a name="export-your-target-audience"></a>Esportatu zure xede-publikoa

Gure xede-publikoa identifikatuta, Customer Insights-etik Azure Blob Storage kontu batera esportatzea konfiguratu dezakegu.

### <a name="configure-a-connection"></a>Konfiguratu konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **Azure blob biltegiratzea** edo hautatu **Konfiguratu** urtean **Azure blob biltegiratzea** lauza konexioa konfiguratzeko.

   :::image type="content" source="media/export-azure-blob-storage-tile.png" alt-text="Azure blob-biltegiko konfigurazio lauza."::: 

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** segmentua esportatu nahi duzun Blob Storage konturako.  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 
   
    - Blob Storage kontuaren izena eta kontuaren gakoa nola aurkitu jakiteko, ikusi [Kudeatu biltegiratze kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
    - Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

1. Hautatu **Gorde** konexioa osatzeko. 

### <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Azure Blob biltegiaren sekzioan. Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.

1. Aukeratu esportatu nahi duzun segmentua. Adibide honetan, **ChurnProneCustomers** da.

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. Sakatu **Gorde**.

Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Datuak** > **Esportazioak**.

Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#run-exports-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).

> [!NOTE]
> Ziurtatu esportatutako segmentuan erregistro kopurua zure baimendutako mugaren barruan dagoela Adobe Campaign Standard lizentzia.

Esportatutako datuak goian konfiguratu duzun Azure blob Storage edukiontzian gordetzen dira. Karpeta bide hau automatikoki sortzen da zure edukiontzian:

*%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/ChurnSegmentDemo/2021/02/16/1433/ChurnProneCustomers_1.csv

*Eredua.json* esportatutako entitateak *%ExportDestinationName%* maila.

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo/model.json

## <a name="define-experience-data-model-xdm-in-adobe-experience-platform"></a>Definitu Experience Data Model (XDM) urtean Adobe Experience Platform

Customer Insights-en esportatutako datuak barruan erabil daitezkeen aurretik Adobe Experience Platform, Experience Data Model eskema definitu behar dugu eta [konfiguratu denbora errealeko bezeroaren profilaren datuak](https://experienceleague.adobe.com/docs/experience-platform/profile/tutorials/dataset-configuration.html#tutorials).

Ikasi [zer den XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) eta ulertu [eskemaren konposizioaren oinarriak](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schema).

## <a name="import-data-into-adobe-experience-platform"></a>Inportatu datuak Adobe Experience Platform aplikaziora

Orain dena prest dagoela, Customer Insights-etik prestatutako audientzia-datuak inportatu behar ditugu Adobe Experience Platform.

Lehenik eta behin, [sortu Azure blob-biltegia iturburu konexioa](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/blob.html#getting-started).    

Iturburu-konexioa zehaztu ondoren, [datu-fluxu bat konfiguratu](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html#ui-tutorials) hodeiko biltegiratze batch konexio baterako Customer Insights-en segmentuaren irteerara inportatzeko Adobe Experience Platform.

## <a name="create-an-audience-in-adobe-campaign-standard"></a>Sortu audientzia bat bertan Adobe Campaign Standard

Kanpaina honen mezu elektronikoa bidaltzeko, Adobe Campaign Standard erabiliko dugu. Datuak inportatu ondoren Adobe Experience Platform, behar dugu [audientzia sortu](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/get-started-profiles-and-audiences.html#permission) urtean Adobe Campaign Standard datuak erabiliz Adobe Experience Platform.


Ikasi nola egin [erabili segmentu eraikitzailea](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/audience-destinations/aep-using-segment-builder.html) urtean Adobe Campaign Standard audientzia definitzeko datuetan oinarrituta Adobe Experience Platform.

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a>Sortu eta bidali mezu elektronikoa erabiliz Adobe Campaign Standard

Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Posta elektronikoaren adibidea berritze eskaintzarekin Adobe Campaign Standard.":::
