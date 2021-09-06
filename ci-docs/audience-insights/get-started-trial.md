---
title: Sortu eta konfiguratu Customer Insights-en probako bertsioa
description: Dynamics 365 Customer Insights probarako harpidetza lortzeko eta konfiguratzeko urratsak.
ms.date: 07/22/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: MichelleDevaney
ms.author: midevane
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: f038dedd369ac9e623146b66528efa87c47a8c23769037d8709fa9b804a0b723
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7035400"
---
# <a name="set-up-a-trial-environment"></a>Konfiguratu probako ingurunea 

Dynamics 365 Customer Insights-en proba bertsioak funtsezko gaitasuna berrikusteko eta hainbat ezaugarriei buruz gehiago jakiteko aukera ematen dizu. Probako harpidetza iraungi ondoren ezabatzen da. Probako inguruneak probako inguruneko administratzaile bihurtzen diren erabiltzaileek sortzen dituzte. Erabiltzaile gehiago gonbidatu ditzakete probara eta hainbat funtzio konfiguratu ditzakete.

## <a name="create-a-trial-environment"></a>Sortu probako ingurunea

Epaiketa batean izena eman dezakezu [proba saioa hasteko orria](https://dynamics.microsoft.com/get-started/free-trial/?appname=customerinsights). 

1. Aukeratu **Eman izena doako probarako** aukera eta hautatu **Eman izena orain**.

1. Eman zure laneko edo ikastetxeko helbide elektronikoa, esaiguzu zure buruari buruzko informazio gehiago eta hautatu **Hasi**.

   :::image type="content" source="media/trial-signup-dialog.png" alt-text="Probako instantzian izena emateko elkarrizketa-koadroa":::

1. Berrikusi baldintzak betetzera eta, hautatu **Ados** berresteko.

1. Eman **Izena** zure ingurune berrirako. 

1. Ingurune **Mota** ezarri **Proba** gisa.

1. **Aukeratu industriaren demoa** eremuan, industriaren datu multzo jakin bat aukeratu dezakezu. Ere egin dezakezu [aldatu industriaren demora](#use-industry-specific-demo-data-sets-in-audience-insights) geroago eta lehenetsitako datu multzoarekin hasi.

1. Aukeratu **Eskualdea** zure ingurunerako.

1. Aukeran, Dynamics 365 erakunde baten administratzailea bazara: hautatu **Ezarpen aurreratuak** eta eman zure erakundearen URLa iragarpen ezaugarriak erabiltzeko, adibidez, bezeroaren galera-tasa. 

1. Hautatu **Sortu**. 

Minutu gutxi batzuk baino ez dira behar ingurunea konfiguratzeko. Amaitu ondoren, goiko urratsean aukeratutako demo ingurunera edo industriako demora bideratuko zaituzte. Aplikazioa arakatu dezakezu irakurtzeko soilik diren demo datuekin. Inguruneari zure datuak gehitzeko, ikusi [Sortu eszenatokien araberako demo datuak zure ingurunean](#create-scenario-specific-demo-data-in-your-own-environment).

:::image type="content" source="media/trial-environment.png" alt-text="Sortu berri den probako ingurunearen pantaila-argazkia.":::

## <a name="use-industry-specific-demo-data-sets-in-audience-insights"></a>Erabili sektoreko berariazko demo datu multzoak ikusleen estatistiketan

Benetako datu iturriak konektatzea Customer Insights-en indarra erabiltzeko urrats kritikoetako bat da. Ezaugarriak zure datuekin oztopatu gabe probatzeko, industriaren berariazko demo datuak erabil ditzakezu. Demo datu multzo batzuk daude eskuragarri industria hauetarako: 

-   Automobilgintza
-   Bankua
-   Kontsumo-ondasunak
-   Gobernua
-   Osasun-zerbitzuak
-   Ostatuak
-   Aseguruak
-   Fabrikazioa
-   Zerbitzu profesionalak
-   Txikizkako salmenta

### <a name="see-industry-specific-demo-data-in-trials"></a>Ikusi industriaren berariazko demo datuak entseguetan

Customer Insights-en irakurtzeko soilik den bertsiorako, industria edo eszenatoki zehatzetara egokituta, hasi Demo ingurunean. 
 
1.  Ikusleen estatistiketan, aukeratu **Demo** ingurunea ingurumen hautatzailean.

2.  **Etxean**, aukeratu aukera bat Aukeratu industria demo goitibeherako menuan.

:::image type="content" source="media/trial-select-industry-demo.png" alt-text="Aukeratu industria probako ingurunerako.":::

### <a name="create-scenario-specific-demo-data-in-your-own-environment"></a>Sortu eszenatokien araberako demo datuak zure ingurunean

Administratzaile gisa, hautatu ingurunearen hautatzailea aplikazioaren goiburuan ingurune berri bat sortzeko. Ingurune berrian, zure datu iturriak konfigura ditzakezu eta aplikazioa zure beharren arabera konfigura dezakezu. 

1.  Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2.  Zure datu iturriak inportatzeko, joan [datuak sartzeari buruzko gida](data-sources.md).     
   Datuen iradokizuna probatzea ahalbidetzen duten lagin-datuekin lan egitea nahiago baduzu, industriaren demo datuak zure ingurunean har ditzakezu. Aukeratu **Inportatu Datahub-etik** aukera eta jarraitu beheko urratsak.

3.  Aukeratu zure eszenatokira egokitzen den industria txartela. 

4.  Berrikusi eta aukeran eguneratu datu-iturburuen iradokitako izena. 

5.  Aukeratu **Hurrengoa** laginaren datuak irensteko. 

Orain sartutako datuak erabil ditzakezu Customer Insights zure eszenatokira egokitzeko. Iragarritako demo datuen ingurune zehatz bat ikusteko, aukeratu **<Industry> Demo** aukera ingurunea hautatzeko.

## <a name="limitations-in-trials"></a>Mugak probetan

- Probak aktibatuta daude 30 egun lehenespenez. Hala ere, proban saioa hasten duzunean 23. egunetik aurrera luza ditzakezu.
- Ezin duzu Azure Data Lake biltegiratze kontua erabili probako irteerako datuak gordetzeko. Hala ere, datuak Data Lake biltegiratze kontu batetik har ditzakezu.
- Gehienez 3 GB datu gorde ditzakezu Dataverse Customer Insights proban hasten zarenean automatikoki hornitzen den ingurunean.

## <a name="copy-data-from-a-trial-to-a-paid-subscription"></a>Kopiatu probako datuak ordaindutako harpidetzara

Orokorrean, zure datuekin berriro hastea gomendatzen dugu Customer Insights-en ordaindutako bertsiora eguneratzean. 

Aukeran, zure datuak proba ingurune batetik kopia ditzakezu Customer Insights erosten baduzu. Customer Insights probako administratzailea eta zure Microsoft 365 maizterraren administratzaile globala edo zure erakundeko Dynamics 365 administratzailea izan behar duzu ezarpenak probako ingurunetik ordaindutako ingurunera migratzeko. 

Customer Insights-en ordaindutako instantziarekin lehen aldiz saioa hasi ondoren, ingurune berri bat sortzeko eskatuko zaizu. Prozesu honetan, konfigurazioa lehendik dagoen ingurune batetik kopiatzea eta ezarpen gehienak migratzea aukera dezakezu. Goian aipatutako baimenak badituzu, proba-ingurunea zerrenda honetan agertuko da. Informazio gehiagorako, ikus [Kopiatu ingurunearen konfigurazioa](manage-environments.md#copy-the-environment-configuration).

## <a name="next-steps"></a>Hurrengo urratsak

Berrikusi hurrengo artikuluak Customer Insights konfiguratzen hasteko. 

- [Gehitu erabiltzaile gehiago eta eman baimenak](permissions.md).
- [Sartu zure datu-iturburuak](data-sources.md) eta exekutatu [datuak bateratzeko prozesuaren](data-unification.md) bidez lortzeko [bezeroen profil bateratuak](customer-profiles.md).
- [Aberastu bezeroen profil bateratuak](enrichment-hub.md) edo [exekutatu eredu iragarleak](predictions-overview.md).
- Sortu [segmentuak](segments.md) bezeroak taldekatzeko eta [neurrien](measures.md) berrikuspen KPIak.
- Konfiguratu [konexioak](connections.md) eta [esportazioak](export-destinations.md) zure datuen azpimultzoak beste aplikazio batzuetan prozesatzeko.