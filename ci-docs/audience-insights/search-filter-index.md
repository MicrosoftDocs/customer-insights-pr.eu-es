---
title: Bilatu eta iragazi bezeroen profilak
description: Aurki itzazu zehaztutako atributuetarako bezeroen profil bateratuei eta iragazkiari buruzko informazioa.
ms.date: 01/19/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
manager: shellyha
ms.openlocfilehash: b6cc0ad1a47a6c00e3bf220271f42870fc53621b
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597128"
---
# <a name="customer-profiles-search--filter-index"></a><span data-ttu-id="ba16f-103">Bezeroen profilak: Bilatu eta iragazi indizea</span><span class="sxs-lookup"><span data-stu-id="ba16f-103">Customer profiles: Search & filter index</span></span>

<span data-ttu-id="ba16f-104">Zure bezeroen datuak bateratzearen emaitza Bezeroaren Profilaren entitatea da zure bezero base guztiari ikuspegi bateratua ematen diona.</span><span class="sxs-lookup"><span data-stu-id="ba16f-104">The result of unifying your customer data is a Customer Profile entity that provides a unified view into your total customer base.</span></span> <span data-ttu-id="ba16f-105">Azkar egiteko [bezero edo talde jakin bati buruzko informazioa bilatu](customer-profiles.md), konfigura dezakezu **Bilatu** eta **Iragazi** gaitasunak **Bezeroak** orria.</span><span class="sxs-lookup"><span data-stu-id="ba16f-105">To quickly [find information on a specific customer or group of customers](customer-profiles.md), you can configure the **Search** and **Filter** capabilities on the **Customers** page.</span></span> <span data-ttu-id="ba16f-106">Irakurri gehiago administratzaileek gailuan atributuak edita ditzaketen jakiteko **Bilatu eta iragazi indizea** orrialdea, erabiltzaileak bilatzeko eta iragazteko erabilgarri daudenak.</span><span class="sxs-lookup"><span data-stu-id="ba16f-106">Read on to learn how admins can edit the attributes on the **Search & filter index** page, which are available to users for searching and filtering.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="ba16f-107">![Bilaketa-iragazkia](media/search-filter.png "Bilaketa-iragazkia")</span><span class="sxs-lookup"><span data-stu-id="ba16f-107">![Search filter](media/search-filter.png "Search filter")</span></span>

## <a name="add-fields-and-specify-attributes"></a><span data-ttu-id="ba16f-108">Gehitu eremuak eta zehaztu atributuak</span><span class="sxs-lookup"><span data-stu-id="ba16f-108">Add fields and specify attributes</span></span>

<span data-ttu-id="ba16f-109">Bilaketa atributuak administratzaile gisa definitzen dituzun lehen aldia bada, indexatu beharreko eremuak lehenik definitu behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="ba16f-109">If it's the first time you define searchable attributes as an administrator, you need to define indexed fields first.</span></span> <span data-ttu-id="ba16f-110">Erabiltzaileek bezeroak bilatu eta iragazi ditzaketen atributu guztiak aukeratzea gomendatzen dizugu **Bezeroak** orria.</span><span class="sxs-lookup"><span data-stu-id="ba16f-110">We suggest you choose all the attributes by which users can search and filter customers on the **Customers** page.</span></span> <span data-ttu-id="ba16f-111">Datuak bateratzeko prozesuan sortutako Bezero Profilaren entitatean dauden atributuak soilik zehaztu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="ba16f-111">You can only specify attributes that exist in the Customer Profile entity that you created during the data unification process.</span></span>

1. <span data-ttu-id="ba16f-112">Ireki **Bezeroak** orria eta hautatu **Bilatu eta iragazi indizea**.</span><span class="sxs-lookup"><span data-stu-id="ba16f-112">Open the **Customers** page and select **Search & filter index**.</span></span>

2. <span data-ttu-id="ba16f-113">Hautatu **+ Gehitu** zehazteko indexatutako eremuak.</span><span class="sxs-lookup"><span data-stu-id="ba16f-113">Select **+ Add** to specify the indexed fields.</span></span>

3. <span data-ttu-id="ba16f-114">Hautatu indexatutako eremu gisa gehitu nahi dituzun zerrendan atributuak.</span><span class="sxs-lookup"><span data-stu-id="ba16f-114">Select the attributes in the list you want to add as indexed fields.</span></span> <span data-ttu-id="ba16f-115">Atributu gehiago gehitu ditzakezu **Gehitu** hautatuta.</span><span class="sxs-lookup"><span data-stu-id="ba16f-115">You can always add more attributes by selecting **Add**.</span></span> <span data-ttu-id="ba16f-116">Aukeratutako atributuak ere kendu ditzakezu **Kendu** sinboloa.</span><span class="sxs-lookup"><span data-stu-id="ba16f-116">You can also remove any selected attributes by selecting the **Remove** symbol.</span></span>

## <a name="explore-the-indexed-customer-fields-table"></a><span data-ttu-id="ba16f-117">Arakatu indexatutako bezeroen eremuen taula</span><span class="sxs-lookup"><span data-stu-id="ba16f-117">Explore the Indexed customer fields table</span></span>

<span data-ttu-id="ba16f-118">Taulan aurkezten da hurrengo informazioa.</span><span class="sxs-lookup"><span data-stu-id="ba16f-118">The following information is presented in the table.</span></span>

- <span data-ttu-id="ba16f-119">**izena**: Atributuaren izena Bezero Profilaren entitatean agertzen den bezala adierazten du.</span><span class="sxs-lookup"><span data-stu-id="ba16f-119">**Name**: Represents the attribute's name as it appears in the Customer Profile entity.</span></span>
- <span data-ttu-id="ba16f-120">**Datu mota**: Datu mota katea, zenbakia edo data den zehazten du.</span><span class="sxs-lookup"><span data-stu-id="ba16f-120">**Data type**: Specifies whether the data type is a string, a number, or a date.</span></span>
- <span data-ttu-id="ba16f-121">**Bilaketa barne**: Ezartzen du atributu hau bezeroan bilatzeko **Bezeroak** orrialdea **Bilatu** eremu.</span><span class="sxs-lookup"><span data-stu-id="ba16f-121">**Included in search**: Specifies whether this attribute can be used for searching customers on the **Customers** page using the **Search** field.</span></span>
- <span data-ttu-id="ba16f-122">**Gehitu iragazkia**: Kontrola atributu hau iragaztean nola erabil daitekeen definitzeko **Bezeroak** orria.</span><span class="sxs-lookup"><span data-stu-id="ba16f-122">**Add Filter**: Control to define how this attribute can be used for filtering on the **Customers** page.</span></span>

## <a name="editing-filtering-options-for-a-given-attribute"></a><span data-ttu-id="ba16f-123">Emandako atributu baten iragazketa aukerak editatzea</span><span class="sxs-lookup"><span data-stu-id="ba16f-123">Editing filtering options for a given attribute</span></span>

<span data-ttu-id="ba16f-124">The **Iragazi** menuan **Bezeroak** orrialdeak hainbat atributu-maila izan ditzake (adibidez, bezeroak iragazteko adin-talde desberdinak).</span><span class="sxs-lookup"><span data-stu-id="ba16f-124">The **Filter** menu on the **Customers** page can include a varying number of attribute levels (for example, different age groups to filter customers by).</span></span>

1. <span data-ttu-id="ba16f-125">Aukeratu **Gehitu iragazkia** atributu jakin batentzako gaiari buruz **Bilatu eta iragazi indizea** orria.</span><span class="sxs-lookup"><span data-stu-id="ba16f-125">Select **Add Filter** for a given attribute on the **Search & filter index** page.</span></span> <span data-ttu-id="ba16f-126">Emaitza kopurua eta zer antolatuko diren zehaztu dezakezu.</span><span class="sxs-lookup"><span data-stu-id="ba16f-126">You can define the number of results and the order in which they'll be organized.</span></span> <span data-ttu-id="ba16f-127">Atributuaren datu motaren arabera, panela hau agertzen da.</span><span class="sxs-lookup"><span data-stu-id="ba16f-127">Depending on the attribute's data type, one of the following panes appears.</span></span>

- <span data-ttu-id="ba16f-128">Kate motako atributuak: zehaztu nahi duzun emaitzen kopurua **Kate-iragazkiaren aukerak** taulan eta emaitzok antolatzeko baldintzak.</span><span class="sxs-lookup"><span data-stu-id="ba16f-128">String-type attributes: Specify the number of desired results on the **String filter options** pane and the order policy by which they'll be organized.</span></span>

- <span data-ttu-id="ba16f-129">Zenbaki motako atributuak: zehaztu **Zenbaki-iragazkiaren aukerak** taulan gehitzeko interbaloak eta hauek antolatzeko baldintzak.</span><span class="sxs-lookup"><span data-stu-id="ba16f-129">Numerical-type attributes: Specify the intervals included on the **Number filter options** pane and the order policy by which they'll be organized.</span></span>

- <span data-ttu-id="ba16f-130">Datu motako atributuak: zehaztu **Datu-iragazkiaren aukerak** taulan gehitzeko interbaloak eta hauek antolatzeko baldintzak.</span><span class="sxs-lookup"><span data-stu-id="ba16f-130">Date-type attributes:  Specify the intervals included on the **Date filter options** pane and the order policy by which they'll be organized.</span></span>

2. <span data-ttu-id="ba16f-131">Aldaketak aplikatzeko, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="ba16f-131">Select **Save** to apply your changes.</span></span>

3. <span data-ttu-id="ba16f-132">Aukeratu **Exekutatu** zure ezarpenak aplikatzeko prest dagoenean.</span><span class="sxs-lookup"><span data-stu-id="ba16f-132">Select **Run** once you're ready to apply your settings.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ba16f-133">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="ba16f-133">Next steps</span></span>

<span data-ttu-id="ba16f-134">Joan **Bezeroak** orrira bezeroen profilak bilatzeko edo aurkitutako eremuak erabiltzea bezeroen profil guztien azpimultzoa ikusteko.</span><span class="sxs-lookup"><span data-stu-id="ba16f-134">Go to the **Customers** page to search for customer profiles or use the indexed fields to see a subset of all customer profiles.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]