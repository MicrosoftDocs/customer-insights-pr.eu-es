---
title: Osatu datu partzialak iragarpenak erabiliz
description: Erabili iragarpenak bezeroen datu osatugabeak betetzeko.
ms.date: 11/01/2021
ms.subservice: audience-insights
ms.topic: how-to
author: zacookmsft
ms.author: zacook
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-predictions
- ci-custom-models
- customerInsights
ms.openlocfilehash: 57ef46416db0a11cde9f9d7650a0b502a01bf0ab
ms.sourcegitcommit: b515120bebd2638f2639004422cee3cff42fbdf7
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/24/2022
ms.locfileid: "8800635"
---
# <a name="complete-your-partial-data-with-predictions-deprecated"></a>Osatu zure datu partzialak iragarpenekin (zaharkituta)

> [!IMPORTANT]
> Ezaugarri hau izango da **zaharkitua** bezala **2021eko azaroaren 5a**. Uneko inplementazioek funtzionatzen jarraituko dute eginbidea kendu arte, baina ezin izango duzu integrazio berririk sortu beheko argibideak erabiliz.

Aurreikuspenek erraz iragarritako balioak sor ditzakezu bezeroaren ulermena hobetzeko. Gainean **Adimena** > **iragarpenak** orrialdea, hauta dezakezu **Nire iragarpenak** Customer Insights zerbitzuko beste atal batzuetan konfiguratu dituzun iragarpenak ikusteko eta horiek pertsonalizatzeko aukera ematen du.

> [!NOTE]
> Ezin duzu funtzio hau erabili zure inguruak Azure Data Lake Gen 2 biltegia erabiltzen badu.
>
> Aurreikuspenen funtzionalitateak bitarteko automatizatuak erabiltzen ditu datuak ebaluatzeko eta datu horietan oinarritutako iragarpenak egiteko, eta, beraz, profilak egiteko metodo gisa erabiltzeko gaitasuna du, termino hori Datuak Babesteko Araudi Orokorrak ("DBAO") definitzen baitu. Bezeroak funtzio hau erabiltzeko datuak prozesatzeko DBAO edo beste lege edo arau batzuen menpe egon daiteke. Zu zara Dynamics 365 Customer Insights-en erabileraren arduradun, iragarpenez aplikagarriak diren lege eta arau guztiak betetzeaz barne, hala nola pribatutasunarekin, datu pertsonalekin, datu biometrikoekin, datuen babesarekin eta komunikazioen konfidentzialtasunarekin lotutako legeak.

## <a name="prerequisites"></a>Aurrebaldintzak

Zure erakundeak iragarpenen funtzioa erabili ahal izateko, ziurtatu baldintza hauek bete aurretik:

1. Zure erakundeak instantzia bat du [Microsoft Dataverse-n konfiguratuta](/ai-builder/build-model#prerequisites) eta Customer Insights-en erakunde berean dago.

2. Zure Customer Insights ingurunea erantsita dago Dataverse instantzia.

Informazio gehiago lortzeko, ikusi [Sortu ingurune berri bat](create-environment.md).

## <a name="create-a-prediction-in-the-customer-entity"></a>Sortu iragarpenak bezeroaren entitatean

1. Joan **Datuak** > **Entitateak**.

2. Hautatu **Bezeroa** entitatea.

3. Sarbidean **Bezeroa: CustomerInsights** entitatea, hautatu aukeran **eremuak** fitxa.

4. Bilatu balioak aurreikusteko nahi duzun atributu izena eta ondoren hautatu **Orokorra** ikonoa hemen **Laburpen** zutabea.
   > [!div class="mx-imgBorder"]
   > ![Ikuspegi orokorra.](media/intelligence-overviewicon.png "Ikuspegi orokorra")

5. Zure atributua lortzeko balio gutxi falta bada, hautatu **Falta diren balioak aurreikustea** zure iragarpenarekin jarraitzeko.
   > [!div class="mx-imgBorder"]
   > ![Egoera orokorra falta diren balioen iragarpen botoia erakusten da.](media/intelligence-overviewpredictmissingvalues.png "Egoera orokorra falta diren balioen iragarpen botoia erakusten da")

6. Eman a **Bistaratu izena** eta **Irteerako entitatearen izena** iragarpenaren emaitzetarako.

7. Aurrez okupatutako aukeren zerrenda batek iragarritako kategoria batera non mapatu ditzakezun erakutsiko du. Kasu honetan, zure kategoriako aukerak 0 edo 1 izango dira, iragarpenaren benetako / gezurra edo bitarra izaerara mapatzen duten heinean. Kategoria zutabean, esleitu "0" gisa sailkatu nahi dituzun eremu-balioak azken iragarpenean "0"-ra, eta "1" gisa sailkatu nahi dituzun elementuak "1" eremura azken iragarpenean.
   > [!div class="mx-imgBorder"]
   > ![Adibidez, mapen eremuaren balioak kategorietan erakusteko.](media/intelligence-categorymapping.png "Adibidez, mapen eremuaren balioak kategorietan erakusteko")

8. Aukeratu **Egina** eta iragarpena prozesatuko da. Tratamenduak denbora gutxi iraungo du, datuen tamainaren eta konplexutasunaren arabera. Emaitzak entitate berri batean egongo dira eskuragarri **Irteerako entitatearen izena** sortu zenuen iragarpenaz.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="create-a-prediction-while-creating-a-segment"></a>Sortu iragarpenak segmentu bat sortzen duzun bitartean

Aukera zehatz baterako falta diren balioa aurreikustea ere posible da segmentu bat sortzerakoan. Zehazki, zure bezero entitate bateratuan edo Customer_Measure entitatean oinarritutako segmentua azkar sortzen duzunean.

Fluxu horren baitan atributu zehatz bat aukeratu behar duzu zure segmentua nola bezeroaren gogobetetzea, erosketa zenbatekoa. Segmentuak sortzean, sistemak metodo bat proposatuko du atributu honentzako falta diren balioak aurreikusteko.

1. Joan **Segmentuak** eta hautatu **Profilak** teila.

2. Aukeratu a **eremua** segmentu bat sortu eta hautatu bat **Operadorea** eta hautatu **Berrikusi**.

3. Eman a **izena** eta **Bistaratu izena** segmentuarentzat.

4. Sakatu **Gorde**.

5. Sortu berri duzun segmentuak datu osatugabeak baditu iturburu eremuan, falta diren balioak aurreikustea aukeratu dezakezu.
   > [!div class="mx-imgBorder"]
   > ![Iragarpen botoia.](media/segments-predictoption.png "Iragarpen botoia")

6. Eman a **Bistaratu izena** eta **Irteerako entitatearen izena** iragarpenaren emaitzetarako.

7. Hautatu **Eginda**. Zure iragarpena laster sortuko da eta entitate berri batean izenarekin **Irteerako entitatearen izena**.

## <a name="view-a-prediction"></a>Ikusi iragarpena

1. Joan **Adimena** > **Iragarpenak** > **Nire iragarpenak**.

2. Hautatu berrikusi nahi duzun iragarpena.

3. Hautatu elipsi bertikala (&vellip;)-n **Ekintzak** zutabea eta aukeratu **Ikusi**.

4. Zure iragarpena ikusita hainbat datu puntu ikusiko dituzu.
   > [!div class="mx-imgBorder"]
   > ![Iragarpenen orria.](media/intelligence-predictionsviewpage.png "Iragarpenen orria")

   - **Aurreikusitako balioak** Erakusten den mapeketa erakusten du Eremuaren balioa kategorian mapak egiteko fasean. Horiek dira kategoria jakin batera mapatu diren zure datu-baseko balioak.
   -**Goi mailako eragileak** kategoria zehatz batera mapak egitean iragarpenen konfiantzan eragina izan dezaketen datu-multzoko faktoreak dira.
   - **Errendimendua** Iragarpenak nola egiten diren adierazten du. Hautatu esteka gehiago ikasteko.
   - **Aurreikusi** Aurreikusitako irteera-datuen laginak erakusten ditu eta aurreikusitako balioa 0 ziurgabetasuna eta 1 ziurtatuta dauzkagula.

## <a name="update-a-prediction"></a>Eguneratu iragarpena

1. Joan **Adimena** > **Iragarpenak** > **Nire iragarpenak**.

2. Hautatu eguneratu nahi duzun iragarpena, eta hautatu ... **eguneratu** ikonoa.

3. Aurreikuspena prozesatzeko programatuta egongo da. Azkenean eguneratu den momentua ikus dezakezu **eguneratua** zutabe honen **iragarpenak** orria.

## <a name="edit-a-prediction"></a>Editatu iragarpena

Iragarpen bat sortu ondoren, eredua pertsonaliza dezakezu AI Builder zure ereduaren eraginkortasuna areagotzeko.  

1. Joan **Adimena** > **Iragarpenak** > **Nire iragarpenak**.

2. Hautatu editatu nahi duzun iragarpena.

3. Hautatu elipsi bertikala (&vellip;)-n **Ekintzak** zutabea eta aukeratu **Ikusi**.

4. Hautatu **Pertsonalizatu AI Builder**.

5. Eguneratu zure eredua AI Builder. [Argibide gehiago AI builder ereduak kudeatzeari buruz](/ai-builder/manage-model#retrain-and-republish-existing-models).

Zure iragarpenaren hurrengo exekutatuak sortu duzun eredu eguneratua erabiliko du.

> [!NOTE]
> Urtean sortutako eredu berriak AI Builder ez da Customer Insights-en bistaratuko eredua goian zerrendatutako esperientzietatik sortu ez bada.

## <a name="remove-a-prediction"></a>Kendu iragarpena

1. Joan **Adimena** > **Iragarpenak** > **Nire iragarpenak**.

2. Hautatu ezabatu nahi duzun iragarpena.

3. Hautatu elipsi bertikala (&vellip;)-n **Ekintzak** zutabea eta aukeratu **Ezabatu**.

4. Berretsi ezabatzea.

## <a name="troubleshooting"></a>Irtenbideak

Eranskina ezin baduzu osatu Dataverse prozesua akats bat dela eta, prozesua eskuz betetzen saia zaitezke. Erantsitako prozesuan gerta daitezkeen bi arazo ezagutzen dira:

- Bezeroaren txartelaren osagarriaren soluzioa ez dago instalatuta.
    1. Jarraitu argibideak [instalatu eta konfiguratu irtenbidea](customer-card-add-in.md).

- Aplikazio baimenak ez dira eman.
    1. Joan [https://admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com)-ra.
    1. Hautatu **Inguruneak**.
    1. Hautatu elipsi bertikala (&vellip;) baimena gehitu eta hautatu nahi duzun ingurunearen ondoan **Ezarpenak**.
    1. Zabaldu **Erabiltzaileak + baimenak** eta hautatu **erabiltzaileak**.
    1. Aukeratu **+ Berria** eta hautatu **Erabiltzailea**.
    1. Aukeratu **Aplikazioaren erabiltzailea** hautatuta ez badago, eta sartu informazio hau:
        - **Erabiltzaile-izena:** cihelp@microsoft.com
        - **Aplikazioaren ID-a:** 38c77d00-5fcb-4cce-9d93-af4738258e3c
        - **Izena:** Bezeroa
        - **Abizena:** xehetasunak
        - **Posta elektroniko nagusia:** cihelp@microsoft.com
    1. Hautatu **Gorde eta itxi**.
    1. Hautatu sortu duzun erabiltzailea.
    1. Aukeratu **Kudeatu Rolak** goiko menu-barran.
    1. Aukeratu **Sistemaren administratzailea** eta hautatu **Ados**.


[!INCLUDE [footer-include](includes/footer-banner.md)]
