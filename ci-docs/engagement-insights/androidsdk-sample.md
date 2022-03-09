---
title: Android SDK adibidea
description: Android SDK buruz ikasteko lagin proiektua
author: britl
ms.reviewer: m-hartmann
ms.author: britl
ms.date: 06/23/2021
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: 2ee29a98192bb53bd92241d71c1a76ec2b7bf846
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8229903"
---
# <a name="run-the-android-sdk-sample"></a>Abiarazi Android SDK adibidea

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Android proiektuaren adibide honek SDK aplikazio batean nola funtzionatzen duen ulertzen lagunduko dizu. Ez duzu koderik idatzi behar. Gehitu irensteko gakoa eta gertaerak zure laneko eremuan berehala ikus ditzakezu.

## <a name="prerequisites"></a>Aurrebaldintzak

- [Android Studio](https://developer.android.com/studio)
- [Gehitze gakoa](get-started-android.md)

## <a name="download-the-android-sdk-sample"></a>Deskargatu Android SDK adibidea

1. [Deskargatu konpromisoari buruzko Android SDK lagina](https://download.pi.dynamics.com/sdk/EI-SDKs/ei-android-sample.zip).
1. Deskonprimitu konprimitutako fitxategia `ei-android-sample.zip`.
1. Ireki deskonprimitutako karpeta hemen Android Studio.
1. Urtean `AndroidManifest.xml` fitxategia, ordeztu katea `"Your-Ingestion-Key"` zelaian zure laneko espazioa sartzeko gakoarekin, konpromisoen inguruko informazioetatik **Administratzailea** > **Lan eremua** > **Instalazio gida**. 

   > [!NOTE]
   > Ez duzu ordezkatu behar `${applicationId}` atala. Automatikoki bete beharko litzateke.

   ```xml
   <application>
   ...
       <provider
           android:authorities="${applicationId}.com.microsoft.engagementinsights.eiandroidsdk.AnalyticsContentProvider"
           android:name="microsoft.dynamics.engagementinsights.eiandroidsdk.AnalyticsContentProvider" />
       <meta-data
           android:name="com.microsoft.engagementinsights.ingestionKey"
           android:value="Your-Ingestion-Key" />
       <meta-data
           android:name="com.microsoft.engagementinsights.autoCapture"
           android:value="true" />
   ...
   </application>
   ```

1. Hautatu **Exekutatu** adibide-proiektua hasteko.
1. Ikusi gertaerak zure laneko eremuan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
