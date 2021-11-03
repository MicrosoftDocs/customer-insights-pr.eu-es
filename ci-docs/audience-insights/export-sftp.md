---
title: Esportatu Customer Insights datuak SFTP ostalarietara
description: Ikasi konexioa nola konfiguratu eta SFTP kokapen batera esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: a54025588945e4db6ab800dca034520b5f08d49b
ms.sourcegitcommit: 31985755c7c973fb1eb540c52fd1451731d2bed2
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/22/2021
ms.locfileid: "7673901"
---
# <a name="export-segments-and-other-data-to-sftp-preview"></a>Esportatu segmentuak eta beste datu batzuk SFTP-ra (aurrebista)

Erabili zure bezeroen datuak hirugarrenen aplikazioetan, fitxategi transferentzia protokolo segurura (SFTP) kokapen batera esportatuz.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWO94X]

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

- SFTP ostalariaren erabilgarritasuna eta dagozkien egiaztagiriak.

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da. Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa. 
- Gehienez 100 milioi bezero profil dituzten entitate esportatzaileek 90 minutu iraun dezakete gomendatutako gutxieneko konfigurazioa erabiltzen duten bi PUZ nukleorekin eta 1 Gb memoria. 

## <a name="set-up-connection-to-sftp"></a>Konfiguratu konexioa SFTP-en

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **SFTP** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman SFTP kontuaren **Erabiltzaile-izena**, **Pasahitza**, **Ostalari-izena** eta **Esportazio-karpeta**.

1. Hautatu **Egiaztatu** konexioa probatzeko.

1. Aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimatu gabe** eta **eremu mugatzailea** esportatutako fitxategietarako.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SFTP sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Aukeratu entitateak, adibidez, esportatu nahi dituzun segmentuak.

   > [!NOTE]
   > Aukeratutako entitate bakoitza bost irteerako fitxategitan banatuko da esportatzerakoan. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
