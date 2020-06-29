---
title: Planification du déploiement d'Application Virtualization Client
description: Planification du déploiement d'Application Virtualization Client
author: dansimp
ms.assetid: a352f80f-f0f9-4fbf-ac10-24c510b2d6be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6c9fc4f29020af83a8606827015947e78761f4d7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806513"
---
# Planification du déploiement d'Application Virtualization Client


Une fois que vous avez décidé du mode de publication et de déploiement des packages d’application virtuels sur les ordinateurs des utilisateurs finaux, vous devez planifier le déploiement du logiciel client de virtualisation d’applications.

Le client de virtualisation des applications est le composant qui exécute réellement les applications virtuelles. Le client de virtualisation des applications permet aux utilisateurs d’interagir avec des icônes et de double-cliquer sur les types de fichiers pour démarrer une application virtuelle. Il gère également la diffusion en continu du contenu de l’application à partir d’un serveur en flux continu et la cache avant de démarrer l’application. Le contenu de l’application est structuré de telle sorte que tout le contenu nécessaire au démarrage de l’application et le traitement de l’interaction utilisateur initiale soient transmis d’abord à l’ordinateur de l’utilisateur final. Il existe deux types différents de logiciels de client de virtualisation d’application: le client de virtualisation d’application pour les services Bureau à distance (anciennement services Terminal Server), qui est utilisé sur les systèmes serveur du serveur hôte de bureau RDSession, et le client de bureau de virtualisation des applications, qui est utilisé pour tous les autres ordinateurs.

Le client de virtualisation des applications doit être configuré au moment de l’installation, soit dans la console de gestion de l’application, soit via la ligne de commande du programme d’installation, avec un certain nombre de paramètres importants, dont les suivantes:

-   Emplacements des icônes pour toutes les applications.

-   Emplacement du fichier OSD qui contient les informations de définition du package.

-   Source de contenu de l’application.

-   Protocole de communication à utiliser pour récupérer les éléments précédents.

-   La taille de cache et la méthode de gestion de la taille de cache à utiliser.

Pour promouvoir le déploiement du logiciel client de virtualisation des applications lors de l’utilisation d’une solution de distribution de logiciel électronique (ESD), les paramètres précédents doivent être définis à l’avance. C’est particulièrement important lorsque vous disposez d’ordinateurs dans différents bureaux et que leurs clients doivent être configurés de manière à utiliser des emplacements sources différents.

**Remarque**  
-   L’emplacement de l’icône et les valeurs du fichier OSD sont un facteur important à prendre en considération lors du choix de votre méthode de publication, que vous utilisiez Windows Installer ou SFTMIME. Le paramètre de la source de contenu de l’application est défini par votre choix de méthode de streaming.

-   Pour vous assurer que le cache dispose de suffisamment d’espace alloué pour tous les packages qui peuvent être déployés, utilisez le paramètre **utiliser le seuil d’espace disque libre** lorsque vous configurez le client de manière à ce que le cache puisse augmenter selon les besoins. Par ailleurs, vous pouvez déterminer à l’avance la quantité d’espace disque nécessaire pour le cache de l’application V et au moment de l’installation, définir la taille de cache en conséquence. Pour plus d’informations sur la fonctionnalité de gestion de l’espace dans le cache, voir **comment utiliser la fonctionnalité de gestion de l’espace** dans le cache du Guide des opérations de Microsoft Application Virtualization (App-V).

-   Au cours des opérations de diffusion en continu de publication et HTTP (S), les clients App-V 4,5 SP1 utilisent les paramètres du serveur proxy configurés dans Internet Explorer sur l’ordinateur de l’utilisateur.

Pour plus d’informations sur la configuration des paramètres d’installation du client, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md).

 

Enfin, vous devez déterminer le mode de déploiement du logiciel client de bureau Virtualization pour les clients de bureau. Même s’il est possible de déployer manuellement le client de bureau de virtualisation d’application sur chaque ordinateur, la plupart des organisations doivent procéder par le biais d’un processus automatisé. Dans le cas d’une entreprise moyenne ou de grande taille, il est possible qu’elle ait un système ESD et qu’il s’agissait d’une méthode idéale pour déployer le client. S’il n’existe aucun système ESD, vous pouvez utiliser votre méthode standard d’installation de logiciels au sein de votre organisation. Les choix incluent une stratégie de groupe ou différentes techniques de script. Selon le nombre et la taille des bureaux dont vous disposez, ce processus de déploiement peut être complexe, et il est essentiel de prendre une approche structurée pour garantir que tous les ordinateurs obtiennent un client avec la configuration correcte.

## Rubriques connexes


[Planification du déploiement du système Application Virtualization](planning-for-application-virtualization-system-deployment.md)

[Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)

[Procédure pour publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md)

[Procédure pour mettre à niveau Application Virtualization Client](how-to-upgrade-the-application-virtualization-client.md)

[Procédure pour désinstaller App-V Client](how-to-uninstall-the-app-v-client.md)

 

 





