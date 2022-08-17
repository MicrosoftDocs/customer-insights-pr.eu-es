---
title: Erabili bezeroaren baimena
description: Errespetatu bezeroen baimen-hobespenak Customer Insights-en, baimenaren datuak inportatuz.
ms.date: 06/07/2022
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 6c951219410b55adc34691f677158b574cea1e01
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9245680"
---
# <a name="use-customer-consent"></a>Erabili bezeroaren baimena

Datuak babesteko eta pribatutasuneko araudiek norbanakoek erakunde batek bere datu pertsonalak nola erabiltzen dituen arautzeko eskubidea ematen die. Arau horien adibide dira Europar Batasuneko Datuak Babesteko Erregelamendu Orokorra edo Estatu Batuetako Kaliforniako Kontsumitzaileen Pribatutasunaren Legea. Araudi honek aukera ematen die jendeak bere datu pertsonalak bildu, tratatu edo hirugarren batzuekin partekatzeari uko egitea.  

Bezeroek euren baimena kentzea edo uko egitea aukeratu dezakete harremanetarako forma zehatzetarako. Era berean, haien datu pertsonalak biltzea, biltegiratzea, erabiltzea edo saltzeari uko egitea eska dezakete. Garrantzitsua da zure erakundeak bezeroen baimena eta pribatutasun-hobespenak errespetatzea.  

Dynamics 365 Customer Insights Zure bezeroen eskaerak betetzen laguntzen dizu, haien hobespenak bezeroen profil bateratuen parte gisa inportatuz eta gordez.

Adostasun-datuak zure bezero-profiletatik bereizita gordetzen badira, [gehitu zure baimenaren datuak datu-iturburu berri gisa](#import-and-unify-consent-data). Adostasun-datuak biltzen dituen datu-iturburu datuak bateratzeko prozesura gehitzen da. Adostasun-datuen eta bezero-profilen bateratze arrakastatsuak gero, baimenaren informazioa duten bezero-profil bateratuetara eramaten du. Dagoeneko baimen-informazioa duten bezero-profiletarako, joan zuzenean helbidera [adostasun datuak erabiltzea](#use-consent-data) atala.

## <a name="prerequisites"></a>Aurrebaldintzak

Informazio hau erabilgarri egon behar da zure iturburu-datuetan adostasun-datuak beste bezero-profilekin bateratzeko:

- Ordezko gako adostasun-informazioa Customer Insights-en erabiltzaile-profilekin mapatzeko. Adibidez, helbide elektroniko bat edo telefono zenbaki bat.
- Adostasunaren balioa bezeroaren baimenaren egoera zehazteko.

Demagun hurrengoa gehitzea *aukerakoa* informazioa:

- Bezero batek aldaketa eskatzen badu baimenaren egoera eguneratzeko gako nagusia.
- Adostasun mota, bezeroen informazioa prozesatzeko modu bat baino gehiago badago.
- Baimenaren data edo zure baimenaren eszenatokietarako garrantzitsua den beste edozein datu mota.

Adostasun-aukera anitz dituen adostasun datu-base sinple baten adibidea:

|Baimenaren IDa (gako nagusia)   |Posta elektronikoa (ordezko gako)  |Adostasun aukera  |Adostasunaren balioa  |
|---------|---------|---------|---------|
|1    |  holly@contoso.com       |  Buletina       |  Gezurrezkoa       |
|2    |  holly@contoso.com       |  Produktuen eguneratzeak       |  Egiazkoa       |
|3    |  frank@contoso.com       |  Buletina       | Egiazkoa        |
|4    |  frank@contoso.com       |  Produktuen eguneratzeak       |  Gezurrezkoa       |

## <a name="import-and-unify-consent-data"></a>Inportatu eta bateratu baimenaren datuak

Inportatu baimenaren datuak Customer Insights-era beste datu-iturri batzuk sartzen dituzun moduan. Onartutako datu-iturburuei eta horiek inportatzeko moduari buruzko informazio gehiago lortzeko, ikus [Datu iturrien ikuspegi orokorra](data-sources.md).

Datu-iturriak bateratzeari buruzko informazio gehiago lortzeko, ikus [Datuen bateratzearen ikuspegi orokorra](data-unification.md).

## <a name="use-consent-data"></a>Erabili baimenaren datuak

Zure baimenaren datuak zure bezeroen profil bateratuen parte direnean, Customer Insights-en erabil ditzakezu. Adibidez, sortu segmentu bat arau batekin, zure bezeroen pribatutasuna eta datuen babesaren hobespenak betetzen dituzula ziurtatzeko. Baimenaren hobespenak onartzen dituzten arauak erabiltzen dira erabiltzaileak profilaren atributuetan oinarritutako segmentu batetik baztertzeko. Gehitu arau bat harremanetan jartzeko baimenik eman ez duten bezero-profilak baztertzen dituen segmentu batean.

Goiko lagin-taulari erreferentzia eginez, segmentu batek arau hau eduki dezake:`Consent option=Newsletter & Consent value=True`. Konfigurazio honek buletina bidaltzeko kontaktuen hobespenak errespetatzen dituen segmentu bat sortzen du.

Eraikuntza-segmentuei buruzko informazio gehiago lortzeko, ikus [Sortu segmentuak](segment-builder.md).

Segmentua sortu ondoren, askotariko bat erabil dezakezu [esportatzeko aukerak](export-destinations.md) segmentua beste aplikazio batzuetan erabiltzeko.

## <a name="ensure-updated-consent-status"></a>Ziurtatu baimenaren egoera eguneratua

Garrantzitsua da zure bezeroen baimenaren egoera eguneratuta mantentzea. Customer Insights-en programatutako freskatzeak beti inportatzen du zure datu-iturrien azken egoera. Ondoren, informazio hori datuak bateratzearen bidez prozesatzen da eta bezeroen profil eguneratuak sortzen dira. Ondoren, eguneratutako profil hauek segmentuak freskatzeko erabiltzen dira, informazio eguneratuenarekin lan egiten duzula ziurtatzeko.

Beste era batera esanda, ziurtatu Customer Insights-era inportatzen diren iturburuko datuek azken informazioa dutela beti.

Informazio gehiagorako, ikus [Freskatu segmentuak eskuz](segments.md#refresh-segments) edo [konfiguratu programatutako freskatze bat](schedule-refresh.md).

[!INCLUDE [footer-include](includes/footer-banner.md)]
