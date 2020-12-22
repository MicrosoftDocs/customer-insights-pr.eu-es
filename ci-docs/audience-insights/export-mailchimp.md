---
title: Esportatu Customer Insights datuak Mailchimp-era
description: Ikasi Mailchimp-erako konexioa nola konfiguratu.
ms.date: 10/26/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: edff494f6edf26a8b641cb1d788a715389ddb346
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404958"
---
# <a name="connector-for-mailchimp-preview"></a>Mailchimp-eko konektorea (aurrebista)

Esportatu bezero profil bateratuen segmentuak Mailchimp-era buletinak eta posta elektronikoko kanpainak sortzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [Mailchimp kontua](https://mailchimp.com/) eta dagozkion administratzaile kredentzialak.
-   Mailchimp-en hartzaileak eta dagozkien IDak daude. Informazio gehiagorako, ikus [Mailchimp-eko hartzaileak](https://mailchimp.com/help/create-audience/).
-   [Konfiguratutako segmentuak](segments.md) dituzu
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="connect-to-mailchimp"></a>Konektatu Mailchimp-era

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. **Mailchimp** atalean hautatu **Konfiguratu**.

1. Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Sartu zure **[Mailchimp hartzaileen IDa](https://mailchimp.com/help/find-audience-id/)** eta hautatu **Konektatu** Mailchimp-eko konexioa hasieratzeko.

1. Aukeratu **Egiaztatu Mailchimp-ekin** eta eman zure Mailchimp kredentzialak.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

   :::image type="content" source="media/export-connect-mailchimp.png" alt-text="Esportatu pantaila-argazkia Mailchimp konexiorako":::

1. Aukeratu **hurrengoa** esportazioa konfiguratzeko.

## <a name="configure-the-connector"></a>Konfiguratu konektorea

1. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. 

1. Aukeran, **izena** eta **abizena** esporta ditzakezu mezu pertsonalizatuagoak sortzeko eremu osagarri gisa. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak. Guztira 1 milioi bezero profil esporta ditzakezu Mailchimp-era.

   :::image type="content" source="media/export-segments-mailchimp.png" alt-text="Aukeratu eremuak eta segmentuak Mailchimp-era esportatzeko":::

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab). Mailchimp-en, zure segmentuak azpian aurki ditzakezu hemen: [Mailchimp-eko hartzaileak](https://mailchimp.com/help/create-audience/).

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat profil Mailchimp-era esportatzeko.
- Mailchimp-era esportatzea segmentuetara mugatuta dago.
- Guztira 1 milioi profil dituzten segmentuak esportatzeak hiru ordu arte iraun dezake hornitzailearen aldetik mugak direla eta. 
- Mailchimp-era esporta ditzakezun profilen kopurua Mailchimp-ekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Mailchimp-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Mailchimp-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
