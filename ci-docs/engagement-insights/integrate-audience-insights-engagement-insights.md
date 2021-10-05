---
title: Sortu esteka bat hartzaile xehetasun eta elkarreragin xehetasunen artean
description: Sortu lotura aktibo bat ikusleen estatistiken eta konpromisoen estatistiken artean, datuen noranzko bikoitza partekatzea ahalbidetzeko.
ms.date: 09/08/2021
ms.service: customer-insights
ms.topic: conceptual
author: mkisel
ms.author: mkisel
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 8d93a49a29c29103e189a6d4a42294c18dc28abd
ms.sourcegitcommit: f1e3cc51ea4cf68210eaf0210ad6e14b15ac4fe8
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/27/2021
ms.locfileid: "7559003"
---
# <a name="create-a-link-between-audience-insights-and-engagement-insights"></a>Sortu esteka bat hartzaile xehetasun eta elkarreragin xehetasunen artean

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Konpromisoen eta publikoaren estatistiken arteko integrazioak inguruneak lotzen ditu bi gaitasunetatik, eta datuak haien artean noranzko bitan banatzeko aukera ematen du.

Erabili profil bateratuak eta segmentuen audientzia estatistiketatik konpromiso estatistiketan analisi aukera gehiago lortzeko. Esportatu negozio balio handia duten gertaerak konpromisoen estatistiketatik. Erabili gertaera hauek audientzia estatistiketan profil bateratuetara datuak gehitzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- Ikusleen estatistiken profilak an gorde behar dira Azure Data Lake Storage jabea duzun kontua edo [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro.md)&ndash;datuen laku kudeatua. 
- Hartzaileen xehetasunen ingurunean erlazionatutako Dataverse ingurune bat izan behar du. Eta ingurune horrek Dataverse erabiltzen badu datuak gordetzeko, ziurtatu **Gaitu datuak partekatzea** aukera hautatzen duzula hartzaileen xehetasunetan. Informazio gehiaog lortzeko, ikusi [Sortu eta konfiguratu ordainpeko ingurune bat hartzaileen xehetasunetan](../audience-insights/get-started-paid.md).
- Administratzaile-baimenak behar dituzu bai konpromisoen inguruko estatistiketarako eta bai publikoetako estatistiketarako.
- Lotutako inguruneek eskualde geografiko berean egon behar dute.

> [!NOTE]
> - Hartzaileen xehetasunen harpidetza probako bertsioa bada, hartzaileen xehetasunen barruan kudeatutako datu-biltegi bat erabiltzen duena, jarri harremanetan honekin laguntza lortzeko: [pirequest@microsoft.com](mailto:pirequest@microsoft.com). 
> - Zure ikusleei buruzko informazioa inguruneak zurea erabiltzen badu Azure Data Lake Storage datuak gordetzeko, konpromisoari buruzko informazioaren Azure zerbitzu nagusia gehitu behar duzu zure biltegiratze kontuan. Xehetasunak lortzeko, joan hona [Konektatu Azure Data Lake Storage kontua Azure zerbitzu nagusiarekin ikusleei buruzko informazioa lortzeko](../audience-insights/connect-service-principal.md). 


## <a name="create-an-environment-link"></a>Sortu ingurune bat estekan

Ingurunearen esteka sor dezakezu **Administratzailea** > **Ingurumena** ezarpenak konpromiso estatistiketan.

**Ezartzeko aktiboa den esteka bat hartzaile xehetasun eta elkarreragin xehetasunen artean**

1. Gainean **Ingurumen administratzailea** orria, hautatu **Lotu inguruneak** fitxa.

    :::image type="content" source="media/integrate1.png" alt-text="Konfiguratu ingurunea.":::

1. Aukeratu **Konfiguratu inguruneak** goiko ezkerreko izkinan edo pantailaren behealdean.

     :::image type="content" source="media/integrate2.png" alt-text="Hautatu hartzaileen xehetasunen ingurune bat.":::

1. Aukeratu ikusleen ikuspegi ingurunea eta hautatu ***Hurrengoa** amaitzeko. Orain estekatutako inguruneetarako aukerako ezaugarriak hauta ditzakezu.
 
## <a name="enable-audience-insights-unified-profiles-attributes-and-segments"></a>Gaitu publikoaren estatistikak profil bateratuen atributuak eta segmentuak

Inguruneak estekatu ostean estekatutako inguruneetarako aukerako ezaugarriak hauta ditzakezu. Ezaugarri horiei esker, publikoaren estatistiketatik profil bateratuen atributuak eta segmentuak bezeroen datuen analisi interaktiboa egiteko daude.

> [!IMPORTANT]
> Ikusleen estatistiken segmentuak konpromisoen estatistiketan agertzeko, lehenik eta behin egin behar duzu [exekutatu bateratze eta downstream prozesuak](../audience-insights/merge-entities.md). Downstream prozesuak garrantzitsuak dira, ikusleei buruzko informazio segmentuak prestatzen dituen taula bakarra sortzen dutelako, konpromisoekin partekatzeko. (Sistema freskatzea programatuta badago, automatikoki beheranzko prozesuak sartuko ditu.)

**Web datuak konpromiso estatistiketan aztertzeko**

1. Gainean **Ingurumen administratzailea** orrialdea, aktibatu **Partekatu ikusleen estatistiketako datuak konpromisoekin** txandakatu eta hautatu **Hurrengoa**.

    :::image type="content" source="media/integrate4.png" alt-text="Hautatu eginbideak.":::

1. Hautatu konpromiso estatistiketan dimentsio bihurtuko diren profil bateratuen atributuak. (Atributu guztiak ez dira dimentsio baliagarriak. Adibidez, litekeena da behar izatea **izen** edo **abizen** zure webguneko gertaerak aztertzeko atributu gisa.)

    :::image type="content" source="media/integrate5.png" alt-text="Aukeratutako dimentsioak.":::

   >[!NOTE]
   > Identifikatzaileak irudikatzen dituzten ikusleen profileko atributu guztiek (adibidez **NAN** eta **ordezko IDa**) eskuragarri dauden atributuetatik iragazi eta konpromisoari buruzko informazioetan dimentsio bihurtzen dira.

1. Atributuak hautatzen amaitutakoan, hautatu **Hurrengoa**.
1. Gehitu audientzia estatistiken profileko neurriak eta segmentuak ikus ditzaketen erabiltzaileak konpromiso estatistiketan.

    :::image type="content" source="media/integrate6.png" alt-text="Kudeatu bezeroen datuetarako sarbidea.":::

   > [!IMPORTANT]
   > Urrats honetan erabiltzaileak esplizituki gehitzen ez badituzu, datuak ezkutatuko zaizkie erabiltzaileei konpromisoari buruzko informazioetan.
   > Ikusleen estatistiken segmentuak konpromisoen estatistiketan agertzeko, lehenik eta behin egin behar duzu [exekutatu bateratze eta downstream prozesuak](../audience-insights/merge-entities.md). Downstream prozesuak garrantzitsuak dira, ikusleei buruzko informazio segmentuak prestatzen dituen taula bakarra sortzen dutelako, konpromisoekin partekatzeko. (Sistema freskatzea programatuta badago, automatikoki beheranzko prozesuak sartuko ditu.)

1. Berrikusi zure hautapena eta hautatu **Amaitu**.

    :::image type="content" source="media/integrate7.png" alt-text="Berrikusi bezeroen datuen ezarpenak.":::

## <a name="export-refined-events-to-audience-insights"></a>Esportatu findutako gertaerak hartzaileen xehetasunetara

Inguruneen arteko lotura sortu ondoren, gertaera finduak esportatu ditzakezu konpromisoen estatistiketatik ikusleen estatistiketara eta datu-iturburu berri gisa har ditzakezu. 

Informazio gehiagorako, joan hona [Integratu konpromiso estatistiketatik datozen webguneak ikusleekin](../audience-insights/integrate-engagement-insights.md).

<!--
## Share engagement insights refined events with audience insights

After you create a link between environments, a new option becomes available for you to share [refined events](refined-events.md) with audience insights.

Consider the following when creating refined events for audience insights: 

- Provide a meaningful name for the refined event. It will be used as an activity name in audience insights.
- Select at least the following properties to create an activity in audience insights: 
    - Signal.Action.Name indicates the activity details.
    - Signal.User.Id maps with the customer ID.
    - Signal.View.Uri is a web address as a basis for segments or measures.
    - Signal.Export.Id is a primary key for events.
    - Signal.Timestamp determines the date and time for the activity.

To share refined events:

1. From the engagement insights menu, select **Data** and then select the **Events** tab.
2. On the **Action** menu, select **Share as activity**.

    :::image type="content" source="media/integrate8.png" alt-text="Data shared events settings.":::

3. You can view and stop actively shared events on the **Export and Sharing** tab.
4. -- per Michael K, we need a mock here (Mukesh needs to update to reflect what happens in AUI once a user shares a refined event (i.e. no longer AUI, data wrangler needs to go discover data in the storage, the shared event is available as a DS and entity, correct?)

### Attach refined events shared as activities to unified profiles in audience insights

You can bring customer web activity data from engagement insights into audience insights. In addition to transactional, demographic, or behavioral data, you can view activities on the web in unified customer profiles. You can then use these profiles to get insights such as segments, measures, and predictions for audience activation.

Follow the steps in [data unification](../audience-insights/data-unification.md) to map, match, and merge website authentication information to unified profiles in audience insights.

You can also share refined events that are now available in audience insights, identified as data sources and entities. 

Next, you can relate event data from engagement insights as unified activities in customer profiles.

### Relate refined event data as an activity of a customer profile

After unifying the data, you can configure the activity for the customer profile. For more information, go to [Customer activities](../audience-insights/activities.md).

:::image type="content" source="media/web-event-activity.png" alt-text="Activities page with expanded Edit activity pane.":::

Next, configure the new activity by using mapping elements: 

- **Primary Key**: Signal.Export.Id, a unique ID that is available for every event record in engagement insights. This property is automatically generated.

- **Timestamp**: Signal.Timestamp in the event property.

- **Event**: Signal.Name, the event name that you want to track.

- **Web address**: Signal.View.Uri that refers to the URI of the page that created the event.

- **Details**: Signal.Action.Name to represent the information to associate with the event. The selected property in this case indicates that the event is for email promotion.

- **Activity type**: In this example, we choose the existing activity type WebLog. This selection is a useful filter option to run prediction models or create segments based on this activity type.

- **Set up relationship**: This important setting ties the activity to existing customer profiles. **Signal.User.Id** is the identifier configured in the SDK to be collected. It relates to the user ID in other data sources that are configured in audience insights. 

This example configures the relationship between Signal.User.Id and RetailCustomers:CustomerRetailId, which is the primary key that was identified in the map step of the data unification process.

After processing the activities, you can review customer records and open a customer card to see activities from engagement insights in the timeline. 

> [!TIP]
> To find a customer ID that has an engagement insights activity, go to **Entities** and preview the data for the UnifiedActivity entity. **ActivityTypeDisplay = WebLog** contains the engagement insights activity configured in the preceding example. Copy the customer ID for one of those records and search<!--note from editor: Edit okay? I couldn't quite follow this.-- > for that ID on the **Customers** page.

--> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
