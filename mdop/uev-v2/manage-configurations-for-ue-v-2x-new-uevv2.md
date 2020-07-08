---
title: Gérer les configurations pour UE-V2.x
description: Gérer les configurations pour UE-V2.x
author: dansimp
ms.assetid: e2332eca-a9cd-4446-8f7c-d17058b03466
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 20d5d2942dbd805a4054a9431b237c821cbb70fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812323"
---
# Gérer les configurations pour UE-V2.x


Dans le cadre de la virtualisation de l’interface utilisateur de Microsoft (UE-V) 2,0, de 2,1 ou du cycle de vie 2,1 SP1, vous devez gérer la configuration de l’agent UE-V et gérer les emplacements de stockage des ressources telles que les fichiers du package de paramètres. Vous devrez peut-être effectuer d’autres tâches (par exemple, configurer le centre de paramètres de la société) pour définir le mode d’interaction des utilisateurs avec UE-V. Les rubriques suivantes fournissent des instructions pour la gestion de ces ressources UE-V.

## Configuration d’UE-V 2. x à l’aide d’objets de stratégie de groupe


Vous pouvez utiliser les objets de stratégie de groupe pour modifier les paramètres définissant la façon dont UE-V synchronise les paramètres sur les ordinateurs.

[Configuration d’UE-V 2. x avec des objets de stratégie de groupe](configuring-ue-v-2x-with-group-policy-objects-both-uevv2.md)

## Configuration d’UE-V 2. x avec System Center Configuration Manager 2012


Vous pouvez utiliser SystemCenter2012 ConfigurationManager pour gérer l’agent UE-V à l’aide du Pack de configuration UE-V 2.

[Configuration d’UE-V 2. x avec System Center Configuration Manager 2012](configuring-ue-v-2x-with-system-center-configuration-manager-2012-both-uevv2.md)

## Administration d’UE-V 2. x avec PowerShell et WMI


UE-V fournit des cmdlets Windows PowerShell, qui permettent aux administrateurs d’effectuer différentes tâches d’UE-V.

[Administration d’UE-V 2. x avec Windows PowerShell et WMI](administering-ue-v-2x-with-windows-powershell-and-wmi-both-uevv2.md)

## Configuration du centre de paramètres de société pour UE-V 2. x


Vous pouvez configurer le centre de paramètres de l’entreprise installé à l’aide de l’agent UE-V pour définir le mode d’interaction des utilisateurs avec UE-V.

[Configuration du centre de paramètres de société pour UE-V 2. x](configuring-the-company-settings-center-for-ue-v-2x-both-uevv2.md)

## Exemples de paramètres de configuration pour UE-V 2. x


Vous trouverez ci-dessous des exemples de paramètres de configuration de UE-V:

-   **Emplacement de stockage des paramètres:** Spécifie l’emplacement du partage de fichiers qui stocke les paramètres d’UE-V.

-   **Modèle d’emplacement du modèle de paramètres:** Spécifie le chemin d’accès UNC (Universal Naming Convention) qui définit l’emplacement dans lequel les nouveaux modèles d’emplacement des paramètres sont consultés.

-   **Enregistrez les modèles Microsoft:** Indique si les modèles Microsoft par défaut doivent être inscrits lors de l’installation.

-   **Méthode de synchronisation:** Indique si UE-V utilise le fournisseur de synchronisation ou «aucune». Le «SyncProvider» prend en charge les ordinateurs qui sont déconnectés du réseau. «Aucune» s’applique lorsque l’ordinateur est toujours connecté au réseau. Pour plus d’informations sur la méthode de synchronisation, voir [méthodes de synchronisation pour UE-V 2. x](sync-methods-for-ue-v-2x-both-uevv2.md).

-   **Délai d’expiration de la synchronisation:** Spécifie le nombre de millisecondes que l’ordinateur attend avant la fin de son exécution lors de la récupération des paramètres utilisateur à partir de l’emplacement de stockage des paramètres.

-   **Activation de la synchronisation:** Indique si la synchronisation des paramètres d’UE-V est activée ou désactivée.

-   **Taille maximale du package:** Spécifie une taille de seuil du fichier de package de paramètres pour lequel l’agent UE-V signale une alerte.

-   **Ne synchronisez pas les paramètres de l’application Windows:** Spécifie qu’UE-V ne peut pas synchroniser les applications Windows.

-   **Activez/désactivez la notification d’utilisation initiale:** Indique si UE-V affiche une boîte de dialogue la première fois que l’agent UE-V est exécuté sur l’ordinateur d’un utilisateur.

-   **Activer/désactiver l’icône** de la barre d’état système: Indique si UE-V affiche une icône dans la zone de notification et les notifications associées à celle-ci. L’icône fournit un lien vers le centre de paramètres de l’entreprise.

-   **Contact personnalisé il s’agit d’un lien hypertexte:** Spécifie le chemin d’accès, le texte et la description de l’hyperlien de **contact** dans le centre de paramètres de l’entreprise.






## Rubriques connexes


[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

[Déployer les fonctionnalités UE-V2.x requises](deploy-required-features-for-ue-v-2x-new-uevv2.md)

[Déployer UE-V 2. x pour des applications personnalisées](deploy-ue-v-2x-for-custom-applications-new-uevv2.md)

 

 





