---
title: À propos d'User Experience Virtualization1.0
description: À propos d'User Experience Virtualization1.0
author: dansimp
ms.assetid: 3758b100-35a8-4e10-ac08-f583fb8ddbd9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6010f9c4ebc260eec0324fb880dc2c92fd675130
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809521"
---
# À propos d'User Experience Virtualization1.0


Microsoft User Interface Virtualization (UE-V) vérifie les modifications apportées par les utilisateurs aux paramètres d’application et aux paramètres du système d’exploitation Windows. Les paramètres utilisateur sont capturés et centralisés vers un emplacement de stockage des paramètres. Ces paramètres peuvent ensuite être appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).

La virtualisation de l’interface utilisateur utilise les modèles d’emplacement des paramètres pour spécifier les applications et les paramètres Windows sur les ordinateurs des utilisateurs qui sont surveillés et centralisés. Le modèle d’emplacement des paramètres est un fichier XML qui spécifie le fichier et les emplacements du Registre associés à chaque paramètre de l’application ou du système d’exploitation. Le modèle ne contient pas de valeurs pour les paramètres. Il contient uniquement les emplacements des paramètres à surveiller.

Les paramètres de l’application et les paramètres Windows sont surveillés par UE-V lorsque les utilisateurs travaillent sur leur ordinateur. Les valeurs des paramètres de l’application sont stockées sur le serveur de stockage de paramètres lorsque l’utilisateur ferme l’application. Les valeurs des paramètres Windows sont stockées lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé, ou lorsqu’il se déconnecte à distance à partir d’un ordinateur.

Un administrateur peut créer un modèle d’emplacement des paramètres UE-V pour spécifier quels paramètres d’application d’entreprise seront itinérants. UE-V inclut un ensemble de modèles d’emplacement pour certains paramètres de l’application Microsoft et de Windows. Pour obtenir la liste des applications et paramètres par défaut dans UE-V, voir [planification des applications à synchroniser avec UE-v 1,0](planning-which-applications-to-synchronize-with-ue-v-10.md).

## Notes de publication de UEV 1,0


Pour plus d’informations et pour les actualités de dernière minute qui n’ont pas été intégrées à la documentation, voir [notes de publication de Microsoft User Interface Virtualization (UE-V) 1,0](microsoft-user-experience-virtualization--ue-v--10-release-notes.md).

## Rubriques connexes


[Prise en main de User Experience Virtualization1.0](getting-started-with-user-experience-virtualization-10.md)

[Microsoft User Experience Virtualization (UE-V)1.0](index.md)

[Architecture de haut niveau pour UE-V1.0](high-level-architecture-for-ue-v-10.md)

 

 





