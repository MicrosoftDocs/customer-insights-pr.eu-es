---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft Power Automate hurrengoan Dynamics 365 Customer Insights.
ms.date: 01/20/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: ce2477d957a1792e0436a0dfc15a33621b1c89a9
ms.sourcegitcommit: e8e03309ba2515374a70c132d0758f3e1e1851d0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5976073"
---
# <a name="power-automate-connector-preview"></a>Power Automate konektorea (Aurrebista)

Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.

## <a name="power-automate-triggers"></a>Power Automate Abiarazleak

Erabili abiarazleak hodei fluxuak sortzeko eta zeregin errepikakorrak automatizatzeko, hala nola jakinarazpenak edo ekintza aurreratuagoak. 

- Aktibatu datu-iturburu freskatzeak huts egiten duenean. 
- Aktibatu datu-iturburu freskatzeak arrakasta duenean.
- Abiarazi atalasea gainditzen denean segmentu batean. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi atalasea gainditzen denean negozio-neurketa batean. Dimentsiorik gabeko negozio-neurriak soilik onartzen dira. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.
- Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.

[Konfiguratu zure abiarazleak Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).

## <a name="power-automate-actions"></a>Power Automate ekintzak
Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu. Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](/connectors/customerinsights/).

## <a name="create-a-power-automate-flow"></a>Sortu Power Automate fluxu bat

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Power Automate** fitxan, hautatu **Konfiguratu**.

1. Power Automate-ko Customer Insights konektorea irekitzen da. **Hasi saioa** Power Automate.

1. Aukeratu erabilgarri dauden abiarazleetako bat eta gehitu urrats gehiago zure fluxu berrian. Informazio gehiagorako, ikusi [Sortu hodei fluxua hemen Power Automate](/power-automate/get-started-logic-flow).

Fluxuak nola erabili adibideak: 
- Bidali mezu bat Microsoft Teams kanalera datu-iturburu freskatzeak huts egiten badu. 
- Bidali mezu elektronikoa datu jabeei segmentu bateko atalasea gainditzen denean.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
