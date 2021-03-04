---
title: Entitateen eta entitateen bide-izenen arteko erlazioak
description: Sortu eta kudeatu datu-iturburu anitzetako entitateen arteko harremanak.
ms.date: 04/14/2020
ms.reviewer: mukeshpo
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 292da986faa7f62d8aa73ed7214075612178e2e1
ms.sourcegitcommit: 139548f8a2d0f24d54c4a6c404a743eeeb8ef8e0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 02/15/2021
ms.locfileid: "5269851"
---
# <a name="relationships-between-entities"></a><span data-ttu-id="a7313-103">Harremanak entitateen artean</span><span class="sxs-lookup"><span data-stu-id="a7313-103">Relationships between entities</span></span>

<span data-ttu-id="a7313-104">Harremanek entitateak lotzen eta zure datuen grafikoa sortzen laguntzen dute entitateek entitate batetik bestera erreferentzia daitekeen identifikatzaile komun bat (atzerriko gakoa) partekatzen dutenean.</span><span class="sxs-lookup"><span data-stu-id="a7313-104">Relationships help you connect entities and generate a graph of your data when entities share a common identifier (foreign key) that can be referenced from one entity to another.</span></span> <span data-ttu-id="a7313-105">Konektatutako entitateek datu-iturri anitzetan oinarritutako segmentuak eta neurriak definitzeko aukera ematen dute.</span><span class="sxs-lookup"><span data-stu-id="a7313-105">Connected entities enable you to define segments and measures based on multiple data sources.</span></span>

<span data-ttu-id="a7313-106">Bi harreman-mota daude:</span><span class="sxs-lookup"><span data-stu-id="a7313-106">There are two types of relationships.</span></span> <span data-ttu-id="a7313-107">Editatu gabeko sistema-harremanak, automatikoki sortzen direnak eta erabiltzaileek sortutako eta konfiguratutako harreman pertsonalizatuak.</span><span class="sxs-lookup"><span data-stu-id="a7313-107">Non-editable system relationships, which are created automatically, and custom relationships created and configured by users.</span></span>

<span data-ttu-id="a7313-108">Partiduen eta bateratze prozesuen artean, sistemen arteko harremanak agertokien atzean sortzen dira, bat etorri adimentsuan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="a7313-108">During the match and merge processes, system relationships are created behind the scenes based on intelligent matching.</span></span> <span data-ttu-id="a7313-109">Harreman hauek Bezeroaren Profilaren erregistroak dagozkien beste erakundeen erregistroekin erlazionatzen lagunduko dute.</span><span class="sxs-lookup"><span data-stu-id="a7313-109">These relationships help relate the Customer Profile records with other corresponding entities' records.</span></span> <span data-ttu-id="a7313-110">Hurrengo diagrama honetan, hiru sistema harreman sortu dira, bezero entitatea entitate osagarriekin lotzen denean Bezeroaren azken profila entitatea ekoizteko.</span><span class="sxs-lookup"><span data-stu-id="a7313-110">The following diagram illustrates the creation of three system relationships when the customer entity is matched with additional entities to produce the final Customer Profile entity.</span></span>

> [!div class="mx-imgBorder"]
> <span data-ttu-id="a7313-111">![Erlazioak sortzen](media/relationships-entities-merge.png "Erlazioak sortzen")</span><span class="sxs-lookup"><span data-stu-id="a7313-111">![Relationship creation](media/relationships-entities-merge.png "Relationship creation")</span></span>

- <span data-ttu-id="a7313-112">***CustomerToContact* harremana** Bezeroaren entitatearen eta Harremanetarako entitatearen artean sortu zen.</span><span class="sxs-lookup"><span data-stu-id="a7313-112">***CustomerToContact* relationship** was created between the Customer entity and the Contact entity.</span></span> <span data-ttu-id="a7313-113">Bezero entitateak giltza eremua lortzen du **Contact_contactId** Harremanetarako entitatearen gako eremua erlazionatzeko **contactId**.</span><span class="sxs-lookup"><span data-stu-id="a7313-113">The Customer entity gets the key field **Contact_contactId** to relate to the Contact entity key field **contactId**.</span></span>
- <span data-ttu-id="a7313-114">***CustomerToAccount* harremana** Bezeroaren entitatearen eta konturako entitatearen artean sortu zen.</span><span class="sxs-lookup"><span data-stu-id="a7313-114">***CustomerToAccount* relationship** was created between the Customer entity and the Account entity.</span></span> <span data-ttu-id="a7313-115">Bezero entitateak giltza eremua lortzen du **Account_contactId** Konturako entitatearen gako eremua erlazionatzeko **accountId**.</span><span class="sxs-lookup"><span data-stu-id="a7313-115">The Customer entity gets the key field **Account_accountId** to relate to the Account entity key field **accountId**.</span></span>
- <span data-ttu-id="a7313-116">***CustomerToWebAccount* harremana** Bezeroaren entitatearen eta web-konturako entitatearen artean sortu zen.</span><span class="sxs-lookup"><span data-stu-id="a7313-116">***CustomerToWebAccount* relationship** was created between the Customer entity and the WebAccount entity.</span></span> <span data-ttu-id="a7313-117">Bezero entitateak giltza eremua lortzen du **WebAccount_contactId** Web-Konturako entitatearen gako eremua erlazionatzeko **webaccountId**.</span><span class="sxs-lookup"><span data-stu-id="a7313-117">The Customer entity gets the key field **WebAccount_webaccountId** to relate to the WebAccount entity key field **webaccountId**.</span></span>

## <a name="create-a-relationship"></a><span data-ttu-id="a7313-118">Sortu erlazioa</span><span class="sxs-lookup"><span data-stu-id="a7313-118">Create a relationship</span></span>

<span data-ttu-id="a7313-119">Definitu harreman pertsonalizatuak **Harremanak** orria.</span><span class="sxs-lookup"><span data-stu-id="a7313-119">Define custom relationships on the **Relationships** page.</span></span> <span data-ttu-id="a7313-120">Harreman bakoitza Iturri entitate batek (atzerriko giltza duen entitatea) eta Xede entitate batek (iturri erakundearen atzerriko gakoa adierazten duen entitatea) osatzen dute.</span><span class="sxs-lookup"><span data-stu-id="a7313-120">Each relationship consists of a Source entity (the entity that holds the foreign key) and a Target entity (the entity that the source entity's foreign key points to).</span></span>

1. <span data-ttu-id="a7313-121">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Harremanak**.</span><span class="sxs-lookup"><span data-stu-id="a7313-121">In audience insights, go to **Data** > **Relationships**.</span></span>

2. <span data-ttu-id="a7313-122">Hautatu **Harreman berria**.</span><span class="sxs-lookup"><span data-stu-id="a7313-122">Select **New relationship**.</span></span>

3. <span data-ttu-id="a7313-123">**Gehitu harremana** panelean, eman ondorengo informazioa:</span><span class="sxs-lookup"><span data-stu-id="a7313-123">In the **Add relationship** pane, provide the following information:</span></span>

   > [!div class="mx-imgBorder"]
   > <span data-ttu-id="a7313-124">![Sartu harremanaren xehetasunak](media/relationships-add.png "Sartu harremanaren xehetasunak")</span><span class="sxs-lookup"><span data-stu-id="a7313-124">![Enter relationship details](media/relationships-add.png "Enter relationship details")</span></span>

   - <span data-ttu-id="a7313-125">**Harreman izena**: Harremanaren xedea islatzen duen izena (adibidez, **AccountWebLogs**).</span><span class="sxs-lookup"><span data-stu-id="a7313-125">**Relationship name**: Name that reflects the purpose of the relationship (for example, **AccountWebLogs**).</span></span>
   - <span data-ttu-id="a7313-126">**Deskribapena**: Erlazio-funtzioaren azalpena.</span><span class="sxs-lookup"><span data-stu-id="a7313-126">**Description**: Description of the relationship.</span></span>
   - <span data-ttu-id="a7313-127">**Iturri entitatea**: Harremanean iturri gisa erabiltzen den entitatea hautatu (adibidez, WebLog).</span><span class="sxs-lookup"><span data-stu-id="a7313-127">**Source entity**: Select the entity that is used as a source in the relationship (for example, WebLog).</span></span>
   - <span data-ttu-id="a7313-128">**Kardinalitatea**: Iturri entitatearen erregistroen kardinalitatea aukeratu.</span><span class="sxs-lookup"><span data-stu-id="a7313-128">**Cardinality**: Select the cardinality of the source entity records.</span></span> <span data-ttu-id="a7313-129">Adibidez, "askok" esan nahi du Weblog erregistro anitz WebAccount-ekin erlazionatuta daudela.</span><span class="sxs-lookup"><span data-stu-id="a7313-129">For example, "many" means that multiple Weblog records are related to one WebAccount.</span></span>
   - <span data-ttu-id="a7313-130">**Iturriaren gako eremua**: Iturri-erakundeko atzerriko gako-eremua adierazten du.</span><span class="sxs-lookup"><span data-stu-id="a7313-130">**Source key field**: This represents the foreign key field in the source entity.</span></span> <span data-ttu-id="a7313-131">Adibidez, WebLog-ek dauka **accountId** atzerriko gako eremua.</span><span class="sxs-lookup"><span data-stu-id="a7313-131">For example, WebLog has the **accountId** foreign key field.</span></span>
   - <span data-ttu-id="a7313-132">**Helmugako entitatea**: Harremanean helmuga gisa erabiltzen den entitatea hautatu (adibidez, WebAccount).</span><span class="sxs-lookup"><span data-stu-id="a7313-132">**Target entity**: Select the entity that is used as a target in the relationship (for example, WebAccount).</span></span>
   - <span data-ttu-id="a7313-133">**Helmugako kardinalitatea**: helmugako entitatearen erregistroen kardinalitatea aukeratu.</span><span class="sxs-lookup"><span data-stu-id="a7313-133">**Target cardinality**: Select the cardinality of the target entity records.</span></span> <span data-ttu-id="a7313-134">Adibidez, "bat" esan nahi du Weblog erregistro anitz WebAccount-ekin erlazionatuta daudela.</span><span class="sxs-lookup"><span data-stu-id="a7313-134">For example, "one" means that multiple Weblog records are related to one WebAccount.</span></span>
   - <span data-ttu-id="a7313-135">**Helburuko gako eremua**: Eremu honek xede entitatearen funtsezko eremua adierazten du.</span><span class="sxs-lookup"><span data-stu-id="a7313-135">**Target key field**: This field represents the key field of target entity.</span></span> <span data-ttu-id="a7313-136">Adibidez, WebAccount-ek dauka **accountId** gako eremua.</span><span class="sxs-lookup"><span data-stu-id="a7313-136">For example, WebAccount has the **accountId** key field.</span></span>

> [!NOTE]
> <span data-ttu-id="a7313-137">Banan-banan eta banan-banako harremanak bakarrik onartzen dira.</span><span class="sxs-lookup"><span data-stu-id="a7313-137">Only many-to-one and one-to-one relationships are supported.</span></span> <span data-ttu-id="a7313-138">Asko eta asko harremanak bat eta bi erlazio eta lotura-entitate bat (iturri-entitatea eta xede-entitatea konektatzeko erabiltzen den entitatea) sor daitezke.</span><span class="sxs-lookup"><span data-stu-id="a7313-138">Many-to-many relationships can be created using two many-to-one relationships and a link entity (an entity that is used to connect the source entity and the target entity).</span></span>

## <a name="delete-a-relationship"></a><span data-ttu-id="a7313-139">Ezabatu erlazioa</span><span class="sxs-lookup"><span data-stu-id="a7313-139">Delete a relationship</span></span>

1. <span data-ttu-id="a7313-140">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Harremanak**.</span><span class="sxs-lookup"><span data-stu-id="a7313-140">In audience insights, go to **Data** > **Relationships**.</span></span>

2. <span data-ttu-id="a7313-141">Hautatu ezabatu nahi dituzun harremanen kontrol-laukiak.</span><span class="sxs-lookup"><span data-stu-id="a7313-141">Select check boxes for the relationships you want to delete.</span></span>

3. <span data-ttu-id="a7313-142">Aukeratu **Ezabatu** goialdean **Harremanak** mahaia.</span><span class="sxs-lookup"><span data-stu-id="a7313-142">Select **Delete** at the top of the **Relationships** table.</span></span>

4. <span data-ttu-id="a7313-143">Berretsi ezabatu nahi duzula.</span><span class="sxs-lookup"><span data-stu-id="a7313-143">Confirm your deletion.</span></span>

## <a name="next-step"></a><span data-ttu-id="a7313-144">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="a7313-144">Next step</span></span>

<span data-ttu-id="a7313-145">Sistema eta pertsonalizatutako harremanak sekretuak isilik ez dituzten datu iturri anitzetan oinarritutako segmentuak sortzeko erabiltzen dira.</span><span class="sxs-lookup"><span data-stu-id="a7313-145">System and custom relationships are used to create segments based on multiple data sources that are no longer siloed.</span></span> <span data-ttu-id="a7313-146">Informazio gehiago lortzeko, [Segmentuak](segments.md).</span><span class="sxs-lookup"><span data-stu-id="a7313-146">For more information, see [Segments](segments.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]