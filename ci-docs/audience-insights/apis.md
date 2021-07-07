---
title: Egin lan API-ekin
description: Erabili APIak eta ulertu mugak.
ms.date: 05/10/2021
ms.reviewer: wimohabb
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
ms.openlocfilehash: 9326f821f9970ba2254ab804814e369abb677eb0
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304727"
---
# <a name="work-with-customer-insights-apis"></a><span data-ttu-id="617ad-103">Lan egin Customer Insights APIekin</span><span class="sxs-lookup"><span data-stu-id="617ad-103">Work with Customer Insights APIs</span></span>

<span data-ttu-id="617ad-104">Dynamics 365 Customer Insights APIak eskaintzen ditu zure datuetan oinarritutako zure aplikazioak eraikitzeko Customer Insights-en.</span><span class="sxs-lookup"><span data-stu-id="617ad-104">Dynamics 365 Customer Insights provides APIs to build your own applications based on your data in Customer Insights.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="617ad-105">API horien xehetasunak hemen daude zerrendatuta: [Customer Insights APIen erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights).</span><span class="sxs-lookup"><span data-stu-id="617ad-105">Details of these APIs are listed on the [Customer Insights APIs reference](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights).</span></span> <span data-ttu-id="617ad-106">Eragiketei, parametroei eta erantzunen inguruko informazio osagarria biltzen dute.</span><span class="sxs-lookup"><span data-stu-id="617ad-106">They include additional information about operations, parameters, and responses.</span></span>

<span data-ttu-id="617ad-107">Artikulu honetan Customer Insights APIak nola sartu, Azure aplikazioen erregistroa sortu eta eskuragarri dauden bezero liburutegiekin nola hasi deskribatzen da.</span><span class="sxs-lookup"><span data-stu-id="617ad-107">This article describes how to access the Customer Insights APIs, create an Azure App Registration, and get started with the available client libraries.</span></span>

## <a name="get-started-trying-the-customer-insights-apis"></a><span data-ttu-id="617ad-108">Hasi Customer Insights APIak probatzen</span><span class="sxs-lookup"><span data-stu-id="617ad-108">Get started trying the Customer Insights APIs</span></span>

1. <span data-ttu-id="617ad-109">[Hasi saioa](https://home.ci.ai.dynamics.com) Customer Insights-en.</span><span class="sxs-lookup"><span data-stu-id="617ad-109">[Sign in](https://home.ci.ai.dynamics.com) to Customer Insights.</span></span> <span data-ttu-id="617ad-110">Harpidetzarik ez baduzu oraindik, [erregistratu Customer Insights-en probako bertsiorako](https://aka.ms/tryci).</span><span class="sxs-lookup"><span data-stu-id="617ad-110">If you don't have a subscription yet, [sign up for a trial of Customer Insights](https://aka.ms/tryci).</span></span>

1. <span data-ttu-id="617ad-111">Customer Insights ingurunean APIak gaitzeko, joan hona: **Administratzailea** > **Baimenak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-111">To enable APIs on your Customer Insights environment, go to **Admin** > **Permissions**.</span></span> <span data-ttu-id="617ad-112">Administratzaile baimenak beharko dituzu horretarako.</span><span class="sxs-lookup"><span data-stu-id="617ad-112">You'll need admin permissions to do so.</span></span>

1. <span data-ttu-id="617ad-113">Joan **APIak** fitxara eta hautatu **Gaitu** botoia.</span><span class="sxs-lookup"><span data-stu-id="617ad-113">Go to the **APIs** tab and select the **Enable** button.</span></span>    
 
   <span data-ttu-id="617ad-114">APIak gaitzeak API eskaeretan erabiltzen den harpidetza gako nagusia eta bigarren mailakoa sortzen ditu zure instantziarako.</span><span class="sxs-lookup"><span data-stu-id="617ad-114">Enabling the APIs creates a primary and secondary subscription key for your instance that gets used in the API requests.</span></span> <span data-ttu-id="617ad-115">Gakoak birsortu ditzakezu **Birsortu nagusia** edo **Birsortu bigarren mailakoa** hautatuz hemen: **Administratzailea** > **Baimenak** > **APIak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-115">You can regenerate the keys by selecting the **Regenerate primary** or **Regenerate secondary** on **Admin** > **Permissions** > **APIs**.</span></span>

   :::image type="content" source="media/enable-apis.gif" alt-text="Gaitu Customer Insights APIak":::

1. <span data-ttu-id="617ad-117">Hautatu **Esploratu gure APIak** hurrengora [probatu APIak](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances).</span><span class="sxs-lookup"><span data-stu-id="617ad-117">Select **Explore our APIs** to [try out the APIs](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances).</span></span>

1. <span data-ttu-id="617ad-118">Aukeratu API eragiketa bat eta hautatu **Probatu**.</span><span class="sxs-lookup"><span data-stu-id="617ad-118">Choose an API operation and select **Try it**.</span></span>

1. <span data-ttu-id="617ad-119">Alboko panelean, ezarri balioa **Baimena** menuan goitibeherako menua **inplizitua**.</span><span class="sxs-lookup"><span data-stu-id="617ad-119">In the side pane, set the value in the **Authorization** dropdown menu to **implicit**.</span></span> <span data-ttu-id="617ad-120">`Authorization` goiburua eramaile token batekin gehitzen da.</span><span class="sxs-lookup"><span data-stu-id="617ad-120">The `Authorization` header gets added with a bearer token.</span></span> <span data-ttu-id="617ad-121">Zure harpidetza gakoa automatikoki beteko da.</span><span class="sxs-lookup"><span data-stu-id="617ad-121">Your subscription key will be automatically populated.</span></span>
  
1. <span data-ttu-id="617ad-122">Aukeran, gehitu beharrezko kontsulta parametro guztiak.</span><span class="sxs-lookup"><span data-stu-id="617ad-122">Optionally, add all necessary query parameters.</span></span>

1. <span data-ttu-id="617ad-123">Joan alboko panelaren behealdera eta hautatu **Bidali**.</span><span class="sxs-lookup"><span data-stu-id="617ad-123">Scroll to the bottom of the side pane and select **Send**.</span></span>

<span data-ttu-id="617ad-124">HTTP erantzuna laster agertuko da behean.</span><span class="sxs-lookup"><span data-stu-id="617ad-124">The HTTP response will soon appear below.</span></span>

   :::image type="content" source="media/try-apis.gif" alt-text="APIak nola probatu.":::

## <a name="create-a-new-app-registration-in-the-azure-portal"></a><span data-ttu-id="617ad-126">Sortu aplikazioen erregistro berria Azure atarian</span><span class="sxs-lookup"><span data-stu-id="617ad-126">Create a new app registration in the Azure portal</span></span>

<span data-ttu-id="617ad-127">Urrats hauei esker, Azure aplikazio batean Customer Insights APIak erabiltzen hasi ahal izango dituzu eskuordetutako baimenak erabiliz.</span><span class="sxs-lookup"><span data-stu-id="617ad-127">These steps help you get started with using the Customer Insights APIs in an Azure application using delegated permissions.</span></span> <span data-ttu-id="617ad-128">Ziurtatu [Hasteko atala](#get-started-trying-the-customer-insights-apis) lehenengoa.</span><span class="sxs-lookup"><span data-stu-id="617ad-128">Make sure to complete the [Getting started section](#get-started-trying-the-customer-insights-apis) first.</span></span>

1. <span data-ttu-id="617ad-129">Saioa hasi [Azure atarian](https://portal.azure.com) Customer Insights datuetara sar daitekeen kontuarekin.</span><span class="sxs-lookup"><span data-stu-id="617ad-129">Sign in to the [Azure portal](https://portal.azure.com) with the account that can access the Customer Insights data.</span></span>

1. <span data-ttu-id="617ad-130">Ezkerrean, hautatu **Aplikazioen erregistroak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-130">On the left, select **App registrations**.</span></span>

1. <span data-ttu-id="617ad-131">Aukeratu **Erregistro berria**, eman aplikazioaren izena eta aukeratu kontu mota.</span><span class="sxs-lookup"><span data-stu-id="617ad-131">Select **New registration**, provide an application name and choose the account type.</span></span>
 
   <span data-ttu-id="617ad-132">Aukeran, gehitu birbideratzeko URLa.</span><span class="sxs-lookup"><span data-stu-id="617ad-132">Optionally, add a redirect URL.</span></span> <span data-ttu-id="617ad-133">http://localhost nahikoa da zure ordenagailu lokalean aplikazio bat garatzeko.</span><span class="sxs-lookup"><span data-stu-id="617ad-133">http://localhost is sufficient for developing an application on your local computer.</span></span>

1. <span data-ttu-id="617ad-134">Aplikazio berriaren erregistroan, joan hona: **API baimenak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-134">On your new App registration, go to **API permissions**.</span></span>

   :::image type="content" source="media/app-registration-1.gif" alt-text="Nola ezarri API baimenak aplikazioaren erregistroan.":::

1. <span data-ttu-id="617ad-136">Aukeratu **Gehitu baimena** eta hautatu **Customer Insights** alboko panelean.</span><span class="sxs-lookup"><span data-stu-id="617ad-136">Select **Add a permission** and select **Customer Insights** in the side pane.</span></span>

1. <span data-ttu-id="617ad-137">**Baimen mota**, hautatu **Baimen delegatuak** eta, ondoren, hautatu **user_impersonation** baimena.</span><span class="sxs-lookup"><span data-stu-id="617ad-137">For **Permission type**, select **Delegated permissions** and then select the **user_impersonation** permission.</span></span>

1. <span data-ttu-id="617ad-138">Hautatu **Gehitu baimenak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-138">Select **Add permissions**.</span></span> <span data-ttu-id="617ad-139">Erabiltzailearen saioa hasi gabe APIan sartu behar baduzu, berrikusi [Zerbitzaritik zerbitzarirako aplikazioen baimenak](#server-to-server-application-permissions) atala.</span><span class="sxs-lookup"><span data-stu-id="617ad-139">If you need to access the API without a user signing in, review the [Server-to-server application permissions](#server-to-server-application-permissions) section.</span></span>

1. <span data-ttu-id="617ad-140">Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="617ad-140">Select **Grant admin consent for...** to complete the app registration.</span></span>

<span data-ttu-id="617ad-141">Aplikazioaren / Bezeroaren IDa erabil dezakezu Microsoft Authentication Library (MSAL) zerbitzuarekin aplikazioa erregistratzeko, eskaerarekin batera APIra bidaltzeko titularraren tokena eskuratzeko.</span><span class="sxs-lookup"><span data-stu-id="617ad-141">You can use the Application/Client ID for this app registration with the Microsoft Authentication Library (MSAL) to obtain a bearer token to send with your request to the API.</span></span>

:::image type="content" source="media/grant-admin-consent.gif" alt-text="Administratzailearen baimena nola eman.":::

<span data-ttu-id="617ad-143">MSAL-i buruzko informazio gehiago lortzeko, ikusi [Microsoft Authentication Library (MSAL) zerbitzuaren ikuspegi orokorra](/azure/active-directory/develop/msal-overview).</span><span class="sxs-lookup"><span data-stu-id="617ad-143">For more information about MSAL, see [Overview of Microsoft Authentication Library (MSAL)](/azure/active-directory/develop/msal-overview).</span></span>

<span data-ttu-id="617ad-144">Azure aplikazioen erregistroari buruzko informazio gehiago lortzeko, ikusi [Erregistratu eskaera bat](/azure/active-directory/develop/quickstart-register-app.md#register-an-application).</span><span class="sxs-lookup"><span data-stu-id="617ad-144">For more information about app registration in Azure, see [Register an application](/azure/active-directory/develop/quickstart-register-app.md#register-an-application).</span></span>

<span data-ttu-id="617ad-145">APIak gure bezeroen liburutegietan erabiltzeari buruzko informazioa lortzeko, ikusi [Customer Insights bezero liburutegiak](#customer-insights-client-libraries).</span><span class="sxs-lookup"><span data-stu-id="617ad-145">For information on using the APIs in our client libraries, see [Customer Insights client libraries](#customer-insights-client-libraries).</span></span>

### <a name="server-to-server-application-permissions"></a><span data-ttu-id="617ad-146">Zerbitzaritik zerbitzarirako aplikazioen baimenak</span><span class="sxs-lookup"><span data-stu-id="617ad-146">Server-to-server application permissions</span></span>

<span data-ttu-id="617ad-147">[Aplikazioak erregistratzeko atalak](#create-a-new-app-registration-in-the-azure-portal) erabiltzaileak autentikatzeko saioa hastea eskatzen duen aplikazio bat nola erregistratu azaltzen du.</span><span class="sxs-lookup"><span data-stu-id="617ad-147">The [app registration section](#create-a-new-app-registration-in-the-azure-portal) outlines how to register an app that requires a user to sign in for authentication.</span></span> <span data-ttu-id="617ad-148">Ikasi erabiltzaileen elkarrekintzarik behar ez duen eta zerbitzarian exekutatu daitekeen aplikazioen erregistroa nola sortu.</span><span class="sxs-lookup"><span data-stu-id="617ad-148">Learn how to create an app registration that does not need user interaction and can be run on a server.</span></span>

1. <span data-ttu-id="617ad-149">Azure atariko aplikazioaren erregistroan, joan hona: **API baimenak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-149">On your App registration in the Azure portal, go to **API permissions**.</span></span>

1. <span data-ttu-id="617ad-150">Hautatu **Gehitu baimena**.</span><span class="sxs-lookup"><span data-stu-id="617ad-150">Select **Add a permission**.</span></span> 

1. <span data-ttu-id="617ad-151">Aukeratu **Nire erakundeak erabiltzen dituen APIak** fitxa eta aukeratu **Customer Insights-erako Dynamics 365 AI** zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="617ad-151">Select the **APIs my organization uses** tab and choose **Dynamics 365 AI for Customer Insights** from the list.</span></span> 

1. <span data-ttu-id="617ad-152">**Baimen mota**, hautatu **Aplikazioen baimenak** eta, ondoren, hautatu **CustomerInsights.Api.All** baimena.</span><span class="sxs-lookup"><span data-stu-id="617ad-152">For **Permission type**, select **Application permissions** and then select the **CustomerInsights.Api.All** permission.</span></span>

1. <span data-ttu-id="617ad-153">Hautatu **Gehitu baimenak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-153">Select **Add permissions**.</span></span>

1. <span data-ttu-id="617ad-154">Aplikazio berriaren erregistratzeko, itzuli hona: **API baimenak**.</span><span class="sxs-lookup"><span data-stu-id="617ad-154">Go back to **API permissions** for your app registration.</span></span>

1. <span data-ttu-id="617ad-155">Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="617ad-155">Select **Grant admin consent for...** to complete the app registration.</span></span>

   :::image type="content" source="media/grant-admin-consent.gif" alt-text="Administratzailearen baimena nola eman.":::

1. <span data-ttu-id="617ad-157">Amaitzeko, aplikazioaren erregistroaren izena gehitu behar dugu erabiltzaile gisa Customer Insights-en.</span><span class="sxs-lookup"><span data-stu-id="617ad-157">To conclude, we have to add the name of the app registration as a user in Customer Insights.</span></span>  
   
   <span data-ttu-id="617ad-158">Ireki Customer Insights, joan hona: **Administratzailea** > **Baimenak** eta hautatu **Gehitu erabiltzailea**.</span><span class="sxs-lookup"><span data-stu-id="617ad-158">Open Customer Insights, go to **Admin** > **Permissions** and select **Add user**.</span></span>

1. <span data-ttu-id="617ad-159">Bilatu zure aplikazioaren erregistroaren izena, hautatu bilaketaren emaitzetan eta hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="617ad-159">Search for the name of your app registration, select it from the search results, and select **Save**.</span></span>

## <a name="customer-insights-client-libraries"></a><span data-ttu-id="617ad-160">Customer Insights bezero liburutegiak</span><span class="sxs-lookup"><span data-stu-id="617ad-160">Customer Insights client libraries</span></span>

<span data-ttu-id="617ad-161">Atal honek Customer Insights APIen eskuragarri dauden bezero liburutegiak erabiltzen hasteko laguntza ematen dizu.</span><span class="sxs-lookup"><span data-stu-id="617ad-161">This section helps you get started using the client libraries available for the Customer Insights APIs.</span></span> <span data-ttu-id="617ad-162">Liburutegiaren iturburu kodea eta adibideen aplikazio guztiak hemen aurki ditzakezu [Customer Insights GitHub orria](https://github.com/microsoft/Dynamics365-CustomerInsights-Client-Libraries).</span><span class="sxs-lookup"><span data-stu-id="617ad-162">All library source code and sample applications can be found on the [Customer Insights GitHub page](https://github.com/microsoft/Dynamics365-CustomerInsights-Client-Libraries).</span></span> 

### <a name="c-nuget"></a><span data-ttu-id="617ad-163">C# NuGet</span><span class="sxs-lookup"><span data-stu-id="617ad-163">C# NuGet</span></span>

<span data-ttu-id="617ad-164">Ikasi NuGet.org orrialdetik C# bezero liburutegiak erabiltzen hasten. NuGet paketeari buruzko informazio gehiagorako, ikusi [Microsoft.Dynamics.CustomerInsights.Api](https://www.nuget.org/packages/Microsoft.Dynamics.CustomerInsights.Api/).</span><span class="sxs-lookup"><span data-stu-id="617ad-164">Learn how to get started using the C# client libraries from NuGet.org. For more information on the NuGet package, see [Microsoft.Dynamics.CustomerInsights.Api](https://www.nuget.org/packages/Microsoft.Dynamics.CustomerInsights.Api/).</span></span> <span data-ttu-id="617ad-165">Gaur egun, pakete hau netstandard2.0 eta netcoreapp2.0 markoetara bideratuta dago.</span><span class="sxs-lookup"><span data-stu-id="617ad-165">Currently, this package targets the netstandard2.0 and netcoreapp2.0 frameworks.</span></span>

#### <a name="add-the-c-client-library-to-a-c-project"></a><span data-ttu-id="617ad-166">Gehitu C # bezero liburutegia C # proiektu batera</span><span class="sxs-lookup"><span data-stu-id="617ad-166">Add the C# client library to a C# project</span></span>

1. <span data-ttu-id="617ad-167">Visual Studio-n, ireki proiektuaren **NuGet Pakete kudeatzailea**.</span><span class="sxs-lookup"><span data-stu-id="617ad-167">In Visual Studio, open the **NuGet Package Manager** for your project.</span></span>

1. <span data-ttu-id="617ad-168">Bilatu **Microsoft.Dynamics.CustomerInsights.Api**.</span><span class="sxs-lookup"><span data-stu-id="617ad-168">Search for **Microsoft.Dynamics.CustomerInsights.Api**.</span></span>

1. <span data-ttu-id="617ad-169">Aukeratu **Instalatu** paketea proiektuari gehitzeko.</span><span class="sxs-lookup"><span data-stu-id="617ad-169">Select **Install** to add the package to the project.</span></span>
 
   <span data-ttu-id="617ad-170">Bestela, exekutatu komando hau **NuGet Pakete kudeatzailearen kontsolan**: `Install-Package -Id Microsoft.Dynamics.CustomerInsights.Api -Source nuget.org -ProjectName <project name> [-Version <version>]`</span><span class="sxs-lookup"><span data-stu-id="617ad-170">Alternatively, run this command in the **NuGet Package Manager Console**: `Install-Package -Id Microsoft.Dynamics.CustomerInsights.Api -Source nuget.org -ProjectName <project name> [-Version <version>]`</span></span>

   :::image type="content" source="media/visual-studio-nuget-package.gif" alt-text="Gehitu NuGet paketea Visual Studio proiektuan":::

#### <a name="use-the-c-client-library"></a><span data-ttu-id="617ad-172">Erabili C # bezero liburutegia</span><span class="sxs-lookup"><span data-stu-id="617ad-172">Use the C# client library</span></span>

1. <span data-ttu-id="617ad-173">Erabili [Microsoft autentifikazio liburutegia (MSAL)](/azure/active-directory/develop/msal-overview) `AccessToken` bat lortzeko lehendik duzun [Azure aplikazioaren erregistroa](#create-a-new-app-registration-in-the-azure-portal) erabiliz.</span><span class="sxs-lookup"><span data-stu-id="617ad-173">Use the [Microsoft Authentication Library (MSAL)](/azure/active-directory/develop/msal-overview) to get an `AccessToken` using your existing [Azure app registration](#create-a-new-app-registration-in-the-azure-portal).</span></span>

1. <span data-ttu-id="617ad-174">Token bat behar bezala autentifikatu eta eskuratu ondoren, eraiki berria edo erabili lehendik dagoen `HttpClient` **DefaultRequestHeaders "Baimena"** gehigarria **Titularra <access token>** gisa eta **Ocp-Apim-Subscription-Key** [Customer Insights inguruneko **harpidetza gakoa**](#get-started-trying-the-customer-insights-apis) gisa ezarrita.</span><span class="sxs-lookup"><span data-stu-id="617ad-174">After successfully authenticating and acquiring a token, construct a new or use an existing `HttpClient` with the additional **DefaultRequestHeaders "Authorization"** set to **Bearer <access token>** and **Ocp-Apim-Subscription-Key** set to the [**subscription key** from your Customer Insights environment](#get-started-trying-the-customer-insights-apis).</span></span>   
 
   <span data-ttu-id="617ad-175">Berrezarri **Baimena** goiburua egokia denean.</span><span class="sxs-lookup"><span data-stu-id="617ad-175">Reset the **Authorization** header when appropriate.</span></span> <span data-ttu-id="617ad-176">Adibidez, token-a iraungi denean.</span><span class="sxs-lookup"><span data-stu-id="617ad-176">For example, when the token expired.</span></span>

1. <span data-ttu-id="617ad-177">Pasatu `HttpClient` `CustomerInsights` bezeroaren sorkuntzara.</span><span class="sxs-lookup"><span data-stu-id="617ad-177">Pass this `HttpClient` into the construction of the `CustomerInsights` client.</span></span>

   :::image type="content" source="media/httpclient-sample.png" alt-text="Httpclient-en lagina":::

1. <span data-ttu-id="617ad-179">Egin deiak bezeroekin "luzapen metodoetara", adibidez, `GetAllInstancesAsync`.</span><span class="sxs-lookup"><span data-stu-id="617ad-179">Make calls with the client to the "extension methods"—for example, `GetAllInstancesAsync`.</span></span> <span data-ttu-id="617ad-180">Azpiko `Microsoft.Rest.HttpOperationResponse`-rako sarbidea hobetsi bada, erabili "http mezuen metodoak" erabili, adibidez, `GetAllInstancesWithHttpMessagesAsync`.</span><span class="sxs-lookup"><span data-stu-id="617ad-180">If access to the underlying `Microsoft.Rest.HttpOperationResponse` is preferred, use the "http message methods"—for example, `GetAllInstancesWithHttpMessagesAsync`.</span></span>

1. <span data-ttu-id="617ad-181">Erantzuna `object` motakoa izango da ziurrenik, metodoak hainbat mota itzul ditzakeelako (adibidez, `IList<InstanceInfo>` eta `ApiErrorResult`).</span><span class="sxs-lookup"><span data-stu-id="617ad-181">The response will likely be of type `object` because the method can return multiple types (for example, `IList<InstanceInfo>` and `ApiErrorResult`).</span></span> <span data-ttu-id="617ad-182">Itzulera mota egiaztatzeko, objektuak segurtasunez bihur ditzakezu eragiketaren [APIaren xehetasunen orrian](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) zehaztutako erantzun motara.</span><span class="sxs-lookup"><span data-stu-id="617ad-182">To check the return type, you can safely cast the objects into the response types specified on the [API details page](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) for that operation.</span></span>    
   
   <span data-ttu-id="617ad-183">Eskaerari buruzko informazio gehiago behar izanez gero, erabili **http mezuen metodoak** erantzun gordineko objektuan sartzeko.</span><span class="sxs-lookup"><span data-stu-id="617ad-183">If more information on the request is needed, use the **http message methods** to access the raw response object.</span></span>

### <a name="nodejs-package"></a><span data-ttu-id="617ad-184">NodeJS paketea</span><span class="sxs-lookup"><span data-stu-id="617ad-184">NodeJS package</span></span>

<span data-ttu-id="617ad-185">Erabili NPM bidez eskuragarri dauden NodeJS bezero liburutegiak: https://www.npmjs.com/package/@microsoft/customerinsights</span><span class="sxs-lookup"><span data-stu-id="617ad-185">Use the NodeJS client libraries available through NPM: https://www.npmjs.com/package/@microsoft/customerinsights</span></span>

### <a name="python-package"></a><span data-ttu-id="617ad-186">Python paketea</span><span class="sxs-lookup"><span data-stu-id="617ad-186">Python package</span></span>

<span data-ttu-id="617ad-187">Erabili PyPi bidez eskuragarri dauden Python bezero liburutegiak: https://pypi.org/project/customerinsights/</span><span class="sxs-lookup"><span data-stu-id="617ad-187">Use the Python client libraries available through PyPi: https://pypi.org/project/customerinsights/</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
