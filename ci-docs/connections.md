---
title: Konexioen ikuspegi orokorra (aurrebista)
description: Customer Insights-etik beste zerbitzu batzuetarako konexioak.
ms.date: 08/04/2022
ms.reviewer: nikeller
ms.subservice: audience-insights
ms.topic: overview
author: m-hartmann
ms.author: mhart
manager: shellyha
searchScope:
- ci-connections
- customerInsights
ms.openlocfilehash: 8580dc7d90c75f66f73efc15f8e38f5e10fbb8a7
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9245496"
---
# <a name="connections-preview-overview"></a>Konexioen ikuspegi orokorra (aurrebista)

Konexioak dira Customer Insights-etik eta horretatik datuak partekatzea ahalbidetzeko gakoa. Konexio bakoitzak zerbitzu jakin batekin datuak partekatzea ezartzen du. Erabili konexioak [hirugarrenen aberasketak konfiguratu](enrichment-hub.md) eta [esportazioak konfiguratu](export-destinations.md). Konexio bera hainbat aldiz erabil daiteke. Adibidez, Dynamics 365 Marketing-erako konexio batek esportazio anitzetarako balio du eta Leadspace konexio bat aberastu ahal izateko.

## <a name="export-connections"></a>Esportatu konexioak

Administratzaileek soilik konfigura ditzakete konexio berriak, baina egin ditzakete [laguntzaileei sarbidea eman](#allow-contributors-to-use-a-connection-for-exports) dauden konexioak erabiltzeko. Administratzaileek datuak nora joan daitezkeen kontrolatzen dute, laguntzaileek beren beharretara egokitzen duten karga eta maiztasuna definitzen dute.

## <a name="enrichment-connections"></a>Aberaste-konexioak

Administratzaileek soilik konfigura ditzakete konexio berriak, baina sortutako konexioak beti daude erabilgarri administratzaileentzat zein laguntzaileentzat. Administratzaileek egiaztagiriak kudeatzen dituzte eta datuen transferentziei baimena ematen diete. Konexioak administratzaileek eta laguntzaileek aberasteko erabil ditzakete.

## <a name="add-a-new-connection"></a>Gehitu konexio bat

### <a name="prerequisites"></a>Aurrebaldintzak

- [Administratzailearen baimenak](permissions.md)
- Microsoft-eko beste zerbitzu batzuk, halakorik balego, erakunde berean daude

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu sortu nahi duzun konexio mota. Edo, joan **Ezagutu** fitxa eta hautatu **Konfiguratu** konexio fitxa batean.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Sartu beharrezko xehetasunak. Eremu zehatzak konektatzen ari zaren zerbitzuaren araberakoak dira. Konexio mota zehatz baten xehetasunak lortzeko, ikusi xede-zerbitzuari buruzko artikulua.

1. Bada [erabili zure Key Vault](use-azure-key-vault.md) sekretuak gordetzeko, aktibatu **Erabili Key Vault** eta aukeratu zerrendako sekretua.

1. Berrikusi datuen pribatutasuna eta betetzea eta hautatu **ados**.

1. Hautatu **Gorde** konexioa sortzeko.

### <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Gaitzen duzunean Dynamics 365 Customer Insights hirugarrenei edo Microsoft-eko beste produktu batzuei datuak transmititzeko, datuak betetze-mugatik kanpo transferitzea onartzen duzu Dynamics 365 Customer Insights, potentzialki sentikorrak diren datuak barne, hala nola Datu Pertsonalak. Microsoft-ek datu horiek zure aginduetara transferituko ditu, baina hirugarrenak izan ditzakezun pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzeaz arduratzen zara. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).

Zure Dynamics 365 Customer Insights administratzaileak konexioa ken dezake edozein unetan funtzionalitatearen erabilerari uzteko.

## <a name="allow-contributors-to-use-a-connection-for-exports"></a>Baimendu laguntzaileei esportazioetarako konexioa erabiltzea

Esportazio-konexio bat konfiguratzean edo editatzen duzunean, aukeratu zein erabiltzailek baimentzen duten konexio zehatz hori definitzeko [esportazioak](export-destinations.md). Lehenespenez, konexio bat erabilgarri dago administratzaile rola duten erabiltzaileentzat. Aldatu **Aukeratu nork erabil dezakeen konexio hau** kolaboratzaile rola duten erabiltzaileei konexio hau erabiltzeko aukera emateko ezarpena.

- Laguntzaileek ezin izango dute konexioa ikusi edo editatu. Bistaratzeko izena eta bere mota soilik ikusiko dituzte esportazio bat sortzean.
- Konexioa partekatuz gero, laguntzaileei konexioa erabiltzeko baimena ematen diezu. Laguntzaileek partekatutako konexioak ikusiko dituzte esportazioak konfiguratzen dituztenean. Konexio zehatz hau erabiltzen duten esportazio guztiak kudea ditzakete.
- Ezarpen hau alda dezakezu laguntzaileek definitutako esportazioak mantenduz.

## <a name="manage-existing-connections"></a>Kudeatu lehendik dauden konexioak

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Aberastea** edo **Esportazioak** fitxa aberasteko edo esportatzeko konexioen zerrenda ikusteko, konexio mota, noiz sortu zen eta nork duen sarbidea. Konexioen zerrenda edozein zutaberen arabera ordena dezakezu.

1. Hautatu konexioa erabilgarri dauden ekintzak ikusteko.

   - **Editatu** konexioa.
   - [**Kendu**](#remove-a-connection) konexio bat.

### <a name="remove-a-connection"></a>Konexioa kendu nahi duzu

Kentzen ari zaren konexioa aberasteek edo esportazioek erabiltzen badute, lehenik, kendu edo kendu itzazu. Kendu elkarrizketa-koadroak aberasgarri edo esportazioetara bideratzen zaitu.

> [!TIP]
> Desaktibatutako aberasketak eta banandutako esportazioak inaktibo bihurtzen dira. Berriro aktibatuko dituzu haiekin beste konexio bat gehituz [Aberastasunak](enrichment-hub.md) edo [Esportazioak](export-destinations.md) orrialdea.

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Aberastea** edo **Esportazioak** fitxa.

1. Hautatu kendu nahi duzun konexioa.

1. Hautatu **Kendu** goitibeherako menuan. Berresteko elkarrizketa agertzen da.

   1. Konexio hau erabiltzen duten aberastasunak edo esportazioak badaude, hautatu botoia konexioa erabiltzen ari dena ikusteko.
      - **Esportazioak:** Aukeratu bai **Kendu** esportazioa edo **Kendu konexioa**. Konexioa kentzeak esportazio-konfigurazioa mantentzen du, baina ez da exekutatuko beste konexio bat gehitu arte.
      - **Aberasgarriak:** Aukeratu bai **Ezabatu** edo **Desaktibatu** aberastasunak.
   1. Konexioak mendekotasun gehiago ez duenean, itzuli berriro **Administratzailea** > **Konexioak** eta saiatu berriro konexioa kentzen.

1. Ezabapena berresteko hautatu **Kendu**.

## <a name="set-up-connections-with-secrets-managed-by-your-own-key-vault"></a>Konfiguratu konexioak zeure Key Vault-ek kudeatutako sekretuekin

Konexio batzuek API gakoak edo pasahitzak bezalako sekretuak behar dituzte. Konexio batzuek zure Key Vault-en gordetako sekretuak onartzen dituzte. Lortu informazio gehiago onartzen diren konexioei eta nola konfiguratu [zure Key Vault Customer Insights egiteko](use-azure-key-vault.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
