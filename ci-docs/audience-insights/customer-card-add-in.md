---
title: Dynamics 365 aplikazioetarako bezeroaren txartelaren osagarria
description: Erakutsi audientzia estatistiken datuak Dynamics 365 aplikazioetan gehigarri honekin.
ms.date: 05/18/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 88492943ddbf9ae30c64d92b261433b74f34f682
ms.sourcegitcommit: d74430270f1b754322287c4f045d7febdae35be2
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059573"
---
# <a name="customer-card-add-in-preview"></a>Bezeroaren txartelaren osagarria (aurrebista)

[!INCLUDE [cc-data-platform-banner](../includes/cc-data-platform-banner.md)]

Lortu zure bezeroen 360 graduko ikuspegia zuzenean Dynamics 365 aplikazioetan. Bezeroaren txartelaren gehigarria onartutako Dynamics 365 aplikazio batean instalatuta dagoenez, demografia, estatistikak eta jardueren kronogramak bistaratzea aukera dezakezu. Gehigarriak Customer Insights-etik datuak berreskuratuko ditu konektatutako Dynamics 365 aplikazioko datuak eragin gabe. 

## <a name="prerequisites"></a>Aurrebaldintzak

- Gehigarriak Dynamics 365 ereduak gidatutako aplikazioekin soilik funtzionatzen du, hala nola Sales edo bezeroarentzako arreta-zerbitzu, 9.0 bertsioa eta berriagoak.
- Zure Dynamics 365 datuak ikusleekin esleitu ahal izateko izan behar dituzten bezeroen profilak [Dynamics 365 aplikaziotik gehituta Common Data Service konektorea](connect-power-query.md).
- Bezero txartelaren gehigarriaren Dynamics 365 erabiltzaile guztiek izan behar dute [erabiltzaile gisa gehitu da](permissions.md) datuak ikusteko ikusleei buruzko informazioetan.
- [Bilaketa eta iragazki gaitasunak konfiguratuta](search-filter-index.md) audientziari buruzko datuetan funtzionatu behar da.
- Gehigarrien kontrol bakoitza datu zehatzetan oinarritzen da ikusleen estatistiketan:
  - Neurriaren kontrola: [Konfiguratutako neurriak](measures.md) behar dira.
  - Adimenaren kontrola: erabiliz sortutako datuak eskatzen ditu [iragarpenak](predictions.md) edo [eredu pertsonalizatuak](custom-models.md).
  - Kontrol demografikoa: eremu demografikoak (adina edo generoa), adibidez, bezeroen profil bateratuan daude eskuragarri.
  - Aberastearen kontrola: Aktiboa eskatzen du [hobekuntzak](enrichment-hub.md) bezeroen profiletan aplikatuta.
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

1. Hautatu datuak eskuratu nahi dituzun Customer Insights ingurunea.

1. Zehaztu Dynamics 365 aplikazioko erregistroen eremuen mapak. Customer Insights-en dituzun datuen arabera, aukera hauek esleitzea aukeratu dezakezu:
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
