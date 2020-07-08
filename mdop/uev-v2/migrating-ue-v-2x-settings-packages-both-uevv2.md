---
title: Migration des packages de paramètres UE-V 2. x
description: Migration des packages de paramètres UE-V 2. x
author: dansimp
ms.assetid: f79381f4-e142-405c-b728-5c048502aa70
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0aa1f1c36594d69de40306dfa70a4a0cf5c86dbb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811202"
---
# Migration des packages de paramètres UE-V 2. x


Dans le cycle de vie d’un déploiement de Microsoft User Interface Virtualization (UE-V) 2,0, 2,1 ou 2,1 SP1, vous devrez peut-être replacer les packages de paramètres utilisateur lorsque vous migrez vers un nouveau serveur ou lorsque vous effectuez des sauvegardes. Il est possible que vous deviez migrer les packages de paramètres dans les cas suivants:

-   Effectuez la mise à niveau du matériel du serveur existant vers un serveur plus moderne.

-   Migration d’un emplacement de stockage des paramètres vers un serveur de production depuis un serveur de test.

Le simple fait de copier les fichiers et dossiers ne conserve pas les paramètres de sécurité et les autorisations. Les étapes suivantes décrivent la copie correcte du package de paramètres avec ses autorisations de système de fichiers NTFS vers un nouveau partage.

**Pour conserver les packages de paramètres d’UE-V 2 lors de la migration vers un nouveau serveur**

1.  Dans un nouvel emplacement sur un autre serveur, créez un dossier, par exemple, MySettings.

2.  Désactivez le partage pour l’ancien dossier partage sur l’ancien serveur.

3.  Pour copier les packages de paramètres existants sur le nouveau serveur avec Robocopy

    ``` syntax
    C:\start robocopy "\\servername\E$\MySettings" "\\servername\E$\MySettings" /b /sec /secfix /e /LOG:D:\Robocopylogs\MySettings.txt
    ```

    **Remarques**  Pour surveiller la progression de la copie, ouvrez MySettings.txt à l’aide d’une visionneuse de journaux telle que trace32.

     

4.  Accordez des autorisations de niveau partage au nouveau partage. Laissez les autorisations du système de fichiers NTFS telles qu’elles ont été définies par Robocopy.

    Sur les ordinateurs qui exécutent l’agent UE-V, mettez à jour le paramètre de configuration **SettingsStoragePath** sur le chemin UNC (Universal Naming Convention) du nouveau partage.

    Vous **avez une suggestion pour UE-V**? Ajoutez ou Votez en fonction [de suggestions.](http://uev.uservoice.com/forums/280428-microsoft-user-experience-virtualization) Vous **avez un problème UE-V**? Utiliser le [Forum de TechNet UE-V](https://social.technet.microsoft.com/Forums/home?forum=mdopuev).

## Rubriques connexes


[Administration d’UE-V 2. x](administering-ue-v-2x-new-uevv2.md)

 

 





