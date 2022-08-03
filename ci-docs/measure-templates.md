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
ms.openlocfilehash: 6dc7fce78d10ba91de4b2abf54c6c6ab1c919d3a
ms.sourcegitcommit: 8a28e9458b857adf8e90e25e43b9bc422ebbb2cd
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/18/2022
ms.locfileid: "9170758"
---
# <a name="create-measures-from-templates"></a>Sortu neurriak txantiloietatik

Erabili ohiko erabilitako aurredefinitutako txantiloiak [neurriak](measures.md) horiek sortzeko. Txantiloiak mapako datuen gainean eraikitzen dira *Jarduera bateratua* entitatea. Beraz, ziurtatu konfiguratu duzula [bezeroen jarduerak](activities.md) txantiloi batetik neurria sortu aurretik.

Neurrien txantiloiak inguruneetan soilik onartzen dira **bezero indibidualak**. Neurri pertsonalizatuak sortzeko edo B-to-Brako neurriak sortzeko, ikus [Erabili neurri-sortzailea](measure-builder.md).

Neurketa txantiloi erabilgarriak:
- Transakzioen batezbesteko balioa
- Transakzioaren balioa, guztira
- Eguneko batezbesteko diru-sarrerak
- Hileko batezbesteko diru-sarrerak
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

1. urtean **Ezarri denbora-epea** atalean, zehaztu datuen denbora-tartea. Aukeratu neurri berriak datu multzo osoa estaltzea nahi baduzu hautatuz **Denbora guztian**, edo neurria a ardatz izatea nahi baduzu **Denbora-tarte zehatza**.

   :::image type="content" source="media/measure-set-time-period.png" alt-text="Neurria txantiloi batetik konfiguratzerakoan denbora tartea erakusten duen pantaila-argazkia.":::

1. Hurrengo atalean, hautatu **Gehitu datuak** jarduerak aukeratzeko eta dagozkion datuak mapatzeko *Jarduera bateratua* entitatea.

    1. 1. urratsa: 2. azpian **Jarduera mota**, aukeratu erabili nahi duzun entitatearen mota. Izan ere **Jarduerak**, hautatu mapatu nahi dituzun entitateak eta, gero, hautatu **Hurrengoa**.
    1. 2. urratsa 2: aukeratu atributua *Jarduera bateratua* formulak eskatzen duen osagaiaren entitatea. Adibidez, Transakzioaren batez besteko balioa, Transakzio balioa adierazten duen atributua da. Izan ere **Jardueraren denbora-zigilua**, aukeratu atributua *Jarduera bateratua* jardueraren data eta ordua adierazten duen entitatea.
    1. Sakatu **Gorde**.

    Datuen mapaketa arrakastatsua denean, egoera erakusten da **Osatu** eta mapatutako jardueren eta atributuen izena bistaratzen dute.

1. Hautatu **Korrika egin** neurriaren emaitzak kalkulatzeko. Hautatu **Gorde zirriborroa** uneko konfigurazioa mantendu eta neurria geroago exekutatu nahi baduzu. The **Neurriak** orrialdeak bistaratzen ditu.

## <a name="next-step"></a>Hurrengo urratsa

Erabili lehendik dauden neurriak sortzeko [bezeroen segmentu bat](segments.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
