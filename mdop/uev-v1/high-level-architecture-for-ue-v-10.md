---
title: Architecture de haut niveau pour UE-V1.0
description: Architecture de haut niveau pour UE-V1.0
author: dansimp
ms.assetid: d54f9f10-1a4d-4e56-802d-22d51646e1cc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 76703cf4c7297401e6516830bf194cef741d60ec
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812150"
---
# Architecture de haut niveau pour UE-V1.0


Cette rubrique décrit les éléments architecturaux de haut niveau de la solution d’itinérance des paramètres Microsoft User Interface Virtualization (UE-V). Les éléments suivants font partie d’un déploiement UE-V standard.

![diagramme de l’architecture UE-v](images/ue-vagentarchitecturaldiagram.gif)

L’agent UE-V surveille les applications et les processus du système d’exploitation tels qu’ils sont identifiés dans les modèles d’emplacement des paramètres d’UE-V. Au démarrage de l’application ou du système d’exploitation, les paramètres sont lus à partir du package de paramètres et appliqués à l’ordinateur. Lorsque l’application se ferme ou que le système d’exploitation est verrouillé ou arrêté, les paramètres sont enregistrés dans un package de paramètres d’UE-V dans l’emplacement de stockage des paramètres.

## Emplacement de stockage des paramètres


L’emplacement de stockage des paramètres est un partage de fichiers auquel l’agent de virtualisation accède pour lire et écrire des paramètres. Cet emplacement est le répertoire de base de l’annuaire Active Directory ou défini au cours de l’installation d’UE-V. Vous pouvez définir l’emplacement de l’installation de l’agent UE-V ou vous pouvez le faire par la suite via une stratégie de groupe, WMI ou PowerShell. L’emplacement peut être situé sur n’importe quel partage de fichiers commun auquel les utilisateurs peuvent accéder. Si aucun emplacement de stockage de paramètres n’est défini lors de l’installation, UE-V utilisera le répertoire de base dans Active Directory. L’agent UE-V vérifie l’emplacement et crée un dossier système masqué à l’utilisateur dans lequel stocker et accéder aux paramètres de l’utilisateur. Pour plus d’informations sur le stockage des paramètres, voir [préparer votre environnement pour UE-V](preparing-your-environment-for-ue-v.md).

## Agent UE-V


L’agent UE-V est installé sur chaque ordinateur avec les paramètres qui sont synchronisés par la virtualisation de l’utilisation de l’utilisateur. L’agent surveille les applications inscrites et le système d’exploitation pour toute modification apportée aux paramètres, et synchronise ces paramètres entre les ordinateurs. Les paramètres sont appliqués à partir de l’emplacement de stockage des paramètres vers l’application au démarrage de l’application. Les paramètres sont ensuite enregistrés dans l’emplacement de stockage des paramètres à la fermeture de l’application. Les paramètres du système d’exploitation sont appliqués lors de l’ouverture de session de l’utilisateur, lorsque l’ordinateur est déverrouillé ou lorsque l’utilisateur se connecte à distance à l’ordinateur à l’aide du protocole RDP (Remote Desktop Protocol). L’agent enregistre les paramètres lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé ou lorsqu’une connexion à distance est déconnectée. Pour plus d’informations sur l’agent UE-V, voir [préparation de votre environnement pour UE-v](preparing-your-environment-for-ue-v.md).

## <a href="" id="bkmk-settingslocationtemplate"></a>Modèles d’emplacement des paramètres


Le modèle d’emplacement des paramètres est un fichier XML qui définit les emplacements des paramètres à surveiller par la virtualisation de l’utilisation de l’utilisateur. Seuls les emplacements de paramètres définis dans ces modèles de paramètres sont capturés ou appliqués sur des ordinateurs exécutant l’agent UE-V. Le modèle d’emplacement des paramètres ne contient pas de valeurs de paramètres, uniquement les emplacements où les valeurs sont stockées sur l’ordinateur.

UE-V inclut un ensemble de modèles d’emplacement des paramètres qui spécifient les emplacements des paramètres pour certains paramètres Windows et applications Microsoft. Un administrateur peut créer des modèles d’emplacement des paramètres personnalisés à l’aide du générateur UE-V.

[Planification des applications à synchroniser avec UE-V1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planification du déploiement de modèle personnalisé d'UE-V1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Utilisation de modèles UE-V personnalisés et du Générateur UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## Packages de paramètres


Les paramètres d’application et les paramètres Windows sont stockés dans des packages de paramètres créés par l’agent UE-V. Un package de paramètres est une collection de paramètres qui sont représentés dans les modèles d’emplacement des paramètres. Ces packages de paramètres sont intégrés, stockés localement, puis copiés dans l’emplacement de stockage des paramètres. Le "dernier enregistrement gagne" détermine quels sont les paramètres qui sont conservés lorsqu’un utilisateur unique synchronise les plus d’un ordinateur à un emplacement de stockage. L’agent qui s’exécute sur un ordinateur lit et écrit à l’emplacement des paramètres indépendamment des agents qui s’exécutent sur d’autres ordinateurs. Les paramètres et valeurs récemment écrits sont appliqués lorsque l’agent suivant lit à partir de l’emplacement de stockage des paramètres.

![processus du générateur UE-v](images/ue-vgeneratorprocess.gif)

## Catalogue de modèles de paramètres


Le catalogue de modèles de paramètres correspond au chemin d’accès d’un dossier sur les ordinateurs UE-V ou un partage réseau de blocs de messages serveur (SMB) qui stocke tous les modèles d’emplacement des paramètres personnalisés. L’agent UE-V récupère les modèles nouveaux ou mis à jour à partir de cet emplacement. L’agent UE-V vérifie cet emplacement une fois par jour et il met à jour son comportement de synchronisation en fonction des modèles figurant dans ce dossier. Les modèles ajoutés ou mis à jour dans ce dossier depuis la dernière vérification sont inscrits par l’agent UE-V. UE-V agent annule les modèles supprimés de ce dossier. Les modèles sont inscrits et annulés une fois par jour par le planificateur de tâches. Si vous n’utilisez que les modèles d’emplacement des paramètres par défaut qui sont inclus dans UE-V, il est inutile d’utiliser un catalogue de modèles de paramètres. Pour plus d’informations sur les paramètres des catalogues de déploiement, voir [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Générateur de virtualisation d’utilisation de l’utilisateur


Le générateur de virtualisation des utilisateurs vous permet de créer des modèles d’emplacement des paramètres personnalisés qui stockeront les emplacements des applications qui sont utilisées dans l’entreprise et que vous souhaitez inclure dans la solution des paramètres d’itinérance. Le générateur UE-V cherche à découvrir les emplacements des valeurs de Registre et les fichiers de paramètres des applications, puis enregistre ces emplacements dans un fichier XML de modèle d’emplacement des paramètres. Vous pouvez ensuite distribuer ces modèles d’emplacement des paramètres sur les ordinateurs des utilisateurs. Le générateur UE-V permet également à un administrateur de modifier un modèle existant ou de valider un modèle qui a été créé dans un autre éditeur XML.

Le générateur UE-V analyse une application pour découvrir et enregistrer le lieu de stockage de ses paramètres. Pour ce faire, il surveille l’emplacement de lecture ou d’écriture de l’application dans le registre HKEY \ _CURRENT \ _USER ou dans les dossiers de fichiers sous **utilisateurs** \ \ \ [nom d’utilisateur \] **\ \**  \\  AppData**itinérance et utilisateurs** \ \ \ [nom d’utilisateur \] \ \ **AppData**  \\  **local**.

Le processus de découverte exclut les clés de Registre et les fichiers auxquels l’utilisateur connecté ne peut pas écrire de valeurs. Aucun d’entre eux n’est inclus dans le fichier XML. Le processus de découverte exclut également les clés de Registre et les fichiers associés aux fonctionnalités principales du système d’exploitation Windows.

Pour plus d’informations sur le générateur UE-V, voir [installation du générateur UE-v](installing-the-ue-v-generator.md).

## Rubriques connexes


[Microsoft User Experience Virtualization (UE-V)1.0](index.md)

[Prise en main de User Experience Virtualization1.0](getting-started-with-user-experience-virtualization-10.md)

[À propos d'User Experience Virtualization1.0](about-user-experience-virtualization-10.md)

[Utilisation de modèles UE-V personnalisés et du Générateur UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





