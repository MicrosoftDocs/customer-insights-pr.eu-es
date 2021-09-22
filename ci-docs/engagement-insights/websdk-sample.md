---
title: Exekutatu web SDK lagina
description: Ikasi web SDK lagina pertsonalizatzen eta exekutatzen.
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 10/30/2020
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: 97e50a51231bcf05f3e381397f0cf41e49afc10e3c3674d7c709c8f521979e12
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036588"
---
# <a name="run-the-web-sdk-sample-for-dynamics-365-customer-insights-engagement-insights-capability"></a>Exekutatu web SDK lagina Dynamics 365 Customer Insights konpromisoari buruzko gaitasuna

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Elkarreragin xehetasunen gaitasuna web SDK liburutegia JavaScript liburutegia da, zure webgunean erabil dezakezun lagin kodearekin.

## <a name="prerequisites"></a>Aurrebaldintzak

- Instalatu [Visual Studio Kodea](https://code.visualstudio.com/).
- [Instalatu Live Server luzapena](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) urtean Visual Studio Kodetu eta ezagutu Live Server nola exekutatu ezagutzen.
- Izan behar duzu [irensteko gakoa](instrument-website.md).

## <a name="run-sample"></a>Exekutatu lagina

1. [Deskargatu web SDK lagina](https://download.pi.dynamics.com/sdk/EngagementInsightsSamples/ei_websdk_sample.zip).

1. Deskonprimitu konprimitutako fitxategia `ei_websdk_sample.zip`.

1. Ireki deskonprimitutako karpeta hemen Visual Studio Kodea.

1. Urtean `ei_websdk_sample.html` fitxategia, ordezkatu "INGESTION_KEY" katea zure konpromiso gaitasunen atariko ingesta-gakoarekin eta "NAME" katea SDK-k instantzia izatea nahi duzun izen globalarekin. Ziurtatu agerraldi guztiak ordezkatzen dituzula.

1. Ireki `ei_websdk_sample.html` fitxategia Live Server zerbitzuan erabiliz Visual Studio Kodea hautatuz **Joan Zuzenean** egoera barratik.

1. Orrialdea irekitzean, ikuspegi gertaera automatikoki bidali behar da. Orriko botoietako batean klik egitean ekintza gertaerak bidaliko dira. **Jarraitu gertaerak** botoiak gertaera pertsonalizatuak ere bidaliko ditu. Aukeratzea **Joan Bingera** botoiak ekintza gertaera bat bidaliko du Bing webgunera joan aurretik.

1. Ikusi laneko espaziora zoazenean gertatzen ari diren gertaerak. Laneko espazio hau 4. urratsean sartutako irensteko gakoarekin lotuta dago.


[!INCLUDE[footer-include](../includes/footer-banner.md)]