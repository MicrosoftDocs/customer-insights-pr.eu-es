---
title: Microsoft Teams-eko bot-a
description: Bilatu bezeroen profil bateratuak Microsoft Teams-en bot baten laguntzarekin.
ms.date: 04/21/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: stefanie-msft
ms.author: sthe
manager: shellyha
ms.openlocfilehash: 45ea23fbefe5f1d44c3961183b76d2cc5c45355e
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404985"
---
# <a name="teams-bot-for-dynamics-365-customer-insights-preview"></a><span data-ttu-id="3d3d0-103">Teams-en bot-a Dynamics 365 Customer Insights-erako (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="3d3d0-103">Teams bot for Dynamics 365 Customer Insights (preview)</span></span>

<span data-ttu-id="3d3d0-104">Konektatu Microsoft Teams-ekin, bot batek bezeroen profil bateratuak bilatzeko Teams kanaletan.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-104">Connect with Microsoft Teams to let a bot look up unified customer profiles in Teams channels.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="3d3d0-105">![Taldeak bezeroaren erregistroa erakusten duten botak](media/teams-bot.png "Taldeak bezeroaren erregistroa erakusten duten botak")</span><span class="sxs-lookup"><span data-stu-id="3d3d0-105">![Teams bot showing a customer record](media/teams-bot.png "Teams bot showing a customer record")</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3d3d0-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="3d3d0-106">Prerequisites</span></span>

<span data-ttu-id="3d3d0-107">Bot-a konfiguratzeko eta konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="3d3d0-107">To set up and configure the bot, the following prerequisites must be met:</span></span>

- <span data-ttu-id="3d3d0-108">Gutxienez bat dago [datu-iturburu gehitu da](data-sources.md).</span><span class="sxs-lookup"><span data-stu-id="3d3d0-108">There's at least one [data source added](data-sources.md).</span></span>
- <span data-ttu-id="3d3d0-109">[Bateratze prozesua](data-unification.md) osatu da.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-109">The [unification process](data-unification.md) is complete.</span></span>
- <span data-ttu-id="3d3d0-110">Eremuak gehitzen dira [bilaketa eta iragazki indizea](search-filter-index.md).</span><span class="sxs-lookup"><span data-stu-id="3d3d0-110">Fields are added to the [search and filter index](search-filter-index.md).</span></span>
- <span data-ttu-id="3d3d0-111">Customer Insights eta taldeak antolaketa berean daude.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-111">Customer Insights and Teams are in the same organization.</span></span>

## <a name="configure-the-bot"></a><span data-ttu-id="3d3d0-112">Konfiguratu bota</span><span class="sxs-lookup"><span data-stu-id="3d3d0-112">Configure the bot</span></span>

1. <span data-ttu-id="3d3d0-113">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-113">In audience insights, go to **Admin** > **Export Destinations**.</span></span>
1. <span data-ttu-id="3d3d0-114">Gainean Microsoft Teams fitxa, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-114">On the Microsoft Teams tile, select **Set up**.</span></span>
1. <span data-ttu-id="3d3d0-115">Hara birbideratu zara **Aplikazioak** eremua Taldeetan.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-115">You're redirected to the **Apps** area in Teams.</span></span> <span data-ttu-id="3d3d0-116">Taldeak ere ireki eta hautatu ditzakezu **Aplikazioak** behe-ezkerreko izkinan edo [atera ezazu AppSource](https://go.microsoft.com/fwlink/?linkid=2124104) zuzenean.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-116">You can also open Teams and select **Apps** in the bottom-left corner or [get it from AppSource](https://go.microsoft.com/fwlink/?linkid=2124104) directly.</span></span>
1. <span data-ttu-id="3d3d0-117">Bilatu **Customer Insights** eta hautatu aplikazioa.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-117">Search for **Customer Insights** and select the app.</span></span>
1. <span data-ttu-id="3d3d0-118">Hautatu **Gehitu**.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-118">Select **Add**.</span></span>
1. <span data-ttu-id="3d3d0-119">Customer Insights taldeetan saioa hasi ondoren, ongietorri mezua ikusiko duzu eta hasteko aukera izango duzu.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-119">After signing in to Customer Insights in Teams, you'll see a welcome message and can get started.</span></span>

## <a name="things-you-can-do-with-the-bot"></a><span data-ttu-id="3d3d0-120">Botarekin egin ditzakezun gauzak</span><span class="sxs-lookup"><span data-stu-id="3d3d0-120">Things you can do with the bot</span></span>

<span data-ttu-id="3d3d0-121">Botak bezeroaren profil bateratuak bilatzeko gaitasunak eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-121">The bot provides lookup capabilities for unified customer profiles.</span></span>

- <span data-ttu-id="3d3d0-122">Sartu **bilatu** ondoren, bilaketa, iragazki indizean gehitzen den bezeroaren profil bateratuaren izen bat, helbide elektronikoa edo beste edozein eremutan.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-122">Enter **search** followed by a name, email address, or any other field on the unified customer profile that is added to the search and filter index.</span></span>

  <span data-ttu-id="3d3d0-123">Lortutako bezeroen profiletik 15 eremu gehienez 15 txartel jasoko dituzu.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-123">You'll get a card with up to 15 fields from the resulting customer profile.</span></span> <span data-ttu-id="3d3d0-124">Hainbat partiduren bidez, profil bat hauta dezakezu emaitza guztien zerrenda itzultzen da.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-124">Multiple matches return a list of results where you can select a profile.</span></span> <span data-ttu-id="3d3d0-125">Bilaketa terminoa komatxo bikoitzetan gehi dezakezu partida zehatza bilatzeko.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-125">You can add the search term in double quotes to look up an exact match.</span></span>

- <span data-ttu-id="3d3d0-126">Zure erakundeak Customer Insights ingurune ugari mantentzen baditu erakunde berean, **aldatu instantzia** atalean sar zaitezke bot-a zein ingurunera konektatu nahi duzun aukeratzeko.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-126">If your organization maintains multiple Customer Insights environments in the same organization, you can enter **switchinstance** to choose which environment you want to connect the bot to.</span></span>

- <span data-ttu-id="3d3d0-127">Sartu **laguntza** boterako erabilgarri dauden komandoen zerrenda ikusteko.</span><span class="sxs-lookup"><span data-stu-id="3d3d0-127">Enter **help** to see a list of available commands for the bot.</span></span>  
