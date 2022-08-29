---
title: Esportatu segmentuak LinkedIn Ads-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta LinkedIn Ads-era esportatzen.
ms.date: 08/12/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 4c3928e05db0ebda262b4ad3e928ce85f70035b9
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304688"
---
# <a name="export-segments-to-linkedin-ads-preview"></a>Esportatu segmentuak LinkedIn Ads-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak LinkedIn Ads-era bat datozen hartzaileak sortzeko. Erabili bat datozen hartzaileak enpresaren bideratzerako eta kontaktuen bideratzerako.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [LinkedIn Campaign Manager kontua](https://business.linkedin.com/marketing-solutions/ads) eta dagozkion administratzailearen kredentzialak.
- A [LinkedIn Campaign Manager Kontuaren IDa](https://www.linkedin.com/help/lms/answer/a424270).
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuek gutxienez eremu zehatz bat behar dute aukeratzen duzun ala ez kontuan hartuta [harremanetarako bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/contact-targeting) edo [enpresaren bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/account-targeting) LinkedIn-en. Eremu posibleak zerrendan ageri dira **Datuen parekatzea** urratsa noiz [esportazioa konfiguratzea](#configure-an-export).

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 100.000 bezero-profil esportazio bakoitzeko LinkedIn Ads-era, eta hori osatzeko 10 minutu iraun ditzake.
- Segmentuak soilik. Segmentu batek gutxienez 300 profil esklusibo izan behar ditu.

## <a name="set-up-connection-to-linkedin-ads"></a>Konfiguratu konexioa LinkedIn Ads-ekin

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **LinkedIn Iragarkiak**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman zure LinkedIn Campaign Manager Kontuaren IDa.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Autentifikatu LinkedIn-ekin** eta eman zure administratzaile egiaztagiriak LinkedIn Campaign Manager-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa LinkedIn Ads sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Aukeratu egin nahi dituzun datuak esportatu nahi dituzun ala ez [kontaktuen bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/contact-targeting) edo [enpresen bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/account-targeting) egiteko LinkedIn-en.

1. Urtean **Datuen bat etortzea** atalean, kontaktuak bideratzeko, hautatu bezeroaren helbide elektronikoa, Apple Ad IDa, Google Ad IDa, Google Erabiltzailearen IDa edo first eta abizen adierazten duen eremu bat gutxienez. Enpresaren bideratzea aukeratzen baduzu, hautatu gutxienez enpresaren izena, posta elektronikoaren domeinua, LinkedIn orriaren URLa, Stock ikurra edo Webgunea adierazten duen eremua.

1. Aukeran, gehitu eremuak zure esportazioa gehiago definitzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak. LinkedIn Campaign Manager-eko bat datozen hartzaileak automatikoki sortuko dira esportatzeko hautatu dituzun segmentuen izenarekin. Segmentu bakoitzak bat datorren hartzaile bereizi bat sortuko du.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
