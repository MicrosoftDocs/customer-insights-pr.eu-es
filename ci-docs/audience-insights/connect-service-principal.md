---
title: Konektatu Azure Data Lake Storage Gen2 kontura zerbitzuaren entitatearekin
description: Erabili hartzaileen xehetasunen Azure zerbitzuaren entitatea zure datu-biltegira konektatzeko horiek hartzaileen xehetasunetan txertatzean.
ms.date: 02/10/2021
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: c670b0065a2833a6dc311d9e86d2b351140382ce
ms.sourcegitcommit: bae40184312ab27b95c140a044875c2daea37951
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "5596484"
---
# <a name="connect-to-an-azure-data-lake-storage-gen2-account-with-an-azure-service-principal-for-audience-insights"></a>Konektatu Azure Data Lake Storage Gen2 kontura hartzaileen xehetasunen Azure zerbitzuaren entitatearekin

Azure zerbitzuak erabiltzen dituzten tresna automatizatuek beti baimen mugatuak izan behar dituzte. Aplikazioek erabiltzaile pribilegiatu gisa saioa hasi beharrean, Azure-k zerbitzuaren entitateak eskaintzen ditu. Irakurri jarraian hartzaileen xehetasunak nola konektatu Azure Data Lake Storage Gen2 kontuarekin Azure zerbitzuaren entitatea erabiliz biltegiratze kontuko gakoen ordez. 

Zerbitzuaren entitatea erabil dezakezu segurtasunez [Common Data Model fitxategi bat gehitu edo editatzeko datu-iturburu gisa](connect-common-data-model.md) edo [ingurune bat sortzeko edo lehendik dagoen ingurune bat eguneratzeko](manage-environments.md#create-an-environment-in-an-existing-organization).

> [!IMPORTANT]
> - Zerbitzu nagusia erabiltzeko asmoa duen Azure Data Lake Gen2 biltegiratze kontuak izan behar du [Izen espazio hierarkikoa (HNS) gaituta dago](/azure/storage/blobs/data-lake-storage-namespace).
> - Administratzaile baimenak behar dituzu Azure harpidetzak zerbitzuaren entitatea sortzeko.

## <a name="create-azure-service-principal-for-audience-insights"></a>Sortu hartzaileen xehetasunen Azure zerbitzuaren entitatea

Hartzaileen xehetasunen zerbitzuaren entitate bat sortu aurretik, egiaztatu dagoeneko badagoen zure erakundean.

### <a name="look-for-an-existing-service-principal"></a>Bilatu lehendik dagoen zerbitzuaren entitatea

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

2. Aukeratu **Azure Active Directory** Azure zerbitzuetatik.

3. **Kudeatu** atalean, hautatu **Enpresaren aplikazioak**.

4. Bilatu hartzaileen xehetasunen lehen alderdiaren aplikazioaren IDa (`0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff`) edo izena (`Dynamics 365 AI for Customer Insights`).

5. Bat datozen erregistroak aurkitzen badituzu, esan nahi du hartzaileen xehetasunen zerbitzuaren entitatea badagoela. Ez duzu berriz sortu behar.
   
   :::image type="content" source="media/ADLS-SP-AlreadyProvisioned.png" alt-text="Lehendik dagoen zerbitzuaren entitatea erakusten duen pantaila-argazkia.":::
   
6. Emaitzarik ematen ez bada, sortu zerbitzuaren entitatea.

### <a name="create-a-new-service-principal"></a>Sortu zerbitzuaren entitatea

1. Instalatu **Graph-erako Azure Active Directory PowerShell** zerbitzuaren azken bertsioa. Informazio gehiagorako, ikus [Instalatu Graph-erako Azure Active Directory PowerShell](/powershell/azure/active-directory/install-adv2).
   - Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta **Exekutatu administratzaile gisa**.
   
   - Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.

2. Sortu hartzaileen xehetasunen zerbitzuaren entitatea Azure AD PowerShell moduluarekin.
   - PowerShell leihoan, sartu `Connect-AzureAD -TenantId "[your tenant ID]" -AzureEnvironmentName Azure`. Ordeztu "zure maizterraren IDa" zerbitzuaren entitatea sortu nahi duzun maizterraren IDarekin. `AzureEnvironmentName` ingurunearen izenaren parametroa aukerakoa da.
  
   - Idatzi `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`. Komando honek hautatutako maizterraren hartzaileei buruzko informazioaren zerbitzuaren entitatea sortzen du.  

## <a name="grant-permissions-to-the-service-principal-to-access-the-storage-account"></a>Eman baimenak zerbitzuaren entitateari biltegiratze kontura sartzeko

Joan Azure atarira hartzaileen xehetasunetan erabili nahi duzun biltegiratze kontuaren zerbitzuaren entitateari baimenak emateko.

1. Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.

1. Ireki hartzaileen xehetasunen zerbitzuaren entitateak sarbidea izan nahi duzun biltegiratze kontua.

1. Aukeratu **Sarbide kontrola (IAM)** nabigazio paneletik eta hautatu **Gehitu** > **Gehitu funtzio esleipena**.
   
   :::image type="content" source="media/ADLS-SP-AddRoleAssignment.png" alt-text="Azure ataria erakusten duen pantaila-argazkia, funtzioa esleitzen duzun bitartean.":::
   
1. **Gehitu funtzio esleipena** panelean, ezarri propietate hauek:
   - Funtzioa: *Biltegiratze blob-aren datuen kolaboratzailea*
   - Esleitu sarbidea hauei: *Erabiltzailea, taldea edo zerbitzuaren entitatea*
   - Aukeratu: *Customer Insights-erako Dynamics 365 AA* ([sortu duzun zerbitzuaren entitatea](#create-a-new-service-principal))

1.  Sakatu **Gorde**.

Baliteke aldaketak barreiatzeko 15 minutu behar izatea.

## <a name="enter-the-azure-resource-id-or-the-azure-subscription-details-in-the-storage-account-attachment-to-audience-insights"></a>Idatzi Azure baliabidearen IDa edo Azure harpidetzaren xehetasunak hartzaileen xehetasunen ataleko biltegirako kontuaren eranskinean.

Erantsi Azure Data Lake biltegiratze-kontua hartzaileei buruzko informazioan [irteerako datuak gordetzeko](manage-environments.md) edo [datu-iturburu gisa erabiltzeko](connect-common-data-service-lake.md). Azure Data Lake aukera aukeratuz gero, baliabideetan oinarritutako edo harpidetzan oinarritutako ikuspegiaren artean aukera dezakezu.

Jarraitu beheko urratsak hautatutako ikuspegiari buruzko beharrezko informazioa emateko.

### <a name="resource-based-storage-account-connection"></a>Baliabideetan oinarritutako biltegiratze-kontuaren konexioa

1. Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.

1. Joan **Ezarpenak** > **Ezaugarriak** atalera nabigazio panelean.

1. Kopiatu biltegiratze kontuaren baliabidearen ID balioa.

   :::image type="content" source="media/ADLS-SP-ResourceId.png" alt-text="Kopiatu biltegiratze kontuaren baliabidearen IDa.":::

1. Hartzaileei buruzko xehetasunetan, sartu baliabidearen IDa biltegiratze kontuko konexio pantailan agertzen den baliabidearen eremuan.

   :::image type="content" source="media/ADLS-SP-ResourceIdConnection.png" alt-text="Idatzi biltegiratze kontuaren baliabidearen IDaren informazioa.":::   
   
1. Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.

### <a name="subscription-based-storage-account-connection"></a>Harpidetzetan oinarritutako biltegiratze-kontuaren konexioa

1. Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.

1. Joan **Ezarpenak** > **Ezaugarriak** atalera nabigazio panelean.

1. Berrikusi biltegiratze-kontuaren **Harpidetza**, **Baliabide taldea**, eta **Izena** eremuak, hartzaileei buruzko xehetasunetan balio egokiak hautatzen dituzula ziurtatzeko.

1. Hartzaileei buruzko xehetasunetan, aukeratu balioak edo dagozkien eremuak biltegiratze kontua eransterakoan.
   
1. Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.


[!INCLUDE[footer-include](../includes/footer-banner.md)]