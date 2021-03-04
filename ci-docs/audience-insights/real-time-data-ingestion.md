---
title: Denbora errealean datuak sartzea eta mugak
description: Hartzaileen xehetasunetako denbora errealeko gaitasunen inguruko informazio orokorra.
ms.date: 10/27/2020
ms.reviewer: nikeller
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 7421ed9d2cb399d546815b2d1b0ea5ec51ca6b6d
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270265"
---
# <a name="real-time-data-ingestion-preview"></a><span data-ttu-id="56b06-103">Denbora errealeko iragazkiak (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="56b06-103">Real-time data ingestion (preview)</span></span>

<span data-ttu-id="56b06-104">Denbora errealeko funtzionalitate hurbilak segundo askoren buruan, bezeroek zure produktuekin edo zerbitzuekin egin dituzten azken elkarrekintzak ikusteko aukera ematen du.</span><span class="sxs-lookup"><span data-stu-id="56b06-104">The near real-time functionality lets you see, within seconds, the latest interactions that your customers have made with your products or services.</span></span>

<span data-ttu-id="56b06-105">[Programatutako freskatzeak](system.md#schedule-tab) erregistro kopuru handia eta hainbat eragiketa konplexu biltzen ditu.</span><span class="sxs-lookup"><span data-stu-id="56b06-105">[Scheduled refreshes](system.md#schedule-tab) include large numbers of records and several complex operations.</span></span> <span data-ttu-id="56b06-106">Lehenik, datuak datu-iturburutik ateratzen dira.</span><span class="sxs-lookup"><span data-stu-id="56b06-106">First, data is pulled from the data source.</span></span> <span data-ttu-id="56b06-107">Ondoren, datuak bateratu egiten dira, eta gero informazio gehiagorekin aberasten dira.</span><span class="sxs-lookup"><span data-stu-id="56b06-107">Next, the data is unified, and then enriched with additional information.</span></span> <span data-ttu-id="56b06-108">Prozesu bakoitzeko korrikalari bakoitzak minutu batzuk ordu iraun ditzake.</span><span class="sxs-lookup"><span data-stu-id="56b06-108">Every run of this process can take minutes to hours.</span></span>

<span data-ttu-id="56b06-109">Denbora errealeko funtzioak berehala ematen ditu kontsumorako datuak, ondorengo eguneratze programatuak datu hauek datu-iturburutik atera arte.</span><span class="sxs-lookup"><span data-stu-id="56b06-109">The real-time functionality provides data immediately for consumption, until the subsequent scheduled refresh pulls this data from the data source.</span></span>

<span data-ttu-id="56b06-110">Denbora errealeko eguneratzeek iraungitze-denbora dute eta ondoren datu-iturburu-etik ez dute balioa gehitzen:</span><span class="sxs-lookup"><span data-stu-id="56b06-110">Real-time updates have an expiration time after which they no longer override the value from the data source:</span></span>

- <span data-ttu-id="56b06-111">Profilaren eguneratzeak 4 orduz mantenduko dira</span><span class="sxs-lookup"><span data-stu-id="56b06-111">Profile updates will be kept for 4 hours</span></span>
- <span data-ttu-id="56b06-112">Jarduerak 30 egunez mantenduko dira</span><span class="sxs-lookup"><span data-stu-id="56b06-112">Activities will be kept for 30 days</span></span>

<span data-ttu-id="56b06-113">Balio hauek API dei parametroak alda ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="56b06-113">These values are API call parameters that you can change.</span></span> <span data-ttu-id="56b06-114">Zure datu iturriak zure egia iturri izaten jarraituko dutela ziurtatzea dute helburu.</span><span class="sxs-lookup"><span data-stu-id="56b06-114">They aim to ensure that your source data remains your source of truth.</span></span> <span data-ttu-id="56b06-115">Denbora errealeko eguneratzeak denbora gehiagoz sartzea nahi baduzu, datu-iturburu batean gehitu behar dituzu hurrengo programatutako freskatzean atera ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="56b06-115">If you want real-time updates to be included for longer, you need to add them to a data source so they get pulled during the next scheduled refresh.</span></span>

## <a name="real-time-update-of-the-unified-customer-profile-fields"></a><span data-ttu-id="56b06-116">Bezeroaren profil bateratutako eremuak eguneratzeko denbora erreala</span><span class="sxs-lookup"><span data-stu-id="56b06-116">Real-time update of the unified customer profile fields</span></span>

<span data-ttu-id="56b06-117">Eguneratutako profilak bezeroaren txartelaren ikuspegian edo beste edozein bistaratzetan agertuko dira segundo gutxiren buruan.</span><span class="sxs-lookup"><span data-stu-id="56b06-117">Updated profiles will show in the customer card view, or any other visualization, within a few seconds.</span></span>

<span data-ttu-id="56b06-118">Denbora errealeko eragiketak datuak bateratu ondoren gertatu direlako, bateratutako bezeroen profiletara soilik aplikatzen dira.</span><span class="sxs-lookup"><span data-stu-id="56b06-118">Because real-time operations take place after the data unification has happened, they only apply to the unified customer profiles.</span></span> <span data-ttu-id="56b06-119">Horrenbestez, denbora errealeko profilaren aldaketek ez dituzte eguneratuko neurriak, segmentuen kideak edo aberastasunak.</span><span class="sxs-lookup"><span data-stu-id="56b06-119">Consequently, real-time profile changes will not update measures, segment membership, or enrichments.</span></span>

### <a name="limitations"></a><span data-ttu-id="56b06-120">Mugak</span><span class="sxs-lookup"><span data-stu-id="56b06-120">Limitations</span></span>

- <span data-ttu-id="56b06-121">Bezeroen profilak eguneratu daitezke, baina ez dira sortu edo ezabatu.</span><span class="sxs-lookup"><span data-stu-id="56b06-121">Customer profiles can be updated, but not created or deleted.</span></span>
- <span data-ttu-id="56b06-122">Eguneratzeak denbora errealeko kanpoko sistemetara esportatu, adibidez Power BI, momentuz ezinezkoa da.</span><span class="sxs-lookup"><span data-stu-id="56b06-122">Exporting real-time updates to external systems, like Power BI, is not possible at the moment.</span></span>

## <a name="real-time-creation-of-activities"></a><span data-ttu-id="56b06-123">Denbora errealean jarduerak sortzea</span><span class="sxs-lookup"><span data-stu-id="56b06-123">Real-time creation of activities</span></span>

<span data-ttu-id="56b06-124">Denbora errealeko APIari esker, zure iturburuko sistematik (iturburuko erregistro indibiduala) jarduera berri bat argitara dezakezu bezeroaren profil bateratura.</span><span class="sxs-lookup"><span data-stu-id="56b06-124">The real-time API lets you publish a new activity from your source system (an individual source record) to a unified customer profile.</span></span> <span data-ttu-id="56b06-125">Jarduera berria bateratutako bezero gisa egongo da eskuragarri bezeroaren profil kronologikoan segundotan.</span><span class="sxs-lookup"><span data-stu-id="56b06-125">The new activity will be available as a unified activity in that unified customer profile's timeline within seconds.</span></span> <span data-ttu-id="56b06-126">Kronologia bezeroaren txartelaren ikuspegian edo konfiguratu duzun beste edozein kronologiaren integrazioan ikus dezakezu.</span><span class="sxs-lookup"><span data-stu-id="56b06-126">You can see the timeline in the customer card view or any other timeline integration you configured.</span></span>

> [!NOTE]
>
> - <span data-ttu-id="56b06-127">Jarduerak ukaezinak dira.</span><span class="sxs-lookup"><span data-stu-id="56b06-127">Activities are immutable.</span></span> <span data-ttu-id="56b06-128">Sortutakoan ez dira aldatzen.</span><span class="sxs-lookup"><span data-stu-id="56b06-128">They don't change once created.</span></span>
> - <span data-ttu-id="56b06-129">Une honetan, segmentuak eta neurriak ez dira eguneratuko jarduera berrian oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="56b06-129">Currently, segments and measures won't update based on the new activity.</span></span>
> - <span data-ttu-id="56b06-130">Denbora errealeko APIaren bidez soilik gehitzen diren jarduerak ez dira esportazioen zati eta ez dira PowerBIn agertuko.</span><span class="sxs-lookup"><span data-stu-id="56b06-130">Activities added only through the real-time API are not part of exports and won't show up in PowerBI.</span></span>

<span data-ttu-id="56b06-131">Denbora errealeko APIarekin konektatzeko bi modu daude:</span><span class="sxs-lookup"><span data-stu-id="56b06-131">There are two ways to connect to the real-time API:</span></span>

- <span data-ttu-id="56b06-132">[zeharka](#connect-via-the-dynamics-365-customer-insights-connector), erabiliz [Dynamics 365 Customer Insights konektorea](https://docs.microsoft.com/connectors/customerinsights/)</span><span class="sxs-lookup"><span data-stu-id="56b06-132">[indirectly](#connect-via-the-dynamics-365-customer-insights-connector), using the [Dynamics 365 Customer Insights connector](https://docs.microsoft.com/connectors/customerinsights/)</span></span>
- <span data-ttu-id="56b06-133">[zuzenean](#connect-directly-to-the-real-time-api), kodearekin</span><span class="sxs-lookup"><span data-stu-id="56b06-133">[directly](#connect-directly-to-the-real-time-api), with code</span></span>

<span data-ttu-id="56b06-134">Bi moduek baldintza hauek betetzen dituzte:</span><span class="sxs-lookup"><span data-stu-id="56b06-134">Both ways share the following prerequisites:</span></span>

- <span data-ttu-id="56b06-135">Customer Insights ingurunea</span><span class="sxs-lookup"><span data-stu-id="56b06-135">A Customer Insights environment</span></span>
- <span data-ttu-id="56b06-136">Bezeroen profil bateratuak</span><span class="sxs-lookup"><span data-stu-id="56b06-136">Unified customer profiles</span></span>
- <span data-ttu-id="56b06-137">Konfiguratutako eta exekutatutako jarduerak</span><span class="sxs-lookup"><span data-stu-id="56b06-137">Activities configured and run</span></span>
- <span data-ttu-id="56b06-138">Laguntzailea edo administratzailea zure kontua autentifikatzeko baimenak</span><span class="sxs-lookup"><span data-stu-id="56b06-138">Contributor or Administrator permissions to authenticate your account</span></span>

## <a name="connect-via-the-dynamics-365-customer-insights-connector"></a><span data-ttu-id="56b06-139">Konektatu Dynamics 365 Customer Insights konektorea</span><span class="sxs-lookup"><span data-stu-id="56b06-139">Connect via the Dynamics 365 Customer Insights connector</span></span>

<span data-ttu-id="56b06-140">Denbora errealeko APIak dedikatu bateko datuak iren ditzake Power Platform konektorea [Dynamics 365 Customer Insights konektorea](https://docs.microsoft.com/connectors/customerinsights/), inolako koderik idatzi eta hedatu beharrik gabe.</span><span class="sxs-lookup"><span data-stu-id="56b06-140">The real-time API can ingest data from a dedicated Power Platform connector, the [Dynamics 365 Customer Insights connector](https://docs.microsoft.com/connectors/customerinsights/), without the need to write and deploy any code.</span></span>    
<span data-ttu-id="56b06-141">Lotzaileak APIaren denbora errealeko ekintzak berak egin ditzake.</span><span class="sxs-lookup"><span data-stu-id="56b06-141">The connector can do the same real-time actions as the API.</span></span> <span data-ttu-id="56b06-142">Lizentzia balioduna behar duzu prima konektoreetarako.</span><span class="sxs-lookup"><span data-stu-id="56b06-142">You need a valid license for premium connectors.</span></span> <span data-ttu-id="56b06-143">Informazio gehiagorako, ikusi [Power Apps eta Power Automate FAQ lizentziak](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq).</span><span class="sxs-lookup"><span data-stu-id="56b06-143">For more information, see [Power Apps and Power Automate licensing FAQs](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq).</span></span>

- <span data-ttu-id="56b06-144">Power Platform [Power Apps eta/edo Power Automate](https://docs.microsoft.com/connectors/)</span><span class="sxs-lookup"><span data-stu-id="56b06-144">Power Platform [Power Apps and/or Power Automate](https://docs.microsoft.com/connectors/)</span></span>
- <span data-ttu-id="56b06-145">Azure [Logic Aplikazioak](https://docs.microsoft.com/azure/connectors/apis-list)</span><span class="sxs-lookup"><span data-stu-id="56b06-145">Azure [Logic Apps](https://docs.microsoft.com/azure/connectors/apis-list)</span></span>

<span data-ttu-id="56b06-146">Fluxuak sortzeari buruzko xehetasun gehiago lortzeko, ikusi [Power Automate dokumentazioa](https://docs.microsoft.com/power-automate/).</span><span class="sxs-lookup"><span data-stu-id="56b06-146">For details about creating flows, see the [Power Automate documentation](https://docs.microsoft.com/power-automate/).</span></span>

## <a name="connect-directly-to-the-real-time-api"></a><span data-ttu-id="56b06-147">Konektatu zuzenean denbora errealeko APIarekin</span><span class="sxs-lookup"><span data-stu-id="56b06-147">Connect directly to the real-time API</span></span>

<span data-ttu-id="56b06-148">Denbora errealeko gaitasunak erabil ditzakezu zure bideratzea eraikiz eta zuzenean denbora errealeko APIarekin konektatuz.</span><span class="sxs-lookup"><span data-stu-id="56b06-148">You can use the real-time capabilities by building your own pipeline and connecting directly to the real-time API.</span></span>    
<span data-ttu-id="56b06-149">Jarduera bat sor dezakezu zure iturburu sistemaren formatuan edo UnifiedActivity formatuan.</span><span class="sxs-lookup"><span data-stu-id="56b06-149">You can post an activity in the format of your source system or in the UnifiedActivity format.</span></span> <span data-ttu-id="56b06-150">Lortu formatua API dei bat eginez /api/instantziak/{instanceId}/Kudeatu/entitate/UnifiedActivity.</span><span class="sxs-lookup"><span data-stu-id="56b06-150">Get the format by making an API call to /api/instances/{instanceId}/manage/entities/UnifiedActivity.</span></span>

<span data-ttu-id="56b06-151">API honen xehetasunak, parametroak eta erantzunak barne, hemen aurki ditzakezu: **Entitatearen datuak** sekzioan, [Customer Insights APIen erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) atalean.</span><span class="sxs-lookup"><span data-stu-id="56b06-151">Details of this API, including parameters and responses, can be found in the **EntityData** section on the [Customer Insights APIs reference](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights).</span></span> <span data-ttu-id="56b06-152">Informazio gehiago lortzeko, ikus [Customer Insights APIekin lan egin](apis.md).</span><span class="sxs-lookup"><span data-stu-id="56b06-152">For more information, see [Work with Customer Insights APIs](apis.md).</span></span>

## <a name="understand-your-real-time-usage-with-telemetry"></a><span data-ttu-id="56b06-153">Ulertu zure denbora errealeko erabilera telemetriarekin</span><span class="sxs-lookup"><span data-stu-id="56b06-153">Understand your real-time usage with telemetry</span></span>

<span data-ttu-id="56b06-154">Lortu denbora errealeko APIrako eskaeren bolumena eta sistemak izan ditzakeen arazoei buruzko informazioa.</span><span class="sxs-lookup"><span data-stu-id="56b06-154">Get an overview of the volume of requests to the real-time API and information about issues the system may encounter.</span></span> <span data-ttu-id="56b06-155">[Atzitu denbora errealeko telemetria](system.md#api-usage-tab).</span><span class="sxs-lookup"><span data-stu-id="56b06-155">You can [access the real-time telemetry](system.md#api-usage-tab).</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]