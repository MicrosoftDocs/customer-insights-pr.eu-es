---
title: Ekarri zure Azure gako-ganga (aurrebista)
description: Ikasi nola konfiguratu Customer Insights zure Azure gakoen ganga erabiltzeko sekretuak kudeatzeko.
ms.date: 10/06/2021
ms.reviewer: mhart
ms.subservice: audience-insights
ms.topic: how-to
author: brndkfr
ms.author: bkief
manager: shellyha
searchScope:
- ci-system-security
- customerInsights
ms.openlocfilehash: 8fdb131de35c7d936d2921265f03faa5682db6f6
ms.sourcegitcommit: dca46afb9e23ba87a0ff59a1776c1d139e209a32
ms.translationtype: MT
ms.contentlocale: eu-ES
ms.lasthandoff: 06/29/2022
ms.locfileid: "9082631"
---
# <a name="bring-your-own-azure-key-vault-preview"></a>Ekarri zure Azure gako-ganga (aurrebista)

Dedikatu bat lotzea [Azure gakoen ganga](/azure/key-vault/general/basic-concepts) Customer Insights ingurune batera erakundeei laguntzen die betetze-baldintzak betetzen.
Eskainitako gako-ganga erakundearen betetze-mugan sekretuak agertzeko eta erabiltzeko erabil daiteke. Customer Insights-ek Azure Key Vault-eko sekretuak erabil ditzake [konexioak ezarri](connections.md) hirugarrenen sistemetara.

## <a name="link-the-key-vault-to-the-customer-insights-environment"></a>Lotu gakoen ganga Customer Insights ingurunearekin

### <a name="prerequisites"></a>Aurrebaldintzak

Customer Insights-en gakoen biltegia konfiguratzeko, aurrebaldintza hauek bete behar dira:

- Azure harpidetza aktibo bat duzu.

- Bat daukazu [Administratzailea](permissions.md#admin) Customer Insights-en eginkizuna. Lortu informazio gehiago [erabiltzailearen baimenak Customer Insights-en](permissions.md#assign-roles-and-permissions).

- Baduzu [Laguntzailea](/azure/role-based-access-control/built-in-roles#contributor) eta [Erabiltzaile sarbide administratzailea](/azure/role-based-access-control/built-in-roles#user-access-administrator) gakoen gangan edo gako gangan dauden baliabideen taldean dauden rolak. Informazio gehiagorako, joan hona [Gehitu edo kendu Azure rolen esleipenak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal). Erabiltzaile sarbide administratzailearen rola ez baduzu gako gangan, roletan oinarritutako sarbide kontrol baimenak konfiguratu behar dituzu Azure zerbitzu nagusirako Dynamics 365 Customer Insights bereizita. Jarraitu urratsak [erabili Azure zerbitzu nagusia](connect-service-principal.md) lotu beharko litzatekeen gako-ganga.

- Gako gangak Key Vault suebakia izan behar du **desgaituta**.

- Giltza-ganga berean dago [Azure kokapena](https://azure.microsoft.com/global-infrastructure/geographies/#overview) Customer Insights ingurune gisa. Customer Insights-en ingurunearen eskualdea azpian ageri da **Admin** > **Sistema** > **Buruz** > **Eskualdea**.

### <a name="link-a-key-vault-to-the-environment"></a>Lotu gako-ganga ingurunearekin

1. Joan **Admin** > **Segurtasuna**, eta, ondoren, hautatu **Gakoen ganga** fitxa.
1. Gainean **Giltza Ganga** fitxa, hautatu **Konfigurazioa**.
1. Aukeratu **Harpidetza**.
1. Aukeratu gakoaren ganga **Giltza Ganga** goitibeherako zerrenda. Gako ganga gehiegi agertzen badira, hautatu baliabide talde bat bilaketaren emaitzak mugatzeko.
1. Onartu **Datuen pribatutasuna eta betetzea** adierazpena.
1. Sakatu **Gorde**.

:::image type="content" source="media/set-up-azure-key-vault.png" alt-text="Estekatutako gako-biltegia konfiguratzeko urratsak Customer Insights-en.":::

**Giltza Ganga** fitxak estekatutako gako gangaren izena, baliabide taldea eta harpidetza erakusten ditu orain. Konexioaren konfigurazioan erabiltzeko prest dago.
Customer Insights-i gakoen gangan zein baimen ematen zaizkion buruzko xehetasunak lortzeko, joan hona [Gakoen gangan emandako baimenak](#permissions-granted-on-the-key-vault), geroago artikulu honetan.

## <a name="use-the-key-vault-in-the-connection-setup"></a>Erabili gako-ganga konexioaren konfigurazioan

Noiz [konexioak ezartzen](connections.md) hirugarrenen sistemetarako, estekatutako Key Vault-eko sekretuak erabil daitezke konexioak konfiguratzeko.

1. Joan **Administratzailea** > **Konexioak**.
1. Hautatu **Gehitu konexioa**.
1. Onartutako konexio motetarako, **Erabili Key Vault** txandakatzea erabilgarri dago gako-ganga lotu baduzu.
1. Sekretua eskuz sartu beharrean, gakoaren gangan balio sekretua adierazten duen izen sekretua aukeratu dezakezu.

:::image type="content" source="media/use-key-vault-secret.png" alt-text="Key Vault sekretua erabiltzen duen SFTP konexioarekin konexio panela.":::

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

Key Vault Reader eta Key Vault Secrets Erabiltzaile rolak gehituko dira Customer Insights egiteko. Eginkizun horiei buruzko xehetasunak lortzeko, joan hona [Azure integratutako rolak Key Vault datu planoaren eragiketetarako](/azure/key-vault/general/rbac-guide?tabs=azure-cli).

## <a name="recommendations"></a>Gomendioak

- Erabili Customer Insights-erako beharrezkoak diren sekretuak soilik dituen gako-biltegia bereizi edo dedikatu bat. Irakurri zergatik buruzko informazio gehiago [gako-ganga bereiziak gomendatzen dira](/azure/key-vault/general/best-practices#why-we-recommend-separate-key-vaults).

- Jarraitu [Key Vault erabiltzeko praktika egokiak](/azure/key-vault/general/best-practices#turn-on-logging) sarbide, segurtasun kopia, auditoria eta berreskurapen aukerak kontrolatzeko.

## <a name="frequently-asked-questions"></a>Ohiko galderak

### <a name="can-customer-insights-write-secrets-or-overwrite-secrets-into-the-key-vault"></a>Customer Insights-ek sekretuak idatz ditzake edo sekretuak gainidatzi ditzake gakoen gangan?

Ez. Irakurtzeko eta zerrendatzeko baimenak soilik [emandako baimenak](#permissions-granted-on-the-key-vault) Artikulu honen aurreko atala Customer Insights-i ematen zaie. Sistemak ezin ditu gakoak gordetzeko sekretuak gehitu, ezabatu edo gainidatzi. Hori da, gainera, konexioak Key Vault erabiltzen duenean ezin dituzun egiaztagiriak sartu.

### <a name="can-i-change-a-connection-from-using-key-vault-secrets-to-default-authentication"></a>Ezin al dut konexiorik aldatu Key Vault sekretuak erabiltzetik autentifikazio lehenetsira?

Ez. Ezin duzu berriro konexio lehenetsira aldatu konfiguratu ondoren estekatutako gako-ganga bateko sekretua erabiliz. Sortu aparteko konexioa, eta ezabatu zaharra, behar ez baduzu.

### <a name="how-can-i-revoke-access-to-a-key-vault-for-customer-insights"></a>Nola ezezta dezaket Customer Insights gakoen ganga baterako sarbidea?

Ea duen [Key Vault sarbide politika](/azure/key-vault/general/assign-access-policy?tabs=azure-portal) edo [Azure rolean oinarritutako sarbide kontrola](/azure/key-vault/general/rbac-guide?tabs=azure-cli) gaituta dago, zerbitzuaren nagusiaren baimenak kendu behar dituzu `0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` izenarekin `Dynamics 365 AI for Customer Insights`. Gako-ganga erabiltzen duten konexio guztiek funtzionatzeari utziko diote.

### <a name="a-secret-thats-used-in-a-connection-got-removed-from-the-key-vault-what-can-i-do"></a>Konexio batean erabiltzen den sekretua gako-gangetik kendu da. Zer egin dezaket?

Jakinarazpen bat agertzen da Customer Insights-en gako-biltegitik konfiguratutako sekretu bat eskuragarri ez dagoenean. Gaitu [soft-ezabatu](/azure/key-vault/general/soft-delete-overview) teklatuko gangan sekretuak leheneratzeko nahi gabe kentzen badira.

### <a name="a-connection-doesnt-work-but-my-secret-is-in-the-key-vault-what-might-be-the-cause"></a>Konexio batek ez du funtzionatzen, baina nire sekretua gako gangan dago. Zein izan daiteke kausa?

Jakinarazpen bat agertzen da Customer Insights-en ezin duenean atzitu gakoen ganga. Hau izan daiteke kausa:

- Customer Insights zerbitzu nagusiaren baimenak kendu dira. Eskuz leheneratu behar dira.

- Gako gangaren suebakia gaituta dago. Suebakia desgaitu egin behar da Customer Insights-en gakoen ganga berriro erabilgarri izan dadin.
