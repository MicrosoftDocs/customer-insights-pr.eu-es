---
title: Sortu eta kudeatu inguruneak
description: Ikasi zerbitzuan izena ematen eta inguruneak kudeatzen.
ms.date: 11/10/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
ms.reviewer: nimagen
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 010336445d0825a7ff82d1b7a65702fc12245788
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644118"
---
# <a name="manage-environments"></a><span data-ttu-id="9f953-103">Kudeatu inguruneak</span><span class="sxs-lookup"><span data-stu-id="9f953-103">Manage environments</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="9f953-104">Artikulu honetan erakunde berri bat nola sortu eta ingurune bat nola hornitu azaltzen da.</span><span class="sxs-lookup"><span data-stu-id="9f953-104">This article explains how to create a new organization and how to provision an environment.</span></span>

## <a name="sign-up-and-create-an-organization"></a><span data-ttu-id="9f953-105">Eman izena eta sortu erakunde bat</span><span class="sxs-lookup"><span data-stu-id="9f953-105">Sign up and create an organization</span></span>

1. <span data-ttu-id="9f953-106">Joan [Dynamics 365 Customer Insights](https://dynamics.microsoft.com/ai/customer-insights/) webgunea.</span><span class="sxs-lookup"><span data-stu-id="9f953-106">Go to the [Dynamics 365 Customer Insights](https://dynamics.microsoft.com/ai/customer-insights/) website.</span></span>

2. <span data-ttu-id="9f953-107">Hautatu **Hasi erabiltzen**.</span><span class="sxs-lookup"><span data-stu-id="9f953-107">Select **Get Started**.</span></span>

3. <span data-ttu-id="9f953-108">Aukeratu zure sinadura-agertokia eta hautatu dagokion esteka.</span><span class="sxs-lookup"><span data-stu-id="9f953-108">Choose your preferred sign-up scenario and select the corresponding link.</span></span>

4. <span data-ttu-id="9f953-109">Onartu baldintzak eta hautatu **Jarraitu** erakundea sortzen hasteko.</span><span class="sxs-lookup"><span data-stu-id="9f953-109">Accept the terms and conditions and select **Continue** to start creating the organization.</span></span>

5. <span data-ttu-id="9f953-110">Ingurunea sortu ondoren, bertara birbideratuko zaituzte [Customer Insights](https://home.ci.ai.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="9f953-110">After the environment is created, you'll be redirected to [Customer Insights](https://home.ci.ai.dynamics.com).</span></span>

6. <span data-ttu-id="9f953-111">Erabili demo ingurunea aplikazioa arakatzeko edo ingurune berria sortzeko hurrengo ataleko urratsak jarraituz.</span><span class="sxs-lookup"><span data-stu-id="9f953-111">Use the demo environment to explore the app, or create a new environment by following the steps in the next section.</span></span>

7. <span data-ttu-id="9f953-112">Ingurumenaren ezarpenak zehaztu ondoren, hautatu **Sortu**.</span><span class="sxs-lookup"><span data-stu-id="9f953-112">After specifying the environment settings, select **Create**.</span></span>

8. <span data-ttu-id="9f953-113">Ingurunea behar bezala sortu ondoren hasiko da saioa.</span><span class="sxs-lookup"><span data-stu-id="9f953-113">You'll be signed in after the environment was created successfully.</span></span>

## <a name="create-an-environment-in-an-existing-organization"></a><span data-ttu-id="9f953-114">Sortu ingurune bat lehendik dagoen erakunde batean</span><span class="sxs-lookup"><span data-stu-id="9f953-114">Create an environment in an existing organization</span></span>

<span data-ttu-id="9f953-115">Ingurune berria sortzeko bi era daude:</span><span class="sxs-lookup"><span data-stu-id="9f953-115">There are two ways to create a new environment.</span></span> <span data-ttu-id="9f953-116">Guztiz konfigurazio berria zehaz dezakezu edo konfigurazio ezarpen batzuk kopiatu ditzakezu lehendik dagoen ingurunetik.</span><span class="sxs-lookup"><span data-stu-id="9f953-116">You can either specify an entirely new configuration, or you can copy some configuration settings from an existing environment.</span></span>

<span data-ttu-id="9f953-117">Ingurune bat sortzeko:</span><span class="sxs-lookup"><span data-stu-id="9f953-117">To create an environment:</span></span>

1. <span data-ttu-id="9f953-118">Hautatu botoia **ezarpenak** ikurra aplikazioaren goiburuan.</span><span class="sxs-lookup"><span data-stu-id="9f953-118">Select the **Settings** symbol in the header of the app.</span></span>

1. <span data-ttu-id="9f953-119">Hautatu **Ingurune berria**.</span><span class="sxs-lookup"><span data-stu-id="9f953-119">Select **New environment**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="9f953-120">![Ingurune-ezarpenak](media/environment-settings-dialog.png)</span><span class="sxs-lookup"><span data-stu-id="9f953-120">![Environment settings](media/environment-settings-dialog.png)</span></span>

1. <span data-ttu-id="9f953-121">**Inguru berria sortu** elkarrizketa-koadroa, hautatu **Ingurune berria**.</span><span class="sxs-lookup"><span data-stu-id="9f953-121">In the **Create new environment** dialog, select **New environment**.</span></span>

   <span data-ttu-id="9f953-122">Nahi baduzu [kopiatu uneko inguruneko datuak](#additional-considerations-for-copy-configuration-preview), hautatu **Kopiatu lehendik dagoen ingurunetik**.</span><span class="sxs-lookup"><span data-stu-id="9f953-122">If you want to [copy data from the current environment](#additional-considerations-for-copy-configuration-preview), select **Copy from existing environment**.</span></span> <span data-ttu-id="9f953-123">Zure erakundearen eskura dauden ingurune guztien zerrenda ikusiko duzu non datuak kopiatzeko.</span><span class="sxs-lookup"><span data-stu-id="9f953-123">You'll see a list of all available environments in your organization where you can copy data from.</span></span>

1. <span data-ttu-id="9f953-124">Hornitu hurrengo xehetasunak:</span><span class="sxs-lookup"><span data-stu-id="9f953-124">Provide the following details:</span></span>
   - <span data-ttu-id="9f953-125">**Izena**: entitatearen izena.</span><span class="sxs-lookup"><span data-stu-id="9f953-125">**Name**: The name for this environment.</span></span> <span data-ttu-id="9f953-126">Eremu hau dagoeneko bete da ingurune batetik kopiatzen baduzu, baina alda dezakezu.</span><span class="sxs-lookup"><span data-stu-id="9f953-126">This field is already filled in if you've copied an existing environment, but you can change it.</span></span>
   - <span data-ttu-id="9f953-127">**Eskualdea**: Zerbitzua hedatu eta ostatatzen den eskualdea.</span><span class="sxs-lookup"><span data-stu-id="9f953-127">**Region**: The region into which the service is deployed and hosted.</span></span>
   - <span data-ttu-id="9f953-128">**Mota**: Aukeratu Produkzio edo Sandbox ingurunea sortu nahi duzun ala ez.</span><span class="sxs-lookup"><span data-stu-id="9f953-128">**Type**: Select whether you want to create a Production or Sandbox environment.</span></span>

2. <span data-ttu-id="9f953-129">Nahi baduzu, hauta dezakezu **Ezarpen aurreratuak**:</span><span class="sxs-lookup"><span data-stu-id="9f953-129">Optionally, you can select **Advanced settings**:</span></span>

   - <span data-ttu-id="9f953-130">**Gorde datu guztiak**: Customer Insights-ek sortutako irteerako datuak non gorde nahi dituzun zehazten du.</span><span class="sxs-lookup"><span data-stu-id="9f953-130">**Save all data to**: Specifies where you want to store the output data generated from Customer Insights.</span></span> <span data-ttu-id="9f953-131">Bi aukera dituzu: **Customer Insights biltegiratzea** (Azure Data Lake Customer Insights taldearen bidez kudeatua) eta **Azure Data Lake Storage Gen2** (zure berezko Azure Data Lake Storage).</span><span class="sxs-lookup"><span data-stu-id="9f953-131">You'll have two options: **Customer Insights storage** (an Azure Data Lake managed by the Customer Insights team) and **Azure Data Lake Storage Gen2** (your own Azure Data Lake Storage).</span></span> <span data-ttu-id="9f953-132">Lehenespenez, Customer Insights biltegiratzeko aukera hautatuko da.</span><span class="sxs-lookup"><span data-stu-id="9f953-132">By default, the Customer Insights storage option is selected.</span></span>

   > [!NOTE]
   > <span data-ttu-id="9f953-133">Datuak Azure Data Lake Storage-n gordez gero, onartu egingo duzu datuak Azure biltegiratze-konturako egokia den kokaleku geografikora transferitu eta bertan biltegiratuko direla, eta balitekeela Dynamics 365 Customer Insights-en datuak biltegiratzen diren lekua ez den beste kokaleku bat izatea. Informazio gehiago lortzeko, ikusi.</span><span class="sxs-lookup"><span data-stu-id="9f953-133">By saving data to Azure Data Lake Storage, you agree that data will be transferred to and stored in the appropriate geographic location for that Azure storage account, which may differ from where data is stored in Dynamics 365 Customer Insights.</span></span> [<span data-ttu-id="9f953-134">Argibide gehiago Microsoft Trust Center-en.</span><span class="sxs-lookup"><span data-stu-id="9f953-134">Learn more at the Microsoft Trust Center.</span></span>](https://www.microsoft.com/trust-center)
   >
   > <span data-ttu-id="9f953-135">Gaur egun, irensten diren erakundeak Customer Insights kudeatutako data lake-n gordetzen dira beti.</span><span class="sxs-lookup"><span data-stu-id="9f953-135">Currently, ingested entities are always stored in the Customer Insights managed data lake.</span></span>
   > <span data-ttu-id="9f953-136">Ingurunea sortzerakoan hautatu zenuen Azure eskualde bereko Azure Data Lake Gen2 biltegiratze kontuak soilik onartzen ditugu.</span><span class="sxs-lookup"><span data-stu-id="9f953-136">We support only Azure Data Lake Gen2 storage accounts from the same Azure region you selected when creating the environment.</span></span>
   > <span data-ttu-id="9f953-137">Azure Data Lake Gen2 Hierarkikoa Izen espazioaren (HNS) gaitutako biltegiratze kontuak soilik onartzen ditugu.</span><span class="sxs-lookup"><span data-stu-id="9f953-137">We support only Azure Data Lake Gen2 Hierarchical Name Space (HNS) enabled storage accounts.</span></span>

   - <span data-ttu-id="9f953-138">Azure Data Lake Storage Gen2 aukerarako, baliabideetan oinarritutako aukera eta harpidetzan oinarritutako aukera erabil dezakezu autentifikatzeko.</span><span class="sxs-lookup"><span data-stu-id="9f953-138">For the Azure Data Lake Storage Gen2 option, you can choose between a resource-based option and a subscription-based option for authentication.</span></span> <span data-ttu-id="9f953-139">Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md).</span><span class="sxs-lookup"><span data-stu-id="9f953-139">For more information, see [Connect audience insights to an Azure Data Lake Storage Gen2 account with an Azure service principal](connect-service-principal.md).</span></span> <span data-ttu-id="9f953-140">**Edukiontzia** izena ezin da aldatu eta "customerinsights" izango da.</span><span class="sxs-lookup"><span data-stu-id="9f953-140">The **Container** name can't be changed and will be "customerinsights".</span></span>
   
   - <span data-ttu-id="9f953-141">[Iragarpenak](predictions.md) erabili nahi badituzu, sartu Common Data Service instantziaren URLa **Zerbitzariaren helbidea** eremua, **Erabili iragarpenak** atalean.</span><span class="sxs-lookup"><span data-stu-id="9f953-141">If you want to use [predictions](predictions.md), enter the Common Data Service instance URL in the **Server address** field under **Use predictions**.</span></span>

   <span data-ttu-id="9f953-142">Prozesuak exekutatzen dituzunean, adibidez, datuak sartzea edo segmentua sortzea, dagozkien karpetak sortuko dira goian zehaztu duzun biltegiratze kontuan.</span><span class="sxs-lookup"><span data-stu-id="9f953-142">When you run processes, such as data ingestion or segment creation, corresponding folders will be created in the storage account you specified above.</span></span> <span data-ttu-id="9f953-143">Datu fitxategiak eta model.json fitxategiak dagozkien azpi-karpetetan sortu eta gehituko dira exekutatzen duzun prozesuan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="9f953-143">Data files and model.json files will be created and added to the respective subfolders based on the process you run.</span></span>

   <span data-ttu-id="9f953-144">Customer Insights-eko hainbat ingurune sortzen badituzu eta ingurune horietako irteerako entitateak zure biltegiratze kontuan gordetzea aukeratzen baduzu, karpeta bereiziak sortuko dira ingurune bakoitzarentzat ci_<environmentid> edukiontzian.</span><span class="sxs-lookup"><span data-stu-id="9f953-144">If you create multiple environments of Customer Insights and choose to save the output entities from those environments in your storage account, separate folders will be created for each environment with ci_<environmentid> in the container.</span></span>

### <a name="additional-considerations-for-copy-configuration-preview"></a><span data-ttu-id="9f953-145">Kopiaren konfiguraziorako gogoeta osagarriak (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="9f953-145">Additional considerations for copy configuration (preview)</span></span>

<span data-ttu-id="9f953-146">Hurrengo konfigurazio ezarpenak kopiatzen dira:</span><span class="sxs-lookup"><span data-stu-id="9f953-146">The following configuration settings are copied:</span></span>

- <span data-ttu-id="9f953-147">Eginbide konfigurazioak</span><span class="sxs-lookup"><span data-stu-id="9f953-147">Feature configurations</span></span>
- <span data-ttu-id="9f953-148">Inbertitu / inportatutako datu-iturriak</span><span class="sxs-lookup"><span data-stu-id="9f953-148">Inegsted/imported data sources</span></span>
- <span data-ttu-id="9f953-149">Datuen bateratzea (mapa, bat etorri, batu) konfigurazioa</span><span class="sxs-lookup"><span data-stu-id="9f953-149">Data unification (Map, Match, Merge) configuration</span></span>
- <span data-ttu-id="9f953-150">Segmentuak</span><span class="sxs-lookup"><span data-stu-id="9f953-150">Segments</span></span>
- <span data-ttu-id="9f953-151">Neurriak</span><span class="sxs-lookup"><span data-stu-id="9f953-151">Measures</span></span>
- <span data-ttu-id="9f953-152">Erlazioak</span><span class="sxs-lookup"><span data-stu-id="9f953-152">Relationships</span></span>
- <span data-ttu-id="9f953-153">Jarduerak</span><span class="sxs-lookup"><span data-stu-id="9f953-153">Activities</span></span>
- <span data-ttu-id="9f953-154">Bilaketa eta iragazkien indizea</span><span class="sxs-lookup"><span data-stu-id="9f953-154">Search & filter Index</span></span>
- <span data-ttu-id="9f953-155">Esportatze-helburuak</span><span class="sxs-lookup"><span data-stu-id="9f953-155">Export destinations</span></span>
- <span data-ttu-id="9f953-156">Programatutako freskatzea</span><span class="sxs-lookup"><span data-stu-id="9f953-156">Scheduled refresh</span></span>
- <span data-ttu-id="9f953-157">Aberasteak</span><span class="sxs-lookup"><span data-stu-id="9f953-157">Enrichments</span></span>
- <span data-ttu-id="9f953-158">Ereduen kudeaketa</span><span class="sxs-lookup"><span data-stu-id="9f953-158">Model management</span></span>
- <span data-ttu-id="9f953-159">Funtzio-zereginak</span><span class="sxs-lookup"><span data-stu-id="9f953-159">Role assignments</span></span>

<span data-ttu-id="9f953-160">Hurrengo konfigurazio ezarpenak kopiatzen *ez* dira:</span><span class="sxs-lookup"><span data-stu-id="9f953-160">The following settings are *not* copied:</span></span>

- <span data-ttu-id="9f953-161">Bezeroen profilak.</span><span class="sxs-lookup"><span data-stu-id="9f953-161">Customer profiles.</span></span>
- <span data-ttu-id="9f953-162">Datu-iturburuaren kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="9f953-162">Data source credentials.</span></span> <span data-ttu-id="9f953-163">Datu-iturburu bakoitzerako kredentzialak eman beharko dituzu eta datu iturriak eskuz freskatu.</span><span class="sxs-lookup"><span data-stu-id="9f953-163">You'll have to provide the credentials for every data source and refresh the data sources manually.</span></span>
- <span data-ttu-id="9f953-164">Datu iturri arruntaren karpetaren datu iturriak Common Data Service lakua kudeatu.</span><span class="sxs-lookup"><span data-stu-id="9f953-164">Data sources from Common Data Model folder and Common Data Service managed lake.</span></span> <span data-ttu-id="9f953-165">Datu iturri horiek eskuz sortu beharko dituzu iturri ingurunean izen berdinekin.</span><span class="sxs-lookup"><span data-stu-id="9f953-165">You'll have to create those data sources manually with the same name as in the source environment.</span></span>

<span data-ttu-id="9f953-166">Ingurumena kopiatzean, berrespen mezu bat ikusiko duzu ingurune berria sortu dela.</span><span class="sxs-lookup"><span data-stu-id="9f953-166">When you copy an environment, you'll see a confirmation message that the new environment has been created.</span></span> <span data-ttu-id="9f953-167">Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.</span><span class="sxs-lookup"><span data-stu-id="9f953-167">Select **Go to data sources** to see the list of data sources.</span></span>

<span data-ttu-id="9f953-168">Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera.</span><span class="sxs-lookup"><span data-stu-id="9f953-168">All the data sources will show a **Credentials Required** status.</span></span> <span data-ttu-id="9f953-169">Editatu datu-iturriak eta sartu kredentzialak freskatzeko.</span><span class="sxs-lookup"><span data-stu-id="9f953-169">Edit the data sources and enter the credentials to refresh them.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="9f953-170">![Kopiatutako datu-iturburuak](media/data-sources-copied.png)</span><span class="sxs-lookup"><span data-stu-id="9f953-170">![Data sources copied](media/data-sources-copied.png)</span></span>

<span data-ttu-id="9f953-171">Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**.</span><span class="sxs-lookup"><span data-stu-id="9f953-171">After refreshing the data sources, go to **Data** > **Unify**.</span></span> <span data-ttu-id="9f953-172">Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="9f953-172">Here you'll find settings from the source environment.</span></span> <span data-ttu-id="9f953-173">Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.</span><span class="sxs-lookup"><span data-stu-id="9f953-173">Edit them as needed or select **Run** to start the data unification process and create the unified customer entity.</span></span>

<span data-ttu-id="9f953-174">Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.</span><span class="sxs-lookup"><span data-stu-id="9f953-174">When the data unification is complete, go to **Measures** and **Segments** to refresh them too.</span></span>

## <a name="edit-an-existing-environment"></a><span data-ttu-id="9f953-175">Editatu lehendik dagoen ingurunea</span><span class="sxs-lookup"><span data-stu-id="9f953-175">Edit an existing environment</span></span>

<span data-ttu-id="9f953-176">Dauden inguruneen xehetasun batzuk editatu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="9f953-176">You can edit some of the details of existing environments.</span></span>

1. <span data-ttu-id="9f953-177">Joan **Administratzailea** > **Sistema** > **Hurrengoari buruz**.</span><span class="sxs-lookup"><span data-stu-id="9f953-177">Go to **Admin** > **System** > **About**.</span></span>

2. <span data-ttu-id="9f953-178">Hautatu **Editatu**.</span><span class="sxs-lookup"><span data-stu-id="9f953-178">Select **Edit**.</span></span>

3. <span data-ttu-id="9f953-179">Ingurugiroa eguneratu dezakezu **Bistaratu izena** baina ezin duzu aldatu **Eskualdea** edo **Mota**.</span><span class="sxs-lookup"><span data-stu-id="9f953-179">You can update the environment's **Display name**, but you can't change the **Region** or **Type**.</span></span>

4. <span data-ttu-id="9f953-180">Ingurumena konfiguratuta badago, datuak gordetzeko Azure Data Lake Storage Gen2, eguneratu dezakezu **Kontuaren gakoa**.</span><span class="sxs-lookup"><span data-stu-id="9f953-180">If an environment is configured to store data in Azure Data Lake Storage Gen2, you can update the **Account key**.</span></span> <span data-ttu-id="9f953-181">Hala ere, ezin duzu aldatu **Kontuaren izena** edo **edukiontzia** izendatzeko.</span><span class="sxs-lookup"><span data-stu-id="9f953-181">However, you can't change the **Account name** or **Container** name.</span></span>

5. <span data-ttu-id="9f953-182">Aukeran, kontuaren gakoan oinarritutako konexio batetik baliabideetan oinarritutako edo harpidetzan oinarritutako konexio batera egunera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="9f953-182">Optionally, you can update from an account key based connection to a resource-based or subscription-based connection.</span></span> <span data-ttu-id="9f953-183">Bertsio berritu ondoren, ezin duzu kontuaren gakoetara itzuli eguneratu ondoren.</span><span class="sxs-lookup"><span data-stu-id="9f953-183">Once upgraded, you cannot revert to account key after the update.</span></span> <span data-ttu-id="9f953-184">Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md).</span><span class="sxs-lookup"><span data-stu-id="9f953-184">For more information, see [Connect audience insights to an Azure Data Lake Storage Gen2 account with an Azure service principal](connect-service-principal.md).</span></span> <span data-ttu-id="9f953-185">Ezin duzu aldatu **Edukiontzia**-ren informazioa konexioa eguneratzean.</span><span class="sxs-lookup"><span data-stu-id="9f953-185">You can't change **Container** information when updating the connection.</span></span>

## <a name="reset-an-existing-environment"></a><span data-ttu-id="9f953-186">Berrezarri lehendik dagoen ingurunea</span><span class="sxs-lookup"><span data-stu-id="9f953-186">Reset an existing environment</span></span>

<span data-ttu-id="9f953-187">Ingurunea egoera hutsera berrezar dezakezu konfigurazio guztiak ezabatu eta sartutako datuak kendu nahi badituzu.</span><span class="sxs-lookup"><span data-stu-id="9f953-187">You can reset an environment to an empty state if you want to delete all configurations and remove the ingested data.</span></span>

1.  <span data-ttu-id="9f953-188">Joan **Administratzailea** > **Sistema** > **Hurrengoari buruz**.</span><span class="sxs-lookup"><span data-stu-id="9f953-188">Go to **Admin** > **System** > **About**.</span></span>

2.  <span data-ttu-id="9f953-189">Hautatu **Berrezarri**.</span><span class="sxs-lookup"><span data-stu-id="9f953-189">Select **Reset**.</span></span> 

3.  <span data-ttu-id="9f953-190">Ezabapena berresteko, idatzi ingurunearen izena eta hautatu **Berrezarri**.</span><span class="sxs-lookup"><span data-stu-id="9f953-190">To confirm the deletion, enter the environment name and select **Reset**.</span></span>


## <a name="delete-an-existing-environment"></a><span data-ttu-id="9f953-191">Aurretik bazegoen ingurune bat ezabatu</span><span class="sxs-lookup"><span data-stu-id="9f953-191">Delete an existing environment</span></span>

1. <span data-ttu-id="9f953-192">Joan **Administratzailea** > **Sistema** > **Hurrengoari buruz**.</span><span class="sxs-lookup"><span data-stu-id="9f953-192">Go to **Admin** > **System** > **About**.</span></span>

1. <span data-ttu-id="9f953-193">Hautatu **Ezabatu**.</span><span class="sxs-lookup"><span data-stu-id="9f953-193">Select **Delete**.</span></span>

1. <span data-ttu-id="9f953-194">Ezabatzea berresteko, idatzi ingurumenaren izena eta hautatu **Ezabatu**.</span><span class="sxs-lookup"><span data-stu-id="9f953-194">To confirm the deletion, enter the environment name and select **Delete**.</span></span>
