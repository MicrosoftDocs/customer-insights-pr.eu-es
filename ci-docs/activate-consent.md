---
title: Aktibatu adostasun-arauak segmentuetarako
description: Jarraitu urrats hauek baimenaren datuak lotzeko eta baimenaren egiaztapenak aktibatzeko Dynamics 365 Customer Insights. Administratzaile batek baimenaren egiaztapenak ere desgai ditzake.
ms.date: 04/27/2022
ms.topic: how-to
author: anubhav-t
ms.author: antando
ms.reviewer: mhart
manager: shellyha
ms.openlocfilehash: f82e3a4031fee8bcaa88575cbd68b37385a7fffb
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755155"
---
# <a name="activate-consent-rules"></a>Aktibatu adostasun-arauak

The [Adostasun Zentroa (aurrebista)](consent-management/overview.md) Hainbat iturritako adostasun-datuak harmonizatzen laguntzen dizu. Erabili bateratua *Adostasuna* entitateak baimenaren egiaztapen lehenetsiak aplikatzeko. Adostasun-datuak inportatu eta mapa-arauak konfiguratu ondoren, *Adostasuna* entitatea automatikoki sinkronizatzen da Dynamics 365 Customer Insights.

## <a name="enable-consent-checks"></a>Gaitu onarpen-egiaztapenak

Adostasun-datuak Adostasun Zentrora (aurrebista) inportatuta eta arauak konfiguratuta, baimen-egiaztapenak gaitu ditzakezu. 

:::image type="content" source="consent-management/media/enable-consent-checks.png" alt-text="Adostasun fitxa, Customer Insights ezarpenetan, aktibatuta dauden baimen-datuak.":::

1. Customer Insights atalean, joan **Admin** > **Sistema**.

1. Hautatu **Adostasuna (aurrebista)** fitxa.

1. urtean **Gaitu baimenaren egiaztapenak** atalean, ezarri etengailua **On** gaitu nahi dituzun eremu guztietarako.

1. Hautatu **Baimendu baimen-arau lehenetsiak gainidaztea** kontrol-laukia segmentu jakin batean ezarritako baimen-kontrol lehenetsiak kentzeko. 

1. Goitibeherako menuan, hautatu non baimendu nahi dituzun gainidatziak.     

1. urtean **Lotu baimena bezeroen profilekin** atalean, aukeratu adostasun-datuak bezero-datuekin lotzeko identifikatzaile gisa erabiltzen den atributua. Litekeena da telefono-zenbaki bat edo helbide elektroniko bat izango da. 

1. Hautatu **Gorde** zure ezarpenak aplikatzeko.

## <a name="disable-consent-checks"></a>Desgaitu baimenaren egiaztapenak

Customer Insights-en adostasun-datuak erabiltzeari uzteko, administratzaileak sistemaren ezarpenak eguneratu behar ditu.

1. Customer Insights atalean, joan **Admin** > **Sistema**.

1. Hautatu **Adostasuna (aurrebista)** fitxa.

1. urtean **Gaitu baimenaren egiaztapenak** atalean, ezarri etengailua **Desaktibatuta**.

> [!TIP]
> Adostasuna kudeatzeko gaitasuna erabiltzeari uzteko, ikus [Sistemaren ezarpenak Adostasun Zentroan (aurrebista)](consent-management/system-settings.md).
