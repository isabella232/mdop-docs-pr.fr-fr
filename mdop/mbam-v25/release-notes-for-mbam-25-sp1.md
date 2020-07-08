---
title: Notes de publication de MBAM2.5 SP1
description: Notes de publication de MBAM2.5 SP1
author: dansimp
ms.assetid: 3ac424c8-c490-4d62-aba4-1b462c02e962
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/06/2017
ms.openlocfilehash: 837892897aeca341433de54aca1228c0faeee124
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810884"
---
# Notes de publication de MBAM2.5 SP1


Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.

Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker Administration and Monitoring (MBAM) 2,5 SP1. Ces notes de publication contiennent des informations nécessaires à l’installation réussie de MBAM et contiennent des informations qui ne sont pas disponibles dans la documentation du produit. Si ces notes de publication diffèrent d’autres MBAM 2,5 SP1, considérez la dernière modification comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## <a href="" id="---------mbam-2-5-sp1-known-issues"></a> Problèmes connus de MBAM 2,5 SP1


Cette section contient des notes de publication pour MBAM 2,5 SP1.

### <a href="" id="powershell-read-ad--cmdlets-do-not-provide-feedback-if-user-does-not-have-sufficient-rights"></a>Les applets de cmdlet de lecture-publicité pour PowerShell ne fournissent pas de commentaires si l’utilisateur ne dispose pas de droits suffisants

Si un utilisateur tente d’utiliser les applets de contrôle PowerShell lecture-AD pour le serveur MBAM n’a pas de droits d’utilisateur pour lire les informations de récupération Active Directory ou pour lire les informations du TPM, les applets de contrôle ne fournissent aucun message d’erreur ou d’avertissement à l’utilisateur.

**Solution de contournement:** Utilisez uniquement les applets de applet de lecture/publicité PowerShell Si vous disposez des droits d’utilisateur requis.

### Les applets de commande de migration MBAM Active Directory (AD) ne récupèrent pas les informations de récupération de volume

Les applets de commande de migration MBAM Active Directory (AD) ne peuvent pas récupérer les informations de récupération de volume pour les ordinateurs dans les unités d’organisation (UO) si le caractère barre oblique (/) fait partie du nom de l’unité d’organisation. Les extractions publicitaires répétées échoueront en raison d’une erreur de canal de terminaison lorsque cette erreur se produit.

**Détails techniques:** Ce message d’erreur s’affiche lorsque vous exécutez la commande suivante:

``` syntax
Read-ADRecoveryInformation : Unknown error (0x80005000)
At line:1 char:1
+ Read-ADRecoveryInformation -Server "…" -SearchBase " ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : NotSpecified: (:) [Read-ADRecoveryInformation], COMException
    + FullyQualifiedErrorId : System.Runtime.InteropServices.COMException,Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADRecoveryInformationCommand
```

De plus, la trace de pile d’exception `Error[0].Exception.StackTrace` ressemble à ceci:

``` syntax
   at System.DirectoryServices.DirectoryEntry.Bind(Boolean throwIfFail)
   at System.DirectoryServices.DirectoryEntry.Bind()
   at System.DirectoryServices.DirectoryEntry.get_AdsObject()
   at System.DirectoryServices.PropertyValueCollection.PopulateList()
   at System.DirectoryServices.PropertyValueCollection..ctor(DirectoryEntry entry, String propertyName)
   at System.DirectoryServices.PropertyCollection.get_Item(String propertyName)
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.VerifySettingsConnectivity()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadCore.ExecuteRead()
   at Microsoft.Mbam.Server.Commands.ADPullCommands.ReadADInformationBase.ProcessRecord()
   at System.Management.Automation.CommandProcessor.ProcessRecord()
```

**Solution de contournement:** Pour résoudre ce problème, effectuez l’une des opérations suivantes:

-   Renommez l’unité d’organisation pour supprimer le caractère barre oblique avant d’exécuter le script.

-   Pour exclure toute unité d’organisation problématique du processus de sauvegarde, recherchez une liste d’unités d’organisation dont les noms ne contiennent pas de caractères de barre oblique. Exécutez le script sur ces UO, une unité d’organisation à la fois.

### <a href="" id="-------------mbam-fails-to-encrypt-a-volume-and-reports-an-error-if-you-set-a-tpm---pin-protector-on-a-tablet-device"></a> MBAM ne parvient pas à chiffrer un volume et signale une erreur si vous avez configuré un module de protection TPM + PIN sur un appareil de tablette

Si les utilisateurs finaux essaient de définir un protecteur de plateforme sécurisée + code confidentiel sur un appareil de tablette, MBAM ne peut pas être chiffré et signale une erreur. Ce problème survient parce que les appareils tablettes n’ont pas de clavier d’environnement de pré-démarrage.

**Solution de contournement:** Activez l’option **activer l’authentification BitLocker nécessitant une entrée au clavier prédémarrage sur des tablettes** . Ce paramètre est un paramètre de stratégie de groupe BitLocker qui n’est pas disponible dans les modèles de stratégie de groupe MBAM.

### Le nom d’utilisateur principal est requis pour tous les comptes de service.

Un nom d’utilisateur principal (UPN) doit être défini pour tous les comptes de service dans MBAM. Si vous ne parvenez pas à créer un UPN pour un compte, un message d’erreur s’affiche lors du processus de configuration pour indiquer que l’utilisateur ou le groupe est introuvable dans Active Directory.

**Solution de contournement:** Ajoutez le nom d’utilisateur principal au compte de service.

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

### Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité de l’ordinateur BitLocker

Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur BitLocker dans le niveau d’intégration de Configuration Manager affiche toujours «inconnu» pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement de 128 bits. Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.

**Solution de contournement:** Définissez toujours une clé de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** l’objet de stratégie de groupe santé du chiffrement.

### Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration

Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.

**Solution de contournement:** Néant. La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.

### La configuration de la sécurité améliorée peut entraîner un affichage incorrect du message d’erreur

Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message d’erreur «Accès refusé» peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM. Par défaut, la fonction Échap est activée pour protéger le serveur en diminuant son exposition aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.

**Solution de contournement:** Si le message d’erreur «Accès refusé» s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier manuellement la valeur par défaut de votre image pour désactiver la configuration de la sécurité améliorée. Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel ESC n’est pas activé.

### Prise en charge de l’algorithme de chiffrement BitLocker XTS-AES
BitLocker a ajouté une prise en charge pour l’algorithme de chiffrement XTS-AES dans Windows 10, version 1511. Avec HF02, MBAM a ajouté une prise en charge du client pour cette option BitLocker et dans HF04, la prise en charge côté serveur a été ajoutée. Néanmoins, il existe une limite connue:

* Les clients doivent utiliser la même force de chiffrement pour le système d’exploitation et les volumes de données sur le même ordinateur.
Si les différents niveaux de cryptage sont utilisés, MBAM signale que l’ordinateur n’est **pas compatible**.

### Le portail libre-service ajoute automatiquement «-» sur une entrée d’ID clé
À partir de HF02, le portail libre-service MBAM ajoute automatiquement l’élément «-» à l’entrée d’ID clé.  
**Remarque:** Le serveur doit être reconfiguré pour que JavaScript prenne effet.

### Les rapports MBAM 2,5 SP1 ne fonctionnent pas correctement
La page rapports ne s’affiche pas correctement lorsque SSRS est hébergé sur SQL Server 2016 Edition. 
Par exemple, pour accéder au support technique, vous pouvez cliquer sur rapports (en surbrillance avec «x» en surbrillance) en vous appuyant davantage sur 4,0 les États (en surbrillance).

**Solution de contournement:** En examinant le code site. Master et remarqué que le mode X-UA a été dicté par IE8. Comme IE8 est passé en fin de vie, et le client utilise IE11. Mettez à jour le paramètre vers le code ci-dessous. Cela permet au site d’utiliser les technologies de rendu IE11

    <meta http-equiv="X-UA-Compatible" content="IE=Edge" />

Le paramètre initial est le suivant: 

    <meta http-equiv="X-UA-Compatible" content="IE=8" />


C’est la raison pour laquelle le problème ne s’est pas produit avec d’autres navigateurs, tels que Chrome, Firefox etc.



## Rubriques connexes


[À propos de MBAM2.5](about-mbam-25.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





