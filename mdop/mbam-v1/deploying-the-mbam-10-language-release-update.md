---
title: Déploiement de MBAM1.0 Language Release Update
description: Déploiement de MBAM1.0 Language Release Update
author: dansimp
ms.assetid: 9dbd85c3-e470-4752-a90f-25754dd46dab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a819be81594efd9349e3f6c0f6559c2b810bdc9d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804518"
---
# Déploiement de MBAM1.0 Language Release Update


La version linguistique de Microsoft BitLocker Analysis and Monitoring (MBAM) 1.0 est une mise à jour de MBAM et inclut la prise en charge de nouvelles langues. Les nouvelles langues sont les suivantes:

-   Anglais (fr-fr)

-   Français (fr)

-   Italien (IT)

-   Allemand (de)

-   Espagnol (es)

-   Coréen (Ko)

-   Japonais (ja)

-   Portugais (Brésil)

-   Russe (RU)

-   Chinois traditionnel (zh-TW)

-   Chinois simplifié (zh-NC)

La mise à jour du langage MBAM 1.0 va changer le numéro de version de MBAM 1.0.1237.1 à MBAM 1.0.2001.

Vous n’avez pas besoin de réinstaller toutes les fonctionnalités MBAM pour ajouter ces langues supplémentaires. Cette rubrique définit les étapes nécessaires à l’ajout de nouvelles langues prises en charge.

## Déploiement de la version internationale de MBAM sur les fonctionnalités de MBAM Server


Pour commencer, vous devez mettre à jour les fonctionnalités suivantes du serveur MBAM:

-   Rapport de conformité et d’audit

-   Serveur d’administration et de surveillance

-   Modèles de stratégie

Ensuite, vous devez exécuter **MbamSetup.exe** pour mettre à niveau les fonctionnalités MBAM qui s’exécutent sur le même serveur en même temps.

[Installation de MBAM Language Update sur un serveur unique](how-to-install-the-mbam-language-update-on-a-single-server-mbam-1.md)

[Installation de MBAM Language Update sur des serveurs distribués](how-to-install-the-mbam-language-update-on-distributed-servers-mbam-1.md)

## Installer la mise à jour de langue MBAM pour les stratégies de groupe


Les modèles de stratégie de groupe MBAM peuvent être installés sur chaque station de travail de gestion ou copiés sur le magasin central de stratégies de groupe, afin de rendre les modèles accessibles aux administrateurs de la stratégie de groupe. Les modèles de stratégie ne peuvent pas être installés directement sur un contrôleur de domaine. Si vous n’utilisez pas un magasin central de stratégies de groupe, vous devez les copier manuellement vers chaque contrôleur de domaine qui gère la stratégie de groupe MBAM.

Pour ajouter les modèles de stratégies de langue de MBAM, copiez les fichiers de langue de stratégie de groupe à partir de%SystemRoot%\\PolicyDefinitions sur l’ordinateur sur lequel le rôle «modèles de stratégie» a été installé au même emplacement sur l’ordinateur de poste de travail. Voici quelques exemples de fichiers de stratégie de groupe:

-   BitLockerManagement. admx

-   BitLockerUserManagement. admx

-   en-us\\BitLockerManagement.adml

-   en-us\\BitLockerUserManagement.adml

-   fr-fr\\ BitLockerManagement. adml

-   fr-fr\\ BitLockerUserManagement. adml

-   (et de la même manière pour chaque langue prise en charge)

## Problèmes connus dans la version internationale de MBAM


Cette rubrique décrit les problèmes connus liés à l’administration de Microsoft BitLocker et à l’analyse internationale.

[Problèmes connus dans MBAM International Release](known-issues-in-the-mbam-international-release-mbam-1.md)

## Autres ressources pour le déploiement de la mise à jour de langue de MBAM 1,0


[Déploiement de MBAM1.0](deploying-mbam-10.md)

 

 





