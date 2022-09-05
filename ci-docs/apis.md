---
title: Lan egin Customer Insights APIekin
description: Erabili APIak eta ulertu mugak.
ms.date: 08/31/2022
ms.reviewer: wimohabb
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: wimohabb
manager: shellyha
searchScope:
- ci-system-api-usage
- customerInsights
ms.openlocfilehash: f499bff4a6ac07a88ff0f773b9cee77dc74989e8
ms.sourcegitcommit: 624b27bb65a0de1970dc1ac436643b493f0a31cf
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387325"
---
# <a name="work-with-customer-insights-apis"></a>Lan egin Customer Insights APIekin

Dynamics 365 Customer Insights APIak eskaintzen ditu zure datuetan oinarritutako zure aplikazioak eraikitzeko Customer Insights-en.

> [!IMPORTANT]
> API horien xehetasunak hemen daude zerrendatuta: [Customer Insights APIen erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights). Eragiketei, parametroei eta erantzunen inguruko informazio osagarria biltzen dute.

Probatu Customer Insights APIak, sortu Azure App Registration bat eta hasi bezeroen liburutegiekin.

## <a name="get-started-trying-the-customer-insights-apis"></a>Hasi Customer Insights APIak probatzen

Gaitu Customer Insights APIak eta probatu. Customer Insights administratzaile batek API sarbidea gaitu behar du Customer Insights-erako. Sarbidea gaituta dagoenean, edozein erabiltzailek APIa erabil dezake harpidetza-gakoarekin.

1. [Hasi saioa](https://home.ci.ai.dynamics.com) Customer Insights-en. Harpidetzarik ez baduzu oraindik, [erregistratu Customer Insights-en probako bertsiorako](https://aka.ms/tryci).

1. Joan **Admin** > **Segurtasuna** eta hautatu **APIak** fitxa.

1. Ingurunerako API sarbidea konfiguratu ez bada, hautatu **Gaitu**.

   APIak gaitzeak API eskaeretan erabiltzen den harpidetza gako nagusia eta bigarren mailakoa sortzen ditu zure instantziarako. Teklak birsortzeko, hautatu **Birsortu primarioa** edo **Bigarren mailako birsortzea** gainean **APIak** fitxa.

1. Hautatu [**Arakatu gure APIak**](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances) APIak probatzeko.

1. Bilatu eta hautatu API eragiketa bat eta hautatu **Saiatu** .

   :::image type="content" source="media/try-api.png" alt-text="APIak nola probatu.":::

1. Alboko panelean, ezarri balioa **Baimena** menuan goitibeherako menua **inplizitua**. `Authorization` goiburua eramaile token batekin gehitzen da. Zure harpidetza-gakoa automatikoki betetzen da.
  
1. Aukeran, gehitu beharrezko kontsulta parametro guztiak.

1. Joan alboko panelaren behealdera eta hautatu **Bidali**.

   HTTP erantzuna panelaren behealdean bistaratzen da.

## <a name="create-a-new-app-registration-in-the-azure-portal"></a>Sortu aplikazioen erregistro berria Azure atarian

Sortu berri bat [aplikazioaren erregistroa](/graph/auth-register-app-v2) Customer Insights APIak Azure aplikazio batean erabiltzeko delegatutako baimenak erabiliz.

1. Osatu [Hasteko atala](#get-started-trying-the-customer-insights-apis) .

1. Saioa hasi [Azure atarian](https://portal.azure.com) Customer Insights datuetara sar daitekeen kontuarekin.

1. Bilatu eta gero hautatu **Aplikazioen erregistroak** .

1. Aukeratu **Erregistro berria**, eman aplikazioaren izena eta aukeratu kontu mota.

   Aukeran, gehitu birbideratzeko URLa. http://localhost nahikoa da zure ordenagailu lokalean aplikazio bat garatzeko.

1. Hautatu **Erregistratu**.

1. Aplikazio berriaren erregistroan, joan hona: **API baimenak**.

1. Hautatu **Gehitu baimena** eta hautatu **Dynamics 365 AI Customer Insights-erako** alboko panelean.

1. **Baimen mota**, hautatu **Baimen delegatuak** eta, ondoren, hautatu **user_impersonation** baimena.

1. Hautatu **Gehitu baimenak**.

1. Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.

1. Erabiltzaileak saioa hasi gabe APIra sartzeko, joan hona [Zerbitzaritik zerbitzarirako aplikazioen baimenak](#server-to-server-application-permissions) .

Aplikazioa/Bezeroaren IDa erabil dezakezu aplikazio hau erregistratzeko [Microsoft autentifikazio liburutegia (MSAL)](/azure/active-directory/develop/msal-overview) zure eskaerarekin batera APIra bidaltzeko eramaile-token bat lortzeko.

<!-- :::image type="content" source="media/grant-admin-consent.gif" alt-text="How to grant admin consent."::: -->

APIak gure bezeroen liburutegietan erabiltzeari buruzko informazioa lortzeko, ikusi [Customer Insights bezero liburutegiak](#customer-insights-client-libraries).

### <a name="server-to-server-application-permissions"></a>Zerbitzaritik zerbitzarirako aplikazioen baimenak

Sortu erabiltzailearen interakziorik behar ez duen eta zerbitzari batean exekutatu daitekeen aplikazioaren erregistroa.

1. Azure atariko aplikazioaren erregistroan, joan hona: **API baimenak**.

1. Hautatu **Gehitu baimena**.

1. Aukeratu **Nire erakundeak erabiltzen dituen APIak** fitxa eta aukeratu **Customer Insights-erako Dynamics 365 AI** zerrendatik.

1. **Baimen mota**, hautatu **Aplikazioen baimenak** eta, ondoren, hautatu **CustomerInsights.Api.All** baimena.

1. Hautatu **Gehitu baimenak**.

1. Aplikazio berriaren erregistratzeko, itzuli hona: **API baimenak**.

1. Aukeratu **Eman administratzailearen baimena honetarako:...** aplikazioaren erregistroa osatzeko.

   <!--  :::image type="content" source="media/grant-admin-consent.gif" alt-text="How to grant admin consent."::: -->

1. Gehitu aplikazioaren erregistroaren izena erabiltzaile gisa Customer Insights-en.

   1. Ireki Customer Insights, joan hona **Admin** > **Segurtasuna** eta hautatu **Gehitu erabiltzaileak** .

   1. Bilatu zure aplikazioaren erregistroaren izena, hautatu bilaketaren emaitzetan eta hautatu **Gorde**.

## <a name="sample-queries"></a>Lagin-kontsultak

APIekin lan egiteko OData lagin-kontsulten zerrenda laburra ikusteko, ikus [OData kontsultaren adibideak](odata-examples.md) .

## <a name="customer-insights-client-libraries"></a>Customer Insights bezero liburutegiak

Hasi Customer Insights APIetarako eskuragarri dauden bezero liburutegiak erabiltzen. Liburutegiaren iturburu kodea eta adibideen aplikazio guztiak hemen aurki ditzakezu [Customer Insights GitHub orria](https://github.com/microsoft/Dynamics365-CustomerInsights-Client-Libraries).

### <a name="c-nuget"></a>C# NuGet

Erabili C# bezero liburutegiak NuGet .org. Gaur egun, paketeak netstandard2.0 eta netcoreapp2.0 esparruak ditu helburu. Informazio gehiagorako NuGet paketea, ikusi [Microsoft.Dynamics.CustomerInsights.Api](https://www.nuget.org/packages/Microsoft.Dynamics.CustomerInsights.Api/) .

#### <a name="add-the-c-client-library-to-a-c-project"></a>Gehitu C # bezero liburutegia C # proiektu batera

1. Visual Studio-n, ireki proiektuaren **NuGet Pakete kudeatzailea**.

1. Bilatu **Microsoft.Dynamics.CustomerInsights.Api**.

1. Aukeratu **Instalatu** paketea proiektuari gehitzeko.

   Bestela, exekutatu komando hau **NuGet Pakete kudeatzailearen kontsolan**: `Install-Package -Id Microsoft.Dynamics.CustomerInsights.Api -Source nuget.org -ProjectName <project name> [-Version <version>]`

   <!--  :::image type="content" source="media/visual-studio-nuget-package.gif" alt-text="Add NuGet package to Visual Studio project."::: -->

#### <a name="use-the-c-client-library"></a>Erabili C # bezero liburutegia

1. Erabili [Microsoft autentifikazio liburutegia (MSAL)](/azure/active-directory/develop/msal-overview) `AccessToken` bat lortzeko lehendik duzun [Azure aplikazioaren erregistroa](#create-a-new-app-registration-in-the-azure-portal) erabiliz.

1. Token bat ongi autentifikatu eta eskuratu ondoren, eraiki berria edo erabili lehendik dagoen bat`HttpClient` nirekin **DefaultRequestHeaders "Baimena"** ezarri **Eramailearen "sarbide-tokena"** eta **Ocp-Apim-Harpidetza-gakoa** ezarri [**harpidetza-gakoa** zure Customer Insights ingurunetik](#get-started-trying-the-customer-insights-apis) .   

   Berrezarri **Baimena** goiburua egokia denean. Adibidez, token-a iraungi denean.

1. Pasatu `HttpClient` `CustomerInsights` bezeroaren sorkuntzara.

   <!--   :::image type="content" source="media/httpclient-sample.png" alt-text="Sample of httpclient."::: -->

1. Egin deiak bezeroekin "luzapen metodoetara", adibidez, `GetAllInstancesAsync`. Azpikorako sarbidea bada`Microsoft.Rest.HttpOperationResponse` hobe da, erabili "http mezuen metodoak", adibidez,`GetAllInstancesWithHttpMessagesAsync` .

1. Erantzuna litekeena da`object` idatzi metodoak hainbat mota itzul ditzakeelako (adibidez,`IList<InstanceInfo>` eta`ApiErrorResult` ). Itzulpen-mota egiaztatzeko, erabili gailuan zehaztutako erantzun-motetako objektuak [API xehetasunen orria](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights) eragiketa horretarako.

   Eskaerari buruzko informazio gehiago behar izanez gero, erabili **http mezuen metodoak** erantzun gordineko objektuan sartzeko.

### <a name="nodejs-package"></a>NodeJS paketea

Erabili NPM bidez eskuragarri dauden NodeJS bezero liburutegiak: https://www.npmjs.com/package/@microsoft/customerinsights

### <a name="python-package"></a>Python paketea

Erabili PyPi bidez eskuragarri dauden Python bezero liburutegiak: https://pypi.org/project/customerinsights/

[!INCLUDE [footer-include](includes/footer-banner.md)]
