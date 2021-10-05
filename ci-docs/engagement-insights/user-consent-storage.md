---
title: Kudeatu cookieak eta erabiltzaileen baimena erabiltzaileen datuak Dynamics 365 Customer Insights-en gordetzeko
description: Ezagutu nola erabiltzen diren cookieak eta erabiltzaileen baimena webguneko bisitariak identifikatzeko.
author: mochimochi016
ms.reviewer: mhart
ms.author: jefhar
ms.date: 09/27/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: c824e50b723fe7f3b421048bb6ab96b7a9efc31f
ms.sourcegitcommit: f1e3cc51ea4cf68210eaf0210ad6e14b15ac4fe8
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558789"
---
# <a name="manage-cookies-and-user-consent"></a>Kudeatu cookieak eta erabiltzaileen baimena

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Dynamics 365 Customer Insights-en parte hartzearen xehetasunen gaitasunak cookieak erabiltzen ditu eta (`localStorage`) gakoak webguneko bisitariak identifikatzeko.

Cookieak erabiltzaile batek webgunearekin dituen elkarreraginei buruzko informazio zatiak gordetzen dituzten fitxategi txikiak dira. Web arakatzaileetan gordetzen dira. Erabiltzaileek zure erabiltzaileek cookieak gordeta dituzten webgune bat bisitatzen dutenean, arakatzaileak zerbitzarira bidaltzen du informazio hori eta horrek erabiltzailearentzako bakarra den informazioa itzultzen du. Hau da, adibidez, lineako erosketa saskiak hautatutako artikuluak bertan gordetzeko aukera ematen duen teknologia, nahiz eta erabiltzaile batek webgunetik urrun nabigatu.

## <a name="user-consent"></a>Erabiltzailearen baimena

[Datuen Babeserako Arau Orokorra (DBAO)](/dynamics365/get-started/gdpr/) Europar Batasuneko (EB) araudia da, erakundeek erabiltzaileen pribatutasuna eta segurtasuna nola kudeatu behar duten agintzen duena. Cookiek askotan "datu pertsonalak" gordetzen edo biltzen dituzte, esate baterako DBAOk estaltzen duen lineako identifikatzailea. Zure negozioak EBko datu interesdunei enplegatzen eta / edo saltzen badie, DBAOk zuri eragiten dio. [Lortu informazio gehiago Microsoftek DBAO betetzea nola lagun zaitzakeen](https://www.microsoft.com/trust-center/privacy/gdpr-faqs).

Elkarreragin xehetasunak SDK-k cookieak edo bestelako informazio sentikorra gorde ahal izateko, zure erabiltzaileek baimena eman duten zehaztu behar duzu. Hau SDK hasieratzean gertatzen da `userConsent` konfigurazioko eremua ezarrita.

Erabiltzailearen baimenik ez dagoela adierazten baduzu, SDK-k ez du inolako daturik gordeko eta ez ditu erabiltzaileen portaeraren jarraipena egiteko erabil daitezkeen gertaerak bidaliko. Aurretik gordetako datuak arakatzailetik ezabatuko dira.

Erabiltzailearen baimenik zehazten ez bada, SDK-k erabiltzaileak baimena eman duela suposatuko du. Horrek esan nahi du zuk (gure bezero gisa) SDK-n erabiltzaileen baimenaren balioa zehazten ez baduzu, datuak bilduko direla. Hala ere, erabiltzailearen baimenaren balioa "egia" izan behar dela zehazten baduzu, ez dira datuak bilduko erabiltzaile batek baimen esplizitua ematen ez badu edo ematen ez badu.

Jarraian kode zati dago web SDK hasieratzeko erabiltzailearen baimenarekin:
```js
<script>
  (function(a,t,i){var e="MSEI";var s="Analytics";var o=e+"queue";a[o]=a[o]||[];var r=a[e]||function(n){var t={};t[s]={};function e(e){while(e.length){var r=e.pop();t[s][r]=function(e){return function(){a[o].push([e,n,arguments])}}(r)}}var r="track";var i="set";e([r+"Event",r+"View",r+"Action",i+"Property",i+"User","initialize","teardown"]);return t}(i.name);var n=i.name;if(!a[e]){a[n]=r[s];a[o].push(["new",n]);setTimeout(function(){var e="script";var r=t.createElement(e);r.async=1;r.src=i.src;var n=t.getElementsByTagName(e)[0];n.parentNode.insertBefore(r,n)},1)}else{a[n]=new r[s]}if(i.user){a[n].setUser(i.user)}if(i.props){for(var c in i.props){a[n].setProperty(c,i.props[c])}}a[n].initialize(i.cfg)})(window,document,{
    src:"https://download.pi.dynamics.com/sdk/web/msei-1.min.js",
    name:"EiJS",
    cfg:{
      ingestionKey:"YOUR-INGESTIONKEY",
      autoCapture:{
        view:true,
        click:true
      },
      userConsent: true
    }
  });
</script>
```

## <a name="visitor-data-storage-in-engagement-insights-capability"></a>Bisitarien datuak biltegiratzeko konpromisoen gaitasunean

### <a name="cookies"></a>Cookie-ak

- _msei
    - Erabiltzaile ID anonimoa gordetzen du. Cookie hau bezeroaren domeinuan ezartzen da eta 365 egunen buruan iraungitzen da.

### <a name="local-storage"></a>Tokiko biltegia

Parte hartzearen xehetasunen gaitasunak ere erabiltzen ditu (`localStorage`) gakoak sentikorrak ez diren datuen jarraipena egiteko. Datu hauek guztiz arakatzailean bertan gordetzen dira, zure zerbitzarietara edo zure zerbitzaritik trafikorik bidali gabe.

- *EISession.Id*
    - Etengabeko erabiltzailearen saioari buruzko informazioa gordetzen du, hala nola, saioaren IDa, noiz hasi zen eta noiz iraungitzen den.
- *EISession.Previous*
    - Uneko saioan aurrez bisitatutako orrialdearen URLa gordetzen du.

Biltegiratze lokaleko gakoak ez dira automatikoki iraungitzen eta hurrengo SDK saioan berrezarriko dira.

## <a name="deleting-cookies"></a>Cookieak ezabatzen

Zure bezeroek eskuz ezabatu ditzakete cookieak eta tokiko biltegiratze gakoak arakatzaileen ezarpenen bidez.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
