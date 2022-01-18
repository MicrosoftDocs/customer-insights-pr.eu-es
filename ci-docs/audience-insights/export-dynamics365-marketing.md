---
title: Esportatu Customer Insights datuak Dynamics 365 Marketing-era
description: Ikasi konexioa konfiguratzen eta esportatzen Dynamics 365 Marketing-era.
ms.date: 08/24/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 2c673c432f308efa289625a159de608d07f8d2b3
ms.sourcegitcommit: f988114ac7a288ccadf2db35b02dbef5cacea4d9
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 01/14/2022
ms.locfileid: "7975109"
---
# <a name="use-segments-in-dynamics-365-marketing-preview"></a>Erabili segmentuak Dynamics 365 Marketing-en (aurrebista)

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Erabili [segmentuak](segments.md) Dynamics 365 Marketing-ekin kanpainak eta kontaktu-talde zehatzak sortzeko. Informazio gehiago lortzeko, ikus [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing](/dynamics365/marketing/customer-insights-segments).

Dynamics 365 Marketing-en gaitasun berriak erabiltzen ari bazara denbora errealean bezero-bidaia orkestraziorako Dataverse org, ez duzu Dynamics 365 Marketing-era esportazio estandarrik sortu behar. Audientzia estatistiketako kontaktuak eta segmentuak zuzenean eskuragarri daude Dynamics 365 Marketing-en Marketing eta Customer Insights konektatu ondoren. Lehendik dauden esportazioak ezabatu aurretik, berrikusi dokumentazioa hemen [nola konektatu ikuslearen estatistikak eta Dynamics 365 Marketing bezero-bidaia orkestrazioa](/dynamics365/marketing/real-time-marketing-ci-profile).

## <a name="prerequisite-for-a-connection"></a>Konexioaren aurrebaldintza

- Kontaktu-erregistroek Dynamics 365 Marketing-en egon behar dute segmentu bat Customer Insights-etik Marketing-era esportatu ahal izateko. Irakurri gehiago kontaktuak nola sartu [Dynamics 365 Marketing erabiliz Microsoft Dataverse](connect-power-query.md).

  > [!NOTE]
  > Ikuspegien estatistiketatik Marketing segmentuak esportatzeak ez du kontaktu erregistro berririk sortuko Marketing instantzietan. Marketing kontaktuen erregistroak ikusleen estatistiketan sartu behar dira eta datu-iturburu gisa erabili. Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
