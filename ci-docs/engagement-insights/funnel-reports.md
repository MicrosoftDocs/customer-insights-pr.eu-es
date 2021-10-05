---
title: Inbutuaren txostenak
description: Nola erabili inbutu-txostenak ikusleak erabakiak nola hartzen dituen ulertzeko.
ms.reviewer: mhart
ms.author: kamacdon
author: kamacdon
ms.date: 09/21/2021
ms.service: customer-insights
ms.subservice: engagement-insights
ms.topic: how-to
ms.manager: shellyha
ms.openlocfilehash: efb10f2664630a5851d9582ff09c378c01777b96
ms.sourcegitcommit: f1e3cc51ea4cf68210eaf0210ad6e14b15ac4fe8
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558798"
---
# <a name="create-and-manage-funnel-reports"></a>Sortu eta kudeatu inbutu-txostenak

[!INCLUDE [cc-beta-prerelease-disclaimer](includes/cc-beta-prerelease-disclaimer.md)]

Inbutu txosten batek bezero-bidaia batean gertatzen diren pausoei buruzko informazioa biltzen du zure webgunearen edo mugikorretarako aplikazioaren bidez. Ikusleak prozesu baten bidez nola aurrera egiten duen ulertzen eta uzteko puntuak identifikatzen laguntzen dizu. Adibidez, inbutuaren txostena erabil dezakezu bezeroek erosketa egin aurretik egiten dituzten bideak identifikatzeko. Inbutu txosten batek erabakiak informatzeko eta optimizatzeko eta prozesuaren hobekuntzarako eremuak identifikatzeko datuak eskaintzen ditu.

## <a name="create-a-funnel-report"></a>Sortu inbutuaren txostena

Inbutuaren txostena sortzeko, zehaztu zein urrats gehitu nahi dituzun eta urrats bakoitzeko jarduera. Jarduera bat da [gertaera](glossary.md) erabiltzailearen portaera adierazten duena. Inbutuko txostenak zehaztutako urrats bakoitza bete duten erabiltzaile kopurua erakusten du. 

1. Joan **Inbutuak** eta hautatu **+ Inbutu berria** inbutuaren txostena hasteko.

1. Urtean **Inbutu editorea**, azpian **Urratsak** hautatu **+ Gehitu urratsa.** 

1. Idatzi izena hemen **Urratsaren izenburua**.

   :::image type="content" source="media/new-funnel-report.png" alt-text="Inbutu berriaren txostena.":::

1. Hautatu **Jarduera** bat. Jarduera batek erabiltzaile batek orri bat ikustean (**Ikusi** jarduera) edo edukiarekin elkarreragiten du (**Ekintza** jarduera).

1. Erabilera **Urrats irizpideak** jardueraren dimentsioa zehazteko. [Dimentsioak](dimensions.md) datuak deskribatu, iragazi edo taldeka ditzaketen atributuak dira.

1. Aukeran, baldintza anitzeko inbutu pausoak konfigura ditzakezu. Aukeratu **Gehitu baldintza** urrats batean dimentsio gehiago zehazteko. Irizpide osagarriek jarduera mota bera erabili behar dute. Baldintza anitz AND edo OR operadore batekin lotuta dauden ala ez aukeratu dezakezu.

   :::image type="content" source="media/funnel-add-condition.png" alt-text="Urratsen konfigurazioa baldintza anitzeko urratsekin erakusten duen inbutu editorea.":::

1. Aukeratu **Gehitu urratsa** txostenean nahi dituzun urrats guztiak bete arte.

1. Aukeratu **Gorde**, izendatu txostena eta **Gorde** berriro. 

### <a name="example-fourth-coffee-company-funnel-report"></a>Adibidez: Laugarren Kafe konpainiaren inbutuaren txostena

Ondorengo eszenatokiak inbutu txostena erabiltzeko modu bat erakusten du. Fourth Coffee konpainiako analista batek azken promozio batek harpidetzaren tasetan duen eragina ulertu nahi du. Analistak inbutuaren txostena sortzen du bezeroen jarduera identifikatzeko. Bezeroak konpainiaren hasierako orrialdera iristen direnean hasten da harpidetza sustatzeko kodea erabili arte. Analistak inbutuaren txostena sortzen du urrats hauekin:

1. urratsa: hasierako orrialdean sartzen diren bezeroak   
2. urratsa: erosketa egiten duten bezeroak   
3. urratsa: promozio kodea harpidetzan deskontua lortzeko erabiltzen duten bezeroak   
4. Urratsa: Harpidetza erregistratzea   

:::image type="content" source="media/funnel-report-example.png" alt-text="inbutuaren txostenaren adibidea.":::
  
Inbutu honi esker, harpidetza programan izena emateko behin-behineko erosketa egin ondoren promozio kodea erabili duten erabiltzaile kopurua ikus dezakezu.

### <a name="configure-advanced-settings"></a>Konfiguratu ezarpen aurreratuak 

Enbutu txostenek inbutua osatzeko behar den denboraren muga zehazteko aukera ematen dute. Adibidez, inbutua osatzeko denbora lau egunetan ezar dezakezu. Ezarpen honek erabiltzaile batek orrialdea bisitatzen duenetik lau egunetara izandako harpidetza erregistratze arrakastatsuak soilik kontatuko ditu.

1. Joan **Inbutuak** irekitzeko **Inbutuen liburutegia**.

1. Aukeratu izen bat txostena irekitzeko. 

1. **Inbutu editorea** panelean, hautatu **Ezarpen aurreratuak**. 

1. Ezarri Mugatu inbutuaren osatze-ordua **Aktibatuta** gisa.

   :::image type="content" source="media/funnel-limit-time.png" alt-text="Inbutu editoreak ezarpen aurreratuak eta inbutua osatzeko denbora mugatzeko aukerak erakusten ditu.":::

1. Aukeratu inbutuak denbora bete behar duenean **Ezarri muga** goitibeherako zerrenda.

1. Aldaketak aplikatzeko, hautatu **Gorde**.


## <a name="cross-channel-funnel-reports"></a>Kanalen arteko inbutuen txostenak 

Parte-hartzearen xehetasunek portaerako bezeroen datuak zure mugikorreko aplikazioan biltzeko ere balio dezake. Mugikorretarako aplikazioa konpromisoen estatistikekin instrumentatu ondoren [Android SDK](get-started-android.md) edo [iOS SDK](get-started-ios.md), kanalen arteko inbutu txostenak sor ditzakezu. 

### <a name="create-a-cross-channel-funnel-report"></a>Sortu kanalen arteko inbutu-txostenak 

1. Jarraitu urratsak [sortu inbutuaren txostena](#create-a-funnel-report).    

1. Zure bezeroek zure marka zure webgunean zein mugikorreko aplikazioetan edo webgune anitzetan nola elkarreragiten duten jarraitzeko, erabili laneko espazioaren aldatzailea beste lan-eremu batzuetako datuekin inbutu pausoak sortzeko. Urtean **Inbutu editorea**, azpian **Urratsak** hautatu zein lan-espaziotatik atera behar diren zure inbutu urratserako datuak.

## <a name="manage-funnel-reports"></a>Kudeatu inbutuaren txostenak

Inbutu txostenak berrikus ditzakezu datuak aztertzeko, errendimendua jarraitzeko eta estatistikak biltzeko.

> [!NOTE]
> - Elkarreragin xehetasunen inbutuaren txostenek inbutuko erabiltzaile guztiak anonimoak diren edo erabiltzaile guztiak autentifikatuta dauden agertokiak onartzen dituzte. 
> - Inbutu txostenetako datu historikoak eskuragarri daude azken 30 egunetan.

### <a name="view-funnel-reports"></a>Ikusi inbutuaren txostenak

1. Joan **Inbutuak** irekitzeko **Inbutuen liburutegia**.
1. Aukeratu izen bat txostena irekitzeko.    

### <a name="see-the-data-collected-for-a-report"></a>Ikusi jasotako datuak txosten baterako   

Fase bati buruzko informazioa ikusteko

- Seinalatu txostenean urrats bat.

:::image type="content" source="media/funnel-step-data.png" alt-text="inbutuaren datuak.":::

### <a name="change-the-date-range-for-the-funnel-report"></a>Aldatu inbutuaren txostenaren data tartea

1. Joan **Inbutuak** irekitzeko **Inbutuen liburutegia**.

1. Aukeratu izen bat txostena irekitzeko.

1. Ireki **denbora tartea** eta hautatu denbora tarte berri bat zerrendatik edo **Data tarte finkoa** data tartea zehazteko.

## <a name="edit-or-delete-funnel-reports"></a>Editatu edo ezabatu inbutu-txostenak

Inbutuko txosten baten izena aldatu, ezabatu edo txosteneko urratsak alda ditzakezu.

### <a name="rename-or-delete-a-funnel-report"></a>Aldatu izena edo ezabatu inbutuaren txostena

1. Joan **Inbutuak** irekitzeko **Inbutuen liburutegia**. 

1. Aukeratu **Gehiago** Aldatu eta aukeratu nahi duzun txostenaren ondoan **Editatu izena** edo **Ezabatu**.

### <a name="edit-a-funnel-step"></a>Editatu inbutuaren urratsa  

1. Joan **Inbutuak** irekitzeko **Inbutuen liburutegia**. 

1. Aukeratu izen bat txostena irekitzeko.

1. Hautatu editatu nahi duzun urratsa.

1. Hautatu **Editatu**.

1. Urtean **Inbutu editorea**, eguneratu aldatu nahi duzun informazioa.  

1. Sakatu **Gorde**.

### <a name="reorder-a-funnel-step"></a>Berriz agindu inbutuaren urratsa

1. Joan **Inbutuak** irekitzeko **Inbutuen liburutegia**. 

1. Aukeratu izen bat txostena irekitzeko.

1. Hautatu berriz agindu nahi duzun urratsa.

1. Aukeratu **Mugitu**, eta gero **Gora**, **Behera**, **Gora**, edo **Beheraino**, urratsa mugitzeko.

### <a name="delete-a-funnel-step"></a>Ezabatu inbutuaren urratsa

1. Joan **Inbutuak** irekitzeko **Inbutuen liburutegia**. 

1. Aukeratu izen bat txostena irekitzeko.

1. Hautatu urratsa kendu nahi duzuna eta hautatu **Ezabatu**.

## <a name="funnel-insights"></a>Inbutuaren xehetasunak 

Parte-hartzearen xehetasunek inbutuaren xehetasunak eskaintzen dituzte bezeroentzat. Erabili inbutuaren xehetasunak inbutuaren txosteneko urratsei buruzko bezeroaren portaera hobeto ulertzeko. Inbutuaren txosten bat sortu eta gordetzerakoan, txostenerako inbutuaren xehetasunak automatikoki sortzen dira. 

:::image type="content" source="media/funnel-insights.png" alt-text="Inbutuaren xehetasunak.":::

> [!NOTE]
> Inbutuaren estatistikak neurri pertsonalizaturik **ez duten** inbutuaren urratsetarako bakarrik sor daitezke. Inbutuaren urrats guztietarako inbutuari buruzko informazioa sortzeko, erabili parte hartzearen inguruko xehetasunen erabiltzeko prest dauden dimentsioak inbutuaren urratsak sortzeko. 

Inbutuaren xehetasunak honako kategoria hauen bidez ikus ditzakezu, bai maila nagusi eta urrats mailan: 

 - Bihurketa-tasa
 -    Erosketa amaitzearen eta erosketaren arteko bihurketa-tasa % 22koa da.
 - Trantsizio-denbora 
 -    Saskiaren eta erosketa amaitzearen arteko batez besteko denbora 23 minutukoa da. 
 - Osatze-ordua 
 -    Bezeroek inbutua osatzeko behar duten batez besteko denbora 47 minutukoa da. 

Erabili xehetasun horiek bezeroaren portaera sakonago arakatzeko eta inbutuaren txosteneko entrega-puntuak eta bihurketak hobeto ulertzeko. 

Urrats desberdinetako estatistikak alderatzeko, hautatu **Ikusi urratsen banaketa** edo **Konparatu beste urrats batzuekin** ikuspegi txarteletatik. Hauek barra-grafikoa bistaratuko dute inbutuko urrats bakoitzeko metrikak alderatuz. 

Inbutuaren xehetasunak 24 orduro kalkulatzen dira edo inbutuaren txostena **Gordetzen** duzunero. 

> [!NOTE]
> Inbutuaren xehetasunak ikusteko, txostena gorde behar duzu aldaketak egiten dituzunero. 

