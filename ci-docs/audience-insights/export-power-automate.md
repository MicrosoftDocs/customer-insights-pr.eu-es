---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft-en Power Automate batetik Dynamics 365 Customer Insights.
ms.date: 01/20/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
ms.reviewer: philk
manager: shellyha
ms.openlocfilehash: fb1df4e9ab1f78300b8ec1f8dfdfbfbac0e71447
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5268809"
---
# <a name="power-automate-connector-preview"></a>Power Automate konektorea (Aurrebista)

Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.

## <a name="power-automate-triggers"></a>Power Automate Abiarazleak

Erabili abiarazleak hodei fluxuak sortzeko eta zeregin errepikakorrak automatizatzeko, hala nola jakinarazpenak edo ekintza aurreratuagoak. 

- Aktibatu datu-iturburu freskatzeak huts egiten duenean. 
- Aktibatu datu-iturburu freskatzeak arrakasta duenean.
- Abiarazi atalasea gainditzen denean segmentu batean. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi atalasea gainditzen denean negozio-neurketa batean. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.
- Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.

[Konfiguratu zure abiarazleak Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).

## <a name="power-automate-actions"></a>Power Automate ekintzak
Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu. Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](https://docs.microsoft.com/connectors/customerinsights/).

## <a name="create-a-power-automate-flow"></a>Sortu Power Automate fluxu bat

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Power Automate** fitxan, hautatu **Konfiguratu**.

1. Power Automate-ko Customer Insights konektorea irekitzen da. **Hasi saioa** Power Automate.

1. Aukeratu erabilgarri dauden abiarazleetako bat eta gehitu urrats gehiago zure fluxu berrian. Informazio gehiagorako, ikusi [Sortu hodei fluxua hemen Power Automate](https://docs.microsoft.com/power-automate/get-started-logic-flow).

Fluxuak nola erabili adibideak: 
- Bidali mezu bat Microsoft Teams kanalera datu-iturburu freskatzeak huts egiten badu. 
- Bidali mezu elektronikoa datu jabeei segmentu bateko atalasea gainditzen denean.



[!INCLUDE[footer-include](../includes/footer-banner.md)]