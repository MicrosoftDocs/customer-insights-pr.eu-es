---
title: Konexioen ikuspegi orokorra (aurrebista)
description: Customer Insights-etik beste zerbitzu batzuetarako konexioak.
ms.date: 04/09/2021
ms.reviewer: nikeller
ms.subservice: audience-insights
ms.topic: overview
author: m-hartmann
ms.author: mhart
manager: shellyha
searchScope:
- ci-connections
- customerInsights
ms.openlocfilehash: a8b4b8a9bdcf7cf43c47a67d547405dd20dad60d
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9082085"
---
# <a name="connections-preview-overview"></a>Konexioen ikuspegi orokorra (aurrebista)

Konexioak dira Customer Insights-etik eta horretatik datuak partekatzea ahalbidetzeko gakoa. Konexio bakoitzak zerbitzu jakin batekin datuak partekatzea ezartzen du. Konexioak dira oinarria [konfiguratu hirugarrenen aberastasunak](enrichment-hub.md) eta [esportazioak konfiguratu](export-destinations.md). Konexio bera hainbat aldiz erabil daiteke. Adibidez, Dynamics 365 Marketing-erako konexio batek esportazio anitzetarako balio du eta Leadspace konexio bat aberastu ahal izateko.

Joan **Administratzailea** > **Konexioak** konexioak sortzeko eta ikusteko.

**Konexioak** fitxak konexio aktibo guztiak erakusten dizkizu. Zerrendan konexio bakoitzerako errenkada bat agertzen da.

Lortu ikuspegi orokorra, deskribapena eta jakin zer egin dezakezun **Ezagutu** fitxa.

## <a name="exports"></a>Esportazioak

Administratzaileek soilik konfigura ditzakete konexio berriak, baina laguntzaileei sarbidea eman diezaiekete lehendik dauden konexioak erabiltzeko. Administratzaileek datuak nora joan daitezkeen kontrolatzen dute, laguntzaileek beren beharretara egokitzen duten karga eta maiztasuna definitzen dute. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](#allow-contributors-to-use-a-connection-for-exports).

## <a name="enrichments"></a>Aberasteak

Administratzaileek soilik konfigura ditzakete konexio berriak, baina sortutako konexioak beti daude eskuragarri administratzaile zein laguntzaileentzat. Administratzaileek egiaztagiriak kudeatzen dituzte eta datuen transferentziei baimena ematen diete. Konexioak administratzaileek eta laguntzaileek aberasteko erabil ditzakete.

## <a name="add-a-new-connection"></a>Gehitu konexio bat

Konexioak gehitzeko, eduki behar duzu [administratzaile baimenak](permissions.md). Beste Microsoft zerbitzu batzuekin konektatzen bazara, bi zerbitzuak erakunde berean daudela suposatuko dugu.

1. Joan **Administratzailea** > **Konexioak (aurrebista)**.

1. Joan **Konexioak** fitxara.

1. Hautatu **Gehitu konexioa** konexio berri bat sortzeko. Aukeratu goitibeherako menuan zein konexio mota sortu nahi duzun.

1. Hurrengoan **Konfiguratu konexioa** panelean, eman beharrezko xehetasunak.
   1. **Bistaratzeko izena** eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.
   1. Eremu zehatzak konektatzen ari zaren zerbitzuaren araberakoak dira. Konexio mota zehatz baten xehetasunak ezagutu ditzakezu xede zerbitzuaren inguruko artikulua.
   1. Bada [erabili zure Key Vault](use-azure-key-vault.md) sekretuak gordetzeko, aktibatu **Erabili Key Vault** eta aukeratu zerrendako sekretua.

1. Konexioa sortzeko, hautatu **Gorde**.

Aukeratu ere egin dezakezu **Konfiguratu** teila batean **Ezagutu** fitxa.

### <a name="allow-contributors-to-use-a-connection-for-exports"></a>Baimendu laguntzaileei esportazioetarako konexioa erabiltzea

Esportazio konexioa konfiguratu edo editatzerakoan, aukeratzen duzu zein erabiltzaile konexio zehatz hau erabili ahal izateko definitzeko [esportazioak](export-destinations.md). Berez, konexioa erabilgarri dago administratzaile funtzioa duten erabiltzaileentzat. Ezarpen hau alda dezakezu **Aukeratu nork erabil dezakeen konexio hau** eta lagundu laguntzaile rolak dituzten erabiltzaileei konexio hau erabiltzeko.

- Laguntzaileek ezin izango dute konexioa ikusi edo editatu. Bistaratzeko izena eta haren mota soilik ikusiko dituzte esportazio bat sortzean.
- Konexioa partekatuz gero, laguntzaileei konexioa erabiltzeko baimena ematen diezu. Laguntzaileek partekatutako konexioak ikusiko dituzte esportazioak konfiguratzen dituztenean. Konexio zehatz hau erabiltzen duten esportazio guztiak kudea ditzakete.
- Ezarpen hau alda dezakezu laguntzaileek definitutako esportazioak mantenduz.

## <a name="edit-a-connection"></a>Editatu konexio bat

1. Joan **Administratzailea** > **Konexioak (aurrebista)**.

1. Joan **Konexioak** fitxara.

1. Hautatu elipsi bertikala (&vellip;) editatu nahi duzun konexiorako.

1. Hautatu **Editatu**.

1. Aldatu eguneratu nahi dituzun balioak eta hautatu **Gorde**.

## <a name="remove-a-connection"></a>Konexioa kendu nahi duzu

Kentzen ari zaren konexioa aberasteek edo esportazioek erabiltzen badute, lehenik kendu edo kendu behar dituzu. Kendu elkarrizketa-koadroak aberastasun edo esportazio garrantzitsuetara eramango zaitu.

Bereizitako aberastasunak eta esportazioak inaktibo bihurtzen dira. Berriro aktibatuko dituzu haiekin beste konexio bat gehituz [Aberastasunak](enrichment-hub.md) edo [Esportazioak](export-destinations.md) orrialdea.

1. Joan **Administratzailea** > **Konexioak (aurrebista)**.

1. Joan **Konexioak** fitxara.

1. Hautatu elipsi bertikala (&vellip;) kendu nahi duzun konexiorako.

1. Hautatu **Kendu** goitibeherako menuan. Berresteko elkarrizketa agertzen da.

   1. Konexio hau erabiltzen duten aberastasunak edo esportazioak badaude, hautatu botoia konexioa erabiltzen ari dena ikusteko.
      - **Esportazioak:** Konexioa kendu ahal izateko esportazioak kentzea edo deskonektatzea aukera dezakezu. Esportazio bat deskonektatzeko, administratzaileek **Deskonektatu** ekintza. Ekintza hau eskuragarri dago banakako eta hautatutako esportazio anitzetarako. Deskonektatuta esportazio konfigurazioa mantenduko duzu, baina ez da exekutatuko beste konexio bat gehitu arte.
      - **Aberasteak:** Konexioa kendu ahal izateko aberasteak desaktibatzea edo kentzea aukera dezakezu.
   1. Konexioak mendekotasun gehiago ez duenean, itzuli berriro **Administratzailea** > **Konexioak** eta saiatu berriro konexioa kentzen.

1. Ezabapena berresteko hautatu **Kendu**.

## <a name="set-up-connections-with-secrets-managed-by-your-own-key-vault"></a>Konfiguratu konexioak zeure Key Vault-ek kudeatutako sekretuekin

Konexio batzuek API gakoak edo pasahitzak bezalako sekretuak behar dituzte. Konexio batzuek zure Key Vault-en gordetako sekretuak onartzen dituzte. Lortu informazio gehiago onartzen diren konexioei eta nola konfiguratu [zure Key Vault Customer Insights egiteko](use-azure-key-vault.md).
