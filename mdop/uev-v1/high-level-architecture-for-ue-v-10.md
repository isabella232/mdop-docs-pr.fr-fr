---
title: Architecture de haut niveau pour UE-V 1.0
description: Architecture de haut niveau pour UE-V 1.0
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
ms.openlocfilehash: b54a9a207f9b74ad3d028cf4ab1f9842d59b0b3a
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910449"
---
# <a name="high-level-architecture-for-ue-v-10"></a>Architecture de haut niveau pour UE-V 1.0


Cette rubrique décrit les éléments architecturaux de haut niveau de la solution d’itinérance Microsoft User Experience Virtualization (UE-V). Les éléments suivants font partie d’un déploiement UE-V standard.

![Diagramme architectural de l’agent ue-v.](images/ue-vagentarchitecturaldiagram.gif)

L’agent UE-V contrôle les applications et les processus du système d’exploitation tels qu’ils sont identifiés dans les modèles UE-V d’emplacement des paramètres. Au démarrage de l’application ou du système d’exploitation, les paramètres sont lus à partir du package de paramètres et appliqués à l’ordinateur. Lorsque l’application se ferme ou lorsque le système d’exploitation est verrouillé ou arrêté, les paramètres sont enregistrés dans un package de paramètres UE-V situé à l’emplacement de stockage des paramètres.

## <a name="settings-storage-location"></a>Paramètres de stockage


L’emplacement de stockage des paramètres est un partage de fichiers accessible par l’agent de virtualisation de l’expérience utilisateur aux paramètres de lecture et d’écriture. Cet emplacement est soit le répertoire d’accueil Active Directory, soit défini pendant l’installation UE-V’installation. Vous pouvez définir l’emplacement pendant l’installation de l’agent UE-V, ou vous pouvez le définir ultérieurement avec la stratégie de groupe, WMI ou PowerShell. L’emplacement peut se trouver sur n’importe quel partage de fichiers commun accessible aux utilisateurs. Si aucun emplacement de stockage de paramètre n’est définie pendant l’installation, UE-V utilisera le répertoire d’accueil dans Active Directory. L’agent UE-V vérifie l’emplacement et crée un dossier système qui est masqué à l’utilisateur dans lequel stocker et accéder aux paramètres utilisateur. Pour plus d’informations sur le stockage des paramètres, voir [Préparation de votre](preparing-your-environment-for-ue-v.md)environnement pour UE-V .

## <a name="ue-v-agent"></a>UE-V Agent


L’agent UE-V est installé sur chaque ordinateur avec des paramètres synchronisés par la virtualisation de l’expérience utilisateur. L’agent surveille les applications inscrites et le système d’exploitation pour les modifications apportées aux paramètres et synchronise ces paramètres entre les ordinateurs. Paramètres sont appliquées à partir de l’emplacement de stockage des paramètres à l’application au début de l’application. Les paramètres sont ensuite enregistrés à l’emplacement de stockage des paramètres lorsque l’application se ferme. Les paramètres du système d’exploitation sont appliqués lorsque l’utilisateur se connecte, lorsque l’ordinateur est déverrouillé ou lorsqu’il se connecte à distance à l’ordinateur à l’aide du protocole RDP (Remote Desktop Protocol). L’agent enregistre les paramètres lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé ou lorsqu’une connexion distante est déconnectée. Pour plus d’informations sur l’agent UE-V, voir [Préparation de votre](preparing-your-environment-for-ue-v.md)environnement pour UE-V .

## <a name="settings-location-templates"></a><a href="" id="bkmk-settingslocationtemplate"></a>Paramètres d’emplacement


Le modèle d’emplacement des paramètres est un fichier XML qui définit les emplacements de paramètres à surveiller par la virtualisation de l’expérience utilisateur. Seuls les emplacements de paramètres définis dans ces modèles de paramètres sont capturés ou appliqués sur les ordinateurs exécutant l’agent UE-V. Le modèle d’emplacement des paramètres ne contient pas de valeurs de paramètres, mais uniquement les emplacements où les valeurs sont stockées sur l’ordinateur.

UE-V comprend un ensemble de modèles d’emplacement de paramètres qui spécifient des emplacements de paramètres pour certaines applications Microsoft et des Windows paramètres. Un administrateur peut créer des modèles d’emplacement de paramètres personnalisés à l’aide UE-V Générateur.

[Planification des applications à synchroniser avec UE-V 1.0](planning-which-applications-to-synchronize-with-ue-v-10.md)

[Planification du déploiement de modèle personnalisé d'UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md)

[Utilisation de modèles UE-V personnalisés et du Générateur UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

## <a name="settings-packages"></a>Paramètres packages


Les paramètres d Windows et les paramètres d’Windows sont stockés dans des packages de paramètres créés par l’agent UE-V. Un package de paramètres est une collection de paramètres qui sont représentés dans les modèles d’emplacement des paramètres. Ces packages de paramètres sont créés, stockés localement, puis copiés dans l’emplacement de stockage des paramètres. « Dernière écriture l’emporte » détermine quels paramètres sont conservés lorsqu’un utilisateur unique synchronise plusieurs ordinateurs avec un emplacement de stockage. L’agent qui s’exécute sur un ordinateur lit et écrit à l’emplacement des paramètres indépendamment des agents qui s’exécutent sur d’autres ordinateurs. Les derniers paramètres et valeurs écrits sont appliqués lorsque l’agent suivant lit à partir de l’emplacement de stockage des paramètres.

![Processus du générateur ue-v.](images/ue-vgeneratorprocess.gif)

## <a name="settings-template-catalog"></a>Paramètres catalogue de modèles


Le catalogue de modèles de paramètres est un chemin d’accès de dossier sur des ordinateurs UE-V ou un partage réseau SMB (Server Message Block) qui stocke tous les modèles d’emplacement des paramètres personnalisés. L’agent UE-V récupère les modèles nouveaux ou mis à jour à partir de cet emplacement. L’agent UE-V vérifie cet emplacement une fois par jour et met à jour son comportement de synchronisation en fonction des modèles de ce dossier. Les modèles ajoutés ou mis à jour dans ce dossier depuis la dernière vérification sont enregistrés par l’agent UE-V. L UE-V agent désinsère les modèles qui ont été supprimés de ce dossier. Les modèles sont enregistrés et désinsérés une fois par jour par le programmeur de tâches. Si vous utilisez uniquement les modèles d’emplacement de paramètres par défaut inclus dans UE-V, un catalogue de modèles de paramètres est inutile. Pour plus d’informations sur les catalogues de déploiement de paramètres, voir [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).

## <a name="user-experience-virtualization-generator"></a>User Experience Virtualization Generator


Le Générateur de virtualisation d’expérience utilisateur vous permet de créer des modèles d’emplacement de paramètres personnalisés qui stockent les emplacements de paramètres des applications utilisées dans l’entreprise et que vous souhaitez inclure dans la solution de paramètres d’itinérance. Le générateur UE-V recherchera les emplacements des valeurs de Registre et les fichiers de paramètres des applications, puis enregistrera ces emplacements dans un fichier XML de modèle d’emplacement de paramètres. Vous pouvez ensuite distribuer ces modèles d’emplacement de paramètres aux ordinateurs des utilisateurs. Le générateur UE-V permet également à un administrateur de modifier un modèle existant ou de valider un modèle créé avec un autre éditeur XML.

Le générateur UE-V surveille une application pour découvrir et enregistrer l’endroit où elle stocke ses paramètres. Pour ce faire, il surveille l’endroit où l’application lit ou écrit dans le Registre HKEY\_CURRENT\_USER ou dans les dossiers de fichiers sous **Utilisateurs** \\ \[Nom d’utilisateur\] \\ **Itinérance AppData**et Utilisateurs  \\  **** \\ \[Nom d’utilisateur\] \\ **AppData**  \\  **Local**.

Le processus de découverte exclut les clés de Registre et les fichiers dans lesquels l’utilisateur connecté ne peut pas écrire de valeurs. Aucun de ces éléments ne sera inclus dans le fichier XML. Le processus de découverte exclut également les clés de Registre et les fichiers associés aux fonctionnalités principales du Windows d’exploitation.

Pour plus d’informations sur UE-V générateur de UE-V, voir [Installing the UE-V Generator](installing-the-ue-v-generator.md).

## <a name="related-topics"></a>Rubriques associées


[Microsoft User Experience Virtualization (UE-V) 1.0](index.md)

[Prise en main de User Experience Virtualization 1.0](getting-started-with-user-experience-virtualization-10.md)

[À propos d'User Experience Virtualization 1.0](about-user-experience-virtualization-10.md)

[Utilisation de modèles UE-V personnalisés et du Générateur UE-V](working-with-custom-ue-v-templates-and-the-ue-v-generator.md)

 

 





