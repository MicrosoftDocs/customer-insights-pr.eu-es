---
title: Konbinatu entitateak datuen bateratzean
description: Konbinatu entitateak bezeroen profil bateratuak sortzeko.
ms.date: 01/28/2022
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: tutorial
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-merge
ms.openlocfilehash: eb08ab38d23bf22a17896b63c93e6821431b002a
ms.sourcegitcommit: 3807202283dd116a30f900a163d8141db621e5a8
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 01/28/2022
ms.locfileid: "8046548"
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

## <a name="edit-a-merged-field"></a>Editatu konbinatutako eremua

1.  Hautatu konbinatutako eremua.

1.  Aukeratu **Erakutsi gehiago** eta aukeratu **Editatu**.

1.  Zehaztu nola konbinatu eremuak hiru aukera hauetatik:
    - **Garrantzia**: balio nagusia identifikatzen du parte hartzen duten zehaztutako eremuen garrantziaren sailkapenean oinarrituta. Hori da konbinatzeko aukera lehenetsia. Garrantziaren araberako sailkapena ezartzeko, hautatu **Eraman gora/behera**.
    :::image type="content" source="media/importance-merge-option.png" alt-text="Garrantziaren aukera eremuak konbinatzeko elkarrizketan."::: 
    - **Azkena**: balio nagusia identifikatzen du, berritasunaren arabera. Berritasuna definitzeko, data edo zenbakizko eremua behar da eremuak konbinatzeko esparruan parte hartzen duen entitate bakoitzerako.
    :::image type="content" source="media/recency-merge-option.png" alt-text="Berritasunaren aukera eremuak konbinatzeko elkarrizketan.":::
    - **Zaharrena**: balio nagusia identifikatzen du, zahartasunaren arabera. Berritasuna definitzeko, data edo zenbakizko eremua behar da eremuak konbinatzeko esparruan parte hartzen duen entitate bakoitzerako.

1.  Eremu gehiago gehitu ditzakezu bateratze prozesuan parte hartzeko.

1.  Konbinatutako eremuaren izena alda dezakezu.

1. Aldaketak aplikatzeko, hautatu **Eginda**.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko. 

## <a name="combine-fields-manually"></a>Konbinatu eremuak eskuz

Zehaztu bateratutako atributu bat eskuz.

1. Gainean **Batu** orrialdea, hautatu **Konbinatu**.

1. Aukeratu **Eremuak** aukera.

1. Zehaztu konbinazio nagusiaren gidalerroak **Konbinatu eremuak honen arabera** goitibeherako menuan.

1. Aukeratu gehituko duzun eremua. Hautatu **Gehitu eremuak** eremu gehiago konbinatzeko.

1. Eman **Izena** bat eta **Irteerako eremuaren izena**.

1. Aldaketak aplikatzeko, hautatu **Eginda**.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko. 

## <a name="combine-a-group-of-fields"></a>Konbinatu eremu talde bat

Tratatu eremu talde bat unitate bakar gisa. Adibidez, gure erregistroek Helbidea1, Helbidea2, Hiria, Estatua eta Zip eremuak badituzu. Seguruenik, ez dugu nahi beste erregistro baten Helbide2 batean batu, gure datuak osatuagoak izango direlakoan

1. Gainean **Batu** orrialdea, hautatu **Konbinatu**.

1. Aukeratu **Eremu multzoa** aukera.

1. Zehaztu bateratze irabazlearen politika **Sailkatu taldeak arabera** goitibeherako.

1. Hautatu **Gehitu** eta aukeratu eremuetan eremu gehiago edo talde gehiago gehitu nahi dituzun.

1. Eman a **Izena** eta bat **Irteera izena** eremu konbinatu bakoitzeko.

1. Eman a **Izena** eremuen talderako. 

1. Aldaketak aplikatzeko, hautatu **Eginda**.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.

## <a name="change-the-order-of-fields"></a>Aldatu eremuen ordena

Entitate batzuek besteek baino xehetasun gehiago dituzte. Entitate batek eremu bati buruzko azken datuak biltzen baditu, baliteke bat egitean lehentasuna eman diezaiokezu beste entitateei.

1. Hautatu konbinatutako eremua.
  
1. Aukeratu **Erakutsi gehiago** eta aukeratu **Editatu**.

1. Urtean **Konbinatu eremuak** panela, hautatu **Mugitu gora edo behera** ordena ezartzeko edo arrastatu eta askatu nahi duzun posizioan.

1. Berretsi aldaketa.

1. Aukeratu **Gorde** eta **Korrika egin** aldaketak prozesatzeko.

## <a name="configure-customer-id-generation"></a>Konfiguratu bezeroaren IDaren sorrera 

Konbinazio-eremuak konfiguratu ondoren, definitu dezakezu nola sortu CustomerId balioak, bezeroaren profilaren identifikatzaile esklusiboak. Datuak bateratzeko prozesuko konbinazio-urratsak sortzen du bezero-profilaren identifikatzaile esklusiboa. *Bezeroaren* entitateko CustomerId identifikatzailea sortzen da datuen bateratze-prozesutik. 

Bezeroaren entitateko CustomerId lehenengo balioaren eta hutsa ez den gako nagusi irabazlearen arteko hash-ean oinarritzen da. Gako horiek bat-etortze eta konbinazio urratsetan erabilitako entitateetatik datoz eta bat-etortzearen sailkapenak eragina dute horiengan. Sortutako CustomerID-a aldatu daiteke gako-balio nagusia aldatzen denean bat-etortzearen ordenako lehen mailako entitatean. Beraz, baliteke lehen mailako balio nagusiak ez izatea beti bezero bera.

Bezeroaren ID egonkor bat sortzeak portaera hori ekiditeko aukera ematen dizu.

**Konfiguratu bezeroaren ID esklusiboa**

1. Joan hona: **Bateratu** > **Konbinatu**.

1. Hautatu **Gakoak** fitxa. 

1. Jarri **CustomerId** errenkadaren gainean eta hautatu **Konfiguratu** aukera.
   :::image type="content" source="media/customize-stable-id.png" alt-text="IDaren sorrera pertsonalizatzeko kontrola.":::

1. Hautatu gehienez bost eremu, bezeroaren ID esklusiboaz osatuta egongo direnak eta egonkorragoak izango direnak. Konfigurazioarekin bat ez datozen erregistroek sistemak konfiguratutako IDa erabiltzen dute haren ordez.  

1. Aldaketak aplikatzeko, hautatu **eginda** eta exekutatu konbinazio-prozesua.

## <a name="group-profiles-into-households-or-clusters"></a>Taldeko profilak etxeetan edo klusterretan

Bezeroen profila sortzeko konfigurazio prozesuaren barruan, erlazionatutako profilak kluster batean biltzeko arauak defini ditzakezu. Gaur egun bi kluster mota daude eskuragarri - etxekoak eta pertsonalizatutakoak. Sistemak automatikoki aurrez zehaztutako arauak dituen etxea aukeratzen du *Bezeroa* entitateak eremu semantikoak ditu *Person.LastName* eta *Location.Address*. Klusterra ere sor dezakezu zure arau eta baldintzekin, antzekoa [partida arauak](match-entities.md#define-rules-for-match-pairs).

**Definitu etxea edo klusterra**

1. Joan hona: **Bateratu** > **Konbinatu**.

1. Gainean **Batu** fitxa, hautatu **Aurreratua** > **Sortu klusterra**.

   :::image type="content" source="media/create-cluster.png" alt-text="Kontrolatu kluster berria sortzeko.":::

1. Aukeratu **Etxekoa** edo bat **Pertsonalizatua** klusterra. Eremu semantikoak bada *Person.LastName* eta *Location.Address* existitzen dira *Bezeroa* entitatea, etxea automatikoki hautatzen da.

1. Eman klusterraren izena eta hautatu **Eginda**.

1. Aukeratu **Klusterrak** fitxa sortu duzun klusterra aurkitzeko.

1. Zehaztu arauak eta baldintzak zure klusterra definitzeko.

1. Aukeratu **Korrika egin** bateratze prozesua exekutatzeko eta klusterra sortzeko.

Bateratze prozesua exekutatu ondoren, klusterren identifikatzaileak eremu berri gisa gehitzen dira *Bezeroa* entitatea.

## <a name="run-your-merge"></a>Exekutatu zure bateratzea

Eskuz batu atributuak edo sistemak batzen dituzun ala ez, beti bat egin dezakezu. Hautatu **Exekutatu** **Konbinatu** orrian prozesua hasteko.

> [!div class="mx-imgBorder"]
> ![Datuen batzea Gorde eta Exekutatu.](media/configure-data-merge-save-run.png "Datuen batzea Gorde eta Exekutatu")

Aukeratu **Exekutatu soilik Batu** bezero entitate bateratuan islatutako irteera soilik ikusi nahi baduzu. Beherantz egindako prozesuak bezala freskatuko dira [freskatze-programan definitzen da](system.md#schedule-tab).

Aukeratu **Exekutatu, konbinatu eta erraztu prozesuak** sistema zure aldaketekin freskatzeko. Prozesu guztiak, aberastea, segmentuak eta neurriak barne automatikoki berriro abiaraziko dira. Erraztu prozesu guztiak amaitu ondoren, bezeroen profilek egindako aldaketak islatzen dituzte.

Aldaketa gehiago egiteko eta urratsa berriro exekutatzeko, abian den bateratze bat bertan behera utzi dezakezu. Aukeratu **Freskagarria ...** eta hautatu **Lana bertan behera utzi** agertzen den alboko panelean.

[!INCLUDE [progress-details-include](../includes/progress-details-pane.md)]

:::image type="content" source="media/process-detail-path.png" alt-text="Lortu xehetasunak bide-izenari buruz zereginaren egoeraren estekatik prozesuaren xehetasunak lortzeko.":::

## <a name="next-step"></a>Hurrengo urratsa

Konfiguratu [jarduerak](activities.md), [aberastea](enrichment-hub.md), edo [Harremanak](relationships.md) zure bezeroei buruzko ikuspegi gehiago lortzeko.

Aurretik jarduerak, aberastasuna edo segmentuak konfiguratu badituzu, automatikoki prozesatuko dira bezeroen azken datuak erabiltzeko.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
