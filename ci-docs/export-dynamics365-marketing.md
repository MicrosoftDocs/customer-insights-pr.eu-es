---
title: Esportatu segmentuak Dynamics 365 Marketing-era (aurrebista)
description: Ikasi konexioa konfiguratzen eta esportatzen Dynamics 365 Marketing-era.
ms.date: 08/24/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
searchScope:
- ci-export
- customerInsights
ms.openlocfilehash: fed4ae1b017cca2b6060c4dda155859cd77e0daf
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9054601"
---
# <a name="export-segments-to-dynamics-365-marketing-preview"></a>Esportatu segmentuak Dynamics 365 Marketing-era (aurrebista)

Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko. Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments).

Dynamics 365 Marketing-en gaitasun berriak erabiltzen ari bazara denbora errealean bezero-bidaia orkestraziorako Dataverse org, ez duzu Dynamics 365 Marketing-era esportazio estandarrik sortu behar. Customer Insights-eko kontaktuak eta segmentuak zuzenean eskuragarri daude Dynamics 365 Marketing-en Marketing eta Customer Insights konektatu ondoren. Lehendik dauden esportazioak ezabatu baino lehen, berrikusi hemen buruzko dokumentazioa [nola konektatu Customer Insights eta Dynamics 365 Marketing bezero-bidaia orkestrazioa](/dynamics365/marketing/real-time-marketing-ci-profile).

## <a name="prerequisite-for-a-connection"></a>Konexioaren aurrebaldintza

- Kontaktu-erregistroek Dynamics 365 Marketing-en egon behar dute segmentu bat Customer Insights-etik Marketing-era esportatu ahal izateko. Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Marketing erabiliz Microsoft Dataverse](connect-dataverse-managed-lake.md).

  > [!NOTE]
  > Customer Insights-etik Marketin-era segmentuak esportatzeak ez du kontaktu-erregistro berririk sortuko Marketing-en instantzietan. Marketing-eko kontaktuen erregistroak Customer Insights-en sartu eta datu-iturburu gisa erabili behar dira. Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.

## <a name="set-up-connection-to-marketing"></a>Konfiguratu konexioa Marketing-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Dynamics 365 Marketing** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu erakundearen Marketing URLa **Zerbitzariaren helbidea** eremu.

1. Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Marketing kontua.

1. Mapeatu Bezeroaren entitateko Contact ID eremua Dynamics 365 Contact ID-arekin.

1. Hautatu **Gorde** konexioa osatzeko. 

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Dynamics 365 Marketing sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Aukeratu segmentu bat edo gehiago.

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

[!INCLUDE [footer-include](includes/footer-banner.md)]
