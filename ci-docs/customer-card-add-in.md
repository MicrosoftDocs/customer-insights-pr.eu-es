---
title: Dynamics 365 aplikazioetarako Bezero txartelaren gehigarria (bideoa dauka)
description: Erakutsi Dynamics 365 aplikazioetan Customer Insights-en bezero-profilaren datuak gehigarri honekin.
ms.date: 02/02/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: Nils-2m
ms.author: nikeller
manager: shellyha
searchScope:
- ci-customers-page
- ci-search-filter
- ci-customer-card
- customerInsights
ms.openlocfilehash: 2dfa6c643cbe9a8531a085d8ce01b0f64776476f
ms.sourcegitcommit: b7dbcd5627c2ebfbcfe65589991c159ba290d377
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/27/2022
ms.locfileid: "8642010"
---
# <a name="customer-card-add-in-preview"></a>Bezeroaren txartelaren osagarria (aurrebista)



Lortu zure bezeroen 360 graduko ikuspegia zuzenean Dynamics 365 aplikazioetan. Bezeroaren txartelaren gehigarria onartutako Dynamics 365 aplikazio batean instalatuta baduzu, bezeroaren profileko eremuak, estatistikak eta jardueren kronograma bistaratzea aukera dezakezu. Gehigarriak Customer Insights-etik datuak berreskuratuko ditu konektatutako Dynamics 365 aplikazioko datuak eragin gabe.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWN1qv]

## <a name="prerequisites"></a>Aurrebaldintzak

- Gehigarriak Dynamics 365 ereduak gidatutako aplikazioekin soilik funtzionatzen du, hala nola Sales edo bezeroarentzako arreta-zerbitzu, 9.0 bertsioa eta berriagoak.
- Dynamics 365 datuak Customer Insights bezeroen profiletara mapatzeko, gomendatzen dugu [Dynamics 365 aplikaziotik irentsita Microsoft Dataverse konektorea](connect-power-query.md). Dynamics 365 kontaktuak (edo kontuak) irensteko beste metodo bat erabiltzen baduzu, ziurtatu behar duzu`contactid` (edo`accountid`) eremua gisa ezartzen da [datu-iturburu horren lehen gakoa datuak bateratzeko prozesuaren mapa-urratsean](map-entities.md#select-primary-key-and-semantic-type-for-attributes). 
- Bezero txartelaren gehigarriaren Dynamics 365 erabiltzaile guztiek izan behar dute [erabiltzaile gisa gehituta](permissions.md) Customer Insights-en datuak ikusteko.
- [Bilaketa eta iragazketa gaitasunak konfiguratuta](search-filter-index.md) Customer Insights-en beharrezkoak dira datuen bilaketak funtziona dezan.
- Gehigarri-kontrol bakoitza Customer Insights-eko datu zehatzetan oinarritzen da. Datu eta kontrol batzuk mota jakin batzuetako inguruneetan soilik daude eskuragarri. Gehigarrien konfigurazioak hautatutako ingurune mota dela eta kontrolik eskuragarri ez dagoen jakinaraziko dizu. Ikasi gehiago hurrengoari buruz [ingurunearen erabilera-kasuak](work-with-business-accounts.md).
  - **Neurriaren kontrola**: Beharrezkoa da [konfiguratutako neurriak](measures.md) bezeroaren atributu mota.
  - **Inteligentzia kontrola** : Erabiliz sortutako datuak eskatzen ditu [iragarpenak edo eredu pertsonalizatuak](predictions-overview.md).
  - **Bezeroen xehetasunak kontrolatzea**: Profileko eremu guztiak eskuragarri daude bezeroaren profil bateratuan.
  - **Aberastearen kontrola**: eskatzen du aktiboa [hobekuntzak](enrichment-hub.md) aplikatuta bezeroaren profiletara. Txartelaren gehigarriak aberastasun hauek onartzen ditu: [Markak](enrichment-microsoft.md) Microsoft-ek emandakoa, [Interesak](enrichment-microsoft.md) Microsoft-ek emandakoa, eta [Bulegoko konpromiso-datuak](enrichment-office.md) Microsoft-ek emandakoa.
  - **Kontaktuen kontrola**: Motako kontaktuen entitate semantikoaren definizioa eskatzen du.
  - **Kronologiaren kontrola**: eskatzen du [konfiguratutako jarduerak](activities.md).

## <a name="install-the-customer-card-add-in"></a>Instalatu Bezeroaren txartelaren osagarria

Bezeroaren Txartelaren Gehigarria Dynamics 365-en customer engagement aplikazioetarako irtenbidea da. Konponbidea instalatzeko, joan AppSource eta bilatu **Bezero txartel dinamikoa**. Hautatu [Bezero txartela AppSource-n](https://appsource.microsoft.com/product/dynamics-365/mscrm.dynamics_365_customer_insights_customer_card_addin?tab=Overview) eta hautatu **Eskuratu orain**.

Baliteke Dynamics 365 aplikaziorako zure administratzaileekin saioa hasi behar duzula irtenbidea instalatzeko. Zenbait denbora behar izango duzu irtenbidea zure ingurunean instalatzeko.

## <a name="configure-the-customer-card-add-in"></a>Konfiguratu Bezeroaren Kartaren Gehigarria

1. Administratzaile gisa, zoaz webgunera **ezarpenak** atala Dynamics 365-en, eta hautatu **Soluzioak**.

1. Hautatu botoia **Bistaratu izena** esteka **Dynamics 365 Customer Insights Bezero-txartelaren gehigarria (aurrebista)** konponbidea.

   > [!div class="mx-imgBorder"]
   > ![Hautatu Proiektuaren bistaratze-izena.](media/select-display-name.png "Hautatu Proiektuaren bistaratze-izena.")

1. Aukeratu **saioa hasi** eta sartu Customer Insights konfiguratzeko erabiltzen duzun kudeatzaileko kontuaren kredentzialak.

   > [!NOTE]
   > Egiaztatu arakatzailearen pop-up blokeatzaileak autentikazio-leihoa ez duela blokeatzen **Hasi saioa** botoia.

1. Hautatu datuak eskuratu nahi dituzun Customer Insights ingurunea.

1. Zehaztu Dynamics 365 aplikazioko erregistroen eremuen mapak. Customer Insights-en dituzun datuen arabera, aukera hauek esleitzea aukeratu dezakezu:
   - Kontaktu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontaktuaren entitatea.
   - Kontu batekin esleitzeko, hautatu Bezeroaren entitateko IDarekin bat datorren kontuaren entitatea.

   > [!div class="mx-imgBorder"]
   > ![Kontaktuaren IDaren eremua.](media/contact-id-field.png "Kontaktuaren IDaren eremua.")

1. Hautatu **Gorde konfigurazioa** gutxieneko balioaren ezarpenak gordetzeko.

1. Ondoren, Dynamics 365-en segurtasun rolak esleitu behar dituzu erabiltzaileek bezeroaren txartela pertsonalizatu eta ikusteko aukera izan dezaten. Dynamics 365-en, joan **Ezarpenak** > **Segurtasuna** > **Erabiltzaileak** aukerara. Hautatu erabiltzaileak rolak editatzeko eta hautatu **Rolak kudeatu**.

1. Esleitu **Customer Insights txartela pertsonalizatzailea** eginkizuna erakunde osoarentzako txartelean erakutsitako edukia pertsonalizatuko duten erabiltzaileentzat.

## <a name="add-customer-card-controls-to-forms"></a>Gehitu bezeroaren txartelaren kontrola inprimakietan

Zure agertokiaren arabera, kontroletara gehitzea aukera dezakezu **Harremanetarako** inprimakia edo **Kontua** forma. Zure Customer Insights ingurunea negozio-kontuetarako bada, kontrolak Kontuaren inprimakian gehitzea gomendatzen dugu. Kasu horretan, ordeztu "kontaktua" beheko urratsetan "kontua."

1. Bezero-txartelaren kontrolak zure Kontaktu inprimakian gehitzeko, joan **ezarpenak** > **pertsonalizazioak** Dynamics 365-en.

1. Hautatu **Pertsonalizatu sistema**.

1. Arakatu **Harremanetarako** entitatera, zabaldu menua eta ondoren hautatu **Inprimakiak**.

1. Aukeratu Bezeroaren Txartelak kontrolak gehitu nahi dituzun harremanetarako formularioa.

    > [!div class="mx-imgBorder"]
    > ![Hautatu Kontaktuaren inprimakia.](media/contact-active-forms.png "Hautatu Kontaktuaren inprimakia.")

1. Kontrola gehitzeko, inprimaki-editore-en, arrastatu edozein eremu **Eremu-esploradorea**-etik kontrolatu demografikoa nahi duzun lekura.

1. Hautatu gehitu berri duzun eremua inprimakian eta gero hautatu **Aldatu propietateak**.

1. Joan **Kontrolak** fitxara eta hautatu **Gehitu kontrola**. Aukeratu erabilgarri dauden kontroletako bat eta hautatu **Gehitu**.

1. Sarbidean **Eremuaren propietateak** elkarrizketa-koadroa, garbitu **Erakutsi etiketa inprimakian** kontrol-laukia.

1. Hautatu **Web** aukera kontrolerako. Aberastasunaren kontrolerako, hautatu zein aberastasun mota erakutsi nahi duzun **enrichmentType** eremu. Gehitu aberaste kontrol bereizi bat aberaste mota bakoitzerako.

1. Aukeratu **Gorde** eta **Argitaratu** kontaktu formulario eguneratua argitaratzeko.

1. Joan argitaratutako harremanetarako formulariora. Gehitu berri den kontrola ikusiko duzu. Baliteke erabiltzen duzun lehen aldian saioa hastea.

1. Kontrol pertsonalizatuan erakutsi nahi duzuna pertsonalizatzeko, hautatu editatzeko botoia goiko eskuineko izkinan.

## <a name="upgrade-customer-card-add-in"></a>Eguneratu Bezeroaren txartelaren osagarria

Bezeroaren txartelaren gehigarria ez da automatikoki eguneratzen. Azken bertsiora eguneratzeko, jarraitu urrats hauek gehigarria instalatuta duen Dynamics 365 aplikazioan.

1. Dynamics 365 aplikazioan, joan hona: **Ezarpenak** > **Pertsonalizazioa** eta hautatu **Irtenbideak**.

1. Gehigarrien taulan bilatu **CustomerInsightsCustomerCard** eta hautatu errenkada.

1. Aukeratu **Aplikatu irtenbidea berritzea** ekintza barran.

   :::image type="content" source="media/customer-card-add-in-upgrade.png" alt-text="Eguneratu irtenbidea Dynamics 365 aplikazioen Pertsonalizazio eremuan.":::

1. Bertsio-berritze prozesua hasi ondoren, kargatzeko adierazle bat ikusiko duzu bertsio berritzea amaitu arte. Bertsio berririk ez badago, bertsio berritzeak errore mezu bat erakutsiko du.

## <a name="troubleshooting"></a>Arazoak konpontzea

### <a name="controls-from-customer-card-add-in-dont-find-data"></a>Bezero Txartelaren Gehigarriko kontrolek ez dute daturik aurkitzen

**Arazoa:**

Nahiz eta behar bezala konfiguratutako ID eremuak, kontrolek ezin dute inolako bezeroren daturik aurkitu.  

**Ebazpena:**

1. Ziurtatu Txartelaren gehigarria argibideen arabera konfiguratu duzula: [Konfiguratu Bezero Txartelaren gehigarria](#configure-the-customer-card-add-in) 

1. Berrikusi datuak sartzeko konfigurazioa. Editatu kontaktuaren ID GUIDa duen Dynamics 365 sistemarako datu-iturburu. Kontaktuaren ID GUID letra larriz agertzen bada Power Query editorea, saiatu honako hau: 
    1. Editatu datu-iturburu datu-iturburu hemen irekitzeko Power Query Editorea.
    1. Hautatu kontaktuaren ID zutabea.
    1. Hautatu **Eraldatu** goiburuko barran erabilgarri dauden ekintzak ikusteko.
    1. Hautatu **minuskula**. Baliozkotu taulako GUIDak letra xeheak badira.
    1. Gorde datu-iturburua.
    1. Exekutatu datuak sartzea, bateratzea eta beheranzko prozesuak aldaketak GUIDera hedatzeko. 

Freskatze osoa amaitu ondoren, Bezero Txartelaren gehigarrien kontrolak espero diren datuak erakutsi beharko lituzke. 

[!INCLUDE [footer-include](includes/footer-banner.md)]
