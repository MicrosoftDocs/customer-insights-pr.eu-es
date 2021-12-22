---
title: Entitateak eta datu multzoak
description: Ikusi datuak Entitateen orrian.
ms.date: 12/06/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
ms.openlocfilehash: 00c5ee50fb9f0906622c91699852ffba0acb5c15
ms.sourcegitcommit: 11b343f6622665251ab84ae39ebcd91fa1c928ca
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 12/08/2021
ms.locfileid: "7900412"
---
# <a name="entities-in-audience-insights"></a>Hartzaileen xehetasunetako entitateak

Ondoren [zure datu-iturriak konfiguratuz](data-sources.md), joan **erakundeak** iradokitako datuen kalitatea ebaluatzeko orria. Entitateak datu multzo gisa hartzen dira. Dynamics 365 Customer Insights-eko hainbat gaitasun entitate horien inguruan eraikitzen dira. Hurbiletik berrikusteak gaitasun horien irteera balioztatzen lagun dezake.

The **Entitateak** orrialdeak entitateak zerrendatzen ditu eta zutabe hauek barne hartzen ditu:

- **Izena** : Datu-entitatearen izena. Entitate izenaren ondoan abisu sinbolo bat ikusiz gero, entitate horretako datuak ez dira behar bezala kargatu esan nahi du.
- **Iturria** : Entitatea irentsi duen datu-iturburu mota.
- **Eguneratua** : Entitatea azken aldiz eguneratu zen ordua.
- **Egoera** : Entitatearen azken eguneraketari buruzko xehetasunak.

[!INCLUDE [progress-details-include](../includes/progress-details-pane.md)]

## <a name="explore-a-specific-entitys-data"></a>Arakatu entitate jakin baten datuak

1. Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Entitateak**.
1. Tik **Entitateak** orrialdea, hautatu entitate bat xehetasunen orria irekitzeko.  
1. Arakatu entitate horretarako sartutako eremu eta erregistro desberdinak.

- **Atributuak** fitxa lehenespenez hautatuta dago eta hautatutako entitatearen xehetasunak berrikusteko taula erakusten du, hala nola, eremuen izenak, datu motak eta motak. **Mota** zutabeak Datuen eredu arruntari lotutako sistemak erakusten ditu, sistemak edo identifikatutako autoak [eskuz mapatuta](map-entities.md) erabiltzaileek. Mota hauek atributuen datu motetatik desberdinak izan daitezkeen mota semantikoak dira. Adibidez, beheko *Posta elektronikoa* eremuak *Testua* datu-mota du baina bere Common Data Model (semantikoa) mota izan liteke *Posta elektronikoa* edo *Posta elektroniko helbidea*.

> [!div class="mx-imgBorder"]
> ![Eremuen taula.](media/data-manager-entities-fields.PNG "Eremuen taula")

> [!NOTE]
> Orrialde honek zure entitatearen datuen lagin bat baino ez du erakusten. Datu multzo osoa ikusteko, joan **Datu iturriak** orrialdea, entitate bat aukeratu, hautatu **Editatu** eta, ondoren, ikusi entitate honen datuak Power Query editorearekin deskribatutako moduan [Datu iturriak](data-sources.md).

Erakundean irensten diren datuei buruz gehiago jakiteko, **Laburpena** zutabeak datuen zenbait ezaugarri garrantzitsu eskaintzen ditu, hala nola, nuluak, falta diren balioak, balio bakarrak, zenbatekoak eta banaketak, datuei dagokienez. Hautatu diagramaren ikonoa datuen laburpena ikusteko.

> [!div class="mx-imgBorder"]
> ![Laburpenaren sinboloa.](media/data-manager-entities-summary.png "Datuen laburpen-taula")

- **Datuak** fitxan entitatearen banakako erregistroei buruzko xehetasunak agertzen diren taula erakusten da. Zerrendatutako xehetasunak entitatearen datu-motaren araberakoak dira.

> [!div class="mx-imgBorder"]
> ![Hautatu entitate bat.](media/data-manager-entities-data.png "Hautatu entitate bat")

- The **Txostenak** fitxak (entitate batzuentzat eskuragarri) zure datuak txosten bat sortuz ikusteko aukera ematen dizu, eta zutabe hauek ditu:

  - **Txostenaren izena** : Txostenaren izena.
  - **Sortua** : Entitatea sortu duen pertsonaren izena.
  - **Sortu** : Entitatearen sorreraren data eta ordua.
  - **Egileak editatua** : Entitatea aldatu duen pertsonaren izena.
  - **Editatua** : Erakundearen aldaketaren data eta ordua. 

## <a name="entity-specific-information"></a>Entitatearen informazio zehatza

Hurrengo atalean sistemak sortutako entitate batzuei buruzko informazioa ematen da.

### <a name="corrupted-data-sources"></a>Hondatutako datu-iturburuak

Irentsitako datu-iturburu baten eremuek hondatutako datuak eduki ditzakete. Sistemak sortutako entitateetan hondatutako eremuak dituzten erregistroak agerian daude. Hondatutako erregistroak ezagutzeak iturburuko sisteman zein datu berrikusi eta eguneratu nahi dituzun identifikatzen lagunduko dizu. Datu-iturburuaren hurrengo freskatzearen ondoren, zuzendutako erregistroak Customer Insights-en irensten dira eta beheranzko prozesuetara pasatzen dira. 

Adibidez, "urtebetetzea" zutabeak datu mota "data" gisa ezarrita dauka. Bezeroaren erregistroan urtebetetzea '01/01/19777' gisa sartu da. Sistemak erregistro hau hondatuta dagoela markatuko du. Norbaitek iturburuko sisteman urtebetetzea '1977ra' alda dezake. Datu-iturriak freskatze automatizatuaren ondoren, eremuak baliozko formatua du eta erregistroa hondatutako entitatetik kenduko da. 

Joan **Datuak** > **Entitateak** eta bilatu hondatutako entitateak **Sistema** atalean. Hondatutako entitateen izendapen eskema: 'DataSourceName_EntityName_corrupt'.

Customer Insights-ek oraindik hondatutako erregistroak prozesatzen ditu. Hala ere, arazoak sor ditzakete datu bateratuekin lan egitean.

Iragarritako datuekin egiaztapen hauek exekutatzen dira hondatutako erregistroak agerian uzteko: 

- Eremu baten balioa ez dator bat bere zutabeko datu motarekin.
- Eremuek zutabeak espero den eskemarekin bat ez datozen eragiten duten karaktereak dituzte. Adibidez: gaizki formateatutako komatxoak, ihes egin gabeko komatxoak edo karaktere lerro berriak.
- Datetime/date/datetimeoffset zutabeak badaude, haien formatua ereduan zehaztu behar da ISO formatu estandarra jarraitzen ez badu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
