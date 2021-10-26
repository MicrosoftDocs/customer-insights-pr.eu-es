---
title: Ekarri zure Azure gako-ganga sekretuak kudeatzeko
description: Ikasi Customer Insights nola konfiguratu zure Azure gako-ganga erabiltzeko.
ms.date: 10/06/2021
ms.reviewer: mhart
ms.service: customer-insights
ms.subservice: audience-insights
ms.topic: how-to
author: brndkfr
ms.author: bkief
manager: shellyha
ms.openlocfilehash: 6f521dfce3e0922238d16beee3be8e1bbcfc63a5
ms.sourcegitcommit: 693458e13e4b4d94b6205093559912f6a4dc4a1c
ms.translationtype: HT
ms.contentlocale: eu-ES
ms.lasthandoff: 10/06/2021
ms.locfileid: "7606030"
---
# <a name="bring-your-own-azure-key-vault-preview"></a>Ekarri zure Azure gako-ganga (aurrebista)

Dedikatu bat estekatzea [Azure gako ganga](/azure/key-vault/general/basic-concepts) audientziari buruzko informazioaren inguruneak erakundeei betetzen dituen baldintzak betetzen laguntzen die.
Eskainitako gako-ganga erakundearen betetze-mugan sekretuak agertzeko eta erabiltzeko erabil daiteke. Ikusleen estatistikek Azure Key Vault-eko sekretuak erabil ditzakete [konexioak konfiguratu](connections.md) hirugarrenen sistemetara.

## <a name="link-the-key-vault-to-the-audience-insights-environment"></a>Lotu gako-ganga ikusleen ikuspegi ingurunearekin

### <a name="prerequisites"></a>Aurrebaldintzak

Entzuleen estatistiketan gako-ganga konfiguratzeko, honako baldintza hauek bete behar dira:

- Azure harpidetza aktibo bat duzu.

- Baduzu [Administratzailea](permissions.md#administrator) funtzioa hartzaileen xehetasunetan. Lortu informazio gehiago [erabiltzaileen baimenak ikusleen estatistiketan](permissions.md#assign-roles-and-permissions).

- Baduzu [Laguntzailea](/azure/role-based-access-control/built-in-roles#contributor) eta [Erabiltzaile sarbide administratzailea](/azure/role-based-access-control/built-in-roles#user-access-administrator) gakoen gangan edo gako gangan dauden baliabideen taldean dauden rolak. Informazio gehiagorako, joan hona [Gehitu edo kendu Azure rolen esleipenak Azure ataria erabiliz](/azure/role-based-access-control/role-assignments-portal). Erabiltzaile sarbide administratzailearen rola ez baduzu gako gangan, roletan oinarritutako sarbide kontrol baimenak konfiguratu behar dituzu Azure zerbitzu nagusirako Dynamics 365 Customer Insights bereizita. Jarraitu urratsak [erabili Azure zerbitzu nagusia](connect-service-principal.md) lotu beharko litzatekeen gako-ganga.

- Gako gangak Key Vault suebakia izan behar du **desgaituta**.

- Giltza ganga berean dago [Azure kokapena](https://azure.microsoft.com/global-infrastructure/geographies/#overview) ikusleek ingurunea ulertzen duten heinean. Ikusleei buruzko informazioaren ingurunearen eskualdea zerrendan agertzen da **Administratzailea** > **Sistema** > **Buruz** > **Eskualdea**.

### <a name="link-a-key-vault-to-the-environment"></a>Lotu gako-ganga ingurunearekin

1. Joan **Administratzailea** > **Sistema**, eta gero hautatu **Segurtasuna** fitxa.
1. Gainean **Giltza Ganga** fitxa, hautatu **Konfigurazioa**.
1. Aukeratu **Harpidetza**.
1. Aukeratu gakoaren ganga **Giltza Ganga** goitibeherako zerrenda. Gako ganga gehiegi agertzen badira, hautatu baliabide talde bat bilaketaren emaitzak mugatzeko.
1. Onartu **Datuen pribatutasuna eta betetzea** adierazpena.
1. Sakatu **Gorde**.

:::image type="content" source="media/set-up-azure-key-vault.png" alt-text="Lotutako gako-ganga bat konfiguratzeko urratsak ikusleen estatistiketan.":::

**Giltza Ganga** fitxak estekatutako gako gangaren izena, baliabide taldea eta harpidetza erakusten ditu orain. Konexioaren konfigurazioan erabiltzeko prest dago.
Gako-gangaren baimenak zein diren ikusleei buruzko informazioari buruzko xehetasunak ikusteko, joan hona [Ikuspegi estatistiketarako gako-gangan emandako baimenak](#permissions-granted-on-the-key-vault-to-audience-insights), geroago artikulu honetan.

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

## <a name="permissions-granted-on-the-key-vault-to-audience-insights"></a>Ikuspegi estatistiketarako gako-gangan emandako baimenak

Ondorengo baimenak estekatutako gako-ganga bateko ikusleei buruzko informazioa ematen zaie [Key Vault sarbide politika](/azure/key-vault/general/assign-access-policy?tabs=azure-portal) edo [Azure rolean oinarritutako sarbide kontrola](/azure/key-vault/general/rbac-guide?tabs=azure-cli) gaituta dago.

### <a name="key-vault-access-policy"></a>Key Vault sarbide politika

| Mota        | Baimenak          |
| ----------- | -------------------- |
| Tekla         | [Lortu Gakoak](/rest/api/keyvault/get-keys), [Lortu Gakoa](/rest/api/keyvault/get-key)                                 |
| Dun & Bradstreet proiektuaren eskualdea      | [Lortu sekretuak](/rest/api/keyvault/get-secrets), [Lortu sekretua](/rest/api/keyvault/get-secret)                     |
| Ziurtagiria | [Lortu ziurtagiriak](/rest/api/keyvault/get-certificates), [Lortu ziurtagiria](/rest/api/keyvault/get-certificate) |

Aurreko balioak exekuzioan zehar zerrendatzeko eta irakurtzeko gutxienekoak dira.

### <a name="azure-role-based-access-control"></a>Azure rolean oinarritutako sarbide kontrola

Key Vault Reader eta Key Vault Secrets Erabiltzailearen rolak ikusleei buruzko informazioa lortzeko gehituko dira. Eginkizun horiei buruzko xehetasunak lortzeko, joan hona [Azure integratutako rolak Key Vault datu planoaren eragiketetarako](/azure/key-vault/general/rbac-guide?tabs=azure-cli).

## <a name="recommendations"></a>Gomendioak

- Erabili bereizitako edo dedikatutako gako-ganga bat, ikusleentzako estatistiketarako beharrezkoak diren sekretuak soilik biltzen dituena. Irakurri zergatik buruzko informazio gehiago [gako-ganga bereiziak gomendatzen dira](/azure/key-vault/general/best-practices#why-we-recommend-separate-key-vaults).

- Jarraitu [Key Vault erabiltzeko praktika egokiak](/azure/key-vault/general/best-practices#turn-on-logging) sarbide, segurtasun kopia, auditoria eta berreskurapen aukerak kontrolatzeko.

## <a name="frequently-asked-questions"></a>Maiz egiten diren galderak

### <a name="can-audience-insights-write-secrets-or-overwrite-secrets-into-the-key-vault"></a>Ikuslegoaren ikuspegiak sekretuak idatz ditzake edo sekretuak gainidatzi gako-gangan?

Ez. Fitxategian azaltzen diren irakurtzeko eta zerrendatzeko baimenak soilik [baimenak eman ditu](#permissions-granted-on-the-key-vault-to-audience-insights) artikulu honetako lehen atalak ikusleen ikuspegiei ematen zaizkie. Sistemak ezin ditu gakoak gordetzeko sekretuak gehitu, ezabatu edo gainidatzi. Hori da, gainera, konexioak Key Vault erabiltzen duenean ezin dituzun egiaztagiriak sartu.

### <a name="can-i-change-a-connection-from-using-key-vault-secrets-to-default-authentication"></a>Ezin al dut konexiorik aldatu Key Vault sekretuak erabiltzetik autentifikazio lehenetsira?

Ez. Ezin duzu berriro konexio lehenetsira aldatu konfiguratu ondoren estekatutako gako-ganga bateko sekretua erabiliz. Sortu aparteko konexioa, eta ezabatu zaharra, behar ez baduzu.

### <a name="how-can-i-revoke-access-to-a-key-vault-for-audience-insights"></a>Nola ezezta dezaket entzuleen argibideetarako gako-giltzarako sarbidea?

Ea duen [Key Vault sarbide politika](/azure/key-vault/general/assign-access-policy?tabs=azure-portal) edo [Azure rolean oinarritutako sarbide kontrola](/azure/key-vault/general/rbac-guide?tabs=azure-cli) gaituta dago, zerbitzuaren nagusiaren baimenak kendu behar dituzu `0bfc4568-a4ba-4c58-bd3e-5d3e76bd7fff` izenarekin `Dynamics 365 AI for Customer Insights`. Gako-ganga erabiltzen duten konexio guztiek funtzionatzeari utziko diote.

### <a name="a-secret-thats-used-in-a-connection-got-removed-from-the-key-vault-what-can-i-do"></a>Konexio batean erabiltzen den sekretua gako-gangetik kendu da. Zer egin dezaket?

Jakinarazpen bat agertzen da ikusleen estatistiketan, gako-gordelekutik konfiguratutako sekretua eskuragarri ez dagoenean. Gaitu [soft-ezabatu](/azure/key-vault/general/soft-delete-overview) teklatuko gangan sekretuak leheneratzeko nahi gabe kentzen badira.

### <a name="a-connection-doesnt-work-but-my-secret-is-in-the-key-vault-what-might-be-the-cause"></a>Konexio batek ez du funtzionatzen, baina nire sekretua gako gangan dago. Zein izan daiteke kausa?

Jakinarazpen bat entzuleen estatistiketan agertzen da gako-gangera sartu ezin denean. Hau izan daiteke kausa:

- Ikusleei buruzko informazioaren zerbitzuaren zuzendariaren baimenak kendu egin dira. Eskuz leheneratu behar dira.

- Gako gangaren suebakia gaituta dago. Suebakia desgaitu behar da gako-ganga berriro ikusleentzako eskuragarri egon dadin.
