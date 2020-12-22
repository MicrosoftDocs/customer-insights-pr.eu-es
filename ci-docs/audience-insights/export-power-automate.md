---
title: Power Automate konektorea | Microsoft Docs
description: Sortu fluxuak Microsoft-en Power Automate batetik Dynamics 365 Customer Insights.
ms.date: 08/03/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: philk
manager: shellyha
ms.openlocfilehash: ffe92414365b0b777691a4a2d585100e4fbea591
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404952"
---
# <a name="power-automate-connector-preview"></a><span data-ttu-id="97794-103">Power Automate konektorea (Aurrebista)</span><span class="sxs-lookup"><span data-stu-id="97794-103">Power Automate connector (preview)</span></span>

<span data-ttu-id="97794-104">Konfiguratu datuak aldatzen direnean automatikoki abiaraziko diren gertaera zehatzak eta kudeatu fluxu konplexuagoak [Power Automate](https://flow.microsoft.com/)-n zuzenean.</span><span class="sxs-lookup"><span data-stu-id="97794-104">Trigger specific events to occur automatically when your data changes and manage more complex flows directly in [Power Automate](https://flow.microsoft.com/).</span></span>

## <a name="power-automate-triggers"></a><span data-ttu-id="97794-105">Power Automate Abiarazleak</span><span class="sxs-lookup"><span data-stu-id="97794-105">Power Automate triggers</span></span>

<span data-ttu-id="97794-106">Hainbat aktibatzaile erabil ditzakezu zeregin errepikakorrak automatizatzeko fluxuak sortzeko, hala nola, jakinarazpenak edo ekintza aurreratuagoak.</span><span class="sxs-lookup"><span data-stu-id="97794-106">You can use a variety of triggers that allow you to create flows to automate repetitive tasks, such as notifications or more advanced actions.</span></span> 

- <span data-ttu-id="97794-107">Aktibatu datu-iturburu freskatzeak huts egiten duenean.</span><span class="sxs-lookup"><span data-stu-id="97794-107">Trigger when a data source refresh fails.</span></span> 
- <span data-ttu-id="97794-108">Aktibatu datu-iturburu freskatzeak arrakasta duenean.</span><span class="sxs-lookup"><span data-stu-id="97794-108">Trigger when a data source refresh succeeds.</span></span>
- <span data-ttu-id="97794-109">Abiarazi atalasea gainditzen denean segmentu batean.</span><span class="sxs-lookup"><span data-stu-id="97794-109">Trigger when a threshold is crossed on a segment.</span></span> <span data-ttu-id="97794-110">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="97794-110">The trigger is limited to crossing above the threshold.</span></span>
- <span data-ttu-id="97794-111">Abiarazi atalasea gainditzen denean negozio-neurketa batean.</span><span class="sxs-lookup"><span data-stu-id="97794-111">Trigger when a threshold is crossed on a business measure.</span></span> <span data-ttu-id="97794-112">Harrapatzailea atalasearen gainetik zeharkatzera mugatzen da.</span><span class="sxs-lookup"><span data-stu-id="97794-112">The trigger is limited crossing above the threshold.</span></span>
- <span data-ttu-id="97794-113">Abiarazi eguneratze osoa (datu iturriak, segmentuak, neurriak, ...) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="97794-113">Trigger when a full refresh of (data sources, segments, measures,...) is completed.</span></span>
- <span data-ttu-id="97794-114">Aktibatu bateratze-prozesuaren freskaketa bat (mapa, bat etorri, batu) amaitzen denean.</span><span class="sxs-lookup"><span data-stu-id="97794-114">Trigger when a refresh of the unification process (map, match, merge) is completed.</span></span>

<span data-ttu-id="97794-115">[Konfiguratu zure abiarazleak Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).</span><span class="sxs-lookup"><span data-stu-id="97794-115">[Configure your triggers in Power Automate](https://flow.microsoft.com/connectors/shared_customerinsights/dynamics-365-customer-insights-connector/).</span></span>

## <a name="power-automate-actions"></a><span data-ttu-id="97794-116">Power Automate ekintzak</span><span class="sxs-lookup"><span data-stu-id="97794-116">Power Automate actions</span></span>
<span data-ttu-id="97794-117">Power Automate konektoreak erabilgarri dauden abiarazleak baino beste ekintza batzuk eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="97794-117">The Power Automate connector provides other actions than the available triggers.</span></span> <span data-ttu-id="97794-118">Informazio gehiagorako, ikus [Dynamics 365 Customer Insights Connector](https://docs.microsoft.com/connectors/customerinsights/).</span><span class="sxs-lookup"><span data-stu-id="97794-118">For more information, see the [Dynamics 365 Customer Insights Connector](https://docs.microsoft.com/connectors/customerinsights/).</span></span>

## <a name="create-a-power-automate-flow-in-audience-insights"></a><span data-ttu-id="97794-119">Sortu Power Automate fluxu bat hartzaileen xehetasunetan</span><span class="sxs-lookup"><span data-stu-id="97794-119">Create a Power Automate flow in audience insights</span></span>

1. <span data-ttu-id="97794-120">Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Sistema**.</span><span class="sxs-lookup"><span data-stu-id="97794-120">In audience insights, go to **Admin** > **System**.</span></span>

1. <span data-ttu-id="97794-121">**Sistema** orrian, hautatu **Egoera** fitxa.</span><span class="sxs-lookup"><span data-stu-id="97794-121">On the **System** page, select the **Status** tab.</span></span>

1. <span data-ttu-id="97794-122">Sarbidean **Datu iturriak** atala aukeratu **fluxuak** eta hautatu **Sortu fluxua** goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="97794-122">In the **Data Sources** section, select **Flows** and select **Create a flow** from the dropdown list.</span></span>
   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="97794-123">![Power Automate konektorea erakusten du Sortu fluxua ekintza](media/power-automate-connector-create-flow.png "Power Automate konektorea erakusten du Sortu fluxua ekintza")</span><span class="sxs-lookup"><span data-stu-id="97794-123">![Power Automate connector showing Create a Flow action](media/power-automate-connector-create-flow.png "Power Automate connector showing Create a Flow action")</span></span>

1. <span data-ttu-id="97794-124">Power Automate-n, hautatu abiarazle erabilgarri bat zure nahiago duen fluxua sortzeko.</span><span class="sxs-lookup"><span data-stu-id="97794-124">In Power Automate, select one of the available triggers to create your preferred flow.</span></span> <span data-ttu-id="97794-125">Zure lehen fluxua sortzen ari bazara, identifikatu egin behar duzu Power Automate konektorea lehenengo.</span><span class="sxs-lookup"><span data-stu-id="97794-125">If you're creating your first flow, you'll need to authenticate with the Power Automate connector first.</span></span>
