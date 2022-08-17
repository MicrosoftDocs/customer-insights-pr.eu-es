---
title: Erabili zurea Azure Data Lake Storage Gen2 kontua
author: mukeshpo
description: Ezagutu zurea erabiltzeko baldintzak Azure Data Lake Storage kontua Customer Insights datuak gordetzeko.
ms.author: mukeshpo
ms.date: 06/08/2022
ms.topic: conceptual
ms.manager: shellyha
ms.custom: intro-internal
ms.reviewer: mhart
ms.openlocfilehash: d2ff49c324c5c5c28213f362ff330d441fcb6052
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9246186"
---
# <a name="use-your-own-azure-data-lake-storage-gen2-account"></a>Erabili zurea Azure Data Lake Storage Gen2 kontua

Dynamics 365 Customer Insights zure datu guztiak gordetzeko aukera ematen dizu [Azure Data Lake Storage Gen2](/azure/storage/blobs/data-lake-storage-introduction).

Datuak Data Lake Storage-n gordez gero, onartzen duzu datuak Azure biltegiratze-kontu horren kokapen geografiko egokian transferituko direla eta gordeko direla. Informazio gehiagorako, ikus [Microsoft Trust Center](https://www.microsoft.com/trust-center).

Customer Insights-eko administratzaileek egin dezakete [inguruneak sortu](create-environment.md) eta [zehaztu datuak gordetzeko aukera](create-environment.md#step-2-configure-data-storage) prozesuan.

## <a name="prerequisites-to-use-your-storage-account"></a>Biltegiratze-kontua erabiltzeko aurrebaldintzak

- Azure Data Lake Storage kontuek Customer Insights ingurunea sortzean hautatu zenuen Azure eskualde berean egon behar dute. Bezeroen Insights ingurunearen eskualdea ikus dezakezu hemen **Admin** > **Sistema** > **Buruz**.
- Data Lake biltegiratzeak Gen2 izan behar du eta eduki [izen-espazio hierarkikoa gaituta](/azure/storage/blobs/create-data-lake-storage-account). Gen1 biltegiratze-kontuak ez dira onartzen.
- Izeneko edukiontzi bat`customerinsights` biltegiratze-kontuan egon behar du. Sortu behar duzu zure Data Lake biltegiratzea Customer Insights-en erabili aurretik. Customer Insights ingurunea konfiguratzen duen administratzaileak biltegiratze-kontuan edo biltegiratze-kontuan biltegiratze-kontuan edo biltegiratze-kontuan biltegiratze-kontuan edo biltegiratze-datuen kolaboratzailea edo biltegiratze-datuen jabearen rola behar du.`customerinsights` edukiontzia. Biltegiratze-kontu batean baimena esleitzeari buruzko informazio gehiago lortzeko, ikus [Sortu biltegiratze kontu bat](/azure/storage/common/storage-account-create?toc=%2Fazure%2Fstorage%2Fblobs%2Ftoc.json&tabs=azure-portal).

## <a name="connect-customer-insights-with-your-storage-account"></a>Konektatu Customer Insights zure biltegiratze-kontuarekin

Ingurune berri bat sortzen duzunean, ziurtatu Data Lake Storage kontua badagoela eta aurrebaldintza guztiak betetzen direla.

1. urtean **Datuen biltegiratzea** ingurunea sortzean urratsa, ezarri **Gorde irteerako datuak** to **Azure Data Lake Storage Gen2**.
1. Aukeratu nola egin **Konektatu biltegia**. Baliabideetan oinarritutako aukera eta autentifikaziorako harpidetzan oinarritutako aukera bat aukeratu dezakezu. Informazio gehiagorako, ikus [Konektatu batera Azure Data Lake Storage kontua Azure Service Principal bat erabiliz](connect-service-principal.md).
   - Izan ere **Azure harpidetza**, aukeratu **Harpidetza**, **taldea**, eta **Biltegiratze kontua** daukan`customerinsights` edukiontzia.
   - Izan ere **Kontuaren gakoa**, eman **Kontuaren izena** eta **Kontuaren gakoa** Data Lake Storage konturako. Autentifikazio-metodo hau erabiltzeak zure erakundeak gakoak biratzen dituen ala ez jakinarazten dizula esan nahi du. Behar duzu [eguneratu ingurunearen konfigurazioa](manage-environments.md#edit-an-existing-environment) giltza berriarekin biratzen denean.
1. Aukeratu Azure Private Link erabili nahi duzun biltegiratze-kontura konektatzeko eta [sortu konexioa Esteka pribaturako](security-overview.md#set-up-an-azure-private-link) bi urratseko prozesu batekin.

Sistemak datuak sartzea bezalako prozesuak amaitzen direnean, sistemak dagozkien karpetak sortzen ditu biltegiratze-kontuan. Datu fitxategiak eta *model.json* fitxategiak sortzen dira eta karpetetan gehitzen dira prozesuaren izenean oinarrituta.

Customer Insights-eko hainbat ingurune sortzen badituzu eta irteerako entitateak ingurune horietako biltegiratze kontuan gordetzea aukeratzen baduzu, Customer Insights-ek karpeta bereiziak sortzen ditu ingurune bakoitzarekin `ci_environmentID` edukiontzian.
