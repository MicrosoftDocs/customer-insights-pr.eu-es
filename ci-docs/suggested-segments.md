---
title: Neurrietan oinarritutako iradokitako segmentuak (aurrebista)
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
ms.openlocfilehash: e3f504827029afa12c65ec6f065a62606aaa823f
ms.sourcegitcommit: 8a28e9458b857adf8e90e25e43b9bc422ebbb2cd
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/18/2022
ms.locfileid: "9170942"
---
# <a name="suggested-segments-based-on-measures-preview"></a>Neurrietan oinarritutako iradokitako segmentuak (aurrebista)

Ezagutu zure bezeroen segmentu interesgarriak adimen artifizialeko eredu baten laguntzarekin. Ikaskuntza automatiko funtzionatutako funtzio honek neurriak edo bezeroaren atributuetan oinarritutako segmentuak iradokitzen ditu. Zure Funtsezko Errendimendu Adierazleak (KPI) hobetzen lagun dezake edo atributuek beste atributu batzuen testuinguruan duten eragina hobeto ulertzen lagun dezake.

> [!NOTE]
> Iradokitako segmentuen funtzioak baliabide automatizatuak erabiltzen ditu datuak ebaluatzeko eta datu horietan oinarrituta iragarpenak egiteko. Beraz, profilak egiteko metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Erregelamendu Orokorrak ("GDPR") definitzen baitu. Ezaugarri hau datuak tratatzeko zure erabilera DBAO edo beste lege edo arau batzuen menpe egon daiteke. Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, eginbide, lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.

:::image type="content" source="media/suggested-segments.png" alt-text="Alboko panel batean iradokizun baten xehetasunak erakusten dituen iradokitako segmentuen orria.":::

## <a name="suggested-segments-to-improve-your-kpis"></a>KPIak hobetzeko gomendatutako segmentuak

Erabiltzen baduzu [sortutako neurriak](measures.md) zure KPIen jarraipena egiteko, sortu segmentuak KPIren eraginak ikusteko. Informazio hau oso zuzendutako kanpaina bat egiteko erabil dezakezu.

Adibidez, izeneko neurri baten jarraipena egiten duzu *TotalSpendPerCustomer*. Enpresa gisa, kopuru hau hazten ikustea gustatuko litzaizuke. Neurri bat atributu nagusi gisa aukeratuz gero, hautatu eraginaren arabera ebaluatu nahi dituzun atributuak. Demagun *kide-maila*, *bazkide-aldia*, eta *okupazioa*. Customer Insights-ek neurri horren eragin handiena nor den esaten duen segmentua iradoki dezake. Adibidez, *Kontulariak* nor dira *Urrea* kideak eta zure negozioarekin egon direnak *gutxienez bost urte* dira eragile handienak *TotalSpendPerCustomer*. Iradokizun bakoitzeko segmentuaren tamaina kalkulatuko duzu. Informazio hau erabil dezakezue bideratutako publikoentzako kanpainak sortzeko.

## <a name="understand-what-influences-a-customer-attribute"></a>Ulertu bezeroaren atributuak zerk eragiten duen

Bezeroaren atributu bat neurri baten ordez hauta dezakezu atributu nagusi gisa. Atributuak eragiteko aukeraren arabera, adimen artifizialeko ereduak hautatutako atributuek atributu nagusian nola eragiten duten erakusten duten iradokizun sorta sortzen du.

Adibidez, zuk aukeratzen duzu *Rewards kidea (Bai/Ez)* atributu nagusi gisa. *Agintaldia*, *Okupazioa* eta *Laguntza txartel kopurua* eragiteko beste atributu gisa ezartzen dira. Adimen artifizialeko ereduak bi urte baino gehiagoko agintaldia duten IKT profesionalak adierazten dituzten segmentuak saritzen kideak direla iradoki dezake. Beste iradokizun batek urtebetetik gorako agintaldia eta hiru laguntza txartel baino gutxiago dituzten kontulariak saritutako kideak direla nabarmendu dezake.

## <a name="artificial-intelligence-usage"></a>Adimen artifizialaren erabilera

Atributu nagusia eta eraginen atributuak erabiliz, erabaki zuhaitz algoritmo batek segmentu interesgarriak iradokitzen ditu. Iradokizunak adimen artifizialeko algoritmoak jasotako arau edo ereduetan oinarritzen dira. Batez besteko biztanleriarekiko nabarmen desberdintzen diren segmentuak soilik agertzen dira iradokizun gisa. Batez besteko biztanleriarekin alderatzea hautatutako neurrian edo atributu nagusian oinarritzen da.

### <a name="responsible-ai"></a>AA arduratsua

Iradokitako segmentuekin, atributuak hautatzen dituzu segmentu berriak sortzeko eta hautatzen dituzun datuak prozesatzeko. Atributuak aukeratzean, besteak beste, arraza, sexu orientazioa edo generoa bezalako sentikorrak, ziurtatu behar duzu datu horiek prozesatu ditzakezula eta egin beharko duzula. Zure erakundeari aplika dakizkiokeen legeak betetzeaz arduratzen zara eta zure erakundearen printzipioak eta pribatutasun politikak errespetatzea.

### <a name="different-results-for-primary-attributes-with-categorical-and-numeric-values"></a>Emaitza desberdinak lehen mailako atributuetarako kategoriko eta zenbakizko balioekin

Segmentu iradokizunak desberdinak dira atributu numeriko bat edo atributu kategoriko bat aukeratzen baduzu atributu nagusi gisa. Atributu kategoriko bateko balioek bi kategoria edo mota edo gehiago dituzte. Zenbaki-atributu batek datu kuantitatiboak ditu eta horrekin lotutako neurketa-zentzua du.

Bezalako zenbakizko atributu batekin *urteko errenta* edo *bazkide aldia* atributu nagusia denez, sistemak zenbakizko atributuaren batez besteko balio handiagoa edo txikiagoa duten segmentuak iradokitzen ditu bezero guztiekin alderatuta.

Bezalako atributu kategorikoa *bezeroaren gogobetetasuna* atributu nagusiak kategoria jakin bateko bezeroen ehuneko handiagoa edo txikiagoa duten iradokitako segmentuak lortzen baititu, kategoria bereko bezero guztien ehunekoarekin alderatuta. Adibidez, *bezeroaren gogobetetasuna* atributu nagusi gisa aukeratzen da eta hiru kategoria ditu (*Baxua*, *Ertaina* eta *Altua*). Kategoria bakoitzerako, kategoria horretako bezeroen ehuneko handiagoa edo txikiagoa duten segmentuak proposatuko dira, kategoria bereko bezero guztien proportzioaren aldean. Bezeroen %22k asebetetze *altua* badu, asebetetze *altua* duten bezeroen ehuneko handiagoa edo baxuagoa duten segmentuak iradokiko dira, kategoria horretarako iradokitako %22arekin alderatuta. Era berean, segmentuak iradokiko dira beste kategoria bakoitzerako (*Baxua* eta *Ertaina*) estatistikoki esanguratsuak badira.

> [!NOTE]
> Gaur egun, gehienez 10 kategoria dituzten atributu kategoriko nagusiak onartzen ditugu. 10 kategoria baino gehiago dituen atributu nagusi batean oinarritutako segmentu-iradokizunak ikusi nahi badituzu, kategoria batzuk taldekatzea gomendatzen dugu, kategoria kopurua 10era edo gutxiagora murrizteko. Muga hau lehen mailako atributuei bakarrik dagokie. Atributu kategorikoetan eragiteko, gehienez 100 kategoria onartzen ditugu.

## <a name="generate-suggested-segments"></a>Sortu iradokitako segmentuak

1. Joan **Segmentuak** eta hautatu **Iradokizunak (aurrebista)** fitxa.

1. Hautatu **Bilatu iradokizun berriak** eta aukeratu **Neurri/metrika bat hobetu**. Hautatu **Hasi**.

   :::image type="content" source="media/suggested-segments-measure.png" alt-text="Iradokitako segmentuetan hobekuntza neurria hautatzea.":::

1. Aukeratu bezero-atributu edo neurri bat atributu nagusi gisa eta hautatu **Hurrengoa**.

1. Hautatu eragin-atributuak eta hautatu **Korrika egin**.

   > [!TIP]
   > Eragin anitzeko atributuak hautatzeak atributu nagusian nola eragiten duten ebaluatzeko aukerak hobetzen ditu. Ez sartu atributu nagusian eraginik ez duten atributuak. Adibidez, zure bezero guztiak herrialde jakin batekoak badira, ez sartu *herrialdea* atributua ez du inolako eraginik izango irteeran.

Bezeroen profil kopuruaren eta hautatutako atributuen arabera, hautatutako atributuak prozesatzeko minutu batzuk igaro daitezke.

## <a name="manage-suggested-segments"></a>Kudeatu iradokitako segmentuak

Joan **Segmentuak** eta hautatu **Iradokizunak (aurrebista)** fitxa. urtean **Atributuetan oinarritutako segmentu-iradokizunak** atalean, hautatu iradokitako segmentu bat erabilgarri dauden ekintzak ikusteko.

- **Ikusi** iradokitako segmentuaren xehetasunak eta AI ereduak ikasitako atributu-balioak edo arauak.
- **Gorde segmentu gisa** iradokizuna segmentu gisa. Bertan bistaratzen da **Segmentu guztiak** fitxa eta izan daiteke [freskatu, editatu edo ezabatu](segments.md).
- **Editatu atributuak** eta egungo iradokizunak ordezkatuko dituzten konfiguratutako atributuak aldatu.
- **Freskatu iradokizunak** iradokizunak freskatzeko, konfiguratutako atributuak mantenduz.

## <a name="limitations"></a>Murriztapenak

1. Kalkulatutako segmentuaren tamaina ez dator bat: balio hutsak dituen atributu nagusia hautatzen baduzu, segmentuaren iradokizunetan kalkulatutako segmentuaren tamaina eragin dezake. Segmentu hori gordetzean, benetako segmentuaren tamaina jatorrizko estimazioaren desberdina izan daiteke.

2. Boolear motako lehen mailako atributuek ez dute funtzionatzen: gaur egun, kate eta zenbakizko datu motak soilik onartzen ditugu atributu nagusi gisa.

3. Iradokitako segmentuak ez dira nahikoa bereizten: Gogoan izan aukeratutako atributuek eta atributu horien balioen banaketak emaitzetan eragina duela. Zure eraginaren atributuak edo baita atributu nagusia alda ditzakezu emaitza desberdinak lortzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]