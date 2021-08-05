---
title: Sortu eta kudeatu inguruneak
description: Ikasi zerbitzuan izena ematen eta inguruneak kudeatzen.
ms.date: 07/22/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
ms.reviewer: mhart
author: NimrodMagen
ms.author: nimagen
manager: shellyha
ms.openlocfilehash: 2f115269b9d07dd118ec18cc48b55de8aea9b5bb
ms.sourcegitcommit: 98267da3f3eddbdfbc89600a7f54e5e664a8f069
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/28/2021
ms.locfileid: "6683458"
---
# <a name="manage-environments"></a>Kudeatu inguruneak

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

## <a name="switch-environments"></a>Aldatu inguruneak

Hautatu botoia **Ingurumena** kontrol orria orriaren goiko eskuinaldean inguruneak aldatzeko.

:::image type="content" source="media/home-page-environment-switcher.png" alt-text="Inguruaz aldatzeko kontrolaren pantaila-argazkia.":::

Administratzaileek inguruneak [sortu](get-started-paid.md) eta kudeatu ditzakete.

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
   > - [Entitate batean falta diren balioen iragarpena](predictions.md) eta PowerBI Embedded txostenak hartzaileen xehetasunetan (zure ingurunean gaituta badaude) ez dira onartzen datuak partekatzea gaitzen duzunean Microsoft Dataverse-k kudeatutako datu-biltegiarekin.

   Datuak partekatzeko aukera gaitu ondoren Microsoft Dataverse-rekin, datu-iturburuen freskatze osoa eta beste prozesu batzuk hasiko dira. Une honetan prozesuak martxan badaude, ez duzu ikusiko datuak partekatzea gaitzeko aukera Microsoft Dataverse. Itxaron prozesu horiek amaitu arte edo utzi bertan behera datuak partekatzea ahalbidetzeko. 
   
   :::image type="content" source="media/datasharing-with-DataverseMDL.png" alt-text="Konfigurazioaren aukerak gaitzeko datuak partekatzeko Microsoft Dataverse.":::
   
   Prozesuak exekutatzen dituzunean, adibidez, datuak sartzea edo segmentua sortzea, dagozkien karpetak sortuko dira goian zehaztu duzun biltegiratze kontuan. Datu fitxategiak eta model.json fitxategiak sortu eta dagozkien azpikarpetetara gehituko dira, exekutatzen duzun prozesuaren arabera.

## <a name="copy-the-environment-configuration"></a>Kopiatu ingurunearen konfigurazioa

Ingurune berri bat sortzen duzunean, konfigurazioa lehendik dagoen ingurune batetik kopiatzea aukeratu dezakezu. 

:::image type="content" source="media/environment-settings-dialog.png" alt-text="Ingurumen ezarpenetako ezarpen aukeren pantaila-argazkia.":::

Zure erakundearen eskura dauden ingurune guztien zerrenda ikusiko duzu non datuak kopiatzeko.

Hurrengo konfigurazio ezarpenak kopiatzen dira:

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

Datu hauek *ez* dira kopiatu:

- Bezeroen profilak.
- Datu-iturburuaren kredentzialak. Datu-iturburu bakoitzerako kredentzialak eman beharko dituzu eta datu iturriak eskuz freskatu.
- Common Data Model karpetako datu iturriak eta Dataverse kudeatzen du Data Lake. Datu iturri horiek eskuz sortu beharko dituzu iturri ingurunean izen berdinekin.

Ingurumena kopiatzean, berrespen mezu bat ikusiko duzu ingurune berria sortu dela. Aukeratu **Joan datu iturrietara** datu-iturrien zerrenda ikusteko.

Datu iturri guztiek a **Beharrezkoak diren egiaztagiriak** egoera. Editatu datu-iturriak eta sartu kredentzialak freskatzeko.

:::image type="content" source="media/data-sources-copied.png" alt-text="Kopiatu ziren eta autentifikazioa behar duten datu iturrien zerrenda.":::

Datu iturriak freskatu ondoren, joan **Datuak** > **bateratzeko**. Hemen iturburu ingurumenaren ezarpenak aurkituko dituzu. Editatu behar dituzunean edo hautatu **Exekutatu** datuak bateratzeko prozesua hasteko eta bezero bateratutako entitatea sortzeko.

Datuen bateratzea amaitutakoan, joan **Neurriak** eta **segmentuak** haiek freskatzeko ere.

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
