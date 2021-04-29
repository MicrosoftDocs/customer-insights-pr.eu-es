---
title: Aberastea Experian hirugarrenen aberastearekin
description: Experian-en hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 9cf2a7fa18ecc022ea67f6829f52381ad59f3172
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5896358"
---
# <a name="enrich-customer-profiles-with-demographics-from-experian-preview"></a><span data-ttu-id="7f3ad-103">Aberastu bezeroen profilak demografiarekin Experian-etik (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="7f3ad-103">Enrich customer profiles with demographics from Experian (preview)</span></span>

<span data-ttu-id="7f3ad-104">Experian mundu mailako liderra da kontsumitzaileen eta negozioen kredituen berri emateko eta marketin zerbitzuetan.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-104">Experian is a global leader in consumer and business credit reporting and marketing services.</span></span> <span data-ttu-id="7f3ad-105">Batera Experianen datuak aberasteko zerbitzuak, zure bezeroen ulermen sakona sor dezakezu zure bezeroen profilak datu demografikoekin aberastuz, hala nola etxeko tamaina, diru sarrerak eta abar.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-105">With Experian’s data enrichment services, you can build a deeper understanding of your customers by enriching your customer profiles with demographic data such as household size, income, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7f3ad-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="7f3ad-106">Prerequisites</span></span>

<span data-ttu-id="7f3ad-107">Experian konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="7f3ad-107">To configure Experian, the following prerequisites must be met:</span></span>

- <span data-ttu-id="7f3ad-108">Experian harpidetza aktiboa duzu.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-108">You have an active Experian subscription.</span></span> <span data-ttu-id="7f3ad-109">Harpidetza lortzeko, [jarri harremanetan Experian-ekin](https://www.experian.com/marketing-services/contact) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-109">To get a subscription, [contact Experian](https://www.experian.com/marketing-services/contact) directly.</span></span> <span data-ttu-id="7f3ad-110">[Ikasi gehiago Experian datu-aberasteari buruz](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span><span class="sxs-lookup"><span data-stu-id="7f3ad-110">[Learn more about Experian Data Enrichment](https://www.experian.com/marketing-services/microsoft?cmpid=ems_web_mci_cdppage).</span></span>

- <span data-ttu-id="7f3ad-111">Administratzaile batek dagoeneko Experian konexioa konfiguratu du *edo* duzu [administratzailea](permissions.md#administrator) baimenak.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-111">An Experian connection has already been configured by an administrator *or* you have [administrator](permissions.md#administrator) permissions.</span></span> <span data-ttu-id="7f3ad-112">Experianek zuretzako sortu duen SSH gaitutako Garraio Seguru (ST) konturako Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia ere behar dituzu.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-112">You also need the User ID, Party ID, and Model Number for your SSH-enabled Secure Transport (ST) account that Experian created for you.</span></span>

## <a name="configure-the-enrichment"></a><span data-ttu-id="7f3ad-113">Konfiguratu aberastea</span><span class="sxs-lookup"><span data-stu-id="7f3ad-113">Configure the enrichment</span></span>

1. <span data-ttu-id="7f3ad-114">Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-114">Go to **Data** > **Enrichment** and select the **Discover** tab.</span></span>

1. <span data-ttu-id="7f3ad-115">Aukeratu **Aberastu nire datuak** Experian fitxan.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-115">Select **Enrich my data** on the Experian tile.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="7f3ad-116">![Teila Experian](media/experian-tile.png "Teila Experian")</span><span class="sxs-lookup"><span data-stu-id="7f3ad-116">![Experian tile](media/experian-tile.png "Experian tile")</span></span>
   > 

1. <span data-ttu-id="7f3ad-117">Hautatu [konexioa](connections.md) goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-117">Select a [connection](connections.md) from the drop-down.</span></span> <span data-ttu-id="7f3ad-118">Jarri harremanetan administratzaile batekin konexiorik ez badago.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-118">Contact an administrator if no connection is available.</span></span> <span data-ttu-id="7f3ad-119">Administratzailea bazara, sor dezakezu konexioa hautatuz **Gehitu konexioa** eta aukeratuz Experian goitibeherako zerrendan.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-119">If you are an administrator, you can create a connection by selecting **Add connection** and choosing Experian from the drop-down.</span></span> 

1. <span data-ttu-id="7f3ad-120">Aukeratu **Konektatu Experian** konexioaren hautapena berresteko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-120">Select **Connect to Experian** to confirm the connection selection.</span></span>

1.  <span data-ttu-id="7f3ad-121">Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** Experian datu demografikoekin aberastu nahi duzu.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-121">Select **Next** and choose the **Customer data set** you want to enrich with demographics data from Experian.</span></span> <span data-ttu-id="7f3ad-122">**Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-122">You can select the **Customer** entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

    :::image type="content" source="media/enrichment-Experian-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. <span data-ttu-id="7f3ad-124">Aukeratu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu mota erabili behar diren Experian-eko datu demografikoak bat datozen bilatzeko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-124">Select **Next** and define which type of fields from your unified profiles should be used to look for matching demographics data from Experian.</span></span> <span data-ttu-id="7f3ad-125">Eremuetako bat gutxienez **Izena eta helbidea**, **Mugikorra**, edo **Posta elektronikoa** beharrezkoa da.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-125">At least one of the fields **Name and address**, **Phone**, or **Email** is required.</span></span> <span data-ttu-id="7f3ad-126">Partiduen zehaztasun handiagoa lortzeko, beste bi eremu gehi daitezke.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-126">For a higher match accuracy, up to two other fields can be added.</span></span> <span data-ttu-id="7f3ad-127">Aukeraketa honek hurrengo urratsean atzitu ditzakezun mapen eremuei eragingo die.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-127">This selection will affect the mapping fields you have access to in the next step.</span></span>

    > [!TIP]
    > <span data-ttu-id="7f3ad-128">Litekeena da Experian-era bidalitako gako identifikatzaile atributu gehiagok bat etortze tasa handiagoa lortzea.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-128">More key identifier attributes sent to Experian likely yield a higher match rate.</span></span>

1. <span data-ttu-id="7f3ad-129">Hautatu **Hurrengoa** eremuaren jarraipena hasteko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-129">Select **Next** to start the field mapping.</span></span>

1. <span data-ttu-id="7f3ad-130">Definitu zure profil bateratuetako zein eremu mota erabili behar diren Experian-eko datu demografikoak bat datozen bilatzeko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-130">Define which fields from your unified profiles should be used to look for matching demographics data from Experian.</span></span> <span data-ttu-id="7f3ad-131">Eskatutako eremuak markatuta daude.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-131">Required fields are marked.</span></span>

1. <span data-ttu-id="7f3ad-132">Hornitu aberasturako izena eta irteerako entitatearen izena.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-132">Provide a name for the enrichment and a name for the output entity.</span></span>

1. <span data-ttu-id="7f3ad-133">Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-133">Select **Save enrichment** after reviewing your choices.</span></span>

## <a name="configure-the-connection-for-experian"></a><span data-ttu-id="7f3ad-134">Konfiguratu konexioa Experian-erako</span><span class="sxs-lookup"><span data-stu-id="7f3ad-134">Configure the connection for Experian</span></span> 

<span data-ttu-id="7f3ad-135">Administratzailea izan behar duzu konexioak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-135">You need to be an administrator to configure connections.</span></span> <span data-ttu-id="7f3ad-136">Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** Experian fitxan.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-136">Select **Add connection** when configuring an enrichment *or* go to **Admin** > **Connections** and select **Set up** on the Experian tile.</span></span>

1. <span data-ttu-id="7f3ad-137">Hautatu **Hasi erabiltzen**.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-137">Select **Get Started**.</span></span>

1. <span data-ttu-id="7f3ad-138">Idatzi konexioaren izena **Bistaratzeko izena** kutxa.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-138">Enter a name for the connection in the **Display name** box.</span></span>

1. <span data-ttu-id="7f3ad-139">Idatzi baliozko Erabiltzaile IDa, Alderdiaren IDa eta Modelo zenbakia Experian Secure Transport konturako.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-139">Enter valid User ID, Party ID, and Model Number for your Experian Secure Transport account.</span></span>

1. <span data-ttu-id="7f3ad-140">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia</span><span class="sxs-lookup"><span data-stu-id="7f3ad-140">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox</span></span>

1. <span data-ttu-id="7f3ad-141">Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-141">Select **Verify** to validate the configuration.</span></span>

1. <span data-ttu-id="7f3ad-142">Egiaztapena amaitu ondoren, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-142">After completing the verification, select **Save**.</span></span>
   
   :::image type="content" source="media/enrichment-Experian-connection.png" alt-text="Experian konexioa konfigurazioaren panela.":::

## <a name="enrichment-results"></a><span data-ttu-id="7f3ad-144">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="7f3ad-144">Enrichment results</span></span>

<span data-ttu-id="7f3ad-145">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-145">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="7f3ad-146">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="7f3ad-146">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="7f3ad-147">Prozesatzeko denbora zure bezeroen datuen tamainaren eta Experian-ek zure konturako aberastutako prozesuen araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-147">The processing time will depend on the size of your customer data and the enrichment processes set up for your account by Experian.</span></span>

<span data-ttu-id="7f3ad-148">Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-148">After the enrichment process completes, you can review the newly enriched customer profiles data under **My enrichments**.</span></span> <span data-ttu-id="7f3ad-149">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-149">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="7f3ad-150">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-150">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="7f3ad-151">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="7f3ad-151">Next steps</span></span>

<span data-ttu-id="7f3ad-152">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-152">Build on top of your enriched customer data.</span></span> <span data-ttu-id="7f3ad-153">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-153">Create [segments](segments.md), [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="7f3ad-154">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="7f3ad-154">Data privacy and compliance</span></span>

<span data-ttu-id="7f3ad-155">Dynamics 365 Customer Insights gaitzen duzunean datuak Experian-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-155">When you enable Dynamics 365 Customer Insights to transmit data to Experian, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="7f3ad-156">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Experian-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-156">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Experian meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="7f3ad-157">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="7f3ad-157">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="7f3ad-158">Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="7f3ad-158">Your Dynamics 365 Customer Insights Administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
