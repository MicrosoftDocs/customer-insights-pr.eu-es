---
title: datu-iturburu aberastea
description: Aberastu datu-iturriak datuak bateratze-prozesua igaro aurretik.
ms.date: 03/02/2022
ms.subservice: audience-insights
ms.topic: how-to
author: NimrodMagen
ms.author: nimagen
ms.reviewer: v-wendysmith
manager: shellyha
ms.openlocfilehash: 56f6a8ad20224922f9968f0ad3b6a0e0a400214b
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642006"
---
# <a name="enrichment-for-data-sources-preview"></a>Datu-iturburuetarako aberastea (aurrebista)

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak zure bezeroen datuak aberasteko datuak bateratu aurretik. datu-iturburu aberasteek datuen osotasun eta kalitate handiagoak lortzen laguntzen dute, eta horrek emaitza hobeak lortzen lagunduko dizu datuak bateratu ondoren. Esaterako, helbideetarako formatu normalizatu eta estandarizatu bat erabiltzeak bat emaitzen kalitatea areagotzen du. Onartutako aberasteen zerrendarako, ikus [datu-iturburu aberasteko aukerak onartzen ditu](#supported-data-source-enrichments).

## <a name="enrich-a-data-source"></a>Aberastu datu-iturburu

Kolaboratzaile edo Administratzaile baimenak izan behar dituzu aberasketak sortzeko edo editatzeko. Informazio gehiago lortzeko, [Baimenak](permissions.md).  

1. Joan **Datuak** > **Bateratu**. Hautatu aberastu nahi duzun entitatea eta hautatu atributu bat entitatearen gako nagusi gisa. Informazio gehiagorako, ikus [Hautatu gako nagusia](map-entities.md#select-primary-key-and-semantic-type-for-attributes).

1. Joan **Datuak** > **Datu-iturburuak**.
 
1. Hautatu aberastu nahi duzun datu-iturburu ondoan dagoen elipsi bertikala eta hautatu **Aberastu**.

   :::image type="content" source="media/data_sources_enrich_discover.png" alt-text="Datu iturriak aberasteko orria.":::

   The **Ezagutu** fitxa bistaratzen du [datu-iturburu aberasteko aukerak onartzen ditu](#supported-data-source-enrichments).

1. Hautatu **Aberastu nire datuak** datu-iturburu aberaste bat konfiguratzeko. Irteerako entitatearen izena automatikoki betetzen da.

## <a name="supported-data-source-enrichments"></a>datu-iturburu aberasgarriak onartzen dira

Une honetan datu-iturrietarako eskuragarri daude honako aberasgarri hauek. Berrikusi aberasteko urrats zehatzak nola konfiguratu ikasteko.

- [Helbide hobetuak](enrichment-enhanced-addresses.md)
- [Enpresaren datu hobetuak](enrichment-enhanced-company-data.md)

## <a name="manage-existing-data-source-enrichments"></a>Kudeatu lehendik dauden datu-iturburu aberasgarriak

Joan **Nire aberastasunak** fitxa konfiguratutako aberastasun guztiak ikusteko.

Aukeratu aberastea eskuragarri dauden aukerak ikusteko. Zerrenda bateko elipsia (...) ere hauta dezakezu aukerak ikusteko. Zenbait aberaste konfiguratu badituzu, bilaketa-koadroa erabil dezakezu azkar aurkitzeko.

datu-iturburu aberaste bat ikusi, editatu, exekutatu edo ezabatu dezakezu. Informazio gehiagorako, ikus [Dauden aberastasunak kudeatu](enrichment-hub.md).
