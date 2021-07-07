---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft Power Automate hurrengoan Dynamics 365 Customer Insights.
ms.date: 06/24/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 57be0a204ef920b7a4bb31cf9a5b3a77f96eca0d
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305049"
---
# <a name="power-automate-connector-preview"></a><span data-ttu-id="7144a-103">Power Automate konektorea (Aurrebista)</span><span class="sxs-lookup"><span data-stu-id="7144a-103">Power Automate connector (preview)</span></span>

<span data-ttu-id="7144a-104">Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.</span><span class="sxs-lookup"><span data-stu-id="7144a-104">Trigger specific events to occur automatically when your data changes and manage more complex flows directly in [Power Automate](https://flow.microsoft.com/).</span></span>

## <a name="power-automate-triggers"></a><span data-ttu-id="7144a-105">Power Automate Abiarazleak</span><span class="sxs-lookup"><span data-stu-id="7144a-105">Power Automate triggers</span></span>

<span data-ttu-id="7144a-106">Erabili abiarazleak hodei fluxuak sortzeko eta zeregin errepikakorrak automatizatzeko, hala nola jakinarazpenak edo ekintza aurreratuagoak.</span><span class="sxs-lookup"><span data-stu-id="7144a-106">Use triggers to create cloud flows and automate repetitive tasks, such as notifications or more advanced actions.</span></span> 

- <span data-ttu-id="7144a-107">Aktibatu datu-iturburu freskatzeak huts egiten duenean.</span><span class="sxs-lookup"><span data-stu-id="7144a-107">Trigger when a data source refresh fails.</span></span> 
- <span data-ttu-id="7144a-108">Aktibatu datu-iturburu freskatzeak arrakasta duenean.</span><span class="sxs-lookup"><span data-stu-id="7144a-108">Trigger when a data source refresh succeeds.</span></span>
- <span data-ttu-id="7144a-109">Abiarazi atalasea gainditzen denean segmentu batean.</span><span class="sxs-lookup"><span data-stu-id="7144a-109">Trigger when a threshold is crossed on a segment.</span></span> <span data-ttu-id="7144a-110">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="7144a-110">The trigger is limited to crossing above the threshold.</span></span>
- <span data-ttu-id="7144a-111">Abiarazi atalasea gainditzen denean negozio-neurketa batean.</span><span class="sxs-lookup"><span data-stu-id="7144a-111">Trigger when a threshold is crossed on a business measure.</span></span> <span data-ttu-id="7144a-112">Dimentsiorik gabeko negozio-neurriak soilik onartzen dira.</span><span class="sxs-lookup"><span data-stu-id="7144a-112">Only business measures without a dimension are supported.</span></span> <span data-ttu-id="7144a-113">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="7144a-113">The trigger is limited to crossing above the threshold.</span></span>
- <span data-ttu-id="7144a-114">Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="7144a-114">Trigger when a full refresh of (data sources, segments, measures, ...) is completed.</span></span>
- <span data-ttu-id="7144a-115">Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="7144a-115">Trigger when a refresh of the unification process (map, match, merge) is completed.</span></span>

[<span data-ttu-id="7144a-116">Konfiguratu zure abiarazleak Power Automate-n.</span><span class="sxs-lookup"><span data-stu-id="7144a-116">Configure your triggers in Power Automate.</span></span>](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/)

## <a name="power-automate-actions"></a><span data-ttu-id="7144a-117">Power Automate ekintzak</span><span class="sxs-lookup"><span data-stu-id="7144a-117">Power Automate actions</span></span>

<span data-ttu-id="7144a-118">Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="7144a-118">The Power Automate connector provides other actions than the available triggers.</span></span> <span data-ttu-id="7144a-119">Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](/connectors/customerinsights/).</span><span class="sxs-lookup"><span data-stu-id="7144a-119">For more information, see the [Dynamics 365 Customer Insights Connector](/connectors/customerinsights/).</span></span>

## <a name="create-a-power-automate-flow"></a><span data-ttu-id="7144a-120">Sortu Power Automate fluxu bat</span><span class="sxs-lookup"><span data-stu-id="7144a-120">Create a Power Automate flow</span></span>

1. <span data-ttu-id="7144a-121">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="7144a-121">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="7144a-122">**Power Automate** fitxan, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="7144a-122">On the **Power Automate** tile, select **Set up**.</span></span>

1. <span data-ttu-id="7144a-123">Power Automate-ko Customer Insights konektorea irekitzen da.</span><span class="sxs-lookup"><span data-stu-id="7144a-123">The Customer Insights Connector (preview) in Power Automate opens.</span></span> <span data-ttu-id="7144a-124">**Hasi saioa** Power Automate.</span><span class="sxs-lookup"><span data-stu-id="7144a-124">**Sign in** to Power Automate.</span></span>

1. <span data-ttu-id="7144a-125">Aukeratu erabilgarri dauden abiarazleetako bat eta gehitu urrats gehiago zure fluxu berrian.</span><span class="sxs-lookup"><span data-stu-id="7144a-125">Choose one of the available triggers and add more steps to your new flow.</span></span> <span data-ttu-id="7144a-126">Informazio gehiagorako, ikusi [Sortu hodei fluxua hemen Power Automate](/power-automate/get-started-logic-flow).</span><span class="sxs-lookup"><span data-stu-id="7144a-126">For more information, see [Create a cloud flow in Power Automate](/power-automate/get-started-logic-flow).</span></span>

<span data-ttu-id="7144a-127">Fluxuak erabiltzeko adibideak:</span><span class="sxs-lookup"><span data-stu-id="7144a-127">Examples of how to use flows:</span></span> 
- <span data-ttu-id="7144a-128">Bidali mezu bat Microsoft Teams kanalera datu-iturburu freskatzeak huts egiten badu.</span><span class="sxs-lookup"><span data-stu-id="7144a-128">Post a message to a Microsoft Teams channel if a data source refresh fails.</span></span> 
- <span data-ttu-id="7144a-129">Bidali mezu elektronikoa datu jabeei segmentu bateko atalasea gainditzen denean.</span><span class="sxs-lookup"><span data-stu-id="7144a-129">Send an email to the data owners when a threshold on a segment is crossed.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
