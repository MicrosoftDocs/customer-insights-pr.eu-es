---
title: Bilatu antzeko bezeroak AI (aurrebista) (bideoa dauka)
description: Aurkitu antzeko bezeroen segmentuak adimen artifizialarekin.
ms.date: 03/25/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-segment-builder
- ci-segment-insights
- customerInsights
ms.openlocfilehash: 09fe36a4da45d114cbfccf8dad1e7b80b4b7e320
ms.sourcegitcommit: 8a28e9458b857adf8e90e25e43b9bc422ebbb2cd
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/18/2022
ms.locfileid: "9170712"
---
# <a name="find-similar-customers-with-ai-preview"></a>Bilatu antzeko bezeroak AIarekin (aurrebista)

Aurkitu zure bezero basean antzeko bezeroak adimen artifiziala erabiliz. Eginbide hau erabiltzeko gutxienez segmentu bat sortu behar duzu. Lehendik dagoen segmentu baten irizpideak zabaltzeak segmentu horren antzekoak diren bezeroak aurkitzen laguntzen du.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWOFou]

> [!NOTE]
> *Bilatu antzeko bezeroak* bitarteko automatizatuak erabiltzen ditu datuak ebaluatzeko eta datu horietan oinarrituta iragarpenak egiteko. Beraz, profilak egiteko metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Erregelamendu Orokorrak ("GDPR") definitzen baitu. Bezeroak funtzio hau erabiltzeko datuak prozesatzeko DBAO edo beste lege edo arau batzuen menpe egon daiteke. Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, iragarpenez aplikagarriak diren lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.

## <a name="find-similar-customers"></a>Bilatu antzeko bezeroak

1. Joan **Segmentuak** eta hautatu segmentu berria oinarritu nahi duzun segmentua. Hori da zurea *iturriaren segmentua*.

1. Hautatu **Bilatu antzeko bezeroak**.

1. Berrikusi zure segmentu berrirako iradokitako izena eta aldatu behar izanez gero.

1. Aukeran, gehitu [etiketak](work-with-tags-columns.md#manage-tags) segmentu berrira.

1. Berrikusi zure segmentu berria definitzen duten eremuak. Eremu hauek zehazten dute sistemaren oinarria zure bezero iturriaren antzeko bezeroak bilatzen saiatuko dela. Sistemak gomendatutako eremuak hautatzen ditu lehenespenez. Behar izanez gero, gehitu eremu gehiago.
  Ereduaren errendimendua nabarmen murrizteko eremuak automatikoki baztertzen dira:
  
   - Datu mota hauek dituzten eremuak: StringType, BooleanType, CharType, LongType, IntType, DoubleType, FloatType, ShortType
   - 2 edo 30 baino gutxiagoko kardinalitatea (eremu bateko elementu kopurua) duten eremuak

1. Aukeratu sartu nahi duzun ala ez **Bezero guztiak** iturburu-segmentua izan ezik edo bezeroak soilik batean **segmentu ezberdina** zure segmentu berrian.

1. Berez, sistemak iradokitzen du zure irteeran xede-audientziaren tamainaren % 20 soilik sartzea. Editatu atalasea behar den moduan. Atalasea handitzeak zehaztasuna murriztuko du.

1. Sartu bezeroak zure iturburu-segmentuan hautatuta **Sartu iturri-segmentuko kideak antzeko atributuak dituzten bezeroez gain** kontrol-laukia.

1. Hautatu **Korrika egin** orriaren behealdean a hasteko [Sailkapen zeregin bitarra](#about-similarity-scores) (Ikaskuntza automatiko metodoa) datu multzoa aztertzen duena.

## <a name="view-the-similar-segment"></a>Ikusi antzeko segmentua

Antzeko segmentua prozesatu ondoren, atalean zerrendatutako segmentu berria aurkituko duzu **Segmentuak** orria motarekin **Hedapena**.

Hautatu **Ikusi** emaitzaren banaketa ikusteko [antzekotasun puntuazioak](#about-similarity-scores) eta antzekotasun puntuazioaren balioak azpian **Segmentuko kideen aurrebista**.

:::image type="content" source="media/expanded-segment.png" alt-text="Antzeko bezeroen segmentua.":::

## <a name="manage-a-similar-segment"></a>Kudeatu antzeko segmentu bat

[Antzeko segmentu batekin lan egin eta kudeatu](segments.md#manage-existing-segments) beste segmentuekin egiten duzun bezala. Adibidez, esportatu segmentua edo neurri bat eraiki.

Editatu, freskatu, aldatu izena, deskargatu eta ezabatu antzeko segmentu bat. Antzeko segmentu bat editatzeak zure datuak birprozesatzen ditu. Aurretik sortutako segmentua eguneratutako datuekin eguneratzen da.

## <a name="about-similarity-scores"></a>Antzekotasun puntuazioari buruz

Ikaskuntza automatiko eredu bitarren sailkapenak puntuazio bat ematen die antzeko segmentuko bezeroei. Puntuazioa iturri-segmentuko bezeroek duten antzekotasunean oinarritzen da.

- Antzekotasun puntuazioak 0.55 azpitik daude sailkatutako sisteman *ez da antzekoa* iturri-segmentuko bezeroei
- Antzekotasunaren puntuazioak 0.55 eta 0.7 artean sailkatzen dira *zertxobait antzeko*
- Antzekotasunaren puntuazioak 0.7 eta 0.85 artean sailkatzen dira *antzeko*
- Antzekotasun-puntuazioak 0.85 eta 1 artekoak dira *oso antzekoak*

Ez dira ereduaren irteeraren barruan sartzen 0.4 azpitik dituzten antzekotasunak dituzten bezeroak. Sistemak ez ditu iturburu-segmentuaren antzekoak.

[!INCLUDE [footer-include](includes/footer-banner.md)]
