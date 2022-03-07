---
title: Hasi iOS SDK erabiltzen
description: Ikusi iOS SDK pertsonalizatzen eta exekutatzen
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 09/15/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: f05929435eeee9cf3f891ab18842c5861e39d5ba
ms.sourcegitcommit: fecdee73e26816c42d39d160d4d5cfb6c8a91596
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/15/2021
ms.locfileid: "7494215"
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

- Laneko area sortu ondoren, joan hona: **Administratzailea** > **Lan eremua** eta, ondoren, hautatu **Instalazio gida**.

## <a name="configure-the-sdk"></a>Konfiguratu SDK

SDK deskargatu ondoren, Xcode-en lan egin dezakezu gertaerak gaitu eta definitzeko. Bi modu daude horretarako:

### <a name="option-1-using-cocoapods-recommended"></a>1. aukera: CocoaPods erabiltzea (gomendatua)
CocoaPods Swift and Objective-C Cocoa proiektuen mendekotasun-kudeatzailea da. Horri esker, iOS-erako parte-hartzearen xehetasunen SDK errazago integratzen da. CocoaPods-ek parte-hartzearen xehetasunen SDKren azken bertsiora bertsio-berritzeko aukera ematen du. Hona hemen nora erabili CocoaPods parte-hartzearen xehetasunen SDK integratzeko Xcode proiektuan. 

1. Instalatu CocoaPods. 

1. Sortu Podfile izeneko fitxategi bat proiektuaren erroko direktorioan eta gehitu honako adierazpen hauek. Ordeztu YOUR_TARGET_PROJECT_NAME Xcode proiektuaren izenarekin. 
```objectivec
platform :ios, '9.0'  

 target '${YOUR_TARGET_PROJECT_NAME}' do 

     use_frameworks!   

     pod 'EIObjC.framework.debug' 

     pod 'EIObjC.framework.release' 

 end 
```
Goiko pod konfigurazioak SDKren arazteko eta kaleratutako bertsioak dituzte. Aukeratu proiekturako egokiena dena.

1. Pod-a instalatzeko, exekutatu komando hau: `pod install --repo-update `

### <a name="option-2-using-download-link"></a>2. aukera: deskarga-esteka erabiltzea

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
