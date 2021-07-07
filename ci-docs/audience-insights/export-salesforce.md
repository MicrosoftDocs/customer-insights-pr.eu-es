---
title: Esportatu Customer Insights datuak Salesforce Marketing Cloudera
description: Ikasi konexioa nola konfiguratu eta Salesforce Marketing Cloud-era esportatu.
ms.date: 06/24/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: pkieffer
ms.author: philk
manager: shellyha
ms.openlocfilehash: 123f8b2dbb6140785dec6c1b4164d2f513f66a53
ms.sourcegitcommit: 057079532e31c12bac36f374857ba3dc847d6ad0
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314570"
---
# <a name="export-segments-and-other-data-to-salesforce-marketing-cloud-preview"></a>Esportatu segmentuak eta bestelako datuak Salesforce Marketing Cloud-era (aurrebista)

Erabili zure bezeroen datuak Salesforce Marketing Cloud-en esportatuz fitxategi transferentzia protokolo seguruaren (SFTP) kokapen baten bidez.

## <a name="prerequisites-for-connection"></a>Konexioaren aurrebaldintzak

- SFTP ostalariaren eta dagozkien administratzaile kredentzialen erabilgarritasuna. [Nola konfiguratu SFTP kokapenak Salesforce Marketing Cloud-erako](https://help.salesforce.com/articleView?id=sf.mc_es_configure_enhanced_ftp.htm&type=5) 

## <a name="known-limitations"></a>Muga ezagunak

- Esportazio baten iraupena zure sistemaren errendimenduaren araberakoa da. Bi PUZ nukleo eta 1 Gb memoria gomendatzen dizugu zure zerbitzariaren gutxieneko konfigurazio gisa. 
- Gehienez 100 milioi bezero profil dituzten entitate esportatzaileek 90 minutu iraun dezakete gomendatutako gutxieneko konfigurazioa erabiltzean. 

## <a name="set-up-the-connection-to-salesforce-marketing-cloud"></a>Konfiguratu konexioa Salesforce Marketing Cloud-era

1. Joan **Administratzailea** > **Konexioak**.

1. Aukeratu **Gehitu konexioa** eta aukeratu **Salesforce Marketing Cloud** konexioa konfiguratzeko.

1. Eman zure konexioa ezaguna den izena **Bistaratze izena** eremua. Izena eta konexio motak konexio bat deskribatzen du. Konexio honen xedea eta xedea azaltzen duen izena aukeratzea gomendatzen dugu.

1. Aukeratu nork erabil dezakeen konexioa. Inolako neurririk hartzen ez baduzu, lehenetsia izango da Administratzaileak. Informazio gehiagorako, ikus [Baimendu laguntzaileei esportazioetarako konexioa erabiltzea](connections.md#allow-contributors-to-use-a-connection-for-exports).

1. Eman SFTP kontuaren **Erabiltzaile-izena**, **Pasahitza**, **Ostalari-izena** eta **Esportazio-karpeta**.

1. Hautatu **Egiaztatu** konexioa probatzeko.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Hautatu **Gorde** konexioa osatzeko.

## <a name="configure-an-export"></a>Konfiguratu esportazio bat

Esportazio hau konfigura dezakezu mota honetako konexiorako sarbidea baduzu. Informazio gehiagorako, ikusi [Esportazioa konfiguratzeko beharrezkoak diren baimenak](export-destinations.md#set-up-a-new-export).

1. Joan **Datuak** > **Esportazioak**.

1. Esportazio berria sortzeko, hautatu **Gehitu helmuga**.

1. Hurrengoan **Konexioa esportatzeko** eremuan, aukeratu konexioa SFTP sekzioan. Atal honen izena ikusten ez baduzu, ez dago mota honetako konexiorik erabilgarri.

1. Aukeratu zure datuak esportatu nahi dituzun **Gzipped** edo **Konprimatu gabe** eta **eremu mugatzailea** esportatutako fitxategietarako.

1. Aukeratu entitateak, adibidez, esportatu nahi dituzun segmentuak.

   > [!NOTE]
   > Aukeratutako entitate bakoitza bost irteerako fitxategitan banatuko da esportatzerakoan. 

1. Sakatu **Gorde**.

Esportazio bat gordetzeak ez du esportazioa berehala exekutatzen.

Esportazioa guztiekin egiten da [freskatze programatua](system.md#schedule-tab). Ere egin dezakezu [esportatu eskariaren arabera](export-destinations.md#run-exports-on-demand). 

## <a name="import-customer-insights-data-from-sftp-location-to-salesforce-marketing-cloud"></a>Inportatu Customer Insights datuak SFTP kokalekutik Salesforce Marketing Cloud-era

1. Sortu [datuen luzapenak Salesforce Marketing Cloud-en](https://help.salesforce.com/articleView?id=sf.mc_es_create_data_extension.htm&type=5) Customer Insights datu fitxategia SFTP kokapenetik inportatzeko.

2. [Inportatu datuak SFTP kokapenetik](https://help.salesforce.com/articleView?id=sf.mc_es_import_data_extension_classic.htm&type=5) Salesforce Marketing Cloud datuen luzapenean sartu. 

3. Konfiguratu automatizazioa datuak datu luzapenetara inportatzeko. Lortu informazio gehiago [fitxategien jaitsiera automatizazioak eta programatutako automatizazioak](https://help.salesforce.com/articleView?id=sf.mc_as_triggered_automations.htm&type=5).

   Definitu [fitxategien jaitsiera automatizazioa](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_triggered_automation.htm&type=5) edo bat [programatutako automatizazioa](https://help.salesforce.com/articleView?id=sf.mc_as_define_a_scheduled_automation.htm&type=5). 

Hona hemen adibide bat [automatizazio bat SFTPrekin](https://help.salesforce.com/articleView?id=sf.mc_as_ftp_and_triggered_automation_scenario.htm&type=5).

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
