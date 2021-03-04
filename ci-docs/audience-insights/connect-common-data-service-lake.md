---
title: Konektatu Common Data Service-n kudeatutako biltegiko entitateetara
description: Inportatu datuak Common Data Service kudeatutako datu-biltegia.
ms.date: 09/29/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.reviewer: adkuppa
ms.openlocfilehash: 18b6cd3fdaf5b738877a73b520b91dbc6ded40de
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267775"
---
# <a name="connect-to-data-in-a-common-data-service-managed-data-lake"></a>Konektatu datuekin Common Data Service kudeatutako data lake-ra

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Artikulu honek egungo Dynamics 365 bezeroak beren entitate analitikoekin azkar nola konektatu daitezkeen buruzko informazioa eskaintzen du Common Data Service kudeatutako aintzira. Administratzailea izan behar duzu Common Data Service erakundeak aurrera egiteko eta kudeatutako aintziran dauden entitateen zerrenda ikusteko.

## <a name="important-considerations"></a>Gogoeta garrantzitsuak

Lineako zerbitzuetan gordetako datuak, esaterako Azure Data Lake Storage datuak prozesatu edo biltegiratutako beste toki batean gorde daitezke Dynamics 365 Customer Insights.Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz onartu egiten duzu Dynamics 365 Customer Insights-rekin transferitu eta biltegiratu daitezkeen datuak. [Ezagutu gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)

## <a name="connect-to-a-common-data-service-managed-lake"></a>Konektatu a Common Data Service lake kudeatu

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Hautatu **Gehitu datu-iturburua**.

3. Aukeratu **Konektatu Common Data Service** eta hautatu **hurrengoa**.

4. Idatzi **Izena** datu-iturbururako eta hautatu **Hurrengoa**. Jarri izena jarraibideei: 
   - Hasi letra batekin.
   - Erabili letrak eta zenbakiak soilik. Ezin da idatzi karaktere berezirik edo zuriunerik.
   - Erabili 3 eta 64 karaktere artean.

5. Eman **Zerbitzariaren helbidea** zuretzako Common Data Service antolatzea eta hautatu **saioa hasi**.

   > [!div class="mx-imgBorder"]
   > ![Sartzeko elkarrizketa-koadroa Common Data Service zerbitzariaren helbidea](media/enter-CDS-org-details.png)

6. Aukeratu eskuragarri dauden zerrendatik sartu nahi dituzun entitateak.    

   > [!NOTE]
   > Entitate batzuk dagoeneko hautatuak badira, beste Dynamics 365 aplikazio batzuek erabil ditzakete (Dynamics 365 Sales Insights edo Customer Service Insights adibidez). Ezin da aldatu aukeraketa. Entitate hauek eskuragarri egongo dira datu-iturburu sortutakoan.

   > [!div class="mx-imgBorder"]
   > ![Elkarrizketa-koadroa, eremuko entitateen zerrenda erakusten duena Common Data Service org](media/select-analytical-entities.png)

7. Gorde zure aukera, hautatutako entitateak sinkronizatzen hasteko Common Data Service lake kudeatu. Konexio berria gehitu duzu **Datu iturriak** orria. Freskatzeko ilaran jarriko da eta entitateak 0 gisa zenbatuko dira entitate guztiak sinkronizatu arte.

Ingurune bateko datu-iturburu batek bakarrik erabil dezake aldi berean Common Data Service-k kudeatutako biltegia.

## <a name="edit-a-common-data-service-managed-lake-data-source"></a>Editatu a Common Data Service lakua kudeatu datu-iturburu

datu-iturburu sortu ondoren entitateen hautapena soilik editatzen duzu. Adibidez, entitate osagarriak gehitu badira Common Data Service eta horiek ere inportatu nahi dituzu.    
Common Data Service desberdinera konektatzeko, [sortu datu-iturri berria](#connect-to-a-common-data-service-managed-lake).

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Eguneratu nahi duzun datu-iturburu ondoan, hautatu elipsia.

3. Hautatu **Editatu** aukera zerrendan.

4. Entitate osagarriak eskuragarri dauden entitateen zerrendatik hautatu eta hautatu **Gorde**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]