---
title: Eginbide berriak eta datozenak
description: Ezaugarri berriei, hobekuntzei eta akatsak konpontzeko ezaugarriei buruzko informazioa.
ms.date: 04/05/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: skumm
manager: shellyha
ms.openlocfilehash: 2f081306271a170cf3e250fc1a193cedb70aeec6
ms.sourcegitcommit: 0363559a1af7ae16da2a96b09d6a4a8a53a8cbb8
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547657"
---
# <a name="whats-new-in-the-audience-insights-capability-of-dynamics-365-customer-insights"></a>Dynamics 365 Customer Insights hartzaileen xehetasunei buruzko zerbitzuaren ezaugarri berriak

Gogotsu gaude gure eguneratze berrienak iragartzeko! Artikulu honek aurrebista publikoko eginbideak, aurrebistako funtzioak, erabilgarritasun orokorreko hobekuntzak, eta eginbideen eguneratzeak. Epe luzerako eginbide planak ikusteko, begiratu [Dynamics 365 eta Power Platform kaleratzeko planak](/dynamics365/release-plans/).

Eguneratzeak eskualdeen arabera banatzen ditugu. Beraz, eskualde batzuek beste batzuen aurretik ezaugarriak ikus ditzakete. Modu ezberdinean zehaztu ezean, ez duzu inolako neurririk egin behar eta aplikazioa automatikoki eguneratuko dugu inolako denborarik gabe.

> [!TIP]
> Bidali eta bozkatzeko eginbideak eskaerak eta produktuaren iradokizunak, joan [Dynamics 365 aplikazioaren ideiak atarira](https://experience.dynamics.com/ideas/categories/?forum=79a8c474-4e35-e911-a971-000d3a4f3343&forumName=Dynamics%20365%20Customer%20Insights).


## <a name="march-2022-updates"></a>2022ko martxoko eguneraketak

2022ko martxoko eguneratzeek ezaugarri berriak, errendimendu-berritzeak eta akatsen konponketak barne hartzen dituzte.

### <a name="liveramp-abilitec-enrichment-preview"></a>LiveRamp AbiliTec aberastea (aurrebista)

LiveRamp-ek bezeroen datuen identitatearen ebazpena eta finkatzea eskaintzen du. Zure bezeroen datuetan identifikatzaile pertsonalak mapa ditzakezu AbiliTec identitate grafikoarekin eta AbiliTec IDak jaso ditzakezu. Orduan ID hauek erabil ditzakezu zure bezeroen datuak hobeto bateratzeko.

Informazio gehiagorako, ikus [Aberastu bezeroen profilak LiveRamp-eko identitate-datuekin (aurrebista)](enrichment-liveramp.md).

### <a name="organize-segments-and-measures-with-tags-and-filters"></a>Antolatu segmentuak eta neurriak etiketa eta iragazkiekin
Zure erakundeak segmentu edo neurri asko mantentzen baditu, egokia aurkitzea zaila izan daiteke batzuetan. Ezaugarri berri honek etiketak eta zutabeak erabiliz zerrendak antolatzeko aukera ematen dizu. Datuak azkar eta erraz aurkitzen eta ikuspegiak pertsonalizatzen laguntzen du.

Informazio gehiagorako, ikus [Etiketa eta zutabeekin lan egin](work-with-tags-columns.md).

### <a name="enable-data-sharing-with-dataverse-when-using-your-own-storage-account"></a>Gaitu honekin datuak partekatzea Dataverse zure biltegiratze kontua erabiltzen duzunean

Zure inguruneak erabiltzen badu Azure Data Lake Storage Customer Insights datuak gordetzeko, datuak partekatzeko Microsoft Dataverse konfigurazio gehigarri bat behar du.
Lehenago, datuen partekatzea soilik gaitu dezakezu Dataverse zure datuak gure kudeatutako datu-lakuan gorde zirenean. 

Informazio gehiagorako, ikus [Gaitu honekin datuak partekatzea Dataverse zuretik Azure Data Lake Storage (Aurrebista)](manage-environments.md#enable-data-sharing-with-dataverse-from-your-own-azure-data-lake-storage-preview).

### <a name="new-export-destinations-iterable-and-braze"></a>Esportazio-helmuga berriak: Iterable eta Braze

Esportazio-helmugetako gure ekosistema zabaltzen jarraitzen dugu konexio berriekin. Orain segmentuak esporta ditzakezu Iterable eta Braze-ra haien aktibazio zerbitzuak erabiltzeko.

Informazio gehiagorako, ikus [Esportatu segmentuak Iterablera (aurrebista)](export-iterable.md) eta [Esportatu segmentuak Braze-ra (aurrebista)](export-braze.md).

### <a name="improvements-to-marketo-and-google-ads-export"></a>Marketo eta Google Ads esportatzeko hobekuntzak

Konektatutako zerbitzuetan APIak aldatzeak konektoreen eguneraketak ekartzen ditu fidagarri eta arin exekutatzeko. Marketo eta Google Ads zerbitzuetara esportatzeko eguneratze batzuk kaleratu ditugu:

- Google Ads: Google Ads esportazio-konektorearen bertsio berriak autentifikazio-esperientzia errazten du eta orain Google Ads-eko audientzia berriak automatikoki sortzeko aukera ematen dizu. 
- Marketo: Marketo esportazio-konektorearen bertsio berriak Marketo IDrako euskarria eskaintzen du, eta horri esker, datuak bikoiztu, lehendik dauden erregistroak eguneratu eta Marketo-n erregistro berriak sortu ditzakezu. 


## <a name="february-2022-updates"></a>2022ko otsaileko eguneraketak

2022ko otsaileko eguneratzeek ezaugarri berriak, errendimenduaren hobekuntzak eta akatsen konponketak barne hartzen dituzte.

### <a name="general-availability-for-prediction-models"></a>Iragarpen ereduen erabilgarritasun orokorra

Kutxaz kanpoko iragarpen ereduak, barne **harpidetza txanda**, **txandaka**, eta **bezeroaren bizitzako balioa (CLV)** orokorrean eskuragarri egongo da Customer Insights-en zati gisa. 

Informazio gehiagorako, ikus [Iragarpenen ikuspegi orokorra](predictions-overview.md).

### <a name="new-data-source-integration-with-azure-synapse-analytics-preview"></a>datu-iturburu berria: bateratzea Azure Synapse Analytics (Aurrebista)

Azure Synapse Analytics datu biltegietan eta datu handien sistemetan informaziorako denbora azkartzen duen enpresa analitika zerbitzu bat da.

Dagoeneko erabiltzen duten erakundeak Azure Synapse Analytics Datu horiek Customer Insights-en har ditzake. 

Informazio gehiagorako, ikus [Konektatu bat Azure Synapse datu-iturburu (Aurrebista)](connect-synapse.md).

### <a name="liveramp-enrichment-preview"></a>LiveRamp aberastea (aurrebista)

LiveRamp-ek bezeroen datuen identitatearen ebazpena eta finkatzea eskaintzen du. Zure bezeroen datuetan identifikatzaile pertsonalak mapa ditzakezu AbiliTec identitate grafikoarekin eta AbiliTec IDak jaso ditzakezu. Orduan ID hauek erabil ditzakezu zure bezeroen datuak hobeto bateratzeko.

Informazio gehiagorako, ikus [Aberastu bezeroen profilak LiveRamp-eko identitate-datuekin (aurrebista)](enrichment-liveramp.md).

### <a name="enrichment-for-data-sources-preview"></a>Datu-iturburuetarako aberastea (aurrebista)

Erabili Microsoft eta beste bazkide batzuen iturrietako datuak zure bezeroen datuak aberasteko datuak bateratu aurretik. datu-iturburu aberasteek datuen osotasun eta kalitate handiagoak lortzen laguntzen dute, eta horrek emaitza hobeak lortzen lagunduko dizu datuak bateratu ondoren.

Informazio gehiagorako, ikus [Datu-iturburuetarako aberastea (aurrebista)](data-sources-enrichment.md).

### <a name="change-owner-of-environment"></a>Aldatu ingurunearen jabea

Hainbat erabiltzailek Customer Insights-en administratzaile-baimenak izan ditzaketen arren, erabiltzaile bakarra da ingurune baten jabea. Esperientzia hobetu batek ingurune baten jabeak alda ditzakezu eta jabe ohi batek erakundea utziz gero jabetza erreklamatzeko aukera ematen dizu. 

Informazio gehiagorako, ikus [Ingurune baten jabea aldatu](manage-environments.md#change-the-owner-of-an-environment).

### <a name="data-preparation-process-lists-corruption-reason-for-corrupted-records"></a>Datuak prestatzeko prozesuak hondatutako erregistroen ustelkeria arrazoiak zerrendatzen ditu

Datuak prestatzeak datu hondatuak dituzten eremu guztien ustelkeriaren arrazoia erakusten du. Informazioa erregistro indibidualaren mailan ematen da erraz identifikatzeko. 

Informazio gehiagorako, ikus [Datu iturri hondatuak](entities.md#corrupted-data-sources).

### <a name="end-of-preview-for-reporting-features-in-the-engagement-insights-capability"></a>Engaiamenduaren estatistiken gaitasunean txostenak egiteko eginbideen aurrebistaren amaiera

The Dynamics 365 Customer Insights konpromisoari buruzko informazio-gaitasunaren aurrebista 2022ko otsailaren 15ean amaitu zen.  
Aldaketa honek esan nahi du Customer Insights-en probako esperientziak ez duela inbutuak sortzeko gaitasunik ezta txostenak egiteko beste funtzionalitaterik ere.

Beste hainbat ezaugarri arakatu eta ebaluatzera gonbidatzen zaitugu [Bezeroen ikuspegiak](https://dynamics.microsoft.com/ai/customer-insights/), Microsoft bezeroen datuen plataforma (CDP).    
 
Trantsizio-aldi baterako, lehendik dauden aurrebista-parte-hartzaileek aurrebista-gaitasun eta funtzionalitate batzuetarako sarbidea dute oraindik:

- Lortu webguneak edo mugikorreko aplikazioak hornitzeko kodea 
- Ikusi gertaerak eta gertaeren propietateak 
- Hobetu profil bateratuak irensten eta findutako gertaerekin, bezeroen datuen balio osoaz baliatzeko
  
Trantsizio-aldian, harrapatutako gertaerak konektatutako Data Lake-ra igortzen dira oraindik. Funtzionalitate hau desaktibatuta dagoenean, interakzio-estatistiken eta ikusleen estatistiken arteko datu-partekatzea geldituko da eta ez da gertaera berririk bidaliko konektatutako biltegiratze.
Jarri harremanetan zure Microsoft kontuko taldearekin zuzenean gaitasunen aurrebistaren amaierari buruzko galderarik baduzu. Zure Kontu-taldeak datozen abiarazteen berri emango dizu. 

## <a name="january-2022-updates"></a>2022ko urtarrileko eguneraketak

2022ko urtarrileko eguneratzeek ezaugarri berriak, errendimenduaren hobekuntzak eta akatsen konponketak barne hartzen dituzte.

### <a name="sentiment-analysis-of-your-customers-feedback"></a>Zure bezeroen iritzien analisia

Customer Insights-ek AI-k bultzatutako eginbide berri bat eskaintzen du bezeroen sentimendua sintetizatzeko eta negozio-alderdi zehatzak identifikatzeko, hobekuntzak hobetzeko aukera gisa. Zure bezeroen idatzizko iritziak aztertuz gero, informazio zehatzak lor ditzakezu kostu baxuan. Sentimenduen analisia Lengoaia Naturaleko Prozesamenduaren (NLP) ereduek bultzatuta, bezeroaren ID bakoitzeko bi informazio eratorri sortzen dituztenak. Sentimendu puntuazioa (-5etik 5era) eta negozio-alderdi aplikagarrien zerrenda. 

Informazio gehiagorako, ikus [Aztertu sentimendua bezeroen iritzietan (Aurrebista)](sentiment-analysis.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]