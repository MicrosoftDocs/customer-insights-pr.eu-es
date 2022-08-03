---
title: Esportatu datuak Salesforce Marketing Cloud-era (aurrebista)
description: Ikasi konexioa nola konfiguratu eta Salesforce Marketing Cloud-era esportatu.
ms.date: 07/25/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 58e76e51c18c25177f9b4551b70b25b41248b142
ms.sourcegitcommit: 594081c82ca385f7143b3416378533aaf2d6d0d3
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 07/27/2022
ms.locfileid: "9197023"
---
# <a name="export-data-to-salesforce-marketing-cloud-preview"></a>Esportatu datuak Salesforce Marketing Cloud-era (aurrebista)

Erabili zure bezeroen datuak Salesforce Marketing Cloud-en esportatuz fitxategi transferentzia protokolo seguruaren (SFTP) kokapen baten bidez.

## <a name="prerequisites"></a>Aurrebaldintzak

- An [Salesforce Marketing Cloud-erako SFTP ostalaria](https://help.salesforce.com/articleView?id=sf.mc_es_configure_enhanced_ftp.htm&type=5) eta dagozkion administratzaile-kreditazioak.

## <a name="set-up-connection-to-salesforce-marketing-cloud"></a>Konfiguratu konexioa Salesforce Marketing Cloud-era

[!INCLUDE [export-connection-include](includes/export-connection-admn.md)]

1. Joan **Administratzailea** > **Konexioak**.

1. Hautatu **Gehitu konexioa** eta aukeratu **Salesforce Marketing Cloud**.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Berez, administratzaileak soilik dira. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman SFTP kontuaren **Erabiltzaile-izena**, **Pasahitza**, **Ostalari-izena** eta **Esportazio-karpeta**.

1. Hautatu **Egiaztatu** konexioa probatzeko.

1. Berrikusi [datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

[!INCLUDE [export-permission-include](includes/export-permission.md)]

1. Joan **Datuak** > **Esportazioak**.

1. Hautatu **Gehitu esportazioa**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SFTP sekzioan. Jarri harremanetan administratzaile batekin konexiorik ez badago.

1. Idatzi esportaziorako izen bat.

1. Aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimatu gabe** eta **eremu mugatzailea** esportatutako fitxategietarako.

1. Hautatu esportatu nahi dituzun entitateak, segmentuak adibidez.

   > [!NOTE]
   > Hautatutako entitate bakoitza gehienez bost irteera fitxategitan banatuko da esportatzen denean.

1. Sakatu **Gorde**.

[!INCLUDE [export-saving-include](includes/export-saving.md)]

## <a name="import-customer-insights-data-from-sftp-location-to-salesforce-marketing-cloud"></a>Inportatu Customer Insights datuak SFTP kokalekutik Salesforce Marketing Cloud-era

1. Sortu [datuen luzapenak Salesforce Marketing Cloud-en](https://help.salesforce.com/articleView?id=sf.mc_es_create_data_extension.htm&type=5) Customer Insights datu fitxategia SFTP kokapenetik inportatzeko.

2. [Inportatu datuak SFTP kokapenetik](https://help.salesforce.com/articleView?id=sf.mc_es_import_data_extension_classic.htm&type=5) Salesforce Marketing Cloud datuen luzapenean sartu.

3. Konfiguratu automatizazioa datuak datu luzapenetara inportatzeko. Lortu informazio gehiago [fitxategien jaitsiera automatizazioak eta programatutako automatizazioak](https://help.salesforce.com/articleView?id=sf.mc_as_triggered_automations.htm&type=5).

   Definitu [fitxategien jaitsiera automatizazioa](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_triggered_automation.htm&type=5) edo bat [programatutako automatizazioa](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_scheduled_automation.htm&type=5).

Hona hemen adibide bat [automatizazio bat SFTPrekin](https://help.salesforce.com/articleView?id=sf.mc_as_ftp_and_triggered_automation_scenario.htm&type=5).

[!INCLUDE [footer-include](includes/footer-banner.md)]
