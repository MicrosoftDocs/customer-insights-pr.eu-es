---
title: Enpresako profilak aberastea hirugarrenen Leadspace aberastearekin
description: Leadspace-ren hirugarrenen aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-MS
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: ccf4f661ecffb281556a4545b1f26ee809c697cd
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5895898"
---
# <a name="enrichment-of-company-profiles-with-leadspace-preview"></a><span data-ttu-id="77345-103">Enpresen profilak aberastea Leadspace-rekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="77345-103">Enrichment of company profiles with Leadspace (preview)</span></span>

<span data-ttu-id="77345-104">Leadspace B2B Bezeroaren Datuen Plataforma eskaintzen duen datuen zientzia enpresa da.</span><span class="sxs-lookup"><span data-stu-id="77345-104">Leadspace is a data science company that provides a B2B Customer Data Platform.</span></span> <span data-ttu-id="77345-105">Enpresentzako bezeroen profil bateratuak dituzten bezeroei beren datuak aberasteko aukera ematen die.</span><span class="sxs-lookup"><span data-stu-id="77345-105">It enables customers with unified customer profiles for companies to enrich their data.</span></span> <span data-ttu-id="77345-106">Aberasketek atributu gehiago biltzen dituzte, hala nola enpresaren tamaina, kokapena, industria eta abar.</span><span class="sxs-lookup"><span data-stu-id="77345-106">Enrichments include more attributes such as company size, location, industry, and more.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="77345-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="77345-107">Prerequisites</span></span>

<span data-ttu-id="77345-108">Leadspace konfiguratzeko eta konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="77345-108">To configure Leadspace, the following prerequisites must be met:</span></span>

- <span data-ttu-id="77345-109">Leadspace lizentzia aktiboa duzu.</span><span class="sxs-lookup"><span data-stu-id="77345-109">You have an active Leadspace license.</span></span>
- <span data-ttu-id="77345-110">Duzu [bezeroen profil bateratuak](customer-profiles.md) enpresentzat.</span><span class="sxs-lookup"><span data-stu-id="77345-110">You have [unified customer profiles](customer-profiles.md) for companies.</span></span>
- <span data-ttu-id="77345-111">Administratzaile batek konfiguratu du dagoeneko Leadspace konexioa edo zuk [administratzailea](permissions.md#administrator) baimenak eta "betiko giltza" (aipatzen da **Leadspace token**).</span><span class="sxs-lookup"><span data-stu-id="77345-111">A Leadspace connection has already been configured by an administrator or you have [administrator](permissions.md#administrator) permissions and the “perpetual key” (referred to as **Leadspace token**).</span></span> <span data-ttu-id="77345-112">Harremanetarako [Leadspace](https://www.leadspace.com/products/leadspace-on-demand/) zuzenean produktuaren inguruko xehetasunak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="77345-112">Contact [Leadspace](https://www.leadspace.com/products/leadspace-on-demand/) directly for details about their product.</span></span>

## <a name="configure-the-enrichment"></a><span data-ttu-id="77345-113">Konfiguratu aberastea</span><span class="sxs-lookup"><span data-stu-id="77345-113">Configure the enrichment</span></span>

1. <span data-ttu-id="77345-114">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Aberastea**.</span><span class="sxs-lookup"><span data-stu-id="77345-114">In audience insights, go to **Data** > **Enrichment**.</span></span>

1. <span data-ttu-id="77345-115">Aukeratu **Aberastu nire datuak** Leadspace fitxan eta hautatu **Hasi**.</span><span class="sxs-lookup"><span data-stu-id="77345-115">Select **Enrich my data** on the Leadspace tile and select **Get started**.</span></span>

   :::image type="content" source="media/leadspace-tile.png" alt-text="Leadspace lauzaren pantaila-argazkia.":::

1. <span data-ttu-id="77345-117">Hautatu [konexioa](connections.md) goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="77345-117">Select a [connection](connections.md) from the drop-down.</span></span> <span data-ttu-id="77345-118">Jarri harremanetan administratzaile batekin konexiorik ez badago.</span><span class="sxs-lookup"><span data-stu-id="77345-118">Contact an administrator if no connection is available.</span></span> <span data-ttu-id="77345-119">Administratzailea bazara, sor dezakezu konexioa **Gehitu konexioa** hautatuz eta **Leadspace** aukeratuz.</span><span class="sxs-lookup"><span data-stu-id="77345-119">If you are an administrator, you can create a connection by selecting **Add connection** and choosing **Leadspace**.</span></span> 

1. <span data-ttu-id="77345-120">Aukeratu **Konektatu Leadspace** konexioa berresteko.</span><span class="sxs-lookup"><span data-stu-id="77345-120">Select **Connect to Leadspace** to confirm the connection.</span></span>

1. <span data-ttu-id="77345-121">Aukeratu **Hurrengoa** eta aukeratu **Bezeroen datu multzoa** Leadspace konpainiaren datuekin aberastu nahi duzu.</span><span class="sxs-lookup"><span data-stu-id="77345-121">Select **Next** and choose the **Customer data set** you want to enrich with company data from Leadspace.</span></span> <span data-ttu-id="77345-122">**Bezeroen** entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="77345-122">You can select the **Customer** entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

    :::image type="content" source="media/enrichment-Leadspace-configuration-customer-data-set.png" alt-text="Pantaila-argazkia bezeroaren datu multzoa aukeratzerakoan.":::

1. <span data-ttu-id="77345-124">Aukeratu **Hurrengoa** eta zehaztu zure profil bateratuetako zein eremu mota erabili behar diren Leadspace-ko konpainiaren datuak bat datozen bilatzeko.</span><span class="sxs-lookup"><span data-stu-id="77345-124">Select **Next** and define which fields from your unified profiles are used to look for matching company data from Leadspace.</span></span> <span data-ttu-id="77345-125">**Enpresaren izena** eremua beharrezkoa da.</span><span class="sxs-lookup"><span data-stu-id="77345-125">The **Name of company** field is required.</span></span> <span data-ttu-id="77345-126">Bat-etortzeen zehaztasun handiagoa lortzeko, beste bi eremu, **Enpresaren webgunea** eta **Enpresaren kokapena**, gehitu daitezke.</span><span class="sxs-lookup"><span data-stu-id="77345-126">For a higher match accuracy, up to two other fields, **Company website** and **Company location**, can be added.</span></span>

   :::image type="content" source="media/enrichment-leadspace-mapping.png" alt-text="Leadspace eremuak esleitzeko panela.":::

1. <span data-ttu-id="77345-128">Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.</span><span class="sxs-lookup"><span data-stu-id="77345-128">Select **Next** to complete the field mapping.</span></span>

1. <span data-ttu-id="77345-129">Eman aberasturako izena eta hautatu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.</span><span class="sxs-lookup"><span data-stu-id="77345-129">Provide a name for the enrichment and select **Save enrichment** after reviewing your choices.</span></span>


## <a name="configure-the-connection-for-leadspace"></a><span data-ttu-id="77345-130">Konfiguratu konexioa Leadspace-rako</span><span class="sxs-lookup"><span data-stu-id="77345-130">Configure the connection for Leadspace</span></span> 

<span data-ttu-id="77345-131">Administratzailea izan behar duzu konexioak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="77345-131">You need to be an administrator to configure connections.</span></span> <span data-ttu-id="77345-132">Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** Leadspace fitxan.</span><span class="sxs-lookup"><span data-stu-id="77345-132">Select **Add connection** when configuring an enrichment *or* go to **Admin** > **Connections** and select **Set up** on the Leadspace tile.</span></span>

1. <span data-ttu-id="77345-133">Hautatu **Hasi erabiltzen**</span><span class="sxs-lookup"><span data-stu-id="77345-133">Select **Get Started**</span></span> 

1. <span data-ttu-id="77345-134">Idatzi konexioaren izena **Bistaratzeko izena** kutxa.</span><span class="sxs-lookup"><span data-stu-id="77345-134">Enter a name for the connection in the **Display name** box.</span></span>

1. <span data-ttu-id="77345-135">Hornitu balizoko Leadspace tokena.</span><span class="sxs-lookup"><span data-stu-id="77345-135">Provide a valid Leadspace token.</span></span>

1. <span data-ttu-id="77345-136">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia</span><span class="sxs-lookup"><span data-stu-id="77345-136">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox</span></span>

1. <span data-ttu-id="77345-137">Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.</span><span class="sxs-lookup"><span data-stu-id="77345-137">Select **Verify** to validate the configuration.</span></span>

1. <span data-ttu-id="77345-138">Egiaztapena amaitu ondoren, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="77345-138">After completing the verification, select **Save**.</span></span>
   
   :::image type="content" source="media/enrichment-Leadspace-connection.png" alt-text="Leadspace konexioa konfigurazioaren orria.":::

## <a name="enrichment-results"></a><span data-ttu-id="77345-140">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="77345-140">Enrichment results</span></span>

<span data-ttu-id="77345-141">Aberastea freskatu ondoren, azpian dagoen enpresa aberastutako datuak berrikus ditzakezu [Nire aberastasunak](enrichment-hub.md).</span><span class="sxs-lookup"><span data-stu-id="77345-141">After refreshing the enrichment, you can review the newly enriched company data under [My enrichments](enrichment-hub.md).</span></span> <span data-ttu-id="77345-142">Azken eguneraketaren ordua eta aberastutako profil kopurua aurki ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="77345-142">You can find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="77345-143">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="77345-143">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

<span data-ttu-id="77345-144">Informazio gehiago lortzeko, ikus [Leadspace API](https://support.leadspace.com/hc/en-us/sections/201997649-API).</span><span class="sxs-lookup"><span data-stu-id="77345-144">For more information, see [Leadspace APIs](https://support.leadspace.com/hc/en-us/sections/201997649-API).</span></span>

## <a name="next-steps"></a><span data-ttu-id="77345-145">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="77345-145">Next steps</span></span>

<span data-ttu-id="77345-146">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="77345-146">Build on top of your enriched customer data.</span></span> <span data-ttu-id="77345-147">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="77345-147">Create [segments](segments.md), [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="77345-148">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="77345-148">Data privacy and compliance</span></span>

<span data-ttu-id="77345-149">Dynamics 365 Customer Insights gaitzen duzunean datuak Leadspace-ra bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="77345-149">When you enable Dynamics 365 Customer Insights to transmit data to Leadspace, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="77345-150">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da Leadspace-k pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="77345-150">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that Leadspace meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="77345-151">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="77345-151">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="77345-152">Dynamics 365 Customer Insights administratzaileak edonoiz ken dezake aberastea funtzio hau erabiltzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="77345-152">Your Dynamics 365 Customer Insights Administrator can remove this enrichment at any time to discontinue use of this functionality.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
