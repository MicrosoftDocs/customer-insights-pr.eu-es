---
title: Esportatu Customer Insights segmentuak hona Adobe Kanpainaren estandarra (aurrebista)
description: Ikasi nola erabiltzen diren Customer Insights segmentuak Adobe Kanpainaren estandarra.
ms.date: 03/29/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: 9915591cd969bf825f5d1669de43ed4f9953f898
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9082337"
---
# <a name="export-customer-insights-segments-to-adobe-campaign-standard-preview"></a>Esportatu Customer Insights segmentuak hona Adobe Kanpainaren estandarra (aurrebista)

-ren erabiltzaile gisa Dynamics 365 Customer Insights, baliteke segmentuak sortu izana zure marketin-kanpainak eraginkorragoak izan daitezen, publiko garrantzitsuak zuzenduta. Customer Insights-en segmentu bat erabiltzeko Adobe Experience Platform eta bezalako aplikazioak Adobe Kanpainaren estandarra, artikulu honetan azaltzen diren urrats batzuk jarraitu behar dituzu.

:::image type="content" source="media/ACS-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a>Aurrebaldintzak

- Dynamics 365 Customer Insights lizentzia
- Adobe Campaign Standard lizentzia
- Azure blob-biltegia kontua

## <a name="campaign-overview"></a>Kanpainaren informazio orokorra

Customer Insights-en segmentuak nola erabil ditzakezun hobeto ulertzeko Adobe Experience Platform, ikus dezagun fikziozko lagin-kanpaina bat.

Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei. Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu. Bezero hauek mantentzeko, posta elektroniko bidez promozio eskaintza bidali nahi diezu Adobe Campaign Standard.

Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu. Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen. Hala ere, Customer Insights eta Adobe Kanpaina estandarra errepikatzen den kanpainaren agertoki baterako ere konfigura daiteke.

## <a name="identify-your-target-audience"></a>Identifikatu zure xede-publikoa

Gure eszenatokian, bezeroen helbide elektronikoak eskuragarri daudela eta haien sustapen-hobespenak aztertu dira segmentuko kideak identifikatzeko.

The [Customer Insights-en definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero horiei posta elektronikoko promozioa bidaltzeko asmoa duzu.

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira. Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.

## <a name="export-your-target-audience"></a>Esportatu zure xede-publikoa

### <a name="configure-a-connection"></a>Konfiguratu konexioa

Gure xede-publikoa identifikatuta, esportazioa Azure Blob Storage kontu batera konfiguratu dezakegu.

1. Customer Insights atalean, joan hona **Admin** > **Konexioak**.

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

1. Orain mapatzen dugu **Iturria** Customer Insights segmentutik eremuetara **Helburua** eremuko izenak Adobe Kanpainaren profil estandarraren eskema.

   :::image type="content" source="media/ACS-field-mapping.png" alt-text="Eremurako mapak Adobe Campaign Standard konektorea.":::

   Atributu gehiago gehitu nahi badituzu, hautatu **Gehitu atributua**. Xede-izena iturburu-eremuaren izenaren aldean desberdina izan daiteke, Customer Insights-en segmentu-irteera oraindik ere mapatu ahal izateko Adobe Campaign Standard eremuek izen bera ez badute bi sistemetan.

   > [!NOTE]
   > Helbide elektronikoa identitate eremu gisa erabiltzen da, baina bezeroaren profileko beste edozein identifikatzaile erabil dezakezu datuak mapatzeko Adobe Kanpainaren estandarra.

1. Sakatu **Gorde**.

Esportazio helmuga gorde ondoren, aktibatuta aurkituko duzu **Datuak** > **Esportazioak**.

Orain egin dezakezu [esportatu segmentua eskariaren arabera](export-destinations.md#run-exports-on-demand). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md).

> [!NOTE]
> Ziurtatu esportatutako segmentuan erregistro kopurua zure baimendutako mugaren barruan dagoela Adobe Campaign Standard lizentzia.

Esportatutako datuak goian konfiguratu duzun Azure blob Storage edukiontzian gordetzen dira. Karpeta bide hau automatikoki sortzen da zure edukiontzian:

*%ContainerName%/CustomerInsights_%instanceID%/% exportdestination-name%_%segmentname%_%timestamp%.csv*

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv

## <a name="configure-adobe-campaign-standard"></a>Konfiguratu Adobe Campaign Standard

Esportatutako segmentuek aurreko urratsean esportazio-helmuga definitzean hautatu dituzun zutabeak dituzte. Datu hauek erabil daitezke [profilak sortu Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).

Atalean erabiltzeko Adobe Campaign Standard, profilaren eskema hemen zabaldu behar dugu Adobe Campaign Standard bi eremu gehigarri sartzeko. Ikasi nola egin [profila baliabidea luzatu](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) eremu berriekin Adobe Campaign Standard.

Gure adibidean, eremu hauek dira *Segmentuaren izena eta segmentuaren data (aukerakoa)*.

Eremu hauek profilak identifikatzeko erabiliko ditugu Adobe Campaign Standard honetara bideratu nahi duguna.

Beste dokumenturik ez badago Adobe Campaign Standard, inportatzera zoazenaz aparte, urrats hau salta dezakezu.

## <a name="import-data-into-adobe-campaign-standard"></a>Inportatu datuak Adobe Campaign Standard

Orain dena prest dagoela, Customer Insights-etik prestatutako audientzia-datuak inportatu behar ditugu Adobe Kanpaina estandarra profilak sortzeko. Ikasi [profilak nola inportatu Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences) lan-fluxua erabiliz.

Beheko irudiko inportazio-fluxua zortzi orduro exekutatzeko eta esportatutako Customer Insights segmentuak bilatzeko konfiguratu da (.csv fitxategia Azure Blob biltegian). Lan-fluxuak .csv fitxategiaren edukia zehaztutako zutabe ordenan ateratzen du. Lan-fluxu hau oinarrizko erroreak kudeatzeko eta erregistro bakoitzak helbide elektronikoa duela ziurtatzeko sortu da, datuak hidratatu aurretik Adobe Campaign Standard. Lan-fluxuak segmentuaren izena fitxategi-izenetik ateratzen du Adobe Campaign Standard profileko datuetara sartu aurretik.

:::image type="content" source="media/ACS-import-workflow.png" alt-text="Inportazio lan fluxuaren pantaila argazkia Adobe Campaign Standard erabiltzaile interfazea.":::

## <a name="retrieve-the-audience-in-adobe-campaign-standard"></a>Eskuratu audientzia bertan Adobe Campaign Standard

Datuak inportatu ondoren Adobe Campaign Standard, zuk [lan fluxua sor dezakezu](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) eta [kontsulta](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) bezeroak oinarritzat hartuta *Segmentuaren izena* eta *Segmentuaren Data* gure lagin kanpainarako identifikatutako profilak hautatzeko.

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a>Sortu eta bidali mezu elektronikoa erabiliz Adobe Campaign Standard

Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Posta elektronikoaren adibidea berritze eskaintzarekin Adobe Campaign Standard.":::
