---
title: Entitateak eta datu multzoak
description: Ikusi datuak Entitateen orrian.
ms.date: 04/16/2020
ms.reviewer: mukeshpo
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: e71c69a6207147d8cd65363d51a5fa6bbf896151
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269361"
---
# <a name="entities-in-audience-insights"></a><span data-ttu-id="810ac-103">Hartzaileen xehetasunetako entitateak</span><span class="sxs-lookup"><span data-stu-id="810ac-103">Entities in audience insights</span></span>

<span data-ttu-id="810ac-104">Ondoren [zure datu-iturriak konfiguratuz](data-sources.md), joan **erakundeak** iradokitako datuen kalitatea ebaluatzeko orria.</span><span class="sxs-lookup"><span data-stu-id="810ac-104">After [configuring your data sources](data-sources.md), go to the **Entities** page to evaluate the quality of the ingested data.</span></span> <span data-ttu-id="810ac-105">Entitateak datu multzo gisa hartzen dira.</span><span class="sxs-lookup"><span data-stu-id="810ac-105">Entities are considered datasets.</span></span> <span data-ttu-id="810ac-106">Dynamics 365 Customer Insights-eko hainbat gaitasun entitate horien inguruan eraikitzen dira.</span><span class="sxs-lookup"><span data-stu-id="810ac-106">Multiple capabilities of Dynamics 365 Customer Insights are built around these entities.</span></span> <span data-ttu-id="810ac-107">Hurbiletik berrikusteak gaitasun horien irteera balioztatzen lagun dezake.</span><span class="sxs-lookup"><span data-stu-id="810ac-107">Reviewing them closely can help you validate the output of those capabilities.</span></span>

<span data-ttu-id="810ac-108">**Erakundeak** orrialdeak entitateen zerrenda eta hainbat zutabe biltzen ditu:</span><span class="sxs-lookup"><span data-stu-id="810ac-108">The **Entities** page lists entities and includes several columns:</span></span>

- <span data-ttu-id="810ac-109">**izena**: Zure datu erakundearen izena.</span><span class="sxs-lookup"><span data-stu-id="810ac-109">**Name**: The name of your data entity.</span></span> <span data-ttu-id="810ac-110">Entitate izenaren ondoan abisu sinbolo bat ikusiz gero, entitate horretako datuak ez dira behar bezala kargatu esan nahi du.</span><span class="sxs-lookup"><span data-stu-id="810ac-110">If you see a warning symbol next to an entity name, it means that the data for that entity didn't load successfully.</span></span>
- <span data-ttu-id="810ac-111">**Iturria**: Entitateak irentsitako datu-iturri mota</span><span class="sxs-lookup"><span data-stu-id="810ac-111">**Source**: The type of data source that ingested the entity</span></span>
- <span data-ttu-id="810ac-112">**Hurrengoak sortua**: Entitatea sortu zuen pertsonaren izena</span><span class="sxs-lookup"><span data-stu-id="810ac-112">**Created by**: Name of the person who created the entity</span></span>
- <span data-ttu-id="810ac-113">**Sortu**: Entitatea sortzearen eguna eta ordua</span><span class="sxs-lookup"><span data-stu-id="810ac-113">**Created**: Date and time of the entity creation</span></span>
- <span data-ttu-id="810ac-114">**Hurrengoak eguneratu**: Entitatea eguneratu zuen pertsonaren izena</span><span class="sxs-lookup"><span data-stu-id="810ac-114">**Updated by**: Name of the person who updated the entity</span></span>
- <span data-ttu-id="810ac-115">**Azken eguneraketa**: Erakundearen azken eguneraketaren data eta ordua</span><span class="sxs-lookup"><span data-stu-id="810ac-115">**Last updated**: Date and time of the last update of the entity</span></span>
- <span data-ttu-id="810ac-116">**Azken freskagarria**: Azken datuen berritze data eta ordua</span><span class="sxs-lookup"><span data-stu-id="810ac-116">**Last refresh**: Date and time of the last data refresh</span></span>

## <a name="exploring-a-specific-entitys-data"></a><span data-ttu-id="810ac-117">Entitate jakin baten datuak arakatzea</span><span class="sxs-lookup"><span data-stu-id="810ac-117">Exploring a specific entity's data</span></span>

<span data-ttu-id="810ac-118">Hautatu entitate bat entitate horren barne dauden eremu eta erregistro ezberdinak arakatzeko.</span><span class="sxs-lookup"><span data-stu-id="810ac-118">Select an entity to explore the different fields and records included within that entity.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="810ac-119">![Hautatu entitatea](media/data-manager-entities-data.png "Hautatu entitatea")</span><span class="sxs-lookup"><span data-stu-id="810ac-119">![Select an entity](media/data-manager-entities-data.png "Select an entity")</span></span>

- <span data-ttu-id="810ac-120">The **Datuak** fitxa lehenespenez hautatzen da eta entitatearen erregistro indibidualen inguruko xehetasunak agertzen ditu.</span><span class="sxs-lookup"><span data-stu-id="810ac-120">The **Data** tab is selected by default and shows a table listing details about individual records of the entity.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="810ac-121">![Eremuen taula](media/data-manager-entities-fields.PNG "Eremuen taula")</span><span class="sxs-lookup"><span data-stu-id="810ac-121">![Fields table](media/data-manager-entities-fields.PNG "Fields table")</span></span>

- <span data-ttu-id="810ac-122">The **eremuak** fitxak taula bat erakusten du hautatutako entitatearen xehetasunak berrikusteko, hala nola, eremu izenak, datu motak eta motak.</span><span class="sxs-lookup"><span data-stu-id="810ac-122">The **Fields** tab shows a table to review details for the selected entity, such as field names, data types, and types.</span></span> <span data-ttu-id="810ac-123">**Mota** zutabeak Datuen eredu arruntari lotutako sistemak erakusten ditu, sistemak edo identifikatutako autoak [eskuz mapatuta](map-entities.md) erabiltzaileek.</span><span class="sxs-lookup"><span data-stu-id="810ac-123">The **Type** column shows Common Data Model associated types, which are either auto-identified by the system or [manually mapped](map-entities.md) by users.</span></span> <span data-ttu-id="810ac-124">Ezaugarri semantiko hauek desberdinak izan daitezke, adibidez, eremua *Emaila* azpian datu mota bat dago *Testua* baina bere (semantikoa) datu arruntaren eredua motakoa izan liteke *Emaila* edo *Posta elektroniko helbidea*.</span><span class="sxs-lookup"><span data-stu-id="810ac-124">These are semantic types that can differ from the attributes' data types—for example, the field *Email* below has a data type *Text* but its (semantic) Common Data Model type might be *Email* or *EmailAddress*.</span></span>

> [!NOTE]
> <span data-ttu-id="810ac-125">Bi taulek zure entitatearen datuen lagin bat baino ez dute erakusten.</span><span class="sxs-lookup"><span data-stu-id="810ac-125">Both tables show only a sample of your entity's data.</span></span> <span data-ttu-id="810ac-126">Datu multzo osoa ikusteko, joan **Datu iturriak** orrialdea, entitate bat aukeratu, hautatu **Editatu** eta, ondoren, ikusi entitate honen datuak Power Query editorearekin deskribatutako moduan [Datu iturriak](data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="810ac-126">To view the full data set, go to the **Data sources** page, select an entity, select **Edit**, and then view this entity's data with the Power Query editor as explained in [Data sources](data-sources.md).</span></span>

<span data-ttu-id="810ac-127">Erakundean irensten diren datuei buruz gehiago jakiteko, **Laburpena** zutabeak datuen zenbait ezaugarri garrantzitsu eskaintzen ditu, hala nola, nuluak, falta diren balioak, balio bakarrak, zenbatekoak eta banaketak, datuei dagokienez.</span><span class="sxs-lookup"><span data-stu-id="810ac-127">To learn more about the data ingested in the entity, the **Summary** column provides you with some important characteristics of the data, such as nulls, missing values, unique values, counts, and distributions, as applicable to your data.</span></span>

<span data-ttu-id="810ac-128">Hautatu diagramaren ikonoa datuen laburpena ikusteko.</span><span class="sxs-lookup"><span data-stu-id="810ac-128">Select the chart icon to see the summary of the data.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="810ac-129">![Laburpenaren sinboloa](media/data-manager-entities-summary.png "Datuen laburpen-taula")</span><span class="sxs-lookup"><span data-stu-id="810ac-129">![Summary symbol](media/data-manager-entities-summary.png "Data summary table")</span></span>

### <a name="next-step"></a><span data-ttu-id="810ac-130">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="810ac-130">Next step</span></span>

<span data-ttu-id="810ac-131">Ikusi [bateratzeko](data-unification.md) gaia ikasteko *mapa*, *bat-etortzea*, eta *konbinatu* iradokitako datuak.</span><span class="sxs-lookup"><span data-stu-id="810ac-131">See the [Unify](data-unification.md) topic to learn how to *map*, *match*, and *merge* the ingested data.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]