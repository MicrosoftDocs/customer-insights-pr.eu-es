---
title: Esportatu Customer Insights datuak SendGrid-era
description: Ikasi konexioa nola konfiguratu eta SendGrid-era esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: a4c64cf77c682e07f3d0759c43355336b5806fc8
ms.sourcegitcommit: 1b671c6100991fea1cace04b5d4fcedcd88aa94f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "5759750"
---
# <a name="export-segments-to-sendgrid-preview"></a>Esportatu segmentuak SendGrid-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak SendGrid kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko SendGrid-en. 

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [SendGrid kontua](https://sendgrid.com/) eta dagozkion administratzaile kredentzialak.
-   SendGrid-en kontaktu-zerrendak eta dagozkien IDak daude. Informazio gehiagorako, ikus [SendGrid: kudeatu kontaktuak](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts).
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 100.000 profil guztira SendGrid-era.
- SendGrid-era esportatzea segmentuetara mugatuta dago.
- SendGrid-era 100.000 profil gehienera esportatzeak ordu batzuk behar izan ditzake osatzeko. 
- SendGrid-era esporta ditzakezun profilen kopurua SendGrid-ekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="set-up-connection-to-sendgrid"></a>Konfiguratu konexioa SendGrid-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **SendGrid** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure **SendGrid API gakoa** [SendGrid API gakoa](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** SendGrid-eko konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SendGrid sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Sartu zure **[SendGrid zerrendaren IDa](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts)**.

1. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **herrialdea/eskualdea**, **estatua**, **hiria** eta **posta kodea**.

1. Hautatu esportatu nahi dituzun segmentuak. Biziki **gomendatzen dugu 100.000 bezero profil baino gehiago ez esportatzea guztira** SendGrid-era. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak SendGrid-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da SendGrid-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]