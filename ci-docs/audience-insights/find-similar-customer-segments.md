---
title: Bilatu antzeko bezeroak adimen artifizialarekin
description: Aurkitu antzeko bezeroen segmentuak adimen artifizialarekin.
ms.date: 06/25/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: jimsonc
manager: shellyha
ms.openlocfilehash: 8cdec4edd599b0249fcf144b5e5c0124504e1e14
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404984"
---
# <a name="similar-customers-preview"></a><span data-ttu-id="32921-103">Bezero antzekoak (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="32921-103">Similar Customers (preview)</span></span>

<span data-ttu-id="32921-104">Ezaugarri honek adimen artifiziala erabiliz zure bezero basean antzeko bezeroak topa ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="32921-104">This feature lets you find similar customers in your customer base using artificial intelligence.</span></span> <span data-ttu-id="32921-105">Ezaugarri hau erabiltzeko gutxienez segmentu bat sortu behar duzu.</span><span class="sxs-lookup"><span data-stu-id="32921-105">You need to have at least one segment created to use this feature.</span></span> <span data-ttu-id="32921-106">Lehendik dagoen segmentu baten irizpideak zabaltzeak segmentu horren antzekoak diren bezeroak aurkitzen laguntzen du.</span><span class="sxs-lookup"><span data-stu-id="32921-106">Expanding the criteria of an existing segment help find customers that are similar to that segment.</span></span>

> [!NOTE]
> <span data-ttu-id="32921-107">*Aurkitu antzeko bezeroak* Datu horietan oinarritutako datuak ebaluatzeko eta iragarpenak egiteko bitarteko automatizatuak erabiltzen ditu eta, beraz, profil metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Erregelamendu Orokorrak ("DBAO") definitzen baitu.</span><span class="sxs-lookup"><span data-stu-id="32921-107">*Find similar customers* uses automated means to evaluate data and make predictions based on that data, and therefore has the capability to be used as a method of profiling, as that term is defined by the General Data Protection Regulation (“GDPR”).</span></span> <span data-ttu-id="32921-108">Bezeroak funtzio hau erabiltzeko datuak prozesatzeko DBAO edo beste lege edo arau batzuen menpe egon daiteke.</span><span class="sxs-lookup"><span data-stu-id="32921-108">Customer’s use of this feature to process data may be subject to GDPR or other laws or regulations.</span></span> <span data-ttu-id="32921-109">Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, iragarpenez aplikagarriak diren lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.</span><span class="sxs-lookup"><span data-stu-id="32921-109">You are responsible for ensuring that your use of Dynamics 365 Customer Insights, including predictions, complies with all applicable laws and regulations, including laws related to privacy, personal data, biometric data, data protection, and confidentiality of communications.</span></span>

## <a name="finding-similar-customers"></a><span data-ttu-id="32921-110">Antzeko bezeroak aurkitzea</span><span class="sxs-lookup"><span data-stu-id="32921-110">Finding similar customers</span></span>

1. <span data-ttu-id="32921-111">Hartzaileen xehetasunetan, joan **Segmentuak** atalera eta hautatu segmentu berrirako oinarritzat hartu nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="32921-111">In audience insights, go to **Segments** and select the segment you want to base your new segment on.</span></span> <span data-ttu-id="32921-112">Hori da zurea *iturriaren segmentua*.</span><span class="sxs-lookup"><span data-stu-id="32921-112">That's your *source segment*.</span></span>

1. <span data-ttu-id="32921-113">Ekintza-barran, hautatu **Aurkitu antzeko bezeroak**.</span><span class="sxs-lookup"><span data-stu-id="32921-113">In the action bar, select **Find similar customers**.</span></span>

1. <span data-ttu-id="32921-114">Berrikusi zure segmentu berrirako iradokitako izena eta aldatu behar izanez gero.</span><span class="sxs-lookup"><span data-stu-id="32921-114">Review the suggested name for your new segment and change it if necessary.</span></span>

1. <span data-ttu-id="32921-115">Berrikusi zure segmentu berria definitzen duten eremuak.</span><span class="sxs-lookup"><span data-stu-id="32921-115">Review the fields that define your new segment.</span></span> <span data-ttu-id="32921-116">Eremu hauek zehazten dute sistemaren oinarria zure bezero iturriaren antzeko bezeroak bilatzen saiatuko dela.</span><span class="sxs-lookup"><span data-stu-id="32921-116">These fields define the basis on which the system will try to find similar customers to your source segment.</span></span> <span data-ttu-id="32921-117">Sistemak gomendatutako eremuak aukeratuko ditu lehenespenez.</span><span class="sxs-lookup"><span data-stu-id="32921-117">The system will select recommended fields by default.</span></span>
  <span data-ttu-id="32921-118">Ereduaren errendimendua nabarmen murrizteko eremuak automatikoki baztertzen dira:</span><span class="sxs-lookup"><span data-stu-id="32921-118">Fields that can significantly reduce the model performance are automatically excluded:</span></span>
  
   - <span data-ttu-id="32921-119">Datu mota hauek dituzten eremuak: StringType, BooleanType, CharType, LongType, IntType, DoubleType, FloatType, ShortType</span><span class="sxs-lookup"><span data-stu-id="32921-119">Fields with the following data types: StringType, BooleanType, CharType, LongType, IntType, DoubleType, FloatType, ShortType</span></span>
   - <span data-ttu-id="32921-120">2 edo 30 baino gutxiagoko kardinalitatea (eremu bateko elementu kopurua) duten eremuak</span><span class="sxs-lookup"><span data-stu-id="32921-120">Fields with a cardinality (the number of elements in a field) of less than 2 or more than 30</span></span>

1. <span data-ttu-id="32921-121">Aukeratu barneratu nahi baduzu **Bezero guztiak** edo bezeroak bakarrik **Lehendik dagoen segmentu espezifikoa** zure segmentu berrian.</span><span class="sxs-lookup"><span data-stu-id="32921-121">Choose if you want to include **All customers** or only customers in a **Specific existing segment** in your new segment.</span></span>

1. <span data-ttu-id="32921-122">Baztertu zure iturburuko segmentuko bezeroak aukeratuz **Baztertu iturri-segmentuko denak** laukia.</span><span class="sxs-lookup"><span data-stu-id="32921-122">Exclude customers in your source segment by selecting the **Exclude everyone in source segment** checkbox.</span></span>

1. <span data-ttu-id="32921-123">Berez, sistemak iradokitzen du zure irteeran xede-audientziaren tamainaren % 20 soilik sartzea.</span><span class="sxs-lookup"><span data-stu-id="32921-123">By default, the system suggests including only 20% of the target audience size in your output.</span></span> <span data-ttu-id="32921-124">Editatu atalasea behar den moduan.</span><span class="sxs-lookup"><span data-stu-id="32921-124">Edit this threshold as needed.</span></span> <span data-ttu-id="32921-125">Atalasea handitzeak zehaztasuna murriztuko du.</span><span class="sxs-lookup"><span data-stu-id="32921-125">Increasing the threshold will reduce the precision.</span></span>

1. <span data-ttu-id="32921-126">Aukeratu **Exekutatu** orriaren behealdean sailkapen binarioko zeregin bat hasteko (Ikaskuntza automatiko metodo bat) datu multzoa aztertzen duena.</span><span class="sxs-lookup"><span data-stu-id="32921-126">Select **Run** at the bottom of the page to start a binary classification task (a method of machine learning) which analyzes the dataset.</span></span>

## <a name="view-the-similar-segment"></a><span data-ttu-id="32921-127">Ikusi antzeko segmentua</span><span class="sxs-lookup"><span data-stu-id="32921-127">View the similar segment</span></span>

<span data-ttu-id="32921-128">Antzeko segmentua prozesatu ondoren, zerrendan agertzen den segmentu berria aurkituko duzu **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="32921-128">After processing the similar segment, you'll find the new segment listed on the **Segments** page.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="32921-129">![Antzeko bezeroen segmentua](media/expanded-segment.png "Antzeko bezeroen segmentua")</span><span class="sxs-lookup"><span data-stu-id="32921-129">![Similar customers segment](media/expanded-segment.png "Similar customers segment")</span></span>

<span data-ttu-id="32921-130">Aukeratu **ikusi** segmentuko xehetasunak irekitzeko ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="32921-130">Select **View** in the action bar to open the segment detail.</span></span> <span data-ttu-id="32921-131">Ikuspegi honek emaitzen banaketaren inguruko informazioa jasotzen du [antzekotasun puntuazioak](#about-similarity-scores).</span><span class="sxs-lookup"><span data-stu-id="32921-131">This view contains information about the result distribution across [similarity scores](#about-similarity-scores).</span></span> <span data-ttu-id="32921-132">Antzekotasun puntuazioaren balioak ere aurkituko dituzu **Segmentuko kideen aurrebista**.</span><span class="sxs-lookup"><span data-stu-id="32921-132">You'll also find the similarity score values in the **Segment members preview**.</span></span>

## <a name="use-the-output-of-a-similar-segment"></a><span data-ttu-id="32921-133">Erabili antzeko segmentu baten irteera</span><span class="sxs-lookup"><span data-stu-id="32921-133">Use the output of a similar segment</span></span>

<span data-ttu-id="32921-134">Ahal duzu [antzeko segmentu baten irteerarekin lan egin](segments.md) beste segmentuekin egiten duzun bezala.</span><span class="sxs-lookup"><span data-stu-id="32921-134">You can [work with the output of a similar segment](segments.md) as you do with other segments.</span></span> <span data-ttu-id="32921-135">Adibidez, esportatu segmentua edo neurri bat eraiki.</span><span class="sxs-lookup"><span data-stu-id="32921-135">For example, export the segment or build a measure.</span></span>

## <a name="refresh-and-edit-a-similar-segment"></a><span data-ttu-id="32921-136">Eguneratu antzeko segmentua eta editatu</span><span class="sxs-lookup"><span data-stu-id="32921-136">Refresh and edit a similar segment</span></span>

<span data-ttu-id="32921-137">Antzeko segmentua freskatzeko, hautatu botoian **segmentuak** orria eta hautatu **Freskatu** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="32921-137">To refresh a similar segment, select it on the **Segments** page and select **Refresh** in the action bar.</span></span>

<span data-ttu-id="32921-138">Antzeko segmentua editatzean zure datuak berriro prozesatuko dira.</span><span class="sxs-lookup"><span data-stu-id="32921-138">Editing a similar segment will reprocess your data.</span></span> <span data-ttu-id="32921-139">Aurretik sortutako segmentua eguneratutako datuekin eguneratzen da.</span><span class="sxs-lookup"><span data-stu-id="32921-139">The previously created segment gets updated with refreshed data.</span></span>    
<span data-ttu-id="32921-140">Antzeko segmentua editatzeko, hautatu botoian **segmentuak** orria eta hautatu **Editatu** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="32921-140">To edit a similar segment, select it on the **Segments** page and select **Edit** in the action bar.</span></span> <span data-ttu-id="32921-141">Aplikatu aldaketak eta hautatu **Exekutatu** prozesatzen hasteko.</span><span class="sxs-lookup"><span data-stu-id="32921-141">Apply your changes and select **Run** to start the processing.</span></span>

## <a name="delete-a-similar-segment"></a><span data-ttu-id="32921-142">Ezabatu antzeko segmentua</span><span class="sxs-lookup"><span data-stu-id="32921-142">Delete a similar segment</span></span>

<span data-ttu-id="32921-143">Hautatu segmentua **Segmentuak** orrian eta hautatu **Ezabatu** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="32921-143">Select the segment on the **Segments** page and select **Delete** in the action bar.</span></span> <span data-ttu-id="32921-144">Orduan baieztatu ezabatu nahi duzula.</span><span class="sxs-lookup"><span data-stu-id="32921-144">Then, confirm your deletion.</span></span>

## <a name="about-similarity-scores"></a><span data-ttu-id="32921-145">Antzekotasun puntuazioari buruz</span><span class="sxs-lookup"><span data-stu-id="32921-145">About similarity scores</span></span>

<span data-ttu-id="32921-146">Ikaskuntza automatiko eredu bitarren sailkapenak puntuazio bat ematen die antzeko segmentuko bezeroei.</span><span class="sxs-lookup"><span data-stu-id="32921-146">The binary classification machine learning model assigns a score to customers in the similar segment.</span></span> <span data-ttu-id="32921-147">Puntuazioa iturri-segmentuko bezeroek duten antzekotasunean oinarritzen da.</span><span class="sxs-lookup"><span data-stu-id="32921-147">The score is based on the similarity to customers in the source segment.</span></span>

- <span data-ttu-id="32921-148">Antzekotasun puntuazioak 0.55 azpitik daude sailkatutako sisteman *ez da antzekoa* iturri-segmentuko bezeroei</span><span class="sxs-lookup"><span data-stu-id="32921-148">Similarity scores below 0.55 are customers the system classified as *not similar* to customers in the source segment</span></span>
- <span data-ttu-id="32921-149">Antzekotasunaren puntuazioak 0.55 eta 0.7 artean sailkatzen dira *zertxobait antzeko*</span><span class="sxs-lookup"><span data-stu-id="32921-149">Similarity scores between 0.55 – 0.7 are classified as *somewhat similar*</span></span>
- <span data-ttu-id="32921-150">Antzekotasunaren puntuazioak 0.7 eta 0.85 artean sailkatzen dira *antzeko*</span><span class="sxs-lookup"><span data-stu-id="32921-150">Similarity scores between 0.7 – 0.85 are classified as *similar*</span></span>
- <span data-ttu-id="32921-151">Antzekotasun-puntuazioak 0.85 eta 1 artekoak dira *oso antzekoak*</span><span class="sxs-lookup"><span data-stu-id="32921-151">Similarity scores between 0.85 – 1 are customers the system classified as *very similar*</span></span>

<span data-ttu-id="32921-152">Ez dira ereduaren irteeraren barruan sartzen 0.4 azpitik dituzten antzekotasunak dituzten bezeroak.</span><span class="sxs-lookup"><span data-stu-id="32921-152">Customers with similarity scores below 0.4 aren't included in the model output.</span></span> <span data-ttu-id="32921-153">Sistemak ez ditu iturburu-segmentuaren antzekoak.</span><span class="sxs-lookup"><span data-stu-id="32921-153">The system doesn't consider them similar enough to the source segment.</span></span>
