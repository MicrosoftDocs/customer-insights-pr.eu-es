---
title: Helbidea hobetzeko aberastea
description: Aberastu eta normalizatu bezeroen profilen helbideen informazioa Microsoft-en ereduekin.
ms.date: 04/21/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-ms
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: e0ca731f944da9a7eaae7c2dc2d7568b6386089f
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305417"
---
# <a name="enrichment-of-customer-profiles-with-enhanced-addresses"></a><span data-ttu-id="c405e-103">Bezeroen profilak aberastu helbide hobetuekin</span><span class="sxs-lookup"><span data-stu-id="c405e-103">Enrichment of customer profiles with enhanced addresses</span></span>

<span data-ttu-id="c405e-104">Zure datuetako helbideak desegituratuak, osatugabeak edo okerrak izan daitezke.</span><span class="sxs-lookup"><span data-stu-id="c405e-104">Addresses in your data can be unstructured, incomplete, or incorrect.</span></span> <span data-ttu-id="c405e-105">Erabili Microsoft-en ereduak zure helbideak normalizatzeko eta aberasteko [Common Data Model formatua](/common-data-model/schema/core/applicationcommon/address) zehaztasun eta ikuspegi hobeak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="c405e-105">Use Microsoft's models to normalize and enrich your addresses into the [Common Data Model format](/common-data-model/schema/core/applicationcommon/address) for better accuracy and insights.</span></span>

## <a name="how-we-enhance-addresses"></a><span data-ttu-id="c405e-106">Helbideak nola hobetzen ditugun</span><span class="sxs-lookup"><span data-stu-id="c405e-106">How we enhance addresses</span></span>

<span data-ttu-id="c405e-107">Gure ereduak bi urratseko prozesua egiten du helbide bat hobetzeko.</span><span class="sxs-lookup"><span data-stu-id="c405e-107">Our model goes through a two-step process to enhance an address.</span></span> <span data-ttu-id="c405e-108">Lehenik eta behin, helbidea analizatzen du bere osagaiak identifikatzeko eta formatu egituratu batean jartzen ditu.</span><span class="sxs-lookup"><span data-stu-id="c405e-108">First, it parses the address to identify its components and puts them into a structured format.</span></span> <span data-ttu-id="c405e-109">Ondoren, AI erabiltzen dugu helbideko balioak zuzentzeko, osatzeko eta estandarizatzeko.</span><span class="sxs-lookup"><span data-stu-id="c405e-109">Then, we use AI to correct, complete, and standardize the values in the address.</span></span>

### <a name="example"></a><span data-ttu-id="c405e-110">Adibidez</span><span class="sxs-lookup"><span data-stu-id="c405e-110">Example</span></span>

<span data-ttu-id="c405e-111">Baliteke helbideen informazioa formatu estandarra izatea eta akats ortografikoak izatea.</span><span class="sxs-lookup"><span data-stu-id="c405e-111">Address information might be in a nonstandard format and contain spelling errors.</span></span> <span data-ttu-id="c405e-112">Ereduak arazo horiek konpon ditzake eta helbide koherenteak sor ditzake bezeroen profil bateratuetan.</span><span class="sxs-lookup"><span data-stu-id="c405e-112">The model can fix these issues and create consistent addresses in unified customer profiles.</span></span>

```Input
4567 w main stret californa missouri 54321 us
```

```Output
- Street1: 4567 W Main St
- City: California
- StateOrProvince: MO
- ZipOrPostalCode: 54321
- CountryOrRegion: United States of America

- Address: 4567 W Main St, California, MO, 54321, United States of America
```

### <a name="limitations"></a><span data-ttu-id="c405e-113">Murriztapenak</span><span class="sxs-lookup"><span data-stu-id="c405e-113">Limitations</span></span>

<span data-ttu-id="c405e-114">Helbide hobetuak sartutako helbide datuetan dauden balioekin bakarrik funtzionatzen du.</span><span class="sxs-lookup"><span data-stu-id="c405e-114">Enhanced addresses only works with the values that already exist in your ingested address data.</span></span> <span data-ttu-id="c405e-115">Ereduak ez du:</span><span class="sxs-lookup"><span data-stu-id="c405e-115">The model doesn't:</span></span> 

1. <span data-ttu-id="c405e-116">Egiaztatu helbidea baliozko helbidea den.</span><span class="sxs-lookup"><span data-stu-id="c405e-116">Verify if the address is a valid address.</span></span>
2. <span data-ttu-id="c405e-117">Egiaztatu balioetako bat, hala nola, posta-kodeak edo kaleen izenak, baliozkoak diren.</span><span class="sxs-lookup"><span data-stu-id="c405e-117">Verify if any of the values, such as ZIP codes or street names, are valid.</span></span>
3. <span data-ttu-id="c405e-118">Aldatu ezagutzen ez dituen balioak.</span><span class="sxs-lookup"><span data-stu-id="c405e-118">Change values it doesn't recognize.</span></span>

<span data-ttu-id="c405e-119">Ereduak automatikoki ikasten oinarritutako teknikak erabiltzen ditu helbideak hobetzeko.</span><span class="sxs-lookup"><span data-stu-id="c405e-119">The model uses machine learning-based techniques to enhance addresses.</span></span> <span data-ttu-id="c405e-120">Ereduak sarrerako balioa aldatzen duenerako konfiantza atalase handia aplikatzen dugun bitartean, ikaskuntzan oinarritutako edozein eredurekin gertatzen den moduan, ez da ehuneko 100eko zehaztasuna bermatzen.</span><span class="sxs-lookup"><span data-stu-id="c405e-120">While we apply a high confidence threshold for when the model changes an input value, as with any machine learning-based model, 100 percent accuracy is not guaranteed.</span></span>

## <a name="supported-countries-or-regions"></a><span data-ttu-id="c405e-121">Lagundutako herrialdeak edo eskualdeak</span><span class="sxs-lookup"><span data-stu-id="c405e-121">Supported countries or regions</span></span>

<span data-ttu-id="c405e-122">Gaur egun herrialde edo eskualde hauetan helbide aberasgarriak onartzen ditugu:</span><span class="sxs-lookup"><span data-stu-id="c405e-122">We currently support enriching addresses in these countries or regions:</span></span> 

- <span data-ttu-id="c405e-123">Australia</span><span class="sxs-lookup"><span data-stu-id="c405e-123">Australia</span></span>
- <span data-ttu-id="c405e-124">Kanada</span><span class="sxs-lookup"><span data-stu-id="c405e-124">Canada</span></span>
- <span data-ttu-id="c405e-125">Erresuma Batua</span><span class="sxs-lookup"><span data-stu-id="c405e-125">United Kingdom</span></span>
- <span data-ttu-id="c405e-126">Estatu Batuak</span><span class="sxs-lookup"><span data-stu-id="c405e-126">United States</span></span>

<span data-ttu-id="c405e-127">Helbideek herrialde edo eskualde balioa izan behar dute.</span><span class="sxs-lookup"><span data-stu-id="c405e-127">Addresses must contain a country/region value.</span></span> <span data-ttu-id="c405e-128">Ez dugu prozesatzen onartzen ez diren herrialde edo eskualdeen helbiderik eta herrialderik edo eskualderik eman ez duten helbiderik.</span><span class="sxs-lookup"><span data-stu-id="c405e-128">We don't process addresses for countries or regions that aren't supported and addresses that have no country or region provided.</span></span>

## <a name="configure-the-enrichment"></a><span data-ttu-id="c405e-129">Konfiguratu aberastea</span><span class="sxs-lookup"><span data-stu-id="c405e-129">Configure the enrichment</span></span>

1. <span data-ttu-id="c405e-130">Joan **Datuak** > **Aberastua**.</span><span class="sxs-lookup"><span data-stu-id="c405e-130">Go to **Data** > **Enrichment**.</span></span>

1. <span data-ttu-id="c405e-131">Aukeratu **Aberastu nire datuak** **Helbide hobetuak** lauzan.</span><span class="sxs-lookup"><span data-stu-id="c405e-131">Select **Enrich my data** on the **Enhanced addresses** tile.</span></span>

   :::image type="content" source="media/enhanced-addresses-tile.png" alt-text="Helbide hobetuen fitxaren pantaila-argazkia.":::

1. <span data-ttu-id="c405e-133">Aukeratu **Bezeroen datu multzoa** eta aukeratu aberastu nahi dituzun helbideak dituen entitatea.</span><span class="sxs-lookup"><span data-stu-id="c405e-133">Select the **Customer data set** and choose the entity containing the addresses you want to enrich.</span></span> <span data-ttu-id="c405e-134">Aukeratu dezakezu *Bezeroa* entitateak helbideak aberastu ditzan zure bezeroen profil guztietan edo hautatu segmentu bat entitateak helbideak segmentu horretan dauden bezeroen profiletan soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="c405e-134">You can select the *Customer* entity to enrich addresses in all your customer profiles or select a segment entity to enrich addresses only in customer profiles contained in that segment.</span></span>

1. <span data-ttu-id="c405e-135">Hautatu zein formatu eman datu multzoetako helbideei.</span><span class="sxs-lookup"><span data-stu-id="c405e-135">Select how addresses are formatted in your data set.</span></span> <span data-ttu-id="c405e-136">Aukeratu **Atributu bakarreko helbidea** zure datuetako helbideek eremu bakarra erabiltzen badute.</span><span class="sxs-lookup"><span data-stu-id="c405e-136">Choose **Single-attribute address** if addresses in your data use a single field.</span></span> <span data-ttu-id="c405e-137">Aukeratu **Hainbat atributuko helbidea** zure datuetako helbideek eremu bat edo gehiago erabiltzen badituzte.</span><span class="sxs-lookup"><span data-stu-id="c405e-137">Choose **Multiple-attribute address** if addresses in your data use more than one data field.</span></span>

   > [!NOTE]
   > <span data-ttu-id="c405e-138">Herrialde / eskualdea derrigorrezkoa da atributu bakarreko eta atributu anitzeko helbideetan.</span><span class="sxs-lookup"><span data-stu-id="c405e-138">Country/Region is mandatory in both single-attribute and multiple-attribute addresses.</span></span> <span data-ttu-id="c405e-139">Herrialde edo eskualde balio baliodunak edo onartuak ez dituzten helbideak ez dira aberastuko.</span><span class="sxs-lookup"><span data-stu-id="c405e-139">Addresses that don't contain valid or supported country/region values won't be enriched.</span></span>

1.  <span data-ttu-id="c405e-140">Esleitu helbide eremuak zure bezero entitate bateratuarekin.</span><span class="sxs-lookup"><span data-stu-id="c405e-140">Map the address fields from your unified customer entity.</span></span>

    :::image type="content" source="media/enhanced-address-mapping.png" alt-text="Helbide hobetuen eremuak esleitzeko orria.":::

1. <span data-ttu-id="c405e-142">Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.</span><span class="sxs-lookup"><span data-stu-id="c405e-142">Select **Next** to complete the field mapping.</span></span>

1. <span data-ttu-id="c405e-143">Hornitu aberastearen izena eta irteerako entitatearen izena.</span><span class="sxs-lookup"><span data-stu-id="c405e-143">Provide a name for the enrichment and the output entity.</span></span>

1. <span data-ttu-id="c405e-144">Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.</span><span class="sxs-lookup"><span data-stu-id="c405e-144">Select **Save enrichment** after reviewing your choices.</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="c405e-145">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="c405e-145">Enrichment results</span></span>

<span data-ttu-id="c405e-146">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="c405e-146">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="c405e-147">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="c405e-147">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="c405e-148">Prozesatzeko denbora zure bezeroen datuen tamainaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="c405e-148">The processing time depends on the size of your customer data.</span></span>

<span data-ttu-id="c405e-149">Aberasteko prozesua amaitu ondoren, aberastu berri diren bezeroen profilen datuak berrikus ditzakezu atalean **Nire aberastasunak**.</span><span class="sxs-lookup"><span data-stu-id="c405e-149">After the enrichment process completes, you can review the newly enriched customer profiles data under **My enrichments**.</span></span> <span data-ttu-id="c405e-150">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="c405e-150">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="c405e-151">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="c405e-151">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c405e-152">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="c405e-152">Next steps</span></span>

<span data-ttu-id="c405e-153">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="c405e-153">Build on top of your enriched customer data.</span></span> <span data-ttu-id="c405e-154">Sortu [segmentuak](segments.md) eta [neurriak](measures.md), eta are [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="c405e-154">Create [segments](segments.md) and [measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
