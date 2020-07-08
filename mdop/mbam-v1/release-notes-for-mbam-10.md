---
title: Notes de publication de MBAM1.0
description: Notes de publication de MBAM1.0
author: dansimp
ms.assetid: d82fddde-c360-48ef-86a0-d9b5fe066861
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 705fd1b936da1454081dd14a7f075f642fc4a405
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811508"
---
# Notes de publication de MBAM1.0


**Pour rechercher un problème spécifique dans ces notes de publication, appuyez sur CTRL + F.**

Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker Administration and Monitoring (MBAM).

Ces notes de publication contiennent des informations requises pour l’installation réussie de MBAM. Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents de MBAM, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## À propos de la documentation relative aux produits


Pour plus d’informations sur la documentation MBAM, voir la page d’accueil MBAM sur Microsoft TechNet.

Pour obtenir la version téléchargeable de la documentation MBAM, voir <https://go.microsoft.com/fwlink/p/?LinkId=225356> sur le centre de téléchargement Microsoft.

## Fournir des commentaires


Vos commentaires vous intéressent sur MBAM. Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .

**Remarques**  Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs dans la documentation et les versions de nos produits.

 

Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problèmes connus avec MBAM 1,0


Cette section contient des notes de publication relatives aux problèmes connus liés à la configuration et à l’installation d’MBAM.

### <a href="" id="if-you-select-the--use-a-certificate-to-encrypt-the-network-communication--option-during-setup--existing-database-connections-and-dependent-applications-can-stop-functioning-"></a>Si vous sélectionnez l’option «utiliser un certificat pour chiffrer les communications réseau» lors de l’installation, les connexions de base de données et les applications dépendantes existantes peuvent cesser de fonctionner

Vous pouvez configurer MBAM pour la **communication réseau chiffrée** après l’installation de la base de données de récupération et du matériel ou des fonctionnalités de la base de données d’état de conformité. Si vous choisissez de configurer MBAM pour la communication réseau chiffrée, MBAM programme d’installation configure l’instance du moteur de base de données SQL Server de façon à utiliser SSL (Secure Sockets Layer) pour la communication entre la base de données en vigueur et les fonctionnalités du serveur d’administration et de surveillance ainsi que les fonctionnalités du serveur rapport de conformité et d’audit.

-   Si l’instance du moteur de base de données SQL Server n’est pas déjà configurée pour utiliser SSL, le programme d’installation de MBAM la configure pour le faire. Cela peut empêcher les applications qui essaient d’utiliser des bases de données non MBAM sur l’instance du moteur de base de données SQL Server de communiquer avec leurs bases de données.

-   Si l’instance du moteur de base de données SQL Server est déjà configurée pour utiliser SSL, il est configuré de manière à utiliser le certificat que l’utilisateur a sélectionné lors de l’installation. Si ce certificat est différent de celui déjà utilisé, il peut empêcher l’exécution des applications qui utilisent les bases de données SQL Server sur l’instance du moteur de base de données SQL Server.

**Solution de contournement:** Néant

### Échec de la configuration de MBAM lors de l’installation lorsque vous utilisez un compte d’administrateur local

Échec de l’installation d’MBAM lorsque vous utilisez un compte d’administrateur local. Le fichier journal contient les informations suivantes:

``` syntax
Locating group 'MBAM Report Users'
Adding <GUID>' to group 'MBAM Report Users'
Locating group 'MBAM Recovery and Hardware DB Access'
Adding 'S-1-5-20' to group 'MBAM Recovery and Hardware DB Access'
Exception: A new member could not be added to a local group because the member has the wrong account type.
 
  StackTrace:    at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SDSUtils.ApplyChangesToDirectory(Principal p, StoreCtx storeCtx, GroupMembershipUpdater updateGroupMembership, NetCred credentials, AuthenticationTypes authTypes)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.Update(Principal p)
   at Microsoft.Windows.Mdop.BitlockerManagement.Setup.Groups.CreateGroupsDeferred(Session session)
  InnerException:Exception: A new member could not be added to a local group because the member has the wrong account type.
 
    InnerException:StackTrace:    at System.DirectoryServices.AccountManagement.UnsafeNativeMethods.IADsGroup.Add(String bstrNewItem)
   at System.DirectoryServices.AccountManagement.SAMStoreCtx.UpdateGroupMembership(Principal group, DirectoryEntry de, NetCred credentials, AuthenticationTypes authTypes)
CustomAction MbamCreateGroupsDeferred returned actual error code 1603 (note this may not be 100% accurate if translation happened inside sandbox)
Action ended 11:41:29: InstallExecute. Return value 3.
```

**Solution de contournement:** Utilisez un compte de domaine avec des informations d’identification d’administrateur sur l’ordinateur serveur lors de l’installation d’MBAM.

### MBAM-XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX

Lorsque vous installez la base de données de récupération et de matériel ou la base de données de statut de conformité, vous pouvez utiliser le programme d’installation pour configurer MBAM en sélectionnant **communication réseau chiffrée**. Si vous décidez de ne pas chiffrer la communication réseau, le programme d’installation de MBAM reconfigure l’instance du moteur de base de données SQL Server de sorte qu’elle n’utilise pas SSL.

-   Si l’instance du moteur de base de données SQL Server est déjà configurée pour utiliser SSL, le programme d’installation d’MBAM désactive SSL sur l’instance du moteur de base de données SQL Server. Cette opération modifie la sécurité des communications entre les applications qui utilisent des bases de données qui ne sont pas liées à des bases de données MBAM sur l’instance du moteur de base de données SQL Server.

**Solution de contournement:** Néant

### Conditions préalables manquantes pour les scripts de gestion d’Internet Information Services (IIS) et la fonctionnalité serveur Web outils

La configuration de MBAM dépend des scripts de gestion IIS et de la fonctionnalité serveur Web outils, mais elle n’est pas obligatoire. Le programme d’installation du serveur vous permet d’installer MBAM lorsque cette fonctionnalité n’est pas disponible. Toutefois, cela a pour effet que le rédacteur du service de sauvegarde MBAM le démarrage puis s’arrête, car il ne parvient pas à trouver les informations WMI (Windows Management Instrumentation) et les fournisseurs de services Internet (IIS). Aucun message d’erreur ne s’affiche pour cette condition, sauf dans le journal des événements. L’installation d’MBAM sans les scripts et les outils de gestion IIS entraîne l’exécution des opérations de sauvegarde pour MBAM.

**Solution de contournement:** Assurez-vous que les scripts de gestion IIS et la fonctionnalité serveur Web Tools sont installés avant de lancer la configuration de MBAM.

### <a href="" id="mbam-setup-stops-responding-during-the--installing-selected-features--phase-when-setup-is-configured-to-use-a-certificate"></a>Le programme d’installation d’MBAM cesse de répondre lors de la phase d’installation des fonctionnalités sélectionnées lorsque le programme d’installation est configuré pour utiliser un certificat

Le programme d’installation d’MBAM cesse de répondre lors de l' **installation de fonctionnalités sélectionnées** du programme d’installation. Cette situation se produit lors de l’installation de la base de données de récupération et de matériel ou de la base de données d’état de conformité, après avoir sélectionné l’option **utiliser un certificat pour chiffrer les communications réseau** . Par ailleurs, la configuration d’MBAM cesse de répondre si l’instance du moteur de base de données SQL Server ne peut pas accéder au certificat qui a été spécifié lors de l’installation.

**Solution de contournement:** Mettez à jour les autorisations sur le certificat, afin que le service Windows pour l’instance correspondante du moteur de base de données SQL Server puisse accéder au certificat. Vous pouvez également modifier le compte sous lequel l’instance du moteur de base de données SQL Server s’exécute, afin que le moteur de base de données utilise le certificat. Pour déterminer les autorisations du certificat, tapez la commande suivante à l’invite de commandes: **certutil-v-Store My**

### La configuration de MBAM est interrompue lors de l’installation de SQL Server Reporting Services

Lors de l’installation d’MBAM, lorsque vous sélectionnez une instance de SQL Server Reporting Services (SSRS) et qu’elle n’est pas disponible, ou qu’elle est configurée de manière incorrecte, le programme d’installation de MBAM risque de suspendre pendant une minute tout en essayant de communiquer avec l’instance SSRS.

**Solution de contournement:** Attendez au moins une minute pour la reprise de l’installation d’MBAM alors que le programme d’installation tente de contacter l’instance de SSRS.

### <a href="" id="administration-and-monitoring-server-does-not-run-after-setup-"></a>Le serveur d’administration et de surveillance ne s’exécute pas après l’installation

Après l’installation réussie de la fonctionnalité d’administration et de surveillance du serveur par MBAM, MBAM affiche des messages d’erreur lorsque vous essayez d’accéder au site Web de l’administrateur MBAM. Ce problème survient pour l’une des raisons suivantes:

-   Une ou plusieurs conditions préalables sur le serveur d’administration et de surveillance ont été supprimées après l’installation d’MBAM.

-   Une ou plusieurs conditions préalables ont été installées sur le serveur et ont été supprimées après l’exécution de la configuration de MBAM.

**Solution de contournement:** Passez en revue la documentation MBAM et vérifiez que tous les éléments requis MBAM sont installés.

### Un clic sur les liens de documentation lors de l’installation entraîne l’exécution d’une erreur d’application après la fin de l’installation

Lorsque vous cliquez sur un lien de la documentation lors de l’installation, puis fermez le programme d’installation en cliquant sur **Annuler** ou **Terminer** une fois l’installation terminée, un message d’erreur d’application s’affiche. Le problème est dû à une erreur de violation d’accès dans le planificateur de tâches Windows.

**Solution de contournement:** Néant. Vous pouvez ignorer cette erreur.

### Échec de l’installation d’MBAM ne supprime pas les nouvelles bases de données

En cas d’échec de la configuration de MBAM, il est possible que le programme d’installation ne supprime pas les bases de données nouvellement créées. Cela peut provoquer des échecs lors des installations suivantes.

**Solution de contournement:** Sélectionnez un autre nom pour l’instance de base de données au cours de l’installation suivante.

### Le programme d’installation d’MBAM ne reconnaît pas les certificats valides de cluster d’équilibrage de charge réseau

Lors de l’installation du serveur d’administration et de surveillance d’MBAM, l’option de chiffrement réseau sélectionnée ne correspond pas au certificat valide. Il est reconnu comme valide lorsque le certificat de communication avec la base de données est installé, mais qu’il est rejeté pour la communication par le cluster d’équilibrage de charge.

**Solution de contournement:** Vérifiez que la liste de révocation de certificats associée au certificat est accessible, ou utilisez un certificat qui ne nécessite pas une validation à l’aide de la liste de révocation.

## Informations de copyright des notes de publication


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft. Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.



## Rubriques connexes


[À propos de MBAM1.0](about-mbam-10.md)

 

 





