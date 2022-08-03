---
title: Bezeroen jarduerak
description: Definitu bezeroen jarduerak eta ikusi denbora-lerroan bezeroen profiletan.
ms.date: 07/22/2022
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: CadeSanthaMSFT
ms.author: cadesantha
manager: shellyha
searchScope:
- ci-entities
- ci-customer-card
- ci-relationships
- ci-activities
- ci-activities-wizard
- ci-measures
- ci-segment-suggestions
- customerInsight
ms.openlocfilehash: cc21b0eeb368156437e60d851c2d144f3974c066
ms.sourcegitcommit: c45c3e044034bf866b0662f80a59166cee4ababe
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/22/2022
ms.locfileid: "9188124"
---
# <a name="customer-activities"></a>Bezeroen jarduerak

Bezeroen jarduerak bezeroek egindako ekintzak edo gertaerak dira. Adibidez, transakzioak, laguntza-deien iraupena, webguneen berrikuspenak, erosketak edo itzulketak. Jarduera hauek datu-iturri batean edo gehiagotan daude. Customers Insights-ekin, sendotu zure bezeroen jarduerak hauetatik [datu-iturriak](data-sources.md) eta bezeroen profilekin lotu. Jarduera hauek kronologikoki agertzen dira denbora-lerro batean bezeroaren profilean. Sartu denbora-lerroa Dynamics 365 aplikazioetan [Bezero txartelaren gehigarria](customer-card-add-in.md) irtenbidea.

## <a name="define-an-activity"></a>Definitu jarduera

Entitate batek gutxienez motako atributu bat izan behar du **Data** bezeroaren denbora-lerro batean sartzeko. The **Gehitu jarduera** kontrola ezgaitzen da horrelako entitate bat aurkitzen ez bada.

1. Joan **Datuak** > **Jarduerak**.

1. Hautatu **Gehitu jarduera** esperientzia gidatua hasteko.

1. urtean **Jardueraren datuak** urratsa, sartu informazio hau:

   - **Jardueraren izena** : Zure jardueraren izena.
   - **Jarduera-entitatea** : transakzio- edo jarduera-datuak barne hartzen dituen entitatea.
   - **Lehen gakoa** : Erregistro bat modu esklusiboan identifikatzen duen eremua. Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.

   :::image type="content" source="media/Activity_Wizard1.PNG" alt-text="Konfiguratu jardueraren datuak izena, entitatea eta gako nagusiarekin.":::

1. Hautatu **Hurrengoa**.

1. urtean **Harremana** urratsa, hautatu **Gehitu harremana** zure jarduera-datuak dagokion bezero-erregistroarekin konektatzeko. Urrats honek entitateen arteko konexioa bistaratzen du.  

   - **Entitatearen atzerriko gakoa** : beste entitate batekin harremana ezartzeko erabiliko den zure jarduera-entitateko eremua.
   - **Entitatearen izenari** : Zure jarduera-entitatearekin harremana izango duen iturburu-bezero-entitatea. Datuak bateratzeko prozesuan erabiltzen diren iturburu bezeroen entitateekin bakarrik lotu zaitezke.
   - **Harremanaren izena** : Entitateen arteko harremana identifikatzen duen izena. Jarduera-entitate honen eta hautatutako iturburu-bezero-entitatearen arteko erlaziorik badago, erlazioaren izena irakurtzeko soilik da.

   :::image type="content" source="media/Activity_Wizard2.PNG" alt-text="Definitu entitate-harremana.":::

   > [!TIP]
   > B-to-B inguruneetan, kontuko entitateen eta beste entitate batzuen artean hauta dezakezu. Kontuko entitate bat hautatzen baduzu, harreman bidea automatikoki ezartzen da. Beste entitate batzuetarako, bitarteko entitate baten edo gehiagoren arteko harremana definitu behar duzu, kontuko entitate batera iritsi arte.

1. Hautatu **Aplikatu** harremana sortzeko.

1. Hautatu **Hurrengoa**.

1. Hurrengoan **Jarduera bateratzea** urratsa, aukeratu jarduera gertaera eta zure jardueraren hasiera ordua.
   - **Beharrezko eremuak**
      - **Ekitaldi jarduera**: Jarduera honen gertaera den eremua.
      - **Denbora-marka**: Zure jardueraren hasiera ordua adierazten duen eremua.

   - **Aukerako eremuak**
      - **Xehetasun osagarria**: Jarduera honetarako informazio garrantzitsua duen eremua.
      - **Ikonoa**: Jarduera mota hau ondoen irudikatzen duen ikonoa.
      - **Web-helbidea**: Jarduera honi buruzko informazioa duen URLa duen eremua. Adibidez, jarduera hau iturri duen transakzio-sistema. URL hau datu-iturburu-eko edozein eremu izan daiteke, edo eremu berri gisa eraiki daiteke Power Query eraldaketa. URL datuak fitxategian gordeko dira *Jarduera bateratua* entitatea, erabilita ibaian behera kontsumitu daitekeena [APIak](apis.md).

   - **Erakutsi denbora-eskalan**
      - Aukeratu jarduera ikuspegi kronologikoan erakutsi nahi duzun bezeroen profiletan. Jarduera denbora-lerroan erakusteko, hautatu **Bai**. Ezkutatzeko, hautatu **Ez**.

      :::image type="content" source="media/Activity_Wizard3.PNG" alt-text="Zehaztu bezeroaren jardueraren datuak Jarduera bateratuko entitate batean.":::

1. Hautatu **Hurrengoa** jarduera mota aukeratzeko edo hautatu **Amaitu eta berrikusi** jarduera gordetzeko jarduera mota gisa ezarrita **Bestela**.

1. Hurrengoan **Jarduera mota** urratsa, aukeratu jarduera mota eta hautatu aukeran Customer Insights beste arlo batzuetan erabiltzeko jarduera mota batzuk semantikoki mapatu nahi dituzun. Gaur egun, *Iritzia*, *·*, *Eskaera*, *·*, eta *Harpidetza* jarduera motak semantika onartzen dute eremuak mapatzea onartu ondoren. Jarduera mota bat jarduera berrirako garrantzitsua ez bada, hauta dezakezu *Beste batzuk* edo *Sortu berria* jarduera mota pertsonalizatua lortzeko.

1. Hautatu **Hurrengoa**.

1. Hurrengoan **Berrikuspena** urratsa, egiaztatu hautapenak. Itzuli aurreko edozein urratsetara eta eguneratu informazioa beharrezkoa bada.

1. Aukeratu **Gorde jarduera** aldaketak aplikatzeko eta hautatu **Eginda** atzera joateko **Datuak** > **Jarduerak**. Sortutako jarduera bistaratzen da.

1. Zure jarduera guztiak sortu ondoren, hautatu **Korrika egin** horiek prozesatzeko.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="manage-existing-activities"></a>Kudeatu lehendik dauden jarduerak

Joan **Datuak** > **Jarduerak** gordetako jarduerak, haien iturburu-entitatea, jarduera mota eta bezeroen denbora-lerroan sartzen badira ikusteko. Jardueren zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun jarduera aurkitzeko.

Hautatu jarduera bat erabilgarri dauden ekintzak ikusteko.

- **Editatu** konfigurazioa aldatzeko jarduera. Konfigurazioa berrikuspen urratsean irekitzen da. Konfigurazioa aldatu ondoren, hautatu **Gorde jarduera** eta, ondoren, hautatu **Korrika egin** aldaketak prozesatzeko.
- **Aldatu izena** jarduera. Aldaketak aplikatzeko, hautatu **Gorde**.
- **Ezabatu** jarduera. Jarduera bat baino gehiago aldi berean ezabatzeko, hautatu jarduerak eta gero **Ezabatu**. Berretsi ezabatzea.

## <a name="view-activity-timelines-on-customer-profiles"></a>Ikusi jarduera profilak bezeroen profiletan

1. Hautatu baduzu **Erakutsi jardueren denbora-lerroan** jardueraren konfigurazioan, joan hona **Bezeroak** eta hautatu bezeroaren profil bat bezeroaren jarduerak ikusteko **Jardueren kronograma** atala.

   :::image type="content" source="media/Activity_Timeline1.PNG" alt-text="Ikusi konfiguratutako jarduerak Bezeroen profiletan.":::

1. Jarduerak jardueren denbora-lerroan iragazteko:

   - Hautatu jarduera-ikonoetako bat edo gehiago zure emaitzak hobetzeko, hautatutako motak soilik sartzeko.

     :::image type="content" source="media/Activity_Timeline2.PNG" alt-text="Iragazi jarduerak motaren arabera ikonoak erabiliz.":::

   - Hautatu **Iragazkia** iragazkien panel bat irekitzeko zure denbora-lerroko iragazkiak konfiguratzeko. Iragazi arabera *Jarduera mota* eta/edo *Data*. Hautatu **Aplikatu**.

     :::image type="content" source="media/Activity_Timeline3.PNG" alt-text="Erabili iragazki panela iragazki baldintzak konfiguratzeko.":::

1. Iragazkiak kentzeko, hautatu **Garbitu iragazkiak** edo hautatu **Iragazkia** eta garbitu iragazkia kontrol-laukia.

> [!NOTE]
> Jardueren iragazkiak bezeroaren profila uzten duzunean kentzen dira. Bezero profila irekitzen duzun bakoitzean aplikatu behar dituzu.

[!INCLUDE [footer-include](includes/footer-banner.md)]
