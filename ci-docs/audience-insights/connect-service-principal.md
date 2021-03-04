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
ms.openlocfilehash: eebbac1370a847869d98beaf70db49b809d762e7
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5267707"
---
# <a name="connect-to-an-azure-data-lake-storage-gen2-account-with-an-azure-service-principal-for-audience-insights"></a><span data-ttu-id="4085e-103">Konektatu Azure Data Lake Storage Gen2 kontura hartzaileen xehetasunen Azure zerbitzuaren entitatearekin</span><span class="sxs-lookup"><span data-stu-id="4085e-103">Connect to an Azure Data Lake Storage Gen2 account with an Azure service principal for audience insights</span></span>

<span data-ttu-id="4085e-104">Azure zerbitzuak erabiltzen dituzten tresna automatizatuek beti baimen mugatuak izan behar dituzte.</span><span class="sxs-lookup"><span data-stu-id="4085e-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="4085e-105">Aplikazioek erabiltzaile pribilegiatu gisa saioa hasi beharrean, Azure-k zerbitzuaren entitateak eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="4085e-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span> <span data-ttu-id="4085e-106">Irakurri jarraian hartzaileen xehetasunak nola konektatu Azure Data Lake Storage Gen2 kontuarekin Azure zerbitzuaren entitatea erabiliz biltegiratze kontuko gakoen ordez.</span><span class="sxs-lookup"><span data-stu-id="4085e-106">Read on to learn how to connect audience insights with an Azure Data Lake Storage Gen2 account using an Azure service principal instead of storage account keys.</span></span> 

<span data-ttu-id="4085e-107">Zerbitzuaren entitatea erabil dezakezu segurtasunez [Common Data Model fitxategi bat gehitu edo editatzeko datu-iturburu gisa](connect-common-data-model.md) edo [ingurune bat sortzeko edo lehendik dagoen ingurune bat eguneratzeko](manage-environments.md#create-an-environment-in-an-existing-organization).</span><span class="sxs-lookup"><span data-stu-id="4085e-107">You can use the service principal to securely [add or edit a Common Data Model folder as a data source](connect-common-data-model.md) or [create a new or update an existing environment](manage-environments.md#create-an-environment-in-an-existing-organization).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="4085e-108">Zerbitzu nagusia erabiltzeko asmoa duen Azure Data Lake Gen2 biltegiratze kontuak izan behar du [Izen espazio hierarkikoa (HNS) gaituta dago](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-namespace).</span><span class="sxs-lookup"><span data-stu-id="4085e-108">The Azure Data Lake Gen2 storage account that intends to use the service principal must have [Hierarchical Name Space (HNS) enabled](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-namespace).</span></span>
> - <span data-ttu-id="4085e-109">Administratzaile baimenak behar dituzu Azure harpidetzak zerbitzuaren entitatea sortzeko.</span><span class="sxs-lookup"><span data-stu-id="4085e-109">You need admin permissions for your Azure subscription to create the service principal.</span></span>

## <a name="create-azure-service-principal-for-audience-insights"></a><span data-ttu-id="4085e-110">Sortu hartzaileen xehetasunen Azure zerbitzuaren entitatea</span><span class="sxs-lookup"><span data-stu-id="4085e-110">Create Azure service principal for audience insights</span></span>

<span data-ttu-id="4085e-111">Hartzaileen xehetasunen zerbitzuaren entitate bat sortu aurretik, egiaztatu dagoeneko badagoen zure erakundean.</span><span class="sxs-lookup"><span data-stu-id="4085e-111">Before creating a new service principal for audience insights, check if it already exists in your organization.</span></span>

### <a name="look-for-an-existing-service-principal"></a><span data-ttu-id="4085e-112">Bilatu lehendik dagoen zerbitzuaren entitatea</span><span class="sxs-lookup"><span data-stu-id="4085e-112">Look for an existing service principal</span></span>

1. <span data-ttu-id="4085e-113">Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.</span><span class="sxs-lookup"><span data-stu-id="4085e-113">Go to the [Azure admin portal](https://portal.azure.com) and sign in to your organization.</span></span>

2. <span data-ttu-id="4085e-114">Aukeratu **Azure Active Directory** Azure zerbitzuetatik.</span><span class="sxs-lookup"><span data-stu-id="4085e-114">Select **Azure Active Directory** from the Azure services.</span></span>

3. <span data-ttu-id="4085e-115">**Kudeatu** atalean, hautatu **Enpresaren aplikazioak**.</span><span class="sxs-lookup"><span data-stu-id="4085e-115">Under **Manage**, select **Enterprise Applications**.</span></span>

4. <span data-ttu-id="4085e-116">Bilatu hartzaileen xehetasunen lehen alderdiaren aplikazioaren IDa (`0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff`) edo izena (`Dynamics 365 AI for Customer Insights`).</span><span class="sxs-lookup"><span data-stu-id="4085e-116">Search for the audience insights first party application ID `0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` or the name `Dynamics 365 AI for Customer Insights`.</span></span>

5. <span data-ttu-id="4085e-117">Bat datozen erregistroak aurkitzen badituzu, esan nahi du hartzaileen xehetasunen zerbitzuaren entitatea badagoela.</span><span class="sxs-lookup"><span data-stu-id="4085e-117">If you find a matching record, it means that the service principal for audience insights exists.</span></span> <span data-ttu-id="4085e-118">Ez duzu berriz sortu behar.</span><span class="sxs-lookup"><span data-stu-id="4085e-118">You don't need to create it again.</span></span>
   
   :::image type="content" source="media/ADLS-SP-AlreadyProvisioned.png" alt-text="Lehendik dagoen zerbitzuaren entitatea erakusten duen pantaila-argazkia.":::
   
6. <span data-ttu-id="4085e-120">Emaitzarik ematen ez bada, sortu zerbitzuaren entitatea.</span><span class="sxs-lookup"><span data-stu-id="4085e-120">If no results are returned, create a new service principal.</span></span>

### <a name="create-a-new-service-principal"></a><span data-ttu-id="4085e-121">Sortu zerbitzuaren entitatea</span><span class="sxs-lookup"><span data-stu-id="4085e-121">Create a new service principal</span></span>

1. <span data-ttu-id="4085e-122">Instalatu **Graph-erako Azure Active Directory PowerShell** zerbitzuaren azken bertsioa.</span><span class="sxs-lookup"><span data-stu-id="4085e-122">Install the latest version of the **Azure Active Directory PowerShell for Graph**.</span></span> <span data-ttu-id="4085e-123">Informazio gehiagorako, ikus [Instalatu Graph-erako Azure Active Directory PowerShell](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="4085e-123">For more information, see [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
   - <span data-ttu-id="4085e-124">Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta **Exekutatu administratzaile gisa**.</span><span class="sxs-lookup"><span data-stu-id="4085e-124">On your PC, select the Windows key on your keyboard and search for **Windows PowerShell** and **Run as Administrator**.</span></span>
   
   - <span data-ttu-id="4085e-125">Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.</span><span class="sxs-lookup"><span data-stu-id="4085e-125">In the PowerShell window that opens, enter `Install-Module AzureAD`.</span></span>

2. <span data-ttu-id="4085e-126">Sortu hartzaileen xehetasunen zerbitzuaren entitatea Azure AD PowerShell moduluarekin.</span><span class="sxs-lookup"><span data-stu-id="4085e-126">Create the  service principal for audience insights with the Azure AD PowerShell Module.</span></span>
   - <span data-ttu-id="4085e-127">PowerShell leihoan, sartu `Connect-AzureAD -TenantId "[your tenant ID]" -AzureEnvironmentName Azure`.</span><span class="sxs-lookup"><span data-stu-id="4085e-127">In the PowerShell window, enter `Connect-AzureAD -TenantId "[your tenant ID]" -AzureEnvironmentName Azure`.</span></span> <span data-ttu-id="4085e-128">Ordeztu "zure maizterraren IDa" zerbitzuaren entitatea sortu nahi duzun maizterraren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="4085e-128">Replace “your tenant ID” with the actual ID of your tenant where you want to create the service principal.</span></span> <span data-ttu-id="4085e-129">`AzureEnvironmentName` ingurunearen izenaren parametroa aukerakoa da.</span><span class="sxs-lookup"><span data-stu-id="4085e-129">The environment name parameter `AzureEnvironmentName` is optional.</span></span>
  
   - <span data-ttu-id="4085e-130">Idatzi `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`.</span><span class="sxs-lookup"><span data-stu-id="4085e-130">Enter `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`.</span></span> <span data-ttu-id="4085e-131">Komando honek hautatutako maizterraren hartzaileei buruzko informazioaren zerbitzuaren entitatea sortzen du.</span><span class="sxs-lookup"><span data-stu-id="4085e-131">This command creates the service principal for audience insights on the selected tenant.</span></span>  

## <a name="grant-permissions-to-the-service-principal-to-access-the-storage-account"></a><span data-ttu-id="4085e-132">Eman baimenak zerbitzuaren entitateari biltegiratze kontura sartzeko</span><span class="sxs-lookup"><span data-stu-id="4085e-132">Grant permissions to the service principal to access the storage account</span></span>

<span data-ttu-id="4085e-133">Joan Azure atarira hartzaileen xehetasunetan erabili nahi duzun biltegiratze kontuaren zerbitzuaren entitateari baimenak emateko.</span><span class="sxs-lookup"><span data-stu-id="4085e-133">Go to the Azure portal to grant permissions to the service principal for the storage account you want to use in audience insights.</span></span>

1. <span data-ttu-id="4085e-134">Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.</span><span class="sxs-lookup"><span data-stu-id="4085e-134">Go to the [Azure admin portal](https://portal.azure.com) and sign in to your organization.</span></span>

1. <span data-ttu-id="4085e-135">Ireki hartzaileen xehetasunen zerbitzuaren entitateak sarbidea izan nahi duzun biltegiratze kontua.</span><span class="sxs-lookup"><span data-stu-id="4085e-135">Open the storage account you want the service principal for audience insights to have access to.</span></span>

1. <span data-ttu-id="4085e-136">Aukeratu **Sarbide kontrola (IAM)** nabigazio paneletik eta hautatu **Gehitu** > **Gehitu funtzio esleipena**.</span><span class="sxs-lookup"><span data-stu-id="4085e-136">Select **Access control (IAM)** from the navigation pane and select **Add** > **Add role assignment**.</span></span>
   
   :::image type="content" source="media/ADLS-SP-AddRoleAssignment.png" alt-text="Azure ataria erakusten duen pantaila-argazkia, funtzioa esleitzen duzun bitartean.":::
   
1. <span data-ttu-id="4085e-138">**Gehitu funtzio esleipena** panelean, ezarri propietate hauek:</span><span class="sxs-lookup"><span data-stu-id="4085e-138">In the **Add role assignment** pane, set the following properties:</span></span>
   - <span data-ttu-id="4085e-139">Funtzioa: *Biltegiratze blob-aren datuen kolaboratzailea*</span><span class="sxs-lookup"><span data-stu-id="4085e-139">Role: *Storage Blob Data Contributor*</span></span>
   - <span data-ttu-id="4085e-140">Esleitu sarbidea hauei: *Erabiltzailea, taldea edo zerbitzuaren entitatea*</span><span class="sxs-lookup"><span data-stu-id="4085e-140">Assign access to: *User, group, or service principal*</span></span>
   - <span data-ttu-id="4085e-141">Aukeratu: *Customer Insights-erako Dynamics 365 AA* ([sortu duzun zerbitzuaren entitatea](#create-a-new-service-principal))</span><span class="sxs-lookup"><span data-stu-id="4085e-141">Select: *Dynamics 365 AI for Customer Insights* (the [service principal you created](#create-a-new-service-principal))</span></span>

1.  <span data-ttu-id="4085e-142">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="4085e-142">Select **Save**.</span></span>

<span data-ttu-id="4085e-143">Baliteke aldaketak barreiatzeko 15 minutu behar izatea.</span><span class="sxs-lookup"><span data-stu-id="4085e-143">It can take up to 15 minutes to propagate the changes.</span></span>

## <a name="enter-the-azure-resource-id-or-the-azure-subscription-details-in-the-storage-account-attachment-to-audience-insights"></a><span data-ttu-id="4085e-144">Idatzi Azure baliabidearen IDa edo Azure harpidetzaren xehetasunak hartzaileen xehetasunen ataleko biltegirako kontuaren eranskinean.</span><span class="sxs-lookup"><span data-stu-id="4085e-144">Enter the Azure Resource ID or the Azure Subscription details in the storage account attachment to Audience Insights.</span></span>

<span data-ttu-id="4085e-145">Erantsi Azure Data Lake biltegiratze-kontua hartzaileei buruzko informazioan [irteerako datuak gordetzeko](manage-environments.md) edo [datu-iturburu gisa erabiltzeko](connect-common-data-service-lake.md).</span><span class="sxs-lookup"><span data-stu-id="4085e-145">Attach an Azure Data Lake storage account in audience insights to [store output data](manage-environments.md) or [use it as a data source](connect-common-data-service-lake.md).</span></span> <span data-ttu-id="4085e-146">Azure Data Lake aukera aukeratuz gero, baliabideetan oinarritutako edo harpidetzan oinarritutako ikuspegiaren artean aukera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="4085e-146">Choosing the Azure Data Lake option lets you choose between a resource-based or a subscription-based based approach.</span></span>

<span data-ttu-id="4085e-147">Jarraitu beheko urratsak hautatutako ikuspegiari buruzko beharrezko informazioa emateko.</span><span class="sxs-lookup"><span data-stu-id="4085e-147">Follow the below steps to provide the required information on the selected approach.</span></span>

### <a name="resource-based-storage-account-connection"></a><span data-ttu-id="4085e-148">Baliabideetan oinarritutako biltegiratze-kontuaren konexioa</span><span class="sxs-lookup"><span data-stu-id="4085e-148">Resource-based storage account connection</span></span>

1. <span data-ttu-id="4085e-149">Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.</span><span class="sxs-lookup"><span data-stu-id="4085e-149">Go to the [Azure admin portal](https://portal.azure.com), sign in to your subscription and open the storage account.</span></span>

1. <span data-ttu-id="4085e-150">Joan **Ezarpenak** > **Ezaugarriak** atalera nabigazio panelean.</span><span class="sxs-lookup"><span data-stu-id="4085e-150">Go to **Settings** > **Properties** on navigation pane.</span></span>

1. <span data-ttu-id="4085e-151">Kopiatu biltegiratze kontuaren baliabidearen ID balioa.</span><span class="sxs-lookup"><span data-stu-id="4085e-151">Copy the storage account resource ID value.</span></span>

   :::image type="content" source="media/ADLS-SP-ResourceId.png" alt-text="Kopiatu biltegiratze kontuaren baliabidearen IDa.":::

1. <span data-ttu-id="4085e-153">Hartzaileei buruzko xehetasunetan, sartu baliabidearen IDa biltegiratze kontuko konexio pantailan agertzen den baliabidearen eremuan.</span><span class="sxs-lookup"><span data-stu-id="4085e-153">In audience insights, insert the resource ID in the resource field displayed in the storage account connection screen.</span></span>

   :::image type="content" source="media/ADLS-SP-ResourceIdConnection.png" alt-text="Idatzi biltegiratze kontuaren baliabidearen IDaren informazioa.":::   
   
1. <span data-ttu-id="4085e-155">Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="4085e-155">Continue with the remaining steps in audience insights to attach the storage account.</span></span>

### <a name="subscription-based-storage-account-connection"></a><span data-ttu-id="4085e-156">Harpidetzetan oinarritutako biltegiratze-kontuaren konexioa</span><span class="sxs-lookup"><span data-stu-id="4085e-156">Subscription-based storage account connection</span></span>

1. <span data-ttu-id="4085e-157">Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.</span><span class="sxs-lookup"><span data-stu-id="4085e-157">Go to the [Azure admin portal](https://portal.azure.com), sign in to your subscription and open the storage account.</span></span>

1. <span data-ttu-id="4085e-158">Joan **Ezarpenak** > **Ezaugarriak** atalera nabigazio panelean.</span><span class="sxs-lookup"><span data-stu-id="4085e-158">Go to **Settings** > **Properties** on navigation pane.</span></span>

1. <span data-ttu-id="4085e-159">Berrikusi biltegiratze-kontuaren **Harpidetza**, **Baliabide taldea**, eta **Izena** eremuak, hartzaileei buruzko xehetasunetan balio egokiak hautatzen dituzula ziurtatzeko.</span><span class="sxs-lookup"><span data-stu-id="4085e-159">Review the **Subscription**, **Resource group**, and the **Name** of the storage account to make sure you select the right values in audience insights.</span></span>

1. <span data-ttu-id="4085e-160">Hartzaileei buruzko xehetasunetan, aukeratu balioak edo dagozkien eremuak biltegiratze kontua eransterakoan.</span><span class="sxs-lookup"><span data-stu-id="4085e-160">In audience insights, choose the values or for the corresponding fields when attaching the storage account.</span></span>
   
1. <span data-ttu-id="4085e-161">Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="4085e-161">Continue with the remaining steps in audience insights to attach the storage account.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]