---
title: Bezeroen jarduerak
description: Definitu bezeroen jarduerak eta ikusi bezeroaren kronologian.
ms.date: 10/13/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: MichelleDevaney
ms.author: midevane
manager: shellyha
ms.openlocfilehash: fbfa9d7e00859cc80c24b98bd2dc806f1fda7803
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596714"
---
# <a name="customer-activities"></a>Bezeroen jarduerak

Konbinatu Dynamics 365 Customer Insights-eko [hainbat datu-iturburutako](data-sources.md) bezeroen jarduerak, jarduerak ordena kronologikoan zerrendatuko dituen bezeroen kronologia sortzeko. Kronika customer engagement aplikazioetan sar dezakezu Dynamics 365 aplikazioan [Bezero Txartelaren gehigarria](customer-card-add-in.md), edo a Power BI Arbel.

## <a name="define-an-activity"></a>Definitu jarduera

Zure datu-iturriak datu-iturri ugarietatik transakzio- eta jarduera-datuak dituzten entitateak dira. Identifika itzazu entitate horiek eta hautatu bezeroaren denbora-lerroan ikusi nahi dituzun jarduerak. Aukeratu zure xede-jarduera edo jarduerak biltzen dituen entitatea.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.

1. Hautatu **Gehitu jarduera**.

   > [!NOTE]
   > Entitate batek gutxienez motako atributu bat izan behar du **Data** bezeroaren denbora-lerroan sartzeko eta ezin dituzu entitateak gehitu gabe **data** eremuak. The **Gehitu jarduera** kontrola ezgaitzen da horrelako entitate bat aurkitzen ez bada.

1. Sarbidean **Gehitu jarduera** panela, ezarri hurrengo eremuetarako balioak:

   - **Erakunde**: Aukeratu transakzio- edo jarduera-datuak biltzen dituen entitatea.
   - **Gako nagusia**: Hautatu erregistroa era esklusiboan identifikatzen duen eremua. Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.
   - **Denbora-zigilua**: Aukeratu zure jardueraren hasiera ordua adierazten duen eremua.
   - **Gertaera**: Aukeratu jardueraren gertaera den eremua.
   - **Web helbidea**: Aukeratu URLa adierazten duen eremua jarduera honi buruzko informazio osagarria eskaintzen duena. Adibidez, jarduera hau iturri duen transakzio-sistema. URL hau datu-iturburu-eko edozein eremu izan daiteke edo Power Query eraldaketa erabiliz eremu berri gisa eraiki daiteke. URLko datu hau Jarduera Unibidearen entitatean gordeko da, APIak erabiliz downstream kontsumitu daitekeena.
   - **Xehetasunak**: Aukeran, hautatu gehitzen den eremua xehetasun gehiagorako.
   - **Ikonoa**: Aukeran, hautatu jarduera hau adierazten duen ikonoa.
   - **Jarduera mota**: Idatzi jarduera motaren definizio semantikoa hobekien deskribatzen duen datu arruntaren ereduari erreferentzia.

1. Sarbidean **Ezarri harremana** atala konfiguratu xehetasunak zure jardueraren datuak dagokion bezeroari lotzeko.

    - **Jardueraren entitatearen eremua**: Aukeratu beste erakunde batekin harremana ezartzeko erabiliko den eremuko zure entitatearen eremua.
    - **Bezero entitatea**: Aukeratu dagokion iturburu bezeroaren entitatea zein harremana izango duen. Datuak bateratzeko prozesuan erabiltzen diren iturri bezeroak dituzten erakundeekin soilik erlaziona zaitezke.
    - **Bezeroaren entitatearen eremua**: Eremu honek iturburu bezeroaren entitatearen gako nagusia mapa prozesuan hautatzen den bezala erakusten du. Jatorri bezeroaren entitatearen funtsezko eremu hau jarduera-entitatearekin harremana ezartzeko erabiltzen da.
    - **Izena**: Jarduera-entitate honen eta hautatutako iturri bezeroaren entitatearen arteko harremana badago, erlazioaren izena irakurtzeko moduan egongo da. Horrelako harremanik ez badago, harreman berria sortuko da hemen emandako izenarekin.
   
   > [!div class="mx-imgBorder"]
   > ![Definitu entitate-harremana](media/activities-entities-define.png "Definitu entitate-harremana")

1. Aldaketak aplikatzeko, hautatu **Gorde**.

1. **Jarduerak** orrian, hautatu **Exekutatu**.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="edit-an-activity"></a>Editatu jarduera

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.

2. Hautatu editatu nahi duzun entitate-jarduera eta hautatu **Editatu**. Edo, entitate errenkadan pasa dezakezu eta hauta dezakezu **Editatu** ikonoa.

3. Egin klik botoian **Editatu** ikonoa.

4. Sarbidean **Editatu jarduera** panela, eguneratu balioak eta hautatu **Gorde**.

5. **Jarduerak** orrian, hautatu **Exekutatu**.

## <a name="delete-an-activity"></a>Ezabatu jarduera

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.

2. Hautatu kendu nahi duzun entitate-jarduera eta hautatu **Ezabatu**. Edo, entitate errenkadan pasa dezakezu eta hauta dezakezu **Ezabatu** ikonoa. Gainera, aldi berean ezabatu beharreko hainbat jarduera-entitate hauta ditzakezu.
   > [!div class="mx-imgBorder"]
   > ![Editatu edo ezabatu entitatearen erlazioak](media/activities-entities-edit-delete.png "Editatu edo ezabatu entitatearen erlazioak")

3. Hautatu botoian **Ezabatu** ikonoa.

4. Berretsi ezabatu nahi duzula.


[!INCLUDE[footer-include](../includes/footer-banner.md)]