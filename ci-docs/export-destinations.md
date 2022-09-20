---
title: Esportazioak (aurreargitalpena) ikuspegi orokorra
description: Kudeatu esportazioak datuak partekatzeko.
ms.date: 08/12/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: overview
author: pkieffer
ms.author: philk
manager: shellyha
searchScope:
- ci-export
- ci-connections
- customerInsights
ms.openlocfilehash: 44f58d694b9bd35a8d8c04d487d40743291e0566
ms.sourcegitcommit: ef3e17134d44d2731605381ea0385dbc5aef6120
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460175"
---
# <a name="exports-preview-overview"></a>Esportazioak (aurreargitalpena) ikuspegi orokorra

 Esportazioek datu zehatzak hainbat aplikaziorekin partekatzeko aukera ematen dute. Bezeroen profilak, entitateak, eskemak eta mapen xehetasunak sar ditzakete. Esportazio bakoitzak [konexioa, administratzaile batek konfiguratuta, autentifikazioa eta sarbidea kudeatzeko](connections.md). **Esportazioak** orrialdeak konfiguratutako esportazio guztiak erakusten ditu.

## <a name="export-types"></a>Esportatze-motak

Bi esportazio mota nagusi daude:  

- **Datuak ateratzeko esportazioak** Customer Insights-en erabilgarri dagoen edozein motatako entitateak esportatzeko aukera ematen dizu. Esportatzeko hautatzen dituzun entitateak datu-eremu, metadatu, eskema eta mapping xehetasun guztiekin esportatzen dira.
- **Segmentu esportazioak** Customer Insights-etik segmentu-entitateak esportatzeko aukera ematen dizu. Banakako kontsumitzaileentzat (B-to-C), segmentuek bezeroen profilen zerrenda adierazten dute. Enpresentzat (B-to-B), [segmentuek kontu edo kontaktuen zerrenda irudika dezakete](segment-builder.md#create-a-new-segment-with-segment-builder). Esportazioa konfiguratzean, sartutako datu-eremuak hautatzen dituzu, datuak esportatzen ari zaren helburu-sistemaren arabera.

### <a name="export-segments"></a>Esportatu segmentuak

**Segmentuak esportatzea negozio kontuetarako (B-to-B) edo kontsumitzaile partikularretarako (B-to-C) inguruneetan**  
Esportazio-aukera gehienek bi ingurune mota onartzen dituzte. Segmentuak helburu-sistema ezberdinetara esportatzeak baldintza zehatzak ditu. 

**Banakako kontsumitzaileen inguruneetako esportazioak segmentatu (B-to-C)**  
- Segmentuak testuinguruan inguruneetan banakako bezeroak eraikitzen dira *bezero profil bateratua* entitatea. Xede-sistemen baldintzak betetzen dituen segmentu guztiak (adibidez, helbide elektronikoa) esportatu ahal izango dira.

**Segmentu esportazioak negozio-kontuetarako inguruneetan (B-to-B)**  
- Enpresa-kontuetarako inguruneen testuinguruko segmentuak oinarrian eraikitzen dira *kontua* entitatea edo *kontaktua* entitate. Kontuen segmentuak bere horretan esportatzeko, xede-sistemak kontu segmentu puruak onartzen ditu. Hau da kasua [LinkedIn](export-linkedin-ads.md) aukeratzerakoan **konpainia** aukera esportazioa definitzerakoan.
- Helburuko beste sistema guztiek harremanetarako entitatearen eremuak behar dituzte.
- Bi segmentu motarekin (kontaktuak eta kontuak), Customer Insights-ek automatikoki identifikatzen du zein segmentu mota esportatzeko eskubidea duten helburu-sisteman oinarrituta. Adibidez, Mailchimp bezalako kontaktuetan ardaztutako helburu-sistema baterako, Customer Insights-ek esportatzeko kontaktu-segmentuak aukeratzen ditu soilik.

**Segmentuen esportazioen mugak**  
- Hirugarrenen helburu sistemek esporta ditzakezun bezeroen profil kopurua muga dezakete. 
- Banakako bezeroentzako, segmentuko kide kopurua ikusiko duzu esportatzeko segmentu bat hautatzen duzunean. Segmentu bat handiegia bada abisu bat jasoko duzu. 
- Enpresa-kontuetarako, segmentuaren araberako kontu edo kontaktu kopurua ikusiko duzu. Abisu bat jasoko duzu segmentua handiegia bada. Helburuko sistemen emaitzen mugak gaindituz gero, esportazioa saltatuko da.

## <a name="set-up-a-new-export"></a>Konfiguratu esportazio berria

Esportazio bat konfiguratzeko edo editatzeko, eskuragarri dituzun konexio egokiak behar dituzu. Konexioak zure araberakoak dira [erabiltzailearen rola](permissions.md):
- **Administratzaileak** sarbidea dute konexio guztietara. Konexio berriak sor ditzakete esportazioa konfiguratzerakoan.
- **Laguntzaileek** sarbidea dute konexio espezifikoetara. Konexioak konfiguratzeko eta partekatzeko administratzaileen mende daude. Esportazioen zerrendan agertzen da laguntzaileek esportazio bat editatu edo soilik ikus dezaketen **Zure baimenak** zutabean. Informazio gehiagorako, joan hona [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).
- **Ikusleak** lehendik dauden esportazioak soilik ikus ditzake —ez sortu.

1. Joan **Datuak** > **Esportazioak**.

1. Esportatze berria sortzeko, hautatu **Gehitu esportatzea**.

1. urtean **Konfiguratu esportazioa** panela, hautatu zein [konexioa](connections.md) erabiltzeko.

1. Eman beharrezko xehetasunak eta hautatu **Gorde** esportazioa sortzeko. Beharrezko xehetasunak lortzeko, berrikusi esportazio espezifikorako Customer Insights dokumentazioa.

## <a name="manage-existing-exports"></a>Kudeatu lehendik dauden esportazioak

Joan **Datuak** > **Esportazioak** esportazioak, haien konexioaren izena, konexio mota eta egoera ikusteko. Erabiltzaile rol guztiek konfiguratutako esportazioak ikus ditzakete. Esportazioen zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun esportazioa aurkitzeko.

Hautatu esportazio bat erabilgarri dauden ekintzak ikusteko.

:::image type="content" source="media/exports_showmore.png" alt-text="Esportazioen orria.":::

- **Ikusi** edo **Editatu** esportazioa. Editatzeko baimenik ez duten erabiltzaileak hautatzen dituzte **Ikusi** ordez **Editatu** esportazio xehetasunak ikusteko.
- **Korrika egin** esportatu azken datuak esportatzeko.
- **Sortu bikoiztuak** esportazio batena.
- **[Ordutegia](#schedule-and-run-exports)** esportazioa.
- **Kendu konexioa** esportazio honetarako konexioa kentzeko. Deskonektatzeak ez du konexioa kentzen, esportazioa desaktibatu baizik. The **Erabilitako konexioa** zutabeak Konexiorik ez erakusten du.
- **Kendu** esportazioa.

## <a name="schedule-and-run-exports"></a>Antolatu eta exekutatu esportazioak

Konfiguratzen duzun esportazio bakoitzak freskatze ordutegia du. Freskatze batean, sistemak esportazio batean sartzeko datu berri edo eguneratuak bilatzen ditu. Berez, esportazioak [programatutako eguneratze sistema](schedule-refresh.md) guztien zati gisa exekutatzen dira. Freskatze ordutegia pertsonaliza dezakezu edo desaktiba dezakezu esportazioak eskuz exekutatzeko.

> [!TIP]
> Minimizatu segmentu-esportazioen prozesatze-denbora praktika onenekin:
> - Banatu segmentu-entitateak esportazio anitzetan.
> - Saihestu esportazio guztiak aldi berean programatzea. Utzi 30 minutu edo ordu bat esportazio bakoitzaren programatutako orduaren artean.

Esportazio ordutegiak zure ingurunearen egoeraren araberakoak dira. Eguneratzeak martxan badaude aktibatuta [mendekotasunak](system.md#refresh-processes) programatutako esportazio bat hasi behar denean, sistemak eguneraketak osatuko ditu eta esportazioa exekutatuko du. The **Freskatua** zutabeak esportazio bat azken aldiz noiz freskatu den erakusten du.

### <a name="schedule-exports"></a>Antolatu esportazioak

Definitu freskatze programazio pertsonalizatuak esportazio indibidualetarako edo hainbat esportazio aldi berean. Unean definitutako ordutegia esportazio zerrendako **Antolaketa** zutabean agertzen da. Ordutegia aldatzeko baimena bera da [esportazioak editatzea eta definitzea](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu antolatu nahi duzun esportazioa.

1. Hautatu **Antolaketa**.

1. **Programatu esportazioa** panelean, ezarri **Antolatu exekuzioa** aukera **Aktibatuta** gisa, esportazioa automatikoki exekutatzeko. Ezarri **Desaktibatuta** gisa eskuz freskatzeko.

1. Automatikoki freskatutako esportazioetarako, aukeratu **Errepikatzearen** balioa eta zehaztu horren xehetasunak. Definitutako denbora errepikatze-kasu guztiei aplikatzen zaie. Esportazio bat freskatzen hasi behar den unea da.

1. Sakatu **Gorde**.

Hainbat esportazioren egutegia editatzerakoan, egin aukeraketa azpian **Mantendu edo gainidatzi ordutegiak**:

- **Mantendu banakako ordutegiak** : Gorde hautatutako esportazioetarako aurrez zehaztutako programazioa eta soilik gaitu edo desgaitu.
- **Zehaztu hautatutako esportazio guztientzako antolaketa berria**: Gainidatzi hautatutako esportazioen dauden antolaketak.

### <a name="run-exports-on-demand"></a>Exekutatu esportazioak eskatu ahala

Datuak esportatzeko programatutako freskapenaren zain egon gabe, joan hona: **Datuak** > **Esportazioak**.

- Esportazio guztiak exekutatzeko, hautatu **Exekutatu guztiak** komando barran. Programazio aktiboa duten esportazioak bakarrik exekutatzen dira. Aktibo ez dagoen esportazio bat exekutatzeko, exekutatu esportazio bakarra.
- Esportazio bakarra exekutatzeko, hautatu zerrendatik eta hautatu **Exekutatu** komando barran.

## <a name="troubleshooting"></a>Arazoak konpontzea

### <a name="segment-not-eligible-for-export"></a>Segmentua ez da esportatzeko eskubidea

**Arazoa** Enpresa-kontuen ingurune batean, zure esportazioek huts egiten dute errore-mezuarekin: "Segmentu hau ez da esportazio-helmuga honetarako egokia:"{ segmentuaren izena} '. Aukeratu ContactProfile motako segmentuak soilik eta saiatu berriro."

**Ebazpena** Enpresa-kontuetarako Customer Insights inguruneak eguneratu dira kontu-segmentuez gain kontaktu-segmentuak onartzeko. Aldaketa hori dela eta, kontaktuen xehetasunak behar dituzten esportazioek kontaktuetan oinarritutako segmentuekin soilik funtzionatzen dute.

1. [Sortu segmentu bat kontaktuetan oinarrituta](segment-builder.md) aurrez erabilitako segmentuarekin bat datorrena.

1. Kontaktu-segmentu hori exekutatzen denean, editatu dagokion esportazioa eta hautatu segmentu berria.

1. Hautatu **Gorde** konfigurazioa gordetzeko edo **Gorde eta exekutatu** esportazio hori berehala probatzeko.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]


[!INCLUDE [footer-include](includes/footer-banner.md)]
