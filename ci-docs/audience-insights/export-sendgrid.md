---
title: Esportatu Customer Insights datuak SendGrid-era
description: Ikasi SendGrid-erako konexioa nola konfiguratu.
ms.date: 12/08/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: phkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 1a1f679fa42d47d524ebfdd6e931ae2822565f77
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597266"
---
# <a name="connector-for-sendgrid-preview"></a>SendGrid-eko konektorea (aurrebista)

Esportatu bezeroen profil bateratuen segmentuak SendGrid kontaktu zerrendetara eta erabili kanpainak eta posta elektronikoa merkaturatzeko SendGrid-en. 

## <a name="prerequisites"></a>Aurrebaldintzak

-   Baduzu [SendGrid kontua](https://sendgrid.com/) eta dagozkion administratzaile kredentzialak.
-   SendGrid-en kontaktu-zerrendak eta dagozkien IDak daude. Informazio gehiagorako, ikus [SendGrid: kudeatu kontaktuak](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts).
-   Badituzu [konfiguratutako segmentuak](segments.md) hartzaileei buruzko xehetasunetan.
-   Esportatutako segmentuetako bezeroen profil bateratuek helbide elektronikoa adierazten duen eremua dute.

## <a name="connect-to-sendgrid"></a>Konektatu SendGrid-era

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. **SendGrid** atalean hautatu **Konfiguratu**.

1. Eman zure esportatze-helmugari izen bat **Bistaratu izena** eremuan.

   :::image type="content" source="media/export-sendgrid.PNG" alt-text="SendGrid esportazio konfigurazio panela.":::

1. Sartu zure **SendGrid API gakoa** [SendGrid API gakoa](https://sendgrid.com/docs/ui/account-and-settings/api-keys/).

1. Sartu zure **[SendGrid zerrendaren IDa](https://sendgrid.com/docs/ui/managing-contacts/create-and-manage-contacts/#manage-contacts)**.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **Konektatu** SendGrid-eko konexioa hasieratzeko.

1. Aukeratu **Gehitu zeure burua esportazio erabiltzaile gisa** eta eman zure Customer Insights kredentzialak.

1. Aukeratu **hurrengoa** esportazioa konfiguratzeko.

## <a name="configure-the-connector"></a>Konfiguratu konektorea

1. **Datuen bat etortzea** atalean, **Posta elektronikoa** eremuan, hautatu zure bezeroaren profil bateratuko eremua, bezero baten helbide elektronikoa adierazten duena. Errepikatu urrats berak aukerako beste eremu batzuetarako, esaterako **izena**, **abizena**, **herrialdea/eskualdea**, **estatua**, **hiria** eta **posta kodea**.

1. Hautatu esportatu nahi dituzun segmentuak. Biziki **gomendatzen dugu 100.000 bezero profil baino gehiago ez esportatzea guztira** SendGrid-era. 

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).

## <a name="known-limitations"></a>Muga ezagunak

- Gehienez 100.000 profil guztira SendGrid-era.
- SendGrid-era esportatzea segmentuetara mugatuta dago.
- SendGrid-era 100.000 profil gehienera esportatzeak ordu batzuk behar izan ditzake osatzeko. 
- SendGrid-era esporta ditzakezun profilen kopurua SendGrid-ekin duzun kontratuaren menpe dago eta mugatua da.

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak SendGrid-era bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da SendGrid-ek pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.


[!INCLUDE[footer-include](../includes/footer-banner.md)]