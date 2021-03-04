---
title: LiveRamp konektorea
description: Ikasi datuak LiveRamp-era esportatzen.
ms.date: 12/02/2020
ms.reviewer: kishorem
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 64d781f52e8124fc3e83a7b84f468830c5249cfd
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270143"
---
# <a name="liverampreg-connector-preview"></a>LiveRamp&reg; konektorea (aurrebista)

Aktibatu zure datuak LiveRamp-en, 500 plataforma baino gehiagorekin konektatzeko digital, sozial eta telebistetako ekosistemetan. Lan egin LiveRamp-ekin zure datuekin iragarki-kanpainak zuzentzeko, ezabatzeko eta pertsonalizatzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- Konektore hau erabiltzeko LiveRamp-eko harpidetza behar duzu.
- Harpidetza lortzeko, [jarri harremanetan LiveRamp-ekin](https://liveramp.com/contact/) zuzenean. [Argibide gehiago LiveRamp Onboarding-i buruz](https://liveramp.com/our-platform/data-onboarding/).

## <a name="connect-to-liveramp"></a>Konektatu LiveRamp-era

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **LiveRamp** lauzan, hautatu **Konfiguratu**.

1. Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.

1. Eman **Erabiltzaile izena** eta **Pasahitza** zure LiveRamp Secure FTP (SFTP) kontuan.
Kredentzial hauek zure LiveRamp Onboarding kredentzialak desberdinak izan daitezke.

1. Aukeratu **Ziurtatu** LiveRamp-ekin konexioa probatzeko.

1. Egiaztatu ondoren, eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.

1. Aukeratu **hurrengo** LiveRamp konektorea konfiguratzeko.

## <a name="configure-the-connector"></a>Konfiguratu konektorea

1. Sarbidean **Aukeratu zure gako identifikatzailea** eremua, hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** identitatearen ebazpenerako LiveRamp-era bidali.

1. Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.

1. Aukeratu **Gehitu atributua** LiveRamp-era bidaltzeko atributu osagarriak mapatzeko.

   > [!TIP]
   > LiveRamp erabiltzaileari gako identifikatzaile atributu gehiago bidaltzeak baliteke partidu tasa handiagoa lortzea.

1. Hautatu LiveRamp-era esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

> [!div class="mx-imgBorder"]
> ![LiveRamp konektorea atributuen mapak](media/export-liveramp-segments.png "LiveRamp konektorea atributuen mapak")

## <a name="export-the-data"></a>Esportatu datuak

Esportazioa laster hasiko da esportaziorako baldintza guztiak bete badira. Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).
Esportazioa behar bezala burututa, LiveRamp Onboarding zerbitzuan saioa egin dezakezu zure datuak aktibatzeko eta banatzeko.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Liveramp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Liveramp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.

[!INCLUDE[footer-include](../includes/footer-banner.md)]