---
title: Esportatu Customer Insights datuak SFTP ostalarietara
description: Ikusi nola konfiguratu konexioa SFTP ostalaria.
ms.date: 06/05/2020
ms.reviewer: philk
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: c2529744d7a26a06324b79cad6a8001d75903545
ms.sourcegitcommit: 6a6df62fa12dcb9bd5f5a39cc3ee0e2b3988184b
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643488"
---
# <a name="connector-for-sftp-preview"></a>Konektorea SFTP-rako (aurrebista)

Erabili hirugarrenen aplikazioetako bezero-datuak horiek fitxategiak modu seguruan transferitzeko protokoloaren (SFTP) ostalarira transferituz.

## <a name="prerequisites"></a>Aurrebaldintzak

- SFTP ostalari baten eta dagozkien egiaztagirien eskuragarritasuna.

## <a name="connect-to-sftp"></a>Konektatu SFTP-ra

1. Joan **Administratzailea** > **Esportazio-helburuak** atalera.

1. Azpian **SFTP** hautatu **Konfiguratu**.

1. Eman zure destinoari izen ezagun bat **Bistaratu izena** eremu.

1. Eman SFTP kontuaren **Erabiltzaile izena**, **Pasahitza** eta **Ostalari izena**. Adibidez: zure SFTP zerbitzariaren erroko karpeta /root/folder bada eta datuak /root/folder/ci_export_destination_folder karpetara esportatzea nahi baduzu, ostalariak honakoa izan beharko luke: sftp://<server_address>/ci_export_destination_folder".

1. Hautatu **Egiaztatu** konexioa probatzeko.

1. Egiaztatu ondoren, aukeratu zure datuak esportatu nahi dituzun **konprimitutako** edo **konprimitu gabea** eta hautatu **eremuaren mugatzailea** esportatutako fitxategietarako.

1. Aukeratu **ados** baieztatzeko **Datuen pribatutasuna eta betetzea**.

1. Aukeratu **hurrengoa** esportazioa konfiguratzen hasteko.

## <a name="configure-the-connection"></a>Konfiguratu konexioa

1. Hautatu **bezeroaren atributuak** esportatu nahi dituzunak. Ezaugarri bat edo gehiago esporta ditzakezu.

1. Hautatu **Hurrengoa**.

1. Hautatu esportatu nahi dituzun segmentuak.

1. Sakatu **Gorde**.

## <a name="export-the-data"></a>Esportatu datuak

Hurrengoa egin dezakezu [esportatu datuak eskatu ahala](export-destinations.md). Esportazioa guztiekin ere exekutatuko da [programatutako freskapen](system.md#schedule-tab).

## <a name="data-privacy-and-compliance"></a>Datuen pribatutasuna eta arau-gordetzea

Dynamics 365 Customer Insights gaitzen duzunean datuak SFTP bidez bidaltzeko, datuak betetzeko mugatik kanpo transferitzea baimentzen duzu Dynamics 365 Customer Insights-erako, datu pertsonalak bezalako datu sentikorrak barne. Microsoft-ek datu horiek transferituko ditu zure aginduz, baina zure ardura da esportatzeko helmugak pribatutasun- edo segurtasun-betebeharrak betetzen dituela ziurtatzea. Informazio gehiago eskuratzeko, ikusi [Microsoft-en pribatutasun-adierazpena](https://go.microsoft.com/fwlink/?linkid=396732).
Funtzio hau erabiltzeari uzteko, Dynamics 365 Customer Insights-en administratzaileak esportazioaren helburuko kokalekua edonoiz ken dezake.
