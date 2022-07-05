---
title: Esportatu segmentuak Dynamics 365 Sales-era (aurrebista)
description: Ikasi konexioa nola konfiguratu eta Dynamics 365 Sales-era esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
searchScope:
- ci-export
- customerInsights
ms.openlocfilehash: b8e756313ca037dca41cb25587229808f0c584c9
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9082379"
---
# <a name="export-segments-to-dynamics-365-sales-preview"></a>Esportatu segmentuak Dynamics 365 Sales-era (aurrebista)

Dynamics 365 Sales-ekin marketin-zerrendak sortzeko, lan-fluxuen segimendua egiteko eta eskaintzak bidaltzeko, erabili bezeroen datuak.

## <a name="known-limitations"></a>Muga ezagunak

- Dynamics 365 Sales-era esportazioak 100.000 kidera mugatzen dira segmentu bakoitzeko.
- Dynamics 365 Sales-era segmentuen esportazioak gehienez 3 ordu behar izan ditzake osatzeko. 

## <a name="prerequisite-for-connection"></a>Konexiorako aurrebaldintza

1. Kontaktu-erregistroek Dynamics 365 Sales-en egon behar dute segmentu bat Customer Insights-etik Sales-era esportatu ahal izateko. Irakurri gehiago kontaktuak nola irensteko [Dynamics 365 Sales erabiliz Microsoft Dataverse](connect-dataverse-managed-lake.md).

   > [!NOTE]
   > Customer Insights-etik Sales-era segmentuak esportatzeak ez du kontaktu-erregistro berririk sortuko Sales-en instantzietan. Sales-en kontaktuen erregistroak Customer Insights-en sartu eta datu-iturburu gisa erabili behar dira. Gainera, Bezeroen entitate bateratuan sartu behar dira bezeroen IDak esleitzeko IDak harremanetan jartzeko, segmentuak esportatu aurretik.

## <a name="set-up-the-connection-to-sales"></a>Konfiguratu konexioa Sales-era

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Dynamics 365 Sales** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Sartu erakundearen Salmentako URLa **Zerbitzariaren helbidea** eremu.

1. Sarbidean **Zerbitzariaren administratzaile kontua** atala aukeratu **saioa hasi** eta aukeratu Dynamics 365 Sales kontua.

1. Esleitu bezeroaren IDaren eremua Dynamics 365 kontaktuaren IDarekin.

1. Hautatu **Gorde** konexioa osatzeko. 

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa Dynamics 365 Sales sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Aukeratu segmentu bat edo gehiago.

1. Sakatu **Gorde**

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

[!INCLUDE [footer-include](includes/footer-banner.md)]
