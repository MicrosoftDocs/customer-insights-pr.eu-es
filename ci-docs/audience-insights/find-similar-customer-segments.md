---
title: Bilatu IA duten antzeko bezeroak (bideoa dauka)
description: Aurkitu antzeko bezeroen segmentuak adimen artifizialarekin.
ms.date: 06/25/2020
ms.subservice: audience-insights
ms.topic: conceptual
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-segment-builder
- ci-segment-insights
- customerInsights
ms.openlocfilehash: 5626b980ad8802aae9657052e3ca51a70c49baf9
ms.sourcegitcommit: 73cb021760516729e696c9a90731304d92e0e1ef
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/25/2022
ms.locfileid: "8355230"
---
# <a name="similar-customers-preview"></a>Bezero antzekoak (aurrebista)

Ezaugarri honek adimen artifiziala erabiliz zure bezero basean antzeko bezeroak topa ditzakezu. Ezaugarri hau erabiltzeko gutxienez segmentu bat sortu behar duzu. Lehendik dagoen segmentu baten irizpideak zabaltzeak segmentu horren antzekoak diren bezeroak aurkitzen laguntzen du.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWOFou]

> [!NOTE]
> *Aurkitu antzeko bezeroak* Datu horietan oinarritutako datuak ebaluatzeko eta iragarpenak egiteko bitarteko automatizatuak erabiltzen ditu eta, beraz, profil metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Erregelamendu Orokorrak ("DBAO") definitzen baitu. Bezeroak funtzio hau erabiltzeko datuak prozesatzeko DBAO edo beste lege edo arau batzuen menpe egon daiteke. Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, iragarpenez aplikagarriak diren lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.

## <a name="finding-similar-customers"></a>Antzeko bezeroak aurkitzea

1. Hartzaileen xehetasunetan, joan **Segmentuak** atalera eta hautatu segmentu berrirako oinarritzat hartu nahi duzun segmentua. Hori da zurea *iturriaren segmentua*.

1. Ekintza-barran, hautatu **Aurkitu antzeko bezeroak**.

1. Berrikusi zure segmentu berrirako iradokitako izena eta aldatu behar izanez gero.

1. Berrikusi zure segmentu berria definitzen duten eremuak. Eremu hauek zehazten dute sistemaren oinarria zure bezero iturriaren antzeko bezeroak bilatzen saiatuko dela. Sistemak gomendatutako eremuak aukeratuko ditu lehenespenez.
  Ereduaren errendimendua nabarmen murrizteko eremuak automatikoki baztertzen dira:
  
   - Datu mota hauek dituzten eremuak: StringType, BooleanType, CharType, LongType, IntType, DoubleType, FloatType, ShortType
   - 2 edo 30 baino gutxiagoko kardinalitatea (eremu bateko elementu kopurua) duten eremuak

1. Aukeratu barneratu nahi baduzu **Bezero guztiak** edo bezeroak bakarrik **Lehendik dagoen segmentu espezifikoa** zure segmentu berrian.

1. Baztertu zure iturburuko segmentuko bezeroak aukeratuz **Baztertu iturri-segmentuko denak** laukia.

1. Berez, sistemak iradokitzen du zure irteeran xede-audientziaren tamainaren % 20 soilik sartzea. Editatu atalasea behar den moduan. Atalasea handitzeak zehaztasuna murriztuko du.

1. Aukeratu **Exekutatu** orriaren behealdean sailkapen binarioko zeregin bat hasteko (Ikaskuntza automatiko metodo bat) datu multzoa aztertzen duena.

## <a name="view-the-similar-segment"></a>Ikusi antzeko segmentua

Antzeko segmentua prozesatu ondoren, zerrendan agertzen den segmentu berria aurkituko duzu **segmentuak** orria.

> [!div class="mx-imgBorder"]
> ![Antzeko bezeroen segmentua.](media/expanded-segment.png "Antzeko bezeroen segmentua")

Aukeratu **ikusi** segmentuko xehetasunak irekitzeko ekintza barran. Ikuspegi honek emaitzen banaketaren inguruko informazioa jasotzen du [antzekotasun puntuazioak](#about-similarity-scores). Antzekotasun puntuazioaren balioak ere aurkituko dituzu **Segmentuko kideen aurrebista**.

## <a name="use-the-output-of-a-similar-segment"></a>Erabili antzeko segmentu baten irteera

Ahal duzu [antzeko segmentu baten irteerarekin lan egin](segments.md) beste segmentuekin egiten duzun bezala. Adibidez, esportatu segmentua edo neurri bat eraiki.

## <a name="refresh-and-edit-a-similar-segment"></a>Eguneratu antzeko segmentua eta editatu

Antzeko segmentua freskatzeko, hautatu botoian **segmentuak** orria eta hautatu **Freskatu** ekintza barran.

Antzeko segmentua editatzean zure datuak berriro prozesatuko dira. Aurretik sortutako segmentua eguneratutako datuekin eguneratzen da.    
Antzeko segmentua editatzeko, hautatu botoian **segmentuak** orria eta hautatu **Editatu** ekintza barran. Aplikatu aldaketak eta hautatu **Exekutatu** prozesatzen hasteko.

## <a name="delete-a-similar-segment"></a>Ezabatu antzeko segmentua

Hautatu segmentua **Segmentuak** orrian eta hautatu **Ezabatu** ekintza barran. Orduan baieztatu ezabatu nahi duzula.

## <a name="about-similarity-scores"></a>Antzekotasun puntuazioari buruz

Ikaskuntza automatiko eredu bitarren sailkapenak puntuazio bat ematen die antzeko segmentuko bezeroei. Puntuazioa iturri-segmentuko bezeroek duten antzekotasunean oinarritzen da.

- Antzekotasun puntuazioak 0.55 azpitik daude sailkatutako sisteman *ez da antzekoa* iturri-segmentuko bezeroei
- Antzekotasunaren puntuazioak 0.55 eta 0.7 artean sailkatzen dira *zertxobait antzeko*
- Antzekotasunaren puntuazioak 0.7 eta 0.85 artean sailkatzen dira *antzeko*
- Antzekotasun-puntuazioak 0.85 eta 1 artekoak dira *oso antzekoak*

Ez dira ereduaren irteeraren barruan sartzen 0.4 azpitik dituzten antzekotasunak dituzten bezeroak. Sistemak ez ditu iturburu-segmentuaren antzekoak.


[!INCLUDE[footer-include](../includes/footer-banner.md)]