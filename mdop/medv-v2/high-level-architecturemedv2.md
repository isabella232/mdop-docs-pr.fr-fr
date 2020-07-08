---
title: Architecture de haut niveau
description: Architecture de haut niveau
author: dansimp
ms.assetid: a00edb9f-207b-4f32-9e8f-522ea2739d2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8a5db4a56b2abfb0df19b0d6d86f4bf88380c2bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812269"
---
# Architecture de haut niveau


Cette section décrit l’architecture système de niveau supérieur et la conception des composants de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Architecture système


MED-V améliore le PC virtuel Windows pour exécuter deux systèmes d’exploitation sur un appareil, l’ajout d’une remise d’image virtuelle, la mise en service basée sur une stratégie de groupe et la gestion centralisée. Grâce à l’utilisation de MED-V, vous pouvez facilement configurer, déployer et gérer des images d’entreprise virtuelles PC Windows sur n’importe quel ordinateur de bureau Windows 7 professionnel, entreprise ou Windows 7. La solution MED-V inclut les composants suivants:

<a href="" id="---------------med-v-host"></a> **Hôte MED-V**  
Un environnement Windows 7 qui inclut un agent hôte MED-V, un système de distribution de logiciels électronique (ESD), un système de gestion du Registre et un invité MED-V. L’hôte MED-V interagit avec l’invité MED-V de façon à ce que certaines fonctions de configuration et informations système puissent être traitées.

<a href="" id="-------------------med-v-host-agent"></a> **Agent hôte MED-V**  
Le logiciel MED-V contenu dans l’hôte MED-V, qui fournit un canal permettant de communiquer avec l’invité MED-V. Il fournit également des fonctionnalités telles que la première configuration et la publication d’applications.

**Remarques**  Après l’installation de MED-V et de ses composants nécessaires, MED-V doit être configuré. La configuration de MED-V est désignée sous le nom de configuration pour la première fois.

 

<a href="" id="esd-system"></a>**Système ESD**  
Votre méthode de distribution de logiciels existante qui vous permet de déployer et d’installer les fichiers de package d’espace de travail MED-V créés par MED-V.

<a href="" id="registry-management-system"></a>**Système de gestion du Registre**  
Votre méthode de gestion des paramètres de stratégie de groupe et des préférences.

<a href="" id="windows-virtual-pc-image"></a>**Image de l’ordinateur virtuel Windows**  
Une machine virtuelle définie par l’administrateur qui contient les composants suivants:

<a href="" id="corporate-operating-system"></a>**Système d’exploitation de l’entreprise**  
Votre système d’exploitation standard.

<a href="" id="management-and-security-tools"></a>**Outils de gestion et de sécurité**  
Vos outils de gestion standard et de sécurité, tels que la protection antivirus.

<a href="" id="-----------------------med-v-guest"></a> **Invité MED-V**  
Un environnement Windows XP SP3, dans le cadre d’un PC virtuel Windows exécuté sur Windows 7 qui contient les composants suivants:

<a href="" id="---------------------------med-v-guest-agent"></a> **Agent d’invité MED-V**  
Le logiciel MED-V contenu dans l’invité MED-V, qui fournit un canal permettant de communiquer avec l’hôte MED-V. Il prend également en charge l’agent hôte MED-V avec des fonctions telles que la première configuration.

**Remarques**  L’agent d’invité MED-V est automatiquement installé lors de la première configuration.

 

<a href="" id="esd-client"></a>**Client ESD**  
Partie facultative de votre système ESD qui installe les packages logiciels et signale l’état du système ESD.

## Rubriques connexes


[Planification de la compatibilité du système d'exploitation avec les applications](planning-for-application-operating-system-compatibility.md)

[Préparer l'environnement de déploiement de MED-V](prepare-the-deployment-environment-for-med-v.md)

 

 





