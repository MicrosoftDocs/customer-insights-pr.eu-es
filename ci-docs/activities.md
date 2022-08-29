---
title: Bezeroarekin edo enpresarekin harremanetan jartzeko jarduerak
description: Definitu bezeroaren edo negozioaren harremanetarako jarduerak eta ikusi itzazu denbora-lerro batean bezeroen profiletan.
ms.date: 08/12/2022
ms.subservice: audience-insights
ms.reviewer: v-wendysmith
ms.topic: conceptual
author: CadeSanthaMSFT
ms.author: cadesantha
manager: shellyha
searchScope:
- ci-entities
- ci-customer-card
- ci-relationships
- ci-activities
- ci-activities-wizard
- ci-measures
- ci-segment-suggestions
- customerInsights
ms.openlocfilehash: bbb8bc30d079273bc935181c628915bb3c02d982
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304090"
---
# <a name="customer-or-business-contact-activities"></a>Bezeroarekin edo enpresarekin harremanetan jartzeko jarduerak

Bezeroen jarduerak bezeroek edo negozio-kontaktuek egindako ekintzak edo gertaerak dira. Adibidez, transakzioak, laguntza-deien iraupena, webguneen berrikuspenak, erosketak edo itzulketak. Jarduera hauek datu-iturri batean edo gehiagotan daude. Customers Insights-ekin, sendotu zure bezeroen jarduerak hauetatik [datu-iturriak](data-sources.md) eta bezeroen profilekin lotu. Jarduera hauek kronologikoki agertzen dira denbora-lerro batean bezeroaren profilean. Sartu denbora-lerroa Dynamics 365 aplikazioetan [Bezero txartelaren gehigarria](customer-card-add-in.md) irtenbidea.

## <a name="define-a-customer-activity"></a>Definitu bezeroaren jarduera

Entitate batek gutxienez motako atributu bat izan behar du **Data** bezeroaren denbora-lerro batean sartzeko. The **Gehitu jarduera** kontrola ezgaitzen da horrelako entitate bat aurkitzen ez bada.

1. Joan **Datuak** > **Jarduerak**.

1. Hautatu **Gehitu jarduera** esperientzia gidatua hasteko.

1. urtean **Jardueraren datuak** urratsa, sartu informazio hau:

   - **Jardueraren izena**: Hautatu zure jarduerarako izen bat.
   - **Jarduera-entitatea** : Hautatu transakzio- edo jarduera-datuak biltzen dituen entitate bat.
   - **Gako nagusia**: Hautatu erregistroa era esklusiboan identifikatzen duen eremua. Ez luke balio bikoizturik, balio hutsak edo falta diren balioak.

   :::image type="content" source="media/Activity_Wizard1.PNG" alt-text="Konfiguratu jardueraren datuak izena, entitatea eta gako nagusiarekin.":::

1. Hautatu **Hurrengoa**.

1. urtean **Harremana** urratsa, hautatu **Gehitu harremana** zure jarduera-datuak dagokion bezero-erregistroarekin konektatzeko. Urrats honek entitateen arteko konexioa bistaratzen du.  

   - **Atzerriko giltza** : beste entitate batekin harremana ezartzeko erabiliko den zure jarduera-entitateko atzerriko eremua.
   - **Entitatearen izenari** : Zure jarduera-entitatearekin harremana izango duen iturburu-bezero-entitatea. Datuak bateratzeko prozesuan erabiltzen diren iturburu bezeroen entitateekin bakarrik lotu zaitezke.
   - **Harremanaren izena** : jarduera-entitate honen eta hautatutako iturburu-bezero-entitatearen arteko erlazio bat badago jada, erlazioaren izena irakurtzeko moduan egongo da. Harreman hori existitzen ez bada, harreman berri bat sortuko da koadro honetan ematen duzun izenarekin.

   :::image type="content" source="media/Activity_Wizard2.PNG" alt-text="Definitu entitate-harremana.":::

   > [!TIP]
   > B-to-B inguruneetan, kontuko entitateen eta beste entitate batzuen artean hauta dezakezu. Kontuko entitate bat hautatzen baduzu, harreman bidea automatikoki ezartzen da. Beste entitate batzuetarako, bitarteko entitate baten edo gehiagoren arteko harremana definitu behar duzu, kontuko entitate batera iritsi arte.

1. Hautatu **Aplikatu** harremana sortzeko.

1. Hautatu **Hurrengoa**.

1. Hurrengoan **Jarduera bateratzea** urratsa, aukeratu jarduera gertaera eta zure jardueraren hasiera ordua.
   - **Beharrezko eremuak**
      - **Ekitaldi jarduera**: Jarduera honen gertaera den eremua.
      - **Denbora-marka**: Zure jardueraren hasiera ordua adierazten duen eremua.

   - **Aukerako eremuak**
      - **Xehetasun osagarria**: Jarduera honetarako informazio garrantzitsua duen eremua.
      - **Ikonoa**: Jarduera mota hau ondoen irudikatzen duen ikonoa.
      - **Web-helbidea**: Jarduera honi buruzko informazioa duen URLa duen eremua. Adibidez, jarduera hau iturri duen transakzio-sistema. URL hau datu-iturburu-eko edozein eremu izan daiteke, edo eremu berri gisa eraiki daiteke Power Query eraldaketa. URL datuak fitxategian gordeko dira *Jarduera bateratua* entitatea, erabilita ibaian behera kontsumitu daitekeena [APIak](apis.md).

   - **Erakutsi denbora-eskalan**
      - Aukeratu jarduera ikuspegi kronologikoan erakutsi nahi duzun bezeroen profiletan. Jarduera denbora-lerroan erakusteko, hautatu **Bai**. Ezkutatzeko, hautatu **Ez**.

      :::image type="content" source="media/Activity_Wizard3.PNG" alt-text="Zehaztu bezeroaren jardueraren datuak Jarduera bateratuko entitate batean.":::

1. Hautatu **Hurrengoa** jarduera mota aukeratzeko edo hautatu **Amaitu eta berrikusi** jarduera gordetzeko jarduera mota gisa ezarrita **Bestela**.

1. Hurrengoan **Jarduera mota** urratsa, aukeratu jarduera mota eta hautatu aukeran Customer Insights beste arlo batzuetan erabiltzeko jarduera mota batzuk semantikoki mapatu nahi dituzun. Gaur egun, *Iritzia*, *·*, *Eskaera*, *·*, eta *Harpidetza* jarduera motak semantika onartzen dute eremuak mapatzea onartu ondoren. Jarduera mota bat jarduera berrirako garrantzitsua ez bada, hauta dezakezu *Beste batzuk* edo *Sortu berria* jarduera mota pertsonalizatua lortzeko.

1. Hautatu **Hurrengoa**.

1. Hurrengoan **Berrikuspena** urratsa, egiaztatu hautapenak. Itzuli aurreko edozein urratsetara eta eguneratu informazioa beharrezkoa bada.

1. Aukeratu **Gorde jarduera** aldaketak aplikatzeko eta hautatu **Eginda** atzera joateko **Datuak** > **Jarduerak**. Sortutako jarduera bistaratzen da.

1. Zure jarduera guztiak sortu ondoren, hautatu **Korrika egin** horiek prozesatzeko.

[!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="manage-existing-customer-activities"></a>Kudeatu lehendik dauden bezeroen jarduerak

Joan **Datuak** > **Jarduerak** gordetako jarduerak, haien iturburu-entitatea, jarduera mota eta bezeroaren denbora-lerroan sartzen badira ikusteko. Jardueren zerrenda edozein zutaberen arabera ordena dezakezu edo bilaketa-koadroa erabili kudeatu nahi duzun jarduera aurkitzeko.

Hautatu jarduera bat erabilgarri dauden ekintzak ikusteko.

- **Editatu** konfigurazioa aldatzeko jarduera. Konfigurazioa berrikuspen urratsean irekitzen da. Konfigurazioa aldatu ondoren, hautatu **Gorde jarduera** eta, ondoren, hautatu **Korrika egin** aldaketak prozesatzeko.
- **Aldatu izena** jarduera. Aldaketak aplikatzeko, hautatu **Gorde**.
- **Ezabatu** jarduera. Jarduera bat baino gehiago aldi berean ezabatzeko, hautatu jarduerak eta gero **Ezabatu**. Berretsi ezabatzea.

## <a name="view-activity-timelines-on-customer-profiles"></a>Ikusi jarduera profilak bezeroen profiletan

1. Hautatu baduzu **Erakutsi jardueren denbora-lerroan** jardueraren konfigurazioan, joan hona **Bezeroak** eta hautatu bezeroaren profil bat bezeroaren jarduerak ikusteko **Jardueren kronograma** atala.

   :::image type="content" source="media/Activity_Timeline1.PNG" alt-text="Ikusi konfiguratutako jarduerak Bezeroen profiletan.":::

1. Jarduerak jardueren denbora-lerroan iragazteko:

   - Hautatu jarduera-ikonoetako bat edo gehiago zure emaitzak hobetzeko, hautatutako motak soilik sartzeko.

     :::image type="content" source="media/Activity_Timeline2.PNG" alt-text="Iragazi jarduerak motaren arabera ikonoak erabiliz.":::

   - Hautatu **Iragazkia** iragazkien panel bat irekitzeko zure denbora-lerroko iragazkiak konfiguratzeko. Iragazi arabera *Jarduera mota* eta/edo *Data*. Hautatu **Aplikatu**.

     :::image type="content" source="media/Activity_Timeline3.PNG" alt-text="Erabili iragazki panela iragazki baldintzak konfiguratzeko.":::

> [!NOTE]
> Jardueren iragazkiak bezeroaren profila uzten duzunean kentzen dira. Bezero profila irekitzen duzun bakoitzean aplikatu behar dituzu.

## <a name="define-a-contact-activity"></a>Definitu harremanetarako jarduera bat

Enpresa-kontuetarako (B-to-B), erabili a *HarremanetarakoProfila* kontaktuen jarduerak harrapatzeko entitatea. Kontu bateko jardueraren kronograman ikus dezakezu zein kontaktu zen jarduera bakoitzaren arduraduna. Urrats gehienek bezeroaren jardueren maparen konfigurazioa jarraitzen dute.

   > [!NOTE]
   > Kontaktu mailako jarduera bat definitzeko, a *HarremanetarakoProfila* entitatea sortu behar da, bai a [kontaktu profil bateratua](data-unification-contacts.md) edo bidez [mapa semantikoa](semantic-mappings.md#define-a-contactprofile-semantic-entity-mapping).
   >
   > Biak izan behar dituzu **Kontuaren ID** eta **Kontaktu ID** zure jarduera-datuen barruan erregistro bakoitzerako atributuak.
  
1. Joan **Datuak** > **Jarduerak**.

1. Hautatu **Gehitu jarduera**.

1. Jarriari izena eman, hautatu iturburuko jarduera-entitatea eta hautatu jarduera-entitatearen gako nagusia.

1. urtean **Harremanak** urratsa, sortu zure jarduera-iturburuko datuen arteko zeharkako harremana kontuekin, zure harremanetarako datuak bitartekari gisa erabiliz. Informazio gehiagorako, ikus [zuzeneko eta zeharkako harreman bideak](relationships.md#relationship-paths).
   - Deitutako jarduera baterako erlazio adibidea *Erosketak*:
      - **Erosketak Iturburu Jardueren Datuak** > **Harremanetarako datuak** atributuaren gainean **Kontaktu ID**
      - **Harremanetarako datuak** > **Kontuaren datuak** atributuaren gainean **Kontuaren ID**

   :::image type="content" source="media/Contact_Activities1.png" alt-text="Erlazio-konfigurazio adibidea.":::

1. Harremanak konfiguratu ondoren, hautatu **Hurrengoa** eta osatu zure jarduera-maparen konfigurazioa. Jarduerak sortzeari buruzko urrats zehatzak ikusteko, ikus [bezeroen jarduera definitzea](#define-a-customer-activity).

1. Exekutatu zure jardueren mapak.

1. Zure kontaktu-mailako jarduerak zure bezeroen denbora-lerroan ikusgai egongo dira orain.

   :::image type="content" source="media/Contact_Activities2.png" alt-text="Azken emaitza kontaktu-jarduerak konfiguratu ondoren":::

## <a name="contact-level-activity-timeline-filtering"></a>Kontaktu mailako jardueren denbora-lerroaren iragazketa

Kontaktu-mailako jardueren mapa konfiguratu eta exekutatu ondoren, zure bezeroen jarduera-kronologia eguneratuko da. Beren ID edo izenak biltzen ditu, zurearen arabera *HarremanetarakoProfila* konfigurazioa, jardun zuten jardueretarako. Jarduerak kontaktuen arabera iragazi ditzakezu denbora-lerroan, interesatzen zaizkizun kontaktu zehatzak ikusteko. Gainera, kontaktu zehatz bati esleituta ez dauden jarduera guztiak ikus ditzakezu hautatuta **Kontaktu bati mapatu gabeko jarduerak**.

   :::image type="content" source="media/Contact_Activities3.png" alt-text="Kontaktu mailako jardueretarako eskuragarri dauden iragazketa-aukerak.":::

[!INCLUDE [footer-include](includes/footer-banner.md)]
