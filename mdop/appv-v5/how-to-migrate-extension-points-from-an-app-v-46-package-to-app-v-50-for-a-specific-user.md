---
title: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique
description: Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique
ms.assetid: dad25992-3c75-4b7d-b4c6-c2edf43baaea
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: a17d9dad11092a4c8356983b70bea3c18da1be04
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805305"
---
# Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique

*Remarque:** App-V 4,6 a quitté la version standard du support technique.

Utilisez la procédure suivante pour migrer des packages créés avec App-V à l’aide du fichier de configuration utilisateur.

**Pour convertir un package**

1. Recherchez le fichier de configuration utilisateur pour le package que vous voulez convertir. Pour définir la stratégie, effectuez les mises à jour suivantes dans la section **userConfiguration** : **ManagingAuthority TakeoverExtensionPointsFrom46 = "true" PackageName = &lt; ID &gt; du package**.

   Voici un exemple de fichier de configuration utilisateur:

   &lt;? XML version = "1.0"&gt;

   &lt;UserConfiguration PackageId = &lt; ID &gt; de package DisplayName = &lt; nom du package&gt;

   xmlns = " <https://schemas.microsoft.com/appv/2010/userconfiguration"&gt> ; &lt; ManagingAuthority TakeoverExtensionPointsFrom46 = "true"

   PackageName = &lt; ID de package&gt;

   &lt;/UserConfiguration&gt;

2. Pour ajouter le package App-V 5,0, tapez ce qui suit dans une invite de commandes PowerShell avec élévation de privilèges:

   PS &gt; **$pkg = Add-AppvClientPackage-** Path &lt; pour l’emplacement du package&gt;

   &gt;**Publication PS-AppVClientPackage $pkg-chemin DynamicUserConfiguration** &lt; du fichier de configuration de l’utilisateur&gt;

3. Ouvrez l’application à l’aide de FTAs ou raccourcis. L’application doit s’ouvrir à l’aide de App-V 5,0.

   Le package App-V SP2 et le package App-V 5,0 converti sont publiés pour l’utilisateur, mais les FTAs et raccourcis des applications ont été supposés par le package App-V 5,0.

   Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 





