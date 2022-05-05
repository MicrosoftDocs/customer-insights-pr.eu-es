---
title: Esportatu Customer Insights datuak SendGrid-era
description: Ikasi konexioa nola konfiguratu eta SendGrid-era esportatu.
ms.date: 10/08/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 38dd782fdf06d5970e79e6deb6e8fc94252da585
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642159"
---
# <a name="export-segments-to-sendgrid-preview"></a>Esportatu segmentuak SendGrid-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak SendGrid kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko SendGrid-en. 

## <a name="prerequisites-for-a-connection"></a>Konexioaren aurrebaldintzak

-   Baduzu [SendGrid kontua](https://sendgrid.com/) eta dagozkion administratzaile kredentzialak.
-   SendGrid-en kontaktu-zerrendak eta dagozkien IDak daude. Informazio gehiagorako, ikus [SendGrid: kudeatu kontaktuak](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts).
-   Zuk daukazu [konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- 100.000 bezero profil gehienez guztira SendGrid-era.
- SendGrid-era esportatzea segmentuetara mugatuta dago.
- 100.000 arte bezero profil SendGrid-en dituzten segmentuak esportatzen ordu gutxi behar izan ditzakete osatzeko. 
- SendGrid-era esporta ditzakezun bezeroen profil kopurua SendGrid-ekin duzun kontratuaren menpe dago eta mugatua da.

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

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua. Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **herrialdea/eskualdea**, **estatua**, **hiria** eta **posta kodea**.

1. Hautatu esportatu nahi dituzun segmentuak. Biziki **gomendatzen dugu 100.000 bezero profil baino gehiago ez esportatzea guztira** SendGrid-era. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak SendGrid-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da SendGrid-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE [footer-include](includes/footer-banner.md)]
