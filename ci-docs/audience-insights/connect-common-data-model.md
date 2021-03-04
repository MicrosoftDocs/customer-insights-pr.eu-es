---
title: Konektatu Common Data Model-eko datuak Azure Data Lake kontu batekin
description: Egin lan Common Data Model-ekin Azure Data Lake Storage erabiliz.
ms.date: 05/29/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
ms.openlocfilehash: 247e4d9c47ff2373065ebf3c6d554323e45a120b
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267845"
---
# <a name="connect-to-a-common-data-model-folder-using-an-azure-data-lake-account"></a><span data-ttu-id="d9881-103">Konektatu Common Data Model karpetara Azure Data Lake kontua erabiliz</span><span class="sxs-lookup"><span data-stu-id="d9881-103">Connect to a Common Data Model folder using an Azure Data Lake account</span></span>

<span data-ttu-id="d9881-104">Artikulu honek Azure Data Lake Storage Gen2 kontua erabiliz Common Data Model-eko datuak sartzeko moduari buruzko informazioa eskaintzen du.</span><span class="sxs-lookup"><span data-stu-id="d9881-104">This article provides information on how to ingest data from a Common Data Model folder using your Azure Data Lake Storage Gen2 account.</span></span>

## <a name="important-considerations"></a><span data-ttu-id="d9881-105">Gogoeta garrantzitsuak</span><span class="sxs-lookup"><span data-stu-id="d9881-105">Important considerations</span></span>

- <span data-ttu-id="d9881-106">Azure Data Lake-eko datuek datu arrunten ereduaren estandarra jarraitu behar dute.</span><span class="sxs-lookup"><span data-stu-id="d9881-106">Data in your Azure Data Lake needs to follow the Common Data Model standard.</span></span> <span data-ttu-id="d9881-107">Oraingoz ez dira beste formatuak onartzen.</span><span class="sxs-lookup"><span data-stu-id="d9881-107">Other formats aren't supported at the moment.</span></span>

- <span data-ttu-id="d9881-108">Datuak sartzeak Azure Data Lake *Gen2* biltegiratze kontuak soilik onartzen ditu.</span><span class="sxs-lookup"><span data-stu-id="d9881-108">Data ingestion supports Azure Data Lake *Gen2* storage accounts exclusively.</span></span> <span data-ttu-id="d9881-109">Ezin dituzu Azure Data Lake Gen1 biltegiratze kontuak erabili datuak sartzeko.</span><span class="sxs-lookup"><span data-stu-id="d9881-109">You can't use Azure Data Lake Gen1 storage accounts to ingest data.</span></span>

- <span data-ttu-id="d9881-110">Azure zerbitzuaren entitatearekin autentifikatzeko, ziurtatu zure maizterrean konfiguratuta dagoela.</span><span class="sxs-lookup"><span data-stu-id="d9881-110">To authenticate with an Azure service principal, make sure it's configured in your tenant.</span></span> <span data-ttu-id="d9881-111">Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md).</span><span class="sxs-lookup"><span data-stu-id="d9881-111">For more information, see [Connect audience insights to an Azure Data Lake Storage Gen2 account with an Azure service principal](connect-service-principal.md).</span></span>

- <span data-ttu-id="d9881-112">Konektatu eta datuak sartu nahi dituzun Azure datu-biltegiak Dynamics 365 Customer Insights ingurunearen Azure eskualde berean egon behar du.</span><span class="sxs-lookup"><span data-stu-id="d9881-112">The Azure Data Lake you want to connect and ingest data from have to be in the same Azure region as the Dynamics 365 Customer Insights environment.</span></span> <span data-ttu-id="d9881-113">Ez da onartzen beste Azure eskualde bateko datu-biltegi batetik Common Data Model-eko karpeta batera konektatzea.</span><span class="sxs-lookup"><span data-stu-id="d9881-113">Connections to a Common Data Model folder from a data lake in a different Azure region is not supported.</span></span> <span data-ttu-id="d9881-114">Inguruneko Azure eskualdea ezagutzeko, joan hona: **Administratzailea** > **Sistema** > **Honi buruz** hartzaileei buruzko xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="d9881-114">To know the Azure region of the environment, go to **Admin** > **System** > **About** in audience insights.</span></span>

- <span data-ttu-id="d9881-115">Lineako zerbitzuetan gordetako datuak Dynamics 365 Customer Insights-en datuak prozesatzen edo gordetzen direna ez den beste kokaleku batean gorde daitezke.</span><span class="sxs-lookup"><span data-stu-id="d9881-115">Data stored in online services, may be stored in a different location than where data is processed or stored in Dynamics 365 Customer Insights.</span></span><span data-ttu-id="d9881-116">Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz onartu egiten duzu Dynamics 365 Customer Insights-rekin transferitu eta biltegiratu daitezkeen datuak. [Ezagutu gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)</span><span class="sxs-lookup"><span data-stu-id="d9881-116"> By importing or connecting to data stored in online services, you agree that data can be transferred to and stored with Dynamics 365 Customer Insights. [Learn more at the Microsoft Trust Center.](https://www.microsoft.com/trust-center)</span></span>

## <a name="connect-to-a-common-data-model-folder"></a><span data-ttu-id="d9881-117">Konektatu Common Data Model-eko karpeta batera</span><span class="sxs-lookup"><span data-stu-id="d9881-117">Connect to a Common Data Model folder</span></span>

1. <span data-ttu-id="d9881-118">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="d9881-118">In audience insights, go to **Data** > **Data sources**.</span></span>

1. <span data-ttu-id="d9881-119">Hautatu **Gehitu datu-iturburua**.</span><span class="sxs-lookup"><span data-stu-id="d9881-119">Select **Add data source**.</span></span>

1. <span data-ttu-id="d9881-120">Aukeratu **Konektatu Common Data Model karpeta batera**, sartu **Izena** datu-iturbururako, eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="d9881-120">Select **Connect to a Common Data Model folder**, enter a **Name** for the data source, and select **Next**.</span></span> <span data-ttu-id="d9881-121">Jarri izena jarraibideei:</span><span class="sxs-lookup"><span data-stu-id="d9881-121">Name guidelines:</span></span> 
   - <span data-ttu-id="d9881-122">Hasi letra batekin.</span><span class="sxs-lookup"><span data-stu-id="d9881-122">Start with a letter.</span></span>
   - <span data-ttu-id="d9881-123">Erabili letrak eta zenbakiak soilik.</span><span class="sxs-lookup"><span data-stu-id="d9881-123">Use letters and numbers only.</span></span> <span data-ttu-id="d9881-124">Ezin da idatzi karaktere berezirik edo zuriunerik.</span><span class="sxs-lookup"><span data-stu-id="d9881-124">Special characters and spaces are not allowed.</span></span>
   - <span data-ttu-id="d9881-125">Erabili 3 eta 64 karaktere artean.</span><span class="sxs-lookup"><span data-stu-id="d9881-125">Use between 3 and 64 characters.</span></span>

1. <span data-ttu-id="d9881-126">Baliabideetan oinarritutako aukera eta harpidetzan oinarritutako aukera erabil dezakezu autentifikatzeko.</span><span class="sxs-lookup"><span data-stu-id="d9881-126">You can choose between using a resource-based option and a subscription-based option for authentication.</span></span> <span data-ttu-id="d9881-127">Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md).</span><span class="sxs-lookup"><span data-stu-id="d9881-127">For more information, see [Connect audience insights to an Azure Data Lake Storage Gen2 account with an Azure service principal](connect-service-principal.md).</span></span> <span data-ttu-id="d9881-128">Sartu **Edukiontzia** -ren informazioa eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="d9881-128">Enter the **Container** information and select **Next**.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="d9881-129">![Elkarrizketa-koadroa Azure Data Lake-rako konexio xehetasun berriak sartzeko](media/enter-new-storage-details.png)
   > </span><span class="sxs-lookup"><span data-stu-id="d9881-129">![Dialog box to enter new connection details for Azure Data Lake](media/enter-new-storage-details.png)
   > </span></span>[!NOTE]
<span data-ttu-id="d9881-130">Datu-iturburu batera konektatu eta sortu ahal izateko goiko aipatutako edukiontzian edo biltegiratze kontuan honako rol hauetako bat behar duzu:</span><span class="sxs-lookup"><span data-stu-id="d9881-130">You need one of the following roles either to the container or the storage account referred above to be able to connect to and create a data source:</span></span>
   >  - <span data-ttu-id="d9881-131">Storage Blob datu-irakurgailua</span><span class="sxs-lookup"><span data-stu-id="d9881-131">Storage Blob Data Reader</span></span>
   >  - <span data-ttu-id="d9881-132">Storage Blob datuen jabea</span><span class="sxs-lookup"><span data-stu-id="d9881-132">Storage Blob Data Owner</span></span>
   >  - <span data-ttu-id="d9881-133">Storage Blob datuen kolaboratzailea</span><span class="sxs-lookup"><span data-stu-id="d9881-133">Storage Blob Data Contributor</span></span>

1. <span data-ttu-id="d9881-134">**Aukeratu Common Data Model karpeta** elkarrizketa-koadroa, hautatu datuak inportatzeko model.json edo manifest.json fitxategia eta hautatu **Hurrengoa**.</span><span class="sxs-lookup"><span data-stu-id="d9881-134">In the **Select a Common Data Model folder** dialog, select the model.json or manifest.json file to import data from, and select **Next**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="d9881-135">Inguruneko beste datu-iturburu batekin lotutako model.json edo manifest.json fitxategia ez da zerrendan agertuko.</span><span class="sxs-lookup"><span data-stu-id="d9881-135">Any model.json or manifest.json file associated with another data source in the environment won't show in the list.</span></span>

1. <span data-ttu-id="d9881-136">Aukeratutako model.json edo manifest.json fitxategian eskuragarri dauden entitateen zerrenda lortuko duzu.</span><span class="sxs-lookup"><span data-stu-id="d9881-136">You'll get a list of available entities in the selected model.json or manifest.json file.</span></span> <span data-ttu-id="d9881-137">Berrikusi eta hautatu egin dezakezu zerrendan eskuragarri dauden entitateak eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="d9881-137">You can review and select from the list of available entities and select **Save**.</span></span> <span data-ttu-id="d9881-138">Datu-iturburu berriko hautatutako entitate guztiak sartuko dira.</span><span class="sxs-lookup"><span data-stu-id="d9881-138">All of the selected entities will be ingested from the new data source.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="d9881-139">![Elkarrizketa-koadroa model.json fitxategi bateko entitateen zerrenda erakusten da](media/review-entities.png)</span><span class="sxs-lookup"><span data-stu-id="d9881-139">![Dialog box showing a list of entities from a model.json file](media/review-entities.png)</span></span>

8. <span data-ttu-id="d9881-140">Zehaztu zein datu-entitate gaitu nahi duzun datu-profilak gaitzeko eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="d9881-140">Indicate which data entities you want to enable data profiling and select **Save**.</span></span> <span data-ttu-id="d9881-141">Datuen profilak sortzean analisiak eta beste gaitasun batzuk gaitzen dira.</span><span class="sxs-lookup"><span data-stu-id="d9881-141">Data profiling enables analytics and other capabilities.</span></span> <span data-ttu-id="d9881-142">Entitate osoa hauta dezakezu, entitatetik atributu guztiak hautatzen dituena edo zenbait atributu hauta ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="d9881-142">You can select the whole entity, which selects all attributes from the entity, or select certain attributes of your choice.</span></span> <span data-ttu-id="d9881-143">Lehenespenez, ez dago entitaterik gaituta datu-profilak egiteko.</span><span class="sxs-lookup"><span data-stu-id="d9881-143">By default, no entity is enabled for data profiling.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="d9881-144">![Datu-profilak erakusten dituen elkarrizketa-koadroa](media/dataprofiling-entities.png)</span><span class="sxs-lookup"><span data-stu-id="d9881-144">![Dialog box showing a data profiling](media/dataprofiling-entities.png)</span></span>

9. <span data-ttu-id="d9881-145">Zure hautaketak gorde ondoren, **Datu iturriak** orria irekitzen da.</span><span class="sxs-lookup"><span data-stu-id="d9881-145">After saving your selections, the **Data sources** page opens.</span></span> <span data-ttu-id="d9881-146">Datu eredu arruntaren karpetaren konexioa datu-iturburu gisa ikusi beharko zenuke orain.</span><span class="sxs-lookup"><span data-stu-id="d9881-146">You should now see the Common Data Model folder connection as a data source.</span></span>

> [!NOTE]
> <span data-ttu-id="d9881-147">model.json edo manifest.json fitxategi bat ingurune bereko datu-iturburu batekin bakarrik lotu daiteke.</span><span class="sxs-lookup"><span data-stu-id="d9881-147">A model.json file or manifest.json can only associate with one data source in the same environment.</span></span> <span data-ttu-id="d9881-148">Hala ere, model.json edo manifest.json fitxategi bera erabil daiteke hainbat ingurunetako datu-iturburuetarako.</span><span class="sxs-lookup"><span data-stu-id="d9881-148">However, the same model.json or manifest.json file can be used for data sources in multiple environments.</span></span>

## <a name="edit-a-common-data-model-folder-data-source"></a><span data-ttu-id="d9881-149">Editatu datu arrunten ereduaren karpeta datu-iturburu</span><span class="sxs-lookup"><span data-stu-id="d9881-149">Edit a Common Data Model folder data source</span></span>

<span data-ttu-id="d9881-150">Common Data Model karpeta duen biltegiratze konturako sarbide gakoa egunera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="d9881-150">You can update the access key for the storage account containing the Common Data Model folder.</span></span> <span data-ttu-id="d9881-151">Model.json edo manifest.json fitxategia ere alda dezakezu.</span><span class="sxs-lookup"><span data-stu-id="d9881-151">You may also change the model.json or manifest.json file.</span></span> <span data-ttu-id="d9881-152">Biltegiratze kontutik beste edukiontzi batera konektatu nahi baduzu edo kontuaren izena aldatu nahi baduzu [datu-iturburu konexio berria sortu](#connect-to-a-common-data-model-folder).</span><span class="sxs-lookup"><span data-stu-id="d9881-152">To connect to a different container from your storage account, or change the account name, [create a new data source connection](#connect-to-a-common-data-model-folder).</span></span>

1. <span data-ttu-id="d9881-153">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.</span><span class="sxs-lookup"><span data-stu-id="d9881-153">In audience insights, go to **Data** > **Data sources**.</span></span>

2. <span data-ttu-id="d9881-154">Eguneratu nahi duzun datu-iturburu ondoan, hautatu elipsia.</span><span class="sxs-lookup"><span data-stu-id="d9881-154">Next to the data source you'd like to update, select the ellipsis.</span></span>

3. <span data-ttu-id="d9881-155">Hautatu **Editatu** aukera zerrendan.</span><span class="sxs-lookup"><span data-stu-id="d9881-155">Select the **Edit** option from the list.</span></span>

4. <span data-ttu-id="d9881-156">Aukeran, eguneratu **Sarbide gakoa** eta hautatu **hurrengo**.</span><span class="sxs-lookup"><span data-stu-id="d9881-156">Optionally, update the **Access key** and select **Next**.</span></span>

   ![Elkarrizketa-koadroa lehendik dagoen datu-iturburu-eko sarbide-gakoa editatzeko eta eguneratzeko](media/edit-access-key.png)

5. <span data-ttu-id="d9881-158">Aukeran, kontuaren gako konexio batetik baliabideetan oinarritutako edo harpidetzan oinarritutako konexio batera egunera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="d9881-158">Optionally, you can update from an account key connection to a resource-based or a subscription-based connection.</span></span> <span data-ttu-id="d9881-159">Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md).</span><span class="sxs-lookup"><span data-stu-id="d9881-159">For more information, see [Connect audience insights to an Azure Data Lake Storage Gen2 account with an Azure service principal](connect-service-principal.md).</span></span> <span data-ttu-id="d9881-160">Ezin duzu aldatu **Edukiontzia**-ren informazioa konexioa eguneratzean.</span><span class="sxs-lookup"><span data-stu-id="d9881-160">You can't change **Container** information when updating the connection.</span></span>
   > [!div class="mx-imgBorder"]

   > ![Elkarrizketa-koadroa Azure Data Lake-k lehendik dagoen biltegiratze-kontu batekin konexioaren xehetasunak sartzeko](media/enter-existing-storage-details.png)

   > [!NOTE]
   > <span data-ttu-id="d9881-162">Datu-iturburu batera konektatu eta sortu ahal izateko goiko aipatutako edukiontzian edo biltegiratze kontuan honako rol hauetako bat behar duzu:</span><span class="sxs-lookup"><span data-stu-id="d9881-162">You need one of the following roles either to the container or the storage account referred above to be able to connect to and create a data source:</span></span>
   >  - <span data-ttu-id="d9881-163">Storage Blob datu-irakurgailua</span><span class="sxs-lookup"><span data-stu-id="d9881-163">Storage Blob Data Reader</span></span>
   >  - <span data-ttu-id="d9881-164">Storage Blob datuen jabea</span><span class="sxs-lookup"><span data-stu-id="d9881-164">Storage Blob Data Owner</span></span>
   >  - <span data-ttu-id="d9881-165">Storage Blob datuen kolaboratzailea</span><span class="sxs-lookup"><span data-stu-id="d9881-165">Storage Blob Data Contributo</span></span>


6. <span data-ttu-id="d9881-166">Aukeran, aukeratu model.json edo manifest.json fitxategi desberdin bat edukiontziaren beste entitate multzo batekin.</span><span class="sxs-lookup"><span data-stu-id="d9881-166">Optionally, choose a different model.json or manifest.json file with a different set of entities from the container.</span></span>

7. <span data-ttu-id="d9881-167">Aukeran, sartzeko entitate osagarriak hauta ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="d9881-167">Optionally, you can select additional entities to ingest.</span></span> <span data-ttu-id="d9881-168">Dagoeneko hautatutako edozein entitate ken ditzakezu mendekotasunik ez badago.</span><span class="sxs-lookup"><span data-stu-id="d9881-168">You can also remove any already selected entities if there are no dependencies.</span></span>

   > [!IMPORTANT]
   > <span data-ttu-id="d9881-169">Lehendik dauden model.json edo manifest.json fitxategiaren eta entitateen multzoaren menpekotasunak badaude, errore mezu bat ikusiko duzu eta ezin duzu model.json edo manifest.json fitxategi desberdin bat hautatu.</span><span class="sxs-lookup"><span data-stu-id="d9881-169">If there are dependencies on the existing model.json or manifest.json file and the set of entities, you'll see an error message and can't select a different model.json or manifest.json file.</span></span> <span data-ttu-id="d9881-170">Kendu mendekotasun horiek model.json edo manifest.json fitxategia aldatu aurretik edo sortu datu-iturburu berri bat mendekotasunak ez kentzeko erabili nahi dituzun model.json edo manifest.json fitxategiarekin.</span><span class="sxs-lookup"><span data-stu-id="d9881-170">Remove those dependencies before changing the model.json or manifest.json file or create a new data source with the model.json or manifest.json file that you want to use to avoid removing the dependencies.</span></span>

8. <span data-ttu-id="d9881-171">Aukeran, atributu edo entitate osagarriak hauta ditzakezu datuen profilak gaitzeko edo lehendik hautatutakoak desgaitzeko.</span><span class="sxs-lookup"><span data-stu-id="d9881-171">Optionally, you can select additional attributes or entities to enable data profiling on or disable already selected ones.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]