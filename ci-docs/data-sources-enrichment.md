---
title: Datu-iturburuetarako aberastea (aurrebista)
description: Aberastu datu-iturriak datuak bateratze-prozesua igaro aurretik.
ms.date: 05/20/2022
ms.subservice: audience-insights
ms.topic: how-to
author: NimrodMagen
ms.author: nimagen
ms.reviewer: v-wendysmith
manager: shellyha
ms.openlocfilehash: 98e9e330e7ef9cf085caa94a506fa788cebdd67b
ms.sourcegitcommit: 5807b7d8c822925b727b099713a74ce2cb7897ba
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/28/2022
ms.locfileid: "9207168"
---
# <a name="enrichment-for-data-sources-preview"></a>Datu-iturburuetarako aberastea (aurrebista)

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak zure bezeroen datuak aberasteko datuak bateratu aurretik. datu-iturburu aberasteek datuen osotasun eta kalitate handiagoa sortzen laguntzen dute, eta horrek emaitza hobeak lortzen lagunduko dizu datuak bateratu ondoren. Esaterako, helbideetarako formatu normalizatu eta estandarizatu bat erabiltzeak bateren emaitzen kalitatea areagotzen du. Onartutako aberasteen zerrendarako, ikus [datu-iturburu aberasteko aukerak onartzen ditu](#supported-data-source-enrichments).

## <a name="enrich-a-data-source"></a>Aberastu datu-iturburu bat

Kolaboratzailea edo Administratzailea izan behar duzu [baimenak](permissions.md) aberasgarriak sortzeko edo editatzeko.  

1. Joan **Datuak** > **Bateratu**. Hautatu aberastu nahi duzun entitatea eta hautatu atributu bat a gisa [lehen gakoa](map-entities.md#select-primary-key-and-semantic-type-for-attributes) entitatearentzat.

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu elipsi bertikala (&vellip;) aberastu eta hautatu nahi duzun datu-iturburu ondoan **Aberastu**.

   :::image type="content" source="media/data_sources_enrich.png" alt-text="Datu-iturburuen orria Aberastea nabarmenduta":::

   The **Ezagutu** fitxa bistaratzen du [datu-iturburu aberasteko aukerak onartzen ditu](#supported-data-source-enrichments).

   :::image type="content" source="media/data_sources_enrich_discover.png" alt-text="Datu-iturriak aberasteko orria.":::

1. Hautatu **Aberastu nire datuak** datu-iturburu aberaste bat konfiguratzeko. Irteerako entitatearen izena automatikoki betetzen da.

## <a name="supported-data-source-enrichments"></a>datu-iturburu aberasgarriak onartzen dira

Une honetan datu-iturrietarako eskuragarri daude honako aberasgarri hauek. Berrikusi aberasteko urrats zehatzak nola konfiguratu ikasteko.

- [Helbide hobetuak](enrichment-enhanced-addresses.md)
- [Enpresaren datu hobetuak](enrichment-enhanced-company-data.md)
- [LiveRamp-en nortasun datuak](enrichment-liveramp.md)

## <a name="manage-existing-data-source-enrichments"></a>Kudeatu lehendik dauden datu-iturburu aberasgarriak

Joan **Datuak** > **Aberastua**. Gainean **Nire aberastasunak** fitxan, ikusi konfiguratutako aberasketak, haien egoera, aberastutako bezero kopurua eta datuak freskatu diren azken aldia. Aberasteen zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun aberastasuna aurkitzeko.

Aukeratu aberastea eskuragarri dauden aukerak ikusteko. Elipse bertikala ere hauta dezakezu (&vellip;) zerrendako elementu batean aukerak ikusteko.

datu-iturburu aberaste bat ikusi, editatu, exekutatu edo ezabatu dezakezu. Informazio gehiagorako, ikus [Dauden aberastasunak kudeatu](enrichment-hub.md#manage-existing-enrichments).
