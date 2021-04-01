---
title: Power Apps konektorea
description: Konektatu Power Apps eta Power Automate-rekin.
ms.date: 01/19/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: Nils-2m
ms.author: nikeller
manager: shellyha
ms.openlocfilehash: 3fa91553fd50a22ab62b5a2b1e3f13b9483776a8
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5598140"
---
# <a name="microsoft-power-apps-connector-preview"></a><span data-ttu-id="2dd04-103">Microsoft Power Apps konektorea (Aurrebista)</span><span class="sxs-lookup"><span data-stu-id="2dd04-103">Microsoft Power Apps connector (preview)</span></span>

<span data-ttu-id="2dd04-104">Ekarri bezeroen profil bateratuak aplikazio pertsonalizatuekin Power Apps.</span><span class="sxs-lookup"><span data-stu-id="2dd04-104">Bring unified customer profiles into your personalized apps with Power Apps.</span></span>

## <a name="connect-power-apps-and-dynamics-365-customer-insights"></a><span data-ttu-id="2dd04-105">Konektatu Power Apps eta Dynamics 365 Customer Insights</span><span class="sxs-lookup"><span data-stu-id="2dd04-105">Connect Power Apps and Dynamics 365 Customer Insights</span></span>

<span data-ttu-id="2dd04-106">Customer Insights askoren artean dago [erabilgarri dauden datuetarako iturriak Power Apps](/powerapps/maker/canvas-apps/working-with-data-sources).</span><span class="sxs-lookup"><span data-stu-id="2dd04-106">Customer Insights is one of the many [available sources for data in Power Apps](/powerapps/maker/canvas-apps/working-with-data-sources).</span></span>

<span data-ttu-id="2dd04-107">Erreferentzi Power Apps dokumentazioa nola ikasi ikasteko [gehitu datuen konexioa aplikazio bati](/powerapps/maker/canvas-apps/add-data-connection).</span><span class="sxs-lookup"><span data-stu-id="2dd04-107">Refer to the Power Apps documentation to learn how to [add a data connection to an app](/powerapps/maker/canvas-apps/add-data-connection).</span></span> <span data-ttu-id="2dd04-108">Berrikustea ere gomendatzen dugu [nola Power Apps Delegazioa erabiltzen du Canvas aplikazioetan datu-multzo handiak kudeatzeko](/powerapps/maker/canvas-apps/delegation-overview).</span><span class="sxs-lookup"><span data-stu-id="2dd04-108">We recommend you also review [how Power Apps uses delegation to handle large datasets in Canvas apps](/powerapps/maker/canvas-apps/delegation-overview).</span></span>

## <a name="available-entities"></a><span data-ttu-id="2dd04-109">Entitate erabilgarriak</span><span class="sxs-lookup"><span data-stu-id="2dd04-109">Available entities</span></span>

<span data-ttu-id="2dd04-110">Customer Insights konexio gisa gehitu ondoren, ondorengo entitateak aukeratu ditzakezu Power Apps:</span><span class="sxs-lookup"><span data-stu-id="2dd04-110">After adding Customer Insights as a data connection, you can choose the following entities in Power Apps:</span></span>

- <span data-ttu-id="2dd04-111">Bezeroa: hurrengoko datuak erabiltzeko [bezeroaren profil bateratua](customer-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="2dd04-111">Customer: to use data from the [unified customer profile](customer-profiles.md).</span></span>
- <span data-ttu-id="2dd04-112">UnifiedActivity: aplikazioan [jardueren denbora-lerroa](activities.md) bistaratzeko.</span><span class="sxs-lookup"><span data-stu-id="2dd04-112">UnifiedActivity: to display the [activity timeline](activities.md) on the app.</span></span>

## <a name="limitations"></a><span data-ttu-id="2dd04-113">Murriztapenak</span><span class="sxs-lookup"><span data-stu-id="2dd04-113">Limitations</span></span>

### <a name="retrievable-entities"></a><span data-ttu-id="2dd04-114">Eskura daitezkeen entitateak</span><span class="sxs-lookup"><span data-stu-id="2dd04-114">Retrievable entities</span></span>

<span data-ttu-id="2dd04-115">Fitxategia soilik berreskura dezakezu **Bezeroa**, **UnifiedActivity**, eta **Segmentuak** entitateak Power Apps konektore.</span><span class="sxs-lookup"><span data-stu-id="2dd04-115">You can only retrieve the **Customer**, **UnifiedActivity**, and **Segments** entities through the Power Apps connector.</span></span> <span data-ttu-id="2dd04-116">Beste entitate batzuk erakusten dira azpiko konektoreak abiarazle bidez onartzen dituelako Power Automate.</span><span class="sxs-lookup"><span data-stu-id="2dd04-116">Other entities are shown because the underlying connector supports them through triggers in Power Automate.</span></span>  

### <a name="delegation"></a><span data-ttu-id="2dd04-117">Ordezkaritza</span><span class="sxs-lookup"><span data-stu-id="2dd04-117">Delegation</span></span>

<span data-ttu-id="2dd04-118">Ordezkaritza Bezeroen entitatearen eta UnifiedActivity entitatearen funtzionatzen du.</span><span class="sxs-lookup"><span data-stu-id="2dd04-118">Delegation works for the Customer entity and UnifiedActivity entity.</span></span> 

- <span data-ttu-id="2dd04-119">**Bezeroa** entitatearen ordezkaritza: entitate honen ordezkaritza erabiltzeko, eremuak indexatu behar dira hemen: [Bilaketa- eta iragazki-indizea](search-filter-index.md).</span><span class="sxs-lookup"><span data-stu-id="2dd04-119">Delegation for **Customer** entity: To use delegation for this entity, the fields need to be indexed in [Search & filter index](search-filter-index.md).</span></span>  

- <span data-ttu-id="2dd04-120">Ordezkaritza **UnifiedActivity**: Erakunde honen ordezkaritzak eremuetarako bakarrik funtzionatzen du **ActivityId** eta **Bezeroaren IDa**.</span><span class="sxs-lookup"><span data-stu-id="2dd04-120">Delegation for **UnifiedActivity**: Delegation for this entity only works for the fields **ActivityId** and **CustomerId**.</span></span>  

- <span data-ttu-id="2dd04-121">Ordezkaritzari buruzko informazio gehiago lortzeko, ikusi [Power Apps funtzio eta eragiketa delegagarriak](/connectors/commondataservice/#power-apps-delegable-functions-and-operations-for-the-cds-for-apps).</span><span class="sxs-lookup"><span data-stu-id="2dd04-121">For more information about delegation, see [Power Apps delegable functions and operations](/connectors/commondataservice/#power-apps-delegable-functions-and-operations-for-the-cds-for-apps).</span></span> 

## <a name="example-gallery-control"></a><span data-ttu-id="2dd04-122">Adibidez galeria kontrola</span><span class="sxs-lookup"><span data-stu-id="2dd04-122">Example gallery control</span></span>

<span data-ttu-id="2dd04-123">Adibidez, bezero profilak gehitzen dizkiozu [galeriaren kontrolari](/powerapps/maker/canvas-apps/add-gallery).</span><span class="sxs-lookup"><span data-stu-id="2dd04-123">For example, you add customer profiles to a [gallery control](/powerapps/maker/canvas-apps/add-gallery).</span></span>

1. <span data-ttu-id="2dd04-124">Gehitu a **Galeria** kontrolatzen ari zaren aplikazio batera.</span><span class="sxs-lookup"><span data-stu-id="2dd04-124">Add a **Gallery** control to an app you're building.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="2dd04-125">![Gehitu galeria-elementu bat](media/connector-powerapps9.png "Gehitu galeria-elementu bat")</span><span class="sxs-lookup"><span data-stu-id="2dd04-125">![Add a gallery element](media/connector-powerapps9.png "Add a gallery element")</span></span>

1. <span data-ttu-id="2dd04-126">Aukeratu **Bezeroaren** datu-iturburu elementuen gisa.</span><span class="sxs-lookup"><span data-stu-id="2dd04-126">Select **Customer** as the data source for items.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="2dd04-127">![Hautatu datu-iturburua](media/choose-datasource-powerapps.png "Hautatu datu-iturburua")</span><span class="sxs-lookup"><span data-stu-id="2dd04-127">![Select a data source](media/choose-datasource-powerapps.png "Select a data source")</span></span>

1. <span data-ttu-id="2dd04-128">Eskubian dagoen datuen panela alda dezakezu Bezeroaren entitateak galerian erakusteko zein eremutan hautatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="2dd04-128">You can change the data panel on the right to select which field for the Customer entity to show on the gallery.</span></span>

1. <span data-ttu-id="2dd04-129">Aukeratutako bezeroaren eremuan edozein galeria erakutsi nahi baduzu, bete etiketa baten Testuaren propietatea: **{Name_of_the_gallery}.Selected.{property_name}**</span><span class="sxs-lookup"><span data-stu-id="2dd04-129">If you want to show any field from the selected customer on the gallery, fill in the Text property of a label:  **{Name_of_the_gallery}.Selected.{property_name}**</span></span>

    <span data-ttu-id="2dd04-130">Adibidea: Gallery1.Selected.address1_city</span><span class="sxs-lookup"><span data-stu-id="2dd04-130">Example: Gallery1.Selected.address1_city</span></span>

1. <span data-ttu-id="2dd04-131">Bezeroarentzako denbora-lerro bateratua bistaratzeko, gehitu Galeriako elementua eta gehitu elementuak jabetza: **Iragazkia('UnifiedActivity', CustomerId = {Customer_Id})**</span><span class="sxs-lookup"><span data-stu-id="2dd04-131">To display the unified timeline for a customer, add a Gallery element, and add the Items property: **Filter('UnifiedActivity', CustomerId = {Customer_Id})**</span></span>

    <span data-ttu-id="2dd04-132">Adibidez: Iragazkia('UnifiedActivity', CustomerId = Gallery1.Selected.CustomerId)</span><span class="sxs-lookup"><span data-stu-id="2dd04-132">Example: Filter('UnifiedActivity', CustomerId = Gallery1.Selected.CustomerId)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]