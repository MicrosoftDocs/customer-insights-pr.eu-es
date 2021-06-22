---
title: Zeregin partekatuak iragarpen agertokietarako
description: Ikasi iragarpenak kudeatzen, konpontzen eta zehazten.
ms.date: 05/17/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: diegogranados117
ms.author: digranad
manager: shellyha
ms.openlocfilehash: b935be08199f20e83bceb3317985b0e1dc120016
ms.sourcegitcommit: 6b07c9c3102761be162e4842f3c9fbc19f948a9b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/25/2021
ms.locfileid: "6095682"
---
# <a name="manage-predictions"></a><span data-ttu-id="c05c3-103">Iragarpenak kudeatu</span><span class="sxs-lookup"><span data-stu-id="c05c3-103">Manage predictions</span></span>

<span data-ttu-id="c05c3-104">Artikulu honetan iragarpen agertoki gehienek partekatzen dituzten zenbait zeregin aztertzen dira.</span><span class="sxs-lookup"><span data-stu-id="c05c3-104">This article discusses some tasks that most prediction scenarios share.</span></span>

## <a name="troubleshoot-a-failed-prediction"></a><span data-ttu-id="c05c3-105">Huts egin duen iragarpen baten arazoak konpontzea</span><span class="sxs-lookup"><span data-stu-id="c05c3-105">Troubleshoot a failed prediction</span></span>

1. <span data-ttu-id="c05c3-106">Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.</span><span class="sxs-lookup"><span data-stu-id="c05c3-106">Go to **Intelligence** > **Predictions** and select the **My predictions** tab.</span></span>

1. <span data-ttu-id="c05c3-107">Aukeratu elipseak bertikalak errore-egunkariak ikusi nahi dituzun iragarpenaren ondoan.</span><span class="sxs-lookup"><span data-stu-id="c05c3-107">Select the vertical ellipses next to the prediction you want to view error logs for.</span></span>

1. <span data-ttu-id="c05c3-108">Hautatu **Egunkariak**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-108">Select **Logs**.</span></span>

1. <span data-ttu-id="c05c3-109">Berrikusi errore guztiak.</span><span class="sxs-lookup"><span data-stu-id="c05c3-109">Review all the errors.</span></span> <span data-ttu-id="c05c3-110">Hainbat akats mota gerta daitezke eta deskribatzen dute zer baldintza eragin duen errorea.</span><span class="sxs-lookup"><span data-stu-id="c05c3-110">There are several types of errors that can occur, and they describe what condition caused the error.</span></span> <span data-ttu-id="c05c3-111">Adibidez, errore batek ez dauka datu nahikoak zehaztasunez iragartzeko ohikoa da ebaztea kargatzea datu osagarriak Customer Insights-en.</span><span class="sxs-lookup"><span data-stu-id="c05c3-111">For example, an error that there's not enough data to accurately predict is typically resolved by loading additional data into Customer Insights.</span></span>

## <a name="input-data-usability-report"></a><span data-ttu-id="c05c3-112">Sarrerako datuen erabilgarritasun-txostena</span><span class="sxs-lookup"><span data-stu-id="c05c3-112">Input data usability report</span></span>

<span data-ttu-id="c05c3-113">Sarrerako datuak erabiltzeko txostena Sarrerako datuen erabilgarritasun txostenak erabiltzeko prest dauden iragarpenek sor ditzaketen akats eta abisuen ikuspegi bateratua eskaintzen du.</span><span class="sxs-lookup"><span data-stu-id="c05c3-113">The input data usability report provides a consolidated view of the errors and warnings that your out-of-box predictions may be generating.</span></span> <span data-ttu-id="c05c3-114">Ereduaren errendimendua hobetzeko gomendioak ere ematen ditu.</span><span class="sxs-lookup"><span data-stu-id="c05c3-114">It also gives recommendations how to improve the model performance.</span></span>

<span data-ttu-id="c05c3-115">Txostena eredu batek bere prestakuntza prozesua amaitu ondoren eskuragarri dago.</span><span class="sxs-lookup"><span data-stu-id="c05c3-115">The report is available after a model has completed its training process.</span></span> <span data-ttu-id="c05c3-116">Eredu bakoitzerako bereizita sortu da, ondo osatu den edo ez kontuan hartu gabe.</span><span class="sxs-lookup"><span data-stu-id="c05c3-116">It's created for each model separately, regardless if it completed successfully or not.</span></span>

> [!NOTE]
> <span data-ttu-id="c05c3-117">Gaur egun, eginbide hau transakzioen galera-tasaren ereduan bakarrik funtzionatzen du.</span><span class="sxs-lookup"><span data-stu-id="c05c3-117">Currently, this feature only works for the Transaction Churn model.</span></span>

### <a name="view-the-input-data-usability-report"></a><span data-ttu-id="c05c3-118">Ikusi sarrerako datuen erabilgarritasun-txostena</span><span class="sxs-lookup"><span data-stu-id="c05c3-118">View the input data usability report</span></span>

<span data-ttu-id="c05c3-119">Erabiltzeko prest dagoen eredu batek prestakuntza-urratsa amaitu ondoren, ikusi txostena:</span><span class="sxs-lookup"><span data-stu-id="c05c3-119">After an out-of-box model has completed its training step, view the report:</span></span>
- <span data-ttu-id="c05c3-120">Aukeratu modeloaren izenaren ondoan dauden elipseak eta aukeratu **Sarrerako datuen erabilgarritasun txostena**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-120">Select the ellipses next to the model name and choose **Input data usability report**.</span></span>
- <span data-ttu-id="c05c3-121">Aukeratu eredu baten egoera hautatu **Ikusi Sarrerako datuak erabiltzeko txostena** alboko panelean.</span><span class="sxs-lookup"><span data-stu-id="c05c3-121">Select the status of a model select **See Input data usability report** in the side pane.</span></span>
- <span data-ttu-id="c05c3-122">Zerrendako ereduetako bat aukeratu eta hautatu **Sarrerako datuen erabilgarritasun txostena** komando barran.</span><span class="sxs-lookup"><span data-stu-id="c05c3-122">Selecting one of the models in the list and select **Input data usability report** in the command bar.</span></span>
- <span data-ttu-id="c05c3-123">Ireki ereduen emaitzen orria eta hautatu **Sarrerako datuen erabilgarritasun txostena** komando barran.</span><span class="sxs-lookup"><span data-stu-id="c05c3-123">Open the model results page and select **Input data usability report** in the command bar.</span></span>

### <a name="information-in-the-input-data-usability-report"></a><span data-ttu-id="c05c3-124">Sarrerako datuen erabilgarritasun txostenari buruzko informazioa</span><span class="sxs-lookup"><span data-stu-id="c05c3-124">Information in the input data usability report</span></span>

<span data-ttu-id="c05c3-125">Txostenaren hurrengo zutabeek informazio lagungarria dute ereduaren datuak hobetzeko.</span><span class="sxs-lookup"><span data-stu-id="c05c3-125">The following columns in the report contain helpful information to improve the data for the model.</span></span>

:::image type="content" source="media/input-data-usability-report.png" alt-text="Sarrerako datuen erabilgarritasun txostenaren adibidea, akatsak, abisuak eta gomendioak dituen taula erakusten duena.":::

- <span data-ttu-id="c05c3-127">Izena: errore, abisu edo gomendioaren izen deskribatzailea.</span><span class="sxs-lookup"><span data-stu-id="c05c3-127">Name: Descriptive name of the error, warning, or recommendation.</span></span>
- <span data-ttu-id="c05c3-128">Urratsa: ereduaren fasea, entrenamendua edo puntuazioa, informazioa aipatzen da.</span><span class="sxs-lookup"><span data-stu-id="c05c3-128">Step: Model phase, train or score, the information refers to.</span></span>
- <span data-ttu-id="c05c3-129">Egoera: informazioaren larritasuna (errorea, abisua, gomendioa).</span><span class="sxs-lookup"><span data-stu-id="c05c3-129">State: Severity of the information (error, warning, recommendation).</span></span>
- <span data-ttu-id="c05c3-130">Zutabe izena: ereduaren errendimendua hobetzeko aldatu behar den entitate bateko zutabea.</span><span class="sxs-lookup"><span data-stu-id="c05c3-130">Column name: Column in an entity that needs to be modified to improve the model performance.</span></span>
- <span data-ttu-id="c05c3-131">Entitatearen izena: ereduaren errendimendua hobetzeko aldatu behar den entitate baten izena.</span><span class="sxs-lookup"><span data-stu-id="c05c3-131">Entity name: Name of the entity that needs to be modified to improve the model performance.</span></span>
- <span data-ttu-id="c05c3-132">Xehetasunak: akatsari, abisuari edo gomendioari buruzko xehetasunak.</span><span class="sxs-lookup"><span data-stu-id="c05c3-132">Details: Details about the error, warning, or recommendation.</span></span>

## <a name="refresh-a-prediction"></a><span data-ttu-id="c05c3-133">Iragarpen bat eguneratu</span><span class="sxs-lookup"><span data-stu-id="c05c3-133">Refresh a prediction</span></span>

<span data-ttu-id="c05c3-134">Aurreikuspenak automatikoki berritu egingo dira [programatu zure datuak freskatzea](system.md#schedule-tab) ezarpenetan konfiguratuta.</span><span class="sxs-lookup"><span data-stu-id="c05c3-134">Predictions will automatically refresh on the same [schedule your data refreshes](system.md#schedule-tab) as configured in settings.</span></span> <span data-ttu-id="c05c3-135">Eskuz freskatu ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="c05c3-135">You can refresh them manually too.</span></span>

1. <span data-ttu-id="c05c3-136">Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.</span><span class="sxs-lookup"><span data-stu-id="c05c3-136">Go to **Intelligence** > **Predictions** and select the **My predictions** tab.</span></span>

1. <span data-ttu-id="c05c3-137">Hautatu freskatu nahi duzun iragarpenaren ondoan elipsi bertikalak.</span><span class="sxs-lookup"><span data-stu-id="c05c3-137">Select the vertical ellipses next to the prediction you want to refresh.</span></span>

1. <span data-ttu-id="c05c3-138">Aukeratu **Freskatu**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-138">Select **Refresh**.</span></span>

## <a name="delete-a-prediction"></a><span data-ttu-id="c05c3-139">Ezabatu iragarpena</span><span class="sxs-lookup"><span data-stu-id="c05c3-139">Delete a prediction</span></span>

<span data-ttu-id="c05c3-140">Iragarpen ezabatzeak bere irteerako entitatea ere kentzen du.</span><span class="sxs-lookup"><span data-stu-id="c05c3-140">Deleting a prediction also removes its output entity.</span></span>

1. <span data-ttu-id="c05c3-141">Joan **Adimena** > **Iragarpenak** atalera eta hautatu **Nire iragarpenak** fitxa.</span><span class="sxs-lookup"><span data-stu-id="c05c3-141">Go to **Intelligence** > **Predictions** and select the **My predictions** tab.</span></span>

1. <span data-ttu-id="c05c3-142">Hautatu ezabatu nahi duzun iragarpenaren ondoan elipsi bertikalak.</span><span class="sxs-lookup"><span data-stu-id="c05c3-142">Select the vertical ellipses next to the prediction you want to delete.</span></span>

1. <span data-ttu-id="c05c3-143">Hautatu **Ezabatu**.</span><span class="sxs-lookup"><span data-stu-id="c05c3-143">Select **Delete**.</span></span>
