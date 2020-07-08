---
title: Onglet général des propriétés de virtualisation des applications
description: Onglet général des propriétés de virtualisation des applications
author: dansimp
ms.assetid: be7449d9-171a-4a11-9382-83b7008ccbdd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6ee00bfc7f70ee7b17da42aad61356540a7a0be0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808006"
---
# Propriétés d'Application Virtualization: onglet Général


Utilisez l’onglet **général** de la boîte de dialogue **Propriétés de virtualisation d’application** pour modifier les paramètres du journal et les emplacements des données.

Cet onglet contient les éléments suivants.

<a href="" id="log-level"></a>**Niveau du journal**  
Sélectionnez le niveau dans la liste déroulante. Le niveau par défaut est **informations**.

<a href="" id="reset-log"></a>**Réinitialiser le journal**  
Cliquez sur ce bouton pour sauvegarder le fichier journal actuel et commencer immédiatement un nouveau fichier journal.

<a href="" id="location"></a>**Location**  
Accédez à l’emplacement où vous souhaitez enregistrer le fichier journal sftlog.txt. Les emplacements par défaut sont les suivants:

-   Pour WindowsXP, Windows Server2003 —*C:\\Documents et settings\\All users\\application Data\\Microsoft\\Application client de virtualisation*

-   Pour Windows Vista, Windows 7, Windows Server 2008 —*client de virtualisation C:\\ProgramData\\Microsoft\\Application*

<a href="" id="system-log-level"></a>**Niveau du journal système**  
Sélectionnez le niveau dans la liste déroulante. Le niveau par défaut est **Avertissement**.

**Remarques**  Le paramètre **niveau du journal système** contrôle le niveau de messages envoyés au journal des événements système. Les messages enregistrés s’affichent de la même façon que les messages qui sont enregistrés dans le journal des événements du client, mais qui sont stockés dans un autre emplacement sans limitations d’espace du journal des événements client. Dans la mesure où le journal des événements système ne présente pas de limitations d’espace, il convient idéalement pour les situations dans lesquelles la journalisation détaillée est nécessaire.

 

<a href="" id="global-data-directory"></a>**Global Data Directory**  
Accédez à l’emplacement du répertoire du fichier journal. Les emplacements par défaut sont les suivants:

-   Pour WindowsXP, Windows Server2003 —*C:\\Documents et settings\\All users\\application Data\\Microsoft\\Application client de virtualisation*

-   Pour Windows Vista, Windows 7, Windows Server 2008 —*client de virtualisation C:\\ProgramData\\Microsoft\\Application*

<a href="" id="user-data-directory"></a>**Répertoire de données utilisateur**  
Accédez à l’emplacement du répertoire où se trouvent les données propres à l’utilisateur. La valeur par défaut est% APPDATA%. Ce chemin doit être une variable d’environnement valide sur l’ordinateur client.

## Rubriques connexes


[Client Management Console: propriétés d'Application Virtualization](client-management-console-application-virtualization-properties.md)

 

 





