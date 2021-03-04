---
title: Aberastea SFTP inportazio pertsonalizatuarekin
description: SFTP pertsonalizatutako inportazio aberasteari buruzko informazio orokorra.
ms.date: 11/18/2020
ms.reviewer: kishorem
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: jdahl
ms.author: mhart
manager: shellyha
ms.openlocfilehash: f25dcc08d96d36507e47af0d7b184003ae095819
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269591"
---
# <a name="enrich-customer-profiles-with-custom-data-preview"></a><span data-ttu-id="cd6e3-103">Aberastu bezeroen profilak datu pertsonalizatuekin (aurrebista)</span><span class="sxs-lookup"><span data-stu-id="cd6e3-103">Enrich customer profiles with custom data (preview)</span></span>

<span data-ttu-id="cd6e3-104">Fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) inportazio pertsonalizatuari esker, datuak bateratzeko prozesua igaro behar ez duten datu-aberasteak inporta ditzakezu.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-104">Secure File Transfer Protocol(SFTP) custom import enables you to import data that doesn't have to go through the process of data unification.</span></span> <span data-ttu-id="cd6e3-105">Zure datuak ekartzeko modu malgua, segurua eta erraza da.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-105">It's a flexible, secure, and easy way to bring in your data.</span></span> <span data-ttu-id="cd6e3-106">SFTP inportazio pertsonalizatua erabil daiteke [SFTP esportazioarekin batera](export-sftp.md). Horrek aberastu behar den bezeroen profileko datuak esportatzen uzten dizu.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-106">SFTP custom import can be used in combination with [SFTP export](export-sftp.md) that lets you export the customer profile data that is needed for enrichment.</span></span> <span data-ttu-id="cd6e3-107">Datuak prozesatu, aberastu eta SFTP inportazio pertsonalizatuak erabil daitezke datu aberastuak Dynamics 365 Customer Insights-eko hartzaileei buruzko informazioaren gaitasunera itzultzeko.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-107">The data can then be processed, enriched, and SFTP custom import can be used to bring the enriched data back to the audience insights capability of Dynamics 365 Customer Insights.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cd6e3-108">Aurrebaldintzak</span><span class="sxs-lookup"><span data-stu-id="cd6e3-108">Prerequisites</span></span>

<span data-ttu-id="cd6e3-109">SFTP inportazio pertsonalizatua konfiguratzeko, honako baldintza hauek bete behar dira:</span><span class="sxs-lookup"><span data-stu-id="cd6e3-109">To configure SFTP custom import, the following prerequisites must be met:</span></span>

- <span data-ttu-id="cd6e3-110">Erabiltzaile kredentzialak (erabiltzaile izena eta pasahitza) dituzue datuak inportatuko diren SFTP kokapenerako.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-110">You have user credentials (user name and password) for the SFTP location where the data that is going to be imported from.</span></span>
- <span data-ttu-id="cd6e3-111">STFP ostalariaren URLa eta ataka zenbakia (normalean 22) dituzu.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-111">You have the URL and port number (usually 22) for the STFP host.</span></span>
- <span data-ttu-id="cd6e3-112">SFTP ostalarian inportatuko den fitxategiaren izena eta kokapena dituzu.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-112">You have the filename and location of the file to be imported on the SFTP host.</span></span>
- <span data-ttu-id="cd6e3-113">Bada inportatu nahi diren datuen eskema zehazten duen *model.json* fitxategia.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-113">There's a *model.json* file that specifies the schema for the data that are to be imported.</span></span> <span data-ttu-id="cd6e3-114">Fitxategi honek inportatzeko fitxategiaren direktorio berean egon behar du.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-114">This file must be in the same directory as the file to import.</span></span>
- <span data-ttu-id="cd6e3-115">[Administratzaile](permissions.md#administrator) baimena duzu.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-115">You have [Administrator](permissions.md#administrator) permission.</span></span>

## <a name="configuration"></a><span data-ttu-id="cd6e3-116">Konfigurazioa</span><span class="sxs-lookup"><span data-stu-id="cd6e3-116">Configuration</span></span>

1. <span data-ttu-id="cd6e3-117">Joan **Datuak** > **Aberastea** eta hautatu **Deskubritu** fitxa.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-117">Go to **Data** > **Enrichment** and select the **Discover** tab.</span></span>

1. <span data-ttu-id="cd6e3-118">**SFTP inportazio pertsonalizatuaren lauzan**, hautatu **Aberastu nire datuak**.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-118">On the **SFTP custom import tile**, select **Enrich my data**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cd6e3-119">![SFTP inportazio pertsonalizatuaren lauza](media/SFTP_Custom_Import_tile.png "SFTP inportazio pertsonalizatuaren lauza")</span><span class="sxs-lookup"><span data-stu-id="cd6e3-119">![SFTP Custom Import tile](media/SFTP_Custom_Import_tile.png "SFTP Custom Import tile")</span></span>

1. <span data-ttu-id="cd6e3-120">Aukeratu **Hasi** eta eman SFTP zerbitzariaren kredentzialak eta helbidea.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-120">Select **Get started** and provide the credentials and the address for the SFTP server.</span></span> <span data-ttu-id="cd6e3-121">Adibidez, sftp://mysftpserver.com:22.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-121">For example, sftp://mysftpserver.com:22.</span></span>

1. <span data-ttu-id="cd6e3-122">Idatzi datuak dituen fitxategiaren izena eta SFTP zerbitzarirako bide-izena, ez badago erro-karpetan.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-122">Enter the name of the file that contains the data and path to the file on the SFTP server if it's not in the root folder.</span></span>

1. <span data-ttu-id="cd6e3-123">Berretsi sarrera guztiak **Konektatu inportazio pertsonalizatura** hautatuta.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-123">Confirm all inputs by selecting **Connect to Custom Import**.</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="cd6e3-124">![SFTP inportazio pertsonalizatuaren konfigurazioaren kontrol mugikorra](media/SFTP_Custom_Import_Configuration_flyout.png "SFTP inportazio pertsonalizatuaren konfigurazioaren kontrol mugikorra")</span><span class="sxs-lookup"><span data-stu-id="cd6e3-124">![SFTP Custom Import Configuration flyout](media/SFTP_Custom_Import_Configuration_flyout.png "SFTP Custom Import Configuration flyout")</span></span>

## <a name="defining-field-mappings"></a><span data-ttu-id="cd6e3-125">Eremu-esleipenak definitzen</span><span class="sxs-lookup"><span data-stu-id="cd6e3-125">Defining field mappings</span></span> 

<span data-ttu-id="cd6e3-126">SFTP zerbitzarian inportatu beharreko fitxategia duen direktorioak ere eduki behar du *model.json* fitxategia.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-126">The directory that contains the file to be imported on the SFTP server must also contain a *model.json* file.</span></span> <span data-ttu-id="cd6e3-127">Fitxategi honek datuak inportatzeko erabili beharreko eskema definitzen du.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-127">This file defines the schema to use for importing the data.</span></span> <span data-ttu-id="cd6e3-128">Eskemak [Common Data Model](https://docs.microsoft.com/common-data-model/) erabili behar du eremuen esleipena zehazteko.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-128">The schema has to use [the Common Data Model](https://docs.microsoft.com/common-data-model/) to specify the field mapping.</span></span> <span data-ttu-id="cd6e3-129">model.json fitxategi baten adibide soil batek itxura hau du:</span><span class="sxs-lookup"><span data-stu-id="cd6e3-129">A simple example of a model.json file looks like this:</span></span>

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

## <a name="enrichment-results"></a><span data-ttu-id="cd6e3-130">Aberastearen emaitzak</span><span class="sxs-lookup"><span data-stu-id="cd6e3-130">Enrichment results</span></span>

<span data-ttu-id="cd6e3-131">Aberasteko prozesua hasteko, hautatu **Korrika egin** komando barratik.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-131">To start the enrichment process, select **Run** from the command bar.</span></span> <span data-ttu-id="cd6e3-132">Gainera, sistemak aberastea automatikoki exekutatzen utzi dezakezu [freskatze programatua](system.md#schedule-tab).</span><span class="sxs-lookup"><span data-stu-id="cd6e3-132">You can also let the system run the enrichment automatically as part of a [scheduled refresh](system.md#schedule-tab).</span></span> <span data-ttu-id="cd6e3-133">Prozesatzeko denbora inportatu beharreko datuen tamainaren eta SFTP zerbitzarirako konexioaren araberakoa izango da.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-133">The processing time will depend on the size of the data to be imported and the connection to the SFTP server.</span></span>

<span data-ttu-id="cd6e3-134">Aberaste-prozesua amaitu ondoren, inportatutako aberaste pertsonalizatuko datuak berrikus ditzakezu **Nire aberasteak** atalean.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-134">After the enrichment process completes, you can review your newly imported custom enrichment data under **My enrichments**.</span></span> <span data-ttu-id="cd6e3-135">Gainera, azken eguneratzearen ordua eta profil aberastuen kopurua aurkituko dituzu.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-135">Additionally, you'll find the time of the last update and the number of enriched profiles.</span></span>

<span data-ttu-id="cd6e3-136">Aberastutako profil bakoitzaren ikuspegi zehatza sar dezakezu hautatuta **Ikusi aberastutako datuak**.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-136">You can access a detailed view of each enriched profile by selecting **View enriched data**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="cd6e3-137">Hurrengo urratsak</span><span class="sxs-lookup"><span data-stu-id="cd6e3-137">Next steps</span></span>

<span data-ttu-id="cd6e3-138">Eraiki zure bezeroen datu aberastuen gainean.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-138">Build on top of your enriched customer data.</span></span> <span data-ttu-id="cd6e3-139">Sortu [segmentuak](segments.md), [neurriak](measures.md), eta [esportatu](export-destinations.md) datuak zure bezeroei esperientzia pertsonalizatuak emateko.</span><span class="sxs-lookup"><span data-stu-id="cd6e3-139">Create [segments](segments.md), [measures](measures.md), and [export the data](export-destinations.md) to deliver personalized experiences to your customers.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]