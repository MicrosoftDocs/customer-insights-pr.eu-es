---
title: Iragarri produktuen gomendioak
description: Aurreikusi litekeena dela bezeroak eros ditzakeen produktuak edo haiekin elkarreragitea.
ms.date: 09/30/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: wmelewong
ms.author: wameng
manager: shellyha
ms.openlocfilehash: 0057d6796bb60db44d08b58d9e0daaf6e7c90fde
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9610267"
---
# <a name="predict-product-recommendations"></a>Iragarri produktuen gomendioak

Produktuen gomendio ereduak produktu iragarleentzako gomendio multzoak sortzen ditu. Gomendioak aurreko erosketa portaeran eta antzeko erosketa ereduak dituzten bezeroetan oinarritzen dira. Eredu hau kontsumitzaile indibidualentzat da (B-to-C).

Negozioaren ezagutza izan behar duzu zure negoziorako produktu mota desberdinei buruz eta zure bezeroek haiekin nola elkarreragiten duten. Zure bezeroek aurretik erositako produktuak gomendatzea edo produktu berrietarako gomendioak onartzen ditugu.

Produktuen gomendioak tokiko lege eta araudien eta bezeroen itxaropenen mende egon daitezke, eredua bereziki kontuan hartzeko diseinatuta ez dagoena. Horregatik, **gomendioak berrikusi behar dituzu zure bezeroei entregatu aurretik** aplikagarriak diren lege edo araudiak eta bezeroen itxaropenak gomenda diezaiokezunaren arabera betetzen dituzula ziurtatzeko.

Eredu honen irteerak produktuaren IDan oinarritutako gomendioak ematen ditu. Zure bidalketa-mekanismoak aurreikusitako produktuen IDak mapatu behar ditu bezeroek lokalizazioa, irudi-edukia eta negozioaren beste eduki edo portaera espezifikoen konturako eduki egokiarekin.

> [!TIP]
> Probatu iragarpen produktuaren gomendioa lagin-datuak erabiliz: [Produktuen gomendioa iragarpen lagin-gida](sample-guide-predict-product-recommendation.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Gutxienez [Kolaboratzaileen baimenak](permissions.md)
- Gutxienez 100 bezero, ahal izanez gero 10.000 bezero baino gehiago.
- Bezeroaren identifikatzailea, transakzioak bezero indibidual batekin lotzeko identifikatzaile bakarra
- Gutxienez urtebeteko transakzio-datuak, ahal dela bizpahiru urte urtaroen bat sartzeko. Egokiena, gutxienez hiru transakzio edo gehiago Bezero ID bakoitzeko. Transakzioen historiak honako hauek izan behar ditu:
  - **Transakzioaren IDa** : erosketa edo transakzio baten identifikatzaile bakarra.
  - **Transakzio data** : Erosketaren edo transakzioaren data.
  - **Transakzioaren balioa** : Erosketaren edo transakzioaren balio numerikoa.
  - **Produktu ID bakarra** : erositako produktuaren edo zerbitzuaren ID zure datuak lerro-elementu mailan badaude.
  - **Erosi edo itzuli** : Egia/gezurra balio boolearra non *egia* transakzio bat itzulera izan zela identifikatzen du. Erosketa edo Itzulketaren datuak ereduan ematen ez badira eta **Transakzioaren balioa** negatiboa da, itzulera ondorioztatzen dugu.
- Produktuen katalogoko datu-entitate bat produktuaren iragazki gisa erabiltzeko.

> [!NOTE]
> - Ereduak zure bezeroen transakzioen historia eskatzen du, non transakzioa erabiltzaile-produktu interakzioa deskribatzen duen edozein datu den. Adibidez, produktu bat erostea, klasea hartzea edo ekitaldi batera joatea.
> - Transakzioen historiako entitate bakarra konfigura daiteke. Erosketa-entitate anitz badaude, konbinatu Power Query datuak sartu aurretik.
> - Ordena eta eskaeraren xehetasunak entitate desberdinak badira, batu haiekin ereduan erabili aurretik. Ereduak ez du entitate bateko eskaera IDarekin edo ordainagiriaren IDarekin soilik funtzionatzen.

## <a name="create-a-product-recommendation-prediction"></a>Sortu produktuak gomendatzeko iragarpena

Hautatu **Gorde zirriborroa** edozein unetan iragarpen zirriborro gisa gordetzeko. Iragarpen zirriborroa atalean bistaratzen da **Nire iragarpenak** fitxa.

1. Joan **Adimena** > **Iragarpenak**.

1. Gainean **Sortu** fitxa, hautatu **Erabili eredua** gainean **Produktuen gomendioak (aurrebista)** teila.

1. Hautatu **Hasi erabiltzen**.

1. **Eman izena eredu honi** eta **Irteerako entitatearen izenari** beste eredu edo entitate batzuetatik bereizteko.

1. Hautatu **Hurrengoa**.

### <a name="define-product-recommendation-preferences"></a>Definitu produktuen gomendioen hobespenak

1. Ezarri **Produktu kopurua** bezero bati gomendatzeko. Balio hori zure bidalketa metodoak datuak nola betetzen dituen araberakoa da.

1. Aukeratu bezeroek aurretik erositako produktuak sartu nahi dituzun **Errepikatu erosketak espero dira** eremua.

1. Ezarri **Begiratu atzera leihoa** produktua erabiltzaileari berriro gomendatu aurretik ereduak kontuan hartzen duen denbora-tartearekin. Adibidez, adierazi bezero batek bi urtean behin ordenagailu eramangarri bat erosten duela. Ereduak azken bi urteetako erosketa-historia aztertzen du, eta elementu bat aurkitzen badu, gomendioetatik iragazten da.

1. Hautatu **Hurrengoa**

### <a name="add-purchase-history"></a>Gehitu erosketa-historia

1. Hautatu **Gehitu datuak** rentzat **Bezeroaren transakzioen historia**.

1. Hautatu jarduera semantikoaren mota **SalesOrderLine** beharrezko transakzio- edo erosketa-historiaren informazioa jasotzen duena. Jarduera konfiguratu ez bada, hautatu **hemen** eta sortu.

1. Azpian **Jarduerak**, jarduera sortu zenean jarduera-atributuak semantikoki mapatu baziren, aukeratu kalkulua zentratu nahi duzun atributu edo entitate zehatzak. Mapa semantikoa gertatu ez bada, hautatu **Editatu** eta mapatu zure datuak.

   :::image type="content" source="media/product-recommendation-select-semantic-activity.PNG" alt-text="Alboko panela, mota semantikoan jarduera jakinak aukeratzeko eragiketa erakusten.":::

1. Hautatu **Hurrengoa** eta eredu honetarako behar diren atributuak berrikusi.

1. Sakatu **Gorde**.

1. Hautatu **Hurrengoa**.

### <a name="add-product-information-and-filters"></a>Gehitu produktuaren informazioa eta iragazkiak

Batzuetan, produktu batzuk bakarrik dira onuragarriak edo egokiak eraikitzen duzun iragarpen motarako. Erabili produktu-iragazkiak ezaugarri zehatzak dituzten produktuen azpimultzo bat identifikatzeko, zure bezeroei gomendatzeko. Ereduak ereduak ikasteko erabilgarri dauden produktu guztiak erabiliko ditu, baina produktuaren iragazkiarekin bat datozen produktuak soilik erabiliko ditu bere irteeran.

1. Gehitu produktu bakoitzaren informazioa duen produktuen katalogoko entitatea. Mapeatu behar den informazioa eta hautatu **Gorde**.

1. Hautatu **Hurrengoa**.

1. Hautatu **Produktu-iragazkiak**:

   - **Ez dago iragazkirik**: Erabili produktu guztiak iragarpen gomendioan.

   - **Produktu iragazki zehatzak zehaztu**: Erabili produktu zehatzak produktuaren gomendioan iragarpen. urtean **Produktuen katalogoko atributuak** panelean, hautatu iragazkian sartu nahi dituzun produktuen katalogoko entitateko atributuak.

     :::image type="content" source="media/product-filters-sidepane.png" alt-text="Produktuen katalogoaren entitatean egotzitako alboko panela, produktuen iragazkiak hautatzeko.":::

1. Aukeratu produktuaren iragazkia erabiltzea nahi duzun **eta** edo **edo** produktuen katalogoko atributuen hautaketa logikoki konbinatzeko.

   :::image type="content" source="media/product-filters-sample.png" alt-text="Produktuen iragazkien laginaren konfigurazioa AND konektoreak logikoekin konbinatuta.":::

1. Hautatu **Hurrengoa**.

### <a name="set-update-schedule"></a>Konfiguratu antolaketaren eguneratzea

1. Aukeratu maiztasun bat zure eredua berriro trebatzeko. Ezarpen hau garrantzitsua da iragarpenen zehaztasuna eguneratzeko, Customer Insights-en datu berriak sartzen diren heinean. Negozio gehienek hilean behin birsortu eta zehaztasun ona lortu dezakete.

1. Hautatu **Hurrengoa**.

### <a name="review-and-run-the-model-configuration"></a>Berrikusi eta exekutatu modeloaren konfigurazioa

The **Berrikusi eta exekutatu** urratsak konfigurazioaren laburpena erakusten du eta iragarpen sortu aurretik aldaketak egiteko aukera ematen du.

1. Hautatu **Editatu** aldaketak berrikusteko eta egiteko edozein urratsetan.

1. Zure hautapenekin pozik bazaude, hautatu **Gorde eta exekutatu** eredua exekutatzen hasteko. Hautatu **Eginda**. The **Nire iragarpenak** fitxa bistaratzen da iragarpen sortzen ari den bitartean. Prozesuak hainbat ordu iraun dezake iragarpenean erabilitako datu kopuruaren arabera.

[!INCLUDE [progress-details](includes/progress-details-pane.md)]

## <a name="view-prediction-results"></a>Ikusi iragarpen emaitzak

1. Joan **Adimena** > **Iragarpenak**.

1. urtean **Nire iragarpenak** fitxan, hautatu ikusi nahi duzun iragarpen.

Emaitzen orrialdean datuen bost atal nagusi daude.

- **Ereduaren errendimendua:** A, B edo C kalifikazioek iragarpen-en errendimendua adierazten dute eta irteerako entitatean gordetako emaitzak erabiltzeko erabakia hartzen lagun zaitzake.
  
  :::image type="content" source="media/product-recommendation-modelperformance.PNG" alt-text="Ereduaren errendimenduaren emaitzaren irudia A kalifikazioarekin.":::

  Kalifikazioak arau hauetan oinarrituta zehazten dira:
  - **A** "Arrakasta @ K" metrika oinarrizko lerroa baino % 10 handiagoa denean.
  - **B** "Arrakasta @ K" metrika oinarrizko lerroa baino % 0 eta % 10 gehiago denean.
  - **C** "Arrakasta @ K" metrika oinarri-lerroa baino txikiagoa denean.
  - **Oinarrizko lerroa** : erosketaren araberako produktu gomendatuenen kopurua bezero guztien artean + ereduak identifikatutako arau ikasiak = bezeroentzako gomendio multzoa. Iragarpenak goiko produktuekin alderatzen dira, produktua erosi zuten bezero kopuruaren arabera kalkulatuta. Bezero batek gutxienez erositako produktuetan ere ikusi den produktu bat gutxienez gomendatutako produktuetan baldin badu, oinarrizko oinarritzat hartzen da. Esate baterako, bezero horietako 10ek produktu gomendatu bat erosi zuten guztira 100 bezeroren artean, oinarri-lerroa % 10ekoa da.
  - **Arrakasta @ K** : Gomendioak bezero guztientzat sortzen dira eta transakzioen denbora-tarteen baliozkotze-multzoarekin alderatzen dira. Esate baterako, 12 hilabeteko aldian, 12. hilabetea baliozkotzeko datu multzo gisa uzten da. Ereduak gutxienez 12. hilean erosiko zenukeen gauza bat iragartzen badu aurreko 11 hilabeteetan ikasitakoaren arabera, bezeroak "Arrakasta @ K" metrika handituko luke.

- **Iradokitako produktu gehienak (kalkuluarekin):** Zure bezeroentzat aurreikusitako lehen bost produktuak.
  
  :::image type="content" source="media/product-recommendation-topproducts.PNG" alt-text="Gomendatutako 5 produktu onenak erakusten dituen grafikoa.":::

- **Gomendio faktore nagusiak:** Ereduak bezeroen transakzioen historia erabiltzen du produktuen gomendioak emateko. Iraganeko erosketetan oinarritutako ereduak ikasten ditu eta bezeroen eta produktuen arteko antzekotasunak aurkitzen ditu. Antzekotasun horiek produktuen gomendioak sortzeko erabiltzen dira.
  Faktore hauek ereduak sortutako produktuaren gomendio batean eragina izan dezakete.
  - **Iraganeko transakzioak** : Gomendatutako produktu bat iraganeko erosketa ereduetan oinarritzen zen. Adibidez, ereduak a gomendatu dezake *Azaleko arku sagua* duela gutxi norbaitek erosi badu *3. azaleko liburua* eta *Azaleko boligrafoa*. Ereduak jakin zuen historikoki bezero askok erosi zutela *Azaleko arku sagua* erosi ondoren *3. azaleko liburua* eta *Azaleko boligrafoa*.
  - **Bezeroen antzekotasuna**: Gomendatutako produktu bat antzeko erosketa ereduak erakusten dituzten beste bezero batzuek erosi zuten historikoki. Adibidez, John gomendatu zuten *Azaleko entzungailuak 2* izan ere, duela gutxi Jennifer eta Bradek erosi dute *Azaleko entzungailuak 2*. Ereduak uste du John Jennifer eta Braden antzekoa dela historikoki erosketa eredu antzekoak izan dituztelako.
  - **Produktuaren antzekotasuna**: Gomendatutako produktu bat bezeroak aurretik erositako beste produktu batzuen antzekoa da. Ereduak bi produktu antzekoak direla uste du elkarrekin edo antzeko bezeroek erosi badituzte. Adibidez, norbaitek gomendio bat jasotzen du *USB biltegiratze unitatea* aurretik erosi dutelako *USB-C-tik USB egokitzailea* eta ereduak hori uste du *USB biltegiratze unitatea* antzekoa da *USB-C-tik USB egokitzailea* erosketa eredu historikoetan oinarrituta.

  Produktuen gomendio guztietan faktore horietako batek edo gehiagok eragiten dute. Eragindako faktore bakoitzak rol bat izan duen gomendioen ehunekoa taula batean ikus daiteke. Hurrengo adibidean, gomendioen % 100ek iraganeko transakzioen eragina izan zuten, % 60ek bezeroen antzekotasunaren eta % 22 produktuaren antzekotasunaren arabera. Pasa zaitez diagramako barren gainean eragin faktoreek zer portzentaia izan duten jakiteko.
  
  :::image type="content" source="media/product-recommendation-keyrecommendationfactors.png" alt-text="Produktuen gomendioak sortzeko ereduak ikasitako gomendio-faktore nagusiak.":::

- **Datuen estatistikak** : ereduak kontuan hartutako transakzio, bezero eta produktu kopuruaren ikuspegi orokorra. Ereduak ikasteko eta produktuen gomendioak sortzeko erabili ziren sarrerako datuetan oinarritzen da.

  :::image type="content" source="media/product-recommendation-datastatistics.png" alt-text="Ereduak ereduak ikasteko erabiltzen dituen sarrera-datuen inguruko datu-estatistikak.":::
  
  Ereduak eskuragarri dauden datu guztiak erabiltzen ditu ereduak ikasteko. Hori dela eta, ereduaren konfigurazioan produktuen iragazketa erabiltzen baduzu, atal honek ereduak ereduak ikasteko aztertu dituen produktuen guztizko kopurua erakusten du, definitutako iragazketa-irizpideekin bat datozen produktu-kopurutik desberdina izan daitekeena. Iragazkia ereduak sortutako irteeran aplikatzen da.

- **Produktu gomendioak:** Ereduaren ustez bezeroak erosiko dituen gomendioen lagin bat. Produktuen katalogo bat gehitzen bada, produktuen IDak produktuen izenekin ordeztuko dira.

  :::image type="content" source="media/product-recommendation-highconfidence.PNG" alt-text="Bezero partikular batzuentzako konfiantza handiko iradokizunak erakusten dituen zerrenda.":::

> [!NOTE]
> Eredu honen irteerako entitatean, *Puntuazioa* gomendioaren neurri kuantitatiboa erakusten du. Ereduak puntuazio altuagoa duten produktuak gomendatzen ditu puntuazio txikiagoa duten produktuen aldean. Partitura ikusteko, joan hona **Datuak** > **Entitateak** eta ikusi eredu honetarako definitu duzun irteera-entitatearen datu-fitxa.

[!INCLUDE [footer-include](includes/footer-banner.md)]
