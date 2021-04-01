---
title: Sortu eta kudeatu segmentuak
description: Sortu bezeroen segmentuak, hainbat atributuren arabera taldekatzeko.
ms.date: 03/02/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 4a6e8a3216a2c0738d60247054afa9fc18412f55
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597036"
---
# <a name="create-and-manage-segments"></a>Sortu eta kudeatu segmentuak

Segmentuei esker, zure bezeroak demografia-, transakzio- edo portaera-atributuen arabera taldekatu ditzakezu. Segmentuak erabil ditzakezu promozio kanpainak, salmentako jarduerak eta bezeroei laguntzeko ekintzak bideratzeko, zure negozioaren helburuak lortzeko.

Iragazki konplexuak defini ditzakezu Bezero Profilaren entitatearen inguruan eta horiekin lotutako entitateak. Segmentu bakoitzak, prozesatu ondoren, bezeroen erregistro multzo bat sortzen du eta esportatu eta neurriak hartu ditzakezu. [Zerbitzuaren muga](service-limits.md) batzuk aplikatzen dira.

Besterik adierazi ezean, segmentu guztiak **Segmentu dinamikoak** dira, aldizkako antolaketan berritzen direnak.

Hurrengo adibideak segmentazio gaitasunaren erabilera ilustratzen du. Azken 90 egunetan gutxienez $500 agindu duten bezeroentzako segmentu bat zehaztu dugu *eta* bezeroarentzako arreta-zerbitzu deitu batean parte hartu zutenak eskalatu egin ziren.

> [!div class="mx-imgBorder"]
> ![Hainbat talde](media/segmentation-group1-2.png "Hainbat talde")

## <a name="create-a-new-segment"></a>Sortu segmentu berria

Segmentuak **Segmentuak** orrian kudeatzen dira.

1. Hartzaileen xehetasunetan, joan **Segmentuak** orrira.

1. Aukeratu **Berria** > **Segmentu zuria**.

1. Sarbidean **Segmentu berria** hautatu panela, eta aukeratu segmentu mota bat **izena**.

   Aukeran, eman pantailaren izena eta segmentua identifikatzen lagunduko duen deskribapena.

1. Aukeratu **hurrengo** etortzeko **Segmentuen eraikitzailea** taldea non definitzen duzun. Talde bat bezero multzo bat da.

1. Aukeratu segmentatu nahi duzun atributua barne hartzen duen entitatea.

1. Aukeratu arabera zatitu beharreko atributua. Atributu honek lau balio motetako bat izan dezake: zenbakikoa, katea, data edo boolearra.

1. Aukeratu operadorea eta balio bat hautatutako atributurako.

   > [!div class="mx-imgBorder"]
   > ![Pertsonalizatu taldeko iragazkia](media/customer-group-numbers.png "Bezeroaren taldeko iragazkia")

   |Zenbakia |Definizioa  |
   |---------|---------|
   |1     |Entity          |
   |2     |Atributua          |
   |3    |Eragilea         |
   |4    |Balioa         |

8. Erakundea bezero bateratutako entitatearekin konektatuta badago [harremanak](relationships.md), erlazio bidea zehaztu behar duzu baliozko segmentua sortzeko. Gehitu entitateak erlazio-bide honetatik hautatu dezakezu arte **Bezeroa: CustomerInsights** entitatea goitibehera. Ondoren, aukeratu **Erregistro guztiak** baldintza bakoitzerako.

   > [!div class="mx-imgBorder"]
   > ![Harreman bidea segmentuak sortzean](media/segments-multiple-relationships.png "Harreman bidea segmentuak sortzean")

1. Lehenespenez, segmentuek definitutako iragazkiekin bat datozen bezeroen profilen atributu guztiak dituen irteerako entitatea sortzen dute. Segmentu bat ez den beste entitate batzuetan oinarrituta badago *Bezeroa* entitatea, entitate hauetatik atributu gehiago gehi ditzakezu irteerako entitateari. Aukeratu **Proiektuaren atributuak** irteerako entitateari erantsiko zaizkion atributuak aukeratzeko.  

   
   Adibidez: segmentu bat bezeroarekin lotutako jarduerak dituen entitate batean oinarritzen da *Bezeroa* entitatea. Segmentuak azken 60 egunetan laguntza-mahaira deitu duten bezero guztiak bilatzen ditu. Irteerako entitatean bat datozen bezeroen erregistro guztiei deiaren iraupena eta dei kopurua eranstea aukera dezakezu. Informazio hau baliagarria izan daiteke maiz deitzen duten bezeroei lineako laguntza artikuluen eta ohiko galderen esteka lagungarriekin mezu elektronikoak bidaltzeko.

1. Segmentua gordetzeko, sakatu **Gorde**. Zure segmentua gordeko da eta prozesatu egingo da baldintza guztiak baliozkotuz gero. Bestela, zirriborro gisa gordeko da.

1. Aukeratu **Segurtasunetara itzuli** berriro ere **segmentuak** orria.

## <a name="manage-existing-segments"></a>Kudeatu lehendik dauden segmentuak

Gainean **segmentuak** orrialdean, gordetako segmentu guztiak ikusi eta kudeatu ahal izango dituzu.

Segmentu bakoitza segmentuari buruzko informazio osagarria biltzen duen errenkada batez irudikatuta dago.

Zutabeak segmentu bat ordenatu dezakezu zutabearen goiburua hautatuta.

Erabili **Bilatu** goiko eskuineko izkinan segmentuak iragazteko kutxa.

> [!div class="mx-imgBorder"]
> ![Aukerak lehendik dagoen segmentu bat kudeatzeko](media/segments-selected-segment.png "Aukerak lehendik dagoen segmentu bat kudeatzeko")

Segmentu bat hautatzean ekintza hauek erabilgarri daude:

- **ikusi** segmentuko xehetasunak, kideen zenbaketa joera segmentuko kideen aurrebista barne.
- **Editatu** segmentuak bere propietateak aldatzeko.
- **Sortu bikoiztuak** segmentu baten. Bere propietateak berehala editatzea edo bikoiztua gordetzea aukeratu dezakezu.
- **Freskatu** segmentuak azken datuak sartuko ditu.
- **Aktibatu** edo **Desaktibatu** segmentua. Segmentuek bi egoera posible dituzte: aktiboak edo inaktiboak. Egoera hauek oso ondo etortzen dira segmentu bat editatzerakoan. Segmentu inaktiboetan, segmentuaren definizioa badago, baina oraindik ez du bezeroik. Segmentu bat aktibatzean, egoera "inaktibo" izatetik "aktibo" izatera pasatzen da eta segmentuaren definizioarekin bat datozen bezeroak bilatzen hasiko da. A bada [freskatze programatua](system.md#schedule-tab) konfiguratuta dago, segmentu inaktiboek dute **Egoera** gisa zerrendatuta **Saltatuta**, freskatzen saiatu ere ez zela egin adieraziz. Segmentu inaktiboa aktibatzen denean, freskatu egingo da eta programatutako freskapenetan sartuko da.
  Bestela, erabil dezakezu **Ordutegiak beranduago** funtzionaltasuna **Aktibatu / Desaktibatu** goitibehera, segmentu jakin bat aktibatzeko eta desaktibatzeko etorkizuneko data eta ordua zehazteko.
- **Aldatu izena** segmentuari.
- **Deskargatu** .CSV fitxategi gisa segmentuko kideen zerrenda.
- **Gehitu** aukerak segmentuan dauden bezeroen IDen zerrenda bidaltzen du beste aplikazio batean prozesatzeko.
- **Ezabatu** segmentua.

## <a name="refresh-segments"></a>Freskatu segmentuak

Segmentu guztiak freskatu ditzakezu aldi berean hautatuta **Freskatu guztiak** gainean **segmentuak** orrialdea edo segmentu bat edo gehiago freskatu ditzakezu hautatzen dituzunean eta aukeratutakoan **Freskatu** aukeren artean. Bestela, berriztagarria den aldizka konfigura dezakezu **administratzailea** > **Sistema** > **Ordutegiak**.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="download-and-export-segments"></a>Deskargatu eta esportatu segmentuak

Zure segmentuak CSV fitxategi batera deskarga ditzakezu edo Dynamics 365 Sales-era esportatu.

### <a name="download-segments-to-a-csv-file"></a>Deskargatu segmentuak CSV fitxategi batera

1. Hartzaileen xehetasunetan, joan **Segmentuak** orrira.

2. Hautatu elipsia segmentu jakin bateko fitxan.

3. Aukeratu **Deskargatu CSV gisa** ekintzen goitibeherako zerrendatik.

### <a name="export-segments-to-dynamics-365-sales"></a>Esportatu segmentuak Dynamics 365 Sales-era

Dynamics 365 Sales-en segmentuak esportatu aurretik, administratzaile bat behar da [sortu esportazio-helmuga](export-destinations.md) Dynamics 365 Sales-erako.

1. Hartzaileen xehetasunetan, joan **Segmentuak** orrira.

2. Hautatu elipsia segmentu jakin bateko fitxan.

3. Aukeratu **Gehitu** ekintzen goitibeherako zerrendatik eta hautatu datuak bidali nahi dituzun esportazio helmuga.

## <a name="draft-mode-for-segments"></a>Zirriborroen modua segmentuetarako

Segmentu bat prozesatzeko baldintza guztiak betetzen ez badira, segmentua zirriborro gisa gorde dezakezu eta sar itzazu **segmentuak** orria.

Segmentu aktibo gisa gordeko da eta ezin da aktibatu baliozkoa izan arte.

## <a name="add-more-conditions-to-a-group"></a>Gehitu baldintza gehiago taldeari

Talde bati baldintza gehiago gehitzeko, bi operadore logiko erabil ditzakezu:

- **ETA** operadorea: Bi baldintza segmentazio prozesuaren baitan bete behar dira. Aukera hau baliagarria da entitate desberdinetan baldintzak definitzen dituzunean.

- **EDO** operadorea: Baldintzaren bat segmentazio prozesuaren zati gisa bete behar da. Aukera hau oso baliagarria da hainbat baldintza definitzen dituzunean entitate berarentzat.

   > [!div class="mx-imgBorder"]
   > ![EDO baldintza bat bete behar den operadorea](media/segmentation-either-condition.png "EDO baldintza bat bete behar den operadorea")

Gaur egun, habia habia egin daiteke **EDO** operadorea **ETA** operadorea, baina ez alderantziz.

## <a name="combine-multiple-groups"></a>Konbinatu hainbat talde

Talde bakoitzak bezero multzo zehatz bat sortzen du. Talde horiek konbinatu ditzakezu zure negoziorako behar diren bezeroak sartzeko.

1. Hartzaileen xehetasunetan, joan hona: **Segmentuak** orrira eta hautatu segmentu bat.

2. Hautatu **Gehitu taldea**.

   > [!div class="mx-imgBorder"]
   > ![Bezeroen taldea gehitzeko taldea](media/customer-group-add-group.png "Bezeroen taldea gehitzeko taldea")

3. Hautatu multzo multzo hauetako eragileetako bat: **Batura**, **Gurutzatu**, edo **Salbu**.

   > [!div class="mx-imgBorder"]
   > ![Bezeroen taldea gehitzeko bateratzea](media/customer-group-union.png "Bezeroen taldea gehitzeko bateratzea")

   Hautatu multzo operatiboa talde berria definitzeko. Gorde talde desberdinak, zer datu mantentzen diren zehazteko:

   - **Bateratzea** bi taldeak batzen ditu.

   - **Gurutzatu** bi taldeak gainjartzen ditu. Bi taldeetako datu *komunak* soilik mantentzen dira talde bateratuan.

   - **Salbuespena** bi taldeak batzen ditu. A eta B talde bietan *ez dauden* datuak soilik mantentzen dira.

## <a name="view-processing-history-and-segment-members"></a>Ikusi prozesaketaren historia eta segmentuko kideak

Segurtasun bati buruzko datu bateratuak ikus ditzakezu haren xehetasunak berrikusiz.

**Segmentuak** orrian, hautatu berrikusi nahi duzun segmentua.

Orriaren goiko aldean joera grafikoa dago, kideen zenbateko aldaketak bistaratzen dituena. Pasa datuak gainetik kideak data jakin batean ikusteko.

Bistaratzeko denbora-markoa eguneratu dezakezu.

> [!div class="mx-imgBorder"]
> ![Segmentuaren denbora-tartea](media/segment-time-range.png "Segmentuaren denbora-tartea")

Beheko aldean segmentuko kideen zerrenda dago.

> [!NOTE]
> Zerrenda honetan agertzen diren eremuak zure segmentuko entitateen atributuetan oinarrituta daude.
>
>Zerrenda bat datorren segmentuko kideen aurrebista da eta zure segmentuko lehen 100 erregistroak erakusten ditu, behar bezala baloratu eta haren definizioak berrikusteko. Bat datozen erregistro guztiak ikusteko, beharrezkoa da [esportatu segmentua](export-destinations.md).

## <a name="quick-segments"></a>Segmentu azkarrak

Segmentu-egileaz gain, segmentuak sortzeko beste bide bat dago. Segmentu azkarrek segmentu errazak (operadore bakarrarekin) eraiki eta berehala eskaintzen dizute.

1. Gainean **segmentuak** orria, hautatu **Berria** > **Sortu azkar**.

   - Hautatu botoia **profilak** Aukeratutako bezeroaren entitatean oinarritutako segmentu bat eraikitzeko aukera.
   - Hautatu botoia **Neurriak** Aukera hau aurrez sortu dituzun bezeroarentzako atributu mota bakoitzaren inguruan segmentu bat eraikitzeko **Neurriak** orria.
   - Hautatu botoia **Adimen** Aukera hau bai erabiliz sortu duzun irteerako entitateetako baten inguruan eraikitzeko aukera **iragarpenak** edo **Neurrira egindako ereduak** gaitasunak.

2. Sarbidean **Segmentu azkar berria** elkarrizketa-koadroan, hautatu atributu bat **eremua** goitibeherako menuko.

3. Sistemak ikuspegi osagarriak emango ditu zure bezeroen segmentu hobeak sortzen lagunduko dutenak.
   - Eremu kategorikoetarako, 10 bezero zenbatuko ditugu. Hautatu **Balio** bat eta hautatu **Berrikusi**.

   - Zenbakizko atributu bat lortzeko, sistemak erakutsiko du zer atributu-balioa eroriko den bezero bakoitzaren portzentalaren azpian. Aukeratu bat **Operadorea** eta **Balioa** eta hautatu **Berrikusi**.

4. Sistemak zurekin hornituko zaitu **Segurtasunaren neurria**. Definitu duzun segmentua sortu edo aukeratu dezakezu edo, bestela, berrikusi beste segmentu baten tamaina lortzeko.

    > [!div class="mx-imgBorder"]
    > ![Izena eta estimazioa segmentu azkar baterako](media/quick-segment-name.png "Izena eta estimazioa segmentu azkar baterako")

5. Jarri **izena** zure segmentuari. Nahi baduzu, eman **Bistaratzeko izena**.

6. Segmentua sortzeko, sakatu **Gorde**.

7. Segmentua prozesatu ondoren, sortu duzun beste edozein segmentu bezala ikus dezakezu.

Hurrengo agertokietarako, gomendatzen dugu segmentu eraikitzailea erabiltzea gomendatutako segmentuen gaitasuna baino:

- Segurtasunak sortzen iragazkiak eremu kategorietan operadorea ez den beste eremuetan **da** operadorea
- Segmentuak sortu iragazkiak zenbaki-eremuetan, operadorea baino desberdinak direnetan **bitarte honetan**, **Baino handiagoa**, eta **Baino gutxiago** operadore
- Data-motako eremuetan iragazkiak dituzten segmentuak sortzen

## <a name="next-steps"></a>Hurrengo urratsak

[Esportatu segmentua](export-destinations.md) eta esploratu [Bezero txartela](customer-card-add-in.md) eta [Konektoreak](export-power-bi.md) bezeroaren mailari buruzko informazioa lortzeko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]