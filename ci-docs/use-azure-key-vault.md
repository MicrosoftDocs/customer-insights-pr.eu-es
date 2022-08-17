---
title: Ekarri zure Azure gako-ganga (aurrebista)
description: Ikasi Customer Insights nola konfiguratu zure Azure gakoen ganga erabiltzeko sekretuak kudeatzeko.
ms.date: 08/02/2022
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: brndkfr
ms.author: bkief
manager: shellyha
searchScope:
- ci-system-security
- customerInsights
ms.openlocfilehash: 229fb5698a02d1d73c30442f61c7b1b5fce918bf
ms.sourcegitcommit: 49394c7216db1ec7b754db6014b651177e82ae5b
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 08/10/2022
ms.locfileid: "9246140"
---
# <a name="bring-your-own-azure-key-vault-preview"></a>Ekarri zure Azure gako-ganga (aurrebista)

Dedikatu bat lotzea [Azure gakoen ganga](/azure/key-vault/general/basic-concepts) Customer Insights ingurunera erakundeei laguntzen die betetze-baldintzak betetzen.

## <a name="link-the-key-vault-to-the-customer-insights-environment"></a>Lotu gakoen ganga Customer Insights ingurunearekin

Konfiguratu dedikatu gako-biltegia erakunde baten betetze-mugan sekretuak antolatzeko eta erabiltzeko.

### <a name="prerequisites"></a>Aurrebaldintzak

- Azure harpidetza aktibo bat.

- An [Administratzailea](permissions.md#admin) rola [esleitu](permissions.md#add-users) Bezeroen Insights-en.

- [Laguntzailea](/azure/role-based-access-control/built-in-roles#contributor) eta [Erabiltzaileen Sarbide Administratzailea](/azure/role-based-access-control/built-in-roles#user-access-administrator) gako-gankoan edo gako-gangako baliabide-taldeari dagozkion rolak. Informazio gehiagorako, joan hona [Gehitu edo kendu Azure rolen esleipenak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal). Ez baduzu Erabiltzaileen Sarbidearen Administratzaile rola gakoen gangan, konfiguratu Azure zerbitzu nagusirako roletan oinarritutako sarbidea kontrolatzeko baimenak.Dynamics 365 Customer Insights bereizita. Jarraitu urratsak [erabili Azure zerbitzu nagusia](connect-service-principal.md) lotu beharko litzatekeen gako-ganga.

- Gako-gangak Key Vault suebakia izan behar du **desgaituta**.

- Gako-ganga berean dago [Azure kokapena](https://azure.microsoft.com/global-infrastructure/geographies/#overview) Customer Insights ingurune gisa. Customer Insights atalean, joan hona **Admin** > **Sistema** eta **Buruz** fitxa inguruneko eskualdea ikusteko.

### <a name="recommendations"></a>Gomendioak

- [Erabili gako-ganga bereizi edo dedikatu bat](/azure/key-vault/general/best-practices#why-we-recommend-separate-key-vaults) Customer Insights-erako beharrezkoak diren sekretuak baino ez dituena.

- Jarraitu [Key Vault erabiltzeko praktika egokiak](/azure/key-vault/general/best-practices#turn-on-logging) sarbide, segurtasun kopia, auditoria eta berreskurapen aukerak kontrolatzeko.

### <a name="link-a-key-vault-to-the-environment"></a>Lotu gako-ganga ingurunearekin

1. Joan **Admin** > **Segurtasuna**, eta, ondoren, hautatu **Gakoen ganga** fitxa.
1. Gainean **Giltza Ganga** fitxa, hautatu **Konfigurazioa**.
1. Aukeratu **Harpidetza**.
1. Aukeratu gakoaren ganga **Giltza Ganga** goitibeherako zerrenda. Gako-ganga gehiegi erabilgarri badaude, hautatu baliabide-talde bat bilaketa-emaitzak mugatzeko.
1. Berrikusi [Datuen pribatutasuna eta betetzea](connections.md#data-privacy-and-compliance) eta hautatu **ados**.
1. Sakatu **Gorde**.

The **Gakoen ganga** fitxak estekatutako gakoen gangaren izena, harpidetza eta baliabide taldea erakusten ditu. Konexioaren konfigurazioan erabiltzeko prest dago.
Gakoen gangan zein baimen ematen zaizkion Customer Insights-i buruzko xehetasunak lortzeko, joan hona [Gakoen gangan emandako baimenak](#permissions-granted-on-the-key-vault).

## <a name="use-the-key-vault-in-the-connection-setup"></a>Erabili gako-ganga konexioaren konfigurazioan

Noiz [konexioak ezartzea](connections.md) to [onartzen duen hirugarren batek](#supported-connection-types) sistemak, erabili estekatutako Key Vault-eko sekretuak konexioak konfiguratzeko.

1. Joan **Administratzailea** > **Konexioak**.
1. Hautatu **Gehitu konexioa**.
1. Onartutako konexio motetarako, **Erabili Key Vault** txandakatzea erabilgarri dago gako-ganga lotu baduzu.
1. Sekretua eskuz sartu beharrean, aukeratu gakoen kutxako balio sekretua adierazten duen sekretua.

   :::image type="content" source="media/use-key-vault-secret.png" alt-text="Key Vault sekretua erabiltzen duen SFTP konexioarekin konexio panela.":::

1. Hautatu **Gorde** konexioa sortzeko.

## <a name="supported-connection-types"></a>Onartutako konexio motak

Hurrengo [esportatu](export-destinations.md) konexioak onartzen dira:

* [ActiveCampaign](export-active-campaign.md)
* [Autopilot](export-autopilot.md)
* [DotDigital](export-dotdigital.md)
* [Google Ads](export-google-ads.md)
* [Klaviyo](export-klaviyo.md)
* [LiveRamp](export-liveramp.md)
* [Marketo](export-marketo.md)
* [Omnisend](export-omnisend.md)
* [Salesforce Marketing Cloud](export-salesforce.md)
* [Sendgrid](export-sendgrid.md)
* [Sendinblue](export-sendinblue.md)
* [SFTP](export-sftp.md)

## <a name="permissions-granted-on-the-key-vault"></a>Gakoen gangan emandako baimenak

Honako baimen hauek ematen zaizkio Customer Insights-i estekatutako gako-biltegian [Key Vault-en sarbide-politika](/azure/key-vault/general/assign-access-policy?tabs=azure-portal) edo [Azure roletan oinarritutako sarbide-kontrola](/azure/key-vault/general/rbac-guide?tabs=azure-cli) gaituta dago.

### <a name="key-vault-access-policy"></a>Key Vault sarbide politika

| Mota        | Baimenak          |
| ----------- | -------------------- |
| Tekla         | [Lortu Gakoak](/rest/api/keyvault/keys/get-keys/get-keys), [Lortu Gakoa](/rest/api/keyvault/keys/get-key/get-key)                                 |
| Dun & Bradstreet proiektuaren eskualdea      | [Lortu sekretuak](/rest/api/keyvault/secrets/get-secrets/get-secrets), [Lortu sekretua](/rest/api/keyvault/secrets/get-secret/get-secret)                     |
| Ziurtagiria | [Lortu ziurtagiriak](/rest/api/keyvault/certificates/get-certificates/get-certificates), [Lortu ziurtagiria](/rest/api/keyvault/certificates/get-certificate/get-certificate) |

Aurreko balioak exekuzioan zehar zerrendatzeko eta irakurtzeko gutxienekoak dira.

### <a name="azure-role-based-access-control"></a>Azure rolean oinarritutako sarbide kontrola

The [Key Vault Reader eta Key Vault Secrets Erabiltzaile rolak](/azure/key-vault/general/rbac-guide?tabs=azure-cli) gehituko da Customer Insights-erako.

## <a name="frequently-asked-questions"></a>Ohiko galderak

### <a name="can-customer-insights-write-secrets-or-overwrite-secrets-into-the-key-vault"></a>Customer Insights-ek sekretuak idatz ditzake edo sekretuak gainidatzi ditzake gakoen gangan?

Ez. Irakurtzeko eta zerrendatzeko baimenak bakarrik [emandako baimenak](#permissions-granted-on-the-key-vault) Customer Insights-i ematen zaie. Sistemak ezin ditu gakoak gordetzeko sekretuak gehitu, ezabatu edo gainidatzi. Hori da, gainera, konexioak Key Vault erabiltzen duenean ezin dituzun egiaztagiriak sartu.

### <a name="can-i-change-a-connection-from-using-key-vault-secrets-to-default-authentication"></a>Ezin al dut konexiorik aldatu Key Vault sekretuak erabiltzetik autentifikazio lehenetsira?

Ez. Ezin duzu berriro konexio lehenetsira aldatu konfiguratu ondoren estekatutako gako-ganga bateko sekretua erabiliz. Sortu aparteko konexioa, eta ezabatu zaharra, behar ez baduzu.

### <a name="how-can-i-revoke-access-to-a-key-vault-for-customer-insights"></a>Nola ezezta dezaket Customer Insights-en gakoen biltegirako sarbidea?

bada [Key Vault-en sarbide-politika](/azure/key-vault/general/assign-access-policy?tabs=azure-portal) edo [Azure roletan oinarritutako sarbide-kontrola](/azure/key-vault/general/rbac-guide?tabs=azure-cli) gaituta dago, kendu zerbitzu nagusiaren baimenak`0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` izenarekin `Dynamics 365 AI for Customer Insights`. Gako-ganga erabiltzen duten konexio guztiek funtzionatzeari utziko diote.

### <a name="a-secret-thats-used-in-a-connection-got-removed-from-the-key-vault-what-can-i-do"></a>Konexio batean erabiltzen den sekretua gako-gangetik kendu da. Zer egin dezaket?

Jakinarazpen bat agertzen da Customer Insights-en gako-biltegitik konfiguratutako sekretu bat eskuragarri ez dagoenean. Gaitu [soft-ezabatu](/azure/key-vault/general/soft-delete-overview) teklatuko gangan sekretuak leheneratzeko nahi gabe kentzen badira.

### <a name="a-connection-doesnt-work-but-my-secret-is-in-the-key-vault-what-might-be-the-cause"></a>Konexio batek ez du funtzionatzen, baina nire sekretua gako gangan dago. Zein izan daiteke kausa?

Jakinarazpen bat agertzen da Customer Insights-en ezin duenean atzitu gakoen ganga. Hau izan daiteke kausa:

- Customer Insights zerbitzu nagusiaren baimenak kendu dira. Eskuz leheneratu behar dira.

- Gako gangaren suebakia gaituta dago. Suebakia desgaitu egin behar da Customer Insights-en gakoen biltegia berriro erabilgarri izan dadin.
