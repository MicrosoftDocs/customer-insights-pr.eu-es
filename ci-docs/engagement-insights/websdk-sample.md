---
title: Exekutatu web SDK lagina
description: Ikasi web SDK lagina pertsonalizatzen eta exekutatzen.
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 10/01/2021
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: a50a10db784ec7c1943c94e74000713309787e5c
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8225316"
---
# <a name="run-the-web-sdk-sample-for-dynamics-365-customer-insights-engagement-insights-capability"></a>Exekutatu web SDK lagina Dynamics 365 Customer Insights konpromisoari buruzko gaitasuna

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Elkarreragin xehetasunen gaitasuna web SDK liburutegia JavaScript liburutegia da, zure webgunean erabil dezakezun lagin kodearekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- Instalatu [Visual Studio Kodea](https://code.visualstudio.com/).
- [Instalatu Live Server luzapena](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) urtean Visual Studio Kodetu eta ezagutu Live Server nola exekutatu ezagutzen.
- Izan behar duzu [elkarreragin xehetasunen lan-eremua](create-workspace.md).

## <a name="run-sample"></a>Exekutatu lagina

1. [Deskargatu web SDK lagina](https://download.pi.dynamics.com/sdk/EngagementInsightsSamples/ei_websdk_sample.zip).

1. Deskonprimitu konprimitutako fitxategia `ei_websdk_sample.zip`.

1. Ireki deskonprimitutako karpeta hemen Visual Studio Kodea.

1. Joan zure lan-eremuko konpromisoen atarira. Aukeratu **Administratzailea** > **Lan-eremua** eta gero **Instalazio gida**. Jarraitu lehen aukera eta hautatu **Kopiatu kodea** JavaScript kode zati kopiatzeko.

1. Urtean `ei_websdk_sample.html` fitxategia, itsatsi lerro honen azpian kopiatu berri duzun kode zati:

   - <-- ITSASI JAVASCRIPT KODE ZATI BAT HEMEN INGURUKO INSIGHTS ATARitik LERRO HONEN BEHEAN -->

1. Ireki `ei_websdk_sample.html` fitxategia Live Server zerbitzuan erabiliz Visual Studio Kodea hautatuz **Joan Zuzenean** egoera barratik.

1. Orrialdea irekitzean, ikuspegi gertaera automatikoki bidali behar da. Orriko botoietako batean klik egitean ekintza gertaerak bidaliko dira. **Jarraitu gertaerak** botoiak gertaera pertsonalizatuak ere bidaliko ditu. Aukeratzea **Joan Bingera** botoiak ekintza gertaera bat bidaliko du Bing webgunera joan aurretik.

1. Ikusi laneko espaziora zoazenean gertatzen ari diren gertaerak. Laneko espazio hau 4. urratsean sartutako irensteko gakoarekin lotuta dago.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
