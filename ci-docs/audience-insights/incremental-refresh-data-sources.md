---
title: Power Query-n oinarritutako datu-iturburuen freskatze inkrementala
description: Freskatu datu berri eta eguneratuak datu iturri handietarako Power Query oinarritzat hartuta.
ms.date: 12/06/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.openlocfilehash: f614d701aeb06720a60b14549a7fe666f8fe0617
ms.sourcegitcommit: 11b343f6622665251ab84ae39ebcd91fa1c928ca
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/08/2021
ms.locfileid: "7900240"
---
# <a name="incremental-refresh-for-data-sources-based-on-power-query"></a>Power Query-n oinarritutako datu iturrientzako freskapen gehikorra

Artikulu honek Power Query-en oinarritutako datu-iturburuetarako freskatze inkrementala nola konfiguratu aztertzen du.

Datu iturrien freskapen gehigarriak abantaila hauek eskaintzen ditu:

- **Arinago freskatu** - Aldatutako datuak soilik freskatzen dira. Adibidez, datu historiko baten azken bost egunak soilik berritu ditzakezu.
- **Fidagarritasun handiagoa** - Freskatze txikiagoekin, ez duzu iturri iturri hegazkorretako sistemekin konexioak mantendu beharrik denbora luzez, konexio arazoen arriskua murriztuz.
- **Baliabideen kontsumoa murriztea** - Zure datuen azpimultzo bat soilik egiteak baliabide informatikoen erabilera eraginkorragoa ekarriko du eta ingurumen aztarna gutxitzen du.

## <a name="configure-incremental-refresh"></a>Konfiguratu freskatze inkrementala

Hartzaileen xehetasunek sartze inkrementala onartzen duten Power Query bidez inportatutako datu-iturburuen freskatze inkrementala onartzen dute. Adibidez, Azure SQL datu baseak data eta orduaren eremuekin, datuen erregistroak eguneratu zirenean adierazten dutenak.

1. [Sortu datu-iturburu berria Power Query oinarrituta](connect-power-query.md).

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
