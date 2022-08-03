---
title: Esportatu segmentuak DotDigital-era (aurrebista)
description: Ikasi konexioa nola konfiguratu eta DotDigital-era esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: cabaea84e31f8fe97bc558a8dca8d93bc40f43b7
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196057"
---
# <a name="export-segments-to-dotdigital-preview"></a>Esportatu segmentuak DotDigital-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak DotDigital helbide liburuetara eta erabili kanpainetarako, posta elektroniko bidezko marketinerako eta DotDigital-ekin bezero segmentuak eraikitzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [DotDigital kontua](https://dotdigital.com/) eta bat [API erabiltzailea](https://support.dotdigital.com/hc/articles/115001718730-How-do-I-create-an-API-user).
- DotDigital ID bat a [berria](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book) edo DotDigital-en dagoen helbide-liburua. IDa URLan aurki daiteke helbide-liburua hautatu eta irekitzean.
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero-profil DotDigital-era esportatzeko, hiru ordu iraun ditzake osatzeko hornitzailearen aldetik dauden mugak direla eta. DotDigital-era esporta dezakezun bezero-profilen kopurua DotDigital-ekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-dotdigital"></a>Konfiguratu konexioa DotDigital-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **DotDigital**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Idatzi **DotDigital-eko API erabiltzaile-izena eta pasahitza**.

1. Sartu zure **DotDigital helbide-liburuaren IDa**.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa DotDigital sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, esportatu **izen**, **·**, **osoa**, **·**, eta **Posta kodea**.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

DotDigital-en, aurkitu zure segmentuak hemen [DotDigital helbide-liburuak](https://support.dotdigital.com/hc/articles/212211968-Creating-an-address-book).

[!INCLUDE [footer-include](includes/footer-banner.md)]
