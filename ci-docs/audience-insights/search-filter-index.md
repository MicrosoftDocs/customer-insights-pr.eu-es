---
title: Bilatu eta iragazi bezeroen profilak
description: Aurki itzazu zehaztutako atributuetarako bezeroen profil bateratuei eta iragazkiari buruzko informazioa.
ms.date: 04/16/2020
ms.reviewer: nimagen
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 1842ad333c23bb155abc89167556163ae79cdd34
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404999"
---
# <a name="customer-profiles-search--filter-index"></a><span data-ttu-id="dade1-103">Bezeroen profilak: Bilatu eta iragazi indizea</span><span class="sxs-lookup"><span data-stu-id="dade1-103">Customer profiles: Search & filter index</span></span>

<span data-ttu-id="dade1-104">Zure bezeroen datuak bateratzearen emaitza Bezeroaren Profilaren entitatea da zure bezero base guztiari ikuspegi bateratua ematen diona.</span><span class="sxs-lookup"><span data-stu-id="dade1-104">The result of unifying your customer data is a Customer Profile entity that provides a unified view into your total customer base.</span></span> <span data-ttu-id="dade1-105">Azkar egiteko [bezero edo talde jakin bati buruzko informazioa bilatu](customer-profiles.md), konfigura dezakezu **Bilatu** eta **Iragazi** gaitasunak **Bezeroak** orria.</span><span class="sxs-lookup"><span data-stu-id="dade1-105">To quickly [find information on a specific customer or group of customers](customer-profiles.md), you can configure the **Search** and **Filter** capabilities on the **Customers** page.</span></span> <span data-ttu-id="dade1-106">Irakurri gehiago administratzaileek gailuan atributuak edita ditzaketen jakiteko **Bilatu eta iragazi indizea** orrialdea, erabiltzaileak bilatzeko eta iragazteko erabilgarri daudenak.</span><span class="sxs-lookup"><span data-stu-id="dade1-106">Read on to learn how admins can edit the attributes on the **Search & filter index** page, which are available to users for searching and filtering.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="dade1-107">![Bilaketa-iragazkia](media/search-filter.png "Bilaketa-iragazkia")</span><span class="sxs-lookup"><span data-stu-id="dade1-107">![Search filter](media/search-filter.png "Search filter")</span></span>

## <a name="add-fields-and-specify-attributes"></a><span data-ttu-id="dade1-108">Gehitu eremuak eta zehaztu atributuak</span><span class="sxs-lookup"><span data-stu-id="dade1-108">Add fields and specify attributes</span></span>

<span data-ttu-id="dade1-109">Bilaketa atributuak administratzaile gisa definitzen dituzun lehen aldia bada, indexatu beharreko eremuak lehenik definitu behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="dade1-109">If it's the first time you define searchable attributes as an administrator, you need to define indexed fields first.</span></span> <span data-ttu-id="dade1-110">Erabiltzaileek bezeroak bilatu eta iragazi ditzaketen atributu guztiak aukeratzea gomendatzen dizugu **Bezeroak** orria.</span><span class="sxs-lookup"><span data-stu-id="dade1-110">We suggest you choose all the attributes by which users can search and filter customers on the **Customers** page.</span></span> <span data-ttu-id="dade1-111">Datuak bateratzeko prozesuan sortutako Bezero Profilaren entitatean dauden atributuak soilik zehaztu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="dade1-111">You can only specify attributes that exist in the Customer Profile entity that you created during the data unification process.</span></span>

1. <span data-ttu-id="dade1-112">Ireki **Bezeroak** orria eta hautatu **Bilatu eta iragazi indizea**.</span><span class="sxs-lookup"><span data-stu-id="dade1-112">Open the **Customers** page and select **Search & filter index**.</span></span>

> [!NOTE]
> <span data-ttu-id="dade1-113">Bilaketa-indize konfigurazio lehenetsi bat sortzen dugu Bezeroaren entitatean eskuragarri dauden atributuetan, honako mapa semantiko hauetatik, maparen orrian definituta.</span><span class="sxs-lookup"><span data-stu-id="dade1-113">We create a default search index configuration on the available attributes in the Customer entity from the following semantic types as defined on the Map page.</span></span>
> - <span data-ttu-id="dade1-114">Pertsonaren izena, abizena, bigarren izena, izen osoa</span><span class="sxs-lookup"><span data-stu-id="dade1-114">Person First name, Last name, Middle name, Full Name</span></span>
> - <span data-ttu-id="dade1-115">Erakundearen izena</span><span class="sxs-lookup"><span data-stu-id="dade1-115">Organization Name</span></span>
> - <span data-ttu-id="dade1-116">Helbide elektronikoa</span><span class="sxs-lookup"><span data-stu-id="dade1-116">Email address</span></span>
> - <span data-ttu-id="dade1-117">Telefono-zenbakia</span><span class="sxs-lookup"><span data-stu-id="dade1-117">Phone number</span></span>
> - <span data-ttu-id="dade1-118">Kokapenaren informazioa</span><span class="sxs-lookup"><span data-stu-id="dade1-118">Location information</span></span>

2. <span data-ttu-id="dade1-119">Hautatu **+ Gehitu** zehazteko indexatutako eremuak.</span><span class="sxs-lookup"><span data-stu-id="dade1-119">Select **+ Add** to specify the indexed fields.</span></span>

3. <span data-ttu-id="dade1-120">Hautatu indexatutako eremu gisa gehitu nahi dituzun zerrendan atributuak.</span><span class="sxs-lookup"><span data-stu-id="dade1-120">Select the attributes in the list you want to add as indexed fields.</span></span> <span data-ttu-id="dade1-121">Atributu gehiago gehitu ditzakezu **Gehitu** hautatuta.</span><span class="sxs-lookup"><span data-stu-id="dade1-121">You can always add more attributes by selecting **Add**.</span></span> <span data-ttu-id="dade1-122">Aukeratutako atributuak ere kendu ditzakezu **Kendu** sinboloa.</span><span class="sxs-lookup"><span data-stu-id="dade1-122">You can also remove any selected attributes by selecting the **Remove** symbol.</span></span>

## <a name="explore-the-indexed-customer-fields-table"></a><span data-ttu-id="dade1-123">Arakatu indexatutako bezeroen eremuen taula</span><span class="sxs-lookup"><span data-stu-id="dade1-123">Explore the Indexed customer fields table</span></span>

<span data-ttu-id="dade1-124">Taulan aurkezten da hurrengo informazioa.</span><span class="sxs-lookup"><span data-stu-id="dade1-124">The following information is presented in the table.</span></span>

- <span data-ttu-id="dade1-125">**izena**: Atributuaren izena Bezero Profilaren entitatean agertzen den bezala adierazten du.</span><span class="sxs-lookup"><span data-stu-id="dade1-125">**Name**: Represents the attribute's name as it appears in the Customer Profile entity.</span></span>
- <span data-ttu-id="dade1-126">**Datu mota**: Datu mota katea, zenbakia edo data den zehazten du.</span><span class="sxs-lookup"><span data-stu-id="dade1-126">**Data type**: Specifies whether the data type is a string, a number, or a date.</span></span>
- <span data-ttu-id="dade1-127">**Bilaketa barne**: Ezartzen du atributu hau bezeroan bilatzeko **Bezeroak** orrialdea **Bilatu** eremu.</span><span class="sxs-lookup"><span data-stu-id="dade1-127">**Included in search**: Specifies whether this attribute can be used for searching customers on the **Customers** page using the **Search** field.</span></span>
- <span data-ttu-id="dade1-128">**Gehitu iragazkia**: Kontrola atributu hau iragaztean nola erabil daitekeen definitzeko **Bezeroak** orria.</span><span class="sxs-lookup"><span data-stu-id="dade1-128">**Add Filter**: Control to define how this attribute can be used for filtering on the **Customers** page.</span></span>

## <a name="editing-filtering-options-for-a-given-attribute"></a><span data-ttu-id="dade1-129">Emandako atributu baten iragazketa aukerak editatzea</span><span class="sxs-lookup"><span data-stu-id="dade1-129">Editing filtering options for a given attribute</span></span>

<span data-ttu-id="dade1-130">The **Iragazi** menuan **Bezeroak** orrialdeak hainbat atributu-maila izan ditzake (adibidez, bezeroak iragazteko adin-talde desberdinak).</span><span class="sxs-lookup"><span data-stu-id="dade1-130">The **Filter** menu on the **Customers** page can include a varying number of attribute levels (for example, different age groups to filter customers by).</span></span>

1. <span data-ttu-id="dade1-131">Aukeratu **Gehitu iragazkia** atributu jakin batentzako gaiari buruz **Bilatu eta iragazi indizea** orria.</span><span class="sxs-lookup"><span data-stu-id="dade1-131">Select **Add Filter** for a given attribute on the **Search & filter index** page.</span></span> <span data-ttu-id="dade1-132">Emaitza kopurua eta zer antolatuko diren zehaztu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="dade1-132">You can define the number of results and the order in which they'll be organized.</span></span> <span data-ttu-id="dade1-133">Atributuaren datu motaren arabera, panela hau agertzen da.</span><span class="sxs-lookup"><span data-stu-id="dade1-133">Depending on the attribute's data type, one of the following panes appears.</span></span>

- <span data-ttu-id="dade1-134">Kate motako atributuak: zehaztu nahi duzun emaitzen kopurua **Kate-iragazkiaren aukerak** taulan eta emaitzok antolatzeko baldintzak.</span><span class="sxs-lookup"><span data-stu-id="dade1-134">String-type attributes: Specify the number of desired results on the **String filter options** pane and the order policy by which they'll be organized.</span></span>

- <span data-ttu-id="dade1-135">Zenbaki motako atributuak: zehaztu **Zenbaki-iragazkiaren aukerak** taulan gehitzeko interbaloak eta hauek antolatzeko baldintzak.</span><span class="sxs-lookup"><span data-stu-id="dade1-135">Numerical-type attributes: Specify the intervals included on the **Number filter options** pane and the order policy by which they'll be organized.</span></span>

- <span data-ttu-id="dade1-136">Datu motako atributuak: zehaztu **Datu-iragazkiaren aukerak** taulan gehitzeko interbaloak eta hauek antolatzeko baldintzak.</span><span class="sxs-lookup"><span data-stu-id="dade1-136">Date-type attributes:  Specify the intervals included on the **Date filter options** pane and the order policy by which they'll be organized.</span></span>

2. <span data-ttu-id="dade1-137">Aldaketak aplikatzeko, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="dade1-137">Select **Save** to apply your changes.</span></span>

3. <span data-ttu-id="dade1-138">Aukeratu **Exekutatu** zure ezarpenak aplikatzeko prest dagoenean.</span><span class="sxs-lookup"><span data-stu-id="dade1-138">Select **Run** once you're ready to apply your settings.</span></span>
