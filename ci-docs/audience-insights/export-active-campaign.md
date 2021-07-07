---
title: Esportatu Customer Insights datuak ActiveCampaign-ra
description: Ikasi konexioa nola konfiguratu eta ActiveCampaign-ra esportatu.
ms.date: 06/29/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 6d85fa9836618e27f7f3da6ce17c07b4bc89e187
ms.sourcegitcommit: 057079532e31c12bac36f374857ba3dc847d6ad0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314572"
---
# <a name="export-segments-to-activecampaign-preview"></a>Esportatu segmentuak ActiveCampaign-ra (aurrebista)

Esportatu bezero profil bateratuen segmentuak ActiveCampaign-era eta erabili marketin-jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [ActiveCampaign kontua](https://www.activecampaign.com/) eta dagozkien administratzaile egiaztagiriak.
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa duen eremu bat dute.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio bakoitzeko milioi bat profil esportatu ditzakezu ActiveCampaign-era eta 90 minutu behar izan ditzakezu osatzeko.
- ActiveCampaign-era esportatzea segmentuetara mugatzen da.
- ActiveCampaign-era esporta ditzakezun profilen kopurua ActiveCampaign-ekin duzun kontratuaren araberakoa da.

## <a name="set-up-connection-to-activecampaign"></a>Konfiguratu ActiveCampaign-era konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **ActiveCampaign** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure [ActiveCampaign API gakoa eta REST amaiera puntuko ostalari izena](https://help.activecampaign.com/hc/articles/207317590-Getting-started-with-the-API#how-to-obtain-your-activecampaign-api-url-and-key). REST Endpoint ostalari izena ostalari izena soilik da, gabe https://. 

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** ActiveCampaign konexioaren hautapena berresteko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio bat konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Urtean **Esportaziorako konexioa** eremuan, aukeratu konexio bat ActiveCampaign atalean. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Sartu zure [**ActiveCampaign zerrendaren IDa**](https://help.activecampaign.com/hc/articles/360000030559-How-to-create-a-list-in-ActiveCampaign).    

3. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. ActiveCampaign-era esportatzea segmentuetara beharrezkoa da. Aukeran, esporta dezakezu Izena, Abizena eta Telefonoa mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu Gehitu atributua eremu horiek esleitzeko.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights datuak transmititzeko ActiveCampaign-era, datuak betetze mugatik kanpo transferitzea baimentzen duzu, Dynamics 365 Customer Insights datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu hauek transferituko ditu zure aginduz, baina zu arduratuko zara hori ziurtatzeaz ActiveCampaign izan ditzakezun pribatutasun edo segurtasun betebeharrak betetzen ditu. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
