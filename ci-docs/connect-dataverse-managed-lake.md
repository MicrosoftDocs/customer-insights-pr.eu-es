---
title: Konektatu tauletara Microsoft Dataverse-en
description: Inportatu datuak Microsoft Dataverse kudeatutako datu-biltegia.
ms.date: 03/18/2022
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.reviewer: v-wendysmith
searchScope:
- ci-dataverse
- customerInsights
ms.openlocfilehash: c470956b0453ac2558ed85acdeebba120a0ca55d
ms.sourcegitcommit: 5e26cbb6d2258074471505af2da515818327cf2c
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/14/2022
ms.locfileid: "9011688"
---
# <a name="connect-to-data-in-a-microsoft-dataverse-managed-data-lake"></a>Konektatu datuekin Microsoft Dataverse kudeatutako data lake-ra

Microsoft Dataverse erabiltzaileak azkar konektatu daitezke entitate analitikoetara Microsoft Dataverse kudeatutako lakua.

> [!NOTE]
> Admin izan behar duzu Dataverse erakundeak aurrera egin eta kudeatutako lakuan eskuragarri dauden entitateen zerrenda ikusteko.

## <a name="important-considerations"></a>Gogoeta garrantzitsuak

1. Lineako zerbitzuetan gordetako datuak, esaterako Azure Data Lake Storage datuak prozesatu edo biltegiratutako beste toki batean gorde daitezke Dynamics 365 Customer Insights.Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz gero, onartzen duzu datuak batera transferitu eta gorde daitezkeela.Dynamics 365 Customer Insights . [Lortu informazio gehiago Microsoft Trust Center-en](https://www.microsoft.com/trust-center).
2. Bakarrik Dataverse duten entitateak [aldaketen jarraipena](/power-platform/admin/enable-change-tracking-control-data-synchronization) gaituta daude ikusgai. Entitate hauek honera esporta daitezke Dataverse -kudeatutako datu-lakua eta Customer Insights-en erabiltzen da. Kutxaz kanpo Dataverse taulek aldaketen jarraipena gaituta dute lehenespenez. Aldaketen jarraipena aktibatu behar duzu taula pertsonalizatuetarako. A ala ez egiaztatzeko Dataverse taula aldaketen jarraipena egiteko gaituta dago, joan hona [Power Apps](https://make.powerapps.com) > **Datuak** > **Taulak**. Aurkitu zure intereseko taula eta hautatu. Joan **Ezarpenak** > **Aukera aurreratuak** eta berrikusi **Aldaketen jarraipena** ezarpena.

## <a name="connect-to-a-dataverse-managed-lake"></a>Konektatu a Dataverse lake kudeatu

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Hautatu **Microsoft Dataverse**.

1. Sartu a **Izena** datu-iturburu eta aukerakoa **Deskribapena**.

1. Eman **Zerbitzariaren helbidea** Dataverse erakundearena, eta hautatu **saioa hasi**.

1. Hautatu Customer Insights-en entitate gisa sartu nahi dituzun taulak eskuragarri dagoen zerrendatik.

   > [!NOTE]
   > Taula batzuk dagoeneko hautatuta badaude, Dynamics 365 aplikazioek (adibidez, Dynamics 365 Sales Insights edo Customer Service Insights) erabil ditzakete. Ezin da aldatu aukeraketa. Taula hauek entitate gisa erabilgarri egongo dira datu-iturburu sortu ondoren.

    :::image type="content" source="media/select-dataverse-entities.png" alt-text="Elkarrizketa koadroa Dataverse inguruneko entitate zerrenda erakusten.":::

1. Gorde hautapena Dataverse-ko hautatutako taulak sinkronizatzen hasteko. Konexio berria gehitu duzu **Datu iturriak** orria. Freskatzeko ilaran egongo da eta entitate kopurua 0 gisa erakutsiko da hautatutako taula guztiak sinkronizatu arte.

Ingurune bateko datu-iturburu batek bakarrik erabil dezake aldi berean Dataverse-k kudeatutako biltegia.

## <a name="edit-a-dataverse-managed-lake-data-source"></a>Editatu a Dataverse lakua kudeatu datu-iturburu

datu-iturburu sortu ondoren entitateen hautapena soilik editatzen duzu. Adibidez, entitate osagarriak gehitu badira Dataverse eta horiek ere inportatu nahi dituzu.
Beste Dataverse datu biltegi batekin konektatzeko, [sortu datu-iturburu berria](#connect-to-a-dataverse-managed-lake).

1. Joan **Datuak** > **Datu-iturburuak**.

1. Eguneratu nahi duzun datu-iturburu-aren ondoan, hautatu **Editatu**.

1. Entitate osagarriak eskuragarri dauden entitateen zerrendatik hautatu eta hautatu **Gorde**.
