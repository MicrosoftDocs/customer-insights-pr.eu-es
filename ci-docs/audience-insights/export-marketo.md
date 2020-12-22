---
title: Esportatu Customer Insights datuak Marketo-ra
description: Ikasi Marketo-rako konexioa nola konfiguratu.
ms.date: 11/12/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 34ccee2894f1f2b552d0c6a88a6810e2dfc677a3
ms.sourcegitcommit: 0b1d3ca11b8ba362a959da0eea15c37e9cdba084
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "4570388"
---
# <a name="connector-for-marketo-preview"></a>Marketo-ko konektorea (aurrebista)

Kanpainak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzak erabiltzeko Marketo bidez, esportatu bezeroen profil bateratuetako segmentuak.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [Marketo kontua](https://login.marketo.com/) eta dagozkion administratzaile kredentzialak.
-   Marketo-n zerrendak eta dagozkien IDak daude. Informazio gehiagorako, ikus [Marketo-ko zerrendak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).
-   [Konfiguratutako segmentuak](segments.md) dituzu.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="connect-to-marketo"></a>Konektatu Marketo-ra

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. **Marketo** atalean hautatu **Konfiguratu**.

1. Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.

1. Sartu zure **[Marketo-ren bezeroaren IDa, Bezeroaren sekretua eta REST amaiera-puntuaren ostalari izena](https://developers.marketo.com/rest-api/authentication/)**.

1. Sartu zure **[Marketo zerrendaren IDa](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)** 

1. Aukeratu **ados** **Datu-pribatutasuna eta arau-betetzea** onartzeko eta hautatu **Konektatu** Marketo-rekin konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

   :::image type="content" source="media/export-connect-marketo.png" alt-text="Esportatu pantaila-argazkia Marketo konexiorako":::

1. Aukeratu **hurrengoa** esportazioa konfiguratzeko.

## <a name="configure-the-connector"></a>Konfiguratu konektorea

1. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. 

1. Aukeran **izena**, **abizena**, **herria**, **probintzia**, eta **herrialdea/eskualdea** esporta ditzakezu eremu gehigarri gisa, mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak. Guztira 1 milioi bezero profil esporta ditzakezu Marketo-ra.

   :::image type="content" source="media/export-segment-marketo.png" alt-text="Aukeratu eremuak eta segmentuak Marketo-ra esportatzeko":::

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab). Marketo-n, zure segmentuak azpian aurki ditzakezu hemen: [Marketo-ko hartzaileak](ttps://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat profil Marketo-ra esportatzeko.
- Marketo-ra esportatzea segmentuetara mugatuta dago.
- Guztira 1 milioi profil dituzten segmentuak esportatzen 3 ordu behar izan daitezke. 
- Marketo-ra esporta ditzakezun profilen kopurua Marketo-rekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Marketo-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Marketo-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
