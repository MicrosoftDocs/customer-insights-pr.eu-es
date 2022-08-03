---
title: Esportatu segmentuak Omnisend-era (aurrebista)
description: Ikasi konexioa nola konfiguratu eta Omnisend-era esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: c23d6d3538c4df6006c14064f95379169af06622
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196149"
---
# <a name="export-segments-to-omnisend-preview"></a>Esportatu segmentuak Omnisend-era (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak Omnisend-era eta erabili marketin jardueretarako.

## <a name="prerequisites"></a>Aurrebaldintzak

- An [Omnisend kontua](https://www.omnisend.com/) eta dagozkion administratzailearen kredentzialak.
- An [Omnisend API gakoa](https://support.omnisend.com/en/articles/1061890-generating-api-key).
- [Konfiguratutako segmentuak](segments.md) Bezeroen Insights-en.
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez milioi bat bezero profil Omnisend-era esportatzeko, eta hori lau ordu behar izan daiteke osatzeko. Omnisend-era esporta ditzakezun bezeroen profil kopurua Omnisend-ekin duzun kontratuaren menpe dago.
- Segmentuak soilik.

## <a name="set-up-connection-to-omnisend"></a>Konfiguratu konexioa Omnisend-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Omnisend**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure Omnisend-en API gakoa.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Omnisend sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, esportatu **izen**, **·**, **·**, **/Eskualdea**, **·**, **·**, eta **Posta Kodea** mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
