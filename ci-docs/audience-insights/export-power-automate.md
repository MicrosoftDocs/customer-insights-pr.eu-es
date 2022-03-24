---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft Power Automate hurrengoan Dynamics 365 Customer Insights.
ms.date: 06/24/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: dd90ef4576246b49d4a9c74005196ee9813a6744
ms.sourcegitcommit: d168a738a08adb8b4b2e410bdaa3716d7b63cc9b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/17/2022
ms.locfileid: "8455892"
---
# <a name="power-automate-connector-preview"></a>Power Automate konektorea (Aurrebista)

Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.

## <a name="known-limitations"></a>Muga ezagunak

- 60 segundoko 100 dei egin ditzakezu gehienez. API amaierako puntuari hainbat aldiz dei diezaiokezu $skip parametroa erabiliz. [Lortu informazio gehiago $skip parametroari buruz](/connectors/customerinsights/#get-items-from-an-entity).

## <a name="power-automate-triggers"></a>Power Automate Abiarazleak

Erabili abiarazleak hodei fluxuak sortzeko eta zeregin errepikakorrak automatizatzeko, hala nola jakinarazpenak edo ekintza aurreratuagoak. 

- Aktibatu datu-iturburu freskatzeak huts egiten duenean. 
- Aktibatu datu-iturburu freskatzeak arrakasta duenean.
- Abiarazi atalasea gainditzen denean segmentu batean. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi atalasea gainditzen denean negozio-neurketa batean. Dimentsiorik gabeko negozio-neurriak soilik onartzen dira. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.
- Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.

[Konfiguratu zure abiarazleak Power Automate-n.](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/)

## <a name="power-automate-actions"></a>Power Automate ekintzak

Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu. Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](/connectors/customerinsights/).

## <a name="create-a-power-automate-flow"></a>Sortu Power Automate fluxu bat

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Power Automate** fitxan, hautatu **Konfiguratu**.

1. Power Automate-ko Customer Insights konektorea irekitzen da. **Hasi saioa** Power Automate.

1. Aukeratu erabilgarri dauden abiarazleetako bat eta gehitu urrats gehiago zure fluxu berrian. Informazio gehiagorako, ikusi [Sortu hodei fluxua hemen Power Automate](/power-automate/get-started-logic-flow).

Fluxuak erabiltzeko adibideak: 
- Bidali mezu bat Microsoft Teams kanalera datu-iturburu freskatzeak huts egiten badu. 
- Bidali mezu elektronikoa datu jabeei segmentu bateko atalasea gainditzen denean.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
