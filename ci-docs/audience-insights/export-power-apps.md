---
title: Power Apps konektorea
description: Konektatu Power Apps eta Power Automate-rekin.
ms.date: 01/19/2021
ms.reviewer: nikeller
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 5a8bbb9a09218d54228589d43c21c8894680b56e
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5268901"
---
# <a name="microsoft-power-apps-connector-preview"></a>Microsoft Power Apps konektorea (Aurrebista)

Ekarri bezeroen profil bateratuak aplikazio pertsonalizatuekin Power Apps.

## <a name="connect-power-apps-and-dynamics-365-customer-insights"></a>Konektatu Power Apps eta Dynamics 365 Customer Insights

Customer Insights askoren artean dago [erabilgarri dauden datuetarako iturriak Power Apps](https://docs.microsoft.com/powerapps/maker/canvas-apps/working-with-data-sources).

Erreferentzi Power Apps dokumentazioa nola ikasi ikasteko [gehitu datuen konexioa aplikazio bati](https://docs.microsoft.com/powerapps/maker/canvas-apps/add-data-connection). Berrikustea ere gomendatzen dugu [nola Power Apps Delegazioa erabiltzen du Canvas aplikazioetan datu-multzo handiak kudeatzeko](https://docs.microsoft.com/powerapps/maker/canvas-apps/delegation-overview).

## <a name="available-entities"></a>Entitate erabilgarriak

Customer Insights konexio gisa gehitu ondoren, ondorengo entitateak aukeratu ditzakezu Power Apps:

- Bezeroa: hurrengoko datuak erabiltzeko [bezeroaren profil bateratua](customer-profiles.md).
- UnifiedActivity: aplikazioan [jardueren denbora-lerroa](activities.md) bistaratzeko.

## <a name="limitations"></a>Murriztapenak

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]