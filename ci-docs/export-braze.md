---
title: Esportatu Customer Insights datuak Braze-ra
description: Ikasi nola konfiguratu konexioa eta Braze-ra esportatzen.
ms.date: 03/29/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: bfc9b34506dc3385b5edf12b31e74d05f2d20655
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642082"
---
# <a name="export-segment-lists-to-braze-preview"></a>Esportatu segmentu-zerrendak Braze-ra (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Braze-ra eta erabili marketin-jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

-   Bat daukazu [Braze kontua](https://www.braze.com/) eta dagozkion administratzaile-kreditazioak.
-   Zuk daukazu [konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
-   Esportatutako segmentuetako bezero profil bateratuek helbide elektroniko bat eta Braze bezero ID bat adierazten duten eremu bat dute. 

## <a name="known-limitations"></a>Muga ezagunak

- Braze-ra esportatzea segmentuetara mugatzen da.
- Gehienez milioi bat bezero-profil Braze-ra esportatzeak 40 minutu behar izan ditzake osatzeko. 
- Braze-ra esporta ditzakezun bezero-profilen kopurua Braze-rekin duzun kontratuaren menpe dago eta mugatuta dago.

## <a name="set-up-connection-to-braze"></a>Konfiguratu Braze-rekin konexioa

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Braze** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman zure [Braze API gakoa](https://www.braze.com/docs/api/basics/) saioa hasten jarraitzeko. 

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Hautatu **Konektatu** Braze-rako konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Braze ataleko. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.  

3. urtean **Datuen parekatzea** atalean, in **Posta elektronikoa** eremuan, hautatu bezero baten helbide elektronikoa adierazten duen eremua, "Bezeroaren IDa" eremuan, hautatu bezeroaren Braze IDa adierazten duen eremua. Beharrezkoa da segmentuak Braze-ra esportatzeko. Braze-ko segmentuak atalean dagoen segmentuaren izen berarekin sortuko dira Dynamics 365 Customer Insights. Datuak parekatzeko aukerako eremu osagarriak hauta ditzakezu. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights Braze-ra datuak transmititzeko, datuen transferentzia onartzen duzu betetze-mugatik kanpo Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek transferituko ditu zure aginduetara, baina Braze-k izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeko ardura duzu. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
