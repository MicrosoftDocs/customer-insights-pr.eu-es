---
title: Instalatu eta konfiguratu Bezeroaren txartelaren osagarria
description: Instalatu eta konfiguratu Dynamics 365 Customer Insights-erako Bezeroen txartelaren osagarria.
ms.date: 01/20/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: f3c4a01f9ce7749eeee72f7901620dae7cb9b8d3
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597312"
---
# <a name="customer-card-add-in-preview"></a><span data-ttu-id="4fb66-103">Bezeroaren txartelaren osagarria (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="4fb66-103">Customer Card Add-in (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="4fb66-104">Lortu zure bezeroen 360 graduko ikuspegia zuzenean Dynamics 365 aplikazioetan.</span><span class="sxs-lookup"><span data-stu-id="4fb66-104">Get a 360-degree view of your customers directly in Dynamics 365 apps.</span></span> <span data-ttu-id="4fb66-105">Ikusi demografia, xehetasunak eta jarduera-denborak Bezero-txartelaren gehigarrian.</span><span class="sxs-lookup"><span data-stu-id="4fb66-105">View demographics, insights, and activity timelines with the Customer Card Add-in.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4fb66-106">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="4fb66-106">Prerequisites</span></span>

- <span data-ttu-id="4fb66-107">Dynamics 365 aplikazioa (Salmenten atala edo bezeroarentzako arreta-zerbitzu Hub adibidez), 9.0 bertsioa eta ondoren Interfaze bateratu gaituta.</span><span class="sxs-lookup"><span data-stu-id="4fb66-107">Dynamics 365 app (such as Sales Hub or Customer Service Hub), version 9.0 and later with Unified Interface enabled.</span></span>
- <span data-ttu-id="4fb66-108">[Common Data Service erabiliz Dynamics 365 aplikaziotik sartutako](connect-power-query.md) bezeroen profilak.</span><span class="sxs-lookup"><span data-stu-id="4fb66-108">Customer profiles [ingested from the Dynamics 365 app using Common Data Service](connect-power-query.md).</span></span>
- <span data-ttu-id="4fb66-109">Bezeroaren txartelaren osagarriaren erabiltzaileak [erabiltzaile gisa gehitu behar dira](permissions.md) hartzaileen xehetasunetan.</span><span class="sxs-lookup"><span data-stu-id="4fb66-109">Users of the Customer Card Add-in need to be [added as users](permissions.md) in audience insights.</span></span>
- <span data-ttu-id="4fb66-110">[Bilaketa konfiguratua eta iragazkiaren gaitasunak](search-filter-index.md).</span><span class="sxs-lookup"><span data-stu-id="4fb66-110">[Configured search and filter capabilities](search-filter-index.md).</span></span>
- <span data-ttu-id="4fb66-111">Kontrol demografikoa: eremu demografikoak (adina edo generoa), adibidez, bezeroen profil bateratuan daude eskuragarri.</span><span class="sxs-lookup"><span data-stu-id="4fb66-111">Demographic control: Demographic fields(such as age or gender) are available in the unified customer profile.</span></span>
- <span data-ttu-id="4fb66-112">Aberastearen kontrola: Aktiboa eskatzen du [hobekuntzak](enrichment-hub.md) bezeroen profiletan aplikatuta.</span><span class="sxs-lookup"><span data-stu-id="4fb66-112">Enrichment control: Requires active [enrichments](enrichment-hub.md) applied to customer profiles.</span></span>
- <span data-ttu-id="4fb66-113">Adimenaren kontrola: Azure Machine Learning ([iragarpenak](predictions.md) edo [eredu pertsonalizatuak](custom-models.md)) erabiliz sortutako datuak behar dira</span><span class="sxs-lookup"><span data-stu-id="4fb66-113">Intelligence control: Requires data generated using Azure Machine Learning ([Predictions](predictions.md) or [Custom Models](custom-models.md))</span></span>
- <span data-ttu-id="4fb66-114">Neurriaren kontrola: [Konfiguratutako neurriak](measures.md) behar dira.</span><span class="sxs-lookup"><span data-stu-id="4fb66-114">Measure control: Requires [configured measures](measures.md).</span></span>
- <span data-ttu-id="4fb66-115">Kronogramaren kontrola: [konfiguratutako jarduerak](activities.md) behar dira.</span><span class="sxs-lookup"><span data-stu-id="4fb66-115">Timeline control: Requires [configured activities](activities.md).</span></span>

## <a name="install-the-customer-card-add-in"></a><span data-ttu-id="4fb66-116">Instalatu Bezeroaren txartelaren osagarria</span><span class="sxs-lookup"><span data-stu-id="4fb66-116">Install the Customer Card Add-in</span></span>

<span data-ttu-id="4fb66-117">Bezeroaren Txartelaren Gehigarria Dynamics 365-en customer engagement aplikazioetarako irtenbidea da.</span><span class="sxs-lookup"><span data-stu-id="4fb66-117">The Customer Card Add-in is a solution for customer engagement apps in Dynamics 365.</span></span> <span data-ttu-id="4fb66-118">Konponbidea instalatzeko, joan AppSource eta bilatu **Bezero txartel dinamikoa**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-118">To install the solution, go to AppSource and search for **Dynamics Customer Card**.</span></span> <span data-ttu-id="4fb66-119">Hautatu [Bezero txartela AppSource-n](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics_365_customer_insights_customer_card_addin?tab=Overview) eta hautatu **Eskuratu orain**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-119">Select the [Customer Card Add-in on AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics_365_customer_insights_customer_card_addin?tab=Overview) and select **Get It Now**.</span></span>

<span data-ttu-id="4fb66-120">Baliteke Dynamics 365 aplikaziorako zure administratzaileekin saioa hasi behar duzula irtenbidea instalatzeko.</span><span class="sxs-lookup"><span data-stu-id="4fb66-120">You may need to sign in with your admin credentials for the Dynamics 365 app to install the solution.</span></span>

<span data-ttu-id="4fb66-121">Zenbait denbora behar izango duzu irtenbidea zure ingurunean instalatzeko.</span><span class="sxs-lookup"><span data-stu-id="4fb66-121">It can take some time for the solution to be installed to your environment.</span></span>

## <a name="configure-the-customer-card-add-in"></a><span data-ttu-id="4fb66-122">Konfiguratu Bezeroaren Kartaren Gehigarria</span><span class="sxs-lookup"><span data-stu-id="4fb66-122">Configure the Customer Card Add-in</span></span>

1. <span data-ttu-id="4fb66-123">Administratzaile gisa, zoaz webgunera **ezarpenak** atala Dynamics 365-en, eta hautatu **Soluzioak**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-123">As an admin, go to the **Settings** section in Dynamics 365 and select **Solutions**.</span></span>

1. <span data-ttu-id="4fb66-124">Hautatu botoia **Bistaratu izena** esteka **Dynamics 365 Customer Insights Bezero-txartelaren gehigarria (aurrebista)** konponbidea.</span><span class="sxs-lookup"><span data-stu-id="4fb66-124">Select the **Display Name** link for the **Dynamics 365 Customer Insights Customer Card Add-in (Preview)** solution.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="4fb66-125">![Hautatu Proiektuaren bistaratze-izena](media/select-display-name.png "Hautatu Proiektuaren bistaratze-izena")</span><span class="sxs-lookup"><span data-stu-id="4fb66-125">![Select display name](media/select-display-name.png "Select display name")</span></span>

1. <span data-ttu-id="4fb66-126">Aukeratu **saioa hasi** eta sartu Customer Insights konfiguratzeko erabiltzen duzun kudeatzaileko kontuaren kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="4fb66-126">Select **Sign in** and enter the credentials for the admin account you use to configure Customer Insights.</span></span>

   > [!NOTE]
   > <span data-ttu-id="4fb66-127">Egiaztatu arakatzailearen pop-up blokeatzaileak autentikazio-leihoa ez duela blokeatzen **Hasi saioa** botoia.</span><span class="sxs-lookup"><span data-stu-id="4fb66-127">Check that the browser pop-up blocker does not block the authentication window when you select the **Sign in** button.</span></span>

1. <span data-ttu-id="4fb66-128">Hautatu datuak eskuratu nahi dituzun ingurunea.</span><span class="sxs-lookup"><span data-stu-id="4fb66-128">Select the environment you want to fetch data from.</span></span>

1. <span data-ttu-id="4fb66-129">Zehaztu zein eremu esleituko zaion Dynamics 365 aplikazioko erregistroari.</span><span class="sxs-lookup"><span data-stu-id="4fb66-129">Define which the field mapping to records in the Dynamics 365 app.</span></span>
   - <span data-ttu-id="4fb66-130">Kontaktu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontaktuaren entitatea.</span><span class="sxs-lookup"><span data-stu-id="4fb66-130">To map with a contact, select the field in the Customer entity that matches the ID of your contact entity.</span></span>
   - <span data-ttu-id="4fb66-131">Kontu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontuaren entitatea.</span><span class="sxs-lookup"><span data-stu-id="4fb66-131">To map with an account, select the field in the Customer entity that matches the ID of your account entity.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="4fb66-132">![Kontaktuaren IDaren eremua](media/contact-id-field.png "Kontaktuaren IDaren eremua")</span><span class="sxs-lookup"><span data-stu-id="4fb66-132">![Contact ID field](media/contact-id-field.png "Contact ID field")</span></span>

1. <span data-ttu-id="4fb66-133">Hautatu **Gorde konfigurazioa** gutxieneko balioaren ezarpenak gordetzeko.</span><span class="sxs-lookup"><span data-stu-id="4fb66-133">Select **Save configuration** to save the settings.</span></span>

1. <span data-ttu-id="4fb66-134">Ondoren, Dynamics 365-en segurtasun rolak esleitu behar dituzu erabiltzaileek bezeroaren txartela pertsonalizatu eta ikusteko aukera izan dezaten.</span><span class="sxs-lookup"><span data-stu-id="4fb66-134">Next, you need to assign security roles in Dynamics 365 so users can customize and see the customer card.</span></span> <span data-ttu-id="4fb66-135">Dynamics 365-en, joan **Ezarpenak** > **Segurtasuna** > **Erabiltzaileak** aukerara.</span><span class="sxs-lookup"><span data-stu-id="4fb66-135">In Dynamics 365, go to **Settings** > **Security** > **Users**.</span></span> <span data-ttu-id="4fb66-136">Hautatu erabiltzaileak rolak editatzeko eta hautatu **Rolak kudeatu**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-136">Select the users to edit user roles and select **Manage roles**.</span></span>

1. <span data-ttu-id="4fb66-137">Esleitu **Customer Insights txartela pertsonalizatzailea** eginkizuna erakunde osoarentzako txartelean erakutsitako edukia pertsonalizatuko duten erabiltzaileentzat.</span><span class="sxs-lookup"><span data-stu-id="4fb66-137">Assign the **Customer Insights Card Customizer** role to users who will customize the content shown on the card for the whole organization.</span></span>

## <a name="add-customer-card-controls-to-forms"></a><span data-ttu-id="4fb66-138">Gehitu bezeroaren txartelaren kontrola inprimakietan</span><span class="sxs-lookup"><span data-stu-id="4fb66-138">Add Customer Card controls to forms</span></span>
  
1. <span data-ttu-id="4fb66-139">Bezero-txartelaren kontrolak zure Kontaktu inprimakian gehitzeko, joan **ezarpenak** > **pertsonalizazioak** Dynamics 365-en.</span><span class="sxs-lookup"><span data-stu-id="4fb66-139">To add the Customer Card controls to your Contact form, go to the **Settings** > **Customizations** in Dynamics 365.</span></span>

1. <span data-ttu-id="4fb66-140">Hautatu **Pertsonalizatu sistema**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-140">Select **Customize the System**.</span></span>

1. <span data-ttu-id="4fb66-141">Arakatu **Harremanetarako** entitatera, zabaldu menua eta ondoren hautatu **Inprimakiak**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-141">Browse to the **Contact** entity, expand it and select **Forms**.</span></span>

1. <span data-ttu-id="4fb66-142">Aukeratu Bezeroaren Txartelak kontrolak gehitu nahi dituzun harremanetarako formularioa.</span><span class="sxs-lookup"><span data-stu-id="4fb66-142">Select the contact form to which you want to add the Customer Card controls.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="4fb66-143">![Hautatu Kontaktuaren inprimakia](media/contact-active-forms.png "Hautatu Kontaktuaren inprimakia")</span><span class="sxs-lookup"><span data-stu-id="4fb66-143">![Select Contact form](media/contact-active-forms.png "Select Contact form")</span></span>

1. <span data-ttu-id="4fb66-144">Kontrola gehitzeko, inprimaki-editore-en, arrastatu edozein eremu **Eremu-esploradorea**-etik kontrolatu demografikoa nahi duzun lekura.</span><span class="sxs-lookup"><span data-stu-id="4fb66-144">To add a control, in the form editor, drag any field from the **Field Explorer** to where you want the control to appear.</span></span>

1. <span data-ttu-id="4fb66-145">Hautatu gehitu berri duzun eremua inprimakian eta gero hautatu **Aldatu propietateak**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-145">Select the field on the form that you just added, and select **Change Properties**.</span></span>

1. <span data-ttu-id="4fb66-146">Joan **Kontrolak** fitxara eta hautatu **Gehitu kontrola**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-146">Go to the **Controls** tab and select **Add Control**.</span></span> <span data-ttu-id="4fb66-147">Aukeratu erabilgarri dauden kontroletako bat eta hautatu **Gehitu**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-147">Choose one of the available custom controls and select **Add**.</span></span>

1. <span data-ttu-id="4fb66-148">Sarbidean **Eremuaren propietateak** elkarrizketa-koadroa, garbitu **Erakutsi etiketa inprimakian** kontrol-laukia.</span><span class="sxs-lookup"><span data-stu-id="4fb66-148">In the **Field Properties** dialog, clear the **Display label on the form** check box.</span></span>

1. <span data-ttu-id="4fb66-149">Hautatu **Web** aukera kontrolerako.</span><span class="sxs-lookup"><span data-stu-id="4fb66-149">Select the **Web** option for the control.</span></span> <span data-ttu-id="4fb66-150">Aberastasunaren kontrolerako, hautatu zein aberastasun mota erakutsi nahi duzun **enrichmentType** eremu.</span><span class="sxs-lookup"><span data-stu-id="4fb66-150">For the Enrichment control, select which enrichment type you want to display by configuring the **enrichmentType** field.</span></span> <span data-ttu-id="4fb66-151">Gehitu aberaste kontrol bereizi bat aberaste mota bakoitzerako.</span><span class="sxs-lookup"><span data-stu-id="4fb66-151">Add a separate enrichment control for each enrichment type.</span></span>

1. <span data-ttu-id="4fb66-152">Aukeratu **Gorde** eta **Argitaratu** kontaktu formulario eguneratua argitaratzeko.</span><span class="sxs-lookup"><span data-stu-id="4fb66-152">Select **Save** and **Publish** to publish the updated contact form.</span></span>

1. <span data-ttu-id="4fb66-153">Joan argitaratutako harremanetarako formulariora.</span><span class="sxs-lookup"><span data-stu-id="4fb66-153">Go to the published contact form.</span></span> <span data-ttu-id="4fb66-154">Gehitu berri den kontrola ikusiko duzu.</span><span class="sxs-lookup"><span data-stu-id="4fb66-154">You'll see the newly added control.</span></span> <span data-ttu-id="4fb66-155">Baliteke erabiltzen duzun lehen aldian saioa hastea.</span><span class="sxs-lookup"><span data-stu-id="4fb66-155">You might need to sign in the first time you use it.</span></span>

1. <span data-ttu-id="4fb66-156">Kontrol pertsonalizatuan erakutsi nahi duzuna pertsonalizatzeko, hautatu editatzeko botoia goiko eskuineko izkinan.</span><span class="sxs-lookup"><span data-stu-id="4fb66-156">To customize what you want to show on the custom control, select the edit button in the upper-right corner.</span></span>

## <a name="upgrade-customer-card-add-in"></a><span data-ttu-id="4fb66-157">Eguneratu Bezeroaren txartelaren osagarria</span><span class="sxs-lookup"><span data-stu-id="4fb66-157">Upgrade Customer Card Add-in</span></span>
<span data-ttu-id="4fb66-158">Bezeroaren txartelaren gehigarria ez da automatikoki eguneratzen.</span><span class="sxs-lookup"><span data-stu-id="4fb66-158">The Customer Card Add-in doesn't upgrade automatically.</span></span> <span data-ttu-id="4fb66-159">Azken bertsiora eguneratzeko, jarraitu prozedura hau gehigarria instalatuta duen Dynamics 365 aplikazioan.</span><span class="sxs-lookup"><span data-stu-id="4fb66-159">To upgrade to the latest version, follow this procedure in the Dynamics 365 app that has the Add-in installed.</span></span>

1. <span data-ttu-id="4fb66-160">Dynamics 365 aplikazioan, joan hona: **Ezarpenak** > **Pertsonalizazioa** eta hautatu **Irtenbideak**.</span><span class="sxs-lookup"><span data-stu-id="4fb66-160">In the Dynamics 365 app, go to **Settings** > **Customization** and select **Solutions**.</span></span>

1. <span data-ttu-id="4fb66-161">Gehigarrien taulan bilatu **CustomerInsightsCustomerCard** eta hautatu errenkada.</span><span class="sxs-lookup"><span data-stu-id="4fb66-161">In the table of add-ins look for **CustomerInsightsCustomerCard** and select the row.</span></span>

1. <span data-ttu-id="4fb66-162">Aukeratu **Aplikatu irtenbidea berritzea** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="4fb66-162">Select the **Apply Solution Upgrade** in the action bar.</span></span>

   :::image type="content" source="media/customer-card-add-in-upgrade.png" alt-text="Eguneratu irtenbidea Dynamics 365 aplikazioen Pertsonalizazio eremuan":::

1. <span data-ttu-id="4fb66-164">Bertsio-berritze prozesua hasi ondoren, kargatzeko adierazle bat ikusiko duzu bertsio berritzea amaitu arte.</span><span class="sxs-lookup"><span data-stu-id="4fb66-164">After starting the upgrade process, you'll see a loading indicator until the upgrade completes.</span></span> <span data-ttu-id="4fb66-165">Bertsio berririk ez badago, bertsio berritzeak errore mezu bat erakutsiko du.</span><span class="sxs-lookup"><span data-stu-id="4fb66-165">If there's no newer version, the upgrade will show an error message.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]