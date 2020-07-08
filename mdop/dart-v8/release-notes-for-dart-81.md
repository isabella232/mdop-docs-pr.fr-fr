---
title: Notes de publication pour DaRT8.1
description: Notes de publication pour DaRT8.1
author: dansimp
ms.assetid: 44303107-60f4-485c-848a-7e0529f142d4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d0ba817ddd5bbdefcf7fed833f4c47e7b9d9ce0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810751"
---
# Notes de publication pour DaRT8.1


**Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.**

Lisez attentivement ces notes de publication avant de procéder à l’installation de Microsoft Diagnostics and Recovery Tools (DaRT) 8,1.

Ces notes de publication contiennent des informations nécessaires à l’installation réussie des 8,1 outils de diagnostics et de récupération. Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents DaRT, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## Problèmes connus avec le 8,1 DaRT


### Disk commander ne peut pas réparer un enregistrement de démarrage maître endommagé dans une partition physique dans Windows 8,1

Dans Windows 8,1, l’option «restaurer l’enregistrement de démarrage principal (MBR) ou l’en-tête de la table de partitions GUID (GPT) dans Disk commander ne peut pas réparer un enregistrement de démarrage maître endommagé dans une partition physique, et ne peut donc pas démarrer l’ordinateur client.

**Solution de contournement:** Cliquez sur **résolution des problèmes** **, sur** **Options avancées**, puis sur Démarrer la **réparation**.

### Plusieurs instances d’une réinitialisation de disque qui ciblent le même lecteur, à l’exception de la première, de signaler une panne.

Si vous démarrez plusieurs instances de Disk Wipe et que vous essayez de réinitialiser le même lecteur en utilisant deux instances de réinitialisation de disque distinctes, toutes les instances à l’exception du dernier indiquent un échec de réinitialisation du lecteur.

**Solution de contournement:** Néant.

### La réinitialisation du disque risque de ne pas effacer toutes les données sur les lecteurs à état solide disposant d’une mémoire flash

Si vous utilisez la fonction de réinitialisation du disque pour effacer les données sur un disque SSD qui est doté de mémoire flash, il est possible que l’ensemble des données ne soient pas effacées. Ce problème se produit car le microprogramme SSD contrôle l’emplacement physique des écritures lorsque le disque est en cours d’exécution.

**Solution de contournement:** Néant.

### La restauration du système échoue lorsque vous exécutez l’Assistant Locksmith ou l’éditeur du Registre

Si vous exécutez l’Assistant Locksmith, l’éditeur du Registre et éventuellement d’autres outils, la restauration du système échoue.

**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez la restauration du système.

### Le vérificateur des fichiers système ne peut pas être exécuté après que vous avez démarré et fermé Locksmith Assistant ou la gestion de l’ordinateur

Si vous démarrez, puis fermez Locksmith Assistant ou outils dans gestion de l’ordinateur, le vérificateur de fichiers système ne fonctionne pas.

**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez le vérificateur des fichiers système.

### <a href="" id="-------------dart-installer-does-not-fail-when-the-windows-assessment-and-deployment-kit-is-not-installed"></a> Le programme d’installation de DaRT ne fonctionne pas lorsque le kit d’évaluation et de déploiement Windows n’est pas installé

Si vous installez DaRT 8,1 à l’aide de la ligne de commande pour exécuter Windows Installer (. msi) et que le kit d’évaluation et de déploiement Windows (WindowsADK) n’a pas été installé, l’installation DaRT doit échouer. Pour le moment, le programme d’installation 8,1 de DaRT installe tous les composants, à l’exception de l’image de récupération DaRT.

**Solution de contournement:** Néant.

### Windows Defender ne peut pas démarrer après le démarrage de l’Assistant Locksmith, de l’éditeur du Registre, de l’analyse crash et de la gestion de l’ordinateur

Windows Defender ne démarre pas si vous avez déjà démarré l’Assistant Locksmith, l’éditeur du Registre, l’analyse crash et la gestion de l’ordinateur.

**Solution de contournement:** Fermez et redémarrez DaRT, puis démarrez Windows Defender.

### Windows Defender risque de ne pas être démarré

Le démarrage de Windows Defender peut prendre quelques minutes. La barre de progression indique l’état de chargement actuel.

**Solution de contournement:** Néant.

## Rubriques connexes


[À propos de DaRT8.1](about-dart-81.md)

 

 





