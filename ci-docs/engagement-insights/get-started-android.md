---
title: Hasi Android SDK erabiltzen
description: Ikusi Android SDK pertsonalizatzen eta exekutatzen
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 06/23/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: 77e63929bbcc7ecff34a3839af525b76ec3c7f21173ddc5f8f2d69f11c25c441
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036903"
---
# <a name="get-started-with-the-android-sdk"></a>Hasi Android SDK erabiltzen

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Tutorial honek Android aplikazioa Dynamics 365 Customer Insights parte-hartzearen xehetasunen SDK-rekin hornitzeko prozesuan lagunduko dizu. Zure atarian gertaerak ikusten bost minutu edo lehenago hasiko zara.

## <a name="configuration-options"></a>Konfigurazio-aukerak
Ondorengo konfigurazio aukerak SDKra pasa daitezke:

- **ingestionKey**: zure laneko areari gertaerak bidaltzeko erabilitako iradokizun gakoa.

## <a name="prerequisites"></a>Aurrebaldintzak

- Android Studio

- Gutxienekoa Android API maila: 16 (Jelly Bean)

- Irensteko giltza bat (ikusi jarraian nola eskuratzeko beheko argibideak)

## <a name="step-1-integrate-the-sdk-into-your-application"></a>1. urratsa. Integratu SDK zure aplikazioan
Hasi prozesua lan egiteko lan eremua hautatuz, Android plataforma mugikorra hautatuz eta Android SDK deskargatuz.

- Erabili ezkerreko nabigazio paneleko laneko espazio aldatzailea zure lan eremua hautatzeko.

- Ez baduzu lehendik dagoen lan-eremurik, hautatu **Laneko area berria** eta jarraitu pausoak sortzeko [laneko area berria](create-workspace.md).

## <a name="step-2-configure-the-sdk"></a>2. urratsa. Konfiguratu SDK

1. Laneko area sortu ondoren, joan hona: **Administratzailea** > **Lan eremua** eta, ondoren, hautatu **Instalazio gida**. 

1. Deskargatu [parte-hartzearen xehetasunen Android SDK](https://download.pi.dynamics.com/sdk/EI-SDKs/ei-android-sdk.zip), eta jarri `eiandroidsdk-debug.aar` fitxategia `libs` karpetan.

1. Ireki proiektu mailako `build.gradle` fitxategia eta gehitu kode zati hauek:
    ```gradle
    dependencies {
        implementation(name: 'eiandroidsdk-debug', ext: 'aar')
        api 'com.google.code.gson:gson:2.8.1'
    }

    repositories {
        flatDir {
            dirs 'libs'
        }
    }
    ```

1. Konfiguratu konpromiso estatistiken SDK konfigurazioa zure bidez `AndroidManifest.xml` fitxategia `manifests` karpeta. 
1. Kopiatu XML kode zati helbidetik **Instalazio gida**. `Your-Ingestion-Key` automatikoki bete beharko litzateke.

   > [!NOTE]
   > Ez duzu ordezkatu behar `${applicationId}` atala. Automatikoki bete beharko litzateke.
   

   ```xml
   <application>
   ...
       <provider
           android:authorities="${applicationId}.com.microsoft.engagementinsights.AnalyticsContentProvider"
           android:name="com.microsoft.engagementinsights.AnalyticsContentProvider" />
       <meta-data
           android:name="com.microsoft.engagementinsights.ingestionKey"
           android:value="Your-Ingestion-Key" />
       <meta-data
           android:name="com.microsoft.engagementinsights.autoCapture"
           android:value="true" />
   ...
   </application>
   ```

1. `View` gertaerak ikusteko eginbidearen `autoCapture` gaitzeko edo desgaitzeko, ezarri goiko autoCapture eremua `true` edo `false` gisa.

1. (Aukerakoa) Beste konfigurazio batzuen artean, amaierako puntu biltzailearen URLa ezartzea dago. Iradokizun gako metadatuen azpian gehi daitezke `AndroidManifest.xml`:
    ```xml
        <meta-data
            android:name="com.microsoft.engagementinsights.endpointUrl"
            android:value="https://some-endpoint-url.com" />
    ```

## <a name="step-3-initialize-the-sdk-from-mainactivity"></a>3. urratsa. Hasieratu MainActivity elementuko SDK 

SDK hasieratu ondoren, gertaerekin eta haien propietateekin lan egin dezakezu MainActivity ingurunean.

    
Java:
```java
Analytics analytics = new Analytics();
```

Kotlin:
```kotlin
var analytics = Analytics()
```

### <a name="set-property-for-all-events-optional"></a>Ezarri gertaera guztietako propietatea (aukerakoa)
    
Java:
```java
analytics.setProperty("year", 2021);
```

Kotlin:
```kotlin
analytics.setProperty("year", 2021)
```

Testuinguruaren gertaeren propietateetarako mota hauek onartzen dira:
- String
- Data
- Bikoitza
- Long
- Boolean
- UUID

### <a name="track-an-event"></a>Egin gertaera baten jarraipena

Java:
```java
Event event = new Event("video");
event.setProperty("duration", 320);
event.setProperty("ad_shown", true);
analytics.trackEvent(event);
```

Kotlin:
```kotlin
var event = Event("video")
event.setProperty("duration", 320)
event.setProperty("ad_shown", true)
analytics.trackEvent(event)
```

### <a name="set-user-details-for-your-event-optional"></a>Ezarri zure gertaeraren erabiltzaile xehetasunak (aukerakoa)

SDK-k gertaera guztiekin bidal daitekeen erabiltzailearen informazioa zehazteko aukera ematen du. Erabiltzailearen informazioa zehaztu dezakezu `setUser(user: User)` APIa `Analytics` mailan.

Java:
```java
User user = new User();
user.setName("testuser");
user.setEmail("abc@xyz.com");
analytics.setUser(user);
```

Kotlin:
```kotlin
var user = User()
user.name = "testuser"
user.email = "abc@xyz.com"
analytics.setUser(user)
```

`User` datu klaseak kate-propietate hauek ditu:

- **localId**: Erabiltzailearen ID lokala.
- **autentifikazioa**: Autentifikatutako erabiltzaile IDa.
- **authType**: Autentifikatutako erabiltzaile IDa lortzeko erabiltzen den autentifikazio mota.
- **izena**: Erabiltzailearen izena.
- **posta elektronikoa**: erabiltzailearen helbide elektronikoa.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
