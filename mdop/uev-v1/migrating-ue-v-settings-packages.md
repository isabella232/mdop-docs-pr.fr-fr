---
title: Migration des packages de paramètres UE-V
description: Migration des packages de paramètres UE-V
author: dansimp
ms.assetid: 93d99254-3e17-4e96-92ad-87059d8554a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d0087f334e916c06e7611d2671d0b50e7d1dd916
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809816"
---
# Migration des packages de paramètres UE-V


Dans le cycle de vie d’un déploiement de la virtualisation de l’interface utilisateur de Microsoft (UE-V), vous devrez peut-être déplacer les packages de paramètres utilisateur lors de la migration vers un nouveau serveur ou à des fins de sauvegarde. La migration des packages de paramètres peut être nécessaire dans les cas suivants:

-   Effectuez la mise à niveau du matériel du serveur existant vers un serveur plus moderne.

-   Migration d’un emplacement de stockage des paramètres d’un laboratoire vers un serveur de production.

Le simple fait de copier les fichiers et dossiers ne conserve pas les paramètres de sécurité et les autorisations. Les étapes décrites ci-dessous permettent de copier correctement les fichiers du package de paramètres avec leurs autorisations NTFS vers un nouveau partage.

**Conservation des packages de paramètres d’UE-V lors de la migration vers un nouveau serveur**

1.  Dans un nouvel emplacement sur un autre serveur, créez un nouveau dossier. par exemple, MySettings.

2.  Désactivez le partage pour l’ancien dossier partage sur l’ancien serveur.

3.  Déplacez les packages de paramètres existants vers le nouveau serveur avec Robocopy à partir de la ligne de commande. Exemple:

    ``` syntax
    c:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Remarques**  Pour surveiller la progression de la copie, ouvrez MySettings.txt avec un lecteur de fichier journal tel que trace32.

     

4.  Accordez des autorisations de niveau partage au nouveau partage. Laissez les autorisations NTFS telles qu’elles ont été définies par Robocopy.

    Sur les ordinateurs qui exécutent l’agent UE-V, mettez à jour le paramètre de configuration SettingsStoragePath sur le chemin UNC du nouveau partage.

## Rubriques connexes


[Administration d'UE-V1.0](administering-ue-v-10.md)

[Opérations d'UE-V1.0](operations-for-ue-v-10.md)

 

 





