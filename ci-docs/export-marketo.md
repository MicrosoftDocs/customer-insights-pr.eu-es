---
title: Esportatu Customer Insights datuak Marketo-ra
description: Ikasi konexioa konfiguratzen eta Marketo-ra esportatzen.
ms.date: 10/08/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 7354b0aeafbe95e60d172b16c26d83c5dc25fb96
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642186"
---
# <a name="export-segments-to-marketo-preview"></a>Esportatu segmentuak Marketo-era (aurrebista)

Kanpainak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzak erabiltzeko Marketo bidez, esportatu bezeroen profil bateratuetako segmentuak.

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [Marketo kontua](https://login.marketo.com/) eta dagozkion administratzaile kredentzialak.
-   Marketo-n zerrendak eta dagozkien IDak daude. Informazio gehiagorako, ikus [Marketo-ko zerrendak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).
-   [Konfiguratutako segmentuak](segments.md) dituzu.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero-profil Marketo-ra esportatzeko.
- Marketo-ra esportatzea segmentuetara mugatuta dago.
- Guztira milioi bat bezero profil dituzten segmentuak esportatzeak hiru ordu arte iraun dezake. 
- Marketo-ra esporta ditzakezun bezeroen profil kopurua Marketo-rekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="set-up-connection-to-marketo"></a>Konfiguratu konexioa Marketo-ra

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Marketo** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure **[Marketo-ren bezeroaren IDa, Bezeroaren sekretua eta REST amaiera-puntuaren ostalari izena](https://developers.marketo.com/rest-api/authentication/)**. REST Endpoint ostalari izena ostalari izena soilik da, gabe `https://`. Adibidez: `xyz-abc-123.mktorest.com`. 

1. Aukeratu **ados** **Datu-pribatutasuna eta arau-betetzea** onartzeko eta hautatu **Konektatu** Marketo-rekin konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Marketo sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Idatzi **[Marketo zerrendaren IDa](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists)**. Zerrendaren IDa zenbaki hutsa da. Adibidez, Marketo zerrendaren IDa ST12345A7 bada, kendu karakterea zenbakien aurretik eta ondoren eta idatzi `12345`. 

1. urtean **Datuen parekatzea** atalean, hautatu bezero baten helbide elektronikoa edo bezero baten Marketo IDa adierazten duen eremu bat gutxienez. 

1. Aukeran, esporta dezakezu **Izena**, **Abizena**, **Hiria**, **Egoera** eta **Herrialdea/eskualdea** mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak. Guztira 1 milioi bezero profil esporta ditzakezu Marketo-ra.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). Marketo-n, zure segmentuak azpian aurki ditzakezu hemen: [Marketo-ko hartzaileak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).


## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak Marketo-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Marketo-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE [footer-include](includes/footer-banner.md)]