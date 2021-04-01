---
title: Aberastea Experian hirugarrenen aberastearekin
description: Experian-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 12/10/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 4d4723e8f793ee857c4f5204a42be8338c71d4c3
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597772"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a>Aberastu bezeroen profilak demografiarekin Experian-etik (aurrebista)

Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta marketin zerbitzuetan. Batera Experianen datuak aberasteko zerbitzuak, zure bezeroen ulermen sakona sor dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.

## <a name="prerequisites"></a>Aurrebaldintzak

Experian konfiguratzeko, honako baldintza hauek bete behar dira:

- Experian harpidetza aktiboa duzu. Harpidetza lortzeko, [jarri harremanetan Experian-ekin](https://www.experian.com/marketing-services/contact) zuzenean. [Ikasi gehiago Experian datu-aberasteari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).
- Experian-ek sortu duen SSH gaitutako Garraio Seguru (ST) konturako Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia dituzu.
- Badituzu [Administratzaile](permissions.md#administrator) baimenak hartzaileei buruzko xehetasunetan.

## <a name="configuration"></a>Konfigurazioa

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Aukeratu **Aberastu nire datuak** Experian fitxan.

   > [!div class="mx-imgBorder"]
   > ![Teila Experian](media/experian-tile.png "Teila Experian")

1. Aukeratu **Hasi** eta sartu Erabiltzailearen IDa, Alderdiaren IDa eta Modelo zenbakia Experian Secure Transport konturako. Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia. Berretsi sarrera guztiak hautatuta **Aplikatu**.

## <a name="map-your-fields"></a>Esleitu eremuak

1.  Aukeratu **Gehitu datuak** eta aukeratu Experian-eko enpresako datu demografikoekin aberastu nahi duzun **Bezeroaren datu multzoa**. **Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

1. Aukeratu zure gako identifikatzaileak **Izena eta helbidea**, **Helbide elektronikoa**, edo **Mugikorra** identitate-ebazpena Experian-era bidaltzeko.

   > [!TIP]
   > Litekeena da Experian-era bidalitako gako identifikatzaile atributu gehiagok bat etortze tasa handiagoa lortzea.

1. Aukeratu **Hurrengoa** eta mapatu dagozkien atributuak zure bezero entitate bateratuarekin hautatutako gako identifikatzailearen eremuetarako.

1. Aukeratu **Gehitu atributua** Experian-era bidali nahi dituzun atributu osagarriak mapatzeko.

1.  Aukeratu **Gorde** eremuaren mapa osatzeko.

    > [!div class="mx-imgBorder"]
    > ![Experian eremuaren esleipena](media/experian-field-mapping.png "Experian eremuaren esleipena")

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