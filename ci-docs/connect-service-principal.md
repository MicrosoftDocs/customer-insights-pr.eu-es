---
title: Konektatu Azure Data Lake Storage kontu nagusia zerbitzuaren nagusia erabiliz
description: Erabili Azure zerbitzu nagusia zure data lake konektatzeko.
ms.date: 04/26/2022
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
searchScope:
- ci-system-security
- customerInsights
ms.openlocfilehash: 776eee79c25edbd40ed119510a314f5126933c3e
ms.sourcegitcommit: a50c5e70d2baf4db41a349162fd1b1f84c3e03b6
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/11/2022
ms.locfileid: "8739147"
---
# <a name="connect-to-an-azure-data-lake-storage-account-by-using-an-azure-service-principal"></a>Konektatu Azure Data Lake Storage kontu nagusia Azure zerbitzuaren nagusia erabiliz

Artikulu honek nola konektatu eztabaidatzen du Dynamics 365 Customer Insights batekin Azure Data Lake Storage kontua Azure zerbitzu nagusi bat erabiliz biltegiratze-kontuaren gakoen ordez. 

Azure zerbitzuak erabiltzen dituzten tresna automatizatuek beti baimen mugatuak izan behar dituzte. Aplikazioek erabiltzaile pribilegiatu gisa saioa hasi beharrean, Azure-k zerbitzuaren entitateak eskaintzen ditu. Zerbitzu nagusiak modu seguruan erabil ditzakezu [gehitu edo editatu Common Data Model karpeta bat datu-iturburu gisa](connect-common-data-model.md) edo [ingurune bat sortu edo eguneratu](create-environment.md).

> [!IMPORTANT]
> - Zerbitzu nagusia erabiliko duen Data Lake Storage kontuak Gen2 izan behar du eta eduki [izen-espazio hierarkikoa gaituta](/azure/storage/blobs/data-lake-storage-namespace). Azure Data Lake Gen1 biltegiratze-kontuak ez dira onartzen.
> - Zure Azure harpidetzarako administratzaile-baimenak behar dituzu zerbitzu nagusi bat sortzeko.

## <a name="create-an-azure-service-principal-for-customer-insights"></a>Sortu Azure zerbitzu nagusia Customer Insights-entzat

Customer Insights-en zerbitzu nagusi berri bat sortu aurretik, egiaztatu zure erakundean dagoeneko badagoen.

### <a name="look-for-an-existing-service-principal"></a>Bilatu lehendik dagoen zerbitzuaren entitatea

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

2. Hurrengoan **Azure zerbitzuak**, hautatu **Azure Active Directory**.

3. **Kudeatu** atalean, hautatu **Enpresaren aplikazioak**.

4. Gehitu iragazki bat **Aplikazioaren IDarekin hasten da**`0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` edo bilatu izena `Dynamics 365 AI for Customer Insights`.

5. Bat datorren erregistroa aurkitzen baduzu, esan nahi du zerbitzuaren nagusia dagoeneko badagoela. 
   
   :::image type="content" source="media/ADLS-SP-AlreadyProvisioned.png" alt-text="Lehendik dagoen zerbitzu nagusia erakusten duen pantaila-argazkia.":::
   
6. Emaitzarik ematen ez bada, sortu zerbitzuaren entitatea.

### <a name="create-a-new-service-principal"></a>Sortu zerbitzuaren entitatea

1. Instalatu azken bertsioa Azure Active Directory PowerShell for Graph. Informazio gehiagorako, joan hona [Instalatu Azure Active Directory PowerShell grafikorako](/powershell/azure/active-directory/install-adv2).

   1. Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta hautatu **Exekutatu administratzaile gisa**.
   
   1. Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.

2. Sortu Customer Insights zerbitzuaren nagusia Azure AD PowerShell modulua.

   1. PowerShell leihoan, sartu `Connect-AzureAD -TenantId "[your Directory ID]" -AzureEnvironmentName Azure`. Ordezkatu *[zure direktorioa ID]* zerbitzu nagusia sortu nahi duzun zure Azure harpidetzaren benetako Directory IDarekin. `AzureEnvironmentName` ingurunearen izenaren parametroa aukerakoa da.
  
   1. Idatzi `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`. Komando honek Customer Insights zerbitzu nagusia sortzen du hautatutako Azure harpidetzan. 

## <a name="grant-permissions-to-the-service-principal-to-access-the-storage-account"></a>Eman baimenak zerbitzuaren entitateari biltegiratze kontura sartzeko

Joan Azure atarira Customer Insights-en erabili nahi duzun biltegiratze-kontuaren zerbitzu nagusiari baimenak emateko.

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

1. Ireki Customer Insights zerbitzu nagusiak sarbidea izan dezan nahi duzun biltegiratze-kontua.

1. Ezkerreko panelean, hautatu **Sarbide kontrola (IAM)** eta, ondoren, hautatu **Gehitu** > **Gehitu rol esleipena**.

   :::image type="content" source="media/ADLS-SP-AddRoleAssignment.png" alt-text="Azure ataria erakusten duen pantaila-argazkia eginkizuna esleitzen duzun bitartean.":::

1. Gainean **Gehitu rol esleipena** panelean, ezarri propietate hauek:
   - Funtzioa: **Biltegiratze blob-aren datuen kolaboratzailea**
   - Esleitu sarbidea hauei: **Erabiltzailea, taldea edo zerbitzuaren entitatea**
   - Aukeratu kideak: **Dynamics 365 AI Customer Insights-erako** (a [zerbitzu nagusia](#create-a-new-service-principal) prozedura honetan lehenago sortu zenuen)

1.  Hautatu **Berrikusi + esleitu**.

Baliteke aldaketak barreiatzeko 15 minutu behar izatea.

## <a name="enter-the-azure-resource-id-or-the-azure-subscription-details-in-the-storage-account-attachment-to-customer-insights"></a>Sartu Azure baliabideen IDa edo Azure harpidetzaren xehetasunak Customer Insights biltegiratze-kontuaren eranskinean

Customer Insights-en Data Lake Storage kontu bat erantsi diezaiokezu [irteerako datuak gordetzea](manage-environments.md) edo [erabili datu-iturburu gisa](connect-dataverse-managed-lake.md). Aukera honek baliabideetan oinarritutako edo harpidetzan oinarritutako ikuspegiaren artean aukeratzeko aukera ematen du. Aukeratzen duzun ikuspegiaren arabera, jarraitu prozedura hurrengo ataletako batean.

### <a name="resource-based-storage-account-connection"></a>Baliabideetan oinarritutako biltegiratze-kontuaren konexioa

1. Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.

1. Ezkerreko panelean, joan hona **Ezarpenak** > **Ezaugarriak**.

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