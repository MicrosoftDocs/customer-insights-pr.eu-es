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
ms.openlocfilehash: a2d450635c19432bdd88db74b61c17febdeb568d
ms.sourcegitcommit: aaa275c60c0c77c88196277b266a91d653f8f759
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 04/14/2021
ms.locfileid: "5896266"
---
# <a name="enrich-customer-profiles-with-custom-data-preview"></a><span data-ttu-id="43ac9-103">Aberastu bezeroen profilak datu pertsonalizatuekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="43ac9-103">Enrich customer profiles with custom data (preview)</span></span>

<span data-ttu-id="43ac9-104">Fitxategiak transferitzeko protokolo segurua (SFTP) inportazio pertsonalizatuak datuak bateratzeko prozesua gainditu behar ez duten datuak inportatzeko aukera ematen du.</span><span class="sxs-lookup"><span data-stu-id="43ac9-104">Secure File Transfer Protocol (SFTP) custom import enables you to import data that does not have to go through the process of data unification.</span></span> <span data-ttu-id="43ac9-105">Zure datuak ekartzeko modu malgua, segurua eta erraza da.</span><span class="sxs-lookup"><span data-stu-id="43ac9-105">It's a flexible, secure, and easy way to bring in your data.</span></span> <span data-ttu-id="43ac9-106">SFTP inportazio pertsonalizatua erabil daiteke [SFTP esportazioarekin batera](export-sftp.md). Horrek aberastu behar den bezeroen profileko datuak esportatzen uzten dizu.</span><span class="sxs-lookup"><span data-stu-id="43ac9-106">SFTP custom import can be used in combination with [SFTP export](export-sftp.md) that lets you export the customer profile data that is needed for enrichment.</span></span> <span data-ttu-id="43ac9-107">Datuak prozesatu, aberastu eta SFTP inportazio pertsonalizatuak erabil daitezke datu aberastuak Dynamics 365 Customer Insights-eko hartzaileei buruzko informazioaren gaitasunera itzultzeko.</span><span class="sxs-lookup"><span data-stu-id="43ac9-107">The data can then be processed, enriched, and SFTP custom import can be used to bring the enriched data back to the audience insights capability of Dynamics 365 Customer Insights.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="43ac9-108">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="43ac9-108">Prerequisites</span></span>

<span data-ttu-id="43ac9-109">SFTP inportazio pertsonalizatua konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="43ac9-109">To configure SFTP custom import, the following prerequisites must be met:</span></span>

- <span data-ttu-id="43ac9-110">SFTP ostalarian inportatu beharreko fitxategiaren izena eta kokapena (bidea) dituzu.</span><span class="sxs-lookup"><span data-stu-id="43ac9-110">You have the filename and location (path) of the file to be imported on the SFTP host.</span></span>
- <span data-ttu-id="43ac9-111">Badago *eredua.json* zehazten duen fitxategia [Datuen eredu arruntaren eskema](/common-data-model/) datuak inportatzeko.</span><span class="sxs-lookup"><span data-stu-id="43ac9-111">There is a *model.json* file that specifies [the Common Data Model schema](/common-data-model/) for the data to be imported.</span></span> <span data-ttu-id="43ac9-112">Fitxategi honek inportatzeko fitxategiaren direktorio berean egon behar du.</span><span class="sxs-lookup"><span data-stu-id="43ac9-112">This file must be in the same directory as the file to import.</span></span>
- <span data-ttu-id="43ac9-113">Administratzaile batek SFTP konexioa konfiguratu du dagoeneko *edo* duzu [administratzailea](permissions.md#administrator) baimenak.</span><span class="sxs-lookup"><span data-stu-id="43ac9-113">An SFTP connection has already been configured by an administrator *or* you have [administrator](permissions.md#administrator) permissions.</span></span> <span data-ttu-id="43ac9-114">Datuak inportatu nahi dituzun SFTP kokapenerako erabiltzaile kredentzialak, URLa eta ataka zenbakia beharko dituzu.</span><span class="sxs-lookup"><span data-stu-id="43ac9-114">You'll need the user credentials, URL, and port number for the SFTP location where you want to import data from.</span></span>


## <a name="configure-the-import"></a><span data-ttu-id="43ac9-115">Konfiguratu inportatzea</span><span class="sxs-lookup"><span data-stu-id="43ac9-115">Configure the import</span></span>

1. <span data-ttu-id="43ac9-116">Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="43ac9-116">Go to **Data** > **Enrichment** and select the **Discover** tab.</span></span>

1. <span data-ttu-id="43ac9-117">Hurrengoan **SFTP pertsonalizatutako inportazio-lauza**, hautatu **Aberastu nire datuak** eta gero hautatu **Hasi**.</span><span class="sxs-lookup"><span data-stu-id="43ac9-117">On the **SFTP custom import tile**, select **Enrich my data** and then select **Get started**.</span></span>

   :::image type="content" source="media/SFTP_Custom_Import_tile.png" alt-text="SFTP inportazio pertsonalizatuaren lauza.":::

1. <span data-ttu-id="43ac9-119">Hautatu [konexioa](connections.md) goitibeherako zerrendatik.</span><span class="sxs-lookup"><span data-stu-id="43ac9-119">Select a [connection](connections.md) from the drop-down.</span></span> <span data-ttu-id="43ac9-120">Jarri harremanetan administratzaile batekin konexiorik ez badago.</span><span class="sxs-lookup"><span data-stu-id="43ac9-120">Contact an administrator if no connection is available.</span></span> <span data-ttu-id="43ac9-121">Administratzailea bazara, hautatuz konexioa sor dezakezu **Gehitu konexioa** eta aukeratzea **SFTP inportazio pertsonalizatua** goitibeheratik.</span><span class="sxs-lookup"><span data-stu-id="43ac9-121">If you are an administrator, you can create a connection by selecting **Add connection** and choosing **SFTP Custom Import** from the drop-down.</span></span>

1. <span data-ttu-id="43ac9-122">Aukeratu **Konektatu Inportazio pertsonalizatura** hautatutako konexioa berresteko.</span><span class="sxs-lookup"><span data-stu-id="43ac9-122">Select **Connect to Custom Import** to confirm the selected connection.</span></span>

1.  <span data-ttu-id="43ac9-123">Aukeratu **Hurrengoa** eta sartu **Fitxategi izena** eta **Bidea** inportatu nahi duzun datu fitxategiaren.</span><span class="sxs-lookup"><span data-stu-id="43ac9-123">Select **Next** and enter the **Filename** and **Path** of the data file that you want to import.</span></span>

    :::image type="content" source="media/enrichment-SFTP-path-and-filename.png" alt-text="Pantaila argazkia datuak kokatzerakoan.":::

1. <span data-ttu-id="43ac9-125">Aukeratu **Hurrengoa** eta eman aberasturako izena eta irteerako entitatearen izena.</span><span class="sxs-lookup"><span data-stu-id="43ac9-125">Select **Next** and provide a name for the enrichment and a name for the output entity.</span></span> 

1. <span data-ttu-id="43ac9-126">Aukeratu **Aurreztu aberastasuna** zure aukerak aztertu ondoren.</span><span class="sxs-lookup"><span data-stu-id="43ac9-126">Select **Save enrichment** after reviewing your choices.</span></span>

## <a name="configure-the-connection-for-sftp-custom-import"></a><span data-ttu-id="43ac9-127">Konfiguratu konexioa SFTP pertsonalizatutako inportaziorako</span><span class="sxs-lookup"><span data-stu-id="43ac9-127">Configure the connection for SFTP Custom Import</span></span> 

<span data-ttu-id="43ac9-128">Administratzailea izan behar duzu konexioak konfiguratzeko.</span><span class="sxs-lookup"><span data-stu-id="43ac9-128">You need to be an administrator to configure connections.</span></span> <span data-ttu-id="43ac9-129">Aukeratu **Gehitu konexioa** aberastasun bat konfiguratzerakoan *edo* joan **Administratzailea** > **Konexioak** eta hautatu **Konfiguratu** inportazio pertsonalizatuaren fitxan.</span><span class="sxs-lookup"><span data-stu-id="43ac9-129">Select **Add connection** when configuring an enrichment *or* go to **Admin** > **Connections** and select **Set up** on the Custom Import tile.</span></span>

1. <span data-ttu-id="43ac9-130">Idatzi konexioaren izena **Bistaratzeko izena** kutxa.</span><span class="sxs-lookup"><span data-stu-id="43ac9-130">Enter a name for the connection in the **Display name** box.</span></span>

1. <span data-ttu-id="43ac9-131">Idatzi balio duen erabiltzaile izena, pasahitza eta ostalariaren URLa inportatu beharreko datuak STFP zerbitzariarentzat.</span><span class="sxs-lookup"><span data-stu-id="43ac9-131">Enter valid user name, password, and host URL for the STFP server the data to be imported resides on.</span></span>

1. <span data-ttu-id="43ac9-132">Berrikusi eta eman baimena **Datuen pribatutasuna eta betetzea** aukeratuz **ados** laukia.</span><span class="sxs-lookup"><span data-stu-id="43ac9-132">Review and provide your consent for **Data privacy and compliance** by selecting the **I agree** checkbox.</span></span>

1. <span data-ttu-id="43ac9-133">Aukeratu **Egiaztatu** konfigurazioa balioztatzeko.</span><span class="sxs-lookup"><span data-stu-id="43ac9-133">Select **Verify** to validate the configuration.</span></span>

1. <span data-ttu-id="43ac9-134">Egiaztapena amaitutakoan, konexioa klik eginez gorde daiteke **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="43ac9-134">Once the verification has completed, the connection can be saved by clicking **Save**.</span></span>

> [!div class="mx-imgBorder"]
   > <span data-ttu-id="43ac9-135">![Experian konexioa konfigurazioaren orria](media/enrichment-SFTP-connection.png "Experian konexioa konfigurazioaren orria")</span><span class="sxs-lookup"><span data-stu-id="43ac9-135">![Experian connection configuration page](media/enrichment-SFTP-connection.png "Experian connection configuration page")</span></span>


## <a name="defining-field-mappings"></a><span data-ttu-id="43ac9-136">Eremu-esleipenak definitzen</span><span class="sxs-lookup"><span data-stu-id="43ac9-136">Defining field mappings</span></span> 

<span data-ttu-id="43ac9-137">SFTP zerbitzarian inportatu beharreko fitxategia duen direktorioak ere eduki behar du *model.json* fitxategia.</span><span class="sxs-lookup"><span data-stu-id="43ac9-137">The directory that contains the file to be imported on the SFTP server must also contain a *model.json* file.</span></span> <span data-ttu-id="43ac9-138">Fitxategi honek datuak inportatzeko erabili beharreko eskema definitzen du.</span><span class="sxs-lookup"><span data-stu-id="43ac9-138">This file defines the schema to use for importing the data.</span></span> <span data-ttu-id="43ac9-139">Eskemak [Common Data Model](/common-data-model/) erabili behar du eremuen esleipena zehazteko.</span><span class="sxs-lookup"><span data-stu-id="43ac9-139">The schema has to use [the Common Data Model](/common-data-model/) to specify the field mapping.</span></span> <span data-ttu-id="43ac9-140">model.json fitxategi baten adibide soil batek itxura hau du:</span><span class="sxs-lookup"><span data-stu-id="43ac9-140">A simple example of a model.json file looks like this:</span></span>

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

## <a name="enrichment-results"></a><span data-ttu-id="43ac9-141">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="43ac9-141">Enrichment results</span></span>

<span data-ttu-id="43ac9-142">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="43ac9-142">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="43ac9-143">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="43ac9-143">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="43ac9-144">Prozesatzeko denbora inportatu beharreko datuen tamainaren eta SFTP zerbitzarirako konexioaren araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="43ac9-144">The processing time will depend on the size of the data to be imported and the connection to the SFTP server.</span></span>

<span data-ttu-id="43ac9-145">Aberaste-prozesua amaitu ondoren, inportatutako aberaste pertsonalizatuko datuak berrikus ditzakezu **Nire aberasteak** atalean.</span><span class="sxs-lookup"><span data-stu-id="43ac9-145">After the enrichment process completes, you can review your newly imported custom enrichment data under **My enrichments**.</span></span> <span data-ttu-id="43ac9-146">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="43ac9-146">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="43ac9-147">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="43ac9-147">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="43ac9-148">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="43ac9-148">Next steps</span></span>

<span data-ttu-id="43ac9-149">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="43ac9-149">Build on top of your enriched customer data.</span></span> <span data-ttu-id="43ac9-150">Sortu [segmentuak](segments.md), [neurriak](measures.md), eta [esportatu](export-destinations.md) datuak zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="43ac9-150">Create [segments](segments.md), [measures](measures.md), and [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
