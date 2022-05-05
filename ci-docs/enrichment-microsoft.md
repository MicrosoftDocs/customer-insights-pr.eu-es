---
title: Aberastu bezeroen profilak Microsoften datuekin
description: Erabili Microsoft-en jabedun datuak zure bezeroen datuak afinitateekin eta ahots-partekatzeekin aberasteko.
ms.date: 03/02/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: kishorem-MS
ms.author: kishorem
manager: shellyha
searchScope:
- ci-enrichments
- ci-enrichment-wizard
- customerInsights
ms.openlocfilehash: 5c016a394fdf485057a190d03bfed9ce5481f435
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642113"
---
# <a name="enrich-customer-profiles-with-affinities-and-share-of-voice-preview"></a>Aberastu bezeroen profilak afinitateekin eta ahots partekatuekin (aurrebista)

Erabili Microsoft-en jabedun datuak zure bezeroen datuak aberasteko marka-akidetasunekin, intereseko kidetasunekin eta ahots-partekatzearekin (SoV). Afinitate hauek eta SoV zure bezeroen antzeko demografia duten pertsonen datuetan oinarritzen dira. Informazio honek zure bezeroak hobeto ulertzen eta segmentatzen laguntzen dizu marka eta interes zehatzekiko duten kidetasunen edo SoVren arabera.

Joan **Datuak** > **Aberastea** to [aberasgarriak konfiguratu eta ikusi](enrichment-hub.md).

Marka-afintasunak eta SoV aberastea konfiguratzeko, joan hona **Ezagutu** fitxa eta hautatu **Aberastu nire datuak** gainean **Markak** teila.

Interes-afintasunak eta SoV aberastea konfiguratzeko, joan **Ezagutu** fitxa eta hautatu **Aberastu nire datuak** gainean **Interesak** teila.

   > [!div class="mx-imgBorder"]
   > ![Markak eta zaletasunak lauzak.](media/BrandsInterest-tile-Hub.png "Markak eta zaletasunen lauzak")

## <a name="how-we-determine-affinities-and-sov"></a>Nola zehazten ditugun afinitateak eta SoV

Microsoft-en lineako bilaketa-datuak erabiltzen ditugu hainbat segmentu demografikotan (adinaren, generoaren edo kokapenaren arabera definitutako marken eta interesen arteko afinitateak eta SoV) aurkitzeko. Marka edo interes baten lineako bilaketa-bolumena afinitatea edo SoV zehazteko oinarria da. Hala ere, bakoitzak ikuspegi ezberdin bat eskaintzen du zure bezeroak ulertzeko.

- Afinitatea segmentu demografikoen arteko konparazio bat da. Informazio hau erabil dezakezu marka edo interes jakin batekin afinitate handiena duten segmentu demografikoak identifikatzeko, beste segmentuekin alderatuta.

- Ahots-partekatzea hautatutako marken edo interesen arteko konparazio bat da. Informazio hau erabil dezakezu zein marka edo interes duen segmentu demografiko jakin baterako ahots-parte handiena zein den identifikatzeko, hautatu dituzun beste marka edo interes batzuekin alderatuta.

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

## <a name="share-of-voice-sov"></a>Ahotsaren partekatzea (SoV)

SoV 100 puntuko eskalan kalkulatzen dugu. Bezeroen profil aberastu bakoitzeko marka edo interes guztien SoV osoa 100 gehitzen da. Afinitateak ez bezala, SoV hautatzen dituzun marken eta interesekiko erlatiboa da. Adibidez, 'Microsoft'-en SoV balioak desberdinak izan daitezke hautatutako markak ('Microsoft', 'GitHub') eta ('Microsoft', 'LinkedIn') badira.

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

Hautatu **Entitate aberastua** eta aukeratu Microsoft-en datuekin aberastu nahi duzun datu multzoa. Bezeroen entitatea hauta dezakezu zure bezeroen profil guztiak aberasteko edo segmentu-entitate bat hauta dezakezu segmentu horretan dauden bezeroen profilak soilik aberasteko.

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

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberaste prozesua exekutatu ostean, joan **Nire aberasteak** berrikusteko guztira aberastutako bezeroen kopurua eta aberastutako bezeroen profilen marka eta interesen banaketa.

:::image type="content" source="media/my-enrichments.png" alt-text="Abantaila prozesua exekutatu ondoren, emaitzen aurrebista.":::

Taula bat aurkituko duzu denboran zehar aberastutako bezero-profilen kopuruarekin eta aberastutako entitateen aurrebistarekin. Berrikusi aberastutako datuak hautatuz **Gehiago ikusi** urtean **Afinitate maila** edo **Ahotsaren partekatzea** taulak. Marken datu aberastuak **BrandAffinityFromMicrosoft** eta **BrandShareOfVoiceFromMicrosoft** entitateak. Interesen datuak atalean daude **InterestAffinityFromMicrosoft** eta **InterestShareOfVoiceFromMicrosoft** entitateak. Erakunde hauek zerrendan aurkituko dituzu **aberastea** taldean **Datuak** > **erakundeak** atalean.

## <a name="see-enrichment-data-on-the-customer-card"></a>Ikusi aberastasun datuak bezeroaren txartelean

Marka eta interesa SoV bezero banakako txarteletan ere ikus daiteke. Joan **Bezeroak** atalera eta hautatu bezeroaren profila. Bezero-txartelean, marka edo interes SoVrako grafikoak aurkituko dituzu bezero horren profil demografikoko pertsonen arabera.

:::image type="content" source="media/enrichment-customer-card.png" alt-text="Aberastutako datuak dituen bezeroaren txartela.":::

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]


[!INCLUDE [footer-include](includes/footer-banner.md)]