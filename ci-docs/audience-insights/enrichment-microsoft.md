---
title: Aberastu bezeroen profilak Microsoften datuekin
description: Erabili Microsoft-en jabedun datuak bezeroen datuak marka eta interes kidetasunekin aberasteko.
ms.date: 06/14/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-MS
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: e92360bb886739cfe477ce1d2eb62219228a0292
ms.sourcegitcommit: d4b4053f6ee8f60f1a214982c4726c9de84615ef
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/14/2021
ms.locfileid: "6245692"
---
# <a name="enrich-customer-profiles-with-brand-and-interest-affinities-preview"></a><span data-ttu-id="44285-103">Aberastu bezeroen profilak marka eta interes kidetasunekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="44285-103">Enrich customer profiles with brand and interest affinities (preview)</span></span>

<span data-ttu-id="44285-104">Erabili Microsoft-en jabedun datuak bezeroen datuak marka eta interes kidetasunekin aberasteko.</span><span class="sxs-lookup"><span data-stu-id="44285-104">Use Microsoft's proprietary data to enrich your customer data with brand and interest affinities.</span></span> <span data-ttu-id="44285-105">Afinitate horiek zure bezeroen antzeko demografia duten pertsonen datuetan oinarrituta zehazten dira.</span><span class="sxs-lookup"><span data-stu-id="44285-105">These affinities are determined based on data from people with similar demographics to your customers.</span></span> <span data-ttu-id="44285-106">Informazio honek bezeroak hobeto ulertzen eta segmentatzen laguntzen du, marka eta interes jakin batzuen arabera.</span><span class="sxs-lookup"><span data-stu-id="44285-106">This information helps you to better understand and segment your customers based on their affinities to specific brands and interests.</span></span>

<span data-ttu-id="44285-107">Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** [aberasteak konfiguratu eta ikusteko](enrichment-hub.md).</span><span class="sxs-lookup"><span data-stu-id="44285-107">In audience insights, go to **Data** > **Enrichment** to [configure and view enrichments](enrichment-hub.md).</span></span>

<span data-ttu-id="44285-108">Marka afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Markak** teila.</span><span class="sxs-lookup"><span data-stu-id="44285-108">To configure brand affinities enrichment, go to the **Discover** tab and select **Enrich my data** on the **Brands** tile.</span></span>

<span data-ttu-id="44285-109">Interes afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Interesak** teila.</span><span class="sxs-lookup"><span data-stu-id="44285-109">To configure interest affinities enrichment, go to the **Discover** tab and select **Enrich my data** on the **Interests** tile.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="44285-110">![Markak eta interesen lauzak](media/BrandsInterest-tile-Hub.png "Markak eta interesaren lauzak")</span><span class="sxs-lookup"><span data-stu-id="44285-110">![Brands & Interests tiles](media/BrandsInterest-tile-Hub.png "Brands & Interest tiles")</span></span>

## <a name="how-we-determine-affinities"></a><span data-ttu-id="44285-111">Afinitateak nola zehazten ditugun</span><span class="sxs-lookup"><span data-stu-id="44285-111">How we determine affinities</span></span>

<span data-ttu-id="44285-112">Microsoften lineako bilaketa-datuak erabiltzen ditugu marka eta interesen arteko afinitateak aurkitzeko hainbat segmentu demografikotan (adinaren, generoaren edo kokapenaren arabera definituak).</span><span class="sxs-lookup"><span data-stu-id="44285-112">We use Microsoft’s online search data to find affinities for brands and interests across various demographic segments (defined by age, gender, or location).</span></span> <span data-ttu-id="44285-113">Marka edo interes baten bilaketa-bolumenak zehazten du zein den afinitate batek segmentu demografiko batek, beste segmentu batzuekin alderatuta, marka edo interes hori.</span><span class="sxs-lookup"><span data-stu-id="44285-113">The online search volume for a brand or interest determines how much affinity a demographic segment, compared to other segments, has to that brand or interest.</span></span>

## <a name="affinity-level-and-score"></a><span data-ttu-id="44285-114">Afinitate-maila eta puntuazioa</span><span class="sxs-lookup"><span data-stu-id="44285-114">Affinity level and score</span></span>

<span data-ttu-id="44285-115">Bezeroen profil aberastu guztietan, erlazionatutako bi balio ematen ditugu: afinitate-maila eta afinitate-puntuazioa.</span><span class="sxs-lookup"><span data-stu-id="44285-115">On every enriched customer profile, we provide two related values – affinity level and affinity score.</span></span> <span data-ttu-id="44285-116">Balio horiei esker, profil horren segmentu demografikoarekiko, marka edo interesekiko, beste segmentu demografiko batzuekiko duten afinitatea zehazten lagunduko dizute.</span><span class="sxs-lookup"><span data-stu-id="44285-116">These values help you determine how strong the affinity is for that profile’s demographic segment, for a brand or interest, as compared to other demographic segments.</span></span>

<span data-ttu-id="44285-117">*Afinitate-maila* lau maila ditu eta *afinitate puntuazioa* afinitate mailetara esleitzen den 100 puntuko eskalan kalkulatzen da.</span><span class="sxs-lookup"><span data-stu-id="44285-117">*Affinity level* consists of four levels and *affinity score* is calculated on a 100-point scale that maps to the affinity levels.</span></span>


|<span data-ttu-id="44285-118">Afinitate-maila</span><span class="sxs-lookup"><span data-stu-id="44285-118">Affinity level</span></span> |<span data-ttu-id="44285-119">Afinitate-puntuazioa</span><span class="sxs-lookup"><span data-stu-id="44285-119">Affinity score</span></span>  |
|---------|---------|
|<span data-ttu-id="44285-120">Oso handia</span><span class="sxs-lookup"><span data-stu-id="44285-120">Very high</span></span>     | <span data-ttu-id="44285-121">85-100</span><span class="sxs-lookup"><span data-stu-id="44285-121">85-100</span></span>       |
|<span data-ttu-id="44285-122">Handia</span><span class="sxs-lookup"><span data-stu-id="44285-122">High</span></span>     | <span data-ttu-id="44285-123">70-84</span><span class="sxs-lookup"><span data-stu-id="44285-123">70-84</span></span>        |
|<span data-ttu-id="44285-124">Ertaina</span><span class="sxs-lookup"><span data-stu-id="44285-124">Medium</span></span>     | <span data-ttu-id="44285-125">35-69</span><span class="sxs-lookup"><span data-stu-id="44285-125">35-69</span></span>        |
|<span data-ttu-id="44285-126">Txikia</span><span class="sxs-lookup"><span data-stu-id="44285-126">Low</span></span>     | <span data-ttu-id="44285-127">1-34</span><span class="sxs-lookup"><span data-stu-id="44285-127">1-34</span></span>        |

<span data-ttu-id="44285-128">Afinitatea neurtzeko nahi duzun xehetasunen arabera, afinitate maila edo puntuazioa erabil dezakezu.</span><span class="sxs-lookup"><span data-stu-id="44285-128">Depending on the granularity you would like for measuring the affinity, you can use either affinity level or score.</span></span> <span data-ttu-id="44285-129">Afinitate-puntuazioak kontrol zehatzagoa ematen dizu.</span><span class="sxs-lookup"><span data-stu-id="44285-129">Affinity score gives you more precise control.</span></span>

## <a name="supported-countriesregions"></a><span data-ttu-id="44285-130">Lagundutako herrialde / eskualdeak</span><span class="sxs-lookup"><span data-stu-id="44285-130">Supported countries/regions</span></span>

<span data-ttu-id="44285-131">Egun, herrialde / eskualdeko aukerak onartzen ditugu: Australia, Kanada (ingelesa), Frantzia, Alemania, Erresuma Batua edo Estatu Batuak (ingelesa).</span><span class="sxs-lookup"><span data-stu-id="44285-131">We currently support the following country/region options: Australia, Canada (English), France, Germany, United Kingdom, or United States (English).</span></span>

<span data-ttu-id="44285-132">Herrialdea hautatzeko, ireki **Marken aberastasuna** edo **Interesak aberastea** eta hautatu **Aldaketa** Alboan **Herrialdea / eskualdea**.</span><span class="sxs-lookup"><span data-stu-id="44285-132">To select a country, open the **Brands enrichment** or **Interest enrichment** and select **Change** next to **Country/Region**.</span></span> <span data-ttu-id="44285-133">Sarbidean **Herrialdearen eta eskualdeen ezarpenak** panela, aukeratu aukera bat eta hautatu **aplikatu**.</span><span class="sxs-lookup"><span data-stu-id="44285-133">In the **Country/Region settings** pane, choose an option and select **Apply**.</span></span>

### <a name="implications-related-to-country-selection"></a><span data-ttu-id="44285-134">Herrialdearen hautaketarekin lotutako ondorioak</span><span class="sxs-lookup"><span data-stu-id="44285-134">Implications related to country selection</span></span>

- <span data-ttu-id="44285-135">[Zure markak aukeratzen dituzunean](#define-your-brands-or-interests), sistemak hautatutako herrialdean edo eskualdean oinarritutako iradokizunak eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="44285-135">When [choosing your own brands](#define-your-brands-or-interests), the system provides suggestions based on the selected country or region.</span></span>

- <span data-ttu-id="44285-136">[Sektorea aukeratzean](#define-your-brands-or-interests), hautatutako herrialdean edo eskualdean oinarritutako marka edo interes garrantzitsuenak lortuko dituzu.</span><span class="sxs-lookup"><span data-stu-id="44285-136">When [choosing an industry](#define-your-brands-or-interests), you'll get the most relevant brands or interests based on the selected country or region.</span></span>

- <span data-ttu-id="44285-137">[Profilak aberastean](#refresh-enrichment), bezeroen profil guztiak aberastuko ditugu hautatutako marka eta interesen datuak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="44285-137">When [enriching profiles](#refresh-enrichment), we'll enrich all customer profiles for which we get data for the selected brands and interests.</span></span> <span data-ttu-id="44285-138">Aukeratutako herrialdean edo eskualdean ez dauden profilak barne.</span><span class="sxs-lookup"><span data-stu-id="44285-138">Including profiles that are not in the selected country or region.</span></span> <span data-ttu-id="44285-139">Adibidez, Alemania aukeratu baduzu, Estatu Batuetan kokatutako profilak aberastuko ditugu AEBetan hautatutako marka eta interesetarako datuak eskuragarri baditugu.</span><span class="sxs-lookup"><span data-stu-id="44285-139">For example, if you selected Germany, we'll enrich profiles located in the United States if we have data available for the selected brands and interests in the US.</span></span>

## <a name="configure-enrichment"></a><span data-ttu-id="44285-140">Aberastea konfiguratu</span><span class="sxs-lookup"><span data-stu-id="44285-140">Configure Enrichment</span></span>

<span data-ttu-id="44285-141">Esperientzia gidatu batek aberastasunak konfiguratzen lagunduko dizu.</span><span class="sxs-lookup"><span data-stu-id="44285-141">A guided experience helps you through the configuration of the enrichments.</span></span> 

### <a name="define-your-brands-or-interests"></a><span data-ttu-id="44285-142">Zehaztu zure markak edo zaletasunak</span><span class="sxs-lookup"><span data-stu-id="44285-142">Define your brands or interests</span></span>

<span data-ttu-id="44285-143">Aukeratu gehienez bost marka edo interes aukera hauetako bat edo biak erabiliz:</span><span class="sxs-lookup"><span data-stu-id="44285-143">Choose up to five brands or interests using one or both of these options:</span></span>

- <span data-ttu-id="44285-144">**Industria**: Aukeratu zure industria goitibeherako zerrendan eta hautatu industria horretako marka edo interes garrantzitsuenen artean.</span><span class="sxs-lookup"><span data-stu-id="44285-144">**Industry**: Select your industry from the drop-down list and then choose from the top brands or interests for that industry.</span></span>
- <span data-ttu-id="44285-145">**Aukeratu zeurea**: Sartu zure erakundearentzako garrantzitsua den marka edo interesa eta aukeratu bat datorren iradokizunen artean.</span><span class="sxs-lookup"><span data-stu-id="44285-145">**Choose your own**: Enter a brand or interest that is relevant to your organization and then choose from the matching suggestions.</span></span> <span data-ttu-id="44285-146">Bilatzen ari zaren marka edo interesa zerrendatzen ez badugu, bidal iezaguzu iritzia erabilita **Proposatu** esteka.</span><span class="sxs-lookup"><span data-stu-id="44285-146">If we don't list a brand or interest you're looking for, send us feedback using the **Suggest** link.</span></span>

### <a name="review-enrichment-preferences"></a><span data-ttu-id="44285-147">Berrikusi aberaste-hobespenak</span><span class="sxs-lookup"><span data-stu-id="44285-147">Review enrichment preferences</span></span>

<span data-ttu-id="44285-148">Berrikusi aberastasun lehentasun lehenetsiak eta eguneratu behar dituzun moduan.</span><span class="sxs-lookup"><span data-stu-id="44285-148">Review your default enrichment preferences and update them as needed.</span></span>

:::image type="content" source="media/affinity-enrichment-preferences.png" alt-text="Aberasteko lehentasunen leihoaren pantaila-argazkia.":::

### <a name="select-entity-to-enrich"></a><span data-ttu-id="44285-150">Hautatu aberasteko entitatea</span><span class="sxs-lookup"><span data-stu-id="44285-150">Select entity to enrich</span></span>

<span data-ttu-id="44285-151">Hautatu **Aberastutako entitatea** eta aukera datuak ezartzeko aberastu nahi duzuna konpainiaren datuekin Microsoft-etik.</span><span class="sxs-lookup"><span data-stu-id="44285-151">Select **Enriched entity** and choose the data set you want to enrich with company data from the Microsoft.</span></span> <span data-ttu-id="44285-152">Bezeroen entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="44285-152">You can select the Customer entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

### <a name="map-your-fields"></a><span data-ttu-id="44285-153">Esleitu eremuak</span><span class="sxs-lookup"><span data-stu-id="44285-153">Map your fields</span></span>

<span data-ttu-id="44285-154">Esleitu zure bezero entitate bateratuko eremuak sistemak zure bezeroaren datuak aberasteko erabili nahi duzun segmentu demografikoa definitzeko.</span><span class="sxs-lookup"><span data-stu-id="44285-154">Map fields from your unified customer entity to define the demographic segment you want the system to use for enriching your customer data.</span></span> <span data-ttu-id="44285-155">Esleitu herrialdea/eskualdea eta gutxienez Jaiotze-data edo Generoa atributuak.</span><span class="sxs-lookup"><span data-stu-id="44285-155">Map Country/Region and at least Date of Birth or Gender attributes.</span></span> <span data-ttu-id="44285-156">Gainera, herrialdea/eskualdea esleitu behar duzu. Halaber, hiri bat (eta estatua/probintzia) edo posta-kode bat esleitu behar dituzu gutxienez.</span><span class="sxs-lookup"><span data-stu-id="44285-156">Additionally, you must map at least one of City (and State/Province) or Postal code.</span></span> <span data-ttu-id="44285-157">Aukeratu **Editatu** eremuen mapa zehaztu eta hautatu **aplikatu** amaitutakoan.</span><span class="sxs-lookup"><span data-stu-id="44285-157">Select **Edit** to define the mapping of the fields and select **Apply** when you're done.</span></span> <span data-ttu-id="44285-158">Aukeratu **Gorde** eremuaren mapa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="44285-158">Select **Save** to complete the field mapping.</span></span>

<span data-ttu-id="44285-159">Formatu eta balio hauek onartzen dira, balioak ez dira maiuskulak:</span><span class="sxs-lookup"><span data-stu-id="44285-159">The following formats and values are supported, values are not case-sensitive:</span></span>

- <span data-ttu-id="44285-160">**Jaioteguna**: Jaiotze-data DataTime motara bihurtzea gomendatzen dugu datuak irensten diren bitartean.</span><span class="sxs-lookup"><span data-stu-id="44285-160">**Date of Birth**: We recommend that date of birth is converted to DateTime type during data ingestion.</span></span> <span data-ttu-id="44285-161">Bestela, barruko katea izan daiteke [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) "uuuu-HH-ee" edo "uuuu-HH-eeHH:mm:ssZ" formatua.</span><span class="sxs-lookup"><span data-stu-id="44285-161">Alternatively, it can be a string in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format "yyyy-MM-dd" or "yyyy-MM-ddTHH:mm:ssZ".</span></span>
- <span data-ttu-id="44285-162">**Generoa**: Gizona, Emakumezkoa, Ezezaguna</span><span class="sxs-lookup"><span data-stu-id="44285-162">**Gender**: Male, Female, Unknown</span></span>
- <span data-ttu-id="44285-163">**Posta kodea**: Bost digitu ZIP kodea AEBetarako, posta estandarraren beste edozein lekutan</span><span class="sxs-lookup"><span data-stu-id="44285-163">**Postal code**: Five-digit ZIP Codes for US, standard postal code everywhere else</span></span>
- <span data-ttu-id="44285-164">**hiria**: Hiria izena ingelesez</span><span class="sxs-lookup"><span data-stu-id="44285-164">**City**: City name in English</span></span>
- <span data-ttu-id="44285-165">**Estatua / Probintzia**: AEB eta Kanadako bi gutun-laburdura.</span><span class="sxs-lookup"><span data-stu-id="44285-165">**State/Province**: Two-letter abbreviation for the US and Canada.</span></span> <span data-ttu-id="44285-166">Bi edo hiru gutun laburdura Australiarako.</span><span class="sxs-lookup"><span data-stu-id="44285-166">Two or three letter abbreviation for Australia.</span></span> <span data-ttu-id="44285-167">Ez da aplikagarria Frantzian, Alemanian edo Erresuma Batuan.</span><span class="sxs-lookup"><span data-stu-id="44285-167">Not applicable for France, Germany, or the UK.</span></span>
- <span data-ttu-id="44285-168">**Herrialdea/Eskualdea**:</span><span class="sxs-lookup"><span data-stu-id="44285-168">**Country/Region**:</span></span>

  - <span data-ttu-id="44285-169">AEB: Ameriketako Estatu Batuak, Estatu Batuak, AEBak, AEBak, Amerika</span><span class="sxs-lookup"><span data-stu-id="44285-169">US: United States of America, United States, USA, US, America</span></span>
  - <span data-ttu-id="44285-170">CA: Kanada, CA</span><span class="sxs-lookup"><span data-stu-id="44285-170">CA: Canada, CA</span></span>
  - <span data-ttu-id="44285-171">GB: Erresuma Batua, Erresuma Batua, Britainia Handia, GB, Britainia Handia eta Ipar Irlanda, Erresuma Batua</span><span class="sxs-lookup"><span data-stu-id="44285-171">GB: United Kingdom, UK, Great Britain, GB, United Kingdom of Great Britain and Northern Ireland, United Kingdom of Great Britain</span></span>
  - <span data-ttu-id="44285-172">AU: Australia, AU, Australiako Aberastasun Komuna</span><span class="sxs-lookup"><span data-stu-id="44285-172">AU: Australia, AU, Common Wealth of Australia</span></span>
  - <span data-ttu-id="44285-173">FR: Frantzia, FR, Frantziar Errepublika</span><span class="sxs-lookup"><span data-stu-id="44285-173">FR: France, FR, French Republic</span></span>
  - <span data-ttu-id="44285-174">DE: Alemania, Alemania, Deutschland, Allemagne, DE, Alemaniako Errepublika Federala, Alemaniako Errepublika</span><span class="sxs-lookup"><span data-stu-id="44285-174">DE: Germany, German, Deutschland, Allemagne, DE, Federal Republic of Germany, Republic of Germany</span></span>

## <a name="review-and-name-the-enrichment"></a><span data-ttu-id="44285-175">Aberaspena berrikusi eta izendatu</span><span class="sxs-lookup"><span data-stu-id="44285-175">Review and name the enrichment</span></span>

<span data-ttu-id="44285-176">Azkenean, informazioa berrikusi eta aberasteko izena eman dezakezu.</span><span class="sxs-lookup"><span data-stu-id="44285-176">Finally, you get to review the information and provide a name for the enrichment.</span></span>

:::image type="content" source="media/enrichment-interests-summary.png" alt-text="Interesak berrikusteko eta izendatzeko orria.":::

## <a name="refresh-enrichment"></a><span data-ttu-id="44285-178">Freskatu aberastea</span><span class="sxs-lookup"><span data-stu-id="44285-178">Refresh enrichment</span></span>

<span data-ttu-id="44285-179">Exekutatu aberastasuna marka, interesak eta eremuen mapak konfiguratu ondoren demografiarako.</span><span class="sxs-lookup"><span data-stu-id="44285-179">Run the enrichment after configuring brands, interests, and the field mapping for demographics.</span></span> <span data-ttu-id="44285-180">Prozesua hasteko, hautatu **Korrika egin** marka edo interesen konfigurazio orrian.</span><span class="sxs-lookup"><span data-stu-id="44285-180">To start the process, select **Run** on the brand or interest configuration page.</span></span> <span data-ttu-id="44285-181">Gainera, sistemak aberastasuna automatikoki utz dezakezu planifikatu gabeko freskatze baten baitan.</span><span class="sxs-lookup"><span data-stu-id="44285-181">Additionally, you can let the system run the enrichment automatically as part of a scheduled refresh.</span></span>
<span data-ttu-id="44285-182">Bezeroaren datuen tamainaren arabera, minutu batzuk behar izango dira aberasteko exekuzioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="44285-182">Depending on the size of your customer data, it may take several minutes for an enrichment run to complete.</span></span>

> [!TIP]
> <span data-ttu-id="44285-183">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="44285-183">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="44285-184">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="44285-184">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="44285-185">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="44285-185">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="44285-186">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="44285-186">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="44285-187">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="44285-187">Enrichment results</span></span>

<span data-ttu-id="44285-188">Aberaste prozesua exekutatu ostean, joan **Nire aberasteak** berrikusteko guztira aberastutako bezeroen kopurua eta aberastutako bezeroen profilen marka eta interesen banaketa.</span><span class="sxs-lookup"><span data-stu-id="44285-188">After running the enrichment process, go to **My enrichments** to review the total number of enriched customers and a breakdown of brands or interests in the enriched customer profiles.</span></span>

:::image type="content" source="media/my-enrichments.png" alt-text="Abantaila prozesua exekutatu ondoren, emaitzen aurrebista":::

<span data-ttu-id="44285-190">Berrikusi aberastutako datuak, hautatuta **Ikusi aberastutako datuak** grafikoan.</span><span class="sxs-lookup"><span data-stu-id="44285-190">Review the enriched data by selecting **View enriched data** in the chart.</span></span> <span data-ttu-id="44285-191">Marken datu aberastuak: **BrandAffinityFromMicrosoft** Erakunde.</span><span class="sxs-lookup"><span data-stu-id="44285-191">Enriched data for brands goes to the **BrandAffinityFromMicrosoft** entity.</span></span> <span data-ttu-id="44285-192">Interesen datuak datuak daude **InterestAffinityFromMicrosoft** Erakunde.</span><span class="sxs-lookup"><span data-stu-id="44285-192">Data for interests is in the **InterestAffinityFromMicrosoft** entity.</span></span> <span data-ttu-id="44285-193">Erakunde hauek zerrendan aurkituko dituzu **aberastea** taldean **Datuak** > **erakundeak** atalean.</span><span class="sxs-lookup"><span data-stu-id="44285-193">You'll also find these entities listed in the **Enrichment** group in **Data** > **Entities**.</span></span>

## <a name="see-enrichment-data-on-the-customer-card"></a><span data-ttu-id="44285-194">Ikusi aberastasun datuak bezeroaren txartelean</span><span class="sxs-lookup"><span data-stu-id="44285-194">See enrichment data on the customer card</span></span>

<span data-ttu-id="44285-195">Marka eta interes kidetasunak bezero banakako txarteletan ere ikus daitezke.</span><span class="sxs-lookup"><span data-stu-id="44285-195">Brand and interest affinities can also be viewed on individual customer cards.</span></span> <span data-ttu-id="44285-196">Joan **Bezeroak** atalera eta hautatu bezeroaren profila.</span><span class="sxs-lookup"><span data-stu-id="44285-196">Go to **Customers** and select a customer profile.</span></span> <span data-ttu-id="44285-197">Bezeroaren txartelean, bezeroaren demografia profil horretako pertsonek afinitatea duten marken edo interesen zerrendak aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="44285-197">In the customer card, you'll find charts for the brands or interests that people in that customer's demographic profile have affinity for.</span></span>

:::image type="content" source="media/enrichment-customer-card.png" alt-text="Aberastutako datuak dituen bezeroaren txartela":::

## <a name="next-steps"></a><span data-ttu-id="44285-199">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="44285-199">Next steps</span></span>

<span data-ttu-id="44285-200">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="44285-200">Build on top of your enriched customer data.</span></span> <span data-ttu-id="44285-201">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="44285-201">Create [Segments](segments.md), [Measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
