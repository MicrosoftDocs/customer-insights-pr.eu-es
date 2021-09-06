---
title: Esportatu Customer Insights datuak Klaviyo-ra
description: Ikasi konexioa nola konfiguratu eta Klaviyo-ra esportatu.
ms.date: 08/13/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 7c1297fd5381c00c07d6501186c51fe4798773d1
ms.sourcegitcommit: 205f931ec671a0ab1850f2c1c94df3307ffb62c9
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7385773"
---
# <a name="export-segment-lists-to-klaviyo-preview"></a>Esportatu segmentuen zerrendak Klaviyo-ra (aurrebista)

Esportatu bezero profil bateratuen segmentuak Klaviyo-ra eta erabili marketin-jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [Klaviyo kontua](https://www.klaviyo.com/) eta dagozkien administratzaile egiaztagiriak.
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio bakoitzeko 100'000 profil esporta ditzakezu Klaviyo-ra.
- Klaviyo-ra esportatzea segmentuetara mugatzen da.
- 1 milioi profil Klaviyo-ra esportatzeko 20 minutu behar izan ditzakezu osatzeko. 
- Klaviyo-ra esporta ditzakezun profilen kopurua Klaviyo-rekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="set-up-connection-to-klaviyo"></a>Konfiguratu Klaviyo-ra konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **Klaviyo** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman zure [Klaviyo API gakoa](https://help.klaviyo.com/hc/articles/115005062267-How-to-Manage-Your-Account-s-API-Keys) saioa hasten jarraitzeko. 

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** Klaviyo konexioaren hautapena berresteko.

1. Aukeratu **Egiaztatu Klaviyo-rekin** eta eman zure administratzaile kredentzialak Klaviyo-rako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Urtean **Esportaziorako konexioa** eremuan, aukeratu konexio bat Klaviyo atalean. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Sartu zure [**Klaviyo zerrendaren IDa**](https://help.klaviyo.com/hc/articles/115005078647-How-to-Find-a-List-ID).     

3. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. Klaviyo-ra esportatzea segmentuetara beharrezkoa da.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko Klaviyo-ra, datuak betetze mugatik kanpo transferitzea baimentzen duzu, Dynamics 365 Customer Insights datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz Klaviyo izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
