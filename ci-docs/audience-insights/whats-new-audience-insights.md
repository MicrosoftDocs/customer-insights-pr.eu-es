---
title: Eginbide berriak eta datozenak
description: Ezaugarri berriei, hobekuntzei eta akatsak konpontzeko ezaugarriei buruzko informazioa.
ms.date: 05/06/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: midevane
manager: shellyha
ms.openlocfilehash: c66b37d6e4d6ed830238566fbc09934832892b34
ms.sourcegitcommit: 3f9981df97fa7b1f432a446d3f11936ea4cfbde5
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/06/2021
ms.locfileid: "5988905"
---
# <a name="whats-new-in-the-audience-insights-capability-of-dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights hartzaileen xehetasunei buruzko zerbitzuaren ezaugarri berriak

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Gogotsu gaude gure eguneratze berrienak iragartzeko! Artikulu honek aurrebista publikoko eginbideak, aurrebistako funtzioak, erabilgarritasun orokorreko hobekuntzak, eta eginbideen eguneratzeak. Epe luzerako eginbide planak ikusteko, begiratu [Dynamics 365 eta Power Platform kaleratzeko planak](/dynamics365/release-plans/).

Eguneratzeak eskualdeen arabera banatzen ditugu. Beraz, eskualde batzuek beste batzuen aurretik ezaugarriak ikus ditzakete. Modu ezberdinean zehaztu ezean, ez duzu inolako neurririk egin behar eta aplikazioa automatikoki eguneratuko dugu inolako denborarik gabe.

> [!TIP]
> Bidali eta bozkatzeko eginbideak eskaerak eta produktuaren iradokizunak, joan [Dynamics 365 aplikazioaren ideiak atarira](https://experience.dynamics.com/ideas/categories/?forum=79a8c474-4e35-e911-a971-000d3a4f3343&forumName=Dynamics%20365%20Customer%20Insights).

## <a name="april-2021-updates"></a>2021eko apirileko eguneratzeak

2021eko apirileko eguneratzeen artean hainbat funtzio, errendimendu bertsio berritzea eta akatsak konpondu dira.

### <a name="data-unification"></a>Datuak bateratzea
 
- **Datuak bateratzeko bateratze esperientzia hobetua**    
  
   Datuen bateratze prozesuaren bateratze konfigurazioan erabiltzaile esperientzia hobea dugu. Aldaketen artean, bateratutako eremuen ordenamendu intuitiboa eta eremu konbinatuen eta bakarreko estatistiken xehetasunak daude.

- **Entitatea berriro ordenatu eta konfiguratu iturburu erregistro guztiak Bezeroaren entitatean**  
      
   Datuak bateratzeko prozesuan lehendik dagoen konbinazio plan batetik erakundeak berrantolatu eta ken ditzakezu. Malgutasuna ematen du partidu prozesuan entitateak negozioaren beharren arabera ordenatzeko. Gainera, bat ez datozen erregistro guztiak finalean sartzea ahalbidetzen dugu *Bezeroa* entitatea, bezeroaren profileko datuen definizioa definitzen uzten diena.

### <a name="enrichments"></a>Aberasteak

 - **Aberaste berria: helbide hobetuak**    
  
   Pozik gaude bezeroen datuetan helbideak hobetzeko aberastasun berria aurkezteko. Zure datuetako helbideak desegituratuak, osatugabeak edo okerrak izan daitezke. Eginbide honek Microsoft-en ereduak erabiltzen ditu zure helbideak normalizatzeko eta aberasteko Common Data Model formatua zehaztasun eta ikuspegi hobeak lortzeko.
 
   Informazio gehiagorako, ikusi [Bezeroen profilak aberastu helbide hobetuekin](enrichment-enhanced-addresses.md).

- **Aberasketetarako konfigurazio esperientzia gidatua**    
  
   Konfigurazio esperientzia berriro aberastu dugu esperientzia sinple eta gidatu batekin. Orain aberastasunak sortzeko eta editatzeko urratsez urrats argi duzu.
 
   Gainera, hirugarrenen aberastasunetarako konexioen konfigurazioa bereizi genuen konexio bera aberastasun anitzek erabili ahal izateko. Administratzaileek soilik konfigura ditzakete konexio berriak, baina sortutako konexioak daude eskuragarri administratzaile zein laguntzaileentzat.    

   Informazio gehiago eskuratzeko, ikusi [Konexioen informazio orokorra](connections.md).

- **Mota bereko hainbat aberastasun**    
  
   Orain aukera ematen diegu erabiltzaileei aberastasun mota bereko hainbat aberastasun sortzeko eta kudeatzeko. Adibidez, orain bi helbide aberastasun bereizi sor ditzakezu bi bezero segmentu desberdin aberasteko. Mota bereko zenbat aberastasun sor daitezkeen mugak aplikatzen dira eta aberastasun motaren arabera aldatzen dira.
  
   Informazio gehiago lortzeko, ikus [Bezeroen profiletarako aberastea](enrichment-hub.md).

## <a name="march-2021-updates"></a>2021eko eguneratzeak

2021eko martxoko eguneratzeen artean hainbat funtzio, errendimendu bertsio berritzea eta akatsak konpondu dira.

### <a name="activities"></a>Ekintzak

- **Jarduera-morroia eta mota semantikoak**

   Jardueren mapen esperientzia hobetu eta eguneratu dugu jardueren mapen sorrera bideratu eta errazteko. Esperientzia berri honetan, erabiltzaileek esperientzia gidatua lortzen dute prozesuaren urrats bakoitza betetzen laguntzeko. Jarduerak mapatzeko urratsean, jarduera mota askoren artean aukeratzeaz gain, erabiltzaileak datuak semantikoki mapatzea aukeratu dezake *Harpidetza* eta / edo *SalesOrderLine* industria eskema estandarretara, downstream kontsumorako erabil daitezkeenak.   

   Informazio gehiago lortzeko, ikus [Bezeroaren jarduerak](activities.md).

### <a name="data-ingestion"></a>Datu-horniketa

- **Konektatu lokal datu iturrietara erabiliz Power Platform datu-fluxuak eta atebideak** Pozik gaude aurrerapenaren berri ematean Power Platform datu-fluxuak eta lokal konektibitatea Customer Insights-eko atebideak erabiliz lotutako batekin Power Platform edo Dataverse ingurunea. Customer Insights ingurunearekin estekatutako datu iturri berriak Dataverse ingurunea lehenetsia izango da Power Platform datu-fluxuak lokal datuen konektibitatea eta konektore eta transformazio gaitasun multzo aberatsa ekartzen dute.

### <a name="extensibility"></a>Hedagarritasuna

- **Konexioetan eta esportazioetan antolatutako esportazioak** izena aldatu dugu **Esportatu helmugak** orrialdera **Konexioak** eta beste orrialde bat gehitu du **Esportazioak**. Eguneratze honen barruan, lehendik dauden esportazioak konexio eta esportazio batera bihurtuko ditugu konexio hori erabiliz. Administratzaileek argitasun handiagoa dute orain irteerako datuetan **Konexioak** orrialdea. Erabiltzaile rol guztiek dute sarbidea **Esportazioak** orrialdea, baina administratzaileek soilik aukera dezakete laguntzaileek partekatutako konexioekin esportazio zehatzak editatzeko baimena ematea.     
  Informazio gehiagorako, ikus [Konexioen ikuspegi orokorra](connections.md) eta [Esportazioen ikuspegi orokorra](export-destinations.md).

- **Esportatu segmentuak Campaign Monitor-era** Esportaziorako helmugak Campaign Monitor barne zabaldu ditugu. Segmentuak Customer Insights-etik Campaign Monitor zerrendetara esporta ditzakezu eta zure marketin kanpainetarako oinarri gisa erabil ditzakezu.    
   Informazio gehiago eskuratzeko, ikusi [Esportatu Campaign Monitor](export-campaign-monitor.md).

- **Esportatu segmentuak Constant Contact** Esportaziorako helmugak Etengabeko Kontaktua barne zabaldu ditugu. Segmentuak Customer Insights-etik Constant Contact zerrendetara esporta ditzakezu eta zure marketin kanpainetarako oinarri gisa erabil ditzakezu.   
   Informazio gehiago eskuratzeko, ikusi [Esportatu Constant Contact](export-constant-contact.md).

- **Esportatu segmentuak RollWorks-era** Esportaziorako helmugak RollWorks barne zabaldu ditugu. Segmentuak Customer Insights-etik RollWorks audientzetera esporta ditzakezu eta zure B2B iragarkiak oinarri gisa erabil ditzakezu.    
   Informazio gehiago eskuratzeko, ikusi [Esportatu RollWorks-era ](export-rollworks.md).

- **Esportatu segmentuak Snapchat-era** Esportaziorako helmugak Snapchat barne zabaldu ditugu. Segmentuak Customer Insights-etik Snapchat audientzetera esporta ditzakezu eta zure iragarkiak oinarri gisa erabil ditzakezu.     
   Informazio gehiago lortzeko, ikusi [Esportatu Snapchat-era](export-snapchat.md).

### <a name="predictions"></a>Iragarpenak

- **Erabili produktuaren iragazkiak produktu iragarleen gomendioetan** Produktuen iragazkiak erabiltzeko gaitasuna gehitu dugu gure produktuen gomendio ereduan. Zure produktuen azpimultzoa soilik erabiltzen duen iragarpen sor dezakezu.    
   Informazio gehiagorako, ikus [Konfiguratu produktuen iragazkiak](predict-product-recommendation.md#configure-product-filters).

- **Sortu segmentuen ereduen iragarpenak** iragarpen eredu baten emaitzak erabiliz segmentuak sortzeko modu azkarra gehitu dugu. Ereduaren emaitzen orrialdetik, segmentu berri bat erraz sor dezakezu berria hautatuta **Sortu segmentua** aukera.    
  Informazio gehiagorako, ikus [Sortu segmentu bat iragarpen ereduan oinarrituta](prediction-based-segment.md).

- **Produktuen gomendioen azalpenak** Informazioa gehitu dugu, AI ereduak produktuaren gomendioak sortzeko ikasitako funtsezko faktoreak azaltzen dituena eta faktore horiek produktuaren gomendioetan zenbateraino laguntzen duten azalduz. Informazio hau ereduaren emaitzen pantailan gehitzen da.    
   Informazio gehiagorako, ikusi [Berrikusi iragarpen-egoera eta emaitzak](predict-product-recommendation.md#review-a-prediction-status-and-results).

## <a name="february-2021-updates"></a>2021eko otsailaren eguneratzeak

2021eko otsaileko eguneratzeak hainbat funtzio, errendimendu berritze eta akats konponketak biltzen ditu.

#### <a name="extensibility"></a>Hedagarritasuna

- **Esportatu segmentuak AdRoll-era**

  Esportaziorako helmugak AdRoll barne hartzeko zabaldu ditugu. Segmentuak Customer Insights-etik AdRoll-eko ikusleetara esporta ditzakezu eta zure iragarkirako oinarri gisa erabil ditzakezu. Informazio gehiagorako, ikus [AdRoll-erako konektorea](export-adroll.md).

#### <a name="segments"></a>Segmentuak
 
- **Segmentu bikoiztua**
  
  Dauden segmentu berri bat sortzeko, orain segmentu bat bikoiztu eta segmentu bikoitza editatu dezakezu gehiago fintzeko. 

- **Gehitu atributu osagarriak segmentu bati**

  Orain atributuak sar ditzakezu zure segmentuko irteeran, nahiz eta atributu horiek bezeroaren profilekoak ez izan. Adibidez, sartu harpidetzaren IDak segmentu batean, bezero-entitatearekin M: 1 harremana duen harpidetzako entitatearen parte bada ere. Atributua bezeroaren entitatearekin erlazionatutako entitate bati badagokio, atributu hauek sar ditzakezu.  

#### <a name="predictions"></a>Iragarpenak

- **Sortu iragarpen produktuaren gomendioak**

  Bezeroek zer erosteko interesa duten ulertzea negozioaren diru-sarrerak hobetzeko eta pertsonalizazioaren eta konpromisoaren bidez bezeroen leialtasuna lortzeko lehen urratsetako bat da. Zure bezeroaren interesekin bat ez datozen produktuentzako gomendioak emateak bezeroaren eta zure negozioaren arteko deskonektazio sentsazioa sor dezake eta, azken finean, bezero batek izan ditzakeen diru sarrera eta esperientzia orokorrak muga ditzake. 

  Zure datuak erabiliz, etorkizunean zure bezeroek etorkizunean zer produktu eros ditzaketen aurreikuspenak sor ditzakezu. Informazio gehiagorako, ikusi [Produktuen gomendioa iragarpen](predict-product-recommendation.md).

#### <a name="system-administration"></a>Sistemaren administrazioa

- **Kopiatu inguruneak datu iturri mota gehiago onartzen ditu**

  Administratzaileek ingurune konfigurazioak erakunde berdinean ingurune berri batera kopia ditzakete. Ezaugarri honek kopiatze ingurunearen funtzionaltasuna hedatzen du datu baseak oinarritzat hartuta Common Data Service datu-biltegia edo Common Data Model karpeta erabiltzen dira.

## <a name="january-2021-updates"></a>2021eko urtarrilaren eguneratzeak

2021eko urtarrilaren eguneratzeak hainbat funtzio, errendimendu berritze eta akats konponketak biltzen ditu.

#### <a name="extensibility"></a>Hedagarritasuna

- **Funtzionalitate hedatua eta errendimendu hobetua SFTP esportaziorako** Orain irteerako entitate guztiak Customer Insights-etik SFTP ostalari batera esporta ditzakezu. Lehen, esportazioa segmentuko entitateetara mugatzen zen. Gainera, SFTP esportazioaren errendimenduak datu bolumen handiagoa ahalbidetzen du denbora gutxian, zure SFTP ostalariaren errendimenduaren arabera.    
  Informazio gehiagorako, ikusi [SFTP-erako konektorea (aurreargitalpena)](export-sftp.md).  

#### <a name="segments"></a>Segmentuak

- **Ikaskuntza automatikoak iradokitako segmentuak bultzatu ditu metrikak hobetzeko** Segmentuak ezagutzeko eta sortzeko modu berri bat dago. Sistemak dagoeneko jarraitzen ari zaren KPI (neurria) hobetzen lagun dezaketen segmentuak iradokitzeko adimen artifizialeko eredua erabiltzen du. Neurri batean edo beste atributu nagusi batean hautatzen dituzun atributuen eraginaren neurria erakusten dugu. Informazio horrek aukerak aurkezten dituzten segmentu potentzialak aurkitzen laguntzen du.    
  Informazio gehiagorako, ikusi [Iradokitako segmentuak (aurreargitalpena)](suggested-segments.md).

#### <a name="data-unification"></a>Datuak bateratzea

- **Bat-etortzeko esperientzia hobetua** Datuak bateratzeko eremuan, partiduaren esperientzia eguneratu zen. Bat-etortzeen arauak konfiguratu eta ikustea ahalbidetzen du, estatistika zehatzak barne, bat-etortzeak nola funtzionatzen duen azaltzeko. Bat-etortzeen araua desgaitzeko aukerak daude, beraz, jada aktibo ez dago konfigurazioa mantentzen duen bitartean, arrastatu eta askatu bat-etortzeen arauak eta beste.
  Informazio gehiago lortzeko, ikusi [Bat etortzeko entitateak](match-entities.md).

- **Bat etortzearen prozesuko bikoiztea desegiteko irteera entitate gisa eskuragarri dago** Bat-etortzeen prozesuko bikoiztea desegiteko prozesuaren irteera entitate bereizi batean idazten da gehiago aztertzeko. Entitate hau bikoiztuak desegiteko prozesuan eta irabazlearen erregistroan erabilitako eremuek eta irabazle erregistroarekin bat egiten duten ordezko erregistroek osatzen dute.
  Informazio gehiagorako, ikusi [Bikoiztuak desegiteko irteera entitate gisa](match-entities.md#deduplication-output-as-an-entity).

#### <a name="system-administration"></a>Sistemaren administrazioa

- **Partekatu datuak zuzenean Microsoft Dataverse-n** Orain Customer Insights irteera parteka dezakezu Microsoft Dataverse aplikazioaren Microsoft Dataverse Kudeatutako Data Lake erabiliz. Dataverse ingurune bat erlazionatu ostean Customer Insights-ekin, datuak partekatzea gaitzeko aukera duzu.
  Informazio gehiagorako, ikusi [Kudeatu inguruneak](manage-environments.md).




[!INCLUDE[footer-include](../includes/footer-banner.md)]