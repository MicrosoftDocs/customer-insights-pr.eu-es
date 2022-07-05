---
title: 'Nola: Inguruneak kudeatu'
description: Ikasi lehendik dauden Customer Insights inguruneak administratzaile gisa kudeatzen."
ms.date: 05/31/2022
ms.subservice: audience-insights
ms.topic: how-to
ms.reviewer: mhart
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-system-about
- customerInsights
ms.openlocfilehash: fc3b3f404cf0ac84c782778414494289c803babe
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9083051"
---
# <a name="how-to-manage-environments"></a>Nola: Inguruneak kudeatu

Administratzaileak [sortu](create-environment.md) eta inguruneak kudeatu. Ezarpen batzuk alda ditzakete lehendik dauden inguruneetan. Negozioa, mota, eskualdea, biltegiratzeko aukera eta Dataverse ezarpenak ingurunea sortu ondoren konpontzen dira. Ezarpen hauek aldatu nahi badituzu, berrezarri ingurunea edo sortu ingurune berri bat.

## <a name="edit-an-existing-environment"></a>Editatu lehendik dagoen ingurunea

Dauden inguruneen xehetasun batzuk editatu ditzakezu.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu **Editatu** ikonoa.

   :::image type="content" source="media/edit-environment.png" alt-text="Ingurunearen ezarpenak editatzeko ikonoa.":::

1. Urtean **Editatu ingurunea** koadroan, ingurunearen ezarpenak egunera ditzakezu.

Ingurune fresko batekin hasteko, ikus [Sortu ingurune berri bat](create-environment.md).

## <a name="change-the-owner-of-an-environment"></a>Ingurune baten jabea aldatu

Hainbat erabiltzailek administratzaile-baimenak izan ditzakete, baina erabiltzaile bakarra da ingurune baten jabea. Lehenespenez, administratzailea da hasieran ingurune bat sortzen duena. Ingurune baten administratzaile gisa, administratzaile baimenak dituen beste erabiltzaile bati jabetza esleitu diezaiokezu.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu **Editatu** ikonoa.

1. urtean **Editatu ingurunea** kutxa, joan **Oinarrizko informazioa** urratsa.

1. urtean **Ingurunearen jabea aldatu** eremuan, aukeratu ingurunearen jabe berria.  

1. Hautatu **Berrikusi eta amaitu**, orduan **Eguneratu** aldaketak aplikatzeko.

## <a name="claim-ownership-of-an-environment"></a>Ingurune baten jabetza aldarrikatu

Jabearen erabiltzaile-kontua ezabatzen edo eteten bada, inguruneak ez du jaberik izango. Erabiltzaile administratzaile bakoitzak jabetza erreklamatu eta jabe berria bihurtu daiteke. Inguruaren jabe izaten jarraitu dezakete edo [aldatu jabetza beste administratzaile bati](#change-the-owner-of-an-environment).

Jabetza erreklamatzeko, hautatu **Jabetu** Customer Insights-en orrialde bakoitzaren goialdean agertzen den botoia, jatorrizko jabeak erakundea utzi zuenean.

## <a name="reset-an-existing-environment-preview"></a>Lehendik dagoen ingurune bat berrezarri (Aurrebista)

Ingurune baten jabe gisa, ingurune bat egoera huts batera berrezarri dezakezu konfigurazio guztiak ezabatu eta irentsitako datuak kendu nahi badituzu.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu berrezarri nahi duzun ingurunea eta hautatu elipsi bertikala (&vellip;).

1. Aukeratu **Berrezarri** aukera.

   :::image type="content" source="media/reset-environment.png" alt-text="Kontrola ingurune bat berrezartzeko.":::

1. Aukeratu ingurune osoa, datu-iturriak izan ezik, edo bezeroen profil bateratuaren gainean konfiguratuta dagoen guztia berrezarri nahi duzun.

1. Berresteko, sartu ingurunearen izena eta hautatu **Berrezarri**.

## <a name="delete-an-existing-environment"></a>Aurretik bazegoen ingurune bat ezabatu

Ingurune baten jabe gisa, zuk kudeatzen duzun ingurune bat ezaba dezakezu.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu berrezarri nahi duzun ingurunea eta hautatu elipsi bertikala (&vellip;). 

1. Aukeratu **Ezabatu** aukera.

   :::image type="content" source="media/delete-environment.png" alt-text="Kontrola ingurunea ezabatzeko.":::

1. Ezabatzea berresteko, idatzi ingurumenaren izena eta hautatu **Ezabatu**.

> [!IMPORTANT]
> Ingurune bat ezabatzeak ez du konexioa kentzen a Dataverse ingurunea. Berdin konektatzeko asmoa baduzu Dataverse etorkizunean Customer Insights ingurune berri batera, konexio hori kendu behar duzu Ikasi nola egin [kendu lehendik dagoen konexio bat a Dataverse ingurunea](customer-insights-dataverse.md#remove-an-existing-connection-to-a-dataverse-environment).

[!INCLUDE [footer-include](includes/footer-banner.md)]
