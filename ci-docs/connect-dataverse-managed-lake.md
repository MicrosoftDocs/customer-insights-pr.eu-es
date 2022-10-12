---
title: Konektatu datuekin Microsoft Dataverse kudeatutako data lake-ra
description: Inportatu datuak Microsoft Dataverse kudeatutako datu-biltegia.
ms.date: 08/18/2022
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.reviewer: v-wendysmith
searchScope:
- ci-dataverse
- customerInsights
ms.openlocfilehash: 0d9612525344c8ac99b6e3edfe33a426dc0a474b
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9609776"
---
# <a name="connect-to-data-in-a-microsoft-dataverse-managed-data-lake"></a>Konektatu datuekin Microsoft Dataverse kudeatutako data lake-ra

Microsoft Dataverse erabiltzaileak azkar konektatu daitezke entitate analitikoetara Microsoft Dataverse kudeatutako lakua. Ingurune bateko datu-iturburu batek bakarrik erabil dezake aldi berean Dataverse-k kudeatutako biltegia.

> [!NOTE]
> Admin izan behar duzu Dataverse erakundeak aurrera egin eta kudeatutako lakuan eskuragarri dauden entitateen zerrenda ikusteko.

## <a name="prerequisites"></a>Aurrebaldintzak

- Lineako zerbitzuetan gordetako datuak, esaterako Azure Data Lake Storage datuak prozesatu edo biltegiratutako beste toki batean gorde daitezke Dynamics 365 Customer Insights.Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz gero, onartzen duzu datuak batera transferitu eta gorde daitezkeela.Dynamics 365 Customer Insights . [Lortu informazio gehiago Microsoft Trust Center-en](https://www.microsoft.com/trust-center).

- Bakarrik Dataverse duten entitateak [aldaketen jarraipena](/power-platform/admin/enable-change-tracking-control-data-synchronization) gaituta daude ikusgai. Entitate hauek honera esporta daitezke Dataverse -kudeatutako datu-lakua eta Customer Insights-en erabiltzen da. Kutxaz kanpo Dataverse taulek aldaketen jarraipena gaituta dute lehenespenez. Aldaketen jarraipena aktibatu behar duzu taula pertsonalizatuetarako. A ala ez egiaztatzeko Dataverse taula aldaketen jarraipena egiteko gaituta dago, joan hona [Power Apps](https://make.powerapps.com) > **Datuak** > **Taulak**. Aurkitu zure intereseko taula eta hautatu. Joan **Ezarpenak** > **Aukera aurreratuak** eta berrikusi **Aldaketen jarraipena** ezarpena.

## <a name="connect-to-a-dataverse-managed-lake"></a>Konektatu a Dataverse lake kudeatu

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Hautatu **Microsoft Dataverse**.

1. Sartu a **Izena** datu-iturburu eta aukerako bat **Deskribapena**.

1. Eman **Zerbitzariaren helbidea** Dataverse erakundearena, eta hautatu **saioa hasi**.

1. Hautatu eskuragarri dagoen zerrendatik Customer Insights-en entitate gisa sartu nahi dituzun taulak.

   > [!NOTE]
   > Taula batzuk dagoeneko hautatuta badaude, Dynamics 365 aplikazioek (adibidez, Dynamics 365 Sales Insights edo Customer Service Insights) erabil ditzakete. Ezin da aldatu aukeraketa. Taula hauek entitate gisa erabilgarri egongo dira datu-iturburu sortu ondoren.

    :::image type="content" source="media/select-dataverse-entities.png" alt-text="Elkarrizketa koadroa Dataverse inguruneko entitate zerrenda erakusten.":::

1. Gorde hautapena Dataverse-ko hautatutako taulak sinkronizatzen hasteko. Konexio berria gehitu duzu **Datu iturriak** orria. Freskatzeko ilaran egongo da eta entitate kopurua 0 gisa erakutsiko da hautatutako taula guztiak sinkronizatu arte.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

Datuak kargatzeak denbora behar dezake. Freskatu arrakastatsu baten ondoren, irentsitako datuak berrikusi daitezke [**Entitateak**](entities.md) orrialdea.

## <a name="edit-a-dataverse-managed-lake-data-source"></a>Editatu a Dataverse lakua kudeatu datu-iturburu

datu-iturburu sortu ondoren entitateen hautapena soilik editatzen duzu. Adibidez, entitate osagarriak gehitu badira Dataverse eta horiek ere inportatu nahi dituzu.
Beste Dataverse datu biltegi batekin konektatzeko, [sortu datu-iturburu berria](#connect-to-a-dataverse-managed-lake).

1. Joan **Datuak** > **Datu-iturburuak**.

1. Eguneratu nahi duzun datu-iturburu-aren ondoan, hautatu **Editatu**.

1. Hautatu entitate osagarriak eskuragarri dauden entitateen zerrendatik.

1. Egin klik **Gorde** zure aldaketak aplikatzeko eta itzultzeko **Datu-iturriak** orrialdea.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="common-reasons-for-ingestion-errors-or-corrupted-data"></a>Irenste-akatsen edo datu hondatuen ohiko arrazoiak

Iragarritako datuekin egiaztapen hauek exekutatzen dira hondatutako erregistroak agerian uzteko:

- Eremu baten balioa ez dator bat bere zutabeko datu motarekin.
- Eremuek zutabeak espero den eskemarekin bat ez datozen eragiten duten karaktereak dituzte. Adibidez: gaizki formateatutako komatxoak, ihes egin gabeko komatxoak edo karaktere lerro berriak.
- Datetime/date/datetimeoffset zutabeak badaude, haien formatua ereduan zehaztu behar da ISO formatu estandarra jarraitzen ez badu.

### <a name="schema-or-data-type-mismatch"></a>Eskema edo datu-mota ez datoz bat

Datuak eskemarekin bat ez badatoz, erregistroak hondatuta bezala sailkatuko dira. Zuzendu iturburuko datuak edo eskema eta sartu berriro datuak.

### <a name="datetime-fields-in-the-wrong-format"></a>Data-orduaren eremuak formatu okerrean

Entitateko data-orduaren eremuak ez daude ISO edo en-US formatuetan. Customer Insights-en data-orduaren formatu lehenetsia en-US formatua da. Entitate bateko data-ordu-eremu guztiek formatu berean egon behar dute. Customer Insights-ek beste formatu batzuk onartzen ditu, baldin eta oharrak edo ezaugarriak ereduan edo manifest.json iturburuan edo entitate mailan egiten badira. Adibidez:

**Model.json**

   ```json
      "annotations": [
        {
          "name": "ci:CustomTimestampFormat",
          "value": "yyyy-MM-dd'T'HH:mm:ss:SSS"
        },
        {
          "name": "ci:CustomDateFormat",
          "value": "yyyy-MM-dd"
        }
      ]   
   ```

  Manifest.json batean, datetime formatua entitate mailan edo atributu mailan zehaztu daiteke. Entitate mailan, erabili "exhibitsTraits" *.manifest.cdm.json entitatean datu-orduaren formatua definitzeko. Atributu mailan, erabili "appliedTraits" entityname.cdm.json atributuan.

**Manifest.json entitate mailan**

```json
"exhibitsTraits": [
    {
        "traitReference": "is.formatted.dateTime",
        "arguments": [
            {
                "name": "format",
                "value": "yyyy-MM-dd'T'HH:mm:ss"
            }
        ]
    },
    {
        "traitReference": "is.formatted.date",
        "arguments": [
            {
                "name": "format",
                "value": "yyyy-MM-dd"
            }
        ]
    }
]
```

**Entity.json atributu mailan**

```json
   {
      "name": "PurchasedOn",
      "appliedTraits": [
        {
          "traitReference": "is.formatted.date",
          "arguments" : [
            {
              "name": "format",
              "value": "yyyy-MM-dd"
            }
          ]
        },
        {
          "traitReference": "is.formatted.dateTime",
          "arguments" : [
            {
              "name": "format",
              "value": "yyyy-MM-ddTHH:mm:ss"
            }
          ]
        }
      ],
      "attributeContext": "POSPurchases/attributeContext/POSPurchases/PurchasedOn",
      "dataFormat": "DateTime"
    }
```

[!INCLUDE [footer-include](includes/footer-banner.md)]
