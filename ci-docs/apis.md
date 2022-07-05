---
title: Lan egin Customer Insights APIekin
description: Erabili APIak eta ulertu mugak.
ms.date: 05/10/2021
ms.reviewer: wimohabb
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
searchScope:
- ci-system-api-usage
- customerInsights
ms.openlocfilehash: 8e8bd590d3bba9dc7b1644b6ff42b9fc53237ca9
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9054049"
---
# <a name="work-with-customer-insights-apis"></a>Lan egin Customer Insights APIekin

Dynamics 365 Customer Insights APIak eskaintzen ditu zure datuetan oinarritutako zure aplikazioak eraikitzeko Customer Insights-en.

> [!IMPORTANT]
> API horien xehetasunak hemen daude zerrendatuta: [Customer Insights APIen erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights). Eragiketei, parametroei eta erantzunen inguruko informazio osagarria biltzen dute.

Artikulu honek deskribatzen du nola atzitu Customer Insights APIetara, nola sortu Azure App erregistroa eta nola hasi bezeroen liburutegiekin.

## <a name="get-started-trying-the-customer-insights-apis"></a>Hasi Customer Insights APIak probatzen

1. [Hasi saioa](https://home.ci.ai.dynamics.com) Customer Insights-en. Harpidetzarik ez baduzu oraindik, [erregistratu Customer Insights-en probako bertsiorako](https://aka.ms/tryci).

1. Customer Insights ingurunean APIak gaitzeko, joan hona **Admin** > **Segurtasuna**. Administratzaile baimenak beharko dituzu horretarako.

1. Joan **APIak** fitxara eta hautatu **Gaitu** botoia.    
 
   APIak gaitzeak API eskaeretan erabiltzen den harpidetza gako nagusia eta bigarren mailakoa sortzen ditu zure instantziarako. Teklak birsor ditzakezu hautatuta **Birsortu primarioa** edo **Bigarren mailako birsortzea** on **Admin** > **Segurtasuna** > **APIak**.

<!--  :::image type="content" source="media/enable-apis.gif" alt-text="Enable Customer Insights APIs."::: -->

1. Hautatu **Esploratu gure APIak** hurrengora [probatu APIak](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances).

1. Aukeratu API eragiketa bat eta hautatu **Probatu**.

1. Alboko panelean, ezarri balioa **Baimena** menuan goitibeherako menua **inplizitua**. `Authorization` goiburua eramaile token batekin gehitzen da. Zure harpidetza gakoa automatikoki beteko da.
  
1. Aukeran, gehitu beharrezko kontsulta parametro guztiak.

1. Joan alboko panelaren behealdera eta hautatu **Bidali**.

HTTP erantzuna laster agertuko da behean.

<!--   :::image type="content" source="media/try-apis.gif" alt-text="How to test the APIs."::: -->

## <a name="create-a-new-app-registration-in-the-azure-portal"></a>Sortu aplikazioen erregistro berria Azure atarian

Urrats hauei esker, Azure aplikazio batean Customer Insights APIak erabiltzen hasi ahal izango dituzu eskuordetutako baimenak erabiliz. Ziurtatu [Hasteko atala](#get-started-trying-the-customer-insights-apis) lehenengoa.

1. Saioa hasi [Azure atarian](https://portal.azure.com) Customer Insights datuetara sar daitekeen kontuarekin.

1. Ezkerrean, hautatu **Aplikazioen erregistroak**.

1. Aukeratu **Erregistro berria**, eman aplikazioaren izena eta aukeratu kontu mota.

   Aukeran, gehitu birbideratzeko URLa. http://localhost nahikoa da zure ordenagailu lokalean aplikazio bat garatzeko.

1. Aplikazio berriaren erregistroan, joan hona: **API baimenak**.

1. Hautatu **Gehitu baimena** eta hautatu **Dynamics 365 AI Customer Insights-erako** alboko panelean.

1. **Baimen mota**, hautatu **Baimen delegatuak** eta, ondoren, hautatu **user_impersonation** baimena.

1. Hautatu **Gehitu baimenak**. Erabiltzailearen saioa hasi gabe APIan sartu behar baduzu, berrikusi [Zerbitzaritik zerbitzarirako aplikazioen baimenak](#server-to-server-application-permissions) atala.

1. Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.

Aplikazioaren / Bezeroaren IDa erabil dezakezu Microsoft Authentication Library (MSAL) zerbitzuarekin aplikazioa erregistratzeko, eskaerarekin batera APIra bidaltzeko titularraren tokena eskuratzeko.

<!-- :::image type="content" source="media/grant-admin-consent.gif" alt-text="How to grant admin consent."::: -->

MSAL-i buruzko informazio gehiago lortzeko, ikusi [Microsoft Authentication Library (MSAL) zerbitzuaren ikuspegi orokorra](/azure/active-directory/develop/msal-overview).

Azure aplikazioen erregistroari buruzko informazio gehiago lortzeko, ikusi [Erregistratu eskaera bat](/graph/auth-register-app-v2).

APIak gure bezeroen liburutegietan erabiltzeari buruzko informazioa lortzeko, ikusi [Customer Insights bezero liburutegiak](#customer-insights-client-libraries).

### <a name="server-to-server-application-permissions"></a>Zerbitzaritik zerbitzarirako aplikazioen baimenak

[Aplikazioak erregistratzeko atalak](#create-a-new-app-registration-in-the-azure-portal) erabiltzaileak autentikatzeko saioa hastea eskatzen duen aplikazio bat nola erregistratu azaltzen du. Ikasi erabiltzailearen interakziorik behar ez duen eta zerbitzari batean exekutatu daitekeen aplikazioen erregistroa nola sortu.

1. Azure atariko aplikazioaren erregistroan, joan hona: **API baimenak**.

1. Hautatu **Gehitu baimena**. 

1. Aukeratu **Nire erakundeak erabiltzen dituen APIak** fitxa eta aukeratu **Customer Insights-erako Dynamics 365 AI** zerrendatik. 

1. **Baimen mota**, hautatu **Aplikazioen baimenak** eta, ondoren, hautatu **CustomerInsights.Api.All** baimena.

1. Hautatu **Gehitu baimenak**.

1. Aplikazio berriaren erregistratzeko, itzuli hona: **API baimenak**.

1. Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.

 <!--  :::image type="content" source="media/grant-admin-consent.gif" alt-text="How to grant admin consent."::: -->

1. Amaitzeko, aplikazioaren erregistroaren izena gehitu behar dugu erabiltzaile gisa Customer Insights-en.  
   
   Ireki Customer Insights, joan hona **Admin** > **Segurtasuna** eta hautatu **Gehitu erabiltzailea**.

1. Bilatu zure aplikazioaren erregistroaren izena, hautatu bilaketaren emaitzetan eta hautatu **Gorde**.

## <a name="sample-queries"></a>Lagin-kontsultak

OData lagin-kontsulten zerrenda labur bat osatu dugu APIekin lan egiteko: [OData kontsultaren adibideak](odata-examples.md).

## <a name="customer-insights-client-libraries"></a>Customer Insights bezero liburutegiak

Atal honek Customer Insights APIen eskuragarri dauden bezero liburutegiak erabiltzen hasteko laguntza ematen dizu. Liburutegiaren iturburu kodea eta adibideen aplikazio guztiak hemen aurki ditzakezu [Customer Insights GitHub orria](https://github.com/microsoft/Dynamics365-CustomerInsights-Client-Libraries). 

### <a name="c-nuget"></a>C# NuGet

Ikasi NuGet.org orrialdetik C# bezero liburutegiak erabiltzen hasten. NuGet paketeari buruzko informazio gehiagorako, ikusi [Microsoft.Dynamics.CustomerInsights.Api](https://www.nuget.org/packages/Microsoft.Dynamics.CustomerInsights.Api/). Gaur egun, pakete hau netstandard2.0 eta netcoreapp2.0 markoetara bideratuta dago.

#### <a name="add-the-c-client-library-to-a-c-project"></a>Gehitu C # bezero liburutegia C # proiektu batera

1. Visual Studio-n, ireki proiektuaren **NuGet Pakete kudeatzailea**.

1. Bilatu **Microsoft.Dynamics.CustomerInsights.Api**.

1. Aukeratu **Instalatu** paketea proiektuari gehitzeko.
 
   Bestela, exekutatu komando hau **NuGet Pakete kudeatzailearen kontsolan**: `Install-Package -Id Microsoft.Dynamics.CustomerInsights.Api -Source nuget.org -ProjectName <project name> [-Version <version>]`

 <!--  :::image type="content" source="media/visual-studio-nuget-package.gif" alt-text="Add NuGet package to Visual Studio project."::: -->

#### <a name="use-the-c-client-library"></a>Erabili C # bezero liburutegia

1. Erabili [Microsoft autentifikazio liburutegia (MSAL)](/azure/active-directory/develop/msal-overview) `AccessToken` bat lortzeko lehendik duzun [Azure aplikazioaren erregistroa](#create-a-new-app-registration-in-the-azure-portal) erabiliz.

1. Token bat ongi autentifikatu eta eskuratu ondoren, eraiki berria edo erabili lehendik dagoen bat`HttpClient` nirekin **DefaultRequestHeaders "Baimena"** ezarri **Eramailearen "sarbide-tokena"** eta **Ocp-Apim-Harpidetza-gakoa** ezarri [**harpidetza-gakoa** zure Customer Insights ingurunetik](#get-started-trying-the-customer-insights-apis).   
 
   Berrezarri **Baimena** goiburua egokia denean. Adibidez, token-a iraungi denean.

1. Pasatu `HttpClient` `CustomerInsights` bezeroaren sorkuntzara.

<!--   :::image type="content" source="media/httpclient-sample.png" alt-text="Sample of httpclient."::: -->

1. Egin deiak bezeroekin "luzapen metodoetara", adibidez, `GetAllInstancesAsync`. Azpiko `Microsoft.Rest.HttpOperationResponse`-rako sarbidea hobetsi bada, erabili "http mezuen metodoak" erabili, adibidez, `GetAllInstancesWithHttpMessagesAsync`.

1. Erantzuna `object` motakoa izango da ziurrenik, metodoak hainbat mota itzul ditzakeelako (adibidez, `IList<InstanceInfo>` eta `ApiErrorResult`). Itzultze-mota egiaztatzeko, gailuan zehaztutako erantzun-motetako objektuak erabiltzen dituzu [API xehetasunen orria](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) eragiketa horretarako.    
   
   Eskaerari buruzko informazio gehiago behar izanez gero, erabili **http mezuen metodoak** erantzun gordineko objektuan sartzeko.

### <a name="nodejs-package"></a>NodeJS paketea

Erabili NPM bidez eskuragarri dauden NodeJS bezero liburutegiak: https://www.npmjs.com/package/@microsoft/customerinsights

### <a name="python-package"></a>Python paketea

Erabili PyPi bidez eskuragarri dauden Python bezero liburutegiak: https://pypi.org/project/customerinsights/

[!INCLUDE [footer-include](includes/footer-banner.md)]
