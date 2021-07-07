---
title: Esportatu Customer Insights datuak Salesforce Marketing Cloudera
description: Ikasi konexioa nola konfiguratu eta Salesforce Marketing Cloud-era esportatu.
ms.date: 06/24/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 123f8b2dbb6140785dec6c1b4164d2f513f66a53
ms.sourcegitcommit: 057079532e31c12bac36f374857ba3dc847d6ad0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314570"
---
# <a name="export-segments-and-other-data-to-salesforce-marketing-cloud-preview"></a><span data-ttu-id="87263-103">Esportatu segmentuak eta bestelako datuak Salesforce Marketing Cloud-era (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="87263-103">Export segments and other data to Salesforce Marketing Cloud (preview)</span></span>

<span data-ttu-id="87263-104">Erabili zure bezeroen datuak Salesforce Marketing Cloud-en esportatuz fitxategi transferentzia protokolo seguruaren (SFTP) kokapen baten bidez.</span><span class="sxs-lookup"><span data-stu-id="87263-104">Use your customer data in Salesforce Marketing Cloud by exporting them through a Secure File Transfer Protocol (SFTP) location.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="87263-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="87263-105">Prerequisites for connection</span></span>

- <span data-ttu-id="87263-106">SFTP ostalariaren eta dagozkien administratzaile kredentzialen erabilgarritasuna.</span><span class="sxs-lookup"><span data-stu-id="87263-106">Availability of an SFTP host and corresponding admin credentials.</span></span> [<span data-ttu-id="87263-107">Nola konfiguratu SFTP kokapenak Salesforce Marketing Cloud-erako</span><span class="sxs-lookup"><span data-stu-id="87263-107">How to setup SFTP locations for Salesforce Marketing Cloud</span></span>](https://help.salesforce.com/articleView?id=sf.mc_es_configure_enhanced_ftp.htm&type=5) 

## <a name="known-limitations"></a><span data-ttu-id="87263-108">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="87263-108">Known limitations</span></span>

- <span data-ttu-id="87263-109">Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="87263-109">The runtime of an export depends on your system performance.</span></span> <span data-ttu-id="87263-110">Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa.</span><span class="sxs-lookup"><span data-stu-id="87263-110">We recommend two CPU cores and 1 Gb of memory as minimal configuration of your server.</span></span> 
- <span data-ttu-id="87263-111">Gehienez 100 milioi bezero profil dituzten entitate esportatzaileek 90 minutu iraun dezakete gomendatutako gutxieneko konfigurazioa erabiltzean.</span><span class="sxs-lookup"><span data-stu-id="87263-111">Exporting entities with up to 100 million customer profiles can take 90 minutes when using the recommended minimal configuration.</span></span> 

## <a name="set-up-the-connection-to-salesforce-marketing-cloud"></a><span data-ttu-id="87263-112">Konfiguratu konexioa Salesforce Marketing Cloud-era</span><span class="sxs-lookup"><span data-stu-id="87263-112">Set up the connection to Salesforce Marketing Cloud</span></span>

1. <span data-ttu-id="87263-113">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="87263-113">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="87263-114">Aukeratu **Gehitu konexioa** eta aukeratu **Salesforce Marketing Cloud** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="87263-114">Select **Add connection** and choose **Salesforce Marketing Cloud** to configure the connection.</span></span>

1. <span data-ttu-id="87263-115">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="87263-115">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="87263-116">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="87263-116">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="87263-117">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="87263-117">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="87263-118">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="87263-118">Choose who can use this connection.</span></span> <span data-ttu-id="87263-119">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="87263-119">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="87263-120">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="87263-120">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="87263-121">Eman SFTP kontuaren **Erabiltzaile-izena**, **Pasahitza**, **Ostalari-izena** eta **Esportazio-karpeta**.</span><span class="sxs-lookup"><span data-stu-id="87263-121">Provide a **Username**, **Password**, **Hostname**, and **Export folder** for your SFTP account.</span></span>

1. <span data-ttu-id="87263-122">Hautatu **Egiaztatu** konexioa probatzeko.</span><span class="sxs-lookup"><span data-stu-id="87263-122">Select **Verify** to test the connection.</span></span>

1. <span data-ttu-id="87263-123">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="87263-123">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="87263-124">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="87263-124">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="87263-125">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="87263-125">Configure an export</span></span>

<span data-ttu-id="87263-126">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="87263-126">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="87263-127">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="87263-127">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="87263-128">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="87263-128">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="87263-129">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="87263-129">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="87263-130">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SFTP sekzioan.</span><span class="sxs-lookup"><span data-stu-id="87263-130">In the **Connection for export** field, choose a connection from the SFTP section.</span></span> <span data-ttu-id="87263-131">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="87263-131">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="87263-132">Aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimatu gabe** eta **eremu mugatzailea** esportatutako fitxategietarako.</span><span class="sxs-lookup"><span data-stu-id="87263-132">Choose if you want to export your data **Gzipped** or **Unzipped** and the **field delimiter** for the exported files.</span></span>

1. <span data-ttu-id="87263-133">Aukeratu entitateak, adibidez, esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="87263-133">Select the entities, for example segments, you want to export.</span></span>

   > [!NOTE]
   > <span data-ttu-id="87263-134">Aukeratutako entitate bakoitza bost irteerako fitxategitan banatuko da esportatzerakoan.</span><span class="sxs-lookup"><span data-stu-id="87263-134">Each selected entity will be split up into up to five output files when exported.</span></span> 

1. <span data-ttu-id="87263-135">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="87263-135">Select **Save**.</span></span>

<span data-ttu-id="87263-136">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="87263-136">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="87263-137">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="87263-137">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="87263-138">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="87263-138">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="import-customer-insights-data-from-sftp-location-to-salesforce-marketing-cloud"></a><span data-ttu-id="87263-139">Inportatu Customer Insights datuak SFTP kokalekutik Salesforce Marketing Cloud-era</span><span class="sxs-lookup"><span data-stu-id="87263-139">Import Customer Insights data from SFTP location to Salesforce Marketing Cloud</span></span>

1. <span data-ttu-id="87263-140">Sortu [datuen luzapenak Salesforce Marketing Cloud-en](https://help.salesforce.com/articleView?id=sf.mc_es_create_data_extension.htm&type=5) Customer Insights datu fitxategia SFTP kokapenetik inportatzeko.</span><span class="sxs-lookup"><span data-stu-id="87263-140">Create [data extensions in Salesforce Marketing Cloud](https://help.salesforce.com/articleView?id=sf.mc_es_create_data_extension.htm&type=5) to import the Customer Insights data file from the SFTP location.</span></span>

2. <span data-ttu-id="87263-141">[Inportatu datuak SFTP kokapenetik](https://help.salesforce.com/articleView?id=sf.mc_es_import_data_extension_classic.htm&type=5) Salesforce Marketing Cloud datuen luzapenean sartu.</span><span class="sxs-lookup"><span data-stu-id="87263-141">[Import the data from the SFTP location](https://help.salesforce.com/articleView?id=sf.mc_es_import_data_extension_classic.htm&type=5) into the Salesforce Marketing Cloud data extension.</span></span> 

3. <span data-ttu-id="87263-142">Konfiguratu automatizazioa datuak datu luzapenetara inportatzeko.</span><span class="sxs-lookup"><span data-stu-id="87263-142">Set up the automation to import the data into the data extensions.</span></span> <span data-ttu-id="87263-143">Lortu informazio gehiago [fitxategien jaitsiera automatizazioak eta programatutako automatizazioak](https://help.salesforce.com/articleView?id=sf.mc_as_triggered_automations.htm&type=5).</span><span class="sxs-lookup"><span data-stu-id="87263-143">Learn more about [file drop automations and scheduled automations](https://help.salesforce.com/articleView?id=sf.mc_as_triggered_automations.htm&type=5).</span></span>

   <span data-ttu-id="87263-144">Definitu [fitxategien jaitsiera automatizazioa](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_triggered_automation.htm&type=5) edo bat [programatutako automatizazioa](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_scheduled_automation.htm&type=5).</span><span class="sxs-lookup"><span data-stu-id="87263-144">Define a [file drop automation](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_triggered_automation.htm&type=5) or a  [scheduled automation](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_scheduled_automation.htm&type=5).</span></span> 

<span data-ttu-id="87263-145">Hona hemen adibide bat [automatizazio bat SFTPrekin](https://help.salesforce.com/articleView?id=sf.mc_as_ftp_and_triggered_automation_scenario.htm&type=5).</span><span class="sxs-lookup"><span data-stu-id="87263-145">Here's an example of [an automation with SFTP](https://help.salesforce.com/articleView?id=sf.mc_as_ftp_and_triggered_automation_scenario.htm&type=5).</span></span>

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="87263-146">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="87263-146">Data privacy and compliance</span></span>

<span data-ttu-id="87263-147">Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="87263-147">When you enable Dynamics 365 Customer Insights to transmit data via SFTP, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="87263-148">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="87263-148">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that the export destination meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="87263-149">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="87263-149">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="87263-150">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="87263-150">Your Dynamics 365 Customer Insights administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
