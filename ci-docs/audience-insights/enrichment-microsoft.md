---
title: Aberastu bezeroen profilak Microsoften datuekin
description: Erabili Microsoft-en jabedun datuak bezeroen datuak marka eta interes kidetasunekin aberasteko.
ms.date: 06/14/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-MS
ms.author: kishorem
manager: shellyha
ms.openlocfilehash: 45c81a037258e42d8975e0372c104865a9d4cbfe
ms.sourcegitcommit: 2acda3c5adf40bc3f5bbb4b2b4b6c22f84371da7
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466609"
---
# <a name="enrich-customer-profiles-with-brand-and-interest-affinities-preview"></a>Aberastu bezeroen profilak marka eta interes kidetasunekin (aurrebista)

Erabili Microsoft-en jabedun datuak bezeroen datuak marka eta interes kidetasunekin aberasteko. Afinitate hauek zure bezeroen demografia antzekoko jendearen datuetan oinarritzen dira. Informazio honek bezeroak hobeto ulertzen eta segmentatzen laguntzen du, marka eta interes jakin batzuen arabera.

Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** [aberasteak konfiguratu eta ikusteko](enrichment-hub.md).

Marka afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Markak** teila.

Interes afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Interesak** teila.

   > [!div class="mx-imgBorder"]
   > ![Markak eta zaletasunak lauzak.](media/BrandsInterest-tile-Hub.png "Markak eta zaletasunen lauzak")

## <a name="how-we-determine-affinities"></a>Afinitateak nola zehazten ditugun

Microsoften lineako bilaketa-datuak erabiltzen ditugu marka eta interesen arteko afinitateak aurkitzeko hainbat segmentu demografikotan (adinaren, generoaren edo kokapenaren arabera definituak). Marka edo interes baten bilaketa-bolumenak zehazten du zein den afinitate batek segmentu demografiko batek, beste segmentu batzuekin alderatuta, marka edo interes hori.

## <a name="affinity-level-and-score"></a>Afinitate-maila eta puntuazioa

Bezeroen profil aberastu guztietan, erlazionatutako bi balio ematen ditugu: afinitate-maila eta afinitate-puntuazioa. Balio horiei esker, profil horren segmentu demografikoarekiko, marka edo interesekiko, beste segmentu demografiko batzuekiko duten afinitatea zehazten lagunduko dizute.

*Afinitate-maila* lau maila ditu eta *afinitate puntuazioa* afinitate mailetara esleitzen den 100 puntuko eskalan kalkulatzen da.


|Afinitate-maila |Afinitate-puntuazioa  |
|---------|---------|
|Oso handia     | 85-100       |
|Handia     | 70-84        |
|Ertaina     | 35-69        |
|Txikia     | 1-34        |

Afinitatea neurtzeko nahi duzun xehetasunen arabera, afinitate maila edo puntuazioa erabil dezakezu. Afinitate-puntuazioak kontrol zehatzagoa ematen dizu.

## <a name="supported-countriesregions"></a>Lagundutako herrialde / eskualdeak

Egun, herrialde / eskualdeko aukerak onartzen ditugu: Australia, Kanada (ingelesa), Frantzia, Alemania, Erresuma Batua edo Estatu Batuak (ingelesa).

Herrialde edo eskualde bat hautatzeko, ireki **Markak aberastea** edo **Interesa aberastea** eta hautatu **Aldaketa** Alboan **Herrialdea/Eskualdea**. Sarbidean **Herrialdearen eta eskualdeen ezarpenak** panela, aukeratu aukera bat eta hautatu **aplikatu**.

### <a name="implications-related-to-country-selection"></a>Herrialdearen hautaketarekin lotutako ondorioak

- [Zure markak aukeratzen dituzunean](#define-your-brands-or-interests), sistemak hautatutako herrialdean edo eskualdean oinarritutako iradokizunak eskaintzen ditu.

- [Sektorea aukeratzean](#define-your-brands-or-interests), hautatutako herrialdean edo eskualdean oinarritutako marka edo interes garrantzitsuenak lortuko dituzu.

- Noiz [profil aberasgarriak](#refresh-enrichment), aberastuko ditugu hautatutako marken eta interesen datuak lortzeko bezeroen profil guztiak, hautatutako herrialdean edo eskualdean ez dauden profilak barne. Adibidez, Alemania aukeratu baduzu, Estatu Batuetan kokatutako profilak aberastuko ditugu AEBetan hautatutako marka eta interesetarako datuak eskuragarri baditugu.

## <a name="configure-enrichment"></a>Aberastea konfiguratzea

Esperientzia gidatu batek aberastasunak konfiguratzen lagunduko dizu. 

### <a name="define-your-brands-or-interests"></a>Zehaztu zure markak edo zaletasunak

Aukeratu gehienez bost marka edo interes aukera hauetako bat edo biak erabiliz:

- **Industria**: Aukeratu zure industria goitibeherako zerrendan eta aukeratu industria horretako marka edo interes gorenen artean.
- **Aukeratu zeurea**: Sartu zure erakundearentzako garrantzitsua den marka edo interesa eta aukeratu bat datorren iradokizunen artean. Bilatzen ari zaren marka edo interesa zerrendatzen ez badugu, bidal iezaguzu iritzia erabilita **Proposatu** esteka.

### <a name="review-enrichment-preferences"></a>Berrikusi aberaste-hobespenak

Berrikusi aberastasun lehentasun lehenetsiak eta eguneratu behar dituzun moduan.

:::image type="content" source="media/affinity-enrichment-preferences.png" alt-text="Aberasteko lehentasunen leihoaren pantaila-argazkia.":::

### <a name="select-entity-to-enrich"></a>Hautatu aberasteko entitatea

Hautatu **Aberastutako entitatea** eta aukera datuak ezartzeko aberastu nahi duzuna konpainiaren datuekin Microsoft-etik. Bezeroen entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

### <a name="map-your-fields"></a>Esleitu eremuak

Esleitu zure bezero entitate bateratuko eremuak sistemak zure bezeroaren datuak aberasteko erabili nahi duzun segmentu demografikoa definitzeko. Esleitu herrialdea/eskualdea eta gutxienez Jaiotze-data edo Generoa atributuak. Gainera, herrialdea/eskualdea esleitu behar duzu. Halaber, hiri bat (eta estatua/probintzia) edo posta-kode bat esleitu behar dituzu gutxienez. Aukeratu **Editatu** eremuen mapa zehaztu eta hautatu **aplikatu** amaitutakoan. Aukeratu **Gorde** eremuaren mapa osatzeko.

Formatu eta balio hauek onartzen dira (balioak ez dira maiuskulak):

- **Jaioteguna**: Jaiotze-data DataTime motara bihurtzea gomendatzen dugu datuak irensten diren bitartean. Bestela, katea izan daiteke [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) formatua "aaaa-MM-dd" edo "aaaa-MM-ddTHH: mm: ss".
- **Generoa**: Gizona, Emakumezkoa, Ezezaguna.
- **Posta kodea**: Estatu Batuetako bost digituko posta kodeak, beste edozein lekutan posta kodea estandarra.
- **Hiria**: Hiria izena ingelesez.
- **Estatua / Probintzia**: AEB eta Kanadako bi gutun-laburdura. Bi edo hiru gutun-laburdura Australiarako. Ez da aplikagarria Frantzian, Alemanian edo Erresuma Batuan.
- **Herrialdea/Eskualdea**:

  - AEB: Ameriketako Estatu Batuak, Estatu Batuak, AEBak, AEBak, Amerika
  - CA: Kanada, CA
  - GB: Erresuma Batua, Erresuma Batua, Britainia Handia, GB, Britainia Handia eta Ipar Irlanda, Erresuma Batua
  - AU: Australia, AU, Australiako Mankomunitatea
  - FR: Frantzia, FR, Frantziar Errepublika
  - DE: Alemania, Alemania, Deutschland, Allemagne, DE, Alemaniako Errepublika Federala, Alemaniako Errepublika

## <a name="review-and-name-the-enrichment"></a>Aberaspena berrikusi eta izendatu

Azkenean, informazioa berrikusi eta aberasteko izena eman dezakezu.

:::image type="content" source="media/enrichment-interests-summary.png" alt-text="Interesak berrikusteko eta izendatzeko orria.":::

## <a name="refresh-enrichment"></a>Freskatu aberastea

Exekutatu aberastasuna marka, interesak eta eremuen mapak konfiguratu ondoren demografiarako. Prozesua hasteko, hautatu **Korrika egin** marka edo interesen konfigurazio orrian. Gainera, sistemak aberastasuna automatikoki utz dezakezu planifikatu gabeko freskatze baten baitan.

Bezeroaren datuen tamainaren arabera, minutu batzuk behar izango dira aberasteko exekuzioa osatzeko.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberaste prozesua exekutatu ostean, joan **Nire aberasteak** berrikusteko guztira aberastutako bezeroen kopurua eta aberastutako bezeroen profilen marka eta interesen banaketa.

:::image type="content" source="media/my-enrichments.png" alt-text="Abantaila prozesua exekutatu ondoren, emaitzen aurrebista.":::

Berrikusi aberastutako datuak, hautatuta **Ikusi aberastutako datuak** grafikoan. Marken datu aberastuak: **BrandAffinityFromMicrosoft** Erakunde. Interesen datuak datuak daude **InterestAffinityFromMicrosoft** Erakunde. Erakunde hauek zerrendan aurkituko dituzu **aberastea** taldean **Datuak** > **erakundeak** atalean.

Diagraman, denboran zehar aberastu diren bezeroen profil kopurua eta aberastutako entitatearen aurrebista ikusiko dituzu. Aberastutako entitatea ikusteko, hautatu **Erakutsi gehiago** aurrebista-lauzan.

## <a name="see-enrichment-data-on-the-customer-card"></a>Ikusi aberastasun datuak bezeroaren txartelean

Marka eta interes kidetasunak bezero banakako txarteletan ere ikus daitezke. Joan **Bezeroak** atalera eta hautatu bezeroaren profila. Bezeroaren txartelean, bezeroaren demografia profil horretako pertsonek afinitatea duten marken edo interesen zerrendak aurkituko dituzu.

:::image type="content" source="media/enrichment-customer-card.png" alt-text="Aberastutako datuak dituen bezeroaren txartela.":::

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Sortu [Segmentuak](segments.md) eta [Neurriak](measures.md), eta are [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
