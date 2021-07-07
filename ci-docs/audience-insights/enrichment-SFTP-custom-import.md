---
title: Aberastea SFTP inportazio pertsonalizatuarekin
description: SFTP pertsonalizatutako inportazio aberasteari buruzko informazio orokorra.
ms.date: 04/09/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jodahlMSFT
ms.author: jodahl
manager: shellyha
ms.openlocfilehash: f92b36ac5364ea8586f9cbba7ba03178641555c0
ms.sourcegitcommit: d84d664e67f263bfeb741154d309088c5101b9c3
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "6304635"
---
# <a name="enrich-customer-profiles-with-custom-data-preview"></a><span data-ttu-id="5b391-103">Aberastu bezeroen profilak datu pertsonalizatuekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="5b391-103">Enrich customer profiles with custom data (preview)</span></span>

<span data-ttu-id="5b391-104">Fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) inportazio pertsonalizatuari esker, datuak bateratzeko prozesua igaro behar ez duten datu-aberasteak inporta ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="5b391-104">Secure File Transfer Protocol (SFTP) custom import enables you to import data that doesn't have to go through the process of data unification.</span></span> <span data-ttu-id="5b391-105">Zure datuak ekartzeko modu malgua, segurua eta erraza da.</span><span class="sxs-lookup"><span data-stu-id="5b391-105">It's a flexible, secure, and easy way to bring in your data.</span></span> <span data-ttu-id="5b391-106">SFTP inportazio pertsonalizatua erabil daiteke [SFTP esportazioarekin batera](export-sftp.md). Horrek aberastu behar den bezeroen profileko datuak esportatzen uzten dizu.</span><span class="sxs-lookup"><span data-stu-id="5b391-106">SFTP custom import can be used in combination with [SFTP export](export-sftp.md) that lets you export the customer profile data that is needed for enrichment.</span></span> <span data-ttu-id="5b391-107">Datuak prozesatu eta aberastu daitezke, eta SFTP inportazio pertsonalizatua erabil daiteke datu aberastuak ikusleei buruzko informazioaren gaitasunera itzultzeko Dynamics 365 Customer Insights.</span><span class="sxs-lookup"><span data-stu-id="5b391-107">The data can then be processed and enriched, and SFTP custom import can be used to bring the enriched data back to the audience insights capability of Dynamics 365 Customer Insights.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5b391-108">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="5b391-108">Prerequisites</span></span>

<span data-ttu-id="5b391-109">SFTP inportazio pertsonalizatua konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="5b391-109">To configure SFTP custom import, the following prerequisites must be met:</span></span>

- <span data-ttu-id="5b391-110">SFTP ostalarian inportatu beharreko fitxategiaren izena eta kokapena (bidea) dituzu.</span><span class="sxs-lookup"><span data-stu-id="5b391-110">You have the file name and location (path) of the file to be imported on the SFTP host.</span></span>
- <span data-ttu-id="5b391-111">Badago *eredua.json* zehazten duen fitxategia [Datuen eredu arruntaren eskema](/common-data-model/) datuak inportatzeko.</span><span class="sxs-lookup"><span data-stu-id="5b391-111">There is a *model.json* file that specifies [the Common Data Model schema](/common-data-model/) for the data to be imported.</span></span> <span data-ttu-id="5b391-112">Fitxategi honek inportatzeko fitxategiaren direktorio berean egon behar du.</span><span class="sxs-lookup"><span data-stu-id="5b391-112">This file must be in the same directory as the file to import.</span></span>
- <span data-ttu-id="5b391-113">Administratzaile batek SFTP konexioa konfiguratu du dagoeneko *edo* duzu [administratzailea](permissions.md#administrator) baimenak.</span><span class="sxs-lookup"><span data-stu-id="5b391-113">An SFTP connection has already been configured by an administrator *or* you have [administrator](permissions.md#administrator) permissions.</span></span> <span data-ttu-id="5b391-114">Datuak inportatu nahi dituzun SFTP kokapenerako erabiltzaile kredentzialak, URLa eta ataka zenbakia beharko dituzu.</span><span class="sxs-lookup"><span data-stu-id="5b391-114">You'll need the user credentials, URL, and port number for the SFTP location where you want to import data from.</span></span>


## <a name="configure-the-import"></a><span data-ttu-id="5b391-115">Konfiguratu inportatzea</span><span class="sxs-lookup"><span data-stu-id="5b391-115">Configure the import</span></span>

1. <span data-ttu-id="5b391-116">Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="5b391-116">Go to **Data** > **Enrichment** and select the **Discover** tab.</span></span>

1. <span data-ttu-id="5b391-117">Hurrengoan **SFTP pertsonalizatutako inportazio-lauza**, hautatu **Aberastu nire datuak** eta gero hautatu **Hasi**.</span><span class="sxs-lookup"><span data-stu-id="5b391-117">On the **SFTP custom import tile**, select **Enrich my data** and then select **Get started**.</span></span>

   :::image type="content" source="media/SFTP_Custom_Import_tile.png" alt-text="SFTP inportazio pertsonalizatuaren lauza.":::

1. <span data-ttu-id="5b391-119">Hautatu goitibeherako zerrendako [konexio](connections.md) bat.</span><span class="sxs-lookup"><span data-stu-id="5b391-119">Select a [connection](connections.md) from the dropdown list.</span></span> <span data-ttu-id="5b391-120">Jarri harremanetan administratzaile batekin konexiorik ez badago.</span><span class="sxs-lookup"><span data-stu-id="5b391-120">Contact an administrator if no connection is available.</span></span> <span data-ttu-id="5b391-121">Administratzailea bazara, konexioa sor dezakezu hautatuta **Gehitu konexioa** eta aukeratzea **SFTP inportazio pertsonalizatua** goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="5b391-121">If you are an administrator, you can create a connection by selecting **Add connection** and choosing **SFTP Custom Import** from the dropdown list.</span></span>

1. <span data-ttu-id="5b391-122">Aukeratu **Konektatu Inportazio pertsonalizatura** hautatutako konexioa berresteko.</span><span class="sxs-lookup"><span data-stu-id="5b391-122">Select **Connect to Custom Import** to confirm the selected connection.</span></span>

1.  <span data-ttu-id="5b391-123">Aukeratu **Hurrengoa** eta sartu **Bidea** eta **Fitxategi izena** inportatu nahi duzun datu fitxategiaren.</span><span class="sxs-lookup"><span data-stu-id="5b391-123">Select **Next** and enter the **Path** and **Filename** of the data file that you want to import.</span></span>

    :::image type="content" source="media/enrichment-SFTP-path-and-filename.png" alt-text="Pantaila argazkia datuak kokatzerakoan.":::

1. <span data-ttu-id="5b391-125">Aukeratu **Hurrengoa** eta eman aberasturako izena eta irteerako entitatearen izena.</span><span class="sxs-lookup"><span data-stu-id="5b391-125">Select **Next** and provide a name for the enrichment and a name for the output entity.</span></span> 

1. <span data-ttu-id="5b391-126">Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.</span><span class="sxs-lookup"><span data-stu-id="5b391-126">Select **Save enrichment** after reviewing your choices.</span></span>

## <a name="configure-the-connection-for-sftp-custom-import"></a><span data-ttu-id="5b391-127">Konfiguratu konexioa SFTP pertsonalizatutako inportaziorako</span><span class="sxs-lookup"><span data-stu-id="5b391-127">Configure the connection for SFTP Custom Import</span></span> 

<span data-ttu-id="5b391-128">Administratzailea izan behar duzu konexioak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="5b391-128">You need to be an administrator to configure connections.</span></span> <span data-ttu-id="5b391-129">Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** inportazio pertsonalizatuaren fitxan.</span><span class="sxs-lookup"><span data-stu-id="5b391-129">Select **Add connection** when configuring an enrichment *or* go to **Admin** > **Connections** and select **Set up** on the Custom Import tile.</span></span>

1. <span data-ttu-id="5b391-130">Idatzi konexioaren izena **Bistaratzeko izena** kutxa.</span><span class="sxs-lookup"><span data-stu-id="5b391-130">Enter a name for the connection in the **Display name** box.</span></span>

1. <span data-ttu-id="5b391-131">Idatzi balio duen erabiltzaile izena, pasahitza eta ostalariaren URLa inportatu beharreko datuak dauden SFTP zerbitzariarentzat.</span><span class="sxs-lookup"><span data-stu-id="5b391-131">Enter a valid username, password, and host URL for the SFTP server that the data to be imported resides on.</span></span>

1. <span data-ttu-id="5b391-132">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="5b391-132">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span>

1. <span data-ttu-id="5b391-133">Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.</span><span class="sxs-lookup"><span data-stu-id="5b391-133">Select **Verify** to validate the configuration.</span></span>

1. <span data-ttu-id="5b391-134">Egiaztapena amaitutakoan, konexioa hautatuta gorde daiteke **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="5b391-134">Once the verification has completed, the connection can be saved by selecting **Save**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="5b391-135">![Experian konexioaren konfigurazio-orria](media/enrichment-SFTP-connection.png "Experian konexioaren konfigurazio-orria")</span><span class="sxs-lookup"><span data-stu-id="5b391-135">![Experian connection configuration page](media/enrichment-SFTP-connection.png "Experian connection configuration page")</span></span>


## <a name="defining-field-mappings"></a><span data-ttu-id="5b391-136">Eremu-esleipenak definitzen</span><span class="sxs-lookup"><span data-stu-id="5b391-136">Defining field mappings</span></span> 

<span data-ttu-id="5b391-137">SFTP zerbitzarian inportatu beharreko fitxategia duen direktorioak ere eduki behar du *model.json* fitxategia.</span><span class="sxs-lookup"><span data-stu-id="5b391-137">The directory that contains the file to be imported on the SFTP server must also contain a *model.json* file.</span></span> <span data-ttu-id="5b391-138">Fitxategi honek datuak inportatzeko erabili beharreko eskema definitzen du.</span><span class="sxs-lookup"><span data-stu-id="5b391-138">This file defines the schema to use for importing the data.</span></span> <span data-ttu-id="5b391-139">Eskemak erabili behar du [Common Data Model](/common-data-model/) eremuen mapaketa zehazteko.</span><span class="sxs-lookup"><span data-stu-id="5b391-139">The schema has to use [Common Data Model](/common-data-model/) to specify the field mapping.</span></span> <span data-ttu-id="5b391-140">model.json fitxategi baten adibide soil batek itxura hau du:</span><span class="sxs-lookup"><span data-stu-id="5b391-140">A simple example of a model.json file looks like this:</span></span>

```
{
    "name": "EnrichmentFromMicrosoft",
    "description": "Model containing data enrichment",
    "entities": [
        {
            "name": "CustomImport",
            "attributes": [
                {
                    "name": "CustomerId",
                    "friendlyName": "Client id",
                    "dataType": "string"
                },
                {
                    "name": "PreferredCity",
                    "friendlyName": "Preferred City for vacation",
                    "dataType": "string"
                },
                {
                    "name": "PreferredTransportation",
                    "friendlyName": "Preferred transportation",
                    "dataType": "string"
                }
            ],
            "annotations": [
                {
                    "name": "c360:PrimaryKey",
                    "value": "CustomerId"
                }
            ]
        }
    ],
    "modifiedTime": "2020-01-02T12:00:00+08:00",
    "annotations": [
        {
            "name": "testAnnotation",
            "value": "testValue"
        }
    ]
}
```

## <a name="enrichment-results"></a><span data-ttu-id="5b391-141">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="5b391-141">Enrichment results</span></span>

<span data-ttu-id="5b391-142">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="5b391-142">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="5b391-143">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="5b391-143">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="5b391-144">Prozesatzeko denbora inportatu beharreko datuen tamainaren eta SFTP zerbitzarirako konexioaren araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="5b391-144">The processing time will depend on the size of the data to be imported and the connection to the SFTP server.</span></span>

<span data-ttu-id="5b391-145">Aberaste-prozesua amaitu ondoren, inportatutako aberaste pertsonalizatuko datuak berrikus ditzakezu **Nire aberasteak** atalean.</span><span class="sxs-lookup"><span data-stu-id="5b391-145">After the enrichment process completes, you can review your newly imported custom enrichment data under **My enrichments**.</span></span> <span data-ttu-id="5b391-146">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="5b391-146">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="5b391-147">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="5b391-147">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5b391-148">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="5b391-148">Next steps</span></span>

<span data-ttu-id="5b391-149">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="5b391-149">Build on top of your enriched customer data.</span></span> <span data-ttu-id="5b391-150">Sortu [segmentuak](segments.md) eta [neurriak](measures.md), eta are [datuak esportatu](export-destinations.md) zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="5b391-150">Create [segments](segments.md) and [measures](measures.md), and [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
