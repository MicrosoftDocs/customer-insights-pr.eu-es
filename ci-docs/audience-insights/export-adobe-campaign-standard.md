---
title: Esportatu Customer Insights datuak Adobe Campaign Standard
description: Ikusi publikoaren estatistiken segmentuak nola erabiltzen diren Adobe Campaign Standard.
ms.date: 03/29/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: d301b4f0cb875303fb3d373b77177acd1c1f5219cd6f23c2a1d29ce67a222eab
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7032148"
---
# <a name="use-customer-insights-segments-in-adobe-campaign-standard-preview"></a>Erabili Customer Insights segmentuak atalean Adobe Campaign Standard (aurrebista)

-N ikusleei buruzko informazioaren erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortzea zure marketin kanpainak eraginkorragoak izan daitezen publiko garrantzitsuei zuzenduta. Ikusleen estatistiketatik segmentu bat erabiltzeko Adobe Experience Platform eta bezalako aplikazioak Adobe Campaign Standard, artikulu honetan zehaztutako urrats batzuk jarraitu behar dituzu.

:::image type="content" source="media/ACS-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a>Aurrebaldintzak

-   Dynamics 365 Customer Insights lizentzia
-   Adobe Campaign Standard lizentzia
-   Azure blob-biltegia kontua

## <a name="campaign-overview"></a>Kanpainaren informazio orokorra

Ikusleen estatistiketako segmentuak nola erabil ditzakezun hobeto ulertzeko Adobe Experience Platform Ikus dezagun fikziozko lagin kanpaina.

Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei. Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu. Bezero hauek mantentzeko, posta elektroniko bidez promozio eskaintza bidali nahi diezu Adobe Campaign Standard.

Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu. Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen. Hala ere, ikusleen ikuspegiak eta Adobe Campaign Standard kanpaina errepikakorreko eszenatoki batean lan egiteko ere konfigura daiteke.

## <a name="identify-your-target-audience"></a>Identifikatu zure xede-publikoa

Gure eszenatokian, bezeroen helbide elektronikoak ikusleen estatistiketan eskuragarri daudela eta haien promozio hobespenak segmentuko kideak identifikatzeko aztertu direla suposatzen dugu.

[Ikusleen estatistiketan definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero hauei posta elektroniko bidezko promozioa bidaltzeko asmoa duzu.

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira. Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.

## <a name="export-your-target-audience"></a>Esportatu zure xede-publikoa

### <a name="configure-a-connection"></a>Konfiguratu konexioa

Gure xede-audientzia identifikatuta, esportazioen konfigurazioa konfiguratu ahal izango dugu ikusleen estatistiketatik Azure blob-biltegia kontura.

1. Ikusleen ikuspegietan, joan hona **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Adobe Campaign** konfiguratzeko konexioa edo hautatu **Konfiguratu** hurrengoan **Adobe Campaign** lauza.

   :::image type="content" source="media/adobe-campaign-standard-tile.png" alt-text="Konfigurazio fitxa Adobe Campaign Standard.":::

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Sartu **Kontuaren izena**, **Kontuaren gakoa**, eta **Edukiontzia** Azure Blob biltegiratze-kontuarena, segmentua esportatu nahi duzunera.  
      
   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. "::: 

   - Azure Blob Storage kontuaren izena eta kontuaren gakoa aurkitzeko informazio gehiago lortzeko, ikus [Kudeatu biltegiratze kontuen ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).

   - Edukiontzia nola sortzen den jakiteko, ikus [Sortu edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

1. Hautatu **Gorde** konexioa osatzeko.

### <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. Hurrengoan **Konexioa esportatzeko** eremua, aukeratu konexioa Adobe Campaign atalean. Atal honen izena ikusten ez baduzu, mota honetako konexiorik ez duzu eskuragarri.

1. Aukeratu esportatu nahi duzun segmentua. Adibide honetan, **ChurnProneCustomers** da.

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. Hautatu **Hurrengoa**.

1. Orain mapak egiten ditugu **Iturria** audientzien ikuspegi segmentutik eremura **Helburua** eremuko izenak Adobe Campaign Standard profilaren eskema.

   :::image type="content" source="media/ACS-field-mapping.png" alt-text="Eremurako mapak Adobe Campaign Standard konektorea.":::

   Atributu gehiago gehitu nahi badituzu, hautatu **Gehitu atributua**. Helburuaren izena iturburuko eremuaren izenarekin desberdina izan daiteke, segmentuen irteera ikusleen ikuspegietatik mapatu ahal izateko Adobe Campaign Standard eremuek bi sistemetan izen bera ez badute.

   > [!NOTE]
   > Helbide elektronikoa identitate-eremu gisa erabiltzen da, baina ikusleen bezeroaren profileko beste edozein identifikatzaile erabil dezakezu datuak mapatzeko Adobe Campaign Standard.

1. Sakatu **Gorde**.

Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Datuak** > **Esportazioak**.

Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#run-exports-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).

> [!NOTE]
> Ziurtatu esportatutako segmentuan erregistro kopurua zure baimendutako mugaren barruan dagoela Adobe Campaign Standard lizentzia.

Esportatutako datuak goian konfiguratu duzun Azure blob Storage edukiontzian gordetzen dira. Karpeta bide hau automatikoki sortzen da zure edukiontzian:

*%ContainerName%/CustomerInsights_%instanceID%/% exportdestination-name%_%segmentname%_%timestamp%.csv*

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv

## <a name="configure-adobe-campaign-standard"></a>Konfiguratu Adobe Campaign Standard

Audientzia estatistiketatik ateratako segmentu bat esportatzen denean, aurreko urratsean esportazio-helmuga definitzen zenuen bitartean aukeratu dituzun zutabeak ditu. Datu hauek erabil daitezke [profilak sortu Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).

Atalean erabiltzeko Adobe Campaign Standard, profilaren eskema hemen zabaldu behar dugu Adobe Campaign Standard bi eremu gehigarri sartzeko. Ikasi nola egin [profila baliabidea luzatu](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) eremu berriekin Adobe Campaign Standard.

Gure adibidean, eremu hauek dira *Segmentuaren izena eta segmentuaren data (aukerakoa)*.

Eremu hauek profilak identifikatzeko erabiliko ditugu Adobe Campaign Standard honetara bideratu nahi duguna.

Beste dokumenturik ez badago Adobe Campaign Standard, inportatzera zoazenaz aparte, urrats hau salta dezakezu.

## <a name="import-data-into-adobe-campaign-standard"></a>Inportatu datuak Adobe Campaign Standard

Dena indarrean dagoenean, prestatutako audientzia datuak inportatu behar ditugu ikusleen estatistiketatik Adobe Campaign Standard profilak sortzeko. Ikasi [profilak nola inportatu Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences) lan-fluxua erabiliz.

Beheko irudiko inportazio lan-fluxua zortzi orduro exekutatzeko eta esportatutako audientzia estatistiken segmentuak bilatzeko konfiguratu da (.csv fitxategia Azure Blob Storage). Lan-fluxuak .csv fitxategiaren edukia zehaztutako zutabe ordenan ateratzen du. Lan-fluxu hau oinarrizko erroreak kudeatzeko eta erregistro bakoitzak helbide elektronikoa duela ziurtatzeko sortu da, datuak hidratatu aurretik Adobe Campaign Standard. Lan-fluxuak segmentuaren izena fitxategi-izenetik ateratzen du Adobe Campaign Standard profileko datuetara sartu aurretik.

:::image type="content" source="media/ACS-import-workflow.png" alt-text="Inportazio lan fluxuaren pantaila argazkia Adobe Campaign Standard erabiltzaile interfazea.":::

## <a name="retrieve-the-audience-in-adobe-campaign-standard"></a>Eskuratu audientzia bertan Adobe Campaign Standard

Datuak inportatu ondoren Adobe Campaign Standard, zuk [lan fluxua sor dezakezu](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) eta [kontsulta](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) bezeroak oinarritzat hartuta *Segmentuaren izena* eta *Segmentuaren Data* gure lagin kanpainarako identifikatutako profilak hautatzeko.

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a>Sortu eta bidali mezu elektronikoa erabiliz Adobe Campaign Standard

Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Posta elektronikoaren adibidea berritze eskaintzarekin Adobe Campaign Standard.":::
