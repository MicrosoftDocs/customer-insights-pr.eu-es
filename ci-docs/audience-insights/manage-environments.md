---
title: Sortu eta kudeatu inguruneak
description: Ikasi zerbitzuan izena ematen eta inguruneak kudeatzen.
ms.date: 06/15/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
ms.reviewer: mhart
author: NimrodMagen
ms.author: nimagen
manager: shellyha
ms.openlocfilehash: 904ce68336cba4b7a4d5a37692b72d091400559d
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304865"
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

> [!NOTE]
> Erakundeek sor dezakete *bi* Customer Insights lizentzia bakoitzeko inguruneak. Zure erakundeak lizentzia behin baino gehiagotan erosten badu, mesedez [jarri harremanetan gure laguntza taldearekin](https://go.microsoft.com/fwlink/?linkid=2079641) erabilgarri dauden ingurune kopurua handitzeko. Edukiera eta gehigarritasunari buruzko informazio gehiago lortzeko, deskargatu [Dynamics 365 lizentzien gida](https://go.microsoft.com/fwlink/?LinkId=866544).

Ingurune bat sortzeko:

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu **Berria**.

   > [!div class="mx-imgBorder"]
   > ![Ingurune-ezarpenak.](media/environment-settings-dialog.png)

1. Urtean **Ingurune bat sortu** elkarrizketa-koadroa, hautatu **Ingurune berria**.

   Nahi baduzu [kopiatu uneko inguruneko datuak](#considerations-for-copy-configuration-preview), hautatu **Kopiatu lehendik dagoen ingurunetik**. Zure erakundearen eskura dauden ingurune guztien zerrenda ikusiko duzu non datuak kopiatzeko.

1. Hornitu hurrengo xehetasunak:
   - **Izena**: entitatearen izena. Eremu hau dagoeneko bete da ingurune batetik kopiatzen baduzu, baina alda dezakezu.
   - **Mota**: Aukeratu Produkzio edo Sandbox ingurunea sortu nahi duzun ala ez.
   - **Eskualdea**: Zerbitzua hedatu eta ostatatzen den eskualdea.
   
1. Nahi baduzu, hauta dezakezu **Ezarpen aurreratuak**:

   - **Gorde datu guztiak**: Customer Insights-ek sortutako irteerako datuak non gorde nahi dituzun zehazten du. Bi aukera izango dituzu: **Customer Insights biltegiratzea** (Customer Insights taldeak kudeatzen duen Azure Data Lake) eta **Azure Data Lake Storage** (zeurea Azure Data Lake Storage). Lehenespenez, Customer Insights biltegiratzeko aukera hautatuko da.

     > [!NOTE]
     > Datuak Azure Data Lake Storage-n gordez gero, onartu egingo duzu datuak Azure biltegiratze-konturako egokia den kokaleku geografikora transferitu eta bertan biltegiratuko direla, eta balitekeela Dynamics 365 Customer Insights-en datuak biltegiratzen diren lekua ez den beste kokaleku bat izatea. Informazio gehiago lortzeko, ikusi. [Argibide gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)
     >
     > Gaur egun, irensten diren erakundeak Customer Insights Kudeatutako Data Lake-n gordetzen dira beti. 
     > 
     > Bakarrik onartzen dugu Azure Data Lake Storage ingurunea sortzerakoan hautatu zenituen Azure eskualde bereko kontuak. 
     > 
     > Bakarrik onartzen dugu Azure Data Lake Storage izen espazio hierarkikoa gaituta duten kontuak.


   - Azure Data Lake Storage aukera, baliabideetan oinarritutako aukera bat eta harpidetzan oinarritutako aukera bat autentifikatzeko aukera dezakezu. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md). **Edukiontzia** izena ezin da aldatu eta `customerinsights` izango da.
   
   - Erabili nahi baduzu [iragarpenak](predictions.md), konfiguratu datuak partekatzea konfiguratzea Microsoft Dataverse-rekin, edo gaitu lokal datu iturrietatik datuak sartzea, eman Microsoft Dataverse inguruneko URL azpian **Konfiguratu datuak partekatzearekin Microsoft Dataverse eta gaitasun osagarriak gaitu**. Aukeratu **Gaitu datuak partekatzea** Customer Insights-en irteerako datuak partekatzeko Microsoft Dataverse kudeatutako datuen lakua.

     > [!NOTE]
     > - Datuak partekatzearekin Microsoft Dataverse-ren kudeatutako datuen lakua ez da onartzen une honetan datu guztiak gordetzen dituzunean Azure Data Lake Storage.
     > - [Entitate batean falta diren balioen iragarpena](predictions.md) ez da onartzen une honetan datuak partekatzea gaitzen duzunean Microsoft Dataverse-n kudeatutako Data Lake.

     > [!div class="mx-imgBorder"]
     > ![Konfigurazioaren aukerak gaitzeko datuak partekatzeko Microsoft Dataverse.](media/datasharing-with-DataverseMDL.png)

   Prozesuak exekutatzen dituzunean, adibidez, datuak sartzea edo segmentua sortzea, dagozkien karpetak sortuko dira goian zehaztu duzun biltegiratze kontuan. Datu fitxategiak eta model.json fitxategiak sortu eta karpetetara gehituko dira, prozesuaren izenaren arabera.

   Customer Insights-eko hainbat ingurune sortzen badituzu eta ingurune horietako irteerako entitateak zure biltegiratze kontuan gordetzea aukeratzen baduzu, karpeta bereiziak sortuko dira ingurune bakoitzarentzat ci_<environmentid> edukiontzian.

### <a name="considerations-for-copy-configuration-preview"></a>Kopiatzeko konfigurazioaren inguruko gogoetak (aurrebista)

Hurrengo konfigurazio ezarpenak kopiatzen dira:

- Eginbide konfigurazioak
- Hornitutako edo inportatutako datu-iturburuak
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
- Common Data Model karpetako datu iturriak eta Dataverse kudeatzen du Data Lake. Datu iturri horiek eskuz sortu beharko dituzu iturri ingurunean izen berdinekin.

Ingurumena kopiatzean, berrespen mezu bat ikusiko duzu ingurune berria sortu dela. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.

Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera. Editatu datu-iturriak eta sartu kredentzialak freskatzeko.

> [!div class="mx-imgBorder"]
> ![Kopiatutako datu-iturburuak.](media/data-sources-copied.png)

Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.

Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.

## <a name="edit-an-existing-environment"></a>Editatu lehendik dagoen ingurunea

Dauden inguruneen xehetasun batzuk editatu ditzakezu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

2.  Hautatu **Editatu** ikonoa.

3. **Editatu ingurunea** koadroan, ingurunekoak egunera ditzakezu **Bistaratzeko izena**, baina ezin duzu aldatu **Eskualdea** edo **Mota**.

4. Ingurunea datuak gordetzeko konfiguratuta badago Azure Data Lake Storage, eguneratu dezakezu **Kontuaren gakoa**. Hala ere, ezin duzu aldatu **Kontuaren izena** edo **edukiontzia** izendatzeko.

5. Aukeran, kontuaren gakoan oinarritutako konexio batetik baliabideetan oinarritutako edo harpidetzan oinarritutako konexio batera egunera dezakezu. Bertsio berritu ondoren, ezin duzu kontuaren gakoetara itzuli eguneratu ondoren. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md). Ezin duzu aldatu **Edukiontzia**-ren informazioa konexioa eguneratzean.

6. Aukeran, a eman dezakezu Microsoft Dataverse inguruneko URL azpian **Konfiguratu datuak partekatzearekin Microsoft Dataverse eta gaitasun osagarriak gaitu**. Gaitasun hauek datuak oinarritutako aplikazioekin eta soluzioekin partekatzea dira Microsoft Dataverse, lokal datu iturrietatik jasotako datuak edo erabilera [iragarpenak](predictions.md). Aukeratu **Gaitu datuak partekatzea** Customer Insights-en irteerako datuak partekatzeko Microsoft Dataverse kudeatutako Data Lake.

   > [!NOTE]
   > - Datuak partekatzearekin Microsoft Dataverse-ren kudeatutako datuen lakua ez da onartzen une honetan datu guztiak gordetzen dituzunean Azure Data Lake Storage.
   > - [Entitate batean falta diren balioen iragarpen](predictions.md) ez da onartzen une honetan datuak partekatzea gaitzen duzunean Microsoft Dataverse Kudeatutako Data Lake.

   Datuak partekatzeko aukera gaitu ondoren Microsoft Dataverse-rekin, datu-iturburuen freskatze osoa eta beste prozesu batzuk hasiko dira. Une honetan prozesuak martxan badaude, ez duzu ikusiko datuak partekatzea gaitzeko aukera Microsoft Dataverse. Itxaron prozesu horiek amaitu arte edo utzi bertan behera datuak partekatzea ahalbidetzeko. 
   
   :::image type="content" source="media/datasharing-with-DataverseMDL.png" alt-text="Konfigurazioaren aukerak gaitzeko datuak partekatzeko Microsoft Dataverse.":::
   
   Prozesuak exekutatzen dituzunean, adibidez, datuak sartzea edo segmentua sortzea, dagozkien karpetak sortuko dira goian zehaztu duzun biltegiratze kontuan. Datu fitxategiak eta model.json fitxategiak sortu eta dagozkien azpikarpetetara gehituko dira, exekutatzen duzun prozesuaren arabera.

## <a name="reset-an-existing-environment"></a>Berrezarri lehendik dagoen ingurunea

Administratzaile gisa, ingurunea egoera hutsera berrezar dezakezu konfigurazio guztiak ezabatu eta sartutako datuak kendu nahi badituzu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan. 

2.  Aukeratu berrezarri nahi duzun ingurunea eta hautatu elipsia (**...**). 

3. Aukeratu **Berrezarri** aukera. 

4.  Ezabapena berresteko, idatzi ingurunearen izena eta hautatu **Berrezarri**.

## <a name="delete-an-existing-environment"></a>Aurretik bazegoen ingurune bat ezabatu

Administratzaile gisa, kudeatzen duzun ingurunea ezabatu dezakezu.

1.  Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

2.  Aukeratu berrezarri nahi duzun ingurunea eta hautatu elipsia (**...**). 

3. Aukeratu **Ezabatu** aukera. 

4.  Ezabatzea berresteko, idatzi ingurumenaren izena eta hautatu **Ezabatu**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
