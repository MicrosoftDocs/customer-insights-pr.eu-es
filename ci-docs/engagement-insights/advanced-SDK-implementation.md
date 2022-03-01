---
title: Web SDK aurreratuen egoerak
description: Zure webgunea SDK batekin ekipatzerakoan kontuan hartu beharreko agertoki aurreratuak.
author: britl
ms.reviewer: mhart
ms.author: britl
ms.date: 11/12/2020
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: conceptual
ms.manager: shellyha
ms.openlocfilehash: 7455d276035bfaf1f8a93d0e3b0b0884353a4010715c05d1d696309f7eb4b233
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7036313"
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
    
Hurrengo adibidean erabiltzailearen informazioa bidaltzen duen kode zati erakusten da. * Bidez adierazten diren funtzioak ikusten dituzunean, ordezkatu balio horiei deitzeko inplementazioarekin:  

```
[…]
window, document 
{
    src:"https://download.pi.dynamics.com/sdk/web/mspi-0.min.js", 
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

Erabiltzailearen informazioa ere zehaztu dezakezu `setUser(user: IUser)` APIa SDKn. Deitu ondoren bidali da telemetria `setUser API` erabiltzailearen informazioa edukiko du.

## <a name="adding-custom-properties-for-each-event"></a>Gertaera bakoitzerako propietate pertsonalizatuak gehitzea

SDK-k gertaera guztiekin bidal daitekeen propietate pertsonalizatuak zehazteko aukera ematen du. Propietate pertsonalizatuak gako-balio bikoteak dituen objektu gisa zehaz ditzakezu (balioa motakoa izan daiteke `string | number | boolean`). Objektua izeneko propietate batean gehi daiteke `props`, antzekoak `src`, `name`, eta `cfg` kode zati konfigurazioan. 

Hurrengo adibidean propietate pertsonalizatuak bidaltzen duen kode zati erakusten da.

```
[…]
window, document 
{
    src:"https://download.pi.dynamics.com/sdk/web/mspi-0.min.js", 
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

Propietate pertsonalizatuak banan-banan zehaztu ditzakezu `setProperty(name: string, value: string | number | boolean)` APIa SDKn.

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