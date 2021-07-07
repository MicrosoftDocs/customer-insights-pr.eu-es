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
# <a name="work-with-customer-insights-apis"></a>Lan egin Customer Insights APIekin

Dynamics 365 Customer Insights APIak eskaintzen ditu zure datuetan oinarritutako zure aplikazioak eraikitzeko Customer Insights-en.

> [!IMPORTANT]
> API horien xehetasunak hemen daude zerrendatuta: [Customer Insights APIen erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights). Eragiketei, parametroei eta erantzunen inguruko informazio osagarria biltzen dute.

Artikulu honetan Customer Insights APIak nola sartu, Azure aplikazioen erregistroa sortu eta eskuragarri dauden bezero liburutegiekin nola hasi deskribatzen da.

## <a name="get-started-trying-the-customer-insights-apis"></a>Hasi Customer Insights APIak probatzen

1. [Hasi saioa](https://home.ci.ai.dynamics.com) Customer Insights-en. Harpidetzarik ez baduzu oraindik, [erregistratu Customer Insights-en probako bertsiorako](https://aka.ms/tryci).

1. Customer Insights ingurunean APIak gaitzeko, joan hona: **Administratzailea** > **Baimenak**. Administratzaile baimenak beharko dituzu horretarako.

1. Joan **APIak** fitxara eta hautatu **Gaitu** botoia.    
 
   APIak gaitzeak API eskaeretan erabiltzen den harpidetza gako nagusia eta bigarren mailakoa sortzen ditu zure instantziarako. Gakoak birsortu ditzakezu **Birsortu nagusia** edo **Birsortu bigarren mailakoa** hautatuz hemen: **Administratzailea** > **Baimenak** > **APIak**.

   :::image type="content" source="media/enable-apis.gif" alt-text="Gaitu Customer Insights APIak":::

1. Hautatu **Esploratu gure APIak** hurrengora [probatu APIak](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances).

1. Aukeratu API eragiketa bat eta hautatu **Probatu**.

1. Alboko panelean, ezarri balioa **Baimena** menuan goitibeherako menua **inplizitua**. `Authorization` goiburua eramaile token batekin gehitzen da. Zure harpidetza gakoa automatikoki beteko da.
  
1. Aukeran, gehitu beharrezko kontsulta parametro guztiak.

1. Joan alboko panelaren behealdera eta hautatu **Bidali**.

HTTP erantzuna laster agertuko da behean.

   :::image type="content" source="media/try-apis.gif" alt-text="APIak nola probatu.":::

## <a name="create-a-new-app-registration-in-the-azure-portal"></a>Sortu aplikazioen erregistro berria Azure atarian

Urrats hauei esker, Azure aplikazio batean Customer Insights APIak erabiltzen hasi ahal izango dituzu eskuordetutako baimenak erabiliz. Ziurtatu [Hasteko atala](#get-started-trying-the-customer-insights-apis) lehenengoa.

1. Saioa hasi [Azure atarian](https://portal.azure.com) Customer Insights datuetara sar daitekeen kontuarekin.

1. Ezkerrean, hautatu **Aplikazioen erregistroak**.

1. Aukeratu **Erregistro berria**, eman aplikazioaren izena eta aukeratu kontu mota.
 
   Aukeran, gehitu birbideratzeko URLa. http://localhost nahikoa da zure ordenagailu lokalean aplikazio bat garatzeko.

1. Aplikazio berriaren erregistroan, joan hona: **API baimenak**.

   :::image type="content" source="media/app-registration-1.gif" alt-text="Nola ezarri API baimenak aplikazioaren erregistroan.":::

1. Aukeratu **Gehitu baimena** eta hautatu **Customer Insights** alboko panelean.

1. **Baimen mota**, hautatu **Baimen delegatuak** eta, ondoren, hautatu **user_impersonation** baimena.

1. Hautatu **Gehitu baimenak**. Erabiltzailearen saioa hasi gabe APIan sartu behar baduzu, berrikusi [Zerbitzaritik zerbitzarirako aplikazioen baimenak](#server-to-server-application-permissions) atala.

1. Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.

Aplikazioaren / Bezeroaren IDa erabil dezakezu Microsoft Authentication Library (MSAL) zerbitzuarekin aplikazioa erregistratzeko, eskaerarekin batera APIra bidaltzeko titularraren tokena eskuratzeko.

:::image type="content" source="media/grant-admin-consent.gif" alt-text="Administratzailearen baimena nola eman.":::

MSAL-i buruzko informazio gehiago lortzeko, ikusi [Microsoft Authentication Library (MSAL) zerbitzuaren ikuspegi orokorra](/azure/active-directory/develop/msal-overview).

Azure aplikazioen erregistroari buruzko informazio gehiago lortzeko, ikusi [Erregistratu eskaera bat](/azure/active-directory/develop/quickstart-register-app.md#register-an-application).

APIak gure bezeroen liburutegietan erabiltzeari buruzko informazioa lortzeko, ikusi [Customer Insights bezero liburutegiak](#customer-insights-client-libraries).

### <a name="server-to-server-application-permissions"></a>Zerbitzaritik zerbitzarirako aplikazioen baimenak

[Aplikazioak erregistratzeko atalak](#create-a-new-app-registration-in-the-azure-portal) erabiltzaileak autentikatzeko saioa hastea eskatzen duen aplikazio bat nola erregistratu azaltzen du. Ikasi erabiltzaileen elkarrekintzarik behar ez duen eta zerbitzarian exekutatu daitekeen aplikazioen erregistroa nola sortu.

1. Azure atariko aplikazioaren erregistroan, joan hona: **API baimenak**.

1. Hautatu **Gehitu baimena**. 

1. Aukeratu **Nire erakundeak erabiltzen dituen APIak** fitxa eta aukeratu **Customer Insights-erako Dynamics 365 AI** zerrendatik. 

1. **Baimen mota**, hautatu **Aplikazioen baimenak** eta, ondoren, hautatu **CustomerInsights.Api.All** baimena.

1. Hautatu **Gehitu baimenak**.

1. Aplikazio berriaren erregistratzeko, itzuli hona: **API baimenak**.

1. Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.

   :::image type="content" source="media/grant-admin-consent.gif" alt-text="Administratzailearen baimena nola eman.":::

1. Amaitzeko, aplikazioaren erregistroaren izena gehitu behar dugu erabiltzaile gisa Customer Insights-en.  
   
   Ireki Customer Insights, joan hona: **Administratzailea** > **Baimenak** eta hautatu **Gehitu erabiltzailea**.

1. Bilatu zure aplikazioaren erregistroaren izena, hautatu bilaketaren emaitzetan eta hautatu **Gorde**.

## <a name="customer-insights-client-libraries"></a>Customer Insights bezero liburutegiak

Atal honek Customer Insights APIen eskuragarri dauden bezero liburutegiak erabiltzen hasteko laguntza ematen dizu. Liburutegiaren iturburu kodea eta adibideen aplikazio guztiak hemen aurki ditzakezu [Customer Insights GitHub orria](https://github.com/microsoft/Dynamics365-CustomerInsights-Client-Libraries). 

### <a name="c-nuget"></a>C# NuGet

Ikasi NuGet.org orrialdetik C# bezero liburutegiak erabiltzen hasten. NuGet paketeari buruzko informazio gehiagorako, ikusi [Microsoft.Dynamics.CustomerInsights.Api](https://www.nuget.org/packages/Microsoft.Dynamics.CustomerInsights.Api/). Gaur egun, pakete hau netstandard2.0 eta netcoreapp2.0 markoetara bideratuta dago.

#### <a name="add-the-c-client-library-to-a-c-project"></a>Gehitu C # bezero liburutegia C # proiektu batera

1. Visual Studio-n, ireki proiektuaren **NuGet Pakete kudeatzailea**.

1. Bilatu **Microsoft.Dynamics.CustomerInsights.Api**.

1. Aukeratu **Instalatu** paketea proiektuari gehitzeko.
 
   Bestela, exekutatu komando hau **NuGet Pakete kudeatzailearen kontsolan**: `Install-Package -Id Microsoft.Dynamics.CustomerInsights.Api -Source nuget.org -ProjectName <project name> [-Version <version>]`

   :::image type="content" source="media/visual-studio-nuget-package.gif" alt-text="Gehitu NuGet paketea Visual Studio proiektuan":::

#### <a name="use-the-c-client-library"></a>Erabili C # bezero liburutegia

1. Erabili [Microsoft autentifikazio liburutegia (MSAL)](/azure/active-directory/develop/msal-overview) `AccessToken` bat lortzeko lehendik duzun [Azure aplikazioaren erregistroa](#create-a-new-app-registration-in-the-azure-portal) erabiliz.

1. Token bat behar bezala autentifikatu eta eskuratu ondoren, eraiki berria edo erabili lehendik dagoen `HttpClient` **DefaultRequestHeaders "Baimena"** gehigarria **Titularra <access token>** gisa eta **Ocp-Apim-Subscription-Key** [Customer Insights inguruneko **harpidetza gakoa**](#get-started-trying-the-customer-insights-apis) gisa ezarrita.   
 
   Berrezarri **Baimena** goiburua egokia denean. Adibidez, token-a iraungi denean.

1. Pasatu `HttpClient` `CustomerInsights` bezeroaren sorkuntzara.

   :::image type="content" source="media/httpclient-sample.png" alt-text="Httpclient-en lagina":::

1. Egin deiak bezeroekin "luzapen metodoetara", adibidez, `GetAllInstancesAsync`. Azpiko `Microsoft.Rest.HttpOperationResponse`-rako sarbidea hobetsi bada, erabili "http mezuen metodoak" erabili, adibidez, `GetAllInstancesWithHttpMessagesAsync`.

1. Erantzuna `object` motakoa izango da ziurrenik, metodoak hainbat mota itzul ditzakeelako (adibidez, `IList<InstanceInfo>` eta `ApiErrorResult`). Itzulera mota egiaztatzeko, objektuak segurtasunez bihur ditzakezu eragiketaren [APIaren xehetasunen orrian](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) zehaztutako erantzun motara.    
   
   Eskaerari buruzko informazio gehiago behar izanez gero, erabili **http mezuen metodoak** erantzun gordineko objektuan sartzeko.

### <a name="nodejs-package"></a>NodeJS paketea

Erabili NPM bidez eskuragarri dauden NodeJS bezero liburutegiak: https://www.npmjs.com/package/@microsoft/customerinsights

### <a name="python-package"></a>Python paketea

Erabili PyPi bidez eskuragarri dauden Python bezero liburutegiak: https://pypi.org/project/customerinsights/

[!INCLUDE[footer-include](../includes/footer-banner.md)]
