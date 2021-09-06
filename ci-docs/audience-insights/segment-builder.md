---
title: Sortu eta kudeatu segmentuak
description: Sortu bezeroen segmentuak, hainbat atributuren arabera taldekatzeko.
ms.date: 07/18/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: e759872643cc7387cf732d73c7a320ae8901e5a9
ms.sourcegitcommit: 42692a815695b9fdc93b9358eae09f2c3e97293c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "7377773"
---
# <a name="create-and-manage-segments"></a>Sortu eta kudeatu segmentuak

> [!IMPORTANT]
> 2021eko irailean segmentua sortzeko esperientziari buruzko hainbat aldaketa gauzatu dira: 
> - Segmentuen eraikitzaileak itxura desberdina izango du birziklatutako elementuekin eta erabiltzaileen fluxu hobearekin.
> - Data-ordu operadore berriak eta data-hautatzaile hobetua gaituta daude segmentu-sortzailean.
> - Segmentuen baldintzak eta arauak gehitu edo kendu ahal izango dituzu. 
> - OR baldintzarekin hasten diren arau habiaratuak erabilgarri egongo dira. Jada ez duzu AND baldintzarik kanpoko geruzan.
> - Atributuak hautatzeko alboko panela erabilgarri egongo da etengabe.
> - Entitate erlazio bideak hautatzeko aukera.
> Segmentu-sortzaile berria probatzeko, bidali mezu elektroniko bat "Segmentu-eraikitzaile berria gaitzeko eskaera" gaiari heltzeko [at] microsoft.com helbidera. Sartu zure erakundearen izena eta zure sandbox ingurunearen IDa.
> :::image type="content" source="media/segment-builder-overview.png" alt-text="Segmentu-sortzailearen elementuak." lightbox="media/segment-builder-overview.png":::
>
> 1 - Antolatu zure segmentua arau eta azpi arauekin. Arau edo azpi-arau bakoitza baldintzez osatuta dago. Konbinatu baldintzak eragile logikoekin
>
> 2 - Aukeratu [harreman bidea](relationships.md) arau bati aplikatzen zaion entitateen artean. Harreman-bideak baldintza batean zein atributu erabil daitezkeen zehazten du.
>
> 3 - Kudeatu arauak eta azpi-arauak. Arau baten kokapena aldatu edo ezabatu.
>
> 4 - Gehitu baldintzak eta eraiki habia maila egokia azpi-arauak erabiliz.
>
> 5 - Aplikatu multzo eragiketak konektatutako arauei.
>
> 6 - Erabili atributuen panela eskuragarri dauden entitateen atributuak gehitzeko edo atributuetan oinarritutako baldintzak sortzeko. Panelak hautatutako araurako erabilgarri dauden hautatutako harreman bideen arabera oinarritutako entitate eta atributuen zerrenda erakusten du.
>
> 7 - Gehitu atributuetan oinarritutako baldintzak lehendik dauden arau eta azpiurrei edo gehitu arau berri bati.
>
> 8 - Desegin eta berregin aldaketak segmentua eraikitzean.

Definitu iragazki konplexuak bezero entitate bateratuaren eta hari lotutako entitateen inguruan. Segmentu bakoitzak, prozesatu ondoren, bezeroen erregistro multzo bat sortzen du eta esportatu eta neurriak hartu ditzakezu. Segmentuak **Segmentuak** orrian kudeatzen dira. 

Hurrengo adibideak segmentazio gaitasunaren erabilera ilustratzen du. Azken 90 egunetan gutxienez $500 agindu duten bezeroentzako segmentu bat zehaztu dugu *eta* bezeroarentzako arreta-zerbitzu deitu batean parte hartu zutenak eskalatu egin ziren.

:::image type="content" source="media/segmentation-group1-2.png" alt-text="Segmentu-sortzailearen UIren pantaila-argazkia bezero segmentu bat zehazten duten bi taldeekin.":::

## <a name="create-a-new-segment"></a>Sortu segmentu berria

Segmentu berri bat sortzeko hainbat modu daude. Atal honetan a nola sortu deskribatzen da *segmentu hutsa* hutsetik. A ere sor dezakezu *segmentu azkarra* dauden entitateetan oinarrituta edo lortzeko Ikaskuntza automatiko ereduak *iradokitako segmentuak*. Informazio gehiago lortzeko: [Segmentuen informazio orokorra](segments.md).

Segmentua sortu bitartean, zirriborroa gorde dezakezu. Segmentu inaktibo gisa gordeko da eta ezin da aktibatu baliozko konfigurazio batekin amaituta.

1. Zoaz **Segmentuak** orrira.

1. Aukeratu **Berria** > **Segmentu zuria**.

1. **Segmentu berria** panelean, aukeratu segmentu mota bat:

   - **Segmentu dinamikoak** [freskatu](segments.md#refresh-segments) aldizkako ordutegian.
   - **Segmentu estatikoak** exekutatu behin sortzen duzunean.

1. Eman **Irteerako entitatearen izena** segmenturako. Aukeran, eman pantailaren izena eta segmentua identifikatzen lagunduko duen deskribapena.

1. Aukeratu **hurrengo** etortzeko **Segmentuen eraikitzailea** taldea non definitzen duzun. Talde bat bezero multzo bat da.

1. Aukeratu segmentatu nahi duzun atributua barne hartzen duen entitatea.

1. Aukeratu arabera zatitu beharreko atributua. Atributu honek lau balio motetako bat izan dezake: zenbakikoa, katea, data edo boolearra.

1. Aukeratu operadorea eta balio bat hautatutako atributurako.

   > [!div class="mx-imgBorder"]
   > ![Pertsonalizatu taldeko iragazkia.](media/customer-group-numbers.png "Bezeroaren taldeko iragazkia")

   |Zenbakia |Definizioa  |
   |---------|---------|
   |1     |Entity          |
   |2     |Atributua          |
   |3    |Eragilea         |
   |4    |Balioa         |

   1. Talde bati baldintza gehiago gehitzeko, bi operadore logiko erabil ditzakezu:

      - **ETA** operadorea: Bi baldintza segmentazio prozesuaren baitan bete behar dira. Aukera hau baliagarria da entitate desberdinetan baldintzak definitzen dituzunean.

      - **EDO** operadorea: Baldintzaren bat segmentazio prozesuaren zati gisa bete behar da. Aukera hau oso baliagarria da hainbat baldintza definitzen dituzunean entitate berarentzat.

      > [!div class="mx-imgBorder"]
      > ![EDO baldintza bat bete behar den operadorea.](media/segmentation-either-condition.png "EDO baldintza bat bete behar den operadorea")

      Gaur egun, habia habia egin daiteke **EDO** operadorea **ETA** operadorea, baina ez alderantziz.

   1. Talde bakoitza bezero multzoarekin bat dator. Taldeak konbinatu ditzakezu zure negozio kasurako behar diren bezeroak sartzeko.    
   Hautatu **Gehitu taldea**.

      > [!div class="mx-imgBorder"]
      > ![Bezeroen taldea gehitzeko taldea.](media/customer-group-add-group.png "Bezeroen taldea gehitzeko taldea")

   1. Aukeratu multzo operadoreetako bat: **Batasuna**, **Elkartu**, edo **Izan ezik**.

   > [!div class="mx-imgBorder"]
   > ![Bezeroen taldea gehitzeko bateratzea.](media/customer-group-union.png "Bezeroen taldea gehitzeko bateratzea")

   - **Bateratzea** bi taldeak batzen ditu.

   - **Gurutzatu** bi taldeak gainjartzen ditu. Bi taldeetako datu *komunak* soilik mantentzen dira talde bateratuan.

   - **Salbuespena** bi taldeak batzen ditu. A eta B talde bietan *ez dauden* datuak soilik mantentzen dira.

1. Erakundea bezero bateratutako entitatearekin konektatuta badago [harremanak](relationships.md), erlazio bidea zehaztu behar duzu baliozko segmentua sortzeko. Gehitu entitateak erlazio-bide honetatik hautatu dezakezu arte **Bezeroa: CustomerInsights** entitatea goitibehera. Ondoren, aukeratu **Erregistro guztiak** urrats bakoitzerako.

   > [!div class="mx-imgBorder"]
   > ![Harreman bidea segmentuak sortzean.](media/segments-multiple-relationships.png "Harreman bidea segmentuak sortzean")

1. Lehenespenez, segmentuek definitutako iragazkiekin bat datozen bezeroen profilen atributu guztiak dituen irteerako entitatea sortzen dute. Segmentu bat ez den beste entitate batzuetan oinarrituta badago *Bezeroa* entitatea, entitate hauetatik atributu gehiago gehi ditzakezu irteerako entitateari. Aukeratu **Proiektuaren atributuak** irteerako entitateari erantsiko zaizkion atributuak aukeratzeko.  
  
   Adibidez: segmentu bat bezeroarekin lotutako jarduerak dituen entitate batean oinarritzen da *Bezeroa* entitatea. Segmentuak azken 60 egunetan laguntza-mahaira deitu duten bezero guztiak bilatzen ditu. Irteerako entitatean bat datozen bezeroen erregistro guztiei deiaren iraupena eta dei kopurua eranstea aukera dezakezu. Informazio hau baliagarria izan daiteke maiz deitzen duten bezeroei lineako laguntza artikuluen eta ohiko galderen esteka lagungarriekin mezu elektronikoak bidaltzeko.

   > [!NOTE]
   > - Proiektatutako atributuek bezeroaren entitatearekin bat-bateko harremana duten entitateentzat bakarrik funtzionatzen dute. Adibidez, bezero batek harpidetza ugari izan ditzake.
   > - Eraikitzen ari zaren segmentu kontsulta talde guztietan erabiltzen den entitate bateko atributuak soilik proiekta ditzakezu.
   > - Multzo operadoreak erabiltzean proiektatutako atributuak kontuan hartzen dira.

1. Segmentua gordetzeko, sakatu **Gorde**. Zure segmentua gordeko da eta prozesatu egingo da baldintza guztiak baliozkotuz gero. Bestela, zirriborro gisa gordeko da.

1. Aukeratu **Segurtasunetara itzuli** berriro ere **segmentuak** orria.



## <a name="quick-segments"></a>Segmentu azkarrak

Segmentu bizkorrek segmentu sinpleak operadore bakar batekin azkar eraikitzeko aukera ematen dute ikuspegi azkarragoak lortzeko.

1. **Segmentuak** orrian, hautatu **Berria** > **Sortu honetatik**.

   - Hautatu **Profilak** aukera *bateratutako bezeroaren* entitatean oinarritutako segmentu bat eraikitzeko aukera.
   - Aukeratu **Neurriak** aukera sortu aurretik sortutako neurrien inguruan segmentu bat eraikitzeko.
   - Hautatu botoia **Adimen** Aukera hau bai erabiliz sortu duzun irteerako entitateetako baten inguruan eraikitzeko aukera **iragarpenak** edo **Neurrira egindako ereduak** gaitasunak.

2. Sarbidean **Segmentu azkar berria** elkarrizketa-koadroan, hautatu atributu bat **eremua** goitibeherako menuko.

3. Sistemak ikuspegi osagarriak emango ditu zure bezeroen segmentu hobeak sortzen lagunduko dutenak.
   - Eremu kategorikoetarako, 10 bezero zenbatuko ditugu. Hautatu **Balio** bat eta hautatu **Berrikusi**.

   - Zenbakizko atributu bat lortzeko, sistemak erakutsiko du zer atributu-balioa eroriko den bezero bakoitzaren portzentalaren azpian. Aukeratu bat **Operadorea** eta **Balioa** eta hautatu **Berrikusi**.

4. Sistemak zurekin hornituko zaitu **Segurtasunaren neurria**. Definitu duzun segmentua sortu edo aukeratu dezakezu edo, bestela, berrikusi beste segmentu baten tamaina lortzeko.

    > [!div class="mx-imgBorder"]
    > ![Izena eta estimazioa segmentu azkar baterako.](media/quick-segment-name.png "Izena eta estimazioa segmentu azkar baterako")

5. Jarri **izena** zure segmentuari. Nahi baduzu, eman **Bistaratzeko izena**.

6. Segmentua sortzeko, sakatu **Gorde**.

7. Segmentua prozesatu ondoren, sortu duzun beste edozein segmentu bezala ikus dezakezu.

## <a name="next-steps"></a>Hurrengo urratsak

[Esportatu segmentu bat](export-destinations.md) eta esploratu [Bezeroen txartelaren integrazioa](customer-card-add-in.md) segmentuak beste aplikazio batzuetan erabiltzeko.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
