---
title: Aberastu bezeroen profil bateratuak
description: Erabili gaitasunak zure bezeroaren datuak aberasteko.
ms.date: 03/29/2022
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
ms.openlocfilehash: 510a20306e793a5ba522a6ac0d9c7194f03472d2
ms.sourcegitcommit: ae02ac950810242e2505d7d371b80210dc8a0777
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/29/2022
ms.locfileid: "8491933"
---
# <a name="enrichment-for-customer-profiles-preview"></a>Bezeroen profiletarako aberastea (aurrebista)

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak bezeroaren datuak aberasteko.

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Aberasteko gunearen orria.":::

Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** aberasteko aukerekin lan egiteko.  

Laguntzaileak edo Administratzaileak baimenak izan behar dituzu aberastasunak sortzeko edo editatzeko. Informazio gehiago lortzeko, [Baimenak](permissions.md).

Gainean **Ezagutu** fitxa, onartutako aberasteko aukera guztiak aurkituko dituzu.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- [Markak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- [Interesak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- [Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita 
- Experian-ek eskainitako [datu demografikoak](enrichment-experian.md)
- [Datu pertsonalizatuak](enrichment-SFTP-custom-import.md) fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) bidez 
- [Azure Maps](enrichment-azure-maps.md), Microsoft-ek eskainia
- [Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak 
- [Identitatea](enrichment-liveramp.md) LiveRamp AbiliTec-ek emandakoa

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- [Enpresaren datuak](enrichment-leadspace.md) , Leadspace-k emanak
- [Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita 
- [Enpresaren datu hobetuak](enrichment-enhanced-company-data.md) Microsoft-ek emandakoa
- [Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak 
- [Datu pertsonalizatuak](enrichment-SFTP-custom-import.md) fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) bidez 
- [Azure Maps](enrichment-azure-maps.md), Microsoft-ek eskainia
- [Kontuaren partaidetza-datuak](enrichment-office.md) Microsoft-ek emandakoa

---

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

Hirugarrenen aberastasunak erabiliz konfiguratzen dira [konexioak](connections.md), administratzaileak kredentzialekin konfiguratzen duena eta datuak transferitzeko baimena ematen duena. Konexioak erabil daitezke administratzaile eta langileen aldetik hobekuntzak konfiguratzeko.  

## <a name="multiple-enrichments-of-the-same-type"></a>Mota bereko hainbat aberastasun

Aberastu nahi den entitatea aberasteko konfigurazioan zehazten da eta horrek zure profilen azpimultzo bat soilik aberastea ahalbidetzen du. Adibidez, aberastu datuak segmentu zehatz baterako soilik. Mota bereko hainbat aberastasun konfigura ditzakezu eta konexio bera berrerabili. Zenbait aberastasunek sor ditzaketen mota bereko aberastasunen kopuruak izango dituzte mugak. Mugak eta egungo erabilera webgunean ikus daitezke **Aberastea** orrialdea.

## <a name="enrich-data-sources-before-unification"></a>Aberastu datu-iturriak bateratu aurretik

Zure bezeroen datuak aberastu ditzakezu datuak bateratu aurretik, datuen bat-etortzeen kalitatea areagotzen laguntzeko. Informazio gehiagorako, ikus [datu-iturburu aberastea](data-sources-enrichment.md).

## <a name="see-the-progress-of-the-enrichment-process"></a>Ikusi aberaste-prozesuaren garapena

Aberaste-prozesuaren xehetasunak aurki ditzakezu, bere egoera eta arazo posibleak barne, freskatu bitartean edo freskatu ondoren. Ulertu zein prozesu sartzen diren aberastea freskatzeko prozesuan eta zenbat denbora behar izan den prozesuak exekutatzeko. Aberaste-egoera Experian, Leadspace, HERE Technologies, SFTP Import, eta Azure Maps-ek onartzen dute.

Aberastearen egoera ikusteko

1. Joan **Datuak** > **Aberastua**. 
1. **Aberasteak** fitxan, hautatu aberaste baten egoera alboko panela irekitzeko. 
1. **Garapenaren xehetasunen** panelean, zabaldu **Aberasteak** sekzioa. 
1. Ikusi nahi duzun aberastearen egoeran, hautatu **ikusi xehetasunak**. 
1. **Zereginaren xehetasunak** panelean, hautatu **erakutsi xehetasunak** aberastea eta bere egoera eguneratzeko eragiketan dauden prozesuak ikusteko. 

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberaste-exekutapen baten ondoren, aberastearen emaitzak berrikus ditzakezu.

1. Joan **Datuak** > **Aberastua**. 
1. Hautatu informazioa nahi duzun aberastasuna.

Aberaste guztiek oinarrizko informazioa erakusten dute, hala nola profil aberastuen kopurua, sortutako aberaste-entitatearen aurrebista eta denboran zehar aberastutako profil kopurua. Eskuragarri badago, **Alorka aberastutako bezero kopurua** aberasturiko eremu bakoitzaren estaldura sakontzen du.

:::image type="content" source="media/enrichments-results.png" alt-text="Aberasteen emaitzen orria.":::

Aberaste batzuek aberastasun motari dagokion informazioa ere erakusten dute. Informazio gehiago lortzeko dagokion aberasteari buruzko dokumentazioa kontsultatu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
