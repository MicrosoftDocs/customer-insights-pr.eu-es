---
title: Freskatze gehigarria Power Query oinarritutako datu-iturriak
description: Freskatu datu berriak eta eguneratuak datu-iturri handietarako Power Query.
ms.date: 12/06/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
searchScope:
- ci-system-schedule
- customerInsights
ms.openlocfilehash: 62632efda3c0c7e53fcdd8864b053ba93e2918bc
ms.sourcegitcommit: 73cb021760516729e696c9a90731304d92e0e1ef
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/25/2022
ms.locfileid: "8353666"
---
# <a name="incremental-refresh-for-data-sources-based-on-power-query"></a>Horretan oinarritutako datu-iturburuetarako freskatze gehigarria Power Query

Artikulu honek datu-iturburuetarako freskatze inkrementala nola konfiguratu aztertzen du Power Query.

Datu iturrien freskapen gehigarriak abantaila hauek eskaintzen ditu:

- **Arinago freskatu** - Aldatutako datuak soilik freskatzen dira. Adibidez, datu historiko baten azken bost egunak soilik berritu ditzakezu.
- **Fidagarritasun handiagoa** - Freskatze txikiagoekin, ez duzu iturri iturri hegazkorretako sistemekin konexioak mantendu beharrik denbora luzez, konexio arazoen arriskua murriztuz.
- **Baliabideen kontsumoa murriztea** - Zure datuen azpimultzo bat soilik egiteak baliabide informatikoen erabilera eraginkorragoa ekarriko du eta ingurumen aztarna gutxitzen du.

## <a name="configure-incremental-refresh"></a>Konfiguratu freskatze inkrementala

Ikusleei buruzko informazioak inportatutako datu-iturburuen freskatze gehigarria ahalbidetzen du Power Query gehigarrian irenstea onartzen dutenak. Adibidez, Azure SQL datu baseak data eta orduaren eremuekin, datuen erregistroak eguneratu zirenean adierazten dutenak.

1. [Sortu datu-iturburu berri bat Power Query](connect-power-query.md).

1. Eman a **Izena** datu-iturburu-erako.

1. Hautatu freskatze inkrementala onartzen duen datu-iturburu, adibidez [Azure SQL datu-basea](/power-query/connectors/azuresqldatabase).

1. Aukeratu irensteko entitateak edo taulak.

1. Osatu eraldaketaren urratsak eta hautatu **hurrengoa**.

1. **Konfiguratu gehigarri gehigarria** elkarrizketa-koadroan, hautatu **Konfiguratu** **Goranzko freskatze ezarpenak** irekitzeko. **Jauzi egin** hautatzen baduzu, datu-iturburuak datu multzo osoa freskatuko du.
   > [!TIP]
   > Geroago freskatze gehigarria ere aplika dezakezu lehendik dagoen datu-iturburu editatuz.

1. **Goranzko freskatze ezarpenak** atalean, datu-iturburu sortzerakoan hautatu dituzun entitate guztientzako goranzko freskatzea konfiguratuko duzu.

   :::image type="content" source="media/incremental-refresh-settings.png" alt-text="Konfiguratu datu-iturburuko entitateak goranzko freskatzerako.":::

1. Hautatu entitate bat eta eman xehetasun hauek:

   - **Definitu gako nagusia**: Entitate edo taularako gako nagusia aukeratu.
   - **Definitu "azken eguneratutako" eremua**: Eremu honek data edo ordua motako atributuak baino ez ditu bistaratuko. Hautatu erregistroen azken eguneraketa adierazten duen atributu bat. Freskatze denbora gehikorraren barruan sartzen diren erregistroak identifikatzeko erabiliko da.
   - **Eguneratzeak egiaztatzeko maiztasuna** : Zehaztu zenbat denbora luzatu nahi den goranzko freskatzearen denbora tartea.

1. Aukeratu **Gorde** datu-iturburuaren sorrera osatzeko. Hasierako datuen freskatzea freskatze osoa izango da. Ondoren, datuen goranzko freskatzea aurreko urratsean konfiguratutako moduan gertatzen da.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
