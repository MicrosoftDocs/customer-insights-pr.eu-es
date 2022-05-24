---
ms.openlocfilehash: 1d79987893986148421c316193b27d268cfe0a0b
ms.sourcegitcommit: 4ae316c856b8de0f08a4605f73e75a8c2cf51c4e
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 05/13/2022
ms.locfileid: "8755529"
---
Datuak hartu ondoren, hasi datuak bateratzeko prozesua bezeroen profil bateratua sortzeko. Informazio gehiago lortzeko, ikusi [Datuen bateratzea](../data-unification.md).

### <a name="select-source-fields"></a>Hautatu iturri-eremuak

1. Behin datuak sartuta, esleitu merkataritza elektronikoko eta fideltasun-datuetako kontaktuak ohiko datu motei. Joan **Datuak** > **Bateratu**.

1. Hautatu bezeroaren profila adierazten duten entitateak – **eCommerceContacts** eta **loyCustomers**.

   ![bateratu ecommerce eta loyalty datu-iturburuak.](../media/unify-ecommerce-loyalty.png)

1. Hautatu **ContactId** **eCommerceContacts** entitatearen gako nagusi gisa eta **LoyaltyID** **loyCustomers** entitatearen gako nagusi gisa.

1. Hautatu **Hurrengoa**. Saltatu erregistro bikoiztuak eta hautatu **Hurrengoa**.

### <a name="match-conditions"></a>Partiduen baldintzak

1. Aukeratu **eCommerceContacts: eCommerce** entitate nagusi gisa eta erregistro guztiak barne hartzen ditu.

1. Aukeratu **loyCustomers: LoyaltyScheme** eta erregistro guztiak sartu.

1. Gehitu arau bat:
   - Hautatu **Izen osoa** bai eCommerceContacts eta loyCustomers.
   - Hautatu **Mota (Telefonoa, Izena, Helbidea, ...)** rentzat **Normalizatu**.
   - Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.
   - Sartu **Izen osoa, posta elektronikoa** izenagatik.

1. Gehitu bigarren baldintza bat helbide elektronikorako:
   - Hautatu **Posta elektronikoa** bai eCommerceContacts eta loyCustomers.
   - "Normalizatu" hutsik utzi.
   - Ezarri **Zehaztasun maila**: **Oinarrizkoa** eta **Balioa**: **Altua**.

   ![Bateratu izenaren eta helbide elektronikoaren bat-etortze araua.](../media/unify-match-rule.png)

1. Hautatu **Eginda**.

1. Hautatu **Hurrengoa**.

### <a name="unify-fields"></a>Eremuak bateratu

1. Aldatu izena **Kontaktu ID** rentzat **loyBezeroak** entitateari **Harremanetarako IDLEIALTASUNA** irensten diren beste IDetatik bereizteko.

1. Hautatu **Hurrengoa** berrikusteko eta gero hautatu **Sortu bezeroen profilak**.
