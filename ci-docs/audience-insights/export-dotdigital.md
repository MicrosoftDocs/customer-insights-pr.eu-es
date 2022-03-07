---
title: Esportatu Customer Insights datuak DotDigital-era
description: Ikasi konexioa nola konfiguratu eta DotDigital-era esportatu.
ms.date: 10/08/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: f9302e17c07238d837dcafb82baecb5aedda17de
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8231603"
---
# <a name="export-segments-to-dotdigital-preview"></a>Esportatu segmentuak DotDigital-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak DotDigital helbide liburuetara eta erabili kanpainetarako, posta elektroniko bidezko marketinerako eta DotDigital-ekin bezero segmentuak eraikitzeko. 

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [DotDigital kontua](https://dotdigital.com/) eta sortu zuen [API erabiltzailea](https://support.dotdigital.com/hc/articles/115001718730-How-do-I-create-an-API-user). API erabiltzailearen egiaztagiriak erabili beharko dituzu konexioa sortzeko
-   DotDigital-en helbide-liburuak eta dagozkien IDak daude. IDa URLan aurki daiteke helbide-liburua hautatu eta irekitzean. Informazio gehiagorako, ikus [DotDigital helbide-liburuak](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero-profil DotDigital-era esportatzeko.
- DotDigital-era esportatzea segmentuetara mugatuta dago.
- Guztira 1 milioi bezero profil dituzten segmentuak esportatzeak 3 ordu arte iraun dezake hornitzailearen aldetik mugak daudelako. 
- DotDigital-era esporta ditzakezun bezeroen profil kopurua DotDigital-ekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="set-up-connection-to-dotdigital"></a>Konfiguratu konexioa DotDigital-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **DotDigital** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Idatzi **DotDigital-eko API erabiltzaile-izena eta pasahitza**. 

1. Sartu zure **[DotDigital helbide liburuaren IDa](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book)**.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** DotDigital-eko konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko. 

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa DotDigital sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.


1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **Izen osoa**, **Generoa**, eta **Posta kodea**.

1. Hautatu esportatu nahi dituzun segmentuak. Guztira 1 milioi bezero profil esporta ditzakezu DotDigital-era.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 
 
DotDigital-en, zure segmentuak hemen aurki ditzakezu: [DotDigital-eko helbide liburuak](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak DotDigital-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da DotDigital-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
