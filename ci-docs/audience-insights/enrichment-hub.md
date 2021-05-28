---
title: Aberastu bezeroen profil bateratuak
description: Erabili gaitasunak zure bezeroaren datuak aberasteko.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: c8e4a7247ccf575a62440038180010916b09d51b
ms.sourcegitcommit: f9e2fa3f11ecf11a5d9cccc376fdeb1ecea54880
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "5954472"
---
# <a name="enrichment-for-customer-profiles-preview"></a><span data-ttu-id="1c646-103">Bezeroen profiletarako aberastea (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="1c646-103">Enrichment for customer profiles (preview)</span></span>

<span data-ttu-id="1c646-104">Erabili Microsoft eta beste bazkide batzuen iturrietako datuak bezeroaren datuak aberasteko.</span><span class="sxs-lookup"><span data-stu-id="1c646-104">Use data from sources like Microsoft and other partners to enrich your customer data.</span></span>

:::image type="content" source="media/enrichment-hub-page.png" alt-text="Aberasteko gunearen orria":::

<span data-ttu-id="1c646-106">Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** aberasteko aukerekin lan egiteko.</span><span class="sxs-lookup"><span data-stu-id="1c646-106">In audience insights, go to **Data** > **Enrichment** to work with enrichment options.</span></span>    
<span data-ttu-id="1c646-107">Laguntzaileak edo Administratzaileak baimenak izan behar dituzu aberastasunak sortzeko edo editatzeko.</span><span class="sxs-lookup"><span data-stu-id="1c646-107">You need to have Contributor or Administrator permissions to create or edit enrichments.</span></span> <span data-ttu-id="1c646-108">Informazio gehiago lortzeko, [Baimenak](permissions.md).</span><span class="sxs-lookup"><span data-stu-id="1c646-108">For more information, see [Permissions](permissions.md).</span></span>

<span data-ttu-id="1c646-109">Gainean **Ezagutu** fitxa, aberastasun hauek aurkituko dituzu:</span><span class="sxs-lookup"><span data-stu-id="1c646-109">On the **Discover** tab, you'll find the following enrichments:</span></span>

- <span data-ttu-id="1c646-110">[Markak](enrichment-microsoft.md) hornituta Microsoft-en arabera</span><span class="sxs-lookup"><span data-stu-id="1c646-110">[Brands](enrichment-microsoft.md) provided by Microsoft</span></span>
- <span data-ttu-id="1c646-111">[Interesak](enrichment-microsoft.md) hornituta Microsoft-en arabera</span><span class="sxs-lookup"><span data-stu-id="1c646-111">[Interests](enrichment-microsoft.md) provided by Microsoft</span></span>
- <span data-ttu-id="1c646-112">[Helbide hobetuak](enrichment-enhanced-addresses.md) Microsoft-ek eskainita</span><span class="sxs-lookup"><span data-stu-id="1c646-112">[Enhanced addresses](enrichment-enhanced-addresses.md) provided by Microsoft</span></span>
- <span data-ttu-id="1c646-113">[Enpresaren datuak](enrichment-leadspace.md) , Leadspace-k emanak</span><span class="sxs-lookup"><span data-stu-id="1c646-113">[Company data](enrichment-leadspace.md) provided by Leadspace</span></span>
- <span data-ttu-id="1c646-114">[Demografiak](enrichment-experian.md) hornituta daude Experian-ek</span><span class="sxs-lookup"><span data-stu-id="1c646-114">[Demographics](enrichment-experian.md) provided by Experian</span></span>
- <span data-ttu-id="1c646-115">[Kokapen datuak](enrichment-here.md) HERE Technologies-ek emanak</span><span class="sxs-lookup"><span data-stu-id="1c646-115">[Location data](enrichment-here.md) provided by HERE Technologies</span></span>
- <span data-ttu-id="1c646-116">[Datu pertsonalizatuak](enrichment-SFTP-custom-import.md) fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) bidez</span><span class="sxs-lookup"><span data-stu-id="1c646-116">[Custom data](enrichment-SFTP-custom-import.md) through Secure File Transfer Protocol (SFTP)</span></span>

<span data-ttu-id="1c646-117">Gainean **Nire aberastasunak** fitxan, konfiguratutako aberastasunak eta haien propietateak editatzen ikus ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="1c646-117">On the **My enrichments** tab, you can see the enrichments you've configured and edit their properties.</span></span>

## <a name="manage-existing-enrichments"></a><span data-ttu-id="1c646-118">Lehendik dauden aberastasunak kudeatu</span><span class="sxs-lookup"><span data-stu-id="1c646-118">Manage existing enrichments</span></span>

<span data-ttu-id="1c646-119">Joan **Nire aberastasunak** konfiguratutako aberastasun guztiak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="1c646-119">Go to the **My enrichments** to see all configured enrichments.</span></span> <span data-ttu-id="1c646-120">Aberastu bakoitza aberastearen inguruko informazio osagarria biltzen duen errenkada gisa irudikatzen da.</span><span class="sxs-lookup"><span data-stu-id="1c646-120">Each enrichment is represented as a row that includes additional information about the enrichment.</span></span>

<span data-ttu-id="1c646-121">Aukeratu aberastasuna eskuragarri dauden aukerak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="1c646-121">Select an enrichment to see the available options.</span></span> <span data-ttu-id="1c646-122">Zerrenda bateko elipsia (...) ere hauta dezakezu aukerak ikusteko.</span><span class="sxs-lookup"><span data-stu-id="1c646-122">You can also select the ellipsis (...) on a list item to see the options.</span></span>

:::image type="content" source="media/enrichment-hub-options-run.png" alt-text="Aberastasunen zerrendan aberastasunak kudeatzeko aukerak":::

- <span data-ttu-id="1c646-124">**ikusi** aberastasun xehetasunak bezeroen profil aberastuen kopuruarekin.</span><span class="sxs-lookup"><span data-stu-id="1c646-124">**View** enrichment details with the number of enriched customer profiles.</span></span>
- <span data-ttu-id="1c646-125">**Editatu** aberastasunaren konfigurazioa.</span><span class="sxs-lookup"><span data-stu-id="1c646-125">**Edit** the enrichment configuration.</span></span>
- <span data-ttu-id="1c646-126">**Korrika egin** bezeroen profilak azken datuekin eguneratzeko aberastasuna.</span><span class="sxs-lookup"><span data-stu-id="1c646-126">**Run** the enrichment to update customer profiles with the latest data.</span></span>
- <span data-ttu-id="1c646-127">**Desaktibatu** lehendik dagoen aberastasuna programatutako freskatze automatikoekin automatikoki freskatzeari uzteko.</span><span class="sxs-lookup"><span data-stu-id="1c646-127">**Deactivate** an existing enrichment to stop it from refreshing automatically with every scheduled refresh.</span></span> <span data-ttu-id="1c646-128">Azken freskatze arrakastatsuaren datuak erabilgarri egongo dira.</span><span class="sxs-lookup"><span data-stu-id="1c646-128">Data from the last successful refresh will continue to be available.</span></span> <span data-ttu-id="1c646-129">**Aktibatu** aberastu aktiboa, freskatze automatikoa programatutako freskapen guztiekin berrabiarazteko.</span><span class="sxs-lookup"><span data-stu-id="1c646-129">**Activate** an inactive enrichment to restart automatic refreshing with every scheduled refresh.</span></span>
- <span data-ttu-id="1c646-130">**Ezabatu** aberastea.</span><span class="sxs-lookup"><span data-stu-id="1c646-130">**Delete** an enrichment.</span></span>

<span data-ttu-id="1c646-131">Aberastasun anitz exekutatu edo desaktiba ditzakezu aldi berean zerrendan hautatuta.</span><span class="sxs-lookup"><span data-stu-id="1c646-131">You can run or deactivate multiple enrichments at once by selecting them in the list.</span></span> <span data-ttu-id="1c646-132">Ikusi eta editatzeko aukerak ez daude eskuragarri gisa eta soilik aberasteko soilik funtzionatzen du.</span><span class="sxs-lookup"><span data-stu-id="1c646-132">View and edit options aren't available as bulk action and only work for one enrichment at a time.</span></span>

## <a name="enrichments-and-connections"></a><span data-ttu-id="1c646-133">Aberasteak eta konexioak</span><span class="sxs-lookup"><span data-stu-id="1c646-133">Enrichments and connections</span></span>

<span data-ttu-id="1c646-134">Hirugarrenen aberastasunak erabiliz konfiguratzen dira [konexioak](connections.md), administratzaileak kredentzialekin konfiguratzen duena eta datuak transferitzeko baimena ematen duena.</span><span class="sxs-lookup"><span data-stu-id="1c646-134">Third-party enrichments are configured using [connections](connections.md), which an administrator sets up with credentials and provides consent for data transfers.</span></span> <span data-ttu-id="1c646-135">Konexioa erabil daiteke administratzaileen eta laguntzaileen bitartez aberasteak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="1c646-135">The connection can be used by administrators and contributors to configure enrichments.</span></span>  

## <a name="multiple-enrichments-of-the-same-type"></a><span data-ttu-id="1c646-136">Mota bereko hainbat aberastasun</span><span class="sxs-lookup"><span data-stu-id="1c646-136">Multiple enrichments of the same type</span></span>

<span data-ttu-id="1c646-137">Aberastu nahi den entitatea aberasteko konfigurazioan zehazten da eta horrek zure profilen azpimultzo bat soilik aberastea ahalbidetzen du.</span><span class="sxs-lookup"><span data-stu-id="1c646-137">The entity to be enriched is specified during the enrichment configuration, which allows you to enrich only a subset of your profiles.</span></span> <span data-ttu-id="1c646-138">Exmaple-rako, aberastu datuak segmentu zehatz baterako soilik.</span><span class="sxs-lookup"><span data-stu-id="1c646-138">For exmaple, enrich data only for a specific segment.</span></span> <span data-ttu-id="1c646-139">Mota bereko hainbat aberastasun konfigura ditzakezu eta konexio bera berrerabili.</span><span class="sxs-lookup"><span data-stu-id="1c646-139">You can configure several enrichments of the same type and reuse the same connection.</span></span> <span data-ttu-id="1c646-140">Zenbait aberastasunek sor ditzaketen mota bereko aberastasunen kopuruak izango dituzte mugak.</span><span class="sxs-lookup"><span data-stu-id="1c646-140">Some enrichments will have limits to the number of enrichments of the same type that can be created.</span></span> <span data-ttu-id="1c646-141">Mugak eta egungo erabilera webgunean ikus daitezke **Aberastea** orrialdea.</span><span class="sxs-lookup"><span data-stu-id="1c646-141">The limits and current use can be seen on the **Enrichment** page.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
