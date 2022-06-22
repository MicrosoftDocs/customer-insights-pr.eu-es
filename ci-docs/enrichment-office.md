---
title: Aberastu bezeroen profilak datuekin Microsoft Office 365
description: Erabili jabedun datuak Microsoft Office zure bezeroen profilak konpromiso datuekin aberasteko.
ms.date: 06/10/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: jodahl
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: 7192b7680e73a581dd603de174c57b20bec996dd
ms.sourcegitcommit: 27c5473eecd851263e60b2b6c96f6c0a99d68acb
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/13/2022
ms.locfileid: "8954118"
---
# <a name="enrich-customer-profiles-with-engagement-data-preview"></a>Aberastu bezeroen profilak konpromiso datuekin (aurrebista)

Erabili datuak Microsoft Office 365 zure bezero-kontuaren profilak engaiamenduei buruzko informazioekin aberasteko Office 365 aplikazioak. Konpromiso-datuak posta elektronikoa eta bilera-jarduerak dira, kontu mailan batzen direnak. Adibidez, negozio-kontu bateko mezu elektronikoen kopurua edo kontuarekin izandako bilera-kopurua. Ez dago erabiltzaile indibidualei buruzko daturik eskuragarri.

## <a name="supported-countries-or-regions"></a>Lagundutako herrialdeak edo eskualdeak

Gaur egun, eskualde hauek onartzen ditugu: Erresuma Batua, Europa, Ipar Amerika.

## <a name="prerequisites"></a>Aurrebaldintzak

- Aktibo bat Office 365 hodeiko lizentzia.
- [Bezeroen profil bateratuak](customer-profiles.md) oinarrituta [negozio kontuak](work-with-business-accounts.md).
- A [Microsoft Dataverse erakundea erantsita](create-environment.md#step-3-connect-to-microsoft-dataverse) zure Customer Insights ingurunean.
- [Administratzailea](permissions.md#admin) baimenak.
- Zure adostasuna Office 365 maizter administratzailea erabiltzeko Office 365 eman beharreko datuak **Antolakuntzarako ikuspegiak** Dynamics 365 aplikazioen barruan.

## <a name="configure-the-enrichment"></a>Konfiguratu aberastea

1. Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.

1. Hautatu **Aberastu nire datuak** gainean **Kontu-konpromisoa** teila.

   :::image type="content" source="media/enrichment-office-tile.png" alt-text="Kontuaren konpromiso-lauza.":::

1. Berrikusi ikuspegi orokorra eta, ondoren, hautatu **Hurrengoa**.

1. Sartu zure erakundeko helbide elektronikoak zeinetarako Office datuak bilduko diren. Zerrendatutako helbide elektronikoetako datuak soilik prozesatzen dira dagokion komunikaziorako. Praktika onena posta elektronikoko taldeak erabiltzea da, adibidez, *AEBetako salmenta taldea*, eta bertan kudeatu dezakezu Office 365. Taldeetako helbide elektronikoen kopurua ebatzi eta erakusten da. Helbide elektronikoen kopuruak gutxienez 2 izan behar ditu eta ezin dira 2.500 baino gehiago izan.

   :::image type="content" source="media/enrichment-office-email-addresses.png" alt-text="Kontuaren parte hartzeko helbide elektronikoak.":::

1. Berrikusi eta eman zure baimena [Office 365 maizter administratzaileen baimena](#office-365-tenant-administrator-consent) hautatuz **ados**.

1. Hautatu **Hurrengoa**.

1. Hautatu **Harremanetarako datu multzoa** eta aukeratu aberastu nahi duzun profila. Hautatu **Hurrengoa**.

1. Mapeatu kontaktuaren helbide elektronikoaren eremua eta hautatu **Hurrengoa**.

1. Eman a **Izena** aberasteko eta **Irteerako entitatea**.

1. Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.

1. Hautatu **Itxi** itzultzeko **Aberasgarriak** orrialdea.

### <a name="office-365-tenant-administrator-consent"></a>Office 365 maizter administratzaileen baimena

Baten adostasuna Office 365 maizter-administratzailea behar da aberastea aktibatzeko. E-mail bat bidaltzen da Office 365 maizter-administratzaileei aberastea gordetzen denean, eta horrek Dynamics 365 aplikazioei zure enpresak erabiltzeko baimena emateko eta berrikusteko eskatzen die.Office 365 eman beharreko datuak **Antolakuntzarako ikuspegiak**. The Office 365 maizter-administratzaileak zuzenean baimena eman dezake Office 365 administrazio kontsola, hautatuz **Antolakuntzarako ikuspegiak**.

## <a name="running-the-enrichment-for-the-first-time"></a>Aberasketa lehen aldiz exekutatzen

Aberastea lehen aldiz hasten denean, ondoren Office 365 maizter-administratzaileak baimena eman du, deskargatzeko datuak Office 365 hasten da. Prozesu honek denbora pixka bat behar du. Lehenengo aberaste-ibilaldia sei orduko atzerapenarekin egitea aurreikusiko da. Datuek zenbat egun hartzen duten ikus dezakezu kontuaren konpromisoaren ikuspegi orokorraren orrian, aberastea amaitu ondoren. Datu-bolumen handiarekin, exekutatu berriro aberastea egun batzuen buruan. Datuak denbora-leiho osorako osatuta daudela ziurtatzen du, hau da, urtebetekoa.

Office-ko datuen tamainaren arabera, hainbat ordu behar izan ditzake aberasteko exekuzioa burutzeko.

Aberaste bat exekutatzen duzunean, Microsoft-ek datuak prozesatuko ditu Office 365 betetze-muga, informazio agregatuak sortzeko, gero zure Customer Insights ingurunera gehitzen direnak. Maila indibidualeko daturik (adibidez, edozein e-mail edo egutegiko gonbidapenen gorputza) ez dute eskuragarri Customer Insights-en erabiltzaileek.

Hautatu **Korrika egin** aberaste-prozesua hasteko.

[!INCLUDE [progress-details-pane](includes/progress-details-pane.md)]

## <a name="enrichment-results"></a>Aberastearen emaitzak

[!INCLUDE [enrichment-results](includes/enrichment-results.md)] Hau da *Bulegoa* entitate. The *Bulegoa_ErabiltzaileEntitatea* aberastearen konfigurazioan aukeratu ziren helbide elektronikoen Active Directory IDak ditu.

:::image type="content" source="media/enrichment-office-results-overview.png" alt-text="Abantaila prozesua exekutatu ondoren, emaitzen aurrebista.":::

Datu guztiak kontu mailara arte batzen dira. Sistemak konpromiso puntuazio bat kalkulatzen du, 0tik 100era bitartekoa, kontu bakoitzeko. Konpromisoaren puntuazioak mezu elektronikoetan eta bileretan kontuaren konpromisoaren neurketa konposatua eskaintzen du zure beste kontuekiko. Ondorengo zerrendak kontu-konpromisoa aberasteak ematen dituen datu bateratuak ditu:

| Datuak                                                                              | Zutabearen izena                              |
| :-------------------------------------------------------------------------------- |:---------------------------------------- |
| Parte hartzearen puntuazioa                                                                  |  EngagementScore                         |
| Konturako mezu elektroniko kopurua                                                       |  NoOfEmails_ToAccount                    |
| Kontuko mezu elektroniko kopurua                                                     |  NoOfEmails_From Account                  |
| Kontuaren arabera hasitako bilera kopurua                                           |  NoOfMeetings_From Account                |
| Zure erakundeak hasitako bilera kopurua                                 |  NoOfMeetings_ToAccount                  |
| Zure erakundeko pertsona kopurua kontuarekin bileretan                  |  NoOfContactsInvolved_Meetings           |
| Zure erakundeko pertsona kopurua kontuarekin posta elektroniko bidezko elkarrizketetan       |  NoOfContacts Involved_Emails             |
| Kontuko pertsona kopurua zure erakundearekin egindako bileretan                  |  NoOfAccountContactsInvolved_Meetings    |
| Kontuko pertsona kopurua zure erakundearekin posta elektroniko bidezko elkarrizketetan       |  NoOfAccountContactsInvolved_Emails      |
| Konpromisoaren hasiera-data (lehen posta elektronikoa edo bilera datuetan)                        |  EngagementStartDate                     |
| Azken mezu elektronikotik egun batzuk                                                             |  DaysSinceLastE-mail                      |
| Azken bileratik egunak                                                           |  DaysSinceLastMeeting                    |
| Bileren batez besteko iraupena                                                      |  Bileren_batez besteko iraupena             |
| Kontuaren posta elektronikoko erantzunen batez besteko iraupena                                    |  AverageDuration_Of_AccountEmailReplies  |
| Agregazio hasiera data                                                            |  AggregationStartDate                    |
| Agregazio maila (urtea, hilabetea edo astea)                                          |  AgregazioMaila                        |

## <a name="see-enrichment-data-on-the-customer-card"></a>Ikusi aberastasun datuak bezeroaren txartelean

Kontuaren konpromisoa bezeroen banakako txarteletan ere ikus daiteke. Joan **Bezeroak** atalera eta hautatu bezeroaren profila. Bezero-txartelean, kontuaren konpromisoaren puntuazioa, mezu elektronikoen guztizko kopurua eta azken urtean bildutako bilera-kopurua guztira aurkituko dituzu. Posta elektronikoa eta bileraren historia erakusten duten grafikoak ere aurkituko dituzu.

:::image type="content" source="media/enrichment-office-customer-card.png" alt-text="Aberastutako datuak dituen bezeroaren txartela.":::

## <a name="next-steps"></a>Hurrengo urratsak

[!INCLUDE [next-steps-enrichment](includes/next-steps-enrichment.md)]
Adibidez, 60tik gorako balioa duten bezero guztiak biltzen dituen segmentua *azken mezu elektronikotik egun* eta *azken bileratik egunak*. Segmentu horrek zaharkitutako kontuak ditu, berriro aktibatzen saia zaitezke.

[!INCLUDE [footer-include](includes/footer-banner.md)]
