---
title: Aberastea Experian hirugarrenen aberastearekin
description: Experian-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 9cf2a7fa18ecc022ea67f6829f52381ad59f3172
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5896358"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a>Aberastu bezeroen profilak demografiarekin Experian-etik (aurrebista)

Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta marketin zerbitzuetan. Batera Experianen datuak aberasteko zerbitzuak, zure bezeroen ulermen sakona sor dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.

## <a name="prerequisites"></a>Aurrebaldintzak

Experian konfiguratzeko, honako baldintza hauek bete behar dira:

- Experian harpidetza aktiboa duzu. Harpidetza lortzeko, [jarri harremanetan Experian-ekin](https://www.experian.com/marketing-services/contact) zuzenean. [Ikasi gehiago Experian datu-aberasteari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).

- Administratzaile batek dagoeneko Experian konexioa konfiguratu du *edo* duzu [administratzailea](permissions.md#administrator) baimenak. Experianek zuretzako sortu duen SSH gaitutako Garraio Seguru (ST) konturako Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia ere behar dituzu.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Aukeratu **Aberastu nire datuak** Experian fitxan.

   > [!div class="mx-imgBorder"]
   > ![Teila Experian](media/experian-tile.png "Teila Experian")
   > 

1. Hautatu [konexioa](connections.md) goitibeherako zerrendatik. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, sor dezakezu konexioa hautatuz **Gehitu konexioa** eta aukeratuz Experian goitibeherako zerrendan. 

1. Aukeratu **Konektatu Experian** konexioaren hautapena berresteko.

1.  Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** Experian datu demografikoekin aberastu nahi duzu. **Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

    :::image type="content" source="media/enrichment-Experian-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Aukeratu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu mota erabili behar diren Experian-eko datu demografikoak bat datozen bilatzeko. Eremuetako bat gutxienez **Izena eta helbidea**, **Mugikorra**, edo **Posta elektronikoa** beharrezkoa da. Partiduen zehaztasun handiagoa lortzeko, beste bi eremu gehi daitezke. Aukeraketa honek hurrengo urratsean atzitu ditzakezun mapen eremuei eragingo die.

    > [!TIP]
    > Litekeena da Experian-era bidalitako gako identifikatzaile atributu gehiagok bat etortze tasa handiagoa lortzea.

1. Hautatu **Hurrengoa** eremuaren jarraipena hasteko.

1. Definitu zure profil bateratuetako zein eremu mota erabili behar diren Experian-eko datu demografikoak bat datozen bilatzeko. Eskatutako eremuak markatuta daude.

1. Hornitu aberasturako izena eta irteerako entitatearen izena.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="configure-the-connection-for-experian"></a>Konfiguratu konexioa Experian-erako 

Administratzailea izan behar duzu konexioak konfiguratzeko. Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** Experian fitxan.

1. Hautatu **Hasi erabiltzen**.

1. Idatzi konexioaren izena **Bistaratzeko izena** kutxa.

1. Idatzi baliozko Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia Experian Secure Transport konturako.

1. Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitu ondoren, hautatu **Gorde**.
   
   :::image type="content" source="media/enrichment-Experian-connection.png" alt-text="Experian konexioa konfigurazioaren panela.":::

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren eta Experian-ek zure konturako aberastutako prozesuen araberakoa izango da.

Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Experian-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Experian-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
