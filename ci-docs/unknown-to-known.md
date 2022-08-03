---
title: Pertsonalizatu zure esperientziak erabiltzaile ezagunei eta ezezagunei buruzko datuekin
description: Sartu lehen ezezagun erabiltzaileei buruzko informazioa haien identitatea ezagutzen duzunean.
ms.date: 07/07/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: conceptual
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-system-diagnostic
- customerInsights
ms.openlocfilehash: ff99721bef0004bc8cae1ec14ff9df16cbb0682e
ms.sourcegitcommit: ece8ff732490ecd3b3421ab273f331e6fd46a7f7
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/19/2022
ms.locfileid: "9173810"
---
# <a name="personalize-your-experiences-with-data-about-known-and-unknown-users"></a>Pertsonalizatu zure esperientziak erabiltzaile ezagunei eta ezezagunei buruzko datuekin

Bezeroen datuak kudeatzea ez da erronka berria, baina gero eta zailagoa da erabiltzaileek markek eskaintzen dituzten kanal digital ezberdinetan nabigatzen duten heinean. Kanal batean ezagutzen (autentifikatu) den erabiltzailea ezezagun bihurtzen da (autentifikatu gabe) beste batean saioa hasi ezean. Arazoa da askotan autentifikatu gabeko erabiltzaileek (ezezagunak) ez dutela ID komunik. Profilen atributu esanguratsuak lotzeko eta bezeroen profil bateratuak sortzeko erabil liteke. Customer Insights-ek arazo hau konpontzen laguntzen du zure iturburu-sistemetako jarraipen-metodoetako datuak irensten. Profil ezezagun eta ezagun bateratuek erakundeei profil eguneratuen eta haien transakzio, jokabide eta datu demografiko historikoen ikuspegi osoa eskaintzen diete. Are gehiago, urrats bat gehiago ematen du, bezeroen jarduera hainbat kanaletan bateratzeko aukera ematen duen identitate-ebazpena eskainiz, besteak beste, zure webgunea, dendako erosketa, leialtasun programak eta abar.

## <a name="sample-scenario"></a>Laginaren egoera

Pentsa dezagun kafe-kate batean, bezero-base zabala duen kafea eta janaria dendetan erosi eta produktuak sarean eskatzeko. Sarritan, lineako bisitariak ez dira autentifikatzen produktuak arakatzean, eta "erabiltzaile ezezagun" bihurtzen dira. Kafe-katearentzat zaila da eskaintza eta esperientzia pertsonalizatuak ematea, erabiltzaileak ezezagunak badira. Bestalde, bezeroak beren kontuan saioa hasi eta enpresaren "erabiltzaile ezagunak" bihur daitezke leialtasun-sistema batean sartuz, eta horrek esperientzia pertsonalizatuagoak ahalbidetzen ditu. Customer Insights-ek kafe-kateari erabiltzaile ezagunei eta lehen ezezagunei buruzko informazioa lortzen lagun diezaioke.

Customer Insights-ekin, konpainiak bezeroen profilak konbina ditzake autentifikatu gabeko (ezezagunak) saioetako jardueren datuekin, erabiltzailea saioa hasi eta ezaguna egin ondoren. Kafe-kateak beste datu-iturri batzuetako datuak ekar ditzake Customer Insights-en konektore integratuak erabiliz, hainbat kanaletako bezeroen identitateak batzeko.

## <a name="prerequisites"></a>Aurrebaldintzak

- Webeko datuak biltzen dira eta bisitari guztien "bisitarien IDak" dituzte.
- Webeko datuek "erabiltzaile ID autentifikatuak" dituzte saioa hasi duten bisitarientzat. NAN hauek leialtasun sistemarekin lotuta daude.
- Balio handiko gertaeren datuak, hala nola, "Produktuaren ikuspegia" eta "Ordenatzea" bezalako datuak iturburuko datuetan definitzen eta sartzen dira, gertaeraren denbora-zigiluarekin eta gertaeren ID batekin batera.

Ondorengo taulak balio handiko web-gertaerak nola har ditzaketen adibide sinplifikatu bat erakusten du.

|Gertaeraren ID|Gertaera-ordu-zigilua|Erabiltzaile ID|LeialtasunaID|Gertaeraren izena|
|--|--|--|--|--|
|1|07-23-2022 10:00:00|abc123|--|Produktuen ikuspegia|
|2|07-23-2022 10:05:00|abc123|707|Leialtasun-saioa|
|3|07-23-2022 10:10:00|abc123|707|Amaitu erosketa|
|4|07-23-2022 10:20:00|xyz789|--|Produktuen ikuspegia|

## <a name="data-ingestion"></a>Datu-horniketa

Bezeroei buruzko datuak zure webgunetik sor daitezke gertaeren datu gisa eta zure barneko edo hirugarrenen datuen analisi-zerbitzuetan gorde daitezke. Webguneko datuek erabiltzaile ezagunak eta ezezagunak dituzte webguneak autentifikazio-zerbitzu batekin integratzen den autentifikazio-fluxua badu. Adibidez, erosketa-transakzio bat amaitzeko erabiltzaileek xehetasun osoak eman behar dituzten merkataritza elektronikoko sistema. Edo sarien deskontuen baliozko hartzailea berresteko autentifikazioa behar duen leialtasun-sistema bat.

Goiko adibideko gertaeren datuek erabiltzaile ezagunen eta ezezagunen profil ID desberdinak dituzte. 1. eta 4. gertaeretan, erabiltzaileak ezezagunak dira, 2. eta 3. ekitaldian abc123 IDa duen erabiltzaileak fidelizazio programa batean izena ematen du.

:::image type="content" source="media/website-data-source.png" alt-text="Datu-iturriak Contoso webgunea barne.":::

Datuak sartzeko dauden aukerei buruzko informazio gehiago lortzeko, ikus [Datu iturrien ikuspegi orokorra](data-sources.md).

## <a name="data-unification"></a>Datuak bateratzea

Identitate ezezagunekin identitate ezagunekin bat egiteak erabiltzaileen jokabideetan oinarritutako pertsonalizazioa gaitzen laguntzen du, edozein dela ere bere profilaren egoera (ezaguna edo ezezaguna). Erabiltzaile guztien eduki pertsonalizatuak bezeroei une horretan interesatzen zaizkien produktu edo zerbitzu garrantzitsuenetara azkar iristen laguntzen die.

Gure datuetako erabiltzaile batzuk ezagunak direnez, Customer Insights erabil dezakegu datu horiek erabiltzailearen profilarekin konbinatzeko. Bezeroen profilak bateratzeari buruzko informazio gehiago lortzeko, ikus [Datuen bateratzearen ikuspegi orokorra](data-unification.md).

1. Hautatu iturburu-eremuak web-datuen entitateko. Erabili zure web-datuetan gordeta dauden profileko datuak eta hautatu datu demografikoekin IDak adierazten dituzten eremuak.

   :::image type="content" source="media/website-source-fields.png" alt-text="Weberako iturburu-eremuak datu-iturburu.":::

1. Gehitu arauak bikoiztutako erregistroak batzeko. Webeko datuetarako, aukeratu gehien betetako datuak.

1. Konfiguratu partida-arauak eta baldintzak. Adibide honetako web-profilen gertaeren datuak IDetan bat egingo dute bezeroen informazioa duten beste datu-iturrietako profilekin. Konfiguratu IDen bat-etortze-arau zehatzak arau bereizi gisa, dagokion gako nagusi bat edo ID bat-etortzea duten beste profil-entitate bakoitzarekin. Adibidean, web-gertaeren profilaren datuak bat datorren azken entitate gisa erabiltzen dira, beste profilaren datuak lehenik konbinatzeko.
   1. Ez egiaztatzen **Sartu erregistro guztiak** erabiltzaile ezagunentzako profil bateratuak sortzen ditu eta dagozkion erabiltzaile ID ezezagunak sartzen ditu. Lagungarria da oraindik ezezagunak ziren erabiltzaile ezagunen iraganeko jokabide-jarduerak ikusteko interesa duzun agertokietan.
   1. Egiaztatzea **Sartu erregistro guztiak** erabiltzaile ezezagunentzako profil-erregistro bereiziak sortzen ditu. Erabiltzaile ezezagunek bezeroaren ID esklusibo bat lortzen dute. Etorkizunean profil ezagun bat sareko gertaeren profilaren datuetan erlazionatzen denean, ezagutu berri den erabiltzailearen bidaia ikusi eta pertsonalizatzeko erabili ahal izango da iraganeko portaera-datu ezezagunetan oinarrituta.

:::image type="content" source="media/website-match-rule.png" alt-text="datu-iturburu entitatearen parekatze-araua.":::

## <a name="get-insights"></a>Lortu xehetasunak

Erabiltzaile ezezagun eta ezagunentzat bezeroen profilak sortzen badira, balio handiko web gertaeren datuak gisa erabil daitezke [jarduerak](activities.md). Jarduera hauek informazio gehiago sortzeko erabil daitezke. Adibidez, duela sei hilabete webgune bat bisitatu zuten bezeroek (oraindik ezezagunak zirenean) edo leialtasun-identifikaziorik ez duten bezeroek ez zuten inoiz ordainketarik egin.

:::image type="content" source="media/website-known-unknown.png" alt-text="Bezeroen orriaren pantaila-argazkia bezero ezagunekin eta ezezagunekin.":::

[Aberastu](enrichment-hub.md) zure datuak, eraiki [neurriak](measures.md), eta sortu [segmentuak](segments.md) gehiago aktibatzeko.

Esaterako, produktu batzuk begiratu baina ordainketa amaitu ez duten erabiltzaile ezagunen segmentuak sor ditzakezu.

Informazio gehiagorako, ikus [Segmentuen ikuspegi orokorra](segments.md).

## <a name="activate-insights"></a>Aktibatu estatistikak

Hainbat modu daude zure datuak esportatzeko eta azpiko informazioetan oinarritutako neurriak hartzeko.

Informazio gehiagorako, ikus [Esportazioen ikuspegi orokorra](export-destinations.md).
