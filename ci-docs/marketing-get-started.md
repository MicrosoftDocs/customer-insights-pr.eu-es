---
title: Erabili profil bateratuak Dynamics 365 Marketing-en
description: Ikasi profil eta segmentu bateratuak nola integratzen Dynamics 365 Marketing-ekin.
ms.date: 04/20/2022
ms.topic: conceptual
author: m-hartmann
ms.author: mhart
manager: shellyha
ms.openlocfilehash: 99ec463299a24ea81cfe26bb785e36bdefdcd080
ms.sourcegitcommit: a97d31a647a5d259140a1baaeef8c6ea10b8cbde
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9054417"
---
# <a name="use-unified-customer-profiles-in-dynamics-365-marketing"></a>Erabili bezero-profil bateratuak Dynamics 365 Marketing-en

[Dynamics 365 Marketing](/dynamics365/marketing/overview) bezeroen esperientziak hobetzen ditu, eta ukipen-puntu guztietan bidaia pertsonalizatuak antolatu ditzakezu harremanak sendotzeko eta leialtasuna lortzeko. Dynamics 365 Marketing aplikazioak ezin hobeto funtzionatzen du Dynamics 365 Sales-ekin,Dynamics 365 Customer Insights,Microsoft Teams, eta beste produktu batzuk eta datuen eta IAren boterea erabiliz erabaki azkarrago eta hobeak har ditzakezu.

Customer Insights datuak Marketing-ekin konektatuz, hau egin dezakezu:

- Helburua bezeroen profil eta segmentu bateratuetara. Horri esker, bezero bakoitzarekin harremanetan jar zaitezke, bezeroaren datuen kokapena edozein dela ere.
- Oinarri eduki dinamikoa (adibidez, token pertsonalizatuak) mezu elektronikoetan, SMSetan eta push jakinarazpenetan, besteak beste, leialtasun-egoera, harpidetza berritzeko data, kontu nagusi edo Customer Insights profil bateratuan jaso duzun beste edozein neurritan.
- Kargatu Marketing-eko datuak Customer Insights-en eta konbinatu beste iturri batzuetako bezeroen datuekin.
- Aplikatu Customer Insights datuak garbitzeko, aberasteko eta parekatzeko tresna lausoak.

## <a name="use-rich-customer-profiles-in-real-time-marketing"></a>Erabili bezeroen profil aberatsak denbora errealeko marketinean

Denbora errealeko marketinak sortzeko aukera ematen dizu [abiarazle pertsonalizatuak](/dynamics365/marketing/real-time-marketing-custom-triggers) bezeroen bidaiak abiarazten dituztenak bezeroaren edozein ekintzatan oinarrituta. Zenbat eta pertsonalizatuago zure datuak, orduan eta garrantzitsuago eta pertsonalizatuagoak izango dira zure bidaiak. Hori da marketina eta bezeroen ikuspegia konbinatzea hain indartsua. Ahal duzu [datuak bateratu](data-unification.md) edozein iturritatik, gero erabili bezeroen bidaia hiperpertsonalizatuak elikatzeko.

Gehiago ikasi: [Erabili Customer Insights profilak eta segmentuak denbora errealeko marketinean](/dynamics365/marketing/real-time-marketing-ci-profile)

## <a name="use-unified-segments-with-outbound-customer-journeys"></a>Erabili segmentu bateratuak irteerako bezeroen bidaiekin

Customer Insights-ek iturri askotako datuak fintzeko eta bezeroen segmentu agregatuetan konbinatzeko aukera ematen du. Nork [Customer Insights irteerako marketinarekin lotzea](export-dynamics365-marketing.md), segmentu hauek automatikoki agertuko dira *eta* freskatu automatikoki bezero-bidaia diseinatzailean.

Gehiago ikasi: [Erabili segmentuak Dynamics 365 Customer Insights Dynamics 365 Marketing-ekin](/dynamics365/marketing/customer-insights-segments)

## <a name="pull-data-from-your-own-azure-data-lake-storage"></a>Atera zure datuak Azure Data Lake Storage

Ez zara hodeiko biltegiratzera mugatzen Customer Insights datuak Marketing-ekin erabili nahi badituzu. Dagoeneko zurea baduzu Azure Data Lake Storage konfiguratu, Customer Insights-ekin konekta zaitezke, gero datuak Marketing aplikazioarekin parteka ditzakezu hodeian oinarritutako konfigurazio batekin egingo zenukeen bezala.

Gehiago ikasi: [Gaitu honekin datuak partekatzea Dataverse zuretik Azure Data Lake Storage](customer-insights-dataverse.md#enable-data-sharing-with-dataverse-from-your-own-azure-data-lake-storage-preview)
