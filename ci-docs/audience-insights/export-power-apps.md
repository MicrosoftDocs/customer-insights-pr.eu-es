---
title: Power Apps konektorea
description: Konektatu Power Apps eta Power Automate-rekin.
ms.date: 10/01/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: Nils-2m
ms.author: nikeller
manager: shellyha
ms.openlocfilehash: 18cc32a169e79794d2d3203d462620ab41efaafe
ms.sourcegitcommit: d168a738a08adb8b4b2e410bdaa3716d7b63cc9b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/17/2022
ms.locfileid: "8455923"
---
# <a name="microsoft-power-apps-connector-preview"></a>Microsoft Power Apps konektorea (Aurrebista)

Ekarri bezeroen profil bateratuak aplikazio pertsonalizatuekin Power Apps.

## <a name="connect-power-apps-and-dynamics-365-customer-insights"></a>Konektatu Power Apps eta Dynamics 365 Customer Insights

Customer Insights askoren artean dago [erabilgarri dauden datuetarako iturriak Power Apps](/powerapps/maker/canvas-apps/working-with-data-sources).

Erreferentzi Power Apps dokumentazioa nola ikasi ikasteko [gehitu datuen konexioa aplikazio bati](/powerapps/maker/canvas-apps/add-data-connection). Berrikustea ere gomendatzen dugu [nola Power Apps Delegazioa erabiltzen du Canvas aplikazioetan datu-multzo handiak kudeatzeko](/powerapps/maker/canvas-apps/delegation-overview).

## <a name="available-entities"></a>Entitate erabilgarriak

Customer Insights konexio gisa gehitu ondoren, ondorengo entitateak aukeratu ditzakezu Power Apps:

- **Bezeroa**: erabiltzeko datuak hurrengoan [bateratutako bezeroaren profila](customer-profiles.md).
- **UnifiedActivity**: bistaratzeko [jardueren kronograma](activities.md) aplikazioan.
- **ContactProfile**: bezero baten kontaktuak bistaratzeko. Entitate hori soilik eskuragarria publikoaren xehetasunak ingurunearena negozio-konturako.

## <a name="limitations"></a>Murriztapenak

### <a name="retrievable-entities"></a>Eskura daitezkeen entitateak

Fitxategia soilik berreskura dezakezu **Bezeroa**, **UnifiedActivity**, **Segmentuak**, eta **ContactProfile** entitateak Power Apps konektore. ContactProfile soilik eskuragarria publikoaren xehetasunak instantzia negozio-konturako. Beste entitate batzuk erakusten dira azpiko konektoreak abiarazle bidez onartzen dituelako Power Automate.

60 segundoko 100 dei egin ditzakezu gehienez. API amaierako puntuari hainbat aldiz dei diezaiokezu $skip parametroa erabiliz. [Lortu informazio gehiago $skip parametroari buruz](/connectors/customerinsights/#get-items-from-an-entity).

### <a name="delegation"></a>Ordezkaritza

Ordezkaritza lanak **Bezeroa** entitatea eta **UnifiedActivity** entitatea. 

- **Bezeroa** entitatearen ordezkaritza: entitate honen ordezkaritza erabiltzeko, eremuak indexatu behar dira hemen: [Bilaketa- eta iragazki-indizea](search-filter-index.md).  
- Ordezkaritza **UnifiedActivity**: Erakunde honen ordezkaritzak eremuetarako bakarrik funtzionatzen du **ActivityId** eta **Bezeroaren IDa**.  
- Ordezkaritza **ContactProfile**: Entitate honen ordezkaritzak eremuetarako bakarrik funtzionatzen du **ContactId** eta **CustomerId**. ContactProfile soilik eskuragarria publikoaren xehetasunak inguruneak negozio-konturako.

Ordezkaritzari buruzko informazio gehiago lortzeko, joan hona [Power Apps funtzio eta eragiketa delegagarriak](/powerapps/maker/canvas-apps/delegation-overview). 

## <a name="example-gallery-control"></a>Adibidez galeria kontrola

Bezeroen profilak gehi ditzakezu [galeriaren kontrola](/powerapps/maker/canvas-apps/add-gallery).

1. Gehitu **galeria** kontrolatzen ari zaren aplikazio batera.

    > [!div class="mx-imgBorder"]
    > ![Gehitu galeria-elementu bat.](media/connector-powerapps9.png "Gehitu galeria-elementu bat.")

2. Aukeratu **Bezeroaren** datu-iturburu elementuen gisa.

    > [!div class="mx-imgBorder"]
    > ![Hautatu datu-iturburua.](media/choose-datasource-powerapps.png "Hautatu datu-iturburua.")

3. Eskubian dagoen datuen panela alda dezakezu Bezeroaren entitateak galerian erakusteko zein eremutan hautatu ahal izateko.

4. Aukeratutako bezeroaren eremuan edozein galeria erakutsi nahi baduzu, bete **Testua** propietatea etiketa erabiliz **{Name_of_the_gallery}.hautatutakoa.{property_name}**  
    - Adibidez: _Gallery1.Selected.address1_city_

5. Bistaratzeko bateratua kronologia bezero baterako, gehitu galeriaren elementua, eta gehitu **Elementuak** propietatea erabiliz **Iragazi('UnifiedActivity', CustomerId = {Customer_Id})**  
    - Adibidez: _Iragazi('UnifiedActivity', CustomerId = Gallery1.Selected.CustomerId)_


[!INCLUDE[footer-include](../includes/footer-banner.md)]
