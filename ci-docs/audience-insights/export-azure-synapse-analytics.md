---
title: Esportatu Customer Insights datuak Azure Synapse Analytics-era
description: Ikasi konexioa nola konfiguratu Azure Synapse Analytics-en.
ms.date: 04/12/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 822082d661863e737ea3d3a749a6c878db766967
ms.sourcegitcommit: e8e03309ba2515374a70c132d0758f3e1e1851d0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5977362"
---
# <a name="export-data-to-azure-synapse-analytics-preview"></a><span data-ttu-id="87dde-103">Esportatu datuak Azure Synapse Analytics-era (aurreargitalpena)</span><span class="sxs-lookup"><span data-stu-id="87dde-103">Export data to Azure Synapse Analytics (Preview)</span></span>

<span data-ttu-id="87dde-104">Azure Synapse datu-biltegi eta makrodatuen sistemen ikuspegi luzea lortzeko denbora azkartzen duen analisi zerbitzua da.</span><span class="sxs-lookup"><span data-stu-id="87dde-104">Azure Synapse is an analytics service that accelerates time to insight across data warehouses and big data systems.</span></span> <span data-ttu-id="87dde-105">Zure Customer Insights datuak gehitu eta erabil ditzakezu hemen: [Azure Synapse](/azure/synapse-analytics/overview-what-is).</span><span class="sxs-lookup"><span data-stu-id="87dde-105">You can ingest and use your Customer Insights data in [Azure Synapse](/azure/synapse-analytics/overview-what-is).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="87dde-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="87dde-106">Prerequisites</span></span>

<span data-ttu-id="87dde-107">Customer Insights-etik konexioa konfiguratzeko honako baldintza hauek bete behar dira Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="87dde-107">The following prerequisites must be met to configure the connection from Customer Insights to Azure Synapse.</span></span>

> [!NOTE]
> <span data-ttu-id="87dde-108">Ziurtatu guztiak ezartzen dituzula **funtzioak esleitzea** azaldu bezala.</span><span class="sxs-lookup"><span data-stu-id="87dde-108">Make sure to set all **role assignments** as described.</span></span>  

## <a name="prerequisites-in-customer-insights"></a><span data-ttu-id="87dde-109">Customer Insights-eko aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="87dde-109">Prerequisites in Customer Insights</span></span>

* <span data-ttu-id="87dde-110">Baduzu **Administratzailea** funtzioa hartzaileen xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="87dde-110">You have an **Administrator** role in audience insights.</span></span> <span data-ttu-id="87dde-111">Lortu informazio gehiago [erabiltzaileen baimenak ezartzea audientzia estatistiketan](permissions.md#assign-roles-and-permissions)</span><span class="sxs-lookup"><span data-stu-id="87dde-111">Learn more about [setting user permissions in audience insights](permissions.md#assign-roles-and-permissions)</span></span>

<span data-ttu-id="87dde-112">Azure-n:</span><span class="sxs-lookup"><span data-stu-id="87dde-112">In Azure:</span></span> 

- <span data-ttu-id="87dde-113">Azure harpidetza aktibo bat.</span><span class="sxs-lookup"><span data-stu-id="87dde-113">An active Azure subscription.</span></span>

- <span data-ttu-id="87dde-114">Azure Data Lake Storage Gen2 kontu berria erabiltzen baduzu, *hartzaileei buruzko informazioaren zerbitzu nagusia* beharrak **Biltegiko blob-datuen laguntzailea** baimenak.</span><span class="sxs-lookup"><span data-stu-id="87dde-114">If using a new Azure Data Lake Storage Gen2 account, the *service principal for audience insights* needs **Storage Blob Data Contributor** permissions.</span></span> <span data-ttu-id="87dde-115">Lortu informazio gehiago [Azure Data Lake Storage Gen2 kontu batera konektatzea Azure zerbitzuaren nagusiarekin hartzaileei buruzko informazioa lortzeko](connect-service-principal.md).</span><span class="sxs-lookup"><span data-stu-id="87dde-115">Learn more on [connecting to an Azure Data Lake Storage Gen2 account with Azure service principal for audience insights](connect-service-principal.md).</span></span> <span data-ttu-id="87dde-116">Data Lake Storage Gen2-k **behar du** [izen-leku hierarkikoa](/azure/storage/blobs/data-lake-storage-namespace) gaituta.</span><span class="sxs-lookup"><span data-stu-id="87dde-116">The Data Lake Storage Gen2 **must have** [hierarchical namespace](/azure/storage/blobs/data-lake-storage-namespace) enabled.</span></span>

- <span data-ttu-id="87dde-117">Baliabide taldean Azure Synapse laneko area dago *zerbitzu nagusia* eta *erabiltzailea ikusleentzako estatistiketarako* gutxienez esleitu behar da **Irakurlea** baimenak.</span><span class="sxs-lookup"><span data-stu-id="87dde-117">On the resource group the Azure Synapse workspace is located, the *service principal* and the *user for audience insights* needs to be assigned at least **Reader** permissions.</span></span> <span data-ttu-id="87dde-118">Informazio gehiagorako, ikusi [Esleitu Azure funtzioak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal).</span><span class="sxs-lookup"><span data-stu-id="87dde-118">For more information, see [Assign Azure roles using the Azure portal](/azure/role-based-access-control/role-assignments-portal).</span></span>

- <span data-ttu-id="87dde-119">*Erabiltzailea* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean.</span><span class="sxs-lookup"><span data-stu-id="87dde-119">The *user* needs **Storage Blob Data Contributor** permissions on the Azure Data Lake Storage Gen2 account where the data is located and linked to the Azure Synapse workspace.</span></span> <span data-ttu-id="87dde-120">Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).</span><span class="sxs-lookup"><span data-stu-id="87dde-120">Learn more about [using the Azure portal to assign an Azure role for access to blob and queue data](/azure/storage/common/storage-auth-aad-rbac-portal) and [Storage Blob Data Contributor permissions](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).</span></span>

- <span data-ttu-id="87dde-121">*[Azure Synapse laneko eremuaren kudeatutako identitatea](/azure/synapse-analytics/security/synapse-workspace-managed-identity)* **Biltegiratzearen blob-datuen laguntzailea** baimenak behar ditu Azure Data Lake Storage Gen2 kontuan datuak non kokatzen diren eta Azure Synapse laneko arean.</span><span class="sxs-lookup"><span data-stu-id="87dde-121">The *[Azure Synapse workspace managed identity](/azure/synapse-analytics/security/synapse-workspace-managed-identity)* needs **Storage Blob Data Contributor** permissions on the Azure Data Lake Storage Gen2 account where the data is located and linked to the Azure Synapse workspace.</span></span> <span data-ttu-id="87dde-122">Lortu informazio gehiago [Azure ataria erabiliz bloke eta ilara datuetara sartzeko Azure rola esleitzeko](/azure/storage/common/storage-auth-aad-rbac-portal) eta [Biltegiratzearen blob-datuen laguntzailearen baimenak](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).</span><span class="sxs-lookup"><span data-stu-id="87dde-122">Learn more on [using the Azure portal to assign an Azure role for access to blob and queue data](/azure/storage/common/storage-auth-aad-rbac-portal) and [Storage Blob Data Contributor permissions](/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor).</span></span>

- <span data-ttu-id="87dde-123">Azure Synapse laneko arean *hartzaileei buruzko informazioaren zerbitzu nagusiak* **Synapse-ren administratzailea** funtzioa behar du.</span><span class="sxs-lookup"><span data-stu-id="87dde-123">On the Azure Synapse workspace, the *service principal for audience insights* needs **Synapse Administrator** role assigned.</span></span> <span data-ttu-id="87dde-124">Informazio gehiagorako, ikus [Nola konfiguratu sarbide kontrola zure Synapse laneko areako](/azure/synapse-analytics/security/how-to-set-up-access-control).</span><span class="sxs-lookup"><span data-stu-id="87dde-124">For more information, see [How to set up access control for your Synapse workspace](/azure/synapse-analytics/security/how-to-set-up-access-control).</span></span>

## <a name="set-up-the-connection-and-export-to-azure-synapse"></a><span data-ttu-id="87dde-125">Konfiguratu eta esportatu konexioa Azure Synapse-ra</span><span class="sxs-lookup"><span data-stu-id="87dde-125">Set up the connection and export to Azure Synapse</span></span>

### <a name="configure-a-connection"></a><span data-ttu-id="87dde-126">Konfiguratu konexioa</span><span class="sxs-lookup"><span data-stu-id="87dde-126">Configure a connection</span></span>

1. <span data-ttu-id="87dde-127">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="87dde-127">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="87dde-128">Aukeratu **Gehitu konexioa** eta aukeratu **Azure Synapse Analytics** edo hautatu **Konfiguratu** **Azure Synapse Analytics** lauzan konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="87dde-128">Select **Add connection** and choose **Azure Synapse Analytics** or select the **Set up** on the **Azure Synapse Analytics** tile to configure the connection.</span></span>

1. <span data-ttu-id="87dde-129">Eman zure konexioa ezaguna den izena Bistaratze izena eremua.</span><span class="sxs-lookup"><span data-stu-id="87dde-129">Give your connection a recognizable name in the Display name field.</span></span> <span data-ttu-id="87dde-130">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="87dde-130">The name and the type of the connection describes this connection.</span></span> <span data-ttu-id="87dde-131">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="87dde-131">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="87dde-132">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="87dde-132">Choose who can use this connection.</span></span> <span data-ttu-id="87dde-133">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="87dde-133">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="87dde-134">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="87dde-134">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="87dde-135">Aukeratu edo bilatu Customer Insights datuak erabili nahi dituzun harpidetza.</span><span class="sxs-lookup"><span data-stu-id="87dde-135">Select or search for the subscription you want to use the Customer Insights data in.</span></span> <span data-ttu-id="87dde-136">Harpidetza hautatu bezain laster, hauta dezakezu **Laneko area**, **Biltegiratze kontua**, eta **Edukiontzia**.</span><span class="sxs-lookup"><span data-stu-id="87dde-136">As soon as a subscription is selected, you can also select **Workspace**, **Storage account**, and **Container**.</span></span>

1. <span data-ttu-id="87dde-137">Konexioa gordetzeko, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="87dde-137">Select **Save** to save the connection.</span></span>

### <a name="configure-an-export"></a><span data-ttu-id="87dde-138">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="87dde-138">Configure an export</span></span>

<span data-ttu-id="87dde-139">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="87dde-139">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="87dde-140">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="87dde-140">For more information, see [permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="87dde-141">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="87dde-141">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="87dde-142">Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.</span><span class="sxs-lookup"><span data-stu-id="87dde-142">To create a new export, select **Add export**.</span></span>

1. <span data-ttu-id="87dde-143">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa **Azure Synapse Analytics** sekzioan.</span><span class="sxs-lookup"><span data-stu-id="87dde-143">In the **Connection for export** field, choose a connection from the **Azure Synapse Analytics** section.</span></span> <span data-ttu-id="87dde-144">Atal honen izena ikusten ez baduzu, ez dago mota honetako [konexiorik](connections.md) erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="87dde-144">If you don't see this section name, there are no [connections](connections.md) of this type available to you.</span></span>

1. <span data-ttu-id="87dde-145">Ezagutzeko modukoa eman **Bistaratzeko izena** zure esportaziorako eta **Datu-basearen izena**.</span><span class="sxs-lookup"><span data-stu-id="87dde-145">Provide a recognizable **Display name** for your export and a **Database name**.</span></span>

1. <span data-ttu-id="87dde-146">Aukeratu zein entitatetara esportatu nahi duzun Azure Synapse Analytics-era.</span><span class="sxs-lookup"><span data-stu-id="87dde-146">Select which entities you want to export to Azure Synapse Analytics.</span></span>

1. <span data-ttu-id="87dde-147">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="87dde-147">Select **Save**.</span></span>

<span data-ttu-id="87dde-148">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="87dde-148">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="87dde-149">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="87dde-149">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="87dde-150">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="87dde-150">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span>

### <a name="update-an-export"></a><span data-ttu-id="87dde-151">Eguneratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="87dde-151">Update an export</span></span>

1. <span data-ttu-id="87dde-152">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="87dde-152">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="87dde-153">Hautatu **Editatu** eguneratu nahi duzun esportazioan.</span><span class="sxs-lookup"><span data-stu-id="87dde-153">Select **Edit** on the export you want to update.</span></span>

   - <span data-ttu-id="87dde-154">**Gehitu** edo **Kendu** hautapeneko entitateak.</span><span class="sxs-lookup"><span data-stu-id="87dde-154">**Add** or **Remove** entities from the selection.</span></span> <span data-ttu-id="87dde-155">Entitateak hautaketatik kentzen badira, ez dira Synapse Analytics datu basetik ezabatuko.</span><span class="sxs-lookup"><span data-stu-id="87dde-155">If entities are removed from the selection, they aren't deleted from the Synapse Analytics database.</span></span> <span data-ttu-id="87dde-156">Hala ere, etorkizuneko datuak freskatzeak ez ditu datu-base horretako kendutako entitateak eguneratuko.</span><span class="sxs-lookup"><span data-stu-id="87dde-156">However, future data refreshes won't update the removed entities in that database.</span></span>

   - <span data-ttu-id="87dde-157">**Datu-basearen izena aldatzea** Synapse Analytics datu-base berria sortzen du.</span><span class="sxs-lookup"><span data-stu-id="87dde-157">**Changing the Database Name** creates a new Synapse Analytics database.</span></span> <span data-ttu-id="87dde-158">Aurretik konfiguratutako izenaren datu baseak ez du eguneratzerik jasoko etorkizuneko freskatze-eragiketetan.</span><span class="sxs-lookup"><span data-stu-id="87dde-158">The database with the name that was configured before won't receive any updates in future refreshes.</span></span>
