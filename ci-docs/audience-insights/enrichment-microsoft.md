---
title: Aberastu bezeroen profilak Microsoften datuekin
description: Erabili Microsoft-en jabedun datuak bezeroen datuak marka eta interes kidetasunekin aberasteko.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-MS
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 6f19033236190547f68d2b91ec6b32074bf7912a
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5896587"
---
# <a name="enrich-customer-profiles-with-brand-and-interest-affinities-preview"></a><span data-ttu-id="064c0-103">Aberastu bezeroen profilak marka eta interes kidetasunekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="064c0-103">Enrich customer profiles with brand and interest affinities (preview)</span></span>

<span data-ttu-id="064c0-104">Erabili Microsoft-en jabedun datuak bezeroen datuak marka eta interes kidetasunekin aberasteko.</span><span class="sxs-lookup"><span data-stu-id="064c0-104">Use Microsoft's proprietary data to enrich your customer data with brand and interest affinities.</span></span> <span data-ttu-id="064c0-105">Afinitate horiek zure bezeroen antzeko demografia duten pertsonen datuetan oinarrituta zehazten dira.</span><span class="sxs-lookup"><span data-stu-id="064c0-105">These affinities are determined based on data from people with similar demographics to your customers.</span></span> <span data-ttu-id="064c0-106">Informazio honek bezeroak hobeto ulertzen eta segmentatzen laguntzen du, marka eta interes jakin batzuen arabera.</span><span class="sxs-lookup"><span data-stu-id="064c0-106">This information helps you to better understand and segment your customers based on their affinities to specific brands and interests.</span></span>

<span data-ttu-id="064c0-107">Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** [aberasteak konfiguratu eta ikusteko](enrichment-hub.md).</span><span class="sxs-lookup"><span data-stu-id="064c0-107">In audience insights, go to **Data** > **Enrichment** to [configure and view enrichments](enrichment-hub.md).</span></span>

<span data-ttu-id="064c0-108">Marka afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Markak** teila.</span><span class="sxs-lookup"><span data-stu-id="064c0-108">To configure brand affinities enrichment, go to the **Discover** tab and select **Enrich my data** on the **Brands** tile.</span></span>

<span data-ttu-id="064c0-109">Interes afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Interesak** teila.</span><span class="sxs-lookup"><span data-stu-id="064c0-109">To configure interest affinities enrichment, go to the **Discover** tab and select **Enrich my data** on the **Interests** tile.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="064c0-110">![Markak eta interesen lauzak](media/BrandsInterest-tile-Hub.png "Markak eta interesaren lauzak")</span><span class="sxs-lookup"><span data-stu-id="064c0-110">![Brands & Interests tiles](media/BrandsInterest-tile-Hub.png "Brands & Interest tiles")</span></span>

## <a name="how-we-determine-affinities"></a><span data-ttu-id="064c0-111">Afinitateak nola zehazten ditugun</span><span class="sxs-lookup"><span data-stu-id="064c0-111">How we determine affinities</span></span>

<span data-ttu-id="064c0-112">Microsoften lineako bilaketa-datuak erabiltzen ditugu marka eta interesen arteko afinitateak aurkitzeko hainbat segmentu demografikotan (adinaren, generoaren edo kokapenaren arabera definituak).</span><span class="sxs-lookup"><span data-stu-id="064c0-112">We use Microsoft’s online search data to find affinities for brands and interests across various demographic segments (defined by age, gender, or location).</span></span> <span data-ttu-id="064c0-113">Marka edo interes baten bilaketa-bolumenak zehazten du zein den afinitate batek segmentu demografiko batek, beste segmentu batzuekin alderatuta, marka edo interes hori.</span><span class="sxs-lookup"><span data-stu-id="064c0-113">The online search volume for a brand or interest determines how much affinity a demographic segment, compared to other segments, has to that brand or interest.</span></span> <span data-ttu-id="064c0-114">Marka edo interesa.</span><span class="sxs-lookup"><span data-stu-id="064c0-114">brand or interest.</span></span>

## <a name="affinity-level-and-score"></a><span data-ttu-id="064c0-115">Afinitate-maila eta puntuazioa</span><span class="sxs-lookup"><span data-stu-id="064c0-115">Affinity level and score</span></span>

<span data-ttu-id="064c0-116">Bezeroen profil aberastu guztietan, erlazionatutako bi balio ematen ditugu: afinitate-maila eta afinitate-puntuazioa.</span><span class="sxs-lookup"><span data-stu-id="064c0-116">On every enriched customer profile, we provide two related values – affinity level and affinity score.</span></span> <span data-ttu-id="064c0-117">Balio horiei esker, profil horren segmentu demografikoarekiko, marka edo interesekiko, beste segmentu demografiko batzuekiko duten afinitatea zehazten lagunduko dizute.</span><span class="sxs-lookup"><span data-stu-id="064c0-117">These values help you determine how strong the affinity is for that profile’s demographic segment, for a brand or interest, as compared to other demographic segments.</span></span>

<span data-ttu-id="064c0-118">*Afinitate-maila* lau maila ditu eta *afinitate puntuazioa* afinitate mailetara esleitzen den 100 puntuko eskalan kalkulatzen da.</span><span class="sxs-lookup"><span data-stu-id="064c0-118">*Affinity level* consists of four levels and *affinity score* is calculated on a 100-point scale that maps to the affinity levels.</span></span>


|<span data-ttu-id="064c0-119">Afinitate-maila</span><span class="sxs-lookup"><span data-stu-id="064c0-119">Affinity level</span></span> |<span data-ttu-id="064c0-120">Afinitate-puntuazioa</span><span class="sxs-lookup"><span data-stu-id="064c0-120">Affinity score</span></span>  |
|---------|---------|
|<span data-ttu-id="064c0-121">Oso handia</span><span class="sxs-lookup"><span data-stu-id="064c0-121">Very high</span></span>     | <span data-ttu-id="064c0-122">85-100</span><span class="sxs-lookup"><span data-stu-id="064c0-122">85-100</span></span>       |
|<span data-ttu-id="064c0-123">Handia</span><span class="sxs-lookup"><span data-stu-id="064c0-123">High</span></span>     | <span data-ttu-id="064c0-124">70-84</span><span class="sxs-lookup"><span data-stu-id="064c0-124">70-84</span></span>        |
|<span data-ttu-id="064c0-125">Ertaina</span><span class="sxs-lookup"><span data-stu-id="064c0-125">Medium</span></span>     | <span data-ttu-id="064c0-126">35-69</span><span class="sxs-lookup"><span data-stu-id="064c0-126">35-69</span></span>        |
|<span data-ttu-id="064c0-127">Txikia</span><span class="sxs-lookup"><span data-stu-id="064c0-127">Low</span></span>     | <span data-ttu-id="064c0-128">1-34</span><span class="sxs-lookup"><span data-stu-id="064c0-128">1-34</span></span>        |

<span data-ttu-id="064c0-129">Afinitatea neurtzeko nahi duzun xehetasunen arabera, afinitate maila edo puntuazioa erabil dezakezu.</span><span class="sxs-lookup"><span data-stu-id="064c0-129">Depending on the granularity you would like for measuring the affinity, you can use either affinity level or score.</span></span> <span data-ttu-id="064c0-130">Afinitate-puntuazioak kontrol zehatzagoa ematen dizu.</span><span class="sxs-lookup"><span data-stu-id="064c0-130">Affinity score gives you more precise control.</span></span>

## <a name="supported-countriesregions"></a><span data-ttu-id="064c0-131">Lagundutako herrialde / eskualdeak</span><span class="sxs-lookup"><span data-stu-id="064c0-131">Supported countries/regions</span></span>

<span data-ttu-id="064c0-132">Egun, herrialde / eskualdeko aukerak onartzen ditugu: Australia, Kanada (ingelesa), Frantzia, Alemania, Erresuma Batua edo Estatu Batuak (ingelesa).</span><span class="sxs-lookup"><span data-stu-id="064c0-132">We currently support the following country/region options: Australia, Canada (English), France, Germany, United Kingdom, or United States (English).</span></span>

<span data-ttu-id="064c0-133">Herrialdea hautatzeko, ireki **Marken aberastasuna** edo **Interesak aberastea** eta hautatu **Aldaketa** Alboan **Herrialdea / eskualdea**.</span><span class="sxs-lookup"><span data-stu-id="064c0-133">To select a country, open the **Brands enrichment** or **Interest enrichment** and select **Change** next to **Country/Region**.</span></span> <span data-ttu-id="064c0-134">Sarbidean **Herrialdearen eta eskualdeen ezarpenak** panela, aukeratu aukera bat eta hautatu **aplikatu**.</span><span class="sxs-lookup"><span data-stu-id="064c0-134">In the **Country/Region settings** pane, choose an option and select **Apply**.</span></span>

### <a name="implications-related-to-country-selection"></a><span data-ttu-id="064c0-135">Herrialdearen hautaketarekin lotutako ondorioak</span><span class="sxs-lookup"><span data-stu-id="064c0-135">Implications related to country selection</span></span>

- <span data-ttu-id="064c0-136">[Zure markak aukeratzen dituzunean](#define-your-brands-or-interests), sistemak hautatutako herrialdean edo eskualdean oinarritutako iradokizunak eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="064c0-136">When [choosing your own brands](#define-your-brands-or-interests), the system provides suggestions based on the selected country or region.</span></span>

- <span data-ttu-id="064c0-137">[Sektorea aukeratzean](#define-your-brands-or-interests), hautatutako herrialdean edo eskualdean oinarritutako marka edo interes garrantzitsuenak lortuko dituzu.</span><span class="sxs-lookup"><span data-stu-id="064c0-137">When [choosing an industry](#define-your-brands-or-interests), you'll get the most relevant brands or interests based on the selected country or region.</span></span>

- <span data-ttu-id="064c0-138">[Profilak aberastean](#refresh-enrichment), bezeroen profil guztiak aberastuko ditugu hautatutako marka eta interesen datuak lortzeko.</span><span class="sxs-lookup"><span data-stu-id="064c0-138">When [enriching profiles](#refresh-enrichment), we'll enrich all customer profiles for which we get data for the selected brands and interests.</span></span> <span data-ttu-id="064c0-139">Aukeratutako herrialdean edo eskualdean ez dauden profilak barne.</span><span class="sxs-lookup"><span data-stu-id="064c0-139">Including profiles that are not in the selected country or region.</span></span> <span data-ttu-id="064c0-140">Adibidez, Alemania aukeratu baduzu, Estatu Batuetan kokatutako profilak aberastuko ditugu AEBetan hautatutako marka eta interesetarako datuak eskuragarri baditugu.</span><span class="sxs-lookup"><span data-stu-id="064c0-140">For example, if you selected Germany, we'll enrich profiles located in the United States if we have data available for the selected brands and interests in the US.</span></span>

## <a name="configure-enrichment"></a><span data-ttu-id="064c0-141">Aberastea konfiguratu</span><span class="sxs-lookup"><span data-stu-id="064c0-141">Configure Enrichment</span></span>

<span data-ttu-id="064c0-142">Esperientzia gidatu batek aberastasunak konfiguratzen lagunduko dizu.</span><span class="sxs-lookup"><span data-stu-id="064c0-142">A guided experience helps you through the configuration of the enrichments.</span></span> 

### <a name="define-your-brands-or-interests"></a><span data-ttu-id="064c0-143">Zehaztu zure markak edo zaletasunak</span><span class="sxs-lookup"><span data-stu-id="064c0-143">Define your brands or interests</span></span>

<span data-ttu-id="064c0-144">Hautatu aukera hauetariko bat:</span><span class="sxs-lookup"><span data-stu-id="064c0-144">Select one of the following options:</span></span>

- <span data-ttu-id="064c0-145">**Industria**: Sistemak zure industrian garrantzitsuak diren marka edo interesak identifikatzen ditu eta zure bezeroaren datuak aberasten ditu.</span><span class="sxs-lookup"><span data-stu-id="064c0-145">**Industry**: The system identifies the top brands or interests relevant to your industry and enriches your customer data with them.</span></span>
- <span data-ttu-id="064c0-146">**Aukeratu zeurea**: Zure erakunderako garrantzitsuenak diren marka edo interesen zerrendako bost elementu aukeratu.</span><span class="sxs-lookup"><span data-stu-id="064c0-146">**Choose your own**: Select up to five items from the list of brands or interests that are most relevant to your organization.</span></span>

<span data-ttu-id="064c0-147">Marka edo interesa gehitzeko, sartu sarrerako eremuan, datozen terminoen araberako iradokizunak jasotzeko.</span><span class="sxs-lookup"><span data-stu-id="064c0-147">To add a brand or interest, enter it in the input area to get suggestions based on matching terms.</span></span> <span data-ttu-id="064c0-148">Bilatzen ari zaren marka edo interesa zerrendatzen ez badugu, bidal iezaguzu iritzia erabilita **Proposatu** esteka.</span><span class="sxs-lookup"><span data-stu-id="064c0-148">If we don't list a brand or interest you're looking for, send us feedback using the **Suggest** link.</span></span>

### <a name="review-enrichment-preferences"></a><span data-ttu-id="064c0-149">Berrikusi aberaste-hobespenak</span><span class="sxs-lookup"><span data-stu-id="064c0-149">Review enrichment preferences</span></span>

<span data-ttu-id="064c0-150">Berrikusi aberastasun lehentasun lehenetsiak eta eguneratu behar dituzun moduan.</span><span class="sxs-lookup"><span data-stu-id="064c0-150">Review your default enrichment preferences and update them as needed.</span></span>

:::image type="content" source="media/affinity-enrichment-preferences.png" alt-text="Aberasteko lehentasunen leihoaren pantaila-argazkia.":::

### <a name="select-entity-to-enrich"></a><span data-ttu-id="064c0-152">Hautatu aberasteko entitatea</span><span class="sxs-lookup"><span data-stu-id="064c0-152">Select entity to enrich</span></span>

<span data-ttu-id="064c0-153">Hautatu **Aberastutako entitatea** eta aukera datuak ezartzeko aberastu nahi duzuna konpainiaren datuekin Microsoft-etik.</span><span class="sxs-lookup"><span data-stu-id="064c0-153">Select **Enriched entity** and choose the data set you want to enrich with company data from the Microsoft.</span></span> <span data-ttu-id="064c0-154">Bezeroen entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.</span><span class="sxs-lookup"><span data-stu-id="064c0-154">You can select the Customer entity to enrich all your customer profiles or select a segment entity to enrich only customer profiles contained in that segment.</span></span>

### <a name="map-your-fields"></a><span data-ttu-id="064c0-155">Esleitu eremuak</span><span class="sxs-lookup"><span data-stu-id="064c0-155">Map your fields</span></span>

<span data-ttu-id="064c0-156">Esleitu zure bezero entitate bateratuko eremuak sistemak zure bezeroaren datuak aberasteko erabili nahi duzun segmentu demografikoa definitzeko.</span><span class="sxs-lookup"><span data-stu-id="064c0-156">Map fields from your unified customer entity to define the demographic segment you want the system to use for enriching your customer data.</span></span> <span data-ttu-id="064c0-157">Esleitu herrialdea/eskualdea eta gutxienez Jaiotze-data edo Generoa atributuak.</span><span class="sxs-lookup"><span data-stu-id="064c0-157">Map Country/Region and at least Date of Birth or Gender attributes.</span></span> <span data-ttu-id="064c0-158">Gainera, herrialdea/eskualdea esleitu behar duzu. Halaber, hiri bat (eta estatua/probintzia) edo posta-kode bat esleitu behar dituzu gutxienez.</span><span class="sxs-lookup"><span data-stu-id="064c0-158">Additionally, you must map at least one of City (and State/Province) or Postal code.</span></span> <span data-ttu-id="064c0-159">Aukeratu **Editatu** eremuen mapa zehaztu eta hautatu **aplikatu** amaitutakoan.</span><span class="sxs-lookup"><span data-stu-id="064c0-159">Select **Edit** to define the mapping of the fields and select **Apply** when you're done.</span></span> <span data-ttu-id="064c0-160">Aukeratu **Gorde** eremuaren mapa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="064c0-160">Select **Save** to complete the field mapping.</span></span>

<span data-ttu-id="064c0-161">Formatu eta balio hauek onartzen dira, balioak ez dira maiuskulak:</span><span class="sxs-lookup"><span data-stu-id="064c0-161">The following formats and values are supported, values are not case-sensitive:</span></span>

- <span data-ttu-id="064c0-162">**Jaioteguna**: Jaiotze-data DataTime motara bihurtzea gomendatzen dugu datuak irensten diren bitartean.</span><span class="sxs-lookup"><span data-stu-id="064c0-162">**Date of Birth**: We recommend that date of birth is converted to DateTime type during data ingestion.</span></span> <span data-ttu-id="064c0-163">Bestela, barruko katea izan daiteke [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) "uuuu-HH-ee" edo "uuuu-HH-eeHH:mm:ssZ" formatua.</span><span class="sxs-lookup"><span data-stu-id="064c0-163">Alternatively, it can be a string in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format "yyyy-MM-dd" or "yyyy-MM-ddTHH:mm:ssZ".</span></span>
- <span data-ttu-id="064c0-164">**Generoa**: Gizona, Emakumezkoa, Ezezaguna</span><span class="sxs-lookup"><span data-stu-id="064c0-164">**Gender**: Male, Female, Unknown</span></span>
- <span data-ttu-id="064c0-165">**Posta kodea**: Bost digitu ZIP kodea AEBetarako, posta estandarraren beste edozein lekutan</span><span class="sxs-lookup"><span data-stu-id="064c0-165">**Postal code**: Five-digit ZIP Codes for US, standard postal code everywhere else</span></span>
- <span data-ttu-id="064c0-166">**hiria**: Hiria izena ingelesez</span><span class="sxs-lookup"><span data-stu-id="064c0-166">**City**: City name in English</span></span>
- <span data-ttu-id="064c0-167">**Estatua / Probintzia**: AEB eta Kanadako bi gutun-laburdura.</span><span class="sxs-lookup"><span data-stu-id="064c0-167">**State/Province**: Two-letter abbreviation for the US and Canada.</span></span> <span data-ttu-id="064c0-168">Bi edo hiru gutun laburdura Australiarako.</span><span class="sxs-lookup"><span data-stu-id="064c0-168">Two or three letter abbreviation for Australia.</span></span> <span data-ttu-id="064c0-169">Ez da aplikagarria Frantzian, Alemanian edo Erresuma Batuan.</span><span class="sxs-lookup"><span data-stu-id="064c0-169">Not applicable for France, Germany, or the UK.</span></span>
- <span data-ttu-id="064c0-170">**Herrialdea/Eskualdea**:</span><span class="sxs-lookup"><span data-stu-id="064c0-170">**Country/Region**:</span></span>

  - <span data-ttu-id="064c0-171">AEB: Ameriketako Estatu Batuak, Estatu Batuak, AEBak, AEBak, Amerika</span><span class="sxs-lookup"><span data-stu-id="064c0-171">US: United States of America, United States, USA, US, America</span></span>
  - <span data-ttu-id="064c0-172">CA: Kanada, CA</span><span class="sxs-lookup"><span data-stu-id="064c0-172">CA: Canada, CA</span></span>
  - <span data-ttu-id="064c0-173">GB: Erresuma Batua, Erresuma Batua, Britainia Handia, GB, Britainia Handia eta Ipar Irlanda, Erresuma Batua</span><span class="sxs-lookup"><span data-stu-id="064c0-173">GB: United Kingdom, UK, Great Britain, GB, United Kingdom of Great Britain and Northern Ireland, United Kingdom of Great Britain</span></span>
  - <span data-ttu-id="064c0-174">AU: Australia, AU, Australiako Aberastasun Komuna</span><span class="sxs-lookup"><span data-stu-id="064c0-174">AU: Australia, AU, Common Wealth of Australia</span></span>
  - <span data-ttu-id="064c0-175">FR: Frantzia, FR, Frantziar Errepublika</span><span class="sxs-lookup"><span data-stu-id="064c0-175">FR: France, FR, French Republic</span></span>
  - <span data-ttu-id="064c0-176">DE: Alemania, Alemania, Deutschland, Allemagne, DE, Alemaniako Errepublika Federala, Alemaniako Errepublika</span><span class="sxs-lookup"><span data-stu-id="064c0-176">DE: Germany, German, Deutschland, Allemagne, DE, Federal Republic of Germany, Republic of Germany</span></span>

## <a name="review-and-name-the-enrichment"></a><span data-ttu-id="064c0-177">Aberaspena berrikusi eta izendatu</span><span class="sxs-lookup"><span data-stu-id="064c0-177">Review and name the enrichment</span></span>

<span data-ttu-id="064c0-178">Azkenean, informazioa berrikusi eta aberasteko izena eman dezakezu.</span><span class="sxs-lookup"><span data-stu-id="064c0-178">Finally, you get to review the information and provide a name for the enrichment.</span></span>

:::image type="content" source="media/enrichment-interests-summary.png" alt-text="Interesak berrikusteko eta izendatzeko orria.":::

## <a name="refresh-enrichment"></a><span data-ttu-id="064c0-180">Freskatu aberastea</span><span class="sxs-lookup"><span data-stu-id="064c0-180">Refresh enrichment</span></span>

<span data-ttu-id="064c0-181">Exekutatu aberastasuna marka, interesak eta eremuen mapak konfiguratu ondoren demografiarako.</span><span class="sxs-lookup"><span data-stu-id="064c0-181">Run the enrichment after configuring brands, interests, and the field mapping for demographics.</span></span> <span data-ttu-id="064c0-182">Prozesua hasteko, hautatu **Korrika egin** marka edo interesen konfigurazio orrian.</span><span class="sxs-lookup"><span data-stu-id="064c0-182">To start the process, select **Run** on the brand or interest configuration page.</span></span> <span data-ttu-id="064c0-183">Gainera, sistemak aberastasuna automatikoki utz dezakezu planifikatu gabeko freskatze baten baitan.</span><span class="sxs-lookup"><span data-stu-id="064c0-183">Additionally, you can let the system run the enrichment automatically as part of a scheduled refresh.</span></span>
<span data-ttu-id="064c0-184">Bezeroaren datuen tamainaren arabera, minutu batzuk behar izango dira aberasteko exekuzioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="064c0-184">Depending on the size of your customer data, it may take several minutes for an enrichment run to complete.</span></span>

> [!TIP]
> <span data-ttu-id="064c0-185">Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude.</span><span class="sxs-lookup"><span data-stu-id="064c0-185">There are [six types of status](system.md#status-types) for tasks/processes.</span></span> <span data-ttu-id="064c0-186">Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies).</span><span class="sxs-lookup"><span data-stu-id="064c0-186">Additionally, most processes [depend on other downstream processes](system.md#refresh-policies).</span></span> <span data-ttu-id="064c0-187">Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="064c0-187">You can select the status of a process to see details on the progress of the entire job.</span></span> <span data-ttu-id="064c0-188">Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.</span><span class="sxs-lookup"><span data-stu-id="064c0-188">After selecting **See details** for one of the job's tasks, you find additional information: processing time, the last processing date, and all errors and warnings associated with the task.</span></span>

## <a name="enrichment-results"></a><span data-ttu-id="064c0-189">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="064c0-189">Enrichment results</span></span>

<span data-ttu-id="064c0-190">Aberaste prozesua exekutatu ostean, joan **Nire aberasteak** berrikusteko guztira aberastutako bezeroen kopurua eta aberastutako bezeroen profilen marka eta interesen banaketa.</span><span class="sxs-lookup"><span data-stu-id="064c0-190">After running the enrichment process, go to **My enrichments** to review the total number of enriched customers and a breakdown of brands or interests in the enriched customer profiles.</span></span>

:::image type="content" source="media/my-enrichments.png" alt-text="Abantaila prozesua exekutatu ondoren, emaitzen aurrebista":::

<span data-ttu-id="064c0-192">Berrikusi aberastutako datuak, hautatuta **Ikusi aberastutako datuak** grafikoan.</span><span class="sxs-lookup"><span data-stu-id="064c0-192">Review the enriched data by selecting **View enriched data** in the chart.</span></span> <span data-ttu-id="064c0-193">Marken datu aberastuak: **BrandAffinityFromMicrosoft** Erakunde.</span><span class="sxs-lookup"><span data-stu-id="064c0-193">Enriched data for brands goes to the **BrandAffinityFromMicrosoft** entity.</span></span> <span data-ttu-id="064c0-194">Interesen datuak datuak daude **InterestAffinityFromMicrosoft** Erakunde.</span><span class="sxs-lookup"><span data-stu-id="064c0-194">Data for interests is in the **InterestAffinityFromMicrosoft** entity.</span></span> <span data-ttu-id="064c0-195">Erakunde hauek zerrendan aurkituko dituzu **aberastea** taldean **Datuak** > **erakundeak** atalean.</span><span class="sxs-lookup"><span data-stu-id="064c0-195">You'll also find these entities listed in the **Enrichment** group in **Data** > **Entities**.</span></span>

## <a name="see-enrichment-data-on-the-customer-card"></a><span data-ttu-id="064c0-196">Ikusi aberastasun datuak bezeroaren txartelean</span><span class="sxs-lookup"><span data-stu-id="064c0-196">See enrichment data on the customer card</span></span>

<span data-ttu-id="064c0-197">Marka eta interes kidetasunak bezero banakako txarteletan ere ikus daitezke.</span><span class="sxs-lookup"><span data-stu-id="064c0-197">Brand and interest affinities can also be viewed on individual customer cards.</span></span> <span data-ttu-id="064c0-198">Joan **Bezeroak** atalera eta hautatu bezeroaren profila.</span><span class="sxs-lookup"><span data-stu-id="064c0-198">Go to **Customers** and select a customer profile.</span></span> <span data-ttu-id="064c0-199">Bezeroaren txartelean, bezeroaren demografia profil horretako pertsonek afinitatea duten marken edo interesen zerrendak aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="064c0-199">In the customer card, you'll find charts for the brands or interests that people in that customer's demographic profile have affinity for.</span></span>

:::image type="content" source="media/enrichment-customer-card.png" alt-text="Aberastutako datuak dituen bezeroaren txartela":::

## <a name="next-steps"></a><span data-ttu-id="064c0-201">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="064c0-201">Next steps</span></span>

<span data-ttu-id="064c0-202">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="064c0-202">Build on top of your enriched customer data.</span></span> <span data-ttu-id="064c0-203">Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="064c0-203">Create [Segments](segments.md), [Measures](measures.md), and even [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
