---
title: Résolution des problèmes liés à MED-V
description: Résolution des problèmes liés à MED-V
author: dansimp
ms.assetid: f43dae36-6485-4e06-9c66-0a646e27079d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38d13be699a92368ff258026acd8e0d5f0e28cd6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811411"
---
# Résolution des problèmes liés à MED-V


Cette section fournit des informations pour vous aider à résoudre les problèmes généraux liés à la virtualisation de bureau de Microsoft entreprise (MED-V).

## La modification de la résolution de l’hôte puis l’agrandissement de l’espace de travail MED-V entraîne l’affichage du bureau noir.


Lorsque vous travaillez en mode Bureau complet, si vous modifiez la résolution de l’hôte, puis agrandissez la fenêtre d’espace de travail MED-V, le Bureau s’affiche en noir et l’espace de travail MED-V ne répond pas.

### Solution

Arrêtez et démarrez l’espace de travail MED-V.

## Démarrage d’un espace de travail MED-V avec un adaptateur réseau désactivé, puis l’activation ultérieure de l’adaptateur ne restaure pas la connectivité réseau


Si vous configurez un espace de travail MED-V en mode pont et démarrez l’espace de travail MED-V alors qu’une carte réseau est désactivée, la connectivité réseau par le biais de cet adaptateur ne sera pas restaurée.

### Solution

Arrêtez et démarrez l’espace de travail MED-V.

## Une image ne peut être utilisée que par un seul utilisateur Windows par ordinateur


Une image d’espace de travail MED-V ne peut être utilisée que par l’utilisateur Windows qui a téléchargé ou importé l’image. Cet utilisateur est le seul à ne pas utiliser d’administrateurs disposant d’autorisations sur le dossier dans lequel se trouvent les images téléchargées.

### Solution

Changez manuellement la liste de contrôle d’accès (ACL) sur le magasin d’images.

## Lors de l’installation de MED-V à l’aide de Configuration Manager avec des droits d’utilisateur activés, la désinstallation échoue


Si MED-V est installé à l’aide de Microsoft System Center Configuration Manager et que le mode exécution du package a pour valeur utilisateurs, la désinstallation échoue avec un message d’erreur indiquant que seuls les utilisateurs administratifs peuvent désinstaller MED-V.

### Solution

Lors de la création d’un package de gestionnaire de configuration pour MED-V, définissez le mode d’exécution sur droits d’administration.

## Lors de l’installation de MED-V à l’aide d’un système de déploiement d’entreprise, où l’installation est configurée pour exécuter le client après l’installation, vous ne pouvez pas exécuter le client.


Si MED-V est installé à l’aide d’un système de déploiement d’entreprise et que le package d’installation est configuré pour exécuter un client MED-V après l’installation, une fois le client exécuté sous le compte système, vous ne pouvez pas voir que le client s’exécute (sauf dans la zone de notification) et que vous ne pouvez pas interagir avec ce dernier.

### Solution

Lors de l’installation de MED-V à l’aide d’un système de déploiement d’entreprise, utilisez le paramètre *Start \ _MEDV = 0* . msi.

## Échec du démarrage de l’image de test MED-V


Si une image de test MED-V ne démarre pas, elle ne sera jamais récupérée et tous les démarrages futurs échoueront avec un message d’erreur «Impossible de charger GINA».

### Solution

Supprimez l’image de test existante, puis recréez-la.

## Après avoir essayé de rejoindre un domaine avec des informations d’identification incorrectes, l’image ne fonctionne jamais dans le domaine.


S’il existe une erreur de configuration dans le bloc de construction de domaine de jointure, qui fait partie du script de configuration de l’ordinateur virtuel pour la première fois, l’espace de travail MED-V peut échouer lorsque vous essayez de rejoindre un domaine. Une fois l’erreur de configuration réparée, l’image incluse dans l’espace de travail MED-V ne peut pas rejoindre le domaine.

### Solution

Si l’image a été déployée, redistribuez l’image. Si l’image est une image de test, recréez l’image.

## MED-V ne prend pas en charge plusieurs moniteurs


MED-V ne prend pas en charge l’affichage des applications publiées sur plusieurs moniteurs. Les applications et les applications clientes publiées peuvent s’afficher sur l’écran incorrect, et parfois après la déconnexion d’un écran, MED-V tente d’envoyer l’écran à l’écran de sorte que le moniteur connecté reste vide.

### Solution

Déconnectez l’écran supplémentaire, puis redémarrez le client.

## Le démarrage de l’espace de travail MED-V peut échouer si l’hôte se bloque lors du démarrage d’un espace de travail MED-V


Si l’hôte se bloque pendant le processus de démarrage d’un espace de travail MED-V et qu’un message d’erreur s’affiche et indique «élément racine manquant», l’espace de travail MED-V peut ajouter des données à un fichier de configuration de machine virtuelle vide

### Solution

Remplacez le fichier VMC vide par un fichier VMC de l’image de base.

## Le clavier ne répond pas dans les fenêtres d’application publiées


Dans un espace de travail MED-V, si vous appuyez sur la touche du logo Windows lorsque l’application publiée est activée, le clavier ne répond plus dans les fenêtres d’application publiées.

### Solution

Appuyez sur la touche du logo Windows alors qu’une application publiée a le focus.

## Un espace de travail MED-V de domaine ne met pas à jour les informations d’identification de domaine


Lors de l’utilisation d’un espace de travail MED-V persistant dans un environnement de domaine, si vous modifiez le mot de passe de votre domaine, le client MED-V ne met pas à jour les informations d’identification du domaine d’espace de travail MED-V. Lorsqu’une application publiée tente d’accéder à une ressource réseau, vous recevez un message d’erreur vous informant que vos informations d’identification ont expiré.

### Solution

Redémarrez le système d’exploitation de l’espace de travail MED-V.

## Les fenêtres d’application publiées optimisées couvrent la barre des tâches hôte


Si vous agrandissez une fenêtre d’application publiée au mode plein écran, il est possible que la barre des tâches hôte s’affiche.

### Solution

Effectuez l'une des opérations suivantes:

Réduisez la fenêtre de l’application publiée pour accéder à la zone de notification, puis redémarrez l’espace de travail MED-V.

Réduisez la fenêtre de l’application publiée, puis restaurez la fenêtre à son état agrandi.

## L’ajout d’utilisateurs ou de groupes dans le gestionnaire de configuration du serveur MED-V ne fonctionne pas


Lorsque vous ajoutez des utilisateurs ou des groupes dans la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** , les utilisateurs ou groupes sélectionnés ne sont pas ajoutés à la liste de contrôle d’accès dans le gestionnaire de configuration de MED-V Server.

### Solution

Ajoutez des utilisateurs ou des groupes à l’aide de la boîte de dialogue **entrer un nom d’utilisateur ou de groupe** . Pour en savoir plus, voir [Comment installer et configurer le composant serveur MED-V](how-to-install-and-configure-the-med-v-server-component.md#bkmk-configuringpermissions).

## MED-V ne fonctionne pas sur les ordinateurs sur lesquels Windows Virtual PC pour Windows 7 est installé


MED-V nécessite Windows Virtual PC2007. Le PC virtuel pour Windows et Virtual PC2007 SP1 ne peuvent pas être installés sur le même ordinateur.

### Solution

Désinstaller Virtual PC pour plus d’applications avant d’installer Virtual PC2007 SP1 et MED-V.

## <a href="" id="med-v-does-not-support-virtual-pc-and-windows-xp-mode-images-"></a>MED-V ne prend pas en charge les images du mode PC virtuel et WindowsXP


MED-V 1.0 SP1 ne prend pas en charge les images créées par le PC virtuel Windows pour une application. Si une image virtuelle pour une utilisation est utilisée, le client ne peut pas démarrer.

### Solution

Créer des images MED-V en utilisant Virtual PC2007 SP1.

## Le pare-feu Windows bloque l’activité du réseau PC2007 SP1 virtuel


Par défaut, le pare-feu Windows bloque l’activité du réseau PC2007 SP1 virtuel et, lorsque le service SP1 virtuel PC2007 s’exécute sur l’ordinateur client, il existe un message de pare-feu qui bloque la séquence de démarrage et l’accès au réseau.

### Solution

Mettez à jour l’exception de pare-feu à l’aide de la stratégie de groupe avant MED-V, qui est utilisée par l’utilisateur final.

## Lors de la mise à niveau du client, un message d’erreur s’affiche


Lors de la mise à niveau du client de MED-V 1.0 vers MED-V 1.0 SP1, un message peut apparaître indiquant qu’aucun espace de travail MED-V n’est défini.

### Solution

Fermez le client et redémarrez-le.

## Rubriques connexes


[Notes de publication pour MED-V1.0](med-v-10-release-notesmedv-10.md)

[Notes de publication pour MED-V1.0 SP1 et SP2](med-v-10-sp1-and-sp2-release-notesmedv-10-sp1.md)

 

 





