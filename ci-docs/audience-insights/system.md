---
title: Sistemaren konfigurazioa hartzaileen xehetasunetan
description: Lortu informazio sistemaren ezarpenei buruz Dynamics 365 Customer Insights audientziari buruzko informazio-gaitasunean.
ms.date: 11/01/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: NimrodMagen
ms.author: nimagen
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 1b790106f8b9617d0c1f244e1d15a74c7ef9a82b
ms.sourcegitcommit: 834651b933b1e50e7557d44f926a3fb757c1f83a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/02/2021
ms.locfileid: "7732344"
---
# <a name="system-configuration"></a>Sistemaren konfigurazioa

Ikusleen informazioetan sistemaren konfigurazioetara sartzeko, hautatu ezkerreko nabigazio-barran **Admin** > **Sistema** sistemako zereginen eta prozesuen zerrenda ikusteko.

**Sistema** orriak fitxa hauek ditu:
- [Fasea](#status-tab)
- [Antolaketa](#schedule-tab)
- [API erabilera](#api-usage-tab)
- [Honi buruz](#about-tab)
- [Orokorrak](#general-tab)
- [Segurtasuna](#security-tab)

:::image type="content" source="media/system-tabs.png" alt-text="Sistemaren orrian ezarpenen fitxak.":::

## <a name="status-tab"></a>Egoera fitxa

The **Egoera fitxa** zereginen, datuen sarreraren, datuen esportazioen eta beste hainbat produktu-prozesu garrantzitsuen jarraipena egiteko aukera ematen du. Berrikusi fitxa honetako informazioa zure zeregin eta prozesu aktiboen osotasuna ziurtatzeko.

Fitxa honek hainbat prozesurako egoera eta prozesatzeko informazioa duten taulak biltzen ditu. Taula bakoitzak jarraipena egiten du **izena** zeregina eta dagokion entitatea da **Egoera** bere korrika berriena eta noiz izan zen **Azken eguneraketa**. Azken exekuzioen xehetasunak ikus ditzakezu ataza edo prozesuaren izena hautatuta. 

Hautatu ataza edo prozesuaren ondoan dagoen egoera **Egoera** zutabea irekitzeko **Aurrerapen xehetasunak** panela.

   :::image type="content" source="media/system-progress-details.png" alt-text="Sistemaren aurrerapenaren xehetasunen panela":::

### <a name="status-definitions"></a>Egoeraren definizioak

Sistemak egoera hauek erabiltzen ditu zereginetarako eta prozesuetarako:

|Fasea  |Definizioa  |
|---------|---------|
|Utzi da |Prozesatzea amaitu baino lehen bertan behera utzi du erabiltzaileak.   |
|Huts eginda   |Datuen iradokizunak akatsak izan ditu.         |
|Huts egin du  |Prozesatzeak huts egin du.  |
|Hasi gabe   |Datu-iturburuak oraindik ez du daturik sartu edo oraindik zirriborro moduan daude.         |
|Prozesatze  |Zeregin edo prozesua abian da.  |
|Freskatzen    |Datuen horniketa martxan da. Eragiketa hau bertan behera utzi dezakezu **Utzi freskagarria** herrian **Ekintzak** zutabea. datu-iturburu-en freskagarria gelditzeak azken freskatze egoeran itzuliko du.       |
|Saltatuta  |Zeregin edo prozesua saltatu egin da. Zeregin hau kontrolatzen duen downstream-eko prozesu bat edo gehiago huts egin edo saihestu egiten dira.|
|Osatuta  |Zeregin edo prozesua behar bezala burutu da. Datu-iturburuetarako, datuak behar bezala irentsi direla adierazten du denboraren bat aipatzen bada **Freskatua** zutabea.|
|Ilaran | Prozesatzea ilaran dago eta gorako zeregin eta prozesu guztiak amaitutakoan hasiko da. Informazio gehiagorako, ikus [Freskatzeko prozesuak](#refresh-processes).|

### <a name="refresh-processes"></a>Freskatzeko prozesuak

Zereginen eta prozesuen freskatzearen arabera exekutatzen da [konfiguratutako ordutegia](#schedule-tab). 

|Prozesua  |Deskribapenak  |
|---------|---------|
|Jarduera  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. Ikuspegiak prozesatzearen araberakoak dira.|
|Analisien estekatzea |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Analisien prestaketa |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Datu-prestaketa   |Batzearen araberakoa da.   |
|Datu-iturburuak   |Ez dago beste prozesurik. Partida prozesu honen arrakastaren araberakoa da.  |
|Aberasteak   |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. |
|Esportazio-helmugak |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Xehetasunak |Eskuz exekutatzen da (denbora bakarreko freskagarria). Segmentuen araberakoa da.  |
|Adimena   |Batzearen araberakoa da.   |
|Lotu |Partiduen definizioan erabilitako datu-iturrien prozesamenduaren araberakoa da.      |
|Neurketak  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da.  |
|Konbinazioa   |Bat-etortzearen prozesuaren osatzearen araberakoa da. Segmentuak, neurriak, aberastea, bilaketa, jarduerak, iragarpenak eta datuen prestaketa prozesu honen arrakastaren araberakoak dira.   |
|Profilak   |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. |
|Bilaketa   |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. |
|Segmentuak  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Batze-prozesuaren araberakoa da. Ikuspegiak prozesatzearen araberakoak dira.|
|Sistema   |Bat-etortzearen prozesuaren osatzearen araberakoa da. Segmentuak, neurriak, aberastea, bilaketa, jarduerak, iragarpenak eta datuen prestaketa prozesu honen arrakastaren araberakoak dira.   |
|Erabiltzailea  |Eskuz exekutatzen da (denbora bakarreko freskagarria). Entitateen araberakoa da.  |

Hautatu prozesu baten egoera lan guztiaren aurrerapenaren xehetasunak ikusteko. Goiko freskatze prozesuek a konpontzeko zer egin dezakezun ulertzen lagun dezakete **Saltatu** edo **Ilaran jarrita** zeregina edo prozesua.

## <a name="schedule-tab"></a>Antolaketa fitxa

Erabili **Antolaketa** fitxa [sartutako datu-iturburuen](data-sources.md) freskatze automatikoak antolatzeko. Freskatze automatikoak zure datuen iturrien eguneratzeak zure bezeroen profil bateratuetan islatzen laguntzen du.

1. Hartzaileen xehetasunetan, joan hona: **Administratzailea** > **Sistema** eta hautatu **Antolaketa** fitxa.

2. Aurreikusitako freskagarriaren egoera lehenetsia da **itzalita**. Programatutako freskariak gaitzeko, aldatu pantailaren goiko aldean txandakatzeko aukera **Aktibatu**.

3. Aukeratu artean **Asterokoa** (lehenetsia) eta **Egunekoa** freskatzen. Astean freskagarriak antolatzeko asmoa baduzu, hautatu freskagarria exekutatu nahi duzun egun bat edo gehiago.

4. Ezarri zure **Ordu eremu** eta ondoren erabili **Ordua** goitibeherako zure freskatze-denbora ezartzeko. Bukatu duzunean, hautatu **Ezarri** aukera. Egun bakarrean hainbat freskatze programatu nahi badituzu, hautatu **Gehitu beste denbora**.

5. Aldaketak aplikatzeko, hautatu **Gorde**.

## <a name="about-tab"></a>Fitxari buruz

**Buruz** fitxan zure erakundearenak daude **Bistaratu izena**, aktiboa **Ingurumenaren IDa**, **Eskualdea**, eta zure **Saioaren IDa**. Laneko ingurune bat baino gehiago baduzu, bakoitzari erraz identifikatzeko bistaratzeko izena eman beharko zenioke.

## <a name="general-tab"></a>Fitxa orokorra

Hizkuntza eta herrialde/eskualde formatua alda ditzakezu **Orokorra** fitxan.

Bezeroen ikuspegiak [hizkuntza asko onartzen ditu](/dynamics365/get-started/availability). Aplikazioak zure hizkuntza-lehentasuna erabiliko du menua, etiketako testua eta sistemaren mezuak bezalako elementuak hobetsitako hizkuntzan erakusteko.

Eskuz sartu dituzun inportatutako datuak eta informazioa ez dira itzuliko.

### <a name="update-the-settings"></a>Eguneratu ezarpenak

Nahiago duzun hizkuntza aldatzeko, aukeratu a **Hizkuntza** goitibehera.

Data, ordua eta zenbakiak nahiago duzun formateatzea aldatzeko, erabili '... **Herrialdearen/Eskualdearen formatua** goitibeherako menuko. Eremu honen azpian formateatze aurrebista bistaratzen da. Sistemak automatikoki hautapen bat proposatuko du hizkuntza berria aukeratzen duzunean.

Hautatu **Gorde** zure aukerak baieztatzeko.

## <a name="api-usage-tab"></a>APIaren erabilera fitxa

Bilatu denbora errealeko APIaren erabilerari buruzko xehetasunak eta ikusi denbora-tarte jakin batean zein gertaera gertatu diren. Denboraren denbora tartea aukeratzen duzu **Aukeratu denbora markoa** goitibeherako menua. 

**APIaren erabilera** hiru atal ditu: 
- **API deiak**: hautatutako epean APIra egindako deien kopuru agregatua bistaratzen duen taula.

- **Datuen transferentzia**: hautatutako denbora tartean APIaren bidez transferitu diren datu kopurua erakusten duen taula.

-  **Eragiketak**: taula bat erabilgarri dauden API eragiketa bakoitzerako errenkadekin eta eragiketen erabilerari buruzko xehetasunak. Joan nahi duzun eragiketaren izena hauta dezakezu [APIaren erreferentzia](https://developer.ci.ai.dynamics.com/api-details#api=CustomerInsights&operation=Get-all-instances).

   Erabiltzen duten eragiketak [denbora errealeko datuak sartzea](real-time-data-ingestion.md) ikur prismatiko bat duen botoi bat edukitzea denbora errealeko APIaren erabilera ikusteko. Aukeratu botoia APIaren denbora errealeko uneko inguruneko erabilerari buruzko xehetasunak dituen alboko panela irekitzeko.   
   Erabili **Taldekatu honen arabera** koadroan **APIaren erabilera denbora errealean** panelean denbora errealeko elkarrekintzak nola aurkeztu behar diren aukeratzeko. Datuak API metodoaren, entitatearen izen kualifikatua (irenstutako entitatea), sortutako (gertaeraren iturria), emaitza (arrakasta edo hutsegitea) edo errore kodeak arabera talka ditzakezu. Datuak historia-taula gisa eta taula gisa eskuragarri daude.

## <a name="security-tab"></a>Segurtasun-fitxa

**Segurtasuna** fitxak [Azure key vault](/azure/key-vault/general/basic-concepts) inguruneari lotu eta kudeatzeko aukera ematen dizu.
Eskainitako gako-ganga erakundearen betetze-mugan sekretuak agertzeko eta erabiltzeko erabil daiteke. Ikusleen estatistikek Azure Key Vault-eko sekretuak erabil ditzakete [konexioak konfiguratu](connections.md) hirugarrenen sistemetara.

Informazio gehiagorako, ikus [Ekarri zure Azure key vault](use-azure-key-vault.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
