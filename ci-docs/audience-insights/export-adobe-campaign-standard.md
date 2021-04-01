---
title: Esportatu Customer Insights datuak Adobe Campaign Standard-era
description: Ikusi audientzia estatistiken segmentuak nola erabiltzen diren Adobe Campaign Standard-en.
ms.date: 02/26/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: a5d0154c3d7c473dcba03fac0847bafcf97de2f2
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596300"
---
# <a name="use-customer-insights-segments-in-adobe-campaign-standard-preview"></a>Erabili Customer Insights segmentuak nola erabiltzen diren Adobe Campaign Standard-en (aurrebista)

Erabiltzaileentzako ikusleen estatistiken erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortzea zure marketin kanpainak eraginkorragoak izan daitezen publiko garrantzitsuei zuzenduta. Adobe Experience Platform-eko eta Adobe Campaign Standard bezalako aplikazioetako audientziaren inguruko segmentu bat erabiltzeko, artikulu honetan zehaztutako urrats batzuk jarraitu behar dituzu.

:::image type="content" source="media/ACS-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a>Aurrebaldintzak

-   Dynamics 365 Customer Insights lizentzia
-   Adobe Campaign Standard lizentzia
-   Azure blob-biltegia kontua

## <a name="campaign-overview"></a>Kanpainaren informazio orokorra

Adobe Experience Platform-en audientzia estatistiketatik segmentuak nola erabil ditzakezun hobeto ulertzeko, ikus dezagun fikziozko lagin kanpaina.

Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei. Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu. Bezero horiek mantentzeko, promozio eskaintza posta elektroniko bidez bidali nahi diezu, Adobe Campaign Standard erabiliz.

Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu. Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen. Hala ere, ikusleei buruzko informazioa eta Adobe Campaign Standard konfiguratu daitezke kanpaina errepikatuko agertoki batean lan egiteko ere.

## <a name="identify-your-target-audience"></a>Identifikatu zure xede-publikoa

Gure eszenatokian, bezeroen helbide elektronikoak ikusleen estatistiketan eskuragarri daudela eta haien promozio hobespenak segmentuko kideak identifikatzeko aztertu direla suposatzen dugu.

[Ikusleen estatistiketan definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero hauei posta elektroniko bidezko promozioa bidaltzeko asmoa duzu.

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira. Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.

## <a name="export-your-target-audience"></a>Esportatu zure xede-publikoa

Gure xede-audientzia identifikatuta, esportazioen konfigurazioa konfiguratu ahal izango dugu ikusleen estatistiketatik Azure blob-biltegia kontura.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Adobe Campaign** lauzan, hautatu **Konfiguratu**.

   :::image type="content" source="media/adobe-campaign-standard-tile.png" alt-text="Adobe Campaign Standard-en konfigurazio lauza.":::

1. Eman **Bistaratzeko izena** esportazio helmuga berri honetarako eta ondoren sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** segmentua esportatu nahi duzun Azure blob-biltegia kontukoa.  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 

   - Azure Blob biltegiratze kontuaren izena eta kontuaren gakoa aurkitzeko informazio gehiago lortzeko, ikus [Kudeatu biltegiratze kontuen ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).

   - Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

1. Hautatu **Hurrengoa**.

1. Aukeratu esportatu nahi duzun segmentua. Adibide honetan, **ChurnProneCustomers** da.

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. Hautatu **Hurrengoa**.

1. Orain mapak egiten ditugu **Iturria** audientzien ikuspegi segmentutik eremura **Helburua** eremuen izenak Adobe Campaign Standard profileko eskeman.

   :::image type="content" source="media/ACS-field-mapping.png" alt-text="Adobe Campaign Standard konektoreko eremuen mapaketa.":::

   Atributu gehiago gehitu nahi badituzu, hautatu **Gehitu atributua**. Helburuaren izena iturburuko eremuaren izenetik desberdina izan daiteke, segmentuen irteera ikus dezakezu Adobe Campaign Standard-era segmentuek bi sistemetan izen bera ez badute.

   > [!NOTE]
   > Helbide elektronikoa identitate-eremu gisa erabiltzen da, baina zure audientzien estatistiken bezeroaren profiletik beste edozein identifikatzaile erabil dezakezu datuak Adobe Campaign Standard-ra mapatzeko.

1. Sakatu **Gorde**.

Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Administratzailea** > **Esportazioak** > **Nire esportazio helmugak**.

:::image type="content" source="media/export-destination-adobe-campaign-standard.png" alt-text="Pantaila-argazkia esportazioen zerrenda eta lagin-segmentua nabarmenduta.":::

Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#export-data-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).

> [!NOTE]
> Ziurtatu esportatutako segmentuan erregistro kopurua Adobe Campaign Standard lizentziaren baimendutako mugaren barruan dagoela.

Esportatutako datuak goian konfiguratu duzun Azure blob-biltegia edukiontzian gordetzen dira. Karpeta bide hau automatikoki sortzen da zure edukiontzian:

*%ContainerName%/CustomerInsights_%instanceID%/% exportdestination-name%_%segmentname%_%timestamp%.csv*

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv

## <a name="configure-adobe-campaign-standard"></a>Konfiguratu Adobe Campaign Standard

Audientzia estatistiketatik ateratako segmentu bat esportatzen denean, aurreko urratsean esportazio-helmuga definitzen zenuen bitartean aukeratu dituzun zutabeak ditu. Datu hauek erabil daitezke [profilak sortu Adobe Campaign Standard zerbitzuan](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).

Adobe Campaign Standard-en segmentua erabiltzeko, Adobe Campaign Standard-en profil eskema luzatu behar dugu bi eremu gehigarri sartzeko. Ikasi nola egin [profila baliabidea luzatu](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) eremu berriekin Adobe Campaign Standard.

Gure adibidean, eremu hauek dira *Segmentuaren izena eta segmentuaren data (aukerakoa).*

Eremu horiek erabiliko ditugu kanpaina honetarako bideratu nahi dugun Adobe Campaign Standard profilak identifikatzeko.

Adobe Campaign Standard-en inportatzera zoazena baino beste erregistroik ez badago, urrats hau salta dezakezu.

## <a name="import-data-into-adobe-campaign-standard"></a>Inportatu datuak Adobe Campaign Standard-era

Dena indarrean dagoela, entzuleen datuetatik prestatutako audientzia datuak Adobe Campaign Standard profilak sortzeko inportatu behar ditugu. Ikasi [nola inportatu profilak Adobe Campaign Standard zerbitzuan](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences) lan-fluxua erabiliz.

Beheko irudiko inportazio lan-fluxua 8 orduro exekutatzeko konfiguratuta dago eta esportatutako audientzia estatistiken segmentuak bilatzen ditu (.csv fitxategia Azure blob-biltegian). Lan-fluxuak .csv fitxategiaren edukia zehaztutako zutabe ordenan ateratzen du. Lan-fluxu hau oinarrizko akatsak kudeatzeko eta erregistro bakoitzak helbide elektronikoa duela ziurtatzeko sortu da, datuak Adobe Campaign Standard-en hidratatu aurretik. Lan-fluxuak ere segmentuaren izena fitxategi-izenetik ateratzen du ACS profileko datuetara sartu aurretik.

:::image type="content" source="media/ACS-import-workflow.png" alt-text="Inportazio lan-fluxuaren pantaila-argazkia Adobe Campaign Standard erabiltzaile interfazean.":::

## <a name="retrieve-the-audience-in-adobe-campaign-standard"></a>Berreskuratu audientzia Adobe Campaign Standard zerbitzuan

Datuak Adobe Campaign Standard-era inportatu ondoren, zuk [lan fluxua sor dezake](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) eta [kontsulta](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) oinarritutako bezeroak *Segmentuaren izena* eta *Segmentuaren Data* gure lagin kanpainarako identifikatutako profilak hautatzeko.

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a>Sortu eta bidali mezu elektronikoa Adobe Campaign Standard erabiliz

Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Adobe Campaign Standard-ren berritze-eskaintza duen posta elektronikoa.":::