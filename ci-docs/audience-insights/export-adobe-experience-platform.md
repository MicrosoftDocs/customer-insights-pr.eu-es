---
title: Esportatu Customer Insights datuak Adobe Experience Platform-era
description: Ikusi audientzia estatistiken segmentuak nola erabiltzen diren Adobe Experience Platform-en.
ms.date: 02/26/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: d1856861562be55c6d1d051050fe965560fa42f8
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596254"
---
# <a name="use-customer-insights-segments-in-adobe-experience-platform-preview"></a>Erabili Customer Insights segmentuak nola erabiltzen diren Adobe Experience Platform-en (aurrebista)

Erabiltzaileentzako ikusleen estatistiken erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortzea zure marketin kanpainak eraginkorragoak izan daitezen publiko garrantzitsuei zuzenduta. Adobe Experience Platform-eko eta Adobe Campaign Standard bezalako aplikazioetako audientziaren inguruko segmentu bat erabiltzeko, artikulu honetan zehaztutako urrats batzuk jarraitu behar dituzu.

:::image type="content" source="media/AEP-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a>Aurrebaldintzak

-   Dynamics 365 Customer Insights lizentzia
-   Adobe Experience Platform lizentzia
-   Adobe Campaign Standard lizentzia
-   Azure blob-biltegia kontua

## <a name="campaign-overview"></a>Kanpainaren informazio orokorra

Adobe Experience Platform-en audientzia estatistiketatik segmentuak nola erabil ditzakezun hobeto ulertzeko, ikus dezagun fikziozko lagin kanpaina.

Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei. Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu. Bezero horiek mantentzeko, promozio eskaintza posta elektroniko bidez bidali nahi diezu, Adobe Experience Platform erabiliz.

Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu. Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen.

## <a name="identify-your-target-audience"></a>Identifikatu zure xede-publikoa

Gure eszenatokian, bezeroen helbide elektronikoak ikusleen estatistiketan eskuragarri daudela eta haien promozio hobespenak segmentuko kideak identifikatzeko aztertu direla suposatzen dugu.

[Ikusleen estatistiketan definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero hauei posta elektroniko bidezko promozioa bidaltzeko asmoa duzu.

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira. Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.

## <a name="export-your-target-audience"></a>Esportatu zure xede-publikoa

Gure xede-audientzia identifikatuta, esportazioen konfigurazioa konfiguratu ahal izango dugu ikusleen estatistiketatik Azure blob-biltegia kontura.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. Hurrengoan **Azure blob-biltegia** fitxa, hautatu **Konfiguratu**.

   :::image type="content" source="media/export-azure-blob-storage-tile.png" alt-text="Azure blob-biltegiko konfigurazio lauza.":::

1. Eman **Bistaratzeko izena** esportazio helmuga berri honetarako eta ondoren sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** segmentua esportatu nahi duzun Azure blob-biltegia kontukoa.  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 

   - Azure Blob biltegiratze kontuaren izena eta kontuaren gakoa aurkitzeko informazio gehiago lortzeko, ikus [Kudeatu biltegiratze kontuen ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).

   - Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

1. Hautatu **Hurrengoa**.

1. Aukeratu esportatu nahi duzun segmentua. Adibide honetan, **ChurnProneCustomers** da.

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. Sakatu **Gorde**.

Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Administratzailea** > **Esportazioak** > **Nire esportazio helmugak**.

:::image type="content" source="media/export-destination-azure-blob-storage.png" alt-text="Pantaila-argazkia esportazioen zerrenda eta lagin-segmentua nabarmenduta.":::

Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#export-data-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).

> [!NOTE]
> Ziurtatu esportatutako segmentuan erregistro kopurua Adobe Campaign Standard lizentziaren baimendutako mugaren barruan dagoela.

Esportatutako datuak goian konfiguratu duzun Azure blob-biltegia edukiontzian gordetzen dira. Karpeta bide hau automatikoki sortzen da zure edukiontzian:

*%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/ChurnSegmentDemo/2021/02/16/1433/ChurnProneCustomers_1.csv

*Eredua.json* esportatutako entitateak *%ExportDestinationName%* maila.

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo/model.json

## <a name="define-experience-data-model-xdm-in-adobe-experience-platform"></a>Definitu Experience Data Model (XDM) Adobe Experience Platform-en

Audientzia estatistiketatik esportatutako datuak Adobe Experience Platform programan erabili aurretik, Experience Data Model eskema eta [konfiguratu datuak denbora errealean bezeroaren profilerako](https://experienceleague.adobe.com/docs/experience-platform/profile/tutorials/dataset-configuration.html#tutorials).

Ikasi [zer den XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) eta ulertu [eskemaren konposizioaren oinarriak](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schema).

## <a name="import-data-into-adobe-experience-platform"></a>Inportatu datuak Adobe Experience Platformera

Dena indarrean dagoela, entzuleen datuetatik prestatutako audientzia datuak Adobe Experience Platformera inportatu behar ditugu.

Lehenik eta behin, [sortu Azure blob-biltegia iturburu konexioa](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/blob.html#getting-started).    

Iturburu konexioa definitu ondoren, [konfiguratu datu-fluxua](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html#ui-tutorials) hodeiko biltegiratze batch konexiorako segmentuen irteera audientzia estatistiketatik Adobe Experience Platformera inportatzeko.

## <a name="create-an-audience-in-adobe-campaign-standard"></a>Sortu audientzia Adobe Campaign Standard zerbitzuan

Kanpaina honen mezu elektronikoa bidaltzeko, Adobe Campaign Standard erabiliko dugu. Datuak Adobe Experience Platform-era inportatu ondoren, behar dugu [audientzia sortu](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/get-started-profiles-and-audiences.html#permission) Adobe Campaign Standard-n Adobe Experience Platform-eko datuak erabiliz.

Ikasi nola egin [erabili segmentu eraikitzailea](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/working-with-adobe-experience-platform/aep-using-segment-builder.html#building-a-segment) Adobe Campaign Standard-en Adobe Experience Platform-eko datuetan oinarritutako audientzia definitzeko.

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a>Sortu eta bidali mezu elektronikoa Adobe Campaign Standard erabiliz

Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Adobe Campaign Standard-ren berritze-eskaintza duen posta elektronikoa.":::