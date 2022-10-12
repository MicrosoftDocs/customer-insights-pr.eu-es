---
title: Konektatu Common Data Model karpetara Azure Data Lake kontua erabiliz
description: Egin lan Common Data Model-ekin Azure Data Lake Storage erabiliz.
ms.date: 09/29/2022
ms.topic: how-to
author: mukeshpo
ms.author: mukeshpo
ms.reviewer: v-wendysmith
manager: shellyha
searchScope:
- ci-data-sources
- ci-create-data-source
- ci-attach-cdm
- customerInsights
ms.openlocfilehash: c12603b9ed8a814356a0f8d0137e97afc749b87c
ms.sourcegitcommit: be341cb69329e507f527409ac4636c18742777d2
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 09/30/2022
ms.locfileid: "9609927"
---
# <a name="connect-to-data-in-azure-data-lake-storage"></a>Konektatu datuetara Azure Data Lake Storage-en

Sartu datuak Dynamics 365 Customer Insights zure erabiliz Azure Data Lake Storage Gen2 kontua. Datuak sartzea osoa edo gehigarria izan daiteke.

## <a name="prerequisites"></a>Aurrebaldintzak

- Datuak sartzea onartzen du Azure Data Lake Storage *Gen2* kontuak soilik. Ezin dituzu Data Lake Storage Gen1 kontuak erabili datuak irensteko.

- The Azure Data Lake Storage kontua izan behar du [izen-espazio hierarkikoa gaituta](/azure/storage/blobs/data-lake-storage-namespace). Datuak erro karpeta definitzen duen eta entitate bakoitzaren azpikarpetak dituen karpeta formatu hierarkiko batean gorde behar dira. Azpikarpetek datu osoak edo datu gehigarriak izan ditzakete.

- Azure zerbitzuaren entitatearekin autentifikatzeko, ziurtatu zure maizterrean konfiguratuta dagoela. Informazio gehiagorako, ikus [Konektatu batera Azure Data Lake Storage Gen2 kontua Azure zerbitzu nagusi batekin](connect-service-principal.md).

- The Azure Data Lake Storage konektatu eta datuak hartu nahi dituzun Azure eskualde berean egon behar du Dynamics 365 Customer Insights ingurunea. Ez da onartzen beste Azure eskualde bateko datu-biltegi batetik Common Data Model-eko karpeta batera konektatzea. Inguruneko Azure eskualdea ezagutzeko, joan hona **Admin** > **Sistema** > **Buruz** Bezeroen Insights-en.

- Lineako zerbitzuetan biltegiratutako datuak datuak prozesatzen edo gordetzen diren tokian beste leku batean bil daitezke Dynamics 365 Customer Insights.Lineako zerbitzuetan gordetako datuak inportatuz edo konektatuz gero, onartzen duzu datuak batera transferitu eta gorde daitezkeela.Dynamics 365 Customer Insights . [Lortu informazio gehiago Microsoft Trust Center-en](https://www.microsoft.com/trust-center).

- Customer Insights zerbitzuko nagusiak rol hauetako batean egon behar du biltegiratze-kontura atzitzeko. Informazio gehiagorako, ikus [Eman baimenak zerbitzu nagusiari biltegiratze-kontura atzitzeko](connect-service-principal.md#grant-permissions-to-the-service-principal-to-access-the-storage-account).
  - Storage Blob datu-irakurgailua
  - Storage Blob datuen jabea
  - Storage Blob datuen kolaboratzailea

- datu-iturburu konexioa konfiguratzen duen erabiltzaileak Storage Blob Data Contributor baimen gutxien behar ditu biltegiratze-kontuan.

- Zure Data Lake Storage-ko datuek zure datuak biltegiratzeko Common Data Model estandarra jarraitu behar dute eta datu-eredu komunaren manifestua izan behar dute datu-fitxategien eskema irudikatzeko (*.csv edo *.parquet). Manifestuak entitateen xehetasunak eman behar ditu, hala nola entitate-zutabeak eta datu-motak, eta datu-fitxategiaren kokapena eta fitxategi-mota. Informazio gehiagorako, ikus [Common Data Model manifestua](/common-data-model/sdk/manifest). Manifestua ez badago, Storage Blob Data Owner edo Storage Blob Data Contributor sarbidea duten administratzaile erabiltzaileek eskema defini dezakete datuak sartzerakoan.

## <a name="recommendations"></a>Gomendioak

Errendimendu optimoa lortzeko, Customer Insights-ek partizio baten tamaina 1 GB edo txikiagoa izatea gomendatzen du eta karpeta bateko partizio-fitxategien kopuruak 1000 baino gehiago ez izatea gomendatzen du.

## <a name="connect-to-azure-data-lake-storage"></a>Konektatu Azure Data Lake Storage-ra

1. Joan **Datuak** > **Datu-iturburuak**.

1. Hautatu **Gehitu datu-iturburua**.

1. Hautatu **Azure data Lake biltegiratzea**.

   :::image type="content" source="media/data_sources_ADLS.png" alt-text="Elkarrizketa-koadroa Azure Data Lake-rako konexioaren xehetasunak sartzeko." lightbox="media/data_sources_ADLS.png":::

1. Sartu a **Izena** datu-iturburu eta aukerako bat **Deskribapena**. Izenak bakarrik identifikatzen du datu-iturburu eta beheranzko prozesuetan aipatzen da eta ezin da aldatu.

1. Aukeratu aukera hauetako bat **Konektatu biltegia erabiliz**. Informazio gehiagorako, ikus [Konektatu Customer Insights bat Azure Data Lake Storage Gen2 kontua Azure zerbitzu nagusi batekin](connect-service-principal.md).

   - **Azure baliabidea** : Sartu **Baliabidearen ID** . Aukeran, biltegiratze-kontu bateko datuak Azure esteka pribatu baten bidez sartu nahi badituzu, hautatu **Gaitu esteka pribatua**. Informazio gehiagorako, ikus [Esteka pribatuak](security-overview.md#set-up-an-azure-private-link).
   - **Azure harpidetza** : Hautatu **Harpidetza** eta gero **Baliabide taldea** eta **Biltegiratze kontua**. Aukeran, biltegiratze-kontu bateko datuak Azure esteka pribatu baten bidez sartu nahi badituzu, hautatu **Gaitu esteka pribatua**. Informazio gehiagorako, ikus [Esteka pribatuak](security-overview.md#set-up-an-azure-private-link).
  
   > [!NOTE]
   > Rol hauetako bat behar duzu edukiontzian edo biltegiratze-kontuan datu-iturburu sortzeko:
   >
   >  - Storage Blob Data Reader nahikoa da biltegiratze-kontu batetik irakurtzeko eta datuak Customer Insights-era sartzeko.
   >  - Storage Blob Data Contributor edo Owner beharrezkoa da manifest-fitxategiak zuzenean Customer Insights-en editatu nahi badituzu.  
  
1. Aukeratu izena **Edukiontzia** datuak eta eskema (model.json edo manifest.json fitxategia) dituen datuak inportatzeko, eta hautatu **Hurrengoa**.
   > [!NOTE]
   > Inguruneko beste datu-iturburu batekin lotutako model.json edo manifest.json fitxategia ez da zerrendan agertuko. Hala ere, model.json edo manifest.json fitxategi bera erabil daiteke hainbat ingurunetako datu-iturburuetarako.

1. Eskema berri bat sortzeko, joan hona [Sortu eskema fitxategi berri bat](#create-a-new-schema-file).

1. Lehendik dagoen eskema bat erabiltzeko, joan model.json edo manifest.cdm.json fitxategia duen karpetara. Direktorio batean bilatu dezakezu fitxategia aurkitzeko.

1. Hautatu json fitxategia eta hautatu **Hurrengoa**. Eskuragarri dauden entitateen zerrenda bistaratzen da.

   :::image type="content" source="media/review-entities.png" alt-text="Hautatu beharreko entitateen zerrendaren elkarrizketa-koadroa":::

1. Hautatu sartu nahi dituzun entitateak.

   :::image type="content" source="media/ADLS_required.png" alt-text="Lehen mailako gakorako Beharrezkoa erakusten duen elkarrizketa-koadroa":::

   > [!TIP]
   > JSON editatzeko interfaze batean entitate bat editatzeko, hautatu entitatea eta gero **Editatu eskema fitxategia**. Egin aldaketak eta hautatu **Gorde**.

1. Ingestio gehigarria behar duten hautatutako entitateetarako, **Beharrezkoa** azpian agertzen da **Freskatze gehigarria**. Entitate horietako bakoitzari buruz, ikus [Konfiguratu inkrementala freskatze bat Azure Data Lake datu-iturburuetarako](incremental-refresh-data-sources.md).

1. Lehen gako bat definitu ez den hautatutako entitateetarako, **Beharrezkoa** azpian agertzen da **Lehen gakoa**. Erakunde hauetako bakoitzarentzat:
   1. Hautatu **Beharrezkoa**. The **Editatu entitatea** paneleko pantailak.
   1. Aukeratu **Lehen gakoa**. Gako nagusia entitatearen atributu bakarra da. Atributu bat baliozko gako nagusia izan dadin, ez lituzke balio bikoiztuak, falta diren balioak edo balio baliorik sartu behar. Katea, osokoa eta GUID datu motako atributuak gako nagusi gisa onartzen dira.
   1. Aukeran, aldatu partizioaren eredua.
   1. Hautatu **Itxi** panela gorde eta ixteko.

1. Hautatu zenbakia **Atributuak** sartutako entitate bakoitzeko. The **Kudeatu atributuak** orrialdeak bistaratzen ditu.

   :::image type="content" source="media/dataprofiling-entities.png" alt-text="Datuen profila hautatzeko elkarrizketa-koadroa.":::

   1. Sortu atributu berriak, editatu edo ezabatu lehendik dauden atributuak. Izena, datu-formatua alda dezakezu edo mota semantiko bat gehi dezakezu.
   1. Analitika eta beste gaitasun batzuk gaitzeko, hautatu **Datuen profilak egitea** entitate osorako edo atributu zehatzetarako. Lehenespenez, ez dago entitaterik gaituta datu-profilak egiteko.
   1. Hautatu **Eginda**.

1. Sakatu **Gorde**. The **Datu-iturriak** orrialdea irekitzen da datu-iturburu berria erakusten **Freskagarria** egoera.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

Datuak kargatzeak denbora behar dezake. Freskatu arrakastatsu baten ondoren, irentsitako datuak berrikusi daitezke [**Entitateak**](entities.md) orrialdea.

### <a name="create-a-new-schema-file"></a>Sortu eskema fitxategi berri bat

1. Hautatu **Eskema fitxategi berria**.

1. Idatzi izen bat fitxategiarentzat eta hautatu **Gorde**.

1. Hautatu **Entitate berria**. The **Entitate Berria** paneleko pantailak.

1. Sartu entitatearen izena eta aukeratu **Datu-fitxategien kokapena**.
   - **.csv edo .parquet fitxategi anitz** : Arakatu erroko karpetara, hautatu eredu mota eta idatzi esamoldea.
   - **.csv edo .parquet fitxategi bakarrak** : Arakatu .csv edo .parquet fitxategira eta hautatu.

   :::image type="content" source="media/ADLS_new_entity_location.png" alt-text="Elkarrizketa-koadroa Datu fitxategien kokapena nabarmenduta duen entitate berri bat sortzeko.":::

1. Sakatu **Gorde**.

   :::image type="content" source="media/ADLS_new_entity_define_attributes.png" alt-text="Atributuak definitzeko edo automatikoki sortzeko elkarrizketa-koadroa.":::

1. Hautatu **atributuak definitzea** atributuak eskuz gehitzeko edo hautatu **automatikoki sortu**. Atributuak definitzeko, idatzi izen bat, hautatu datu-formatua eta aukerako mota semantikoa. Automatikoki sortutako atributuetarako:

   1. Atributuak automatikoki sortu ondoren, hautatu **Berrikusi atributuak**. The **Kudeatu atributuak** orrialdeak bistaratzen ditu.

   1. Ziurtatu datu-formatua egokia dela atributu bakoitzarentzat.

   1. Analitika eta beste gaitasun batzuk gaitzeko, hautatu **Datuen profilak egitea** entitate osorako edo atributu zehatzetarako. Lehenespenez, ez dago entitaterik gaituta datu-profilak egiteko.

      :::image type="content" source="media/dataprofiling-entities.png" alt-text="Datuen profila hautatzeko elkarrizketa-koadroa.":::

   1. Hautatu **Eginda**. The **Hautatu entitateak** orrialdeak bistaratzen ditu.

1. Jarraitu entitateak eta atributuak gehitzen, hala badagokio.

1. Entitate guztiak gehitu ondoren, hautatu **Sartu** entitateak datu-iturburu ingestioan sartzeko.

   :::image type="content" source="media/ADLS_required.png" alt-text="Lehen mailako gakorako Beharrezkoa erakusten duen elkarrizketa-koadroa":::

1. Ingestio gehigarria behar duten hautatutako entitateetarako, **Beharrezkoa** azpian agertzen da **Freskatze gehigarria**. Entitate horietako bakoitzari buruz, ikus [Konfiguratu inkrementala freskatze bat Azure Data Lake datu-iturburuetarako](incremental-refresh-data-sources.md).

1. Lehen gako bat definitu ez den hautatutako entitateetarako, **Beharrezkoa** azpian agertzen da **Lehen gakoa**. Erakunde hauetako bakoitzarentzat:
   1. Hautatu **Beharrezkoa**. The **Editatu entitatea** paneleko pantailak.
   1. Aukeratu **Lehen gakoa**. Gako nagusia entitatearen atributu bakarra da. Atributu bat baliozko gako nagusia izan dadin, ez lituzke balio bikoiztuak, falta diren balioak edo balio baliorik sartu behar. Katea, osokoa eta GUID datu motako atributuak gako nagusi gisa onartzen dira.
   1. Aukeran, aldatu partizioaren eredua.
   1. Hautatu **Itxi** panela gorde eta ixteko.

1. Sakatu **Gorde**. The **Datu-iturriak** orrialdea irekitzen da datu-iturburu berria erakusten **Freskagarria** egoera.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

Datuak kargatzeak denbora behar dezake. Freskatu arrakastatsu baten ondoren, irentsitako datuak berrikusi daitezke [**Entitateak**](entities.md) orrialdea.

## <a name="edit-an-azure-data-lake-storage-data-source"></a>Editatu an Azure Data Lake Storage datu-iturburu

Eguneratu dezakezu *Konektatu biltegiratze-kontura erabiliz* aukera. Informazio gehiagorako, ikus [Konektatu Customer Insights bat Azure Data Lake Storage Gen2 kontua Azure zerbitzu nagusi batekin](connect-service-principal.md). Biltegiratze kontutik beste edukiontzi batera konektatu nahi baduzu edo kontuaren izena aldatu nahi baduzu [datu-iturburu konexio berria sortu](#connect-to-azure-data-lake-storage).

1. Joan **Datuak** > **Datu-iturburuak**.

1. Eguneratu nahi duzun datu-iturburu-aren ondoan, hautatu **Editatu**.

   :::image type="content" source="media/data_sources_edit_ADLS.png" alt-text="Azure Data Lake datu-iturburu editatzeko elkarrizketa-koadroa.":::

1. Aldatu informazio hauetako bat:

   - **Deskribapenak**
   - **Konektatu biltegia erabiliz** eta konexio informazioa. Ezin duzu aldatu **Edukiontzia**-ren informazioa konexioa eguneratzean.
      > [!NOTE]
      > Biltegiratze-kontuari edo edukiontziari eginkizun hauetako bat esleitu behar zaio:
        > - Storage Blob datu-irakurgailua
        > - Storage Blob datuen jabea
        > - Storage Blob datuen kolaboratzailea

   - **Gaitu esteka pribatua** biltegiratze-kontu bateko datuak Azure esteka pribatu baten bidez sartu nahi badituzu. Informazio gehiagorako, ikus [Esteka pribatuak](security-overview.md#set-up-an-azure-private-link).

1. Hautatu **Hurrengoa**.
1. Aldatu hurrengoetako bat:
   - Nabigatu beste model.json edo manifest.json fitxategi batera edukiontziko beste entitate multzo batekin.
   - Irensteko entitate gehigarriak gehitzeko, hautatu **Entitate berria**.
   - Mendekotasunik ez badago jada hautatutako entitateak kentzeko, hautatu entitatea eta **Ezabatu**.
      > [!IMPORTANT]
      > Lehendik dauden model.json edo manifest.json fitxategiaren eta entitateen multzoaren menpekotasunak badaude, errore mezu bat ikusiko duzu eta ezin duzu model.json edo manifest.json fitxategi desberdin bat hautatu. Kendu mendekotasun horiek model.json edo manifest.json fitxategia aldatu aurretik edo sortu datu-iturburu berri bat mendekotasunak ez kentzeko erabili nahi dituzun model.json edo manifest.json fitxategiarekin.
   - Datu-fitxategiaren kokapena edo gako nagusia aldatzeko, hautatu **Editatu**.
   - Irensteko datu gehigarriak aldatzeko, ikus [Konfiguratu inkrementala freskatze bat Azure Data Lake datu-iturburuetarako](incremental-refresh-data-sources.md).
   - Aldatu soilik entitatearen izena .json fitxategiko entitatearen izenarekin bat etor dadin.

     > [!NOTE]
     > Mantendu beti Customer Insights-en entitatearen izena model.json edo manifest.json fitxategiaren barruan dagoen entitatearen izenaren berdina sartu ondoren. Customer Insights-ek entitate-izen guztiak baliozkotzen ditu model.json edo manifest.json-ekin sistemaren freskatze bakoitzean. Entitate-izen bat Customer Insights barruan edo kanpoan aldatzen bada, errore bat gertatuko da Customer Insights-ek ezin duelako aurkitu .json fitxategian entitate-izen berria. Hartutako entitatearen izena ustekabean aldatu bada, editatu entitatearen izena Customer Insights-en .json fitxategiko izenarekin bat etor dadin.

1. Hautatu **Atributuak** atributuak gehitzeko edo aldatzeko, edo datuen profila gaitzeko. Ondoren, sakatu **Eginda**.

1. Egin klik **Gorde** zure aldaketak aplikatzeko eta itzultzeko **Datu-iturriak** orrialdea.

   [!INCLUDE [progress-details-include](includes/progress-details-pane.md)]

## <a name="common-reasons-for-ingestion-errors-or-corrupt-data"></a>Irenste-akatsen edo datuak hondatzearen ohiko arrazoiak

Datuak sartzen direnean, erregistro bat hondatuta har daitekeen arrazoi ohikoenetako batzuk hauek dira:

- Datu-motak eta eremu-balioak ez datoz bat iturburu-fitxategiaren eta eskemaren artean
- Iturburu-fitxategiko zutabe kopurua ez dator bat eskemarekin
- Eremuek zutabeak okertzea eragiten duten karaktereak dituzte espero den eskemarekin alderatuta. Adibidez: gaizki formateatutako komatxoak, ihesik gabeko komatxoak, lerro berriko karaktereak edo fitxadun karaktereak.
- Partizio fitxategiak falta dira
- Datetime/date/datetimeoffset zutabeak badaude, haien formatua eskeman zehaztu behar da formatu estandarra jarraitzen ez badu.

### <a name="schema-or-data-type-mismatch"></a>Eskema edo datu-mota ez datoz bat

Datuak eskemarekin bat ez badatoz, sartze-prozesua akatsekin amaitzen da. Zuzendu iturburuko datuak edo eskema eta sartu berriro datuak.

### <a name="partition-files-are-missing"></a>Partizio fitxategiak falta dira

- Ingestioa arrakastatsua izan bada erregistro hondatu gabe, baina ezin baduzu daturik ikusi, editatu model.json edo manifest.json fitxategia partizioak zehaztuta daudela ziurtatzeko. Orduan, [freskatu datu-iturburu](data-sources.md#refresh-data-sources).

- Programazio automatikoko freskatze batean datu-iturriak freskatzen diren aldi berean datu-ingurketa gertatzen bada, baliteke partizio-fitxategiak hutsik egotea edo erabilgarri ez egotea Customer Insights-ek prozesatzeko. Goragoko freskatze programazioarekin bat egiteko, aldatu [sistema freskatzeko programazioa](schedule-refresh.md) edo datu-iturburu-ren freskatze ordutegia. Lerrokatu denborak, freskaketak guztiak aldi berean gerta ez daitezen eta Customer Insights-en prozesatu beharreko azken datuak eskaintzeko.

### <a name="datetime-fields-in-the-wrong-format"></a>Data-orduaren eremuak formatu okerrean

Entitateko data-orduaren eremuak ez daude ISO 8601 edo en-US formatuan. Customer Insights-en data-orduaren formatu lehenetsia en-US formatua da. Entitate bateko data-ordu-eremu guztiek formatu berean egon behar dute. Customer Insights-ek beste formatu batzuk onartzen ditu, baldin eta oharrak edo ezaugarriak ereduan edo manifest.json iturburuan edo entitate mailan egiten badira. Adibidez:

**Model.json**

   ```json
      "annotations": [
        {
          "name": "ci:CustomTimestampFormat",
          "value": "yyyy-MM-dd'T'HH:mm:ss:SSS"
        },
        {
          "name": "ci:CustomDateFormat",
          "value": "yyyy-MM-dd"
        }
      ]   
   ```

  Manifest.json batean, datetime formatua entitate mailan edo atributu mailan zehaztu daiteke. Entitate mailan, erabili "exhibitsTraits" *.manifest.cdm.json entitatean data-ordu formatua definitzeko. Atributu mailan, erabili "appliedTraits" entityname.cdm.json atributuan.

**Manifest.json entitate mailan**

```json
"exhibitsTraits": [
    {
        "traitReference": "is.formatted.dateTime",
        "arguments": [
            {
                "name": "format",
                "value": "yyyy-MM-dd'T'HH:mm:ss"
            }
        ]
    },
    {
        "traitReference": "is.formatted.date",
        "arguments": [
            {
                "name": "format",
                "value": "yyyy-MM-dd"
            }
        ]
    }
]
```

**Entity.json atributu mailan**

```json
   {
      "name": "PurchasedOn",
      "appliedTraits": [
        {
          "traitReference": "is.formatted.date",
          "arguments" : [
            {
              "name": "format",
              "value": "yyyy-MM-dd"
            }
          ]
        },
        {
          "traitReference": "is.formatted.dateTime",
          "arguments" : [
            {
              "name": "format",
              "value": "yyyy-MM-ddTHH:mm:ss"
            }
          ]
        }
      ],
      "attributeContext": "POSPurchases/attributeContext/POSPurchases/PurchasedOn",
      "dataFormat": "DateTime"
    }
```

[!INCLUDE [footer-include](includes/footer-banner.md)]
