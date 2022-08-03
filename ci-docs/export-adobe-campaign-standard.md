---
title: Esportatu Customer Insights segmentuak hona Adobe Kanpainaren estandarra (aurrebista)
description: Ikasi nola erabiltzen diren Customer Insights segmentuak Adobe Kanpainaren estandarra.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: antando
manager: shellyha
ms.openlocfilehash: 834880cac9c5023157983081ff2513d9b051491f
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195505"
---
# <a name="export-customer-insights-segments-to-adobe-campaign-standard-preview"></a>Esportatu Customer Insights segmentuak hona Adobe Kanpainaren estandarra (aurrebista)

Esportatu publiko garrantzitsuei zuzendutako segmentuak Adobe Kanpainaren estandarra.

:::image type="content" source="media/ACS-flow.png" alt-text="Artikulu honetan azaldutako urratsen prozesuaren diagrama.":::

## <a name="prerequisites"></a>Aurrebaldintzak

- An Adobe Kanpainaren lizentzia estandarra.
- An [Azure Blob Storage kontua](/azure/storage/blobs/create-data-lake-storage-account) izena eta kontu-gakoa. Izena eta gakoa aurkitzeko, ikus [Kudeatu biltegiratze-kontuaren ezarpenak Azure atarian](/azure/storage/common/storage-account-manage).
- An [Azure Blob biltegiratze edukiontzia](/azure/storage/blobs/storage-quickstart-blobs-portal#create-a-container).

## <a name="campaign-overview"></a>Kanpainaren informazio orokorra

Customer Insights-eko segmentuak nola erabil ditzakezun hobeto ulertzeko Adobe Experience Platform, ikus dezagun fikziozko lagin-kanpaina bat.

Demagun zure enpresak hilero harpidetzan oinarritutako zerbitzua eskaintzen diela Estatu Batuetako bezeroei. Datozen zortzi egunetan harpidetzak berritzekoak diren baina oraindik harpidetza berritu ez duten bezeroak identifikatu nahi dituzu. Bezero hauek mantentzeko, posta elektroniko bidez promozio eskaintza bidali nahi diezu Adobe Campaign Standard.

Adibide honetan, promozioko posta elektronikoko kanpaina behin exekutatu nahi dugu. Artikulu honek ez du kanpaina behin baino gehiagotan egitearen erabilera kasua jasotzen. Hala ere, Customer Insights eta Adobe Kanpaina Estandarra konfigura daiteke kanpaina errepikakorren agertoki baterako ere lan egiteko.

## <a name="identify-your-target-audience"></a>Identifikatu zure xede-publikoa

Gure eszenatokian, bezeroen helbide elektronikoak Customer Insights-en eskuragarri daudela suposatzen dugu eta haien sustapen-hobespenak aztertu dira segmentuko kideak identifikatzeko.

The [Customer Insights-en definitu duzun segmentua](segments.md) deitzen da **ChurnProneCustomers** eta bezero horiei posta elektronikoko promozioa bidaltzeko asmoa duzu.

:::image type="content" source="media/churn-prone-customers-segment.png" alt-text="ChurnProneCustomers segmentuarekin sortutako segmentuen orriaren pantaila-argazkia.":::

Bidali nahi duzun eskaintza helbidean izen, abizen, eta bezeroaren harpidetzaren amaiera data egongo dira. Bezeroei harpidetza amaitu baino lehen berritzen badute lortuko duten deskontuaren berri ematen die.

## <a name="export-your-target-audience"></a>Esportatu zure xede-publikoa

### <a name="set-up-connection-to-adobe-campaign"></a>Konfiguratu konexioa Adobe Kanpaina

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Adobe Kanpaina**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu **Kontuaren izena**, **gakoa**, eta **Edukiontzia** zure Blob Storage konturako.  

   :::image type="content" source="media/azure-blob-configuration.png" alt-text="Biltegiratze kontuaren konfigurazioaren pantaila-argazkia. ":::

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

### <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremua, aukeratu konexioa Adobe Campaign atalean. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Aukeratu esportatu nahi duzun segmentua. Adibide honetan, **ChurnProneCustomers** da.

   :::image type="content" source="media/select-segment-churnpronecustomers.png" alt-text="ChurnProneCustomers segmentu hautatutako segmentu aukeraketa erabiltzailearen interfazearen pantaila.":::

1. Hautatu **Hurrengoa**.

1. Mapa **Iturria** Customer Insights segmentutik eremuetara **Helburua** eremuko izenak Adobe Kanpainaren profil estandarraren eskema.

   :::image type="content" source="media/ACS-field-mapping.png" alt-text="Eremurako mapak Adobe Campaign Standard konektorea.":::

   Atributu gehiago gehitu nahi badituzu, hautatu **Gehitu atributua**. Xede-izena iturburu-eremuaren izenaren aldean desberdina izan daiteke, Customer Insights-en segmentu-irteera oraindik ere mapatu ahal izateko Adobe Kanpaina estandarra eremuek bi sistemetan izen bera ez badute.

   > [!NOTE]
   > Helbide elektronikoa identitate eremu gisa erabiltzen da, baina bezeroaren profileko beste edozein identifikatzaile erabil dezakezu datuak mapatzeko Adobe Kanpainaren estandarra.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

> [!NOTE]
> Ziurtatu esportatutako segmentuan erregistro kopurua zure baimendutako mugaren barruan dagoela Adobe Campaign Standard lizentzia.

Esportatutako datuak goian konfiguratu duzun Azure blob Storage edukiontzian gordetzen dira. Karpeta bide hau automatikoki sortzen da zure edukiontzian: *%ContainerName% /CustomerInsights_%instanceID% /% export destination-name%_%segmentname%_%timestamp% .csv*

Adibidez: Dynamics365CustomerInsights/CustomerInsights_abcd1234-4312-11f4-93dc-24f72f43e7d5/ChurnSegmentDemo_ChurnProneCustomers_1613059542.csv

## <a name="configure-adobe-campaign-standard"></a>Konfiguratu Adobe Campaign Standard

Esportatutako segmentuek esportazioa konfiguratzean hautatu dituzun zutabeak dituzte. Datu hauek erabil daitezke [profilak sortu Adobe Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/about-profiles.html#managing-profiles).

Segmentua erabiltzeko Adobe Kanpaina estandarra, [profilaren eskema zabaldu](https://experienceleague.adobe.com/docs/campaign-standard/using/developing/use-cases--extending-resources/extending-the-profile-resource-with-a-new-field.html#developing) urtean Adobe Kanpainaren estandarra bi eremu gehiago sartzeko.

Gure adibidean, eremu hauek segmentuaren izena eta segmentuaren data dira. Eremu hauek profilak identifikatzeko erabiliko ditugu Adobe Campaign Standard honetara bideratu nahi duguna.

Beste erregistrorik ez badago Adobe Kanpainaren estandarra, inportatuko duzunaz gain, saltatu urrats hau.

## <a name="import-data-into-adobe-campaign-standard"></a>Inportatu datuak Adobe Campaign Standard

Inportatu Customer Insights-etik prestatutako audientzia-datuak Adobe Kanpaina Standard to [profilak sortu lan-fluxu bat erabiliz](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/creating-profiles.html#profiles-and-audiences).

Beheko irudiko inportazio-fluxua zortzi orduro exekutatzeko konfiguratu da eta esportatutako Customer Insights segmentuak bilatzeko (.csv fitxategia Azure Blob biltegian). Lan-fluxuak .csv fitxategiaren edukia zehaztutako zutabe ordenan ateratzen du. Lan-fluxu hau oinarrizko erroreak kudeatzeko eta erregistro bakoitzak helbide elektronikoa duela ziurtatzeko sortu da, datuak hidratatu aurretik Adobe Campaign Standard. Lan-fluxuak segmentuaren izena fitxategi-izenetik ateratzen du Adobe Campaign Standard profileko datuetara sartu aurretik.

:::image type="content" source="media/ACS-import-workflow.png" alt-text="Inportazio lan fluxuaren pantaila argazkia Adobe Campaign Standard erabiltzaile interfazea.":::

## <a name="retrieve-the-audience-in-adobe-campaign-standard"></a>Eskuratu audientzia bertan Adobe Campaign Standard

Datuak inportatu ondoren Adobe Kanpaina estandarra, [lan-fluxu bat sortu](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/workflow-general-operation/building-a-workflow.html#managing-processes-and-data) eta [kontsulta](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/targeting-activities/query.html#managing-processes-and-data) bezeroek Segmentuaren Izenan eta Segmentuaren Datan oinarrituta gure lagin-kanpainarako identifikatutako profilak hautatzeko.

## <a name="create-and-send-the-email-using-adobe-campaign-standard"></a>Sortu eta bidali mezu elektronikoa erabiliz Adobe Campaign Standard

Sortu mezu elektronikoaren edukia eta gero [probatu eta bidali](https://experienceleague.adobe.com/docs/campaign-standard/using/testing-and-sending/get-started-sending-messages.html#preparing-and-testing-messages) zure emaila.

:::image type="content" source="media/contoso-sample-email.jpg" alt-text="Posta elektronikoaren adibidea berritze eskaintzarekin Adobe Campaign Standard.":::

[!INCLUDE [footer-include](includes/footer-banner.md)]
