---
title: À propos des packages Application Virtualization
description: À propos des packages Application Virtualization
author: dansimp
ms.assetid: 69bd35c1-7af3-43db-931b-3074780aa926
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cfe6df90881ea4179fa8cd224609ca6d28ff5f61
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808165"
---
# À propos des packages Application Virtualization


Dans la virtualisation des applications, un *package* est la sortie du processus de séquençage. Vous utilisez des packages lorsque vous déployez d’abord des applications sur vos serveurs et que vous effectuez une mise à niveau d’applications avec une nouvelle version. Les packages vous permettent de contrôler les versions d’applications virtuelles sur les serveurs de gestion de la virtualisation des applications. Un package unique peut contenir une ou plusieurs applications. Chaque package d’application contient un ensemble de fichiers sous forme d’unité autonome.

## Gestion des packages


Une fois que le Sequencer a créé un package d’une ou plusieurs applications dans le cadre de son processus, vous pouvez copier les fichiers générés par Sequencer sur un serveur de gestion des applications et les rendre accessibles pour le streaming.

Les packages disponibles apparaissent sous le conteneur **packages** dans le volet gauche de la console de gestion de l’application virtualisation. Lorsque vous importez une application à l’aide d’un fichier de Project de séquence (SPRJ) ou d’un fichier de description de logiciel ouvert (OSD), une entrée liée apparaît dans le conteneur **packages** . À partir de la console de gestion du serveur d’applications, vous pouvez ensuite déployer, mettre à niveau ou supprimer des packages et des versions de celles-ci.

Chaque application virtuelle est associée à un package. Ce package inclut les fichiers suivants:

-   SFT: fichier qui transmet l’application aux clients.

-   Affichage à l’écran: le fichier de descripteur de logiciel ouvert contient les informations nécessaires pour rechercher et lancer l’application.

-   ICO: il s’agit du fichier d’icône qui représente visuellement l’application dans les interfaces utilisateur et les raccourcis.

-   SPRJ: fichier de projet de Sequencer.

Lorsque vous importez le fichier SPRJ, toutes les applications séquencées sont disponibles pour le déploiement par défaut, mais les applications ne sont pas activées pour le streaming. Vous pouvez choisir de diffuser en continu tout ou partie des applications du package. Par exemple, si vous avez séquencé et importé Microsoft Office, vous pouvez choisir de ne pas déployer certaines applications, telles que l’Assistant enregistrer mes paramètres. Dans ce cas, cliquez avec le bouton droit sur chaque application que vous voulez déployer, sélectionnez **Propriétés**, puis assurez-vous que la case **activé** est cochée (vide). Seules les applications pour lesquelles la case **activée** est activée seront transmises aux ordinateurs clients.

Une fois que vous avez reséquencé un package et produit un nouveau fichier SFT pour la diffusion en continu, vous pouvez mettre à niveau l’ancien package de façon rapide et aisée via la console de gestion du serveur d’applications.

Le seul scénario opérationnel qui nécessite l’utilisation du nœud **packages** est le cas où vous introduisez une nouvelle version (fichier SFT) pour le package. Dès lors que vous importez des applications, attribuez l’accès et des licences aux applications, et ainsi de suite, le système de virtualisation des applications effectue le suivi de ces informations au niveau du package. Cela signifie que lorsque vous autorisez un utilisateur à utiliser une application, vous donnez à l’utilisateur l’autorisation d’exécuter une application quelconque dans le même package.

### Version du package

Une version de package est représentée par un fichier SFT spécifique. Lorsque vous mettez à niveau un package (appliquer une mise à jour à une application ou ajouter une application à un package), vous générez un nouveau fichier SFT. Chaque fois que vous créez un nouveau fichier SFT, vous créez une nouvelle version de package.

Lorsque vous importez des applications par le biais de la console de gestion du serveur d’applications, le logiciel crée automatiquement un package et une version de package s’il n’existe pas déjà.

## Rubriques connexes


[À propos des applications Application Virtualization](about-application-virtualization-applications.md)

[À propos d'Application Virtualization Server Management Console](about-the-application-virtualization-server-management-console.md)

[Procédure pour gérer les packages dans Server Management Console](how-to-manage-packages-in-the-server-management-console.md)

 

 





