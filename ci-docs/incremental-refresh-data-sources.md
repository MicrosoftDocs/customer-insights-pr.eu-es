---
title: Freskatze gehigarria Power Query eta Azure Data Lake datu-iturriak
description: Freskatu datu-iturri handietarako datu berriak eta eguneratuak oinarrituta Power Query edo Azure data Lake datu-iturriak.
ms.date: 05/30/2022
ms.reviewer: v-wendysmith
ms.subservice: audience-insights
ms.topic: how-to
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-system-schedule
- customerInsights
ms.openlocfilehash: bff27bf7fec2bcb741846ae76bb1f616f459136c
ms.sourcegitcommit: 5e26cbb6d2258074471505af2da515818327cf2c
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "9012010"
---
# <a name="incremental-refresh-for-power-query-and-azure-data-lake-data-sources"></a>Freskatze gehigarria Power Query eta Azure Data Lake datu-iturriak

Artikulu honek datu-iturburuetarako freskatze inkrementala nola konfiguratu aztertzen du Power Query edo Azure Data Lake.

Datu iturrien freskapen gehigarriak abantaila hauek eskaintzen ditu:

- **Arinago freskatu** - Aldatutako datuak soilik freskatzen dira. Adibidez, datu historiko baten azken bost egunak soilik berritu ditzakezu.
- **Fidagarritasun handiagoa** - Freskatze txikiagoekin, ez duzu iturri iturri hegazkorretako sistemekin konexioak mantendu beharrik denbora luzez, konexio arazoen arriskua murriztuz.
- **Baliabideen kontsumoa murriztea** - Zure datuen azpimultzo bat soilik egiteak baliabide informatikoen erabilera eraginkorragoa ekarriko du eta ingurumen aztarna gutxitzen du.

## <a name="configure-incremental-refresh-for-data-sources-based-on-power-query"></a>Konfiguratu datu-iturburuetarako freskatze inkrementala oinarrituta Power Query

Customer Insights-ek inportatutako datu-iturburuen freskatze gehigarria ahalbidetzen du Power Query gehigarrian irenstea onartzen dutenak. Adibidez, Azure SQL datu baseak data eta orduaren eremuekin, datuen erregistroak eguneratu zirenean adierazten dutenak.

1. [Sortu datu-iturburu berri bat Power Query](connect-power-query.md).

1. Hautatu freskatze inkrementala onartzen duen datu-iturburu, adibidez [Azure SQL datu-basea](/power-query/connectors/azuresqldatabase).

1. Aukeratu irensteko entitateak edo taulak.

1. Osatu eraldaketaren urratsak eta hautatu **hurrengoa**.

1. **Konfiguratu gehigarri gehigarria** elkarrizketa-koadroan, hautatu **Konfiguratu** **Goranzko freskatze ezarpenak** irekitzeko. **Jauzi egin** hautatzen baduzu, datu-iturburuak datu multzo osoa freskatuko du.
   > [!TIP]
   > Geroago freskatze gehigarria ere aplika dezakezu lehendik dagoen datu-iturburu editatuz.

1. **Goranzko freskatze ezarpenak** atalean, datu-iturburu sortzerakoan hautatu dituzun entitate guztientzako goranzko freskatzea konfiguratuko duzu.

   :::image type="content" source="media/incremental-refresh-settings.png" alt-text="Konfiguratu freskatze inkrementalaren ezarpenak.":::

1. Hautatu entitate bat eta eman xehetasun hauek:

   - **Definitu gako nagusia**: Entitate edo taularako gako nagusia aukeratu.
   - **Definitu "azken eguneratutako" eremua**: Eremu honek data edo ordua motako atributuak baino ez ditu bistaratuko. Hautatu erregistroen azken eguneraketa adierazten duen atributu bat. Freskatze denbora gehikorraren barruan sartzen diren erregistroak identifikatzeko erabiliko da.
   - **Eguneratzeak egiaztatzeko maiztasuna** : Zehaztu zenbat denbora luzatu nahi den goranzko freskatzearen denbora tartea.

1. Aukeratu **Gorde** datu-iturburuaren sorrera osatzeko. Hasierako datuen freskatzea freskatze osoa izango da. Ondoren, datuen goranzko freskatzea aurreko urratsean konfiguratutako moduan gertatzen da.

## <a name="configure-incremental-refresh-for-azure-data-lake-data-sources"></a>Konfiguratu freskatze inkrementala Azure Data Lake datu-iturburuetarako

Customer Insights-ek konektaturiko datu-iturburuen freskatze inkrementala ahalbidetzen du Azure Data Lake Storage. Entitate baterako gehikuntza eta freskatzea erabiltzeko, konfiguratu entitate hori datu-iturburu datu-iturburu edo geroago datu-iturburu editatzean Azure Data Lake gehitzean. Entitatearen datuen karpetak karpeta hauek izan behar ditu:

- **Datu osoa** : Hasierako erregistroak dituzten datu-fitxategiekin karpeta
- **Datu gehigarriak** : Data/orduaren hierarkia-karpetak dituen karpeta **yyyy/mm/dd/hh** eguneraketa gehigarriak dituen formatua. **hh** eguneratzeen UTC ordua adierazten du eta edukia dauka **Upserts** eta **Ezabatzen du** karpetak. **Upserts** lehendik dauden erregistroen edo erregistro berrien eguneraketak dituzten datu-fitxategiak ditu. **Ezabatzen du** kendu beharreko erregistroak dituzten datu-fitxategiak ditu.

1. datu-iturburu bat gehitzean edo editatzen duzunean, joan hona **Atributuak** entitatearentzat panela.

1. Berrikusi atributuak. Ziurtatu sortu edo azken eguneratutako data-atributu bat ezarrita dagoela *dataOrdua* **Datuen formatua** eta a *Egutegia.Data* **Mota semantikoa**. Editatu atributua behar izanez gero eta hautatu **Eginda**.

1. Tik **Hautatu Entitateak** panela, editatu entitatea. The **Irenstea gehigarria** kontrol-laukia hautatuta dago.

   :::image type="content" source="media/ADLS_inc_refresh.png" alt-text="Konfiguratu datu-iturburuko entitateak goranzko freskatzerako.":::

   1. Arakatu .csv edo .parquet fitxategiak dituen erroko karpetara datu osoak, datu gehigarriak igotzeko eta datu gehigarriak ezabatzeko.
   1. Sartu datu osoentzako eta bi fitxategi gehigarrientzako luzapena (\. csv edo\. parketa).
   1. Sakatu **Gorde**.

1. Izan ere **Azken eguneratua**, hautatu data ordu-zigiluaren atributua.

1. bada **Lehen gakoa** hautatuta ez dago, hautatu gako nagusia. Gako nagusia entitatearen atributu bakarra da. Atributu bat baliozko gako nagusia izan dadin, ez lituzke balio bikoiztuak, falta diren balioak edo balio baliorik sartu behar. Katea, osokoa eta GUID datu motako atributuak gako nagusi gisa onartzen dira.

1. Hautatu **Itxi** panela gorde eta ixteko.

1. Jarraitu datu-iturburu gehitzen edo editatzen.

[!INCLUDE [footer-include](includes/footer-banner.md)]
