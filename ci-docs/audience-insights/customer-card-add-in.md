---
title: Dynamics 365 aplikazioetarako bezeroaren txartelaren osagarria
description: Erakutsi audientzia estatistiken datuak Dynamics 365 aplikazioetan gehigarri honekin.
ms.date: 05/18/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 88492943ddbf9ae30c64d92b261433b74f34f682
ms.sourcegitcommit: d74430270f1b754322287c4f045d7febdae35be2
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059573"
---
# <a name="customer-card-add-in-preview"></a><span data-ttu-id="240c7-103">Bezeroaren txartelaren osagarria (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="240c7-103">Customer Card Add-in (preview)</span></span>

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

<span data-ttu-id="240c7-104">Lortu zure bezeroen 360 graduko ikuspegia zuzenean Dynamics 365 aplikazioetan.</span><span class="sxs-lookup"><span data-stu-id="240c7-104">Get a 360-degree view of your customers directly in Dynamics 365 apps.</span></span> <span data-ttu-id="240c7-105">Bezeroaren txartelaren gehigarria onartutako Dynamics 365 aplikazio batean instalatuta dagoenez, demografia, estatistikak eta jardueren kronogramak bistaratzea aukera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="240c7-105">With the Customer Card Add-in installed in a supported Dynamics 365 app you can choose to display demographics, insights, and activity timelines.</span></span> <span data-ttu-id="240c7-106">Gehigarriak Customer Insights-etik datuak berreskuratuko ditu konektatutako Dynamics 365 aplikazioko datuak eragin gabe.</span><span class="sxs-lookup"><span data-stu-id="240c7-106">The add-in will retrieve data from Customer Insights without affecting the data in the connected Dynamics 365 app.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="240c7-107">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="240c7-107">Prerequisites</span></span>

- <span data-ttu-id="240c7-108">Gehigarriak Dynamics 365 ereduak gidatutako aplikazioekin soilik funtzionatzen du, hala nola Sales edo bezeroarentzako arreta-zerbitzu, 9.0 bertsioa eta berriagoak.</span><span class="sxs-lookup"><span data-stu-id="240c7-108">The add-in only works with Dynamics 365 model-driven apps, such as Sales or Customer Service, version 9.0 and later.</span></span>
- <span data-ttu-id="240c7-109">Zure Dynamics 365 datuak ikusleekin esleitu ahal izateko izan behar dituzten bezeroen profilak [Dynamics 365 aplikaziotik gehituta Common Data Service konektorea](connect-power-query.md).</span><span class="sxs-lookup"><span data-stu-id="240c7-109">For your Dynamics 365 data to map to the audience insights customer profiles they need to be [ingested from the Dynamics 365 app using the Common Data Service connector](connect-power-query.md).</span></span>
- <span data-ttu-id="240c7-110">Bezero txartelaren gehigarriaren Dynamics 365 erabiltzaile guztiek izan behar dute [erabiltzaile gisa gehitu da](permissions.md) datuak ikusteko ikusleei buruzko informazioetan.</span><span class="sxs-lookup"><span data-stu-id="240c7-110">All Dynamics 365 users of the Customer Card Add-in must be [added as users](permissions.md) in audience insights to see the data.</span></span>
- <span data-ttu-id="240c7-111">[Bilaketa eta iragazki gaitasunak konfiguratuta](search-filter-index.md) audientziari buruzko datuetan funtzionatu behar da.</span><span class="sxs-lookup"><span data-stu-id="240c7-111">[Configured search and filter capabilities](search-filter-index.md) in audience insights are required for lookup of data to work.</span></span>
- <span data-ttu-id="240c7-112">Gehigarrien kontrol bakoitza datu zehatzetan oinarritzen da ikusleen estatistiketan:</span><span class="sxs-lookup"><span data-stu-id="240c7-112">Each add-in control relies on specific data in audience insights:</span></span>
  - <span data-ttu-id="240c7-113">Neurriaren kontrola: [Konfiguratutako neurriak](measures.md) behar dira.</span><span class="sxs-lookup"><span data-stu-id="240c7-113">Measure control: Requires [configured measures](measures.md).</span></span>
  - <span data-ttu-id="240c7-114">Adimenaren kontrola: erabiliz sortutako datuak eskatzen ditu [iragarpenak](predictions.md) edo [eredu pertsonalizatuak](custom-models.md).</span><span class="sxs-lookup"><span data-stu-id="240c7-114">Intelligence control: Requires data generated using [predictions](predictions.md) or [custom models](custom-models.md).</span></span>
  - <span data-ttu-id="240c7-115">Kontrol demografikoa: eremu demografikoak (adina edo generoa), adibidez, bezeroen profil bateratuan daude eskuragarri.</span><span class="sxs-lookup"><span data-stu-id="240c7-115">Demographic control: Demographic fields(such as age or gender) are available in the unified customer profile.</span></span>
  - <span data-ttu-id="240c7-116">Aberastearen kontrola: Aktiboa eskatzen du [hobekuntzak](enrichment-hub.md) bezeroen profiletan aplikatuta.</span><span class="sxs-lookup"><span data-stu-id="240c7-116">Enrichment control: Requires active [enrichments](enrichment-hub.md) applied to customer profiles.</span></span>
  - <span data-ttu-id="240c7-117">Kronogramaren kontrola: [konfiguratutako jarduerak](activities.md) behar dira.</span><span class="sxs-lookup"><span data-stu-id="240c7-117">Timeline control: Requires [configured activities](activities.md).</span></span>

## <a name="install-the-customer-card-add-in"></a><span data-ttu-id="240c7-118">Instalatu Bezeroaren txartelaren osagarria</span><span class="sxs-lookup"><span data-stu-id="240c7-118">Install the Customer Card Add-in</span></span>

<span data-ttu-id="240c7-119">Bezeroaren Txartelaren Gehigarria Dynamics 365-en customer engagement aplikazioetarako irtenbidea da.</span><span class="sxs-lookup"><span data-stu-id="240c7-119">The Customer Card Add-in is a solution for customer engagement apps in Dynamics 365.</span></span> <span data-ttu-id="240c7-120">Konponbidea instalatzeko, joan AppSource eta bilatu **Bezero txartel dinamikoa**.</span><span class="sxs-lookup"><span data-stu-id="240c7-120">To install the solution, go to AppSource and search for **Dynamics Customer Card**.</span></span> <span data-ttu-id="240c7-121">Hautatu [Bezero txartela AppSource-n](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics_365_customer_insights_customer_card_addin?tab=Overview) eta hautatu **Eskuratu orain**.</span><span class="sxs-lookup"><span data-stu-id="240c7-121">Select the [Customer Card Add-in on AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics_365_customer_insights_customer_card_addin?tab=Overview) and select **Get It Now**.</span></span>

<span data-ttu-id="240c7-122">Baliteke Dynamics 365 aplikaziorako zure administratzaileekin saioa hasi behar duzula irtenbidea instalatzeko.</span><span class="sxs-lookup"><span data-stu-id="240c7-122">You may need to sign in with your admin credentials for the Dynamics 365 app to install the solution.</span></span>

<span data-ttu-id="240c7-123">Zenbait denbora behar izango duzu irtenbidea zure ingurunean instalatzeko.</span><span class="sxs-lookup"><span data-stu-id="240c7-123">It can take some time for the solution to be installed to your environment.</span></span>

## <a name="configure-the-customer-card-add-in"></a><span data-ttu-id="240c7-124">Konfiguratu Bezeroaren Kartaren Gehigarria</span><span class="sxs-lookup"><span data-stu-id="240c7-124">Configure the Customer Card Add-in</span></span>

1. <span data-ttu-id="240c7-125">Administratzaile gisa, zoaz webgunera **ezarpenak** atala Dynamics 365-en, eta hautatu **Soluzioak**.</span><span class="sxs-lookup"><span data-stu-id="240c7-125">As an admin, go to the **Settings** section in Dynamics 365 and select **Solutions**.</span></span>

1. <span data-ttu-id="240c7-126">Hautatu botoia **Bistaratu izena** esteka **Dynamics 365 Customer Insights Bezero-txartelaren gehigarria (aurrebista)** konponbidea.</span><span class="sxs-lookup"><span data-stu-id="240c7-126">Select the **Display Name** link for the **Dynamics 365 Customer Insights Customer Card Add-in (Preview)** solution.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="240c7-127">![Hautatu Proiektuaren bistaratze-izena](media/select-display-name.png "Hautatu Proiektuaren bistaratze-izena")</span><span class="sxs-lookup"><span data-stu-id="240c7-127">![Select display name](media/select-display-name.png "Select display name")</span></span>

1. <span data-ttu-id="240c7-128">Aukeratu **saioa hasi** eta sartu Customer Insights konfiguratzeko erabiltzen duzun kudeatzaileko kontuaren kredentzialak.</span><span class="sxs-lookup"><span data-stu-id="240c7-128">Select **Sign in** and enter the credentials for the admin account you use to configure Customer Insights.</span></span>

   > [!NOTE]
   > <span data-ttu-id="240c7-129">Egiaztatu arakatzailearen pop-up blokeatzaileak autentikazio-leihoa ez duela blokeatzen **Hasi saioa** botoia.</span><span class="sxs-lookup"><span data-stu-id="240c7-129">Check that the browser pop-up blocker does not block the authentication window when you select the **Sign in** button.</span></span>

1. <span data-ttu-id="240c7-130">Hautatu datuak eskuratu nahi dituzun Customer Insights ingurunea.</span><span class="sxs-lookup"><span data-stu-id="240c7-130">Select the Customer Insights environment you want to fetch data from.</span></span>

1. <span data-ttu-id="240c7-131">Zehaztu Dynamics 365 aplikazioko erregistroen eremuen mapak.</span><span class="sxs-lookup"><span data-stu-id="240c7-131">Define the field mapping to records in the Dynamics 365 app.</span></span> <span data-ttu-id="240c7-132">Customer Insights-en dituzun datuen arabera, aukera hauek esleitzea aukeratu dezakezu:</span><span class="sxs-lookup"><span data-stu-id="240c7-132">Depending on your data in Customer Insights you can choose to map the following options:</span></span>
   - <span data-ttu-id="240c7-133">Kontaktu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontaktuaren entitatea.</span><span class="sxs-lookup"><span data-stu-id="240c7-133">To map with a contact, select the field in the Customer entity that matches the ID of your contact entity.</span></span>
   - <span data-ttu-id="240c7-134">Kontu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontuaren entitatea.</span><span class="sxs-lookup"><span data-stu-id="240c7-134">To map with an account, select the field in the Customer entity that matches the ID of your account entity.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="240c7-135">![Kontaktuaren IDaren eremua](media/contact-id-field.png "Kontaktuaren IDaren eremua")</span><span class="sxs-lookup"><span data-stu-id="240c7-135">![Contact ID field](media/contact-id-field.png "Contact ID field")</span></span>

1. <span data-ttu-id="240c7-136">Hautatu **Gorde konfigurazioa** gutxieneko balioaren ezarpenak gordetzeko.</span><span class="sxs-lookup"><span data-stu-id="240c7-136">Select **Save configuration** to save the settings.</span></span>

1. <span data-ttu-id="240c7-137">Ondoren, Dynamics 365-en segurtasun rolak esleitu behar dituzu erabiltzaileek bezeroaren txartela pertsonalizatu eta ikusteko aukera izan dezaten.</span><span class="sxs-lookup"><span data-stu-id="240c7-137">Next, you need to assign security roles in Dynamics 365 so users can customize and see the customer card.</span></span> <span data-ttu-id="240c7-138">Dynamics 365-en, joan **Ezarpenak** > **Segurtasuna** > **Erabiltzaileak** aukerara.</span><span class="sxs-lookup"><span data-stu-id="240c7-138">In Dynamics 365, go to **Settings** > **Security** > **Users**.</span></span> <span data-ttu-id="240c7-139">Hautatu erabiltzaileak rolak editatzeko eta hautatu **Rolak kudeatu**.</span><span class="sxs-lookup"><span data-stu-id="240c7-139">Select the users to edit user roles and select **Manage roles**.</span></span>

1. <span data-ttu-id="240c7-140">Esleitu **Customer Insights txartela pertsonalizatzailea** eginkizuna erakunde osoarentzako txartelean erakutsitako edukia pertsonalizatuko duten erabiltzaileentzat.</span><span class="sxs-lookup"><span data-stu-id="240c7-140">Assign the **Customer Insights Card Customizer** role to users who will customize the content shown on the card for the whole organization.</span></span>

## <a name="add-customer-card-controls-to-forms"></a><span data-ttu-id="240c7-141">Gehitu bezeroaren txartelaren kontrola inprimakietan</span><span class="sxs-lookup"><span data-stu-id="240c7-141">Add Customer Card controls to forms</span></span>
  
1. <span data-ttu-id="240c7-142">Bezero-txartelaren kontrolak zure Kontaktu inprimakian gehitzeko, joan **ezarpenak** > **pertsonalizazioak** Dynamics 365-en.</span><span class="sxs-lookup"><span data-stu-id="240c7-142">To add the Customer Card controls to your Contact form, go to the **Settings** > **Customizations** in Dynamics 365.</span></span>

1. <span data-ttu-id="240c7-143">Hautatu **Pertsonalizatu sistema**.</span><span class="sxs-lookup"><span data-stu-id="240c7-143">Select **Customize the System**.</span></span>

1. <span data-ttu-id="240c7-144">Arakatu **Harremanetarako** entitatera, zabaldu menua eta ondoren hautatu **Inprimakiak**.</span><span class="sxs-lookup"><span data-stu-id="240c7-144">Browse to the **Contact** entity, expand it and select **Forms**.</span></span>

1. <span data-ttu-id="240c7-145">Aukeratu Bezeroaren Txartelak kontrolak gehitu nahi dituzun harremanetarako formularioa.</span><span class="sxs-lookup"><span data-stu-id="240c7-145">Select the contact form to which you want to add the Customer Card controls.</span></span>

    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="240c7-146">![Hautatu Kontaktuaren inprimakia](media/contact-active-forms.png "Hautatu Kontaktuaren inprimakia")</span><span class="sxs-lookup"><span data-stu-id="240c7-146">![Select Contact form](media/contact-active-forms.png "Select Contact form")</span></span>

1. <span data-ttu-id="240c7-147">Kontrola gehitzeko, inprimaki-editore-en, arrastatu edozein eremu **Eremu-esploradorea**-etik kontrolatu demografikoa nahi duzun lekura.</span><span class="sxs-lookup"><span data-stu-id="240c7-147">To add a control, in the form editor, drag any field from the **Field Explorer** to where you want the control to appear.</span></span>

1. <span data-ttu-id="240c7-148">Hautatu gehitu berri duzun eremua inprimakian eta gero hautatu **Aldatu propietateak**.</span><span class="sxs-lookup"><span data-stu-id="240c7-148">Select the field on the form that you just added, and select **Change Properties**.</span></span>

1. <span data-ttu-id="240c7-149">Joan **Kontrolak** fitxara eta hautatu **Gehitu kontrola**.</span><span class="sxs-lookup"><span data-stu-id="240c7-149">Go to the **Controls** tab and select **Add Control**.</span></span> <span data-ttu-id="240c7-150">Aukeratu erabilgarri dauden kontroletako bat eta hautatu **Gehitu**.</span><span class="sxs-lookup"><span data-stu-id="240c7-150">Choose one of the available custom controls and select **Add**.</span></span>

1. <span data-ttu-id="240c7-151">Sarbidean **Eremuaren propietateak** elkarrizketa-koadroa, garbitu **Erakutsi etiketa inprimakian** kontrol-laukia.</span><span class="sxs-lookup"><span data-stu-id="240c7-151">In the **Field Properties** dialog, clear the **Display label on the form** check box.</span></span>

1. <span data-ttu-id="240c7-152">Hautatu **Web** aukera kontrolerako.</span><span class="sxs-lookup"><span data-stu-id="240c7-152">Select the **Web** option for the control.</span></span> <span data-ttu-id="240c7-153">Aberastasunaren kontrolerako, hautatu zein aberastasun mota erakutsi nahi duzun **enrichmentType** eremu.</span><span class="sxs-lookup"><span data-stu-id="240c7-153">For the Enrichment control, select which enrichment type you want to display by configuring the **enrichmentType** field.</span></span> <span data-ttu-id="240c7-154">Gehitu aberaste kontrol bereizi bat aberaste mota bakoitzerako.</span><span class="sxs-lookup"><span data-stu-id="240c7-154">Add a separate enrichment control for each enrichment type.</span></span>

1. <span data-ttu-id="240c7-155">Aukeratu **Gorde** eta **Argitaratu** kontaktu formulario eguneratua argitaratzeko.</span><span class="sxs-lookup"><span data-stu-id="240c7-155">Select **Save** and **Publish** to publish the updated contact form.</span></span>

1. <span data-ttu-id="240c7-156">Joan argitaratutako harremanetarako formulariora.</span><span class="sxs-lookup"><span data-stu-id="240c7-156">Go to the published contact form.</span></span> <span data-ttu-id="240c7-157">Gehitu berri den kontrola ikusiko duzu.</span><span class="sxs-lookup"><span data-stu-id="240c7-157">You'll see the newly added control.</span></span> <span data-ttu-id="240c7-158">Baliteke erabiltzen duzun lehen aldian saioa hastea.</span><span class="sxs-lookup"><span data-stu-id="240c7-158">You might need to sign in the first time you use it.</span></span>

1. <span data-ttu-id="240c7-159">Kontrol pertsonalizatuan erakutsi nahi duzuna pertsonalizatzeko, hautatu editatzeko botoia goiko eskuineko izkinan.</span><span class="sxs-lookup"><span data-stu-id="240c7-159">To customize what you want to show on the custom control, select the edit button in the upper-right corner.</span></span>

## <a name="upgrade-customer-card-add-in"></a><span data-ttu-id="240c7-160">Eguneratu Bezeroaren txartelaren osagarria</span><span class="sxs-lookup"><span data-stu-id="240c7-160">Upgrade Customer Card Add-in</span></span>
<span data-ttu-id="240c7-161">Bezeroaren txartelaren gehigarria ez da automatikoki eguneratzen.</span><span class="sxs-lookup"><span data-stu-id="240c7-161">The Customer Card Add-in doesn't upgrade automatically.</span></span> <span data-ttu-id="240c7-162">Azken bertsiora eguneratzeko, jarraitu prozedura hau gehigarria instalatuta duen Dynamics 365 aplikazioan.</span><span class="sxs-lookup"><span data-stu-id="240c7-162">To upgrade to the latest version, follow this procedure in the Dynamics 365 app that has the Add-in installed.</span></span>

1. <span data-ttu-id="240c7-163">Dynamics 365 aplikazioan, joan hona: **Ezarpenak** > **Pertsonalizazioa** eta hautatu **Irtenbideak**.</span><span class="sxs-lookup"><span data-stu-id="240c7-163">In the Dynamics 365 app, go to **Settings** > **Customization** and select **Solutions**.</span></span>

1. <span data-ttu-id="240c7-164">Gehigarrien taulan bilatu **CustomerInsightsCustomerCard** eta hautatu errenkada.</span><span class="sxs-lookup"><span data-stu-id="240c7-164">In the table of add-ins look for **CustomerInsightsCustomerCard** and select the row.</span></span>

1. <span data-ttu-id="240c7-165">Aukeratu **Aplikatu irtenbidea berritzea** ekintza barran.</span><span class="sxs-lookup"><span data-stu-id="240c7-165">Select the **Apply Solution Upgrade** in the action bar.</span></span>

   :::image type="content" source="media/customer-card-add-in-upgrade.png" alt-text="Eguneratu irtenbidea Dynamics 365 aplikazioen Pertsonalizazio eremuan":::

1. <span data-ttu-id="240c7-167">Bertsio-berritze prozesua hasi ondoren, kargatzeko adierazle bat ikusiko duzu bertsio berritzea amaitu arte.</span><span class="sxs-lookup"><span data-stu-id="240c7-167">After starting the upgrade process, you'll see a loading indicator until the upgrade completes.</span></span> <span data-ttu-id="240c7-168">Bertsio berririk ez badago, bertsio berritzeak errore mezu bat erakutsiko du.</span><span class="sxs-lookup"><span data-stu-id="240c7-168">If there's no newer version, the upgrade will show an error message.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
