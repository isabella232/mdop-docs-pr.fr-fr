---
title: Notes de publication pour App-V5.0 SP2
description: Notes de publication pour App-V5.0 SP2
author: dansimp
ms.assetid: fe73139d-240c-4ed5-8e59-6ae76ee8e80c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5e885e67023d0e5c1e36aeb340933c64ae92610e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804896"
---
# Notes de publication pour App-V5.0 SP2


**Pour rechercher un problème spécifique dans ces notes de publication, appuyez sur CTRL + F.**

Lisez soigneusement ces notes de publication avant d’installer App-V 5,0 SP2.

Ces notes de publication contiennent des informations nécessaires pour l’installation de l’application-V 5,0 SP2. Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe des différences entre ces notes de publication et d’autres documents App-V 5,0, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## À propos de la documentation relative aux produits


Pour plus d’informations sur la documentation App-V 5,0, consultez la page d’accueil App-V 5,0 sur Microsoft TechNet.

## Fournir des commentaires


Vos commentaires vous intéressent sur App-V 5,0. Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .

**Remarques**  Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs dans la documentation et les versions de nos produits.

 

Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problèmes connus avec le correctif logiciel 4 pour la virtualisation des applications 5,0 SP2


### Les packages cessent de fonctionner après la désinstallation du package Hotfix 4 pour l’application virtualisation 5,0 SP2

Packages publiés lorsque le correctif logiciel 4 pour l’application virtualisation du SP2 pour applications 5,0 SP2 ne fonctionne plus lorsque le correctif logiciel 4 pour l’application virtualisation 5,0 SP2 est supprimé.

MOYENS

Si le dossier suivant existe, vous devez le supprimer:

**% LocalAppData%**  \\  **Microsoft**  \\  **AppV**  \\  **Client**  \\  **VFS**  \\  ** &lt; ID &gt; de package** de chaque package publié.

**Remarques**  Vous devez disposer de privilèges élevés pour supprimer ce dossier.

 

Pour utiliser un script, pour chaque compte d’utilisateur sur l’ordinateur et pour chaque ID de package publié après l’installation du package de correctif 4 pour l’application virtualisation de l’application 5,0 SP2:

`Rd /s /q “%systemdrive%\users\[UserName]\AppData\Local\Microsoft\AppV\Client\VFS\[Package ID]`

-   Le raccourci reste avec les sessions utilisateur même après la suppression du dossier du répertoire de la section précédente, de sorte que vous pouvez cliquer sur le raccourci pour exécuter de nouveau l’application. Il n’est pas nécessaire de republier l’application.

-   Ce problème survient pour l’utilisateur ayant publié des packages empaquetés et publiés globalement par exemple, Microsoft Centre. Le dossier doit être supprimé pour les deux types de packages.

-   Vous n’avez pas besoin de supprimer le dossier VFS dans les données d’application itinérantes (**% AppData%**). Seule la **% LocalAppData%** doit être supprimée.

### Emplacement du système de fichiers Microsoft Office incorrect

Les points d’intégration de Microsoft Office au mauvais emplacement du système de fichiers (Groove.exe message d’erreur).

MOYENS

Appliquez l’une des méthodes suivantes:

1.  Supprimez le raccourci dans le dossier démarrage après la mise à niveau.

2.  Modifiez le raccourci dans le dossier de démarrage à l’aide d’un script.

3.  Utilisez le fichier de configuration de déploiement pour spécifier le raccourci cible à la racine d’intégration.

### <a href="" id="-------------hotfix-package-4-for-application-virtualization-5-0-sp2-installer-can-take-a-long-time"></a> Le correctif logiciel 4 pour l’application virtualisation du programme d’installation de l’application 5,0 SP2 peut prendre un certain temps

Le correctif logiciel 4 pour l’application virtualisation du programme d’installation de l’application 5,0 SP2 peut prendre un certain temps en fonction du nombre de fichiers stockés dans le cache de package existant.

La mise à jour des descripteurs de sécurité du package associés lors de l’installation du correctif logiciel 4 pour l’installation d’application de la virtualisation du SP2 5,0 a un impact significatif sur le temps nécessaire à l’installation. Auparavant, l’installation était standard dans la durée. Toutefois, elle dépend désormais du nombre de fichiers que vous avez intermédiaires dans le cache du package.

Solution de contournement: aucune

### La désinstallation du package de correctif 4 pour l’application virtualisation du SP2 5,0 échoue si le package JIT-V est en cours d’utilisation

Si vous installez le package de correctif logiciel 4 pour la virtualisation des applications 5,0 SP2 et que vous essayez de désinstaller le correctif lorsque la virtualisation juste-à-V est utilisée, l’opération échoue si toutes les conditions suivantes sont remplies:

-   Vous avez installé l’application à l’aide d’un fichier Windows Installer (. msi), puis vous appliquez les mises à jour à l’aide d’un fichier de correctif Microsoft Installer (. msp).

-   Vous essayez de désinstaller une mise à jour à l’aide de l’option Ajout/suppression de programmes du panneau de configuration.

-   Un package prenant en charge la fonction JIT est en cours d’exécution sur l’ordinateur.

Solution de contournement: procédez comme suit:

1.  Ouvrez Windows PowerShell et exécutez les commandes suivantes:

    -   **Importation-module appvclient**

    -   **Get-AppvClientPackage | Stop-AppvClientPackage**

2.  Désinstaller la mise à jour à l’aide d’ajout/suppression de programmes.

## Problèmes connus avec App-V 5,0 SP2


### <a href="" id="bkmk-folderredirection"></a>La redirection de dossiers d’applications-V ne peut pas déplacer les fichiers de% AppData% vers% LocalAppData%

Lorsque% AppData% est un dossier réseau partagé que vous avez configuré pour la redirection de dossiers, les modifications que les utilisateurs finaux effectuent sur AppData (itinérance) peuvent être perdues lors du changement d’ordinateur ou de l’effacement de leur AppData Local lors de la déconnexion, puis de connexion. Cette erreur se produit, car la clé de Registre (AppDataTime), qui indique le dernier chargement connu, est hors de la synchronisation avec le AppData mis en cache local.

Solution de contournement: supprimez manuellement la clé de Registre suivante pour chaque package approprié lors de la connexion ou de la déconnexion d’un utilisateur final:

``` syntax
HKCU\Software\Microsoft\AppV\Client\Packages\<PACKAGE_GUID>\AppDataTime
```

La première fois que les utilisateurs finaux démarrent une application dans le package après s’être connecté, App-V force le téléchargement de l’enregistrement% AppData%, même si% LocalAppData% est déjà à jour.

### <a href="" id="-------------app-v-5-0-service-pack-2--app-v-5-0-sp2--does-not-include-a-new-version-of-the-app-v-server"></a> App-V 5,0 Service Pack 2 (App-V 5,0 SP2) n’inclut pas de nouvelle version du serveur App-V

App-V 5.0 SP2 n’inclut pas de nouvelle version du serveur App-V. Si vous déployez des clients App-V 5,0 SP2 exécutant Windows 8,1 dans votre environnement et que vous envisagez de gérer les clients à l’aide de l’infrastructure App-V, vous devez installer le [package Hotfix 2 pour Microsoft application virtualization 5,0 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=386634). (https://go.microsoft.com/fwlink/?LinkId=386634)

Si vous exécutez et gérez des clients App-V 5,0 SP2 en utilisant l’une des méthodes suivantes, aucune mise à jour de client n’est requise:

-   Mode autonome.

-   Configuration Manager.

-   Des ESD tiers.

Le client App-V 5,0 SP2 est entièrement compatible avec Windows 8,1

Solution de contournement: aucune.

## Informations de copyright des notes de publication


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft. Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.








## Rubriques connexes


[À propos d'App-V5.0 SP2](about-app-v-50-sp2.md)

 

 





