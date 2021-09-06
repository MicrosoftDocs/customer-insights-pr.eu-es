---
title: Esportatu datuak Customer Insights-etik
description: Kudeatu esportazioak datuak partekatzeko.
ms.date: 06/14/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: be4d142e0f9f422cac459f603aa5dd8bb490321cfe1b2de58f4a128ae56f4ba3
ms.sourcegitcommit: aa0cfbf6240a9f560e3131bdec63e051a8786dd4
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2021
ms.locfileid: "7034667"
---
# <a name="exports-preview-overview"></a>Esportazioak (aurreargitalpena) ikuspegi orokorra

**Esportazioak** orrialdeak konfiguratutako esportazio guztiak erakusten ditu. Esportazioek datu zehatzak partekatzen dituzte hainbat aplikaziorekin. Bezeroen profilak edo entitateak, eskemak eta mapen xehetasunak sar ditzakete. Esportazio bakoitzak [konexioa, administratzaile batek konfiguratuta, autentifikazioa eta sarbidea kudeatzeko](connections.md).

Joan **Datuak** > **Esportazioak** esportazioen orria ikusteko. Erabiltzaile rol guztiek konfiguratutako esportazioak ikus ditzakete. Erabili komando-barrako bilaketa-eremua esportazioak haien izenaren, konexioaren izenaren edo konexio motaren arabera aurkitzeko.

## <a name="set-up-a-new-export"></a>Konfiguratu esportazio berria

Esportazioa konfiguratzeko edo editatzeko, konexioak eskuragarri izan behar dituzu. Konexioak zure araberakoak dira [erabiltzailearen rola](permissions.md):
- Administratzaileek konexio guztietarako sarbidea dute. Konexio berriak sor ditzakete esportazioa konfiguratzerakoan.
- Laguntzaileek konexio zehatzetarako sarbidea izan dezakete. Konexioak konfiguratzeko eta partekatzeko administratzaileen mende daude. Esportazioen zerrendan agertzen da laguntzaileek esportazio bat editatu edo soilik ikus dezaketen **Zure baimenak** zutabean. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).
- Ikusleek lehendik dauden esportazioak soilik ikus ditzakete baina ez dituzte sortu.

### <a name="define-a-new-export"></a>Definitu esportazio berria

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. Hurrengoan **Konfiguratu esportazioa** panelean, hautatu zein konexio erabili. [Konexioak](connections.md) administratzaileek kudeatzen dituzte. 

1. Eman beharrezko xehetasunak eta hautatu **Gorde** esportazioa sortzeko.

### <a name="define-a-new-export-based-on-an-existing-export"></a>Definitu esportazio berri bat lehendik dagoen esportazioan oinarrituta

1. Joan **Datuak** > **Esportazioak**.

1. Esportazioen zerrendan, hautatu bikoiztu nahi duzun esportazioa.

1. Aukeratu **Sortu bikoiztuak** komando barran **Konfiguratu esportazioa** panela irakitzeko, hautatutako esportazioaren xehetasunak dituena.

1. Berrikusi eta egokitu esportazioa eta hautatu **Gorde** esportazio berri bat sortzeko.

### <a name="edit-an-export"></a>Editatu esportazio bat

1. Joan **Datuak** > **Esportazioak**.

1. Esportazioen zerrendan, hautatu editatu nahi duzun esportazioa.

1. Komando-barran, hautatu **Editatu**.

1. Aldatu eguneratu nahi dituzun balioak eta hautatu **Gorde**.

## <a name="view-exports-and-export-details"></a>Ikusi esportazioak eta esportazioen xehetasunak

Esportazio helmugak sortu ondoren, hemen agertzen dira **Datuak** > **Esportazioak**. Erabiltzaile guztiek ikus dezakete zein datu partekatzen diren eta horien azken egoera.

1. Joan **Datuak** > **Esportazioak**.

1. Editatzeko baimenik ez duten erabiltzaileak hautatzen dituzte **Ikusi** ordez **Editatu** esportazio xehetasunak ikusteko.

1. Alboko panelak esportazio baten konfigurazioa erakusten du. Editatzeko baimenik gabe ezin dituzu balioak aldatu. Aukeratu **Itxi** esportazioen orrira itzultzeko.

## <a name="schedule-and-run-exports"></a>Antolatu eta exekutatu esportazioak

Konfiguratzen duzun esportazio bakoitzak freskatze ordutegia du. Freskatze batean, sistemak esportazio batean sartzeko datu berri edo eguneratuak bilatzen ditu. Berez, esportazioak [programatutako eguneratze sistema](system.md#schedule-tab) guztien zati gisa exekutatzen dira. Freskatze ordutegia pertsonaliza dezakezu edo desaktiba dezakezu esportazioak eskuz exekutatzeko.

Esportazio ordutegiak zure ingurunearen egoeraren araberakoak dira. Eguneratzeak martxan badaude aktibatuta [mendekotasunak](system.md#refresh-policies) programatutako esportazio bat hasi behar denean, sistemak eguneraketak osatuko ditu eta esportazioa exekutatuko du. Zutabean esportazio bat noiz freskatu zen azkeneko aldiz ikus dezakezu **Freskatuta** zutabean.

### <a name="schedule-exports"></a>Antolatu esportazioak

Banakako esportazioetarako edo hainbat esportaziorako freskatze ordutegi pertsonalizatuak defini ditzakezu aldi berean. Unean definitutako ordutegia esportazio zerrendako **Antolaketa** zutabean agertzen da. Ordutegia aldatzeko baimena berdina da [esportazioak editatu eta definitzeko](export-destinations.md#set-up-a-new-export). 

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu antolatu nahi duzun esportazioa.

1. Komando-barran, hautatu **Antolatu**.

1. **Programatu esportazioa** panelean, ezarri **Antolatu exekuzioa** aukera **Aktibatuta** gisa, esportazioa automatikoki exekutatzeko. Ezarri **Desaktibatuta** gisa eskuz freskatzeko.

1. Automatikoki freskatutako esportazioetarako, aukeratu **Errepikatzearen** balioa eta zehaztu horren xehetasunak. Definitutako denbora errepikatze-kasu guztiei aplikatzen zaie. Esportazio bat freskatzen hasi behar den unea da.

1. Aplikatu eta aktibatu aldaketak **Gorde** hautatuta.

Hainbat esportazioen antolaketa editatzerakoan, aukeraketa bat egin behar duzu **Antolaketak gorde edo gainidatzi** atalean:
- **Mantendu antolaketa indibidualak**: Aurretik definitutako antolaketari eutsi hautatutako esportazioetarako eta desgaitu edo gaitu bakarrik.
- **Zehaztu hautatutako esportazio guztientzako antolaketa berria**: Gainidatzi hautatutako esportazioen dauden antolaketak.

### <a name="run-exports-on-demand"></a>Exekutatu esportazioak eskatu ahala

Datuak esportatzeko programatutako freskapenaren zain egon gabe, joan hona: **Datuak** > **Esportazioak**.

- Esportazio guztiak exekutatzeko, hautatu **Exekutatu guztiak** komando barran. Ekintza honek antolaketa aktiboa duten esportazioak soilik exekutatuko ditu.
- Esportazio bakarra exekutatzeko, hautatu zerrendatik eta hautatu **Exekutatu** komando barran. Horrela exekutatzen dira antolaketa aktiborik gabeko esportazioak. 

## <a name="remove-an-export"></a>Ezabatu Esportatu

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu kendu nahi duzun esportazioa.

1. Komando-barran, sakatu **Kendu**.

1. Baieztatu kentzea aukeratuz **Kendu** berrespen-pantailan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
