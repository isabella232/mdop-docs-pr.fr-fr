---
title: Utilisation de serveurs Application Virtualization Server comme solution de gestion des packages
description: Utilisation de serveurs Application Virtualization Server comme solution de gestion des packages
author: dansimp
ms.assetid: 41597355-e7bb-45e2-b300-7b1724419975
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2b81ed3ab6fa3a70fe4780904059091f22579d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806181"
---
# Utilisation de serveurs Application Virtualization Server comme solution de gestion des packages


Si vous ne disposez pas d’un système de gestion des opérations de déploiement de votre application, ou si vous ne souhaitez pas en utiliser un, vous devez installer un ou plusieurs serveurs de gestion de la virtualisation des applications en tant que cœur de votre architecture système. Le serveur de gestion de la virtualisation des applications nécessite un ordinateur serveur dédié et a besoin d’une base de données Microsoft SQL Server. La base de données peut se trouver sur le même serveur ou être configurée sur un serveur de base de données d’entreprise accessible par le serveur de gestion de la virtualisation des applications par le biais d’une connexion réseau haut débit. Par ailleurs, vous devez installer la console de gestion des applications Microsoft application, sur le serveur de gestion de la virtualisation des applications ou sur une station de travail de gestion désignée, et vous devrez installer le service Web Microsoft Application Virtualization Management, qui peut également être installé sur le serveur de gestion des applications virtuelles ou sur un serveur IIS distinct. La console de gestion de l’application virtualisation est utilisée pour la connexion au service Web de gestion des applications, permettant ainsi à l’administrateur système d’interagir avec le serveur de gestion de la virtualisation des applications.

**Remarques**  L’accès aux applications est contrôlé par le biais des groupes de sécurité dans les services de domaine Active Directory (AD FS), vous devez donc planifier un processus de configuration d’un groupe de sécurité pour chaque application virtualisée et de gestion des utilisateurs ajoutés à chaque groupe. L’administrateur du serveur de gestion des applications configure le serveur pour utiliser ces groupes Active Directory et le serveur contrôle automatiquement l’accès aux packages en fonction de l’appartenance aux groupes Active Directory.

 

## Dans cette section


<a href="" id="overview-of-the-application-virtualization-system-components"></a>[Présentation des composants du système Application Virtualization](overview-of-the-application-virtualization-system-components.md)  
Répertorie et décrit les principaux composants du système de gestion de Microsoft Application Virtualization.

<a href="" id="publishing-virtual-applications-using-application-virtualization-management-servers"></a>[Publication d'applications virtuelles à l'aide de serveurs Application Virtualization Management Server](publishing-virtual-applications-using-application-virtualization-management-servers.md)  
Fournit une vue d’ensemble de la façon dont les applications virtuelles sont publiées dans un scénario de déploiement basé sur un serveur de virtualisation des applications.

<a href="" id="planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation"></a>[Planification de votre solution de diffusion en continu dans une implémentation basée sur un serveur Application Virtualization Server](planning-your-streaming-solution-in-an-application-virtualization-server-based-implementation.md)  
Décrit les options disponibles pour l’utilisation des serveurs de diffusion en continu d’applications en conjonction avec votre implémentation basée sur le serveur de gestion de la virtualisation des applications.

## Rubriques connexes


[Scénario basé sur un serveur Application Virtualization Server](application-virtualization-server-based-scenario.md)

[Planification du déploiement du système Application Virtualization](planning-for-application-virtualization-system-deployment.md)

 

 





