---
title: Konektatu Azure Data Lake Storage kontu nagusia Azure zerbitzuaren nagusia erabiliz
description: Erabili Azure zerbitzu nagusia zure data lake konektatzeko.
ms.date: 08/12/2022
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-system-security
- customerInsights
ms.openlocfilehash: eba10068c48db5c147100c25a397bcc13b014784
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304182"
---
# <a name="connect-to-an-azure-data-lake-storage-account-by-using-an-azure-service-principal"></a>Konektatu Azure Data Lake Storage kontu nagusia Azure zerbitzuaren nagusia erabiliz

Dynamics 365 Customer Insights batera konektatzeko aukera eskaintzen du Azure Data Lake Storage kontua Azure zerbitzu nagusi bat erabiliz biltegiratze-kontuaren gakoen ordez.

Azure zerbitzuak erabiltzen dituzten tresna automatizatuek baimen mugatuak izan behar dituzte. Aplikazioek erabiltzaile pribilegiatu gisa saioa hasi beharrean, Azure-k zerbitzuaren entitateak eskaintzen ditu. Erabili zerbitzu nagusiak segurtasunez [gehitu edo editatu Common Data Model karpeta bat datu-iturburu gisa](connect-common-data-model.md) edo [ingurune bat sortu edo eguneratu](create-environment.md).

## <a name="prerequisites"></a>Aurrebaldintzak

- Zerbitzu nagusia erabiliko duen Data Lake Storage kontuak Gen2 izan behar du. Azure Data Lake Gen1 biltegiratze-kontuak ez dira onartzen.
- Data Lake Storage kontuak dauka [izen-espazio hierarkikoa gaituta](/azure/storage/blobs/data-lake-storage-namespace).
- Zure Azure maizter administratzaile-baimenak, zerbitzu nagusi berri bat sortu behar baduzu.

## <a name="create-an-azure-service-principal-for-customer-insights"></a>Sortu Azure zerbitzu nagusia Customer Insights-entzat

Customer Insights-en zerbitzu nagusi berri bat sortu aurretik, egiaztatu zure erakundean dagoeneko badagoen. Kasu gehienetan, dagoeneko existitzen da.

### <a name="look-for-an-existing-service-principal"></a>Bilatu lehendik dagoen zerbitzuaren entitatea

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

2. Hurrengoan **Azure zerbitzuak**, hautatu **Azure Active Directory**.

3. Azpian **Kudeatu**, hautatu **Microsoft aplikazioa**.

4. Gehitu iragazki bat **Aplikazioaren IDarekin hasten da**`0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` edo bilatu izena `Dynamics 365 AI for Customer Insights`.

5. Bat datorren erregistroa aurkitzen baduzu, esan nahi du zerbitzuaren nagusia dagoeneko badagoela. [Eman baimenak](#grant-permissions-to-the-service-principal-to-access-the-storage-account) zerbitzu nagusiak biltegiratze-kontura sartzeko.

   :::image type="content" source="media/ADLS-SP-AlreadyProvisioned.png" alt-text="Lehendik dagoen zerbitzu nagusia erakusten duen pantaila-argazkia.":::

6. Emaitzarik itzultzen ez bada, [zerbitzu nagusi berri bat sortu](#create-a-new-service-principal).

### <a name="create-a-new-service-principal"></a>Sortu zerbitzuaren entitatea

1. Instalatu azken bertsioa Azure Active Directory PowerShell for Graph. Informazio gehiagorako, joan hona [Instalatu Azure Active Directory PowerShell grafikorako](/powershell/azure/active-directory/install-adv2).

   1. Zure ordenagailuan, sakatu teklatuko Windows tekla eta bilatu **Windows PowerShell** eta hautatu **Exekutatu administratzaile gisa**.

   1. Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.

2. Sortu Customer Insights zerbitzuaren nagusia Azure AD PowerShell modulua.

   1. PowerShell leihoan, sartu `Connect-AzureAD -TenantId "[your Directory ID]" -AzureEnvironmentName Azure`. Ordezkatu *[zure direktorioa ID]* zerbitzu nagusia sortu nahi duzun zure Azure harpidetzaren benetako Directory IDarekin. `AzureEnvironmentName` ingurunearen izenaren parametroa aukerakoa da.
  
   1. Idatzi `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`. Komando honek Customer Insights zerbitzu nagusia sortzen du hautatutako Azure harpidetzan.

## <a name="grant-permissions-to-the-service-principal-to-access-the-storage-account"></a>Eman baimenak zerbitzuaren entitateari biltegiratze kontura sartzeko

Customer Insights-en erabili nahi duzun biltegiratze-kontuaren zerbitzu nagusiari baimenak emateko, rol hauetako bat esleitu behar zaio biltegiratze-kontuari edo edukiontziari:

|Kredentziala|Eskakizunak|
|----------|------------|
|Momentu honetan saioa hasita dagoen erabiltzailea|**Rola** : biltegiratze-blob datu-irakurlea, biltegiratze-blob laguntzailea edo biltegiratze-blob-en jabea.<br>**Maila** : Biltegiratze-kontuan edo edukiontzian emandako baimenak.</br>|
|Bezeroei buruzko informazio-zerbitzu nagusia -<br>Erabiliz Azure Data Lake Storage datu-iturburu gisa</br>|1. aukera<ul><li>**Rola** : biltegiratze blob datu-irakurlea, biltegiratze blob datuen laguntzailea edo biltegiratze blob datuen jabea.</li><li>**Maila** : Biltegiratze-kontuan emandako baimenak.</li></ul>2. aukera *(Zerbitzu nagusia biltegiratze konturako sarbidea partekatu gabe)*<ul><li>**1. rola** : biltegiratze blob datu-irakurlea, biltegiratze blob datuen laguntzailea edo biltegiratze blob datuen jabea.</li><li>**Maila** : edukiontziari emandako baimenak.</li><li>**2. rola** : Biltegiratze Blob Datuen Delegatzailea.</li><li>**Maila** : Biltegiratze-kontuan emandako baimenak.</li></ul>|
|Bezeroei buruzko informazio-zerbitzu nagusia - <br>Erabiliz Azure Data Lake Storage irteera edo helmuga gisa</br>|1. aukera<ul><li>**Rola** : Storage Blob datuen laguntzailea edo Storage Blob jabea.</li><li>**Maila** : Biltegiratze-kontuan emandako baimenak.</li></ul>2. aukera *(Zerbitzu nagusia biltegiratze konturako sarbidea partekatu gabe)*<ul><li>**Rola** : Storage Blob datuen laguntzailea edo Storage Blob jabea.</li><li>**Maila** : edukiontziari emandako baimenak.</li><li>**2. rola** : Biltegiratze blob delegatzailea.</li><li>**Maila** : Biltegiratze-kontuan emandako baimenak.</li></ul>|

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

1. Ireki Customer Insights zerbitzu nagusiak sarbidea izan dezan nahi duzun biltegiratze-kontua.

1. Ezkerreko panelean, hautatu **Sarbide kontrola (IAM)** eta, ondoren, hautatu **Gehitu** > **Gehitu rol esleipena**.

   :::image type="content" source="media/ADLS-SP-AddRoleAssignment.png" alt-text="Azure ataria erakusten duen pantaila-argazkia eginkizuna esleitzen duzun bitartean.":::

1. Gainean **Gehitu rol esleipena** panelean, ezarri propietate hauek:
   - **Rola** : biltegiratze-blob datu-irakurlea, biltegiratze-blob laguntzailea edo biltegiratze-blob-jabea goian zerrendatutako kredentzialetan oinarrituta.
   - **Esleitu sarbidea** :**Erabiltzailea, taldea edo zerbitzu nagusia**
   - **Hautatu** kideak: **Dynamics 365 AI Customer Insights-erako** (a [zerbitzu nagusia](#create-a-new-service-principal) prozedura honetan lehenago begiratu duzu)

1. Hautatu **Berrikusi + esleitu**.

Baliteke aldaketak barreiatzeko 15 minutu behar izatea.

## <a name="enter-the-azure-resource-id-or-the-azure-subscription-details-in-the-storage-account-attachment-to-customer-insights"></a>Sartu Azure baliabideen IDa edo Azure harpidetzaren xehetasunak Customer Insights biltegiratze-kontuaren eranskinean

Erantsi Data Lake Storage kontu bat Customer Insights-en [irteerako datuak gordetzea](manage-environments.md) edo [erabili datu-iturburu gisa](connect-dataverse-managed-lake.md). Aukeratu a [baliabideetan oinarrituta](#resource-based-storage-account-connection) edo a [harpidetzan oinarrituta](#subscription-based-storage-account-connection) hurbildu eta jarraitu urrats horiei.

### <a name="resource-based-storage-account-connection"></a>Baliabideetan oinarritutako biltegiratze-kontuaren konexioa

1. Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.

1. Ezkerreko panelean, joan hona **Ezarpenak** > **Amaiera-puntuak**.

1. Kopiatu biltegiratze kontuaren baliabidearen ID balioa.

   :::image type="content" source="media/ADLS-SP-ResourceId.png" alt-text="Kopiatu biltegiratze kontuaren baliabidearen IDa.":::

1. Customer Insights-en, sartu baliabidearen IDa biltegiratze-kontuaren konexio-pantailan bistaratzen den baliabideen eremuan.

   :::image type="content" source="media/ADLS-SP-ResourceIdConnection.png" alt-text="Idatzi biltegiratze kontuaren baliabidearen IDaren informazioa.":::

1. Jarraitu Customer Insights-en gainerako urratsekin biltegiratze-kontua eransteko.

### <a name="subscription-based-storage-account-connection"></a>Harpidetzetan oinarritutako biltegiratze-kontuaren konexioa

1. Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.

1. Ezkerreko panelean, joan hona **Ezarpenak** > **Ezaugarriak**.

1. Berrikusi **Harpidetza**, **taldea**, eta **Izena** biltegiratze-kontuaren Customer Insights-en balio egokiak hautatzen dituzula ziurtatzeko.

1. Customer Insights-en, hautatu biltegiratze-kontua eransterakoan dagozkien eremuen balioak.

1. Jarraitu Customer Insights-en gainerako urratsekin biltegiratze-kontua eransteko.

[!INCLUDE [footer-include](includes/footer-banner.md)]
