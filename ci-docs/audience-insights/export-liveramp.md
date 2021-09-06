---
title: LiveRamp konektorea
description: Ikasi konexioa eta esportazioa LiveRamp-era nola konfiguratu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 7940db3efacad62ba16099849b3e3ca00d2a5cc1ed31e15a34209c0797e6ae13
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7035630"
---
# <a name="export-segments-to-liverampreg-preview"></a>Esportatu segmentuak LiveRamp-era&reg; (aurrebista)

Aktibatu zure datuak LiveRamp-en 500 plataforma baino gehiagorekin konektatzeko telebista digitaletan, sozialetan eta telebistetan. Lan egin LiveRamp-ekin zure datuekin iragarki-kanpainak zuzentzeko, ezabatzeko eta pertsonalizatzeko.

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

- Konektore hau erabiltzeko LiveRamp-eko harpidetza behar duzu.
- Harpidetza lortzeko, [jarri harremanetan LiveRamp-ekin](https://liveramp.com/contact/) zuzenean. [Argibide gehiago LiveRamp Onboarding-i buruz](https://liveramp.com/our-platform/data-onboarding/).

## <a name="set-up-connection-to-liveramp"></a>Konfiguratu konexioa LiveRamp-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **LiveRamp** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman **Erabiltzaile izena** eta **Pasahitza** zure LiveRamp Secure FTP (SFTP) kontuan.
Kredentzial hauek zure LiveRamp Onboarding kredentzialak desberdinak izan daitezke.

1. Aukeratu **Ziurtatu** LiveRamp-ekin konexioa probatzeko.

1. Egiaztatu ondoren, eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa LiveRamp sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Sarbidean **Aukeratu zure gako identifikatzailea** eremua, hautatu **Emaila**, **Izena eta helbidea**, edo **Mugikorra** identitatearen ebazpenerako LiveRamp-era bidali.
   > [!div class="mx-imgBorder"]
   > ![LiveRamp konektorea atributuen mapak.](media/export-liveramp-segments.png "LiveRamp konektorea atributuen mapak")

1. Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.

1. Hautatu **Gehitu atributua** LiveRamp-era bidalitako atributu gehiago jarraitzeko.

   > [!TIP]
   > LiveRamp erabiltzaileari gako identifikatzaile atributu gehiago bidaltzeak baliteke partidu tasa handiagoa lortzea.

1. Hautatu LiveRamp-era esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Liveramp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Liveramp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
