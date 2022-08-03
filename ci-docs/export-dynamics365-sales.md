---
title: Esportatu segmentuak Dynamics 365 Sales-era (aurrebista)
description: Ikasi konexioa nola konfiguratu eta Dynamics 365 Sales-era esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
searchScope:
- ci-export
- customerInsights
ms.openlocfilehash: c3497f4625cada49ae33c6987e58994a15536f9b
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9195966"
---
# <a name="export-segments-to-dynamics-365-sales-preview"></a>Esportatu segmentuak Dynamics 365 Sales-era (aurrebista)

Dynamics 365 Sales-ekin marketin-zerrendak sortzeko, lan-fluxuen segimendua egiteko eta eskaintzak bidaltzeko, erabili bezeroen datuak.

## <a name="prerequisites"></a>Aurrebaldintzak

Kontaktu-erregistroek Dynamics 365 Sales-en egon behar dute segmentu bat Customer Insights-etik Sales-era esportatu ahal izateko. Irakurri gehiago kontaktuak nola irensteko [Dynamics 365 Sales erabiliz Microsoft Dataverse](connect-dataverse-managed-lake.md).

   > [!NOTE]
   > Customer Insights-etik Sales-era segmentuak esportatzeak ez du kontaktu-erregistro berririk sortuko Sales-en instantzietan. Sales-en kontaktuen erregistroak Customer Insights-en sartu eta datu-iturburu gisa erabili behar dira. Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.

## <a name="known-limitations"></a>Muga ezagunak

Dynamics 365 Sales-era esportazioak 100.000ra mugatzen dira segmentu bakoitzeko, eta hori 3 ordu behar izan daiteke osatzeko.

## <a name="set-up-connection-to-sales"></a>Konfiguratu Salmentetarako konexioa

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Dynamics 365 Sales**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu erakundearen Salmentako URLa **Zerbitzariaren helbidea** eremu.

1. Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Sales kontua.

1. Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Dynamics 365 Sales sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Hautatu Dynamics 365 Kontaktu IDarekin bat datorren Bezeroaren entitatearen eremua.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
