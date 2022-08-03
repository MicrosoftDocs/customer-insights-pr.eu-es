---
title: Esportatu segmentuak hona Facebook Iragarkien kudeatzailea (aurrebista) (bideoa dauka)
description: Ikasi konexioa konfiguratzen eta esportatzen Facebook Iragarkien kudeatzailea.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 01be1a075db0da05dc5536aea8a33093f9a2ea13
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9194999"
---
# <a name="export-segments-to-facebook-ads-manager-preview"></a>Esportatu segmentuak hona Facebook Iragarkien kudeatzailea (aurrebista)

Bezeroen profil bateratuen segmentuak esportatu Facebook Iragarkien kudeatzailea kanpainak sortzeko Facebook eta Instagram.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWO1aN]

## <a name="prerequisites"></a>Aurrebaldintzak

- A [Facebook Iragarkien kontua](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account) a barne hartzen duena [Facebook Enpresa kontua](https://business.facebook.com/).
- Administratzailearen pribilegioak [Facebook Iragarkien kontua](https://www.facebook.com/business/learn/lessons/step-by-step-ads-manager-account).

## <a name="known-limitations"></a>Muga ezagunak

- 10 milioi bezero-profil gehienez esportazio bakoitzeko Facebook Iragarkien kudeatzailea, 90 minutu arte iraun dezake.
- Segmentuak soilik.
- Facebook *bezeroen zerrenda* idatzi [publiko pertsonalizatuak](https://www.facebook.com/business/help/744354708981227?id=2469097953376494) bakarrik.
  > [!NOTE]
  > Zenbait kasutan, goitibeherako zerrendan mota ezberdinetako audientzia pertsonalizatuak ikus ditzakezu. Beste mota bat hautatzen baduzu *bezeroen zerrenda*, esportazioak huts egiten du.

## <a name="set-up-connection-to-facebook-ads-manager"></a>Konfiguratu konexioa Facebook iragarkien kudeatzailea

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Facebook Iragarkien kudeatzailea**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. [Eman kolaboratzaileei konexioa esportatzeko erabiltzeko](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Autentifikatu Facebook iragarkiekin:

   1. Aukeratu **Jarraitu honekin Facebook** zure saioa hasteko Facebook Iragarkien kontua.

   1. Onartu **iragarkien kudeaketa** baimena, Facebook-ekin autentifikatu ondoren.

   1. Hautatu **Facebook iragarki kontua** lan egin nahi duzunarekin.

   1. Aukeratu **Lehendik dagoen publiko pertsonalizatua** goitibeherako zerrendatik edo sortu **Publiko pertsonalizatu berria**.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. urtean **Esportatzeko konexioa** eremuan, aukeratu konexio bat Facebook Iragarkien kudeatzailea atala. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. urtean **Konektatu datuak** eremua, hautatu **Posta elektronikoa**, **eta helbidea**, edo **Mugikorra** helbidera bidaltzeko Facebook Iragarkien kudeatzailea.

1. Aukeratu hautatutako gako identifikatzaileari zure bezeroen erakunde bateratuari dagozkion atributuak.
   > [!TIP]
   > Aukera onenak hautatuta baldin badaude **Helbide elektronikoa** gako identifikatzaile gisa. Identifikatzaile osagarriak gehitzeak bat egin dezake.

1. Aukeratu **Gehitu atributua** bidali beharreko atributu gehiago mapatzeko Facebook Iragarkien kudeatzailea. Atributuak Facebook Iragarkien kudeatzailea erabiltzaileentzako lagunarteko izen hauek kokatzen dira: **FN** = **izena**, **LN** = **abizena**, **FI** = **Lehen Hasierakoa**, **TELEFONOA** = **Telefonoa**, **GEN** = **Generoa**, **DOB** = **Jaioteguna**, **ST** = **Estatu**, **CT** = **hiria**, **ZIP** = **Posta kodea / zip-kodea**, **HERRIALDEA** = **Herrialdea / Eskualdea**

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
