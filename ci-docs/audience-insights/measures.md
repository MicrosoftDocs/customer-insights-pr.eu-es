---
title: Sortu eta editatu neurriak
description: Bezeroekin erlazionatutako neurriak definitzea zenbait negozio-arloren errendimendua aztertzeko eta islatzeko.
ms.date: 10/15/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: wameng
manager: shellyha
ms.openlocfilehash: 0e214a6eb66abd27f7292db3ce2c2a6e16a8ff33
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404995"
---
# <a name="define-and-manage-measures"></a>Neurriak zehaztu eta kudeatu

**Neurriak** negozio-arlo jakin batzuen errendimendua eta osasuna islatzen dituzten funtsezko errendimenduen adierazleak (KPI) adierazten dituzte. Hartzaileen xehetasunek neurri mota desberdinak eraikitzeko esperientzia intuitiboa eskaintzen dute, neurriak eskuz kodifikatu edo balidatzea eskatzen ez duen kontsulta-sortzailea erabiliz. Zure negozio neurriak jarrai ditzakezu **Hasiera** orrialdean, ikus bezero zehatzentzako neurriak hemen **Bezero txartela** eta erabili neurriak bezeroaren segmentuak definitzeko **segmentu** orria.

## <a name="create-a-measure"></a>Sortu neurri bat

Atal honetan neurritik hutsetik ibiltzen zara. Neurri bat eraiki dezakezu Bezeroaren entitatearen bidez konektatutako datu-iturri ugarietatik. [Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.

1. Hartzaileei buruzko xehetasunetan, joan hona: **Neurriak**.

2. Hautatu **Neurri berria**.

3. Aukeratu neurria **Mota**:

   - **Bezeroaren atributua**: Bezero bakoitzeko puntu bakarra, puntuazioa, balioa edo egoera islatzen duena. Bezeroaren atributuak sistema sortutako entitate berri batean atributu gisa sortzen dira **Customer_Measure**.

   - **Bezeroaren neurria**: Aukeratutako neurrien arabera, bezeroen portaerari buruzko ikuspegi orokorrak. Entitate berri bat sortzen da neurri bakoitzerako, potentzialki bezero bakoitzeko erregistro anitzekin.

   - **Negozio neurria**: Zure negozioaren errendimendua eta osasuna kontrolatzen ditu. Enpresa-neurriek bi irteera desberdin izan ditzakete: etan agertzen den zenbakizko irteera **Hasiera** orrialdean edo aurkitzen duzun entitate berri batean **erakundeak** orria.

4. Eman a **izena** eta aukerakoa **Bistaratu izena** eta hautatu **Hurrengoa**.

5. **Entitatea** atalean, goitibeherako zerrendan, hautatu lehenengo entitatea. Puntu honetan, entitate osagarriak beharrezkoak diren erabaki beharko zenuke neurriaren definizioaren barruan.

   > [!div class="mx-imgBorder"]
   > ![Neurketaren definizioa](media/measure-definition.png "Neurketaren definizioa")

   Entitate gehiago gehitzeko, hautatu **Entitatea gehitu** eta hautatu neurria erabili nahi duzun entitateak.

   > [!NOTE]
   > Soilik hasten ari zaren zuren entitatearekin harremanak dituzten entitateak aukera ditzakezu. Harremanak definitzeari buruz informazio gehiago lortzeko, ikusi [Harremanak](relationships.md).

6. Aukeran, aldagaiak konfigura ditzakezu. **Aldagaiak** atalean, hautatu **Aldagai berria**.

   Aldagaiak zure hautatutako erregistro bakoitzean egiten diren kalkuluak dira. Adibidez, zure salmentako puntuen salmenta (POS) eta lineako salmentak zure bezeroen erregistro bakoitzerako.

7. Jarri **izena** aldagaiari.

8. Sarbidean **Adierazpen** aukeratu eremua zure kalkuluarekin hasteko.

9. Idatzi adierazpen bat teklean **Adierazpen** eremua zure kalkuluan sartu beharreko eremu gehiago aukeratzen dituzun bitartean.

   > [!NOTE]
   > Gaur egun, adierazpen aritmetikoak soilik onartzen dira. Gainera, aldagaien kalkulua ez da onartzen hainbat entitaterentzat [entitate bideak](relationships.md).

10. Hautatu **Eginda**.

11. Sarbidean **Neurrien definizioa** atalean, zure entitate aukeratuak eta kalkulatutako aldagaiak neurri-entitate edo atributu berri batean nola agregatzen diren zehaztuko duzu.

12. Hautatu **Dimentsio berria**. Dimentsio bat bezala pentsa dezakezu *taldeka* funtzioa. Zure Neurri entitatearen edo atributuaren irteera datuak zehaztutako dimentsio guztien arabera taldekatuko dira.

    > [!div class="mx-imgBorder"]
    > ![Aukeratu ziklo agregatua](media/measures-businessreport-measure-definition2.png "Aukeratu ziklo agregatua")

    Hautatu edo sartu informazio hau zure dimentsioaren definizioaren zati gisa:

    - **Erakunde**: Neurketa entitate bat definitzen baduzu, gutxienez atributu bat izan beharko luke. Neurrien atributu bat definitzen baduzu, atributu bakarra sartuko du lehenespenez. Aukeraketa atributu hori biltzen duen entitatea aukeratzeari buruzkoa da.
    - **eremua**: Aukeratu ezazu zure Neurketa entitatean edo atributuan sartu beharreko atributua.
    - **Ontzia**: Egunero, hilero edo urtero datuak batu nahi dituzun aukeratu. Beharrezko hautapena da Data motako atributu bat hautatu baduzu bakarrik.
    - **Hurrengoa bezala**: Zure eremu berriaren izena definitzen du.
    - **Bistaratu izena**: Zure eremuaren bistaratzeko izena definitzen du.

    > [!NOTE]
    > Zure negozio neurria zenbaki bakarreko entitate gisa gordeko da eta hemen agertuko da **Hasiera** orrialdea neurriari neurri gehiago gehitzen ez bazaio. Neurri gehiago gehitu ondoren, neurriak hala egingo du *ez* erakutsi **Hasiera** orria.

13. Aukeran, gehitu funtzioak. Zure neurrien erakundearen edo atributuaren barruan balio berri bat sortzen da. Onartutako agregazio funtzioak hauek dira: **Min**, **Max**, **Batez beste**, **mediana**, **batura**, **Kontu bakarra**, **Lehen** (dimentsioaren balio baten lehenengo erregistroa hartzen du), eta **Azken** (azken erregistroa neurri erantsiko balioa hartzen du).

14. Hautatu **Gorde** zure aldaketak neurriari aplikatzeko.

## <a name="manage-your-measures"></a>Kudeatu neurriak

Neurri bat gutxienez sortu ondoren, neurrien zerrenda ikusiko duzu **Neurriak** orrian.

Neurri motaren inguruko informazioa aurkituko duzu, sortzailea, sortze data eta ordua, azken edizio data eta ordua, egoera (neurria aktiboa den ala ez, aktiboa ala huts egin) eta azken egunera eta ordua freskatzeko. Zerrendako neurri bat hautatzen duzunean, bere irteeraren aurrebista ikus dezakezu.

Neurri guztiak aldi berean freskatzeko, hautatu **Freskatu guztiak** neurri zehatz bat aukeratu gabe.

> [!div class="mx-imgBorder"]
> ![Neurri bakarrak kudeatzeko ekintzak](media/measure-actions.png "Neurri bakarrak kudeatzeko ekintzak")

Bestela, hautatu zerrendako neurri bat eta egin ekintza hauetako bat:

- Hautatu neurriaren izena, haren xehetasunak ikusteko.
- **Editatu** neurriaren konfigurazioa.
- **Aldatu izena** neurria.
- **Ezabatu** neurria.
- Hautatu elipsia (...) eta gero **Freskatu** neurriaren freskatze prozesua hasteko.
- Hautatu elipsia (...) eta gero **Deskargatu** neurriaren .CSV fitxategia lortzeko.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="next-step"></a>Hurrengo urratsa

Lehendik dauden neurriak erabiltzen dituzu zure lehenengo bezero segmentua sortzeko **segmentuak** orria. Informazio gehiago lortzeko, [Segmentuak](segments.md).
