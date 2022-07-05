---
title: Esportatu segmentuak Sendinblue-ra (aurrebista)
description: Ikasi konexioa nola konfiguratu eta Sendinblue-ra esportatu.
ms.date: 10/08/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 9f6550b5c57866702631b4c294bb059279461bd6
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9083072"
---
# <a name="export-segments-to-sendinblue-preview"></a>Esportatu segmentuak Sendinblue-ra (aurrebista)

Esportatu bezero profil bateratuen segmentuak kanpaniak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzei etekinik handiena ateratzeko Sendinblue bidez.

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [Sendinblue kontua](https://www.sendinblue.com/) eta dagozkien administratzaile egiaztagiriak.
-   Sendinblue-n dauden zerrendak eta dagozkien IDak daude.
-   [Konfiguratutako segmentuak](segments.md) dituzu.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero-profil Sendinblue-ra esportatzeko.
- Sendinblue-ra esportatzea segmentuetara mugatzen da.
- Guztira 1 milioi bezero profil dituzten segmentuak esportatzeak 90 minutu arte iraun dezake. 
- Sendinblue-ra esporta ditzakezun bezeroen profil kopurua Sendinblue-rekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="set-up-connection-to-sendinblue"></a>Konfiguratu Sendinblue-ra konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **Sendinblue** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure **[SendinBlue API gakoa](https://developers.sendinblue.com/docs/getting-started#:~:text=Get%20your%20API%20key&text=You%20can%20create%20one%20from,your%20settings%20This%20API%20key)**.

1. Aukeratu **Ados** baieztatzeko **Datuen pribatutasuna eta betetzea** eta hautatu **Konektatu** Sendinblue-rekin konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Urtean **Esportaziorako konexioa** eremuan, aukeratu konexio bat Sendinblue atalean. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Sartu zure **SendinBlue zerrendaren IDa** 

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. 

1. Aukeran, esporta dezakezu **Izena**, **Abizena** eta **Telefonoa** mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko Sendinblue-ra, datuak betetze mugatik kanpo transferitzea baimentzen duzu, Dynamics 365 Customer Insights datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz Sendinblue izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE [footer-include](includes/footer-banner.md)]
