---
title: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique
description: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique
author: dansimp
ms.assetid: 19da3776-5ebe-41e1-9890-12b84ef3c1c7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: e2166b0f280153ad62709b21bb3477d0c4277fcd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805299"
---
# Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique


Utilisez la procédure suivante pour migrer des packages créés avec App-V à l’aide du fichier de configuration utilisateur.

**Remarques**  Cette procédure suppose que vous utilisez la dernière version de App-V 4,6.

**Pour convertir un package**

1. Recherchez le fichier de configuration utilisateur pour le package que vous voulez convertir. Pour définir la stratégie, effectuez les mises à jour suivantes dans la section **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; du package**.

   Voici un exemple de fichier de configuration utilisateur:

   &lt;? XML version = "1.0"&gt;

   &lt;UserConfiguration PackageId = &lt; ID &gt; de package DisplayName = &lt; nom du package&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID de package&gt;

   &lt;/UserConfiguration&gt;

2. Pour ajouter le package App-V 5,1, tapez les informations suivantes dans la fenêtre d’invite de commandes PowerShell avec élévation de privilèges:

   PS &gt; **$pkg = Add-AppvClientPackage-** Path &lt; pour l’emplacement du package&gt;

   &gt;**Publication PS-AppVClientPackage $pkg-chemin DynamicUserConfiguration** &lt; du fichier de configuration de l’utilisateur&gt;

3. Ouvrez l’application à l’aide de FTAs ou raccourcis. L’application doit s’ouvrir à l’aide de App-V 5,1.

   Le package App-V 4,6 et le package App-V 5,1 convertis sont publiés pour l’utilisateur, mais les FTAs et raccourcis des applications ont été supposés par le package App-V 5,1.

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.1](operations-for-app-v-51.md)

[Restauration de points d'extension d'un package App-V5.1 vers un package App-V4.6 pour un utilisateur spécifique](how-to-revert-extension-points-from-an-app-v-51-package-to-an-app-v-46-package-for-a-specific-user.md)

 

 





