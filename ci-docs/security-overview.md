---
title: Segurtasun-ezarpenak Customer Insights-en
description: Lortu informazio gehiago segurtasun-ezarpenei buruz Dynamics 365 Customer Insights.
ms.date: 06/08/2022
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: 163deb9bed4f82d742c46cace27dd128f0aca18b
ms.sourcegitcommit: 8e9f0a9693fd8d91ad0227735ff03688fef5406f
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/10/2022
ms.locfileid: "8947400"
---
# <a name="security-settings-in-customer-insights"></a>Segurtasun-ezarpenak Customer Insights-en

The **Segurtasuna** orrialdeak erabiltzailearen baimenak eta funtzioak egiten laguntzen duten konfiguratzeko aukerak zerrendatzen ditu Dynamics 365 Customer Insights seguruagoa. Administratzaileek soilik atzi dezakete orrialde honetara.

Joan **Admin** > **Segurtasuna** ezarpenak konfiguratzeko.

The **Segurtasuna** orrialdeak fitxa hauek ditu:

- [Erabiltzaileak](#users-tab)
- [APIak](#apis-tab)
- [Esteka pribatuak](#private-links-tab)
- [Key Vault](#key-vault-tab)
- [Sartu segurtasunez bezeroaren datuak Customer Lockbox-ekin (aurrebista)](#securely-access-customer-data-with-customer-lockbox-preview)

## <a name="users-tab"></a>Erabiltzaileak fitxa

Customer Insights-erako sarbidea administratzaile batek aplikazioan gehitu dituen zure erakundeko erabiltzaileei mugatuta dago. The **Erabiltzaileak** fitxak erabiltzaileen sarbidea eta haien baimenak kudeatzeko aukera ematen dizu. Informazio gehiagorako, ikus [Erabiltzaileen baimenak](permissions.md).

## <a name="apis-tab"></a>APIen fitxa

Ikusi eta kudeatu teklak erabiltzeko [Customer Insights APIak](apis.md) zure inguruneko datuekin.

Lehen eta bigarren mailako gako berriak sor ditzakezu hautatuta **Birsortu primarioa** edo **Bigarren mailako birsortzea**. 

API ingurunerako sarbidea blokeatzeko, hautatu **Desgaitu**. APIak desgaituta badaude, hauta dezakezu **Gaitu** berriro sarbidea emateko.

## <a name="private-links-tab"></a>Esteka pribatuak fitxa

[Azure esteka pribatua](/azure/private-link/private-link-overview) konekta gaitezen Customer Insights zure Azure Data Lake Storage kontua zure sare birtualeko amaiera-puntu pribatu batean. Biltegiratze-kontu bateko datuetarako, Internet publikora ez dagoena, Private Link-ek sare mugatu horrekin konektatzea ahalbidetzen du.

> [!IMPORTANT]
> Esteka pribatuko konexioa konfiguratzeko gutxieneko rol-eskakizuna:
>
> - Bezeroaren ikuspegia: Administratzailea
> - Azure integratutako rola: [Biltegiratze-kontuaren laguntzailea](/azure/role-based-access-control/built-in-roles#storage-account-contributor)
> - Azure rol pertsonalizaturako baimenak: [Microsoft.Storage/storageAccounts/read eta Microsoft.Storage/storageAccounts/PrivateEndpointConnectionsApproval/action](/azure/role-based-access-control/resource-provider-operations#microsoftstorage)
>

Customer Insights-en Esteka pribatua konfiguratzea bi urratseko prozesua da. Lehenik eta behin, esteka pribatu bat sortzen hasten zara **Admin** > **Segurtasuna** > **Esteka pribatuak** Bezeroen Insights-en. The **Gehitu esteka pribatua** panelak zure maizterraren biltegiratze-kontuak zerrendatzen ditu ikusteko baimenak dituzunak. Hautatu biltegiratze-kontua eta eman baimena Esteka pribatua sortzeko.

Ondoren, Data Lake biltegiratze kontuaren esteka pribatua onartu behar duzu. Ireki pantailan aurkezten den esteka Esteka pribatu berria onartzeko.

## <a name="key-vault-tab"></a>Gakoen ganga fitxa

The **Gakoen ganga** fitxak zurea lotu eta kudeatzeko aukera ematen dizu [Azure gakoen ganga](/azure/key-vault/general/basic-concepts) ingurumenari.
Eskainitako gako-ganga erakundearen betetze-mugan sekretuak agertzeko eta erabiltzeko erabil daiteke. Customer Insights-ek Azure Key Vault-eko sekretuak erabil ditzake [konexioak ezarri](connections.md) hirugarrenen sistemetara.

Informazio gehiagorako, ikus [Ekarri zure Azure key vault](use-azure-key-vault.md).

## <a name="securely-access-customer-data-with-customer-lockbox-preview"></a>Sartu segurtasunez bezeroaren datuak Customer Lockbox-ekin (aurrebista)

Customer Insights erabiltzen ari da Power Platform Bezeroaren Lockbox gaitasuna. Customer Lockbox interfaze bat eskaintzen du datuak atzitzeko eskaerak berrikusteko eta onartzeko (edo ukatzeko). Eskaera hauek laguntza-kasu bat konpontzeko bezeroen datuetarako sarbidea behar denean gertatzen dira. Eginbide hau erabiltzeko, Customer Insights-ek lehendik dagoen konexio bat izan behar du a Microsoft Dataverse zure maizterren ingurunea.

Bezeroen Lockbox-ari buruzko informazio gehiago lortzeko, ikusi [laburpen](/power-platform/admin/about-lockbox#summary) de Power Platform Bezeroaren Lockbox. Artikuluak ere deskribatzen du [lan-fluxua](/power-platform/admin/about-lockbox#workflow) eta behar dena [konfigurazioa](/power-platform/admin/about-lockbox#enable-the-lockbox-policy) Customer Lockbox gaitzeko.

> [!IMPORTANT]
> Administratzaile globalak Power Platform edo Power Platform administratzaileek Customer Insights-etarako igorritako Customer Lockbox eskaerak onar ditzakete.

[!INCLUDE [footer-include](includes/footer-banner.md)]
