---
title: Konektatu Azure Data Lake Storage kontu nagusia zerbitzuaren nagusia erabiliz
description: Erabili Azure zerbitzu nagusia zure data lake konektatzeko.
ms.date: 09/08/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: b901d799dbd73841a6ddbae754c4e4275f61146a
ms.sourcegitcommit: 53b133a716c73cb71e8bcbedc6273cec70ceba6c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/15/2021
ms.locfileid: "7645157"
---
# <a name="connect-to-an-azure-data-lake-storage-account-by-using-an-azure-service-principal"></a>Konektatu Azure Data Lake Storage kontu nagusia Azure zerbitzuaren nagusia erabiliz

Azure zerbitzuak erabiltzen dituzten tresna automatizatuek beti baimen mugatuak izan behar dituzte. Aplikazioek erabiltzaile pribilegiatu gisa saioa hasi beharrean, Azure-k zerbitzuaren entitateak eskaintzen ditu. Irakurri irakurtzen nola konektatzen den jakiteko Dynamics 365 Customer Insights batekin Azure Data Lake Storage kontua biltegiratze kontuko gakoen ordez Azure zerbitzu nagusia erabilita. 

Zerbitzu nagusia segurtasunez erabil dezakezu [gehitu edo editatu Common Data Model karpeta datu-iturburu gisa](connect-common-data-model.md), edo [ingurune bat sortu edo eguneratu](create-environment.md).

> [!IMPORTANT]
> - Zerbitzuaren entitatea erabiliko duen Data Lake Storage kontuak [gaituta eduki behar du izen-leku hierarkikoa](/azure/storage/blobs/data-lake-storage-namespace).
> - Administratzaile baimenak behar dituzu Azure harpidetzak zerbitzuaren entitatea sortzeko.

## <a name="create-an-azure-service-principal-for-customer-insights"></a>Sortu Azure zerbitzu nagusia Customer Insights-entzat

Ikusleen edo konpromisoen inguruko zerbitzu nagusia sortu aurretik, egiaztatu zure erakundean dagoen ala ez.

### <a name="look-for-an-existing-service-principal"></a>Bilatu lehendik dagoen zerbitzuaren entitatea

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

2. Hurrengoan **Azure zerbitzuak**, hautatu **Azure Active Directory**.

3. **Kudeatu** atalean, hautatu **Enpresaren aplikazioak**.

4. Bilatu Microsoft aplikazioaren bezeroaren IDa:
   - Hartzailearen xehetasunak: `0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` hurrengo izenarekin `Dynamics 365 AI for Customer Insights`
   - Elkarreragin xehetasunak: `ffa7d2fe-fc04-4599-9f6d-7ca06dd0c4fd` hurrengo izenarekin `Dynamics 365 AI for Customer Insights engagement insights`

5. Bat datorren erregistroa aurkitzen baduzu, esan nahi du zerbitzuaren nagusia dagoeneko badagoela. 
   
   :::image type="content" source="media/ADLS-SP-AlreadyProvisioned.png" alt-text="Lehendik dagoen zerbitzu nagusia erakusten duen pantaila-argazkia.":::
   
6. Emaitzarik ematen ez bada, sortu zerbitzuaren entitatea.

>[!NOTE]
>Ahalmen osoa baliatzeko Dynamics 365 Customer Insights, bi aplikazioak zerbitzu nagusira gehitzea gomendatzen dizugu.

### <a name="create-a-new-service-principal"></a>Sortu zerbitzuaren entitatea

1. Instalatu azken bertsioa Azure Active Directory PowerShell for Graph. Informazio gehiagorako, joan hona [Instalatu Azure Active Directory PowerShell grafikorako](/powershell/azure/active-directory/install-adv2).

   1. Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta hautatu **Exekutatu administratzaile gisa**.
   
   1. Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.

2. Sortu Customer Insights zerbitzuaren nagusia Azure AD PowerShell modulua.

   1. PowerShell leihoan, sartu `Connect-AzureAD -TenantId "[your tenant ID]" -AzureEnvironmentName Azure`. Ordeztu *[maizterraren IDa]* zerbitzuaren entitatea sortu nahi duzun maizterraren IDarekin. `AzureEnvironmentName` ingurunearen izenaren parametroa aukerakoa da.
  
   1. Idatzi `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`. Komando honek hautatutako maizterraren hartzaileei buruzko informazioaren zerbitzuaren entitatea sortzen du. 

   1. Idatzi `New-AzureADServicePrincipal -AppId "ffa7d2fe-fc04-4599-9f6d-7ca06dd0c4fd" -DisplayName "Dynamics 365 AI for Customer Insights engagement insights"`. Komando honek parte-hartzailearen xehetasunen zerbitzuaren entitatea sortzen du hautatutako maizterrean.

## <a name="grant-permissions-to-the-service-principal-to-access-the-storage-account"></a>Eman baimenak zerbitzuaren entitateari biltegiratze kontura sartzeko

Joan Azure atarira hartzaileen xehetasunetan erabili nahi duzun biltegiratze kontuaren zerbitzuaren entitateari baimenak emateko.

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

1. Ireki hartzaileen xehetasunen zerbitzuaren entitateak sarbidea izan nahi duzun biltegiratze kontua.

1. Ezkerreko panelean, hautatu **Sarbide kontrola (IAM)** eta, ondoren, hautatu **Gehitu** > **Gehitu rol esleipena**.

   :::image type="content" source="media/ADLS-SP-AddRoleAssignment.png" alt-text="Azure ataria erakusten duen pantaila-argazkia eginkizuna esleitzen duzun bitartean.":::

1. Gainean **Gehitu rol esleipena** panelean, ezarri propietate hauek:
   - Funtzioa: **Biltegiratze blob-aren datuen kolaboratzailea**
   - Esleitu sarbidea hauei: **Erabiltzailea, taldea edo zerbitzuaren entitatea**
   - Aukeratu: **Dynamics 365 AI for Customer Insights** eta **Dynamics 365 AI for Customer Insights-en konpromisoak** (biak [zerbitzu nagusiak](#create-a-new-service-principal) prozedura honetan lehenago sortu zenuen)

1.  Sakatu **Gorde**.

Baliteke aldaketak barreiatzeko 15 minutu behar izatea.

## <a name="enter-the-azure-resource-id-or-the-azure-subscription-details-in-the-storage-account-attachment-to-audience-insights"></a>Idatzi Azure baliabidearen IDa edo Azure harpidetzaren xehetasunak hartzaileen xehetasunen ataleko biltegirako kontuaren eranskinean

Data Lake Storage kontua erantsi dezakezu hartzaileen xehetasunetan [irteerako datuak gordetzeko](manage-environments.md) edo [datu-iturburu gisa erabiltzeko](connect-common-data-service-lake.md). Aukera honek baliabideetan oinarritutako edo harpidetzan oinarritutako ikuspegiaren artean aukeratzeko aukera ematen du. Aukeratzen duzun ikuspegiaren arabera, jarraitu prozedura hurrengo ataletako batean.

### <a name="resource-based-storage-account-connection"></a>Baliabideetan oinarritutako biltegiratze-kontuaren konexioa

1. Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.

1. Ezkerreko panelean, joan hona **Ezarpenak** > **Ezaugarriak**.

1. Kopiatu biltegiratze kontuaren baliabidearen ID balioa.

   :::image type="content" source="media/ADLS-SP-ResourceId.png" alt-text="Kopiatu biltegiratze kontuaren baliabidearen IDa.":::

1. Ikusleen estatistiketan, sartu baliabidearen IDa biltegiratze kontuko konexio pantailan agertzen den baliabide eremuan.

   :::image type="content" source="media/ADLS-SP-ResourceIdConnection.png" alt-text="Idatzi biltegiratze kontuaren baliabidearen IDaren informazioa.":::   

1. Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.

### <a name="subscription-based-storage-account-connection"></a>Harpidetzetan oinarritutako biltegiratze-kontuaren konexioa

1. Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.

1. Ezkerreko panelean, joan hona **Ezarpenak** > **Ezaugarriak**.

1. Berrikusi biltegiratze-kontuaren **Harpidetza**, **Baliabide taldea**, eta **Izena** eremuak, hartzaileei buruzko xehetasunetan balio egokiak hautatzen dituzula ziurtatzeko.

1. Audientzia estatistiketan, aukeratu dagokion eremuen balioak biltegiratze kontua erantsitakoan.

1. Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
