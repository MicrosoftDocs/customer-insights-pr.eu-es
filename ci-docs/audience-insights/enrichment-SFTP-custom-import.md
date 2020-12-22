---
title: Aberastea SFTP inportazio pertsonalizatuarekin
description: SFTP pertsonalizatutako inportazio aberasteari buruzko informazio orokorra.
ms.date: 11/18/2020
ms.reviewer: kishorem
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: jdahl
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 59f7f05ca0825ba147e9e93f10fa3508ec3a16dd
ms.sourcegitcommit: ff824bbbd31fd666ab0da682bf48ea31580d242c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "4568399"
---
# <a name="enrich-customer-profiles-with-custom-data-preview"></a>Aberastu bezeroen profilak datu pertsonalizatuekin (aurrebista)

Fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) inportazio pertsonalizatuari esker, datuak bateratzeko prozesua igaro behar ez duten datu-aberasteak inporta ditzakezu. Zure datuak ekartzeko modu malgua, segurua eta erraza da. SFTP inportazio pertsonalizatua erabil daiteke [SFTP esportazioarekin batera](export-sftp.md). Horrek aberastu behar den bezeroen profileko datuak esportatzen uzten dizu. Datuak prozesatu, aberastu eta SFTP inportazio pertsonalizatuak erabil daitezke datu aberastuak Dynamics 365 Customer Insights-eko hartzaileei buruzko informazioaren gaitasunera itzultzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

SFTP inportazio pertsonalizatua konfiguratzeko, honako baldintza hauek bete behar dira:

- Erabiltzaile kredentzialak (erabiltzaile izena eta pasahitza) dituzue datuak inportatuko diren SFTP kokapenerako.
- STFP ostalariaren URLa eta ataka zenbakia (normalean 22) dituzu.
- SFTP ostalarian inportatuko den fitxategiaren izena eta kokapena dituzu.
- Bada inportatu nahi diren datuen eskema zehazten duen *model.json* fitxategia. Fitxategi honek inportatzeko fitxategiaren direktorio berean egon behar du.
- [Administratzaile](permissions.md#administrator) baimena duzu.

## <a name="configuration"></a>Konfigurazioa

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. **SFTP inportazio pertsonalizatuaren lauzan**, hautatu **Aberastu nire datuak**.

   > [!div class="mx-imgBorder"]
   > ![SFTP inportazio pertsonalizatuaren lauza](media/SFTP_Custom_Import_tile.png "SFTP inportazio pertsonalizatuaren lauza")

1. Aukeratu **Hasi** eta eman SFTP zerbitzariaren kredentzialak eta helbidea. Adibidez, sftp://mysftpserver.com:22.

1. Idatzi datuak dituen fitxategiaren izena eta SFTP zerbitzarirako bide-izena, ez badago erro-karpetan.

1. Berretsi sarrera guztiak **Konektatu inportazio pertsonalizatura** hautatuta.

   > [!div class="mx-imgBorder"]
   > ![SFTP inportazio pertsonalizatuaren konfigurazioaren kontrol mugikorra](media/SFTP_Custom_Import_Configuration_flyout.png "SFTP inportazio pertsonalizatuaren konfigurazioaren kontrol mugikorra")

## <a name="defining-field-mappings"></a>Eremu-esleipenak definitzen 

SFTP zerbitzarian inportatu beharreko fitxategia duen direktorioak ere eduki behar du *model.json* fitxategia. Fitxategi honek datuak inportatzeko erabili beharreko eskema definitzen du. Eskemak [Common Data Model](https://docs.microsoft.com/common-data-model/) erabili behar du eremuen esleipena zehazteko. model.json fitxategi baten adibide soil batek itxura hau du:

```
{
    "name": "EnrichmentFromMicrosoft",
    "description": "Model containing data enrichment",
    "entities": [
        {
            "name": "CustomImport",
            "attributes": [
                {
                    "name": "CustomerId",
                    "friendlyName": "Client id",
                    "dataType": "string"
                },
                {
                    "name": "PreferredCity",
                    "friendlyName": "Preferred City for vacation",
                    "dataType": "string"
                },
                {
                    "name": "PreferredTransportation",
                    "friendlyName": "Preferred transportation",
                    "dataType": "string"
                }
            ],
            "annotations": [
                {
                    "name": "c360:PrimaryKey",
                    "value": "CustomerId"
                }
            ]
        }
    ],
    "modifiedTime": "2020-01-02T12:00:00+08:00",
    "annotations": [
        {
            "name": "testAnnotation",
            "value": "testValue"
        }
    ]
}
```

## <a name="enrichment-results"></a>Aberastearen emaitzak

Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik. Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab). Prozesatzeko denbora inportatu beharreko datuen tamainaren eta SFTP zerbitzarirako konexioaren araberakoa izango da.

Aberaste-prozesua amaitu ondoren, inportatutako aberaste pertsonalizatuko datuak berrikus ditzakezu **Nire aberasteak** atalean. Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.

Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.

## <a name="next-steps"></a>Hurrengo urratsak

Eraiki zure bezeroen datu aberastuen gainean. Sortu [segmentuak](segments.md), [neurriak](measures.md), eta [esportatu](export-destinations.md) datuak zure bezeroei esperientzia pertsonalizatuak emateko.


