---
title: Esportatu Customer Insights datuak SFTP ostalarietara
description: Ikasi konexioa nola konfiguratu eta SFTP kokapen batera esportatu.
ms.date: 03/03/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 3663a48955f0b1db8a96e25403e5f8947bc6a220
ms.sourcegitcommit: e8e03309ba2515374a70c132d0758f3e1e1851d0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/04/2021
ms.locfileid: "5976878"
---
# <a name="export-segment-lists-and-other-data-to-sftp-preview"></a><span data-ttu-id="6d4a5-103">Esportatu segmentu-zerrendak eta beste datu batzuk SFTP-ra (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="6d4a5-103">Export segment lists and other data to SFTP (preview)</span></span>

<span data-ttu-id="6d4a5-104">Erabili zure bezeroen datuak hirugarrenen aplikazioetan, fitxategi transferentzia protokolo segurura (SFTP) kokapen batera esportatuz.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-104">Use your customer data in third-party applications by exporting them to a Secure File Transfer Protocol (SFTP) location.</span></span>

## <a name="prerequisites-for-connection"></a><span data-ttu-id="6d4a5-105">Konexioaren aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="6d4a5-105">Prerequisites for connection</span></span>

- <span data-ttu-id="6d4a5-106">SFTP ostalariaren erabilgarritasuna eta dagozkien egiaztagiriak.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-106">Availability of an SFTP host and corresponding credentials.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="6d4a5-107">Muga ezagunak</span><span class="sxs-lookup"><span data-stu-id="6d4a5-107">Known limitations</span></span>

- <span data-ttu-id="6d4a5-108">Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-108">The runtime of an export depends on your system performance.</span></span> <span data-ttu-id="6d4a5-109">Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-109">We recommend two CPU cores and 1 Gb of memory as minimal configuration of your server.</span></span> 
- <span data-ttu-id="6d4a5-110">Gehienez 100 milioi bezero profil dituzten entitate esportatzaileek 90 minutu iraun dezakete gomendatutako gutxieneko konfigurazioa erabiltzen duten bi PUZ nukleorekin eta 1 Gb memoria.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-110">Exporting entities with up to 100 million customer profiles can take 90 minutes when using the recommended minimal configuration of two CPU cores and 1 Gb of memory.</span></span> 

## <a name="set-up-connection-to-sftp"></a><span data-ttu-id="6d4a5-111">Konfiguratu konexioa SFTP-en</span><span class="sxs-lookup"><span data-stu-id="6d4a5-111">Set up connection to SFTP</span></span>

1. <span data-ttu-id="6d4a5-112">Joan **Administratzailea** > **Konexioak**.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-112">Go to **Admin** > **Connections**.</span></span>

1. <span data-ttu-id="6d4a5-113">Hautatu **Gehitu konexioa** eta aukeratu **SFTP** konexioa konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-113">Select **Add connection** and choose **SFTP** to configure the connection.</span></span>

1. <span data-ttu-id="6d4a5-114">Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-114">Give your connection a recognizable name in the **Display name** field.</span></span> <span data-ttu-id="6d4a5-115">Izena eta konexio motak konexio bat deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-115">The name and the type of the connection describe this connection.</span></span> <span data-ttu-id="6d4a5-116">Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-116">We recommend choosing a name that explains the purpose and target of the connection.</span></span>

1. <span data-ttu-id="6d4a5-117">Aukeratu nork erabil dezakeen konexioa.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-117">Choose who can use this connection.</span></span> <span data-ttu-id="6d4a5-118">Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-118">If you take no action, the default will be Administrators.</span></span> <span data-ttu-id="6d4a5-119">Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).</span><span class="sxs-lookup"><span data-stu-id="6d4a5-119">For more information, see [Allow contributors to use a connection for exports](connections.md#allow-contributors-to-use-a-connection-for-exports).</span></span>

1. <span data-ttu-id="6d4a5-120">Eman SFTP kontuaren **Erabiltzaile-izena**, **Pasahitza**, **Ostalari-izena** eta **Esportazio-karpeta**.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-120">Provide a **Username**, **Password**, **Hostname**, and **Export folder** for your SFTP account.</span></span>

1. <span data-ttu-id="6d4a5-121">Hautatu **Egiaztatu** konexioa probatzeko.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-121">Select **Verify** to test the connection.</span></span>

1. <span data-ttu-id="6d4a5-122">Aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimatu gabe** eta **eremu mugatzailea** esportatutako fitxategietarako.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-122">Choose if you want to export your data **Gzipped** or **Unzipped** and the **field delimiter** for the exported files.</span></span>

1. <span data-ttu-id="6d4a5-123">Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-123">Select **I agree** to confirm the **Data privacy and compliance**.</span></span>

1. <span data-ttu-id="6d4a5-124">Hautatu **Gorde** konexioa osatzeko.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-124">Select **Save** to complete the connection.</span></span>

## <a name="configure-an-export"></a><span data-ttu-id="6d4a5-125">Konfiguratu esportazio bat</span><span class="sxs-lookup"><span data-stu-id="6d4a5-125">Configure an export</span></span>

<span data-ttu-id="6d4a5-126">Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-126">You can configure this export if you have access to a connection of this type.</span></span> <span data-ttu-id="6d4a5-127">Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).</span><span class="sxs-lookup"><span data-stu-id="6d4a5-127">For more information, see [Permissions needed to configure an export](export-destinations.md#set-up-a-new-export).</span></span>

1. <span data-ttu-id="6d4a5-128">Joan **Datuak** > **Esportazioak**.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-128">Go to **Data** > **Exports**.</span></span>

1. <span data-ttu-id="6d4a5-129">Esportazio berria sortzeko, hautatu **Gehitu helmuga**.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-129">To create a new export, select **Add destination**.</span></span>

1. <span data-ttu-id="6d4a5-130">Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SFTP sekzioan.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-130">In the **Connection for export** field, choose a connection from the SFTP section.</span></span> <span data-ttu-id="6d4a5-131">Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-131">If you don't see this section name, there are no connections of this type available to you.</span></span>

1. <span data-ttu-id="6d4a5-132">Aukeratu entitateak, adibidez, esportatu nahi dituzun segmentuak.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-132">Select the entities, for example segments, you want to export.</span></span>

   > [!NOTE]
   > <span data-ttu-id="6d4a5-133">Aukeratutako entitate bakoitza bost irteerako fitxategitan banatuko da esportatzerakoan.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-133">Each selected entity will be split up into up to five output files when exported.</span></span> 

1. <span data-ttu-id="6d4a5-134">Sakatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-134">Select **Save**.</span></span>

<span data-ttu-id="6d4a5-135">Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-135">Saving an export doesn't run the export immediately.</span></span>

<span data-ttu-id="6d4a5-136">Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="6d4a5-136">The export runs with every [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="6d4a5-137">Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand).</span><span class="sxs-lookup"><span data-stu-id="6d4a5-137">You can also [export data on demand](export-destinations.md#run-exports-on-demand).</span></span> 

## <a name="data-privacy-and-compliance"></a><span data-ttu-id="6d4a5-138">Datuen pribatutasuna eta arau-gordetzea</span><span class="sxs-lookup"><span data-stu-id="6d4a5-138">Data privacy and compliance</span></span>

<span data-ttu-id="6d4a5-139">Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-139">When you enable Dynamics 365 Customer Insights to transmit data via SFTP, you allow transfer of data outside of the compliance boundary for Dynamics 365 Customer Insights, including potentially sensitive data such as Personal Data.</span></span> <span data-ttu-id="6d4a5-140">Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-140">Microsoft will transfer such data at your instruction, but you are responsible for ensuring that the export destination meets any privacy or security obligations you may have.</span></span> <span data-ttu-id="6d4a5-141">Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).</span><span class="sxs-lookup"><span data-stu-id="6d4a5-141">For more information, see [Microsoft Privacy Statement](https://go.microsoft.com/fwlink/?linkid=396732).</span></span>
<span data-ttu-id="6d4a5-142">Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.</span><span class="sxs-lookup"><span data-stu-id="6d4a5-142">Your Dynamics 365 Customer Insights Administrator can remove this export destination at any time to discontinue use of this functionality.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
