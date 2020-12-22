---
title: Erabili datu-iturburuak datuak sartzeko
description: Ikasi iturri desberdinetako datuak nola inportatu.
ms.date: 11/03/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: adkuppa
manager: shellyha
ms.openlocfilehash: a720641f7499fc71ff5bceeba48d296c51f77242
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643938"
---
# <a name="overview-about-data-sources"></a>Ikuspegi orokorra datu-iturburuei buruzkoa

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Dynamics 365 Customer Insights-eko hartzaileen xehetasunen gaitasuna iturburu multzo zabal bateko datuekin konektatzen da. datu-iturburu-era konektatzearen prozesua sarritan aipatzen da *datuen irenstea*. Datuak irentsi ondoren, egin dezakezu [bateratu](data-unification.md) eta neurriak hartu.

## <a name="add-a-data-source"></a>Gehitu datu-iturburua

datu-iturburu bat gehitzeko artikulu zehatzak ikusi, aukeratutako aukeraren arabera.

datu-iturburu bat gehi dezakezu hiru modu nagusitan:

- [Dozenaka Power Query lokailuren bidez](connect-power-query.md)
- [Hurrengotik Common Data Model-eko karpeta bat](connect-common-data-model.md)
- [Zuretik Common Data Service lakua](connect-common-data-service-lake.md)

> [!NOTE]
> Ezin dituzu lokal datu iturrietako datuak gehitu oraindik.

## <a name="review-ingested-data"></a>Berrikusi sartutako datuak

Irentsitako datu-iturburu bakoitzaren izena, bere egoera eta iturri horretako datuak berritu ziren azken aldia ikusiko dituzu. Datu-iturburuen zerrenda zutabe bakoitzaren arabera ordenatu dezakezu.

> [!div class="mx-imgBorder"]
> ![Gehitutako datu-iturriak](media/configure-data-datasource-added.png "Gehitutako datu-iturriak")

|Egoera  |Deskribapena  |
|---------|---------|
|Ongi egin da   |Datu-iturburu sartu da **Freskatuta** zutabean denbora-tartea adierazten bada.
|Ez da hasi   |Datu-iturburuak oraindik ez du daturik sartu edo oraindik zirriborro moduan daude.         |
|Freskatzen    |Datuen horniketa martxan da. Eragiketa hau bertan behera utzi dezakezu **Utzi freskagarria** herrian **Ekintzak** zutabea. datu-iturburu-en freskagarria gelditzeak azken freskatze egoeran itzuliko du.       |
|Ezin izan da egin     |Datuen iradokizunak akatsak izan ditu.         |

Aukeratu **Freskatu egoera** freskatze egoerari buruzko xehetasun gehiago berrikusteko, erroreen xehetasunak eta beherako prozesuen eguneratzeak barne.

Datuak kargatzea denbora har dezake. Freskatu ondoren, iradokitako datuak berrikusi daitezke **erakundeak** orria. Informazio gehiago lortzeko, [Entitateak](entities.md).

## <a name="refresh-a-data-source"></a>Freskatu datu-iturburu bat

Datu-iturburuak antolaketa automatikoan freska daitezke edo eskuz freskatu, beharraren arabera. 

Joan **Administratzailea** > **Sistema** > [**Antolaketa**](system.md#schedule-tab) atalera sartutako datu-iturburu guztien freskatze antolatuak konfiguratzeko.

Eskatu ahalako datu-iturburu bat freskatzeko, jarraitu urrats hauek:

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**

2. Hautatu freskatu nahi duzun datu-iturburuaren ondoko elipsi bertikala eta hautatu **Freskatu** goitibeherako zerrendatik.

3. Datu-iturburua eskuz eguneratzeko aktibatuta dago. Datu-iturburua freskatuz gero, entitateen eskema zein datu-iturburuan zehaztutako entitateetako datuak eguneratuko dira.

4. Aukeratu **Freskatzeari utzi** lehendik dagoen freskatzea bertan behera utzi nahi baduzu, eta datu-iturburua bere azken eguneratze-egoerara itzuliko da.

## <a name="delete-a-data-source"></a>Ezabatu datu-iturri bat

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Hautatu kendu nahi duzun datu-iturburu ondoko elipsi bertikala eta hautatu **Ezabatu** goitibeherako menuan.

3. Berretsi ezabatu nahi duzula.
