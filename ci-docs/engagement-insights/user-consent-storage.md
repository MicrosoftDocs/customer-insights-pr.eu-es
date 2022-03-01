---
title: Kudeatu cookieak eta erabiltzaileen baimena erabiltzaileen datuak gordetzeko
description: Ezagutu nola erabiltzen diren cookieak eta erabiltzaileen baimena webguneko bisitariak identifikatzeko.
author: mochimochi016
ms.reviewer: mhart
ms.author: jefhar
ms.date: 10/30/2020
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: 7b3195a92c969ab36e5b43f4c2e4221ff477a0a8958838e1256528f58fe13dce
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036723"
---
# <a name="manage-cookies-and-user-consent"></a>Kudeatu cookieak eta erabiltzaileen baimena

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Dynamics 365 Customer Insights elkarreragin xehetasunen gaitasunak cookieak eta tokiko biltegia erabiltzen ditu (`localStorage`) webguneko bisitariak identifikatzeko.

Cookieak erabiltzaile batek webgunearekin dituen elkarreraginei buruzko informazio zatiak gordetzen dituzten fitxategi txikiak dira. Web arakatzaileetan gordetzen dira. Erabiltzaileek zure erabiltzaileek cookieak gordeta dituzten webgune bat bisitatzen dutenean, arakatzaileak zerbitzarira bidaltzen du informazio hori eta horrek erabiltzailearentzako bakarra den informazioa itzultzen du. Hau da, adibidez, lineako erosketa saskiak hautatutako artikuluak bertan gordetzeko aukera ematen duen teknologia, nahiz eta erabiltzaile batek webgunetik urrun nabigatu.

## <a name="user-consent"></a>Erabiltzailearen baimena

[Datuen Babeserako Arau Orokorra (DBAO)](/dynamics365/get-started/gdpr/) Europar Batasuneko (EB) araudia da, erakundeek erabiltzaileen pribatutasuna eta segurtasuna nola kudeatu behar duten agintzen duena. Cookiek askotan "datu pertsonalak" gordetzen edo biltzen dituzte, esate baterako DBAOk estaltzen duen lineako identifikatzailea. Zure negozioak EBko datu interesdunei enplegatzen eta / edo saltzen badie, DBAOk zuri eragiten dio. [Lortu informazio gehiago Microsoftek DBAO betetzea nola lagun zaitzakeen](https://www.microsoft.com/trust-center/privacy/gdpr-faqs).

Elkarreragin xehetasunak SDK-k cookieak edo bestelako informazio sentikorra gorde ahal izateko, zure erabiltzaileek baimena eman duten zehaztu behar duzu. Hau SDK abiaraztean gertatzen da.

Erabiltzailearen baimenik ez dagoela adierazten baduzu, SDK-k ez du inolako daturik gordeko eta ez ditu erabiltzaileen portaeraren jarraipena egiteko erabil daitezkeen gertaerak bidaliko. Aurretik gordetako datuak arakatzailetik ezabatuko dira.

Erabiltzailearen baimenik zehazten ez bada, SDK-k erabiltzaileak baimena eman duela suposatuko du. Horrek esan nahi du zuk (gure bezero gisa) SDK-n erabiltzaileen baimenaren balioa zehazten ez baduzu, datuak bilduko direla. Hala ere, erabiltzailearen baimenaren balioa "egia" izan behar dela zehazten baduzu, ez dira datuak bilduko erabiltzaile batek baimen esplizitua ematen ez badu edo ematen ez badu.

## <a name="visitor-data-storage-in-engagement-insights-capability"></a>Bisitarien datuak biltegiratzeko konpromisoen gaitasunean

### <a name="cookies"></a>Cookie-ak

- _msei
    - Erabiltzaile ID anonimoa gordetzen du. Cookie hau bezeroaren domeinuan ezartzen da eta 365 egunen buruan iraungitzen da.

### <a name="local-storage"></a>Tokiko biltegia

Elkarreragin xehetasunen gaitasunak tokiko biltegiratzea ere erabiltzen du (`localStorage`) sentikorrak ez diren datuen jarraipena egiteko. Datu hauek guztiz arakatzailean bertan gordetzen dira, zure zerbitzarietara edo zure zerbitzaritik trafikorik bidali gabe.

- *EISession.Id* 
    - Etengabeko erabiltzailearen saioari buruzko informazioa gordetzen du, hala nola, saioaren IDa, noiz hasi zen eta noiz iraungitzen den.
- *EISession.Previous*
    - Uneko saioan aurrez bisitatutako orrialdearen URLa gordetzen du.
    
Biltegiratze lokaleko gakoak ez dira automatikoki iraungitzen. SDK-k hurrengo saioan berrezarriko ditu.

## <a name="deleting-cookies"></a>Cookieak ezabatzen

Zure bezeroek eskuz ezabatu ditzakete cookieak eta tokiko biltegiratze gakoak arakatzaileen ezarpenen bidez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]