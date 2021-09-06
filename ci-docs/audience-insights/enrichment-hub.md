---
title: Aberastu bezeroen profil bateratuak
description: Erabili gaitasunak zure bezeroaren datuak aberasteko.
ms.date: 07/01/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: a64bbd754d4013d0a6243074ac9f55991547be82b269047a9937b583baf98697
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7032513"
---
# <a name="enrichment-for-customer-profiles-preview"></a>Bezeroen profiletarako aberastea (aurrebista)

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak bezeroaren datuak aberasteko.

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Aberasteko gunearen orria.":::

Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** aberasteko aukerekin lan egiteko.  

Laguntzaileak edo Administratzaileak baimenak izan behar dituzu aberastasunak sortzeko edo editatzeko. Informazio gehiago lortzeko, [Baimenak](permissions.md).

Gainean **Ezagutu** fitxa, aberastasun hauek aurkituko dituzu:

- [Markak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- [Interesak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- [Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita
- [Enpresaren datuak](enrichment-leadspace.md) , Leadspace-k emanak
- Experian-ek eskainitako [datu demografikoak](enrichment-experian.md)
- [Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak
- [Datu pertsonalizatuak](enrichment-SFTP-custom-import.md) fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) bidez

Gainean **Nire aberastasunak** fitxan, konfiguratutako aberastasunak eta haien propietateak editatzen ikus ditzakezu.

## <a name="manage-existing-enrichments"></a>Lehendik dauden aberastasunak kudeatu

Joan **Nire aberastasunak** fitxa konfiguratutako aberastasun guztiak ikusteko. Aberastu bakoitza aberastearen inguruko informazio osagarria biltzen duen errenkada gisa irudikatzen da.

Aukeratu aberastea eskuragarri dauden aukerak ikusteko. Zerrenda bateko elipsia (...) ere hauta dezakezu aukerak ikusteko. Zenbait aberaste konfiguratu badituzu, bilaketa-koadroa erabil dezakezu azkar aurkitzeko.

:::image type="content" source="media/enrichment-hub-options-run.png" alt-text="Aberasteen zerrendan aberastasunak kudeatzeko aukerak.":::

- **ikusi** aberastasun xehetasunak bezeroen profil aberastuen kopuruarekin.
- **Editatu** aberastasunaren konfigurazioa.
- **Korrika egin** bezeroen profilak azken datuekin eguneratzeko aberastasuna.
- **Desaktibatu** lehendik dagoen aberastasuna programatutako freskatze automatikoekin automatikoki freskatzeari uzteko. Azken freskatze arrakastatsuaren datuak erabilgarri egongo dira. **Aktibatu** aberastu aktiboa, freskatze automatikoa programatutako freskapen guztiekin berrabiarazteko.
- **Ezabatu** aberastea.

Exekutatu edo desaktibatu aberaste anitz aldi berean zerrendan hautatuta. Ikusi eta editatu aukerak ez daude eskuragarri ekintza masibo gisa. Aldi berean aberaste baterako funtzionatzen egiten dute.

## <a name="enrichments-and-connections"></a>Aberasteak eta konexioak

Hirugarrenen aberastasunak erabiliz konfiguratzen dira [konexioak](connections.md), administratzaileak kredentzialekin konfiguratzen duena eta datuak transferitzeko baimena ematen duena. Konexioa erabil daiteke administratzaileen eta laguntzaileen bitartez aberasteak konfiguratzeko.  

## <a name="multiple-enrichments-of-the-same-type"></a>Mota bereko hainbat aberastasun

Aberastu nahi den entitatea aberasteko konfigurazioan zehazten da eta horrek zure profilen azpimultzo bat soilik aberastea ahalbidetzen du. Adibidez, aberastu datuak segmentu zehatz baterako soilik. Mota bereko hainbat aberastasun konfigura ditzakezu eta konexio bera berrerabili. Zenbait aberastasunek sor ditzaketen mota bereko aberastasunen kopuruak izango dituzte mugak. Mugak eta egungo erabilera webgunean ikus daitezke **Aberastea** orrialdea.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
