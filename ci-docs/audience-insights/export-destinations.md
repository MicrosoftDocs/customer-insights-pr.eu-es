---
title: Esportatu datuak Customer Insights-etik
description: Kudeatu esportazioak datuak partekatzeko.
ms.date: 03/25/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: c1078ed0ba259a6e9cde3c7ede3570890ae48e67
ms.sourcegitcommit: 33a8e21b3bf6521bdb8346f81f79fce88091ddfd
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/10/2021
ms.locfileid: "6016599"
---
# <a name="exports-preview-overview"></a>Esportazioak (aurreargitalpena) ikuspegi orokorra

**Esportazioak** orrialdeak konfiguratutako esportazio guztiak erakusten ditu. Esportazioek datu zehatzak partekatzen dituzte hainbat aplikaziorekin. Bezeroen profilak edo entitateak, eskemak eta mapen xehetasunak sar ditzakete. Esportazio bakoitzak [konexioa, administratzaile batek konfiguratuta, autentifikazioa eta sarbidea kudeatzeko](connections.md).

Joan **Datuak** > **Esportazioak** esportazioen orria ikusteko. Erabiltzaile rol guztiek konfiguratutako esportazioak ikusteko sarbidea dute. Komando-barrako bilaketa-eremua erabiltzea esportazioak haien izenaren, konexioaren izenaren edo konexio motaren arabera aurkitzeko.

## <a name="set-up-a-new-export"></a>Konfiguratu esportazio berria

Esportazioa konfiguratzeko edo editatzeko, konexioak eskuragarri izan behar dituzu. Konexioak zure araberakoak dira [erabiltzailearen rola](permissions.md):
- Administratzaileek konexio guztietarako sarbidea dute. Konexio berriak sor ditzakete esportazioa konfiguratzerakoan.
- Laguntzaileek konexio zehatzetarako sarbidea izan dezakete. Konexioak konfiguratzeko eta partekatzeko administratzaileen mende daude. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).
- Ikusleek lehendik dauden esportazioak soilik ikus ditzakete baina ez dituzte sortu.

1. Joan **Datuak** > **Esportazioak**.

1. Aukeratu **Gehitu esportazioa** esportazio helmuga berria sortzeko.

1. Hurrengoan **Konfiguratu esportazioa** panelean, hautatu zein konexio erabili. [Konexioak](connections.md) administratzaileek kudeatzen dituzte. 

1. Eman beharrezko xehetasunak eta hautatu **Gorde** esportazioa sortzeko.

### <a name="edit-an-export"></a>Editatu esportazio bat

1. Hautatu elipsi bertikala editatu nahi duzun Export helmugarako.

1. Hautatu **Editatu** goitibeherako menutik.

1. Aldatu eguneratu nahi dituzun balioak eta hautatu **Gorde**.

## <a name="view-exports-and-export-details"></a>Ikusi esportazioak eta esportazioen xehetasunak

Esportazio helmugak sortu ondoren, hemen agertzen dira **Datuak** > **Esportazioak**. Erabiltzaile guztiek ikus dezakete zein datu partekatzen diren eta horien azken egoera.

1. Joan **Datuak** > **Esportazioak**.

1. Editatzeko baimenik ez duten erabiltzaileak hautatzen dituzte **Ikusi** ordez **Editatu** ikusi esportazio xehetasunak.

1. Alboko panel honek esportazio honen konfigurazioa erakusten du. Editatzeko baimenik gabe ezin dituzu balioak aldatu. Aukeratu **Itxi** esportazioen orrira itzultzeko.

## <a name="run-exports-on-demand"></a>Exekutatu esportazioak eskatu ahala

Esportazio bat konfiguratu ondoren, guztietan exekutatuko da [freskatze programatua](system.md#schedule-tab) betiere lan konexioa badu.

Datuak esportatzeko programatutako freskapenaren zain egon gabe, joan hona: **Datuak** > **Esportazioak**. Bi aukera dituzu:

- Esportazio guztiak exekutatzeko, hautatu **Exekutatu guztiak** komando barran. 
- Esportazio bakarra exekutatzeko, hautatu elipsia (...) zerrendako elementu batean eta ondoren aukeratu **Exekutatu**.

## <a name="remove-an-export"></a>Ezabatu Esportatu

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu elipsi bertikala kendu nahi duzun Esportaziorako.

1. Hautatu **Kendu** goitibeherako menuan.

1. Baieztatu kentzea aukeratuz **Kendu** berrespen-pantailan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
