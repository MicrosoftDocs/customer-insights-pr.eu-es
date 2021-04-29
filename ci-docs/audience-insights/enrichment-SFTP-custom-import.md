---
title: Aberastea SFTP inportazio pertsonalizatuarekin
description: SFTP pertsonalizatutako inportazio aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: a2d450635c19432bdd88db74b61c17febdeb568d
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5896266"
---
# <a name="enrich-customer-profiles-with-custom-data-preview"></a>Aberastu bezeroen profilak datu pertsonalizatuekin (aurrebista)

Fitxategiak transferitzeko protokolo segurua (SFTP) inportazio pertsonalizatuak datuak bateratzeko prozesua gainditu behar ez duten datuak inportatzeko aukera ematen du. Zure datuak ekartzeko modu malgua, segurua eta erraza da. SFTP inportazio pertsonalizatua erabil daiteke [SFTP esportazioarekin batera](export-sftp.md). Horrek aberastu behar den bezeroen profileko datuak esportatzen uzten dizu. Datuak prozesatu, aberastu eta SFTP inportazio pertsonalizatuak erabil daitezke datu aberastuak Dynamics 365 Customer Insights-eko hartzaileei buruzko informazioaren gaitasunera itzultzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

SFTP inportazio pertsonalizatua konfiguratzeko, honako baldintza hauek bete behar dira:

- SFTP ostalarian inportatu beharreko fitxategiaren izena eta kokapena (bidea) dituzu.
- Badago *eredua.json* zehazten duen fitxategia [Datuen eredu arruntaren eskema](/common-data-model/) datuak inportatzeko. Fitxategi honek inportatzeko fitxategiaren direktorio berean egon behar du.
- Administratzaile batek SFTP konexioa konfiguratu du dagoeneko *edo* duzu [administratzailea](permissions.md#administrator) baimenak. Datuak inportatu nahi dituzun SFTP kokapenerako erabiltzaile kredentzialak, URLa eta ataka zenbakia beharko dituzu.


## <a name="configure-the-import"></a>Konfiguratu inportatzea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hurrengoan **SFTP pertsonalizatutako inportazio-lauza**, hautatu **Aberastu nire datuak** eta gero hautatu **Hasi**.

   :::image type="content" source="media/SFTP_Custom_Import_tile.png" alt-text="SFTP inportazio pertsonalizatuaren lauza.":::

1. Hautatu [konexioa](connections.md) goitibeherako zerrendatik. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, hautatuz konexioa sor dezakezu **Gehitu konexioa** eta aukeratzea **SFTP inportazio pertsonalizatua** goitibeheratik.

1. Aukeratu **Konektatu Inportazio pertsonalizatura** hautatutako konexioa berresteko.

1.  Aukeratu **Hurrengoa** eta sartu **Fitxategi izena** eta **Bidea** inportatu nahi duzun datu fitxategiaren.

    :::image type="content" source="media/enrichment-SFTP-path-and-filename.png" alt-text="Pantaila argazkia datuak kokatzerakoan.":::

1. Aukeratu **Hurrengoa** eta eman aberasturako izena eta irteerako entitatearen izena. 

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="configure-the-connection-for-sftp-custom-import"></a>Konfiguratu konexioa SFTP pertsonalizatutako inportaziorako 

Administratzailea izan behar duzu konexioak konfiguratzeko. Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** inportazio pertsonalizatuaren fitxan.

1. Idatzi konexioaren izena **Bistaratzeko izena** kutxa.

1. Idatzi balio duen erabiltzaile izena, pasahitza eta ostalariaren URLa inportatu beharreko datuak STFP zerbitzariarentzat.

1. Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitutakoan, konexioa klik eginez gorde daiteke **Gorde**.

> [!div class="mx-imgBorder"]
   > ![Experian konexioa konfigurazioaren orria](media/enrichment-SFTP-connection.png "Experian konexioa konfigurazioaren orria")


## <a name="defining-field-mappings"></a>Eremu-esleipenak definitzen 

SFTP zerbitzarian inportatu beharreko fitxategia duen direktorioak ere eduki behar du *model.json* fitxategia. Fitxategi honek datuak inportatzeko erabili beharreko eskema definitzen du. Eskemak [Common Data Model](/common-data-model/) erabili behar du eremuen esleipena zehazteko. model.json fitxategi baten adibide soil batek itxura hau du:

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
