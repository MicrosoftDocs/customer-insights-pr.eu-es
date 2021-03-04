---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft-en Power Automate batetik Dynamics 365 Customer Insights.
ms.date: 01/20/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
ms.reviewer: philk
manager: shellyha
ms.openlocfilehash: fb1df4e9ab1f78300b8ec1f8dfdfbfbac0e71447
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5268809"
---
# <a name="power-automate-connector-preview"></a><span data-ttu-id="f9386-103">Power Automate konektorea (Aurrebista)</span><span class="sxs-lookup"><span data-stu-id="f9386-103">Power Automate connector (preview)</span></span>

<span data-ttu-id="f9386-104">Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.</span><span class="sxs-lookup"><span data-stu-id="f9386-104">Trigger specific events to occur automatically when your data changes and manage more complex flows directly in [Power Automate](https://flow.microsoft.com/).</span></span>

## <a name="power-automate-triggers"></a><span data-ttu-id="f9386-105">Power Automate Abiarazleak</span><span class="sxs-lookup"><span data-stu-id="f9386-105">Power Automate triggers</span></span>

<span data-ttu-id="f9386-106">Erabili abiarazleak hodei fluxuak sortzeko eta zeregin errepikakorrak automatizatzeko, hala nola jakinarazpenak edo ekintza aurreratuagoak.</span><span class="sxs-lookup"><span data-stu-id="f9386-106">Use triggers to create cloud flows and automate repetitive tasks, such as notifications or more advanced actions.</span></span> 

- <span data-ttu-id="f9386-107">Aktibatu datu-iturburu freskatzeak huts egiten duenean.</span><span class="sxs-lookup"><span data-stu-id="f9386-107">Trigger when a data source refresh fails.</span></span> 
- <span data-ttu-id="f9386-108">Aktibatu datu-iturburu freskatzeak arrakasta duenean.</span><span class="sxs-lookup"><span data-stu-id="f9386-108">Trigger when a data source refresh succeeds.</span></span>
- <span data-ttu-id="f9386-109">Abiarazi atalasea gainditzen denean segmentu batean.</span><span class="sxs-lookup"><span data-stu-id="f9386-109">Trigger when a threshold is crossed on a segment.</span></span> <span data-ttu-id="f9386-110">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="f9386-110">The trigger is limited to crossing above the threshold.</span></span>
- <span data-ttu-id="f9386-111">Abiarazi atalasea gainditzen denean negozio-neurketa batean.</span><span class="sxs-lookup"><span data-stu-id="f9386-111">Trigger when a threshold is crossed on a business measure.</span></span> <span data-ttu-id="f9386-112">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="f9386-112">The trigger is limited crossing above the threshold.</span></span>
- <span data-ttu-id="f9386-113">Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="f9386-113">Trigger when a full refresh of (data sources, segments, measures,...) is completed.</span></span>
- <span data-ttu-id="f9386-114">Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="f9386-114">Trigger when a refresh of the unification process (map, match, merge) is completed.</span></span>

<span data-ttu-id="f9386-115">[Konfiguratu zure abiarazleak Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).</span><span class="sxs-lookup"><span data-stu-id="f9386-115">[Configure your triggers in Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).</span></span>

## <a name="power-automate-actions"></a><span data-ttu-id="f9386-116">Power Automate ekintzak</span><span class="sxs-lookup"><span data-stu-id="f9386-116">Power Automate actions</span></span>
<span data-ttu-id="f9386-117">Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="f9386-117">The Power Automate connector provides other actions than the available triggers.</span></span> <span data-ttu-id="f9386-118">Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](https://docs.microsoft.com/connectors/customerinsights/).</span><span class="sxs-lookup"><span data-stu-id="f9386-118">For more information, see the [Dynamics 365 Customer Insights Connector](https://docs.microsoft.com/connectors/customerinsights/).</span></span>

## <a name="create-a-power-automate-flow"></a><span data-ttu-id="f9386-119">Sortu Power Automate fluxu bat</span><span class="sxs-lookup"><span data-stu-id="f9386-119">Create a Power Automate flow</span></span>

1. <span data-ttu-id="f9386-120">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.</span><span class="sxs-lookup"><span data-stu-id="f9386-120">In audience insights, go to **Admin** > **Export destinations**.</span></span>

1. <span data-ttu-id="f9386-121">**Power Automate** fitxan, hautatu **Konfiguratu**.</span><span class="sxs-lookup"><span data-stu-id="f9386-121">On the **Power Automate** tile, select **Set up**.</span></span>

1. <span data-ttu-id="f9386-122">Power Automate-ko Customer Insights konektorea irekitzen da.</span><span class="sxs-lookup"><span data-stu-id="f9386-122">The Customer Insights Connector (preview) in Power Automate opens.</span></span> <span data-ttu-id="f9386-123">**Hasi saioa** Power Automate.</span><span class="sxs-lookup"><span data-stu-id="f9386-123">**Sign in** to Power Automate.</span></span>

1. <span data-ttu-id="f9386-124">Aukeratu erabilgarri dauden abiarazleetako bat eta gehitu urrats gehiago zure fluxu berrian.</span><span class="sxs-lookup"><span data-stu-id="f9386-124">Choose one of the available triggers and add more steps to your new flow.</span></span> <span data-ttu-id="f9386-125">Informazio gehiagorako, ikusi [Sortu hodei fluxua hemen Power Automate](https://docs.microsoft.com/power-automate/get-started-logic-flow).</span><span class="sxs-lookup"><span data-stu-id="f9386-125">For more information, see [Create a cloud flow in Power Automate](https://docs.microsoft.com/power-automate/get-started-logic-flow).</span></span>

<span data-ttu-id="f9386-126">Fluxuak nola erabili adibideak:</span><span class="sxs-lookup"><span data-stu-id="f9386-126">Examples how to use flows:</span></span> 
- <span data-ttu-id="f9386-127">Bidali mezu bat Microsoft Teams kanalera datu-iturburu freskatzeak huts egiten badu.</span><span class="sxs-lookup"><span data-stu-id="f9386-127">Post a message to a Microsoft Teams channel if a data source refresh fails.</span></span> 
- <span data-ttu-id="f9386-128">Bidali mezu elektronikoa datu jabeei segmentu bateko atalasea gainditzen denean.</span><span class="sxs-lookup"><span data-stu-id="f9386-128">Send an email to the data owners when a threshold on a segment is crossed.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]