---
title: Power Query-n oinarritutako datu-iturburuen freskatze inkrementala
description: Freskatu datu berri eta eguneratuak datu iturri handietarako Power Query oinarritzat hartuta.
ms.date: 09/28/2020
ms.reviewer: adkuppa
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: b7e834f5f2fd1328563139675d7f850008348734
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404987"
---
# <a name="incremental-refresh-for-data-sources-based-on-power-query"></a><span data-ttu-id="6f563-103">Power Query-n oinarritutako datu iturrientzako freskapen gehikorra</span><span class="sxs-lookup"><span data-stu-id="6f563-103">Incremental refresh for data sources based on Power Query</span></span>

<span data-ttu-id="6f563-104">Datu iturrien freskapen gehigarriak abantaila hauek eskaintzen ditu:</span><span class="sxs-lookup"><span data-stu-id="6f563-104">Incremental refresh for data sources provides the following advantages:</span></span>

- <span data-ttu-id="6f563-105">**Arinago freskatu** - Aldatutako datuak soilik freskatzen dira.</span><span class="sxs-lookup"><span data-stu-id="6f563-105">**Faster refreshes** - Only data that has changed gets refreshed.</span></span> <span data-ttu-id="6f563-106">Adibidez, datu historiko baten azken bost egunak soilik berritu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="6f563-106">For example, you might refresh only the past five days of a historical dataset.</span></span>
- <span data-ttu-id="6f563-107">**Fidagarritasun handiagoa** - Freskatze txikiagoekin, ez duzu iturri iturri hegazkorretako sistemekin konexioak mantendu beharrik denbora luzez, konexio arazoen arriskua murriztuz.</span><span class="sxs-lookup"><span data-stu-id="6f563-107">**Increased reliability** - With smaller refreshes, you don't need to maintain connections to volatile source systems for as long, reducing the risk of connection issues.</span></span>
- <span data-ttu-id="6f563-108">**Baliabideen kontsumoa murriztea** - Zure datuen azpimultzo bat soilik egiteak baliabide informatikoen erabilera eraginkorragoa ekarriko du eta ingurumen aztarna gutxitzen du.</span><span class="sxs-lookup"><span data-stu-id="6f563-108">**Reduced resource consumption** - Refreshing only a subset of your total data leads to more efficient use of computing resources and decreases the environmental footprint.</span></span>

## <a name="configure-incremental-refresh"></a><span data-ttu-id="6f563-109">Konfiguratu freskatze inkrementala</span><span class="sxs-lookup"><span data-stu-id="6f563-109">Configure incremental refresh</span></span>

<span data-ttu-id="6f563-110">Hartzaileen xehetasunek sartze inkrementala onartzen duten Power Query bidez inportatutako datu-iturburuen freskatze inkrementala onartzen dute.</span><span class="sxs-lookup"><span data-stu-id="6f563-110">Audience insights allows incremental refresh for data sources imported through Power Query that support incremental ingestion.</span></span> <span data-ttu-id="6f563-111">Adibidez, Azure SQL datu baseak data eta orduaren eremuekin, datuen erregistroak eguneratu zirenean adierazten dutenak.</span><span class="sxs-lookup"><span data-stu-id="6f563-111">For example, Azure SQL databases with date and time fields, which indicate when data records were last updated.</span></span>

1. <span data-ttu-id="6f563-112">[Sortu datu-iturburu berria Power Query oinarrituta](connect-power-query.md).</span><span class="sxs-lookup"><span data-stu-id="6f563-112">[Create a new data source based on Power Query](connect-power-query.md).</span></span>

1. <span data-ttu-id="6f563-113">Eman datu-iturburuaren izena.</span><span class="sxs-lookup"><span data-stu-id="6f563-113">Provide a name for the data source.</span></span>

1. <span data-ttu-id="6f563-114">Hautatu freskatze gehigarri bat onartzen duen datu-iturburu bat, hala nola Azure SQL datu basea.</span><span class="sxs-lookup"><span data-stu-id="6f563-114">Select a data source that supports incremental refresh, such as Azure SQL database.</span></span>

1. <span data-ttu-id="6f563-115">Aukeratu irensteko entitateak edo taulak.</span><span class="sxs-lookup"><span data-stu-id="6f563-115">Select the entities or tables to ingest.</span></span>

1. <span data-ttu-id="6f563-116">Osatu eraldaketaren urratsak eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="6f563-116">Complete the transformation steps and select **Next**.</span></span>

1. <span data-ttu-id="6f563-117">**Konfiguratu gehigarri gehigarria** elkarrizketa-koadroan, hautatu **Konfiguratu** **Goranzko freskatze ezarpenak** irekitzeko.</span><span class="sxs-lookup"><span data-stu-id="6f563-117">In the **Set up incremental refresh** dialog box, select **Set up** to open the **Incremental refresh settings**.</span></span> <span data-ttu-id="6f563-118">**Jauzi egin** hautatzen baduzu, datu-iturburuak datu multzo osoa freskatuko du.</span><span class="sxs-lookup"><span data-stu-id="6f563-118">If you select **Skip**, the data source will refresh the entire data set.</span></span>
   > [!TIP]
   > <span data-ttu-id="6f563-119">Geroago freskatze gehigarria ere aplika dezakezu lehendik dagoen datu-iturburu editatuz.</span><span class="sxs-lookup"><span data-stu-id="6f563-119">You can also apply incremental refresh later by editing an existing data source.</span></span>

1. <span data-ttu-id="6f563-120">**Goranzko freskatze ezarpenak** atalean, datu-iturburu sortzerakoan hautatu dituzun entitate guztientzako goranzko freskatzea konfiguratuko duzu.</span><span class="sxs-lookup"><span data-stu-id="6f563-120">On **Incremental refresh settings**, you'll configure the incremental refresh for all entities that you selected when creating the data source.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="6f563-121">![Konfiguratu datu-iturburuko entitateak goranzko freskatzerako](media/incremental-refresh-settings.png "Konfiguratu datu-iturburuko entitateak goranzko freskatzerako")</span><span class="sxs-lookup"><span data-stu-id="6f563-121">![Configure entities in a data source for incremental refresh](media/incremental-refresh-settings.png "Configure entities in a data source for incremental refresh")</span></span>

1. <span data-ttu-id="6f563-122">Hautatu entitate bat eta eman xehetasun hauek:</span><span class="sxs-lookup"><span data-stu-id="6f563-122">Select an entity, and provide the following details:</span></span>

   - <span data-ttu-id="6f563-123">**Definitu gako nagusia**: Entitate edo taularako gako nagusia aukeratu.</span><span class="sxs-lookup"><span data-stu-id="6f563-123">**Define the primary key**: Select a primary key for the entity or table.</span></span>
   - <span data-ttu-id="6f563-124">**Definitu "azken eguneratutako" eremua**: Eremu honek data edo ordua motako atributuak baino ez ditu bistaratuko.</span><span class="sxs-lookup"><span data-stu-id="6f563-124">**Define the "last updated" field**: This field will only display attributes of type date or time.</span></span> <span data-ttu-id="6f563-125">Hautatu erregistroen azken eguneraketa adierazten duen atributu bat.</span><span class="sxs-lookup"><span data-stu-id="6f563-125">Select an attribute that indicates when the records were last updated.</span></span> <span data-ttu-id="6f563-126">Freskatze denbora gehikorraren barruan sartzen diren erregistroak identifikatzeko erabiliko da.</span><span class="sxs-lookup"><span data-stu-id="6f563-126">It will be used to identify the records that fall within the incremental refresh time frame.</span></span>
   - <span data-ttu-id="6f563-127">**Eguneratzeak egiaztatzeko maiztasuna** : Zehaztu zenbat denbora luzatu nahi den goranzko freskatzearen denbora tartea.</span><span class="sxs-lookup"><span data-stu-id="6f563-127">**Check for updates every**: Specify how long you want the incremental refresh time frame to be.</span></span>

1. <span data-ttu-id="6f563-128">Aukeratu **Gorde** datu-iturburuaren sorrera osatzeko.</span><span class="sxs-lookup"><span data-stu-id="6f563-128">Select **Save** to complete the creation of the data source.</span></span> <span data-ttu-id="6f563-129">Hasierako datuen freskatzea freskatze osoa izango da.</span><span class="sxs-lookup"><span data-stu-id="6f563-129">The initial data refresh will be a full refresh.</span></span> <span data-ttu-id="6f563-130">Ondoren, datuen goranzko freskatzea aurreko urratsean konfiguratutako moduan gertatzen da.</span><span class="sxs-lookup"><span data-stu-id="6f563-130">Afterwards, the incremental data refresh happens as configured in the previous step.</span></span>
