---
title: Notes de publication pour App-V5.1
description: Notes de publication pour App-V5.1
author: dansimp
ms.assetid: 62c5be3b-0a46-4512-93ed-97c23184f343
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 09/26/2016
ms.openlocfilehash: 7437a16bc10b21bb15b0f8307c2711177e78cb72
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804879"
---
# Notes de publication pour App-V5.1


Vous trouverez ci-après des problèmes connus dans Microsoft Application Virtualization (App-V) 5,1.

## Une erreur se produit lors de l’actualisation de la publication entre le serveur de gestion App-V 5,0 SP3 et le client App-V 5,1 sur Windows 10


Une erreur est générée lors de l’actualisation de la publication lors de la synchronisation des packages du serveur de gestion App-V 5,0 SP3 vers un client App-V 5,1 sur Windows 10. Cette erreur se produit car le serveur App-V 5,0 SP3 ne comprend pas le système d’exploitation Windows 10 qui est spécifié dans l’URL de publication. Ce problème a été résolu pour le serveur de publication 5,1 App-V, mais n’est pas transféré vers des versions de App-V 5,0 SP3 ou antérieure.

**Solution de contournement**: mettez à niveau le serveur de gestion App-v 5,0 vers le serveur de gestion App-v 5,1 pour les clients Windows 10.

## Les configurations personnalisées ne sont pas appliquées pour les packages qui seront publiés globalement s’ils sont définis à l’aide du serveur App-V 5,1


Si vous affectez un package à un groupe d’annonces qui contient des comptes d’ordinateur et appliquez une configuration personnalisée à ce groupe à l’aide du serveur App-V, la configuration personnalisée ne sera pas appliquée à ces machines. Le client App-V 5,1 publie des packages attribués à un compte d’ordinateur de manière globale. Toutefois, il stocke les fichiers de configuration personnalisés par utilisateur dans le profil de chaque utilisateur. Les packages publiés globalement n’ont pas accès à cette configuration personnalisée.

**Solution de contournement**: effectuez l’une des opérations suivantes:

-   Attribuez le package à des groupes contenant uniquement des comptes d’utilisateurs. Cela permet de s’assurer que la configuration personnalisée du package sera stockée dans le profil de chaque utilisateur et sera appliquée correctement.

-   Créez un fichier de configuration de déploiement personnalisé et appliquez-le au package sur le client à l’aide de l’applet de demande Add-AppvClientPackage avec le paramètre – DynamicDeploymentConfiguration. Pour plus d’informations, voir [à propos de la configuration dynamique de App-V 5,1](about-app-v-51-dynamic-configuration.md) .

-   Créez un package avec la configuration personnalisée à l’aide du séquenceur App-V 5,1.

## Fichiers du serveur non supprimés après l’installation de New App-V 5,1 Server


Si vous désinstallez le serveur App-V 5,0 SP1, puis installez le serveur App-V 5,1, l’installation échoue, la mauvaise version du serveur de gestion est installée et un message d’erreur est renvoyé. Le problème se produit parce que les fichiers serveur ne sont pas supprimés lorsque vous désinstallez App-V 5,0 SP1, de sorte que le processus d’installation effectue une mise à niveau au lieu d’une nouvelle installation.

**Solution de contournement**: supprimez cette clé de Registre avant de commencer à installer App-V 5,1:

Sous HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\Windows\\CurrentVersion\\Uninstall, recherchez et supprimez la clé du GUID d’installation contenant la valeur DWORD «DisplayName» avec les données de valeur «Microsoft Application Virtualization (App-V) Server». Il s’agit de la seule touche qui doit être supprimée.

## Les associations de types de fichiers ajoutées manuellement ne sont pas enregistrées correctement


Les associations de types de fichiers ajoutées à un package d’application manuellement à l’aide de l’onglet raccourcis et FTAs à la fin de l’Assistant Mise à niveau de l’application ne sont pas enregistrées correctement. Ils ne seront pas disponibles pour le client App-V ou pour le Sequencer lors de la mise à jour du package enregistré.

**Solution de contournement**: pour ajouter une association de type de fichier, ouvrez le package à des fins de modification, puis exécutez l’Assistant Mise à jour. Lors de l’étape d’installation, ajoutez la nouvelle association de type de fichier par le biais du système d’exploitation. Le Sequencer détecte la nouvelle association dans le registre système et l’ajoute au registre virtuel du package, là où il sera disponible pour le client.

## Lorsque vous diffusez des packages en continu en mode de stockage de contenu partagé dans un client géré par AppLocker, des données supplémentaires sont écrites sur le disque local.


Pour réduire la quantité de données écrites sur le disque local du client, vous pouvez activer le mode SCS sur le client App-V 5,1 pour diffuser le contenu d’un package à la demande. Toutefois, si AppLocker gère une application au sein du package, il est possible que certaines données soient écrites sur le disque local du client qui ne serait pas écrit autrement.

**Solution de contournement**: aucune

## Dans la boîte de dialogue Ajouter un package de la console de gestion, le bouton Parcourir n’est pas disponible lorsque vous utilisez Chrome ou Firefox


Sur la page packages de la console de gestion, si vous cliquez sur **Ajouter ou mettre à niveau** dans le coin inférieur droit, la boîte de dialogue **Ajouter un package** s’affiche. Si vous accédez à la console de gestion en utilisant chrome ou Firefox comme navigateur, vous ne pourrez pas accéder à l’emplacement du package.

**Solution de contournement**: tapez ou copiez-collez le chemin d’accès du package dans le champ d’entrée **Ajouter le package** . Si la console de gestion a accès à ce chemin d’accès, vous serez en mesure d’ajouter le package. Si le package se trouve sur un partage réseau, vous pouvez accéder à l’emplacement à l’aide de l’Explorateur de fichiers en procédant comme suit:

1.  En appuyant sur **MAJ**, cliquez avec le bouton droit sur le fichier de package.

2.  Sélectionnez **Copy As Path**

3.  Collez le chemin d’accès dans le champ de saisie de la boîte de dialogue **Ajouter un package** .

## <a href="" id="upgrading-app-v-management-server-to-5-1-sometimes-fails-with-the-message--a-database-error-occurred-"></a>La mise à niveau d’App-V Management Server vers 5,1 échoue parfois avec le message «une erreur de base de données s’est produite»


Si vous installez le serveur de gestion App-V 5,0 SP1 et que vous essayez d’effectuer une mise à niveau vers la version Server App-V 5,1 lorsque plusieurs groupes de connexion sont configurés et activés, l’erreur suivante s’affiche: «une erreur de base de données s’est produite. Raison: «nom de colonne non valide» «PackageOptional». Nom de colonne non valide «VersionOptional».

**Solution**: exécutez la commande suivante sur votre base de données SQL:

`ALTER TABLE AppVManagement.dbo.PackageGroupMembers ADD PackageOptional bit NOT NULL DEFAULT 0, VersionOptional bit NOT NULL DEFAULT 0`

où «AppVManagement» est le nom de la base de données.

## Les utilisateurs ne peuvent pas ouvrir un package dans un groupe de connexions publié par un utilisateur si vous ajoutez ou supprimez un package facultatif


Dans les environnements qui exécutent le client RDS ou qui ont plusieurs utilisateurs simultanés par ordinateur, les utilisateurs connectés ne peuvent pas ouvrir les applications dans les packages d’un groupe de connexion publié par l’utilisateur si un package facultatif est ajouté ou supprimé du groupe de connexion.

**Solution**: Demandez aux utilisateurs de se déconnecter, puis de vous reconnecter.

## Le message d’erreur s’affiche par erreur lorsque le groupe de connexions est uniquement publié pour l’utilisateur


Lorsque vous exécutez l’outil de réparation-AppvClientConnectionGroup, l’erreur suivante s’affiche, même lorsque le groupe de connexions est publié uniquement à l’utilisateur: «erreur d’intégration d’application interne-V: package non intégré pour l’utilisateur. Vérifiez que le package est ajouté à l’ordinateur et publié sur l’utilisateur.»

**Solution de contournement**: effectuez l’une des opérations suivantes:

-   Publiez tous les packages d’un groupe de connexion.

    Ce problème survient lorsque le groupe de connexion en cours de réparation comporte des packages qui sont manquants ou ne sont pas disponibles pour l’utilisateur (autrement dit, non publié globalement ou pour l’utilisateur). Toutefois, la réparation fonctionnera si tous les packages du groupe de connexions sont disponibles, vérifiez donc que tous les packages sont publiés.

-   Réparez les packages individuellement à l’aide de la commande réparer-AppvClientPackage plutôt que de la commande réparer-AppvClientConnectionGroup.

    Déterminez les packages disponibles pour les utilisateurs, puis exécutez la commande réparer-AppvClientPackage une fois pour chaque package. Utilisez les cmdlets PowerShell pour effectuer les opérations suivantes:

    1.  Obtenez tous les packages d’un groupe de connexion.

    2.  Vérifiez si chaque package est actuellement publié.

    3.  Si le package est actuellement publié, exécutez réparation-AppvClientPackage sur ce package.

## Les icônes ne s’affichent pas correctement dans le Sequencer


Les icônes de l’onglet raccourcis et des types de fichiers ne s’affichent pas correctement lors de la modification d’un package dans le Sequencer App-V. Ce problème survient lorsque la taille des icônes n’est pas 16x16 ou 32x32.

**Solution**: Utilisez uniquement des icônes de 16x16 ou 32x32.

## Le script InsertVersionInfo. SQL n’est plus requis pour la base de données de gestion


Le script InsertVersionInfo. SQL n’est pas requis pour les versions de la base de données de gestion App-V ultérieure à l’application-V 5,0 SP3.

Le script Permissions. SQL doit être mis à jour en suivant l' **étape 2** de [l’article 3031340](https://support.microsoft.com/kb/3031340)de la base de connaissances.

**Important** 
 L' **étape 1** n’est pas requise pour les versions de App-v ultérieures à l’application-v 5,0 SP3.

 

## Microsoft Visual Studio 2012 non pris en charge


App-V 5,1 ne prend pas en charge Visual Studio 2012.

**Solution de contournement**: aucune

## Restrictions de nom de fichier d’application pour le Sequencer App-V 5. x


Le Sequencer App-V 5. x ne peut pas séquencer des applications avec des noms de fichier correspondant à «CO_ &lt; x &gt; », où x est une valeur numérique. Le 0x8007139F d’erreur est généré.

**Solution**: utilisez un autre nom de fichier

## Erreur «fichier introuvable» intermittente lors du montage d’un package


Occasionnellement lors du montage d’un package, une erreur «fichier introuvable» (0x80070002) est générée. En règle générale, ce problème se produit lorsqu’un dossier d’un package App-V contient un grand nombre de fichiers (c’est-à-dire 20 Ko ou plus). Cela peut entraîner un délai de diffusion plus long que prévu et un délai d’expiration qui génère l’erreur «fichier introuvable».

**Solution de contournement**: à partir de HF06, une nouvelle clé de registre a été ajoutée pour permettre l’extension de ce délai.

<table>
<colgroup>
<col width="20%" />
<col width="80%" />
</colgroup>
<tbody>
<tr>
<td align="left">Chemin d'accès</td>
<td align="left">HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\AppV\Client\Streaming</td>
</tr>
<tr>
<td align="left">Paramètre</td>
<td align="left">StreamResponseWaitTimeout</td>
</tr>
<tr>
<td align="left">Smalldatetime</td>
<td align="left">DWORD</td>
</tr>
<tr>
<td align="left">UnitsIn</td>
<td align="left">Lesquelles</td>
</tr>
<tr>
<td align="left">Par défaut</td>
<td align="left">n°5<br />
<strong>Remarque </strong> : cette valeur est la valeur par défaut si la clé de Registre n’est pas définie ou si une valeur &lt; = 5 est spécifiée.
</td>
</tr>
</tbody>
</table>






## Rubriques connexes


[À propos d'App-V5.1](about-app-v-51.md)

 

 





