---
title: Esportatu Customer Insights datuak Dynamics 365 Sales-era
description: Ikasi Dynamics 365 Sales konexioa nola konfiguratu.
ms.date: 02/01/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 39ecdf528c6be4d8fb420a52a6ed998317e43bcd
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5598094"
---
# <a name="connector-for-dynamics-365-sales-preview"></a>Dynamics 365 Sales konektorea (aurrebista)

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Dynamics 365 Sales-ekin marketin-zerrendak sortzeko, lan-fluxuen segimendua egiteko eta eskaintzak bidaltzeko, erabili bezeroen datuak.

## <a name="prerequisite"></a>Aurrebaldintza

1. Kontaktu-erregistroek Dynamics 365 Sales-en egon behar dute segmentu bat Customer Insights-etik Sales-era esportatu ahal izateko. Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Sales erabiliz Common Data Services](connect-power-query.md).

   > [!NOTE]
   > Ikuspegien estatistiketatik salmentetara segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Sales instantzietan. Sales kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili. Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.

## <a name="configure-the-connector-for-sales"></a>Konfiguratu konektorea Sales-erako

1. Hartzaileei buruzko xehetasunetan, joan hona: **Administratzailea** > **Esportatu helburuak**.

1. **Dynamics 365 Sales** azpian hautatu **Konfiguratu**.

1. Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.

1. Sartu erakundearen Salmentako URLa **Zerbitzariaren helbidea** eremu.

1. Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Sales kontua.

1. Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.

1. Hautatu **Hurrengoa**.

1. Aukeratu segmentu bat edo gehiago.

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).


[!INCLUDE[footer-include](../includes/footer-banner.md)]