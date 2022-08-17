---
title: Ikusi sistemaren konfigurazioa
description: Eskuratu sistemaren ezarpenak buruz Dynamics 365 Customer Insights.
ms.date: 08/09/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-system-status
- ci-system-about
- ci-system-general
- ci-system-api-usage
- customerInsights
ms.openlocfilehash: 2498814a3d2e6330124fb97c036b9b310bcf1f7a
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9246232"
---
# <a name="view-system-configuration"></a>Ikusi sistemaren konfigurazioa

Ikusi sistemaren informazioa, sistemaren egoera eta APIaren erabilera.

## <a name="view-api-usage"></a>Ikusi APIaren erabilera

Ikusi denbora errealeko APIaren erabilerari buruzko xehetasunak eta ikusi zein gertakari gertatu diren denbora-tarte jakin batean.

1. Joan **Admin** > **Sistema** eta hautatu **API erabilera** fitxa.

1. **Hautatu denbora-tarte bat** ikusteko.

   The **API erabilera** orrialdeak hiru atal ditu:

   - **API deiak**: hautatutako epean APIra egindako deien kopuru agregatua bistaratzen duen taula.
   - **Datuen transferentzia**: hautatutako denbora tartean APIaren bidez transferitu diren datu kopurua erakusten duen taula.
   - **Eragiketak**: taula bat erabilgarri dauden API eragiketa bakoitzerako errenkadekin eta eragiketen erabilerari buruzko xehetasunak. Hautatu eragiketa-izen bat bertara joateko [API erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances).

   Erabiltzen duten eragiketak [denbora errealeko datuak sartzea](real-time-data-ingestion.md) ikur prismatiko bat edukitzea denbora errealeko APIaren erabilera ikusteko.

   1. Hautatu binokularra irekitzeko **Denbora errealeko APIaren erabilera** Eragiketaren erabilera xehetasunak dituen panela.
   1. **Hautatu denbora-tarte bat** ikusteko.
   1. Erabili **Taldeka** kutxa zure denbora errealeko elkarrekintzak nola aurkeztu onena aukeratzeko. Taldekatu datuak APIaren arabera **Metodoa**, **izen kualifikatua** (irensatutako entitatea), **Sortua** (gertaeraren iturria), **Emaitza** (arrakasta edo porrota) edo **Errore-kodeak**. Datuak historia-taula gisa eta taula gisa eskuragarri daude.

## <a name="view-system-information"></a>Ikusi sistemaren informazioa

Ikusi ingurunearen bistaratzeko izena, IDa, eskualdea, mota eta saioaren IDa.

1. Joan **Admin** > **Sistema** eta hautatu **Buruz** fitxa.

1. Hizkuntza eta herrialdea/eskualdea ikusteko, hautatu **Orokorra** fitxa.

### <a name="update-preferred-language-or-countryregion"></a>Eguneratu hobetsitako hizkuntza edo herrialdea/eskualdea

Bezeroen ikuspegiak [hizkuntza asko onartzen ditu](/dynamics365/get-started/availability). Aplikazioak zure hizkuntza-lehentasuna erabiliko du menua, etiketako testua eta sistemaren mezuak bezalako elementuak hobetsitako hizkuntzan erakusteko.

Eskuz sartu dituzun inportatutako datuak eta informazioa ez dira itzuliko.

1. Joan **Admin** > **Sistema** eta hautatu **Orokorra** fitxa.

1. Nahiago duzun hizkuntza aldatzeko, aukeratu a **Hizkuntza** goitibehera.

1. Data, ordua eta zenbakiak nahiago duzun formateatzea aldatzeko, erabili '... **Herrialdearen/Eskualdearen formatua** goitibeherako menuko. Formatuaren aurrebista bistaratzen da. Sistemak automatikoki aukeraketa bat iradokitzen du hizkuntza berri bat aukeratzen duzunean.

1. Sakatu **Gorde**.

## <a name="view-system-status"></a>Ikusi sistemaren egoera

Egin jarraipena eginkizunen, datuen sarreraren, datuen esportazioen eta beste hainbat produktu-prozesu garrantzitsuen aurrerapena. Berrikusi informazioa zure zeregin eta prozesu aktiboen osotasuna ziurtatzeko.

1. Joan **Admin** > **Sistema** eta hautatu **Egoera** fitxa.

   Hainbat prozesuren egoera eta prozesatzeko informazioa bistaratzea. Ikusi **Izena** zereginaren, du **Egoera** bere azkeneko ibilbidea, eta noiz izan zen **Azken eguneratua**.

1. Azken exekuzioen xehetasunak ikusteko, hautatu zeregina edo prozesuaren izena.

1. Zeregin baten aurrerapenaren xehetasunak ikusteko, hautatu egoera. The **Aurrerapen xehetasunak** panelak bistaratzen ditu.

   :::image type="content" source="media/system-progress-details.png" alt-text="Sistemaren aurrerapenaren xehetasunen panela":::

1. Zeregin guztien aurrerapenaren xehetasunak ikusteko, hautatu **Lan-fluxu osoa**.

### <a name="status-definitions"></a>Egoera definizioak

Sistemak egoera hauek erabiltzen ditu zeregin eta prozesuetarako:

|Fasea  |Definizioa  |
|---------|---------|
|Utzi da |Zeregin edo prozesua amaitu baino lehen bertan behera utzi du erabiltzaileak.   |
|Ezin izan da egin   |Zereginak edo prozesuak erroreak izan ditu.         |
|Huts egin du  |Zereginak edo prozesuak huts egin du.  |
|Ez da hasi   |datu-iturburu-k ez du daturik irensten oraindik edo zeregina zirriborro moduan dago oraindik.         |
|Prozesatze  |Zeregin edo prozesua abian da.  |
|Freskatzen    |Zeregin edo prozesua abian da. Eragiketa hau bertan behera uzteko, hautatu **Freskagarria** eta **Utzi lana**. Zeregin edo prozesu baten freskapena gelditzeak bere azken freskatze egoerara itzuliko du.       |
|Saltatuta  |Zeregin edo prozesua saltatu egin da. Zeregin hau kontrolatzen duen downstream-eko prozesu bat edo gehiago huts egin edo saihestu egiten dira.|
|Osatuta  |Zeregin edo prozesua behar bezala burutu da. Datu-iturburuetarako, datuak behar bezala irentsi direla adierazten du denboraren bat aipatzen bada **Freskatua** zutabea.|
|Ilaran | Prozesatzea ilaran dago eta gorako zeregin eta prozesu guztiak amaitutakoan hasiko da. Informazio gehiagorako, ikus [Freskatzeko prozesuak](#refresh-processes).|

### <a name="refresh-processes"></a>Freskatzeko prozesuak

Zereginen eta prozesuen freskatzearen arabera exekutatzen da [konfiguratutako ordutegia](schedule-refresh.md).

|Prozesua  |Deskribapenak  |
|---------|---------|
|Jarduera  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. Ikuspegiak prozesatzearen araberakoak dira.|
|Analisien estekatzea |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Analisien prestaketa |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Datu-prestaketa   |Exekutatzeko entitate bat behar du. datu-iturburu entitateak irenstearen araberakoak dira. Entitate aberastuak aberasteen araberakoak dira. Bezeroaren entitatea bateratzearen araberakoa da.  |
|Datu-iturburuak   |Ez dago beste prozesurik. Partida prozesu honen arrakastaren araberakoa da.  |
|Aberasteak   |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. |
|Esportazio-helmugak |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Xehetasunak |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Inteligentzia   |Batzearen araberakoa da.   |
|Lotu |Partiduen definizioan erabilitako datu-iturrien prozesamenduaren araberakoa da.      |
|Neurketak  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da.  |
|Konbinazioa   |Bat-etortzearen prozesuaren osatzearen araberakoa da. Segmentuak, neurriak, aberastea, bilaketa, jarduerak, iragarpenak eta datuen prestaketa prozesu honen arrakastaren araberakoak dira.   |
|Profilak   |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. |
|Bilatu?   |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. |
|Segmentuak  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. Ikuspegiak prozesatzearen araberakoak dira.|
|Sistema   |Bat-etortzearen prozesuaren osatzearen araberakoa da. Segmentuak, neurriak, aberastea, bilaketa, jarduerak, iragarpenak eta datuen prestaketa prozesu honen arrakastaren araberakoak dira.   |
|User  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Entitateen araberakoa da.  |

Hautatu prozesu baten egoera lan guztiaren aurrerapenaren xehetasunak ikusteko. Goiko freskatze prozesuek a konpontzeko zer egin dezakezun ulertzen lagun dezakete **Saltatu** edo **Ilaran jarrita** zeregina edo prozesua.


[!INCLUDE [footer-include](includes/footer-banner.md)]
