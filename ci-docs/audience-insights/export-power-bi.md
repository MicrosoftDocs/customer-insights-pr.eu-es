---
title: Power BI konektorea
description: Ikusi nola erabili laguntzailearen estudioa Dynamics 365 Customer Insights konektorea Power BI-n.
ms.date: 09/21/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: e43e2f9dbc84ebfbf2154990a752740f973296cb
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596024"
---
# <a name="connector-for-power-bi-preview"></a><span data-ttu-id="f84f2-103">Konektorea Power BI-rako (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="f84f2-103">Connector for Power BI (preview)</span></span>

<span data-ttu-id="f84f2-104">Sortu zure datuentzako bistaratzeak Power BI Desktop-ekin.</span><span class="sxs-lookup"><span data-stu-id="f84f2-104">Create visualizations for your data with the Power BI Desktop.</span></span> <span data-ttu-id="f84f2-105">Sortu ikuspegi gehiago eta sortu txostenak zure bezeroen datu bateratuekin.</span><span class="sxs-lookup"><span data-stu-id="f84f2-105">Generate additional insights and build reports with your unified customer data.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f84f2-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="f84f2-106">Prerequisites</span></span>

- <span data-ttu-id="f84f2-107">Bezeroen profil bateratuak dituzu.</span><span class="sxs-lookup"><span data-stu-id="f84f2-107">You have unified customer profiles.</span></span>
- <span data-ttu-id="f84f2-108">Bertsioaren azken bertsioa [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) zure ordenagailuan instalatuta dago.</span><span class="sxs-lookup"><span data-stu-id="f84f2-108">The latest version of [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) is installed on your computer.</span></span> <span data-ttu-id="f84f2-109">[Lortu hauei buruzko informazio gehiago: Power BI Desktop](/power-bi/desktop-what-is-desktop)</span><span class="sxs-lookup"><span data-stu-id="f84f2-109">[Learn more about Power BI Desktop](/power-bi/desktop-what-is-desktop).</span></span>

## <a name="configure-the-connector-for-power-bi"></a><span data-ttu-id="f84f2-110">Konfiguratu konektorea Power BI</span><span class="sxs-lookup"><span data-stu-id="f84f2-110">Configure the connector for Power BI</span></span>

1. <span data-ttu-id="f84f2-111">Power BI Desktop hautatu **Fitxategia** > **Lortu datuak**.</span><span class="sxs-lookup"><span data-stu-id="f84f2-111">In Power BI Desktop, select **File** > **Get Data**.</span></span>

1. <span data-ttu-id="f84f2-112">Hautatu **Ikusi gehiago** eta bilatu **Dynamics 365 Customer Insights**</span><span class="sxs-lookup"><span data-stu-id="f84f2-112">Select **See more** and search for **Dynamics 365 Customer Insights**</span></span>

1. <span data-ttu-id="f84f2-113">Hautatu **Konektatu**.</span><span class="sxs-lookup"><span data-stu-id="f84f2-113">Select **Connect**.</span></span>

1. <span data-ttu-id="f84f2-114">**saioa hasi** Customer Insights-erako erabiltzen duzun antolakuntza-kontu bera daukazu eta hautatu **konektatu**.</span><span class="sxs-lookup"><span data-stu-id="f84f2-114">**Sign in** with the same organizational account you use for Customer Insights and select **Connect**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="f84f2-115">Urrats honetan adierazten duzun kontua Customer Insights-etik datuak eskuratzeko erabiltzen da eta ez du zertan saioa hasita duzun bera izan behar Power BI.</span><span class="sxs-lookup"><span data-stu-id="f84f2-115">The account you indicate in this step is used to fetch data from Customer Insights and doesn't need to be the same you are signed in to Power BI.</span></span> <span data-ttu-id="f84f2-116">Datuak eskuratzeko erabiltzen den kontua berrezartzeko, ireki Power BI eta joan hona: **Fitxategia** > **Aukerak** > **Ezarpenak** > **Datu-iturburuen ezarpenak**.</span><span class="sxs-lookup"><span data-stu-id="f84f2-116">To reset the account that is used for data fetching, open Power BI and go to **File** > **Options** > **Settings** > **Data source settings**.</span></span> <span data-ttu-id="f84f2-117">Datu iturrien zerrendan, hautatu **Dynamics 365 Customer Insights Saioa hasi** eta hautatu **Garbitu baimenak**.</span><span class="sxs-lookup"><span data-stu-id="f84f2-117">In the list of data sources, select **Dynamics 365 Customer Insights Login** and select **Clear permissions**.</span></span>  

1. <span data-ttu-id="f84f2-118">**Nabigatzailea** elkarrizketa-koadroa.</span><span class="sxs-lookup"><span data-stu-id="f84f2-118">In the **Navigator** dialog box.</span></span> <span data-ttu-id="f84f2-119">sarbidea duzun ingurune guztien zerrenda ikusiko duzu.</span><span class="sxs-lookup"><span data-stu-id="f84f2-119">you see the list of all environments you have access to.</span></span> <span data-ttu-id="f84f2-120">Zabaldu ingurune bat eta ireki edozein karpeta (entitateak, neurriak, segmentuak, aberasteak).</span><span class="sxs-lookup"><span data-stu-id="f84f2-120">Expand an environment and open any of the folders (entities, measures, segments, enrichments).</span></span> <span data-ttu-id="f84f2-121">Adibidez, ireki **Entitateak** karpeta, inporta ditzakezun entitate guztiak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="f84f2-121">For example, open the **Entities** folder, to see all entities you can import.</span></span>

   <span data-ttu-id="f84f2-122">![Power BI Konektagailuaren nabigatzailea](media/power-bi-navigator.png "Power BI Konektagailuaren nabigatzailea")</span><span class="sxs-lookup"><span data-stu-id="f84f2-122">![Power BI Connector Navigator](media/power-bi-navigator.png "Power BI Connector Navigator")</span></span>

1. <span data-ttu-id="f84f2-123">Hautatu sartu beharreko entitateen ondoko kontrol laukiak **kargatu**.</span><span class="sxs-lookup"><span data-stu-id="f84f2-123">Select the check boxes next to the entities to include and **Load**.</span></span> <span data-ttu-id="f84f2-124">Hainbat entitate hautatu ahalko dituzu, ingurune anitzetan.</span><span class="sxs-lookup"><span data-stu-id="f84f2-124">You can select multiple entities from multiple environments.</span></span>

1. <span data-ttu-id="f84f2-125">Entitateak kargatzen dituzun bitartean, kargatzeko elkarrizketa-koadroa ikusiko duzu.</span><span class="sxs-lookup"><span data-stu-id="f84f2-125">You'll see a loading dialog box while your entities are loaded.</span></span> <span data-ttu-id="f84f2-126">Aukeratutako entitate guztiak kargatu ondoren, Power BI-ren gaitasunak erabil ditzakezu datuak bistaratzeko.</span><span class="sxs-lookup"><span data-stu-id="f84f2-126">Once all of your selected entities have loaded, you can use the capabilities of Power BI to visualize the data.</span></span>

## <a name="large-data-sets"></a><span data-ttu-id="f84f2-127">Datu multzo handiak</span><span class="sxs-lookup"><span data-stu-id="f84f2-127">Large data sets</span></span>

<span data-ttu-id="f84f2-128">Customer Insights konektorea Power BI bezeroentzako milioi bat profil dituzten datu multzoetarako lan egiteko diseinatuta dago.</span><span class="sxs-lookup"><span data-stu-id="f84f2-128">The Customer Insights connector for Power BI is designed to work for data sets that contain up to 1 million customer profiles.</span></span> <span data-ttu-id="f84f2-129">Datu multzo handiagoak inportatzeak funtziona dezake, baina denbora asko behar da.</span><span class="sxs-lookup"><span data-stu-id="f84f2-129">Importing larger data sets may work, but it takes a long time.</span></span> <span data-ttu-id="f84f2-130">Gainera, prozesuak denbora-muga izan dezake Power BI mugak.</span><span class="sxs-lookup"><span data-stu-id="f84f2-130">Additionally, the process could run into a time-out because of Power BI limitations.</span></span> <span data-ttu-id="f84f2-131">Informazio gehiagorako, ikus [Power BI: Datu multzo handien gomendioak](/power-bi/admin/service-premium-what-is#large-datasets).</span><span class="sxs-lookup"><span data-stu-id="f84f2-131">For more information, see [Power BI: Recommendations for large data sets](/power-bi/admin/service-premium-what-is#large-datasets).</span></span> 

### <a name="work-with-a-subset-of-data"></a><span data-ttu-id="f84f2-132">Lan egin datu azpimultzo batekin</span><span class="sxs-lookup"><span data-stu-id="f84f2-132">Work with a subset of data</span></span>

<span data-ttu-id="f84f2-133">Kontuan hartu zure datuen azpimultzo batekin lan egitea.</span><span class="sxs-lookup"><span data-stu-id="f84f2-133">Consider working with a subset of your data.</span></span> <span data-ttu-id="f84f2-134">Adibidez, [segmentuak](segments.md) sor ditzakezu bezeroaren erregistro guztiak Power BI-ra esportatu beharrean.</span><span class="sxs-lookup"><span data-stu-id="f84f2-134">For example, you can create [segments](segments.md) instead of exporting all customer records to Power BI.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="f84f2-135">Arazoak konpontzea</span><span class="sxs-lookup"><span data-stu-id="f84f2-135">Troubleshooting</span></span>

### <a name="customer-insights-environment-doesnt-show-in-power-bi"></a><span data-ttu-id="f84f2-136">Customer Insights ingurunea ez da agertzen Power BI-n</span><span class="sxs-lookup"><span data-stu-id="f84f2-136">Customer Insights environment doesn't show in Power BI</span></span>

<span data-ttu-id="f84f2-137">Bat baino gehiago dituzten inguruneak [erlazioa](relationships.md) ikusleen estatistiketan bi entitate berdinen artean definitutakoak ez dira erabilgarri egongo Power BI konektorea.</span><span class="sxs-lookup"><span data-stu-id="f84f2-137">Environments that have more than one [relationship](relationships.md) defined between two identical entities in audience insights will not be available in the Power BI connector.</span></span>

<span data-ttu-id="f84f2-138">Bikoiztutako harremanak identifikatu eta kendu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="f84f2-138">You can identify and remove the duplicated relationships.</span></span>

1. <span data-ttu-id="f84f2-139">Ikusleen ikuspegietan, joan hona **Datuak** > **Erlazioak** falta zaizun inguruneari buruz Power BI-n.</span><span class="sxs-lookup"><span data-stu-id="f84f2-139">In audience insights, go to **Data** > **Relationships** on the environment you're missing in Power BI.</span></span>
2. <span data-ttu-id="f84f2-140">Bikoiztutako harremanak identifikatu:</span><span class="sxs-lookup"><span data-stu-id="f84f2-140">Identify duplicated relationships:</span></span>
   - <span data-ttu-id="f84f2-141">Egiaztatu bi entitate berdinen artean erlazio bat baino gehiago definitzen den.</span><span class="sxs-lookup"><span data-stu-id="f84f2-141">Check if there is more than one relationship defined between the same two entities.</span></span>
   - <span data-ttu-id="f84f2-142">Egiaztatu batasun prozesuan sartutako bi entitateen artean sortutako erlaziorik dagoen.</span><span class="sxs-lookup"><span data-stu-id="f84f2-142">Check if there is a relationship created between two entities that are both included in the unification process.</span></span> <span data-ttu-id="f84f2-143">Bateratze prozesuan sartutako entitate guztien artean harreman inplizitua dago definituta.</span><span class="sxs-lookup"><span data-stu-id="f84f2-143">There is an implicit relationship defined between all entities included in the unification process.</span></span>
3. <span data-ttu-id="f84f2-144">Kendu identifikatutako harreman bikoiztuak.</span><span class="sxs-lookup"><span data-stu-id="f84f2-144">Remove any duplicate relationships identified.</span></span>

<span data-ttu-id="f84f2-145">Bikoiztutako harremanak kendu ondoren, saiatu konfiguratzen Power BI konektorea berriro.</span><span class="sxs-lookup"><span data-stu-id="f84f2-145">After removal of the duplicated relationships, try to configure the Power BI connector again.</span></span> <span data-ttu-id="f84f2-146">Ingurumena erabilgarri egon beharko litzateke orain.</span><span class="sxs-lookup"><span data-stu-id="f84f2-146">The environment should be available now.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]