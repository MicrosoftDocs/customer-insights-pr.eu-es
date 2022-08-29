---
title: Kudeatu inguruneak
description: Ikasi lehendik dauden Customer Insights inguruneak administratzaile gisa kudeatzen".
ms.date: 08/15/2022
ms.subservice: audience-insights
ms.topic: how-to
ms.reviewer: mhart
author: mukeshpo
ms.author: mukeshpo
manager: shellyha
searchScope:
- ci-system-about
- customerInsights
ms.openlocfilehash: 8b4a88bdb75c6e638a76c39d18647681ad4556d7
ms.sourcegitcommit: 267c317e10166146c9ac2c30560c479c9a005845
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/16/2022
ms.locfileid: "9304265"
---
# <a name="manage-environments"></a>Kudeatu inguruneak

Administratzaileak [sortu](create-environment.md) eta inguruneak kudeatu. Ezarpen batzuk alda ditzakete lehendik dauden inguruneetan. Negozioa, mota, eskualdea, biltegiratzeko aukera eta Dataverse ezarpenak ingurunea sortu ondoren finkatzen dira. Ezarpen hauek aldatu nahi badituzu, [ingurunea berrezarri](#reset-an-existing-environment-preview) edo [ingurune berri bat sortu](create-environment.md).

## <a name="edit-an-existing-environment"></a>Editatu lehendik dagoen ingurunea

Editatu lehendik dagoen ingurune baten xehetasunak, hala nola izena edo ingurune lehenetsia ezartzea.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu **Editatu** ikonoa.

   :::image type="content" source="media/edit-environment.png" alt-text="Ingurunearen ezarpenak editatzeko ikonoa.":::

1. urtean **Editatu ingurunea** panela, eguneratu ingurunearen ezarpenak.

1. Hautatu **Berrikusi eta amaitu**, orduan **Eguneratu** aldaketak aplikatzeko.

## <a name="change-the-owner-of-an-environment"></a>Ingurune baten jabea aldatu

Hainbat erabiltzailek administratzaile-baimenak izan ditzakete, baina erabiltzaile bakarra da ingurune baten jabea. Lehenespenez, administratzailea da hasiera batean ingurune bat sortzen duena. Ingurune baten administratzaile gisa, administratzaile-baimenak dituen beste erabiltzaile bati jabetza esleitu diezaiokezu.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu **Editatu** ikonoa.

1. urtean **Editatu ingurunea** panela, joan **Oinarrizko informazioa** urratsa.

1. urtean **Ingurunearen jabea aldatu** eremuan, aukeratu ingurunearen jabe berria.  

1. Hautatu **Berrikusi eta amaitu**, orduan **Eguneratu** aldaketak aplikatzeko.

## <a name="claim-ownership-of-an-environment"></a>Ingurune baten jabetza aldarrikatu

Jabearen erabiltzaile-kontua ezabatzen edo eteten bada, inguruneak ez du jaberik izango. Edozein administratzaile erabiltzailek jabetza erreklamatu eta jabe berria bihurtu daiteke. Jabearen administratzaileak ingurunearen jabe izaten jarrai dezake edo [aldatu jabetza beste administratzaile bati](#change-the-owner-of-an-environment).

Jabetza erreklamatzeko, hautatu **Jabetu** Customer Insights-en orrialde bakoitzaren goialdean agertzen den botoia, jatorrizko jabeak erakundea utzi zuenean.

## <a name="reset-an-existing-environment-preview"></a>Lehendik dagoen ingurune bat berrezarri (aurrebista)

Ingurune baten jabe gisa, berrezarri ingurune bat hutsik dagoen egoerara, konfigurazio guztiak ezabatu eta irensten diren datuak kendu nahi badituzu.

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu berrezarri nahi duzun ingurunea eta hautatu elipsi bertikala (&vellip;).

1. Aukeratu **Berrezarri (aurrebista)**.

   :::image type="content" source="media/reset-environment.png" alt-text="Kontrola ingurune bat berrezartzeko.":::

1. Aukeratu ingurune osoa, datu-iturburuak izan ezik, edo bezeroaren profil bateratuaren gainean konfiguratuta dagoen guztia berrezarri nahi duzun.

1. Berresteko, sartu ingurunearen izena eta hautatu **Berrezarri**.

## <a name="delete-an-existing-environment"></a>Aurretik bazegoen ingurune bat ezabatu

Ingurune baten jabe gisa, ezaba dezakezu.

> [!IMPORTANT]
> Ingurune bat ezabatzeak ez du konexiorik kentzen a Dataverse ingurunea. Berdin konektatzeko asmoa baduzu Dataverse etorkizunean Customer Insights ingurune berri batera, behar duzu [kendu konexio hori Dataverse ingurunea](customer-insights-dataverse.md#remove-an-existing-connection-to-a-dataverse-environment).

1. Hautatu **Ingurunea** hautatzailea aplikazioaren goiburuan.

1. Hautatu ezabatu nahi duzun ingurunea eta hautatu elipsi bertikala (&vellip;). 

1. Aukeratu **Ezabatu**.

   :::image type="content" source="media/delete-environment.png" alt-text="Kontrola ingurunea ezabatzeko.":::

1. Ezabatzea berresteko, idatzi ingurumenaren izena eta hautatu **Ezabatu**.

[!INCLUDE [footer-include](includes/footer-banner.md)]
