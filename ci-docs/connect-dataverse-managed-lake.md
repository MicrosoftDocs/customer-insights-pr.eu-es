---
title: Konektatu datuekin Microsoft Dataverse kudeatutako data lake-ra
description: Inportatu datuak Microsoft Dataverse kudeatutako datu-biltegia.
ms.date: 07/26/2022
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.reviewer: v-wendysmith
searchScope:
- ci-dataverse
- customerInsights
ms.openlocfilehash: b21150a1c51bdad35250cae7fde7f38a014ec876
ms.sourcegitcommit: 5807b7d8c822925b727b099713a74ce2cb7897ba
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206938"
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

[!INCLUDE [footer-include](includes/footer-banner.md)]
