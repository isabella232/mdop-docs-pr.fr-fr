---
title: Scénario d'opérations de bout en bout pour MED-V2.0
description: Scénario d'opérations de bout en bout pour MED-V2.0
author: dansimp
ms.assetid: 1d87f5f3-9fc5-4731-8bd1-c155714f34ee
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 90a7c2135ad27040ed87dac980b67321eb771574
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811592"
---
# Scénario d'opérations de bout en bout pour MED-V2.0


Cet exemple de scénario de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 vous permet de déployer et de gérer MED-V en utilisant plusieurs scénarios de bout en bout. Vous pouvez considérer cet exemple de scénario en tant qu’étude de cas, qui permet de mettre en place les différentes procédures et scénarios.

Cette section fournit des informations et des indications de base pour la création, le déploiement et la gestion des espaces de travail MED-V en tant que solution de bout en bout dans votre entreprise.

## Scénario détaillé des opérations MED-V


Les procédures pas à pas à suivre dans un scénario d’opérations MED-V sont les suivantes:

-   La [création d’une image de PC virtuel Windows pour med-v](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-creatingavirtualmachinebyusingmicrosoftvirtualpc) vous explique comment créer et configurer une image de PC virtuel Windows pour med-v. Pour pouvoir livrer un espace de travail MED-V aux utilisateurs, vous devez commencer par préparer un disque dur virtuel (VHD) que vous utilisez pour créer le package d’installation de l’espace de travail MED-v pour MED-V.

-   La [création d’une image de PC virtuel Windows pour MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingwindowsxpontovpc) vous explique comment installer le système d’exploitation Windows XP SP3 sur votre image de PC virtuel Windows. MED-V nécessite l’installation de Windows XP SP3 sur l’image du PC virtuel Windows avant de créer l’espace de travail MED-V.

-   La [création d’une image de PC virtuel pour MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installingnet) consiste à installer manuellement le .net Framework 3,5 SP1 et la mise à jour KB959209 dans l’image du PC virtuel Windows que vous préparez pour une utilisation avec med-v. MED-V nécessite .NET Framework 3,5 SP1 et la mise à jour [KB959209](https://go.microsoft.com/fwlink/?LinkId=204950) ( https://go.microsoft.com/fwlink/?LinkId=204950) corrige plusieurs problèmes de compatibilité liés aux applications connus.

-   La [création d’une image de PC virtuel Windows pour MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-applypatchestovpc) vous explique comment mettre à jour votre image Windows XP avec les mises à jour logicielles et autres correctifs nécessaires ou importants pour exécuter MED-V.

-   La [création d’une image de PC virtuel Windows pour MED-V](creating-a-windows-virtual-pc-image-for-med-v.md#bkmk-installintegration) vous explique comment installer le package composants d’intégration dans votre image Windows XP. Elles offrent des fonctionnalités qui améliorent l’interaction entre l’environnement virtuel et l’ordinateur physique.

-   [L’installation d’applications sur une image de PC virtuel Windows](installing-applications-on-a-windows-virtual-pc-image.md) examine la façon dont vous pouvez installer certains types de logiciels sur votre image Windows XP qui sont utiles lorsque vous exécutez MED-V, par exemple un système de distribution de logiciels électronique et un logiciel antivirus.

-   La [configuration d’une image de PC virtuel Windows pour med-v](configuring-a-windows-virtual-pc-image-for-med-v.md) explique comment configurer l’image en utilisant Sysprep pour vous assurer qu’elle est prête à être utilisée avec med-v. L’image MED-V préparée est alors utilisée pour créer votre package d’espace de travail MED-V.

-   [Créer un package d’espace de travail MED-v](create-a-med-v-workspace-package.md) Apprenez à créer le package d’espace de travail MED-v que vous déploierez au sein de votre entreprise. Vous déployez le package d’espace de travail MED-V pour installer l’espace de travail MED-V sur les ordinateurs des utilisateurs finaux. Un espace de travail MED-V est l’environnement de bureau Windows XP à partir duquel les utilisateurs finaux interagissent avec l’ordinateur virtuel fourni par MED-V.

-   [Le test du package d’espace de travail MED-v](testing-the-med-v-workspace-package.md) décrit la création d’un environnement de test dans lequel vous pouvez tester les fonctionnalités du package d’espace de travail MED-v, telles que les paramètres de configuration de la première utilisation et la publication d’applications. Lorsque vous avez terminé de tester votre package d’espace de travail MED-V et que vous avez vérifié son fonctionnement, vous pouvez le déployer au sein de votre entreprise.

-   [Le déploiement du package d’espace de travail MED-v](deploying-the-med-v-workspace-package.md) décrit le déploiement de l’espace de travail MED-v par le biais d’un système de distribution de logiciels électronique ou d’une image Windows 7. Si vous le souhaitez, cette section vous montre également comment vous pouvez déployer l’espace de travail MED-V manuellement.

-   [Surveiller les espaces de travail MED-v](monitor-med-v-workspaces.md) examine comment surveiller le déploiement d’espaces de travail MED-v pour déterminer si la première configuration s’est déroulée correctement. Il est important de surveiller la réussite de l’installation pour la première fois, car MED-V n’est pas disponible tant qu’il n’a pas été configuré pour la première fois. Cette section vous montre également comment configurer votre environnement pour détecter les modifications de réseau qui peuvent affecter MED-V.

-   [Gestion des applications d’espace de travail MED-v](manage-med-v-workspace-applications.md) examine comment installer et supprimer ou publier et annuler la publication d’applications sur un espace de travail MED-V. Cette section indique également comment mettre à jour manuellement le logiciel dans un espace de travail MED-V et comment gérer les mises à jour automatiques. L’espace de travail MED-V est une machine virtuelle qui contient un système d’exploitation distinct dont le processus automatique de mise à jour logicielle doit être géré exactement comme les ordinateurs physiques de votre entreprise.

-   [Gérer la redirection d’URL MED-V](manage-med-v-url-redirection.md) vous pouvez ajouter et supprimer des paramètres de redirection d’adresse Web sur l’espace de travail MED-v. Vous pouvez ajouter ou supprimer des informations de redirection d’URL par le biais du registre ou en reconstruisant l’espace de travail MED-V. Vous pouvez également utiliser l’Assistant sur le gestionnaire de package d’espace de travail MED-V pour gérer la redirection d’adresse Web.

-   [Gérer les paramètres d’espace de travail MED-v](manage-med-v-workspace-settings.md) examine comment afficher et modifier les paramètres de configuration de med-v à l’aide du gestionnaire de package de l’espace de travail MED-v. Cette section répertorie toutes les clés de Registre MED-V configurables et inclut le type, la valeur par défaut et la description de chacune d’elles. Cette section comprend également des informations sur la façon de gérer les imprimantes dans les espaces de travail MED-V. Dans la version 2,0 de MED-V, la redirection d’imprimante offre aux utilisateurs une interface d’impression homogène entre l’ordinateur virtuel MED-V et l’ordinateur hôte.

## Rubriques connexes


[Opérations de MED-V](operations-for-med-v.md)

[Scénarios de planification de bout en bout pour MED-V2.0](end-to-end-planning-scenario-for-med-v-20.md)

[Scénarios de déploiement de bout en bout pour MED-V2.0](end-to-end-deployment-scenario-for-med-v-20.md)

 

 





