---
title: Aberastea hirugarrenen aberastasunarekin Experian
description: -Ri buruzko informazio orokorra Experian hirugarrenen aberastea.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: ad1023135516ca9c49818d19aa84df68d16b2e3c
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8229949"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a>Aberastu bezeroen profilak datu demografikoekin Experian (aurrebista)

Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta merkaturatzeko zerbitzuetan. Batera Experian Datuak aberasteko zerbitzuak, zure bezeroen ezagutza sakonagoa eraiki dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.

## <a name="prerequisites"></a>Aurrebaldintzak

Konfiguratzeko Experian, honako baldintza hauek bete behar dira:

- Experian harpidetza aktiboa izan behar duzu. Harpidetza lortzeko, [harremanetarako Experian](https://www.experian.com/marketing-services/contact) zuzenean. [Lortu informazio gehiago Experian datuen eraginari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).

- Administratzaile batek Experian konexioa konfiguratu du dagoeneko *edo* duzu [administratzailea](permissions.md#administrator) baimenak. Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia ere behar dituzu SSH gaitutako Garraio Seguru (ST) konturako Experian zuretzat sortua.

## <a name="supported-countriesregions"></a>Lagundutako herrialde / eskualdeak

Gaur egun, Estatu Batuetan bezeroen profil aberasgarriak onartzen ditugu.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Aukeratu **Aberastu nire datuak** gainean Experian teila.

   > [!div class="mx-imgBorder"]
   > ![Experian lauza.](media/experian-tile.png "Experian lauza")
   > 

1. Hautatu goitibeherako zerrendako [konexio](connections.md) bat. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, konexioa sor dezakezu hautatuta **Gehitu konexioa** eta aukeratzea Experian goitibeherako zerrendatik. 

1. Aukeratu **Konektatu Experian** konexioaren hautapena berresteko.

1.  Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** datu demografikoekin aberastu nahi duzu Experian-etik. **Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

    :::image type="content" source="media/enrichment-Experian-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Aukeratu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu mota erabili behar diren datu demografikoekin bat datozenak bilatzeko Experian. Eremuetako bat gutxienez **Izena eta helbidea**, **Mugikorra**, edo **Posta elektronikoa** beharrezkoa da. Partiduen zehaztasun handiagoa lortzeko, beste bi eremu gehi daitezke. Aukeraketa honek hurrengo urratsean atzitu ditzakezun mapen eremuei eragingo die.

    > [!TIP]
    > Gako identifikatzaile atributu gehiago bidali dira Experian litekeena da partida-tasa handiagoa lortzea.

1. Hautatu **Hurrengoa** eremuaren jarraipena hasteko.

1. Zehaztu profil bateratuetako zein eremu mota erabili behar diren datu demografikoekin bat datozenak bilatzeko Experian. Eskatutako eremuak markatuta daude.

1. Hornitu aberasturako izena eta irteerako entitatearen izena.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="configure-the-connection-for-experian"></a>Konfiguratu konexio-funtzioak Experian-en 

Administratzailea izan behar duzu konexioak konfiguratzeko. Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** gainean Experian lauza.

1. Hautatu **Hasi erabiltzen**.

1. Idatzi konexioaren izena **Bistaratzeko izena** kutxa.

1. Idatzi baliozko Erabiltzaile IDa, Alderdiaren IDa eta Modelo Zenbakia Experian Garraio Seguruaren kontua.

1. Berrikusi eta eman zure baimena **Datuen pribatutasuna eta betetzea** hautatuz **Ados**.

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitu ondoren, hautatu **Gorde**.
   
   :::image type="content" source="media/enrichment-Experian-connection.png" alt-text="Experian konexioaren konfigurazio-panela.":::

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren eta zure konturako aberastutako prozesuen araberakoa izango da Experian.

Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](../includes/next-steps-enrichment.md)]

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko Experian, datuak betetze mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz Experian izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
