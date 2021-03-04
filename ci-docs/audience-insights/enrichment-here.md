---
title: HERE Technologies hirugarrenen aberastearekin aberastea
description: HERE Technologies-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 12/10/2020
ms.reviewer: jodahl
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 258e37de9d9685d9ebc30b3c6b8d238d583431b4
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269499"
---
# <a name="enrichment-of-customer-profiles-with-here-technologies-preview"></a>Bezeroen profilak aberastea HERE Technologies-ekin (aurrebista)

HERE Technologies kokapen-plataformako enpresa da, kokapenari buruzko datuak eta zerbitzuak eskaintzen dituena. HERE Technologies-en datuak aberasteko zerbitzuekin, zure bezeroen kokapen zehatzagoa ulertu ahal izango duzu helbide normalizazioarekin, latitudea eta longitudea erauztearekin eta abarrekin.

## <a name="prerequisites"></a>Aurrebaldintzak

HERE Technologies-en aberastea konfiguratzeko, honako baldintza hauek bete behar dira:

- HERE Technologies-en harpidetza aktiboa duzu. Harpidetza lortzeko, [erregistratu hemen](https://developer.here.com/sign-up?utm_medium=referral&utm_source=Microsoft-Dynamics-CI&create=Freemium-Basic) edo [jarri harremanetan HERE Technologies-ekin](https://developer.here.com/help?utm_medium=referral&utm_source=Microsoft-Dynamics-CI#how-can-we-help-you) zuzenean. [Lortu informazio gehiago HERE Technologies-en kokapen-aberasteari buruz.](https://developer.here.com/location-enrichment?cid=Dev-MicrosoftDynamics-DB-0-Dev-&utm_source=MicrosoftDynamics&utm_medium=referral&utm_campaign=Online_Dev_ReferralMicrosoft)

- HERE Technologies-en API gakoa duzu.

- [Administratzaile](permissions.md#administrator) baimenak dituzu.

## <a name="configuration"></a>Konfigurazioa

1. Joan **Datuak** > **Aberastua**.

1. Hautatu **aberastu datuak** HERE Technologies-en lauzan.

   > [!div class="mx-imgBorder"]
   > ![HERE Technologies-en lauza](media/HERE-tile.png "HERE Technologies-en lauza")

1. Sartu **HERE Technologies API gako** aktibo bat. Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia. 

1. Berretsi bi sarrerak **Konektatu HERE-ra** hautatuta.

1.  Aukeratu **Gehitu datuak** eta aukeratu HERE Technologies-eko enpresako datuekin aberastu nahi duzun **Bezeroaren datu multzoa**. **Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

    :::image type="content" source="media/enrichment-HERE-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Aukeratu eremuak lehen eta/edo bigarren helbidera esleitu nahi dituzun. Bi helbideen eremuen esleipena zehaztu ditzakezu (adibidez, etxeko eta negozioaren helbidea) eta bi helbideen profilak bereiz aberastu. Hautatu **Hurrengoa**.

1. Zehaztu zure profil bateratuetako zein eremu erabili beharko liratekeen HERE Technologies-en bat datozen kokapen datuak bilatzeko. **1. kalea** eta **Zip / Posta Kodea** eremuak derrigorrezkoak dira hautatutako lehen eta / edo bigarren mailako helbidean. Bat-etortze zehatzagoak lortzeko, eremu gehiago gehitu daitezke.

   > [!div class="mx-imgBorder"]
   > ![HERE Technologies-en aberastearen konfigurazio orria](media/enrichment-HERE-configuration.png "HERE Technologies-en aberastearen konfigurazio orria")

1. Aukeratu **Aplikatu** eremuen esleipena osatzeko.

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren eta HERE Technologies-en APIaren erantzun denboren araberakoa izango da.

Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak HERE Technologies-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da HERE Technologies-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]