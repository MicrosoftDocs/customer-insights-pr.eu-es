---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft-en Power Automate batetik Dynamics 365 Customer Insights.
ms.date: 08/03/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: philk
manager: shellyha
ms.openlocfilehash: ffe92414365b0b777691a4a2d585100e4fbea591
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404952"
---
# <a name="power-automate-connector-preview"></a>Power Automate konektorea (Aurrebista)

Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.

## <a name="power-automate-triggers"></a>Power Automate Abiarazleak

Hainbat aktibatzaile erabil ditzakezu zeregin errepikakorrak automatizatzeko fluxuak sortzeko, hala nola, jakinarazpenak edo ekintza aurreratuagoak. 

- Aktibatu datu-iturburu freskatzeak huts egiten duenean. 
- Aktibatu datu-iturburu freskatzeak arrakasta duenean.
- Abiarazi atalasea gainditzen denean segmentu batean. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi atalasea gainditzen denean negozio-neurketa batean. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.
- Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.

[Konfiguratu zure abiarazleak Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).

## <a name="power-automate-actions"></a>Power Automate ekintzak
Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu. Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](https://docs.microsoft.com/connectors/customerinsights/).

## <a name="create-a-power-automate-flow-in-audience-insights"></a>Sortu Power Automate fluxu bat hartzaileen xehetasunetan

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Sistema**.

1. **Sistema** orrian, hautatu **Egoera** fitxa.

1. Sarbidean **Datu iturriak** atala aukeratu **fluxuak** eta hautatu **Sortu fluxua** goitibeherako zerrendatik.
   > [!div class="mx-imgBorder"]
   > ![Power Automate konektorea erakusten du Sortu fluxua ekintza](media/power-automate-connector-create-flow.png "Power Automate konektorea erakusten du Sortu fluxua ekintza")

1. Power Automate-n, hautatu abiarazle erabilgarri bat zure nahiago duen fluxua sortzeko. Zure lehen fluxua sortzen ari bazara, identifikatu egin behar duzu Power Automate konektorea lehenengo.
