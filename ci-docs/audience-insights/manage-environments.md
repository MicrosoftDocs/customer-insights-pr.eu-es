---
title: Sortu eta kudeatu inguruneak
description: Ikasi zerbitzuan izena ematen eta inguruneak kudeatzen.
ms.date: 11/10/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
ms.reviewer: nimagen
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 010336445d0825a7ff82d1b7a65702fc12245788
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644118"
---
# <a name="manage-environments"></a>Kudeatu inguruneak

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Artikulu honetan erakunde berri bat nola sortu eta ingurune bat nola hornitu azaltzen da.

## <a name="sign-up-and-create-an-organization"></a>Eman izena eta sortu erakunde bat

1. Joan [Dynamics 365 Customer Insights](https://dynamics.microsoft.com/ai/customer-insights/) webgunea.

2. Hautatu **Hasi erabiltzen**.

3. Aukeratu zure sinadura-agertokia eta hautatu dagokion esteka.

4. Onartu baldintzak eta hautatu **Jarraitu** erakundea sortzen hasteko.

5. Ingurunea sortu ondoren, bertara birbideratuko zaituzte [Customer Insights](https://home.ci.ai.dynamics.com).

6. Erabili demo ingurunea aplikazioa arakatzeko edo ingurune berria sortzeko hurrengo ataleko urratsak jarraituz.

7. Ingurumenaren ezarpenak zehaztu ondoren, hautatu **Sortu**.

8. Ingurunea behar bezala sortu ondoren hasiko da saioa.

## <a name="create-an-environment-in-an-existing-organization"></a>Sortu ingurune bat lehendik dagoen erakunde batean

Ingurune berria sortzeko bi era daude: Guztiz konfigurazio berria zehaz dezakezu edo konfigurazio ezarpen batzuk kopiatu ditzakezu lehendik dagoen ingurunetik.

Ingurune bat sortzeko:

1. Hautatu botoia **ezarpenak** ikurra aplikazioaren goiburuan.

1. Hautatu **Ingurune berria**.

   > [!div class="mx-imgBorder"]
   > ![Ingurune-ezarpenak](media/environment-settings-dialog.png)

1. **Inguru berria sortu** elkarrizketa-koadroa, hautatu **Ingurune berria**.

   Nahi baduzu [kopiatu uneko inguruneko datuak](#additional-considerations-for-copy-configuration-preview), hautatu **Kopiatu lehendik dagoen ingurunetik**. Zure erakundearen eskura dauden ingurune guztien zerrenda ikusiko duzu non datuak kopiatzeko.

1. Hornitu hurrengo xehetasunak:
   - **Izena**: entitatearen izena. Eremu hau dagoeneko bete da ingurune batetik kopiatzen baduzu, baina alda dezakezu.
   - **Eskualdea**: Zerbitzua hedatu eta ostatatzen den eskualdea.
   - **Mota**: Aukeratu Produkzio edo Sandbox ingurunea sortu nahi duzun ala ez.

2. Nahi baduzu, hauta dezakezu **Ezarpen aurreratuak**:

   - **Gorde datu guztiak**: Customer Insights-ek sortutako irteerako datuak non gorde nahi dituzun zehazten du. Bi aukera dituzu: **Customer Insights biltegiratzea** (Azure Data Lake Customer Insights taldearen bidez kudeatua) eta **Azure Data Lake Storage Gen2** (zure berezko Azure Data Lake Storage). Lehenespenez, Customer Insights biltegiratzeko aukera hautatuko da.

   > [!NOTE]
   > Datuak Azure Data Lake Storage-n gordez gero, onartu egingo duzu datuak Azure biltegiratze-konturako egokia den kokaleku geografikora transferitu eta bertan biltegiratuko direla, eta balitekeela Dynamics 365 Customer Insights-en datuak biltegiratzen diren lekua ez den beste kokaleku bat izatea. Informazio gehiago lortzeko, ikusi. [Argibide gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)
   >
   > Gaur egun, irensten diren erakundeak Customer Insights kudeatutako data lake-n gordetzen dira beti.
   > Ingurunea sortzerakoan hautatu zenuen Azure eskualde bereko Azure Data Lake Gen2 biltegiratze kontuak soilik onartzen ditugu.
   > Azure Data Lake Gen2 Hierarkikoa Izen espazioaren (HNS) gaitutako biltegiratze kontuak soilik onartzen ditugu.

   - Azure Data Lake Storage Gen2 aukerarako, baliabideetan oinarritutako aukera eta harpidetzan oinarritutako aukera erabil dezakezu autentifikatzeko. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md). **Edukiontzia** izena ezin da aldatu eta "customerinsights" izango da.
   
   - [Iragarpenak](predictions.md) erabili nahi badituzu, sartu Common Data Service instantziaren URLa **Zerbitzariaren helbidea** eremua, **Erabili iragarpenak** atalean.

   Prozesuak exekutatzen dituzunean, adibidez, datuak sartzea edo segmentua sortzea, dagozkien karpetak sortuko dira goian zehaztu duzun biltegiratze kontuan. Datu fitxategiak eta model.json fitxategiak dagozkien azpi-karpetetan sortu eta gehituko dira exekutatzen duzun prozesuan oinarrituta.

   Customer Insights-eko hainbat ingurune sortzen badituzu eta ingurune horietako irteerako entitateak zure biltegiratze kontuan gordetzea aukeratzen baduzu, karpeta bereiziak sortuko dira ingurune bakoitzarentzat ci_<environmentid> edukiontzian.

### <a name="additional-considerations-for-copy-configuration-preview"></a>Kopiaren konfiguraziorako gogoeta osagarriak (aurrebista)

Hurrengo konfigurazio ezarpenak kopiatzen dira:

- Eginbide konfigurazioak
- Inbertitu / inportatutako datu-iturriak
- Datuen bateratzea (mapa, bat etorri, batu) konfigurazioa
- Segmentuak
- Neurriak
- Erlazioak
- Jarduerak
- Bilaketa eta iragazkien indizea
- Esportatze-helburuak
- Programatutako freskatzea
- Aberasteak
- Ereduen kudeaketa
- Funtzio-zereginak

Hurrengo konfigurazio ezarpenak kopiatzen *ez* dira:

- Bezeroen profilak.
- Datu-iturburuaren kredentzialak. Datu-iturburu bakoitzerako kredentzialak eman beharko dituzu eta datu iturriak eskuz freskatu.
- Datu iturri arruntaren karpetaren datu iturriak Common Data Service lakua kudeatu. Datu iturri horiek eskuz sortu beharko dituzu iturri ingurunean izen berdinekin.

Ingurumena kopiatzean, berrespen mezu bat ikusiko duzu ingurune berria sortu dela. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.

Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera. Editatu datu-iturriak eta sartu kredentzialak freskatzeko.

> [!div class="mx-imgBorder"]
> ![Kopiatutako datu-iturburuak](media/data-sources-copied.png)

Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.

Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.

## <a name="edit-an-existing-environment"></a>Editatu lehendik dagoen ingurunea

Dauden inguruneen xehetasun batzuk editatu ditzakezu.

1. Joan **Administratzailea** > **Sistema** > **Hurrengoari buruz**.

2. Hautatu **Editatu**.

3. Ingurugiroa eguneratu dezakezu **Bistaratu izena** baina ezin duzu aldatu **Eskualdea** edo **Mota**.

4. Ingurumena konfiguratuta badago, datuak gordetzeko Azure Data Lake Storage Gen2, eguneratu dezakezu **Kontuaren gakoa**. Hala ere, ezin duzu aldatu **Kontuaren izena** edo **edukiontzia** izendatzeko.

5. Aukeran, kontuaren gakoan oinarritutako konexio batetik baliabideetan oinarritutako edo harpidetzan oinarritutako konexio batera egunera dezakezu. Bertsio berritu ondoren, ezin duzu kontuaren gakoetara itzuli eguneratu ondoren. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md). Ezin duzu aldatu **Edukiontzia**-ren informazioa konexioa eguneratzean.

## <a name="reset-an-existing-environment"></a>Berrezarri lehendik dagoen ingurunea

Ingurunea egoera hutsera berrezar dezakezu konfigurazio guztiak ezabatu eta sartutako datuak kendu nahi badituzu.

1.  Joan **Administratzailea** > **Sistema** > **Hurrengoari buruz**.

2.  Hautatu **Berrezarri**. 

3.  Ezabapena berresteko, idatzi ingurunearen izena eta hautatu **Berrezarri**.


## <a name="delete-an-existing-environment"></a>Aurretik bazegoen ingurune bat ezabatu

1. Joan **Administratzailea** > **Sistema** > **Hurrengoari buruz**.

1. Hautatu **Ezabatu**.

1. Ezabatzea berresteko, idatzi ingurumenaren izena eta hautatu **Ezabatu**.
