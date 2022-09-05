---
title: Konfiguratu segurtasun ezarpenak
description: Lortu informazio gehiago segurtasun-ezarpenei buruz Dynamics 365 Customer Insights.
ms.date: 08/02/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: d20d57e9b7724e9921f9341eeaa39141b4555ff1
ms.sourcegitcommit: 624b27bb65a0de1970dc1ac436643b493f0a31cf
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387234"
---
# <a name="configure-security-settings"></a>Konfiguratu segurtasun ezarpenak

Kudeatu API gakoak, atzitu bezeroen datuak eta konfiguratu Azure esteka pribatu bat.

## <a name="manage-api-keys"></a>Kudeatu API gakoak

Ikusi eta kudeatu teklak erabiltzeko [Customer Insights APIak](apis.md) zure inguruneko datuekin.

1. Joan **Admin** > **Segurtasuna** eta hautatu **APIak** fitxa.

1. Ingurunerako API sarbidea konfiguratu ez bada, hautatu **Gaitu**. Edo, ingurunerako API sarbidea blokeatzeko, hautatu **Desgaitu** eta baieztatu.

1. Kudeatu API gako nagusiak eta bigarren mailakoak:

   1. API gako nagusia edo bigarren mailakoa erakusteko, hautatu **Erakutsi** sinboloa.

   1. API gako nagusia edo bigarren mailakoa kopiatzeko, hautatu **Kopiatu** sinboloa.

   1. API gako nagusi edo bigarren mailako berriak sortzeko, hautatu **Birsortu primarioa** edo **Bigarren mailako birsortzea** .

## <a name="securely-access-customer-data-with-customer-lockbox-preview"></a>Sartu segurtasunez bezeroaren datuak Customer Lockbox-ekin (aurrebista)

Customer Insights-ek hau erabiltzen du Power Platform Bezeroaren Lockbox gaitasuna. Customer Lockbox interfaze bat eskaintzen du datuak atzitzeko eskaerak berrikusteko eta onartzeko (edo ukatzeko). Eskaera hauek laguntza-kasu bat konpontzeko bezeroen datuetarako sarbidea behar denean gertatzen dira. Eginbide hau erabiltzeko, Customer Insights-ek lehendik dagoen konexio bat izan behar du a Microsoft Dataverse zure maizterren ingurunea.

Bezeroen Lockbox-ari buruzko informazio gehiago lortzeko, ikusi [laburpen](/power-platform/admin/about-lockbox#summary) de Power Platform Bezeroaren Lockbox. Artikuluak ere deskribatzen du [lan-fluxua](/power-platform/admin/about-lockbox#workflow) eta behar dena [konfigurazioa](/power-platform/admin/about-lockbox#enable-the-lockbox-policy) Customer Lockbox gaitzeko.

> [!IMPORTANT]
> Administratzaile globalak Power Platform edo Power Platform administratzaileek Customer Insights-etarako igorritako Customer Lockbox eskaerak onar ditzakete.

## <a name="set-up-an-azure-private-link"></a>Konfiguratu Azure esteka pribatu bat

[Azure esteka pribatua](/azure/private-link/private-link-overview) Customer Insights zure zerbitzura konektatzeko aukera ematen du Azure Data Lake Storage kontua zure sare birtualeko amaierako puntu pribatu batean. Biltegiratze-kontu bateko datuetarako, Internet publikora ez dagoena, Private Link-ek sare mugatu horrekin konektatzea ahalbidetzen du.

> [!IMPORTANT]
> Esteka pribatuko konexioa konfiguratzeko gutxieneko rol-eskakizuna:
>
> - Bezeroen ikuspegia: Administratzailea
> - Azure integratutako rola: [Biltegiratze-kontuaren laguntzailea](/azure/role-based-access-control/built-in-roles#storage-account-contributor)
> - Azure rol pertsonalizaturako baimenak: [Microsoft.Storage/storageAccounts/read eta Microsoft.Storage/storageAccounts/PrivateEndpointConnectionsApproval/action](/azure/role-based-access-control/resource-provider-operations#microsoftstorage)

1. Customer Insights atalean, joan hona **Admin** > **Segurtasuna** eta hautatu **Esteka pribatuak** fitxa.

1. Hautatu **Gehitu esteka pribatua** .

   The **Gehitu esteka pribatua** panelak zure maizterraren biltegiratze-kontuak zerrendatzen ditu ikusteko baimenak dituzunak.

1. Hautatu harpidetza, baliabide taldea eta biltegiratze kontua.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Sakatu **Gorde**.

1. Joan zure Data Lake Storage kontura eta ireki pantailan agertzen den esteka.

1. Onartu esteka pribatua.


[!INCLUDE [footer-include](includes/footer-banner.md)]
