---
title: Résolution des problèmes de déploiement
description: Résolution des problèmes de déploiement
author: dansimp
ms.assetid: 9ee980f2-4e77-4020-9f0e-8c2ffdc390ad
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fe9677175c9538bc070d2adea17a96351397d9a0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809630"
---
# Résolution des problèmes de déploiement


Cette rubrique contient des informations pour vous aider à résoudre les problèmes de déploiement dans Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Résoudre les problèmes de déploiement MED-V


Le problème suivant peut se produire lorsque vous déployez MED-V. La solution aide à résoudre ce problème.

**Des problèmes se produisent lors de l’installation de MED-V pour l’utilisateur actuel uniquement.** MED-V ne prend en charge que l’installation du gestionnaire de package d’espace de travail MED-V, de l’agent hôte MED-V et de l’espace de travail MED-V pour tous les utilisateurs. L’installation pour l’utilisateur actuel cause uniquement les échecs de l’installation des composants et de l’installation de l’espace de travail MED-V.

**Solution**

N’utilisez jamais l’option **ALLUSERS = ""** lors de l’installation des composants MED-V.

**MED-V nécessite une utilisation exclusive de la pile de virtualisation.** Seule une pile de virtualisation peut être exécutée à la fois sur un ordinateur. Le PC virtuel Windows doit utiliser la pile virtuelle et MED-V dépend du PC virtuel Windows. Par conséquent, si vous essayez de déployer ou d’utiliser MED-V lorsque d’autres applications utilisent la pile virtuelle, MED-V ne peut pas s’exécuter ou être installé correctement.

**Solution**

Fermez toute application en cours d’exécution qui utilise la pile de virtualisation avant d’installer ou d’exécuter MED-V.

**Les raccourcis restent après la désinstallation.** Par défaut, lorsque vous désinstallez MED-V, les raccourcis du menu **Démarrer** de l’utilisateur final sont supprimés. Toutefois, dans certains cas, par exemple pour les utilisateurs finaux qui exécutent des profils itinérants, le raccourci vers les applications publiées MED-V reste dans le menu **Démarrer** de l’utilisateur final.

**Solution**

Pour supprimer manuellement les raccourcis restant dans le menu **Démarrer** , cliquez avec le bouton droit sur les raccourcis, puis cliquez sur **supprimer**.

**Désactivez le paramètre de stratégie de groupe message d’ouverture de session dans l’espace de travail MED-V.** Si le message d’ouverture de session Windows XP est activé dans l’espace de travail MED-V, l’utilisateur final doit se connecter chaque fois qu’il souhaite ouvrir une application virtuelle MED-V. Cela crée une mauvaise utilisation de l’utilisateur.

**Solution**

Désactivez les paramètres de stratégie de groupe suivants dans l’ordinateur virtuel MED-V:

**Ouverture de session interactive: contenu du message pour les utilisateurs essayant de se connecter**

**Ouverture de session interactive: titre du message pour les utilisateurs essayant de se connecter**

## Rubriques connexes


[Résolution des problèmes d'opérations](operations-troubleshooting-medv2.md)

 

 





