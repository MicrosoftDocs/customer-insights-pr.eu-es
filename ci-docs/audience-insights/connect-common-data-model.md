---
title: Konektatu Common Data Model-eko datuak Azure Data Lake kontu batekin
description: Egin lan Common Data Model-ekin Azure Data Lake Storage erabiliz.
ms.date: 01/25/2022
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 8a871d65bd79d3246984e23fb52210c8dc7259b8
ms.sourcegitcommit: 7a99f3490e6582c2bc2b38019ed1898348b0eaba
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 01/25/2022
ms.locfileid: "8027037"
---
# <a name="connect-to-a-common-data-model-folder-using-an-azure-data-lake-account"></a>Konektatu Common Data Model karpetara Azure Data Lake kontua erabiliz

Artikulu honek Azure Data Lake Storage Gen2 kontua erabiliz Common Data Model-eko datuak sartzeko moduari buruzko informazioa eskaintzen du.

## <a name="important-considerations"></a>Gogoeta garrantzitsuak

- Azure Data Lake-eko datuek datu arrunten ereduaren estandarra jarraitu behar dute. Oraingoz ez dira beste formatuak onartzen.

- Datuak sartzeak Azure Data Lake *Gen2* biltegiratze kontuak soilik onartzen ditu. Ezin dituzu Azure Data Lake Gen1 biltegiratze kontuak erabili datuak sartzeko.

- Azure Data Lake biltegiratze-kontuak izan behar du [izen-espazio hierarkikoa gaituta](/azure/storage/blobs/data-lake-storage-namespace).

- Azure zerbitzuaren entitatearekin autentifikatzeko, ziurtatu zure maizterrean konfiguratuta dagoela. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md).

- Konektatu eta datuak sartu nahi dituzun Azure datu-biltegiak Dynamics 365 Customer Insights ingurunearen Azure eskualde berean egon behar du. Ez da onartzen beste Azure eskualde bateko datu-biltegi batetik Common Data Model-eko karpeta batera konektatzea. Inguruneko Azure eskualdea ezagutzeko, joan hona: **Administratzailea** > **Sistema** > **Honi buruz** hartzaileei buruzko xehetasunetan.

- Lineako zerbitzuetan biltegiratutako datuak datuak prozesatzen edo gordetzen diren tokian beste toki batean bil daitezke Dynamics 365 Customer Insights.Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz gero, onartzen duzu datuak batera transferitu eta gorde daitezkeela.Dynamics 365 Customer Insights . [Lortu informazio gehiago Microsoft Trust Center-en](https://www.microsoft.com/trust-center).

## <a name="connect-to-a-common-data-model-folder"></a>Konektatu Common Data Model-eko karpeta batera

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Hautatu **Azure data Lake biltegiratzea**, sartu a **Izena** datu-iturburu-rako, gero hautatu **Hurrengoa**.

   - Galdetzen bazaizu, hautatu zure industriari dagozkion datu-multzoetako bat, eta hautatu **Hurrengoa**. 

1. Baliabideetan oinarritutako aukera eta harpidetzan oinarritutako aukera erabil dezakezu autentifikatzeko. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md). Sartu **Zerbitzariaren helbidea**, hautatu **saioa hasi**, gero hautatu **Hurrengoa**.
   > [!div class="mx-imgBorder"]
   > ![Elkarrizketa-koadroa Azure Data Lake-rako konexio xehetasun berriak sartzeko.](media/enter-new-storage-details.png)
   > [!NOTE]
   > Datu-iturburu batera konektatu eta sortu ahal izateko goiko aipatutako edukiontzian edo biltegiratze kontuan honako rol hauetako bat behar duzu:
   >  - Storage Blob datu-irakurgailua
   >  - Storage Blob datuen jabea
   >  - Storage Blob datuen kolaboratzailea

1. **Aukeratu Common Data Model karpeta** elkarrizketa-koadroa, hautatu datuak inportatzeko model.json edo manifest.json fitxategia eta hautatu **Hurrengoa**.
   > [!NOTE]
   > Inguruneko beste datu-iturburu batekin lotutako model.json edo manifest.json fitxategia ez da zerrendan agertuko.

1. Aukeratutako model.json edo manifest.json fitxategian eskuragarri dauden entitateen zerrenda ikusiko duzu. Berrikusi eta hautatu erabilgarri dauden entitateen zerrendatik, gero hautatu **Gorde**. Datu-iturburu berriko hautatutako entitate guztiak sartuko dira.
   > [!div class="mx-imgBorder"]
   > ![Elkarrizketa-koadroa model.json fitxategi bateko entitateen zerrenda erakusten da.](media/review-entities.png)

8. Adierazi zein datu-entitate gaitu nahi dituzun datuen profila eta hautatu **Gorde**. Datuen profilak sortzean analisiak eta beste gaitasun batzuk gaitzen dira. Entitate osoa hauta dezakezu, entitatetik atributu guztiak hautatzen dituena edo zenbait atributu hauta ditzakezu. Lehenespenez, ez dago entitaterik gaituta datu-profilak egiteko.
   > [!div class="mx-imgBorder"]
   > ![Datu-profilak erakusten dituen elkarrizketa-koadroa.](media/dataprofiling-entities.png)

9. Zure hautaketak gorde ondoren, **Datu iturriak** orria irekitzen da. Datu eredu arruntaren karpetaren konexioa datu-iturburu gisa ikusi beharko zenuke orain.

> [!NOTE]
> model.json edo manifest.json fitxategi bat ingurune bereko datu-iturburu batekin bakarrik lotu daiteke. Hala ere, model.json edo manifest.json fitxategi bera erabil daiteke hainbat ingurunetako datu-iturburuetarako.

## <a name="edit-a-common-data-model-folder-data-source"></a>Editatu datu arrunten ereduaren karpeta datu-iturburu

Common Data Model karpeta duen biltegiratze konturako sarbide gakoa egunera dezakezu. Model.json edo manifest.json fitxategia ere alda dezakezu. Biltegiratze kontutik beste edukiontzi batera konektatu nahi baduzu edo kontuaren izena aldatu nahi baduzu [datu-iturburu konexio berria sortu](#connect-to-a-common-data-model-folder).

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Datu-iturburuak**.

2. Eguneratu nahi duzun datu-iturburu ondoan, hautatu elipsia.

3. Hautatu **Editatu** aukera zerrendan.

4. Aukeran, eguneratu **Sarbide gakoa** eta hautatu **hurrengo**.

   ![Elkarrizketa-koadroa lehendik dagoen datu-iturburu-eko sarbide-gakoa editatzeko eta eguneratzeko.](media/edit-access-key.png)

5. Aukeran, kontuaren gako konexio batetik baliabideetan oinarritutako edo harpidetzan oinarritutako konexio batera egunera dezakezu. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md). Ezin duzu aldatu **Edukiontzia**-ren informazioa konexioa eguneratzean.
   > [!div class="mx-imgBorder"]

   > ![Elkarrizketa-koadroa Azure Data Lake-k lehendik dagoen biltegiratze-kontu batekin konexioaren xehetasunak sartzeko.](media/enter-existing-storage-details.png)

   > [!NOTE]
   > Datu-iturburu batera konektatu eta sortu ahal izateko goiko aipatutako edukiontzian edo biltegiratze kontuan honako rol hauetako bat behar duzu:
   >  - Storage Blob datu-irakurgailua
   >  - Storage Blob datuen jabea
   >  - Storage Blob datuen kolaboratzailea


6. Aukeran, aukeratu model.json edo manifest.json fitxategi desberdin bat edukiontziaren beste entitate multzo batekin.

7. Aukeran, sartzeko entitate osagarriak hauta ditzakezu. Dagoeneko hautatutako edozein entitate ken ditzakezu mendekotasunik ez badago.

   > [!IMPORTANT]
   > Lehendik dauden model.json edo manifest.json fitxategiaren eta entitateen multzoaren menpekotasunak badaude, errore mezu bat ikusiko duzu eta ezin duzu model.json edo manifest.json fitxategi desberdin bat hautatu. Kendu mendekotasun horiek model.json edo manifest.json fitxategia aldatu aurretik edo sortu datu-iturburu berri bat mendekotasunak ez kentzeko erabili nahi dituzun model.json edo manifest.json fitxategiarekin.

8. Aukeran, atributu edo entitate osagarriak hauta ditzakezu datuen profilak gaitzeko edo lehendik hautatutakoak desgaitzeko.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
