---
title: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique
description: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique
author: dansimp
ms.assetid: 4ef823a5-3106-44c5-aecc-29edf69c2fbb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 7bac244804b46309a0e0a75cb3742dfe22e92e8f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805310"
---
# Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique


Utilisez la procédure suivante pour migrer des points d’extension d’un package App-V 4.6 vers un package App-V 5,1 à l’aide du fichier de configuration de déploiement.

**Remarques**  Cette procédure suppose que vous utilisez la dernière version de App-V 4,6.  
La procédure suivante ne nécessite pas de serveur de gestion 5,1 App-V.

 

**Pour migrer des points d’extension d’un package d’un package App-V 4.6 vers un package App-V 5,1 converti à l’aide du fichier de configuration de déploiement**

1. Recherchez le répertoire contenant le fichier de configuration de déploiement pour le package que vous voulez migrer. Pour définir la stratégie, effectuez la mise à jour suivante vers la section **userConfiguration** :

   **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID de package&gt;**

   Voici un exemple de contenu d’un fichier de configuration de déploiement:

   &lt;? XML version = "1.0"&gt;

   &lt;DeploymentConfiguration

   xmlns = " <https://schemas.microsoft.com/appv/2010/deploymentconfiguration> " PackageId = &lt; ID de package &gt; DisplayName = &lt; nom d’affichage&gt;

   &lt;MachineConfiguration/&gt;

   &lt;UserConfiguration&gt;

   &lt;ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID de package&gt;

   &lt;/UserConfiguration&gt;

   &lt;/DeploymentConfiguration&gt;

2. Pour ajouter le package App-V 5,1, dans une invite de commandes PowerShell avec élévation de privilèges, tapez:

   PS &gt; **$pkg = Add-AppvClientPackage** **-** Path &lt; pour l’emplacement du package &gt;  - **DynamicDeploymentConfiguration** chemin d’accès &lt; au fichier de configuration de déploiement&gt;

   &gt;**Publication PS-AppVClientPackage $pkg**

3. Pour tester la migration, ouvrez l’application virtuelle à l’aide de FTAs ou raccourcis associés. L’application s’ouvre avec App-V 5,1. À la fois, le package App-V 4,6 et le package App-V 5,1 convertis sont publiés pour l’utilisateur, mais les FTAs et raccourcis des applications ont été supposés par le package App-V 5,1.

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour tous les utilisateurs sur un ordinateur spécifique](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-all-users-on-a-specific-computer.md)

[Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





