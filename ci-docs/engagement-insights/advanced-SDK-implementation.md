---
title: Web SDK aurreratuen egoerak
description: Zure webgunea SDK batekin ekipatzerakoan kontuan hartu beharreko agertoki aurreratuak.
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 09/27/2021
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: a083d8215f295af0884257a016b62b8c7e4ab2c7
ms.sourcegitcommit: e7cdf36a78a2b1dd2850183224d39c8dde46b26f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/16/2022
ms.locfileid: "8227183"
---
# <a name="advanced-web-sdk-instrumentation"></a>Web SDK tresneria aurreratua

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Artikulu honek eszenatoki aurreratuetan zehar gidatuko zaitu noiz kontuan hartu behar den [zure webgunea instrumentatzen](instrument-website.md) batekin Dynamics 365 Customer Insights konpromisoari buruzko gaitasuna SDK.

## <a name="setting-user-details-for-your-event"></a>Zure gertaeraren erabiltzaile xehetasunak ezartzen

SDK-k gertaera guztiekin bidal daitekeen erabiltzailearen informazioa zehazteko aukera ematen du. Erabiltzailearen xehetasunak izeneko propietate batean zehaztu ditzakezu `user` (jabetza honen itxaropenak datuak dira `IUser` objektua), antzekoa `src`, `name`, eta `cfg` kode zati konfigurazioan.

`IUser` objektuak kateen propietate hauek ditu:

- **localId**: Erabiltzailearen ID lokala.
- **autentifikazioa**: Autentifikatutako erabiltzaile IDa.
- **authType**: Autentifikatutako erabiltzaile IDa lortzeko erabiltzen den autentifikazio mota.
- **izena**: Erabiltzailearen izena.
- **posta elektronikoa**: erabiltzailearen helbide elektronikoa.

Hurrengo adibidean erabiltzailearen informazioa bidaltzen duen kode zati erakusten da. Izartxo * sinbolo baten aurreko funtzioak ikusten dituzunean, ordeztu funtzioa zure inplementazio pertsonalizatuarekin:

```
[…]
window, document
{
    src:"https://download.pi.dynamics.com/sdk/web/msei-1.min.js",
    name:"myproject",
    cfg:{
      ingestionKey:<paste your ingestion key>",
      autoCapture:{
        view:true,
        click:true
      }
    },
    user:{
      authId: getLoggedInUserId()*,
      email: getLoggedInUserEmail()*,
      authType: "MSA",
      name: "John Doe"
    }
[…]
```

Erabiltzailearen informazioa ere zehaztu dezakezu `setUser(user: IUser)` APIari deituz. `setUser` APIa deitu ondoren bidali den telemetriak erabiltzailearen informazioa edukiko du.

## <a name="adding-custom-properties-for-each-event"></a>Gertaera bakoitzerako propietate pertsonalizatuak gehitzea

SDK-k gertaera guztiekin bidal daitekeen propietate pertsonalizatuak zehazteko aukera ematen du. Propietate pertsonalizatuak gako-balio bikoteak dituen objektu gisa zehaz ditzakezu (balioa motakoa izan daiteke `string | number | boolean`). `src`, `name`, eta `cfg` propietateen antzekoa den `props` izeneko propietateko objektua gehi dezakezu kode zatiaren konfigurazioan.

Hurrengo adibidean propietate pertsonalizatuak bidaltzen duen kode zati erakusten da.

```
[…]
window, document
{
    src:"https://download.pi.dynamics.com/sdk/web/msei-1.min.js",
    name:"myproject",
    cfg:{
      ingestionKey:<paste your ingestion key>",
      autoCapture:{
        view:true,
        click:true
      }
    },
    props:{
      "key_name_string": "value",
      "key_name_number": 10,
      "key_name_bool": true
    }
[…]
```

Propietate pertsonalizatuak banaka ere zehaztu dezakezu `setProperty(name: string, value: string | number | boolean)` APIari deituz.

## <a name="sending-custom-events"></a>Egin gertaera pertsonalizatuen bidaltzea

SDK erabil dezakezu gertaera pertsonalizatuak bidaltzeko. Ekitaldiaren izenarekin eta gertaerarekin batera bidali beharreko propietateekin zehaztu behar duzu.

Hurrengo adibidean gertaera pertsonalizatuak jarraitzen duen kode zati erakusten da. "NAME" fitxategiaren balioa da `name` tekla kode zati konfigurazioan. SDK kargatzen den leiho-objektuaren aldagaiaren izena ere bada.

```
window["NAME"].trackEvent({
    name: "event_name",
    properties: {
        "duration": 320,
        "name": "getting_started",
        "ad_shown": true
    }
});
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]
