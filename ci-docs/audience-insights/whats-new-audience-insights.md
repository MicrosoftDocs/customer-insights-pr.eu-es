---
title: Eginbide berriak eta datozenak
description: Ezaugarri berriei, hobekuntzei eta akatsak konpontzeko ezaugarriei buruzko informazioa.
ms.date: 03/02/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: midevane
manager: shellyha
ms.openlocfilehash: 667a984f1a2287456f4e6324eafe628fba957bf5
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8232642"
---
# <a name="whats-new-in-the-audience-insights-capability-of-dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights hartzaileen xehetasunei buruzko zerbitzuaren ezaugarri berriak



Gogotsu gaude gure eguneratze berrienak iragartzeko! Artikulu honek aurrebista publikoko eginbideak, aurrebistako funtzioak, erabilgarritasun orokorreko hobekuntzak, eta eginbideen eguneratzeak. Epe luzerako eginbide planak ikusteko, begiratu [Dynamics 365 eta Power Platform kaleratzeko planak](/dynamics365/release-plans/).

Eguneratzeak eskualdeen arabera banatzen ditugu. Beraz, eskualde batzuek beste batzuen aurretik ezaugarriak ikus ditzakete. Modu ezberdinean zehaztu ezean, ez duzu inolako neurririk egin behar eta aplikazioa automatikoki eguneratuko dugu inolako denborarik gabe.

> [!TIP]
> Bidali eta bozkatzeko eginbideak eskaerak eta produktuaren iradokizunak, joan [Dynamics 365 aplikazioaren ideiak atarira](https://experience.dynamics.com/ideas/categories/?forum=79a8c474-4e35-e911-a971-000d3a4f3343&forumName=Dynamics%20365%20Customer%20Insights).


## <a name="january-2022-updates"></a>2022ko urtarrileko eguneraketak

2022ko urtarrileko eguneratzeek ezaugarri berriak, errendimenduaren hobekuntzak eta akatsen konponketak barne hartzen dituzte.

### <a name="sentiment-analysis-of-your-customers-feedback"></a>Zure bezeroen iritzien analisia

Customer Insights-ek AI-k bultzatutako eginbide berri bat eskaintzen du bezeroen sentimendua sintetizatzeko eta negozio-alderdi zehatzak identifikatzeko, hobekuntzak hobetzeko aukera gisa. Zure bezeroen idatzizko iritziak aztertuz gero, informazio zehatzak lor ditzakezu kostu baxuan. Sentimenduen analisia Lengoaia Naturaleko Prozesamenduaren (NLP) ereduek bultzatuta, bezeroaren ID bakoitzeko bi informazio eratorri sortzen dituztenak. Sentimendu puntuazioa (-5etik 5era) eta negozio-alderdi aplikagarrien zerrenda. 

Informazio gehiagorako, ikus [Aztertu sentimendua bezeroen iritzietan (Aurrebista)](sentiment-analysis.md).


## <a name="december-2021-updates"></a>2021eko abenduko eguneraketak

2021eko abenduko eguneratzeek ezaugarri berriak, errendimendu-berritzeak eta akatsen konponketak barne hartzen dituzte.

### <a name="forward-customer-insights-logs-to-azure-monitor"></a>Bidali Customer Insights erregistroak Azure Monitorera

Customer Insights-ek integrazio zuzena eskaintzen du Azure Monitor-ekin. Ezaugarri honek auditoretza-gertaerak eta operazio-gertaerak barne hartzen ditu. Azure Monitor baliabideen erregistroek erregistroak kontrolatu eta Azure Storagera, Azure Log Analytics-era bidaltzeko edo Azure Event Hubs-era igortzeko aukera ematen dute.

Informazio gehiagorako, ikus [Saioa birbidaltzea Dynamics 365 Customer Insights Azure Monitor-ekin (Aurrebista)](diagnostics.md).

### <a name="enrich-customer-profiles-with-engagement-data"></a>Aberastu bezeroen profilak konpromiso datuekin

Erabili datuak Microsoft Office 365 zure bezero-kontuaren profilak engaiamenduei buruzko informazioekin aberasteko Office 365 aplikazioak. Konpromiso-datuak posta elektronikoa eta bilera-jarduerak dira, kontu mailan batzen direnak. Adibidez, negozio-kontu bateko mezu elektronikoen kopurua edo kontuarekin izandako bilera-kopurua. Ez da banakako erabiltzaileei buruzko daturik partekatzen. Aberaste hau eskualde hauetan dago eskuragarri: Erresuma Batua, Europa, Ipar Amerika.

Informazio gehiagorako, ikus [Aberastu bezeroen profilak konpromiso datuekin (Aurrebista)](enrichment-office.md).

### <a name="advanced-data-unification-features"></a>Datuak bateratzeko eginbide aurreratuak

#### <a name="enable-conflict-resolution-policies-at-the-individual-attribute-level"></a>Gaitu gatazkak konpontzeko politikak banakako atributu mailan

Entitate baten barruan bezeroen erregistroak desbikoitzean, baliteke erregistro osoa irabazle gisa aukeratu behar izatea nahi ez izatea. Orain, hainbat erregistrotako eremu onenak batzeko aukera ematen dizugu, atributu bakoitzaren arauetan oinarrituta. Adibidez, posta elektroniko berriena ETA helbiderik osatuena erregistro ezberdinetatik gordetzea aukera dezakezu. 

Orain atributu indibidualentzako bateratze-arau bereiziak defini ditzakezu erregistroak entitate bakarrean desbikoiztu eta batzen dituzun bitartean. Aurretik, bateratze-arau bakarra hautatzen uzten dizugu (erregistroak berritasun-datuen osotasunean oinarrituta mantenduz) eta arau hori erregistro-mailan aplikatzen zen atributu guztietan. Hori ez da aproposa gorde nahi dituzun datu batzuk A erregistroan aurkitzen direnean eta beste datu on batzuk B erregistroan aurkitzen direnean.

Informazio gehiagorako, ikusi [Definitu bikoiztuak kentzea bat datorren entitate batean](match-entities.md#define-deduplication-on-a-match-entity).

#### <a name="custom-rules-for-matching"></a>Lotzeko arau pertsonalizatuak

Batzuetan, arau orokorren salbuespen bat zehaztu behar duzu erregistroak EZ bat etortzeko. Hau gerta daiteke pertsona askok informazio nahikoa partekatzen dutenean, sistemak banako bakar gisa parekatuko lituzke. Adibidez, abizen berdina duten bikiak, hiri berean bizi direnak eta jaiotze data partekatzen dutenak.

Salbuespenek ziurtatzen dute datuen bateratze okerra bateratze-arauetan bideratu daitekeela. Arau bati hainbat salbuespen gehi ditzakezu.

Informazio gehiagorako, ikus [Gehitu salbuespenak arau bati](match-entities.md#add-exceptions-to-a-rule).

#### <a name="provide-additional-conflict-resolution-policies-and-enable-grouping-of-attributes"></a>Eman gatazkak konpontzeko politika osagarriak eta gaitu atributuak taldekatzea

Ezaugarri honek eremu talde bat unitate bakar gisa tratatzeko aukera ematen dizu. Adibidez, gure erregistroek Helbidea1, Helbidea2, Hiria, Estatua eta Zip eremuak badituzu. Seguruenik, ez dugu nahi beste erregistro baten Helbide2 batean batu, gure datuak osatuagoak izango liratekeela pentsatuz.

Orain erlazionatutako eremuen talde bat konbina dezakezu eta bateratze-politika bakarra aplika dezakezu taldeari. 

Informazio gehiagorako, ikus [Konbinatu eremu talde bat](merge-entities.md#combine-a-group-of-fields).


## <a name="november-2021-updates"></a>2021eko azaroko eguneraketak

2021eko azaroko eguneratzeek ezaugarri berriak, errendimendu-berritzeak eta akatsen konponketak barne hartzen dituzte.

### <a name="segment-membership-now-available-in-dataverse"></a>Segmentuko kidetza orain eskuragarri dago hemen Dataverse

Bezeroen profiletarako kideen segmentuari buruzko informazioa eskuragarri dago orain Dataverse bezeroen profil eta ikuspegiekin batera. Dynamics 365 ekintza-aplikazioek eta ereduetan oinarritutako aplikazioek datu hauek erabil ditzakete bezero jakin baten segmentu-kidetasunaren xehetasunak bilatzeko.

### <a name="activities-support-contact-level-details-for-business-accounts"></a>Jarduerek kontaktu-mailako xehetasunak onartzen dituzte enpresa-kontuetarako

Orain, zure negozio-kontuaren jarduera-eremuetan kontaktuen jarduerak konfiguratu, bistaratu eta iragazi ditzakezu kontuko kontaktuek jarduera zehatzetan parte hartu duten hobeto ulertzeko.

## <a name="october-2021-updates"></a>2021eko urriko eguneraketak

2021eko urrian egindako eguneratzeek ezaugarri berriak, errendimenduaren hobekuntzak eta akatsen konponketak dituzte.

### <a name="b-to-b"></a>B-tik-B

2021eko urrian hasita, negozio-kontuekin eta haiei lotutako kontaktuekin lan egin dezakezu Customer Insights-en. Aurretik, aplikazioa kontsumitzaile indibidualentzat egokituta zegoen. Hainbat ezaugarri-eremu eguneratu ziren B-to-B eszenatokiak onartzeko ingurune-mota berri baten gainean. Onartutako B-to-B eginbideei buruzko ikuspegi orokorra lortzeko, ikus [Lan egin negozio-kontuekin ikusleen estatistiketan](work-with-business-accounts.md).

Ondorengo ataletan negozio-kontuei eta kontsumitzaile indibidualei laguntzeko egokitu ziren funtsezko arlo batzuk nabarmentzen dira.

#### <a name="export-segments-based-on-business-accounts"></a>Esportatu segmentuak negozio-kontuetan oinarrituta

Segmentu-esportazio guztiak ikusleen informazioetan eskuragarri daude negozio-kontuen testuinguruan. Segmentu esportazio gehienek konfigurazio gehigarria behar dute eta [aurreikusitako harremanetarako informazioa](segment-builder.md#create-a-new-segment) azpiko segmentuetan negozio-kontuetarako balio izatea. Informazio gehiagorako, ikus [Esportatu segmentuak](export-destinations.md#export-segments).

#### <a name="use-the-linkedin-ads-export-with-business-accounts"></a>Erabili LinkedIn Ads esportazioa negozio-kontuekin

LinkedIn Ads esportazioa eskuragarri dago orain harremanetarako eta enpresentzako bideratzeko negozio-kontuen testuinguruan. Konpainiaren xedea LinkedIn esportazioaren ardatz nagusi gisa hautatzean, negozio-kontuetan eraikitako segmentuak esportatu ditzakezu harremanetarako informazioa proiektatu beharrik gabe. Informazio gehiago lortzeko, joan honi buruzko dokumentuetara [LinkedIn Ads esportatzea](export-linkedin-ads.md) eta arteko aldea [harremanetarako bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/contact-targeting) eta [enpresaren bideratzea](https://business.linkedin.com/marketing-solutions/ad-targeting/account-targeting). 

#### <a name="create-measures-based-on-business-accounts-and-their-hierarchy"></a>Enpresa-kontuetan eta haien hierarkian oinarritutako neurriak sortzea

Neurri-sortzaileak negozio-kontuen inguruan neurriak sortzeko eta hierarkiaren informazioa erabiltzeko aukera ematen dizu. Hierarkiaren informazioa kontu batean eta harekin lotutako azpikontu guztietan neurrien kalkulua biltzeko erabiltzen da. Adibidez, hierarkiak identifikatutako negozio-kontu talde bakoitzeko diru-sarrera osoa bezalako neurriak sor ditzakezu. Informazio gehiagorako, ikusi [Neurriak zehaztea eta kudeatzea](measures.md).

#### <a name="create-segments-based-on-business-accounts-and-their-hierarchy"></a>Sortu segmentuak negozio-kontuetan eta haien hierarkian oinarrituta

Segmentu-sortzaileak aukera ematen du segmentu bateko kontu bakoitzaren kontaktu-informazioa barne hartzen duten negozio-kontuen segmentuak sortzeko. Kontuaren hierarkia konfiguratuta baduzu, kontuaren hierarkia informazioa erabil dezakezu segmentua sortzeko. Informazio gehiagorako, ikus [Sortu segmentu berri bat](segment-builder.md#create-a-new-segment).

#### <a name="retain-your-business-accounts-with-deep-insights-to-their-churn-tendency"></a>Eutsi zure negozio-kontuak beren joerari buruzko ikuspegi sakonekin

Bezeroen txanda iragarpen ereduak negozio-kontuak ere onartzen ditu orain. Kontu baterako ez ezik, kontu baten eta zuri erosten dizuten produktu edo zerbitzu kategoria baten konbinaziorako ere ebaluatu dezakezu. Gehigarri honek ulertzen laguntzen dizu kontu batek orokorrean zuri erosteari uztea edo ondasun edo zerbitzuen kategoria jakin baterako aukera gehiago duen ulertzen. AI eredu hau gehiago erabiltzen laguntzeko, kontu bat litekeena den arrazoiak ere zerrendatzen ditu. Informazio gehiagorako, ikus [Transaction churn iragarpen (aurrebista)](predict-transactional-churn.md).

#### <a name="see-contacts-of-a-business-account-in-customer-view"></a>Ikusi negozio-kontu bateko kontaktuak Bezeroaren ikuspegian

Enpresa-kontuak erlazionatutako kontuekin mapatzen badira, Customer Insights aplikazioak erlazionatutako kontaktu hauek erakusten ditu bezeroaren xehetasunen ikuspegiaren zati gisa. Informazio gehiagorako, ikus [Bezeroen profilak](customer-profiles.md).


## <a name="september-2021-updates"></a>2021eko iraileko eguneratzea

2021eko iraileko eguneratzeek ezaugarri berriak, errendimendu bertsio berritzea eta akatsak konpondu dituzte.

### <a name="activities"></a>Ekintzak

- **Jardueren kronologia hobekuntzak** Jardueren kronologiarako iragazkiak bezeroen profiletan zabaldu ditugu. Gainera, iragazki-pan berria erabil dezakezu jarduera motaren eta dataren arabera iragazteko. Datak baldintza desberdinak erabiliz iragazi daitezke. Informazio gehiagorako, ikus [Ikusi jarduera profilak bezeroen profiletan](activities.md#view-activity-timelines-on-customer-profiles).

### <a name="relationships"></a>Erlazioak

- **Hop anitzeko harremanen laguntza** Saltoki anitzeko harremanak erabiltzea jarduerak konfiguratzerakoan eta entitateen arteko harremanak definitzerakoan. Lupo anitzeko harremanek bitarteko entitate bat erabiltzen dute bi entitate konektatzeko. Jarduera bat konfiguratzerakoan, hop anitzeko erlazioa erabil dezakezu zure jarduera entitatea bitarteko entitate batekin eta gero bezero entitate batekin konektatzeko. Salto anitzeko harremanak bide anitzeko harremanekin konbinatu ditzakezu. Informazio gehiagorako, ikus [Hop anitzeko harremana](relationships.md#multi-hop-relationship).

- **Bide-izena anitzeko harremanen laguntza** Saltoki anitzeko harremanak erabiltzea jarduerak konfiguratzerakoan eta entitateen arteko harremanak definitzerakoan. Bide anitzeko harremanek iturburu-entitate bat entitate batekin baino gehiagorekin erlazionatzen dute. Jarduera bat konfiguratzerakoan, hop anitzeko erlazioa erabil dezakezu zure jarduera bat baino gehiago bezero entitate batekin konektatzeko. Bide anitzeko harremanak bide anitzeko harremanekin konbinatu ditzakezu. Informazio gehiagorako, ikus [Bide anitzeko harremana](relationships.md#multi-path-relationship).

## <a name="august-2021-updates"></a>2021eko abuztuko eguneratzeak

2021eko uztaileko eta abuztuko eguneratzeek eginbide berriak, errendimenduaren bertsio-berritzeak eta akatsen konponketak dituzte.

### <a name="extensibility"></a>Hedagarritasuna

- **Esportatu segmentuak Klaviyo-ra** Zabaldu egin ditugu [esportazio-helburuak, Klaviyo sartzeko](export-klaviyo.md). Orain segmentuak esporta ditzakezu kanpainak sortzeko, posta elektroniko bidezko marketina egiteko eta bezero talde zehatzak erabiltzeko Klaviyo-n. 


## <a name="june-2021-updates"></a>2021ko ekaineko eguneratzeak

2021ko ekaineko eguneratzeak hainbat funtzio, errendimendu berritze eta akats konponketak biltzen ditu.

### <a name="data-ingestion"></a>Datu-horniketa

- **Datuak bateratzeko aurrerapenen eguneratzeak hobetu dira** Orain eguneraketaren egoera dinamiko hobetu eta xeheagoak ikus ditzakezu [datuak bateratzeko prozesua](data-unification.md) urratsetan. Ezaugarri honi esker aurrerapen zehatzen jarraipena egin dezakezu prozesuaren fluxua ulertzeko eta urratsak arreta behar izanez gero neurriak hartzeko.

### <a name="extensibility"></a>Hedagarritasuna

- **Esportatu segmentuak eta bestelako datuak Salesforce Marketing Cloud-era** Esportatzeko helmugak zabaldu ditugu [Salesforce Marketing Cloud](export-salesforce.md) sartzeko. Segmentuak eta beste datu mota batzuk esportatu ditzakezu Salesforce Marketing Cloud-era markako SFTP esportazio baten bidez. Datuen inportazioa Salesforce-n erabat automatiza daiteke eta marketin kanpaina eraginkorragoak sortzeko erabil daiteke.  
 
- **Esportatu segmentuak ActiveCampaign-era** Esportatzeko helmugak zabaldu ditugu [Active Campaign](export-active-campaign.md) sartzeko. Kanpainak sortzeko segmentuak esportatzeko, exekutatu posta elektroniko bidezko marketin-mezuak eta egin lan ActiveCampaign-en bezero talde jakinekin.
 
- **Esportatu segmentuak Sendinblue-era** Esportatzeko helmugak zabaldu ditugu [Sendinblue](export-sendinblue.md) sartzeko. Kanpainak sortzeko segmentuak esportatzeko, exekutatu posta elektroniko bidezko marketin-mezuak eta egin lan Sendinblue-n bezero talde jakinekin.
 
### <a name="ux-updates"></a>UX eguneratzeak 

- **Bezeroen orri berria eta hobetua eta profilaren xehetasunen orria** Bezeroen orria eta profilaren xehetasun orrialdeak berriro diseinatu ditugu erabiltzaileen esperientzia hobetzeko eta errendimendu hobea lortzeko. Aldaketa horiei esker, bezeroak ikusi, ordenatu, bilatu eta iragazi ditzakezu. Iragazkiak URLan irudikatzen dira bilaketa-emaitzak beste erabiltzaileekin batera partekatzeko. Bilaketaren emaitzak segmentu gisa ere gorde daitezke.    
  Bezeroen profilen xehetasunen orrialdeak datuak azpiatal desberdinetan biltzen ditu, hala nola datu demografikoak, IDak eta profileko beste atributuak, irakurgarritasuna hobetzeko. Profilaren xehetasunen orrian beste atal batzuk interaktiboagoak dira. Adibidez jardueren atalak iragazteko eta ordenatzeko aukera ematen du.


## <a name="may-2021-updates"></a>2021eko maiatzeko eguneratzeak

2021eko maiatzeko eguneratzeen artean hainbat funtzio, errendimendu bertsio berritzea eta akatsak konpondu dira.

### <a name="data-ingestion"></a>Datu-horniketa

- **Ikusi edo aldatu metadatuak edo entitatearen definizioa Azure Data Lake Storage-ko datuak eransterakoan** Orain metadatuak edo entitateen definizioa ikus eta editatu ditzakezu hartzaileen xehetasunetan, Azure Data Lake Storage-ko Common Data Model karpetako datuak eranstean. Gaitasun honek denbora errealeko iritzia, modeloaren balioztapena eta erroreen egiaztapena eskaintzen ditu. model.json eta manifest.json editatzeko aukera ematen du.

### <a name="extensibility"></a>Hedagarritasuna

- **Segmentuen esportazioa, antolaketa pertsonalizatua eta bikoizketak hobetu dira** Orain [segmentu zehatz baten esportazio guztiak ikus ditzakezu](export-destinations.md#view-exports-and-export-details) zerrenda batean. Ikuspegi berri honek segmentu zehatz bat nola erabiltzen den kudeatzen eta lehendik daudenak egokitzen edo esportazio berriak sortzen laguntzen du.    
  Banakako esportazioetarako edo hainbat esportaziorako [freskatze ordutegi pertsonalizatuak defini ditzakezu](export-destinations.md#schedule-and-run-exports) aldi berean. Orain arte, esportazio guztiak sistema freskatzen ziren guztietan egiten ziren.    
  Esportazio berri bat hutsetik sortu beharrean, lehendik dagoen batean oinarrituta has zaitezke denbora pixka bat aurrezteko.

- **Esportatu segmentuak Microsoft Advertising-era** Esportaziorako helmugak zabaldu ditugu Microsoft Advertising sartzeko. Sortu bezeroekin bat datozen hartzaileak Microsoft Advertising-en bezero-profil bateratuaren datuekin eta erabili hartzaile horiek iragarki-kanpainetarako. Informazio gehiagorako, ikus [Esportatu segmentuak Microsoft Advertising-era](export-microsoft-advertising.md).

- **Esportatu segmentuak LinkedIn Ads-era** Esportazio-helmugak zabaldu ditugu LinkedIn Ads gehitzeko eta harremanetarako bideratzea eta enpresaren bideratzea LinkedIn bidez desblokeatzeko aukera ematen dizugu, zure bezeroaren profileko datuak bateratuta esportatuz. Informazio gehiagorako, ikus [Esportatu segmentuak LinkedIn Ads-era](export-linkedin-ads.md).


- **Esportatu segmentuak Omnisend-era** Esportaziorako helmugak Omnisend barne zabaldu ditugu. Kanpainak sortzeko, posta elektroniko bidezko marketin-mezuak kudeatzeko eta bezero talde zehatzei etekinik handiena ateratzeko Omnisend bidez, erabili hartzaileen xehetasunetan sortutako segmentuak. Informazio gehiagorako, ikus [Esportatu segmentuak Omnisend-era](export-omnisend.md)

### <a name="predictions"></a>Iragarpenak

- **Sarrerako datuak erabiltzeko txostena** Sarrerako datuen erabilgarritasun txostenak erabiltzeko prest dauden iragarpenek sor ditzaketen akats eta abisuen ikuspegi bateratua eskaintzen du. Ereduaren errendimendua hobetzeko gomendioak ere ematen ditu.    
  Txostena eredu batek bere prestakuntza prozesua amaitu ondoren eskuragarri dago. Eredu bakoitzerako bereizita sortu da, ondo osatu den edo ez kontuan hartu gabe.
  Gaur egun, eginbide hau transakzioen galera-tasaren ereduan bakarrik dago erabilgarri. Informazio gehiagorako, ikus [Sarrerako datuen erabilgarritasun txostena](manage-predictions.md#input-data-usability-report).

### <a name="relationships"></a>Erlazioak

- **Harreman bistaratzailea** Harremanen bistaratzailearen ikuspegiak entitateen eta haien kardinaltasunaren artean dauden harreman guztiak ikusteko aukera ematen du. Harremanak taldeka antolatzen dira orain: erabiltzaileak sortua, sistema eta heredatutako harremanak. Ikuspegia irudi gisa ere esporta dezakezu. Informazio gehiago lortzeko, ikusi [ikusi erlazioak](relationships.md#view-relationships). 

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

- **Esportatu segmentuak RollWorks-era** Esportaziorako helmugak RollWorks barne zabaldu ditugu. Orain Customer Insights-eko segmentuak RollWorks-eko hartzileetara esporta ditzakezu eta zure B-to-B publizitatearen oinarri gisa erabil ditzakezu.    
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

  Administratzaileek ingurune konfigurazioak erakunde berdinean ingurune berri batera kopia ditzakete. Ezaugarri honek kopiatze ingurunearen funtzionaltasuna hedatzen du Microsoft Dataverse-k kudeatutako datu-biltegi batean oinarritutako datu-iturburuak edo Common Data Model karpeta erabiltzen direnean.

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