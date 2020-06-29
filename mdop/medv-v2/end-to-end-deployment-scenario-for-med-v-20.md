---
title: Scénarios de déploiement de bout en bout pour MED-V2.0
description: Scénarios de déploiement de bout en bout pour MED-V2.0
author: dansimp
ms.assetid: 91bb5a9a-5fb1-4743-8494-9d4dee2ec222
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6d56e70ad359ebf2d76cf3f30f54f73cd9ca1c66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811597"
---
# Scénarios de déploiement de bout en bout pour MED-V2.0


Cet exemple de scénario de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 vous permet de déployer les composants MED-V au sein de votre entreprise à l’aide de plusieurs scénarios de bout en bout. Vous pouvez considérer cet exemple de scénario en tant qu’étude de cas, qui permet de mettre en place les différentes procédures et scénarios.

Cette section fournit des informations et des indications de base pour le déploiement de composants MED-V en tant que solution de bout en bout au sein de votre entreprise.

## Scénario détaillé de déploiement MED-V


Les rubriques de cette procédure pas à pas sont les suivantes:

-   Les [Configurations prises en charge par MED-V 2,0](med-v-20-supported-configurations.md) traitent de la configuration requise pour l’installation et l’exécution de Microsoft Enterprise Desktop Virtualization (med-v) 2.0 dans votre environnement. Cette rubrique spécifie la configuration requise du système d’exploitation, la configuration requise pour l’espace de travail MED-V. Cette rubrique inclut également des informations sur la localisation des langues prises en charge par MED-V 2,0.

-   La [vue d’ensemble du déploiement de MED-V 2,0](med-v-20-deployment-overview.md) traite des informations générales et des instructions pour vous aider à installer et déployer med-v au sein de votre entreprise. Les composants MED-V sont basés sur le client et sont remis et gérés en utilisant vos processus et infrastructure d’entreprise existants. Cette rubrique fournit une vue d’ensemble de la solution MED-V qui inclut des informations sur les fichiers d’installation de MED-V et les composants MED-V que vous déployez. Cette rubrique fournit également une vue d’ensemble de l’installation et du processus de déploiement de MED-V.

-   [Préparer l’environnement de déploiement pour med-v](prepare-the-deployment-environment-for-med-v.md) explique comment préparer votre environnement pour un déploiement 2,0 MED-V. Cette section décrit les conditions préalables requises pour l’environnement MED-V, comme Microsoft Windows 7 et une infrastructure Active Directory dans laquelle vous utilisez une stratégie de groupe pour assurer une gestion centralisée et la configuration des systèmes d’exploitation, des applications et des paramètres des utilisateurs. Cette section décrit également les prérequis requis pour l’installation et le déploiement de MED-V 2,0 au sein de votre entreprise, tels que le PC virtuel Windows et la mise à jour de PC virtuel Windows requise.

-   Le [déploiement des composants med-v](deploy-the-med-v-components.md) aborde les différentes méthodes d’installation de tous les fichiers d’installation nécessaires et des composants MED-V au sein de votre entreprise. Pour installer et déployer MED-V, vous devez généralement procéder comme suit:

    1.  Installez le module de création de **package d’espace de travail MED-v** sur l’ordinateur d’administration que vous utiliserez pour générer les packages d’espace de travail MED-v. Pour plus d’informations, reportez-vous [à la rubrique Comment installer le gestionnaire de package MED-V](how-to-install-the-med-v-workspace-packager.md).

    2.  Créez et testez vos packages d’espace de travail MED-V. Pour plus d’informations, consultez [créer un package d’espace de travail MED-v](create-a-med-v-workspace-package.md) et [tester le package d’espace de travail MED-v](testing-the-med-v-workspace-package.md).

    3.  Déployez MED-V au sein de votre entreprise à l’aide de la méthode existante de votre entreprise pour le déploiement d’applications. Pour plus d’informations, reportez-vous à [déploiement du package d’espace de travail MED-V](deploying-the-med-v-workspace-package.md).

## Rubriques connexes


[Déploiement de MED-V](deployment-of-med-v.md)

[Scénarios de planification de bout en bout pour MED-V2.0](end-to-end-planning-scenario-for-med-v-20.md)

[Scénario d'opérations de bout en bout pour MED-V2.0](end-to-end-operations-scenario-for-med-v-20.md)

 

 





