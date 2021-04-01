---
title: Konbinatu entitateak datuen bateratzean
description: Konbinatu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 04/16/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 737c593353878a5e322488d00de5dc5db5befda9
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597818"
---
# <a name="merge-entities"></a>Konbinatu entitateak

Konbinaketa fasea azken fasea da datuak bateratzeko prozesuan. Bere helburua gatazkako datuak bateratzea da. Datu gatazkatsu batzuen adibideetan zure datu multzoetako bi bezeroen izena aurki daiteke, baina bakoitza modu desberdinean agertzen da ("Grant Marshall" versus "Grant Marshal"), edo telefono zenbakia (617-803-091X versus 617803091X ). Datu-puntu gatazkatsu horiek batzea atributuak banatzen dira.

Bete ondoren [partidaren fasea](match-entities.md), batu fasea has dezakezu, hautatuta **konbinatu** lauza **bateratzeko** orria.

## <a name="review-system-recommendations"></a>Aztertu sistemaren gomendioak

Gainean **Konbinatu** orrialdea, zure bezeroaren profil bateratuaren entitatean bateratu beharreko atributuak aukeratu eta baztertu ditzakezu (konfigurazio prozesuaren emaitza). Zenbait atributu automatikoki bateratzen dira sistemak.

### <a name="view-merged-attributes"></a>Ikusi konbinatutako atributuak

Zure automatikoki batu diren atributuren batean sartutako atributuak ikusteko, hautatu batu atributu hori. Bateratutako atributua osatzen duten bi atributuak bi errenkada berri agertuko dira bateratutako atributuaren azpian.

> [!div class="mx-imgBorder"]
> ![Hautatu konbinatutako atributua](media/configure-data-merge-profile-attributes.png "Hautatu konbinatutako atributua")

### <a name="separate-merged-attributes"></a>Bereizi konbinatutako atributuak

Automatikoki batutako atributuak bereizteko edo desmerratzeko, bilatu atributua atalean **Profilaren atributuak** mahaia.

1. Hautatu elipsi (...) botoia.
  
2. Hautatu goitibeherako zerrendan **Eremu bereiziak**.

### <a name="remove-merged-attributes"></a>Kendu konbinatutako atributuak

Atributu bat bezeroaren azken profilaren entitatean baztertzeko, bilatu **Profilaren atributuak** mahaia.

1. Hautatu elipsi (...) botoia.
  
2. Hautatu goitibeherako zerrendan **Ez konbinatu**.

   Atributua mugitzen da **Bezeroaren erregistrotik kendu da** atalera.

## <a name="manually-add-a-merged-attribute"></a>Gehitu batutako atributua eskuz

Bateratutako atributu bat gehitzeko, joan " **Konbinatu** orria.

1. Hautatu **Gehitu konbinatutako atributua**.

2. Eman a **izena** identifikatzeko **konbinatu** orrialdea gero.

3. Aukeran, eman a **Bistaratu izena** hori bezeroaren profil bateratuko entitatean agertuko da.

4. Konfiguratu **Hautatu bikoiztutako atributuak** parekatutako entitateetatik batu nahi dituzun atributuak hautatzeko. Ezaugarriak bila ditzakezu.

5. Ezar ezazu **Sailkatu garrantziaren arabera** atributu bat besteen gainetik lehenestea. Adibidez, *WebAccountCSV* entitateak datuari buruzko datu zehatzenak biltzen ditu *Izen Osoak* atributuari lehentasuna eman diezaiokezu erakunde honi *ContactCSV* hautatuta *WebAccountCSV*. Ondorioz, *WebAccountCSV* lehen lehentasunera mugitzen da, berriz *ContactCSV* Balioak ateratzean bigarren lehentasunera pasatzen da *Izen osoa* atributu.

## <a name="run-your-merge"></a>Exekutatu zure bateratzea

Eskuz batu atributuak edo sistemak batzen dituzun ala ez, beti bat egin dezakezu. Hautatu **Exekutatu** **Konbinatu** orrian prozesua hasteko.

> [!div class="mx-imgBorder"]
> ![Datuen batzea Gorde eta Exekutatu](media/configure-data-merge-save-run.png "Datuen batzea Gorde eta Exekutatu")

Aldaketa gehigarriak egiteko eta pausoa berriro egiteko, aurrerapen bateratzea bertan behera utzi dezakezu. Aukeratu **Freskagarria ...** eta hautatu **Lana bertan behera utzi** agertzen den alboko panelean.

Ondoren **Freskagarria ...** testua aldatzen da **Arrakastatsua**, bateratu zure datuak kontradikzioak osatu eta ebatzi ditu zuk zehaztutako gidalerroen arabera. Bat egin eta bateratu gabeko atributuak profil bateratuko entitatean sartzen dira. Alde batera utzitako atributuak ez dira barne hartzen bateratutako entitate-profilean.

Bateratzea behar bezala egiten ez bazen lehenengo aldia bada, downstream-eko prozesu guztiak automatikoki berriro aberastuko dira, aberastasuna, segmentazioa eta neurriak barne. Beheranzko prozesu guztiak berriro egin ondoren, bezeroen profilek egindako aldaketak islatzen dituzte.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="next-step"></a>Hurrengo urratsa

Konfiguratu [jarduerak](activities.md), [aberastea](enrichment-microsoft-graph.md), edo [Harremanak](relationships.md) zure bezeroei buruzko ikuspegi gehiago lortzeko.

Jarduerak, aberastasuna edo harremanak konfiguratu badituzu edo segmentuak definitu badituzu, automatikoki prozesatuko dira bezeroen azken datuak erabiltzeko.




[!INCLUDE[footer-include](../includes/footer-banner.md)]