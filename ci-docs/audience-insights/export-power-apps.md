---
title: Power Apps konektorea
description: Konektatu Power Apps eta Power Automate-rekin.
ms.date: 08/21/2020
ms.reviewer: nikeller
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: b6ec103e29e218b2f27bfc1193300ea793a6b30b
ms.sourcegitcommit: cf9b78559ca189d4c2086a66c879098d56c0377a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/03/2020
ms.locfileid: "4404954"
---
# <a name="microsoft-power-apps-connector-preview"></a>Microsoft Power Apps konektorea (Aurrebista)

Ekarri bezeroen profil bateratuak aplikazio pertsonalizatuekin Power Apps.

## <a name="connect-power-apps-and-dynamics-365-customer-insights"></a>Konektatu Power Apps eta Dynamics 365 Customer Insights

Customer Insights askoren artean dago [erabilgarri dauden datuetarako iturriak Power Apps](https://docs.microsoft.com/powerapps/maker/canvas-apps/working-with-data-sources).

Erreferentzi Power Apps dokumentazioa nola ikasi ikasteko [gehitu datuen konexioa aplikazio bati](https://docs.microsoft.com/powerapps/maker/canvas-apps/add-data-connection). Berrikustea ere gomendatzen dugu [nola Power Apps Delegazioa erabiltzen du Canvas aplikazioetan datu-multzo handiak kudeatzeko](https://docs.microsoft.com/powerapps/maker/canvas-apps/delegation-overview).

## <a name="available-entities"></a>Entitate erabilgarriak

Customer Insights konexio gisa gehitu ondoren, ondorengo entitateak aukeratu ditzakezu Power Apps:

- Bezeroa: hurrengoko datuak erabiltzeko [bezeroaren profil bateratua](customer-profiles.md).
- Bezeroaren jarduera bateratua: bistaratzeko [jardueraren denbora-eskala](activities.md) aplikazioan.

## <a name="limitations"></a>Mugak

### <a name="retrievable-entities"></a>Eskura daitezkeen entitateak

Fitxategia soilik berreskura dezakezu **Bezeroa**, **UnifiedActivity**, eta **Segmentuak** entitateak Power Apps konektore. Beste entitate batzuk erakusten dira azpiko konektoreak abiarazle bidez onartzen dituelako Power Automate.  

### <a name="delegation"></a>Ordezkaritza

Ordezkaritza Bezeroen entitatearen eta UnifiedActivity entitatearen funtzionatzen du. 

- **Bezeroa** entitatearen ordezkaritza: entitate honen ordezkaritza erabiltzeko, eremuak indexatu behar dira hemen: [Bilaketa- eta iragazki-indizea](search-filter-index.md).  

- Ordezkaritza **UnifiedActivity**: Erakunde honen ordezkaritzak eremuetarako bakarrik funtzionatzen du **ActivityId** eta **Bezeroaren IDa**.  

- Ordezkaritzari buruzko informazio gehiago lortzeko, ikusi [Power Apps funtzio eta eragiketa delegagarriak](https://docs.microsoft.com/connectors/commondataservice/#power-apps-delegable-functions-and-operations-for-the-cds-for-apps). 

## <a name="example-gallery-control"></a>Adibidez galeria kontrola

Adibidez, bezero profilak gehitzen dizkiozu [galeriaren kontrolari](https://docs.microsoft.com/powerapps/maker/canvas-apps/add-gallery).

1. Gehitu a **Galeria** kontrolatzen ari zaren aplikazio batera.

> [!div class="mx-imgBorder"]
> ![Gehitu galeria-elementu bat](media/connector-powerapps9.png "Gehitu galeria-elementu bat")

1. Aukeratu **Bezeroaren** datu-iturburu elementuen gisa.

    > [!div class="mx-imgBorder"]
    > ![Hautatu datu-iturburua](media/choose-datasource-powerapps.png "Hautatu datu-iturburua")

1. Eskubian dagoen datuen panela alda dezakezu Bezeroaren entitateak galerian erakusteko zein eremutan hautatu ahal izateko.

1. Aukeratutako bezeroaren eremuan edozein galeria erakutsi nahi baduzu, bete etiketa baten Testuaren propietatea: **{Name_of_the_gallery}.Selected.{property_name}**

    Adibidea: Gallery1.Selected.address1_city

1. Bezeroarentzako denbora-lerro bateratua bistaratzeko, gehitu Galeriako elementua eta gehitu elementuak jabetza: **Iragazkia('UnifiedActivity', CustomerId = {Customer_Id})**

    Adibidez: Iragazkia('UnifiedActivity', CustomerId = Gallery1.Selected.CustomerId)
