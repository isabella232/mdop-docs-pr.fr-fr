---
title: Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0SP1
description: Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0SP1
author: dansimp
ms.assetid: 447fae0c-fe87-4d1c-b616-6f92fbdaf6d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8584999d9fdbdfccc3e9b2b1486cb97635475747
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804261"
---
# Notes de publication pour Microsoft User Experience Virtualization (UE-V)1.0SP1


Pour effectuer une recherche dans les notes de publication de Microsoft User Interface (UE-V) 1,0 Service Pack 1, appuyez sur Ctrl + F.

Nous vous conseillons de lire soigneusement ces notes de publication avant d’installer UE-V. Les notes de publication contiennent des informations nécessaires à l’installation réussie de la virtualisation de l’interface utilisateur et contiennent des informations supplémentaires qui ne sont pas disponibles dans la documentation du produit. S’il existe des différences entre ces notes de publication et d’autres documents UE-V, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## UE-V problèmes connus


Cette section contient des notes de publication relatives à l’utilisation de User Virtualization 1,0 SP1.

### Les paramètres de registre ne peuvent pas être synchronisés entre les applications App-V et natives sur le même ordinateur

Lorsqu’un ordinateur dispose d’une application disponible via l’application Application Virtualization (App-V) et une application d’installation Native installée avec un programme d’installation Windows (fichier. msi), les paramètres basés sur le registre ne sont pas synchronisés entre les technologies.

SOLUTION: pour résoudre ce problème, exécutez l’application en sélectionnant l’une des deux technologies, mais pas les deux.

### <a href="" id="windows-8-setting-synchronization-fails-when-network-share-is-outside-user-s-domain"></a>La synchronisation de paramètres de Windows 8 échoue lorsque le partage réseau se trouve hors du domaine de l’utilisateur

Lorsque Windows® 8 tente d’utiliser la synchronisation des paramètres du système d’exploitation, l’synchrnization échoue avec le message d’erreur suivant: **Boost:: FileSystem:: exists: nom d’utilisateur ou mot de passe incorrect**. Cette erreur peut indiquer que le partage réseau se trouve en dehors du domaine de l’utilisateur. Pour vérifier les événements du journal opérationnel, ouvrez l' **Observateur d’événements** et naviguez jusqu’à **applications et services consigne**le fonctionnement de l’enregistrement de la virtualisation de l'  /  **Microsoft**  /  **interface utilisateur**de Microsoft  /  **Logging**  /  **Operational**. Les partages réseau utilisés pour les emplacements de stockage des paramètres UE-V doivent résider dans le même domaine Active Directory que l’utilisateur.

SOLUTION: utilisez les partages réseau du même domaine Active Directory que l’utilisateur. .

### Signature électronique de signature pour Outlook 2010

UE-V va itinérance des fichiers de signature Outlook 2010 entre les appareils. Toutefois, les options de signature par défaut pour les nouveaux messages et les réponses/transferts ne sont pas itinérantes. Ces deux paramètres sont stockés dans le profil Outlook, dont UE-V n’est pas itinérant.

Solution de contournement: aucune.

### Les paramètres de synchronisation ne sont pas synchronisés à l’intervalle attendu lors de l’exécution en mode de liaison lente

Dans des conditions normales, les emplacements de stockage des paramètres doivent être disponibles sur une connexion réseau rapide. Le mode de liaison lente est uniquement exécuté de manière périodique. Par défaut, la planification de la synchronisation du mode de liaison lente est définie sur toutes les 360 minutes.

Solution de contournement: pour modifier la fréquence de synchronisation en arrière-plan des ordinateurs en mode de liaison lente, vous pouvez configurer la stratégie de groupe pour la stratégie de synchronisation en arrière-plan pour les **fichiers en mode hors connexion**.

### Les caractères spéciaux ne sont pas synchronisés

Certains caractères, tels que les symboles monétaires, ne sont pas synchronisés entre les ordinateurs Windows 7 et Windows 8 qui exécutent l’agent UE-V.

Solution de contournement: aucune.

### UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits de Microsoft Office

Nous vous recommandons d’installer la version 32 bits de Microsoft Office pour les systèmes d’exploitation 32 bits et 64 bits. Pour choisir la version de Microsoft Office dont vous avez besoin, cliquez ici ( [http://office.microsoft.com/word-help/choose-the-32-bit-or-64-bit-version-of-microsoft-office-HA010369476.aspx](https://go.microsoft.com/fwlink/?LinkID=247623) ). UE-V prend en charge les paramètres d’itinérance entre les différentes versions de l’architecture d’Office. Par exemple, les paramètres d’Office 32 bits s’itinérance entre toutes les instances Office 32 bits. UE-V ne prend pas en charge les paramètres d’itinérance entre les versions 32 bits et 64 bits d’Office.

Solution de contournement: aucune

### <a href="" id="msi-s-are-not-localized"></a>Les MSI ne sont pas localisés

UE-V 1,0 SP1 inclut un programme d’installation localisé pour les agents UE-V et UE-V. Ils sont toujours disponibles, mais l’interface utilisateur est réduite et l’affichage du MSI uniquement en anglais. Malgré le fichier en anglais, le programme d’installation installe toutes les langues prises en charge lors de l’installation.

Solution de contournement: aucune

### Les autres dossiers du partage avec l’emplacement de stockage des paramètres ne sont pas disponibles en mode de connexion lente.

Les partages du magasin de valeurs doivent se trouver sur un partage réseau qui est utilisé pour les autres dossiers qui doivent toujours être disponibles. Lorsque le partage réseau qui héberge l’emplacement de stockage des paramètres passe en mode de connexion lente, le seul dossier disponible est le dossier d’emplacement de stockage des paramètres. Les autres dossiers du partage ne sont pas disponibles en mode de connexion lente.

Solution de contournement: aucune

### Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants

Les favicons associés à des favoris Internet Explorer 9 ne sont pas itinérants par la virtualisation de l’interface utilisateur et qui n’apparaissent pas à la première apparition des favoris sur un nouvel ordinateur.

SOLUTION: favicons apparaît avec les favoris associés une fois que le signet est utilisé et mis en cache dans le navigateur Internet Explorer 9.

### Les chemins d’accès aux paramètres de fichier sont stockés dans le registre

Certains paramètres d’application stockent les chemins d’accès de leurs fichiers de configuration et de paramètres en tant que valeurs dans le registre. Les fichiers référencés sous forme de chemin d’accès dans le registre doivent être synchronisés lorsque les paramètres sont itinérants entre les ordinateurs.

Solution de contournement: utilisez la redirection de dossiers ou d’autres technologies pour vous assurer que tous les fichiers référencés comme chemins d’accès aux paramètres de fichier sont présents et placés au même emplacement sur tous les ordinateurs dans lesquels les paramètres sont itinérants.

### Les chemins de stockage de paramètres longs peuvent générer une erreur

Le raccourci de stockage des paramètres reste le plus court possible. Les chemins longs peuvent empêcher la résolution ou la synchronisation. UE-V utilise le chemin de stockage des paramètres dans le cadre du chemin d’accès calculé au stockage des paramètres. Ce chemin d’accès est calculé comme suit: Path Storage path + "settingspackages" + package dir (ID de modèle) + nom du package (ID de modèle). Si le chemin d’accès calculé est supérieur à 260 caractères, le stockage du package échoue et génère le message d’erreur suivant dans le journal des événements de fonctionnement d’UE-V:

`[boost::filesystem::copy_file: The system cannot find the path specified]`

Pour vérifier les événements du journal opérationnel, ouvrez l’observateur d’événements et naviguez jusqu’à la section journaux des applications et des services/Microsoft/User-Virtualization/Logging/Operations.

Solution de contournement: aucune.

### UE-V agent retarde lors de la connexion ou de la connexion

Si une connexion ou une connexion se produit avant que les fichiers hors connexion n’aient déterminé qu’une liaison lente est en place, la déconnexion ou la connexion peuvent être retardées. La fonctionnalité fichiers en mode hors connexion ne doit pas durer jusqu’à trois minutes pour détecter l’état actuel du réseau. Si la connexion ou l’arrêt se produit avant que les fichiers hors connexion n’aient déterminé que l’ordinateur est connecté à une liaison lente, le package de paramètres d’UE-V sera envoyé au serveur au lieu du cache local.

Solution de contournement: aucune.

### Conflit de paramètres lors de la tentative d’itinérance des paramètres du système d’exploitation sur Windows 8

Dans Windows 8, si la synchronisation de compte Microsoft est activée avec UE-V pour les paramètres du système d’exploitation, les paramètres appliqués peuvent être incohérents.

Solution de contournement: effectuez l’une des opérations suivantes:

-   Désactiver la synchronisation des comptes Microsoft si vous utilisez UE-V pour itinérance dans les paramètres du système d’exploitation

-   Désactiver UE-V pour les paramètres du système d’exploitation

### Certains paramètres du système d’exploitation ne suivent que les versions du système d’exploitation

Les paramètres du système d’exploitation pour le narrateur et les caractères de devise spécifiques aux paramètres régionaux ne seront itinérants que sur les versions de système d’exploitation Windows. Par exemple, les caractères monétaires ne seront déplacés que de Windows 7 vers Windows 7.

Solution de contournement: aucune

 

 





