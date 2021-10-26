---
title: Enpresako profilak aberastea hirugarrenen Leadspace aberastearekin
description: Leadspace-ren hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 09/30/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: c57eb0ceb50e3b778acac72a4bbfd733a5b0c401
ms.sourcegitcommit: 23c8973a726b15050e368cc6e0aab78b266a89f6
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/08/2021
ms.locfileid: "7617336"
---
# <a name="enrichment-of-company-profiles-with-leadspace-preview"></a>Enpresen profilak aberastea Leadspace-rekin (aurrebista)

Leadspace B2B Bezeroaren Datuen Plataforma eskaintzen duen datuen zientzia enpresa da. Kontuetan oinarritutako bezeroen profil bateratuak dituzten inguruneak ahalbidetzen ditu beren datuak aberasteko. Aberastu *Bezeroen profilak* enpresaren tamaina, kokapena edo industria bezalako atributuekin. Aberastu *Harremanetarako profilak* izenburua, pertsona edo posta elektronikoa egiaztatzea bezalako atributuekin.

## <a name="prerequisites"></a>Aurrebaldintzak

Leadspace konfiguratzeko eta konfiguratzeko, honako baldintza hauek bete behar dira:

- Leadspace lizentzia aktiboa duzu.
- Baduzu [bezeroen profil bateratuak](customer-profiles.md) kontuetan oinarrituta.
- Administratzaile batek konfiguratu du dagoeneko Leadspace konexioa edo zuk [administratzailea](permissions.md#administrator) baimenak eta "betiko giltza" (aipatzen da **Leadspace token**). Harremanetarako [Leadspace](https://www.leadspace.com/leadspace-microsoft-dynamics-365/) zuzenean produktuaren inguruko xehetasunak lortzeko.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Aberastea**.

1. Aukeratu **Aberastu nire datuak** Leadspace fitxan eta hautatu **Hasi**.

   :::image type="content" source="media/leadspace-tile.png" alt-text="Leadspace lauzaren pantaila-argazkia.":::

1. Hautatu goitibeherako zerrendako [konexio](connections.md) bat. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, sor dezakezu konexioa **Gehitu konexioa** hautatuz eta **Leadspace** aukeratuz. 

1. Aukeratu **Konektatu Leadspace** konexioa berresteko.

1. Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** Leadspace konpainiaren datuekin aberastu nahi duzu. **Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

    :::image type="content" source="media/enrichment-Leadspace-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. Aukeratu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu mota erabili behar diren Leadspace-ko konpainiaren datuak bat datozen bilatzeko. **Enpresaren izena** eremua beharrezkoa da. Bat-etortzeen zehaztasun handiagoa lortzeko, beste bi eremu, **Enpresaren webgunea** eta **Enpresaren kokapena**, gehitu daitezke.

   :::image type="content" source="media/enrichment-leadspace-mapping.png" alt-text="Leadspace eremuak esleitzeko panela.":::

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Hautatu kontrol laukia baduzu *Harremanetarako profilak* aberastu nahiko zenukeela. Ikusleen estatistikek beharrezko eremuak automatikoki mapatuko dituzte.

   :::image type="content" source="media/enrichment-leadspace-contacts.png" alt-text="Leadspace kontaktuak aberastu egiten du.":::
 
1. Eman aberasturako izena eta hautatu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.


## <a name="configure-the-connection-for-leadspace"></a>Konfiguratu konexioa Leadspace-rako 

Administratzailea izan behar duzu konexioak konfiguratzeko. Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** Leadspace fitxan.

1. Hautatu **Hasi erabiltzen**. 

1. Idatzi konexioaren izena **Bistaratzeko izena** kutxa.

1. Hornitu balizoko Leadspace tokena.

1. Berrikusi eta eman zure baimena **Datuen pribatutasuna eta betetzea** hautatuz **Ados**.

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitu ondoren, hautatu **Gorde**.
   
   :::image type="content" source="media/enrichment-Leadspace-connection.png" alt-text="Leadspace konexioa konfigurazioaren orria.":::

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberastea freskatu ondoren, azpian dagoen enpresa aberastutako datuak berrikus ditzakezu [Nire aberastasunak](enrichment-hub.md). Azken eguneraketaren ordua eta aberastutako profil kopurua aurki ditzakezu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

Informazio gehiago lortzeko, ikus [Leadspace API](https://support.leadspace.com/hc/en-us/sections/201997649-API).

## <a name="next-steps"></a>Hurrengo urratsak


[!INCLUDE [next-steps-enrichment](../includes/next-steps-enrichment.md)]

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Leadspace-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Leadspace-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Dynamics 365 Customer Insights administratzailea edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
