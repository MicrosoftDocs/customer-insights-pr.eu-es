---
title: Konektatu Common Data Service-n kudeatutako biltegiko entitateetara
description: Inportatu datuak Common Data Service kudeatutako datu-biltegia.
ms.date: 09/29/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.reviewer: adkuppa
ms.openlocfilehash: 18b6cd3fdaf5b738877a73b520b91dbc6ded40de
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267775"
---
# <a name="connect-to-data-in-a-common-data-service-managed-data-lake"></a><span data-ttu-id="2ce7f-103">Konektatu datuekin Common Data Service kudeatutako data lake-ra</span><span class="sxs-lookup"><span data-stu-id="2ce7f-103">Connect to data in a Common Data Service managed data lake</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="2ce7f-104">Artikulu honek egungo Dynamics 365 bezeroak beren entitate analitikoekin azkar nola konektatu daitezkeen buruzko informazioa eskaintzen du Common Data Service kudeatutako aintzira.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-104">This article provides information on how existing Dynamics 365 customers can quickly connect to their analytical entities in the Common Data Service managed lake.</span></span> <span data-ttu-id="2ce7f-105">Administratzailea izan behar duzu Common Data Service erakundeak aurrera egiteko eta kudeatutako aintziran dauden entitateen zerrenda ikusteko.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-105">You must be an admin on the Common Data Service organization to proceed and see the list of entities available in the managed lake.</span></span>

## <a name="important-considerations"></a><span data-ttu-id="2ce7f-106">Gogoeta garrantzitsuak</span><span class="sxs-lookup"><span data-stu-id="2ce7f-106">Important considerations</span></span>

<span data-ttu-id="2ce7f-107">Lineako zerbitzuetan gordetako datuak, esaterako Azure Data Lake Storage datuak prozesatu edo biltegiratutako beste toki batean gorde daitezke Dynamics 365 Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-107">Data stored in online services, such as Azure Data Lake Storage, may be stored in a different location than where data is processed or stored in Dynamics 365 Customer Insights.</span></span><span data-ttu-id="2ce7f-108">Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz onartu egiten duzu Dynamics 365 Customer Insights-rekin transferitu eta biltegiratu daitezkeen datuak. [Ezagutu gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="2ce7f-108"> By importing or connecting to data stored in online services, you agree that data can be transferred to and stored with Dynamics 365 Customer Insights. [Learn more at the Microsoft Trust Center.](https://www.microsoft.com/trust-center)</span></span>

## <a name="connect-to-a-common-data-service-managed-lake"></a><span data-ttu-id="2ce7f-109">Konektatu a Common Data Service lake kudeatu</span><span class="sxs-lookup"><span data-stu-id="2ce7f-109">Connect to a Common Data Service managed lake</span></span>

1. <span data-ttu-id="2ce7f-110">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-110">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="2ce7f-111">Hautatu **Gehitu datu-iturburua**.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-111">Select **Add data source**.</span></span>

3. <span data-ttu-id="2ce7f-112">Aukeratu **Konektatu Common Data Service** eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-112">Select **Connect to Common Data Service** and select **Next**.</span></span>

4. <span data-ttu-id="2ce7f-113">Idatzi **Izena** datu-iturbururako eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-113">Enter a **Name** for the data source and select **Next**.</span></span> <span data-ttu-id="2ce7f-114">Jarri izena jarraibideei:</span><span class="sxs-lookup"><span data-stu-id="2ce7f-114">Name guidelines:</span></span> 
   - <span data-ttu-id="2ce7f-115">Hasi letra batekin.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-115">Start with a letter.</span></span>
   - <span data-ttu-id="2ce7f-116">Erabili letrak eta zenbakiak soilik.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-116">Use letters and numbers only.</span></span> <span data-ttu-id="2ce7f-117">Ezin da idatzi karaktere berezirik edo zuriunerik.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-117">Special characters and spaces are not allowed.</span></span>
   - <span data-ttu-id="2ce7f-118">Erabili 3 eta 64 karaktere artean.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-118">Use between 3 and 64 characters.</span></span>

5. <span data-ttu-id="2ce7f-119">Eman **Zerbitzariaren helbidea** zuretzako Common Data Service antolatzea eta hautatu **saioa hasi**.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-119">Provide the **Server address** for your Common Data Service organization, and select **Sign in**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="2ce7f-120">![Sartzeko elkarrizketa-koadroa Common Data Service zerbitzariaren helbidea](media/enter-CDS-org-details.png)</span><span class="sxs-lookup"><span data-stu-id="2ce7f-120">![Dialog box to enter Common Data Service server address](media/enter-CDS-org-details.png)</span></span>

6. <span data-ttu-id="2ce7f-121">Aukeratu eskuragarri dauden zerrendatik sartu nahi dituzun entitateak.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-121">Select the entities you want to ingest from the available list.</span></span>    

   > [!NOTE]
   > <span data-ttu-id="2ce7f-122">Entitate batzuk dagoeneko hautatuak badira, beste Dynamics 365 aplikazio batzuek erabil ditzakete (Dynamics 365 Sales Insights edo Customer Service Insights adibidez).</span><span class="sxs-lookup"><span data-stu-id="2ce7f-122">If some entities are already selected, they might be used by other Dynamics 365 applications (such as Dynamics 365 Sales Insights or Customer Service Insights).</span></span> <span data-ttu-id="2ce7f-123">Ezin da aldatu aukeraketa.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-123">You can't change the selection.</span></span> <span data-ttu-id="2ce7f-124">Entitate hauek eskuragarri egongo dira datu-iturburu sortutakoan.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-124">These entities will be available once the data source is created.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="2ce7f-125">![Elkarrizketa-koadroa, eremuko entitateen zerrenda erakusten duena Common Data Service org](media/select-analytical-entities.png)</span><span class="sxs-lookup"><span data-stu-id="2ce7f-125">![Dialog box showing a list of entities in the Common Data Service org](media/select-analytical-entities.png)</span></span>

7. <span data-ttu-id="2ce7f-126">Gorde zure aukera, hautatutako entitateak sinkronizatzen hasteko Common Data Service lake kudeatu.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-126">Save your selection to start syncing the selected entities to the Common Data Service managed lake.</span></span> <span data-ttu-id="2ce7f-127">Konexio berria gehitu duzu **Datu iturriak** orria.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-127">You'll find the newly added connection on the **Data sources** page.</span></span> <span data-ttu-id="2ce7f-128">Freskatzeko ilaran jarriko da eta entitateak 0 gisa zenbatuko dira entitate guztiak sinkronizatu arte.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-128">It will be queued for refresh and show the entities count as 0 until all the entities are synced.</span></span>

<span data-ttu-id="2ce7f-129">Ingurune bateko datu-iturburu batek bakarrik erabil dezake aldi berean Common Data Service-k kudeatutako biltegia.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-129">Only one data source of an environment can simultaneously use the same Common Data Service managed lake.</span></span>

## <a name="edit-a-common-data-service-managed-lake-data-source"></a><span data-ttu-id="2ce7f-130">Editatu a Common Data Service lakua kudeatu datu-iturburu</span><span class="sxs-lookup"><span data-stu-id="2ce7f-130">Edit a Common Data Service managed lake data source</span></span>

<span data-ttu-id="2ce7f-131">datu-iturburu sortu ondoren entitateen hautapena soilik editatzen duzu.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-131">You only edit the entity selection after creating the data source.</span></span> <span data-ttu-id="2ce7f-132">Adibidez, entitate osagarriak gehitu badira Common Data Service eta horiek ere inportatu nahi dituzu.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-132">For example, if additional entities were added to Common Data Service and you want to import them too.</span></span>    
<span data-ttu-id="2ce7f-133">Common Data Service desberdinera konektatzeko, [sortu datu-iturri berria](#connect-to-a-common-data-service-managed-lake).</span><span class="sxs-lookup"><span data-stu-id="2ce7f-133">To connect to a different Common Data Service, [create a new data source](#connect-to-a-common-data-service-managed-lake).</span></span>

1. <span data-ttu-id="2ce7f-134">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-134">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="2ce7f-135">Eguneratu nahi duzun datu-iturburu ondoan, hautatu elipsia.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-135">Next to the data source you'd like to update, select the ellipsis.</span></span>

3. <span data-ttu-id="2ce7f-136">Hautatu **Editatu** aukera zerrendan.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-136">Select the **Edit** option from the list.</span></span>

4. <span data-ttu-id="2ce7f-137">Entitate osagarriak eskuragarri dauden entitateen zerrendatik hautatu eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="2ce7f-137">Select additional entities from the available list of entities and select **Save**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]