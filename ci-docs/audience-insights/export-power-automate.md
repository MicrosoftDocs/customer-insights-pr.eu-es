---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft Power Automate hurrengoan Dynamics 365 Customer Insights.
ms.date: 01/20/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: e973bb11b31c9e70b695ebec8aa2700fdaa5e44f
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597910"
---
# <a name="power-automate-connector-preview"></a><span data-ttu-id="0b0c7-103">Power Automate konektorea (Aurrebista)</span><span class="sxs-lookup"><span data-stu-id="0b0c7-103">Power Automate connector (preview)</span></span>

<span data-ttu-id="0b0c7-104">Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-104">Trigger specific events to occur automatically when your data changes and manage more complex flows directly in [Power Automate](https://flow.microsoft.com/).</span></span>

## <a name="power-automate-triggers"></a><span data-ttu-id="0b0c7-105">Power Automate Abiarazleak</span><span class="sxs-lookup"><span data-stu-id="0b0c7-105">Power Automate triggers</span></span>

<span data-ttu-id="0b0c7-106">Erabili abiarazleak hodei fluxuak sortzeko eta zeregin errepikakorrak automatizatzeko, hala nola jakinarazpenak edo ekintza aurreratuagoak.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-106">Use triggers to create cloud flows and automate repetitive tasks, such as notifications or more advanced actions.</span></span> 

- <span data-ttu-id="0b0c7-107">Aktibatu datu-iturburu freskatzeak huts egiten duenean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-107">Trigger when a data source refresh fails.</span></span> 
- <span data-ttu-id="0b0c7-108">Aktibatu datu-iturburu freskatzeak arrakasta duenean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-108">Trigger when a data source refresh succeeds.</span></span>
- <span data-ttu-id="0b0c7-109">Abiarazi atalasea gainditzen denean segmentu batean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-109">Trigger when a threshold is crossed on a segment.</span></span> <span data-ttu-id="0b0c7-110">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-110">The trigger is limited to crossing above the threshold.</span></span>
- <span data-ttu-id="0b0c7-111">Abiarazi atalasea gainditzen denean negozio-neurketa batean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-111">Trigger when a threshold is crossed on a business measure.</span></span> <span data-ttu-id="0b0c7-112">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-112">The trigger is limited crossing above the threshold.</span></span>
- <span data-ttu-id="0b0c7-113">Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-113">Trigger when a full refresh of (data sources, segments, measures,...) is completed.</span></span>
- <span data-ttu-id="0b0c7-114">Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-114">Trigger when a refresh of the unification process (map, match, merge) is completed.</span></span>

<span data-ttu-id="0b0c7-115">[Konfiguratu zure abiarazleak Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).</span><span class="sxs-lookup"><span data-stu-id="0b0c7-115">[Configure your triggers in Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).</span></span>

## <a name="power-automate-actions"></a><span data-ttu-id="0b0c7-116">Power Automate ekintzak</span><span class="sxs-lookup"><span data-stu-id="0b0c7-116">Power Automate actions</span></span>
<span data-ttu-id="0b0c7-117">Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-117">The Power Automate connector provides other actions than the available triggers.</span></span> <span data-ttu-id="0b0c7-118">Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](/connectors/customerinsights/).</span><span class="sxs-lookup"><span data-stu-id="0b0c7-118">For more information, see the [Dynamics 365 Customer Insights Connector](/connectors/customerinsights/).</span></span>

## <a name="create-a-power-automate-flow"></a><span data-ttu-id="0b0c7-119">Sortu Power Automate fluxu bat</span><span class="sxs-lookup"><span data-stu-id="0b0c7-119">Create a Power Automate flow</span></span>

1. <span data-ttu-id="0b0c7-120">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-120">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="0b0c7-121">**Power Automate** fitxan, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-121">On the **Power Automate** tile, select **Set up**.</span></span>

1. <span data-ttu-id="0b0c7-122">Power Automate-ko Customer Insights konektorea irekitzen da.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-122">The Customer Insights Connector (preview) in Power Automate opens.</span></span> <span data-ttu-id="0b0c7-123">**Hasi saioa** Power Automate.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-123">**Sign in** to Power Automate.</span></span>

1. <span data-ttu-id="0b0c7-124">Aukeratu erabilgarri dauden abiarazleetako bat eta gehitu urrats gehiago zure fluxu berrian.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-124">Choose one of the available triggers and add more steps to your new flow.</span></span> <span data-ttu-id="0b0c7-125">Informazio gehiagorako, ikusi [Sortu hodei fluxua hemen Power Automate](/power-automate/get-started-logic-flow).</span><span class="sxs-lookup"><span data-stu-id="0b0c7-125">For more information, see [Create a cloud flow in Power Automate](/power-automate/get-started-logic-flow).</span></span>

<span data-ttu-id="0b0c7-126">Fluxuak nola erabili adibideak:</span><span class="sxs-lookup"><span data-stu-id="0b0c7-126">Examples how to use flows:</span></span> 
- <span data-ttu-id="0b0c7-127">Bidali mezu bat Microsoft Teams kanalera datu-iturburu freskatzeak huts egiten badu.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-127">Post a message to a Microsoft Teams channel if a data source refresh fails.</span></span> 
- <span data-ttu-id="0b0c7-128">Bidali mezu elektronikoa datu jabeei segmentu bateko atalasea gainditzen denean.</span><span class="sxs-lookup"><span data-stu-id="0b0c7-128">Send an email to the data owners when a threshold on a segment is crossed.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]