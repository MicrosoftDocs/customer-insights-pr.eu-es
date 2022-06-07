---
title: Sortu neurri berriak neurrien eraikitzailearekin
description: Eraiki neurriak hasieratik zure negozioari buruzko neurketa gakoak aztertzeko.
ms.date: 03/25/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: v-wendysmith
ms.author: wameng
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-measure-builder
- customerInsights
ms.openlocfilehash: d003d054145343cc2feeefeeee413810df43185a
ms.sourcegitcommit: b515120bebd2638f2639004422cee3cff42fbdf7
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/24/2022
ms.locfileid: "8800311"
---
# <a name="use-measure-builder-to-create-measures-from-scratch"></a>Erabili neurrien eraikitzailea neurriak hutsetik sortzeko

Artikulu honek berri bat nola sortu azaltzen du [neurria](measures.md) hutsetik. Neurri-sortzaileak kalkuluak definitzeko aukera ematen dizu operadore matematikoak, agregazio-funtzioak eta iragazkiak erabiliz. Neurri bat eraiki dezakezu bateratuarekin erlazionatutako entitateen atributuekin *Bezeroa* entitate.

B-to-C eta B-to-B inguruneetan neurriak sortzeak berdin funtzionatzen du. Hala ere, B-to-B ingurunea bazara [hierarkiak dituzten kontuak erabiltzen ditu](relationships.md#set-up-account-hierarchies), neurria erlazionatutako azpikontuetan bateratzea aukera dezakezu.

Neurri bat azkar sor dezakezu normalean erabilitako eta aurrez zehaztutako neurri multzo batetik aukeratuz. Informazio gehiagorako, ikus [Erabili txantiloi bat neurri bat eraikitzeko](measure-templates.md).

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

Bezero indibidualen mailan (bezeroaren atributua, bezeroaren neurria) edo negozioaren/erakundearen mailan (negozioaren neurria) neurriak sor ditzakezu. Bezeroaren atributua eta bezeroaren neurria bezero bakoitzeko errendimendua jarraitzeko aukera ematen duten bi mota dira. Adibidez, bezero bakoitzaren gastu osoa. Negozioen neurriek negozio bakoitzeko errendimendua jarraitzeko aukera ematen dute. Adibidez, konpainiaren diru-sarrera osoa.

- Bezeroaren atributua: irteera atributu berri gisa sortzen du, eta zutabe berri gisa gordetzen da sistemak izeneko entitatean.*Bezero_neurria*. Bezero-atributu bat freskatzerakoan, gainerako bezero-atributu guztiak *Bezero_neurria* entitatearen freskatzea aldi berean. Horrez gain, bezeroaren atributuak bezeroaren profil-txartelean erakusten dira. Behin exekutatu edo gordeta, bezeroaren atributua ezin duzu aldatu bezeroaren neurrira.

- Bezeroaren neurria: irteera bere entitate gisa sortzen du eta ezin duzu bezeroaren atributu batera aldatu exekutatu edo gorde ondoren. Bezeroaren neurriak ez dira agertzen bezeroaren profileko txartelean.

- Negozio-neurria: irteera sortzen du bere entitate gisa eta zure Customer Insights inguruneko hasierako orrian erakusten du.

1. Joan **Neurriak**.

1. Aukeratu **Berria** eta aukeratu **Eraiki zeurea**.

   :::image type="content" source="media/measure-b2c.png" alt-text="B-to-C neurri baterako konfigurazio-pantaila hutsa." lightbox="media/measure-b2c.png":::

1. Negozio-mailako errendimendua jarraitzeko, txandakatu **Neurri mota** to **Enpresa maila**. **Bezero maila** lehenespenez hautatuta dago. **Bezero maila** automatikoki gehitzen du *BezeroarenId* Dimentsioari egotzi bitartean **Enpresa maila** automatikoki kentzen du.

1. Konfigurazio eremuan, aukeratu agregazio-funtzioa hemendik **Hautatu funtzioa** goitibeherako menua. Agregazio funtzioek honako hauek dituzte:
   - **Sum**
   - **Batez bestekoa**
   - **Kontaketa**
   - **Kontaketa bakarra**
   - **Gehienekoa**
   - **Min**
   - **Lehenengoa**: datuen erregistroaren lehen balioa hartzen du
   - **Azkena**: datuen erregistroan gehitu den azken balioa hartzen du
   - **ArgMax** : helburu-funtzio baten balio maximoa ematen duen datu-erregistroa aurkitzen du
   - **ArgMin** : helburu-funtzio baten balio minimoa ematen duen datu-erregistroa aurkitzen du

1. Aukeratu **Gehitu atributua** neurri hau sortzeko behar dituzun datuak hautatzeko.

   1. Hautatu **Atributuak** fitxa.
   1. Datu-entitatea: aukeratu neurtu nahi duzun atributua biltzen duen entitatea.
   1. Datuen atributua: aukeratu neurria kalkulatzeko agregazio funtzioan erabili nahi duzun atributua. Aldi berean atributu bat besterik ezin duzu hautatu.
   1. Dagoen neurri batetik datuen atributu bat ere hauta dezakezu **Neurriak** fitxa. Edo entitatearen edo neurketaren izena bila dezakezu.
   1. Aukeratu **Gehitu** hautatutako atributua neurrira gehitzeko.

1. Neurri konplexuagoak eraikitzeko, atributu gehiago gehi ditzakezu edo kalkulu-operadoreak erabil ditzakezu neurri funtzioan.

1. Iragazkiak gehitzeko, hautatu **Iragazi** konfigurazio-eremuan. Iragazkiak aplikatzean iragazkiekin bat datozen erregistroak soilik erabiliko dira neurria kalkulatzeko.
  
   1. Urtean **Gehitu atributua** ataleko **Iragazkiak** panelean, hautatu iragazkiak sortzeko erabili nahi duzun atributua.
   1. Ezarri iragazkien eragileak hautatutako atributu bakoitzaren iragazkia definitzeko.
   1. Aukeratu **Aplikatu** hautatutako atributua neurrira gehitzeko.

1. Hautatu **Dimentsioa** neurrien irteerako entitateari zutabe gisa gehitzen diren eremu gehiago aukeratzeko.

   1. Aukeratu **Editatu dimentsioak** neurriaren balioak taldekatu nahi dituzun datu atributuak gehitzeko. Adibidez, hiria edo generoa.
   > [!TIP]
   > Hautatu baduzu **Bezero maila** gisa **Neurri mota** du *BezeroarenId* atributua dagoeneko gehitu da. Atributua kentzen baduzu, **Neurri mota** aukera aldatzen du **Enpresa maila**.
   1. Aukeratu **Eginda** hautatutako atributua neurrira gehitzeko.

1. Zure datuetan zenbaki oso batekin ordezkatu behar dituzun balioak badaude, hautatu **Arauak**. Konfiguratu araua eta ziurtatu ordezko gisa zenbaki osoak bakarrik aukeratzen dituzula. Adibidez, ordeztu *nulua* hurrengoarekin *0*.

1. Esleitutako datu-entitatearen eta *Bezero* entitatearen artean bide anitz badaude, identifikatutako bat aukeratu behar duzu [entitate erlazio-bideak](relationships.md). Neurriaren emaitzak hautatutako bidearen arabera alda daitezke.

   1. Aukeratu **Harreman bide** eta aukeratu zure neurria identifikatzeko erabili beharreko entitate bidea. Bide bakarra bada *Bezeroa* entitatea, kontrol hau ez da erakutsiko.
   1. Aukeratu **Eginda** zure hautaketa aplikatzeko.

1. Neurriaren kalkulu gehiago gehitzeko, hautatu **Kalkulu berria**. Entitate bide bereko entitateak soilik erabil ditzakezu kalkulu berrietarako. Kalkulu gehiago irteerako entitateko zutabe berri gisa agertuko dira.

1. Hautatu elipsi bertikala (&vellip;) kalkuluari buruz **Bikoiztu**, **izena**, edo **Kendu** neurri batetik kalkulua.

1. **Aurrebista** eremuan, neurketaren irteerako entitatearen datu-eskema ikusiko duzu, iragazkiak eta neurriak barne. Aurrebistak dinamikoki erreakzionatzen du konfigurazioko aldaketen aurrean.

1. Hautatu **Editatu xehetasunak** Izenbururik gabeko neurriaren ondoan. Eman izena neurriari. Aukeran, gehitu [etiketak](work-with-tags-columns.md#manage-tags) neurrira.

   :::image type="content" source="media/measures_edit_details.png" alt-text="Editatu xehetasunak elkarrizketa-koadroa.":::

1. Aukeratu **Exekutatu** konfiguratutako neurriaren emaitzak kalkulatzeko. Aukeratu **Gorde eta itxi** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu.

1. Joan **Neurriak** atalera sortu berri den neurria zerrendan ikusteko.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

Banakako kontuen mailan (bezeroaren neurria) edo kontu guztien mailan (negozioaren neurria) neurriak sor ditzakezu.

- Bezeroaren neurria: irteera sortzen du bere entitate gisa. Bezeroaren neurriak ez dira agertzen bezeroaren profileko txartelean.

- Negozio-neurria: irteera sortzen du bere entitate gisa eta zure Customer Insights inguruneko hasierako orrian erakusten du.

1. Joan **Neurriak**.

1. Hautatu **Berria**.

   :::image type="content" source="media/measure-b2b.png" alt-text="B-to-B neurri baten konfigurazio-pantaila hutsa.":::

1. Konfigurazio eremuan, aukeratu agregazio-funtzioa hemendik **Hautatu funtzioa** goitibeherako menua. Agregazio funtzioek honako hauek dituzte:
   - **Sum**
   - **Batez bestekoa**
   - **Kontaketa**
   - **Kontaketa bakarra**
   - **Gehienekoa**
   - **Min**
   - **Lehenengoa**: datuen erregistroaren lehen balioa hartzen du
   - **Azkena**: datuen erregistroan gehitu den azken balioa hartzen du

1. Aukeratu **Gehitu atributua** neurri hau sortzeko behar dituzun datuak hautatzeko.

   1. Hautatu **Atributuak** fitxa.
   1. Datu-entitatea: aukeratu neurtu nahi duzun atributua biltzen duen entitatea.
   1. Datuen atributua: aukeratu neurria kalkulatzeko agregazio funtzioan erabili nahi duzun atributua. Aldi berean atributu bat besterik ezin duzu hautatu.
   1. Dagoen neurri batetik datuen atributu bat ere hauta dezakezu **Neurriak** fitxa. Edo entitatearen edo neurketaren izena bila dezakezu.
   1. Aukeratu **Gehitu** hautatutako atributua neurrira gehitzeko.

1. Neurri konplexuagoak eraikitzeko, atributu gehiago gehi ditzakezu edo kalkulu-operadoreak erabil ditzakezu neurri funtzioan.

1. Iragazkiak gehitzeko, hautatu **Iragazi** konfigurazio-eremuan. Iragazkiak aplikatzean iragazkiekin bat datozen erregistroak soilik erabiliko dira neurria kalkulatzeko.
  
   1. Urtean **Gehitu atributua** ataleko **Iragazkiak** panelean, hautatu iragazkiak sortzeko erabili nahi duzun atributua.
   1. Ezarri iragazkien eragileak hautatutako atributu bakoitzaren iragazkia definitzeko.
   1. Aukeratu **Aplikatu** hautatutako atributua neurrira gehitzeko.

1. Hautatu **Dimentsioa** neurrien irteerako entitateari zutabe gisa gehitzen diren eremu gehiago aukeratzeko.

   1. Aukeratu **Editatu dimentsioak** neurriaren balioak taldekatu nahi dituzun datu atributuak gehitzeko. Adibidez, hiria edo generoa.
      > [!TIP]
      > Hautatu baduzu **Bezero maila** gisa **Neurri mota** du *BezeroarenId* atributua dagoeneko gehitu da. Atributua kentzen baduzu, **Neurri mota** hona aldatzen da **Enpresa maila**.
   1. Aukeratu **Eginda** hautatutako atributua neurrira gehitzeko.

1. Zure datuetan zenbaki oso batekin ordezkatu behar dituzun balioak badaude, hautatu **Arauak**. Konfiguratu araua eta ziurtatu ordezko gisa zenbaki osoak bakarrik aukeratzen dituzula. Adibidez, ordeztu *nulua* hurrengoarekin *0*.

1. Erabil dezakezu **Bildu azpikontuak** txandakatu nahi baduzu [hierarkiak dituzten kontuak erabili](relationships.md#set-up-account-hierarchies).
   - Ezarrita badago **Desaktibatuta**, neurria kontu bakoitzerako kalkulatzen da. Kontu orok emaitzaz jabetzen da.
   - Ezarrita badago **Aktibatuta**, hautatu **Editatu** irensten diren hierarkien arabera kontu hierarkia aukeratzeko. Neurriak emaitza bakarra emango du, azpikontuekin batera dagoelako.

1. Esleitutako datu-entitatearen eta *Bezero* entitatearen artean bide anitz badaude, identifikatutako bat aukeratu behar duzu [entitate erlazio-bideak](relationships.md). Neurriaren emaitzak hautatutako bidearen arabera alda daitezke.

   1. Aukeratu **Harreman bide** eta aukeratu zure neurria identifikatzeko erabili beharreko entitate bidea. Bide bakarra bada *Bezeroa* entitatea, kontrol hau ez da erakutsiko.
   1. Aukeratu **Eginda** zure hautaketa aplikatzeko.

1. Hautatu elipsi bertikala (&vellip;) kalkuluari buruz **Bikoiztu**, **izena**, edo **Kendu** neurri batetik kalkulua.

1. **Aurrebista** eremuan, neurketaren irteerako entitatearen datu-eskema ikusiko duzu, iragazkiak eta neurriak barne. Aurrebistak dinamikoki erreakzionatzen du konfigurazioko aldaketen aurrean.

1. Hautatu **Editatu xehetasunak** Izenbururik gabeko neurriaren ondoan. Eman izena neurriari. Aukeran, gehitu [etiketak](work-with-tags-columns.md#manage-tags) neurrira.

   :::image type="content" source="media/measures_edit_details.png" alt-text="Editatu xehetasunak elkarrizketa-koadroa.":::

1. Aukeratu **Exekutatu** konfiguratutako neurriaren emaitzak kalkulatzeko. Aukeratu **Gorde eta itxi** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu.

1. Joan **Neurriak** atalera sortu berri den neurria zerrendan ikusteko.
