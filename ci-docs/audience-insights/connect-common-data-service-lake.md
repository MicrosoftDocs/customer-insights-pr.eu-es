---
title: Konektatu Common Data Service-n kudeatutako biltegiko entitateetara
description: Inportatu datuak Common Data Service kudeatutako datu-biltegia.
ms.date: 09/29/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.reviewer: adkuppa
ms.openlocfilehash: 029857e2bbb5f6357a5c01138ceaad78887b7518
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643383"
---
# <a name="connect-to-data-in-a-common-data-service-managed-data-lake"></a><span data-ttu-id="22507-103">Konektatu datuekin Common Data Service kudeatutako data lake-ra</span><span class="sxs-lookup"><span data-stu-id="22507-103">Connect to data in a Common Data Service managed data lake</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="22507-104">Artikulu honek egungo Dynamics 365 bezeroak beren entitate analitikoekin azkar nola konektatu daitezkeen buruzko informazioa eskaintzen du Common Data Service kudeatutako aintzira.</span><span class="sxs-lookup"><span data-stu-id="22507-104">This article provides information on how existing Dynamics 365 customers can quickly connect to their analytical entities in the Common Data Service managed lake.</span></span> <span data-ttu-id="22507-105">Administratzailea izan behar duzu Common Data Service erakundeak aurrera egiteko eta kudeatutako aintziran dauden entitateen zerrenda ikusteko.</span><span class="sxs-lookup"><span data-stu-id="22507-105">You must be an admin on the Common Data Service organization to proceed and see the list of entities available in the managed lake.</span></span>

## <a name="important-considerations"></a><span data-ttu-id="22507-106">Gogoeta garrantzitsuak</span><span class="sxs-lookup"><span data-stu-id="22507-106">Important considerations</span></span>

<span data-ttu-id="22507-107">Lineako zerbitzuetan gordetako datuak, esaterako Azure Data Lake Storage datuak prozesatu edo biltegiratutako beste toki batean gorde daitezke Dynamics 365 Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="22507-107">Data stored in online services, such as Azure Data Lake Storage, may be stored in a different location than where data is processed or stored in Dynamics 365 Customer Insights.</span></span><span data-ttu-id="22507-108">Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz onartu egiten duzu Dynamics 365 Customer Insights-rekin transferitu eta biltegiratu daitezkeen datuak. [Ezagutu gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="22507-108"> By importing or connecting to data stored in online services, you agree that data can be transferred to and stored with Dynamics 365 Customer Insights. [Learn more at the Microsoft Trust Center.](https://www.microsoft.com/trust-center)</span></span>

## <a name="connect-to-a-common-data-service-managed-lake"></a><span data-ttu-id="22507-109">Konektatu a Common Data Service lake kudeatu</span><span class="sxs-lookup"><span data-stu-id="22507-109">Connect to a Common Data Service managed lake</span></span>

1. <span data-ttu-id="22507-110">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="22507-110">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="22507-111">Hautatu **Gehitu datu-iturburua**.</span><span class="sxs-lookup"><span data-stu-id="22507-111">Select **Add data source**.</span></span>

3. <span data-ttu-id="22507-112">Aukeratu **Konektatu Common Data Service** eta hautatu **hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="22507-112">Select **Connect to Common Data Service** and select **Next**.</span></span>

4. <span data-ttu-id="22507-113">Idatzi **Izena** datu-iturbururako eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="22507-113">Enter a **Name** for the data source and select **Next**.</span></span>

5. <span data-ttu-id="22507-114">Eman **Zerbitzariaren helbidea** zuretzako Common Data Service antolatzea eta hautatu **saioa hasi**.</span><span class="sxs-lookup"><span data-stu-id="22507-114">Provide the **Server address** for your Common Data Service organization, and select **Sign in**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="22507-115">![Sartzeko elkarrizketa-koadroa Common Data Service zerbitzariaren helbidea](media/enter-CDS-org-details.png)</span><span class="sxs-lookup"><span data-stu-id="22507-115">![Dialog box to enter Common Data Service server address](media/enter-CDS-org-details.png)</span></span>

6. <span data-ttu-id="22507-116">Aukeratu eskuragarri dauden zerrendatik sartu nahi dituzun entitateak.</span><span class="sxs-lookup"><span data-stu-id="22507-116">Select the entities you want to ingest from the available list.</span></span>    

   > [!NOTE]
   > <span data-ttu-id="22507-117">Entitate batzuk dagoeneko hautatuak badira, beste Dynamics 365 aplikazio batzuek erabil ditzakete (Dynamics 365 Sales Insights edo Customer Service Insights adibidez).</span><span class="sxs-lookup"><span data-stu-id="22507-117">If some entities are already selected, they might be used by other Dynamics 365 applications (such as Dynamics 365 Sales Insights or Customer Service Insights).</span></span> <span data-ttu-id="22507-118">Ezin da aldatu aukeraketa.</span><span class="sxs-lookup"><span data-stu-id="22507-118">You can't change the selection.</span></span> <span data-ttu-id="22507-119">Entitate hauek eskuragarri egongo dira datu-iturburu sortutakoan.</span><span class="sxs-lookup"><span data-stu-id="22507-119">These entities will be available once the data source is created.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="22507-120">![Elkarrizketa-koadroa, eremuko entitateen zerrenda erakusten duena Common Data Service org](media/select-analytical-entities.png)</span><span class="sxs-lookup"><span data-stu-id="22507-120">![Dialog box showing a list of entities in the Common Data Service org](media/select-analytical-entities.png)</span></span>

7. <span data-ttu-id="22507-121">Gorde zure aukera, hautatutako entitateak sinkronizatzen hasteko Common Data Service lake kudeatu.</span><span class="sxs-lookup"><span data-stu-id="22507-121">Save your selection to start syncing the selected entities to the Common Data Service managed lake.</span></span> <span data-ttu-id="22507-122">Konexio berria gehitu duzu **Datu iturriak** orria.</span><span class="sxs-lookup"><span data-stu-id="22507-122">You'll find the newly added connection on the **Data sources** page.</span></span> <span data-ttu-id="22507-123">Freskatzeko ilaran jarriko da eta entitateak 0 gisa zenbatuko dira entitate guztiak sinkronizatu arte.</span><span class="sxs-lookup"><span data-stu-id="22507-123">It will be queued for refresh and show the entities count as 0 until all the entities are synced.</span></span>

<span data-ttu-id="22507-124">Ingurune bateko datu-iturburu batek bakarrik erabil dezake aldi berean Common Data Service-k kudeatutako biltegia.</span><span class="sxs-lookup"><span data-stu-id="22507-124">Only one data source of an environment can simultaneously use the same Common Data Service managed lake.</span></span>

## <a name="edit-a-common-data-service-managed-lake-data-source"></a><span data-ttu-id="22507-125">Editatu a Common Data Service lakua kudeatu datu-iturburu</span><span class="sxs-lookup"><span data-stu-id="22507-125">Edit a Common Data Service managed lake data source</span></span>

<span data-ttu-id="22507-126">datu-iturburu sortu ondoren entitateen hautapena soilik editatzen duzu.</span><span class="sxs-lookup"><span data-stu-id="22507-126">You only edit the entity selection after creating the data source.</span></span> <span data-ttu-id="22507-127">Adibidez, entitate osagarriak gehitu badira Common Data Service eta horiek ere inportatu nahi dituzu.</span><span class="sxs-lookup"><span data-stu-id="22507-127">For example, if additional entities were added to Common Data Service and you want to import them too.</span></span>    
<span data-ttu-id="22507-128">Common Data Service desberdinera konektatzeko, [sortu datu-iturri berria](#connect-to-a-common-data-service-managed-lake).</span><span class="sxs-lookup"><span data-stu-id="22507-128">To connect to a different Common Data Service, [create a new data source](#connect-to-a-common-data-service-managed-lake).</span></span>

1. <span data-ttu-id="22507-129">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="22507-129">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="22507-130">Eguneratu nahi duzun datu-iturburu ondoan, hautatu elipsia.</span><span class="sxs-lookup"><span data-stu-id="22507-130">Next to the data source you'd like to update, select the ellipsis.</span></span>

3. <span data-ttu-id="22507-131">Hautatu **Editatu** aukera zerrendan.</span><span class="sxs-lookup"><span data-stu-id="22507-131">Select the **Edit** option from the list.</span></span>

4. <span data-ttu-id="22507-132">Entitate osagarriak eskuragarri dauden entitateen zerrendatik hautatu eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="22507-132">Select additional entities from the available list of entities and select **Save**.</span></span>
