---
title: Instalatu eta konfiguratu Bezeroaren txartelaren osagarria
description: Instalatu eta konfiguratu Dynamics 365 Customer Insights-erako Bezeroen txartelaren osagarria.
ms.date: 01/20/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: f3c4a01f9ce7749eeee72f7901620dae7cb9b8d3
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5597312"
---
# <a name="customer-card-add-in-preview"></a>Bezeroaren txartelaren osagarria (aurrebista)

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Lortu zure bezeroen 360 graduko ikuspegia zuzenean Dynamics 365 aplikazioetan. Ikusi demografia, xehetasunak eta jarduera-denborak Bezero-txartelaren gehigarrian.

## <a name="prerequisites"></a>Aurrebaldintzak

- Dynamics 365 aplikazioa (Salmenten atala edo bezeroarentzako arreta-zerbitzu Hub adibidez), 9.0 bertsioa eta ondoren Interfaze bateratu gaituta.
- [Common Data Service erabiliz Dynamics 365 aplikaziotik sartutako](connect-power-query.md) bezeroen profilak.
- Bezeroaren txartelaren osagarriaren erabiltzaileak [erabiltzaile gisa gehitu behar dira](permissions.md) hartzaileen xehetasunetan.
- [Bilaketa konfiguratua eta iragazkiaren gaitasunak](search-filter-index.md).
- Kontrol demografikoa: eremu demografikoak (adina edo generoa), adibidez, bezeroen profil bateratuan daude eskuragarri.
- Aberastearen kontrola: Aktiboa eskatzen du [hobekuntzak](enrichment-hub.md) bezeroen profiletan aplikatuta.
- Adimenaren kontrola: Azure Machine Learning ([iragarpenak](predictions.md) edo [eredu pertsonalizatuak](custom-models.md)) erabiliz sortutako datuak behar dira
- Neurriaren kontrola: [Konfiguratutako neurriak](measures.md) behar dira.
- Kronogramaren kontrola: [konfiguratutako jarduerak](activities.md) behar dira.

## <a name="install-the-customer-card-add-in"></a>Instalatu Bezeroaren txartelaren osagarria

Bezeroaren Txartelaren Gehigarria Dynamics 365-en customer engagement aplikazioetarako irtenbidea da. Konponbidea instalatzeko, joan AppSource eta bilatu **Bezero txartel dinamikoa**. Hautatu [Bezero txartela AppSource-n](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics_365_customer_insights_customer_card_addin?tab=Overview) eta hautatu **Eskuratu orain**.

Baliteke Dynamics 365 aplikaziorako zure administratzaileekin saioa hasi behar duzula irtenbidea instalatzeko.

Zenbait denbora behar izango duzu irtenbidea zure ingurunean instalatzeko.

## <a name="configure-the-customer-card-add-in"></a>Konfiguratu Bezeroaren Kartaren Gehigarria

1. Administratzaile gisa, zoaz webgunera **ezarpenak** atala Dynamics 365-en, eta hautatu **Soluzioak**.

1. Hautatu botoia **Bistaratu izena** esteka **Dynamics 365 Customer Insights Bezero-txartelaren gehigarria (aurrebista)** konponbidea.

   > [!div class="mx-imgBorder"]
   > ![Hautatu Proiektuaren bistaratze-izena](media/select-display-name.png "Hautatu Proiektuaren bistaratze-izena")

1. Aukeratu **saioa hasi** eta sartu Customer Insights konfiguratzeko erabiltzen duzun kudeatzaileko kontuaren kredentzialak.

   > [!NOTE]
   > Egiaztatu arakatzailearen pop-up blokeatzaileak autentikazio-leihoa ez duela blokeatzen **Hasi saioa** botoia.

1. Hautatu datuak eskuratu nahi dituzun ingurunea.

1. Zehaztu zein eremu esleituko zaion Dynamics 365 aplikazioko erregistroari.
   - Kontaktu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontaktuaren entitatea.
   - Kontu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontuaren entitatea.

   > [!div class="mx-imgBorder"]
   > ![Kontaktuaren IDaren eremua](media/contact-id-field.png "Kontaktuaren IDaren eremua")

1. Hautatu **Gorde konfigurazioa** gutxieneko balioaren ezarpenak gordetzeko.

1. Ondoren, Dynamics 365-en segurtasun rolak esleitu behar dituzu erabiltzaileek bezeroaren txartela pertsonalizatu eta ikusteko aukera izan dezaten. Dynamics 365-en, joan **Ezarpenak** > **Segurtasuna** > **Erabiltzaileak** aukerara. Hautatu erabiltzaileak rolak editatzeko eta hautatu **Rolak kudeatu**.

1. Esleitu **Customer Insights txartela pertsonalizatzailea** eginkizuna erakunde osoarentzako txartelean erakutsitako edukia pertsonalizatuko duten erabiltzaileentzat.

## <a name="add-customer-card-controls-to-forms"></a>Gehitu bezeroaren txartelaren kontrola inprimakietan
  
1. Bezero-txartelaren kontrolak zure Kontaktu inprimakian gehitzeko, joan **ezarpenak** > **pertsonalizazioak** Dynamics 365-en.

1. Hautatu **Pertsonalizatu sistema**.

1. Arakatu **Harremanetarako** entitatera, zabaldu menua eta ondoren hautatu **Inprimakiak**.

1. Aukeratu Bezeroaren Txartelak kontrolak gehitu nahi dituzun harremanetarako formularioa.

    > [!div class="mx-imgBorder"]
    > ![Hautatu Kontaktuaren inprimakia](media/contact-active-forms.png "Hautatu Kontaktuaren inprimakia")

1. Kontrola gehitzeko, inprimaki-editore-en, arrastatu edozein eremu **Eremu-esploradorea**-etik kontrolatu demografikoa nahi duzun lekura.

1. Hautatu gehitu berri duzun eremua inprimakian eta gero hautatu **Aldatu propietateak**.

1. Joan **Kontrolak** fitxara eta hautatu **Gehitu kontrola**. Aukeratu erabilgarri dauden kontroletako bat eta hautatu **Gehitu**.

1. Sarbidean **Eremuaren propietateak** elkarrizketa-koadroa, garbitu **Erakutsi etiketa inprimakian** kontrol-laukia.

1. Hautatu **Web** aukera kontrolerako. Aberastasunaren kontrolerako, hautatu zein aberastasun mota erakutsi nahi duzun **enrichmentType** eremu. Gehitu aberaste kontrol bereizi bat aberaste mota bakoitzerako.

1. Aukeratu **Gorde** eta **Argitaratu** kontaktu formulario eguneratua argitaratzeko.

1. Joan argitaratutako harremanetarako formulariora. Gehitu berri den kontrola ikusiko duzu. Baliteke erabiltzen duzun lehen aldian saioa hastea.

1. Kontrol pertsonalizatuan erakutsi nahi duzuna pertsonalizatzeko, hautatu editatzeko botoia goiko eskuineko izkinan.

## <a name="upgrade-customer-card-add-in"></a>Eguneratu Bezeroaren txartelaren osagarria
Bezeroaren txartelaren gehigarria ez da automatikoki eguneratzen. Azken bertsiora eguneratzeko, jarraitu prozedura hau gehigarria instalatuta duen Dynamics 365 aplikazioan.

1. Dynamics 365 aplikazioan, joan hona: **Ezarpenak** > **Pertsonalizazioa** eta hautatu **Irtenbideak**.

1. Gehigarrien taulan bilatu **CustomerInsightsCustomerCard** eta hautatu errenkada.

1. Aukeratu **Aplikatu irtenbidea berritzea** ekintza barran.

   :::image type="content" source="media/customer-card-add-in-upgrade.png" alt-text="Eguneratu irtenbidea Dynamics 365 aplikazioen Pertsonalizazio eremuan":::

1. Bertsio-berritze prozesua hasi ondoren, kargatzeko adierazle bat ikusiko duzu bertsio berritzea amaitu arte. Bertsio berririk ez badago, bertsio berritzeak errore mezu bat erakutsiko du.


[!INCLUDE[footer-include](../includes/footer-banner.md)]