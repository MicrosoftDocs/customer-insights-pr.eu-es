---
title: Sortu neurriak txantiloietatik
description: Neurriak definitzea ohiko erabilera-kasuetarako txantiloiak erabiliz.
ms.date: 03/25/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: v-wendysmith
ms.author: wameng
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-measure-template
- customerInsights
ms.openlocfilehash: eeabd889f7b694f8d809894169a3cdc068acc340
ms.sourcegitcommit: 9ef2cf99b847e7bd8f890f83d84b3a4045aaf8cc
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/01/2022
ms.locfileid: "8529386"
---
# <a name="use-a-template-to-build-a-measure"></a>Erabili txantiloia neurri bat eraikitzeko

Erabili ohi diren aurredefinitutako txantiloiak erabil ditzakezu [neurriak](measures.md) horiek sortzeko. Txantiloien deskribapen zehatzak eta esperientzia gidatu batek neurrien sorrera eraginkorra izaten laguntzen dizute. Txantiloiak mapako datuen gainean eraikitzen dira *Jarduera bateratua* entitatea. Beraz, ziurtatu konfiguratu duzula [bezeroen jarduerak](activities.md) txantiloi batetik neurria sortu aurretik.

Neurri pertsonalizatuak sortzeko, ikus [Erabili neurri-sortzailea neurriak hutsetik sortzeko](measure-builder.md).

# <a name="individual-consumers-b-to-c"></a>[Banakako kontsumitzaileak (negoziotik bezerora)](#tab/b2c)

Neurketa txantiloi erabilgarriak: 
- Transakzioen batezbesteko balioa
- Transakzioaren balioa, guztira
- Eguneko batezbesteko diru-sarrerak
- Urteko batezbesteko diru-sarrerak
- Transakzio kopurua
- Irabazitako fideltasun-puntuak
- Erabilitako fideltasun-puntuak
- Fideltasun-puntuen balantzea
- Bezero aktiboaren bizi-iraupena
- Fideltasun-kidetzaren iraupena
- Azken transakziotik igarotako denbora

## <a name="build-a-new-measure-using-a-template"></a>Eraiki neurri berri bat txantiloi bat erabiliz

1. Joan **Neurriak**.

1. Hautatu **Berria** eta hautatu **Aukeratu txantiloia**.

   :::image type="content" source="media/measure-use-template.png" alt-text="Goitibeherako menuaren pantaila-argazkia neurri berri bat sortzean txantiloian nabarmenduta.":::

1. Aurkitu zure beharretara egokitzen den txantiloia eta hautatu **Aukeratu txantiloia**.

1. Berrikusi eskatutako datuak eta hautatu **Hasi** datu guztiak lekuan badituzu.

1. Hautatu **Editatu xehetasunak** Neurri izenaren ondoan. Eman izena neurriari. Aukeran, gehitu [etiketak](work-with-tags-columns.md#manage-tags) neurrira.

   :::image type="content" source="media/measures_edit_details.png" alt-text="Editatu xehetasunak elkarrizketa-koadroa.":::

1. Hautatu **Eginda**.

1. Hurrengoan **Ezarri denbora tartea** atalean, zehaztu erabili beharreko datuen denbora-tartea. Aukeratu neurri berriak datu multzo osoa estaltzea nahi baduzu hautatuz **Denbora guztian**, edo neurria a ardatz izatea nahi baduzu **Denbora-tarte zehatza**.

   :::image type="content" source="media/measure-set-time-period.png" alt-text="Neurria txantiloi batetik konfiguratzerakoan denbora tartea erakusten duen pantaila-argazkia.":::

1. Hurrengo atalean, hautatu **Gehitu datuak** jarduerak aukeratzeko eta dagozkion datuak mapatzeko *Jarduera bateratua* entitatea.

    1. 1. urratsa: 2. azpian **Jarduera mota**, aukeratu erabili nahi duzun entitatearen mota. Hurrengorako **Jarduerak**, hautatu mapatu nahi dituzun entitateak.
    1. 2. urratsa 2: aukeratu atributua *Jarduera bateratua* formulak eskatzen duen osagaiaren entitatea. Adibidez, Transakzioaren batez besteko balioa, Transakzio balioa adierazten duen atributua da. Hurrengorako **Jardueren denbora-marka**, aukeratu aktibitatea jardueraren data eta ordua adierazten duen Jarduera bateratuko entitatearen artean.
   
1. Datuen mapak arrakasta izan ondoren, egoera honela ikus dezakezu **Osatua** eta mapatutako jardueren eta atributuen izena.

1. Orain hauta dezakezu **Exekutatu** neurriaren emaitzak kalkulatzeko. Geroago fintzeko, hautatu **Gorde zirriborroa**.

# <a name="business-accounts-b-to-b"></a>[Negozio-kontuak (negoziotik negoziora)](#tab/b2b)

Funtzio hau bezero partikularrak helburu nagusi dituzten inguruneetan sortutako neurrietarako bakarrik dago erabilgarri.

---
