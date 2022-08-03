---
title: Esportatu segmentuak Sendinblue-ra (aurrebista)
description: Ikasi konexioa nola konfiguratu eta Sendinblue-ra esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 816a3b242fadaa5a75db878adf0a76baf638e41c
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196931"
---
# <a name="export-segments-to-sendinblue-preview"></a>Esportatu segmentuak Sendinblue-ra (aurrebista)

Esportatu bezero profil bateratuen segmentuak kanpaniak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzei etekinik handiena ateratzeko Sendinblue bidez.

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Sendinblue kontua](https://www.sendinblue.com/) eta dagozkion administratzailearen kredentzialak.
- A [SendinBlue API gakoa](https://developers.sendinblue.com/docs/getting-started#:~:text=Get%20your%20API%20key&text=You%20can%20create%20one%20from,your%20settings%20This%20API%20key).
- Sendinblue-n dauden zerrendak eta dagozkion IDak.
- [Konfiguratutako segmentuak](segments.md).
- Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="known-limitations"></a>Muga ezagunak

- Milioi bat bezero-profil gehienez Sendinblue-ra esportatzeko, 90 minutu arte iraun dezaketenak osatzeko. Sendinblue-ra esporta ditzakezun bezero-profilen kopurua Sendinbluerekin duzun kontratuaren araberakoa da.
- Segmentuak soilik.

## <a name="set-up-connection-to-sendinblue"></a>Konfiguratu Sendinblue-ra konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Sendinblue**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu zure **SendinBlue API gakoa**.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Konektatu** konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Urtean **Esportaziorako konexioa** eremuan, aukeratu konexio bat Sendinblue atalean. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Sartu zure **Sendinblue zerrendaren IDa**.

1. Urtean **Datuen bat etortzea** atalean, **Posta elektronikoa** eremua, hautatu bezeroaren helbide elektronikoa adierazten duen eremua.

1. Aukeran, esportatu **izen**, **·**, eta **Mugikorra** mezu elektroniko pertsonalizatuagoak sortzeko. Aukeratu **Gehitu atributua** eremu horiek esleitzeko.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
