---
title: Gehitu kodea zure webgunean
description: Nola gehitu kode zati zure webgunean Dynamics 365 Customer Insights gertaerak jasotzeko.
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 09/27/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: ad835f762226d62fdb0f544627f2a76ff09a1ffd
ms.sourcegitcommit: f1e3cc51ea4cf68210eaf0210ad6e14b15ac4fe8
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558778"
---
# <a name="install-the-web-sdk-on-a-website"></a>Instalatu web SDK webgune batean

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Artikulu honetan administratzaile batek webguneko softwareak garatzeko tresna-multzoa (SDK) nola instalatzen duen azaltzen da webgune batean. Zure webgunea prestatu eta gutxira zure laneko eremuan gertakariak ikusten hasiko zara. Informazio gehiagorako, ikus [Laneko espazioak eta ingurunea kudeatzea](manage-environments-workspaces.md). Mugikorretarako aplikazioetan gertaerak jasotzeko, ikusi [Garatzaileen baliabideen ikuspegi orokorra](developer-resources.md).


### <a name="prerequisites"></a>Aurrebaldintzak

* Datuak gordetzeko laneko espazioko administratzaile baimenak izan behar dituzu.
* Zure webguneak edo proiektuak linean ostatatu behar dira jardueren datuak bidaltzeko. Tokiko fitxategi batetik bidalitako datuak ez ditu zerbitzariak onartuko.


## <a name="add-web-sdk-to-your-website"></a>Gehitu web SDK webgunean

Joan **Administratzailea** > **Lan eremua** eta, ondoren, hautatu **Instalazio gida**. Web SDK instalatzeko bi modu daude. Lehenengoa deskarga esteka erabiltzea da, eta bigarrena nodo pakete kudeatzailea (NPM) paketea instalatzea.

### <a name="option-1-using-the-download-link"></a>1. aukera: deskarga-esteka erabiltzea

1. Aukeratu **Kopiatu kodea** kode zati kopiatzeko. Lehenespenez, zure laneko espazioaren iradokizun gakoa kode zati-en txertatuta dago.
  :::image type="content" source="media/copy-code.png" alt-text="kode zati orriaren pantaila-argazkia.":::

1. Gehitu kopiatutako kodea zure webgunera, <head> Etiketa eta beste edozein script edo CSS etiketak.
1. Argitaratu zure webgune eguneratua eta itxaron minutu batzuk sarrerako web trafikoa atzemateko.
1. Zure datuak ikusteko, hautatu zure lan-eremua nabigazio-paneleko laneko aldatzailetik. Ondoren, hautatu txostenetako bat **Ezagutu** atala.

### <a name="option-2-using-the-npm-package-recommended-for-javascript-based-web-apps"></a>2. aukera: NPM paketea erabiltzea (JavaScript oinarritutako web aplikazioetarako gomendagarria)

1. Joan [NPM web orrira](https://www.npmjs.com/package/engagementinsights-web) eta jarraitu web SDK NPM paketea instalatzeko eta konfiguratzeko argibideak.
1. Argitaratu zure webgune eguneratua eta itxaron minutu batzuk sarrerako web trafikoa atzemateko.
1. Zure datuak ikusteko, hautatu zure lan-eremua nabigazio-paneleko laneko aldatzailetik. Ondoren, hautatu txostenetako bat **Ezagutu** atala.

## <a name="configuration-options"></a>Konfigurazio-aukerak

Kode zati-en konfigurazio aukera hauek alda ditzakezu:

- **irenstea Giltza**: Gertaerak zure lan-eremura bidaltzeko erabilitako iradokizun gakoa. Iradokizun gakoa alda dezakezu gertaerak beste lan eremu batera bidaltzeko. Iradokizun gako bat bakarra da laneko gune bakoitzean.
- **autoCapture**: Orrialde-ikuspegiak eta webgunearekiko elkarrekintzak harrapatzen diren zehazten du. Bi aukera ditu:
    - **ikuspegia**: Ezarri *egia* orrialdearen ikuspegiak harrapatzeko. Orrialde ikuspegiak honela jasotzen dira *Ikusi* [gertaerak](glossary.md#event), mota bat [oinarrizko gertaera](glossary.md#base-event).
    - **egin klik**: Ezarri *egia* webgunean bisitarien interakzioak jasotzeko. Elkarreraginak hautematen dira *Ekintza* [gertaerak](glossary.md#event), mota bat [oinarrizko gertaera](glossary.md#base-event).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
