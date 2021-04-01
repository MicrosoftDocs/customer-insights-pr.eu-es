---
title: Entitateak eta datu multzoak
description: Ikusi datuak Entitateen orrian.
ms.date: 04/16/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
ms.openlocfilehash: 383523bad5105e08e57758838e90a49e805b5f9b
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596392"
---
# <a name="entities-in-audience-insights"></a>Hartzaileen xehetasunetako entitateak

Ondoren [zure datu-iturriak konfiguratuz](data-sources.md), joan **erakundeak** iradokitako datuen kalitatea ebaluatzeko orria. Entitateak datu multzo gisa hartzen dira. Dynamics 365 Customer Insights-eko hainbat gaitasun entitate horien inguruan eraikitzen dira. Hurbiletik berrikusteak gaitasun horien irteera balioztatzen lagun dezake.

**Erakundeak** orrialdeak entitateen zerrenda eta hainbat zutabe biltzen ditu:

- **izena**: Zure datu erakundearen izena. Entitate izenaren ondoan abisu sinbolo bat ikusiz gero, entitate horretako datuak ez dira behar bezala kargatu esan nahi du.
- **Iturria**: Entitateak irentsitako datu-iturri mota
- **Hurrengoak sortua**: Entitatea sortu zuen pertsonaren izena
- **Sortu**: Entitatea sortzearen eguna eta ordua
- **Hurrengoak eguneratu**: Entitatea eguneratu zuen pertsonaren izena
- **Azken eguneraketa**: Erakundearen azken eguneraketaren data eta ordua
- **Azken freskagarria**: Azken datuen berritze data eta ordua

## <a name="exploring-a-specific-entitys-data"></a>Entitate jakin baten datuak arakatzea

Hautatu entitate bat entitate horren barne dauden eremu eta erregistro ezberdinak arakatzeko.

> [!div class="mx-imgBorder"]
> ![Hautatu entitatea](media/data-manager-entities-data.png "Hautatu entitatea")

- The **Datuak** fitxa lehenespenez hautatzen da eta entitatearen erregistro indibidualen inguruko xehetasunak agertzen ditu.

> [!div class="mx-imgBorder"]
> ![Eremuen taula](media/data-manager-entities-fields.PNG "Eremuen taula")

- The **eremuak** fitxak taula bat erakusten du hautatutako entitatearen xehetasunak berrikusteko, hala nola, eremu izenak, datu motak eta motak. **Mota** zutabeak Datuen eredu arruntari lotutako sistemak erakusten ditu, sistemak edo identifikatutako autoak [eskuz mapatuta](map-entities.md) erabiltzaileek. Ezaugarri semantiko hauek desberdinak izan daitezke, adibidez, eremua *Emaila* azpian datu mota bat dago *Testua* baina bere (semantikoa) datu arruntaren eredua motakoa izan liteke *Emaila* edo *Posta elektroniko helbidea*.

> [!NOTE]
> Bi taulek zure entitatearen datuen lagin bat baino ez dute erakusten. Datu multzo osoa ikusteko, joan **Datu iturriak** orrialdea, entitate bat aukeratu, hautatu **Editatu** eta, ondoren, ikusi entitate honen datuak Power Query editorearekin deskribatutako moduan [Datu iturriak](data-sources.md).

Erakundean irensten diren datuei buruz gehiago jakiteko, **Laburpena** zutabeak datuen zenbait ezaugarri garrantzitsu eskaintzen ditu, hala nola, nuluak, falta diren balioak, balio bakarrak, zenbatekoak eta banaketak, datuei dagokienez.

Hautatu diagramaren ikonoa datuen laburpena ikusteko.

> [!div class="mx-imgBorder"]
> ![Laburpenaren sinboloa](media/data-manager-entities-summary.png "Datuen laburpen-taula")

### <a name="next-step"></a>Hurrengo urratsa

Ikusi [bateratzeko](data-unification.md) gaia ikasteko *mapa*, *bat-etortzea*, eta *konbinatu* iradokitako datuak.


[!INCLUDE[footer-include](../includes/footer-banner.md)]