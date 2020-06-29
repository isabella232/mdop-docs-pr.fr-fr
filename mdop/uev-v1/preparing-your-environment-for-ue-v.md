---
title: Préparation de votre environnement pour UE-V
description: Préparation de votre environnement pour UE-V
author: dansimp
ms.assetid: c93d3b33-e032-451a-9e1b-8534e1625396
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 8f806f3c326bad5204a7f1ee69e11b61177e3cce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810680"
---
# Préparation de votre environnement pour UE-V


La virtualisation de l’interface utilisateur de Microsoft (UE-V) réutilise les paramètres d’ordinateurs en utilisant l’emplacement de stockage des paramètres. L’emplacement de stockage des paramètres est un partage de fichiers et doit être configuré lors du déploiement de l’agent UE-V. Elle doit être définie en tant qu’emplacement de stockage des paramètres ou en tant qu’annuaire racine Active Directory. Par ailleurs, l’administrateur doit configurer un serveur de temps pour qu’il prenne en charge une synchronisation cohérente. Pour préparer votre environnement pour UE-V, vous devez tenir compte des éléments suivants:

-   [Stockage des paramètres d’UE-V](#bkmk-uevsettingsstorage):

    -   [Définition d’un emplacement de stockage des paramètres](#bkmk-definingsettingsstoragelocation)

    -   [Utiliser le répertoire de base Active Directory avec UE-V](#bkmk-usingactivedirectoryhomedirectory)

-   [Synchroniser les horloges de l’ordinateur pour la synchronisation des paramètres d’UE-V](#bkmk-synchronizecomputerclocks)

-   [Planification des performances et de la capacité](#bkmk-performancecapacityplanning)

Pour plus d’informations sur le système d’exploitation et les exigences informatiques, voir [Configurations prises en charge pour UE-V 1,0](supported-configurations-for-ue-v-10.md).

## <a href="" id="bkmk-uevsettingsstorage"></a>Stockage des paramètres d’UE-V


Vous pouvez définir le stockage des paramètres de virtualisation de l’utilisation de l’utilisateur dans l’une des deux configurations suivantes: un emplacement de stockage des paramètres ou un répertoire d’accueil Active Directory.

### <a href="" id="bkmk-definingsettingsstoragelocation"></a>Définir un emplacement de stockage des paramètres

L’emplacement de stockage des paramètres d’UE-V est un partage réseau standard accessible aux utilisateurs d’UE-V. Avant de définir l’emplacement de stockage des paramètres, vous devez créer un répertoire racine. Les utilisateurs qui stockeront des paramètres sur le partage doivent disposer d’autorisations en lecture/écriture sur l’emplacement de stockage. L’agent UE-V va créer des dossiers propres à l’utilisateur sous cet annuaire racine. L’emplacement de stockage des paramètres est défini en définissant l’option de configuration **SettingsStoragePath** . Vous pouvez configurer cette option de l’une des façons suivantes:

-   Lors de l’installation de l’agent UE-V par le biais d’un paramètre de ligne de commande ou d’un script de commandes.

-   À l’aide d’une stratégie de groupe.

-   Après l’installation, à l’aide de PowerShell ou WMI.

Le chemin d’accès doit être dans un chemin UNC (Universal Naming Convention) du serveur et le partage. Par exemple, **\\\\server\\settingsshare\\**. Cette option de configuration prend en charge l’utilisation de variables pour activer des scénarios d’itinérance spécifiques.

Vous pouvez utiliser la `%username%` variable avec le chemin UNC du serveur et partager. Cela vous permettra de bénéficier de la même configuration sur tous les ordinateurs ou toutes les sessions auxquelles un utilisateur se connecte. Tenez compte de cette configuration dans les cas suivants:

1.  Les utilisateurs de l’entreprise disposent de plusieurs ordinateurs physiques configurés de la même manière et les paramètres de chaque utilisateur doivent être identiques sur tous les ordinateurs.

2.  Les utilisateurs de l’entreprise utilisent des pools d’infrastructure VDI (Virtual Desktop Infrastructure) où les paramètres doivent être conservés dans les sessions VDI de chaque utilisateur.

3.  Les utilisateurs de l’entreprise disposent d’un ordinateur physique et utilisent également un VDI. L’utilisation des paramètres de l’utilisateur doit être identique à celle de l’ordinateur physique ou de la session VDI.

4.  Plusieurs ordinateurs d’entreprise sont utilisés par plusieurs utilisateurs. L’utilisation des paramètres de l’utilisateur doit être identique sur tous les ordinateurs.

Vous pouvez utiliser les variables **%username%\\%ComputerName%** avec le chemin UNC du serveur et partager. Cela préserve l’option de configuration pour chaque ordinateur. Tenez compte de cette configuration dans les cas suivants:

1.  Les utilisateurs de l’entreprise disposent de plusieurs ordinateurs physiques et vous voulez conserver l’interface des paramètres pour chaque ordinateur.

2.  Les ordinateurs d’entreprise sont utilisés par plusieurs utilisateurs. L’utilisation des paramètres doit être préservée pour chaque ordinateur sur lequel l’utilisateur se connecte.

L’agent UE-V crée dynamiquement le chemin de stockage des paramètres spécifique à l’utilisateur en fonction du paramètre de configuration d’UE-V `SettingsStoragePath` et des variables définies.

L’agent UE-V crée dynamiquement un dossier système caché nommé `SettingsPackages` dans chaque emplacement de stockage spécifique à l’utilisateur. Le l’agent UE-V lit et écrit les paramètres dans cet emplacement, tel que défini par les modèles d’emplacement des paramètres UE-V enregistrés.

Si l’emplacement de stockage des paramètres est le même pour un ensemble d’ordinateurs gérés d’un utilisateur, les paramètres UE-V applicables sont déterminés par une règle «dernier enregistrement WINS». L’agent qui s’exécute sur un ordinateur lit et écrit à l’emplacement des paramètres indépendamment des agents qui s’exécutent sur d’autres ordinateurs. Les derniers paramètres et valeurs écrits sont les paramètres qui sont appliqués lorsque l’agent suivant lit à partir de l’emplacement de stockage des paramètres. Pour plus d’informations, reportez-vous à [déploiement de l’emplacement de stockage des paramètres pour UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md).

### <a href="" id="bkmk-usingactivedirectoryhomedirectory"></a>Utiliser le répertoire de base Active Directory avec UE-V

Si aucun emplacement de stockage des paramètres n’est configuré pour UE-V lors du déploiement de l’agent, le répertoire de base Active Directory (AD) de l’utilisateur est utilisé pour stocker les packages de localisation des paramètres. L’agent UE-V crée dynamiquement le dossier de stockage des paramètres en dessous de la racine du répertoire de base AD de chaque utilisateur. L’agent n’utilise le répertoire de base Active Directory que si un emplacement de stockage des paramètres (SettingsStoragePath) n’est pas défini pour le contraire.

## <a href="" id="bkmk-synchronizecomputerclocks"></a>Synchroniser les horloges de l’ordinateur pour la synchronisation des paramètres d’UE-V


Les ordinateurs qui exécutent l’agent UE-V pour synchroniser les paramètres doivent utiliser un serveur de temps. Les horodatages permettent de déterminer si les paramètres doivent être synchronisés à partir de l’emplacement de stockage des paramètres. Si l’horloge de l’ordinateur est incorrecte, les paramètres plus anciens peuvent remplacer les paramètres plus récents, ou les nouveaux paramètres peuvent ne pas être enregistrés dans l’emplacement de stockage des paramètres. L’utilisation d’un serveur de temps permet à UE-V de garantir une utilisation homogène des paramètres.

## <a href="" id="bkmk-performancecapacityplanning"></a>Planification des performances et de la capacité


La capacité requise pour UE-V peut être déterminée à l’aide de la capacité de disque standard et de la surveillance de l’état du réseau. UE-V utilise un partage SMB (Server Message Block) pour le stockage des packages de paramètres. La taille des packages varie en fonction des informations de paramètres d’une application spécifique. Bien que la plupart des packages de paramètres soient petits, la synchronisation de fichiers potentiellement volumineux, tels que les images de bureau, peut entraîner une médiocre performance, en particulier sur les réseaux plus lents. Pour limiter les problèmes liés à la latence du réseau, vous devez créer des emplacements de stockage des paramètres sur les mêmes réseaux locaux où résident les ordinateurs des utilisateurs.

Par défaut, la synchronisation UE-V va expirer après 2 secondes si le réseau est lent ou si le package de paramètres est volumineux. Vous pouvez configurer le délai d’expiration avec une stratégie de groupe. Pour plus d’informations sur la façon de définir le délai d’expiration, reportez-vous à la rubrique [configuration d’UE-V avec des objets de stratégie de groupe](configuring-ue-v-with-group-policy-objects.md).

## Rubriques connexes


[Microsoft User Experience Virtualization (UE-V)1.0](index.md)

[Planification pour UE-V1.0](planning-for-ue-v-10.md)

[Configurations prises en charge pour UE-V1.0](supported-configurations-for-ue-v-10.md)

 

 





