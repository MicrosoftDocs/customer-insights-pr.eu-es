---
title: Esportatu segmentuak Dynamics 365 Marketing-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Dynamics 365 Marketing-era.
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
ms.openlocfilehash: 123b565421a7d096e7341a8f600f91e59aefe8d0
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9196609"
---
# <a name="export-segments-to-dynamics-365-marketing-preview"></a>Esportatu segmentuak Dynamics 365 Marketing-era (aurrebista)

Erabili [segmentuak](segments.md) kanpainak sortzeko eta bezero talde zehatz batzuekin harremanetan jartzeko [Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments).

Dynamics 365 Marketing-en gaitasun berriak erabiltzen ari bazara denbora errealean bezero-bidaia orkestraziorako Dataverse org, ez duzu Dynamics 365 Marketing-era esportazio estandarrik sortu behar. Customer Insights-eko kontaktuak eta segmentuak zuzenean eskuragarri daude Dynamics 365 Marketing-en Marketing eta Customer Insights konektatu ondoren. Lehendik dauden esportazioak ezabatu baino lehen, berrikusi hemen buruzko dokumentazioa [nola konektatu Customer Insights eta Dynamics 365 Marketing bezero-bidaia orkestrazioa](/dynamics365/marketing/real-time-marketing-ci-profile).

## <a name="prerequisite"></a>Aurrebaldintza

Kontaktu-erregistroek Dynamics 365 Marketing-en egon behar dute segmentu bat Customer Insights-etik Marketing-era esportatu ahal izateko. Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Marketing erabiliz Microsoft Dataverse](connect-dataverse-managed-lake.md).

> [!NOTE]
> Customer Insights-etik Marketin-era segmentuak esportatzeak ez du kontaktu-erregistro berririk sortuko Marketing-en instantzietan. Marketing-eko kontaktuen erregistroak Customer Insights-en sartu eta datu-iturburu gisa erabili behar dira. Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.

## <a name="set-up-connection-to-marketing"></a>Konfiguratu konexioa Marketing-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Dynamics 365 Marketing**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu erakundearen Marketing URLa **Zerbitzariaren helbidea** eremu.

1. Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Marketing kontua.

1. Mapeatu Bezeroaren entitateko Contact ID eremua Dynamics 365 Contact ID-arekin.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Dynamics 365 Marketing sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Hautatu Dynamics 365 Kontaktu IDarekin bat datorren Bezeroaren entitatearen eremua.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

[!INCLUDE [footer-include](includes/footer-banner.md)]
