---
title: Bilatu antzeko bezeroak adimen artifizialarekin
description: Aurkitu antzeko bezeroen segmentuak adimen artifizialarekin.
ms.date: 06/25/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: f588f45ed11efffbb335003642a4b92810153017
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596760"
---
# <a name="similar-customers-preview"></a><span data-ttu-id="1a5dc-103">Bezero antzekoak (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="1a5dc-103">Similar Customers (preview)</span></span>

<span data-ttu-id="1a5dc-104">Ezaugarri honek adimen artifiziala erabiliz zure bezero basean antzeko bezeroak topa ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-104">This feature lets you find similar customers in your customer base using artificial intelligence.</span></span> <span data-ttu-id="1a5dc-105">Ezaugarri hau erabiltzeko gutxienez segmentu bat sortu behar duzu.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-105">You need to have at least one segment created to use this feature.</span></span> <span data-ttu-id="1a5dc-106">Lehendik dagoen segmentu baten irizpideak zabaltzeak segmentu horren antzekoak diren bezeroak aurkitzen laguntzen du.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-106">Expanding the criteria of an existing segment help find customers that are similar to that segment.</span></span>

> [!NOTE]
> <span data-ttu-id="1a5dc-107">*Aurkitu antzeko bezeroak* Datu horietan oinarritutako datuak ebaluatzeko eta iragarpenak egiteko bitarteko automatizatuak erabiltzen ditu eta, beraz, profil metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Erregelamendu Orokorrak ("DBAO") definitzen baitu.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-107">*Find similar customers* uses automated means to evaluate data and make predictions based on that data, and therefore has the capability to be used as a method of profiling, as that term is defined by the General Data Protection Regulation (“GDPR”).</span></span> <span data-ttu-id="1a5dc-108">Bezeroak funtzio hau erabiltzeko datuak prozesatzeko DBAO edo beste lege edo arau batzuen menpe egon daiteke.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-108">Customer’s use of this feature to process data may be subject to GDPR or other laws or regulations.</span></span> <span data-ttu-id="1a5dc-109">Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, iragarpenez aplikagarriak diren lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-109">You are responsible for ensuring that your use of Dynamics 365 Customer Insights, including predictions, complies with all applicable laws and regulations, including laws related to privacy, personal data, biometric data, data protection, and confidentiality of communications.</span></span>

## <a name="finding-similar-customers"></a><span data-ttu-id="1a5dc-110">Antzeko bezeroak aurkitzea</span><span class="sxs-lookup"><span data-stu-id="1a5dc-110">Finding similar customers</span></span>

1. <span data-ttu-id="1a5dc-111">Hartzaileen xehetasunetan, joan **Segmentuak** atalera eta hautatu segmentu berrirako oinarritzat hartu nahi duzun segmentua.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-111">In audience insights, go to **Segments** and select the segment you want to base your new segment on.</span></span> <span data-ttu-id="1a5dc-112">Hori da zurea *iturriaren segmentua*.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-112">That's your *source segment*.</span></span>

1. <span data-ttu-id="1a5dc-113">Ekintza-barran, hautatu **Aurkitu antzeko bezeroak**.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-113">In the action bar, select **Find similar customers**.</span></span>

1. <span data-ttu-id="1a5dc-114">Berrikusi zure segmentu berrirako iradokitako izena eta aldatu behar izanez gero.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-114">Review the suggested name for your new segment and change it if necessary.</span></span>

1. <span data-ttu-id="1a5dc-115">Berrikusi zure segmentu berria definitzen duten eremuak.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-115">Review the fields that define your new segment.</span></span> <span data-ttu-id="1a5dc-116">Eremu hauek zehazten dute sistemaren oinarria zure bezero iturriaren antzeko bezeroak bilatzen saiatuko dela.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-116">These fields define the basis on which the system will try to find similar customers to your source segment.</span></span> <span data-ttu-id="1a5dc-117">Sistemak gomendatutako eremuak aukeratuko ditu lehenespenez.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-117">The system will select recommended fields by default.</span></span>
  <span data-ttu-id="1a5dc-118">Ereduaren errendimendua nabarmen murrizteko eremuak automatikoki baztertzen dira:</span><span class="sxs-lookup"><span data-stu-id="1a5dc-118">Fields that can significantly reduce the model performance are automatically excluded:</span></span>
  
   - <span data-ttu-id="1a5dc-119">Datu mota hauek dituzten eremuak: StringType, BooleanType, CharType, LongType, IntType, DoubleType, FloatType, ShortType</span><span class="sxs-lookup"><span data-stu-id="1a5dc-119">Fields with the following data types: StringType, BooleanType, CharType, LongType, IntType, DoubleType, FloatType, ShortType</span></span>
   - <span data-ttu-id="1a5dc-120">2 edo 30 baino gutxiagoko kardinalitatea (eremu bateko elementu kopurua) duten eremuak</span><span class="sxs-lookup"><span data-stu-id="1a5dc-120">Fields with a cardinality (the number of elements in a field) of less than 2 or more than 30</span></span>

1. <span data-ttu-id="1a5dc-121">Aukeratu barneratu nahi baduzu **Bezero guztiak** edo bezeroak bakarrik **Lehendik dagoen segmentu espezifikoa** zure segmentu berrian.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-121">Choose if you want to include **All customers** or only customers in a **Specific existing segment** in your new segment.</span></span>

1. <span data-ttu-id="1a5dc-122">Baztertu zure iturburuko segmentuko bezeroak aukeratuz **Baztertu iturri-segmentuko denak** laukia.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-122">Exclude customers in your source segment by selecting the **Exclude everyone in source segment** checkbox.</span></span>

1. <span data-ttu-id="1a5dc-123">Berez, sistemak iradokitzen du zure irteeran xede-audientziaren tamainaren % 20 soilik sartzea.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-123">By default, the system suggests including only 20% of the target audience size in your output.</span></span> <span data-ttu-id="1a5dc-124">Editatu atalasea behar den moduan.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-124">Edit this threshold as needed.</span></span> <span data-ttu-id="1a5dc-125">Atalasea handitzeak zehaztasuna murriztuko du.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-125">Increasing the threshold will reduce the precision.</span></span>

1. <span data-ttu-id="1a5dc-126">Aukeratu **Exekutatu** orriaren behealdean sailkapen binarioko zeregin bat hasteko (Ikaskuntza automatiko metodo bat) datu multzoa aztertzen duena.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-126">Select **Run** at the bottom of the page to start a binary classification task (a method of machine learning) which analyzes the dataset.</span></span>

## <a name="view-the-similar-segment"></a><span data-ttu-id="1a5dc-127">Ikusi antzeko segmentua</span><span class="sxs-lookup"><span data-stu-id="1a5dc-127">View the similar segment</span></span>

<span data-ttu-id="1a5dc-128">Antzeko segmentua prozesatu ondoren, zerrendan agertzen den segmentu berria aurkituko duzu **segmentuak** orria.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-128">After processing the similar segment, you'll find the new segment listed on the **Segments** page.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="1a5dc-129">![Antzeko bezeroen segmentua](media/expanded-segment.png "Antzeko bezeroen segmentua")</span><span class="sxs-lookup"><span data-stu-id="1a5dc-129">![Similar customers segment](media/expanded-segment.png "Similar customers segment")</span></span>

<span data-ttu-id="1a5dc-130">Aukeratu **ikusi** segmentuko xehetasunak irekitzeko ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-130">Select **View** in the action bar to open the segment detail.</span></span> <span data-ttu-id="1a5dc-131">Ikuspegi honek emaitzen banaketaren inguruko informazioa jasotzen du [antzekotasun puntuazioak](#about-similarity-scores).</span><span class="sxs-lookup"><span data-stu-id="1a5dc-131">This view contains information about the result distribution across [similarity scores](#about-similarity-scores).</span></span> <span data-ttu-id="1a5dc-132">Antzekotasun puntuazioaren balioak ere aurkituko dituzu **Segmentuko kideen aurrebista**.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-132">You'll also find the similarity score values in the **Segment members preview**.</span></span>

## <a name="use-the-output-of-a-similar-segment"></a><span data-ttu-id="1a5dc-133">Erabili antzeko segmentu baten irteera</span><span class="sxs-lookup"><span data-stu-id="1a5dc-133">Use the output of a similar segment</span></span>

<span data-ttu-id="1a5dc-134">Ahal duzu [antzeko segmentu baten irteerarekin lan egin](segments.md) beste segmentuekin egiten duzun bezala.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-134">You can [work with the output of a similar segment](segments.md) as you do with other segments.</span></span> <span data-ttu-id="1a5dc-135">Adibidez, esportatu segmentua edo neurri bat eraiki.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-135">For example, export the segment or build a measure.</span></span>

## <a name="refresh-and-edit-a-similar-segment"></a><span data-ttu-id="1a5dc-136">Eguneratu antzeko segmentua eta editatu</span><span class="sxs-lookup"><span data-stu-id="1a5dc-136">Refresh and edit a similar segment</span></span>

<span data-ttu-id="1a5dc-137">Antzeko segmentua freskatzeko, hautatu botoian **segmentuak** orria eta hautatu **Freskatu** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-137">To refresh a similar segment, select it on the **Segments** page and select **Refresh** in the action bar.</span></span>

<span data-ttu-id="1a5dc-138">Antzeko segmentua editatzean zure datuak berriro prozesatuko dira.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-138">Editing a similar segment will reprocess your data.</span></span> <span data-ttu-id="1a5dc-139">Aurretik sortutako segmentua eguneratutako datuekin eguneratzen da.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-139">The previously created segment gets updated with refreshed data.</span></span>    
<span data-ttu-id="1a5dc-140">Antzeko segmentua editatzeko, hautatu botoian **segmentuak** orria eta hautatu **Editatu** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-140">To edit a similar segment, select it on the **Segments** page and select **Edit** in the action bar.</span></span> <span data-ttu-id="1a5dc-141">Aplikatu aldaketak eta hautatu **Exekutatu** prozesatzen hasteko.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-141">Apply your changes and select **Run** to start the processing.</span></span>

## <a name="delete-a-similar-segment"></a><span data-ttu-id="1a5dc-142">Ezabatu antzeko segmentua</span><span class="sxs-lookup"><span data-stu-id="1a5dc-142">Delete a similar segment</span></span>

<span data-ttu-id="1a5dc-143">Hautatu segmentua **Segmentuak** orrian eta hautatu **Ezabatu** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-143">Select the segment on the **Segments** page and select **Delete** in the action bar.</span></span> <span data-ttu-id="1a5dc-144">Orduan baieztatu ezabatu nahi duzula.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-144">Then, confirm your deletion.</span></span>

## <a name="about-similarity-scores"></a><span data-ttu-id="1a5dc-145">Antzekotasun puntuazioari buruz</span><span class="sxs-lookup"><span data-stu-id="1a5dc-145">About similarity scores</span></span>

<span data-ttu-id="1a5dc-146">Ikaskuntza automatiko eredu bitarren sailkapenak puntuazio bat ematen die antzeko segmentuko bezeroei.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-146">The binary classification machine learning model assigns a score to customers in the similar segment.</span></span> <span data-ttu-id="1a5dc-147">Puntuazioa iturri-segmentuko bezeroek duten antzekotasunean oinarritzen da.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-147">The score is based on the similarity to customers in the source segment.</span></span>

- <span data-ttu-id="1a5dc-148">Antzekotasun puntuazioak 0.55 azpitik daude sailkatutako sisteman *ez da antzekoa* iturri-segmentuko bezeroei</span><span class="sxs-lookup"><span data-stu-id="1a5dc-148">Similarity scores below 0.55 are customers the system classified as *not similar* to customers in the source segment</span></span>
- <span data-ttu-id="1a5dc-149">Antzekotasunaren puntuazioak 0.55 eta 0.7 artean sailkatzen dira *zertxobait antzeko*</span><span class="sxs-lookup"><span data-stu-id="1a5dc-149">Similarity scores between 0.55 – 0.7 are classified as *somewhat similar*</span></span>
- <span data-ttu-id="1a5dc-150">Antzekotasunaren puntuazioak 0.7 eta 0.85 artean sailkatzen dira *antzeko*</span><span class="sxs-lookup"><span data-stu-id="1a5dc-150">Similarity scores between 0.7 – 0.85 are classified as *similar*</span></span>
- <span data-ttu-id="1a5dc-151">Antzekotasun-puntuazioak 0.85 eta 1 artekoak dira *oso antzekoak*</span><span class="sxs-lookup"><span data-stu-id="1a5dc-151">Similarity scores between 0.85 – 1 are customers the system classified as *very similar*</span></span>

<span data-ttu-id="1a5dc-152">Ez dira ereduaren irteeraren barruan sartzen 0.4 azpitik dituzten antzekotasunak dituzten bezeroak.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-152">Customers with similarity scores below 0.4 aren't included in the model output.</span></span> <span data-ttu-id="1a5dc-153">Sistemak ez ditu iturburu-segmentuaren antzekoak.</span><span class="sxs-lookup"><span data-stu-id="1a5dc-153">The system doesn't consider them similar enough to the source segment.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]