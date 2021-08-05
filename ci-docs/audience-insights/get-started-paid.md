---
title: Sortu eta konfiguratu Customer Insights-en ordainpeko bertsioa
description: Dynamics 365 Customer Insights lizentziadun harpidetza lortzeko eta konfiguratzeko urratsak.
ms.date: 07/22/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: MichelleDevaney
ms.author: midevane
manager: shellyha
ms.custom: intro-internal
ms.openlocfilehash: f8cf1be97ee8af46145a450009fd278b1821f8fe
ms.sourcegitcommit: 5c9c54ffe045017c19f0042437ada2c101dcaa0f
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "6650442"
---
# <a name="get-started-with-a-paid-subscription"></a>Hasi ordainpeko harpidetza erabiltzen

Artikulu honetan zure erakundeak Dynamics 365 Customer Insights harpidetza erosi ondoren ingurune berri bat nola sortu azaltzen da. Customer Insights erosi nahi baduzu, gure harremanetarako aukerak atalean agertzen dira [Dynamics 365 Customer Insights webgunean](https://dynamics.microsoft.com/ai/customer-insights/). 

Zerbitzua eta eginbideak probatu nahi badituzu, ikusi [Konfiguratu proba ingurunea](get-started-trial.md).

## <a name="create-an-environment-in-an-existing-organization"></a>Sortu ingurune bat lehendik dagoen erakunde batean

Customer Insights-erako harpidetza lizentzia erosi ondoren, Microsoft 365 maizterreko administratzaile orokorrak ingurunea sortzera gonbidatzen duen mezu elektronikoa jasotzen du. Erabiltzen hasteko, joan hona: [https://home.ci.dynamics.com/start](https://home.ci.dynamics.com/start). 

Customer Insights-ek ez du erabiltzaile bakoitzeko lizentziarik, beraz ez da Lizentziaren eremuan erakutsiko. Lizentzia Microsoft 365 administrazio zentroan bilatzen ari bazara, joan hona **Zure produktuak**. 

> [!NOTE]
> Erakundeek sor dezakete *bi* Customer Insights lizentzia bakoitzeko inguruneak. Zure erakundeak lizentzia behin baino gehiagotan erosten badu, mesedez [jarri harremanetan gure laguntza taldearekin](https://go.microsoft.com/fwlink/?linkid=2079641) erabilgarri dauden ingurune kopurua handitzeko. Gaitasun eta gaitasun osagarriei buruzko informazio gehiago lortzeko, deskargatu [Dynamics 365 lizentzien gida](https://go.microsoft.com/fwlink/?LinkId=866544).

Ingurune bat sortzeko:

1. Urtean **Ingurune bat sortu** elkarrizketa-koadroa, hautatu **Ingurune berria**.

   :::image type="content" source="media/environment-settings-dialog.png" alt-text="Elkarrizketa-koadroa Customer Insights ingurune berria sortzeko.":::

   Ingurunea hutsetik konfiguratzen hastea gomendatzen dugu. Hala ere, probako ingurune bateko administratzailea edo kidea bazara, egin dezakezu [kopiatu datuak beste ingurune batetik](manage-environments.md#copy-the-environment-configuration), aukeratuz **Kopiatu lehendik dagoen ingurunetik**. Zure erakundearen eskura dauden ingurune guztien zerrenda ikusiko duzu non datuak kopiatzeko.

1. Hornitu hurrengo xehetasunak:
   - **Izena**: entitatearen izena. Eremu hau dagoeneko bete da ingurune batetik kopiatzen baduzu, baina alda dezakezu.
   - **Eskualdea**: Zerbitzua hedatu eta ostatatzen den eskualdea.
   - **Mota**: Aukeratu Produkzio edo Sandbox ingurunea sortu nahi duzun ala ez. Sandbox inguruneek ez dute programatutako datuak freskatzea onartzen eta aurrez ezartzeko eta probatzeko pentsatuta daude.
   
1. Nahi baduzu, hauta dezakezu **Ezarpen aurreratuak**:

   - **Gorde datu guztiak**: Customer Insights-ek sortutako irteerako datuak non gorde nahi dituzun zehazten du. Bi aukera izango dituzu: **Customer Insights biltegiratzea** (Customer Insights taldeak kudeatzen duen Azure Data Lake) eta **Azure Data Lake Storage** (zeurea Azure Data Lake Storage). Lehenespenez, Customer Insights biltegiratzeko aukera hautatuko da.

     > [!NOTE]
     > Datuak Azure Data Lake Storage-n gordez gero, onartu egingo duzu datuak Azure biltegiratze-konturako egokia den kokaleku geografikora transferitu eta bertan biltegiratuko direla, eta balitekeela Dynamics 365 Customer Insights-en datuak biltegiratzen diren lekua ez den beste kokaleku bat izatea. Informazio gehiago lortzeko, ikusi. [Argibide gehiago Microsoft Trust Center-en.](https://www.microsoft.com/trust-center)
     >
     > Gaur egun, Power BI datu-fluxuen irentsitako entitateak Microsoft Dataverse-k kudeatutako Data Lake-n gordetzen dira. 
     > 
     > Bakarrik onartzen dugu Azure Data Lake Storage ingurunea sortzerakoan hautatu zenituen Azure eskualde bereko kontuak. 
     > 
     > Bakarrik onartzen dugu Azure Data Lake Storage izen espazio hierarkikoa gaituta duten kontuak.


   - Azure Data Lake Storage aukera, baliabideetan oinarritutako aukera bat eta harpidetzan oinarritutako aukera bat autentifikatzeko aukera dezakezu. Informazio gehiagorako, ikus [Konektatu hartzaileei buruzko xehetasunak Azure Data Lake Storage Gen2 kontu batera Azure zerbitzuaren entitatearekin](connect-service-principal.md). **Edukiontzia** izena ezin da aldatu eta `customerinsights` izango da.
   
   - Erabili nahi baduzu [eredu berriak](predictions-overview.md#out-of-box-models), konfiguratu datuak partekatzea Microsoft Dataverse-rekin, edo gaitu datu iturri lokaletako datuak sartzea, emn Microsoft Dataverse inguruneko URLa **Konfiguratu datuak partekatzea Microsoft Dataverse-rekin eta gaitasun osagarriak gaitu** atalean. Aukeratu **Gaitu datuak partekatzea** Customer Insights-en irteerako datuak partekatzeko Microsoft Dataverse kudeatutako datuen lakua.

     > [!NOTE]
     > - Datuak partekatzearekin Microsoft Dataverse-ren kudeatutako datuen lakua ez da onartzen une honetan datu guztiak gordetzen dituzunean Azure Data Lake Storage.
     > - [Entitate batean falta diren balioen iragarpen](predictions.md) ez da onartzen une honetan datuak partekatzea gaitzen duzunean Microsoft Dataverse Kudeatutako Data Lake.

     :::image type="content" source="media/Datasharing-with-DataverseMDL.png" alt-text="Konfigurazioaren aukerak gaitzeko datuak partekatzeko Microsoft Dataverse.":::

   Datuak sartzea bezalako sistemaren prozesuak amaitzen direnean, sistemak dagozkion karpetak sortzen ditu zuk zehaztutako biltegiratze kontuan. Datu fitxategiak eta model.json fitxategiak sortzen dira eta karpetetan gehitzen dira prozesuaren izenean oinarrituta.

   Customer Insights-eko hainbat ingurune sortzen badituzu eta ingurune horietako irteerako entitateak zure biltegiratze kontuan gordetzea aukeratzen baduzu, karpeta bereiziak sortuko dira ingurune bakoitzarentzat ci_<environmentid> edukiontzian.

1. Hautatu **Sortu** ingurunea konfiguratzeko. 

## <a name="configure-an-environment"></a>Konfiguratu ingurune bat

Berrikusi hurrengo artikuluak Customer Insights konfiguratzen hasteko. 

- [Gehitu erabiltzaile gehiago eta eman baimenak](permissions.md).
- [Sartu zure datu-iturburuak](data-sources.md) eta exekutatu [datuak bateratzeko prozesuaren](data-unification.md) bidez lortzeko [bezeroen profil bateratuak](customer-profiles.md).
- [Aberastu bezeroen profil bateratuak](enrichment-hub.md) edo [exekutatu eredu iragarleak](predictions-overview.md).
- Sortu [segmentuak](segments.md) bezeroak taldekatzeko eta [neurrien](measures.md) berrikuspen KPIak.
- Konfiguratu [konexioak](connections.md) eta [esportazioak](export-destinations.md) zure datuen azpimultzoak beste aplikazio batzuetan prozesatzeko.
