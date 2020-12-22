---
title: Power BI konektorea
description: Ikusi nola erabili laguntzailearen estudioa Dynamics 365 Customer Insights konektorea Power BI-n.
ms.date: 09/21/2020
ms.reviewer: sthe
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: d497ca779a337c512a7254524f597cff226bcb45
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404957"
---
# <a name="connector-for-power-bi-preview"></a><span data-ttu-id="7a6b7-103">Konektorea Power BI-rako (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="7a6b7-103">Connector for Power BI (preview)</span></span>

<span data-ttu-id="7a6b7-104">Sortu zure datuentzako bistaratzeak Power BI Desktop-ekin.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-104">Create visualizations for your data with the Power BI Desktop.</span></span> <span data-ttu-id="7a6b7-105">Sortu ikuspegi gehiago eta sortu txostenak zure bezeroen datu bateratuekin.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-105">Generate additional insights and build reports with your unified customer data.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7a6b7-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="7a6b7-106">Prerequisites</span></span>

- <span data-ttu-id="7a6b7-107">Bezeroen profil bateratuak dituzu.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-107">You have unified customer profiles.</span></span>
- <span data-ttu-id="7a6b7-108">Bertsioaren azken bertsioa [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) zure ordenagailuan instalatuta dago.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-108">The latest version of [Microsoft Power BI Desktop](https://powerbi.microsoft.com/desktop/) is installed on your computer.</span></span> <span data-ttu-id="7a6b7-109">[Lortu hauei buruzko informazio gehiago: Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-what-is-desktop)</span><span class="sxs-lookup"><span data-stu-id="7a6b7-109">[Learn more about Power BI Desktop](https://docs.microsoft.com/power-bi/desktop-what-is-desktop).</span></span>

## <a name="configure-the-connector-for-power-bi"></a><span data-ttu-id="7a6b7-110">Konfiguratu konektorea Power BI</span><span class="sxs-lookup"><span data-stu-id="7a6b7-110">Configure the connector for Power BI</span></span>

1. <span data-ttu-id="7a6b7-111">Power BI Desktop hautatu **Fitxategia** > **Lortu datuak**.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-111">In Power BI Desktop, select **File** > **Get Data**.</span></span>

1. <span data-ttu-id="7a6b7-112">Hautatu **Ikusi gehiago** eta bilatu **Dynamics 365 Customer Insights**</span><span class="sxs-lookup"><span data-stu-id="7a6b7-112">Select **See more** and search for **Dynamics 365 Customer Insights**</span></span>

1. <span data-ttu-id="7a6b7-113">Aukeratu emaitza eta hautatu **konektatu**.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-113">Select the result and select **Connect**.</span></span>

1. <span data-ttu-id="7a6b7-114">**saioa hasi** Customer Insights-erako erabiltzen duzun antolakuntza-kontu bera daukazu eta hautatu **konektatu**.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-114">**Sign in** with the same organizational account you use for Customer Insights and select **Connect**.</span></span>
   > [!NOTE]
   > <span data-ttu-id="7a6b7-115">Urrats honetan adierazten duzun kontua Customer Insights-etik datuak eskuratzeko erabiltzen da eta ez du zertan saioa hasita duzun bera izan behar Power BI.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-115">The account you indicate in this step is used to fetch data from Customer Insights and doesn't need to be the same you are signed in to Power BI.</span></span> <span data-ttu-id="7a6b7-116">Datuak eskuratzeko erabiltzen den kontua berrezartzeko, ireki Power BI eta joan hona: **Fitxategia** > **Aukerak** > **Ezarpenak** > **Datu-iturburuen ezarpenak**.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-116">To reset the account that is used for data fetching, open Power BI and go to **File** > **Options** > **Settings** > **Data source settings**.</span></span> <span data-ttu-id="7a6b7-117">Datu iturrien zerrendan, hautatu **Dynamics 365 Customer Insights Saioa hasi** eta hautatu **Garbitu baimenak**.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-117">In the list of data sources, select **Dynamics 365 Customer Insights Login** and select **Clear permissions**.</span></span>  

1. <span data-ttu-id="7a6b7-118">**Nabigatzailea** elkarrizketa-koadroa.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-118">In the **Navigator** dialog box.</span></span> <span data-ttu-id="7a6b7-119">sarbidea duzun ingurune guztien zerrenda ikusiko duzu.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-119">you see the list of all environments you have access to.</span></span> <span data-ttu-id="7a6b7-120">Zabaldu ingurune bat eta ireki edozein karpeta (entitateak, neurriak, segmentuak, aberasteak).</span><span class="sxs-lookup"><span data-stu-id="7a6b7-120">Expand an environment and open any of the folders (entities, measures, segments, enrichments).</span></span> <span data-ttu-id="7a6b7-121">Adibidez, ireki **Entitateak** karpeta, inporta ditzakezun entitate guztiak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-121">For example, open the **Entities** folder, to see all entities you can import.</span></span>

   <span data-ttu-id="7a6b7-122">![Power BI Konektagailuaren nabigatzailea](media/power-bi-navigator.png "Power BI Konektagailuaren nabigatzailea")</span><span class="sxs-lookup"><span data-stu-id="7a6b7-122">![Power BI Connector Navigator](media/power-bi-navigator.png "Power BI Connector Navigator")</span></span>

1. <span data-ttu-id="7a6b7-123">Hautatu sartu beharreko entitateen ondoko kontrol laukiak **kargatu**.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-123">Select the check boxes next to the entities to include and **Load**.</span></span> <span data-ttu-id="7a6b7-124">Hainbat entitate hautatu ahalko dituzu, ingurune anitzetan.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-124">You can select multiple entities from multiple environments.</span></span>

1. <span data-ttu-id="7a6b7-125">Entitateak kargatzen dituzun bitartean, kargatzeko elkarrizketa-koadroa ikusiko duzu.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-125">You'll see a loading dialog box while your entities are loaded.</span></span> <span data-ttu-id="7a6b7-126">Aukeratutako entitate guztiak kargatu ondoren, Power BI-ren gaitasunak erabil ditzakezu datuak bistaratzeko.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-126">Once all of your selected entities have loaded, you can use the capabilities of Power BI to visualize the data.</span></span>

## <a name="large-data-sets"></a><span data-ttu-id="7a6b7-127">Datu multzo handiak</span><span class="sxs-lookup"><span data-stu-id="7a6b7-127">Large data sets</span></span>

<span data-ttu-id="7a6b7-128">Customer Insights konektorea Power BI bezeroentzako milioi bat profil dituzten datu multzoetarako lan egiteko diseinatuta dago.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-128">The Customer Insights connector for Power BI is designed to work for data sets that contain up to 1 million customer profiles.</span></span> <span data-ttu-id="7a6b7-129">Datu multzo handiagoak inportatzeak funtziona dezake, baina denbora asko behar da.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-129">Importing larger data sets may work, but it takes a long time.</span></span> <span data-ttu-id="7a6b7-130">Gainera, prozesuak denbora-muga izan dezake Power BI mugak.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-130">Additionally, the process could run into a time-out because of Power BI limitations.</span></span> <span data-ttu-id="7a6b7-131">Informazio gehiagorako, ikus [Power BI: Datu multzo handien gomendioak](https://docs.microsoft.com/power-bi/admin/service-premium-what-is#large-datasets).</span><span class="sxs-lookup"><span data-stu-id="7a6b7-131">For more information, see [Power BI: Recommendations for large data sets](https://docs.microsoft.com/power-bi/admin/service-premium-what-is#large-datasets).</span></span> 

### <a name="work-with-a-subset-of-data"></a><span data-ttu-id="7a6b7-132">Lan egin datu azpimultzo batekin</span><span class="sxs-lookup"><span data-stu-id="7a6b7-132">Work with a subset of data</span></span>

<span data-ttu-id="7a6b7-133">Kontuan hartu zure datuen azpimultzo batekin lan egitea.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-133">Consider working with a subset of your data.</span></span> <span data-ttu-id="7a6b7-134">Adibidez, [segmentuak](segments.md) sor ditzakezu bezeroaren erregistro guztiak Power BI-ra esportatu beharrean.</span><span class="sxs-lookup"><span data-stu-id="7a6b7-134">For example, you can create [segments](segments.md) instead of exporting all customer records to Power BI.</span></span>
