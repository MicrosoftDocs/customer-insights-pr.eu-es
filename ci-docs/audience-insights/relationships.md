---
title: Entitateen eta entitateen bide-izenen arteko erlazioak
description: Sortu eta kudeatu datu-iturburu anitzetako entitateen arteko harremanak.
ms.date: 04/14/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
ms.openlocfilehash: c25bfcb8e2a8223498dd1a5e8cfb3712a40ab85e
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5595197"
---
# <a name="relationships-between-entities"></a>Harremanak entitateen artean

Harremanek entitateak lotzen eta zure datuen grafikoa sortzen laguntzen dute entitateek entitate batetik bestera erreferentzia daitekeen identifikatzaile komun bat (atzerriko gakoa) partekatzen dutenean. Konektatutako entitateek datu-iturri anitzetan oinarritutako segmentuak eta neurriak definitzeko aukera ematen dute.

Bi harreman-mota daude: Editatu gabeko sistema-harremanak, automatikoki sortzen direnak eta erabiltzaileek sortutako eta konfiguratutako harreman pertsonalizatuak.

Partiduen eta bateratze prozesuen artean, sistemen arteko harremanak agertokien atzean sortzen dira, bat etorri adimentsuan oinarrituta. Harreman hauek Bezeroaren Profilaren erregistroak dagozkien beste erakundeen erregistroekin erlazionatzen lagunduko dute. Hurrengo diagrama honetan, hiru sistema harreman sortu dira, bezero entitatea entitate osagarriekin lotzen denean Bezeroaren azken profila entitatea ekoizteko.

> [!div class="mx-imgBorder"]
> ![Erlazioak sortzen](media/relationships-entities-merge.png "Erlazioak sortzen")

- ***CustomerToContact* harremana** Bezeroaren entitatearen eta Harremanetarako entitatearen artean sortu zen. Bezero entitateak giltza eremua lortzen du **Contact_contactId** Harremanetarako entitatearen gako eremua erlazionatzeko **contactId**.
- ***CustomerToAccount* harremana** Bezeroaren entitatearen eta konturako entitatearen artean sortu zen. Bezero entitateak giltza eremua lortzen du **Account_contactId** Konturako entitatearen gako eremua erlazionatzeko **accountId**.
- ***CustomerToWebAccount* harremana** Bezeroaren entitatearen eta web-konturako entitatearen artean sortu zen. Bezero entitateak giltza eremua lortzen du **WebAccount_contactId** Web-Konturako entitatearen gako eremua erlazionatzeko **webaccountId**.

## <a name="create-a-relationship"></a>Sortu erlazioa

Definitu harreman pertsonalizatuak **Harremanak** orria. Harreman bakoitza Iturri entitate batek (atzerriko giltza duen entitatea) eta Xede entitate batek (iturri erakundearen atzerriko gakoa adierazten duen entitatea) osatzen dute.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Harremanak**.

2. Hautatu **Harreman berria**.

3. **Gehitu harremana** panelean, eman ondorengo informazioa:

   > [!div class="mx-imgBorder"]
   > ![Sartu harremanaren xehetasunak](media/relationships-add.png "Sartu harremanaren xehetasunak")

   - **Harreman izena**: Harremanaren xedea islatzen duen izena (adibidez, **AccountWebLogs**).
   - **Deskribapena**: Erlazio-funtzioaren azalpena.
   - **Iturri entitatea**: Harremanean iturri gisa erabiltzen den entitatea hautatu (adibidez, WebLog).
   - **Kardinalitatea**: Iturri entitatearen erregistroen kardinalitatea aukeratu. Adibidez, "askok" esan nahi du Weblog erregistro anitz WebAccount-ekin erlazionatuta daudela.
   - **Iturriaren gako eremua**: Iturri-erakundeko atzerriko gako-eremua adierazten du. Adibidez, WebLog-ek dauka **accountId** atzerriko gako eremua.
   - **Helmugako entitatea**: Harremanean helmuga gisa erabiltzen den entitatea hautatu (adibidez, WebAccount).
   - **Helmugako kardinalitatea**: helmugako entitatearen erregistroen kardinalitatea aukeratu. Adibidez, "bat" esan nahi du Weblog erregistro anitz WebAccount-ekin erlazionatuta daudela.
   - **Helburuko gako eremua**: Eremu honek xede entitatearen funtsezko eremua adierazten du. Adibidez, WebAccount-ek dauka **accountId** gako eremua.

> [!NOTE]
> Banan-banan eta banan-banako harremanak bakarrik onartzen dira. Asko eta asko harremanak bat eta bi erlazio eta lotura-entitate bat (iturri-entitatea eta xede-entitatea konektatzeko erabiltzen den entitatea) sor daitezke.

## <a name="delete-a-relationship"></a>Ezabatu erlazioa

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Harremanak**.

2. Hautatu ezabatu nahi dituzun harremanen kontrol-laukiak.

3. Aukeratu **Ezabatu** goialdean **Harremanak** mahaia.

4. Berretsi ezabatu nahi duzula.

## <a name="next-step"></a>Hurrengo urratsa

Sistema eta pertsonalizatutako harremanak sekretuak isilik ez dituzten datu iturri anitzetan oinarritutako segmentuak sortzeko erabiltzen dira. Informazio gehiago lortzeko, [Segmentuak](segments.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]