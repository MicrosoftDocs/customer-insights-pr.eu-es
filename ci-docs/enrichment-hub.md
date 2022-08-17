---
title: Datuak aberasteko (aurrebista) ikuspegi orokorra
description: Erabili Microsoft-en eta hirugarrenen zerbitzuen gaitasunak zure bezeroen datuak aberasteko.
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
ms.openlocfilehash: 0c2a900190b4ab6e93098d05a2fd66bcd2b847fd
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9245864"
---
# <a name="data-enrichment-preview-overview"></a>Datuak aberasteko (aurrebista) ikuspegi orokorra

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak bezeroaren datuak aberasteko. Hirugarrenen aberastasunak erabiliz konfiguratzen dira [konexioak](connections.md), administratzaileak kredentzialekin konfiguratzen duena eta datuak transferitzeko baimena ematen duena. Konexioak erabil daitezke administratzaile eta langileen aldetik hobekuntzak konfiguratzeko.  

## <a name="multiple-enrichments-of-the-same-type"></a>Mota bereko hainbat aberastasun

Aberastu nahi den entitatea aberasteko konfigurazioan zehazten da eta horrek zure profilen azpimultzo bat soilik aberastea ahalbidetzen du. Adibidez, aberastu datuak segmentu zehatz baterako soilik. Mota bereko hainbat aberastasun konfigura ditzakezu eta konexio bera berrerabili. Zenbait aberastasunek sor ditzaketen mota bereko aberastasunen kopuruak izango dituzte mugak. Mugak eta egungo erabilera ikus daitezke fitxa bakoitzean **Ezagutu** fitxan **Aberastea** orrialdea.

## <a name="enrich-data-sources-before-unification"></a>Aberastu datu-iturriak bateratu aurretik

Zure bezeroen datuak aberastu ditzakezu datuak bateratu aurretik, datuen bat-etortzeen kalitatea areagotzen laguntzeko. Informazio gehiagorako, ikus [datu-iturburu aberastea](data-sources-enrichment.md).

## <a name="create-an-enrichment"></a>Sortu aberaste bat

Kolaboratzailea edo Administratzailea izan behar duzu [baimenak](permissions.md) aberasgarriak sortzeko edo editatzeko.

Joan **Datuak** > **Aberastua**. The **Ezagutu** fitxak onartzen diren aberaste-aukera guztiak erakusten ditu.

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Aberasteko gunearen orria.":::

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

- [AbiliTec Identitatea](enrichment-liveramp.md) LiveRamp AbiliTec-ek emandakoa
- [Markak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- Experian-ek eskainitako [datu demografikoak](enrichment-experian.md)
- [Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita
- [Interesak](enrichment-microsoft.md) hornituta Microsoft-en arabera
- [Kokapen datuak](enrichment-azure-maps.md) emandako Microsoft Azure Mapak
- [Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak
- [SFTP datu pertsonalizatuak](enrichment-SFTP-custom-import.md) Fitxategiak transferitzeko protokolo seguruaren bidez (SFTP)

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

- [Kontuaren partaidetza-datuak](enrichment-office.md) Microsoft-ek emandakoa
- [Enpresaren datuak](enrichment-dnb.md) Dun & Bradstreet-ek emandakoa
- [Enpresaren datuak](enrichment-leadspace.md) , Leadspace-k emanak
- [Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita
- [Enpresaren datu hobetuak](enrichment-enhanced-company-data.md) Microsoft-ek emandakoa
- [Kokapen datuak](enrichment-azure-maps.md) emandako Microsoft Azure Mapak
- [Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak
- [SFTP datu pertsonalizatuak](enrichment-SFTP-custom-import.md) Fitxategiak transferitzeko protokolo seguruaren bidez (SFTP)

---

## <a name="manage-existing-enrichments"></a>Lehendik dauden aberastasunak kudeatu

Joan **Datuak** > **Aberastua**. Gainean **Nire aberastasunak** fitxan, ikusi konfiguratutako aberasketak, haien egoera, aberastutako bezero kopurua eta datuak freskatu diren azken aldia. Aberasteen zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun aberastasuna aurkitzeko.

Hautatu aberastea erabilgarri dauden ekintzak ikusteko.

:::image type="content" source="media/enrichment-hub-options-run.png" alt-text="Aberasteen zerrendan aberastasunak kudeatzeko aukerak.":::

- **ikusi** aberastasun xehetasunak bezeroen profil aberastuen kopuruarekin.
- **Editatu** aberastasunaren konfigurazioa.
- [**Korrika egin**](#run-or-refresh-enrichments) bezeroen profilak azken datuekin eguneratzeko aberastea. Exekutatu hainbat aberasgarri aldi berean zerrendan hautatuz.
- **Aktibatu** edo **Desaktibatu** aberastasun bat. Aberaste inaktiboak ez dira freskatuko a bitartean [programatutako freskadura](schedule-refresh.md).
- **Ezabatu** aberastea.

Sortu ere egin dezakezu [segmentuak](segments.md) edo [neurriak](measures.md) aberasteetatik.

## <a name="run-or-refresh-enrichments"></a>Exekutatu edo freskatu aberasgarriak

Exekutatu ondoren, aberasketak programazio automatiko batean freskatu daitezke edo eskuz, eskaeraren arabera.

1. Aberasgarri bat edo gehiago eskuz freskatzeko, hautatu eta aukeratu **Korrika egin**. To [programatu freskatze automatikoa](schedule-refresh.md), joan **Admin** > **Sistema** > **Ordutegia**. Prozesatzeko denbora zure bezeroen datuen tamainaren araberakoa da.

1. Aukeran, [aberaste prozesuaren aurrerapena ikusi](#see-the-progress-of-the-enrichment-process).

1. Aberaste-prozesua amaitu ondoren, joan hona **Nire aberastasunak** aberastu berri diren bezero-profilen datuak, azken eguneratzearen ordua eta aberastutako profil kopurua berrikusteko.

1. Hautatu aberastasuna ikusteko [aberaste emaitzak](#view-enrichment-results).

### <a name="see-the-progress-of-the-enrichment-process"></a>Ikusi aberaste-prozesuaren garapena

Aberaste-prozesuaren xehetasunak aurki ditzakezu, bere egoera eta arazo posibleak barne, freskatu bitartean edo freskatu ondoren. Ulertu zein prozesu sartzen diren aberastea freskatzeko prozesuan eta zenbat denbora behar izan den prozesuak exekutatzeko. Aberaste-egoera Experian, Leadspace, HERE Technologies, SFTP Import, eta Azure Maps-ek onartzen dute.

1. Joan **Datuak** > **Aberastua**.
1. urtean **Nire aberastasunak** fitxan, hautatu aberastearen egoera alboko panel bat irekitzeko.
1. **Garapenaren xehetasunen** panelean, zabaldu **Aberasteak** sekzioa.
1. Ikusi nahi duzun aberastearen egoeran, hautatu **ikusi xehetasunak**.
1. **Zereginaren xehetasunak** panelean, hautatu **erakutsi xehetasunak** aberastea eta bere egoera eguneratzeko eragiketan dauden prozesuak ikusteko.

[!INCLUDE [progress-details-pane](includes/progress-details-pane.md)]

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

Aberaste-exekualdi baten ondoren, berrikusi aberastearen emaitzak.

1. Joan **Datuak** > **Aberastua**.
1. urtean **Nire aberastasunak** fitxan, hautatu ikusi nahi duzun aberastasuna.

Aberaste guztiek oinarrizko informazioa erakusten dute, hala nola profil aberastu kopurua eta denboran zehar profil aberastu kopurua. The **Bezeroen aurrebista aberastua** fitxak sortutako aberaste-entitatearen lagin bat erakusten du. Ikuspegi zehatza ikusteko, hautatu **Gehiago ikusi** eta hautatu **Datuak** fitxa.

:::image type="content" source="media/enrichments-results.png" alt-text="Aberasteen emaitzen orria.":::

Eskuragarri badago, **Alorka aberastutako bezero kopurua** eremu aberastu bakoitzaren estaldura sakontzea eskaintzen du.

Aberaste batzuek aberastasun motari dagokion informazioa ere erakusten dute. Informazio gehiago lortzeko, ikusi erlazionatutako dokumentazioa.

[!INCLUDE [footer-include](includes/footer-banner.md)]
