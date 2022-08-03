---
title: Sortu neurriak neurri-eraikitzailearekin
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
ms.openlocfilehash: fac00b8a1b4ca6e09dd29abe46dfe240adcc029e
ms.sourcegitcommit: 8a28e9458b857adf8e90e25e43b9bc422ebbb2cd
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/18/2022
ms.locfileid: "9170834"
---
# <a name="create-measures-with-measure-builder"></a>Sortu neurriak neurri-eraikitzailearekin

Measure builder-ek kalkuluak definitzeko aukera ematen dizu operadore matematikoak, agregazio-funtzioak eta iragazkiak erabiliz. Neurriak definitzea bateratuarekin erlazionatutako entitateen atributuak erabiliz *Bezeroa* entitate.

B-to-C eta B-to-B inguruneetan neurriak sortzeak berdin funtzionatzen du. Hala ere, zure B-to-B ingurunea bada [hierarkiak dituzten kontuak erabiltzen ditu](relationships.md#set-up-account-hierarchies), aukeratu neurria erlazionatutako azpikontuetan bateratu nahi duzun ala ez.

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

Sortu neurriak bezero indibidualen mailan (bezeroaren atributua, bezeroaren neurria) edo negozioaren/erakundearen mailan (negozioaren neurria). Bezeroaren atributuek eta bezeroen neurriek bezero bakoitzeko errendimendua jarraitzeko aukera ematen dute. Adibidez, bezero bakoitzak egindako gastu osoa. Negozioek negozio bakoitzeko errendimenduaren jarraipena neurtzen dute. Adibidez, konpainiaren diru-sarrera osoa.

- Bezeroaren atributua: irteera atributu berri gisa sortzen du, eta zutabe berri gisa gordetzen da sistemak izeneko entitatean.*Bezero_neurria*. Bezero-atributu bat freskatzerakoan, gainerako bezero-atributu guztiak *Bezero_neurria* entitatearen freskatzea aldi berean. Horrez gain, bezeroaren atributuak bezeroaren profileko txartelean erakusten dira. Exekutatu edo gorde ondoren, ezin duzu bezero-atributua aldatu bezero-neurri batera.

- Bezeroaren neurria: irteera bere entitate gisa sortzen du eta ezin duzu bezeroaren atributu batera aldatu exekutatu edo gorde ondoren. Bezeroaren neurriak ez dira agertzen bezeroaren profileko txartelean.

- Negozio-neurria: irteera sortzen du bere entitate gisa eta zure Customer Insights inguruneko hasierako orrian erakusten du.

1. Joan **Neurriak**.

1. Hautatu **Berria** > **Sortu zeurea**.

   :::image type="content" source="media/measure-b2c.png" alt-text="B-to-C neurri baterako konfigurazio-pantaila hutsa." lightbox="media/measure-b2c.png":::

1. Hautatu **Editatu xehetasunak** Izenbururik gabeko neurriaren ondoan. Eman izena neurriari. Aukeran, gehitu [etiketak](work-with-tags-columns.md#manage-tags) neurrira.

   :::image type="content" source="media/measures_edit_details.png" alt-text="Editatu xehetasunak elkarrizketa-koadroa.":::

1. Hautatu **Eginda**.

1. Negozio-mailako errendimendua jarraitzeko, txandakatu **Neurri mota** to **Enpresa maila**. **Bezero maila** lehenespenez hautatuta dago. **Bezero maila** automatikoki gehitzen du *Bezeroaren Id* Dimentsioari egotzi bitartean **Enpresa maila** automatikoki kentzen du.

1. Konfigurazio eremuan, aukeratu agregazio-funtzioa **Hautatu funtzioa** goitibeherako menua. Agregazio funtzioek honako hauek dituzte:
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

1. Hautatu **Gehitu atributua** neurri hau sortzeko datuak hautatzeko.

   1. Hautatu **Atributuak** fitxa.
   1. Datu-entitatea: aukeratu neurtu nahi duzun atributua biltzen duen entitatea.
   1. Datuen atributua: aukeratu neurria kalkulatzeko agregazio funtzioan erabili nahi duzun atributua. Aldi berean atributu bat besterik ezin duzu hautatu.
   1. Aukeran, aukeratu lehendik dagoen neurri batetik datu-atributu bat hautatuta **Neurriak** fitxa, edo bilatu entitate edo neurri-izen bat.
   1. Hautatu **Gehitu**.

1. Neurri konplexuagoak eraikitzeko, gehitu atributu gehiago edo erabili operadore matematikoak zure neurketa-funtzioan.

1. Iragazkiak gehitzeko, hautatu **Iragazi** konfigurazio-eremuan. Iragazkiak aplikatzean iragazkiekin bat datozen erregistroak soilik erabiliko dira neurria kalkulatzeko.
  
   1. Urtean **Gehitu atributua** ataleko **Iragazkiak** panelean, hautatu iragazkiak sortzeko erabili nahi duzun atributua.
   1. Ezarri iragazkien eragileak hautatutako atributu bakoitzaren iragazkia definitzeko.
   1. Hautatu **Aplikatu**.

1. Hautatu **Dimentsioa** neurrien irteerako entitateari zutabe gisa gehitzeko eremu gehiago aukeratzeko.

   1. Aukeratu **Editatu dimentsioak** neurriaren balioak taldekatu nahi dituzun datu atributuak gehitzeko. Adibidez, hiria edo generoa.
      > [!TIP]
      > Hautatu baduzu **Bezero maila** gisa **Neurri mota** du *Bezeroaren Id* atributua dagoeneko gehitu da. Atributua kentzen baduzu, **Neurri mota** aukeran aktibatzen du **Enpresa maila**.
   1. Hautatu **Eginda**.

1. Zure datuetan zenbaki oso batekin ordezkatu behar diren balioak badaude, hautatu **Arauak**. Konfiguratu araua eta ziurtatu ordezko gisa zenbaki osoak bakarrik aukeratzen dituzula. Adibidez, ordeztu *nulua* hurrengoarekin *0*.

1. Mapatutako datu-entitatearen eta entitatearen artean bide anitz badaude *Bezeroa* entitatea, aukeratu identifikatutako bat [entitate harreman bideak](relationships.md). Neurriaren emaitzak hautatutako bidearen arabera alda daitezke.

   1. Aukeratu **Harreman bide** eta aukeratu zure neurria identifikatzeko erabili beharreko entitate bidea. Bide bakarra bada *Bezeroa* entitatea, kontrol hau ez da erakutsiko.
   1. Hautatu **Eginda**.

1. Neurriaren kalkulu gehiago gehitzeko, hautatu **Kalkulu berria**. Erabili entitate-bide bereko entitateak soilik kalkulu berrietarako. Kalkulu gehiago irteerako entitateko zutabe berri gisa agertuko dira. Aukeran, hautatu **Editatu izena** kalkulurako izen bat sortzeko.

1. Hautatu elipsi bertikala (&vellip;) kalkuluari buruz **Bikoiztu** edo **Kendu** neurri batetik kalkulua.

1. **Aurrebista** eremuan, neurketaren irteerako entitatearen datu-eskema ikusiko duzu, iragazkiak eta neurriak barne. Aurrebistak dinamikoki erreakzionatzen du konfigurazioko aldaketen aurrean.

1. Aukeratu **Exekutatu** konfiguratutako neurriaren emaitzak kalkulatzeko. Aukeratu **Gorde eta itxi** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu. The **Neurriak** orrialdeak bistaratzen ditu.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

Sortu neurriak banakako kontuen mailan (bezeroaren neurria) edo kontu guztien mailan (enpresa neurria).

- Bezeroaren neurria: irteera sortzen du bere entitate gisa. Bezeroaren neurriak ez dira agertzen bezeroaren profileko txartelean.

- Negozio-neurria: irteera sortzen du bere entitate gisa eta zure Customer Insights inguruneko hasierako orrian erakusten du.

1. Joan **Neurriak**.

1. Hautatu **Berria**.

   :::image type="content" source="media/measure-b2b.png" alt-text="B-to-B neurri baten konfigurazio-pantaila hutsa.":::

1. Hautatu **Editatu xehetasunak** Izenbururik gabeko neurriaren ondoan. Eman izena neurriari. Aukeran, gehitu [etiketak](work-with-tags-columns.md#manage-tags) neurrira. 
   :::image type="content" source="media/measures_edit_details.png" alt-text="Editatu xehetasunak elkarrizketa-koadroa.":::

1. Hautatu **Eginda**.

1. Konfigurazio eremuan, aukeratu agregazio-funtzioa **Hautatu funtzioa** goitibeherako menua. Agregazio funtzioek honako hauek dituzte:
   - **Sum**
   - **Batez bestekoa**
   - **Kontaketa**
   - **Kontaketa bakarra**
   - **Gehienekoa**
   - **Min**
   - **Lehenengoa**: datuen erregistroaren lehen balioa hartzen du
   - **Azkena**: datuen erregistroan gehitu den azken balioa hartzen du

1. Hautatu **Gehitu atributua** neurri hau sortzeko datuak hautatzeko.

   1. Hautatu **Atributuak** fitxa.
   1. Datu-entitatea: aukeratu neurtu nahi duzun atributua biltzen duen entitatea.
   1. Datuen atributua: aukeratu neurria kalkulatzeko agregazio funtzioan erabili nahi duzun atributua. Aldi berean atributu bat besterik ezin duzu hautatu.
   1. Aukeran, aukeratu lehendik dagoen neurri batetik datu-atributu bat hautatuta **Neurriak** fitxa, edo bilatu entitate edo neurri-izen bat.
   1. Aukeratu **Gehitu** hautatutako atributua neurrira gehitzeko.

1. Neurri konplexuagoak eraikitzeko, gehitu atributu gehiago edo erabili operadore matematikoak zure neurketa-funtzioan.

1. Iragazkiak gehitzeko, hautatu **Iragazi** konfigurazio-eremuan. Iragazkiak aplikatzean iragazkiekin bat datozen erregistroak soilik erabiliko dira neurria kalkulatzeko.
  
   1. Urtean **Gehitu atributua** ataleko **Iragazkiak** panelean, hautatu iragazkiak sortzeko erabili nahi duzun atributua.
   1. Ezarri iragazkien eragileak hautatutako atributu bakoitzaren iragazkia definitzeko.
   1. Aukeratu **Aplikatu** hautatutako atributua neurrira gehitzeko.

1. Hautatu **Dimentsioa** neurrien irteerako entitateari zutabe gisa gehitzeko eremu gehiago aukeratzeko.

   1. Aukeratu **Editatu dimentsioak** neurriaren balioak taldekatu nahi dituzun datu atributuak gehitzeko. Adibidez, hiria edo generoa.
      > [!TIP]
      > The *Bezeroaren Id* atributua dagoeneko gehitu da bezero-mailako neurri mota bat dela adieraziz. Atributua kentzen baduzu, neurri mota negozio-mailara aldatuko da.
   1. Aukeratu **Eginda** hautatutako atributua neurrira gehitzeko.

1. Zure datuetan zenbaki oso batekin ordezkatu behar diren balioak badaude, hautatu **Arauak**. Konfiguratu araua eta ziurtatu ordezko gisa zenbaki osoak bakarrik aukeratzen dituzula. Adibidez, ordeztu *nulua* hurrengoarekin *0*.

1. Zuk bada [erabili hierarkiak dituzten kontuak](relationships.md#set-up-account-hierarchies), errepasoa **Bildu azpi-kontuak**.
   - Ezarrita badago **Desaktibatuta**, neurria kontu bakoitzerako kalkulatzen da. Kontu bakoitzak bere emaitza lortzen du.
   - Ezarrita badago **Aktibatuta**, hautatu **Editatu** irensten diren hierarkien arabera kontu hierarkia aukeratzeko. Neurri horrek emaitza bakarra emango du azpikontuekin bateratuta dagoelako.

1. Mapatutako datu-entitatearen eta entitatearen artean bide anitz badaude *Bezeroa* entitatea, aukeratu identifikatutako bat [entitate harreman bideak](relationships.md). Neurriaren emaitzak hautatutako bidearen arabera alda daitezke.

   1. Aukeratu **Harreman bide** eta aukeratu zure neurria identifikatzeko erabili beharreko entitate bidea. Bide bakarra bada *Bezeroa* entitatea, kontrol hau ez da erakutsiko.
   1. Aukeratu **Eginda** zure hautaketa aplikatzeko.

1. Hautatu elipsi bertikala (&vellip;) kalkuluari buruz **Bikoiztu** edo **Kendu** neurri batetik kalkulua.

1. **Aurrebista** eremuan, neurketaren irteerako entitatearen datu-eskema ikusiko duzu, iragazkiak eta neurriak barne. Aurrebistak dinamikoki erreakzionatzen du konfigurazioko aldaketen aurrean.

1. Aukeratu **Exekutatu** konfiguratutako neurriaren emaitzak kalkulatzeko. Aukeratu **Gorde eta itxi** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu. The **Neurriak** orrialdeak bistaratzen ditu.

---

## <a name="next-step"></a>Hurrengo urratsa

Erabili lehendik dauden neurriak sortzeko [bezeroen segmentu bat](segments.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
