---
title: Power Automate konektorea (aurrebista) | Microsoft Docs
description: Sortu fluxuak Microsoft Power Automate hurrengoan Dynamics 365 Customer Insights.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: f87bd6db7143294a264813f6c5c7d7963f303628
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196103"
---
# <a name="power-automate-connector-preview"></a>Power Automate konektorea (Aurrebista)

Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Microsoft Power Automate](https://flow.microsoft.com/)-n zuzenean.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 100 dei 60 segundoko. Erabili [$skip parametroa](/connectors/customerinsights/#get-items-from-an-entity) API amaierako puntura hainbat aldiz deitzeko.

## <a name="power-automate-triggers"></a>Power Automate Abiarazleak

Erabili abiarazleak hodei fluxuak sortzeko eta zeregin errepikakorrak automatizatzeko, hala nola jakinarazpenak edo ekintza aurreratuagoak. Erabili abiarazleak noiz:

- datu-iturburu freskatzeak huts egin du.
- datu-iturburu freskatzea arrakastatsua da.
- Segmentu batean atalase bat gainditzen da. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Negozio-neurri batean atalase bat gainditzen da. Dimentsiorik gabeko negozio-neurriak soilik onartzen dira. Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.
- Programatutako freskatze osoa amaitu da. Abiarazle honek ez du funtzionatzen eskuz hasitako freskatzeetarako.
- Bateratze-prozesuaren freskagarri bat amaitu da.

[Konfiguratu zure abiarazleak Power Automate-n.](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/)

## <a name="power-automate-actions"></a>Power Automate ekintzak

Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu. Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](/connectors/customerinsights/).

## <a name="create-a-power-automate-flow"></a>Sortu Power Automate fluxu bat

1. Joan **Administratzailea** > **Konexioak**.

1. **Power Automate** fitxan, hautatu **Konfiguratu**.

1. Power Automate-ko Customer Insights konektorea irekitzen da. **Hasi saioa** Power Automate.

1. Aukeratu erabilgarri dauden abiarazleetako bat eta gehitu urrats gehiago zure fluxu berrian. Informazio gehiagorako, ikusi [Sortu hodei fluxua hemen Power Automate](/power-automate/get-started-logic-flow).

Fluxuak erabiltzeko adibideak: 
- Bidali mezu bat Microsoft Teams kanalera datu-iturburu freskatzeak huts egiten badu. 
- Bidali mezu elektronikoa datu jabeei segmentu bateko atalasea gainditzen denean.

[!INCLUDE [footer-include](includes/footer-banner.md)]
