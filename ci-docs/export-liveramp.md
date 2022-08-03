---
title: Esportatu segmentuak LiveRamp-era (aurrebista)
description: Ikasi konexioa eta esportazioa LiveRamp-era nola konfiguratu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 55eacea3af83f46583a3a43797d625479f56586b
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196701"
---
# <a name="export-segments-to-liverampreg-preview"></a>Esportatu segmentuak LiveRamp-era&reg; (aurrebista)

Aktibatu zure datuak LiveRamp-en 500 plataforma baino gehiagorekin konektatzeko telebista digitaletan, sozialetan eta telebistetan. Lan egin LiveRamp-ekin zure datuekin iragarki-kanpainak zuzentzeko, ezabatzeko eta pertsonalizatzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- LiveRamp harpidetza bat konektore hau erabiltzeko. Harpidetza lortzeko, [jarri harremanetan LiveRamp-ekin](https://liveramp.com/contact/) zuzenean. [Argibide gehiago LiveRamp Onboarding-i buruz](https://liveramp.com/our-platform/data-onboarding/).

## <a name="known-limitations"></a>Muga ezagunak

- LiveRamp esportazioa SFTP esportazio bat erabiltzen ari da. Suebakien atzean dauden SFTP helmugak ez dira onartzen oraingoz.
- Autentifikaziorako SSH gako bat erabiltzen baduzu, ziurtatu duzula [sortu zure gako pribatua](/azure/virtual-machines/linux/create-ssh-keys-detailed#basic-example) PEM edo SSH.COM formatuan. Putty erabiltzen ari bazara, bihurtu zure gako pribatua esportatuz Open SSH gisa. Gako pribatuen formatu hauek onartzen dira:
  - RSA OpenSSL PEM eta ssh.com formatuan
  - DSA OpenSSL PEM eta ssh.com formatuan
  - ECDSA 256/384/521 OpenSSL PEM formatuan
  - ED25519 eta RSA OpenSSH gako formatuan
- Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da. Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa.
- Gehienez 100 milioi bezero profil dituzten entitate esportatzaileek 90 minutu iraun dezakete gomendatutako gutxieneko konfigurazioa erabiltzen duten bi PUZ nukleorekin eta 1 Gb memoria.
- LiveRamp-era esporta ditzakezun profil (edo datu) benetako kopurua LiveRamp-ekin duzun harpidetzaren araberakoa da.

## <a name="set-up-connection-to-liveramp"></a>Konfiguratu konexioa LiveRamp-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **LiveRamp**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu zure konexiorako SSH edo erabiltzaile-izena/pasahitza bidez autentifikatu nahi duzun eta eman beharrezko xehetasunak.

1. Aukeratu **Ziurtatu** LiveRamp-ekin konexioa probatzeko.

1. Egiaztatu ondoren, berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **Ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa LiveRamp sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. urtean **Konektatu datuak** eremua, hautatu **Posta elektronikoa**, **eta helbidea**, edo **Mugikorra** LiveRamp-era bidaltzeko identitatea konpontzeko.

   :::image type="content" source="media/export-liveramp-segments.png" alt-text="LiveRamp konektorea atributuen mapak.":::

1. Mapatu dagozkien atributuak zure *Bezeroa* hautatutako gako identifikatzailearen entitatea.

1. Hautatu **Gehitu atributua** LiveRamp-era bidalitako atributu gehiago jarraitzeko.

   > [!TIP]
   > LiveRamp erabiltzaileari gako identifikatzaile atributu gehiago bidaltzeak baliteke partidu tasa handiagoa lortzea.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
