---
title: Amélioration de la sécurité lors du séquencement d'App-V
description: Amélioration de la sécurité lors du séquencement d'App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806674"
---
# Amélioration de la sécurité lors du séquencement d'App-V


L’empaquetage d’applications pour le séquençage représente la plus grande tâche en cours dans une infrastructure App-V. Dans la mesure où cette tâche est en cours, vous devez soigneusement envisager la création de stratégies et de procédures à suivre lors du séquençage d’applications. Dans App-V 4.5 lors du séquençage, vous pouvez capturer des listes de contrôle d’accès (ACL) sur les ressources de fichier de l’application virtualisée.

## Analyse antivirus sur le Sequencer


Il est recommandé d’installer le logiciel de numérisation sur l’ordinateur de séquençage, puis de détecter la recherche de virus et de programmes malveillants dans l’ordinateur. Une fois que l’ordinateur de séquençage est scanné et ne dispose pas de virus et de programmes malveillants, désactivez le logiciel de numérisation, y compris le logiciel antivirus et de détection de logiciels malveillants, sur l’ordinateur de séquençage avant de séquencer les applications. Cela accélère le processus de séquençage et empêche les composants logiciels d’analyse d’être détectés lors du séquençage et inclus dans le package d’application virtuelle.

## Capture d’ACL sur des fichiers (NTFS)


Le Sequencer capture les autorisations NTFS (listes de contrôle d’accès (ACL) pour les fichiers surveillés lors de la phase d’installation du séquençage. (Avant la publication de App-V 4.5, les ACL n’ont pas été capturées dans le cadre du processus de séquençage.) Cette nouvelle fonctionnalité permet à certaines applications d’être exécutées pour les utilisateurs disposant d’un niveau d’autorisation faible, qui nécessiteraient normalement des privilèges d’administration.

Cette fonctionnalité permet également aux ingénieurs de Sequencer de capturer les paramètres de sécurité identifiés par le fournisseur. Le non-respect des paramètres recommandés par le fournisseur risque de laisser l’application ouverte aux attaques ou abus par les utilisateurs. Pour plus d’informations sur l’utilisation ou non du déploiement d’une application avec des listes de Contrã’le d’accès ouvertes, reportez-vous au groupe de support de votre application ou au revendeur de logiciels.

**Important**  Même si le Sequencer capture les listes de contrôle d’accès (ACL) NTFS lors de l’analyse de la phase d’installation du séquençage, il n’enregistre pas les listes de contrôle d’accès pour le registre. Les utilisateurs disposent d’un accès complet à toutes les clés de Registre pour les applications virtuelles à l’exception des services. Toutefois, si un utilisateur modifie le registre d’une application virtuelle, cette modification est stockée à un emplacement spécifique ( `uservol_sftfs_v1.pkg` ) et ne peut pas être affectée par d’autres utilisateurs.

 

Pendant la phase d’installation, un ingénieur de séquençage peut modifier les autorisations par défaut des fichiers si nécessaire. Une fois le processus de séquençage terminé, mais avant de l’enregistrer, vous pouvez choisir d’appliquer des descripteurs de sécurité qui ont été capturés lors de la phase d’installation. Il est recommandé de mettre en œuvre des descripteurs de sécurité s’il n’y a aucune autre solution pour que l’application s’exécute correctement une fois virtualisé.

 

 





