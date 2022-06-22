---
title: Aberastu bezeroen profil bateratuak
description: Erabili gaitasunak zure bezeroaren datuak aberasteko.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.custom: intro-internal
searchScope:
- ci-enrichments
- ci-enrichment-details
- ci-enrichment-wizard
- customerInsights
ms.openlocfilehash: 3bbe8b829a6698da55d84709dbab6c36aa76792a
ms.sourcegitcommit: 27c5473eecd851263e60b2b6c96f6c0a99d68acb
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954026"
---
# <a name="enrichment-for-customer-profiles-preview"></a>Bezeroen profiletarako aberastea (aurrebista)

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak bezeroaren datuak aberasteko.

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Aberasteko gunearen orria.":::

Joan **Datuak** > **Aberastea** aberasteko aukerekin lan egiteko.  

Laguntzaileak edo Administratzaileak baimenak izan behar dituzu aberastasunak sortzeko edo editatzeko. Informazio gehiago lortzeko, [Baimenak](permissions.md).

Gainean **Ezagutu** fitxa, onartutako aberasteko aukera guztiak aurkituko dituzu.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- [AbiliTec Identitatea](enrichment-liveramp.md) LiveRamp AbiliTec-ek emandakoa
- [Markak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- Experian-ek eskainitako [datu demografikoak](enrichment-experian.md)
- [Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita
- [Interesak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- [Kokapen datuak](enrichment-azure-maps.md) emandako Microsoft Azure Mapak
- [Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak
- [SFTP datu pertsonalizatuak](enrichment-SFTP-custom-import.md) Fitxategiak Transferitzeko Protokolo Seguruaren (SFTP) bidez

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- [Kontuaren partaidetza-datuak](enrichment-office.md) Microsoft-ek emandakoa
- [Enpresaren datuak](enrichment-dnb.md) Dun & Bradstreet-ek emandakoa
- [Enpresaren datuak](enrichment-leadspace.md) , Leadspace-k emanak
- [Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita
- [Enpresaren datu hobetuak](enrichment-enhanced-company-data.md) Microsoft-ek emandakoa
- [Kokapen datuak](enrichment-azure-maps.md) emandako Microsoft Azure Mapak
- [Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak
- [SFTP datu pertsonalizatuak](enrichment-SFTP-custom-import.md) Fitxategiak Transferitzeko Protokolo Seguruaren (SFTP) bidez

---

Gainean **Nire aberastasunak** fitxan, konfiguratutako aberastasunak eta haien propietateak editatzen ikus ditzakezu. Sortu ere egin dezakezu [segmentuak](segments.md) edo [neurriak](measures.md) aberasteetatik.

## <a name="manage-existing-enrichments"></a>Lehendik dauden aberastasunak kudeatu

Joan **Nire aberastasunak** fitxa konfiguratutako aberastasun guztiak ikusteko. Aberastu bakoitza aberastearen inguruko informazio osagarria biltzen duen errenkada gisa irudikatzen da.

Aukeratu aberastea eskuragarri dauden aukerak ikusteko. Elipse bertikala ere hauta dezakezu (&vellip;) zerrendako elementu batean aukerak ikusteko. Zenbait aberaste konfiguratu badituzu, bilaketa-koadroa erabil dezakezu azkar aurkitzeko.

:::image type="content" source="media/enrichment-hub-options-run.png" alt-text="Aberasteen zerrendan aberastasunak kudeatzeko aukerak.":::

- **ikusi** aberastasun xehetasunak bezeroen profil aberastuen kopuruarekin.
- **Editatu** aberastasunaren konfigurazioa.
- **Korrika egin** bezeroen profilak azken datuekin eguneratzeko aberastasuna.
- **Desaktibatu** lehendik dagoen aberastasuna programatutako freskatze automatikoekin automatikoki freskatzeari uzteko. Azken freskatze arrakastatsuaren datuak erabilgarri egongo dira. **Aktibatu** aberastu aktiboa, freskatze automatikoa programatutako freskapen guztiekin berrabiarazteko.
- **Ezabatu** aberastea.

Exekutatu edo desaktibatu aberaste anitz aldi berean zerrendan hautatuta. Ikusi eta editatu aukerak ez daude eskuragarri ekintza masibo gisa. Aldi berean aberaste baterako funtzionatzen egiten dute.

## <a name="enrichments-and-connections"></a>Aberasteak eta konexioak

Hirugarrenen aberastasunak erabiliz konfiguratzen dira [konexioak](connections.md), administratzaileak kredentzialekin konfiguratzen duena eta datuak transferitzeko baimena ematen duena. Konexioak erabil daitezke administratzaile eta langileen aldetik hobekuntzak konfiguratzeko.  

## <a name="multiple-enrichments-of-the-same-type"></a>Mota bereko hainbat aberastasun

Aberastu nahi den entitatea aberasteko konfigurazioan zehazten da eta horrek zure profilen azpimultzo bat soilik aberastea ahalbidetzen du. Adibidez, aberastu datuak segmentu zehatz baterako soilik. Mota bereko hainbat aberastasun konfigura ditzakezu eta konexio bera berrerabili. Zenbait aberastasunek sor ditzaketen mota bereko aberastasunen kopuruak izango dituzte mugak. Mugak eta egungo erabilera ikus daitezke fitxa bakoitzean **Ezagutu** fitxan **Aberastea** orrialdea.

## <a name="enrich-data-sources-before-unification"></a>Aberastu datu-iturriak bateratu aurretik

Zure bezeroen datuak aberastu ditzakezu datuak bateratu aurretik, datuen bat-etortzeen kalitatea areagotzen laguntzeko. Informazio gehiagorako, ikus [datu-iturburu aberastea](data-sources-enrichment.md).

## <a name="run-or-refresh-enrichments"></a>Exekutatu edo freskatu aberasgarriak

1. Aberaste-prozesua hasteko, hautatu **Korrika egin**. Edo, utzi sistemak aberastea automatikoki exekutatzen duen a [programatutako freskagarritasuna](system.md#schedule-tab). Prozesatzeko denbora zure bezeroen datuen tamainaren araberakoa da.

1. Aukeran, [aberaste prozesuaren aurrerapena ikusi](#see-the-progress-of-the-enrichment-process).

1. Aberaste-prozesua amaitu ondoren, joan hona **Nire aberastasunak** aberastu berri diren bezero-profilen datuak, azken eguneratzearen ordua eta aberastutako profil kopurua berrikusteko.

1. Hautatu aberastasuna ikusteko [aberaste emaitzak](#enrichment-results).

### <a name="see-the-progress-of-the-enrichment-process"></a>Ikusi aberaste-prozesuaren garapena

Aberaste-prozesuaren xehetasunak aurki ditzakezu, bere egoera eta arazo posibleak barne, freskatu bitartean edo freskatu ondoren. Ulertu zein prozesu sartzen diren aberastea freskatzeko prozesuan eta zenbat denbora behar izan den prozesuak exekutatzeko. Aberaste-egoera Experian, Leadspace, HERE Technologies, SFTP Import, eta Azure Maps-ek onartzen dute.

1. Joan **Datuak** > **Aberastua**.
1. urtean **Nire aberastasunak** fitxan, hautatu aberastearen egoera alboko panel bat irekitzeko.
1. **Garapenaren xehetasunen** panelean, zabaldu **Aberasteak** sekzioa.
1. Ikusi nahi duzun aberastearen egoeran, hautatu **ikusi xehetasunak**.
1. **Zereginaren xehetasunak** panelean, hautatu **erakutsi xehetasunak** aberastea eta bere egoera eguneratzeko eragiketan dauden prozesuak ikusteko.

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberaste-exekualdi baten ondoren, berrikusi aberastearen emaitzak.

1. Joan **Datuak** > **Aberastua**.
1. urtean **Nire aberastasunak** fitxan, hautatu informazioa nahi duzun aberastasuna.

Aberaste guztiek oinarrizko informazioa erakusten dute, hala nola profil aberastuen kopurua eta denboran zehar aberastutako profil kopurua. The **Bezeroen aurrebista aberastua** fitxak sortutako aberaste-entitatearen lagin bat erakusten du. Ikuspegi zehatza ikusteko, hautatu **Gehiago ikusi** eta hautatu **Datuak** fitxa.

:::image type="content" source="media/enrichments-results.png" alt-text="Aberasteen emaitzen orria.":::

Eskuragarri badago, **Alorka aberastutako bezero kopurua** aberasturiko eremu bakoitzaren estaldura sakontzen du.

Aberaste batzuek aberastasun motari dagokion informazioa ere erakusten dute. Informazio gehiago lortzeko, ikusi erlazionatutako dokumentazioa.

[!INCLUDE [footer-include](includes/footer-banner.md)]
