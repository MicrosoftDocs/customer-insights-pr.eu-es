---
title: Bezeroen jarduerak
description: Definitu bezeroen jarduerak eta ikusi denbora-lerroan bezeroen profiletan.
ms.date: 09/27/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.reviewer: mhart
ms.topic: conceptual
author: CadeSanthaMSFT
ms.author: cadesantha
manager: shellyha
ms.openlocfilehash: bcb8d42963719f5d225556c31b3fc06db8573e5b
ms.sourcegitcommit: 31985755c7c973fb1eb540c52fd1451731d2bed2
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/22/2021
ms.locfileid: "7673122"
---
# <a name="customer-activities"></a>Bezeroen jarduerak

Konbinatu bezeroaren jarduerak [hainbat datu iturri](data-sources.md) hurrengoan Dynamics 365 Customer Insights jarduerak kronologikoki zerrendatuko dituen kronograma sortzeko. Sartu kronograma Dynamics 365 aplikazioetan [Bezero txartelaren gehigarria](customer-card-add-in.md) irtenbide batean edo Power BI arbela.

## <a name="define-an-activity"></a>Definitu jarduera

Zure datu-iturriak datu-iturri ugarietatik transakzio- eta jarduera-datuak izan ditzaketen entitateak dira. Identifika itzazu entitate horiek eta hautatu bezeroaren denbora-lerroan ikusi nahi dituzun jarduerak. Aukeratu zure xede-jarduera edo jarduerak biltzen dituen entitatea.

Entitate batek gutxienez motako atributu bat izan behar du **Data** bezeroaren denbora-lerroan sartzeko eta ezin dituzu entitateak gehitu gabe **data** eremuak. The **Gehitu jarduera** kontrola ezgaitzen da horrelako entitate bat aurkitzen ez bada.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Jarduerak**.

1. Aukeratu **Gehitu jarduera** jarduera konfiguratzeko prozesuaren esperientzia gidatua hasteko.

1. Hurrengoan **Jardueren datuak** urratsa, ezarri eremu hauetako balioak:

   - **Jardueraren izena**: Hautatu zure jarduerarako izen bat.
   - **Erakunde**: Aukeratu transakzio- edo jarduera-datuak biltzen dituen entitatea.
   - **Gako nagusia**: Hautatu erregistroa era esklusiboan identifikatzen duen eremua. Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.

   :::image type="content" source="media/Activity_Wizard1.PNG" alt-text="Konfiguratu jardueraren datuak izena, entitatea eta gako nagusiarekin.":::

1. Aukeratu **Hurrengoa** hurrengo urratsera joateko.

1. Urtean **Harremana** urratsa, konfiguratu xehetasunak zure jarduera-datuak dagozkien bezeroaren erregistroarekin konektatzeko. Urrats honek entitateen arteko konexioa bistaratzen du.  

   - **Lehenengoa**: Zure jarduera entitatean atzerriko eremua, beste entitate batekin harremanak sortzeko erabiliko dena.
   - **Bigarrena**: Zure jarduera entitatearekin erlazionatuko duen iturburu bezeroari dagokiona. Datuak bateratzeko prozesuan erabiltzen diren iturburu bezeroen entitateekin bakarrik lotu zaitezke.
   - **Hirugarrena**: Jarduera entitate honen eta hautatutako iturburu bezero entitatearen arteko erlazioa badago jadanik, harremanaren izena irakurtzeko soilik moduan egongo da. Harreman hori existitzen ez bada, harreman berri bat sortuko da koadro honetan ematen duzun izenarekin.

   :::image type="content" source="media/Activity_Wizard2.PNG" alt-text="Definitu entitate-harremana.":::

   > [!TIP]
   > B-to-B inguruneetan, kontuko entitateen eta beste entitate batzuen artean hauta dezakezu. Kontuko entitate bat hautatzen baduzu, harreman bidea automatikoki ezartzen da. Beste entitate batzuetarako, bitarteko entitate baten edo gehiagoren arteko harremana definitu behar duzu, kontuko entitate batera iritsi arte.

1. Aukeratu **Hurrengoa** hurrengo urratsera joateko. 

1. Hurrengoan **Jarduera bateratzea** urratsa, aukeratu jarduera gertaera eta zure jardueraren hasiera ordua. 
   - **Beharrezko eremuak**
      - **Ekitaldi jarduera**: Jarduera honen gertaera den eremua.
      - **Denbora-marka**: Zure jardueraren hasiera ordua adierazten duen eremua.

   - **Aukerako eremuak**
      - **Xehetasun osagarria**: Jarduera honetarako informazio garrantzitsua duen eremua.
      - **Ikonoa**: Jarduera mota hau ondoen irudikatzen duen ikonoa.
      - **Web-helbidea**: Jarduera honi buruzko informazioa duen URLa duen eremua. Adibidez, jarduera hau iturri duen transakzio-sistema. URL hau datu-iturburu-eko edozein eremu izan daiteke edo Power Query eraldaketa erabiliz eremu berri gisa eraiki daiteke. URL datuak fitxategian gordeko dira *Jarduera bateratua* entitatea, erabilita ibaian behera kontsumitu daitekeena [APIak](apis.md).

   - **Erakutsi denbora-eskalan**
      - Aukeratu jarduera ikuspegi kronologikoan erakutsi nahi duzun bezeroen profiletan. Jarduera denbora-lerroan erakusteko, hautatu **Bai**. Ezkutatzeko, hautatu **Ez**.

      :::image type="content" source="media/Activity_Wizard3.PNG" alt-text="Zehaztu bezeroaren jardueraren datuak Jarduera bateratuko entitate batean.":::

1. Hautatu **Hurrengoa** hurrengo urratsera mugitzeko. Aukeratu dezakezu **Amaitu eta berrikusi** aktibitatea orain gordetzeko, jarduera mota gisa ezarrita **Beste batzuk**. 

1. Hurrengoan **Jarduera mota** urratsa, aukeratu jarduera mota eta hautatu aukeran Customer Insights beste arlo batzuetan erabiltzeko jarduera mota batzuk semantikoki mapatu nahi dituzun. Unean, *Feedback*, *Loyalty*, *SalesOrder*, *SalesOrderLine*, eta *Subscription* jarduera motak semantikoki esleitu daitezke, eremuak esleitzea onartu ondoren. Jarduera mota bat jarduera berrirako garrantzitsua ez bada, hauta dezakezu *Beste batzuk* edo *Sortu berria* jarduera mota pertsonalizatua lortzeko.

1. Hautatu **Hurrengoa** hurrengo urratsera mugitzeko. 

1. Hurrengoan **Berrikuspena** urratsa, egiaztatu hautapenak. Itzuli aurreko edozein urratsetara eta eguneratu informazioa beharrezkoa bada.

   :::image type="content" source="media/Activity_Wizard5.PNG" alt-text="Berrikusi jarduera baterako zehaztutako eremuak.":::
   
1. Aukeratu **Gorde jarduera** aldaketak aplikatzeko eta hautatu **Eginda** atzera joateko **Datuak** > **Jarduerak**. Hemen ikus ditzakezu zein jarduera erakutsiko diren kronograman. 

1. Gainean **Jarduerak** orrialdea, hautatu **Korrika egin** jarduera prozesatzeko. 

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.


## <a name="manage-existing-activities"></a>Kudeatu lehendik dauden jarduerak

Aktibatuta **Datuak** > **Jarduerak**, gordetako jarduera guztiak ikusi eta kudeatu ditzakezu. Jarduera bakoitza iturriari, entitateari eta jarduera motari buruzko xehetasunak ere biltzen dituen errenkada baten bidez irudikatzen da.

Jarduera bat hautatzean ekintza hauek erabilgarri daude. 

- **Editatu**: Berrikuspen urratsean jarduera konfigurazioa irekitzen du. Urrats honetatik uneko konfigurazioaren zati bat edo guztia alda dezakezu. Konfigurazioa aldatu ondoren, hautatu **Gorde jarduera** eta, ondoren, hautatu **Korrika egin** aldaketak prozesatzeko.

- **Aldatu izena**: Elkarrizketa-koadro bat irekitzen du eta bertan hautatutako jardueraren beste izen bat sar dezakezu. Aldaketak aplikatzeko, hautatu **Gorde**.

- **Ezabatu**: Elkarrizketa bat irekitzen du hautatutako jardueraren ezabaketa berresteko. Jarduera bat baino gehiago aldi berean ezaba ditzakezu jarduerak hautatuta eta gero ezabatzeko ikonoa hautatuta. Hautatu **Ezabatu** ezabatzea baieztatzeko.

## <a name="view-activity-timelines-on-customer-profiles"></a>Ikusi jarduera profilak bezeroen profiletan

Bezeroen jarduerak konfiguratu ondoren, hautatu **Erakutsi jardueren kronograman** jardueraren konfigurazioan zure bezeroaren jarduera guztiak bezeroaren profilean aurkitzeko.

Bezero baten kronograma irekitzeko, joan hona: **Bezeroak** eta aukeratu ikusi nahi duzun bezeroaren profila.

Bezero batek konfiguratu duzun jarduera batean parte hartu badu, helbidean aurkituko duzu **Jardueren kronograma** atala.

:::image type="content" source="media/Activity_Timeline1.PNG" alt-text="Ikusi konfiguratutako jarduerak Bezeroen profiletan.":::

Jardueren denbora-lerroan jarduerak iragazteko hainbat modu daude:

- Jardueraren ikono bat edo gehiago hauta ditzakezu emaitzak fintzeko hautatutako motak soilik sartzeko.

  :::image type="content" source="media/Activity_Timeline2.PNG" alt-text="Iragazi jarduerak motaren arabera ikonoak erabiliz.":::

- Aukeratu dezakezu **Iragazi** iragazki-panela irekitzeko zure denbora-lerroaren iragazkiak konfiguratzeko.

   1. Iragazi dezakezu *Jarduera mota* eta *Data*
   1. Aukeratu **Aplikatu** jardueren denbora-lerroan iragazkiak erabiltzeko.

   :::image type="content" source="media/Activity_Timeline3.PNG" alt-text="Erabili iragazki panela iragazki baldintzak konfiguratzeko.":::

Iragazkiak kentzeko, hautatu **x** kronogramari aplikatutako iragazki bakoitzaren ondoan edo hautatu **Garbitu iragazkiak**.


> [!NOTE]
> Jardueren iragazkiak bezeroaren profila uzten duzunean kentzen dira. Bezeroen profilean irekitzen duzun bakoitzean aplikatu behar dituzu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
