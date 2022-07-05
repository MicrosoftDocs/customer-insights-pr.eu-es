---
title: Esportatu segmentuak Iterablera (aurrebista)
description: Ikasi konexioa konfiguratzen eta Iterablera esportatzen.
ms.date: 03/29/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 98d5aeab6b0e932d291213053d509ec72da82e47
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9052220"
---
# <a name="export-segments-to-iterable-preview"></a>Esportatu segmentuak Iterablera (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Iterablera eta erabili marketin-jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Bat daukazu [Iterable kontua](https://iterable.com/) eta dagozkion administratzaile-kreditazioak.
-   Zuk daukazu [konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Iterablera esportatzea segmentuetara mugatzen da.
- Gehienez 1 milioi bezero-profil Iterablera esportatzeak 30 minutu behar izan ditzake osatzeko. 
- Iterable-ra esporta dezakezun bezero-profilen kopurua Iterable-rekin duzun kontratuaren menpe dago eta mugatuta dago.

## <a name="set-up-connection-to-iterable"></a>Konfiguratu Iterable-ra konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Iteragarria** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman zure [API gako itergarria](https://support.iterable.com/hc/en-us/articles/360043464871) saioa hasten jarraitzeko. 

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Hautatu **Konektatu** Iterable-rako konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Iterable atalean. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

3. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. Segmentuak Iterablera esportatzeko beharrezkoa da. Iterable-n sortutako zerrendak zure segmentuaren izenaren izen bera jasoko du hemen.Dynamics 365 Customer Insights.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights Iterable-ra datuak transmititzeko, datuen transferentzia onartzen duzu betetze-mugatik kanpo Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek zure aginduz transferituko ditu, baina zu zara Iterablek izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
