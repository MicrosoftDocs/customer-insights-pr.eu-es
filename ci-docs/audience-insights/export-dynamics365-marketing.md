---
title: Esportatu Customer Insights datuak Dynamics 365 Marketing-era
description: Ikasi Dynamics 365 Marketing konexioa nola konfiguratu.
ms.date: 08/21/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 163387779b64bd78ef08e2d96a5f1c9615062f28
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643758"
---
# <a name="connector-for-dynamics-365-marketing-preview"></a>Dynamics 365 Marketing konektorea (aurrebista)

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko. Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](https://docs.microsoft.com/dynamics365/marketing/customer-insights-segments)

## <a name="prerequisite"></a>Aurrebaldintza

[Common Data Service-n sartutako Dynamics 365 Marketing-eko](connect-power-query.md) kontaktuen erregistroak.

## <a name="configure-the-connector-for-marketing"></a>Konfiguratu konektorea Marketinerako

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Dynamics 365 Marketing** azpian hautatu **Konfiguratu**.

1. Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.

1. Sartu erakundearen Marketing URLa **Zerbitzariaren helbidea** eremu.

1. Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Marketing kontua.

1. Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.

1. Hautatu **Hurrengoa**.

1. Aukeratu segmentu bat edo gehiago.

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).
