---
title: Gehitu kodea zure webgunean
description: Nola gehitu kode zati zure webgunean gertaerak jasotzeko.
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 04/30/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: b5467da775a621c436bd9ddedb272506acc1e2b31dcf7c87feb5dd11e2daae2b
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7035079"
---
# <a name="install-the-code-snippet-on-a-website"></a>Instalatu kode zatia webgunean

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Artikulu honetan administratzaile batek kode zati webgune batean nola instalatzen duen azaltzen da. Gertaerak zure laneko eremuan ikusten hasiko zara script-a zure webgunera gehitu eta gutxira. Informazio gehiagorako, ikus [Laneko espazioak eta ingurunea kudeatzea](manage-environments-workspaces.md). Mugikorretarako aplikazioetan gertaerak jasotzeko, ikusi [Garatzaileen baliabideen ikuspegi orokorra](developer-resources.md).


### <a name="prerequisites"></a>Aurrebaldintzak

* Datuak gordetzeko laneko espazioko administratzaile baimenak izan behar dituzu.
* Zure webguneak edo proiektuak linean ostatatu behar dira jardueren datuak bidaltzeko. Tokiko fitxategi batetik bidalitako datuak ez ditu zerbitzariak onartuko.


## <a name="add-code-to-your-website"></a>Gehitu kodea zure webgunean
1.  Joan **Administratzailea** > **Lan eremua** eta, ondoren, hautatu **Instalazio gida**.
1. Aukeratu **Kopiatu kodea** kode zati kopiatzeko. Lehenespenez, zure laneko espazioaren iradokizun gakoa kode zati-en txertatuta dago.
:::image type="content" source="media/copy-code.png" alt-text="kode zati orriaren pantaila-argazkia.":::
3. Gehitu kopiatutako kode zati zure webgunera <head> Etiketa eta beste edozein script edo CSS etiketak.
4.  Argitaratu zure webgune eguneratua eta itxaron minutu batzuk sarrerako web trafikoa atzemateko.
5.  Zure datuak ikusteko, hautatu zure lan-eremua nabigazio-paneleko laneko aldatzailetik. Ondoren, hautatu txostenetako bat **Ezagutu** atala.

## <a name="configuration-options"></a>Konfigurazio-aukerak

Kode zati-en konfigurazio aukera hauek alda ditzakezu:

- **irenstea Giltza**: Gertaerak zure lan-eremura bidaltzeko erabilitako iradokizun gakoa. Iradokizun gakoa alda dezakezu gertaerak beste lan eremu batera bidaltzeko. Iradokizun gako bat bakarra da laneko gune bakoitzean. 
- **autoCapture**: Orrialde-ikuspegiak eta webgunearekiko elkarrekintzak harrapatzen diren zehazten du. Bi aukera ditu:
    - **ikuspegia**: Ezarri *egia* orrialdearen ikuspegiak harrapatzeko. Orrialde ikuspegiak honela jasotzen dira *Ikusi* [gertaerak](glossary.md#event), mota bat [oinarrizko gertaera](glossary.md#base-event).
    - **egin klik**: Ezarri *egia* webgunean bisitarien interakzioak jasotzeko. Elkarreraginak hautematen dira *Ekintza* [gertaerak](glossary.md#event), mota bat [oinarrizko gertaera](glossary.md#base-event).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
