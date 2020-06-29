---
title: Nouveautés de MED-V2.0
description: Nouveautés de MED-V2.0
author: dansimp
ms.assetid: 53b10bff-2b6f-463b-bdc2-5edc56526792
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 78dba25fec7ae2bb41da00902b59dcd15030f2b6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810115"
---
# Nouveautés de MED-V2.0


Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 a évolué la prise en charge de la compatibilité des applications pour Windows 7 et des fonctionnalités supprimées qui ne sont pas requises pour ce scénario. Par exemple, des fonctionnalités telles que le chiffrement de l’espace de travail MED-V et du serveur centralisé MED-V et de l’espace de travail MED-V ont été supprimés.

## Modifications apportées aux fonctionnalités standard


Cette section décrit les principaux domaines dans lesquels la fonctionnalité 2,0 MED-V a changé.

### Création d’espace de travail MED-V

Le disque dur virtuel utilisé pour l’espace de travail MED-V est désormais créé dans l’ordinateur virtuel Windows. Les méthodes qui sont utilisées pour créer l’espace de travail MED-V incluent l’installation de Windows XP SP3, la mise à jour du système d’exploitation et la préparation de leur gestion via l’infrastructure de gestion des logiciels.

La fonctionnalité gestion hors connexion et transfert de découpage a été supprimée, en plus des fonctionnalités de chiffrement et de compression d’espace de travail MED-V. Lorsque vous créez un espace de travail MED-V, un administrateur doit préparer et configurer les applications et outils de gestion appropriés dans l’image au lieu d’utiliser l’outil de préparation de l’ordinateur virtuel fourni dans MED-V 1,0.

L’exécution de Sysprep sur l’image MED-V est désormais obligatoire et validée lors de l’empaquetage de l’espace de travail MED-V. Le module de création de package de l’espace de travail MED-V fournit une interface utilisateur graphique qui reguide l’administrateur dans le processus de création de packages. La console de MED-V 1,0 a été retirée en même temps que les fonctionnalités de gestion des images, de gestion des profils d’espace de travail MED-V et de la nécessité de mettre en place et de chiffrer les espaces de travail MED-V.

### Déploiement d’espace de travail MED-V

Pour le déploiement d’un espace de travail MED-V, un administrateur peut désormais bénéficier de ses outils de distribution de logiciels électroniques. La méthode de collecte client disponible dans MED-V 1,0 a été supprimée et l’espace de travail MED-V est désormais remis à l’aide de méthodes en dehors de MED-V. Les administrateurs peuvent traiter les espaces de travail MED-V comme tout autre package d’application et pouvoir planifier des déploiements et des installations de MED-V en utilisant leurs outils et processus existants. Les installations MED-V peuvent être déployées en silence et peuvent facilement être gérées au sein d’une infrastructure de distribution de logiciels existante.

### Gestion de l’espace de travail MED-V

L’espace de travail MED-V dans MED-V 2,0 est basé sur un disque dur virtuel Windows Virtual PC. MED-V a étendu les fonctionnalités fournies par le PC virtuel Windows en améliorant l’interface sans nécessiter un chiffrement ou un outil spécial pour accéder à l’espace de travail MED-V.

Après le déploiement de MED-V sur une station de travail, l’espace de travail MED-V peut être ouvert en mode plein écran à l’aide de l’ordinateur virtuel Windows. Cette nouvelle fonctionnalité supprimait la configuration requise pour les stratégies qui ont défini une préférence pour les modes plein écran, et supprimée la nécessité de forcer l’affichage en plein écran des diagnostics et de la résolution des problèmes.

La publication d’applications sur l’espace de travail MED-V n’est plus effectuée avec les profils et en entrant manuellement le chemin d’accès aux applications. Au lieu de cela, il se produit automatiquement lorsque des applications sont installées sur l’invité. Le référentiel d’image central qui inclut les versions des images fournies par le biais du transfert de découpage est supprimé. En revanche, la gestion des applications et des mises à jour de MED-v permet aux administrateurs de gérer l’espace de travail MED-V de façon à ce qu’ils soient distribués sans la complexité d’une infrastructure MED-V dédiée.

## Modifications apportées aux fonctionnalités de MED-V


Plusieurs domaines clés de MED-V 2,0 reflètent les améliorations ou les ajouts apportées aux fonctionnalités suivantes.

### Création d’espace de travail MED-V

Les espaces de travail MED-V doivent être créés à l’aide du PC virtuel Windows. Les images 2007 de PC virtuelles doivent être déplacées. L’outil virtual machine PReP n’est pas inclus dans MED-V 2,0 et les administrateurs doivent configurer, mettre à jour et optimiser leurs images conformément au fichier d’aide de MED-V 2,0. L’exécution de Sysprep sur l’image MED-V est une étape requise qui doit être effectuée avant l’empaquetage.

### Package d’espace de travail MED-V

Windows PowerShell est la base du gestionnaire de package d’espace de travail MED-V. Cette fonctionnalité remplace certaines fonctions et fonctionnalités de la console et les fonctions centralisées de MED-V. Le module de création de package de l’espace de travail MED-V compresse simplement le disque dur virtuel avec les paramètres et l’image appropriés pour pouvoir être déployé facilement par les administrateurs. Les fonctionnalités avancées sont fournies à l’aide de Windows PowerShell.

### Distribution d’espace de travail MED-V

L’infrastructure de serveur dédiée n’est plus nécessaire pour MED-V 2,0 et la méthode pull du client pour le déploiement d’espaces de travail MED-V a été supprimée. Les espaces de travail MED-V sont désormais déployés à l’aide de votre infrastructure de distribution de logiciels électroniques et peuvent être stockés sur des partages communs qui sont utilisés pour d’autres packages d’installation.

### Configuration pour la première fois

Le processus de configuration pour la première fois est désormais intégré à la Convention d’imagerie standard de Sysprep. Le processus de configuration de l’espace de travail MED-V peut appliquer de manière dynamique des paramètres spécifiés dans le gestionnaire de package de l’espace de travail MED-V à l’image pendant qu’elle lance le mini-programme d’installation. L’outil de script de la console a été supprimé et le processus de configuration pour la première fois est désormais basé sur les options configurées dans le gestionnaire de package MED-V de l’administrateur.

### Publication d’applications

Les administrateurs peuvent installer des applications sur l’image MED-V avant de procéder au conditionnement, après le déploiement de l’espace de travail MED-V ou à l’aide d’une combinaison des deux. MED-V n’examine plus la stratégie d’espace de travail MED-V pour publier des applications, mais désigne plutôt ce qui est réellement installé sur l’invité. À mesure que des applications sont installées sur l’invité, celles-ci sont automatiquement détectées et publiées dans le menu de **démarrage** de l’hôte et sont prêtes à être démarrées par l’utilisateur final.

### Redirection d’URL

MED-V 2,0 fournit une redirection d’une adresse Web d’hôte à invité transparente en fonction des stratégies configurées et gérées par l’administrateur. Dès lors que l’URL est redirigée vers le navigateur invité, l’utilisation par défaut consiste à limiter l’utilisateur à ce site Redirigé. Cela permet de réduire les activités de navigation que l’utilisateur peut effectuer et qui ne sont pas prévues par l’administrateur. La redirection de navigateur invité à hôte a été supprimée.

### Résolution des problèmes

MED-V tire désormais parti des processus standard pour la résolution des problèmes. Dans la mesure où l’espace de travail MED-V n’est plus chiffré, il est possible de l’ouvrir en mode plein écran dans la console Windows Virtual PC, où il peut être affiché et utilisé comme une station de travail standard. De plus, les journaux ne sont plus chiffrés localement et journalisés de manière centralisée. MED-V utilise désormais les journaux des événements locaux, et le niveau de journalisation de la sortie, de l’information aux niveaux de débogage, peut être facilement configuré. Enfin, un kit de tâches de dépannage est désormais fourni pour permettre aux administrateurs et au personnel d’assistance d’avoir un affichage graphique et agrégé de toutes les options de résolution des problèmes, et de sélectionner facilement les activités les plus adaptées à leurs besoins.

MED-V n’est plus exécuté en tant que service système. Au lieu de cela, il s’exécute comme processus appartenant à l’utilisateur et s’exécute uniquement lorsque l’utilisateur est connecté.Les fonctionnalités qui étaient auparavant fournies par le service possédé par le système sont désormais fournies dans les processus côté utilisateur.

## Rubriques connexes


[Déploiement de MED-V](deployment-of-med-v.md)

[Opérations de MED-V](operations-for-med-v.md)

 

 





