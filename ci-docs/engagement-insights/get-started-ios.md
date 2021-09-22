---
title: Hasi iOS SDK erabiltzen
description: Ikusi iOS SDK pertsonalizatzen eta exekutatzen
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 06/23/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: de8291fc429ae6433301a47bfdf9a3271b1b77294fd58448c7aa6bd0783edc97
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036858"
---
# <a name="get-started-with-the-ios-sdk"></a>Hasi iOS SDK erabiltzen

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Tutorial honek aplikazioa parte-hartzearen xehetasunen Dynamics 365 Customer Insights SDK-rekin hornitzeko iOS aplikazioan lagunduko dizu. Zure atarian gertaerak ikusten bost minutu edo lehenago hasiko zara.

## <a name="configuration-options"></a>Konfigurazio-aukerak

Ondorengo konfigurazio aukerak SDKra pasa daitezke emandakoaren bidez `EIConfig.plist` fitxategia:

- **ingestionKey**: zure proiektuari gertaerak bidaltzeko erabilitako iradokizun gakoa.
- **autocollectAction**: Balio boolearra ekintza gertaeraren instrumentazio automatikoa gaitzeko edo desgaitzeko.
- **autocollectView**: Balio boolearra ikuspegia gertaeraren instrumentazio automatikoa gaitzeko edo desgaitzeko.
- **endpointUrl**: Gertaerak bideratuko diren amaierako URLa.

## <a name="prerequisites"></a>Aurrebaldintzak

- Xcode bertisoaren 9+
- iOS bertsioaren 8.2+
- Irensteko giltza bat (ikusi eskuratzeko beheko argibideak)

## <a name="integrate-the-sdk-into-your-application"></a>Integratu SDK zure aplikazioan

Hasi prozesua lan egiteko lan eremua hautatuz, iOS plataforma mugikorra hautatuz eta SDK deskargatuz.

- Erabili ezkerreko nabigazio paneleko laneko espazio aldatzailea zure lan eremua hautatzeko.

- Ez baduzu lehendik dagoen lan-eremurik, hautatu **Laneko area berria** eta jarraitu pausoak sortzeko [laneko area berria](create-workspace.md).

## <a name="configure-the-sdk"></a>Konfiguratu SDK

SDK deskargatu ondoren, Xcode-en lan egin dezakezu gertaerak gaitu eta definitzeko.

1. Laneko area sortu ondoren, joan hona: **Administratzailea** > **Lan eremua** eta, ondoren, hautatu **Instalazio gida**.

1. Deskargatu [parte-hartzearen xehetasunen iOS SDK](https://download.pi.dynamics.com/sdk/EI-SDKs/ei-ios-sdk.zip), eta jarri `EIObjC.xcframework` fitxategia `Frameworks` karpetan.

1. Bada `Frameworks` karpeta ez da existitzen, sortu bat proiektuaren karpetan.

## <a name="enable-auto-instrumentation"></a>Gaitu instrumentazio automatikoa
 
Tresneria automatikoa erraz kodetu gabe gaitu dezakezu. Proiektua exekutatzen denean, automatikoki jarraipena egingo du `view` eta `action` gertaerak konfiguratutako iradokizun gakoa erabiliz. 

1. Eguneratu eta eman emandakoak `EIConfig.plist` fitxategia proiektuaren direktorioko karpetan eremu hauetarako:
    - ingestionKey = `"Your-Ingestion-Key"`
    - autocollectView = YES
    - autocollectAction = YES

2. Ondoren, gehitu `EIConfig.plist` artxibatu zure proiektuan Xcode-n. 



Instrumentazio automatikoa desgaitzeko, eguneratu honako eremu hauek gehitutako `EIConfig.plist` fitxategia proiektuaren direktorioko karpetan eremu hauetarako. 

```objectivec
'autocollectView' = NO (to disable)
'autocollectAction' = NO (to disable)
```


## <a name="implement-custom-events"></a>Ezarri gertaera pertsonalizatuak

1. Ireki proiektua Xcode-n eta nabigatu **Orokorrak** ezarpenetara. 
1. Gehitu `EIObjC.xcframework` proiektuari "Markoak, liburutegiak eta txertatutako edukia" atalean.

1. Inportatu markoaren goiburu-fitxategia AppDelegate.m elementuan, kode zati honekin:

    ```objectivec
    #import <EIObjC/EIObjC.h>
    ```

1. Hasieratu application:didFinishLaunchingWithOptions elementuko SDKaren parte-hartzearen xehetasunak.
1. Kopiatu XML kode zati helbidetik **Instalazio gida**.

    ```objectivec
    NSError *error = [NSError new];
    id<EIIAnalytics> analytics = [EIAnalyticsProvider analyticsForIngestionKey:nil error:&error];
    ```

1. Egin gertaera baten jarraipena:

    ```objectivec
    EIEvent *event = [EIEvent new];
    event.name = @"video.log";
    [event setLongValue:320 forKey:@"duration"];
    [event setBoolValue:YES forKey:@"ad_shown"];
    [analytics trackEvent:event];
    ```

## <a name="set-user-details-for-your-event"></a>Ezarri zure gertaeraren erabiltzaile xehetasunak

SDK-k gertaera guztiekin bidal daitekeen erabiltzailearen informazioa zehazteko aukera ematen du. Erabiltzailearen informazioa zehaztu dezakezu `setUser:(nonnull EIUser *)user` APIa SDKn.

Erabiltzailearen datuak zehaztuz `Analytics` mailak telemetria guztiek informazio hori izango dutela esan nahi du. Hala ere, gertaera mailan zehaztuz gero `setUser:(nonnull EIUser *)user` APIa EIEvent objektuan, gertaera zehatz horrek bakarrik edukiko du informazioa.

`EIUser` datu klaseak NSString propietate hauek ditu:

- **localId**: Erabiltzailearen ID lokala.
- **autentifikazioa**: Autentifikatutako erabiltzaile IDa.
- **authType**: Autentifikatutako erabiltzaile IDa lortzeko erabiltzen den autentifikazio mota.
- **izena**: Erabiltzailearen izena.
- **posta elektronikoa**: erabiltzailearen helbide elektronikoa.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
