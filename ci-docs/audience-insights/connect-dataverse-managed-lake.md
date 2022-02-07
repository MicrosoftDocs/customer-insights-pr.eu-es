---
title: Konektatu tauletara Microsoft Dataverse-en
description: Inportatu datuak Microsoft Dataverse kudeatutako datu-biltegia.
ms.date: 12/06/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
manager: shellyha
ms.reviewer: mhart
---

# <a name="connect-to-data-in-a-microsoft-dataverse-managed-data-lake"></a>Konektatu datuekin Microsoft Dataverse kudeatutako data lake-ra



Artikulu honek nolako informazioa ematen du Dataverse erabiltzaileak azkar konektatu daitezke entitate analitikoetara Microsoft Dataverse kudeatutako lakua. 

> [!NOTE]
> Admin izan behar duzu Dataverse erakundeak aurrera egin eta kudeatutako lakuan eskuragarri dauden entitateen zerrenda ikusteko.

## <a name="important-considerations"></a>Gogoeta garrantzitsuak

Lineako zerbitzuetan gordetako datuak, esaterako Azure Data Lake Storage datuak prozesatu edo biltegiratutako beste toki batean gorde daitezke Dynamics 365 Customer Insights.Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz gero, onartzen duzu datuak batera transferitu eta gorde daitezkeela.Dynamics 365 Customer Insights . [Lortu informazio gehiago Microsoft Trust Center-en](https://www.microsoft.com/trust-center).

## <a name="connect-to-a-dataverse-managed-lake"></a>Konektatu a Dataverse lake kudeatu

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Hautatu **Gehitu datu-iturburua**.

3. Hautatu **Microsoft Dataverse** eta hautatu **Hurrengoa**.

4. Idatzi **Izena** datu-iturbururako eta hautatu **Hurrengoa**. 

5. Eman **Zerbitzariaren helbidea** Dataverse erakundearena, eta hautatu **saioa hasi**.

   :::image type="content" source="media/ingest-dataverse-server-address.png" alt-text="Datuak sartzeko urratsaren pantaila. Erabiltzaileak Dataverse inguruneko URLa sar dezake bertan.":::

6. Aukeratu hartzaileen xehetasunen entitate gisa irentsi nahi dituzun taulak eskuragarri dauden zerrendan.    

   > [!NOTE]
   > Taula batzuk dagoeneko hautatuta badaude, Dynamics 365 aplikazioek (adibidez, Dynamics 365 Sales Insights edo Customer Service Insights) erabil ditzakete. Ezin da aldatu aukeraketa. Taula hauek entitate gisa erabilgarri egongo dira datu-iturburu sortu ondoren.

   :::image type="content" source="media/select-dataverse-entities.png" alt-text="Elkarrizketa koadroa Dataverse inguruneko entitate zerrenda erakusten.":::

7. Gorde hautapena Dataverse-ko hautatutako taulak sinkronizatzen hasteko. Konexio berria gehitu duzu **Datu iturriak** orria. Freskatzeko ilaran egongo da eta entitate kopurua 0 gisa erakutsiko da hautatutako taula guztiak sinkronizatu arte.

Ingurune bateko datu-iturburu batek bakarrik erabil dezake aldi berean Dataverse-k kudeatutako biltegia.

## <a name="edit-a-dataverse-managed-lake-data-source"></a>Editatu a Dataverse lakua kudeatu datu-iturburu

datu-iturburu sortu ondoren entitateen hautapena soilik editatzen duzu. Adibidez, entitate osagarriak gehitu badira Dataverse eta horiek ere inportatu nahi dituzu.    
Beste Dataverse datu biltegi batekin konektatzeko, [sortu datu-iturburu berria](#connect-to-a-dataverse-managed-lake).

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Eguneratu nahi duzun datu-iturburu ondoan, hautatu elipsia.

3. Hautatu **Editatu** aukera zerrendan.

4. Entitate osagarriak eskuragarri dauden entitateen zerrendatik hautatu eta hautatu **Gorde**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
