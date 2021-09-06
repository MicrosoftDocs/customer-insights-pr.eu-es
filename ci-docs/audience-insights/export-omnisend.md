---
title: Esportatu Customer Insights datuak Omnisend-era
description: Ikasi konexioa nola konfiguratu eta Omnisend-era esportatu.
ms.date: 05/21/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 58b54dc24f4656f9dd376415a701539c8796e83e6d4e3c6754f5627ce77c5685
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7031751"
---
# <a name="export-segments-to-omnisend-preview"></a>Esportatu segmentuak Omnisend-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Omnisend-era eta erabili marketin jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [Omnisend kontua](https://www.omnisend.com/) eta dagozkien administratzaile egiaztagiriak.
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio bakoitzeko milioi bat profil esportatu ditzakezu Omnisend-era eta 4 ordu behar izan ditzakezu osatzeko.
- Omnisend-era esportatzea segmentuetara mugatzen da.
- Omnisend-era esporta ditzakezun profilen kopurua Omnisend-ekin duzun kontratuaren araberakoa da.

## <a name="set-up-connection-to-omnisend"></a>Konfiguratu konexioa Omnisend-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Omnisend** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure [Omnisend-en API gakoa](https://support.omnisend.com/en/articles/1061890-generating-api-key).

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** Omnisend-erako konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Omnisend sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. Segmentuak esportatu behar dira Omnisend-era. Aukeran, Izena, Abizena, Helbidea, Herrialdea/eskualdea, Egoera eta posta-kodea esporta ditzakezu mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak Omnisend-era igortzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zu arduratuko zara Omnisend-ek pribatutasun edo segurtasun betebeharrak betetzen dituela ziurtatzeaz. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
