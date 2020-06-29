---
title: Notes de publication pour MED-V1.0
description: Notes de publication pour MED-V1.0
author: dansimp
ms.assetid: 006a3537-5c5b-43b5-8df8-4bf6ddd3cd2f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 683056f768a3d547828996a9b191d58337c21ad6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811849"
---
# Notes de publication pour MED-V1.0


## Problèmes connus avec MED-V


Cette section fournit des informations détaillées sur les problèmes généraux liés à la plateforme Microsoft Enterprise Desktop Virtualization (MED-V). Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire. Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.

### Les téléchargements de fichiers ne respectent pas les règles de redirection Web

Les téléchargements de fichiers ne respectent pas les règles de redirection Web définies dans une stratégie d’espace de travail MED-V.

### Lorsque vous développez une fenêtre d’application publiée sur la console en mode plein écran, cette dernière disparaît

Si vous développez une application de console publiée (par exemple, cmd.exe) en plein écran à l’intérieur d’un espace de travail MED-V configuré en mode d’intégration transparente, la fenêtre de l’application peut disparaître ou ne pas répondre.

### Lorsque vous travaillez en mode Bureau complet, les emplacements des icônes sur le Bureau ne sont pas enregistrés

Lorsque vous travaillez en mode Bureau complet, le changement d’emplacement manuel des icônes sur le bureau n’est pas enregistré entre les sessions d’espace de travail MED-V.

### Une image locale et une image de test portant le même nom ne peuvent pas exister dans le même domaine

Si une image locale est jointe au domaine et que l’administrateur crée une nouvelle version de la même image portant le même nom d’ordinateur qu’une image de test, lorsque l’image de test rejoint le domaine, l’action joindre le domaine échoue ou l’image locale est supprimée du domaine.

### MED-V ne prend pas en charge les fonctionnalités de Windows Aero

MED-V ne prend pas en charge les fonctionnalités de Windows Aero (comme Aero Flip 3D).

### La console de gestion ne peut être utilisée que par un seul utilisateur Windows par ordinateur

La console de gestion MED-V ne peut être utilisée que par les administrateurs et les utilisateurs Windows qui ont installé l’application de gestion.

### L’utilitaire de configuration de serveur MED-V teste la connectivité de Microsoft SQL Server sous le contexte de l’utilisateur plutôt que dans le contexte de service du serveur MED-V.

MED-V utilise le contexte de service du serveur MED-V pour collecter des rapports à partir de la base de données Microsoft SQL Server Reports. L’utilitaire de configuration de serveur MED-V vérifie la base de données et teste la chaîne de connexion de la base de données. Cela ne valide pas l’accès au service du serveur MED-V à la base de données.

 

 





