---
title: Konektatu Azure Data Lake Storage Gen2 kontura zerbitzuaren entitatearekin
description: Erabili hartzaileen xehetasunen Azure zerbitzuaren entitatea zure datu-biltegira konektatzeko horiek hartzaileen xehetasunetan txertatzerakoan.
ms.date: 11/24/2020
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: adkuppa
ms.author: adkuppa
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: c2fae278d34fa02b9168ac70dfa8dd351653245e
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644073"
---
# <a name="connect-to-an-azure-data-lake-storage-gen2-account-with-an-azure-service-principal-for-audience-insights"></a><span data-ttu-id="0fee2-103">Konektatu Azure Data Lake Storage Gen2 kontura hartzaileen xehetasunen Azure zerbitzuaren entitatearekin</span><span class="sxs-lookup"><span data-stu-id="0fee2-103">Connect to an Azure Data Lake Storage Gen2 account with an Azure service principal for audience insights</span></span>

<span data-ttu-id="0fee2-104">Azure zerbitzuak erabiltzen dituzten tresna automatizatuek beti baimen mugatuak izan behar dituzte.</span><span class="sxs-lookup"><span data-stu-id="0fee2-104">Automated tools that use Azure services should always have restricted permissions.</span></span> <span data-ttu-id="0fee2-105">Aplikazioek erabiltzaile pribilegiatu gisa saioa hasi beharrean, Azure-k zerbitzuaren entitateak eskaintzen ditu.</span><span class="sxs-lookup"><span data-stu-id="0fee2-105">Instead of having applications sign in as a fully privileged user, Azure offers service principals.</span></span> <span data-ttu-id="0fee2-106">Irakurri jarraian hartzaileen xehetasunak nola konektatu Azure Data Lake Storage Gen2 kontuarekin Azure zerbitzuaren entitatea erabiliz biltegiratze kontuko gakoen ordez.</span><span class="sxs-lookup"><span data-stu-id="0fee2-106">Read on to learn how to connect audience insights with an Azure Data Lake Storage Gen2 account using an Azure service principal instead of storage account keys.</span></span> 

<span data-ttu-id="0fee2-107">Zerbitzuaren entitatea erabil dezakezu segurtasunez [Common Data Model fitxategi bat gehitu edo editatzeko datu-iturburu gisa](connect-common-data-model.md) edo [ingurune bat sortzeko edo lehendik dagoen ingurune bat eguneratzeko](manage-environments.md#create-an-environment-in-an-existing-organization).</span><span class="sxs-lookup"><span data-stu-id="0fee2-107">You can use the service principal to securely [add or edit a Common Data Model folder as a data source](connect-common-data-model.md) or [create a new or update an existing environment](manage-environments.md#create-an-environment-in-an-existing-organization).</span></span>

<span data-ttu-id="0fee2-108">Administratzaile baimenak behar dituzu Azure harpidetzak zerbitzuaren entitatea sortzeko.</span><span class="sxs-lookup"><span data-stu-id="0fee2-108">You need admin permissions for your Azure subscription to create the service principal.</span></span>

## <a name="create-azure-service-principal-for-audience-insights"></a><span data-ttu-id="0fee2-109">Sortu hartzaileen xehetasunen Azure zerbitzuaren entitatea</span><span class="sxs-lookup"><span data-stu-id="0fee2-109">Create Azure service principal for audience insights</span></span>

<span data-ttu-id="0fee2-110">Hartzaileen xehetasunen zerbitzuaren entitate bat sortu aurretik, egiaztatu dagoeneko badagoen zure erakundean.</span><span class="sxs-lookup"><span data-stu-id="0fee2-110">Before creating a new service principal for audience insights, check if it already exists in your organization.</span></span>

### <a name="look-for-an-existing-service-principal"></a><span data-ttu-id="0fee2-111">Bilatu lehendik dagoen zerbitzuaren entitatea</span><span class="sxs-lookup"><span data-stu-id="0fee2-111">Look for an existing service principal</span></span>

1. <span data-ttu-id="0fee2-112">Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.</span><span class="sxs-lookup"><span data-stu-id="0fee2-112">Go to the [Azure admin portal](https://portal.azure.com) and sign in to your organization.</span></span>

2. <span data-ttu-id="0fee2-113">Aukeratu **Azure Active Directory** Azure zerbitzuetatik.</span><span class="sxs-lookup"><span data-stu-id="0fee2-113">Select **Azure Active Directory** from the Azure services.</span></span>

3. <span data-ttu-id="0fee2-114">**Kudeatu** atalean, hautatu **Enpresaren aplikazioak**.</span><span class="sxs-lookup"><span data-stu-id="0fee2-114">Under **Manage**, select **Enterprise Applications**.</span></span>

4. <span data-ttu-id="0fee2-115">Bilatu hartzaileen xehetasunen lehen alderdiaren aplikazioaren IDa (`0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff`) edo izena (`Dynamics 365 AI for Customer Insights`).</span><span class="sxs-lookup"><span data-stu-id="0fee2-115">Search for the audience insights first party application ID `0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` or the name `Dynamics 365 AI for Customer Insights`.</span></span>

5. <span data-ttu-id="0fee2-116">Bat datozen erregistroak aurkitzen badituzu, esan nahi du hartzaileen xehetasunen zerbitzuaren entitatea badagoela.</span><span class="sxs-lookup"><span data-stu-id="0fee2-116">If you find a matching record, it means that the service principal for audience insights exists.</span></span> <span data-ttu-id="0fee2-117">Ez duzu berriz sortu behar.</span><span class="sxs-lookup"><span data-stu-id="0fee2-117">You don't need to create it again.</span></span>
   
   :::image type="content" source="media/ADLS-SP-AlreadyProvisioned.png" alt-text="Lehendik dagoen zerbitzuaren entitatea erakusten duen pantaila-argazkia.":::
   
6. <span data-ttu-id="0fee2-119">Emaitzarik ematen ez bada, sortu zerbitzuaren entitatea.</span><span class="sxs-lookup"><span data-stu-id="0fee2-119">If no results are returned, create a new service principal.</span></span>

### <a name="create-a-new-service-principal"></a><span data-ttu-id="0fee2-120">Sortu zerbitzuaren entitatea</span><span class="sxs-lookup"><span data-stu-id="0fee2-120">Create a new service principal</span></span>

1. <span data-ttu-id="0fee2-121">Instalatu **Graph-erako Azure Active Directory PowerShell** zerbitzuaren azken bertsioa.</span><span class="sxs-lookup"><span data-stu-id="0fee2-121">Install the latest version of the **Azure Active Directory PowerShell for Graph**.</span></span> <span data-ttu-id="0fee2-122">Informazio gehiagorako, ikus [Instalatu Graph-erako Azure Active Directory PowerShell](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="0fee2-122">For more information, see [Install Azure Active Directory PowerShell for Graph](https://docs.microsoft.com/powershell/azure/active-directory/install-adv2).</span></span>
   - <span data-ttu-id="0fee2-123">Zure ordenagailuan, hautatu Windows tekla teklatuan eta bilatu **Windows PowerShell** eta **Exekutatu administratzaile gisa**.</span><span class="sxs-lookup"><span data-stu-id="0fee2-123">On your PC, select the Windows key on your keyboard and search for **Windows PowerShell** and **Run as Administrator**.</span></span>
   
   - <span data-ttu-id="0fee2-124">Ireki den PowerShell leihoan, sartu `Install-Module AzureAD`.</span><span class="sxs-lookup"><span data-stu-id="0fee2-124">In the PowerShell window that opens, enter `Install-Module AzureAD`.</span></span>

2. <span data-ttu-id="0fee2-125">Sortu hartzaileen xehetasunen zerbitzuaren entitatea Azure AD PowerShell moduluarekin.</span><span class="sxs-lookup"><span data-stu-id="0fee2-125">Create the  service principal for audience insights with the Azure AD PowerShell Module.</span></span>
   - <span data-ttu-id="0fee2-126">PowerShell leihoan, sartu `Connect-AzureAD -TenantId "[your tenant ID]" -AzureEnvironmentName Azure`.</span><span class="sxs-lookup"><span data-stu-id="0fee2-126">In the PowerShell window, enter `Connect-AzureAD -TenantId "[your tenant ID]" -AzureEnvironmentName Azure`.</span></span> <span data-ttu-id="0fee2-127">Ordeztu "zure maizterraren IDa" zerbitzuaren entitatea sortu nahi duzun maizterraren IDarekin.</span><span class="sxs-lookup"><span data-stu-id="0fee2-127">Replace “your tenant ID” with the actual ID of your tenant where you want to create the service principal.</span></span> <span data-ttu-id="0fee2-128">`AzureEnvironmentName` ingurunearen izenaren parametroa aukerakoa da.</span><span class="sxs-lookup"><span data-stu-id="0fee2-128">The environment name parameter `AzureEnvironmentName` is optional.</span></span>
  
   - <span data-ttu-id="0fee2-129">Idatzi `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`.</span><span class="sxs-lookup"><span data-stu-id="0fee2-129">Enter `New-AzureADServicePrincipal -AppId "0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff" -DisplayName "Dynamics 365 AI for Customer Insights"`.</span></span> <span data-ttu-id="0fee2-130">Komando honek hautatutako maizterraren hartzaileei buruzko informazioaren zerbitzuaren entitatea sortzen du.</span><span class="sxs-lookup"><span data-stu-id="0fee2-130">This command creates the service principal for audience insights on the selected tenant.</span></span>  

## <a name="grant-permissions-to-the-service-principal-to-access-the-storage-account"></a><span data-ttu-id="0fee2-131">Eman baimenak zerbitzuaren entitateari biltegiratze kontura sartzeko</span><span class="sxs-lookup"><span data-stu-id="0fee2-131">Grant permissions to the service principal to access the storage account</span></span>

<span data-ttu-id="0fee2-132">Joan Azure atarira hartzaileen xehetasunetan erabili nahi duzun biltegiratze kontuaren zerbitzuaren entitateari baimenak emateko.</span><span class="sxs-lookup"><span data-stu-id="0fee2-132">Go to the Azure portal to grant permissions to the service principal for the storage account you want to use in audience insights.</span></span>

1. <span data-ttu-id="0fee2-133">Joan [Azure administratzaile-atarira](https://portal.azure.com) eta hasi saioa zure erakundean.</span><span class="sxs-lookup"><span data-stu-id="0fee2-133">Go to the [Azure admin portal](https://portal.azure.com) and sign in to your organization.</span></span>

1. <span data-ttu-id="0fee2-134">Ireki hartzaileen xehetasunen zerbitzuaren entitateak sarbidea izan nahi duzun biltegiratze kontua.</span><span class="sxs-lookup"><span data-stu-id="0fee2-134">Open the storage account you want the service principal for audience insights to have access to.</span></span>

1. <span data-ttu-id="0fee2-135">Aukeratu **Sarbide kontrola (IAM)** nabigazio paneletik eta hautatu **Gehitu** > **Gehitu funtzio esleipena**.</span><span class="sxs-lookup"><span data-stu-id="0fee2-135">Select **Access control (IAM)** from the navigation pane and select **Add** > **Add role assignment**.</span></span>
   
   :::image type="content" source="media/ADLS-SP-AddRoleAssignment.png" alt-text="Azure ataria erakusten duen pantaila-argazkia, funtzioa esleitzen duzun bitartean.":::
   
1. <span data-ttu-id="0fee2-137">**Gehitu funtzio esleipena** panelean, ezarri propietate hauek:</span><span class="sxs-lookup"><span data-stu-id="0fee2-137">In the **Add role assignment** pane, set the following properties:</span></span>
   - <span data-ttu-id="0fee2-138">Funtzioa: *Biltegiratze blob-aren datuen kolaboratzailea*</span><span class="sxs-lookup"><span data-stu-id="0fee2-138">Role: *Storage Blob Data Contributor*</span></span>
   - <span data-ttu-id="0fee2-139">Esleitu sarbidea hauei: *Erabiltzailea, taldea edo zerbitzuaren entitatea*</span><span class="sxs-lookup"><span data-stu-id="0fee2-139">Assign access to: *User, group, or service principal*</span></span>
   - <span data-ttu-id="0fee2-140">Aukeratu: *Customer Insights-erako Dynamics 365 AA* ([sortu duzun zerbitzuaren entitatea](#create-a-new-service-principal))</span><span class="sxs-lookup"><span data-stu-id="0fee2-140">Select: *Dynamics 365 AI for Customer Insights* (the [service principal you created](#create-a-new-service-principal))</span></span>

1.  <span data-ttu-id="0fee2-141">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="0fee2-141">Select **Save**.</span></span>

<span data-ttu-id="0fee2-142">Baliteke aldaketak barreiatzeko 15 minutu behar izatea.</span><span class="sxs-lookup"><span data-stu-id="0fee2-142">It can take up to 15 minutes to propagate the changes.</span></span>

## <a name="enter-the-azure-resource-id-or-the-azure-subscription-details-in-the-storage-account-attachment-to-audience-insights"></a><span data-ttu-id="0fee2-143">Idatzi Azure baliabidearen IDa edo Azure harpidetzaren xehetasunak hartzaileen xehetasunen ataleko biltegirako kontuaren eranskinean.</span><span class="sxs-lookup"><span data-stu-id="0fee2-143">Enter the Azure Resource ID or the Azure Subscription details in the storage account attachment to Audience Insights.</span></span>

<span data-ttu-id="0fee2-144">Erantsi Azure Data Lake biltegiratze-kontua hartzaileei buruzko informazioan [irteerako datuak gordetzeko](manage-environments.md) edo [datu-iturburu gisa erabiltzeko](connect-common-data-service-lake.md).</span><span class="sxs-lookup"><span data-stu-id="0fee2-144">Attach an Azure Data Lake storage account in audience insights to [store output data](manage-environments.md) or [use it as a data source](connect-common-data-service-lake.md).</span></span> <span data-ttu-id="0fee2-145">Azure Data Lake aukera aukeratuz gero, baliabideetan oinarritutako edo harpidetzan oinarritutako ikuspegiaren artean aukera dezakezu.</span><span class="sxs-lookup"><span data-stu-id="0fee2-145">Choosing the Azure Data Lake option lets you choose between a resource-based or a subscription-based based approach.</span></span>

<span data-ttu-id="0fee2-146">Jarraitu beheko urratsak hautatutako ikuspegiari buruzko beharrezko informazioa emateko.</span><span class="sxs-lookup"><span data-stu-id="0fee2-146">Follow the below steps to provide the required information on the selected approach.</span></span>

### <a name="resounce-based-storage-account-connection"></a><span data-ttu-id="0fee2-147">Baliabidetan oinarritutako biltegiratze-kontuaren konexioa</span><span class="sxs-lookup"><span data-stu-id="0fee2-147">Resounce-based storage account connection</span></span>

1. <span data-ttu-id="0fee2-148">Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.</span><span class="sxs-lookup"><span data-stu-id="0fee2-148">Go to the [Azure admin portal](https://portal.azure.com), sign in to your subscription and open the storage account.</span></span>

1. <span data-ttu-id="0fee2-149">Joan **Ezarpenak** > **Ezaugarriak** atalera nabigazio panelean.</span><span class="sxs-lookup"><span data-stu-id="0fee2-149">Go to **Settings** > **Properties** on navigation pane.</span></span>

1. <span data-ttu-id="0fee2-150">Kopiatu biltegiratze kontuaren baliabidearen ID balioa.</span><span class="sxs-lookup"><span data-stu-id="0fee2-150">Copy the storage account resource ID value.</span></span>

   :::image type="content" source="media/ADLS-SP-ResourceId.png" alt-text="Kopiatu biltegiratze kontuaren baliabidearen IDa.":::

1. <span data-ttu-id="0fee2-152">Hartzaileei buruzko xehetasunetan, sartu baliabidearen IDa biltegiratze kontuko konexio pantailan agertzen den baliabidearen eremuan.</span><span class="sxs-lookup"><span data-stu-id="0fee2-152">In audience insights, insert the resource ID in the resource field displayed in the storage account connection screen.</span></span>

   :::image type="content" source="media/ADLS-SP-ResourceIdConnection.png" alt-text="Idatzi biltegiratze kontuaren baliabidearen IDaren informazioa.":::   
   
1. <span data-ttu-id="0fee2-154">Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="0fee2-154">Continue with the remaining steps in audience insights to attach the storage account.</span></span>

### <a name="subscription-based-storage-account-connection"></a><span data-ttu-id="0fee2-155">Harpidetzetan oinarritutako biltegiratze-kontuaren konexioa</span><span class="sxs-lookup"><span data-stu-id="0fee2-155">Subscription-based storage account connection</span></span>

1. <span data-ttu-id="0fee2-156">Joan [Azure administratzaile atarira](https://portal.azure.com), hasi saioa zure harpidetzan eta ireki biltegiratze kontua.</span><span class="sxs-lookup"><span data-stu-id="0fee2-156">Go to the [Azure admin portal](https://portal.azure.com), sign in to your subscription and open the storage account.</span></span>

1. <span data-ttu-id="0fee2-157">Joan **Ezarpenak** > **Ezaugarriak** atalera nabigazio panelean.</span><span class="sxs-lookup"><span data-stu-id="0fee2-157">Go to **Settings** > **Properties** on navigation pane.</span></span>

1. <span data-ttu-id="0fee2-158">Berrikusi biltegiratze-kontuaren **Harpidetza**, **Baliabide taldea**, eta **Izena** eremuak, hartzaileei buruzko xehetasunetan balio egokiak hautatzen dituzula ziurtatzeko.</span><span class="sxs-lookup"><span data-stu-id="0fee2-158">Review the **Subscription**, **Resource group**, and the **Name** of the storage account to make sure you select the right values in audience insights.</span></span>

1. <span data-ttu-id="0fee2-159">Hartzaileei buruzko xehetasunetan, aukeratu balioak edo dagozkien eremuak biltegiratze kontua eransterakoan.</span><span class="sxs-lookup"><span data-stu-id="0fee2-159">In audience insights, choose the values or for the corresponding fields when attaching the storage account.</span></span>

   :::image type="content" source="media/ADLS-SP-SubscriptionConnection.png" alt-text="Idatzi biltegiratze kontuaren baliabidearen IDaren informazioa.":::
   
1. <span data-ttu-id="0fee2-161">Jarraitu hartzaileei buruzko informazioaren gainerako urratsekin biltegiratze kontua txertatu ahal izateko.</span><span class="sxs-lookup"><span data-stu-id="0fee2-161">Continue with the remaining steps in audience insights to attach the storage account.</span></span>
