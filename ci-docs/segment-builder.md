---
title: Sortu segmentu konplexuak segmentu-sorgailuarekin
description: Erabili segmentu-sortzailea bezeroen segmentu konplexuak sortzeko hainbat atribututan oinarrituta taldekatuz.
ms.date: 03/25/2022
ms.subservice: audience-insights
ms.topic: how-to
author: JimsonChalissery
ms.author: jimsonc
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-segments
- ci-segment-builder
- ci-segment-details
- customerInsights
ms.openlocfilehash: cde373cd65e296675e1b3c92f3024e1093853842
ms.sourcegitcommit: 8a28e9458b857adf8e90e25e43b9bc422ebbb2cd
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/18/2022
ms.locfileid: "9170620"
---
# <a name="create-complex-segments-with-segment-builder"></a>Sortu segmentu konplexuak segmentu-sorgailuarekin

Definitu iragazki konplexuak bezero entitate bateratuaren eta hari lotutako entitateen inguruan. Segmentu bakoitzak, prozesatu ondoren, bezeroen erregistro multzo bat sortzen du eta esportatu eta neurriak hartu ditzakezu.

> [!TIP]
> Oinarritutako segmentuak **bezero partikularrak** automatikoki sartu segmentuko kideentzako eskuragarri dagoen informazioa. Inguruneetan **negozio kontuak**, segmentuak kontuetan (enpresak edo filialak) oinarritzen dira. Kontaktu informazioa segmentu batean sartzeko, erabili **Proiektuaren atributuak** funtzionalitatea segmentu eraikitzailean. Ziurtatu harremanetarako datu-iturriak daudela [semantikoki mapatuta ContactProfile](semantic-mappings.md#define-a-contactprofile-semantic-entity-mapping) entitatera.

## <a name="segment-builder"></a>Segmentu-egilea

Irudi honek segmentu-sortzailearekin hainbat alderdi adierazten ditu. Bezero talde bat bilakatzen den segmentu bat erakusten du. Bezeroek ondasunak denbora-tarte jakin batean eskatu zituzten eta sari-puntuak bildu edo diru kopuru bat gastatu zuten.

:::image type="content" source="media/segment-builder-overview.png" alt-text="Segmentu-sortzailearen elementuak." lightbox="media/segment-builder-overview.png":::

1. Antolatu zure segmentua arau eta azpi arauekin. Arau edo azpi-arau bakoitza baldintzez osatuta dago. Konbinatu baldintzak operadore logikoekin.

1. Aukeratu [harreman bidea](relationships.md) arau bati aplikatzen zaion entitateen artean. Harreman-bideak baldintza batean zein atributu erabil daitezkeen zehazten du.

1. Kudeatu arauak eta azpi-arauak. Arau baten kokapena aldatu edo ezabatu.

1. Gehitu baldintzak eta eraiki habia maila egokia azpi-arauak erabiliz.

1. Aplikatu multzo eragiketak konektatutako arauei.

1. Erabili atributuen panela eskuragarri dauden entitateen atributuak gehitzeko edo atributuetan oinarritutako baldintzak sortzeko. Panelak hautatutako araurako erabilgarri dauden hautatutako harreman bideen arabera oinarritutako entitate eta atributuen zerrenda erakusten du.

1. Gehitu atributuetan oinarritutako baldintzak lehendik dauden arau eta azpiurrei edo gehitu arau berri bati.

1. Desegin eta berregin aldaketak segmentua eraikitzean.

Goiko adibideak segmentazio-gaitasuna adierazten du. Segmentu bat definitu dugu ondasunak online erosten gutxienez $500 gastatu dituzten eta *softwareen garapenean* interesa duten bezeroentzat.

## <a name="create-a-new-segment-with-segment-builder"></a>Sortu segmentu berri bat segmentu-sortzailearekin

1. Joan hona: **Segmentuak**.

1. Hautatu **Berria** > **Sortu zeurea**. Segmentu-sortzailearen orrian, arauak definitzen edo konposatzen dituzu. Arau batek bezero multzo bat definitzen duten baldintza bat edo gehiago ditu.

1. Hautatu **Editatu xehetasunak** Izenbururik gabeko segmentuaren ondoan. Eman segmentuari izena eta eguneratu segmentuaren iradokitako **irteerako entitatearen izena**. Aukeran, gehitu deskribapen bat eta [etiketak](work-with-tags-columns.md#manage-tags) segmentuari.

   :::image type="content" source="media/segments_edit_details.png" alt-text="Editatu xehetasunak elkarrizketa-koadroa.":::

1. urtean **Araua 1** atalean, aukeratu bezeroak iragazi nahi dituzun entitate baten atributu bat. Bi modu daude atributuak aukeratzeko:
   - Berrikusi erabilgarri dauden entitateak eta atributuak **Gehitu arauan** paneleane ta hautatu gehitu beharreko atributuaren ondoko **+** ikonoa. Aukeratu atributua lehendik dagoen arau batean gehitu nahi duzun, ala arau berri bat sortzeko erabili.
   - Bat datozen iradokizunak ikusteko, idatzi atributuaren izena arauaren sekzioan.

1. Aukeratu baldintzaren bat datozen balioak zehazteko eragileak. Atributuak lau datu mota izan ditzake balio gisa: zenbakizkoa, katea, datua edo boolearra. Atributuaren datu moten arabera, baldintza zehazteko eragile desberdinak daude. Negozio kontuak dituzten segmentuetarako, bi operadore berezi daude eskuratutako iruzkinen arteko balizko hierarkiak sartzeko. Erabili *seme-alabak* eta *guraso* operadoreek lotutako kontuak sartzeko.

1. Arau batean baldintza gehiago gehitzeko, hautatu **Gehitu baldintza**. Arau bat sortzeko uneko arauaren barruan, hautatu **gehitu azpiaraua**.

1. Arau batek beste entitate batzuk erabiltzen baditu *Bezeroa* entitatea, hautatu **Ezarri harreman-bidea** hautatutako entitatea bezero entitate bateratuarekin mapatzeko. Harreman bide posible bakarra badago, sistemak automatikoki hautatzen du. Desberdina [harreman bideak](relationships.md#relationship-paths) emaitza desberdinak eman ditzake. Arau bakoitzak bere erlazioaren bide-izena izan dezake.

   Hautatu :::image type="content" source="media/relationship-path.png" alt-text="Erlazioaren bide-izen posiblea, arau bat sortzerakoan bezeroaren entitate bateratuari esleitutako entitatea batean oinarrituta.":::

1. Arau batean hainbat baldintza badituzu, aukeratu zein operadore logiko konektatzen dituen.  
   - **AND** eragilea: baldintza guztiak bete behar dira erregistro bat segmentuan sartzeko. Erabili aukera hau entitate ezberdinetan baldintzak definitzen dituzunean.
   - **OR** eragilea: baldintzetako bat bete behar da erregistro bat segmentuan sartzeko. Erabili aukera hau entitate bererako hainbat baldintza definitzen dituzunean.

   :::image type="content" source="media/segmentation-either-condition.png" alt-text="Arautu bi AND baldintzen bidez.":::

   OR eragilea erabiltzean, baldintza guztiak erlazioaren bide-izenean dauden entitateetan oinarrituta egon behar dira.

1. Bezeroen erregistro multzo desberdinak sortzeko, sortu hainbat arau. Zure negozio kasurako behar diren bezeroak sartzeko, konbinatu taldeak. Zehazki, ezin baduzu entitate bat arau batean sartu zehaztutako harreman-bidea dela eta, sortu arau berri bat haren atributuak aukeratzeko.

      :::image type="content" source="media/segment-rule-grouping.png" alt-text="Gehitu beste arau bat segmentu batena eta hautatu multzoko eragilea.":::

   1. Hautatu **Gehitu araua**.
   1. Aukeratu multzo operadoreetako bat: **Batasuna**, **Elkartu**, edo **Izan ezik**.

      - **Bateratzea** bi taldeak batzen ditu.
      - **Gurutzatu** bi taldeak gainjartzen ditu. Bi taldeek *komunean dituzten* datuak soilik geratzen dira talde bateratuan.
      - **Salbuespena** bi taldeak batzen ditu. B taldearekiko *Komunak ez diren* A taldeko datuak soilik gordetzen dira B taldean.

1. Lehenespenez, irteerako entitateak automatikoki edukiko ditu definitutako iragazkiekin bat datozen bezero-profilen atributu guztiak. Segmentu bat ez den beste entitate batzuetan oinarritzen bada *Bezeroa* entitatea, hautatu **Proiektuaren ezaugarriak** entitate hauen atributu gehiago irteerako entitateari gehitzeko.

   > [!IMPORTANT]
   > Negozio-kontuetan oinarritutako segmentuetarako, kontu bakoitzeko kontaktu baten edo gehiagoren xehetasunak *HarremanetarakoProfila* entitatea segmentuan sartu behar da segmentu hori aktibatzeko edo harremanetarako informazioa behar duten helmugetara esportatzeko. *ContactProfile* entitateari buruzko informazio gehiago lortzeko, ikus [Esleipen semantikoak](semantic-mappings.md).
   > Kontaktuen proiektatutako atributuak dituzten negozio-kontuetan oinarritutako segmentu baten irteerako lagin bat honela izan daiteke:
   >
   > |ID  |Kontuaren izena  |Diru-sarrerak  |Kontaktuaren izena  | Kontaktuaren funtzioa|
   > |---------|---------|---------|---------|---|
   > |10021     | Contoso | 100K | [Abbie Moss, Ruth Soto]  | [CEO, lorpenen kudeatzailea]

   :::image type="content" source="media/segments-project-attributes.png" alt-text="Alboko panelean hautatutako proiektatutako atributuen adibidea, irteerako entitatean gehitzeko.":::
  
   Adibidez: segmentu bat erosketa datuak dituen entitate batean oinarritzen da *Bezeroa* entitatea. Segmentuak uneko urtean ondasunak erosi dituzten Espainiako bezero guztiak bilatzen ditu. Salgaien prezioa edo erosketa-data bezalako atributuak gehitzea aukera dezakezu irteerako entitatean bat datozen bezero-erregistro guztietan. Informazioa baliagarria izan daiteke gastatutako guztizkoaren urtaroen araberako korrelazioak aztertzeko.

   > [!NOTE]
   > - **Proiektuaren atributuak** bezero entitatearekin bat-bateko harremana duten entitateentzat bakarrik funtzionatzen du. Adibidez, bezero batek harpidetza ugari izan ditzake.
   > - Proiektatu nahi duzun atributua saltotik bat baino gehiagora badago *Bezeroa* entitateak, harremanak definitzen duen moduan, atributu hori eraikitzen ari zaren segmentuaren kontsultaren arau guztietan erabili beharko litzateke.
   > - Proiektatu nahi duzun atributua saltotik batera badago *Bezeroa* entitateak ez du presente egon behar atributu hori eraikitzen ari zaren segmentuaren kontsultaren arau guztietan erabiltzean.
   > - Multzo operadoreak erabiltzean **proiektatutako atributuak** kontuan hartzen dira.

1. Hautatu **Korrika egin** segmentua sortzeko. Hautatu **Gorde** uneko konfigurazioa mantendu eta gero segmentua exekutatu nahi baduzu. The **Segmentuak** orrialdeak bistaratzen ditu.

### <a name="segment-builder-tips"></a>Segmentuak eraikitzeko aholkuak

Segmentu bat sortzeko segmentu-sortzailea erabiliz, kontuan izan aholku hauek:

- Segmentu-egileak ez ditu entitateetako baliozko balioak iradokiko baldintzen eragileak ezartzean. Erabilgarri dauden balioak ikusteko, joan **Datuak** > **Entitateak** atalera eta deskargatu entitatearen datuak.
- Datetan oinarritutako baldintzek data finko eta data-tarte mugikor batetik bestera aldatzeko aukera ematen dute.
- Segmenturako arau ugari badituzu, editatzen ari zaren arauak lerro urdin bertikala du ondoan.
- Arauak eta baldintzak segmentuaren definizioko beste lekuetara eraman ditzakezu. Hautatu elipsi bertikala (&vellip;) arau edo baldintza baten ondoan eta aukeratu nola eta nora eraman.
- **Desegin** eta **Berregin** Komando-barrako kontrolek aldaketak atzeratzeko aukera ematen dute.
- Segmentu bat sortu ondoren, segmentu batzuek aukera ematen dute [segmentuaren erabileraren jarraipena](segments.md#track-usage-of-a-segment).

## <a name="next-steps"></a>Hurrengo urratsak

[Esportatu segmentu bat](export-destinations.md) eta esploratu [Bezeroen txartelaren integrazioa](customer-card-add-in.md) segmentuak beste aplikazio batzuetan erabiltzeko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
