---
title: Sortu segmentuak segmentu-egilearekin
description: Sortu bezeroen segmentuak, hainbat atributuren arabera taldekatzeko.
ms.date: 09/07/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 7f7bd0e7e581305836287bd503ef273a2d556bff
ms.sourcegitcommit: fecdee73e26816c42d39d160d4d5cfb6c8a91596
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/15/2021
ms.locfileid: "7494476"
---
# <a name="create-segments"></a>Sortu segmentuak

Definitu iragazki konplexuak bezero entitate bateratuaren eta hari lotutako entitateen inguruan. Segmentu bakoitzak, prozesatu ondoren, bezeroen erregistro multzo bat sortzen du eta esportatu eta neurriak hartu ditzakezu. Segmentuak **Segmentuak** orrian kudeatzen dira. [Segmentu berriak sortu](#create-a-new-segment) ditzakezu [segmentu-egile](#segment-builder) berria erabiliz edo [segmentu azkarrak sortu](#quick-segments) aplikazioko beste eremuetatik.

## <a name="segment-builder"></a>Segmentu-egilea

Irudi honek segmentu-sortzailearekin hainbat alderdi adierazten ditu. Bezero talde bat bilakatzen den segmentu bat erakusten du. Bezeroek ondasunak eskatu zituzten denbora-tarte jakin batean eta sari gisako puntu batzuk bildu edo diru kopuru jakin bat gastatu zuten. 

:::image type="content" source="media/segment-builder-overview.png" alt-text="Segmentu-sortzailearen elementuak." lightbox="media/segment-builder-overview.png":::

1 - Antolatu zure segmentua arau eta azpi arauekin. Arau edo azpi-arau bakoitza baldintzez osatuta dago. Konbinatu baldintzak eragile logikoekin

2 - Aukeratu [harreman bidea](relationships.md) arau bati aplikatzen zaion entitateen artean. Harreman-bideak baldintza batean zein atributu erabil daitezkeen zehazten du.

3 - Kudeatu arauak eta azpi-arauak. Arau baten kokapena aldatu edo ezabatu.

4 - Gehitu baldintzak eta eraiki habia maila egokia azpi-arauak erabiliz.

5 - Aplikatu multzo eragiketak konektatutako arauei.

6 - Erabili atributuen panela eskuragarri dauden entitateen atributuak gehitzeko edo atributuetan oinarritutako baldintzak sortzeko. Panelak hautatutako araurako erabilgarri dauden hautatutako harreman bideen arabera oinarritutako entitate eta atributuen zerrenda erakusten du.

7 - Gehitu atributuetan oinarritutako baldintzak lehendik dauden arau eta azpiurrei edo gehitu arau berri bati.

8 - Desegin eta berregin aldaketak segmentua eraikitzean.

Goiko adibideak segmentazio-gaitasuna adierazten du. Segmentu bat definitu dugu ondasunak online erosten gutxienez $500 gastatu dituzten eta *softwareen garapenean* interesa duten bezeroentzat.

## <a name="create-a-new-segment"></a>Sortu segmentu berria

Segmentu berri bat sortzeko hainbat modu daude. Sekzio honetan segmentu bat hutsetik nola sortu azaltzen da. A ere sor dezakezu *segmentu azkarra* dauden entitateetan oinarrituta edo lortzeko Ikaskuntza automatiko ereduak *iradokitako segmentuak*. Informazio gehiago lortzeko: [Segmentuen informazio orokorra](segments.md).

Segmentua sortu bitartean, zirriborroa gorde dezakezu. Segmentu inaktibo gisa gordeko da eta ezin da aktibatu baliozko konfigurazio batekin amaituta.

1. Zoaz **Segmentuak** orrira.

1. Hautatu **Berria** > **Sortu zeurea**.

1. Segmentu-egilearen orrian, lehenengo araua zehaztu behar duzu. Arau batek baldintza bat baino gehiago du eta bezero multzo bat definitzen du.

1. **Rule1** sekzioan, aukeratu zein entitateren atributurekin iragazi nahi dituzun bezeroak. Bi modu daude atributuak aukeratzeko: 
   - Berrikusi erabilgarri dauden entitateak eta atributuak **Gehitu arauan** paneleane ta hautatu gehitu beharreko atributuaren ondoko **+** ikonoa. Aukeratu atributua lehendik dagoen arau batean gehitu nahi duzun, ala arau berri bat sortzeko erabili.
   - Bat datozen iradokizunak ikusteko, idatzi atributuaren izena arauaren sekzioan.

1. Aukeratu baldintzaren bat datozen balioak zehazteko eragileak. Atributuak lau datu mota izan ditzake balio gisa: zenbakizkoa, katea, datua edo boolearra. Atributuaren datu moten arabera, baldintza zehazteko eragile desberdinak daude. 

1. Arau batean baldintza gehiago gehitzeko, hautatu **Gehitu baldintza**. Arau bat sortzeko uneko arauaren barruan, hautatu **gehitu azpiaraua**.

1. Arau batek *Bezeroaren* entitatea ez diren beste entitate batzuk erabiltzen baditu, erlazioaren bide-izena ezarri behar duzu. Erlazioaren bide-izena beharrezkoa da sistemari jakinarazteko zein erlazioren bidez atzitu nahi duzun bezeroaren entitate bateratua. Hautatu **ezarri erlazioaren bide izena** hautatutako entitatea esleitzeko bezeroaren entitate bateratuari. Erlazioaren bide-izen posible bakarra badago, sistemak automatikoki hautatuko du. Harreman bide desberdinek emaitza desberdinak eman ditzakete. Arau bakoitzak bere erlazioaren bide-izena izan dezake.

   Hautatu :::image type="content" source="media/relationship-path.png" alt-text="Erlazioaren bide-izen posiblea, arau bat sortzerakoan bezeroaren entitate bateratuari esleitutako entitatea batean oinarrituta.":::

   Adibidez, pantaila-argazkiko *eCommerce_eCommercePurchases* entitateak lau aukera ditu *Bezeroaren* entitateari esleitzeko: 
   - eCommerce_eCommercePurchases > eCommerce_eCommerceContacts > Bezeroa
   - eCommerce_eCommercePurchases > Bezeroa
   - eCommerce_eCommercePurchases > eCommerce_eCommerceContacts > POS_posPurchases > Bezeroa
   - eCommerce_eCommercePurchases > eCommerce_eCommerceContacts > POS_posPurchases > loyaltyScheme_loyCustomers > Bezeroa Azken aukera hautatzerakoan, arauaren baldintzetan zerrendatutako entitate guztien atributuak sar ditzakegu. Baliteke emaitza gutxiago lortzea, bat datozen bezeroaren erregistroek entitate guztien parte izan behar dutelako. Adibide honetan, merkataritza elektroniko (*eCommerce_eCommercePurchases*) bidez ondasunak erosi dituzte, (*POS_posPurchases*) erosketa-puntuan eta geure fideltasun-programan (*loyaltyScheme_loyCustomers*) parte hartzen dute. Bigarren aukera hautatzereakoan, *eCommerce_eCommercePurchases* eta *Bezeroaren* entitateko atributuak soilik aukera ditzakegu. Horri esker, bezeroaren profil gehiago lor daitezke.

1. Arau batean hainbat baldintza badituzu, aukera dezakezu zein eragile logikok konektatzen dituen.

   - **AND** eragilea: baldintza guztiak bete behar dira erregistro bat segmentuan sartzeko. Aukera hau baliagarria da entitate desberdinetan baldintzak definitzen dituzunean.

   - **OR** eragilea: baldintzetako bat bete behar da erregistro bat segmentuan sartzeko. Aukera hau oso baliagarria da hainbat baldintza definitzen dituzunean entitate berarentzat.

   :::image type="content" source="media/segmentation-either-condition.png" alt-text="Arautu bi AND baldintzen bidez.":::

   OR eragilea erabiltzean, baldintza guztiak erlazioaren bide-izenean dauden entitateetan oinarrituta egon behar dira.

   1. Hainbat arau sor ditzakezu bezeroen erregistro multzo desberdinak sortzeko. Taldeak konbinatu ditzakezu zure negozio kasurako behar diren bezeroak sartzeko. Arau berri bat sortzkeo, hautatu **Gehitu araua**. Zehazki, entitate bat ezin baduzu sartu arau batean zehaztutako erlazioaren bide-izena dela eta, beste arau bat sortu behar duzu, atributuak bertatik hautatzeko.

      :::image type="content" source="media/segment-rule-grouping.png" alt-text="Gehitu beste arau bat segmentu batena eta hautatu multzoko eragilea.":::

   1. Aukeratu multzo operadoreetako bat: **Batasuna**, **Elkartu**, edo **Izan ezik**.

   - **Bateratzea** bi taldeak batzen ditu.

   - **Gurutzatu** bi taldeak gainjartzen ditu. Bi taldeetako datu *komunak* soilik mantentzen dira talde bateratuan.

   - **Salbuespena** bi taldeak batzen ditu. A eta B talde bietan *ez dauden* datuak soilik mantentzen dira.

1. Lehenespenez, zehaztutako iragazkiekin bat datozen bezeroen profilen atributu guztiak dituzten irteerako entitateak sortzen dituzte segmentuek. Segmentu bat ez den beste entitate batzuetan oinarrituta badago *Bezeroa* entitatea, entitate hauetatik atributu gehiago gehi ditzakezu irteerako entitateari. Aukeratu **Proiektuaren atributuak** irteerako entitateari erantsiko zaizkion atributuak aukeratzeko.  

   :::image type="content" source="media/segments-project-attributes.png" alt-text="Alboko panelean hautatutako proiektatutako atributuen adibidea, irteerako entitatean gehitzeko.":::
  
   Adibidea: segmentu bat erosketa-datuak dituen entitate batean oinarrituta dago eta *bezeroaren* entitatearekin erlazionatuta dago. Segmentuak uneko urtean ondasunak erosi dituzten Espainiako bezero guztiak bilatzen ditu. Atributuak eranstea aukera dezakezu, adibidez, ondasunen prezioa edo irteerako entitateko bat datozen bezeroen erregistroen erosketa-data. Informazioa baliagarria izan daiteke gastatutako guztizkoaren urtaroen araberako korrelazioak aztertzeko.

   > [!NOTE]
   > - Proiektatutako atributuek bezeroaren entitatearekin bat-bateko harremana duten entitateentzat bakarrik funtzionatzen dute. Adibidez, bezero batek harpidetza ugari izan ditzake.
   > - Sortzen ari zaren segmentuaren kontsultako arau guztietan erabiltzen den entitateetako atributuak soilik proiekta ditzakezu.
   > - Multzo operadoreak erabiltzean proiektatutako atributuak kontuan hartzen dira.

1. Segmentua gorde eta exekutatu aurretik, hautatu **editatu xehetasunak**, segmentuaren izenaren ondoan. Eman segmentuari izena eta eguneratu segmentuaren iradokitako **irteerako entitatearen izena**. Segmentuaren azalpena ere gehi dezakezu.

1. Behin betekizun guztiak balidatuta segmentua gorde eta prozesatzeko, **hautatu exekutatu**. Bestela, segmentuaren zirriborro inaktibo gisa gordeko da.

1. Aukeratu **Segurtasunetara itzuli** berriro ere **segmentuak** orria.

> [!TIP]
> - Segmentu-egileak ez ditu entitateetako baliozko balioak iradokiko baldintzen eragileak ezartzean. Erabilgarri dauden balioak ikusteko, joan **Datuak** > **Entitateak** atalera eta deskargatu entitatearen datuak.
> - Datetan oinarritutako baldintzek data finkoen eta data-tarte mugikorren artean aldatzeko aukera ematen dute.
> - Segmentu batek hainbat arau baditu, barra urdin bat egongo da editatzen ari zaren arauaren inguruan.
> - Arauak eta baldintzak segmentuaren definizioko beste lekuetara eraman ditzakezu. Hautatu [...] arau edo baldintza baten ondoan eta hautatu nola eta nora eraman.
> - Komando-barrako **Desegin** eta **Berregin** kontrolek aldaketak desegiteko aukera ematen dute.

## <a name="quick-segments"></a>Segmentu azkarrak

Segmentu bizkorrek segmentu sinpleak operadore bakar batekin azkar eraikitzeko aukera ematen dute ikuspegi azkarragoak lortzeko.

1. **Segmentuak** orrian, hautatu **Berria** > **Sortu honetatik**.

   - Hautatu **Profilak** aukera *bateratutako bezeroaren* entitatean oinarritutako segmentu bat eraikitzeko aukera.
   - Aukeratu **Neurriak** aukera sortu aurretik sortutako neurrien inguruan segmentu bat eraikitzeko.
   - Hautatu botoia **Adimen** Aukera hau bai erabiliz sortu duzun irteerako entitateetako baten inguruan eraikitzeko aukera **iragarpenak** edo **Neurrira egindako ereduak** gaitasunak.

2. Sarbidean **Segmentu azkar berria** elkarrizketa-koadroan, hautatu atributu bat **eremua** goitibeherako menuko.

3. Sistemak xehetasun gehiago emango dizkizu bezeroen segmentu hobeak sortzeko.
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
