---
title: Aberastu bezeroen profilak Microsoft Graph-ekin
description: Erabili jabedun Microsoft Graph-en datuak bezeroaren datuak aberasteko marka eta interes afinitateekin.
ms.date: 09/28/2020
ms.reviewer: kishorem
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 4f93a2337815f76b98185ecb3755e08443031748
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404964"
---
# <a name="enrich-customer-profiles-with-brand-and-interest-affinities-preview"></a>Aberastu bezeroen profilak marka eta interes kidetasunekin (aurrebista)

Erabili jabedun Microsoft Graph-en datuak bezeroaren datuak aberasteko marka eta interes afinitateekin. Afinitate horiek zure bezeroen antzeko demografia duten pertsonen datuetan oinarrituta zehazten dira. Informazio honek bezeroak hobeto ulertzen eta segmentatzen laguntzen du, marka eta interes jakin batzuen arabera.

Hartzaileen xehetasunetan, joan hona: **Datuak** > **Aberastea** [aberasteak konfiguratu eta ikusteko](enrichment-hub.md).

Marka afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Markak** teila.

Interes afinitateak aberastea konfiguratzeko, joan **Ezagutu** fitxa eta aukeratu **Aberastu nire datuak** gainean **Interesak** teila.

   > [!div class="mx-imgBorder"]
   > ![Markak eta interesen lauzak](media/BrandsInterest-tile-Hub.png "Markak eta interesaren lauzak")

## <a name="about-microsoft-graph"></a>Microsoft Graph-i buruz

Microsoft Graph-eko lineako bilaketa datuak erabiltzen ditugu marka eta interesen afinitateak aurkitzeko hainbat segmentu demografikoetan (adinaren, generoaren edo kokapenen arabera definituta). Marka edo interes baten bilaketa-bolumenak zehazten du zein den afinitate batek segmentu demografiko batek, beste segmentu batzuekin alderatuta, marka edo interes hori.

[Informazio gehiago Microsoft Graph-i buruz](https://docs.microsoft.com/graph/overview).

## <a name="affinity-score-and-confidence"></a>Afinitate puntuazioa eta konfiantza

**Afinitate puntuazioa** 100 puntuko eskalan kalkulatzen da, 100 markako edo interesarekiko afinitate handiena duen segmentua ordezkatuz.

**Afinitate konfiantza** 100 puntuko eskalan ere kalkulatzen da. Sistemaren konfiantza maila adierazten du segmentu batek marka edo interesarekiko afinitatea duela. Konfiantza maila segmentuaren tamainan eta segmentuaren granularitatean oinarritzen da. Segmentuaren tamaina segmentu jakin baterako daukagun datu kopuruaren arabera zehazten da. Segmentuen granularitatea profil batean zenbat atributu (adina, generoa, kokapena) erabilgarri dauden zehazten da.

Ez ditugu normalizatzen zure datu-baseko puntuazioak. Hori dela eta, agian ez duzu zure datu-multzoarentzako afinitate-puntuazio balore guztiak ikusten. Adibidez, baliteke zure datuetan ez izatea 100 afinitate puntuarekin bezeroaren profil aberastua. Hori posible da marka edo interes jakin baterako 100 puntuazio lortu dituen segmentu demografikoan ez badago.

> [!TIP]
> [segmentuak sortuz](segments.md) afinitate puntuazioak erabiltzean, berrikusi zure datu multzoko afinitate puntuazioen banaketa puntuazio atalase egokiak erabaki aurretik. Adibidez, 10 kidetasun puntuazioa esanguratsua izan daiteke marka edo interes jakin baterako 25 soilik duten afinitate puntuazio altuena.

## <a name="supported-countriesregions"></a>Lagundutako herrialde / eskualdeak

Egun, herrialde / eskualdeko aukerak onartzen ditugu: Australia, Kanada (ingelesa), Frantzia, Alemania, Erresuma Batua edo Estatu Batuak (ingelesa).

Herrialdea hautatzeko, ireki **Marken aberastasuna** edo **Interesak aberastea** eta hautatu **Aldaketa** Alboan **Herrialdea / eskualdea**. Sarbidean **Herrialdearen eta eskualdeen ezarpenak** panela, aukeratu aukera bat eta hautatu **aplikatu**.

### <a name="implications-related-to-country-selection"></a>Herrialdearen hautaketarekin lotutako ondorioak

- Noiz [zure marka aukeratu](#define-your-brands-or-interests), iradokizunak emango ditugu hautatutako herrialde / eskualdearen arabera.

- Noiz [industria aukeratzea](#define-your-brands-or-interests), hautatutako herrialde / eskualdean oinarritutako marka edo interes garrantzitsuenak identifikatuko ditugu.

- Noiz [zure eremuen mapa](#map-your-fields), Herrialdea / Eskualdea eremua ez bada mapatzen, aukeratutako herrialde / eskualdeko Microsoft Graph datuak erabiliko ditugu zure bezeroen profilak aberasteko. Aukeraketa hori ere erabiliko dugu herrialde / eskualdeko datuak eskuragarri ez dituzten zure bezero profilak aberasteko.

- Noiz [profil aberasgarriak](#refresh-enrichment), bezeroen profil guztiak aberastuko ditugu, aukeratutako marka eta interesetarako eskuragarri ditugun Microsoft Graph datuak, hautatutako herrialde / eskualdean ez dauden profilak barne. Adibidez, Alemania aukeratu baduzu, Estatu Batuetan kokatutako profilak aberastuko ditugu baldin eta AEBetan hautatutako marka eta interesetarako Microsoft Graph datuak eskura baditugu.

## <a name="configure-enrichment"></a>Aberastea konfiguratu

Markak edo interesak aberastea konfiguratzeak bi pauso ditu:

### <a name="define-your-brands-or-interests"></a>Zehaztu zure markak edo zaletasunak

Hautatu aukera hauetariko bat:

- **Industria**: Sistemak zure industrian garrantzitsuak diren marka edo interesak identifikatzen ditu eta zure bezeroaren datuak aberasten ditu.
- **Aukeratu zeurea**: Zure erakunderako garrantzitsuenak diren marka edo interesen zerrendako bost elementu aukeratu.

Marka edo interesa gehitzeko, sartu sarrerako eremuan, datozen terminoen araberako iradokizunak jasotzeko. Bilatzen ari zaren marka edo interesa zerrendatzen ez badugu, bidal iezaguzu iritzia erabilita **Proposatu** esteka.

### <a name="map-your-fields"></a>Esleitu eremuak

Egin mapak zure bezero-erakunde bateratutik gutxienez bi atributuetara, bezeroaren datuak aberasteko erabili nahi dugun segmentu demografikoa definitzeko. Aukeratu **Editatu** eremuen mapa zehaztu eta hautatu **aplikatu** amaitutakoan. Aukeratu **Gorde** eremuaren mapa osatzeko.

Formatu eta balio hauek onartzen dira, balioak ez dira maiuskulak:

- **Jaioteguna**: Jaiotze-data DataTime motara bihurtzea gomendatzen dugu datuak irensten diren bitartean. Bestela, barruko katea izan daiteke [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) "uuuu-HH-ee" edo "uuuu-HH-eeHH:mm:ssZ" formatua.
- **Generoa**: Gizona, Emakumezkoa, Ezezaguna
- **Posta kodea**: Bost digitu ZIP kodea AEBetarako, posta estandarraren beste edozein lekutan
- **hiria**: Hiria izena ingelesez
- **Estatua / Probintzia**: AEB eta Kanadako bi gutun-laburdura. Bi edo hiru gutun laburdura Australiarako. Ez da aplikagarria Frantzian, Alemanian edo Erresuma Batuan.
- **Herrialdea/Eskualdea**:

  - AEB: Ameriketako Estatu Batuak, Estatu Batuak, AEBak, AEBak, Amerika
  - CA: Kanada, CA
  - GB: Erresuma Batua, Erresuma Batua, Britainia Handia, GB, Britainia Handia eta Ipar Irlanda, Erresuma Batua
  - AU: Australia, AU, Australiako Aberastasun Komuna
  - FR: Frantzia, FR, Frantziar Errepublika
  - DE: Alemania, Alemania, Deutschland, Allemagne, DE, Alemaniako Errepublika Federala, Alemaniako Errepublika

## <a name="refresh-enrichment"></a>Freskatu aberastea

Exekutatu aberastasuna marka, interesak eta eremuen mapak konfiguratu ondoren demografiarako. Prozesua hasteko, hautatu **Korrika egin** marka edo interesen konfigurazio orrian. Gainera, sistemak aberastasuna automatikoki utz dezakezu planifikatu gabeko freskatze baten baitan.
Bezeroaren datuen tamainaren arabera, minutu batzuk behar izango dira aberasteko exekuzioa osatzeko.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberaste prozesua exekutatu ostean, joan **Nire aberasteak** berrikusteko guztira aberastutako bezeroen kopurua eta aberastutako bezeroen profilen marka eta interesen banaketa.

:::image type="content" source="media/my-enrichments.png" alt-text="Abantaila prozesua exekutatu ondoren, emaitzen aurrebista":::

Berrikusi aberastutako datuak, hautatuta **Ikusi aberastutako datuak** grafikoan. Marken datu aberastuak: **BrandAffinityFromMicrosoft** Erakunde. Interesen datuak datuak daude **InterestAffinityFromMicrosoft** Erakunde. Erakunde hauek zerrendan aurkituko dituzu **aberastea** taldean **Datuak** > **erakundeak** atalean.

## <a name="see-enrichment-data-on-the-customer-card"></a>Ikusi aberastasun datuak bezeroaren txartelean

Marka eta interes kidetasunak bezero banakako txarteletan ere ikus daitezke. Joan **Bezeroak** atalera eta hautatu bezeroaren profila. Bezeroaren txartelean, bezeroaren demografia profil horretako pertsonek afinitatea duten marken edo interesen zerrendak aurkituko dituzu.

:::image type="content" source="media/enrichment-customer-card.png" alt-text="Aberastutako datuak dituen bezeroaren txartela":::

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Sortu [segmentuak](segments.md), [Neurriak](measures.md), eta baita [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.
