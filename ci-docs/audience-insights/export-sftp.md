---
title: Esportatu Customer Insights datuak SFTP ostalarietara
description: Ikusi nola konfiguratu konexioa SFTP ostalaria.
ms.date: 01/27/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 9ec14fafa8f99e34b95349371298082e166535d0
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5598370"
---
# <a name="connector-for-sftp-preview"></a>Konektorea SFTP-rako (aurrebista)

Erabili hirugarrenen aplikazioetako bezero-datuak horiek fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) ostalarira transferituz.

## <a name="prerequisites"></a>Aurrebaldintzak

- SFTP ostalariaren erabilgarritasuna eta dagozkien egiaztagiriak.

## <a name="connect-to-sftp"></a>Konektatu SFTP-ra

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. Azpian **SFTP** hautatu **Konfiguratu**.

1. Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.

1. Eman SFTP kontuaren **Erabiltzaile-izena**, **Pasahitza**, **Ostalari-izena** eta **Esportazio-karpeta**.

1. Hautatu **Egiaztatu** konexioa probatzeko.

1. Egiaztatu ondoren, aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimitu gabe**, eta hautatu **eremu-mugatzailea** esportatutako fitxategietarako.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **hurrengoa** esportazioa konfiguratzen hasteko.

## <a name="configure-the-export"></a>Konfiguratu esportazioa

1. Aukeratu entitateak, adibidez, esportatu nahi dituzun segmentuak.

   > [!NOTE]
   > Aukeratutako entitate bakoitzak gehienez bost irteera fitxategi izango ditu esportatzean. 

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da. Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa. 
- Gehienez 100 milioi bezero profil dituzten entitate esportatzaileek 90 minutu iraun dezakete gomendatutako gutxieneko konfigurazioa erabiltzen duten bi PUZ nukleorekin eta 1 Gb memoria. 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]