---
title: Segurtasun-ezarpenak atalean Dynamics 365 Customer Insights
description: Lortu informazio gehiago segurtasun-ezarpenei buruz Dynamics 365 Customer Insights.
ms.date: 04/28/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 5d73bacccadc9193d76d8dfafd0365dabc911e00
ms.sourcegitcommit: cf74b8c20d88eb96e1ac86e18cd44fe27aad5ab9
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/28/2022
ms.locfileid: "8653769"
---
# <a name="security-overview-page"></a>Segurtasunaren ikuspegi orokorra orria

The **Segurtasuna** orrialdeak erabiltzaileen baimenak eta funtzioak egiten laguntzen duten konfiguratzeko aukerak zerrendatzen ditu Dynamics 365 Customer Insights seguruagoa. Administratzaileek soilik atzi dezakete orrialde honetara. 

Joan **Admin** > **Segurtasuna** ezarpenak konfiguratzeko.

The **Segurtasuna** orrialdeak fitxa hauek ditu:
- [Erabiltzaileak](#users-tab)
- [APIak](#apis-tab)
- [Key Vault](#key-vault-tab)

## <a name="users-tab"></a>Erabiltzaileak fitxa

Customer Insights-erako sarbidea administratzaile batek aplikaziora gehitu dituen zure erakundeko erabiltzaileei mugatuta dago. The **Erabiltzaileak** fitxak erabiltzaileen sarbidea eta haien baimenak kudeatzeko aukera ematen dizu. Informazio gehiagorako, ikus [Erabiltzaileen baimenak](permissions.md).

## <a name="apis-tab"></a>APIen fitxa

Ikusi eta kudeatu teklak erabiltzeko [Customer Insights APIak](apis.md) zure inguruneko datuekin.

Lehen eta bigarren mailako gako berriak sor ditzakezu hautatuta **Birsortu primarioa** edo **Bigarren mailako birsortzea**. 

API ingurunerako sarbidea blokeatzeko, hautatu **Desgaitu**. APIak desgaituta badaude, hauta dezakezu **Gaitu** berriro sarbidea emateko.

## <a name="key-vault-tab"></a>Gakoen ganga fitxa

The **Gakoen ganga** fitxak zurea lotu eta kudeatzeko aukera ematen dizu [Azure gakoen ganga](/azure/key-vault/general/basic-concepts) ingurumenari.
Eskainitako gako-ganga erakundearen betetze-mugan sekretuak agertzeko eta erabiltzeko erabil daiteke. Customer Insights-ek Azure Key Vault-eko sekretuak erabil ditzake [konexioak ezarri](connections.md) hirugarrenen sistemetara.

Informazio gehiagorako, ikus [Ekarri zure Azure key vault](use-azure-key-vault.md).


[!INCLUDE [footer-include](includes/footer-banner.md)]
