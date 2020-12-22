---
title: Aberastu bezeroen profil bateratuak
description: Erabili gaitasunak zure bezeroaren datuak aberasteko.
ms.date: 11/02/2020
ms.reviewer: kishorem
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: c25cfbf3808fc1534b54d2d834f1c63ff4c9fe0a
ms.sourcegitcommit: 334633cbd58f5659d20b4f87252c1a10cc7130db
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/03/2020
ms.locfileid: "4667079"
---
# <a name="enrichment-for-customer-profiles-preview"></a><span data-ttu-id="e7516-103">Bezeroen profiletarako aberastea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="e7516-103">Enrichment for customer profiles (preview)</span></span>

<span data-ttu-id="e7516-104">Erabili Microsoft eta beste bazkide batzuen iturrietako datuak bezeroaren datuak aberasteko.</span><span class="sxs-lookup"><span data-stu-id="e7516-104">Use data from sources like Microsoft and other partners to enrich your customer data.</span></span>

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Aberasteko gunearen orria":::

<span data-ttu-id="e7516-106">Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** aberasteko aukerekin lan egiteko.</span><span class="sxs-lookup"><span data-stu-id="e7516-106">In audience insights, go to **Data** > **Enrichment** to work with enrichment options.</span></span>    
<span data-ttu-id="e7516-107">Laguntzaileak edo Administratzaileak baimenak izan behar dituzu aberastasunak sortzeko edo editatzeko.</span><span class="sxs-lookup"><span data-stu-id="e7516-107">You need to have Contributor or Administrator permissions to create or edit enrichments.</span></span> <span data-ttu-id="e7516-108">Informazio gehiago lortzeko, [Baimenak](permissions.md).</span><span class="sxs-lookup"><span data-stu-id="e7516-108">For more information, see [Permissions](permissions.md).</span></span>

<span data-ttu-id="e7516-109">Gainean **Ezagutu** fitxa, aberastasun hauek aurkituko dituzu:</span><span class="sxs-lookup"><span data-stu-id="e7516-109">On the **Discover** tab, you'll find the following enrichments:</span></span>

- <span data-ttu-id="e7516-110">[Markak](enrichment-microsoft-graph.md) emanda Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e7516-110">[Brands](enrichment-microsoft-graph.md) provided by Microsoft Graph</span></span>
- <span data-ttu-id="e7516-111">[Interesak](enrichment-microsoft-graph.md) emanak Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="e7516-111">[Interests](enrichment-microsoft-graph.md) provided by Microsoft Graph</span></span>
- <span data-ttu-id="e7516-112">[Enpresaren datuak](enrichment-leadspace.md) , Leadspace-k emanak</span><span class="sxs-lookup"><span data-stu-id="e7516-112">[Company data](enrichment-leadspace.md) provided by Leadspace</span></span>
- <span data-ttu-id="e7516-113">[Demografiak](enrichment-experian.md) hornituta daude Experian-ek</span><span class="sxs-lookup"><span data-stu-id="e7516-113">[Demographics](enrichment-experian.md) provided by Experian</span></span>
- <span data-ttu-id="e7516-114">[Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak</span><span class="sxs-lookup"><span data-stu-id="e7516-114">[Location data](enrichment-here.md) provided by HERE Technologies</span></span>
- <span data-ttu-id="e7516-115">[Datu pertsonalizatuak](enrichment-SFTP-custom-import.md) fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) bidez</span><span class="sxs-lookup"><span data-stu-id="e7516-115">[Custom data](enrichment-SFTP-custom-import.md) through Secure File Transfer Protocol (SFTP)</span></span>

<span data-ttu-id="e7516-116">Gainean **Nire aberastasunak** fitxan, konfiguratutako aberastasunak eta haien propietateak editatzen ikus ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="e7516-116">On the **My enrichments** tab, you can see the enrichments you've configured and edit their properties.</span></span>

## <a name="manage-existing-enrichments"></a><span data-ttu-id="e7516-117">Lehendik dauden aberastasunak kudeatu</span><span class="sxs-lookup"><span data-stu-id="e7516-117">Manage existing enrichments</span></span>

<span data-ttu-id="e7516-118">Joan **Nire aberastasunak** konfiguratutako aberastasun guztiak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="e7516-118">Go to the **My enrichments** to see all configured enrichments.</span></span> <span data-ttu-id="e7516-119">Aberastu bakoitza aberastearen inguruko informazio osagarria biltzen duen errenkada gisa irudikatzen da.</span><span class="sxs-lookup"><span data-stu-id="e7516-119">Each enrichment is represented as a row that includes additional information about the enrichment.</span></span>

<span data-ttu-id="e7516-120">Aukeratu aberastasuna eskuragarri dauden aukerak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="e7516-120">Select an enrichment to see the available options.</span></span> <span data-ttu-id="e7516-121">Bestela, zerrendako elementu bateko elipsia (...) aukera dezakezu aukerak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="e7516-121">Alternatively, you can select the ellipsis (...) on a list item to see the options.</span></span>

:::image type="content" source="media/enrichment-hub-options-run.png" alt-text="Aberastasunen zerrendan aberastasunak kudeatzeko aukerak":::

- <span data-ttu-id="e7516-123">**ikusi** aberastasun xehetasunak bezeroen profil aberastuen kopuruarekin.</span><span class="sxs-lookup"><span data-stu-id="e7516-123">**View** enrichment details with the number of enriched customer profiles.</span></span>
- <span data-ttu-id="e7516-124">**Editatu** aberastasunaren konfigurazioa.</span><span class="sxs-lookup"><span data-stu-id="e7516-124">**Edit** the enrichment configuration.</span></span>
- <span data-ttu-id="e7516-125">**Korrika egin** bezeroen profilak azken datuekin eguneratzeko aberastasuna.</span><span class="sxs-lookup"><span data-stu-id="e7516-125">**Run** the enrichment to update customer profiles with the latest data.</span></span>
- <span data-ttu-id="e7516-126">**Desaktibatu** lehendik dagoen aberastasuna programatutako freskatze automatikoekin automatikoki freskatzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="e7516-126">**Deactivate** an existing enrichment to stop it from refreshing automatically with every scheduled refresh.</span></span> <span data-ttu-id="e7516-127">Azken freskatze arrakastatsuaren datuak erabilgarri egongo dira.</span><span class="sxs-lookup"><span data-stu-id="e7516-127">Data from the last successful refresh will continue to be available.</span></span> <span data-ttu-id="e7516-128">**Aktibatu** aberastu aktiboa, freskatze automatikoa programatutako freskapen guztiekin berrabiarazteko.</span><span class="sxs-lookup"><span data-stu-id="e7516-128">**Activate** an inactive enrichment to restart automatic refreshing with every scheduled refresh.</span></span>
- <span data-ttu-id="e7516-129">**Ezabatu** aberastea.</span><span class="sxs-lookup"><span data-stu-id="e7516-129">**Delete** an enrichment.</span></span>

<span data-ttu-id="e7516-130">Aberastasun anitz exekutatu edo desaktiba ditzakezu aldi berean zerrendan hautatuta.</span><span class="sxs-lookup"><span data-stu-id="e7516-130">You can run or deactivate multiple enrichments at once by selecting them in the list.</span></span> <span data-ttu-id="e7516-131">Ikusi eta editatzeko aukerak ez daude eskuragarri gisa eta soilik aberasteko soilik funtzionatzen du.</span><span class="sxs-lookup"><span data-stu-id="e7516-131">View and edit options aren't available as bulk action and only work for one enrichment at a time.</span></span>
