---
title: Aberastu bezeroen profilak SFTP pertsonalizatutako inportazioarekin (aurrebista)
description: SFTP pertsonalizatutako inportazio aberasteari buruzko informazio orokorra.
ms.date: 08/08/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: 831d1d3d3045379bbc5bcdcd4b05b8a147221f31
ms.sourcegitcommit: b1d06fe26934f12f0c5ed13e8ef1d37e52e67cc7
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/08/2022
ms.locfileid: "9237751"
---
# <a name="enrich-customer-profiles-with-sftp-custom-import-preview"></a>Aberastu bezeroen profilak SFTP pertsonalizatutako inportazioarekin (aurrebista)

Fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) inportazio pertsonalizatuari esker, datuak bateratzeko prozesua igaro behar ez duten datu-aberasteak inporta ditzakezu. Zure datuak ekartzeko modu malgua, segurua eta erraza da. SFTP inportazio pertsonalizatua erabil daiteke [SFTP esportazioarekin batera](export-sftp.md). Horrek aberastu behar den bezeroen profileko datuak esportatzen uzten dizu. Ondoren, datuak prozesatu eta aberastu daitezke, eta SFTP pertsonalizatutako inportazioa erabil daiteke datu aberastuak itzultzeko Dynamics 365 Customer Insights.

## <a name="prerequisites"></a>Aurrebaldintzak

- SFTP ostalarian inportatu beharreko fitxategiaren izena eta kokapena (bidea) ezagutzen da.

- A *eredua.json* Inportatu beharreko datuetarako Common Data Model eskema zehazten duen fitxategia eskuragarri dago. Fitxategi honek inportatzeko fitxategiaren direktorio berean egon behar du.

- SFTP bat [konexioa](connections.md) da [konfiguratuta](#configure-the-connection-for-sftp-custom-import).

## <a name="file-schema-example"></a>Fitxategi-eskema adibidea

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
                    "friendlyName": "Client ID",
                    "dataType": "string"
                },
                {
                    "name": "PreferredCity",
                    "friendlyName": "Preferred city for vacation",
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

## <a name="configure-the-connection-for-sftp-custom-import"></a>Konfiguratu konexioa SFTP pertsonalizatutako inportaziorako

Bat izan behar duzu [administratzailea](permissions.md#admin) Customer Insights-en eta datuak inportatu nahi dituzun SFTP kokapenaren erabiltzailearen kredentzialak, URLa eta ataka-zenbakia izan.

1. Hautatu **Gehitu konexioa** aberaste bat konfiguratzean edo joan **Admin** > **Konexioak** eta hautatu **Konfiguratu** Inportazio pertsonalizatua fitxan.

   :::image type="content" source="media/enrichment-SFTP-connection.png" alt-text="Inportazio pertsonalizatua konexioaren konfigurazio orria.":::

1. Sartu konexiorako izen bat.

1. Idatzi balio duen erabiltzaile izena, pasahitza eta ostalariaren URLa inportatu beharreko datuak dauden SFTP zerbitzariarentzat.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Egiaztatu** konfigurazioa balioztatzeko eta gero hautatu **Gorde**.

## <a name="configure-the-import"></a>Konfiguratu inportatzea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **SFTP pertsonalizatutako inportazioa** teila.

   :::image type="content" source="media/SFTP_Custom_Import_tile.png" alt-text="SFTP inportazio pertsonalizatuaren lauza.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Hautatu konexioa. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Hautatu **Bezeroaren datu multzoa** eta aukeratu aberastu nahi duzun profila edo segmentua. The *Bezeroa* entitateak zure bezero-profil guztiak aberasten ditu, segmentu batek segmentu horretan dauden bezero-profilak soilik aberasten ditu.

1. Hautatu **Hurrengoa**.

1. Sartu **Bidea** eta **Fitxategi izena** inportatu nahi duzun datu-fitxategiarena.

1. Hautatu **Hurrengoa**.

1. Eman a **Izena** aberasteko eta **Irteerako entitatearen izena**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Korrika egin** aberaste-prozesua hasteko edo hurbiltzeko **Aberasgarriak** orrialdea.

## <a name="view-enrichment-results"></a>Ikusi aberaste-emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)]

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
