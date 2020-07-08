---
title: Notes de publication de MBAM2.5
description: Notes de publication de MBAM2.5
author: dansimp
ms.assetid: fcaf03e6-5e39-4771-af3c-a3cd468f3961
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4bcc17d6295b14a7f3276146d5630b869b94b7f0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810883"
---
# Notes de publication de MBAM2.5


Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.

Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker Administration and Monitoring (MBAM) 2,5. Ces notes de publication contiennent des informations nécessaires à l’installation réussie de MBAM et contiennent des informations qui ne sont pas disponibles dans la documentation du produit. Si ces notes de publication diffèrent d’autres documents de la 2,5 de MBAM, envisagez d’utiliser la dernière modification pour faire autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## <a href="" id="---------mbam-2-5-known-issues"></a> Problèmes connus de MBAM 2,5


Cette section contient des notes de publication pour MBAM 2,5.

### Navigateur Web exécuté involontairement en tant qu’administrateur

Les liens d’aide de l’outil de configuration de MBAM Server peuvent entraîner l’ouverture des fenêtres de navigateur avec des droits d’administrateur.

**Solution de contournement:** Activez la configuration de la sécurité améliorée d’Internet Explorer (IESC) ou fermez votre navigateur Web pour accéder à d’autres sites.

**Remarques**  Ce problème a été résolu dans MBAM 2,5 SP1.

 

### <a href="" id="-------------mbam-reports-as-noncompliant-a-client-encrypted-with-aes-256-bit-encryption-keys-and-diffuser"></a> 256 MBAM-xxx XXXXXXX XXXXXXX xxxx xxx XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX

Si le client MBAM 2,5 est installé et est chiffré à l’aide du système AES 256-bit avec la puissance de chiffrement du diffuseur, le client MBAM est signalé comme non conforme dans les rapports de conformité MBAM.

**Solution de contournement:** Installez le correctif sur [KB2975636](https://go.microsoft.com/fwlink/?LinkId=511972).

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM ne parvient pas à chiffrer un volume et signale une erreur si vous avez configuré un module de protection TPM + PIN sur un appareil de tablette

Si les utilisateurs finaux essaient de définir un protecteur de plateforme sécurisée + code confidentiel sur un appareil de tablette, MBAM ne peut pas être chiffré et signale une erreur. Ce problème survient parce que les appareils tablettes n’ont pas de clavier d’environnement de pré-démarrage.

**Solution de contournement:** Activez l’option **activer l’authentification BitLocker nécessitant une entrée au clavier prédémarrage sur des tablettes** . Ce paramètre est un paramètre de stratégie de groupe BitLocker qui n’est pas disponible dans les modèles de stratégie de groupe MBAM.

### Le nom d’utilisateur principal est requis pour tous les comptes de service.

Un nom d’utilisateur principal (UPN) doit être défini pour tous les comptes de service dans MBAM. Si vous ne parvenez pas à créer un UPN pour un compte, un message d’erreur s’affiche lors du processus de configuration pour indiquer que l’utilisateur ou le groupe est introuvable dans Active Directory.

**Solution de contournement:** Ajoutez le nom d’utilisateur principal au compte de service.

### Le portail libre-service nécessite une configuration supplémentaire si les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu de Microsoft Ajax

Si vos ordinateurs clients n’ont pas accès au réseau de distribution de contenu (CDN) Microsoft Ajax, ce qui donne au portail libre-service l’accès qu’il nécessite pour certains fichiers JavaScript, vous devez configurer le portail libre-service pour qu’il référence les fichiers JavaScript à partir d’une source accessible. Si vous ne configurez pas le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au CDN, seul le nom de la société et le compte sous lequel vous vous êtes connecté est affiché. Aucun message d’erreur ne s’affiche.

**Solution de contournement:** Installez MBAM 2,5 SP1. vous pouvez configurer le portail libre-service en suivant ces instructions: [Comment configurer le portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md).

### Le portail libre-service et le site Web d’administration et de surveillance ne s’ouvrent pas après la mise à niveau d’IIS vers .NET Framework 4,5

Lorsque vous mettez à niveau Internet Information Services (IIS) vers Microsoft .NET Framework 4,5, le portail libre-service et le site Web d’administration et de surveillance ne s’ouvrent pas.

**Solution de contournement:** Voir le [message d’erreur suivant l’installation de .NET Framework 4,0: «impossible de charger le type «System. ServiceModel. activation. HttpModule»](https://go.microsoft.com/fwlink/?LinkId=393568).

### Le site Web d’administration et de surveillance affiche un message d’erreur «rapport introuvable» lorsque les rapports ne sont pas configurés

Si vous configurez le site Web d’administration et de surveillance et que vous essayez d’afficher un rapport sans tout d’abord configurer la fonction rapports, un message d’erreur indique que le rapport est introuvable.

**Solution de contournement:** Configurez la fonctionnalité rapports avant de configurer les applications Web.

### Les rapports figurant sur le site Web d’administration et de surveillance affichent un avertissement si SSL n’est pas configuré dans SSRS

Si SQL Server Reporting Services (SSRS) n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL de la fonctionnalité rapports sera définie sur HTTP au lieu de HTTPs lorsque vous configurez le serveur MBAM. Pour ouvrir le site Web d’administration et de surveillance et sélectionner un rapport, le message d’erreur suivant s’affiche: «seul le contenu sécurisé est affiché».

**Solution de contournement:** Pour afficher l’État, cliquez sur **Afficher tout le contenu**. Pour résoudre ce problème, accédez à l’MBAM ordinateur sur lequel SQL Server Reporting Services est installé, exécutez le **Gestionnaire de configuration de Reporting Services**, puis cliquez sur **URL du service Web**. Sélectionnez le certificat SSL approprié pour le serveur, entrez le port SSL approprié (le port par défaut est 443), puis cliquez sur **appliquer**.

### Cliquer sur «retour» dans le rapport synthèse de conformité BitLocker peut générer une erreur

Si vous explorez un rapport de synthèse de conformité BitLocker, puis cliquez sur le lien **retour** dans le rapport SSRS, une erreur peut être levée.

**Solution de contournement:** Néant.

### Le chiffrement de l’espace utilisé uniquement ne fonctionne pas correctement

Si vous chiffrez un ordinateur pour la première fois après avoir installé le client MBAM, et que vous avez configuré un paramètre de stratégie de groupe pour implémenter le chiffrement de l’espace utilisé uniquement, MBAM chiffre par erreur le disque entier au lieu de chiffrer uniquement l’espace utilisé du disque. Si un ordinateur est déjà chiffré avec l’espace utilisé uniquement lors de l’installation du client MBAM et si vous avez configuré le même paramètre de stratégie de groupe, MBAM indique que le lecteur est correctement crypté et qu’il n’essaye pas de le chiffrer à nouveau.

**Solution de contournement:** Néant.

### Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité de l’ordinateur BitLocker

Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur BitLocker dans le niveau d’intégration de Configuration Manager affiche toujours «inconnu» pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement de 128 bits. Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.

**Solution de contournement:** Définissez toujours une clé de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** l’objet de stratégie de groupe santé du chiffrement.

### Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration

Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.

**Solution de contournement:** Néant. La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.

### La configuration de la sécurité améliorée peut entraîner un affichage incorrect du message d’erreur

Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message d’erreur «Accès refusé» peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM. Par défaut, la fonction Échap est activée pour protéger le serveur en diminuant son exposition aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.

**Solution de contournement:** Si le message d’erreur «Accès refusé» s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier manuellement la valeur par défaut de votre image pour désactiver la configuration de la sécurité améliorée. Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel ESC n’est pas activé.

## <a href="" id="hotfixes-and-knowledge-base-articles-for-mbam-2-5-"></a>Articles sur les correctifs et les Articles de la base de connaissances pour MBAM 2,5


Le tableau suivant répertorie les articles sur les correctifs et les Articles de la base de connaissances pour MBAM 2,5.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Article de la base de connaissances</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2975636</p></td>
<td align="left"><p>Correctif logiciel 1 pour l’administration et le contrôle de 2,5 de Microsoft BitLocker</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975636/EN-US" data-raw-source="[support.microsoft.com/kb/2975636/EN-US](https://support.microsoft.com/kb/2975636/EN-US)">support.microsoft.com/kb/2975636/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>3015477</p></td>
<td align="left"><p>Package Hotfix 2 pour l’administration et l’analyse de BitLocker 2,5</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3015477" data-raw-source="[support.microsoft.com/kb/3015477](https://support.microsoft.com/kb/3015477)">support.microsoft.com/kb/3015477</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>3011022</p></td>
<td align="left"><p>Échec de la création de rapports de l’installation d' 2,5 ou du gestionnaire de configuration MBAM si le nom de l’instance SSRS contient un trait de soulignement</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/3011022/EN-US" data-raw-source="[support.microsoft.com/kb/3011022/EN-US](https://support.microsoft.com/kb/3011022/EN-US)">support.microsoft.com/kb/3011022/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2756402</p></td>
<td align="left"><p>Le client MBAM échoue avec l’ID d’événement 4 et le code d’erreur 0x8004100E dans la description de l’événement.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Erreur lors de l’ouverture des rapports de conformité entreprise ou ordinateur dans MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Échec de l’installation de MBAM 2,0 lors du scénario d’intégration de Configuration Manager avec SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2975472</p></td>
<td align="left"><p>Interblocages SQL lorsque de nombreux clients MBAM se connectent à la base de données de récupération MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2975472/EN-US" data-raw-source="[support.microsoft.com/kb/2975472/EN-US](https://support.microsoft.com/kb/2975472/EN-US)">support.microsoft.com/kb/2975472/EN-US</a></p></td>
</tr>
</tbody>
</table>

 


## Rubriques connexes


[À propos de MBAM2.5](about-mbam-25.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





