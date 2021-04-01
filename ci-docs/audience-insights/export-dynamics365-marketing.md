---
title: Esportatu Customer Insights datuak Dynamics 365 Marketing-era
description: Ikasi Dynamics 365 Marketing konexioa nola konfiguratu.
ms.date: 02/01/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 892aff643872f11307a2c43e5670edab657d7848
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597588"
---
# <a name="connector-for-dynamics-365-marketing-preview"></a>Dynamics 365 Marketing konektorea (aurrebista)

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko. Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments)

## <a name="prerequisite"></a>Aurrebaldintza

- Kontaktu-erregistroek Dynamics 365 Marketing-en egon behar dute segmentu bat Customer Insights-etik Marketing-era esportatu ahal izateko. Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Marketing erabiliz Common Data Services](connect-power-query.md).

  > [!NOTE]
  > Ikuspegien estatistiketatik Marketing segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Marketing instantzietan. Marketing kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili. Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]