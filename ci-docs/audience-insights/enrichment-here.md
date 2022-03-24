---
title: HERE Technologies Aberastea hirugarrenen aberastasunarekin
description: HERE Technologies-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: 1cbbad9bfe559bcb15b23894fc7475507aae8add
ms.sourcegitcommit: 50d32a4cab01421a5c3689af789e20857ab009c4
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376265"
---
# <a name="enrichment-of-customer-profiles-with-here-technologies-preview"></a>Bezeroen profilak aberastea HERE Technologies-ekin (aurrebista)

HERE Technologies kokapen-plataformako enpresa da, kokapenari buruzko datuak eta zerbitzuak eskaintzen dituena. HERE Technologies-en datuak aberasteko zerbitzuekin, zure bezeroen kokapen zehatzagoa ulertu ahal izango duzu helbide normalizazioarekin, latitudea eta longitudea erauztearekin eta abarrekin.

## <a name="prerequisites"></a>Aurrebaldintzak

HERE Technologies-en aberastea konfiguratzeko, honako baldintza hauek bete behar dira:

- HERE Technologies-en harpidetza aktiboa duzu. Harpidetza lortzeko, [erregistratu hemen](https://developer.here.com/sign-up?utm_medium=referral&utm_source=Microsoft-Dynamics-CI&create=Freemium-Basic) edo [jarri harremanetan HERE Technologies-ekin](https://developer.here.com/help?utm_medium=referral&utm_source=Microsoft-Dynamics-CI#how-can-we-help-you) zuzenean. [Lortu informazio gehiago HERE Technologies-en kokapen-aberasteari buruz.](https://developer.here.com/location-enrichment?cid=Dev-MicrosoftDynamics-DB-0-Dev-&utm_source=MicrosoftDynamics&utm_medium=referral&utm_campaign=Online_Dev_ReferralMicrosoft)

- HERE [konexioa](connections.md) eskuragarri dago *edo* duzu [administratzailea](permissions.md#admin) baimenak eta HERE Technologies API gakoa.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastua**. 

1. Aukeratu **Aberastu nire datuak** HERE Technologies fitxan eta hautatu **Hasi**.

   > [!div class="mx-imgBorder"]
   > ![HERE Technologies-en lauza.](media/HERE-tile.png "HERE Technologies-en lauza")

1. Hautatu goitibeherako zerrendako [konexio](connections.md) bat. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, hautatuz konexioa sor dezakezu **Gehitu konexioa**. Aukeratu **HERE Technologies** goitibeherako zerrendatik. 

1. Aukeratu **Konektatu HERE Teknologietara** hautapena berresteko.

1.  Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** HERE Teknologien kokapen datuekin aberastu nahi duzu. **Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

    :::image type="content" source="media/enrichment-HERE-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Aukeratu eremuak lehen eta/edo bigarren helbidera esleitu nahi dituzun. Bi helbideen eremuen mapak zehaztu ditzakezu eta bi helbideen profilak bereiz aberastu. Adibidez, etxea eta negozioaren helbidea badaude. Hautatu **Hurrengoa**.

1. Zehaztu zure profil bateratuetako zein eremu erabili beharko liratekeen HERE Technologies-en bat datozen kokapen datuak bilatzeko. **1. kalea** eta **Zip / Posta Kodea** eremuak derrigorrezkoak dira hautatutako lehen eta / edo bigarren mailako helbidean. Bat-etortze zehatzagoak lortzeko, eremu gehiago gehitu daitezke.

   > [!div class="mx-imgBorder"]
   > ![HERE Technologies-en aberastearen konfigurazio orria.](media/enrichment-HERE-configuration.png "HERE Technologies-en aberastearen konfigurazio orria")

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Idatzi aberastearen izena. 

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="configure-the-connection-for-here-technologies"></a>Konfiguratu konexioa HERE Technologies 

Administratzailea izan behar duzu konexioak konfiguratzeko. Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** HERE Technologies fitxan.

1. Idatzi konexioaren izena **Bistaratzeko izena** kutxa.

1. Eman baliozko HERE Technologies API gakoa.

1. Berrikusi eta eman zure baimena **Datuen pribatutasuna eta betetzea** hautatuz **Ados**.

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitu ondoren, hautatu **Gorde**.

   > [!div class="mx-imgBorder"]
   > ![HEMEN teknologien konexioa konfigurazioaren orria.](media/enrichment-HERE-connection.png "HEMEN teknologien konexioa konfigurazioaren orria")

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren eta HERE Technologies-en APIaren erantzun denboren araberakoa izango da.

Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](../includes/next-steps-enrichment.md)]

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak HERE Technologies-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da HERE Technologies-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
