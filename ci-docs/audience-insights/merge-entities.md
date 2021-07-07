---
title: Konbinatu entitateak datuen bateratzean
description: Konbinatu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 05/10/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 86ab3cefa70e5fab4bdb27cde363adee26efee4c
ms.sourcegitcommit: 0b754d194d765afef70d1008db7b347dd1f0ee40
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6305605"
---
# <a name="merge-entities"></a>Konbinatu entitateak

Konbinaketa fasea azken fasea da datuak bateratzeko prozesuan. Bere helburua gatazkako datuak bateratzea da. Datu gatazkatsu batzuen adibideetan zure datu multzoetako bi bezeroen izena aurki daiteke, baina bakoitza modu desberdinean agertzen da ("Grant Marshall" versus "Grant Marshal"), edo telefono zenbakia (617-803-091X versus 617803091X ). Datu-puntu gatazkatsu horiek batzea atributuak banatzen dira.

:::image type="content" source="media/merge-fields-page.png" alt-text="Batu orria datuak bateratzeko prozesuan bezeroaren profil bateratua definitzen duten eremu bateratuekin taula erakusten duena.":::

Bete ondoren [partidaren fasea](match-entities.md), batu fasea has dezakezu, hautatuta **konbinatu** lauza **bateratzeko** orria.

## <a name="review-system-recommendations"></a>Aztertu sistemaren gomendioak

**Datuak** > **Bat egin** > **Batu** aukeran, atributuak aukeratu eta baztertzen dituzu bezeroaren profileko entitate bateratuan bateratzeko. Bezeroen profil bateratua datuak bateratzeko prozesuaren emaitza da. Zenbait atributu automatikoki bateratzen dira sistemak.

Automatikoki bateratutako atributuetako batean sartutako atributuak ikusteko, hautatu bateratutako atributu hori **Bezeroen eremuak** taularen fitxa. Bateratutako atributua osatzen duten bi atributuak bi errenkada berri bistaratuko dira bateratutako atributuaren azpian.

## <a name="separate-rename-exclude-and-edit-merged-fields"></a>Bereiztu, aldatu izena, baztertu eta editatu bateratutako eremuak

Sistemak bateratutako atributuak nola prozesatzen dituen alda dezakezu bezeroaren profil bateratua sortzeko. Aukeratu **Erakutsi gehiago** eta aukeratu zer aldatu nahi duzun.

:::image type="content" source="media/manage-merged-attributes.png" alt-text="Aukerak Erakutsi goitibeherako menuan bateratutako atributuak kudeatzeko.":::

Informazio gehiagorako, ikus ondorengo atalak.

## <a name="separate-merged-fields"></a>Zatitu konbinatutako eremuak

Batutako eremuak bereizteko, bilatu atributua taulan. Bereizitako eremuak bezeroaren profil bateratuan banakako datu gisa agertzen dira. 

1. Hautatu konbinatutako eremua.
  
1. Aukeratu **Erakutsi gehiago** eta aukeratu **Eremu bereiziak**.
 
1. Berretsi zatiketa.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.

## <a name="rename-merged-fields"></a>Aldatu bateratutako eremuak

Aldatu bateratutako atributuen bistaratzeko izena. Ezin duzu aldatu irteerako entitatearen izena.

1. Hautatu konbinatutako eremua.
  
1. Aukeratu **Erakutsi gehiago** eta aukeratu **Aldatu izena**.

1. Berretsi aldatutako bistaratzeko izena. 

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.

## <a name="exclude-merged-fields"></a>Baztertu konbinatutako eremuak

Baztertu atributu bat konbinatutako bezeroaren profiletik. Eremua beste prozesu batzuetan erabiltzen bada, adibidez segmentu batean, ezabatu prozesu hauetatik bezeroaren profiletik baztertu aurretik. 

1. Hautatu konbinatutako eremua.
  
1. Aukeratu **Erakutsi gehiago** eta aukeratu **Baztertu**.

1. Berretsi bazterketa.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko. 

**Batu** orrian, hautatu **Baztertutako eremuak** baztertutako eremu guztien zerrenda ikusteko. Panel honek baztertutako eremuak berriro gehitzeko aukera ematen du.

## <a name="manually-combine-fields"></a>Konbinatu eremuak eskuz

Zehaztu bateratutako atributu bat eskuz. 

1. **Batu** orrian, hautatu **Konbinatu eremuak**.

1. Eman **Izena** bat eta **Irteerako eremuaren izena**.

1. Aukeratu gehituko duzun eremua. Hautatu **Gehitu eremuak** eremu gehiago konbinatzeko.

1. Berretsi bazterketa.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko. 

## <a name="change-the-order-of-fields"></a>Aldatu eremuen ordena

Entitate batzuek besteek baino xehetasun gehiago dituzte. Entitate batek eremu bati buruzko azken datuak biltzen baditu, baliteke bat egitean lehentasuna eman diezaiokezu beste entitateei.

1. Hautatu konbinatutako eremua.
  
1. Aukeratu **Erakutsi gehiago** eta aukeratu **Editatu**.

1. Urtean **Konbinatu eremuak** panela, hautatu **Mugitu gora edo behera** ordena ezartzeko edo arrastatu eta askatu nahi duzun posizioan.

1. Berretsi aldaketa.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.

## <a name="run-your-merge"></a>Exekutatu zure bateratzea

Eskuz batu atributuak edo sistemak batzen dituzun ala ez, beti bat egin dezakezu. Hautatu **Exekutatu** **Konbinatu** orrian prozesua hasteko.

> [!div class="mx-imgBorder"]
> ![Datuen batzea Gorde eta Exekutatu](media/configure-data-merge-save-run.png "Datuen batzea Gorde eta Exekutatu")

Aukeratu **Exekutatu soilik Batu** bezero entitate bateratuan islatutako irteera soilik ikusi nahi baduzu. Beherantz egindako prozesuak bezala freskatuko dira [freskatze-programan definitzen da](system.md#schedule-tab).

Aukeratu **Exekutatu, konbinatu eta erraztu prozesuak** sistema zure aldaketekin freskatzeko. Prozesu guztiak, aberastea, segmentuak eta neurriak barne automatikoki berriro abiaraziko dira. Erraztu prozesu guztiak amaitu ondoren, bezeroen profilek egindako aldaketak islatzen dituzte.

Aldaketa gehiago egiteko eta urratsa berriro exekutatzeko, abian den bateratze bat bertan behera utzi dezakezu. Aukeratu **Freskagarria ...** eta hautatu **Lana bertan behera utzi** agertzen den alboko panelean.

> [!TIP]
> Zereginen/prozesuen [sei egoera mota](system.md#status-types) daude. Gainera, prozesu gehienak [downstream-eko beste prozesu batzuen mende daude](system.md#refresh-policies). Aukeratu prozesu baten egoera, egon zen lan osoaren aurrerapen xehetasunak ikusteko. Aukeratu ondoren **Ikusi xehetasunak** lanaren zereginetako baterako, informazio osagarria aurkituko duzu: prozesatzeko denbora, azken prozesatze data eta zereginarekin lotutako akats eta abisu guztiak.

## <a name="next-step"></a>Hurrengo urratsa

Konfiguratu [jarduerak](activities.md), [aberastea](enrichment-hub.md), edo [Harremanak](relationships.md) zure bezeroei buruzko ikuspegi gehiago lortzeko.

Aurretik jarduerak, aberastasuna edo segmentuak konfiguratu badituzu, automatikoki prozesatuko dira bezeroen azken datuak erabiltzeko.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
