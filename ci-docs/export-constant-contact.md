---
title: Esportatu segmentuak Constant Contact-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Constant Contact.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: c0affd3ed45f462696850813bd50331061dde780
ms.sourcegitcommit: c3ae7e7e0c9566f9479ba71a26afc5a17fb589c2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/27/2022
ms.locfileid: "9724486"
---
# <a name="export-segments-to-constant-contact-preview"></a>Esportatu segmentuak Constant Contact-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Constant Contact eta erabili marketin jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Kontaktu etengabeko kontua](https://www.constantcontact.com/account-home) eta dagozkion administratzailearen kredentzialak.
- A [Kontaktu zerrendaren ID etengabea](https://app.constantcontact.com/pages/contacts/ui#lists). Ireki zerrenda bat Constant Contact URL zerrendaren IDa aurkitzeko.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Ez da onartzen Bring your own storage (BYOS) esteka pribatua.
- Gehienez milioi bat bezero-profil esportatzen ditu Constant Contact-era, eta hori osatzeko ordubete behar izan daiteke. Constant Contact-era esporta ditzakezun bezero-profilen kopurua Constant Contact-ekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-constant-contact"></a>Konfiguratu konexioa Constant Contact-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Etengabeko kontaktua**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Egiaztatu Constant Contact-ekin** eta eman zure administratzaile kredentzialak Constant Contact-erako.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Constant Contact sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **Kontaktu zerrendaren ID etengabea**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, esportatu **izen** eta **abizen** eremu osagarri gisa mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
