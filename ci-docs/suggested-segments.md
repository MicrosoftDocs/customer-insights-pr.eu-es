---
title: Ikaskuntza automatikoak iradokitako segmentuak bultzatu ditu
description: Utzi Ikaskuntza automatikoak bezeroen atributuetan oinarritutako segmentu berri eta interesgarriak aurkitzen laguntzen.
ms.date: 10/15/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
manager: shellyha
searchScope:
- ci-segment-suggestions
- customerInsights
ms.openlocfilehash: 5c7c6cc8231f758713b989bbe782aa03a4b78fa9
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642141"
---
# <a name="suggested-segments-preview"></a>Iradokitako segmentuak (aurrebista)

Ezagutu zure bezeroen segmentu interesgarriak adimen artifizialeko eredu baten laguntzarekin. Ikaskuntza automatiko funtzionatutako funtzio honek neurriak edo bezeroaren atributuetan oinarritutako segmentuak iradokitzen ditu. Zure KPIak hobetzen lagun dezake edo atributuek beste atributu batzuen testuinguruan duten eragina hobeto ulertzen lagun dezake. 

> [!NOTE]
> Iradokitako segmentuen ezaugarriak bitarteko automatizatuak erabiltzen ditu datuak ebaluatzeko eta aurreikuspenak egiteko datu horietan oinarrituta, eta, beraz, profilak sortzeko metodo gisa erabiltzeko gaitasuna du, termino hori Datuen Babeserako Arau Orokorrak ("DBAO") definitzen baitu. Ezaugarri hau datuak tratatzeko zure erabilera DBAO edo beste lege edo arau batzuen menpe egon daiteke. Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, eginbide, lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.

:::image type="content" source="media/suggested-segments.png" alt-text="Alboko panel batean iradokizun baten xehetasunak erakusten dituen iradokitako segmentuen orria.":::

## <a name="suggested-segments-to-improve-your-kpis"></a>KPIak hobetzeko gomendatutako segmentuak

Customer Insights-en erabiltzaile gisa, ziurrenik hainbat eduki dituzu [sortutako neurriak](measures.md) zure Errendimendu Adierazle Nagusiak (KPI) jarraipena egiten laguntzen dutenak. Garrantzitsua da zenbait atributu KPI honetan nola eragiten duten ulertzea segmentuak sortzeko eta oso bideratutako kanpaina bat egiteko.   
Adibidez, izeneko neurri baten jarraipena egiten duzu *TotalSpendPerCustomer*. Enpresa gisa, kopuru hau hazten ikustea gustatuko litzaizuke. Neurri bat atributu nagusi gisa aukeratzean, eraginaren arabera ebaluatu nahi dituzun atributuak hautatuko dituzu. Demagun *kide-maila*, *bazkide-aldia*, eta *okupazioa*. Customer Insights-ek neurri horren eragin handiena nor den esaten duen segmentua iradoki dezake. Adibidez, *Kontulariak* nor dira *Urrea* kideak eta zure negozioarekin egon direnak *gutxienez bost urte* dira eragile handienak *TotalSpendPerCustomer*. Iradokizun bakoitzeko segmentuaren tamaina kalkulatuko duzu. Informazio hau erabil dezakezue bideratutako publikoentzako kanpainak sortzeko.

## <a name="understand-what-influences-a-customer-attribute"></a>Ulertu bezeroaren atributuak zerk eragiten duen

Bezeroaren atributu bat neurri baten ordez hauta dezakezu atributu nagusi gisa. Atributuak eragiteko aukeraren arabera, adimen artifizialeko ereduak hautatutako atributuek atributu nagusian nola eragiten duten erakusten duten iradokizun sorta sortzen du.   
Adibidez, zuk aukeratzen duzu *Rewards kidea (Bai/Ez)* atributu nagusi gisa. *Agintaldia*, *Okupazioa* eta *Laguntza txartel kopurua* eragiteko beste atributu gisa ezartzen dira. Adimen artifizialeko ereduak bi urte baino gehiagoko agintaldia duten IKT profesionalak adierazten dituzten segmentuak saritzen kideak direla iradoki dezake. Beste iradokizun batek urtebetetik gorako agintaldia eta hiru laguntza txartel baino gutxiago dituzten kontulariak saritutako kideak direla nabarmendu dezake. 

## <a name="artificial-intelligence-usage"></a>Adimen artifizialaren erabilera

Atributu nagusia eta eraginen atributuak erabiliz, erabaki zuhaitz algoritmo batek segmentu interesgarriak iradokitzen ditu. Iradokizunak adimen artifizialeko algoritmoak jasotako arau edo ereduetan oinarritzen dira. Batez besteko biztanleriarekiko nabarmen desberdintzen diren segmentuak soilik agertzen dira iradokizun gisa. Batez besteko biztanleriarekin alderatzea hautatutako neurrian edo atributu nagusian oinarritzen da.

### <a name="responsible-ai"></a>AA arduratsua

Iradokitako segmentuei esker, atributuak hautatu ditzakezu segmentu berriak sortzeko eta hautatutako datuak prozesatzeko. Atributuak aukeratzean, besteak beste, arraza, sexu orientazioa edo generoa bezalako sentikorrak, ziurtatu behar duzu datu horiek prozesatu ditzakezula eta egin beharko duzula. Zure erakundeari aplika dakizkiokeen legeak betetzeaz arduratzen zara eta zure erakundearen printzipioak eta pribatutasun politikak errespetatzea.

### <a name="different-results-for-primary-attributes-with-categorical-and-numeric-values"></a>Emaitza desberdinak lehen mailako atributuetarako kategoriko eta zenbakizko balioekin

Segmentu iradokizunak desberdinak dira atributu numeriko bat edo atributu kategoriko bat aukeratzen baduzu atributu nagusi gisa. Atributu kategoriko bateko balioek bi kategoria edo mota edo gehiago dituzte. Zenbaki-atributu batek datu kuantitatiboak ditu eta horrekin lotutako neurketa-zentzua du.

Bezalako zenbakizko atributu batekin *urteko errenta* edo *bazkide aldia* atributu nagusia denez, sistemak zenbakizko atributuaren batez besteko balio handiagoa edo txikiagoa duten segmentuak iradokitzen ditu bezero guztiekin alderatuta.

Bezalako atributu kategorikoa *bezeroaren gogobetetasuna* atributu nagusiak kategoria jakin bateko bezeroen ehuneko handiagoa edo txikiagoa duten iradokitako segmentuak lortzen baititu, kategoria bereko bezero guztien ehunekoarekin alderatuta. Adibidez, *bezeroaren gogobetetasuna* atributu nagusi gisa aukeratzen da eta hiru kategoria ditu (*Baxua*, *Ertaina* eta *Altua*). Kategoria bakoitzerako, kategoria horretako bezeroen ehuneko handiagoa edo txikiagoa duten segmentuak proposatuko dira, kategoria bereko bezero guztien proportzioaren aldean. Bezeroen %22k asebetetze *altua* badu, asebetetze *altua* duten bezeroen ehuneko handiagoa edo baxuagoa duten segmentuak iradokiko dira, kategoria horretarako iradokitako %22arekin alderatuta. Era berean, segmentuak iradokiko dira beste kategoria bakoitzerako (*Baxua* eta *Ertaina*) estatistikoki esanguratsuak badira.

> [!NOTE]
> Gaur egun, gehienez 10 kategoria dituzten atributu kategoriko nagusiak onartzen ditugu. 10 kategoria baino gehiago dituen atributu nagusi batean oinarritutako segmentuen iradokizunak ikusi nahi badituzu, kategoria batzuk taldekatzea gomendatzen dugu kategoria kopurua 10 edo gutxiagora murrizteko. Muga hau lehen mailako atributuei bakarrik dagokie. Atributu kategorikoetan eragiteko, gehienez 100 kategoria onartzen ditugu.

## <a name="generate-suggested-segments"></a>Sortu iradokitako segmentuak

1. Joan hona: **Segmentuak**.

1. Aukeratu **Iradokizunak (aurrebista)** fitxa.

1. Aukeratu **Lortu iradokizun berriak** esperientzia gidatua hasteko.

1. Aukeratu bezeroaren atributu edo neurri bat atributu nagusi gisa eta sakatu **Hurrengoa**.

   :::image type="content" source="media/suggested-segments-primary-attribute.png" alt-text="Iradokitako segmentuen iradokizunetarako atributu nagusia aukeratzea.":::

1. Aukeratu eraginaren atributuak eta hautatu **Gorde**.
   
   > [!TIP]
   > Eragin anitzeko atributuak hautatzeak atributu nagusian nola eragiten duten ebaluatzeko aukerak hobetzen ditu. Ez sartu atributu nagusia eraginik ez duten atributuak. Adibidez, zure bezero guztiak herrialde jakin batekoak badira, ez sartu *herrialdea* atributua ez du inolako eraginik izango irteeran.

1. Bezeroen profil kopuruaren eta hautatutako atributuen arabera, hautatutako atributuak prozesatzeko minutu batzuk igaro daitezke. 

## <a name="view-details-of-a-suggested-segment"></a>Ikusi Iradokitako segmentuaren xehetasunak

Adimen artifizialeko ereduak iradokizunak sortu ondoren, zerrendan aurkituko dituzu **Segmentuak** > **Iradokizunak (aurrebista)**.
 
Hautatu iradokitako segmentu bat iradokizun horren xehetasunak berrikusteko. AI ereduak hautatutako segmentua iradokitzeko ikasitako atributu balioak edo arauak ere berrikusi ditzakezu.

## <a name="save-a-suggestion-as-a-segment"></a>Gorde segmentu bat iradokizun gisa

1. Joan **Segmentuak** > **Iradokizunak (aurrebista)**.

1. Hautatu gorde nahi duzun segmentua. 

1. Alboko panelean, hautatu **Gorde segmentu gisa**. 

1. Segmentua gorde ondoren, segmentuen zerrendan agertuko da **Segmentu guztiak** fitxa. Orain izan daiteke [freskatu, editatu edo ezabatu beste edozein segmentu bezala](segments.md).

## <a name="refresh-or-edit-a-set-of-suggestions"></a>Freskatu edo editatu iradokizun multzo bat

1. Joan **Segmentuak** > **Iradokizunak (aurrebista)**.

1. Aukeratu **Freskatu iradokizunak** iradokizunak freskatzeko konfiguratutako atributuak mantenduz. Bestela, hautatu **Editatu atributuak** konfiguratutako atributuak aldatzeko. Sistemak adimen artifizialeko eredua berriro exekutatuko du, segmentu iradokizunak sortuko ditu azken datuetan oinarrituta eta uneko iradokizunak ordezkatuko ditu.

## <a name="limitations"></a>Murriztapenak

1. Kalkulatutako segmentuaren tamaina ez dator bat: balio hutsak dituen atributu nagusia hautatzen baduzu, segmentuaren iradokizunetan kalkulatutako segmentuaren tamaina eragin dezake. Segmentu hori gordetzean, benetako segmentuaren tamaina jatorrizko estimazioaren desberdina izan daiteke.
 
2. Boolear motako lehen mailako atributuek ez dute funtzionatzen: gaur egun, kate eta zenbakizko datu motak soilik onartzen ditugu atributu nagusi gisa.

3. Iradokitako segmentuak ez dira nahikoa bereizten: Gogoan izan aukeratutako atributuek eta atributu horien balioen banaketak emaitzetan eragina duela. Zure eraginaren atributuak edo baita atributu nagusia alda ditzakezu emaitza desberdinak lortzeko.



[!INCLUDE [footer-include](includes/footer-banner.md)]