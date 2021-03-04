---
title: Integratu konpromiso-estatistiketatik datozen webguneak ikusleekin
description: Ekarri bezeroei buruzko web-informazioa konpromisoen estatistiketatik ikusleen estatistiketara.
ms.date: 12/17/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: mukeshpo
manager: shellyha
ms.openlocfilehash: ba1cf6c7e85b8fe90baf34018f1309095573adf1
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267661"
---
# <a name="integrate-web-data-from-engagement-insights-with-audience-insights"></a>Integratu konpromiso-estatistiketatik datozen webguneak ikusleekin

Bezeroek sarritan egiten dituzte eguneroko transakzioak webguneak erabiliz. Konpromisoari buruzko informazioa gaitasuna Dynamics 365 Customer Insights web irtenbidea iturri gisa integratzeko irtenbide erabilgarria da. Transakzio, demografia edo portaeraren inguruko datuez gain, sarean bezeroen profil bateratuetan jarduerak ikus ditzakegu. Profil hau erabil dezakegu hartzaileak aktibatzeko segmentuak, neurriak edo iragarpenak bezalako ikuspegi osagarriak lortzeko.

Artikulu honetan zure bezeroen web jardueren datuak konpromisoen inguruko datuetatik zure audientziaren inguruko ingurunera sartzeko urratsak deskribatzen dira.

Adibide honetan, bezeroen profil bateratuak dituen ingurunea dugu. Profilak inkesten iturriekin, txikizkako salmentekin eta txartel-sistema batekin bateratu ziren. Bezeroen inguruko jarduerak ere erakusten ditu. 

Orain bezero batek gure web propietateak bisitatzen dituen eta haien jarduerak ulertzen dituen jakin nahi dugu. Jardueren artean daude, adibidez, webgune bisitatu edo mezu elektroniko batean jasotako esteka batetik produktuen orriak ikusi.

## <a name="prerequisites"></a>Aurrebaldintzak

Konpromisoen estatistiketako datuak integratzeko, aurrebaldintza batzuk bete behar dira: 

- Integratu konpromisoari buruzko SDK zure webgunearekin. Informazio gehiagorako, ikusi [Hasi web SDK erabiltzen](../engagement-insights/instrument-website.md).
- Web-gertaerak konpromiso-estatistiketatik esportatzeko ADLS Gen 2 biltegiratze-konturako sarbidea behar da, web-gertaeren datuak entzuleen estatistiketara sartzeko erabiliko dena. Informazio gehiago lortzeko, ikusi [Esportatu gertaerak](../engagement-insights/export-events.md).

## <a name="configure-refined-events-in-engagement-insights"></a>Konfiguratu finkatutako gertaerak konpromisoen estatistiketan

Administratzaile batek webgune bat konpromiso estatistiken SDK-rekin sortu ondoren, *oinarrizko gertaerak* erabiltzaile batek web orri bat ikustean edo nonbait klik egitean biltzen dira. Oinarrizko gertaerek xehetasun ugari izan ohi dituzte. Erabilera-kasuaren arabera, datuen azpimultzo bat behar duzu oinarrizko gertaera batean. Engagement xehetasunak sortzea ahalbidetzen dizu *gertaera finduak* zuk hautatutako oinarrizko gertaeraren propietateak bakarrik dituztenak.     

Informazio gehiagorako, ikusi [Sortu eta aldatu gertaera finduak](../engagement-insights/refined-events.md).

Gertaera finduak sortzean kontuan hartzekoak: 

- Eman izen esanguratsua gertaera finduari. Ikusleei buruzko informazioetan jarduera izen gisa erabil daiteke.
- Hautatu gutxienez propietate hauek publikoaren estatistiketan jarduera sortzeko: 
    - Signal.Action.Name: jardueraren xehetasunak adierazten ditu
    - Signal.User.Id: bezeroaren IDarekin mapatzeko erabiltzen da
    - Signal.View.Uri: web-helbide gisa erabiltzen da segmentu edo neurrietarako oinarri gisa
    - Signal.Export.Id: gertaeretarako gako nagusi gisa erabiltzeko <!-- system generated, do we need to list?-->
    - Signal.Timestamp: jardueraren data eta ordua zehazteko

Aukeratu iragazkiak zure erabilera kasurako garrantzitsuak diren gertaera eta orrietan zentratzeko. Adibide honetan, "Posta elektronikoa sustatzeko" ekintzaren izena erabiliko dugu.

## <a name="export-the-refined-web-events"></a>Esportatu findutako web-gertaerak 

Gertaera findua definitu ondoren, gertaeraren datuak esportazio batera konfiguratu behar dituzu Azure Data Lake Storage, hori datu-iturburu gisa ezar daiteke ikusleei buruzko informazioetan kudeatzeko. Esportazioak etengabe gertatzen dira gertaerak web propietatetik ateratzen diren heinean.

Informazio gehiago lortzeko, ikusi [Esportatu gertaerak](../engagement-insights/export-events.md).

## <a name="ingest-event-data-to-audience-insights"></a>Kudeatu gertaeren datuak ikusleen estatistiketara

Orain gertaera findua definitu eta esportazioa konfiguratu ondoren, datuak ikusleei buruzko informazioa sartzeari ekingo diogu. Datu-iturburu berri bat sortu behar duzu datuen eredu arrunten karpetan oinarrituta. Idatzi gertaerak esportatzen dituzun biltegiratze kontuaren xehetasunak. Urtean *default.cdm.json* fitxategia, hautatu irensteko gertaera findua eta entitatea ikusleei buruzko informazioetan sortzeko.

Informazio gehiagorako, ikusi [Konektatu Common Data Model karpeta batera Azure Data Lake kontu bat erabiliz](connect-common-data-model.md)


## <a name="relate-refined-event-data-as-an-activity-of-a-customer-profile"></a>Lotu findutako gertaeren datuak bezeroaren profileko jarduera gisa

Entitatea kudeatzen amaitu ondoren, bezeroaren profilerako jarduera konfigura dezakezu.

Informazio gehiago lortzeko, ikus [Bezeroaren jarduerak](activities.md).

:::image type="content" source="media/web-event-activity.png" alt-text="Jardueren orria Editatu jarduera panela zabalduta eta betetako eremuak.":::

Konfiguratu jarduera berria esleipen honekin: 

- **Gako nagusia:** Signal.Export.Id, ID esklusiboa gertaeren erregistro guztietarako eskuragarri dago konpromiso estatistiketan. Propietate hau automatikoki sortzen da.

- **Denbora-zigilua:** Signal.Timestamp gertaeraren propietatean.

- **Gertaera** Signal.Name, jarraitu nahi duzun gertaeraren izena.

- **Web-helbidea:** Signal.View.Uri gertaera sortu duen orriko uriei erreferentzia eginez.

- **Xehetasunak:** Signal.Action.Name gertaerarekin lotzeko informazioa irudikatzeko. Kasu honetan hautatutako propietateak gertaera mezu elektronikoa sustatzeko dela adierazten du.

- **Jarduera mota:** adibide honetan, WebLog jarduera mota aukeratuko dugu. Aukeraketa hau iragazki aukera erabilgarria da iragarpen modeloak exekutatzeko edo jarduera mota horren arabera segmentuak sortzeko.

- **Konfiguratu erlazioa:** ezarpen garrantzitsu honek jarduera dauden bezeroen profilekin lotzen du. **Signal.User.Id** bildu nahi den SDK-n konfiguratutako identifikatzailea da eta audientzia estatistiketan konfiguratuta dauden beste datu iturri batzuetako erabiltzaile IDarekin lotzen da. Adibide honetan, Signal.User.Id eta RetailCustomers-en arteko harremana konfiguratzen dugu: CustomerRetailId, hau da, datuak bateratzeko prozesuaren mapa urratsean zehaztu den gako nagusia.


Jarduerak prozesatu ondoren, bezeroen erregistroak berrikus ditzakezu eta bezeroaren txartela ireki dezakezu konpromisoari buruzko jarduerak denboran ikusteko. 

> [!TIP]
> Konpromisoari buruzko informazioa duen bezeroaren IDa aurkitzeko, joan hona **Entitateak** eta aurreikusi UnifiedActivity entitatearen datuak. ActivityTypeDisplay = WebLog-ek goiko adibidean konfiguratutako konpromisoen inguruko informazioa du. Kopiatu bezeroaren IDa erregistro horietako baten eta ID horretan **Bezeroak** orria.

## <a name="next-steps"></a>Hurrengo urratsak

Orain [segmentuak](segments.md), [neurriak](measures.md) eta [iragarpenak](predictions.md) sor ditzakezu bezeroekin konexio esanguratsua egiteko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]