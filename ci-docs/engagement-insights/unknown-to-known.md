---
title: Ezagut ezazu aurretik ezezagunetik ezagunera autentifikatutako bisitarien web gertaerak
description: Ezezaguna eta ezaguna funtzioak webgune bateko gertaerak aurretik autentifikatutako bisitariekin lotzeko aukera ematen du.
ms.reviewer: mhart
ms.author: mkisel
author: mkisel11
ms.date: 7/15/2021
ms.subservice: engagement-insights
ms.topic: overview
ms.manager: shellyha
ms.openlocfilehash: 75ce776fd5be1c426508ae6f5c239c86bdd3ec39
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8230665"
---
# <a name="recognize-web-events-from-previously-authenticated-visitors"></a>Ezagutu aurretik autentifikatutako bisitarien web gertaerak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Parte-hartzearen xehetasunen **ezezagunetik ezezagunera** gaitasunaren ezaugarriak webgune bateko gertaerak aurretik autentifikatutako bisitariekin lotzea ahalbidetzen du. Ezaugarria desgaituta badago, aurreko bisita batean autentifikatu eta gero utzi zuten bisitariak ez dira identifikatuko berriro itzultzean autentifikatzen ez badira. 

Adibidez, pertsona batek joan den astean webgune bat bisitatu zuen, gunean bere erabiltzaile kontuan sartu eta produktuen katalogoa arakatu zuen. Pertsona hurrengo astean itzuliko da produktu gehiago arakatzera bere kontuan sartu gabe. **Ezezagunetik ezagunera** ezaugarri erabitlzen duen gunearen jabeak jakingo luke pertsona bera itzuli zela eta gunean zer egin zuen. Horri esker, webguneko jardueren berri zehatzagoa eta azterketa gehiago egin daiteke.

## <a name="enable-unknown-to-known"></a>Gaitu ezezagunetik ezagunera

[Laneko arearen administratzaile](user-roles.md) izan behar duzu eginbide hau gaitzeko. 

1. Parte-hartzearen inguruko xehetasunetan, joan hona **Administratzailea** > **Laneko area**. 
2. Hautatu **Ezarpenak** fitxa.
3. **Ezezagunetik ezagunera** atalean, ezarri txandakatzea **Gaituta** gisa.

![Gaitu ezezagunetik ezagunera](media/U2Ktoggle.png "Gaitu ezezagunetik ezagunera")

## <a name="adding-javascript-code-to-your-sites-tracking-snippet"></a>JavaScript kodea gehitzen zure webgunearen jarraipenari kode zati

Webgune batek har dezake **erabiltzailearen authId** Javascript lagin honekin batera: [parte-hartzearen xehetasunen web SDK](advanced-SDK-implementation.md). **Ezezagunetik ezagunera** funtzioak funtzionatzeko, authId hartu behar duzu *eta* gaitu userMapping: Egia gisa JavaScript kode zatian, beheko laginean bezala.

```
[…]
window, document
{
src:"https://download.pi.dynamics.com/sdk/web/mspi-0.min.js",
name:"myproject",
cfg:{
ingestionKey:<paste your ingestion key>",
autoCapture:{
view:true,
click:true
},
userMapping: true
},
user:{
authId: getLoggedInUserId()*,
email: getLoggedInUserEmail()*,
authType: "MSA",
name: "Alex Jensen"
}
[…]
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
