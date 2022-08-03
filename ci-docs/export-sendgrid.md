---
title: Esportatu segmentuak SendGrid-era (aurrebista)
description: Ikasi konexioa nola konfiguratu eta SendGrid-era esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: f2990ad410dda0cbf952f82f3fc30b3a53a7bcd4
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196977"
---
# <a name="export-segments-to-sendgrid-preview"></a>Esportatu segmentuak SendGrid-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak SendGrid kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko SendGrid-en.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [SendGrid kontua](https://sendgrid.com/) eta dagozkion administratzailearen kredentzialak.
- [SendGrid-en dauden kontaktuen zerrendak](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts) eta dagozkion NANak.
- A [SendGrid API gakoa](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 100.000 bezero-profil guztira SendGrid-era, eta horrek ordu batzuk behar izan ditzake osatzeko. SendGrid-era esporta ditzakezun bezero-profilen kopurua SendGrid-ekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-sendgrid"></a>Konfiguratu konexioa SendGrid-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **SendGrid**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure **SendGrid API gakoa**.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SendGrid sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **SendGrid zerrendaren IDa**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, hautatu eremuak, hala nola **izen**, **·**, **/Eskualdea**, **·**, **·**, eta **Posta kodea**.

1. Hautatu esportatu nahi dituzun segmentuak ezagutzen diren mugei jarraituz.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
