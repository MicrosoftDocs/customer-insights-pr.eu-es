---
title: Aberastea SFTP inportazio pertsonalizatuarekin
description: SFTP pertsonalizatutako inportazio aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: f52d24cbe793bee7948ad2af31059cd3edf40f94
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642003"
---
# <a name="enrich-customer-profiles-with-custom-data-preview"></a>Aberastu bezeroen profilak datu pertsonalizatuekin (aurrebista)

Fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) inportazio pertsonalizatuari esker, datuak bateratzeko prozesua igaro behar ez duten datu-aberasteak inporta ditzakezu. Zure datuak ekartzeko modu malgua, segurua eta erraza da. SFTP inportazio pertsonalizatua erabil daiteke [SFTP esportazioarekin batera](export-sftp.md). Horrek aberastu behar den bezeroen profileko datuak esportatzen uzten dizu. Ondoren, datuak prozesatu eta aberastu daitezke, eta SFTP pertsonalizatutako inportazioa erabil daiteke aberastutako datuak itzultzeko Dynamics 365 Customer Insights.

## <a name="prerequisites"></a>Aurrebaldintzak

SFTP inportazio pertsonalizatua konfiguratzeko, honako baldintza hauek bete behar dira:

- SFTP ostalarian inportatu beharreko fitxategiaren izena eta kokapena (bidea) dituzu.
- Badago *eredua.json* zehazten duen fitxategia [Datuen eredu arruntaren eskema](/common-data-model/) datuak inportatzeko. Fitxategi honek inportatzeko fitxategiaren direktorio berean egon behar du.
- Administratzaile batek SFTP konexioa konfiguratu du dagoeneko *edo* duzu [administratzailea](permissions.md#admin) baimenak. Datuak inportatu nahi dituzun SFTP kokapenerako erabiltzaile kredentzialak, URLa eta ataka zenbakia beharko dituzu.


## <a name="configure-the-import"></a>Konfiguratu inportatzea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hurrengoan **SFTP pertsonalizatutako inportazio-lauza**, hautatu **Aberastu nire datuak** eta gero hautatu **Hasi**.

   :::image type="content" source="media/SFTP_Custom_Import_tile.png" alt-text="SFTP inportazio pertsonalizatuaren lauza.":::

1. Hautatu goitibeherako zerrendako [konexio](connections.md) bat. Jarri harremanetan administratzaile batekin konexiorik ez badago. Administratzailea bazara, konexioa sor dezakezu hautatuta **Gehitu konexioa** eta aukeratzea **SFTP inportazio pertsonalizatua** goitibeherako zerrendatik.

1. Aukeratu **Konektatu Inportazio pertsonalizatura** hautatutako konexioa berresteko.

1.  Aukeratu **Hurrengoa** eta sartu **Bidea** eta **Fitxategi izena** inportatu nahi duzun datu fitxategiaren.

    :::image type="content" source="media/enrichment-SFTP-path-and-filename.png" alt-text="Pantaila argazkia datuak kokatzerakoan.":::

1. Aukeratu **Hurrengoa** eta aukeratu bezeroaren datu multzoa. Hau bezeroen profil guztiak edo segmentu bat izan daiteke.

1. Aukeratu **Hurrengoa** eta eman aberasturako izena eta irteerako entitatearen izena. 

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

## <a name="configure-the-connection-for-sftp-custom-import"></a>Konfiguratu konexioa SFTP pertsonalizatutako inportaziorako 

Administratzailea izan behar duzu konexioak konfiguratzeko. Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** inportazio pertsonalizatuaren fitxan.

1. Idatzi konexioaren izena **Bistaratzeko izena** kutxa.

1. Idatzi balio duen erabiltzaile izena, pasahitza eta ostalariaren URLa inportatu beharreko datuak dauden SFTP zerbitzariarentzat.

1. Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.

1. Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.

1. Egiaztapena amaitutakoan, konexioa hautatuta gorde daiteke **Gorde**.

   > [!div class="mx-imgBorder"]
   > ![Experian konexioaren konfigurazio-orria.](media/enrichment-SFTP-connection.png "Experian konexioaren konfigurazio-orria")


## <a name="defining-field-mappings"></a>Eremu-esleipenak definitzen 

SFTP zerbitzarian inportatu beharreko fitxategia duen direktorioak ere eduki behar du *model.json* fitxategia. Fitxategi honek datuak inportatzeko erabili beharreko eskema definitzen du. Eskemak erabili behar du [Common Data Model](/common-data-model/) eremuen mapaketa zehazteko. model.json fitxategi baten adibide soil batek itxura hau du:

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

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
