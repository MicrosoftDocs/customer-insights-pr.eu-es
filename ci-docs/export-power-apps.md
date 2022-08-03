---
title: Power Apps konektorea (Aurrebista)
description: Konektatu Power Apps eta Power Automate-rekin.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: Nils-2m
ms.author: nikeller
manager: shellyha
ms.openlocfilehash: 8807e82e65ea20d1a7f7dc07552229f377927eed
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196885"
---
# <a name="power-apps-connector-preview"></a>Power Apps konektorea (Aurrebista)

Ekarri bezeroen profil bateratuak aplikazio pertsonalizatuekin Microsoft Power Apps.

## <a name="connect-power-apps-and-dynamics-365-customer-insights"></a>Konektatu Power Apps eta Dynamics 365 Customer Insights

Customer Insights askoren artean dago [erabilgarri dauden datuetarako iturriak Power Apps](/powerapps/maker/canvas-apps/working-with-data-sources).

Erreferentzi Power Apps dokumentazioa nola ikasi ikasteko [gehitu datuen konexioa aplikazio bati](/powerapps/maker/canvas-apps/add-data-connection). Berrikustea ere gomendatzen dugu [nola Power Apps Delegazioa erabiltzen du Canvas aplikazioetan datu-multzo handiak kudeatzeko](/powerapps/maker/canvas-apps/delegation-overview).

## <a name="available-entities"></a>Entitate erabilgarriak

Customer Insights datu-konexio gisa gehitu ondoren, aukeratu entitate hauek Power Apps:

- **Bezeroa**: erabiltzeko datuak hurrengoan [bateratutako bezeroaren profila](customer-profiles.md).
- **UnifiedActivity**: bistaratzeko [jardueren kronograma](activities.md) aplikazioan.
- **ContactProfile**: bezero baten kontaktuak bistaratzeko. Entitate hau Customer Insights inguruneetan soilik dago eskuragarri negozio-kontuetarako.

## <a name="limitations"></a>Murriztapenak

### <a name="retrievable-entities"></a>Eskura daitezkeen entitateak

Fitxategia soilik berreskura dezakezu **Bezeroa**, **UnifiedActivity**, **Segmentuak**, eta **ContactProfile** entitateak Power Apps konektore. ContactProfile enpresa-kontuetarako Customer Insights inguruneetan soilik dago eskuragarri. Beste entitate batzuk erakusten dira azpiko konektoreak abiarazle bidez onartzen dituelako Power Automate.

60 segundoko 100 dei egin ditzakezu gehienez. API amaierako puntuari hainbat aldiz dei diezaiokezu $skip parametroa erabiliz. [Lortu informazio gehiago $skip parametroari buruz](/connectors/customerinsights/#get-items-from-an-entity).

### <a name="delegation"></a>Ordezkaritza

Ordezkaritza lanak **Bezeroa** entitatea eta **UnifiedActivity** entitatea.

- Ordezkaritza **Bezeroa** entitatea: entitate honetarako delegazioa erabiltzeko, eremuak indexatu behar dira [bilatu eta iragazi indizea](search-filter-index.md).  
- Ordezkaritza **UnifiedActivity**: Erakunde honen ordezkaritzak eremuetarako bakarrik funtzionatzen du **ActivityId** eta **Bezeroaren IDa**.  
- Ordezkaritza **ContactProfile**: Entitate honen ordezkaritzak eremuetarako bakarrik funtzionatzen du **ContactId** eta **CustomerId**. ContactProfile enpresa-kontuetarako Customer Insights inguruneetan soilik dago eskuragarri.

Ordezkaritzari buruzko informazio gehiago lortzeko, joan hona [Power Apps funtzio eta eragiketa delegagarriak](/powerapps/maker/canvas-apps/delegation-overview).

## <a name="example-gallery-control"></a>Adibidez galeria kontrola

Aukeran, gehitu bezeroen profilak a [galeriaren kontrola](/powerapps/maker/canvas-apps/add-gallery).

1. Gehitu **galeria** kontrolatzen ari zaren aplikazio batera.
  
   :::image type="content" source="media/connector-powerapps9.png" alt-text="Gehitu galeria-elementu bat.":::

1. Aukeratu **Bezeroaren** datu-iturburu elementuen gisa.

   :::image type="content" source="media/choose-datasource-powerapps.png" alt-text="Hautatu datu-iturburua.":::

1. Aldatu eskuineko datu-panela Bezeroaren entitateak galerian erakutsiko duen eremua hautatzeko.

1. Aukeratutako bezeroaren eremuan edozein galeria erakutsi nahi baduzu, bete **Testua** propietatea etiketa erabiliz **{Name_of_the_gallery}.hautatutakoa.{property_name}**  
    - Adibidez: _Gallery1.Selected.address1_city_

1. Bistaratzeko bateratua kronologia bezero baterako, gehitu galeriaren elementua, eta gehitu **Elementuak** propietatea erabiliz **Iragazi('UnifiedActivity', CustomerId = {Customer_Id})**  
    - Adibidez: _Iragazi('UnifiedActivity', CustomerId = Gallery1.Selected.CustomerId)_

[!INCLUDE [footer-include](includes/footer-banner.md)]
