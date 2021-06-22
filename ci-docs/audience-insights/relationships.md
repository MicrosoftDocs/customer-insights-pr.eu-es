---
title: Entitateen eta entitateen bide-izenen arteko erlazioak
description: Sortu eta kudeatu datu-iturburu anitzetako entitateen arteko harremanak.
ms.date: 06/01/2020
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: MichelleDevaney
ms.author: midevane
manager: shellyha
ms.openlocfilehash: d5b9566ec88096fec31d8e164a51598159ec26d4
ms.sourcegitcommit: ece48f80a7b470fb33cd36e3096b4f1e9190433a
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/03/2021
ms.locfileid: "6171149"
---
# <a name="relationships-between-entities"></a><span data-ttu-id="c4a4d-103">Harremanak entitateen artean</span><span class="sxs-lookup"><span data-stu-id="c4a4d-103">Relationships between entities</span></span>

<span data-ttu-id="c4a4d-104">Harremanek entitateak konektatzen dituzte eta zure datuen grafikoa definitzen dute entitateek identifikatzaile komuna partekatzen dutenean, atzerriko gakoa.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-104">Relationships connect entities and define a graph of your data when entities share a common identifier, a foreign key.</span></span> <span data-ttu-id="c4a4d-105">Atzerriko gako honi entitate batetik bestera erreferentzia egin dakioke.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-105">This foreign key can be referenced from one entity to another.</span></span> <span data-ttu-id="c4a4d-106">Konektatutako entitateek datu-iturri anitzetan oinarritutako segmentuak eta neurriak definitzeko aukera ematen dute.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-106">Connected entities enable the definition of segments and measures based on multiple data sources.</span></span>

<span data-ttu-id="c4a4d-107">Hiru harreman mota daude:</span><span class="sxs-lookup"><span data-stu-id="c4a4d-107">There are three types of relationships:</span></span> 
- <span data-ttu-id="c4a4d-108">Editatu ezin diren sistema harremanak, sistemak datuak bateratzeko prozesuaren zati gisa sortuak</span><span class="sxs-lookup"><span data-stu-id="c4a4d-108">Non-editable system relationships, created by the system as part of the data unification process</span></span>
- <span data-ttu-id="c4a4d-109">Editatu ezin diren herentziazko harremanak, datu iturriak sartzetik automatikoki sortzen direnak</span><span class="sxs-lookup"><span data-stu-id="c4a4d-109">Non-editable inherited relationships, which are created automatically from ingesting data sources</span></span> 
- <span data-ttu-id="c4a4d-110">Erabiltzaileek sortutako eta konfiguratutako harreman pertsonalizatu editagarriak</span><span class="sxs-lookup"><span data-stu-id="c4a4d-110">Editable custom relationships, created and configured by users</span></span>

## <a name="non-editable-system-relationships"></a><span data-ttu-id="c4a4d-111">Editatu ezin diren sistemen harremanak</span><span class="sxs-lookup"><span data-stu-id="c4a4d-111">Non-editable system relationships</span></span>

<span data-ttu-id="c4a4d-112">Datuak bateratzerakoan, sistemako harremanak automatikoki sortzen dira bat-etortze adimentsuan oinarrituta.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-112">During data unification, system relationships are created automatically based on intelligent matching.</span></span> <span data-ttu-id="c4a4d-113">Harreman hauek Bezeroaren Profilaren erregistroak dagozkien beste erregistroekin erlazionatzen lagunduko dute.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-113">These relationships help relate the customer profile records with corresponding records.</span></span> <span data-ttu-id="c4a4d-114">Hurrengo diagramak sisteman oinarritutako hiru erlazio sortu direla erakusten du.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-114">The following diagram illustrates the creation of three system-based relationships.</span></span> <span data-ttu-id="c4a4d-115">Bezeroaren entitatea beste entitate batzuekin bateratzen da *Bezeroaren* entitate bateratua ekoizteko.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-115">The customer entity is matched with other entities to produce the unified *Customer* entity.</span></span>

:::image type="content" source="media/relationships-entities-merge.png" alt-text="1-n hiru harreman dituen bezero entitatearen harreman bideekin diagrama.":::

- <span data-ttu-id="c4a4d-117">***CustomerToContact* harremana** *Bezeroaren* entitatearen eta *kontaktuaren* entitatearen artean sortu zen.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-117">***CustomerToContact* relationship** was created between the *Customer* entity and the *Contact* entity.</span></span> <span data-ttu-id="c4a4d-118">*Bezero* entitateak **Contact_contactID** gako-eremua lortzen du *kontaktuaren* entitatearen **contactID** gako eremuarekin erlazionatzeko.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-118">The *Customer* entity gets the key field **Contact_contactID** to relate to the *Contact* entity key field **contactID**.</span></span>
- <span data-ttu-id="c4a4d-119">***CustomerToAccount* harremana** *bezeroaren* entitatearen eta *kontuaren* entitatearen artean sortu zen.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-119">***CustomerToAccount* relationship** was created between the *Customer* entity and the *Account* entity.</span></span> <span data-ttu-id="c4a4d-120">*Bezeroaren* entitateak **Account_accountID** gako eremua lortzen du *kontua* entitatearen **accountID** gako eremuarekin erlazionatzeko.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-120">The *Customer* entity gets the key field **Account_accountID** to relate to the *Account* entity key field **accountID**.</span></span>
- <span data-ttu-id="c4a4d-121">***CustomerToWebAccount* harremana** *bezeroaren* entitatearen eta *WebAccount* entitatearen artean sortu zen.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-121">***CustomerToWebAccount* relationship** was created between the *Customer* entity and the *WebAccount* entity.</span></span> <span data-ttu-id="c4a4d-122">*Bezeroaren* entitateak **WebAccount_webaccountID** gako eremua lortzen du *WebAccount* entitatearen **webaccountID** gako eremuarekin erlazionatzeko.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-122">The *Customer* entity gets the key field **WebAccount_webaccountID** to relate to the *WebAccount* entity key field **webaccountID**.</span></span>

## <a name="non-editable-inherited-relationships"></a><span data-ttu-id="c4a4d-123">Editatu ezin diren heredatutako harremanak</span><span class="sxs-lookup"><span data-stu-id="c4a4d-123">Non-editable inherited relationships</span></span>

<span data-ttu-id="c4a4d-124">Datuak irensteko prozesuan, sistemak datu iturriak egiaztatzen ditu lehendik dauden harremanetarako.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-124">During the data ingestion process, the system checks data sources for existing relationships.</span></span> <span data-ttu-id="c4a4d-125">Harremanik ez badago, sistemak automatikoki sortzen ditu.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-125">If no relationship exists, the system automatically creates them.</span></span> <span data-ttu-id="c4a4d-126">Harreman horiek beheranzko prozesuetan ere erabiltzen dira.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-126">These relationships are also used in downstream processes.</span></span>

## <a name="create-a-custom-relationship"></a><span data-ttu-id="c4a4d-127">Sortu erlazio pertsonalizatu bat</span><span class="sxs-lookup"><span data-stu-id="c4a4d-127">Create a custom relationship</span></span>

<span data-ttu-id="c4a4d-128">Harremanak atzerriko gakoa duen *iturburu-entitatea* eta iturburuko entitatearen atzerriko gakoak adierazten duen *xede-entitatea* ditu.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-128">Relationship consists of a *source entity* containing the foreign key and a *target entity* that the source entity's foreign key points to.</span></span> 

1. <span data-ttu-id="c4a4d-129">Hartzaileei buruzko xehetasunetan, joan hona: **Datuak** > **Harremanak**.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-129">In audience insights, go to **Data** > **Relationships**.</span></span>

2. <span data-ttu-id="c4a4d-130">Hautatu **Harreman berria**.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-130">Select **New relationship**.</span></span>

3. <span data-ttu-id="c4a4d-131">**Erlazio berria** panelean, eman ondorengo informazioa:</span><span class="sxs-lookup"><span data-stu-id="c4a4d-131">In the **New relationship** pane, provide the following information:</span></span>

   :::image type="content" source="media/relationship-add.png" alt-text="Harreman alboko panel berria sarrera eremu hutsekin.":::

   - <span data-ttu-id="c4a4d-133">**Harremanaren izena**: Harremanaren xedea islatzen duen izena.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-133">**Relationship name**: Name that reflects the purpose of the relationship.</span></span> <span data-ttu-id="c4a4d-134">Adibidez: CustomerToSupportCase.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-134">Example: CustomerToSupportCase.</span></span>
   - <span data-ttu-id="c4a4d-135">**Deskribapena**: Erlazio-funtzioaren azalpena.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-135">**Description**: Description of the relationship.</span></span>
   - <span data-ttu-id="c4a4d-136">**Iturburuko entitatea**: Harremanean iturburu gisa erabiltzen den entitatea.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-136">**Source entity**: Entity that is used as a source in the relationship.</span></span> <span data-ttu-id="c4a4d-137">Adibidez: SupportCase.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-137">Example: SupportCase.</span></span>
   - <span data-ttu-id="c4a4d-138">**Helburuko entitatea**: Harremanean helburu gisa erabiltzen den entitatea.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-138">**Target entity**: Entity that is used as a target in the relationship.</span></span> <span data-ttu-id="c4a4d-139">Adibidez: Customer.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-139">Example: Customer.</span></span>
   - <span data-ttu-id="c4a4d-140">**Iturriaren kardinalitatea** : Zehaztu iturburuko entitatearen kardinalitatea.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-140">**Source cardinality**: Specify the cardinality of the source entity.</span></span> <span data-ttu-id="c4a4d-141">Kardinalitateak multzo bateko elementu posibleen kopurua deskribatzen du.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-141">Cardinality describes the number of possible elements in a set.</span></span> <span data-ttu-id="c4a4d-142">Beti xede-kardinalitatearekin lotzen da.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-142">It always relates to the target cardinality.</span></span> <span data-ttu-id="c4a4d-143">Aukera dezakezu **Bat** edo **Asko**.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-143">You can choose between **One** and **Many**.</span></span> <span data-ttu-id="c4a4d-144">Banan-banan eta banan-banako harremanak bakarrik onartzen dira.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-144">Only many-to-one and one-to-one relationships are supported.</span></span>  
     - <span data-ttu-id="c4a4d-145">Hainbatetik baterako: iturburu erregistro anitz xede erregistro batekin erlazionatu daitezke.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-145">Many-to-one: Multiple source records can relate to one target record.</span></span> <span data-ttu-id="c4a4d-146">Adibidez: bezero bakar baten laguntza kasu ugari.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-146">Example: Multiple support cases from a single customer.</span></span>
     - <span data-ttu-id="c4a4d-147">Batetik baterako: iturburuko erregistro bakarra xede erregistro batekin erlazionatzen da.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-147">One-to-one: A single source record relates to a one target record.</span></span> <span data-ttu-id="c4a4d-148">Adibidez: fidelizazio ID bakarra bezero bakarrarentzat.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-148">Example: One loyalty ID for a single customer.</span></span>

     > [!NOTE]
     > <span data-ttu-id="c4a4d-149">Hainbatetik hainbaterako harremanak hainbatetik baterako bi harreman eta lotura duen entitate bat erabiliz sor daitezke, sorburuko entitatea eta xede-entitatea lotzen dituena.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-149">Many-to-many relationships can be created using two many-to-one relationships and a linking entity, which connects the source entity and the target entity.</span></span>

   - <span data-ttu-id="c4a4d-150">**Helmugako kardinalitatea**: helmugako entitatearen erregistroen kardinalitatea aukeratu.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-150">**Target cardinality**: Select the cardinality of the target entity records.</span></span> 
   - <span data-ttu-id="c4a4d-151">**Iturburu gako eremua** : Iturburuko entitateko atzerriko gako eremua.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-151">**Source key field**: The foreign key field in the source entity.</span></span> <span data-ttu-id="c4a4d-152">Adibidez: SupportCase-k CaseID erabil dezake atzerriko gako eremu gisa.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-152">Example: SupportCase could use CaseID as a foreign key field.</span></span>
   - <span data-ttu-id="c4a4d-153">**Helburuko gako eremua**: xede entitatearen gako eremua.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-153">**Target key field**: The key field of the target entity.</span></span> <span data-ttu-id="c4a4d-154">Adibidez bezeroak erabil dezake **Bezeroaren IDa** gako eremua.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-154">Example Customer could use the **CustomerID** key field.</span></span>

4. <span data-ttu-id="c4a4d-155">Erlazio pertsonalizatua sortzeko, hautatu **Gorde**.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-155">Select **Save** to create the custom relationship.</span></span>

## <a name="view-relationships"></a><span data-ttu-id="c4a4d-156">Ikusi erlazioak</span><span class="sxs-lookup"><span data-stu-id="c4a4d-156">View relationships</span></span>

<span data-ttu-id="c4a4d-157">Harremanak orrian sortu diren harreman guztiak zerrendatzen dira.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-157">The Relationships page lists all the relationships that have been created.</span></span> <span data-ttu-id="c4a4d-158">Errenkada bakoitzak erlazio bat adierazten du, iturburu-entitateari, xede-entitateari eta kardinalitateari buruzko xehetasunak ere biltzen dituena.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-158">Each row represents a relationship, which also includes details about the source entity, the target entity, and the cardinality.</span></span> 

:::image type="content" source="media/relationships-list.png" alt-text="Harremanen eta aukeren zerrenda Harremanak orriko ekintza barran.":::

<span data-ttu-id="c4a4d-160">Orrialde honek lehendik dauden eta harreman berrietarako aukera multzo bat eskaintzen du:</span><span class="sxs-lookup"><span data-stu-id="c4a4d-160">This page offers a set of options for existing and new relationships:</span></span> 
- <span data-ttu-id="c4a4d-161">**Erlazio berria:** [Sortu erlazio pertsonalizatu bat](#create-a-custom-relationship).</span><span class="sxs-lookup"><span data-stu-id="c4a4d-161">**New Relationship**: [Create a custom relationship](#create-a-custom-relationship).</span></span>
- <span data-ttu-id="c4a4d-162">**Bistaratzailea**: [Arakatu harremanen bistaratzailea](#explore-the-relationship-visualizer) dauden erlazioen eta haien kardinalitatearen sare-diagrama ikusteko.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-162">**Visualizer**: [Explore the relationship visualizer](#explore-the-relationship-visualizer) to see a network diagram of the existing relationships and their cardinality.</span></span>
- <span data-ttu-id="c4a4d-163">**Iragazi honen arabera**: Aukeratu zerrendan erakutsi beharreko harreman mota.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-163">**Filter by**: Choose the type of relationships to show in the list.</span></span>
- <span data-ttu-id="c4a4d-164">**Bilatu harremanak**: Erabili testuan oinarritutako bilaketa erlazioen propietateetan.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-164">**Search relationships**: Use a text-based search on properties of the relationships.</span></span>

### <a name="explore-the-relationship-visualizer"></a><span data-ttu-id="c4a4d-165">Arakatu harremanen bistaratzailea</span><span class="sxs-lookup"><span data-stu-id="c4a4d-165">Explore the relationship visualizer</span></span>

<span data-ttu-id="c4a4d-166">Harremanen bistaratzaileak konektatuta dauden entitateeen eta haien kardinalitatearen sare-diagrama erakusten du.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-166">The relationship visualizer shows a network diagram of the existing relationships between connected entities and their cardinality.</span></span>

<span data-ttu-id="c4a4d-167">Ikuspegia pertsonalizatzeko, koadroen kokapena alda dezakezu mihisean arrastatuz.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-167">To customize the view, you can change the position of the boxes by dragging them on the canvas.</span></span>

:::image type="content" source="media/relationship-visualizer.png" alt-text="Erlazio bistaratzailearen sare diagramaren pantaila-argazkia erlazionatutako entitateen arteko konexioekin.":::

<span data-ttu-id="c4a4d-169">Aukera erabilgarriak:</span><span class="sxs-lookup"><span data-stu-id="c4a4d-169">Available options:</span></span> 
- <span data-ttu-id="c4a4d-170">**Esportatu irudi gisa**: Uneko ikuspegia irudi fitxategi gisa gorde.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-170">**Export as image**: Save the current view as an image file.</span></span>
- <span data-ttu-id="c4a4d-171">**Aldatu diseinu horizontal / bertikalera**: Entitateen eta harremanen lerrokatzea aldatu.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-171">**Change to horizontal/vertical layout**: Change the alignment of the entities and relationships.</span></span>
- <span data-ttu-id="c4a4d-172">**Editatu**: Harreman pertsonalizatuen propietateak eguneratu editatzeko panelean eta gorde aldaketak.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-172">**Edit**: Update properties of custom relationships in the edit pane and save changes.</span></span>

## <a name="manage-existing-relationships"></a><span data-ttu-id="c4a4d-173">Kudeatu lehendik dauden erlazioak</span><span class="sxs-lookup"><span data-stu-id="c4a4d-173">Manage existing relationships</span></span> 

<span data-ttu-id="c4a4d-174">Harremanak orrian, harreman bakoitza errenkada batez irudikatzen da.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-174">On the Relationships page, each relationship is represented by a row.</span></span> 

<span data-ttu-id="c4a4d-175">Aukeratu harremana eta aukeratu aukera hauetako bat:</span><span class="sxs-lookup"><span data-stu-id="c4a4d-175">Select a relationship and choose one of the following options:</span></span> 
 
- <span data-ttu-id="c4a4d-176">**Editatu**: Harreman pertsonalizatuen propietateak eguneratu editatzeko panelean eta gorde aldaketak.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-176">**Edit**: Update properties of custom relationships in the edit pane and save changes.</span></span>
- <span data-ttu-id="c4a4d-177">**Ezabatu**: Harreman pertsonalizatuak ezabatu.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-177">**Delete**: Delete custom relationships.</span></span>
- <span data-ttu-id="c4a4d-178">**Ikusi**: Sistemak sortutako eta heredatutako harremanak ikusi.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-178">**View**: View system-created and inherited relationships.</span></span> 

## <a name="next-step"></a><span data-ttu-id="c4a4d-179">Hurrengo urratsa</span><span class="sxs-lookup"><span data-stu-id="c4a4d-179">Next step</span></span>

<span data-ttu-id="c4a4d-180">Sistema eta pertsonalizatutako harremanak sekretuak isilik ez dituzten datu iturri anitzetan oinarritutako [segmentuak sortzeko](segments.md) erabiltzen dira.</span><span class="sxs-lookup"><span data-stu-id="c4a4d-180">System and custom relationships are used to [create segments](segments.md) based on multiple data sources that are no longer siloed.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
