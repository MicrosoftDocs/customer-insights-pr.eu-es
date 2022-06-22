---
title: Aberastu bezeroen profilak Microsoft-en marken eta interesen datuekin
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
ms.openlocfilehash: 61262980cafdcd130430e200e466ce7da6cc4d07
ms.sourcegitcommit: 27c5473eecd851263e60b2b6c96f6c0a99d68acb
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/13/2022
ms.locfileid: "8953750"
---
# <a name="enrich-customer-profiles-with-affinities-and-share-of-voice-preview"></a>Aberastu bezeroen profilak afinitateekin eta ahots partekatuekin (aurrebista)

Erabili Microsoft-en jabedun datuak zure bezeroen datuak aberasteko marka-akidetasunekin, intereseko kidetasunekin eta ahots-partekatzearekin (SoV). Afinitate hauek eta SoV zure bezeroen antzeko demografia duten pertsonen datuetan oinarritzen dira. Informazio honek zure bezeroak hobeto ulertzen eta segmentatzen laguntzen dizu marka eta interes zehatzekiko duten kidetasunen edo SoVren arabera.

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

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

   - Marka-afintasunak eta SoV aberastea konfiguratzeko, hautatu **Aberastu nire datuak** gainean **Markak** teila.

   - Interes-afintasunak eta SoV aberastea konfiguratzeko, hautatu **Aberastu nire datuak** gainean **Interesak** teila.

   > [!div class="mx-imgBorder"]
   > ![Markak eta zaletasunak lauzak.](media/BrandsInterest-tile-Hub.png "Markak eta zaletasunen lauzak")

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Zure herrialdea edo eskualdea aldatzeko, hautatu **Aldatu** Alboan **Herrialdea/Eskualdea**. urtean **Herrialde/Eskualde ezarpenak** panela, aukeratu a [onartzen den herrialdea/eskualdea](#supported-countriesregions) eta hautatu **Aplikatu**.

   > [!NOTE]
   > Zure markak aukeratzen dituzunean, sistemak hautatutako herrialdean edo eskualdean oinarritutako iradokizunak eskaintzen ditu. Sektorea aukeratzean, hautatutako herrialdean edo eskualdean oinarritutako marka edo interes garrantzitsuenak lortuko dituzu.

1. Aukeratu gehienez bost marka edo interes aukera hauetako bat edo biak erabiliz:

   - **Industria**: Aukeratu zure industria goitibeherako zerrendan eta aukeratu industria horretako marka edo interes gorenen artean.
   - **Aukeratu zeurea**: Sartu zure erakundearentzako garrantzitsua den marka edo interesa eta aukeratu bat datorren iradokizunen artean. Bilatzen ari zaren marka edo interesa zerrendatzen ez badugu, bidal iezaguzu iritzia erabilita **Proposatu** esteka.

1. Hautatu **Hurrengoa** eta berrikusi zure aberaste-hobespen lehenetsiak eta eguneratu behar izanez gero.

   :::image type="content" source="media/affinity-enrichment-preferences.png" alt-text="Aberasteko lehentasunen leihoaren pantaila-argazkia.":::

1. Hautatu **Hurrengoa**.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu Microsoft-en datuekin aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, eta segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Hautatu **Hurrengoa**.

1. Mapeatu zure eremuak zure bezero-entitate bateratutik Microsoft-eko datuetara.

   > [!NOTE]
   > Jaiotze-data edo genero-atributuak gutxienez behar dira. Herrialdea/eskualdea eta gutxienez hiria (eta estatua/probintzia) edo posta kodea behar dira. Datuak sartzen direnean jaiotze-data DateTime motara bihurtzea gomendatzen dugu. Bestela, katea izan daiteke [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) formatua "aaaa-MM-dd" edo "aaaa-MM-ddTHH: mm: ss".

1. Hautatu **Hurrengoa** eremuaren jarraipena osatzeko.

1. Idatzi aberastearen izena. The **Irteerako entitatearen izena** automatikoki hautatzen da.

   :::image type="content" source="media/enrichment-interests-summary.png" alt-text="Interesak berrikusteko eta izendatzeko orria.":::

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

   Noiz profil aberasgarriak, aberastuko ditugu hautatutako marken eta interesen datuak lortzeko bezeroen profil guztiak, hautatutako herrialdean edo eskualdean ez dauden profilak barne. Adibidez, Alemania aukeratu baduzu, Estatu Batuetan kokatutako profilak aberastuko ditugu AEBetan hautatutako marka eta interesetarako datuak eskuragarri baditugu.

## <a name="enrichment-results"></a>Aberastearen emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

:::image type="content" source="media/my-enrichments.png" alt-text="Abantaila prozesua exekutatu ondoren, emaitzen aurrebista.":::

Emaitzak barne hartzen ditu **Afinitate maila** edo **Ahotsaren partekatzea** taulak.

Aberasteetatik sortutako entitateak azpian daude zerrendatuta **Aberastea** taldean **Datuak** > **Entitateak**. Marken datu aberastuak **BrandAffinityFromMicrosoft** eta **BrandShareOfVoiceFromMicrosoft** entitateak. Interesen datuak atalean daude **InterestAffinityFromMicrosoft** eta **InterestShareOfVoiceFromMicrosoft** entitateak.

## <a name="see-enrichment-data-on-the-customer-card"></a>Ikusi aberastasun datuak bezeroaren txartelean

Marka eta interesa SoV bezero banakako txarteletan ere ikus daiteke. Joan **Bezeroak** atalera eta hautatu bezeroaren profila. Bezero-txartelean, marka edo interes SoVrako grafikoak aurkituko dituzu bezero horren profil demografikoko pertsonen arabera.

:::image type="content" source="media/enrichment-customer-card.png" alt-text="Aberastutako datuak dituen bezeroaren txartela.":::

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]


[!INCLUDE [footer-include](includes/footer-banner.md)]
