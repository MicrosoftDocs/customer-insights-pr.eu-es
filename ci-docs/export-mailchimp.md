---
title: Esportatu segmentuak Mailchimp-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta Mailchimp-era esportatzen.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 54aec10e24b6356e2e4317cf33e740a1a086a2dd
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196839"
---
# <a name="export-segments-to-mailchimp-preview"></a>Esportatu segmentuak Mailchimp-era (aurrebista)

Esportatu bezero profil bateratuen segmentuak Mailchimp-era buletinak eta posta elektronikoko kanpainak sortzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Mailchimp kontua](https://mailchimp.com/) eta dagozkion administratzailearen kredentzialak.
- [Mailchimp-en dauden publikoak](https://mailchimp.com/help/create-audience/) eta dagozkionak [ikusleen IDak](https://mailchimp.com/help/find-audience-id/).
- [Konfiguratutako segmentuak](segments.md).
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Mailchimp-era esportazio bakoitzeko milioi bat bezero-profil gehienez, hiru ordu iraun ditzake. Mailchimp-era esporta ditzakezun bezero-profilen kopurua Mailchimp-ekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-mailchimp"></a>Konfiguratu konexioa Mailchimp-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Mailchimp**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Egiaztatu Mailchimp-ekin** eta eman zure Mailchimp kredentzialak.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Mailchimp sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **Mailchimp audientzia ID**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, esportatu **izen** eta **abizen** mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
