---
title: Esportatu datuak SFTP ostalarietara (aurrebista) (bideoa dauka)
description: Ikasi konexioa nola konfiguratu eta SFTP kokapen batera esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: b12d25ecbd2e5fb31d7d5a6bb775dc3e7c1bf007
ms.sourcegitcommit: 5807b7d8c822925b727b099713a74ce2cb7897ba
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/28/2022
ms.locfileid: "9207214"
---
# <a name="export-data-to-sftp-hosts-preview"></a>Esportatu datuak SFTP ostalarietara (aurrebista)

Erabili zure bezeroen datuak hirugarrenen aplikazioetan, fitxategi transferentzia protokolo segurura (SFTP) kokapen batera esportatuz.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWO94X]

## <a name="prerequisites"></a>Aurrebaldintzak

- SFTP ostalariaren erabilgarritasuna eta dagozkien egiaztagiriak.

## <a name="known-limitations"></a>Muga ezagunak

- Suebakien atzean dauden SFTP helmugak ez dira onartzen oraingoz.
- Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da. Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa.
- Gehienez 100 milioi bezero-profil, 90 minutu iraun ditzakete bi CPU-nukleoen eta 1 Gb-ko memoriaren konfigurazio minimoa erabiltzean.
- Autentifikaziorako SSH gako bat erabiltzen baduzu, ziurtatu duzula [sortu zure gako pribatua](/azure/virtual-machines/linux/create-ssh-keys-detailed#basic-example) PEM edo SSH.COM formatuan. Putty erabiltzen ari bazara, bihurtu zure gako pribatua esportatuz Open SSH gisa. Gako pribatuen formatu hauek onartzen dira:
  - RSA OpenSSL PEM eta ssh.com formatuan
  - DSA OpenSSL PEM eta ssh.com formatuan
  - ECDSA 256/384/521 OpenSSL PEM formatuan
  - ED25519 eta RSA OpenSSH gako formatuan

## <a name="set-up-connection-to-sftp"></a>Konfiguratu konexioa SFTP-en

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **SFTP**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Aukeratu zure konexiorako SSH edo erabiltzaile-izena/pasahitza bidez autentifikatu nahi duzun eta eman beharrezko xehetasunak. Autentifikaziorako SSH gako bat erabiltzen baduzu, ziurtatu duzula [sortu zure gako pribatua](/azure/virtual-machines/linux/create-ssh-keys-detailed#basic-example) PEM edo SSH.COM formatuan. Putty erabiltzen ari bazara, bihurtu zure gako pribatua esportatuz Open SSH gisa. Gako pribatuen formatu hauek onartzen dira:
   - RSA OpenSSL PEM eta ssh.com formatuan
   - DSA OpenSSL PEM eta ssh.com formatuan
   - ECDSA 256/384/521 OpenSSL PEM formatuan
   - ED25519 eta RSA OpenSSH gako formatuan

1. Hautatu **Egiaztatu** konexioa probatzeko.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SFTP sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimatu gabe** eta **eremu mugatzailea** esportatutako fitxategietarako.

1. Hautatu esportatu nahi dituzun entitateak, segmentuak adibidez.

   > [!NOTE]
   > Hautatutako entitate bakoitza gehienez bost irteera fitxategitan banatuko da esportatzen denean.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

> [!TIP]
> Datu kopuru handia duten entitateen esportazioak CSV fitxategi anitz ekar ditzake esportazio bakoitzerako karpeta berean. Esportazioen zatiketa errendimendu arrazoiengatik gertatzen da esportazio bat burutzeko behar den denbora gutxitzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
