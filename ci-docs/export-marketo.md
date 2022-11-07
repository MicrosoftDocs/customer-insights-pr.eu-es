---
title: Esportatu segmentuak Marketo-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta Marketo-ra esportatzen.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: cba40b74b86a40fc41db856760c9361b755a8864
ms.sourcegitcommit: c3ae7e7e0c9566f9479ba71a26afc5a17fb589c2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/27/2022
ms.locfileid: "9724925"
---
# <a name="export-segments-to-marketo-preview"></a>Esportatu segmentuak Marketo-era (aurrebista)

Kanpainak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzak erabiltzeko Marketo bidez, esportatu bezeroen profil bateratuetako segmentuak.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Marketo kontua](https://login.marketo.com/) eta dagozkion administratzailearen kredentzialak.
- A [Marketo bezeroaren IDa, Bezeroaren sekretua eta REST Endpoint Hostname izena](https://developers.marketo.com/rest-api/authentication/).
- [Marketon dauden zerrendak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists) eta dagozkion NANak.
- [Konfiguratutako segmentuak](segments.md).
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Ez da onartzen Bring your own storage (BYOS) esteka pribatua.
- Gehienez milioi bat bezero-profil Marketo-ra esportazio bakoitzeko, eta horrek 3 ordu iraun dezake. Marketo-ra esporta dezakezun bezero-profilen kopurua Marketorekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-marketo"></a>Konfiguratu konexioa Marketo-ra

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Marketo**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure **Marketo bezeroaren IDa, Bezeroaren sekretua eta REST Endpoint Hostname izena**. REST Endpoint ostalari izena ostalari izena soilik da, gabe https://. Adibidea: xyz-abc-123.mktorest.com.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Marketo sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **Marketo zerrendaren IDa**. Zerrendaren IDa zenbaki hutsa da. Adibidez, zure Marketo zerrendako IDa ST12345A7 bada, kendu zenbakien aurreko eta ondorengo karakterea eta idatzi *12345*.

1. urtean **Datuen parekatzea** atalean, hautatu bezero baten helbide elektronikoa edo bezero baten Marketo IDa adierazten duen eremu bat gutxienez.

1. Aukeran, esportatu **izen**, **·**, **·**, **·**, eta **Herrialdea/Eskualdea** mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

Marketo-n, aurkitu zure segmentuak azpian [Marketo zerrendak](https://docs.marketo.com/display/public/DOCS/Understanding+Static+Lists).

[!INCLUDE [footer-include](includes/footer-banner.md)]
