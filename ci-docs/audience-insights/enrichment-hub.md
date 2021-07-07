---
title: Aberastu bezeroen profil bateratuak
description: Erabili gaitasunak zure bezeroaren datuak aberasteko.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: c35e73b366fcd5db2ba5a757295ddda6db30efa0
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305233"
---
# <a name="enrichment-for-customer-profiles-preview"></a>Bezeroen profiletarako aberastea (aurrebista)

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak bezeroaren datuak aberasteko.

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Aberasteko gunearen orria":::

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

Aukeratu aberastasuna eskuragarri dauden aukerak ikusteko. Zerrenda bateko elipsia (...) ere hauta dezakezu aukerak ikusteko.

:::image type="content" source="media/enrichment-hub-options-run.png" alt-text="Aberastasunen zerrendan aberastasunak kudeatzeko aukerak":::

- **ikusi** aberastasun xehetasunak bezeroen profil aberastuen kopuruarekin.
- **Editatu** aberastasunaren konfigurazioa.
- **Korrika egin** bezeroen profilak azken datuekin eguneratzeko aberastasuna.
- **Desaktibatu** lehendik dagoen aberastasuna programatutako freskatze automatikoekin automatikoki freskatzeari uzteko. Azken freskatze arrakastatsuaren datuak erabilgarri egongo dira. **Aktibatu** aberastu aktiboa, freskatze automatikoa programatutako freskapen guztiekin berrabiarazteko.
- **Ezabatu** aberastea.

Aberastasun anitz exekutatu edo desaktiba ditzakezu aldi berean zerrendan hautatuta. Ikusi eta editatzeko aukerak ez daude eskuragarri gisa eta soilik aberasteko soilik funtzionatzen du.

## <a name="enrichments-and-connections"></a>Aberasteak eta konexioak

Hirugarrenen aberastasunak erabiliz konfiguratzen dira [konexioak](connections.md), administratzaileak kredentzialekin konfiguratzen duena eta datuak transferitzeko baimena ematen duena. Konexioa erabil daiteke administratzaileen eta laguntzaileen bitartez aberasteak konfiguratzeko.  

## <a name="multiple-enrichments-of-the-same-type"></a>Mota bereko hainbat aberastasun

Aberastu nahi den entitatea aberasteko konfigurazioan zehazten da eta horrek zure profilen azpimultzo bat soilik aberastea ahalbidetzen du. Adibidez, aberastu datuak segmentu zehatz baterako soilik. Mota bereko hainbat aberastasun konfigura ditzakezu eta konexio bera berrerabili. Zenbait aberastasunek sor ditzaketen mota bereko aberastasunen kopuruak izango dituzte mugak. Mugak eta egungo erabilera webgunean ikus daitezke **Aberastea** orrialdea.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
