---
title: Esportatu segmentuak hona Adobe Experience Platform (aurrebista)
description: Ikasi Customer Insights segmentuak erabiltzen Adobe Experience Platform.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: fcb43e0956c6d1f0ef36b222dd2b718906364244
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195275"
---
# <a name="export-segments-to-adobe-experience-platform-preview"></a>Esportatu segmentuak hona Adobe Experience Platform (aurrebista)

Esportatu publiko garrantzitsuak helburu dituzten segmentuak Adobe Experience Platform.

:::image type="content" source="media/AEP-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a>Aurrebaldintzak

- An Adobe Experience Platform lizentzia.
- An Adobe Kanpainaren lizentzia estandarra.
- An [Azure Blob Storage kontua](/azure/storage/blobs/create-data-lake-storage-account) izena eta kontu-gakoa. Izena eta gakoa aurkitzeko, ikus [Kudeatu biltegiratze-kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
- An [Azure Blob biltegiratze edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

## <a name="campaign-overview"></a>Kanpainaren informazio orokorra

Customer Insights-eko segmentuak nola erabil ditzakezun hobeto ulertzeko Adobe Experience Platform, ikus dezagun fikziozko lagin-kanpaina bat.

Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei. Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu. Bezero hauek mantentzeko, posta elektroniko bidez promozio eskaintza bidali nahi diezu Adobe Experience Platform.

Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu. Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen.

## <a name="identify-your-target-audience"></a>Identifikatu zure xede-publikoa

Gure eszenatokian, bezeroen helbide elektronikoak Customer Insights-en eskuragarri daudela suposatzen dugu eta haien sustapen-hobespenak aztertu dira segmentuko kideak identifikatzeko.

The [Customer Insights-en definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero horiei posta elektronikoko promozioa bidaltzeko asmoa duzu.

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira. Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.

## <a name="export-your-target-audience"></a>Esportatu zure xede-publikoa

Customer Insights-etik Azure Blob Storage kontu batera esportatzea konfiguratuko dugu.

### <a name="set-up-connection-to-azure-blob-storage"></a>Konfiguratu konexioa Azure Blob Storage-rekin

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Azure Blob biltegiratzea**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** segmentua esportatu nahi duzun Blob Storage konturako.  

   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. ":::

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

### <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Azure Blob biltegiaren sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Aukeratu esportatu nahi duzun segmentua. Adibide honetan, **ChurnProneCustomers** da.

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

> [!NOTE]
> Ziurtatu esportatutako segmentuan erregistro kopurua zure baimendutako mugaren barruan dagoela Adobe Campaign Standard lizentzia.

Esportatutako datuak konfiguratu duzun Azure Blob Storage edukiontzian gordetzen dira. Hurrengo karpeta bideak automatikoki sortzen dira zure edukiontzian:

- Sistemak sortutako iturburuko entitate eta entitateetarako:  

  *%ContainerName%/CustomerInsights_%instanceID%/%ExportDestinationName%/%EntityName%/%Year%/%Month%/%Day%/%HHMM%/%EntityName%_%PartitionId%.csv*

  Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/BlobExport/ChurnSegmentDemo/2021/02/16/1433/ChurnProneCustomers_1.csv

- *Eredua.json* esportatutako entitateak *%ExportDestinationName%* maila.

  Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo/model.json

## <a name="define-experience-data-model-xdm-in-adobe-experience-platform"></a>Definitu Experience Data Model (XDM) urtean Adobe Experience Platform

Customer Insights-en esportatutako datuak barruan erabil daitezkeen aurretik Adobe Experience Platform, Definitu Experience Data Model eskema eta [konfiguratu denbora errealeko bezeroaren profilaren datuak](https://experienceleague.adobe.com/docs/experience-platform/profile/tutorials/dataset-configuration.html#tutorials).

Ikasi [zer den XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html) eta ulertu [eskemaren konposizioaren oinarriak](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schema).

## <a name="import-data-into-adobe-experience-platform"></a>Inportatu datuak Adobe Experience Platform aplikaziora

Inportatu Customer Insights-etik prestatutako audientzia-datuak Adobe Experience Platform.

1. [Sortu Azure Blob Storage iturburu-konexio bat](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/cloud-storage/blob.html#getting-started).

1. [Konfiguratu datu-fluxu bat](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/cloud-storage.html#ui-tutorials) hodeiko biltegiratze batch konexio baterako Customer Insights-en segmentuaren irteerara inportatzeko Adobe Experience Platform.

## <a name="create-an-audience-in-adobe-campaign-standard"></a>Sortu audientzia bat bertan Adobe Campaign Standard

Kanpaina honen mezu elektronikoa bidaltzeko, Adobe Campaign Standard erabiliko dugu.

1. [Sortu audientzia](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/get-started-profiles-and-audiences.html#permission) urtean Adobe Kanpaina estandarra datuak erabiliz Adobe Experience Platform.

1. [Erabili segmentu-sortzailea](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/audience-destinations/aep-using-segment-builder.html) urtean Adobe Kanpaina estandarra ikusle bat definitzeko datuetan oinarrituta Adobe Experience Platform.

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a>Sortu eta bidali mezu elektronikoa erabiliz Adobe Campaign Standard

Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Posta elektronikoaren adibidea berritze eskaintzarekin Adobe Campaign Standard.":::

[!INCLUDE [footer-include](includes/footer-banner.md)]
