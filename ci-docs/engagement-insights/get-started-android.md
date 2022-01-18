---
title: Hasi Android SDK erabiltzen
description: Ikusi Android SDK pertsonalizatzen eta exekutatzen
author: britl
ms.reviewer: mhart
ms.custom: intro-internal
ms.author: britl
ms.date: 10/19/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: 71ec4841303bd17d3f605547be8d6032c58a7b21
ms.sourcegitcommit: bb1ca84bc38e81fb2ff2961c457384b7beb5b5fa
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 01/15/2022
ms.locfileid: "7977497"
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

## <a name="integrate-the-sdk-into-your-application"></a>Integratu SDK zure aplikazioan
Hasi prozesua lan egiteko lan eremua hautatuz, Android plataforma mugikorra hautatuz eta Android SDK deskargatuz.

- Erabili ezkerreko nabigazio paneleko laneko espazio aldatzailea zure lan eremua hautatzeko.

- Ez baduzu lehendik dagoen lan-eremurik, hautatu **Laneko area berria** eta jarraitu pausoak sortzeko [laneko area berria](create-workspace.md).

- Laneko area sortu ondoren, joan hona: **Administratzailea** > **Lan eremua** eta, ondoren, hautatu **Instalazio gida**.

## <a name="configure-the-sdk"></a>Konfiguratu SDK

Behin SDK deskargatuta, Android Studio-n egin dezakezu harekin lan, gertaerak gaitu eta definitzeko. Bi modu daude horretarako:
### <a name="option-1-use-jitpack-recommended"></a>1. aukera: Erabili JitPack (gomendatua)
1. Gehitu JitPack biltegia erroko `build.gradle` elementuan:
    ```gradle
    allprojects {
        repositories {
            ...
            maven { url 'https://jitpack.io' }
        }
    }
    ```

1. Gehitu mendekotasuna:
    ```gradle
    dependencies {
        implementation 'com.github.microsoft:engagementinsights-sdk-android:v1.0.0'
        api 'com.google.code.gson:gson:2.8.1'
    }
    ```

### <a name="option-2-use-download-link"></a>2. aukera: Erabili deskargatzeko esteka
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

## <a name="enable-auto-instrumentation"></a>Gaitu instrumentazio automatikoa

1. Gehitu sareko eta Interneteko baimenak `manifests` karpetako `AndroidManifest.xml` fitxategian.
    ```xml
    <manifest>
        ...
        <uses-permission android:name="android.permission.INTERNET" />
        <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
    ```

1. Ezarri parte-hartzearen xehetasunen SDKren konfigurazioa `AndroidManifest.xml` fitxategiaren bidez.

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

   >[!NOTE]
   >`Action` gertaerak eskuz gehitu behar dira.

1. (Aukerakoa) Beste konfigurazio batzuen artean, amaierako puntu biltzailearen URLa ezartzea dago. Ingestio-gako metadatuen azpian gehi daitezke `AndroidManifest.xml`.

   ```xml
        <meta-data
            android:name="com.microsoft.engagementinsights.endpointUrl"
            android:value="https://some-endpoint-url.com" />
   ```

## <a name="implement-custom-events"></a>Ezarri gertaera pertsonalizatuak

Behin SDK abiarazita, gertaerekin eta euren propietateekin lan egin dezakezu `MainActivity` ingurunean.


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

## <a name="set-user-details-for-your-event-optional"></a>Ezarri zure gertaeraren erabiltzaile xehetasunak (aukerakoa)

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
